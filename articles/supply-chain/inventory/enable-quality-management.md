---
title: Oversigt over kvalitetsstyring
description: I dette emne beskrives det, hvordan du kan bruge kvalitetsstyring i Microsoft Dynamics 365 for Finance and Operations til at forbedre produktkvaliteten i forsyningskæden.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1630d13437d7e930fdf32ed5fdc61fc62bc33817
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557494"
---
# <a name="quality-management-overview"></a>Oversigt over kvalitetsstyring

[!include [banner](../includes/banner.md)]

I dette emne beskrives det, hvordan du kan bruge kvalitetsstyring i Microsoft Dynamics 365 for Finance and Operations til at forbedre produktkvaliteten i forsyningskæden.

Kvalitetsstyring kan hjælpe dig med at administrere behandlingstid, når du håndterer ikke-standardiserede produkter, uanset deres oprindelsessted. Fordi diagnosticeringstyper er knyttet til rapportering af korrektion, kan Microsoft Dynamics 365 for Finance and Operations planlægge opgaver for at løse problemer og forhindre dem i fremtiden.

Ud over funktionalitet til administration af uoverensstemmelse omfatter kvalitetsstyring funktionalitet til sporing af problemer efter problemtype (også interne problemer) og til identificering af løsninger som kortsigtede eller langsigtede. Statistik over nøgletal (KPI'er) giver indsigt i historikken for tidligere problemer med uoverensstemmelse, og de løsninger, der blev anvendt til at rette dem. Du kan bruge historikdata til at gennemgå effektiviteten af tidligere kvalitetsmål og fastlægge passende foranstaltninger, der skal bruges i fremtiden.

Når du opretter en kvalitetstilknytning, kan Finance and Operations oprette kvalitetsordrer til forskellige forretningsprocesser, hændelser og betingelser. Kvalitetstilknytningen kan dække en bestemt vare, en bestemt gruppe varer eller alle varer.

## <a name="examples-of-the-use-of-quality-management"></a>Eksempler på brug af kvalitetsstyring
Kvalitetsstyring er fleksibel og kan gennemføres på forskellige måder for at opfylde kravene på bestemte niveauer i forsyningskædeoperationer. Eksemplerne nedenfor viser mulige anvendelser af disse funktioner:

-   Automatisk starte en proces for kvalitetskontrol baseret på foruddefinerede kriterier (ved lagerregistreringen af en indkøbsordre fra en bestemt leverandør).
-   Spærre lageret under kontrol for at forhindre, at ikke-godkendt lagerbeholdning bliver brugt (fuld spærring af indkøbsordreantal).
-   Bruge vareprøve som en del af en kvalitetstilknytning til at definere beløbet af det aktuelle fysiske lager, der skal undersøges. Vareprøver kan baseres på faste antal eller en procentdel.
-   Opret kvalitetsordrer for delleverancer. For at oprette en kvalitetsordre, der er baseret på det antal, der fysisk er modtaget med en ordre, skal du markere afkrydsningsfeltet **Pr. opdateret antal** i formularen **Vareprøve**.
-   Oprette testtyper, der omfatter minimum, maksimum og måltestværdier og udføre kvalitative kontra kvantitative test, der har foruddefinerede valideringsresultater.
-   Angive et acceptabelt kvalitetsniveau (AQL) for at styre tolerancer for kvalitetsmål.
-   Angive de ressourcer, som en inspektionshandling kræver, f.eks. et testområde og testinstrumenter.

## <a name="working-with-quality-associations"></a>Arbejde med kvalitetstilknytninger
Den forretningsproces, der bruger en kvalitetstilknytning, kan knyttes til forskellige kildedokumenter, f.eks. indkøbsordrer, salgsordrer eller produktionsordrer.

De enkelte kvalitetstilknytningsposter definerer de test, det acceptable kvalitetsniveau (AQL) og den vareprøveplan, der gælder for de kvalitetsordrer, der oprettes. Du skal definere en kvalitetstilknytningspost for hver ændring i en forretningsproces. Du kan f.eks. angive en kvalitetstilknytning, der genererer en kvalitetsordre, når en produktkvittering for en indkøbsordre opdateres. Afhængigt af opsætningen af udførelsesplanen kan selve den udløsende proces blive blokeret, mens der er en åben kvalitetsordre, eller de næste processer, som f.eks. fakturering, kan blive blokeret.

**Bemærk!** Der kan være åbne kvalitetsordrer, men lagerantal blokeres automatisk fra at blive udstedet. Afhængigt af indstillingen **Fuld spærring** på siden **Stikprøver af varer** er antallet enten kvantiteten i kvalitetsordren eller kvantiteten i kildedokumentlinjen.

For en given forretningsproces identificerer kvalitetstilknytningsposten hændelsen og de betingelser, som der oprettes en kvalitetsordre for. Betingelserne kan være specifikke for et sted eller en juridisk enhed. En kvalitetsordre, der involverer destruktive prøvninger, kan kun oprettes, når der findes en disponible lagerbeholdning for hændelsen.

I følgende eksempel vises, hvordan en kvalitetstilknytningspost defineres for variationerne i de enkelte forretningsprocesser. Eksemplerne vises også i følgende tabel som en oversigt over de hændelser og betingelser, der er defineret af en kvalitetstilknytningspost.

<table>
<tbody>
<tr>
<th>Referencetype</th>
<th>Hændelsestype</th>
<th>Udførelse</th>
<th>Hændelsesspærring</th>
<th>Dokumentreference</th>
</tr>
<tr>
<td>Lager</td>
<td>Ikke tilgængelig</td>
<td>Ikke tilgængelig</td>
<td>Ingen</td>
<td>Alle</td>
</tr>
<tr>
<td rowspan="7">Salg</td>
<td rowspan="4">Plukproces er planlagt</td>
<td rowspan="4">Før</td>
<td>Ingen</td>
<td rowspan="22">Bestemt id, gruppe eller kun alle</td>
</tr>
<tr>
<td>Plukproces</td>
</tr>
<tr>
<td>Følgeseddel</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="3">Følgeseddel</td>
<td rowspan="3">Før</td>
<td>Ingen</td>
</tr>
<tr>
<td>Følgeseddel</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="15">Indkøb</td>
<td rowspan="7">Tilgangsliste</td>
<td rowspan="4">Før</td>
<td>Ingen</td>
</tr>
<tr>
<td>Tilgangsliste</td>
</tr>
<tr>
<td>Produktkvittering</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="3">Efter</td>
<td>Ingen</td>
</tr>
<tr>
<td>Produktkvittering</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="3">Registrering</td>
<td rowspan="3">Ikke tilgængelig</td>
<td>Ingen</td>
</tr>
<tr>
<td>Produktkvittering</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="5">Produktkvittering</td>
<td rowspan="3">Før</td>
<td>Ingen</td>
</tr>
<tr>
<td>Produktkvittering</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="2">Efter</td>
<td>Ingen</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="8">Produktion</td>
<td rowspan="3">Registrering</td>
<td rowspan="3">Ikke tilgængelig</td>
<td>Ingen</td>
<td rowspan="12">Alle</td>
</tr>
<tr>
<td>Færdigmeld</td>
</tr>
<tr>
<td>Afslut</td>
</tr>
<tr>
<td rowspan="5">Færdigmeld</td>
<td rowspan="3">Før</td>
<td>Ingen</td>
</tr>
<tr>
<td>Færdigmeld</td>
</tr>
<tr>
<td>Afslut</td>
</tr>
<tr>
<td rowspan="2">Efter</td>
<td>Ingen</td>
</tr>
<tr>
<td>Afslut</td>
</tr>
<tr>
<td rowspan="4">Karantæne</td>
<td rowspan="3">Færdigmeld</td>
<td rowspan="2">Før</td>
<td>Færdigmeld</td>
</tr>
<tr>
<td>Afslut</td>
</tr>
<tr>
<td>Efter</td>
<td>Afslut</td>
</tr>
<tr>
<td>Afslut</td>
<td>Før</td>
<td>Afslut</td>
</tr>
<tr>
<td rowspan="3">Ruteoperation</td>
<td rowspan="3">Færdigmeld</td>
<td rowspan="2">Før</td>
<td>Ingen</td>
<td rowspan="3">Bestemt id, gruppe eller alle, og ressourcespecifik, gruppe eller alle</td>
</tr>
<tr>
<td>Færdigmeld</td>
</tr>
<tr>
<td>Efter</td>
<td>Ingen</td>
</tr>
<tr>
<td rowspan="3">Produktion af samprodukter</td>
<td>Registrering</td>
<td>Ikke tilgængelig</td>
<td rowspan="3">Ingen</td>
<td rowspan="3">Alle</td>
</tr>
<tr>
<td rowspan="2">Færdigmeld</td>
<td>Før</td>
</tr>
<tr>
<td>Efter</td>
</tr>
</tbody>
</table>

Tabellen nedenfor indeholder flere oplysninger om, hvordan kvalitetsordrer kan oprettes for bestemte typer processer.
<div class="tableSection">

<table>
<tbody>
<tr>
<th>Procestype</th>
<th>Når kvalitetsordrer kan genereres automatisk</th>
<th>Når kvalitetsordrer kan genereres, hvis destruktiv prøvning er påkrævet</th>
<th>Betingelsesoplysninger</th>
<th>Manuel oprettelse af oplysninger</th>
</tr>
<tr>
<td>Indkøbsordre</td>
<td>Før eller efter en tilgangsliste eller produktkvittering for det materiale, der er modtaget, bogføres</td>
<td>Efter produktkvitteringen for det materiale, der er modtaget, bogføres, da materialet skal være tilgængelig til destruktiv prøvning</td>
<td>Behovet for en kvalitetsordre kan afhænge af en bestemt lokation, vare eller kreditor eller en kombination af disse forhold.</td>
<td>En manuelt oprettet kvalitetsordre, der refererer til en indkøbsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</td>
</tr>
<tr>
<td>Karantæneordre</td>
<td>Før eller efter karantæneordren rapporteres som færdigmeldt eller afsluttet</td>
<td>Kvalitetsordrer, der kræver destruktive prøvninger kan ikke oprettes. Det antages, at funktionerne i karantæneordren håndterer bortskaffelsen af det materiale, der destrueres.</td>
<td>Behovet for en kvalitetsordre kan afhænge af en bestemt lokation, vare eller kreditor eller en kombination af disse forhold.</td>
<td>En manuelt oprettet kvalitetsordre, der refererer til en karantæneordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</td>
</tr>
<tr>
<td>Salgsordre</td>
<td>Før en planlagt plukproces eller opdatering af følgesedlen for de varer, der skal leveres</td>
<td>På alle trin</td>
<td>Behovet for en kvalitetsordre kan afhænge af en bestemt lokation, vare eller debitor eller en kombination af disse forhold.</td>
<td>En manuelt oprettet kvalitetsordre, der refererer til en salgsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</td>
</tr>
<tr>
<td>Produktionsordre</td>
<td>Før eller efter det færdigmeldte antal for produktionsordren er rapporteret</td>
<td>Efter det færdigmeldte antal for produktionsordren er rapporteret</td>
<td>Behovet for en kvalitetsordre kan afhænge af en bestemt lokation eller vare eller en kombination af disse forhold.</td>
<td>En manuelt oprettet kvalitetsordre, der refererer til en produktionsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</td>
</tr>
<tr>
<td>Produktionsordre, der har en ruteoperation</td>
<td>Før eller efter rapporten er færdigmeldt for en operation</td>
<td>Efter færdigrapportering af produktionen for den sidste operation</td>
<td>Behovet for en kvalitetsordre kan afhænge af en bestemt lokation, vare eller operationsressource eller en kombination af disse forhold.</td>
<td>En manuelt oprettet kvalitetsordre, der refererer til en ruteoperation, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</td>
</tr>
<tr>
<td>Lager</td>
<td>En kvalitetsordre kan ikke genereres automatisk for en transaktion i en lagerkladde eller flytteordretransaktioner.</td>
<td></td>
<td></td>
<td>En kvalitetsordre skal oprettes manuelt for en vares lagerantal. Fysisk disponibel lagerbeholdning er påkrævet.</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a>Kvalitetsstyringssider
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Side</th>
<th>Beskrivelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kvalitetstilknytninger</td>
<td>Se de tidligere afsnit i denne artikel.</td>
<td>En kvalitetstilknytning angiver alle følgende oplysninger for en kvalitetsordre, der oprettes:
<ul>
<li>Posteringshændelsen</li>
<li>Det sæt test, der skal udføres på varerne</li>
<li>Det acceptable kvalitetsniveau (AQL)</li>
<li>Prøveplanen</li>
</ul>
Du skal definere en kvalitetstilknytning for hver afvigelse i en forretningsproces, der kræver automatisk generering af kvalitetsordrer. For eksempel kan der oprettes en kvalitetsordre i forretningsprocesserne for indkøbsordrer, karantæneordrer, salgsordrer og produktionsordrer.</td>
</tr>
<tr class="even">
<td>Test</td>
<td>Du kan bruge denne side til at definere og få vist de individuelle test, der bestemmer, om produkterne opfylder kvalitetsspecifikationerne. Du kan tildele en eller flere individuelle test til en testgruppe. Når du gør det, skal du også angive testspecifikke oplysninger, f.eks. de acceptable måleværdier. Måleværdier bruges til kvantitative test, og testvariabler bruges til kvalitative test.
<ul>
<li>En kvantitativ test har testtypen <strong>Heltal</strong> eller <strong>Del</strong> og har også en angivet måleenhed. Kvalitetsspecifikationer og testresultater er udtrykt som tal.</li>
<li>En kvalitativ test har testtypen <strong>Indstilling</strong>. Kvalitative test forudsætter flere oplysninger om den testvariabel, der måles, og de faste indstillinger. Kvalitetsspecifikationer og testresultater er udtrykt i overensstemmelse med et udfald.</li>
</ul></td>
<td>Et produktionsfirma udfører to test af købt materiale: en kvantitativ test for materialets kvalitet og en kvalitetstest for skader på emballagen. Firmaet definerer flere oplysninger om den kvalitative test for at identificere testvariablen (beskadiget emballage) og udfaldet. Firmaet bruger siden <strong>Testgrupper</strong> til at tildele de to test til en testgruppe og til at angive de testspecifikke oplysninger. Testgruppen tildeles til en kvalitetsordre, så firmaet kan rapportere testresultaterne for de to test.</td>
</tr>
<tr class="odd">
<td>Testgrupper</td>
<td>Brug denne side til at konfigurere, redigere og få vist testgrupper og individuelle test, der er tildelt til en testgruppe. I den øverste rude vises testgrupper, og i den nederste gruppe vises de test, der er knyttet til en valgt testgruppe. Du kan tildele flere politikker til en testgruppe, f.eks. en prøveplan, et acceptabelt kvalitetsniveau (AQL) og kravet om destruktiv test. Når du knytter en individuel test til en testgruppe, definerer du flere oplysninger, f.eks. rækkefølge, dokumenter og gyldighedsdatoer. For kvantitative test skal de oplysninger, du angiver, også omfatte acceptable målingsværdier. For kvalitative test skal oplysningerne også omfatte testvariablen og standardudfaldet. Den testgruppe, der tildeles til en kvalitetsordre, definerer det testsæt, der skal som standard skal udføres på den angivne vare. Du kan dog tilføje, slette eller ændre test i kvalitetsordren. Testresultaterne rapporteres for hver test i en kvalitetsordre.</td>
<td>En produktionsvirksomhed definerer en testgruppe for hver afvigelse fra firmaets retningslinjer for kvalitet. De forskellige testgrupper reflekterer forskelle i prøveplaner, hvilke testsæt der skal udføres sammen, det acceptable kvalitetsniveau og andre faktorer. For kvantitative test er der også forskelle i de acceptable måleværdier. Virksomheden sikrer sig, at retningslinjerne for kvalitet følges, ved at tildele en testgruppe til hver enkelt regel for automatisk oprettelse af kvalitetsordrer på siden <strong>Kvalitetstilknytning</strong> og tildeler også en testgruppe til kvalitetsordrer, der oprettes manuelt.</td>
</tr>
<tr class="even">
<td>Varekvalitetsgrupper</td>
<td>Du kan bruge denne side til at konfigurere, redigere og få vist de varer, der er tildelt en kvalitetsgruppe, eller de kvalitetsgrupper, der er tildelt en vare. En kvalitetsgruppe repræsenterer almindelige testkrav til varer. Når du har defineret testkravene på siden <strong>Testgrupper</strong>, kan du definere reglerne for automatisk generering af kvalitetsordrer. For at forenkle processen skal du undlade at definere regler for de enkelte varer. I stedet skal du angive regler for en kvalitetsgruppe ved hjælp af siden <strong>Kvalitetstilknytninger</strong>. Du kan også bruge siden <strong>Varekvalitetsgrupper</strong> for en valgt kvalitetsgruppe for at tildele relevante varer til den pågældende gruppe. Du kan også bruge siden <strong>Varekvalitetsgrupper</strong> for en valgt kvalitetsgruppe for en valgt vare for at tildele relevante kvalitetsgrupper til den pågældende vare.</td>
<td>En produktionsvirksomhed indkøber forskellige råvarer, der har samme testkrav til indgående inspektion. Virksomheden definerer en kvalitetsgruppe og tildeler derefter kvalitetsgruppen de varenumre, der er knyttet gruppen. Senere indkøber virksomheden en ny type råvarer med de samme testkrav. I stedet for at konfigurere nye testkrav til de nye råvarer føjer virksomheden varenummeret på de nye råvarer til den eksisterende kvalitetsgruppe. Den samme produktionsvirksomhed producerer desuden varer med de samme produktionstestkrav og leverer varer med de samme krav til test før forsendelse. Virksomheden definerer yderligere to kvalitetsgrupper og tildeler derefter hver gruppe de relevante varenumre.</td>
</tr>
<tr class="odd">
<td>Testvariabler</td>
<td>Brug denne side til at angive og få vist variabler, der er tilknyttet en kvalitativ test. Du kan angive faste udfald, der repræsenterer mulighederne for hver variabel. Du kan definere test på siden <strong>Test</strong>. Ved kvalitative test skal du angive testtypen <strong>Indstilling</strong>. Brug siden <strong>Testgrupper</strong> til at tildele en testvariabel til en individuel test.</td>
<td>En produktionsvirksomhed, der fremstiller småkager, anvender en inspektionstest for det færdige produkt. Denne inspektionstest har adskillige variabler. En af variablerne er smag, og de mulige udfald for denne variabel er god og dårlig. Farve er en anden variabel, og de mulige udfald er mørk, for lys og korrekt.</td>
</tr>
<tr class="even">
<td>Udfald af testvariabel</td>
<td>Brug denne side til at konfigurere, redigere og få vist de mulige testresultater for en testvariabel, der er knyttet til en kvalitativ test. For hvert udfald angiver du status <strong>Bestået</strong> eller <strong>Mislykket</strong>. Du skal definere en variabel og dens udfald for hver kvalitative test, der er defineret på siden <strong>Test</strong>. (For kvalitative test er testtypen indstillet til <strong>Indstilling</strong> på siden <strong>Test</strong>). Brug siden <strong>Testgrupper</strong> til at tildele en testvariabel og standardudfaldet til en individuel kvalitativ test.</td>
<td>En produktionsvirksomhed, der fremstiller småkager, anvender en inspektionstest for det færdige produkt. Denne inspektionstest har adskillige variabler. En af variablerne er smag, og de mulige udfald for denne variabel er god og dårlig. Farve er en anden variabel, og de mulige udfald er mørk, for lys og korrekt. Hvert udfald får tildelt status <strong>Bestået</strong> eller <strong>Mislykket</strong>. Under inspektionstesten til hver variabel, rapporterer den person, der foretager inspektionen, testresultatet ved at vælge et af udfaldene.</td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a>Yderligere ressourcer
--------

[Processer for kvalitetsstyring](quality-management-processes.md)

[Aktivering af uoverensstemmelsesstyring](enable-nonconformance-management.md)
