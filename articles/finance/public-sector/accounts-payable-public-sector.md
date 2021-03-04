---
title: Oversigt over Kreditor i den offentlige sektor
description: I denne artikel introduceres du til den offentlige sektors funktioner for Kreditor, som er integreret i Microsoft Dynamics 365 Finance. Disse funktioner omfatter IO-koder, bogføringsdefinitioner, engangskreditorfakturering, 1099-skatteformularer, kasserabatter, kreditorcertificeringstyper, aktivitetsoversigt for Projektregnskab, elektroniske betalinger, forsider og signatursider til rapporter, IO-linjebeløb og kladdesider i kreditorfakturaer.
author: ShylaThompson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetParameters, CustParameters, LedgerJournalTable, OMLegalEntity, PurchAgreementListPage, PurchTableListPage, SrmParameters, VendCertificationType, VendCoverPageLayout, VendOpenInvoicesListPage, VendParametersVendParameters, VendTableListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 19661
ms.assetid: b4c903dd-5ec7-4ec5-9dc9-77ba4f00fab8
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: beef5c13c31af7551255c8264c1b6478abee6428
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407663"
---
# <a name="accounts-payable-in-the-public-sector-overview"></a>Oversigt over Kreditor i den offentlige sektor

[!include [banner](../includes/banner.md)]

I denne artikel introduceres du til den offentlige sektors funktioner for Kreditor, som er integreret i Dynamics 365 Finance. Disse funktioner omfatter IO-koder, bogføringsdefinitioner, engangskreditorfakturering, 1099-skatteformularer, kasserabatter, kreditorcertificeringstyper, aktivitetsoversigt for Projektregnskab, elektroniske betalinger, forsider og signatursider til rapporter, IO-linjebeløb og kladdesider i kreditorfakturaer. 

<a name="what-are-the-prerequisites-for-setting-up-accounts-payable-in-the-public-sector"></a>Hvad er forudsætningerne for opsætning af Kreditor i den offentlige sektor?
--------------------------------------------------------------------------------

Før du begynder at justere indstillingerne og angive dine data, skal du udføre følgende opgaver:

-   Konfigurer leverandører.
-   Konfigurere nummereringssystemer for kreditorer, indkøbsordrer og så videre.
-   Bestemme, hvilke indkøbsordrekoder (IO) og meddelelser, der skal bruges.

Når du har konfigureret forudsætningerne, kan det være nødvendigt at konfigurere følgende kreditorfunktioner:

- [Indkøbsordrekoder i den offentlige sektor](purchase-order-codes-public-sector.md) – Du kan oprette koder og særlige meddelelser til bekræftelse af indkøbsordrer. En bekræftende indkøbsordre omgår den typiske indkøbsproces. For eksempel tillader du en ikke-planlagt ordre ved hjælp af et indkøbsordrenummer på tidspunktet for et køb i stedet for ved hjælp af et dokument, der er leveret, før varen er påkrævet. 
  > [!NOTE]
  > Dette gælder også for indkøb og forsyning.

- [Bogføringsdefinitioner i den offentlige sektor](posting-definitions-public-sector.md) – Du kan bruge bogføringsdefinitioner til at oprette kladdelinjer for oprindelige posteringer, der opfylder udvalgte kriterier. Du kan f.eks. bruge bogføringsdefinitioner til at oprette flere afstemte finansposter baseret på attributter som f.eks. posteringstyper og konti. 
  > [!NOTE]
  > Dette gælder også for Finans, Budgettering og Debitor.


- [Engangsleverandører i den offentlige sektor](one-time-vendors-public-sector.md) – Når der ikke kræves godkendelse eller en aftale i form af en indkøbsordre, kan du hurtigt oprette en eller flere fakturaer, samtidig med at du opretter en post for kreditoren. Du kan finde flere oplysninger under [Planlægning for engangsleverandører i den offentlige sektor](plan-one-time-vendors-public-sector.md).
- Oversigt over 1099-formular i den offentlige sektor – Hvis du handler med leverandører, der er omfattet af amerikansk 1099-skat, skal du spore det beløb, du betaler til hver leverandør, og rapportere disse oplysninger til de amerikanske skattemyndigheder ved udgangen af kalenderåret. Offentlige organisationer bruger formular 1099-G og 1099-S.

> [!NOTE]
> Dette gælder også for indkøb og forsyning.

## <a name="additional-public-sector-functionality"></a>Yderligere funktioner til den offentlige sektor
De resterende afsnit i denne artikel beskriver de Kreditor-funktioner, der er tilgængelige for den offentlige sektor.

-   **Kasserabatter** – Vælg den konto, der skal modregnes på, når kasserabatter anvendes.
-   **Certificeringstyper for kreditor** – Definer en certificeringstype for eventuelle kreditorkrav, som du vil spore.
-   **Aktivitetsoversigt for købsaftale** – Angiv oversigt over detaljerne for aktiviteter, der er relateret til en købsaftale.
-   **Elektroniske betalinger** – Angiv elektroniske betalinger til kreditorer. 
-   **For- og signatursider til betalingsrapporter** – Angiv, hvilke oplysninger der skal vises på forsiden og signatursider for en betalingsrapport.
-   **Beløb på indkøbsordrelinjer** – Få vist linjebeløb for en indkøbsordre og eventuelle beløb, der stadig skal faktureres, eller for fakturaer, der venter.

### <a name="how-can-i-apply-cash-discounts-to-vendor-invoices"></a>Hvordan kan jeg anvende kasserabatter på kreditorfakturaer?

