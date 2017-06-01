---
title: "Nyheder eller ændringer i Dynamics AX 7.0 (februar 2016)"
description: "Denne artikel beskriver funktioner, der er nye eller ændrede i Microsoft Dynamics AX 7.0. Denne version indeholder både platformen og programfunktioner og blev udgivet i februar 2016."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 91243
ms.assetid: 515bc6e7-a85d-4995-95c6-6cab6c8aa0f9
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: aba59096bf1ffc9ce6448cb7c0f9bd5d2936d7d7
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="whats-new-or-changed-in-dynamics-ax-70-february-2016"></a>Nyheder eller ændringer i Dynamics AX 7.0 (februar 2016)

[!include[banner](../includes/banner.md)]


Denne artikel beskriver funktioner, der er nye eller ændrede i Microsoft Dynamics AX 7.0. Denne version indeholder både platformen og programfunktioner og blev udgivet i februar 2016.

<a name="cost-management"></a>Omkostningsstyring
---------------

<table>

<tbody>
<tr class="odd">
<td><strong>Hvad kan du gøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er det vigtigt?</strong></td>
</tr>
<tr class="even">
<td>Få et hurtigt overblik over lagersaldoen, lagersaldoen for den igangværende forarbejdning (IGVF), og hvad lagertilgangen og -afgangen har været i det valgte regnskabsår.</td>
<td>Ikke tilgængelig</td>
<td><strong>Omkostningsstyring</strong> arbejdsområdet indeholder et afsnit, hvor lageropgørelsen eller IGVF-lageropgørelsen præsenteres for den valgte regnskabsperiode. Opgørelsen er baseret på en cache med datasæt, der som standard opdateres hvert døgn. Cachen med datasæt kan konfigureres, så brugere kan opdatere den manuelt for rapportering i realtid. <strong>Kortet for dataopdateringsstatus</strong> i arbejdsområdet  <strong>Omkostningsstyring</strong> viser, hvornår cachen sidst blev opdateret.</td>
<td>Omkostningscontrollere er interesseret i at vide, om lager- eller IGVF-lagersaldoen øges eller mindskes over tid. Ved at klassificere operationelle hændelser i opgørelsen, kan omkostningscontrolleren få et overblik over, hvordan lageret flyder. Hvis lageret eller IGVF-lageret vurderes af standardomkostninger, kan der også ses den samlede afvigelse, der er registreret.</td>
</tr>
<tr class="odd">
<td>Brug af modulet <strong>Omkostningsstyring</strong>.</td>
<td>Ikke tilgængelig</td>
<td>Omkostningsstyring er indført som et domæneområde. Omkostningsrelaterede konfiguration og indsigt er spredt ud over Lagerstyring, Produktionsstyring og Kreditor.</td>
<td>Da alle de opgaver, der vedrører omkostningsstyring er samlet i ét modul, vil det være lettere for omkostningscontrollere at vedligeholde systemet.</td>
</tr>
<tr class="even">
<td>De bogføringstyper, der er relateret til bogføring af lager og produktionsregnskab, er blevet opdateret.</td>
<td>Etiketterne i formularerne <strong>InventPosting</strong>, <strong>Ressource</strong>, <strong>ResourceGroup</strong> og <strong>ProductionGroup</strong> justeres ikke altid med de <strong>LedgerPostingType</strong>-etiketter, der faktisk bruges. Det er ikke let at forstå den terminologi, der bruges i etiketterne.</td>
<td>Etiketterne er opdateret, så etiketterne på siderne <strong>InventPosting</strong>, <strong>Ressource</strong>, <strong>ResourceGroup</strong> og <strong>ProductionGroup</strong> stemmer overens med <strong>LedgerPostingType</strong>-etiketterne. Alle etiketterne er også blevet omdøbt, så etiketterne stemmer overens med de operationelle hændelser. Bemærk, at den faktiske bogføringslogik ikke er ændret.</td>
<td>Det er lettere at konfigurere systemet, fordi de nye etiketter er relateret til de operationelle hændelser, der bruger denne posteringstype.</td>
</tr>
<tr class="odd">
<td>Importere/eksportere købs-, kost- eller salgsprisen fra Microsoft Excel til eller fra en efterkalkulationsversion.</td>
<td>Du kan ikke importere priser eller omkostninger korrekt til en efterkalkulationsversion, fordi datamodellen kræver et InventDim-id.</td>
<td>Indførelsen af dataenheder gør det muligt at implementere en funktion til import og eksport. Denne funktion giver brugerne mulighed for at importere eller eksportere priser eller omkostninger i en efterkalkulationsversion.
<ul>
<li>Importer en komplet liste over næste år købspriser, der fås i indkøbsafdelingen.</li>
<li>Skub omkostninger og standardsalgspriser fra hovedkontorer til et eller flere salgsfirmaer på én gang.</li>
</ul></td>
<td>Det kan spare omkostningscontrollere en betydelig mængde tid, når de vedligeholder systemet, især når de skal vedligeholde forudbestemte omkostninger for det næste regnskabsår.</td>
</tr>
<tr class="even">
<td>Få et hurtigt overblik over lagersaldoen og gennemsnitlige enhedsomkostning for et omkostningsobjekt.</td>
<td>Brugeren skal åbne beholdningsformularen og vælge de lagerdimensioner, der afspejler omkostningsobjektet. Derfor skal brugeren vide, hvilke lagerdimensioner der var markeret til økonomisk lager for det specifikke produkt.</td>
<td>En ny <strong>Omkostningsobjekt</strong>-side er blevet indført. Denne side viser som standard alle omkostningsobjekter, der er relateret til produktet. Siden viser det aktuelle lagerantal, værdi og gennemsnitlig enhedskostpris pr. omkostningsobjekt.</td>
<td>Det fjerner noget af kompleksiteten og gør det lettere at være omkostninscontroller.</td>
</tr>
<tr class="odd">
<td>Brug den nye side <strong>Omkostningsposter</strong> under lagerstyring.</td>
<td>Det kan være kompliceret at udføre lagerstyring af registrerede lagerposteringer og relaterede udligninger, da de samme transaktioner kan være fysiske eller økonomiske.</td>
<td>Siden <strong>Omkostningsposter</strong> giver en ny måde at få vist lagertransaktioner.
<ul>
<li>Posteringer vises i kronologisk rækkefølge.</li>
<li>Kun posteringer, der bidrager til omkostninger, medtages.</li>
<li>Der er igen skelnen mellem fysiske eller økonomiske omkostninger.</li>
<li>Der er igen skelnen mellem fysisk eller økonomisk antal.</li>
<li>Omkostningerne tilføjes trinvist.</li>
</ul></td>
<td>Det kan spare omkostningscontrollere en betydelig mængde tid, når de skal udføre lagerstyring på posteringsniveau.</td>
</tr>
<tr class="even">
<td>Bruge den nye <strong>Produktionsopgørelse IGVF</strong>-dialogboks til at få vist en opsummeret oversigt over akkumulerede omkostninger for et bestemt produkt.</td>
<td>Ikke tilgængelig</td>
<td>IGVF-opgørelsen viser en opsummeret IGVF-saldo for den specifikke produktionsordre grupperet i relevante omkostningsklassifikationer. Et diagram viser i kronologisk rækkefølge, hvordan operationelle bogføringer har påvirket IGVA-saldoen.</td>
<td>Det kan spare omkostningscontrollere en betydelig mængde tid, når de har brug for at vide, hvad den aktuelle IGVA-saldo er på en bestemt produktionsordre, eller hvor meget materiale der er brugt på ordren.</td>
</tr>
<tr class="odd">
<td>Bruge funktionen Vis omkostningssammenligning, der er indført på produktionsordrer. Funktionen gør det nemmere at sammenligne omkostninger, der er relateret til en produktionsordre.</td>
<td>Brugeren kan kun sammenligne forkalkulerede omkostninger og faktiske omkostninger. Sammenligningen kan foretages på det laveste niveau.</td>
<td>Med funktionen til omkostningssammenligning kan omkostningscontrollere sammenligne følgende data:
<ul>
<li>Aktive omkostninger i forhold til forkalkulerede omkostninger = Afvigelse i planlægning</li>
<li>Forkalkulerede omkostninger i forhold til realiserede omkostninger = Produktionsafvigelse</li>
<li>Afvigelse i planlægning + produktionsafvigelse = Samlet afvigelse</li>
</ul>
Denne funktion fungerer uafhængigt af andre efterkalkulationsmetoder, der er knyttet til den producerede vare. Som standard viser et diagram omkostningssammenligningen efter kostprisgruppetype. Med diagrammet kan brugere dykke ned i mere detaljerede niveauer.</td>
<td>Omkostningscontrollere eller produktionschefer kan bruge det til at analysere, hvor produktionsafvigelser kommer fra, og hvad er årsagen.</td>
</tr>
</tbody>
</table>

