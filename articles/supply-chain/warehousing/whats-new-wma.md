---
title: Nyheder eller ændringer i Warehouse Management-mobilappen
description: Denne artikel viser de nye og ændrede funktioner for hver frigivet version af Warehouse Management-mobilappen til Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 04/25/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61d3ebc85d3c3d20bb17acd7364adc04cd2f3f94
ms.sourcegitcommit: e9000d0716f7fa45175b03477c533a9df2bfe96d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/13/2022
ms.locfileid: "9843674"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a>Nyheder eller ændringer i Warehouse Management-mobilappen

[!include [banner](../includes/banner.md)]

Denne artikel viser de nye funktioner, rettelser, forbedringer og kendte problemer for hver frigivet version af Warehouse Management-mobilappen til Microsoft Dynamics 365 Supply Chain Management.

## <a name="version-20390"></a>Version 2.0.39.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.
- Øget stabilitet. 
- Felterne på den **brugerdefinerede** side sorteres ikke længere automatisk ud fra indstillingerne for prioritet og underprioritet.  
- Appen bruger nu indstillingerne for prioritet og underprioritet for hvert felt til at identificere det primære felt for en side. Det primære felt vises i trinhovedet. 
- Har løst et problem, hvor det blød tastatur ikke kan skjules på Android.
- Fast en afgang, hvor antalsnøglen viste en forkert korrekt værdi ved åbning i *bevægelsesflowet*. 
- Fastlagde et problem, hvor værdien for skrivebeskyttet antal ikke er rettet korrekt. 
- Fastlagde et problem, hvor websider ikke åbnes fra siden **Om**. 
- *Auto-farvetemaet* har nu standardudseende (lys eller mørke) baseret på det globale tema, der er angivet i operativsystemet for den mobile enhed.

## <a name="version-20370"></a>Version 2.0.37.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.
- Tilføjede en brugerindstilling, som giver arbejderne mulighed for at vælge, hvor appen skal vise produktskærme (i både kort og trinhoveder, kun i trinhoveder eller slet ikke). 
- Forbedret skærmlayout for detaljer ved at reducere størrelsen på trin-banner og antalsinputudbyder, hvilket giver mere plads til andet indhold. 
- Forbedret brugergrænsefladen, når der køres på en Honeywell Thor-enhed. 
- Forbedret tilstand med fuld skærm (gælder kun for enheder med hardwaretastatur). 
- Forbedret resultater, når du sorterer oplysninger om kort og brugerdefinerede sider efter prioritet eller underprioritet (DataPriority eller DisplaySubPriority). 
- Der er tilføjet understøttelse af flere sprog. 
- Forbedret stabilitet. 
- Forbedret flere billeder og ikoner. 

## <a name="version-20350"></a>Version 2.0.35.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.
- Løste et problem på Android, hvor programmet ville gå ned, hvis **Opgaveliste**-siden blev åbnet, når der ikke skulle vises kort.

## <a name="version-20340"></a>Version 2.0.34.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.
- Forbedret stabilitet.
- Forbedret ydeevne.
- Forbedret skærmlayoutet, så der er mere plads til detaljekortet.
- Har føjet en søgefunktion til siden **Opgaveliste**. Arbejderne kan nu scanne eller skrive for at søge i alle felter og titler på siden.
- Listen over tilgængelige forbindelser er nu sorteret alfabetisk.
- Har løst et problem, hvor der blev vist dubletter af kort for varer, der har flere lagerstatusser på samme lokation.
- Løste et problem, hvor siden med den **store valgliste** ikke rullede for at vise det valgte element.
- Rettede farverne på søgelinjen på siden med **stor valgliste**.
- Der er løst et problem, hvor den standardknap, der er defineret i XML-koden, ikke bruges som knappen Send.
- Der blev løst et problem, hvor knapperne i multiscanning- og hurtigvalideringsflowene ikke blev opdateret, når nye id'er blev scannet.
- Der er tilføjet understøttelse af flere sprog.

