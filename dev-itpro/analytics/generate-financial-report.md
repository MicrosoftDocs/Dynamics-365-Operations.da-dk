---
title: "Generér en økonomisk rapport"
description: "Dette emne indeholder oplysninger om generering af en økonomisk rapport."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9b0d8fd9f5ae9d99f299cc71d7caef021ad3fb9d
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017

---

# <a name="generate-a-financial-report"></a>Generér en økonomisk rapport

[!include[banner](../includes/banner.md)]


Dette emne indeholder oplysninger om generering af en økonomisk rapport. 

Åbn den ønskede rapportdefinition for at generere en rapport, og klik derefter på knappen Generer på værktøjslinjen. Vinduet Status for rapportkø åbnes og angiver placeringen af rapporten i køen. Den genererede rapport åbnes som standard i Web Viewer.
| ![Bemærk](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Bemærk")**Bemærk**        |
|------------------------------------------------------------------------------------------------|
| Du kan kun generere rapporter til mapper og placeringer, som du har tilladelse til at åbne. |

I følgende tabel beskrives de indstillinger, der er tilgængelige for generering af rapporter.

| Indstilling                                                                                | Hvis du vil have flere oplysninger |
|---------------------------------------------------------------------------------------|----------------------|
| Angive en tidsplan for automatisk at generere en rapport eller en gruppe af rapporter              |                      |
| Søge efter manglende konti eller data i en rapport og validere nøjagtigheden af en rapport |                      |

Når du genererer en rapport, bruges de indstillinger, du har angivet under fanen Rapportdefinition . Under fanen Output og distribution kan du angive en placering for et rapportbibliotek, så du nemt kan dele rapporten.

## <a name="schedule-report-generation"></a>Planlæg rapportgenerering
Mange virksomheder har et grundlæggende sæt af rapporter, der køres med planlagte intervaller, så de justeres med deres virksomhedsprocesser. Du kan planlægge en rapport, der skal genereres regelmæssigt, f.eks. dagligt, ugentligt, månedligt eller årligt. Det kan være en enkelt rapport eller en gruppe af rapporter, der indeholder flere firmaer. Du skal angive dine legitimationsoplysninger for hver af de selskaber, der er angivet, f.eks. dem i en definition af et rapporteringstræ. Hvis legitimationsoplysningerne ikke er gyldige, viser rapporten kun de oplysninger, du har adgang til, f.eks. den virksomhed, som du er logget på, på tidspunktet. Outputoplysninger læses først fra rapportgruppen og derefter fra de enkelte rapporter.

Efterhånden som rapporttidsplaner oprettes og gemmes, vises de i navigationsruden under Rapporttidsplaner. Du kan oprette mapper for at organisere rapporterne. Hvis en enkelt rapport i en tidsplan ikke kører, fortsætter alle andre rapporter med at køre.
| ![Vigtigt](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Vigtigt")**Vigtigt**                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Du skal have rollen som designer eller administrator for at oprette, redigere eller slette rapporttidsplaner. Når du kører en rapport, bruges legitimationsoplysningerne for den bruger, der oprettede tidsplanen, til at generere rapporten. |

### <a name="create-a-report-schedule"></a>Opret en ny rapporttidsplan

1.  I Report Designer skal du klikke på Ny i menuen Filer, og derefter skal du vælge Rapporttidsplan. Dialogboksen Ny rapporttidsplan åbnes.
2.  Under Indstillinger for skal du vælge en enkelt rapport eller en rapportgruppe for at planlægge. Kun rapporter og rapportgrupper for det firma eller en dokumentkomponent, du aktuelt er logget på, er tilgængelige.
3.  Vælg afkrydsningsfeltet Aktiv for at aktivere rapporttidsplanen. Kun forfatteren af rapporten eller en administrator kan aktivere eller deaktivere en rapporttidsplan.
4.  Klik på knappen Tilladelser for at angive firmaets legitimationsoplysninger. Logonoplysningerne bruges som standard for det firma, du er logget på. Hvis andre firmaer er inkluderet, f.eks som i definitioner af rapporteringstræ, skal du vælge Brug separate legitimationsoplysninger og derefter angiv legitimationsoplysningerne for andre virksomheder, der indgår i rapporttidsplanen. Du kan vælge Windows-godkendelse eller skrive et brugernavn og en adgangskode for hver virksomhed. Vælg afkrydsningsfeltet Gem legitimationsoplysninger for at gemme legitimationsoplysningerne for disse firmaer. Klik derefter på OK for at lukke dialogboksen.
5.  Under Frekvensi feltet Start gentagelse skal du vælge den dato, hvor tidsplanen skal starte. Som standard vælges den aktuelle systemdato på klientcomputeren.
6.  I feltet Kør rapport på skal du vælge det tidspunkt, hvor rapporten skal køres. Hvis du angiver et klokkeslæt, der ligger før det aktuelle systemklokkeslæt, kører rapporten på den næste planlagte dato.
7.  I området Gentagelsesmønster skal du angive, hvor ofte rapporten køres. Som standard vælges Dagligt med en Interval-værdi (dage) på 1. Andre muligheder omfatter Ugentligt, Månedligt og Årligt.
8.  I området Gentagelsesperiode skal du vælge, om rapporten skal stoppe med at genereres.
    -   Slutdato mangler – Rapporttidsplanen kører på ubestemt tid.
    -   Angiv antallet af forekomster – Rapporttidsplanen kører det angivne antal gange og er derefter deaktiveret.
    -   Slut den – Rapporttidsplanen slutter på den angivne dato.

9.  Klik på Gem på værktøjslinjen. I dialogboksen Gem som skal du angive et unikt navn på og en beskrivelse af rapporttidsplanen.

Du skal have rollen som designer eller administrator for at kopiere en rapporttidsplan. Selvom en administrator ændrer rapporttidsplanen, beholder rapporten legitimationsoplysningerne for den bruger, der oprettede rapporten.
### <a name="copy-a-report-schedule"></a>Kopiér en rapporttidsplan

1.  Klik på Rapporttidsplaner i navigationsruden Report Designer, og åbn en rapporttidsplan, der skal kopieres.
2.  I menuen Filer skal du klikke på Gem som og derefter indtaste et nyt navn og beskrivelse af tidsplanen i dialogboksen Gem som. Klik på OK, og den nye tidsplan vises i navigationsruden.
3.  Ændr felter og oplysninger efter behov i den nye tidsplan, og klik derefter på Gem på værktøjslinjen, eller klik på Gem i menuen Filer.

Hvis du vil slette en rapporttidsplan, skal du være ejer af rapporttidsplanen eller have en rolle som administrator.
### <a name="delete-a-report-schedule"></a>Slet en rapporttidsplan

1.  Klik på Rapporttidsplaner i navigationsruden i Report Designer.
2.  Vælg rapporttidsplanen, du vil slette, og klik derefter på Slet, eller tryk på tasten Delete.
3.  I dialogboksen til bekræftelse af sletning skal du klikke på Ja for permanent at slette rapporttidsplanen. Hvis du ikke har tilladelse til at slette tidsplanen, vises en meddelelse, og rapporten slettes ikke.

### <a name="credentials-and-report-schedules"></a>Legitimationsoplysninger og rapporttidsplaner

Hvis du ikke angiver legitimationsoplysninger, der kræves for alle selskaber, der indgår i rapporterne, modtager du følgende meddelelse, når du gemmer rapporttidsplanen: "Du skal angive dine legitimationsoplysninger for de selskaber, der er indeholdt i denne rapporttidsplan. Markér knappen Tilladelser for at indtaste dine legitimationsoplysninger."

Phyllis logger f.eks. på Company A med sit logon og adgangskode. Hun opretter en tidsplan for en rapport, der bruger en definition for et rapporteringstræ, for at indsamle data fra flere firmaer. Når denne rapporttidsplan er gemt, bliver Phyllis bedt om at angive legitimationsoplysninger for de selskaber, der er angivet i definitionen af rapporteringstræet. Når dine legitimationsoplysninger udløber, genereres de berørte rapporter i rapporttidsplanen ikke, før legitimationsoplysningerne er blevet opdateret. Der vises en meddelelse i rapporteringskøen for at angive, at tilladelser skal opdateres. Rapporttidsplanen mislykkes, hvis en af følgende situationer opstår (fordi de kræver legitimationsoplysninger):
-   En ny virksomhed er blevet føjet til en rapporttræ for en individuel rapport.
-   En rapport i en rapportgruppe er blevet ændret.
-   En ny rapport for en ekstra virksomhed er blevet føjet til en rapportgruppe.

Du kan fortsætte ved at klikke på knappen Tilladelser i dialogboksen Rapportplanlægning og derefter angive de korrekte legitimationsoplysninger.

## <a name="missing-account-analysis-feature"></a>Funktion til manglende kontoanalyse
Du kan søge efter finanskonti og økonomiske dimensioner, der kan mangle på tværs af alle rækkedefinitioner, definitioner af rapporteringstræ og rapportdefinitioner i en dokumentkomponentgruppe. Dette er nyttigt, når du opretter eller opdaterer flere konti eller dokumentkomponent i en kort tidsperiode, og du vil kontrollere, at alle nye oplysninger er inkluderet i dine rapporter.

Manglende konti bestemmes ved hjælp af de laveste og højeste værdier fra rækkedefinitionen eller definitionen af rapporteringstræet og derefter vises en liste over firmaer, som ikke er i rækkedefinitionen eller definitionen af rapporteringstræet, men som er i de økonomisk data. Hvis en manglende konto er større end eller mindre end værdierne i rækkedefinitionen, er kontoen ikke medtaget på listen over manglende konti.
| ![Tip](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Tip")**Tip**                                             |
|----------------------------------------------------------------------------------------------------------------------------------|
| Denne proces skal køres, før du genererer månedlige rapporter, og når du opretter nye dokumentkomponenter med henblik på validering. |

Rapporter, der har værdiintervaller, er mindre tilbøjelige til at have manglende konti. Når det er muligt, kan du bruge intervaller i dokumentkomponenten med nye konti, når de oprettes. Hvis en rapportdefinition er angivet til @ANY-virksomhed, kan du logge på en bestemt virksomhed og køre en manglende kontoanalyse for virksomheden.
| ![Bemærk](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Bemærk")**Bemærk**                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hvis der er tilføjet en ny virksomhed, skal du føje den nye virksomhed til rapporteringstræer i eventuelle eksisterende rapporter, ellers medtages virksomheden ikke i manglende kontoanalysen. |

### <a name="run-missing-account-analysis"></a>Kør manglende kontoanalyse

1.  I Report Designer skal du klikke på Værktøjer og derefter klikke på Manglende kontoanalyse.
2.  I feltet Firmafilter skal du vælge en virksomhed, hvorpå resultaterne filtreres, eller vælge Alle (intet filter) for at få vist resultater fra alle tilgængelige firmaer.
3.  I feltet Dimensionsfilter skal du vælge en dimension, hvorpå resultaterne filtreres, eller vælge Alle (intet filter) for at få vist alle dimensionsoplysninger for alle tilgængelige dimensioner.
4.  Vælg en indstilling for at sortere resultaterne i feltet Grupper efter. Du kan sortere resultaterne efter dokumentkomponenten, der påvirkes, eller du kan sortere resultaterne efter dimensions- og værdisæt.
5.  Gennemse de viste resultater. Når du vælger en vare i den øverste rude, vises der yderligere oplysninger om undtagelsen. Dette omfatter relaterede dimensioner, værdier og rapporter.
6.  For at åbne den pågældende vare skal du klikke på det tilhørende ikon, der vises i listeruden, eller højreklikke på varen og vælge Åbn. Du kan markere flere varer ved at holde Ctrl-tasten nede, mens du markerer varerne i den nederste rude.
7.  Hvis alle værdier, dokumentkomponenter eller rapporter returneres, som ikke skal indgå i analysen, skal du højreklikke på varen og vælge Udeluk eller markere afkrydsningsfeltet Udeluk ud for varen for at fjerne varen fra listen. Udeladte varer medtages ikke, når listen er blevet opdateret. Du kan at markere flere varer ved at holde Ctrl-tasten nede, mens du markerer varerne i den nederste rude. For at få vist alle varer, herunder de resultater, du tidligere har valgt ikke skulle medtages i analysen, skal du vælge afkrydsningsfeltet Vis udelukkede dokumentkomponenter og værdier og derefter klikke på Opdater.
8.  Klik på Opdater for at opdatere undtagelser, som du har håndteret. Klik på Ja for at udføre en komplet opdatering af alle resultater, eller klik på Nej for at udføre en delvis opdatering af varer, der er behandlet.
    | ![Bemærk](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Bemærk")**Bemærk**                    |
    |------------------------------------------------------------------------------------------------------------|
    | Formen opdateres automatisk, når den åbnes, medmindre formen er åbnet i de sidste 15 minutter. |

9.  Når problemerne er løst, skal du klikke på OK for at lukke dialogboksen.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Tastaturgenveje til manglende kontoanalyse
Når du kører en manglende kontoanalyse, er følgende tastaturgenveje tilgængelige.

| For at gøre det                           | Du kan bruge denne tastaturgenvej |
|--------------------------------------|----------------------------|
| Filtrer efter firma                    | Alt+C                      |
| Filtrer efter dimension                  | Alt+D                      |
| Vælg feltet Grupper efter            | Alt+G                      |
| Vis udelukkede komponenter og værdier      | Alt+S                      |
| Opdater resultater                      | Alt+R                      |
| Udeluk den markerede dokumentkomponent  | Alt+X                      |
| Udeluk på den valgte rækkedefinition  | Ctrl+B                     |
| Udeluk den valgte dimensionsværdi | Ctrl+D                     |
| Åbn den markerede rapportdefinition  | Ctrl+R                     |
| Åbn den valgte rækkedefinition     | Ctrl+O                     |

 
<a name="see-also"></a>Se også
--------

[Økonomirapportering](financial-reporting-intro.md)

[Grænseflade til Report Designer](report-designer-interface.md)