## <a name="developer"></a>Udvikler
|                                                                                                              |                                                                                                                                                                                                    |                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hvad kan du gøre?**                                                                                         | **Dynamics AX 2012**                                                                                                                                                                               | **Dynamics AX 7.0**                                                                                                                                                                                                            | **Hvorfor er det vigtigt?**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Oprette webbaserede løsninger i skyen, der er tilgængelige på mange enheder.                                 | Ikke ledig                                                                                                                                                                                      | Den aktuelle version af Dynamics AX er baseret på en ny web-baseret klient, og klientstruktur.                                                                                                                                    | Du kan angive fremtidens løsninger til slutbrugerne.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Du kan bruge Microsoft Visual Studio til udvikling af dine løsninger.                                                       | Microsoft MorphX er det vigtigste udviklingsmiljø, men noget af udviklingen sker i Visual Studio.                                                                                                | Visual Studio er det eneste udviklingsmiljø.                                                                                                                                                                             | Det indeholder velkendte Dynamics AX 2012 begreber og tilpasser dem problemfrit til Visual Studio framework og paradigmer. Det giver mulighed for standardinteroperabilitet med andre .NET sprog og projekter.                                                                                                                                                                                                                                                                                                                                                                                                   |
| Kompilere CIL-sprog (Common Intermediate Language) for alle funktioner.                                                 | X ++ kompileres til p-kode.                                                                                                                                                                         | Den helt nye X ++-compiler opretter CIL for alle funktioner. CIL er det samme mellemliggende sprog, der bruges af andre. NET-baserede sprog.                                                                                   | CIL er hurtigere, kan effektivt henvise til klasser i administrerede DLL'er (dynamic link libraries) og kan køre på en stor værktøjsbase med .NET hjælpeprogrammer.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Integrere BI-rapporter (Business Intelligence) og visualiseringer i Microsoft Dynamics AX-klienten.             | Ikke ledig                                                                                                                                                                                      | Oprette meget intuitive og flydende visualiseringer.                                                                                                                                                                              | Det giver indsigt, der er baseret på BI, til beslutningstagning.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Integrere med Microsoft Office.                                                                             | Ikke ledig                                                                                                                                                                                      | Nye funktioner omfatter Excel Data Connector-appen, **Projektmappedesigner**-siden, eksport af API og dokumentstyring.                                                                                                        | Du kan oprette produktivitetsløsninger for dine slutbrugere.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Automatisere build, test og implementer.                                                                            | Delvis ledig                                                                                                                                                                                | Installere udviklertopologi ved hjælp af udvikler og build VM. Konfigurer automatisk build VM for at opdage, bygge moduler fra Visual Studio Online (VSO) og køre test. C\# og X ++ modulkompilering og -referencer understøttes. | Det øger udviklernes produktivitet ved at reducere omkostninger og besvær til test og validering.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Tilpasse med overlejring og udvidelser.                                                                  | Udvidelser er ikke tilgængelige.                                                                                                                                                                       | Den aktuelle version af Dynamics AX har en ny model for tilpasning.                                                                                                                                                              | Du kan tilpasse kildekode og metadata af modelelementer, der leveres af Microsoft eller en tredjepart Microsoft-partnere.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Opbygge nye objekter og elementer til brugergrænsefladen ved hjælp af X ++ og en moderne webstruktur.                                  | Brugerdefinerede kontrolelementer er afhængige af eksterne strukturer såsom Microsoft ActiveX og WPF (Windows Presentation Foundation).                                                                                   | Det er lettere at opbygge objekter i den aktuelle version. X ++ framework kan bruges til programfunktioner og forretningslogik, og en HTML/JavaScript-baseret klient giver mulighed for moderne visuelle effekter.                         | Dine kontrolelementer kan designes til at se ud og fungere ligesom Dynamics AX OOB-kontrolelementer (out-of-box).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Evaluere og justere ydeevnen ved hjælp af nye værktøjer.                                                            | PerfSDK, værktøjspakken til dataudvidelse, sporingsparser WEb-app og PerfTimer er ikke tilgængelige.                                                                                                             | PerfSDK, værktøjspakken til dataudvidelse, sporingsparser Web-app og PerfTimer er nye.                                                                                                                                                  | Software Development Kit (SDK) lader dig teste og validere alle vigtige forretningsprocesser for ydeevne i en enkelt-bruger, og hvis det er relevant, flerbruger-testkørsel. Med værktøjspakke til dataudvidelse kan du udvide alle performance-test, der skal have masterdata og transaktionsdata udvidet korrekt. Med sporingsparseren kan du validere en enkeltbruger-performancetest eller en flerbrugerekørsel. PerfTimer gør det muligt at se, om en forespørgsel eller et bestemt metodekald forårsager problemer med ydeevnen. Derfor kan behøver du ikke at foretage en sporing og analysere alt i detaljer. |
| Fremvise opdaterbar visning ved hjælp af OData.                                                                        | Ikke ledig                                                                                                                                                                                      | Den aktuelle version af Dynamics AX introducerer et offentligt OData-tjenesteslutpunkt, som giver adgang til Dynamics AX-data på en ensartet måde på tværs af et bredt udvalg af klienter.                                                     | Dine løsninger kan interagere med RESTful-tjenester, dele data på en overskuelig måde og aktivere bred integration ved hjælp af HTTP-stakprotokollen.                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Udnytte Business Connector til at oprette forretningsregler og understøtte integrationsmuligheder.         | Business Connector er tilgængelig til at foretage kald til X ++-kode fra administreret kode. Vi anbefaler, at du kun bruger Business Connector til at oprette forretningsregler i C\# og ikke til integrationsscenarier. | Business connector understøttes ikke længere. Oprettelseskravet dækkes af det faktum, at X ++ kompileres til en administreret kode. Derfor er interop lettere. Integrationsmulighederne opfyldes ved hjælp af OData.       | Du kan ikke bruge business connector fremover.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Vælg skala (det vil sige antallet af decimaler) i faktiske databasefelter og udvidede datatyper (EDT'er). | Skala 16 er standardskalaen og kan ikke ændres af udvikleren.                                                                                                                               | EDT'er og felterne har nu en skalaegenskab, der kan anvendes på de enkelte felter og EDT. Standard er sat til 6, ikke 16.                                                                                                | Ydeevne med NCCI tabeller (understøttelse i hukommelse i SQL) er hurtigere ved ordrer af en vis størrelsesorden, når der anvendes en mindre skala. Rediger skalaen som din brug af de enkelte felter kræver.                                                                                                                                                                                                                                                                                                                                                                                                               |
## <a name="financial-management"></a>Økonomistyring
<table>






<tbody>
<tr class="odd">
<td><strong>Hvad kan du gøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er det vigtigt?</strong></td>
</tr>
<tr class="even">
<td>Eksportere kontostrukturer til Microsoft Excel.</td>
<td>Ikke ledig</td>
<td>Du kan nu vælge en kontostruktur og eksportere den til Excel.</td>
<td>Mange kunder har anmodet om muligheden for at eksportere kontostrukturer til Excel for lettere filtrering.</td>
</tr>
<tr class="odd">
<td>Få vist finanskonti og avancerede regelstrukturer, der er knyttet til en kontostruktur på en enkelt side.</td>
<td> Brugeren skal navigere til flere formularer for at se Finans og kontostrukturen, der bruges. </td>
<td>Faktabokse er føjet til kontostruktursiden.</td>
<td>Det er lettere at få adgang til vigtige oplysninger, når kontostrukturer er defineret og redigeret.</td>
</tr>
<tr class="even">
<td>Få vist de finanskonti, der er knyttet til en kontoplan på en enkelt side.</td>
<td>Brugeren skal navigere til hvert firma og åbne finansformularen for at få vist den kontoplan, der er tildelt finanskontoen.</td>
<td>Faktabokse er føjet til siden **Kontoplan**.</td>
<td> Det er lettere at få adgang til vigtige oplysninger, når en kontoplan er defineret og redigeret.</td>
</tr>
<tr class="odd">
<td>Få vist reguleringer af afslutningsark og ultimoposter i separate kolonner på **Råbalance** listesiden. </td>
<td>Brugeren ser begge typer transaktioner i en enkelt kolonne.</td>
<td>En ekstra parameter er føjet til **Råbalance** listesiden.</td>
<td>Det giver mulighed for mere præcis analyse af data og er også nødvendig ved regulerende rapportering i nogle lande. </td>
</tr>
<tr class="even">
<td>Bruge den nye **Global finanskladde** side.</td>
<td>Ikke ledig </td>
<td>Ny **Global finanskladde** side til angivelse af finanskladder. Rettigheder til denne side føjes til rollen **Bogholder**.</td>
<td>Gør det muligt for en bogholder tilknyttet en delt tjeneste at angive finanskladder på tværs af regnskaber uden at forlade formularen eller skifte regnskabskontekst.</td>
</tr> 
<tr class="odd">
<td>Bruge den nye **Sporing af regnskabskilde**side.</td>
<td>Tilgængelig fra Dynamics AX 2012 R3 CU10.</td>
<td>Ny **Sporing af regnskabskilde** side og handlinger til at gå dertil fra **Råbalance** listesiden og **Bilagstransaktioner** siden.</td>
<td>Gør det muligt se de mest detaljerede oplysninger om kilden til en råbalance eller en regnskabspost i Finans eller til ad hoc-analyse.</td>
</tr>
<tr class="even">
<td>Tilføje flere posteringslag.</td>
<td>Tilføjelse af flere posteringslag var en udvikleroplevelse.</td>
<td>Ti posteringslag er nu tilgængelige.</td>
<td>De fleste kunder tilføjer flere posteringslag.</td>
</tr>
<tr class="odd">
<td>Bruge indstillingen Relaterede bilag.</td>
<td>Ikke ledig</td>
<td>Indstillingen Relaterede bilag er tilgængelig, så brugerne kan se bilag i modposteringsfirmaet, når de bogfører interne transaktioner. Fra de relaterede bilag kan brugerne klikke på detaljer og hurtigt hoppe til bilaget i modposteringsregnskabet.</td>
<td>Når brugerne bogførte interne transaktioner, kunne de ikke se eller spore bilaget, der var bogført i modposteringsregnskabet.</td>
</tr>
<tr class="even">
<td>Masseafslutning på regnskabsperiode</td>
<td>Ikke ledig</td>
<td>Brugerne kan opdatere moduladgangen og ændre periodestatus for flere virksomheder ad gangen.</td>
<td>Brugere måtte før denne funktion ændre, hvilken virksomhed de var logget på, gå til finanskalenderformularen og manuelt opdatere moduladgangen og status for perioden.</td>
</tr>
<tr class="odd">
<td>Få valutakurser, der er styret af Oanda.</td>
<td>Konfigurere valutakursudbyderen til at importere satser fra Oanda var for udviklere. </td>
<td>Hvis brugerne har en nøgle til Oanda, kan de indtaste den, når de konfigurerer valutakursudbyderen.</td>
<td>Brugerne kan drage fordel af den avancerede funktionalitet ved at få valutakurser importeret via Oanda i henhold til en plan.</td>
</tr>
<tr class="even">
<td>Filtrere finansielle rapporter (Management Reporter) baseret på dimensioner, attributter, datoer og scenarier. </td>
<td> Alle filtrering af Management Reporter-rapporter håndteres gennem udformningen af rapporten. Hvis en bruger, der har visningsrettigheder, f.eks. ønsker at få vist en rapport for en anden dato, skal en rapportdesigner foretage ændringen. </td>
<td>Rapportindstillinger er blevet tilføjet, så forskellige filtre kan anvendes, når en bruger får vist en rapport. Der genereres derefter en ny rapport baseret på disse filtre.</td>
<td>Forbrugere af finansielle rapporter kan anvende forskellige filtre for dimensioner, datoer, attributter og scenarier uden opdateringer af rapportdesign.</td>
</tr>
<tr class="odd">
<td>Få vist finansielle rapporter (Management Reporter) i Microsoft Dynamics AX-klienten.</td>
<td>En separat webklient blev brugt til at få vist Management Reporter-rapporter.</td>
<td>Der er adgang til alle finansielle rapporter i Dynamics AX-klienten. Brugeren vælger en rapport, der skal vises, og rapporten åbnes i klienten.</td>
<td>Du kan nu få vist finansrapporter uden at skulle åbne en anden klient/et andet program.</td>
</tr>
<tr class="even">
<td>Udskrive finansrapporter (Management Reporter) fra Microsoft Dynamics AX-klienten.</td>
<td>Ved udskrivning af en rapport bruges browserens udskriftsindstillinger, og kun det, brugeren kan se på skærmen, udskrives. </td>
<td>Brugeren kan vælge detaljeniveau og sideopsætning for en rapport ved hjælp af indstillingen Udskriv i den finansielle rapport i Dynamics AX-klienten.</td>
<td>Rapporter udskrives på den måde, brugerne forventer, i stedet for at udskrive en webside.</td>
</tr><tr class="odd">
<td>Analyser økonomiske data ved hjælp af Power BI-indholdet "Overvågning af økonomisk performance".</td>
<td>Ikke tilgængelig</td>
<td>Vælg på PowerBI.com **Hent data**, og vælg derefter indholdspakken **Dynamics AX – økonomisk performance**. Angiv URL-adressen til dit Dynamics AX slutpunkt for at se dine data afspejlet i dashboardet.</td>
<td>Med tre eller fire klik kan organisationer installere et Power BI-dashboard, som indeholder vigtige finansielle data. Indholdet kan tilpasses af organisationen.</td>
</tr>
<tr class="even">
<td>Spore processer for afslutning af regnskabsperiode.</td>
<td>Ikke ledig </td>
<td>Afslutningsskabeloner og -tidsplaner kan oprettes ved hjælp af Afslutning på regnskabsperiode-konfigurationen. Brug **Afslutning på regnskabsperiode**-arbejdsområdet til at spore status for afslutning af tidsplaner på tværs af flere firmaer.</td>
<td>Dette arbejdsområde fjerner manuelle systemer til at definere, planlægge og kommunikere afslutningsaktiviteter. Derfor reduceres antallet af dage inden afslutning.</td>
</tr>
<tr class="odd">
<td>Overvåge budgettet kontra faktiske oplysninger og oprette budgetter i Finans ved hjælp af arbejdsområdet **Finansbudgetter og budgetter** og yderligere forespørgselsformularer.</td>
<td>Ikke ledig</td>
<td> Arbejdsområdet kan åbnes ved hjælp af Dynamics AX-dashboard. Det indeholder links til flere nye forespørgselssider: **Faktisk vs. budgetoversigt**, **Statistik for budgetstyringsoversigt**, **Budgetregisterposter** og **Budgetplaner**.</td>
<td>Ny forespørgselssider giver nem adgang til budgetoplysninger. Arbejdsområdet kombinerer alle budgetvedligeholdelses- og overvågningsopgaver på ét sted, der er let for budgetadministratorer eller regnskabschefer at bruge.</td>
</tr>
<tr class="even">
<td>Oprette layout for budgetplaner og budgetter.</td>
<td>Dokumentet **Budgetplan** vises som en liste over de linjer, der har ikrafttrædelsesdatoer og beløb for kombinationer af økonomiske dimensioner. Brugeren skal oprette og bruge Excel-skabeloner til at få vist budgetplandata i en pivottabel.</td>
<td>Der findes et ubegrænset antal layouts til budgetplaner og budgetter. Du kan kombinere valgte økonomiske dimensioner, brugerdefinerede kolonner og andre rækkeattributter (f.eks. kommentarer, projekter og aktiver) i layoutet. Brugerne kan skifte layout for budgetplandokumentet løbende og redigere data ved hjælp af det valgte layout. Konfiguration af budgetplanlægning forenkles ved at fjerne begrænsninger i scenariet og bruge layout til at definere, hvilke data der kan ses og redigeres i hver fase af budgetplandokumentet.</td>
<td>Det giver fleksibilitet til at oprette og redigere budgetplaner ved hjælp af både Excel og Dynamics AX-klienten. Skabeloner til Excel-projektmapper kan genereres ved hjælp af opsætningen af layoutet for Budgetplan.</td>
</tr>
<tr class="odd">
<td>Udskriv rapporten **Kreditorfakturaposteringer** ved hjælp af oplysninger fra rapporten **Detaljeret forfaldsliste**, som indeholder dagene efter forfald. </td>
<td>Du skal udskrive to forskellige rapporter: **Detaljeret forfaldsliste** og **Kreditorfakturaposteringer**.</td>
<td>Oplysninger om de to rapporter er konsolideret i rapporten **Kreditorfakturaposteringer**. Rapporten **Detaljeret forfaldsliste** er forældet. </td>
<td>Det fjerner behovet for at udskrive to forskellige, men relaterede rapporter.</td>
</tr>
<tr class="even">
<td>Generere lovpligtige rapporter direkte i PDF-format.</td>
<td>Du skal først oprette en regulerende rapport i ét format og derefter eksportere det til PDF-format.</td>
<td>PDF-formatet er standardformatet for lovpligtige rapporter.</td>
<td>Det giver en ensartet skærmoplevelse på computerskærmen og en udskrevet kopi.</td>
</tr>
<tr class="odd">
<td>Køre momsafregningsprocessen som en batchproces. </td>
<td>Ikke ledig</td>
<td>På siden **Momsafregningsperiode** kan du angive, at afregningsprocessen skal køres i batchtilstand.</td>
<td>For perioder, der har mange momstransaktioner, kan afregningsprocessen være tidskrævende, og det kan være bedre at køre processen i baggrunden som en batchproces.</td>
</tr>
</tbody>
</table>