## <a name="version-20320"></a>Version 2.0.32.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Forbedret stabilitet.

## <a name="version-20310"></a>Version 2.0.31.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

-   Forbedret ydeevne og stabilitet.
-   Forbedret brugergrænseflade, der gør det hurtigere og nemmere at arbejde med lange valglister. Arbejderne kan nu søge efter et listeelement ud fra navnet i stedet for at rulle gennem den fulde liste.
-   Løst et problem, hvor foruddefinerede værdier ikke blev overskrevet, da de blev scannet efter tegn.

## <a name="version-20300"></a>Version 2.0.30.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Forbedret stabilitet.

## <a name="version-20280"></a>Version 2.0.28.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Forbedret stabilitet.
- Introducerede muligheden for at fortsætte scanningen, også selvom der vises en fejldialogboks på skærmen.
- Understøttede ASCII 10 i stregkoder.
- Forbedret anvendeligheden af trininstruktionsdialogbokse.
- Fast et problem, hvor der nogle gange kan vises et tomt skærmbillede.
- Løste et problem, hvor opgavelister ikke rulles korrekt, når der køres på Microsoft Windows.

## <a name="version-20250"></a>Version 2.0.25.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Forbedret ydeevne.
- Øget stabilitet.
- Forbedret **Forespørgsel**-side, så den understøtter længere tekster i underoverskrifter.
- Introduceret muligheden for straks at annullere et flow med et enkelt tryk eller klik (når **Annuller** er den eneste handling, der er tilgængelig under **Flere handlinger**).
- Løst et problem, hvor fokus nogle gange kan gå tabt mellem kontrolelementer for indtastning på siden **Rediger forbindelse** og brugerdefinerede sider.
- Løst et problem, hvor knapper nogle gange kan blive inaktive og stadig vises som valgt, når de medtages i rullevisningen.
- Løst et problem, hvor det forkerte layout nogle gange kunne bruges på hovedsiden.

## <a name="version-20240"></a>Version 2.0.24.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Forbedret scannersider for at aktivere scanningsindstillingen på **detaljesider**.
- Forbedret ydeevne, f.eks. touch-/trykskærm.
- Forbedret ydeevne i forbindelse med Android.
- Fast placering af flere overskrifter, så der kan vises flere kort på **forespørgselssiden**.
- Forbedret rulning, så der er mindre afstand til siderulleinddeling.
- Tilføjet lang tryk for at få vist yderligere tekst på **forespørgselssiden**.
- Fast manglende oplysninger om enheds-id til Android.
- Øget stabilitet.
- Optimeret layout for logon.
- Tilføjet højreklik for at lukke dialogboksens pop op-sider på numeriske tastatur, **detaljeside** og inputsider.

## <a name="version-20220"></a>Version 2.0.22.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Har løst flere problemer med nedbrud.
- Løst et problem, hvor nogle tegn ikke genkendes, når der scannes eller skrives på standardsiden.
- Fast et problem, hvor du kan skrive et backspace på standardsiden, sletter to tegn ad gangen.
- Fast et problem, hvor feltet **Sorter efter** på **opgavelistesiden** vil vise en forkert værdi, der ikke svarer til den faktiske sorteringsrækkefølge af kortene.
- har ordnet et problem, hvor der vises et forkert layout, efter at appvinduet er blevet omdannet, mens du kører på Microsoft Windows.
- Løst et problem, hvor du kan rulle i en pop op-liste, kan resultere i, at nogle listeelementer forbliver skjulte eller bliver gemte.
- Ændret logonsiden, så den viser felterne for brugernavn og adgangskode på samme side, når de kører på større visninger.
- Forbedret den måde, kontrollerne reagerer på for hurtigt at kunne arbejde hurtigere.
- Tilføjede en fejllogvisning i appen.
- Yderligere flere forbedringer af handicapfunktioner (forbedret ydeevne, faste manglende pladsholdere på Android, aktiveret tastaturinput til kontrolelementer med mere).

