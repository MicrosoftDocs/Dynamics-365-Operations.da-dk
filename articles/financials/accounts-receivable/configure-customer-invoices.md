---
title: Oprette en debitorfaktura
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2a668e390935e157d9fc7f0ef597f25c2a7b9950
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="create-a-customer-invoice"></a>Oprette en debitorfaktura

[!include[banner](../includes/banner.md)]


En **debitorfaktura for en salgsordre** er en regning, som er relateret til et salg, og som en organisation giver til en kunde. Denne type debitorfaktura oprettes på basis af en salgsordre, som omfatter ordrelinjer og varenumre. Varenumre angives og bogføres i finansmodulet. Reskontrokladdeposter er ikke tilgængelige for en debitorfaktura for en salgsordre. Du kan finde flere oplysninger i [Oprette salgsordrefakturaer](tasks/create-sales-order-invoices.md).

En **fritekstfaktura** er ikke knyttet til en salgsordre. Den indeholder ordrelinjer, der omfatter finanskonti, fritekstbeskrivelser og et salgsbeløb, som du selv angiver. Du kan ikke angive et varenummer på en faktura af denne type. Du skal angive de relevante oplysninger om moms. Der er angivet en hovedkonto for salget på hver fakturalinje, som du kan fordele på flere forskellige finanskonti ved at klikke på **Distribuer beløb** på siden **Fritekstfaktura**. Derudover bogføres debitorsaldoen på samlekontoen fra den posteringsprofil, der bruges til fritekstfakturaen.

Du kan få flere oplysninger på:

[Oprette en fritekstfaktura](tasks/create-free-text-invoice.md)

[Oprette en fritekstskabelon](tasks/create-free-text-invoice-template.md)

[Tildele en skabelon til fritekstfakturaer til en debitor](tasks/assign-free-text-invoice-template-customer.md)

[Generere og bogføre tilbagevendende fritekstfakturaer](tasks/post-recurring-free-text-invoices.md)


En **proformafaktura** er en faktura, der udarbejdes som et estimat over det faktiske fakturabeløb, før fakturaen bogføres. Du kan udskrive en proformafaktura for en debitorfaktura for en salgsordre eller for en fritekstfaktura.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>Bogføre og udskrive individuelle debitorfakturaer, der er baseret på salgsordrer
Brug denne proces til at oprette en faktura, der er baseret på en salgsordre. Det kan du f.eks. gøre, hvis du beslutter at fakturere debitoren, før du leverer varerne eller tjenesterne. 

Når du bogfører en faktura, opdateres antallet i **Fakturarestmængde** for de enkelte varer med det samlede fakturerede antal fra den valgte salgsordre. Hvis både antallet **Fakturarestmængde** og antallet **Levér rest** for alle varer i salgsordren er 0 (nul), ændres salgsordrens status til **Faktureret**. Hvis antallet for **Fakturarestmængde** ikke er 0 (nul), forbliver status for salgsordren uændret, og der kan bogføres ekstra fakturaer for den.

Du kan få vist salgsordrernes status på listesiden **Alle salgsordrer**. Brug listesiden **Åbn debitorfakturaer** til at få vist de fakturaer, du har bogført.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>Bogføre og udskrive individuelle debitorfakturaer, der er baseret på følgesedler og datoen
Brug denne proces, når der er bogført en eller flere følgesedler til salgsordren. Debitorfakturaen er baseret på disse følgesedler og afspejler antallene i dem. De økonomiske oplysninger til fakturaen er baseret på de oplysninger, der angives, når du bogfører fakturaen. 

Du kan oprette en debitorfaktura, der er baseret på de linjeelementer på følgesedlen, som er afsendt til dato, selvom alle varerne i en bestemt salgsordre endnu ikke er afsendt. Det kan du f.eks. gøre, hvis din juridiske enhed udsteder én faktura pr. debitor pr. måned, som dækker alle de leverancer, du sender i den pågældende måned. Hver følgeseddel repræsenterer en dellevering eller en komplet levering af varerne i salgsordren. 