## <a name="foundation"></a>Fond
<table>






<tbody>
<tr class="odd">
<td><strong>Hvad kan du gøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er det vigtigt?</strong></td>
</tr>
<tr class="even">
<td>Få adgang til klienten uanset tid og sted. </td>
<td>AX 2012 klienten til stationære computere giver et komplet sæt af formularer, men den kan køres kun på computere, der kører Microsoft Windows, og kræver installation. Terminal Server bruges ofte med klienten til stationære computere til at give adgang via et WAN-netværk (Wide Area Network). Enterprise Portal-webklienten giver et reduceret sæt af formularer.</td>
<td>De to AX 2012-klienter er blevet erstattet af en enkelt, standardbaserede webklient, der leverer den fulde funktionalitet fra klienten til stationære computere og Enterprise Portal-klientens rækkevidde.</td>
<td>Udviklingsarbejde forhindres i at blive delt mellem to brugergrænsefladeplatforme. Ved at bruge standardwebgrænseflader elimineres behovet for Terminal Server.</td>
</tr>
<tr class="odd">
<td>Være produktiv ved hjælp af den nye Arbejdsrutineoptager.</td>
<td>AX 2012 Arbejdsrutineoptager kræver direkte adgang til en computer med Applikationsobjektserver (AOS) og øgede rettigheder og leverer ingen redigeringsindstillinger.</td>
<td>Den nye Arbejdsrutineoptager kan bruges direkte fra webklienten. Adgang til Arbejdsrutineoptager kræver ikke administratorrettigheder. Indspillede trin kan ses live, når du optager, nye redigeringsindstillinger er blevet introduceret, og Arbejdsrutineoptager understøtter flere eksempler ud over eksisterende Forretningsprocesmodel-scenarier (BPM).</td>
<td>Den nye Arbejdsrutineoptager giver en strømlinet oplevelse og nye muligheder i Dynamics AX. Nogle af disse muligheder er tilgængelige nu og flere følger i fremtiden.</td>
</tr>
<tr class="even">
<td>Hjælpe brugere med bedre at forstå deres kommende arbejde ved hjælp af arbejdsområder.</td>
<td>Rollebaserede områder indeholder en oversigt over oplysninger, der vedrører en brugers jobfunktion i virksomheden eller organisationen.</td>
<td>Arbejdsområder er et nyt koncept i Dynamics AX og er beregnet til at erstatte rollebaserede områder som den primære metode til at navigere til opgaver og bestemte sider. De giver oversigt på en enkelt side over en forretningsaktivitet og hjælper brugerne med at forstå den aktuelle status, den kommende arbejdsbyrde og processens eller brugers performance. Arbejdsområder er mere detaljerede end AX 2012 rollebaserede områder, og en bruger kan have adgang til flere arbejdsområder.</td>
<td>Arbejdsområder er beregnet til at øge brugernes produktivitet. Udviklere skal oprette et arbejdsområde for alle væsentlige "aktiviteter", der understøttes i produktet. Et ældre rollebaseret område fra AX 2012 erstattes typisk med flere arbejdsområder i den aktuelle version af Dynamics AX.</td>
</tr>
<tr class="odd">
<td>Få formularer til at tilpasse sig browserbilledet eller enhedens størrelse.</td>
<td>I AX 2012 er der et fast layout af formularindhold i form af kolonner, og den overordnede højde/bredde af formularen bestemmes i vid udstrækning af kontrolelementerne i formularen.</td>
<td>Med skiftet til internettet i den seneste Dynamics AX er dimensionerne for en formular nu baseret på browserbilledets størrelse eller enheden. Kontrolelementer og layoutparametre er blevet ændret eller tilføjet, så de bedre reagerer på ændringer af billedstørrelsen.</td>
<td>Formularens indhold skal være mere responsivt for at optimalt at kunne udnytte den tilgængelige højde/bredde af browseren eller enheden. Det kan kræve ændringer i den måde, en formular er udformet på, at få den til at respondere.</td>
</tr>
<tr class="even">
<td>Bruge mønstre til en forbedret formularudviklingsoplevelse.</td>
<td>Formularskabeloner var tilgængelig som udgangspunkt for formularudvikling i AX 2012 baseret på et formularformat. Funktionen til kontrol af formularformatet (Form Style Checker), et valgfrit tilføjelsesprogram, giver oplysninger om, hvordan en formular afveg fra den tilsvarende skabelon.</td>
<td>I den aktuelle version af Dynamics AX er der indført formularmønstre. Formularmønstre repræsenterer en kombination af formularskabeloner og Form Style Checker er integreret tæt i udviklingsoplevelsen. Mønstre er defineret på formularniveau (som i AX 2012) med flere undermønstre, der er nu tilgængelige på gruppe- og fanesideniveau.</td>
<td>Formularer, der overholder mønstre, har mange fordele, herunder en mere ensartet brugergrænseflade, en enklere udviklingsproces, lettere formularopgraderingssti og bedre responsivitet af formularlayout.</td>
</tr>
</tbody>
</table>

## <a name="help"></a>Hjælp
<table>






<tbody>
<tr class="odd">
<td><strong>Hvad kan du gøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er det vigtigt?</strong></td>
</tr>
<tr class="even">
<td>Få adgang til automatiseret hjælp (opgaveguider) og emner ved at klikke på **Hjælp**.</td>
<td>Hjælpesystemet i AX 2012 leder til HTML-emner, der er gemt på en lokal webserver. Kunder og partnere kan oprette deres egen Hjælp.</td>
<td>Hjælp-systemet i den aktuelle version af Dynamics AX viser opgaveguider, der er gemt i BPM til Microsoft Dynamics Lifecycle Services (LCS). Hjælp-systemet viser også emner fra webstedet Microsoft Docs. Yderligere oplysninger finder du i afsnittet [Dynamics AX Hjælp - Introduktion](help-overview.md) og [Nye opgaveguider er tilgængelige (februar 2016)](new-task-guides-available-february-2016.md).</td>
<td>Opgaveguider indeholder en automatiseret, interaktive oplevelse, der fører dig gennem trinene i en opgave eller forretningsproces. Du kan downloade og tilpasse opgavehjælpelinjer, som Microsoft leverer. Emnet giver en hurtigere og mere fleksibel måde at oprette, levere og opdatere produktdokumentationen. Derfor hjælper den med at sikre, at du har adgang til de seneste tekniske oplysninger.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Styring af menneskelig kapital
<table>






