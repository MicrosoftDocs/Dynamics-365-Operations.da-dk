---
title: Føje en QR-kode eller stregkode til transaktions- og kvitterings-mails
description: Denne artikel forklarer, hvordan du indsætter QR-koder og stregkoder, der repræsenterer ordre-d'er, i transaktions- og kvitteringsmails i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ffa0009c55b5322b209b19692952c2e0704f65c9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872878"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a>Føje en QR-kode eller stregkode til transaktions- og kvitterings-mails

[!include [banner](includes/banner.md)]

Denne artikel forklarer, hvordan du indsætter QR-koder og stregkoder, der repræsenterer ordre-d'er, i transaktions- og kvitteringsmails i Microsoft Dynamics 365 Commerce.

Du kan nemt medtage QR-koder og stregkoder i transaktionsmails for at gøre ordreopslagsprocessen hurtigere i et detailmiljø. Hvis du vil indsætte QR-koder og stregkoder i mails, kan du bruge et HTML **\<img\>**-tag, der anmoder om en QR-kode eller et stregkodebillede fra en tjeneste til generering og gengivelse. Microsoft leverer ikke denne tjeneste. Der findes dog mange gratis tjenester eller tjenester, der fungerer som tjenester, der fungerer som tjenester, der kan fungere som koder for QR, eller stregkoder, som genereres dynamisk på grundlag af en værdi, som overføres i en forespørgselsstreng.

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a>Føje en QR-kode eller stregkode til transaktions-mail

Hvis du vil indsætte en QR-kode eller stregkode i en transaktionsmail, der sendes som en del af et e-handelskøb, skal du følge disse trin.

1. Åbn kilde-HTML-kilde-skabelonen til mailskabelonen til transaktionen, og tilføj et HTML **\<img\>**-tag, der peger på QR-koden eller stregkodetjenesten. Her er et eksempel.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    Her er en forklaring på tidligere eksempler:

    - **DIN\_QR\_KODE\_STREG\_KODE\_TJENESTE** repræsenterer domænet for din QR-kode eller stregkodetjeneste.
    - **data** repræsenterer den parameter, som QR-koden eller stregkodetjenesten bruger til at modtage det indhold, der skal gengives som en QR-kode eller stregkode.

        Værdien **%salesid%** skal tilknyttes denne parameter. Bemærk i dette eksempel, at værdien også bruges som alt. tekst til billedet.

    - **param1** og **param2** repræsenterer yderligere valgfrie parametre.

1. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Skabelon til organisationsmail**, og overfør den opdaterede HTML til den relevante mailskabelon til transaktioner.

> [!NOTE]
> Parametrene kan variere mellem leverandører af QR-kode og stregkoder. Kontakt derfor din leverandør for at bekræfte de parametre, du skal angive værdier til.

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a>Føje en QR-kode eller stregkode til kvitterings-mail 

Hvis du vil indsætte en QR-kode eller stregkode i en kvitteringsmail, der kan sendes, efter at et køb er foretaget på POS, skal du følge disse trin.

1. Åbn kilde-HTML-kilde-skabelonen til mailskabelonen til kvitteringen, og tilføj et HTML **\<img\>**-tag, der peger på QR-koden eller stregkodetjenesten. Herunder følger et eksempel.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    Her er en forklaring på tidligere eksempler:

    - **DIN\_QR\_KODE\_STREG\_KODE\_TJENESTE** repræsenterer domænet for din QR-kode eller stregkodetjeneste.
    - **data** repræsenterer den parameter, som QR-koden eller stregkodetjenesten bruger til at modtage det indhold, der skal gengives som en QR-kode eller stregkode.

        Værdien **%receiptid%** skal tilknyttes denne parameter. Bemærk i dette eksempel, at værdien også bruges som alt. tekst til billedet.

    - **param1** og **param2** repræsenterer yderligere valgfrie parametre.

1. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Skabelon til organisationsmail**, og overfør den opdaterede HTML til den mailskabelon, der indeholder mail-id **emailrecpt**.

> [!NOTE]
> Parametrene kan variere mellem leverandører af QR-kode og stregkoder. Kontakt derfor din leverandør for at bekræfte de parametre, du skal angive værdier til.

## <a name="additional-resources"></a>Yderligere ressourcer

[Sende mailkvitteringer fra Modern POS (MPOS)](email-receipts.md)

[Oprette e-mailskabeloner til transaktionshændelser](email-templates-transactions.md)
