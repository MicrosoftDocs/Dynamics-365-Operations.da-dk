---
title: Salgsaftaler
description: Dette emne indeholder oplysninger om salgsaftaler. En salgsaftale er en kontrakt, der forpligtiger kunden til at købe produkter i et bestemt antal eller for et bestemt beløb over en periode mod at få særlige priser og rabatter.
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesAgreementListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 9554
ms.assetid: c5d55c8d-99f2-44f9-a897-5b0dee85fc81
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4ab396d06383e3d6fc7bfab2e01f1afe4aa8fc4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560111"
---
# <a name="sales-agreements"></a>Salgsaftaler

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om salgsaftaler. En salgsaftale er en kontrakt, der forpligtiger kunden til at købe produkter i et bestemt antal eller for et bestemt beløb over en periode mod at få særlige priser og rabatter.

En salgsaftale er en kontrakt, der forpligter kunden til at købe produkter til et bestemt beløb eller en bestemt mængde over tid, mod at få særlige priser, særlige rabatter og andre særlige betingelser, f.eks. særlige betalings- og leveringsbetingelser. Priserne og rabatterne i salgsaftalen tilsidesætter de priser og rabatter, der er angivet i de eventuelle samhandelsaftaler, der findes.  

En salgsaftales gyldighedsperiode defineres af felterne **Ikrafttrædelsesdato** og **Udløbsdato** i aftalen. En kundes salgsordre er berettiget til aftalens vilkår, hvis den ønskede afsendelsesdato for ordren ligger inden for gyldighedsperioden. Alle salgsordrelinjer, der er knyttet til en salgsaftale, er med til at opfylde den pågældende salgsaftale.  

Du kan oprette en salgsordre direkte ud fra en salgsaftale ved hjælp af handlingen **Frigiv ordre**. Du kan også vælge en gyldig salgsaftale, når du tager imod ordrer (se afsnittet den "Anvende salgsaftaler i bestillingsprocessen" i denne artikel).  

> [Bemærk!] I tidligere versioner blev salgsaftaler kaldt rammesalgsordrer.

## <a name="commitment-types"></a>Tilsagnstyper
Hver linje i en salgsaftale udtrykker et tilsagn om at sælge noget. Generelt er der to kategorier af tilsagn:

-   **Værditilsagn** – Kunden accepterer at købe produkter for et bestemt beløb.
-   **Mængdetilsagn** – Kunden accepterer at købe et bestemt antal produkter.

En kontrakt kan desuden forpligte kunden til at købe et eller flere bestemte produkter i en produktkategori. Ved at kombinere disse to faktorer (værdi i forhold til antal og specifikke produkter i forhold til produktkategorier) får vi fire typer tilsagn:

-   **Bundet produktantal** – Kunden accepterer at købe et bestemt antal produkter. Linjer, der bruger denne forpligtelsestype, er defineret af et varenummer og af den aftalte mængde og enhed. Feltet **Beløb** er ikke tilgængeligt.
-   **Bundet produktværdi** – Kunden accepterer at købe specifikke produkter for et bestemt beløb. Linjer, der bruger denne forpligtelsestype, defineres af et varenummer og det aftalte beløb. Felterne **Antal** og **Enhed** er ikke tilgængelige.
-   **Værditilsagn for produktkategori** – Kunden accepterer at købe produkter fra en bestemt salgskategori for et bestemt beløb. Linjer, der bruger denne forpligtelsestype, defineres af en salgskategori i hierarkiet over salgskategorier og af et beløb. Felterne **Antal** og **Enhed** er ikke tilgængelige.
-   **Værditilsagn** – Kunden accepterer at købe produkter eller i en hvilken som helst indkøbskategori for at bestemt beløb. Felterne **Antal** og **Enhed** er ikke tilgængelige.

Linjer i samme salgsaftale kan indeholde forskellige forpligtelsestyper.

## <a name="pricing-terms-for-sales-agreements"></a>Prisvilkår for salgsaftaler
Prisvilkår kan variere alt efter forpligtelsestypen. På en salgsordre, der er knyttet til en salgsaftale, tilsidesætter prisvilkårene fra denne salgsaftale andre prisvilkår, der gælder ud fra samhandelsaftaler. Følgende tabel indeholder en beskrivelse af de prisrelaterede felter, der påvirkes af hver enkelt forpligtelsestype. "Ja" angiver, at feltet kan opdateres på en ordrelinje.

