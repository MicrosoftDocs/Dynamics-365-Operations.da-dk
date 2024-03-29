---
title: Konfigurere tilknytning af kolonnerne for salgsordrestatus
description: Denne artikel forklarer, hvordan du kan konfigurere statuskolonnerne for salgsordre til dobbeltskrivning.
author: dasani-madipalli
ms.date: 06/25/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: damadipa
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 2035985f16b5972e02f1ed60c6f02d306217f3be
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288878"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a>Konfigurere tilknytning af kolonnerne for salgsordrestatus

[!include [banner](../../includes/banner.md)]

De kolonner, der angiver status for salgsordrer, har forskellige fasttekstværdier i Microsoft Dynamics 365 Supply Chain Management og Dynamics 365 Sales. Der kræves yderligere opsætning for at knytte disse kolonner til dobbeltskrivning.

## <a name="columns-in-supply-chain-management"></a>kolonner i Supply Chain Management

I Supply Chain Management afspejler to kolonner status for salgsordren. De kolonner, du skal tilknytte, er **Status** og **Dokumentstatus**.

Fastteksten **Status** angiver ordrens overordnede status. Denne status vises i ordrehovedet.

Fastteksten **Status** har følgende værdier:

- Åben ordre
- Leveret
- Er faktureret
- Annulleret

Fastteksten **Dokumentstatus** angiver det seneste dokument, der blev genereret til ordren. Hvis ordren f.eks. er bekræftet, er dette dokument en salgsordrebekræftelse. Hvis en salgsordre er delvist faktureret, og den resterende linje er bekræftet, forbliver dokumentstatussen **Faktura**, fordi fakturaen genereres senere i processen.

Fastteksten **Dokumentstatus** har følgende værdier:

- Bekræftelse
- Plukliste
- Følgeseddel
- Fakturaer

## <a name="columns-in-sales"></a>kolonner i Salg

I Salg angiver to kolonner status for ordren. De kolonner, du skal tilknytte, er **Status** og **Behandlingsstatus**.

Fastteksten **Status** angiver ordrens overordnede status. Den har følgende værdier:

- Aktive
- Sendt
- Opfyldt
- Er faktureret
- Annulleret

Fastteksten **Behandlingsstatus** blev introduceret, så statussen kan tilknyttes mere præcist ved hjælp af Supply Chain Management.

Følgende tabel viser tilknytningen af **Behandlingsstatus** i Supply Chain Management.

| Behandlingsstatus   | Status i Supply Chain Management | Dokumentstatus i Supply Chain Management |
|---------------------|-----------------------------------|--------------------------------------------|
| Aktive              | Åben ordre                        | None                                       |
| Bekræftet           | Åben ordre                        | Bekræftelse                               |
| Plukket              | Åben ordre                        | Plukliste                               |
| Delvist leveret | Åben ordre                        | Følgeseddel                               |
| Leveret           | Leveret                         | Følgeseddel                               |
| Delvist faktureret  | Leveret                         | Fakturaer                                    |
| Er faktureret            | Er faktureret                          | Fakturaer                                    |
| Annulleret           | Annulleret                         | Ikke anvendelig                             |

Følgende tabel viser tilknytningen af **Behandlingsstatus** mellem Salg og Supply Chain Management.

| Behandlingsstatus   | Status i Salg | Status i Supply Chain Management |
|---------------------|-----------------|-----------------------------------|
| Aktive              | Aktive          | Åben ordre                        |
| Bekræftet           | Sendt       | Åben ordre                        |
| Plukket              | Sendt       | Åben ordre                        |
| Delvist leveret | Aktive          | Åben ordre                        |
| Delvist faktureret  | Aktive          | Åben ordre                        |
| Delvist faktureret  | Opfyldt       | Leveret                         |
| Er faktureret            | Er faktureret        | Er faktureret                          |
| Annulleret           | Annulleret       | Annulleret                         |

## <a name="setup"></a>Konfiguration

Hvis du vil konfigurere tilknytningen af statuskolonnerne for salgsordre, skal du aktivere attributterne **IsSOPIntegrationEnabled** og **isIntegrationUser**.

Hvis du vil aktivere attributten **IsSOPIntegrationEnabled**, skal du følge disse trin.

1. Åbn en browser, og gå til `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`. Erstat **\<test-name\>** med dit firmas link til Salg.
2. På den side, der åbnes, skal du søge efter **organizationid** og notere dig værdien.

    ![Finde organizationid.](media/sales-map-orgid.png)

3. Åbn browserkonsollen i Salg, og kør følgende script. Brug værdien af **organizationid** fra trin 2.

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-kode i browserkonsollen.](media/sales-map-script.png)

4. Kontrollér, at **IsSOPIntegrationEnabled** er angivet til **true**. Brug URL-adressen fra trin 1 til at kontrollere værdien.

    ![IsSOPIntegrationEnabled er angivet til true.](media/sales-map-integration-enabled.png)

Hvis du vil aktivere attributten **isIntegrationUser**, skal du følge disse trin.

1. Gå i Salg til **Indstilling \> Tilpasning \> Tilpas systemet**, vælg **Brugertabel**, og åbn derefter **Formular \> Bruger**.

    ![Åbne brugerformularen.](media/sales-map-user.png)

2. I Feltoversigt skal du finde **Integrationsbrugertilstand** og dobbeltklikke på den for at føje den til formularen. Gem ændringerne.

    ![Tilføje kolonnen Integrationsbrugertilstand i formularen.](media/sales-map-field-explorer.png)

3. Gå i Salg til **Indstilling \> Sikkerhed \> Brugere**, og skift visningen fra **Aktiverede brugere** til **Programbrugere**.

    ![Ændre visningen fra Aktiverede brugere til Programbrugere.](media/sales-map-enabled-users.png)

4. Vælg de to poster for **DualWrite IntegrationUser**.

    ![Liste over programbrugere.](media/sales-map-user-mode.png)

5. Ret værdien i kolonnen **Integrationsbrugertilstand** til **Ja**.

    ![Ændre værdien i kolonnen Integrationsbrugertilstand.](media/sales-map-user-mode-yes.png)

Dine salgsordrer er nu tilknyttet.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
