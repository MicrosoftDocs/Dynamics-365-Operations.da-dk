---
title: "Købsaftaler"
description: "Denne artikel indeholder oplysninger om købsaftaler. En købsaftale er en kontrakt, som forpligter en organisation til at købe et bestemt antal eller beløb via flere indkøbsordrer over tid. I bytte for denne forpligtelse får køberen specialpriser og rabatter."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AgreementClassification, AgreementLine, AgreementLinePrompt, PurchAgreement, PurchAgreementCreate, PurchAgreementGenerateReleaseOrder, PurchAgreementHistory, PurchAgreementInvoiceJournal
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 11634
ms.assetid: 8ac20adf-7412-4929-be8c-aaedf23a76ad
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e4414ead4d2c767ecdd3e631035034b01de55b27
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="purchase-agreements"></a>Købsaftaler

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om købsaftaler. En købsaftale er en kontrakt, som forpligter en organisation til at købe et bestemt antal eller beløb via flere indkøbsordrer over tid. I bytte for denne forpligtelse får køberen specialpriser og rabatter. 

Købsaftaler kan gælde for en bestemt mængde af et produkt, et bestemt valutabeløb af et produkt eller for et bestemt valutabeløb af produkter i en indkøbskategori. Priserne og rabatterne i købssaftalen gå forud for de priser og rabatter, der er angivet i de eventuelle samhandelsaftaler, der måtte findes.  

På siden **Købsaftaler** kan du oprette, anvende og følge op på de købsaftaler, der findes mellem din organisation og dine kreditorer. Når du har oprettet en købsaftale, kan du f.eks. oprette en ordre direkte fra den. Hver købsaftale har en gyldighedsperiode, der er defineret af den person, der opretter købsaftalen. Leveringsdatoen for et køb skal ligge inden for denne gyldighedsperiode.  

Når du opretter en købsaftale, skal du aktivere den, før den træder i kraft. Du aktiverer en købsaftale ved at sætte indstillingen **Markér aftale som gældende** til **Ja**.