| Tilsagnstype                   | Enhedspris | Prisenhed | Rabatprocentdel | Kasserabatbeløb |
|-----------------------------------|------------|------------|------------------|----------------------|
| Bundet produktantal       | Ja        | Ja        | Ja              | Ja                  |
| Bundet produktværdi          |            |            | Ja              |                      |
| Værditilsagn for produktkategori |            |            | Ja              |                      |
| Værditilsagn                  |            |            | Ja              |                      |

## <a name="policies-for-sales-agreements"></a>Politikker for salgsaftaler
Følgende politikker påvirker den måde, som tilknytningen mellem en salgsaftaleforpligtelse og de tilsvarende salgsordrelinjer fungerer på:

-   **Maks. gennemtvinges** – Den samlede mængde eller det samlede beløb for alle ordrelinjer må ikke overstige den mængde eller det beløb, der er angivet på den relaterede forpligtelse.
-   **Pris og rabat er fast** – Prisen på en ordrelinje og prisen på den relaterede forpligtelse må ikke afvige. Hvis prisen ændres på ordrelinjen, brydes tilknytningen til forpligtelsen. Hvis tilknytningen brydes, bidrager ordrelinjen ikke til opfyldelse af forpligtelsen.
-   **Minimumbeløb til frigivelse** og **Maksimumbeløb til frigivelse** – Hvis der angives et beløb, vises der en meddelelse, hvis du foretager ændringer af en ordrelinje, der medfører, at ordrelinjen bliver forskellig fra den relaterede forpligtelse.

## <a name="fulfillment-calculations-for-sales-agreements"></a>Indfrielsesberegninger for salgsaftaler
Forpligtelsesmængder og beløb vises under fanen **Opfyldelse** i oversigtspanelet **Linjedetaljer** på siden **Salgsaftaler**.  

I området **Opfyldelse** kan du se de samlede mængder og beløb for alle ordrelinjer, der er knyttet til den angivne salgsaftale. Du kan også se det resterende beløb eller den resterende mængde, der kræves for at opfylde forpligtelsen.  

I området **Aftale** kan du se mængder og beløb fra den angivne salgsaftale. Disse mængder og beløb er de samlede mængder og beløb, der er indgået aftale om.

## <a name="confirmations-and-version-history-for-sales-agreements"></a>Bekræftelser og versionsoplysninger for salgsaftaler
Når du bekræfter en salgsaftale, gemmes den aktuelle version af salgsaftalen i en historiktabel. Hvis du ændrer salgsaftalen, kan du bekræfte den igen for at gemme en anden version af salgsaftalen i historikken.  

Hvis du ikke bekræfter en salgsaftale, kan den stadig bruges til at oprette salgsordrer. Historikoplysninger for salgsaftale bliver dog ikke gemt.  

Du kan få vist eller udskrive alle ændringer af bekræftelser. Derefter kan du dele revisioner med din kunde for at opnå godkendelse.

## <a name="applying-sales-agreements-during-the-ordering-process"></a>Anvende salgsaftaler i bestillingsprocessen
Hvis du ikke frigiver salgsordrer direkte til en salgsaftale, kan du stadig knytte en salgsaftale til en ordre under ordreindtastningsprocessen. Når du opretter en ny salgsordre, og du vælger en salgsaftale, gælder vilkårene i aftalen, såsom betalingsbetingelser, leveringsbetingelser og leveringsadresse, for ordrehovedet, og forbindelsen mellem aftalen og ordren oprettes. Når du på ordrelinjerne vælger produkter og kategorier, der er angivet i salgsaftalen, kopieres priserne og rabatterne fra aftalen. Samme salgsordre kan indeholde både linjer, der ikke er relateret til en salgsaftale, og linjer, der har en forpligtelse til en salgsaftale.

## <a name="modifying-sales-orders-that-are-linked-to-sales-agreements"></a>Ændre salgsordrer, der er knyttet til salgsaftaler
Hvis du har oprettet (frigivet) en salgsordre i henhold til en salgsaftale, kan visse felter i salgsaftrækslinjerne kun ændres, hvis du fjerner forbindelsen til de tilknyttede salgsaftalelinjer. Følgende tabel indeholder nogle af disse felter.

