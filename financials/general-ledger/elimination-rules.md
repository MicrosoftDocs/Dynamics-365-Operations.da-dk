---
title: Elimineringsregler
description: Dette emne indeholder oplysninger om elimineringsregler og de forskellige indstillinger for rapportering om elimineringer.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: db4b05bc55d735513d7580ca5908a1e84eb760c6
ms.openlocfilehash: 152b63fdfc78b3c4e79b93340d18c5cf69257024
ms.lasthandoff: 03/31/2017


---

# <a name="elimination-rules"></a>Elimineringsregler

Dette emne indeholder oplysninger om elimineringsregler og de forskellige indstillinger for rapportering om elimineringer.

Der kræves elimineringsposteringer, når en juridisk enhed for et moderselskab har forretninger med en eller flere juridiske enheder for datterselskaber og bruger konsolideret regnskabsaflæggelse. Konsoliderede regnskaber må kun indeholde transaktioner, der opstår mellem den konsoliderede organisation og de andre enheder uden for de pågældende organisationer. Derfor skal transaktioner mellem juridiske enheder, der er en del af den samme organisation være fjernet, eller elimineres fra regnskabet, så de ikke vises i finansielle rapporter. Der er flere måder at rapportere om elimineringer på:

-   En elimineringsregel kan oprettes og behandles i et konsoliderings- eller elimineringsregnskab.
-   Regnskabsaflæggelse kan bruges til at vise elimineringskonti og -dimensioner for en bestemt række eller kolonne.
-   En særskilt juridisk enhed kan bruges til at bogføre manuelle transaktionsposter for at spore elimineringer.

I dette emne beskrives de elimineringsregler, der behandles i et konsolidering-s eller elimineringsregnskab. Du kan oprette elimineringsregler for at oprette elimineringsposteringer i en juridisk enhed, der er angivet som juridisk destinationsenhed for elimineringer. Denne juridiske destinationsenhed er kendt som juridisk enhed til elimineringen. Der kan oprettes elimineringskladder enten under konsolideringsprocessen eller ved hjælp af et elimineringskladdeforslag. Før du opretter elimineringsregler, skal du sætte dig ind i følgende begreber:

-   **Juridisk kildeenhed** – Den juridiske enhed, hvor de beløb, der elimineres, blev bogført.
-   **Juridisk destinationsenhed** – Den juridiske enhed, hvor elimineringsregler bogføres.
-   **Juridisk elimineringsenhed** – Den juridiske enhed, der er angivet som den juridiske destinationsenhed for elimineringer.
-   **Konsolideret juridisk enhed** – Den juridiske enhed, der er oprettet til at rapportere økonomiske resultater for en gruppe juridiske enheder. De økonomiske data fra de juridiske enheder er konsolideret i denne juridiske enhed, og derefter oprettes der en økonomisk rapport ved hjælp af de kombinerede data.

Følgende tabel viser de typer transaktioner, der måske skal elimineres.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Konteringstype</th>
<th>Eksempel:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Salgsordrepost og fakturering (centraliseret behandling)</td>
<td>Du sælger et produkt til en kunde på vegne af en anden juridisk enhed i organisationen.</td>
</tr>
<tr class="even">
<td>Salgsordrepost (intern handel/ekstern handel) og fakturering</td>
<td>Du sælger produkter mellem juridiske enheder i organisationen.</td>
</tr>
<tr class="odd">
<td>Indkøbsordrer (centraliseret behandling)</td>
<td>Du køber lager, forsyninger, tjenester, anlægsaktiver og andre produkter fra en leverandør på vegne af en anden juridisk enhed i din organisation.</td>
</tr>
<tr class="even">
<td>Lagerstyring (intern handel/ekstern handel)</td>
<td><ul>
<li>Du kan overføre lageret fra én juridisk enhed til anlægsaktiver i en anden juridisk enhed i organisationen.</li>
<li>Du overfører én juridisk enheds lager til lageret i en anden juridisk enhed i organisationen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lagersporing i transit</td>
<td>Du overfører varer mellem lagersteder i den samme juridiske enhed, men på tværs af forskellige geografiske områder.</td>
</tr>
<tr class="even">
<td>Centraliseret fakturabehandling for kreditorer</td>
<td>Du registrerer en faktura på vegne af en anden juridisk enhed i organisationen.</td>
</tr>
<tr class="odd">
<td>Centraliseret betalingsbehandling for kreditorer</td>
<td>Du betaler en faktura på vegne af en anden juridisk enhed i organisationen.</td>
</tr>
<tr class="even">
<td>Likviditetsstyring og aktier (centraliseret behandling)</td>
<td><ul>
<li>Du behandler skattebetalinger, skatterefusioner, rentetillæg, lån, forskud, udbyttebetalinger og forudbetalte royalties eller provisioner.</li>
<li>Du betaler en udgift på vegne af en anden juridisk enhed i organisationen. Fakturaen angives i bøgerne for den juridiske destinationsenhed, og du skal udligne mellem juridiske enheder. En juridisk enhed betaler f.eks. udgiftsrapporten for en medarbejder i en anden juridisk enhed. I dette tilfælde har medarbejderens udgiftsrapport udgifter, der er relateret til en anden juridisk enhed.</li>
<li>Du overføre penge fra én juridisk enhed til en anden i organisationen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Debitorer (centraliseret behandling)</td>
<td>Du modtager kontanter for en anden juridisk enheds debitorfaktura, og du indsætter checken på den pågældende juridiske enheds bankkonto.</td>
</tr>
<tr class="even">
<td>Løn (centraliseret behandling, intern handel/ekstern handel)</td>
<td><ul>
<li>Du betaler løn for en anden juridisk enhed. En juridisk enhed betaler f.eks. egen løn for sine medarbejdere, men tilbagefører arbejde, som en medarbejder har udført for en anden juridisk enhed, under denne lønkørsel. Eller en medarbejder har arbejdet deltids for den juridiske enhed A og deltids for den juridiske enhed B, og frynsegoderne går på tværs af al løn. I disse tilfælde vil medarbejderens løn omfatte løn fra begge juridiske enheder. Ikke blot er lønnen bogført, men afgifter, frynsegoder, fradrag og periodiseret løn bogføres også.</li>
<li>Du overfører arbejdskraft fra én afdeling eller division til en anden.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Anlægsaktiver (intern handel/ekstern handel)</td>
<td>Du overfører anlægsaktiver til en anden juridisk enheds anlægsaktiver eller lager.</td>
</tr>
<tr class="even">
<td>Tildelinger (intern handel/ekstern handel)</td>
<td>Du kan behandle virksomhedstildelinger. Tildelinger er aktiviteter på en hvilken som helst konto, der er tildelt, uanset hvilket modul de stammer fra.</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Eksempel:
Din juridiske enhed, juridisk enhed A, sælger dimser til en anden juridisk enhed i organisationen, juridisk enhed B. Følgende eksempel viser, hvordan transaktioner, der forekommer mellem de to juridiske enheder, muligvis skal elimineres:

