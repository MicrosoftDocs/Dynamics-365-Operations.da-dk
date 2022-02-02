---
title: Oversigt over indkøbsrekvisition
description: Dette emne beskriver arbejdsgangen for indkøbsrekvisitioner og de forskellige statusser, som en indkøbsrekvisition kan have.
author: Henrikan
ms.date: 11/02/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqConsolidation, PurchReqCreate, PurchReqCreatePurchDetails, PurchReqCreatePurchListPage, PurchReqTable, PurchReqTableListPage, PurchReqConsolidationPartByVendor, PurchReqConsolidationLineDetail, PurchReqConsolidationCreate, PurchReqConsolidationBulkEdit, PurchReqConsolidationAddLine
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2174"
- intro-internal
ms.assetid: 77d07119-4d9f-4c0e-acbe-d319203571ab
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: acd0deebe79e29bd1beb32ea21cd179f5bf12c43
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982896"
---
# <a name="purchase-requisition-overview"></a>Oversigt over indkøbsrekvisition

[!include [banner](../includes/banner.md)]

Dette emne beskriver arbejdsgangen for indkøbsrekvisitioner og de forskellige statusser, som en indkøbsrekvisition kan have.

Afhængigt af hvordan organisationen er opbygget, kan du oprette indkøbsrekvisitioner for produkter, som organisationen forbruger. En indkøbsrekvisitionen er et internt dokument, der giver indkøbsafdelingen tilladelse til at købe vare eller tjenesteydelser.  

Når en indkøbsrekvisition er godkendt, kan den bruges til at generere en indkøbsordre. Indkøbsordrer er de eksterne dokumenter, som indkøbsafdelingen sender til kreditorer.

## <a name="creating-purchase-requisitions"></a>Oprette indkøbsrekvisitioner
Du kan oprette en indkøbsrekvisition på siden **Mine indkøbsrekvisitioner** og vælge de varer og tjenester, som du har brug for. Du kan vælge varer fra et indkøbskatalog, din organisation har oprettet, eller du kan anmode om varer, som ikke findes i et katalog, ved at vælge en indkøbskategori og indtast produktoplysningerne.  

Før du kan sende en indkøbsrekvisition til gennemsyn, skal der konfigureres arbejdsgange. Du bruger en arbejdsgang til at bevæge en indkøbsrekvisition gennem gennemsynsprocessen fra den første status som **Kladde** til den endelige status som **Godkendt**.

### <a name="purchase-requisition-statuses"></a>Status for indkøbsrekvisition

Når du opretter en indkøbsrekvisition, tildeles den en status. En status tildeles også hver linje, som du føjer til en indkøbsrekvisition. Når du sender en indkøbsrekvisition til en arbejdsgang til gennemsyn, opdateres indkøbsrekvisitionens og de enkelte linjers status, efterhånden som linjerne bevæger sig gennem arbejdsgangprocessen.  

Du kan konfigurere indkøbsrekvisitionens arbejdsgangsproces, så indkøbsrekvisitionen dirigeres gennem gennemsynsprocessen som ét enkelt dokument. Linjerne på indkøbsrekvisitionen kan også sendes enkeltvist til de rette validatorer. Hvis indkøbsrekvisitionslinjerne gennemses enkeltvist, kan status for indkøbsrekvisitionslinje opdateres, efterhånden som linjerne bevæger sig gennem gennemsynsprocessen. Når alle linjer er nået igennem gennemsynsprocessen, og der ikke er flere tilbageværende gennemsynstrin for indkøbsrekvisitionen, opdateres status for hele indkøbsrekvisitionen.

### <a name="purchase-requisition-workflow"></a>Arbejdsgang for indkøbsrekvisition

Diagrammet nedenfor viser de statusser, som en indkøbsrekvisition og en indkøbsrekvisitionslinje tildeles, efterhånden som de bevæger sig igennem gennemsynsprocessen.  