## <a name="commitment-types"></a>Tilsagnstyper
Hver linje i en købsaftale er en forpligtelse til at købe noget. Du kan bruge linjer fra flere købsordrer (IO'er) til at opfylde forpligtelsen. Der findes fire typer forpligtelser:

-   **Bundet produktantal** – Du køber et bestemt antal af et produkt.
-   **Bundet produktværdi** – Du køber et bestemt valutabeløb af et produkt.
-   **Værditilsagn for produktkategori** – Du køber et bestemt valutabeløb i en produktkategori. Beløbet kan være for en katalogvare eller en ikke-katalogvare.
-   **Værditilsagn** – Du køber for et bestemt valutabeløb af et hvilket som helst produkt eller i en hvilken som helst indkøbskategori.

## <a name="pricing-terms-for-purchase-agreements"></a>Prisvilkår for købsaftaler
Prisvilkår kan variere alt efter forpligtelsestypen. Prisvilkårene fra købsaftaler tilsidesætter andre prisvilkår, der er oprettet i samhandelsaftaler. Følgende tabel indeholder en beskrivelse af de prisrelaterede felter, der påvirkes af hver enkelt forpligtelsestype. Felter, der indeholder **Ja**, kan opdateres på en ordrelinje.

| Tilsagnstype                   | Enhedspris | Prisenhed | Rabatprocentdel | Kasserabatbeløb |
|-----------------------------------|------------|------------|------------------|----------------------|
| Bundet produktantal       | Ja        | Ja        | Ja              | Ja                  |
| Bundet produktværdi          |            |            | Ja              |                      |
| Værditilsagn for produktkategori |            |            | Ja              |                      |
| Værditilsagn                  |            |            | Ja              |                      |

## <a name="policies-for-purchase-agreements"></a>Politikker for købsaftaler
Følgende politikker påvirker den måde, hvorpå tilknytningen mellem en købsaftaleforpligtelse og de tilsvarende IO-linjer fungerer:

-   **Maks. gennemtvinges** – Den samlede mængde eller det samlede beløb for alle ordrelinjer må ikke overstige den mængde eller det beløb, der er angivet på den relaterede forpligtelse.
-   **Pris og rabat er fast** – Prisen på en ordrelinje og prisen på den relaterede forpligtelse skal være den samme. Hvis prisen ændres på ordrelinjen, brydes tilknytningen til forpligtelsen. Hvis tilknytningen brydes, bidrager ordrelinjen ikke til opfyldelsen af forpligtelsen.
-   **Minimumbeløb til frigivelse og Maksimumbeløb til frigivelse** – Hvis der angives et beløb, modtager du en meddelelse, hvis du foretager ændringer til en ordrelinje, der medfører, at ordrelinjen bliver forskellig fra den relaterede forpligtelse.

## <a name="fulfillment-calculations-for-purchase-agreements"></a>Indfrielsesberegninger for købsaftaler
Forpligtelsesmængder og beløb vises under fanen **Opfyldelse** i oversigtspanelet **Linjedetaljer** på siden **Købsaftaler**.  

Området **Opfyldelse** viser det resterende beløb eller den resterende mængde, der kræves for at opfylde forpligtelsen.  

Området **Aftale** viser det samlede antal eller det samlede beløb, som salgsaftalelinjen er gyldig for.  

Du kan få adgang til IO-linjerne og de fakturalinjer, der bidrager til opfyldelsesberegningen, ved at vælge handlingen **Relaterede oplysninger** på linjerne eller i hovedet i en købsaftale.

## <a name="confirmations-and-version-history-for-purchase-agreements"></a>Bekræftelser og versionsoplysninger for købsaftaler
Når du bekræfter en købsaftale, gemmes den aktuelle version af købsaftalen i en historiktabel. Hvis du ændrer købsaftalen, kan du bekræfte den igen for at gemme en anden version af købsaftalen i historikken. Hvis du ikke bekræfter en købsaftale, kan den stadig bruges til at oprette IO'er. Historikoplysningerne for købsaftalen bliver dog ikke gemt. Du kan få vist eller udskrive alle versioner af aftalen. Derefter kan du dele revisioner med din leverandør for at opnå godkendelse.

## <a name="applying-purchase-agreements-in-the-ordering-process"></a>Anvende købsaftaler i bestillingsprocessen
Når du opretter en indkøbsordre, kan du anvende en købsaftale til den. Oplysninger fra betingelserne for aftalen, såsom betalingsbetingelser, leveringsbetingelser og leveringsadresse, kopieres derefter til hovedet i indkøbsordren. Hvis indkøbsordren indeholder en eller flere ordrelinjer for produkter og kategorier, der er omfattet af aftalen, bruges priser og rabatter fra købsaftalen på disse linjer. Beløbet eller antallet på ordrelinjen bidrager til opfyldelse af forpligtelsen i købsaftalen. Samme indkøbsordre kan indeholde både linjer, der ikke er relateret til en købsaftale, og linjer, der har en forpligtelse til en købsaftale.  

Du kan kun vælge en købsaftale, når du opretter en indkøbsordre. Du kan ikke vælge en købsaftale, når indkøbsordren er blevet oprettet.  
I nogle situationer, hvor indkøbsordrer oprettes indirekte, kan du styre, om Finance and Operations automatisk skal søge efter relevante købsaftaler. Du kan f.eks. gøre dette, hvis du automatisk justerer planlagte indkøbsordrer eller opretter købsordrer, der er baseret på salgsordrer.

## <a name="purchase-agreements-and-intercompany-trade"></a>Købsaftaler og samhandel internt i firmaet
Der kan oprettes interne handelsforhold mellem kreditorkonti og debitorkonto, som er i forskellige juridiske enheder. Når der oprettes en salgsordre eller indkøbsordre for en af parterne, oprettes en intern ordretilknytning. I ordretilknytningen oprettes salgsordren og indkøbsordren i de relevante juridiske enheder.  

Du kan oprette en købsaftale eller en salgsaftale for en af de interne handelsparter. Du kan derefter oprette den tilsvarende salgsaftale eller købsaftalen for den anden interne handelspart i den anden juridiske enhed.  

Hvis du opretter en intern indkøbsordre, der bruger den interne købsaftale i én juridisk enhed, anvender den tilsvarende interne salgsordre den tilsvarende interne salgsaftale i den anden juridiske enhed. Opfyldelsen af salgsaftaleforpligtelserne og opfyldelsen af indkøbsaftalerne synkroniseres på samme måde som den interne salgsordre og den interne indkøbsordre synkroniseres.

## <a name="financial-dimensions-on-purchase-agreements"></a>Økonomiske dimensioner for købsaftaler
Du kan kopiere økonomiske dimensioner til dokumentoverskrifter eller til enkelte linjer i en købsaftale. Hvis du ændrer dimensionerne i aftalehovedet eller på aftalelinjen, påvirker ændringen ikke frigivne ordrer, men afspejles i nye ordrer.

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Opret en ny købsaftale (opgaveguide)](tasks/create-purchase-agreement.md)

[Opret en købsaftræksordre ud fra en købsaftale (opgaveguide)](tasks/create-purchase-release-order-purchase-agreement.md)