## <a name="version-20200"></a>Version 2.0.20.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Har løst flere problemer med nedbrud.
- Har løst et problem, hvor forkerte værdier vises på kort på siden **Arbejdsliste**.
- Forbedret rulleoplevelsen og elimineret uregelmæssig rulning på siderne **Opgaveliste** og **Vareforespørgsel** i Android.
- Har tilføjet en afslutningsknap på logonsiden, som afslutter programmet.

## <a name="version-20190"></a>Version 2.0.19.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Har forbedret det generiske dataforespørgselsflow.
- Har forbedret problemet med uregelmæssigheder på siderne **Arbejdsliste** og **Vareforespørgsel**.
- Reduceret batteriforbrug.
- Fjernede grænsen i antallet af felter til arbejdskort.
- Justeret højden på arbejdskort, så de alle har samme størrelse, uanset antallet af felter i hvert kort.
- Løst et problem, hvor mellemrum i stregkoder blev fjernet.
- Tilføjet indstillingen **Knaptypografi**, som giver dig mulighed for at skifte mellem visning af knapper og visning af skyder på alle typer enheder.
- Har løst forskellige problemer, der kunne få appen til at gå ned.
- Fokuserer automatisk på det første tekstfelt på brugerdefinerede sider.
- Forbedringer af tilgængelighedsfunktioner i forbindelse med lysstyrke, kontrast, fortælling og manglende pladsholdertekster.

## <a name="version-20170"></a>Version 2.0.17.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Har løst et problem, hvor stregkoderne scannes forkert.
- Har løst problem med GS1-scanningen til kamerascanneren.
- Har løst problemet med GS1-scanningen for stregkodescanneren på Zebra-enheder.
- Har forbedret omvejsflowet for forespørgsler, så valg af et kort i en omvej nu returnerer til hovedflowet.
- Tilføjet understøttelse af et generisk dataforespørgselsflow.
- Har tilføjet en meddelelse, der giver brugerne besked om ændringer i netværksforbindelsers status.
- Justerede lagertilladelser med politikken for beskyttelse af personlige oplysninger for lagring i Android 10.
- I forbindelse med flow, der har brug for det, inkluderer antalshjulet nu en position, der giver brugerne mulighed for at sende en tom numerisk værdi.
- Har løst problemer med retningen af antalshjulet.
- Har løst et problem, hvor antalshjulet ville springe til den forkerte værdi.
- Har løst et problem, hvor input til den primære side ville gå tabt, når den blev udfyldt fra detaljesiden.
- Har løst et problem, hvor pladsholdertekst behandles som den først valgte værdi på valglister.
- Knappen "Send" ved bekræftelsestrin er nu automatisk aktiveret, hvis der er foruddefinerede værdier.
- Har rettet detaljekortet, så der vises så mange linjer som muligt for tekstfelter med flere linjer.
- Har rettet højden af knapperne "Send" og "Flere handlinger", så de nu optager mindre plads på skærmen.
- Tilføjede manglende titler på valglisten.
- Har løst et problem, hvor knappen Tilbage ikke virkede.
- Har tilføjet flere rettelser og forbedringer af tastaturnavigation, herunder på følgende sider:
  - Brugerlogon
  - Vælg forbindelse
  - Rediger forbindelse
- Har rettet rulning ved brug af tastaturnavigation.
- Forbedret tilgængelighed, herunder følgende forbedringer:
  - Har rettet synlighed og kontrast.
  - Har forhindret tab af tastaturfokusering, når pop op-sider lukkes.
  - Der er føjet fejlmeddelelser til fortællingen.
  - Forøgede størrelsen på pladsholderværdierne i trinbanneret.
- Har rettet eksemplet på den tilpassede ældre side i demotilstand.

## <a name="version-20150"></a>Version 2.0.15.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Forbedret ydeevne ved at rette problemer med hukommelsen.
- Har løst et problem, hvor nogle feltværdier ikke opdateres korrekt, når de er valgt på detaljesiden.