<tbody>
<tr class="odd">
<td><strong>Hvad kan du gøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er det vigtigt?</strong></td>
</tr>
<tr class="even">
<td>Overfør færdigheder og certifikater til kursusdeltagerne ved kursets afslutning.</td>
<td>Dette er en manuel proces.</td>
<td>Når et kursus er gennemført, vises en ny indstilling til opdatering af en deltagers poster med nye kompetencer og certifikater.</td>
<td>Det giver en ny og effektiv måde til vedligeholdelse af medarbejderposter.</td>
</tr>
<tr class="odd">
<td>Hurtigt kontrollere ansættelse.</td>
<td>Dette er en manuel proces.</td>
<td>HR-afdelingen kan hurtigt kontrollere beskæftigelse ved hjælp af et arbejdsområde eller medarbejdersiden.</td>
<td>HR-afdelingen har ikke længere adgang til flere sider for at kontrollere startdatoen, chefen, måneder i stillingen og kompensationsdata.</td>
</tr>
<tr class="even">
<td>Lade medarbejdere se, opdatere og slette oplysninger i systemet.</td>
<td>Tilgængelig, men med begrænsede funktioner til visning og opdatering.</td>
<td>Denne funktion er aktiveret, og gør det muligt for medarbejdere og kontrahenter at se en bred vifte af personlige data. Der kan eventuelt bruges en arbejdsgang, når oplysningerne oprettes, opdateres eller slettes.</td>
<td>Medarbejderne kan tage kontrol med deres oplysninger, uanset om det omfatter opdatering af adresse eller kontaktoplysninger, ansøgning om et job, udfyldning af et spørgeskema eller opdatering af deres billede. Når en arbejdsgang er aktiveret, kan oplysningerne blive gennemset af en godkender eller automatisk godkendes, afhængigt af dine forretningsprocesser.</td>
</tr>
<tr class="odd">
<td>Lade chefer se eller redigere medarbejderoplysninger.</td>
<td>Tilgængelig, men med begrænsede funktioner til visning og opdatering.</td>
<td>Ledere kan se eller redigere medarbejderoplysninger afhængigt af konfigurationsindstillinger og sikkerhed.</td>
<td>Ledere kan få adgang til vigtige medarbejderdata, så de kan træffe bedre beslutninger om ressourcer, præstation og medarbejderudvikling.</td>
</tr>
<tr class="even">
<td>Drage fordel af selvbetjeningsfunktionalitet.</td>
<td>Ikke ledig</td>
<td>Ledere kan nu sende anmodninger om nye ansættelser (medarbejdere og kontrahenter), overførsler og opsigelse (ophør af ansættelse). Ledere kan også anmode om en ny stilling, forlænge en stillings varighed eller anmode om ændringer af stillinger.</td>
<td>Disse scenarier blev tidligere kun vist i Personale. Aktivering af disse scenarier giver effektive værktøjer til ledere i en organisation. Valgfrie arbejdsgange kan aktiveres og give det rette niveau for gennemsyn og godkendelse.</td>
</tr>
<tr class="odd">
<td>Få adgang til resultaterne af kompensationsbehandlingen.</td>
<td>Resultaterne er kun tilgængelige på tidspunktet for behandlingen.</td>
<td>Kompensationsbehandlingens resultater kan nu åbnes når som helst, når processen er blevet kørt.</td>
<td>Det giver en fremragende overvågning af processen og af resultatet af processen. Det giver også en omfattende visning af dataene, før medarbejderposter opdateres.</td>
</tr>
<tr class="even">
<td>Få adgang til resultaterne af frynsegodebehandlingen.</td>
<td>Resultaterne er kun tilgængelige på tidspunktet for behandlingen.</td>
<td>Frynsegodebehandlingens resultater kan nu åbnes når som helst, når processen er blevet kørt.</td>
<td>Det giver en omfattende visning af de data, der er opdateret med frynsegodetilmelding og ændring af omkostninger.</td>
</tr>
<tr class="odd">
<td>Vis ændringer af "Gyldig fra"-tidslinje.</td>
<td>Ikke ledig</td>
<td>Dette sammenligningsværktøj er tilgængeligt for medarbejdere, stillinger og job. Det giver en omfattende visning af ændringer fra én version af en post til en anden.</td>
<td>Det sparer tid, når du kan se ændringer, der er opstået over tid, af medarbejdere, stillinger og jobposter. Du kan hurtigt sammenligne to versioner af en post eller alle poster over tid.</td>
</tr>
<tr class="even">
<td>Få vist medarbejdere pr. virksomhed.</td>
<td>Dette er en manuel proces, der udføres via filtrering.</td>
<td>Medarbejder- og kontrahentlister filtreres automatisk af det firma, du er logget på.</td>
<td>Det giver en filtreret visning af medarbejdere, der er ansat i det firma, der er logget på. Medarbejderlisten er stadig tilgængelig for en ufiltreret visning af alle medarbejdere og kontrahenter. Systemet skifter ikke firma baseret på den medarbejder, der er valgt på listen, i den aktuelle version af Dynamics AX.</td>
</tr>
<tr class="odd">
<td>Opdatere kursusdeltagerlisten.</td>
<td>Ikke ledig</td>
<td>Kursusdeltagere kan fjernes fra deltagerlisten.</td>
<td>Det er en nem måde at opdatere kursusdeltagere, der er registreret ved en fejltagelse.</td>
</tr>
<tr class="even">
<td>Administrere kompensationshændelser i en gruppe.</td>
<td>Ikke ledig</td>
<td>Denne funktion strømliner behandling af ændringer af kompensation for medarbejdere.</td>
<td>Den indeholder en enkel og strømlinet proces til opdatering af medarbejderposter gennem kompensationsarbejdsområdet og relaterede sider.</td>
</tr>
</tbody>
</table>

## <a name="inventory-management"></a>Lagerstyring
Der er ikke blevet tilføjet nye funktioner.

## <a name="localization"></a>Lokalisering
<table>






<tbody>
<tr class="odd">
<td><strong>Hvad kan du gøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er det vigtigt?</strong></td>
</tr>
<tr class="even">
<td>Konfigurere og oprette elektroniske dokumenter for at opfylde de lovgivningsmæssige krav i forskellige lande.</td>
<td>Elektroniske dokumenter er hard-coded i X ++ eller som XSLT (Extensible Stylesheet Language Transformations). Eventuelle formatreguleringer kræver udviklingsarbejde. Adgang til data og formatering er ikke isoleret. En justeret formatinstallation kræver en ny Microsoft Dynamics AX-hotfixpakke, der tilsidesætter det eksisterende format. Brugerdefinerede ændringer af hvert format skal overføres manuelt til kildekoden til en ny Microsoft Dynamics AX-hotfixpakke.</td>
<td>Elektronisk rapportering (ER) er et nyt værktøj til konfiguration og generering af elektroniske dokumenter, der er målrettet en forretningsbruger i stedet for en udvikler. Med ER kan du oprette datamodeller, der er specifikke for domænet og uafhængigt af Microsoft Dynamics AX-databasen som datakilder for dokumentformater. En forretningsbruger kan konfigurere formaterne baseret på disse domænespecifikke datamodeller (f.eks. af betalinger, Intrastat-rapporter eller skatterapporter). Brugeren konfigurerer formaterne ved hjælp af enkle visuelle værktøjer, der svarer nogenlunde til Excel. ER understøtter på nuværende tidspunkt oprettelse af elektroniske dokumenter i tekst-, XML- og Excel-formater. Disse dokumenter kan oprettes samtidig og pakket i zip-filer. Datamodeller og formater understøtter versionering. Formatversioner kan have gyldighedsperioder. Hver datamodel eller formatversion gemmes i en separat konfiguration og distribueres til partnere og kunder via LCS. Partnere og kunder kan tilpasse Microsoft-datamodeller og -formater eller kan oprette deres egne. ER gemmer partner- og konfigurationsændringer, som deltaer til Microsoft-konfigurationer, hvilket forenkler opgraderinger til nye versioner af Microsoft-konfigurationer. Ved hjælp af LCS kan partnere også dele deres datamodel- og formatkonfigurationer med andre partnere og kunder, der kan tilpasse og dele dem. Deltatilpasning og nem opgradering understøttes gennem hele tilpasningskæden.</td>
<td>ER forenkler oprettelse, vedligeholdelse og opgradering af elektroniske dokumentformater for at opfylde forskrifterne i forskellige lande. ER gør processen til oprettelse eller ændring af elektroniske dokumentformater hurtigere og nemmere. Disse ændringer kan foretages af forretningsbrugere i stedet for udviklere. ER gør det hurtigere og nemmere for partnere og kunder at opgradere deres formattilpasninger til nye versioner af formater, der er udgivet af Microsoft eller andre partnere. ER er én fælles måde (via LCS), som Microsoft og partnere kan distribuere elektroniske dokumentkonfigurationer til andre partnere og kunder. ER gør det også nemmere for partnere og kunder at tilpasse, opgradere og distribuere elektroniske dokumentformater for deres specifikke forretningskrav.</td>
</tr>
<tr class="odd">
<td>(MEX) Generere mexicanske lovpligtige momsrapporter.</td>
<td>Du skal generere **Salgs- og købmoms**-rapporter ved hjælp af funktionen ikke-realiseret moms, så brugerne kan identificere posteringer, der tilhører de realiserede og ikke-realiserede sektioner baseret på status.</td>
<td>**Salgs- og købsmoms**-rapporter er blevet ændret, og medtager nu funktionen for betinget moms ved hjælp af specifikke afregningsperioder for definitionen af ikke-realiserede og realiserede momskoder.</td>
<td>Ændringer i konfigurationen af momskoder kræves, før brugerne kan oprette disse rapporter korrekt. En betinget momsfunktion er påkrævet, og brugeren skal konfigurere separate afregningsperioder, ikke-realiserede og realiserede, for at identificere posteringerne i de relaterede områdeafsnit.</td>
</tr>
<tr class="even">
<td>(JPN) Administrere dokumentet med opgørelsen over stigende afskrivning af japanske anlægsaktiver.</td>
<td>Ikke ledig</td>
<td>Vigtige erklæringsoplysninger gemmes centralt i et enkelt dokument for bedre vedligeholdelse.</td>
<td>Dokumentetoverensstemmelse og brugervenlig administrationen er med til at reducere problemer under revision og andre undersøgelser.</td>
</tr>
<tr class="odd">
<td>(JPN) Kontrollere JBA-tegn på bankkontoen.</td>
<td>Ikke ledig</td>
<td>Du kan kontrollere, at kana navnefelter kun indeholder tegn, der er tilladt i JBA-bankformatet.</td>
<td>Det hjælper med at reducere afbrydelser for brugerne under generering af betalingsfil på grund af ugyldige tegn.</td>
</tr>
<tr class="even">
<td>(JPN) Indhente japansk penny-difference for anlægsaktiv i slutningen af regnskabsåret.</td>
<td>Ikke ledig</td>
<td>På siden **Parametre for anlægsaktiv** kan du vælge at indhente i slutningen af regnskabsperioden eller regnskabsåret.</td>
<td>Det giver mere fleksibilitet at sammenholde med lokal praksis.</td>
</tr>
<tr class="odd">
<td>(JPN) Generere japanske tilføjede tabeller til virksomhedsmomsopgørelse 16-serien på et opsummeret beløb efter anlægsaktivets overordnede type.</td>
<td>Ikke ledig</td>
<td>På værdimodeller for et anlægsaktiv kan du vælge at opsummere efter overordnet type. Som standard bruges denne funktionalitet til nyligt oprettede anlægsaktiver.</td>
<td>For store virksomheder, der har tusindvis af anlægsaktiver, reducere de opsummerede rapporter i høj grad størrelsen på den rapport, der oprettes.</td>
</tr>
<tr class="even">
<td>(JPN) Begynde at allokere særlig afskrivningsreserve fra det næste regnskabsår for japanske anlægsaktiver.</td>
<td>Ikke ledig</td>
<td>På værdimodellerne for et anlægsaktiv, der har en passende ekstraordinær afskrivningsprofil, kan vælge at starte fordelingen fra den næste regnskabsperiode eller det næste regnskabsår.</td>
<td>Det giver mere fleksibilitet at sammenholde med lokal praksis.</td>
</tr>
<tr class="odd">
<td>(JPN) Oprette en japansk forbrugsmomsrapport, der indeholder de reviderede momssatser.</td>
<td>Forbrugsmomsrapporten er tilgængelig for en momssats på 5 procent.</td>
<td>Forbrugsmomsrapporten indeholder et afsnit til den reviderede momssats (for eksempel 8 procent).</td>
<td>Layoutet er netop offentliggjort af myndighederne.</td>
</tr>
<tr class="even">
<td>(EU) Konfigurere indstillinger for afrunding for EU-listesystemet.</td>
<td>Afrundingsindstillinger for rapportering i EU-listesystemet for forskellige lande er hard-coded i X ++ eller XSLT'er (Extensible Stylesheet Language Transformations).</td>
<td>Afrundingsindstillinger føjes til Udenrigshandelsparametre. Du kan konfigurere afrundingspræcision, afrundingsmetode, outputpræcision og funktionsmåden for beløb, der er mindre end afrundingspræcisionen.</td>
<td>Dette samler og forenkler konfigurationen af rapporteringen i EU-listesystemet. Regulering af afrundingsindstillinger kræver ikke længere udviklingsarbejde.</td>
</tr>
<tr class="odd">
<td>(EU) Konfigurere regler for anvendelse af modtagermoms.</td>
<td>Anvendelighedsreglerne for modtagermoms er hard-coded til scenariet for indenlandsk modtagermoms. Tærsklen for anvendelighed kan konfigureres pr. varegruppe. Funktionaliteten er kun tilgængelige for Storbritannien.</td>
<td>Du kan konfigurere anvendelighedsregler for modtagermoms pr. dokumenttype (købs-/salgsordre, kreditorfaktura, fritekstfaktura osv.) og en gruppe for modtagermoms, der kombinerer varer, varegrupper og købs-/salgskategorier. Anvendelighedsreglerne er for gældende dato. Du kan også markere enkelte momskoder i momsgrupper som gældende for modtagermoms. Salgsfakturarapporten justeres, så den repræsenterer oplysningerne om den anvendte modtagermoms. Funktionen er tilgængelig for alle europæiske lande/områder.</td>
<td>Denne ændring ensretter konfigurationen af anvendelighedsreglerne for modtagermoms og understøtter anvendelsen af forordningerne for indenlandsk modtagermoms i europæiske lande.</td>
</tr>
<tr class="even">
<td>(DE) Generere den tyske revisionsfil - GDPdUGoBD</td>
<td>Brugere kan konfigurere definitionen af tabeller, der indeholder økonomiske data, der skal eksporteres i et format, der er godkendt af tyske revisorer og myndigheder.</td>
<td>Denne funktion er implementeret som en elektronisk rapporteringskonfiguration. Funktionerne er tilgængelige for Tyskland og Østrig.</td>
<td>Denne ændring giver brugeren mange flere muligheder for dataformatering, transformeringer, og indeholder også alle de fordele, der kommer fra konfigurationsstyring af elektronisk rapporteringslivscyklus, som f.eks. nem konfigurationsudveksling, versionering osv.</td>
</tr>
<tr class="odd">
<td>(FR) Saldoliste med rapport over konti med gruppetotaler.</td>
<td>Saldoliste med rapport over konti med gruppetotaler er implementeret som SSRS-rapport (LedgerAccountSum\_FR).</td>
<td>Saldoliste med rapport over konti med gruppetotaler er implementeret som Management Reporter-rapport tilgængelig i LCS-aktivbibliotekets lokaliserede mappe med finansielle rapporter.</td>
<td>Dette tillader brugere at få fordelene og friheden i tilpasninger fra brug af finansielle rapporter i Management Reporter.</td>
</tr>
<tr class="even">
<td>(EU) Betalingsadviserings-, følgeskrivelses- og kontrolrapporter for betalinger.</td>
<td>Alle disse rapporter er implementeret og SSRS-rapporter.</td>
<td>Disse rapporter er blevet implementeret som Open XML-skabeloner, der bruges i Microsoft Excel.</td>
<td>Elektroniske betalingskonfigurationer indeholder opsætning og skabeloner til betalingsfilformater. Dette gør det muligt for brugere at få fordelene og friheden i rapporttilpasninger fra brug af Elektronisk rapportering.</td>
</tr>
<tr class="odd">
<td>(EU) Konfigurere indstillinger for afrunding for Intrastat.</td>
<td>Afrundingsindstillinger for rapportering i Intrastat for forskellige lande er hard-coded i X ++ eller XSLT'er (Extensible Stylesheet Language Transformations).</td>
<td>Afrundingsindstillinger føjes til udenrigshandelsparametre. Du kan konfigurere afrundingspræcision, afrundingsmetode, outputpræcision og funktionsmåden for beløb, der er mindre end afrundingspræcisionen.</td>
<td>Dette samler og forenkler konfigurationen af rapporteringen i Intrastat. Regulering af afrundingsindstillinger kræver ikke længere udviklingsarbejde.</td>
</tr>
<tr class="even">
<td>(EU) Konfigurere Intrastat-varekoder i kategorihierarkier.</td>
<td>Intrastat-varekoder er en separat liste. Der er kategorihierarki af typen Varekode, men disse varekoder kan have standardværdier i Retail HQent og salgskategorier.</td>
<td>En separat liste over Intrastat-varekoder flettes med produkthierarki af typen Varekode.</td>
<td>Dette samler tilgangen til tildeling af varekoder til frigivne produkter og kategorier i salgs- og købsdokumenter.</td>
</tr>
<tr class="odd">
<td>(EU) Rapportantallet i supplerende enheder til Intrastat ved hjælp af enhedskonverteringsindstilling.</td>
<td>Intrastat-varekoder har et tekstfelt til at identificere flere enheder, og kortet **Produkt** har et felt til at identificere antallet af supplerende enheder i kg.</td>
<td>Supplerende enheder til Intrastat-varekoder vælges på listen over enheder. Antallet af supplerende enheder beregnes gennem enhedskonverteringsindstillinger.</td>
<td>Dette samler tilgangen til genberegning fra transaktionsenheder til yderligere enheder.</td>
</tr>
<tr class="even">
<td>(EU) Tildel standardtransportmåde til leveringsmåde.</td>
<td>Ikke ledig</td>
<td>Et felt for standardtransportmåde føjes til leveringsmåden.</td>
<td>Dette forenkler udarbejdelsen af Intrastat-rapportering.</td>
</tr>
<tr class="odd">
<td>(EU) Marker, at frigivet produkt ikke skal rapporteres i Intrastat.</td>
<td>Ikke ledig</td>
<td>En indstilling, der udelukker varen fra Intrastat-rapportering, føjes til det frigivne produkt.</td>
<td>Dette forenkler udarbejdelsen af Intrastat-rapportering.</td>
</tr>
</tbody>
</table>

