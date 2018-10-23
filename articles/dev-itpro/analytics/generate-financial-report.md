---
title: "Generere økonomiske rapporter"
description: "Dette emne indeholder oplysninger om generering af en økonomisk rapport."
author: aprilolson
manager: AnnBe
ms.date: 09/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: a128f326cb89ab00e69be40801553c0ac551446e
ms.openlocfilehash: 70fa1298c3af43f62b8fa0b833fa817f17858c47
ms.contentlocale: da-dk
ms.lasthandoff: 09/27/2018

---

# <a name="generate-financial-reports"></a>Generere økonomiske rapporter

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om generering af en økonomisk rapport.

Åbn den ønskede rapportdefinition for at generere en rapport, og klik derefter på knappen Generer på værktøjslinjen. Vinduet Status for rapportkø åbnes og angiver placeringen af rapporten i køen. Den genererede rapport åbnes som standard i Web Viewer.

Følgende indstillinger er tilgængelige for generering af rapporter:

- Angive en tidsplan for automatisk at generere en rapport eller en gruppe af rapporter
- Søge efter manglende konti eller data i en rapport og validere nøjagtigheden af en rapport

Når du genererer en rapport, bruges de indstillinger, du har angivet under fanen Rapportdefinition .

## <a name="generate-a-financial-report"></a>Generere en økonomisk rapport

Du kan generere en økonomirapport i Microsoft Dynamics 365 for Finance and Operations ved at gå til **Finans** \> **Forespørgsler og rapporter** \> **Økonomirapporter**.

- Vælg en rapport, du vil generere, og klik på **Generer**.
- Udfyld feltet **Rapportdato**, og klik på **OK**.

Når rapporten er genereret, kan den ses i sektionen **Rapporter**.

Du kan vælge **Vis** eller **Slet** for rapporten.

Åbn den ønskede rapportdefinition for at generere en rapport ved hjælp af **Rapportdesigner**, og klik derefter på knappen Generer på værktøjslinjen. Vinduet Status for rapportkø åbnes og angiver placeringen af rapporten i køen. Den genererede rapport åbnes som standard i Web Viewer.

## <a name="schedule-report-generation"></a>Planlægge rapportgenerering
Mange firmaer har en grundlæggende række rapporter, der køres på planlagte intervaller for at passe ind i deres forretningsprocesser. Du kan planlægge en rapport, der skal genereres regelmæssigt, f.eks. dagligt, ugentligt, månedligt eller årligt. Dette kan være en enkelt rapport eller en gruppe af rapporter, der indeholder flere virksomheder. Du skal indtaste dine legitimationsoplysninger for hvert firma, der er angivet, som f.eks. dem, der er i en trædiagramdefinition. Hvis legitimationsoplysningerne ikke er gyldige, viser rapporten kun de oplysninger, du har adgang til, f.eks. den virksomhed, som du er logget på, på tidspunktet. Outputoplysninger læses først fra rapportgruppen og derefter fra de enkelte rapporter.

Efterhånden som rapporttidsplaner oprettes og gemmes, vises de i navigationsruden under Rapporttidsplaner. Du kan oprette mapper til at organisere rapporterne. Selvom en enkelt rapport i en tidsplan ikke køres, fortsætter alle andre rapporter med at køre.

> [!IMPORTANT]
> For at oprette, redigere og slette rapporttidsplaner skal du have en rolle som designer eller administrator. Når du kører en rapport, bruges legitimationsoplysningerne for den bruger, der oprettede tidsplanen, til at generere rapporten.

### <a name="create-a-report-schedule"></a>Opret en ny rapporttidsplan

1. I Report Designer skal du klikke på Ny i menuen Filer, og derefter skal du vælge Rapporttidsplan. Dialogboksen Ny rapporttidsplan åbnes.
2. Under Indstillinger for skal du vælge en enkelt rapport eller en rapportgruppe for at planlægge. Kun rapporter eller rapportgrupper for det firma eller den rapportkomponent, som du er logget på for øjeblikket, er tilgængelige.
3. Markér afkrydsningsfeltet Aktiv for at aktivere rapporttidsplanen. Kun den, der har oprettet rapporten, eller en administrator kan aktivere eller deaktivere en rapporttidsplan.
4. Klik på knappen Tilladelser for at angive firmaets legitimationsoplysninger. Som standard bruges dine logonoplysninger til det firma, som du er logget på. Hvis et andet firma medtages, f.eks. i trædiagramdefinitioner, skal du vælge Brug separate legitimationsoplysninger og derefter angive legitimationsoplysningerne for et eventuelt andet firma, der indgår i rapporttidsplanen. Du kan vælge Windows-godkendelse eller indtaste et brugernavn og en adgangskode for hvert firma. Vælg afkrydsningsfeltet Gem legitimationsoplysninger for at gemme legitimationsoplysningerne for disse firmaer. Klik derefter på OK for at lukke dialogboksen.
5. Under Frekvensi feltet Start gentagelse skal du vælge den dato, hvor tidsplanen skal starte. Som standard er den aktuelle systemdato i klientcomputeren valgt:
6. Vælg det tidspunkt, hvor rapporten skal køre, i feltet Kør rapport kl.. Hvis du angiver et tidspunkt, der er før den aktuelle tid i systemet, kører rapporten på den næste planlagte dato.
7. I området Gentagelsesmønster skal du angive, hvor ofte rapporten køres. Som standard vælges Dagligt med en Interval-værdi (dage) på 1. Andre muligheder omfatter Ugentligt, Månedligt og Årligt.
8. Vælg, hvornår rapporten ikke længere skal genereres, i området Gentagelsesperiode.

    - Ingen slutdato – Rapporttidsplanen kører på ubestemt tid.
    - Angiv antal forekomster – Rapporttidsplanen kører for det angivne antal gange og deaktiveres derefter.
    - Afslut den – Rapporttidsplanen slutter på den angivne dato.

