---
title: "Sporing af varer og råvarer i lager, produktion og salg"
description: "Dette emne beskriver, hvordan du kan bruge varesporing til at identificere, hvor varer eller råvarer er blevet brugt, i øjeblikket bruges eller skal bruges i produktions- og salgsprocesser."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30191
ms.assetid: fdd0939a-855c-430f-a684-94f3baea1df4
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7af00d0c66f70aa41cfab0ffccef39ba4c115803
ms.openlocfilehash: 98f5696cd6a279bdf0f8d9026a74e5a9bccd2f13
ms.contentlocale: da-dk
ms.lasthandoff: 03/09/2018

---

# <a name="item-and-raw-material-tracing-in-inventory-production-and-sales"></a>Sporing af varer og råvarer i lager, produktion og salg

[!include[banner](../includes/banner.md)]


Dette emne beskriver, hvordan du kan bruge varesporing til at identificere, hvor varer eller råvarer er blevet brugt, i øjeblikket bruges eller skal bruges i produktions- og salgsprocesser.

Varesporingsfunktionalitet er tilgængelig på siden **Varesporing**. I følgende afsnit beskrives, hvordan du kan bruge varesporing, og hvilke muligheder og begrænsninger der er.

## <a name="what-is-item-tracing"></a>Hvad er varesporing?
Varesporing er et business intelligence-værktøj (BI), der synliggør kilde og destination for varer og råvarer i forsyningskæden. Fabrikanterne kan spore varer, råvarer eller ingredienser tilbage til leverandøren og fremad igennem produktionen og salget af det færdige produkt. Varesporing kan hjælpe producenter med at overholde de lovgivningsmæssige krav og også kvalitetsofficerer og produktionschefer med at analysere og skride til handling for at tage hånd om afvigelser i produkternes og materialernes kvalitet. Her nogle eksempler på de måder, producenter kan bruge varesporing:

-   Identificer mængden af en vare eller råvare, som aktuelt er på lager, og hvor den er gemt.
-   Bestem, hvor meget der er leveret af varen eller råvaren, og hvilke kunder den blev leveret til.
-   Identificer eventuelle planlagte forsendelser, som indeholder varen eller råvaren.
-   Find produktionsordrer, der bruger varen eller råvaren, og som er planlagt, i gang eller færdigmeldt.
-   Find ud af, hvor varen eller råvaren er købt.
-   Undersøg, hvor en vare eller råvare er forbrugt ved produktion af en anden vare.

## <a name="what-can-i-trace-and-are-there-any-limitations"></a>Hvad kan jeg spore, og er der nogen begrænsninger?
Du kan spore historiske lagertransaktioner for varer og råvarer, der er baseret på et varenummer og en sporingsdimensions såsom et serienummer, batchnummer eller kreditorbatchnummer. Du kan kun spore en vare eller en råvare, hvis der er tildelt sporingsdimension til den. Da sporing er baseret på lagertransaktioner, er der visse begrænsninger, når du sporer varer. Der er for eksempel begrænsninger relateret til transaktioner for projekter, anlægsaktiver og detail. Derudover vises samprodukter i sporingsdetaljerne, men biprodukter medtages ikke. Sporingen omfatter alle lagertransaktioner fra én lokalitet til en anden. Derfor kan kan brugere finde mængden af oplysninger overvældende. Sporingen vises for én juridisk enhed ad gangen. Der er ingen funktioner på tværs af firmaer i en intern sammenhæng. For hvert firma, hvor en vare modtages eller udstedes, skal du starte en ny sporing.