| Felt                                                             | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ønsket afsendelsesdato                                               | Hvis du ændrer den ønskede afsendelsesdato til en dato, der er tidligere end værdien i **Ikrafttrædelsesdato** på salgsaftalelinjen, skal du fjerne tilknytningen til salgsaftalelinjen, før du kan gemme den ændrede afsendelsesdato. Hvis du ændrer den ønskede afsendelsesdato til en dato, der er senere end værdien i **Udløbsdato** på salgsaftalelinjen, skal du fjerne tilknytningen til salgsaftalelinjen, før du kan gemme den ændrede afsendelsesdato. |
| CurrencyDiscount, percentDiscountUnit, pricePrice, unitNet amount | Hvis du ændrer værdien i nogen af disse felter, og hvis afkrydsningsfeltet **Pris og rabat er fast** er markeret på en tilknyttet salgsaftalelinje, åbnes der en dialogboks, hvor du bliver bedt om at gemme ændringen. Klik på **Ja** for at fjerne linket til salgsaftalelinjen og genberegne prisen. Klik på **Nej** for at fjerne linket til salgsaftalelinjen uden at genberegne prisen.                                                                   |
| Nettobeløb                                                        | Hvis du angiver et beløb, der overstiger det beløb, der er angivet på salgsaftalelinjen, og afkrydsningsfeltet **Maks. gennemtvinges** er markeret, åbnes der en dialogboks, hvor du bliver bedt om at gemme det ændrede beløb. Klik på **Ja** for at fjerne linket til salgsaftalelinjen og genberegne prisen. Klik på **Nej** for at fjerne linket til salgsaftalelinjen uden at genberegne prisen.                                                                 |
| Antal                                                          | Hvis du angiver et antal, der overstiger det antal, der er angivet på salgsaftalelinjen, og afkrydsningsfeltet **Maks. gennemtvinges** er markeret, åbnes der en dialogboks, hvor du bliver bedt om at gemme det ændrede antal. Klik på **Ja** for at fjerne linket til salgsaftalelinjen og genberegne prisen. Klik på **Nej** for at fjerne linket til salgsaftalelinjen uden at genberegne prisen.                                                            |

## <a name="returning-an-item-that-was-ordered-from-a-sales-agreement"></a>Returnere en vare, der er bestilt fra en salgsaftale
Når en kunde returnerer et produkt, der blev bestilt fra en salgsaftale, kan Microsoft Dynamics 365 for Finance and Operations automatisk finde og opdatere den relaterede salgsaftaleforpligtelse for at afspejle ændringen i antal eller beløb. Ved at oprette en returordre, der er baseret på den oprindelige salgsordre, der er knyttet til en salgsaftale, oprettes der en relation mellem en salgsaftaleforpligtelsen, salgsordrelinjen og returordrefakturaen.  

Hvis du ikke vil modregne antallet af returnerede varer fra salgsaftaleforpligtelsen, kan du bruge kontrolelementet **Fjern link** på siden **Returner ordre** til at fjerne tilknytningen mellem returvareordren og salgsaftaleforpligtelsen. Hvis du skal genoprette tilknytningen senere, skal du klikke på **Opret link**.  

**Bemærk!** En returordre kan kun knyttes til én salgsaftale. Hvis en kunde returnerer flere produkter, der er bestilt fra flere salgsaftaler, skal du oprette en ny returordre for hvert produkt og oprette en tilknytning til den relevante salgsaftale.

## <a name="automatic-search-for-sales-agreements"></a>Søge efter salgsaftaler automatisk
I nogle situationer, hvor salgsordrer oprettes indirekte, som når du opretter en kreditnota eller interne salgsordrer, kan du styre, om Microsoft Dynamics 365 for Finance and Operations automatisk skal søge efter relevante salgsaftaler.

## <a name="financial-dimensions-on-sales-agreements"></a>Økonomiske dimensioner for salgsaftaler
Du kan kopiere økonomiske dimensioner enten til dokumentoverskrifter eller til enkelte linjer i en salgsaftale. Du kan til enhver tid ændre dimensionerne på en aftaleoverskrift eller en aftalelinje. I så fald kopieres dimensionerne automatisk til aftræksoverskriften eller aftrækslinjerne i aftræksordrer.