Du kan bruge siden **Kasserabatter** i Kreditor eller Debitor til at vælge kontoen, der skal modposteres, når kasserabatter anvendes på fakturaer. Du kan gøre dette for en eksisterende faktura eller en ny faktura, som du opretter. Kasserabatkoder knyttes til debitor- og kreditorkonti og bruges til salgs- og indkøbsordrer. I oversigtspanelet **Konfiguration** kan du i feltet **Rabatmodkonti** forskyde enten den angivne hovedkonto for kreditorrabatkonto eller -konti, der er angivet på fakturalinjen.

### <a name="how-do-i-specify-and-assign-certification-types-for-vendors"></a>Hvordan kan jeg angive og tildele certificeringstyper for kreditorer?

Du kan oprette og tildele enhver type certificering, som disse kreditorer kan have, til kreditororganisationer. Denne certificering omfatter professionelle legitimationsoplysninger, som en professionel teknikerlicens eller Microsoft SQL Server-certificering. Dog kan certificering også angive, at leverandørerne har ansvarsforsikring eller minoritetsstatus, eller at de overholder forskellige miljømæssige eller forbrugersikkerhedsstandarder. Du kan bruge siden **Certificeringstype** til at oprette typer af certificering og beskrivelser.

### <a name="how-do-i-view-or-enter-summary-information-for-purchase-agreement-activity"></a>Hvordan får jeg vist eller angiver oversigtsoplysninger for købsaftaleaktivitet?

Du kan bruge siden **Købsaftaler** i modulet Kreditor eller Indkøb og forsyning til at angive oversigtsdetaljer for aktiviteter, der er relateret til en købsaftale. Du kan gøre dette for en eksisterende købsaftale eller en ny købsaftale, som du opretter. Eksempler omfatter projektmilepæle, planlagte datoer for betalinger til en kreditor eller de datoer, hvor varer, der er angivet i en kreditorkontrakt, forfalder til gennemsyn.

#### <a name="tips"></a>Tip!

-   Du kan oprette et entydigt nummer for aktiviteten på siden **Juridiske enheder** side i Virksomhedsadministration eller Finans. Når du vælger aktiviteten i købsaftalen, tildeles nummeret automatisk.
-   Du kan også oprette et entydigt id for købsaftalen i afsnittet **Nummerserier** på siden **Indkøbs- og forsyningsparametre**. Når du opretter en købsaftale, tildeles nummeret automatisk.

### <a name="how-do-i-specify-electronic-payments-to-vendors"></a>Hvordan angiver jeg elektroniske betalinger til kreditorer?

Du kan fordele betalingen af en faktura på flere bankkonti for flere kreditorer. Du kan vælge flere bankkonti og tildele en procentdel til hver bankkonto. Afhængigt af de valgte konti, oprettes der en enkelt eller flere åbne posteringer mod fakturaen. Du kan oprette betalinger for hver kladdelinje uden at oprette en delvis betaling for hver kreditorbankkonto.

#### <a name="tip"></a>Tip!

For eksempel findes der en købsordre på 100, og Bank A er standardkreditorbankkontoen. I tabellen for betalingsudbetaling har Bank A 100 procent fordeling. (Hvis der ikke er en standardkreditorbankkonto, er tabellen tom). Du kan ændre fordelingen for Bank A til 30 procent og derefter tilføje en ny række. Du kan vælge en anden kreditorbank som f.eks Bank B i den nye række, hvorefter fordelingen for den nye række automatisk opdateres til 70 procent.

### <a name="how-can-i-create-and-print-cover-and-signature-pages-for-payments-reports"></a>Hvordan kan jeg oprette og udskrive for- og signatursider til betalingsrapporter?

Når du opretter for- og signatursider til en betalingsrapport, kan du angive de oplysninger, der skal vises. Disse oplysninger omfatter navne og titler på de personer, der skal godkende de foreslåede betalinger.

### <a name="how-do-i-view-purchase-order-line-amounts"></a>Hvordan får jeg vist linjebeløb for indkøbsordre?

Du kan få vist linjebeløb for en indkøbsordre. Disse beløb omfatter det samlede bestilte beløb, og eventuelle beløb, der er modtaget eller faktureret. Du kan også få vist beløb, der stadig skal faktureres, eller beløb for fakturaer, der afventer. Tip! Du kan f.eks. få vist en indkøbsordrelinje med indkøb, der er bogført på to finanskonti. Den ene finanskonto er beregnet til varer, der er bestilt hos en leverandør af kontormøbler. Den anden finanskonto er beregnet til kontorartikler. Ordreantallet er lig med summen af fakturerede antal, antallet på ventende fakturaer og antal, der ikke er faktureret endnu. Det modtagne antal er den del af ordreantallet, der er modtaget fra kreditor.


Du kan finde flere oplysninger under følgende emner:

[Tilføje en certificeringstype til en leverandør](tasks/add-certification-type-vendor-public-sector.md)

[Styre adgangen til købsaftaler](tasks/control-access-purchase-agreements-public-sector.md)

[Opret en engangskreditor og -faktura](tasks/create-one-time-vendor-invoice-public-sector.md)

[Oprette en kreditorcertificeringstype](tasks/create-vendor-certification-type-public-sector.md)

[Importere og oprette flere engangskreditorer og fakturaer](tasks/import-multiple-one-time-vendors.md)

[Konfigurer købsaftaleklassifikationer](tasks/set-up-purchase-agreement-classifications-public-sector.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]