Når du bogfører fakturaen, opdateres antallet **Fakturarestmængde** for hver vare med det samlede beløb for de leverede antal fra de valgte følgesedler. Hvis både antallet **Fakturarestmængde** og antallet **Levér rest** for alle varer i salgsordren er 0 (nul), ændres salgsordrens status til **Faktureret**. Hvis antallet for **Fakturarestmængde** ikke er 0 (nul), forbliver status for salgsordren uændret, og der kan bogføres ekstra fakturaer for den. 

Lagerposteringer opdateres med fakturanummeret, og status i feltet **Linjestatus** i salgsordren ændres til **Faktureret**. 

Se salgsordrernes status på listesiden **Alle salgsordrer**.

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>Konsolidere salgsordrer eller følgesedler til bogføring
Brug denne fremgangsmåde, når en eller flere salgsordrer, der er klar til at blive faktureret, og du vil konsolidere dem i én faktura. 

Du kan vælge flere fakturaer på listesiden **Salgsordre** og derefter bruge **Generer fakturaer** for at sammenflette dem. På siden **Bogføring af faktura** kan du ændre indstillingen **Samleordre** til at opsummere ved ordrenummer (hvor der er flere følgesedler for en enkelt salgsordre) eller efter fakturakonto (hvor der er flere salgsordrer for en enkelt faktura). Brug knappen **Arranger** for at konsolidere salgsordrer til enkelte fakturaer, der er baseret på indstillingen **Samleordre**.