-   Juridisk enhed A en sælger en dims, der koster 10,00, til juridisk enhed B for 10,00.
-   Juridisk enhed A sælger en dims, der koster 10,00, til juridisk enhed B for 10,00 plus 2,00 i faktiske leveringsomkostninger.
-   Juridisk enhed A sælger en dims, der koster 10,00, til juridisk enhed B for 15,00 og opnår fortjeneste på salget.
-   Juridisk enhed A sælger en dims, der koster 10,00, til juridisk enhed B for 15,00 og registrerer halvdelen af fortjenesten på salget. Juridisk enhed B får den anden halvdel af fortjenesten på salget. Derfor deles indtægten. En delt indtægt fungerer som incitament for at bestille fra en anden juridisk enhed i organisationen i stedet for fra en ekstern organisation.

Alle disse transaktioner skaber interne transaktioner, der bogføres på skyldig til- og skyldig fra-konti. Derudover kan disse transaktioner omfatte avance- eller tabsbeløb, når beløbet for det interne salg ikke er lig med kostprisen for solgte varer

## <a name="set-up-elimination-rules"></a>Konfigurere elimineringsregler
Når du opretter elimineringsregler i Dynamics 365 for operationer, anbefales det, at du opretter en økonomisk dimension, specielt med henblik på bortskaffelse. De fleste kunder navngive den, samhandelspartnere Partner eller lignende. Hvis du beslutter ikke at bruge en økonomisk dimension, derefter skal du have hovedkonti, der er specifikke for kun interne transaktioner. 

Opsætningen for elimineringer, der findes i området Opsætning i modulet konsolideringer. Når du angiver en beskrivelse af reglen, skal du vælge det regnskab, som elimineringskladden bogføres til. Dette skal være et firma, der har **brug til økonomisk eliminering** valgt i opsætningen af juridisk enhed. 

Du kan angive en dato, hvor elimineringsreglen træder i kraft, og når det er udløbet, hvis det er nødvendigt. Du skal angive **aktive** til **Ja** Hvis det skal være tilgængelige i forslagsprocessen eliminering. Vælg et kladdenavn, der er en slags **eliminering**.

Når du har defineret de grundlæggende elementer, du kan definere de faktiske behandling af regler ved at klikke på **linjer**. Der er to muligheder for elimineringer, afhjælper bevægelse beløbet eller definere et fast beløb. 

Vælg kildekontoen. Du kan bruge en stjerne (\*) som jokertegn. For eksempel 1\* ville vælge alle konti, der starter med 1, som en datakilde til fordelingen. 

Når du har valgt dine kildekonti, den **konto specifikation** bestemmer konto fra det destinationsregnskab, der bruges. Vælg **kilde** Hvis du vil bruge den samme primære konto, der er defineret i den **kilde** konto. Hvis du vælger **brugerdefinerede**, og derefter skal du angive en destinationskonto. 

Specifikation af dimension fungerer på samme måde. Hvis du vælger **kilde**, bruges de samme dimensioner i modtagervirksomheden som kilderegnskab. Hvis du vælger **brugerdefinerede**, skal du angive dimensionerne i modtagervirksomheden ved at klikke på den **destinationsdimensioner** menupunkt. 

Vælg kildedimensioner og de økonomiske dimensioner og værdier, der bruges som kilde til fjernelse.

## <a name="process-elimination-transactions"></a>Anvend elimineringsposter
Der er to måder til at behandle elimineringsposteringer under processen konsolideres online eller ved at oprette en elimineringskladden og kører processen til fjernelse. Dette afsnit fokuserer på oprettelsen af kladden og kører elimineringsprocessen. 

Vælg i en virksomhed, der er defineret som et elimineringsregnskab, **elimineringskladden** i modulet konsolideringer. Når du har valgt kladdenavnet, skal du klikke på **linjer**. Du kan køre forslaget ved at vælge den **forslag** i menuen og derefter vælge **elimineringsforslag**.

Vælg det regnskab, der er kilden til de konsoliderede data, og vælg derefter den regel, du vil behandle. Angiv en startdato for at starte søgningen efter eliminering beløb og en slutdato for at søge slutdato for eliminering beløb. Den **bogføringsdato GL** felt er den dato, der bruges til bogføring af kladde i Finans. Når du klikker på **OK**, kan du gennemse beløbene og bogføre kladden.