## <a name="what-criteria-can-i-specify-for-an-item-trace"></a>Hvilke kriterier kan jeg angive for en varesporing?
De kriterier, der er nødvendige for at spore en vare, er varenummeret, en sporingsdimension (såsom et batchnummer eller serienummer) samt retningen. I følgende tabel beskrives de kriterier, som du kan bruge til en varesporing.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Feltgruppe</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Varenummer</td>
<td>Angiv identifikatoren for den vare eller råvare, som du vil spore.</td>
</tr>
<tr class="even">
<td>Produktdimensioner</td>
<td>Valgfrit: Spor bestemte aspekter af produktdefinitionen såsom en konfiguration, størrelse, farve eller typografi.</td>
</tr>
<tr class="odd">
<td>Sporingsdimensioner</td>
<td>Angiv sporingsdimension til et batchnummer, et kreditorbatchnummer eller et serienummer. Når du bruger batchnummeret som kriterium, vises kreditorbatchnummeret, hvis du har hentet oplysningerne.</td>
</tr>
<tr class="even">
<td>Lagringsdimensioner</td>
<td>Valgfrit: Spor elementer, der er gemt på en bestemt lokalitet.</td>
</tr>
<tr class="odd">
<td>Periode</td>
<td>Valgfrit: Angiv datoer for at begrænse sporingen til en bestemt periode. Sporingsdetaljerne viser kun dokumenter og transaktioner, der er oprettet mellem disse datoer.</td>
</tr>
<tr class="even">
<td>Retning</td>
<td>Vælg retning for sporingen. Du kan spore fremad eller bagud:
<ul>
<li><strong>Baglæns</strong> – Spor downstream for at identificere kilden, den tilbageværende lagerbeholdning og produktionsordrer, der som minimum er delvist færdigmeldt.</li>
<li><strong>Fremad</strong> – Spor upstream for at identificere destinationen. Du kan finde salgsordrerne og de kunder, som den sporede vare eller råvare som minimum er delvist leveret til.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="what-information-is-included-in-the-trace-details"></a>Hvilke oplysninger er inkluderet i sporingsdetaljerne?
Resultaterne af en sporing vises i kronologisk rækkefølge i træet i oversigtspanelet **Detaljer** på siden **Varesporing**. Rækkefølgen varierer afhængigt af sporingens retning. Oplysningerne omfatter alle transaktioner fra købet af varen fra leverandøren til salg af varen til kunden. Sporingsresultater kan også indeholde mellemliggende produkter, der er relateret til varen eller den sporingsdimension, som er angivet i sporingskriterierne. Den øverste node viser vareantallet i lagerenheden, som findes i lagerbeholdningen baseret på de lagerdimensioner, der er angivet i sporingskriterierne. **Bemærk!** Sporingsdetaljerne giver et øjebliksbillede af de oplysninger, der var tilgængelige, da sporingen blev udført. Sporingsdetaljerne opdateres ikke, hvis oplysningerne ændres, efter at sporingen er udført.

## <a name="why-dont-some-nodes-contain-any-details"></a>Hvorfor indeholder visse noder ingen oplysninger?
For at reducere mængden af oplysninger i sporingsdetaljerne vises der kun detaljer for noden ved den første forekomst af varen eller råvaren. Hvis en markeret node ikke indeholder oplysninger, kan du få vist den node, der indeholder detaljer, ved at klikke på **Gå til sporet linje**. Du kan derefter vende tilbage til den node, du forlod, ved at klikke på **Gå tilbage**.

## <a name="can-i-view-only-a-particular-type-of-document-for-example-can-i-view-only-production-orders-customers-or-vendors"></a>Kan jeg kun få vist en bestemt type dokument? Kan jeg for eksempel kun vise produktionsordrer, kunder eller leverandører?
Ja, fra sporingsdetaljerne kan du åbne listesider, der kun indeholder en bestemt type dokument eller transaktion i sporingsdetaljerne. Du kan få adgang til disse sider fra menupunktet **Sporing** i handlingsruden i grupperne **Vare**, **Salg**, **Køb**, **Produktion** og **Kvalitet**. Hvis du f.eks. vil have vist en liste over leverandører i sporingsdetaljerne, skal du klikke på **Sporing** &gt; **Køb** &gt; **Leverandører**. Listesiderne opsummerer dokumenter eller transaktioner fra sporingsdetaljerne. På siderne **Ventende transaktioner**, **Ventende ordrer** og **Ikke-afsendte salgsordrer** vises der også oplysninger, der ikke er medtaget i sporingsdetaljerne. De viser desuden altid resultater fra den aktuelle dato, uanset om der er angivet et datointerval. I følgende tabel beskrives de yderligere oplysninger, som disse sider kan indeholde.