## <a name="additional-settings-that-change-the-posting-behavior"></a>Yderligere indstillinger, der ændrer funktionsmåden for bogføring
Følgende felter ændrer funktionaliteten af bogføringsprocessen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Felt</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Antal</td>
<td>Vælg de antal, som bogføringen af dokumentet skal baseres på. Indstillingerne, der er tilgængelige, afhænger af den type dokument, du bogfører, f.eks. en følgeseddel eller en faktura.
<ul>
<li><strong>Levér nu</strong> – Vælg alle de mængder, der er angivet i feltet <strong>Levér nu</strong>. Du kan bruge denne indstilling til at bekræfte eller levere en delordre.</li>
<li><strong>Plukket</strong> – Vælg alle de mængder, der er plukket.</li>
<li><strong>Alle</strong> – Vælg alle antal i salgsordren, der endnu ikke er opdateret af den aktuelle dokumenttype.</li>
<li><strong>Følgeseddel</strong> – Vælg alle de antal, der er opdateret af en følgeseddel,.</li>
<li><strong>Plukket antal og ikke-lagerførte produkter</strong> – Vælg alle de mængder, der er plukket, og alle de produktmængder, der ikke er på lager.</li>
</ul></td>
</tr>
<tr class="even">
<td>Bogfører</td>
<td><ul>
<li>Vælg denne indstilling for at journalisere salgsordren.</li>
<li>Fjern markeringen af denne indstilling for at udskrive en proformasalgsordre. <strong>Bemærk!</strong> Hvis du har indgået en aftale om en betalingsplan, vises betalingsplanen ikke på proformasalgsordren. Betalingsplaner vises kun på de egentlige salgsordrer.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vælg senere</td>
<td>Vælg denne indstilling for at anvende den valgte forespørgsel senere. Denne indstilling anvendes til batchjob. Forespørgslen køres, når batchjobbet køres.</td>
</tr>
<tr class="even">
<td>Reducer antal</td>
<td>Vælg denne indstilling for automatisk at reducere det leverede antal, når dokumentet bogføres, så det leverede antal er lig med den disponible beholdning.</td>
</tr>
<tr class="odd">
<td>Udskriv</td>
<td>Vælg, hvornår dokumenter skal udskrives:
<ul>
<li><strong>Løbende</strong> – Udskriv dokumenter, når de enkelte fakturaer er opdateret.</li>
<li><strong>Efter</strong> – Udskriv dokumenter, efter alle fakturaerne er blevet opdateret.</li>
</ul>
<strong>Bemærk!</strong> Feltet <strong>Udskrivning</strong> er kun tilgængeligt, hvis du vælger indstillingen <strong>Udskrivning af faktura</strong>, <strong>Udskrivning af bekræftelse</strong>, <strong>Udskrivning af plukliste</strong> eller <strong>Udskrivning af følgeseddel</strong>. På siden <strong>Formsortering</strong> har du f.eks. konfigureret systemet til at sortere efter fakturakonto. Du kan da vælge <strong>Efter</strong> for at udskrive dokumenter i en batch, der er sorteret efter fakturakonto. Ellers udskrives dokumenter, før behandlingen er fuldført, og dokumenterne sorteres ikke i den rækkefølge, der er angivet på siden <strong>Formsortering</strong>.</td>
</tr>
<tr class="even">
<td>Udskrivning af faktura</td>
<td>Vælg denne indstilling for at udskrive fakturaen. Hvis denne indstilling er slået fra, kan du bogføre en faktura uden at udskrive den.</td>
</tr>
<tr class="odd">
<td>Send e-mail</td>
<td>Vælg denne indstilling for at sende fakturaen for en salgsordre som en vedhæftet fil i en e-mail til en kunde, efter at fakturaen er blevet bogført. Vedhæftede filer sendes som PDF- og XML-filer. Denne indstilling er kun tilgængelig, hvis du vælger indstillingen <strong>Aktivér CFD (elektroniske fakturaer)</strong> på siden <strong>Parametre for elektronisk faktura</strong>. <strong>Bemærk!</strong> (MEX) Dette kontrolelement er kun tilgængeligt for juridiske enheder, hvis primære adresse er i Mexico.</td>
</tr>
<tr class="even">
<td>Brug destination for udskriftsstyring</td>
<td>Vælg denne indstilling for at bruge de udskriftsindstillinger, der er angivet for posteringen, dokumentet eller modulet på siden <strong>Opsætning af udskriftsstyring</strong>.</td>
</tr>
<tr class="odd">
<td>Kontrollér kreditmaks.</td>
<td>Vælg de oplysninger, der skal analyseres, når der udføres en kontrol af kreditmaksimum.
<ul>
<li><strong>Ingen</strong> – Der er ingen krav i forbindelse med kontrol af kreditmaksimum.</li>
<li><strong>Saldo</strong> - Kreditmaksimum kontrolleres i forhold til debitorsaldoen.</li>
<li><strong>Saldo + følgeseddel eller produktkvittering</strong> – Kreditmaksimum kontrolleres i forhold til debitorsaldoen og leverancer.</li>
<li><strong>Saldo+Alt</strong> – Kreditmaks. kontrolleres i forhold til debitorsaldoen, leverancer og åbne ordrer.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kreditrettelse</td>
<td>Vælg denne indstilling for at få vist kreditnotaen som debet i bilagsposteringerne.</td>
</tr>
<tr class="odd">
<td>Kredit, restantal</td>
<td>Hvis du bogfører en kreditnota, skal du vælge denne indstilling, hvis du vil beholde den resterende mængde i ordren. Hvis denne indstilling fravælges, angives den resterende mængde til 0 (nul).</td>
</tr>
<tr class="even">
<td>Samleopdatering for</td>
<td>Vælg, hvordan flere salgsordrer skal opsummeres:
<ul>
<li><strong>Ingen</strong> – Opsummer ikke salgsordrer. Der oprettes f.eks. en separat faktura for hver enkelt salgsordre.</li>
<li><strong>Fakturakonto</strong> – Opsummer alle valgte ordrer, baseret på de kriterier, der er angivet på siden <strong>Samleopdateringsparametre</strong>.</li>
<li><strong>Ordre</strong> – Opsummer en udvalgt række ordrer i én ordre, som du angiver. Ordrerne opsummeres baseret på de kriterier, der er angivet på siden <strong>Samleopdateringsparametre</strong>. Hvis du vælger denne indstilling, skal du vælge en værdi i feltet <strong>Salgsordrer</strong>.</li>
<li><strong>Automatisk samling</strong> – Hvis der er angivet samleopdateringer på siden <strong>Samleopdatering</strong>, skal du samle alle de valgte ordrer baseret på de kriterier, der er angivet på siden <strong>Samleopdateringsparametre</strong>. Hvis du ikke har angivet samleopdateringer, bliver ordren bogført særskilt.</li>
<li><strong>Følgeseddel</strong> – Opsummer en udvalgt række ordrer i én faktura for hver følgeseddel. Denne indstilling kan kun benyttes, hvis der er valgt <strong>Følgeseddel</strong> i feltet <strong>Antal</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>