## <a name="manufacturing"></a>Produktion
|                                                                                                                                                      |                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hvad kan du gøre?**                                                                                                                                 | **Dynamics AX 2012**                                                                                                             | **Dynamics AX 7.0**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | **Hvorfor er det vigtigt?**                                                                                                                                                                                                                                            |
| Udfør en kontrol af materialetilgængelighed til produktionsordrer på en separat side, der åbnes fra arbejdsområdet **Administration af produktion**. | Ikke ledig                                                                                                                    | Den produktionsansvarlige kan kontrollere, om materialer til planlagte produktionsordrer er tilgængelige på den ønskede dato. I arbejdsområdet kan den produktionsansvarlige se, hvor mange produktionsordrer er i tilstanden planlagt og afventer frigivelse. Baseret på den dynamiske behovsplan opdateres oplysninger om materialetilgængelighed, hvis materialekrav opfyldes af den disponible lagerbeholdning for faktiske ordrer eller planlagte ordrer. Baseret på oplysninger om materialetilgængelighed, kan den produktionsansvarlige frigive ordrerne på siden **Tilgængelighed af materiale**.                                                                                                                                                                                                                                                                                                                        | Det hjælper produktionsansvarlige med at foretage korrekte beslutninger om tildeling af materialer til ordrer, når produktionsordrer frigives til produktion.                                                                                                       |
| Starte og rapportere status på produktionsjob ved hjælp af den nye side **Jobkortenhed**.                                                              | Formularen **Jobregistrering** er primært målrettet større terminalskærme, og der er typisk adgang til brugergrænsefladen via museklik. | Selvom den nye side **Jobkortenhed** er designet med henblik på overskuelighed, så er den også designet til berøring. Siden passer godt på mobilenheder som tablets og telefoner. Produktionsarbejderen bliver ikke helt så belastet af informationer, men får mere intuitiv brugervenlighed. Arbejderen kan udføre traditionelle opgaver som start, afslutning og rapportering af status på en sag. Ud over at arbejde på det aktuelle job eller logge af og stemple ud kan arbejderen se vedhæftede filer, angive frokostpause og udføre andre aktiviteter. Job sættes i kør til arbejderen i planlagtfølge, men arbejderen kan også plukke dem ud. Siden er primært rettet mod separate produktionsoperationer, hvor materialer forberedes til produktion. Til scenarier, der er relateret til rapportering af samprodukter og biprodukter, og materialer, der plukkes ved sporing af dimensioner, skal du bruge siden **Jobregistrering**. | Med indførelse af en alternativ brugergrænseflade, der er beregnet til berøring og kan åbnes fra alle typer enheder, som f.eks. terminalskærme og mobilenheder, er denne funktion med til at reducere implementeringsomkostninger for en traditionel implementering af produktionsregistreringer. |