## <a name="version-20140"></a>Version 2.0.14.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Har løst et problem, der deaktiverede standardknappen Send.

## <a name="version-20130"></a>Version 2.0.13.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Forbedret rulning mellem sider med blødere animation.
- Har rettet tællerintuitiv respons på strygebevægelser og lejlighedsvise skærmfrysninger.
- Forbedret kombinationer af tekst i mørketilstand og baggrundsfarve, så de bliver mere læsbare.
- Har løst et problem, hvor teksten kunne blive meget lille, når appvinduets størrelse ændredes.
- Har løst et problem, der kunne få appen til at gå ned, når der blev scannet stregkoder.
- Tilføjet mulighed for at erstatte en skyder med en knap.
- Har løst et problem, der kunne få appen til at vise fejlmeddelelsen "AADSTS7000215: Ugyldig klienthemmelighed er angivet."
- Har rettet tipanimationen, der viser, hvordan du lukker en side ved at stryge nedad.
- Tilføjede muligheden for at lukke en side ved at svippe nedad.
- Har løst et problem, hvor rullelistetitlerne ikke blev vist på siden **Brugerindstillinger**.
- Har løst et lokaliseringsproblem, hvor appen ikke kunne anerkende et komma (,) som decimalseparator.
- Forbedret tilgængelighed.
- Har rettet navigering på siden **Ny forbindelse** for at gøre tilgængeligheden bedre.
- Har løst et problem, hvor tastaturet på skærmen ikke blev vist ved valg af et inputfelt.
- Har løst et problem, der kunne få appen til at gå ned, hvis brugerne hurtigt ændrede størrelsen på vinduet.
- Har løst et problem, hvor et hurtigt tastetryk nogle gange blev fortolket som et langt tryk.
- Har løst et problem, hvor applayoutet kunne blive ødelagt på grund af felttilpasninger, der blev foretaget i Supply Chain Management.
- Har løst et problem, hvor varelokationerne ikke blev vist korrekt.
- Har løst et problem vedrørende kort pluk i arbejdsgangen for produktvarianter.
- Har fjernet den unødvendige validering af felter, der indeholder foruddefinerede standardværdier.
- Forbedret ydeevne.
- Har tilføjet en ny indstilling, der giver brugerne mulighed for at vælge, hvordan felter skal filtreres og sorteres på kortsiden.

## <a name="version-20110"></a>Version 2.0.11.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Tilføjet understøttelse af hævede felter.
- Tilføjet understøttelse af navigation på hardwaretastaturet.
- Forbedret tilgængelighed.
- Forbedrede detaljekort.
- Forbedrede omveje til trin i menupunkter.
- Mindre forbedringer af brugergrænsefladen.
- Har løst et problem, der kunne medføre, at appen gik ned, når der blev scannet stregkoder.
- Har løst forskellige problemer, der kunne forårsage, at systemet ikke længere svarede.

## <a name="version-20100"></a>Version 2.0.10.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Tilføjet animation, når du stryger gennem lister og sider.
- Teksten ombrydes nu korrekt på forbindelsens fejlside.
- Kombinationsfelter uden standardværdier vises nu korrekt.
- Oplysninger i underhovedet vises nu kun på siden med fulde detaljer.
- Tomme inputfelter vises ikke længere på detaljekortet.
- Bekræftelsesværdier dubleres ikke længere på detaljekortet.
- Har løst forskellige problemer, der forårsagede, at systemet ikke længere svarede.

## <a name="version-2090"></a>Version 2.0.9.0

Denne version løser en fejl, hvor appen ikke længere kan reagere, hvis brugere går opad fra toppen af en liste.