9. Klik på Gem i værktøjslinjen. I dialogboksen Gem som skal du angive et unikt navn på og en beskrivelse af rapporttidsplanen.

Du skal have rollen som designer eller administrator for at kopiere en rapporttidsplan. Selvom en administrator ændrer rapporttidsplanen, beholder rapporten legitimationsoplysningerne for den bruger, der oprettede rapporten.

### <a name="copy-a-report-schedule"></a>Kopiér en rapporttidsplan

1. Klik på Rapporttidsplaner i navigationsruden Report Designer, og åbn en rapporttidsplan, der skal kopieres.
2. Klik på Gem som i menuen Filer, og angiv derefter et nyt navn og en ny beskrivelse for tidsplanen i dialogboksen Gem som. Klik på OK, og den nye tidsplan vises i navigationsruden.
3. Ændr felter og oplysninger efter behov i den nye tidsplan, og klik derefter på Gem på værktøjslinjen, eller klik på Gem i menuen Filer.

Hvis du vil slette en rapporttidsplan, skal du være ejer af rapporttidsplanen eller have en rolle som administrator.

### <a name="delete-a-report-schedule"></a>Slet en rapporttidsplan

1. Klik på Rapporttidsplaner i navigationsruden i Report Designer.
2. Vælg den rapporttidsplan, der skal slettes, og klik derefter på Slet, eller tryk på tasten Delete.
3. Klik på Ja i bekræftelsesdialogboksen for permanent at slette rapporttidsplanen. Hvis du ikke har tilladelse til at slette tidsplanen, vises en meddelelse, og rapporten slettes ikke.

### <a name="credentials-and-report-schedules"></a>Legitimationsoplysninger og rapporttidsplaner

Hvis du ikke angiver legitimationsoplysninger, der kræves for alle selskaber, der indgår i rapporterne, modtager du følgende meddelelse, når du gemmer rapporttidsplanen: "Du skal angive dine legitimationsoplysninger for de selskaber, der er indeholdt i denne rapporttidsplan. Vælg knappen Tilladelser for at indtaste dine legitimationsoplysninger."

Phyllis logger f.eks. på firma A ved hjælp af sit brugernavn og sin adgangskode. Hun opretter en tidsplan for en rapport, der bruger en definition for et rapporteringstræ, for at indsamle data fra flere firmaer. Når denne rapporttidsplan er gemt, bliver Phyllis bedt om at indtaste legitimationsoplysninger for det andet firma, som er angivet i trædiagramdefinitionen. Når dine legitimationsoplysninger udløber, genereres de berørte rapporter i rapporttidsplanen ikke, før legitimationsoplysningerne er blevet opdateret. Der vises en meddelelse i rapporteringskøen for at angive, at tilladelser skal opdateres. Rapporttidsplanen mislykkes, hvis en af følgende situationer opstår (fordi de kræver legitimationsoplysninger):

- En ny virksomhed er blevet føjet til en rapporttræ for en individuel rapport.
- En rapport i en rapportgruppe er blevet ændret.
- Der er føjet en ny rapport for et ekstra firma til en rapportgruppe.

Du kan fortsætte ved at klikke på knappen Tilladelser i dialogboksen Rapportplanlægning og derefter angive de korrekte legitimationsoplysninger.

## <a name="missing-account-analysis-feature"></a>Funktion til analyse af manglende konto
Du kan søge efter finanskonti og økonomiske dimensioner, der kan mangle på tværs af alle rækkedefinitioner, definitioner af rapporteringstræ og rapportdefinitioner i en dokumentkomponentgruppe. Dette er nyttigt, når du opretter eller opdaterer flere konti eller dokumentkomponent i en kort tidsperiode, og du vil kontrollere, at alle nye oplysninger er inkluderet i dine rapporter.