## <a name="master-planning-and-forecasting"></a>Varedisponering og prognose
|                                                                                                                            |                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hvad kan du gøre?**                                                                                                       | **Dynamics AX 2012**                                                                                                                                                                                                                                                                          | **Dynamics AX 7.0**                                                                                                                                                                                                                                                                                                                                               | **Hvorfor er det vigtigt?**                                                                                                                              |
| Advare brugeren, hvis en salgsordre eller produktionsordre ikke klar til levering på den planlagte dato.                         | Advarsler, der oprettes ved varedisponering, kaldes *terminssætninger*. *Termin* er en kontrakt mellem to parter om køb eller salg af et aktiv til en pris, der er aftalt i dag (*terminsprisen*), selvom levering og betaling foregår på et fremtidigt tidspunkt (*leveringsdatoen*). | *Terminssætninger* og *terminsdatoer* er blevet omdøbt til henholdsvis *beregnede forsinkelser* og *forsinkelsesdatoer*.                                                                                                                                                                                                                                                   | Den terminologi, der blev brugt i AX 2012, var unøjagtig og har ført til forkerte oversættelser.                                                               |
| Få hurtig indsigt i status for en varedisponeringskørsel, hastende planlagte ordrer og ordreforslag, der medfører forsinkelser. | Oplysningerne er tilgængelige, men de er spredt over flere formularer.                                                                                                                                                                                                                       | Arbejdsområdet **Varedisponering** byder på hurtige oplysninger om, hvor den sidste varedisponeringskørsel blev fuldført, om der opstod fejl, hvad de vigtigste ordreforslag er og hvilke ordreforslag medføre forsinkelser.                                                                                                                                   | Du får fordelen af den oversigt, arbejdsområdet viser. Relevante oplysninger er sammensat i en vejledning for varedisponering, som forbedrer produktiviteten. |
| Bruge Excel til at opdatere behovsprognoser.                                                                                      | Ikke ledig                                                                                                                                                                                                                                                                                 | Du kan drage fordel af problemfri integration med Microsoft Excel, når du skriver behovsprognoser, opdatere og slette behovsprognoser.                                                                                                                                                                                                                             | Det hjælper med at øge effektiviteten og produktiviteten.                                                                                                          |
| Beregne fremtidigt behov og oprette behovsprognoser baseret på historiske transaktionsdata.                                  | I Microsoft Dynamics AX 2012 R3 bruges behovsmodeller i Microsoft SQL Server Analysis Service til at oprette behovsprognoseforudsigelser.                                                                                                                                                | Vurdere fremtidige behov ved hjælp af funktionerne og udvidelsesmulighederne i en Microsoft Azure Machine Learning skytjeneste. Det er let at bruge og udvide prognosemodellerne i Machine Learning til at opfylde kundekrav. Tjenesten udfører valg på grundlag af bedste match-modellen og tilbyder nøgletal (KPI'er), der kan bruges til at beregne prognosenøjagtigheden. | Genererer mere nøjagtige prognoser ved hjælp af Machine Learning-teknikker.                                                                              |
| Optimere ordredato og antal baseret på en visuel oversigt over relaterede handlinger fra kørsel af behovsplanlægning.          | Diagrammet med oversigt over handlinger er tilgængeligt, men viser alle relaterede handlinger. Når der anvendes handlinger, forsvinder de straks fra visningen.                                                                                                                                             | Handlingsdiagrammet giver et bedre overblik. Det omfatter indstillinger, der gør det muligt kun at vise anvendte handlinger og direkte relaterede handlinger. Når handlinger udføres, vises de nedtonet, men vises stadig. Derfor bevares oversigten. Yderligere oplysninger er føjet til handlingsdiagrammet for at vise dataene på én side.                               | Du kan drage fordel af forbedringen af produktiviteten, fordi du kun fokuserer på de relevante handlinger.                                                              |

## <a name="procurement-and-sourcing"></a>Indkøb og forsyning
|                                                                                                                                                         |                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hvad kan du gøre?**                                                                                                                                    | **Dynamics AX 2012** | **Dynamics AX 7.0**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | **Hvorfor er det vigtigt?**                                                                                                                                                                                                               |
| Bruge arbejdsområdet **Klargøring af indkøbsordrer** til at få hurtig indsigt i status for indkøbsordrer, der er ved at blive forberedt.                      | Understøttes ikke        | Arbejdsområdet **Klargøring af indkøbsordrer** viser en oversigt over ordrer fra det tidspunkt, hvor de blev oprettet som kladde og sporet via arbejdsgang for godkendelsestilstande og fremad mod bekræftelse.                                                                                                                                                                                                                                                                                                                      | Din indkøbsafdeling behøver ikke længere at søge oplysninger fra flere sider, men nu er omfattet af den oversigt, arbejdsområdet viser.                                                                                         |
| Bruge arbejdsområdet **Indkøbsordre, modtagelse og opfølgning** for at få hurtig indsigt i indkøbsordrer, der afventer tilgang, for at hjælpe med opfølgning. | Understøttes ikke        | Arbejdsområdet **Indkøbsordre, modtagelse og opfølgning** viser en oversigt over bekræftede indkøbsordrer, der har ventende modtagelser eller leverancer. Arbejdsområdet indeholder lister over forfaldne modtagelser og afventende tilgange for at hjælpe med proaktiv gennemgang og opfølgning fra leverandøren. Arbejdsområdet viser også indkøbsordrer, hvor modtagelsesregistrering er sket på lageret, for at sikre, at modtagelsen bogføres. Returvarer fra indkøbsordrer, som endnu ikke er leveret, er også tilgængelige til gennemsyn. | Din indkøbsafdeling får fordelen af den oversigt, arbejdsområdet viser. Relevante oplysninger er sammensat i en vejledning for opfølgning, som forbedrer produktiviteten.                                                                |
| Sende indkøbsordrer til bekræftelse til en kreditorportal, som Dynamics AX-klienten er vært for. Lad kreditoren bekræfte eller afvise.                            | Understøttes ikke        | Grænsefladen i kreditorportalen gør det muligt for kreditorer at modtage indkøbsordrer, der skal bekræftes eller afvises. Den gør det også muligt for kreditoren at få et overblik over alle bekræftede indkøbsordrer på en konto. Indkøberen kan sende en indkøbsordre og anmode om en bekræftelse fra kreditoren. Kreditoren skal være en registreret Microsoft Azure Active Directory-bruger (Azure AD) i Dynamics AX, en kontakt hos kreditoren og har en dedikeret sikkerhedsrolle.                                                     | Din indkøbsafdeling får fordelen af reduceret papirarbejde og manuel styring af svar på indkøbsordrer, når de strømmer direkte ud i systemet. Én kilde til sandheden reducerer misforståelser mellem kunde og leverandør. |

## <a name="projects"></a>Projekter
|                                        |                                                                                         |                                                                                                                                              |                                                          |
|----------------------------------------|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| **Hvad kan du gøre?**                   | **Dynamics AX 2012**                                                                    | **Dynamics AX 7.0**                                                                                                                          | **Hvorfor er det vigtigt?**                               |
| Reservere arbejdere som ressourcer på projekter. | I lighed med ressourcer reserveres arbejdere direkte på projekter sammen med ressourcer. | Ressourcetabellen, hvor ressourcer til produktion opbevares, kan nu bruges til at reservere arbejdere som ressourcer i et projekt. | Når du reserverer projekter, behøver du kun at reservere ressourcer. |

## <a name="retail-sales-marketing-and-customer-service"></a>Detailsalg, marketing og kundeservice
### <a name="retail-hq"></a>Retail HQ

Microsoft Azure-baseret Retail HQ tilbyder centraliseret styring af og fuldstændig synlighed i alle aspekter af handelsoperationer via en webklient.

<table>






<tbody>
<tr class="odd">
<td><strong>Hvad kan du gøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er det vigtigt?</strong></td>
</tr>
<tr class="even">
<td>Udføre handelsoperationer.</td>
<td>Brugere skal have adgang til flere formularer for at administrere disse data:
<ul>
<li>Kategoristyring</li>
<li>Produktstyring</li>
<li>Kanalproduktattributter</li>
<li>Udvalg</li>
<li>Administration af kataloger</li>
<li>Pakker</li>
<li>Priser og rabatter</li>
</ul></td>
<td>Arbejdsområdet <strong>Kategori og produktstyring</strong> giver følgende funktionalitet:
<ul>
<li>Sortimentsstyring.</li>
<li>Sporing af sortimentslivscyklus.</li>
<li>Styring af frigivne produkter.</li>
</ul>
Arbejdsområdet <strong>Styring af priser og rabatter</strong> giver følgende funktionalitet:
<ul>
<li>Administration af pris og rabat for en given kanal og kategori.</li>
<li>Styring af prisregler for kategorier.</li>
<li>Pris- og rabatprioriteter, som du kan bruge til at tildele prioriteter til prisgrupper og rabatter, så du kan styre den rækkefølge, de anvendes i.</li>
<li>Tilhørsforhold og administration af katalograbat.</li>
</ul>
Arbejdsområdet <strong>Administration af kataloger</strong> giver følgende funktionalitet:
<ul>
<li>Oversigt over aktive kataloger.</li>
<li>Kataloglivscyklussporing på én lokalitet.</li>
</ul></td>
<td><ul>
<li>Arbejdsområder forbedrer effektivitet og produktivitet for medarbejdere ved at lade dem administrere deres opgaver og handlinger, der er knyttet til merchandizing-rollen, centralt.</li>
<li>Funktionen pris- og rabatoplysningsprioriteter giver kunderne mere kontrol over, hvordan priser og rabatter anvendes. Funktionen giver også nye scenarier, hvor højere butikspriser vinder over standardpriserne.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Administrer detailkanalsystemer og -operationer.</td>
<td>Brugeren skal have adgang til flere formularer for at udføre følgende opgaver:
<ul>
<li>Oprette og konfigurere nye kanaler og relaterede objekter.</li>
<li>Administrere daglige aktiviteter i butikken.</li>
<li>Behandle detailtransaktioner i Microsoft Dynamics AX, generere detailopgørelser og opdatere Microsoft Dynamics AX-lager og regnskaber.</li>
</ul>
 </td>
<td>Med arbejdsområdet <strong>Installation af kanal</strong> kan du udføre følgende opgaver:
<ul>
<li>Oprette nye kanaler og relaterede objekter.</li>
<li>Spore status for konfiguration af detailbutik.</li>
<li>Tage de nødvendige trin for at fuldføre en opgave eller angive oplysninger til fuldførelse af opgaven.</li>
<li>Spore status for enheder og direkte kontrollere og hente MPOS-programinstallationen (Retail moderne POS) i butikker.</li>
<li>Få adgang til alle relaterede sider.</li>
</ul>Med arbejdsområdet 
<strong>Detailbutiksstyring</strong> kan du udføre følgende opgaver:
<ul>
<li>Administrere arbejdere og arbejdernes POS-tilladelser.</li>
<li>Spore skiftestatus for en bestemt butik eller butiksgruppe.</li>
<li>Direkte validere og hente MPOS-programinstallationen i butikker.</li>
<li>Udskrive rapporter og få adgang til relaterede sider.</li>
</ul>Med arbejdsområdet 
<strong>Detailbutiksregnskab</strong> kan du udføre følgende opgaver:
<ul>
<li>Oprette, beregne og bogføre opgørelser for en given kanal.</li>
<li>Planlægge batchjob for opdatering af lageret, og beregne og bogføre opgørelser.</li>
<li>Spore åbne opgørelser.</li>
<li>Spore skiftestatus for en bestemt butik eller butiksgruppe.</li>
<li>Udskrive rapporter og hurtigt få adgang til alle relaterede sider.</li>
</ul></td>
<td>Arbejdsområder forbedrer effektivitet og produktivitet for arbejdere ved at lade dem administrere de fleste af deres opgaver og handlinger, der er knyttet til kanalinstallation, butiksstyring og regnskaber, centralt.</td>
</tr>
<tr class="even">
<td>Administrere detail-it-drift.</td>
<td>Brugeren skal have adgang til flere formularer.</td>
<td>Arbejdsområdet <strong>Detail-it</strong> muliggør Commerce Data Exchange-forespørgsler i en given kanal på samme sted, så du kan udføre følgende opgaver:
<ul>
<li>Downloade sessioner.</li>
<li>Uploade sessioner.</li>
<li>Spore mislykkede sessioner og starte igen, eller køre dem igen.</li>
<li>Få vist eller køre kommende job.</li>
</ul></td>
<td>Arbejdsområder forbedrer effektivitet og produktivitet for medarbejdere ved at lade dem administrere deres opgaver og handlinger, der er knyttet til detail-it-drift, centralt.</td>
</tr>
<tr class="odd">
<td>Importere eller eksportere data ved hjælp af dataenheder.</td>
<td>AX 2012 understøtter out-of-box overførsel til Microsoft Dynamics Retail Management System (RMS) gennem strukturen til dataimport/-eksport.</td>
<td>Detaildataenheder har blevet udvidet til at omfatte alle hoved- og referencedata, der er relateret til detail. Der er også forbedret understøttelse af dataenheder på tværs af hele Dynamics AX-løsningen.</td>
<td>Dataenheder giver kunder mulighed for at foretage metadatabaseret import og eksport af data. Med OData-enheder kan kunder også integrere Dynamics AX med tredjepartsprogrammer.</td>
</tr>
<tr class="even">
<td>Udføre intelligent analyse ved hjælp af BI-rapporter fra Dynamics AX Microsoft og POS-klienten.</td>
<td>Mere end 25 administrationsrapporter og fem rapporter på kanalsiden er tilgængelige.</td>
<td>Mere end 30 administrationsrapporter og 10 rapporter på kanalsiden er tilgængelige.</td>
<td>Med disse rapporter giver kunder mere BI til at forudsige tendenser, afdække indsigt og løbende få optimal drift.</td>
</tr>
<tr class="odd">
<td>Analyser detailkanalsalgsdata ved hjælp af Power BI-indholdet "Overvåg detailkanalydelse".</td>
<td>Ikke tilgængelig</td>
<td>Vælg på PowerBI.com, <strong>Hent data</strong>, og vælg derefter indholdspakken <strong>Dynamics AX – detailkanalydelse</strong>. Angiv URL-adressen til dit Dynamics AX slutpunkt for at se dine data afspejlet i dashboardet.</td>
<td>Med tre eller fire klik kan organisationer installere et Power BI-dashboard, som indeholder vigtige finansielle data. Indholdet kan tilpasses af organisationen. Desuden kan brugere integrere Power BI-dashboardfelter i deres personlige arbejdsområder i Dynamics AX, så de kan få et overblik over analyseoplysninger.</td>
</tr>
<tr class="even">
<td>Konfigurere forbrugertilladelser.</td>
<td>Ikke ledig</td>
<td>Kunder kan vælge, om POS-handlinger skal være tilgængelige for forbrugerne. Retail Server bruger tilladelser til API-kald (application programming interface).</td>
<td>Det giver mulighed for at konfigurere tilladelser på forbrugerniveau.</td>
</tr>
<tr class="odd">
<td>Administrere og validere enhedskonfigurationer.</td>
<td>Ikke ledig</td>
<td>Funktionen til konfigurationsstyring og validering giver følgende funktionalitet:
<ul>
<li>Overførsel af massekonfigurationsdata</li>
<li>Validering af forretningsenhed</li>
</ul></td>
<td>Det giver mulighed for at initialisere konfigurationen og kontrollere status og fuldstændigheden af konfigurationen for de forskellige elementer i konfigurationen.</td>
</tr>
</tbody>
</table>

### <a name="retail-hardware-station"></a>Retail-hardwarestation

|                                                                                                  |                                                                         |                                                                                                                                                                                                                                                                                                                                                               |                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **Hvad kan du gøre?**                                                                             | **Dynamics AX 2012**                                                    | **Dynamics AX 7.0**                                                                                                                                                                                                                                                                                                                                           | **Hvorfor er det vigtigt?**                                                                                                        |
| Aktivere POS-enheder for at oprette forbindelse til eksterne enheder som printere, pengeskuffer eller betalingsenheder. | MPOS-hardwareprofil bruges til at angive de enheder, der bruges. | En ekstra hardwareprofil understøtter flere forskellige hardwareenheder fra én station til den næste. En ny hardwarestationsprofil understøtter et entydigt terminal-id for hver hardwarestation, når elektroniske pengeoverførselstransaktioner (EFT) behandles. Understøttelse af elektronisk pengeoverførsel er blevet flettet med hardwarestation for at reducere MPOS' deltagelse i elektronisk pengeoverførsel-betalingsbehandling. | Det giver større fleksibilitet for implementeringer. Det giver også forbedret sikkerhed og reduceret eksponering for kreditkortdata. |

### <a name="retail-server-and-data-management"></a>Retail Server og administration af data

Retail Server og administration af data gør det muligt for forbrugere og virksomheder at oprette en omnikanal-indkøbsoplevelse på tværs af online-, butiks- og callcenterkanaler.

<table>






<tbody>
<tr class="odd">
<td><strong>Hvad kan du gøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er det vigtigt?</strong></td>
</tr>
<tr class="even">
<td>Oprette forbindelse til en CRT-database (commerce runtime), der indeholder forretningsdata til kanalen, ved hjælp af CRT-tjenester.</td>
<td>OData V3 understøttes.</td>
<td>OData V4 understøttes.</td>
<td>Det hjælper kunden med at holde sig ajour med OData standarder. Det opretter også en robust omni-kanaloplevelse ved at integrere salg på tværs af kanaler i butikken, mobil- og onlinekanaler.</td>
</tr>
<tr class="odd">
<td>Understøtte detailtjenester som et sæt tjenester, der kan fungere som vært.</td>
<td>E-handels-API'en understøttes ikke via Retail Server.</td>
<td>E-handels-API'en er nu tilgængelig via Retail Server og understøtter onlinescenarier.</td>
<td>Den indeholder hosted og skalerbar e-handelstjenester, der kan bruges med tredjeparts onlinebutikker.</td>
</tr>
<tr class="even">
<td>Flyt data mellem Microsoft Dynamics AX-administration og kanaler ved hjælp af Commerce Data Exchange.</td>
<td>Commerce Data Exchange er et system, der overfører data mellem Microsoft Dynamics AX og detailkanaler, som f.eks. onlinebutikker eller fysiske butikker. Du kan finde flere oplysninger under <a href="https://technet.microsoft.com/en-us/library/dn741440.aspx">Commerce Data Exchange [AX 2012]</a>.</td>
<td>Der er funktionel paritet med Microsoft Dynamics AX 2012 CU8. Men bemærk følgende oplysninger:
<ul>
<li>Commerce Data Exchange er blevet omarbejdet til skyen.</li>
<li>Asynkron tjeneste bruger direkte databaseadgang til kanaldatabasen.</li>
<li>Commerce Data Exchange: Real-time Service er placeret som en brugerdefineret Microsoft Dynamics AX-tjeneste.</li>
<li>MPOS håndterer synkronisering mellem offlinedatabaser og Retail Server.</li>
</ul></td>
<td>Commerce Data Exchange er blevet omarbejdet til skyplatformen. Det styrer fortsat data mellem Microsoft Dynamics AX og detailkanaler, som f.eks. onlinebutikker eller fysiske butikker.</td>
</tr>
<tr class="odd">
<td>Understøtter plug and play, delvist integrerede betalingsprocesser på tværs af kanaler ved hjælp af betalings-SDK'et.</td>
<td>AX 2012 giver følgende funktionalitet:
<ul>
<li>Understøttelse af alle kanaler: POS, e-handel og callcenter.</li>
<li>Understøttelse af kort findes og kortet findes ikke.</li>
<li>Side til at acceptere betaling.</li>
<li>Understøttelse af ekstern enhed til LS5300 og MX925 som eksempelkode i Retail SDK.</li>
</ul></td>
<td>Den aktuelle version af Dynamics AX understøtter alle eksisterende kredit/debetkortfunktioner i Microsoft Dynamics AX for Retail 2012 og fire nye forbedringer.</td>
<td>Det gør det muligt for kunden at behandle kredit/debetkorttransaktioner for betalinger.</td>
</tr>
<tr class="even">
<td>Aktivere enheder ved hjælp af en Microsoft-konto (Microsoft Azure Active Directory (Azure AD)).</td>
<td>Ikke ledig</td>
<td>Følgende funktionalitet leveres:
<ul>
<li>Forbedret sikkerhed ved Azure AD-baseret aktivering til skyen.</li>
<li>Forbedret sikkerhed til administration af token.</li>
<li>Forbedret pålidelighed, fejlfinding og fejlmeddelelser under aktivering</li>
<li>Forenklede it-administrationsopgaver, der vedrører aktivering.</li>
<li>Revurderet trusselsmodel og løste sikkerhedsproblemer.</li>
</ul></td>
<td>Det giver følgende fordele:
<ul>
<li>Sikkerheden forbedres gennem Azure AD og enhedstoken-id (RS-kald, som bruger et token, brugerspecifikt applager).</li>
<li>Det standser uautoriseret fjernbrug af MPOS (fysisk enhed).</li>
<li>Det registrerer MPOS-enheder til PCI-overholdelsesformål.</li>
<li>Det tilknytter fysiske enheder til en forretningsenhed (register) ved hjælp af en tokenenhed.</li>
<li>Den initialiserer indstillingerne for jævn MPOS-funktionalitet (nummerserier og hardwareprofiler) som det første berøringspunkt for MPOS.</li>
<li>Det rapporterer enhedsoplysninger fra hovedkontorer.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Administrer rich media-indhold til oprettelse og betjening via Media Gallery.</td>
<td>Ikke ledig</td>
<td><ul>
<li>Understøttelse af billedoverførsel og også visning, administration og sletning fra Media Gallery for både eksternt tilknyttede og Retail-tilknyttede billeder.</li>
<li>Understøtter billedoverførsel og -visning fra enhedssider (<strong>Produkter</strong>, <strong>Kataloger</strong>og så videre) ved at sammenkæde et billede fra galleriet og indlæse et billede fra skrivebordet.</li>
<li>Optimerer billeder til miniature, brugerdefineret størrelse og original.</li>
<li>Massesammenkæder enheder ved hjælp af en skabelon og baggrundsjob til massetilknytning.</li>
<li>Microsoft Excel-integration overskriver attributgruppebegrænsning af navngivningskonventioner og foruddefinerede stier.</li>
<li>Understøtter offlineafbildninger og sikre billeder til indhold i personlige oplysninger (PII), f.eks. medarbejder- og debitorbilleder, hvor Retail er vært.</li>
</ul></td>
<td><ul>
<li>Det afhjælper smertepunkter omkring eksternt tilknyttede billeder, så du kan undgå at gå frem og tilbage og i stedet kan administrere på et enkelt sted.</li>
<li>Det giver effektiv indholdsstyring via Media Gallery for overførte og eksternt tilknyttede billeder og giver også filtrering, så du bedre kan finde billeder.</li>
<li>Du kan nemt oprette massetilknytninger mellem eksternt tilknyttede billeder og enheder som produkter og kataloger.</li>
<li>Det understøtter lagring af billeder på Retail-vært og Excel-integration til nem opdatering.</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="rich-clientele-experience"></a>Rich clientele-oplevelse

Retail tilbyder fængslende mobiloplevelser hvor som helst, når som helst og på enhver enhed. Denne funktion giver mulighed for udvidet shopping og butiksoplevelser på tværs af alle kanaler.

<table>






<tbody>
<tr class="odd">
<td><strong>Hvad kan du gøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er det vigtigt?</strong></td>
</tr>
<tr class="even">
<td>Søge, gennemse, slå op eller scanne produkter, føje produkter til en indkøbsvogn, acceptere betaling og tjekke ud ved hjælp af en intuitiv, berøringsvenlig, avanceret og fængslende brugeroplevelse på MPOS.</td>
<td>AX 2012 giver mulighed for følgende funktioner:
<ul>
<li>Udføre salg, returvarer og afvisninger.</li>
<li>Oprette, ændre og afhente kundeordrer.</li>
<li>Udføre skifte- og skuffehandlinger.</li>
<li>Plukke og modtage ordrer og udføre statusoptællinger.</li>
<li>Få vist butiksrapporter.</li>
</ul></td>
<td>Funktionel paritet med AX 2012 MPOS leveres. Dette inkluderer følgende funktioner:
<ul>
<li>Kundeopslag på tværs af butikker/kanaler.</li>
<li>Muligheden for at oprette kundeordrer uden adgang til Real-time Service.</li>
<li>Forbedret enhedsaktiveringsarbejdsprocesser, status og fejlmeddelelser.</li>
<li>Forbedringer af udvidelsesmuligheder som f.eks. før/efter-udløsere og understøttelse af aktivitet for forbedret tilpasning.</li>
</ul></td>
<td>Salgsmedarbejderne kan behandle salgsposteringer og kundeordrer og udføre daglige operationer og lagerstyring ved hjælp af mobilenheder hvor som helst i butikken.</td>
</tr>
<tr class="odd">
<td>Starte POS som en web-app via sky-POS.</td>
<td>Ikke ledig</td>
<td>Funktionel paritet med MPOS leveres. Dette inkluderer følgende funktioner:
<ul>
<li>Enhedsaktivering ved hjælp af AAD</li>
<li>Responsivt layoutdesign</li>
<li>Understøttelse af Edge-, Internet Explorer- og Chrome-browsere.</li>
</ul></td>
<td>Det giver en webapp-POS, der indeholder funktioner, der er kompatible med MPOS, og som kan bruges på tværs af platforme og browsere uden omkostninger til installation.</td>
</tr>
<tr class="even">
<td>Integrere med indholdsstyringssystemer for at oprette et omnikanal e-handelswebsted.</td>
<td>Microsoft SharePoint og tredjeparts udstillingsvinduer understøttes.</td>
<td>Der findes en e-handelsplatform, der understøtter tredjeparts udstillingsvinduer. Platformen indeholder følgende funktioner:
<ul>
<li>En omfattende forbruger-API.</li>
<li>Godkendelsesintegration med alle åbne id-udbydere fra tredjepart.</li>
<li>Betalingsintegration.</li>
</ul></td>
<td>Kunder har nu mulighed for at bruge indholdsstyringssystemet efter eget valg.</td>
</tr>
<tr class="odd">
<td>Målrette kunder via kataloger til postordresalg og strømline operationer gennem hurtig ordreindtastning, assisterede salg og udførelse ved hjælp af Call Center.</td>
<td><ul>
<li>Callcenter-kanal</li>
<li>Postordrekataloger</li>
<li>Hurtig ordreindtastning og assisteret salg</li>
<li>Forbedret ordreopfyldelse</li>
<li>Kundeservice</li>
<li>Integreret prissætning og specialtilbud/rabatter</li>
</ul></td>
<td>Funktionsparitet med AX 2012 Call Center-løsning er tilgængelig, med undtagelse af pristilsidesættelser.</td>
<td>Callcentre er en type detailkanal, hvor arbejderne tager ordrer fra kunder over telefonen og opretter salgsordrer.</td>
</tr>
</tbody>
</table>

### <a name="commerce-essentials"></a>Oprindelsesdata til handel

En detail- og handelsfokuseret konfigurationsindstilling hjælper med at strømline detailspecifikke installationer.

|                                               |                                                                                                             |                                                                                                                                                                               |                                                                                                                                                         |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hvad kan du gøre?**                          | **Dynamics AX 2012**                                                                                        | **Dynamics AX 7.0**                                                                                                                                                           | **Hvorfor er det vigtigt?**                                                                                                                              |
| Bruge dashboardet Oprindelsesdata til handel.        | En områdeside med links til menupunkter er tilgængelig.                                                         | Oprindelsesdata til handel-dashboardet indeholder links til hyppige opgaver, herunder links til arbejdsområder, Power BI-webkontrolelementet, favoritter, seneste sider og aktuelle arbejdsopgaver. | Det forbedrede dashboard giver arbejdstagere muligheder ved at gøre dem mere effektive og give dem et fleksibelt udgangspunkt for alle detailspecifikke opgaver.             |
| Bruge dataenheder til at få adgang til kontoændringer.  | Kontoændringer eksporteres til en mappe i filsystemet.                                                | Kontoændringer er tilgængelige via dataenheder.                                                                                                                         | Denne funktion giver større fleksibilitet, når du flytter data mellem forskellige systemer. Denne funktion kan også forbedres gennem OData-applikationer. |
| Bruge sky-POS og MPOS.                       | Kun Enterprise POS (EPOS) understøttes out-of-the-box.                                                     | MPOS og sky-POS erstatter EPOS-klienten. E-handelskanalen er også blevet føjet til Oprindelsesdata til handel som standard.                                                     | Denne funktion giver mulighed for større out-of-box-kanalunderstøttelse med POS-klienter, der kan implementeres hurtigt.                                                  |
| Implementere og vedligeholde to-lagsarkitektur. | Dataimport/eksportstrukturen giver mulighed for at flytte data mellem AX 2012 og tredjepartssystemer. | Data-enheder, der er oprettet for at forbedre understøttelse af to-lagsarkitektur.                                                                                                           | Dataenheder og OData-programmer giver et abstraktionslag for at gøre det lettere at implementere og vedligeholde to-lagscenarier.                          |
| Forenkle formularer.                               | Brugerdefineret kode kræves for at forenkle brugergrænsefladen.                                                                 | Formular- og menuudvidelser giver standardiseret forenkling af brugergrænsefladen.                                                                                                              | Denne funktion giver en hurtigere og nemmere måde at finjustere formularer baseret på forhandlerens behov.                                                             |

### <a name="pos-task-recorder"></a>POS-arbejdsrutineoptager

<table>






<tbody>
<tr class="odd">
<td><strong>Hvad kan du gøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er det vigtigt?</strong></td>
</tr>
<tr class="even">
<td>Oprette og dele opgaveguider og dokumenter til moderne POS.</td>
<td>Ikke ledig</td>
<td>MPOS-arbejdsrutineoptager understøtter følgende funktioner:
<ul>
<li>Oprette opgaveoptagelser til forskellige opgaver, der udføres i MPOS.</li>
<li>Oprette et dokument, der indeholder trin og skærmbilleder, og knytte det til en node i forretningsprocesmodellen.</li>
</ul></td>
<td>Partnere og uafhængige softwareleverandører (ISV'er) kan tilpasse MPOS og levere dokumentation til træning af deres brugere.</td>
</tr>
</tbody>
</table>

### <a name="extensibility"></a>Udvidelsesmuligheder

<table>






<tbody>
<tr class="odd">
<td><strong>Hvad kan du gøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er det vigtigt?</strong></td>
</tr>
<tr class="even">
<td>Understøtte en let installerbare Retail-komponenter, som kan udvides, på tværs af Hovedkvarter, Callcenter, e-handel og POS.</td>
<td>Komponenterne kan udvides ved hjælp af Retail SDK. Ingen paknings- og distributionsfunktioner understøttes.</td>
<td>Udvidelsesmuligheds-hooks er forbedret på tværs af de forskellige komponenter, så de giver bedre understøttelse af kodeisolering og servicevenlighed. Her er nogle af de funktioner, der anvendes:
<ul>
<li>Arbejdsgang, aktivitet og drift.</li>
<li>Før og efter-udløsere, så du kan nemt udvide en arbejdsproces.</li>
<li>Anvendelses- og driftsudløsere.</li>
</ul>
Derudover findes der en ramme, der gør det muligt for dig at opbygge og pakke disse komponenter ved hjælp af MSBuild og derefter installere din tilpasning gennem Microsoft Dynamics Lifecycle Services (LCS) uden problemer.</td>
<td>Detailhandlere har meget specifikke krav, der er baseret på vertikaler og geografisk placering af operationer. Ved at tilbyde en platform med nemme udvidelsesmuligheder muliggør vi forbrug på tværs af vertikaler og markeder. Da Retail har en meget distribueret arkitektur, forbedrer også muligheden for at installere uden problemer produktiviteten betydeligt.</td>
</tr>
</tbody>
</table>

### <a name="lifecycle-management"></a>Styring af livscyklus

Lifecycle Services (LCS) indeholder en række tjenester, som kunder og partnere kan bruge til at administrere systemets livscyklus fra tilmelding til daglige operationer.

<table>






<tbody>
<tr class="odd">
<td><strong>Hvad kan du gøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er det vigtigt?</strong></td>
</tr>
<tr class="even">
<td>Administrere programmet automatisk via skyimplementeringstjenester.</td>
<td>Ikke ledig</td>
<td>Du kan installere følgende topologier til skyen:
<ul>
<li>Retail-prøvetopologi med én boks.</li>
<li>Retail-multibox-topologi for høj tilgængelighed.</li>
<li>Udviklertopologi med Retail SDK.</li>
</ul>
Der er en forbedret "low-touch"-klientkomponentinstallation via selvbetjeningsinstallation:
<ul>
<li>Retail Modern POS.</li>
<li>Retail Hardware Station.</li>
<li>Understøttelse af overførsel og distribution af brugerdefinerede pakker via selvbetjeningsinstallation.</li>
</ul></td>
<td>Skyinstallationstjenester giver følgende fordele:
<ul>
<li>Væsentligt reduceret implementeringsindsats og -kompleksitet for Retail HQ-komponenter.</li>
<li>Oprindelig installation til Microsoft Azure offentlig sky.</li>
<li>Forbedret selvbetjeningsinstallationen af komponenter i butikken for at gøre konfiguration lettere og mere intuitiv</li>
</ul></td>
</tr>
<tr class="odd">
<td>Overvåge systemets tilstand og diagnosticere problemer og fejl.</td>
<td>Denne funktion kræver <a href="http://www.microsoft.com/en-us/download/details.aspx?id=42636">System Center 2012 Management Pack til Microsoft Dynamics AX 2012 R3 CU8 Retail</a>.</td>
<td>Overvågning og diagnosticering for Retail-komponenter er nu tilgængelig via den <strong>Driftsindsigt</strong> dashboardet i LCS.</td>
<td>Dashboardet <strong>Driftsindsigt</strong> er en skybaseret overvågningsportal, som erstatter behovet for at installere SCOM-infrastruktur (System Center Operations Manager).</td>
</tr>
<tr class="even">
<td>Oprette, konfigurere, hente og installere Retail Hardware Station og enheder via selvbetjening.</td>
<td>Ved hjælp af installationspakke og Enterprise Portal kan en bruger udføre en automatiseret installation og konfiguration af alle komponenter, der kræves på en bestemt computer, der er baseret på en defineret topologi.</td>
<td>Fordi der er kun to installationspakker, én for MPOS-klient og den anden for komponenten Retail Hardware Station, har selvbetjening reduceret mængden af arbejde, der skal udføres på alle niveauer til installation af disse klientkomponenter.</td>
<td>Selvbetjening tager sigte på at minimere krav og gøre det lettere for brugeren at udføre en installation.</td>
</tr>
</tbody>
</table>

## <a name="sales"></a>Salg
<table>






<tbody>
<tr class="odd">
<td><strong>Hvad kan du gøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er det vigtigt?</strong></td>
</tr>
<tr class="even">
<td>Få et hurtigt overblik over leveringsalternativer, når du lover ordrer til kunder.</td>
<td>Når der er begrænsninger af tilgængeligheden af produktet, og kundens ønskede leveringsdato for et eller flere produkter på ordren ikke kan imødekommes, bliver ordretilsagnsopgaven en udfordring. For at finde alternativer, der kan opveje problemer med tilgængelighed og leveringstid, så kundens ønskede modtagelsesdato kan opfyldes, eller for at tilbyde kunderne en leveringsløsning, som de kan acceptere og har tillid til, skal ordrebehandleren muligvis åbne flere formularer, som hver især kun indeholder et undersæt af de nødvendige oplysninger. Mere specifikt viser én formular disponibel lagerbeholdning på tværs af steder, en anden viser disponibel lagerbeholdning i den interne indstilling, en tredje gør det muligt for brugerne at beregne den tidligste tilgængelige dato for ét sted eller variant ad gangen og en fjerde viser forsyningsordrer. Derfor kan brugerne ikke føle sig trygge ved, at de har overvejet alle de relevante indstillinger i stedet for blot at vælge en umiddelbar, men ikke-optimal løsning. Brugere føler sig heller ikke effektive, fordi mange afbrydelser opstår under ordretilsagnsstrømmen, når de åbner og lukker flere sider og kombinerer viden og muligheder.</td>
<td>Baseret på de eksisterende algoritmer til beregning af dato for levering, giver siden <strong>Leveringsalternativer </strong>en ny brugeroplevelse for ordretilsagn:
<ul>
<li>Den samler relevante oplysninger fra flere formularer på ét sted.</li>
<li>Den tilbyder "færdige" alternative leveringspakker, f.eks. en kombination af lokation/lagersted/variant/transport-tilstand, baseret på det hurtigste leveringskriterie (tidligste tilgængelige dato), som brugeren kan vælge.</li>
<li>Brugeren kan vælge indstillinger fra simuleringsgrænsefladen og overføre dem til salgsordrelinjen.</li>
</ul></td>
<td>Virksomheder, der aspirer til at levere høj kundeservice og samtidig en strategi for lageroptimering, skal kunne garantere levering af ordrer pålideligt og konkurrencedygtigt. For grundlæggende kræver deres kunders egen virksomhed, at produkter er tilgængelig til tiden. Opgavesiden <strong>Leveringsalternativer</strong> gør ordretilsagnsopgaven hurtigere, nemmere og mere systematisk ved at identificere og anbefale de bedste alternative ordreleveringsdatoer på ét interaktivt sted.</td>
</tr>
</tbody>
</table>

## <a name="service-management"></a>Servicestyring
Der er ikke blevet tilføjet nye funktioner.

## <a name="transportation-management"></a>Transportstyring
Der er ikke blevet tilføjet nye funktioner.

## <a name="travel-and-expense"></a>Rejser og udgifter
Der er ikke blevet tilføjet nye funktioner.

## <a name="warehouse-management"></a>Lagerstedsstyring
|                                                                       |                                                                                                                                                                                                              |                                                                                                                                                               |                                                                                                                                                                                      |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hvad kan du gøre?**                                                  | **Dynamics AX 2012**                                                                                                                                                                                         | **Dynamics AX 7.0**                                                                                                                                           | **Hvorfor er det vigtigt?**                                                                                                                                                           |
| Downloade, installere og konfigurere Warehouse Mobile Devices-portal. | Du kan hente, installere og konfigurere portalen under Microsoft Dynamics AX-installationsprocessen via en standardopsætning. Den er udviklet til selvstændig installation og konfiguration i det lokale miljø. | Du kan hente et separat installationsprogram via et menupunkt i Lagerstedsstyring. Den er udviklet til selvstændig installation og konfiguration i det lokale miljø. | Når du konfigurerer mobilenhedsfunktionen, skal du installere og konfigurere Warehouse Mobile Devices Portal lokalt og oprette forbindelse til Dynamics AX i skyen. |



<a name="see-also"></a>Se også
--------

[Nyheder eller ændret](whats-new-changed.md)

[Nye opgaveguider er tilgængelige (februar 2016)](new-task-guides-available-february-2016.md)