## <a name="version-2080"></a>Version 2.0.8.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Tilføjet understøttelse af [funktionen med trininstruktioner](mobile-app-titles-instructions.md), der blev introduceret i Supply Chain Management version 10.0.21.
- Tilføjet tipanimation for at vise brugere, at de kan lukke overlejringer ved at swipe nedad.
- Tilføjet understøttelse af funktionstaster på handlingslister og menuer. Brugerne kan holde enhver funktionstast nede i tre sekunder for at få vist en oversigt over tilgængelige kommandoer.
- Løst en fejl, der medførte, at følgende fejlmeddelelse blev vist på visse enheder: "Der kan ikke findes en egnet visning til den angivne størrelse".
- Løst en fejl, hvor fuld skærm-tilstand ikke altid fungerer, når skærmtastaturet bruges.
- Løst en fejl, hvor sideswiping ikke fungerer på Windows-enheder.
- Har løst forskellige problemer, der forårsagede, at systemet ikke længere svarede.

## <a name="version-2070"></a>Version 2.0.7.0

### <a name="new-features-fixes-and-improvements-in-version-2070"></a>Nye funktioner, rettelser og forbedringer i version 2.0.7.0

- Har føjet et afsnit til siden **Om**, hvor den seneste version af appen er kontrolleret.
- Har gjort det nemmere svippe og stryge gennem sider.
- Har ændret ikonet for knappen stigende/faldende på opgavelisten.
- Har reduceret margenerne på **Detalje**-kortet, så der er plads til flere oplysninger.
- Har anvendt forskellige forbedringer af ydeevnen for at reducere problemer med, at appen bliver langsommere med tiden.
- Hvis der er flere kontrolelementer, end de kan være på skærmen, hvilket medfører sideskift, ruller drejekontrolelementet ikke længere samme vej som siden.
- Har prioriteret at vise den senest scannede værdi frem for visning af opgavens titel, så hvis de overlapper, afkortes opgavens titel.
- Har løst forskellige problemer, der forårsagede, at systemet ikke længere svarede.
- Tekst forskellige steder afskæres ikke længere på visse sprog.
- Appen kører nu som standard i fuld skærm.
- Har løst et problem, der fra tid til anden ville medføre, at scanninger blev ignoreret på hovedsiden med bestemte enheder.

### <a name="known-issues-in-version-2070"></a>Kendte problemer i version 2.0.7.0

- På visse enheder vises følgende fejlmeddelelse, når du starter appen eller påbegynder en opgave: "Der kan ikke findes en passende visning til den angivne størrelse". Hvis du får vist denne fejlmeddelelse på nogen af dine enheder, skal du nedgradere mobilappen Warehouse Management til version 2.0.6.0 på den pågældende enhed og vente med at opgradere, indtil næste version af appen frigives.

## <a name="version-2060"></a>Version 2.0.6.0

### <a name="new-features-fixes-and-improvements-in-version-2060"></a>Nye funktioner, rettelser og forbedringer i version 2.0.6.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- I demotilstand vises nu alle etiketter på enhedssproget.
- Det er mindre sandsynligt, at du får følgende fejlmeddelelse: "Der kan ikke findes en passende visning til den angivne størrelse".
- Minimumshøjden for arbejdskort er øget (i tilfælde hvor tre eller færre felter konfigureres til at blive vist på opgavelisten).
- Margener (udtoning) nederst i detaljekort er blevet forbedret.
- Ugyldige symboler i XML-filer, der udveksles med serveren, håndteres nu korrekt. (Tegn, der ikke kan udskrives, håndteres for eksempel nu igen korrekt og medfører ikke længere, at appen holder op med at svare).
- HTTP-fejl (for eksempel "fejl 503"), når der sendes en serveranmodning, håndteres nu korrekt.
- Mens der vises en fejl, vises indstillingslisten ikke længere automatisk for kontrolelementer af typen kombinationsboks.
- Appen holder ikke længere op med at svare på grund af den visningsretning, der er valgt i brugerindstillingerne.
- Produktbilleder vises nu i selvbetjeningsmiljøer. (Denne ændring gælder kun for versioner med lav opløsning. Filstyringstjenesten understøtter ikke billeder i fuld størrelse i selvbetjeningsmiljøer).
- En fejl, der involverede korte pluk med nul antal, er blevet løst.
- Appen holder ikke længere op med at svare, når et detaljekort viser flere identiske felter.

