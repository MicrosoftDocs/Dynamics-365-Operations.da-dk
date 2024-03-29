---
title: Indkøb og forsyning i den offentlige sektor
description: Denne artikel forklarer den offentlige sektors funktion Indkøb og forsyning. Dette omfatter indkøbsordrekoder, certificering kreditortyper, funktion til klassificering af købsaftaler og indkøbsordrelinjebeløb.
author: velofog
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: velofog
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 19681
ms.assetid: c99b2aeb-4ac2-4abe-b8b9-786b664c103d
ms.search.industry: Public sector
ms.search.form: AgreementClassification, BudgetParameters, ProcCategoryHierarchyManagement, PurchTableListPage, smmActivities, VendCertificationType, VendTableListPage
ms.openlocfilehash: 69b5262816d06ae7bb155a6ac9daf49e14874478
ms.sourcegitcommit: 1a7729a6ce4f3fcf68bdc4cfdad746a5553da3c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573062"
---
# <a name="procurement-and-sourcing-in-the-public-sector"></a>Indkøb og forsyning i den offentlige sektor

[!include [banner](../includes/banner.md)]

Denne artikel introducerer dig til den offentlige sektors funktion Indkøb og forsyning. Dette omfatter indkøbsordrekoder, certificering kreditortyper, funktion til klassificering af købsaftaler og indkøbsordrelinjebeløb.

## <a name="what-are-the-prerequisites-for-setting-up-procurement-and-sourcing-in-the-public-sector"></a>Hvad er forudsætningerne for opsætning af indkøb og forsyning i den offentlige sektor?
Før du begynder at justere indstillingerne og angive dine data, skal du:

-   Konfigurer leverandører
-   Definere nummereringssystemet for kreditorer, indkøbsordrer og så videre
-   Angiv certificeringstyper for kreditor.

Du skal muligvis konfigurere følgende indkøbs- og forsyningsfunktioner for offentlige organisationer:

-    [Indkøbsordrekoder i den offentlige sektor](purchase-order-codes-public-sector.md): Opret koder og særlige meddelelser til bekræftelse af indkøbsordrer. En bekræftende indkøbsordre omgår den typiske indkøbsproces.

> [!NOTE]
> Dette gælder også for Kreditor.

-   [Regnskab i den offentlige sektor i Frankrig](../localizations/emea-fra-public-sector-accounting.md) 

For franske organisationer kan yderligere trin være nødvendige for den offentlige sektor.

I de følgende afsnit beskrives de indkøbs- og forsyningsfunktioner, der er tilgængelige for den offentlige sektor.

## <a name="what-are-vendor-certification-types"></a>Hvad er kreditorcertificeringstyper?
Du kan oprette og tildele enhver type certificering, som kreditorer kan have, til kreditororganisationer. Dette omfatter ikke kun professionelle legitimationsoplysninger som en professionel teknikers licens eller Microsoft SQL Server-certificering, men også om de har ansvarsforsikring, minoritetsstatus eller overholder forskellige miljømæssige eller forbrugermæssige sikkerhedsstandarder. 

Du kan bruge siden **Certificeringstype** i modulet Kreditor til at angive certificeringstypen og -beskrivelsen.

## <a name="what-do-i-need-to-know-about-purchase-or-sales-agreement-classifications"></a>Værd at vide om købs- eller salgsaftaleklassifikationer
Når brugere opretter en ny købsaftale eller salgsaftale, skal de altid vælge typen købsaftale eller salgsaftale. Yderligere kontroller til den offentlige sektor er tilgængelige på siden **Aftaleklassifikationer**. 

For at oprette og angive aftaleklassifikationer skal du bruge siden **Købsaftaleklassifikation** i Indkøb og forsyning eller siden **Salgsaftaleklassifikation** i Salg og marketing. 

Tag følgende oplysninger i betragtning, når du angiver oplysninger om købs- eller salgsaftaleklassifikationer.

### <a name="how-do-i-enter-information-about-subcontractors-on-purchase-agreements"></a>Hvordan angiver jeg oplysninger om underleverandører i købsaftaler?

Vælg indstillingen **Underleverandører**.

### <a name="how-do-i-enter-information-about-insurance-policies-and-bonds-on-purchase-agreements"></a>Hvordan indtaster jeg oplysninger om forsikringspolicerne og obligationer i købsaftaler?

Vælg indstillingen **Certificeringer**. Oplysningerne kan bruges til at oprette en rapport, du kan bruge til at overvåge kreditorens overholdelse af bestemte krav. (For at generere rapporten skal du gå til siden **Certificeringsoverholdelse ved købsaftale**).

### <a name="how-do-i-enter-information-about-milestones-and-tasks-on-purchase-agreements"></a>Hvordan angiver jeg oplysninger om milepæle og opgaver i købsaftaler?

Vælg indstillingen **Aktiviteter**.

### <a name="how-do-i-require-direct-invoicing-and-prevent-the-use-of-release-orders-with-purchase-agreements"></a>Hvordan kræver jeg direkte fakturering og forhindrer brug af aftræksordrer i købsaftaler?

Vælg indstillingen **Kræv direkte fakturering**. 

## <a name="can-i-view-purchase-order-line-amounts"></a>Kan jeg få vist linjebeløb for indkøbsordre?
Ja. Du kan få vist linjeantal for en indkøbsordre, herunder det aktuelle ordreantal og eventuelle antal, der er modtaget eller faktureret. Du kan også få vist antal, der endnu ikke er faktureret, eller antal for fakturaer, der afventer.

### <a name="tip"></a>Tip!

Lad os sige, at du får vist en indkøbsordrelinje med indkøb, der er bogført på to finanskonti. Den ene finanskonto er beregnet til kontormøbler, der er bestilt hos en leverandør. Den anden finanskonto er beregnet til kontorartikler. Ordreantallet er lig med summen af fakturerede antal, antallet på ventende fakturaer og antal, der ikke er faktureret endnu. Det modtagne antal er den del af ordreantallet, der er modtaget fra kreditor.

<table>

<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />

<tbody>
<tr class="odd">
<td><strong>Finanskonto</strong></td>
<td><strong>Bestilt</strong></td>
<td><strong>Modtaget</strong></td>
<td><strong>Faktureret</strong></td>
<td><strong>Ventende faktura</strong></td>
<td><strong>Fakturarest</strong></td>
</tr>
<tr class="even">
<td>60010 (kontormøbler)</td>
<td><p>1.200,00</p></td>
<td>250,00</td>
<td>350,00</td>
<td>200,00</td>
<td><p>650,00</p></td>
</tr>
<tr class="odd">
<td>60020 (kontorartikler)</td>
<td><p>750,00</p></td>
<td>150,00</td>
<td>400,00</td>
<td>&nbsp;</td>
<td><p>350,00</p></td>
</tr>
<tr class="even">
<td>I alt</td>
<td><p>1.950,00</p></td>
<td>400,00</td>
<td>750,00</td>
<td>200,00</td>
<td><p>1,000.00</p></td>
</tr>
</tbody>
</table>



Du kan finde yderligere oplysninger i [Oversigt over kreditorbetalinger i den offentlige sektor](../../supply-chain/procurement/procurement-sourcing-overview.md) og [Oversigt over indkøb og forsyning i den offentlige sektor](accounts-payable-public-sector.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