[![Statusser for indkøbsrekvisitionshoved og -linje.](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)

### <a name="purchase-requisition-header-and-line-status-relationships"></a>Statusrelationer for indkøbsrekvisitionshoved og -linje

Den overordnede status for indkøbsrekvisitionen bestemmes af status for indkøbsrekvisitionslinjerne. Derfor skal gennemsynsprocessen fuldføres for alle indkøbsrekvisitionslinjer, før gennemsynsprocessen for hele indkøbsrekvisitionen kan fuldføres. Tabellen nedenfor beskriver de statusser, som indkøbsrekvisitionshovedet og -linjer tildeles, efterhånden som indkøbsrekvisitionen bevæger sig igennem arbejdsgangprocessen.

<table>
<thead>
<tr class="header">
<th>Status på indkøbsrekvisition</th>
<th>Status for indkøbsrekvisitionslinjen</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Udkast</td>
<td>Udkast</td>
<td>Indkøbsrekvisitionen og indkøbsrekvisitionslinjen er oprettet, men de er ikke sendt til gennemsyn. Indkøbsrekvisitioner og indkøbsrekvisitionslinjer, der har status <strong>Kladde</strong> kan ændres. En indkøbsrekvisition eller indkøbsrekvisitionslinje har også status som <strong>Kladde</strong>, hvis den er trukket tilbage, men ikke er sendt til gennemsyn igen. <strong>Bemærk:</strong> Du kan sende eller trække en indkøbsrekvisition tilbage på dokumentniveau. Du kan ikke sende eller tilbagekalde en enkelt indkøbsrekvisitionslinje.</td>
</tr>
<tr class="even">
<td>Til gennemsyn</td>
<td><ul>
<li>Til gennemsyn</li>
<li>Afvist</li>
</ul></td>
<td>Hvis arbejdsgangen er konfigureret til at dirigere indkøbsrekvisitionslinjerne til gennemsyn hos enkelte personer, kan hver enkelt linje have en status som <strong>Til gennemsyn</strong> eller <strong>Afvist</strong>. Indkøbsrekvisitionens status opdateres, når gennemsynsprocessen er gennemført for alle indkøbsrekvisitionslinjer, og der ikke er flere gennemsynstrin tilbage for indkøbsrekvisitionen.
<ul>
<li><strong>Til gennemsyn</strong> – Indkøbsrekvisitionslinjerne er sendt til gennemsyn. Når arbejdsgangsprocessen er fuldført for en indkøbsrekvisitionslinje, er dens status fortsat <strong>Til gennemsyn</strong>, indtil alle resterende indkøbsrekvisitionslinjer er gennemset.</li>
<li><strong>Afvist</strong> – En indkøbsrekvisitionslinje er blevet afvist. Afviste indkøbsrekvisitionslinjer kan ændres og sendes til godkendelse igen.</li>
</ul>
Hvis du sender en indkøbsrekvisitionslinje igen, efter at den blev afvist, starter gennemsynsprocessen for alle linjer i indkøbsrekvisitionen, som stadig er til gennemsyn, forfra. </br><strong>Bemærk:</strong> Du kan trække en indkøbsrekvisition tilbage, selvom den allerede er sendt. Når du trækker en indkøbsrekvisition tilbage, tilbagekaldes alle andre indkøbsrekvisitionslinjer samtidig. Indkøbsrekvisitionslinjer, der er trukket tilbage, kan slettes.</td>
</tr>
<tr class="odd">
<td>Afvist</td>
<td>Afvist</td>
<td>Indkøbsrekvisition og alle indkøbsrekvisitionslinjer er blevet afvist. Indkøbsrekvisitionerne og indkøbsrekvisitionslinjer, der er afvist, kan sendes igen.</td>
</tr>
<tr class="even">
<td>Godkendt</td>
<td><ul>
<li>Godkendt</li>
<li>Annulleret</li>
<li>Lukket</li>
</ul></td>
<td>Alle indkøbsrekvisitionslinjer er gennemført i gennemsynsprocessen, og indkøbsrekvisitionen skal ikke igennem flere gennemsynstrin.
<ul>
<li><strong>Godkendt</strong> – Gennemsynsprocessen er fuldført for indkøbsrekvisitionslinjen, og linjen er blevet godkendt.</li>
<li><strong>Annulleret</strong> – Indkøbsrekvisitionslinjen er godkendt, men blev annulleret, fordi der ikke længere er brug for den. Kun godkendte indkøbsrekvisitionslinjer kan annulleres.</li>
<li><strong>Lukket</strong> – Indkøbsrekvisitionslinjen er godkendt, og dokumenter er blevet genereret, afhængigt af formålet med rekvisitionen.
<ul>
<li>Hvis rekvisitionsformålet er forbrug, oprettes der en indkøbsordre for indkøbsrekvisitionslinjen.</li>
<li>Hvis formålet med rekvisitionen genopfyldning, er der oprettet et eller flere dokumenter.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Annulleret</td>
<td>Annulleret</td>
<td>Indkøbsrekvisition og alle indkøbsrekvisitionslinjer er blevet annulleret.</br> <strong>Bemærk:</strong> Hvis du ikke længere har brug for en vare på en indkøbsrekvisitionslinje, skal du annullere indkøbsrekvisitionslinjen, hvis den allerede er godkendt. Kun godkendte indkøbsrekvisitionslinjer kan annulleres. Hvis der er indkøbsrekvisitionslinjer, som stadig er til gennemsyn, har indkøbsrekvisitionen statussen <strong>Til gennemsyn</strong>. I dette tilfælde kan du trække indkøbsrekvisitionen tilbage og slette den relevante indkøbsrekvisitionslinje.</td>
</tr>
<tr class="even">
<td>Lukket</td>
<td><ul>
<li>Lukket</li>
<li>Annulleret</li>
</ul></td>
<td>Indkøbsrekvisitionen er lukket, og et eller flere færdiggørelsesdokumenter er blevet oprettet.
<ul>
<li><strong>Lukket</strong> – Indkøbsrekvisitionslinjen er godkendt, og dokumenter er blevet genereret, afhængigt af formålet med rekvisitionen.
<ul>
<li>Hvis rekvisitionsformålet er forbrug, oprettes der en indkøbsordre for indkøbsrekvisitionslinjen.</li>
<li>Hvis formålet med rekvisitionen genopfyldning, er der oprettet et eller flere dokumenter.</li>
</ul></li>
<li><strong>Annulleret</strong> – Indkøbsrekvisitionslinjen er godkendt, men blev annulleret, fordi der ikke længere er brug for den. Kun godkendte indkøbsrekvisitionslinjer kan annulleres.</li>
</ul>
<strong>Bemærk:</strong> Hvis du ikke længere har brug for en vare på en indkøbsrekvisitionslinje, som er lukket, skal du annullere linjen i det færdiggørelsesdokument, der blev genereret til indkøbsrekvisitionslinjen.</td>
</tr>
</tbody>
</table>

## <a name="distributing-costs-to-multiple-financial-accounts"></a>Fordele omkostninger på flere finanskonti
Du kan fordele omkostningerne for et produkt i en indkøbsrekvisition på flere finanskonti. Hvis organisationen bruger dimensioner, f.eks. bærere eller afdelinger, kan du fordele omkostningen for et produkt til dimensioner for finanskonti.

## <a name="requisition-purposes"></a>Rekvisitionsformål
Rekvisitionsformål gør processen med at opfylde rekvisitionsbehov mere fleksibel. Når du opretter en rekvisition, kan du tildele den ét af to formål: forbrug eller genopfyldning. Afhængigt af rekvisitionsformålet og opsætningen af din organisation, kan rekvisitionsbehov opfyldes af en indkøbsordre, en flytteordre, en produktionsordre eller kanban.  

I indkøbspolitikker kan du styre de tilgængelige indkøbsrekvisitionsformål, når der oprettes en rekvisition til organisationen.

### <a name="requisitions-that-have-a-purpose-of-consumption"></a>Rekvisitioner med formålet forbrug

En rekvisition, der har formålet forbrug, repræsenterer et behov for varer eller tjenester, der skal bruges internt i organisationen. Det behov, der er oprettet af denne type rekvisitionen, opfyldes altid af en indkøbsordre. Hvis Supply Chain Management er konfigureret til at oprette indkøbsordrer automatisk, oprettes der indkøbsordrer, når indkøbsrekvisitionen er godkendt.

### <a name="requisitions-that-have-a-purpose-of-replenishment"></a>Rekvisitioner med formålet genopfyldning

En rekvisition, der har formålet genopfyldning, repræsenterer et behov for genopfyldning af lageret. Du opretter f.eks. en rekvisition for at genopfylde varer, så de kan sælges til en bestemt detaillokalitet på et bestemt tidspunkt. Det behov, der oprettes af denne slags rekvisition kan opfyldes af en købsordre, en flytteordre, en produktionsordre eller kanban.  

Når formålet med rekvisitionen er genopfyldning, udtrykkes behovet som en mængde i stedet for et beløb. Derfor gælder behæftelsesregnskab, budgetstyring, forretningsregler for fastlæggelse af anlægsaktiver (BRAD), projektregnskab og eventuelle relaterede regler ikke. Kun produkter, der er på lager og frigivet til den angivne juridiske enhed, kan opfylde genopfyldningsrekvisitionsbehovet. For at definere de produkter, der er tilgængelige, når formålet med rekvisitionen er genopfyldning, skal du bruge siden **Regel for adgang til genopfyldningskategori**.  

Hvis du vil bruge indkøbsrekvisitioner med formålet genopfyldning, skal du konfigurere behovsplanlægning til at omfatte rekvisitionsbehov. Genopfyldningsmetoden for det behov, der er oprettet af denne slags rekvisition, bestemmes derpå automatisk baseret på de forsyningspolitikker, der er konfigureret for varerne i din organisation og planlagt ved hjælp af behovsplanlægning.

## <a name="purchase-requisitions-and-requests-for-quotation"></a>Indkøbsrekvisitioner og anmodninger om tilbud
I nogle tilfælde skal du starte en tilbudsanmodningsproces (RFQ) for at identificere kreditoren og prisen for produkter, der er anmodet om i en indkøbsrekvisition. En tilbudsanmodning kan oprettes, når indkøbsrekvisitionen er til gennemsyn. Når du accepterer et tilbud, overføres oplysninger om kreditor, pris og så videre til rekvisitionen.  

Du kan sætte en indkøbsrekvisition på hold ved at vælge afkrydsningsfeltet **På hold** på siden **Oplysninger om indkøbsrekvisition**. Behandling af indkøbsrekvisitionen kan kun fortsætte, når du fjerner spærringen ved at fjerne markeringen i afkrydsningsfeltet.  

> [!NOTE]
> I e-indkøb kan tilbudsanmodningen for indkøbsrekvisitionen give leverandører mulighed for at tilføje alternative linjer. I dette tilfælde afspejler din indkøbsrekvisition godkendte alternativer.

## <a name="demand-consolidation"></a>Efterspørgselskonsolidering
Du kan forbedre din forhandlingsposition over for dine kreditorer og dermed opnå bedre priser, lavere forsendelses- og administrationsomkostninger samt lavere faste omkostninger ved at konsolidere indkøbsrekvisitionslinjer fra flere indkøbsrekvisitioner.  

Indkøbsrekvisitionslinjer er kun berettiget til efterspørgselskonsolidering, hvis følgende udsagn er sande:

-   Indkøbsrekvisitionen er blevet godkendt.
-   Indkøbsrekvisitionen opfylder indkøbspolitikkens regelkriterier for manuel behandling og efterspørgselskonsolidering.

Godkendte indkøbsrekvisitionslinjer, der opfylder kriterierne for manuel behandling, der er angivet på siden **Frigiv godkendte indkøbsrekvisitioner**. Hvis en indkøbsrekvisitionslinje også opfylder kriterierne for efterspørgselskonsolidering, kan linjen føjes til en konsolideringsmulighed.  

En konsolideringsmulighed er en gruppe af indkøbsrekvisitionslinjer, der er grupperet sammen, således at indkøberen kan forhandle den bedste handel med leverandørerne. Indkøbsrekvisitionslinjer, du vælger til en konsolideringsmulighed, vises på siden **Konsolidering af indkøbsrekvisition**. Du kan redigere linjer på denne side, hvis der kræves ændringer. Du kan også føje nye linjer til konsolideringsmuligheden eller fjerne eksisterende linjer fra.  

Efter du har føjet rekvisitionslinjerne til en konsolideringsmulighed og foretaget ændringer, der er behov for, kan du oprette en indkøbsordre for de konsoliderede indkøbsrekvisitionslinjer.  

> [!NOTE]
> Ændringer, du laver til en indkøbsrekvisitionslinje på siden **Konsolidering af indkøbsrekvisition**, afspejles på den indkøbsordre, du opretter. I indkøbsrekvisitionen forbliver linjen dog uændret, således at dens historik bevares.  

Du kan oprette en indkøbsordre for indkøbsrekvisitionslinjer, der ikke er berettiget til efterspørgselskonsolidering, eller som ikke er valgt til en konsolideringsmulighed, ved manuelt at behandle linjerne.

### <a name="consolidating-purchase-requisition-lines"></a>Konsoliderende indkøbsrekvisitionslinjer

Processen til efterspørgselskonsolidering starter, når en indkøbsrekvisition godkendes i en arbejdsgang, og hvis budgetstyring er konfigurer for din organisation, når budgetreservationerne og forudgående behæftelser er blevet registreret. Det følgende diagram viser procesforløbet for efterspørgselskonsolidering.  

[![Procesforløb for efterspørgselskonsolidering.](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)  

Følg disse trin for at konsolidere godkendte indkøbsrekvisitionslinjer:

1.  Gennemse godkendte rekvisitionslinjer, der er blevet gemt til manuel behandling, og som er berettiget til efterspørgselskonsolidering.
2.  Vælg linjer, der skal føjes til en konsolideringsmulighed.
3.  Opret en ny konsolideringsmulighed, eller føj rekvisitionslinjer til en eksisterende konsolideringsmulighed.
4.  Foretag de påkrævede ændringer af rekvisitionslinjerne, og fjern de rekvisitionsvarelinjer, som du ikke længere ønsker at inkludere i konsolideringsmuligheden.
5.  Opret indkøbsordrer for konsoliderede rekvisitionslinjer eller for indkøbsrekvisitionslinjer i en konsolideringsmulighed.


## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette en forbrugsrekvisition](tasks/create-requisition-consumption.md)

[Arbejdsgang for indkøbsrekvisitioner](purchase-requisitions-workflow.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]