### <a name="known-issues-in-version-2060"></a>Kendte problemer i version 2.0.6.0

Der findes følgende kendte problemer i denne version:

- Appen (især opgavelisten) bliver langsommere over tid.
- **Windows-version:** Når en USB-drev bruges til scanning i Windows, medfører uoverensstemmende resultater, at scannede symboler blandes sammen.

## <a name="version-2050"></a>Version 2.0.5.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Klienthemmeligheden skjules ikke længere i opsætningen af forbindelsesindstillinger.
- Du kan nu trykke længe på enhver tekst for at se den i fuld længde.
- Fejlmeddelelsen, når der mangler lagertilladelser, er blevet forbedret.
- Der er tilføjet nye kontrolsekvenser for nogle flow.
- Knappen Send bliver ikke længere tilgængelig på grund af størrelsesvinduet.
- Skydere kan nu fortsætte på mindre skærme, når der bruges store knapstørrelser.
- Overlejringen med fire knapper kan ikke længere afskæres.
- Nu understøttes knappen Delete på tastaturet.
- Et problem med lysstyrke, der kan forekomme, når der trykkes på tastaturet, er løst.
- Der er løst forskellige problemer med demodata.
- Et problem, der havde indflydelse på numeriske felter på detaljesiden, er blevet løst.
- Skærmtastaturet forsvinder ikke længere fra tid til anden på nogle enheder.
- Flere forskellige problemer med brugergrænsefladen, for eksempel fejl, der havde indflydelse på baggrundsfarven og positionen, er løst.
- Den russiske brugergrænseflade er blevet forbedret.
- Forskellige problemer, der forårsagede, at systemet ikke længere svarede, er blevet løst.
- Et problem, der var relateret til genåbningen af regnemaskinen, er blevet løst.
- **Android-version:** Der er løst et problem, hvor Android 4.4 holdt op med at svare ved start.
- **Android-version:** Minimumskalering er reduceret til 50 procent.

## <a name="version-2040"></a>Version 2.0.4.0

Version 2.0.4.0 var den første generelt tilgængelige version af Warehouse Management-mobilappen.

### <a name="new-features-fixes-and-improvements-in-version-2040"></a>Nye funktioner, rettelser og forbedringer i version 2.0.4.0

Denne version indeholder følgende nye funktioner, rettelser og forbedringer, som ikke var tilgængelige i forhåndsversionen:

- Hvis et detaljekort indeholder to etiketter, der har identiske data, skjules den ene af etiketterne.
- Specialtegn vises nu som standard, og muligheden for at skjule dem er blevet fjernet fra brugerindstillingerne.
- Deaktiverede send-knapper vises nu som ikke-tilgængelige i håndholdt visning.
- En ændring i sekvenslogikken for kontroller sikrer en mere problemfri skalering på tværs af enheder. Der er derfor mindre behov for at justere skaleringen af skrifttyper eller knapper.
- Standardfarvetemaet er ændret til *Mørk*.
- Det manglende ikon for den deaktiverede send-knap er blevet tilføjet på båndet.
- Timeoutundtagelser åbner nu forbindelsessiden i stedet for at vise en linjefejl.
- Hvis der ikke er en tilgængelig send-handling (for eksempel **OK**, **Ja**, **Accepter**, **Udført** eller **Udført**), deaktiveres knappen Send.
- Appens stabilitet er blevet forbedret.
- Der findes en rettelse til sikkerhedsrisikoen [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).
- **Windows-version:** Et problem i Windows, hvor menuerne ikke reagerede, efter at størrelsen på vinduet var blevet ændret, er blevet løst.

### <a name="known-issue-in-version-2040"></a>Kendt problem i version 2.0.4.0

Der findes følgende kendte problem i denne version:

- Denne version har et problem med enheder, der bruger Android 4.4. Du kan opleve problemer, når du bruger appen på denne version af Android.
