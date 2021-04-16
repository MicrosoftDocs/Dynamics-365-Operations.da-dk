---
title: Arbejdsgang for kreditorer
description: Rediger leverandøroplysninger, og brug arbejdsgange til at godkende dem.
author: mikefalkner
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: e5aef18a7f541c6a0d4abf9d4461d1dd9cd27880
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810264"
---
# <a name="vendor-workflow"></a>Arbejdsgang for kreditorer

[!include [banner](../includes/banner.md)]

Når arbejdsgangen for kreditorer bruges, sendes ændringer, der er foretaget af bestemte felter, til arbejdsgangen til godkendelse, inden de føjes til kreditoren.

## <a name="set-up-the-vendor-workflow"></a>Konfigurere kreditorarbejdsgangen

Du skal aktivere arbejdsgangfunktionen, før du kan bruge den.

1. Gå til **Kreditor \> Opsætning \> Kreditorparametre**.
2. Under fanen **Generelt** på oversigtspanelet **Kreditorgodkendelse** skal du vælge **Ja** i indstillingen **Aktivér kreditorgodkendelser**.
3. I feltet **Dataenheds funktionalitet** skal du vælge den funktionalitet, der skal bruges, når data importeres:

    - **Tillade ændringer uden godkendelse** – Dataenheden kan opdatere kreditorposten uden at behandle den via arbejdsgangen.
    - **Afvis ændringer** – Der kan ikke foretages ændringer af kreditorposten. For de felter, der er aktiveret for arbejdsgangen, mislykkes importen.
    - **Opret forslag til ændring** – Alle felter ændres undtagen de felter, der er aktiveret til arbejdsgangen. De nye værdier for disse felter bliver føjet til kreditoren som foreslåede ændringer, og arbejdsprocessen startes automatisk.

4. På listen over kreditorfelter skal du markere afkrydsningsfeltet **Aktivér** for hvert felt, der skal godkendes, før ændringerne kan udføres.
5. Gå til **Kreditor \> Opsætning \> Kreditorarbejdsgange**.
6. Vælg **Ny**.
7. Vælg **Arbejdsgang for forslag til ændring af kreditor**. 
8. Konfigurer arbejdsgangen, så den passer til godkendelsesprocessen. Elementet til godkendelse af arbejdsgangen **Arbejdsgangsgodkendelse af forslag til ændring af kreditor** anvender ændringerne på kreditoren.

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a>Ændre kreditoroplysninger og sende ændringerne til arbejdsgangen

Når du ændrer et felt, der er aktiveret for arbejdsgangen, vises siden **Foreslåede ændringer**. Denne side viser den oprindelige værdi i feltet og den nye værdi, du har angivet. Det felt, du har ændret, vender tilbage til den oprindelige værdi. En statusmeddelelse fortæller dig også, at ændringerne ikke er sendt. 

Hver gang du ændrer et felt, der er aktiveret for arbejdsgangen, føjes dette felt til listen på siden **Foreslåede ændringer**. For at slette den foreslåede værdi for et felt kan du bruge knappen **Slet** ud for feltet på listen. Hvis du vil slette alle ændringer, skal du bruge knappen **Udelad alle ændringer** nederst på siden. Vælg **OK** for at lukke siden.

Når du har mindst én foreslåede ændring, vises der to ekstra faner i handlingsruden: **Foreslåede ændringer** og **Arbejdsgang**.

1. Vælg **Foreslåede ændringer** for at åbne siden **Foreslåede ændringer** og se dine ændringer.
2. Vælg **Arbejdsgang \> Send for at sende ændringerne til arbejdsgang**.

    Status på siden ændres til **Ændringer, der afventer godkendelse**.

Arbejdsgangen følger standardarbejdsgangsprocessen. Godkenderen dirigeres til siden **Kreditor**, hvor ændringerne kan gennemgås på siden **Forslag til ændringer**. Vælg derefter **Arbejdsgang \> Godkend** for at godkende arbejdsgangen. Når alle godkendelser er fuldført, opdateres felterne med de værdier, du foreslog.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]