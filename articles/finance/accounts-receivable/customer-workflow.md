---
title: Arbejdsgang for kunde
description: Dette emne indeholder oplysninger om arbejdsgangen for kunden. Du kan ændre bestemte felter for en kunde og derefter sende ændringerne til godkendelse ved hjælp af arbejdsgangen, inden de føjes til kunden.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: a74b8ed226c4e13c8684fe86d4dca7236a84040e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012182"
---
# <a name="customer-workflow"></a>Arbejdsgang for kunde

[!include [banner](../includes/banner.md)]

Arbejdsgangen for kunde er føjet til version 8.0.4. Du kan ændre specifikke felter for en kunde, og derefter sende disse ændringer til godkendelse ved hjælp af arbejdsgangen, før de tilføjes til kunden.

## <a name="set-up-the-customer-workflow"></a>Konfigurer kundens arbejdsgang

Før du kan bruge funktionen for kundens arbejdsgang, skal du aktivere den.

1. Gå til **Debitor \> Opsætning \> Debitorparametre**.
2. På fanen **Generelt** i oversigtspanelet **Kundegodkendelse** skal du angive indstillingen **Aktivér kundegodkendelser** til **Ja** for at aktivere funktionen.
3. I feltet **Dataenheds funktionalitet**, skal du vælge den funktionalitet, som dataenhederne skal bruge, når data importeres:

    - **Tillad ændringer uden godkendelse** – En enhed kan opdatere kundeposten uden at behandle den via arbejdsgangen.
    - **Afvis ændringer** – Ændringerne kan ikke foretage ændringer i kundeposten. Importen vil mislykkes for de felter, der er aktiveret for arbejdsgangen.
    - **Opret forslag til ændring** – Alle felter ændres, undtagen de felter, der er aktiveret for arbejdsgangen. De nye værdier for disse felter vil blive føjet til kunden som forslag til ændringer, og arbejdsgangen startes automatisk.

4. På listen over felter for kunden, skal du derefter vælge afkrydsningsfeltet **Aktivér** for hvert felt, der skal godkendes, før ændringerne kan foretages.
5. Gå til **Debitor \> Opsætning \> Debitorarbejdsgange**.
6. Vælg **Ny**.
7. Vælg **Arbejdsgang for forslag til ændring af kunde**. 
8. Konfigurer arbejdsgangen, så den passer til din godkendelsesproces. Elementet for godkendelsen af arbejdsgangen **Arbejdsgangsgodkendelse af forslag til ændring af kunde** aktiverer ændringerne for kunden.

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a>Rediger kundeoplysninger, og send ændringerne af arbejdsgangen

Når du ændrer et felt, der er aktiveret for arbejdsgangen, vises siden **Forslag til ændringer**. Denne side viser den oprindelige værdi i feltet og den nye værdi, du har angivet. Det felt, du ændrede, vender tilbage til den oprindelige værdi. En statusmeddelelse på siden fortæller dig, at dine ændringer ikke er blevet sendt.

Hver gang du ændrer et felt, der er aktiveret for arbejdsgangen, føjes feltet til listen over foreslåede ændringer. Hvis du vil udelade den foreslåede værdi for et felt, kan du bruge knappen **Udelad** ved siden af feltet på listen. Hvis du vil udelade alle ændringer, skal du bruge knappen **Udelad alle ændringer** nederst på siden. Vælg **OK** for at lukke siden.

Når du har mindst én foreslået ændring, vises der yderligere to menuer i handlingsruden: **Forslag til ændringer** og **Arbejdsgang**.

1. Vælg **Forslag til ændringer** for at åbne siden **Forslag til ændringer** og gennemse dine ændringer.
2. Vælg **Arbejdsgang \> Send** for at sende ændringerne af arbejdsgangen.

    Status på siden ændres til **Ændringer, der afventer godkendelse**.

Arbejdsgangen følger standardprocessen for arbejdsgang i applikationen. Godkenderen dirigeres til siden **Kunde**, hvor ændringerne kan gennemgås på siden **Forslag til ændringer**. Vælg derefter **Arbejdsgang \> Godkend** for at godkende arbejdsgangen. Når alle godkendelser er fuldført, opdateres felterne med de værdier, du foreslog.