| Oversigter                    | Beskrivelse                                                                                                                                                                                                                                                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ikke-afsendte salgsordrer | Vis salgsordrelinjer, der ikke er valgt, og som derfor ikke vises i sporingsdetaljerne.                                                                                                                                                                                                                        |
| Ventende ordrer           | Vis alle ventende produktionsordrer for den sporede vare, uanset hvilke sporingsdimensioner der er brugt i sporingskriterierne. Du kan også få vist ventende produktionsordrer, hvor den sporede vare er en ingrediens, og hvor der ikke er foretaget nogen registreringer, og ingen transaktioner er færdigmeldt for ordren. |
| Ventende transaktioner     | Få vist ventende lagerposteringer for den sporede vare, herunder de angivne sporingsdimensioner eller en tom sporingsdimension. Du kan også vise ventende lagertransaktioner for varer og kombinationer af sporingsdimensioner eller en tom værdi i sporingsdetaljerne.                                                |

## <a name="how-many-levels-can-i-trace-up-or-down-in-a-bom-or-formula"></a>Hvor mange niveauer kan jeg spore opad eller nedad i en stykliste eller formel?
Du kan spore ét niveau opad eller nedad i en stykliste eller formel. Hvis du kører en sporing på råvarer, kan du for eksempel se færdigvaren og eventuelle samprodukter. Men hvis du sporer et samprodukt, er færdigvaren ikke med i sporingsdetaljerne.

## <a name="how-can-i-view-more-details-about-a-document-or-transaction-in-the-trace-details"></a>Hvordan kan jeg vise flere oplysninger om et dokument eller en transaktion i sporingsdetaljerne?
I oversigtspanelet **Detaljer** kan du vise yderligere oplysninger om et valgte dokument eller en transaktion i sporingsdetaljerne på to måder:

-   Når du markerer en node i sporingsdetaljerne i oversigtspanelet **Detaljer**, viser de andre oversigtspaneler på siden oplysninger om dokumentet eller transaktionen i noden.
-   Åbn detaljesiden for dokumentet i en markeret node ved at klikke på **Vis detaljer**. Hvis du eksempelvis markerer en node, der beskriver en produktionsordre, og du klikker på **Vis detaljer**, vises siden **Produktionsordrer**.

Nogle oversigtspaneler giver adgang til yderligere oplysninger om den valgte node. For eksempel kan du i oversigtspanelet **Uoverensstemmelser** undersøge, om der er en uoverensstemmelseshistorik, ved at klikke på **Forespørgsler**. I oversigtspanelet **Batch** kan du klikke på **Beholdningsliste** for at vise den aktuelle fysiske lagerbeholdning, samt alle lagertransaktioner, der vedrører batchen.

## <a name="can-i-run-more-than-one-trace-and-then-compare-the-details"></a>Kan jeg køre mere end én sporing og derefter sammenligne detaljerne?
Når du har kørt sporingen, kan du bruge følgende indstillinger på knappen **Spor fra node** til at køre en ny sporing på transaktionen i den valgte node:

-   **Baglæns** eller **Fremad** – Start en ny sporing for den valgte node, og overskriv detaljerne i den aktuelle sporing.
-   **Ny bagud** eller **Ny fremad** – Start en ny sporing i et nyt vindue, og behold oplysningerne om den aktuelle sporing.

Hvis du vil bruge indstillingen **Ny bagud** eller **Ny fremad**, skal du bruge funktionen **Åbn i et nyt vindue**, hvis en ny sporing skal vises i et nyt vindue.