Manglende konti bestemmes ved hjælp af de laveste og højeste værdier fra rækkedefinitionen eller definitionen af rapporteringstræet og derefter vises en liste over firmaer, som ikke er i rækkedefinitionen eller definitionen af rapporteringstræet, men som er i de økonomisk data. Hvis en manglende konto er højere eller lavere end værdierne i rækkedefinitionen, medtages kontoen ikke i oversigten over manglende konti.

> [!TIP]
> Af hensyn til valideringen skal denne proces køres, før du genererer månedlige rapporter, og når du opretter nye rapportkomponenter.

Rapporter, der har værdiintervaller, er mindre tilbøjelige til at have manglende konti. Når det er muligt, kan du bruge intervaller i dokumentkomponenten med nye konti, når de oprettes. Hvis en rapportdefinition er angivet til @ANY-virksomhed, kan du logge på en bestemt virksomhed og køre en manglende kontoanalyse for virksomheden.

> [!NOTE]
> Hvis der er tilføjet en ny virksomhed, skal du føje den nye virksomhed til rapporteringstræer i eventuelle eksisterende rapporter, ellers medtages virksomheden ikke i manglende kontoanalysen.

### <a name="run-missing-account-analysis"></a>Kør manglende kontoanalyse

1. I Report Designer skal du klikke på Værktøjer og derefter klikke på Manglende kontoanalyse.
2. Vælg et firma, som resultaterne skal filtreres efter, i feltet Firmafilter, eller vælg Alle (intet filter) for at få vist resultater fra alle tilgængelige firmaer.
3. Vælg en dimensions, som resultater skal filtreres efter, i feltet Dimensionsfilter, eller vælg Alle (intet filter) for at få vist alle dimensionsoplysninger for alle tilgængelige dimensioner.
4. Vælg en indstilling for sortering af resultaterne i feltet Gruppér efter. Du kan sortere resultaterne i henhold til den rapportkomponent, der påvirkes, eller du kan sortere resultaterne efter dimensions- og værdigrupper.
5. Gennemse de vist resultater. Når du vælger et element i den øverste rude, vises der yderligere oplysninger om undtagelsen i den nederste rude. Dette omfatter tilknyttede dimensioner, værdier og rapporter.
6. For at åbne den pågældende vare skal du klikke på det tilhørende ikon, der vises i listeruden, eller højreklikke på varen og vælge Åbn. Du kan markere flere varer ved at holde Ctrl-tasten nede, mens du markerer varerne i den nederste rude.
7. Hvis alle værdier, dokumentkomponenter eller rapporter returneres, som ikke skal indgå i analysen, skal du højreklikke på varen og vælge Udeluk eller markere afkrydsningsfeltet Udeluk ud for varen for at fjerne varen fra listen. Udeladte varer medtages ikke, når listen er blevet opdateret. Hvis du vil markere flere elementer, skal du holde Ctrl nede, mens du vælger elementer i den nederste rude. Hvis du vil have vist alle elementer, herunder resultater, som du tidligere har valgt at udelade af analysen, skal du markere afkrydsningsfeltet Vis udeladte rapportkomponenter og værdier og klikke på Opdater.
8. Klik på Opdater for at opdatere undtagelser, som du har behandlet. Klik på Ja for at bekræfte en fuld opdatering af alle resultater, eller klik på Nej for at udføre en delvis opdatering af behandlede elementer.

    > [!NOTE]
    > Formularen opdateres automatisk, når den åbnes, medmindre formularen er blevet åbnet inden for de sidste 15 minutter.

9. Når problemerne er løst, skal du klikke på OK for at lukke dialogboksen.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Tastaturgenveje til manglende kontoanalyse
Når du kører en manglende kontoanalyse, er følgende tastaturgenveje tilgængelige.

| For at gøre det                           | Du kan bruge denne tastaturgenvej |
|--------------------------------------|----------------------------|
| Filtrer efter firma                    | Alt+C                      |
| Filtrere efter dimension                  | Alt+D                      |
| Markere feltet Gruppér efter            | Alt+G                      |
| Vise udeladte rapportkomponenter og værdier      | Alt+S                      |
| Opdatere resultater                      | Alt+R                      |
| Udelade den valgte rapportkomponent  | Alt+X                      |
| Udelade den valgte rækkedefinition  | Ctrl+B                     |
| Udelade den valgte dimensionsværdi | Ctrl+D                     |
| Åbne den valgte rapportdefinition  | Ctrl+R                     |
| Åbn den valgte rækkedefinition     | Ctrl+O                     |


## <a name="additional-resources"></a>Yderligere ressourcer

[Økonomirapportering](financial-reporting-intro.md)

[Brugergrænseflade i Rapportdesigner](report-designer-interface.md)