## <a name="can-i-save-the-trace-details"></a>Kan jeg gemme sporingsdetaljerne?
Du kan gemme oplysningerne under fanen **Detaljer** som en XML-fil ved at klikke på **Eksporter** under handlingen ****Sporing**** i handlingsruden. Ud over sporingsdetaljerne indeholder XML-filen sporingskriterierne, den overordnede node og den disponible beholdning. Muligheden for at gemme oplysningerne om en sporing, for eksempel hvis du vil vedhæfte oplysningerne på en kvalitetsordre eller anden dokumentation for overholdelse. Du kan angive, hvor filen er gemt. Vælg indstillingen **Vis dokument** for at få vist filen med det samme. **Bemærk!** Filen gemmes altid – selv hvis du kun vil vise den. Som standard åbnes XML-filen i et browservindue. Du kan dog højreklikke på filen, vælge **Åbn med** og derefter vælge det program, du vil bruge til at få vist indholdet.

## <a name="can-i-calculate-a-balance-for-a-particular-item-or-ingredient"></a>Kan jeg beregne en saldo for en bestemt vare eller ingrediens?
Du kan eksportere oplysninger fra oversigtssiderne til Microsoft Excel. Åbn den relevante side, klik på ikonet **Åbn i Microsoft Office**, og vælg derefter **Eksporter til Microsoft Excel**. Denne funktionalitet er især nyttig, når du vil beregne en massebalance for en vare eller en ingrediens i oversigtssiden **Transaktioner**. På oversigtssiden **Transaktioner** kan du filtrere på varen eller ingrediensen samt evt. batchen og derefter eksportere oplysningerne til Excel. I Excel kan du for eksempel isolere den disponible mængde, den solgte mængde og den mængde, der blev brugt i produktionen.

## <a name="can-i-investigate-whether-there-is-a-history-of-issues-with-items-or-raw-materials"></a>Kan jeg undersøge, om der findes en oversigt over problemer med varer eller råvarer?
Sporingsdetaljerne indeholder oplysninger om kvalitetsordrer og manglende overensstemmelse, der vedrører varen eller råvaren. For at få vist en oversigt over kvalitetsordrer og uoverensstemmelser skal du klikke på **Kvalitetsordrer** eller **Uoverensstemmelser** i handlingsruden. **Bemærk!** Destruktive kvalitetsordrer kan forekomme mere end én gang i sporingsdetaljerne. Når der oprettes en destruktiv kvalitetsordre for et dokument såsom en købsordre, vises den i hver transaktion for det pågældende dokument.

## <a name="are-there-any-reporting-capabilities-that-are-related-to-item-tracing"></a>Er der nogen rapporteringsfunktioner med relation til varesporing?
Du kan generere rapporten **Afsendt til kunder** for at identificere mængden af den leverede vare eller råvare og de kunder, som den blev leveret til. Ved en forespørgsel, der er relateret til overholdelse, kan du generere rapporten for alle kunder. Ved en forespørgsel, der er relateret til kundeservice, kan du generere rapporten for en valgt kunde. Hvis produktet er en råvare, der blev brugt til fremstilling af en færdigvare, medtages færdigvaren også. **Bemærk!** Hvis du bruger funktionerne til at slette eller arkivere salgsordrer, indeholder rapportresultaterne også alle salgsordrer, der er blevet slettet eller arkiveret.

## <a name="can-i-trace-coproducts-and-byproducts"></a>Kan jeg spore samprodukter og biprodukter?
Du kan spore samprodukter, men du kan ikke spore et biprodukt, da der typisk ikke tildeles sporingsdimensioner til biprodukter. Når du sporer en vare, omfatter sporingsdetaljerne alle relaterede samprodukter. En node, der indeholder et samprodukt, har ordet "samprodukter" med i detaljerne. Du kan også få vist detaljer om et samprodukt ved at vælge noden i sporingsdetaljerne og derefter klikke på oversigtspanelet **Produktion**.

