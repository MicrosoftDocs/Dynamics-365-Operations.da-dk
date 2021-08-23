---
title: Generere økonomiske rapporter
description: Dette emne indeholder oplysninger om generering af en økonomisk rapport.
author: jinniew
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 101cf2b29bb6f91cec5a3dac0be30b53388905c96ecf481f5b7b3e90cda3f804
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740257"
---
# <a name="generate-financial-reports"></a>Generere økonomiske rapporter

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om generering af en økonomisk rapport.

Åbn den ønskede rapportdefinition for at generere en rapport, og vælg knappen **Generer** på værktøjslinjen. Vinduet **Status for rapportkø** åbnes og angiver placeringen af rapporten i køen. Den genererede rapport åbnes som standard i Web Viewer.

Følgende indstillinger er tilgængelige for generering af rapporter:

- Angive en tidsplan for automatisk at generere en rapport eller en gruppe af rapporter
- Søge efter manglende konti eller data i en rapport og validere nøjagtigheden af en rapport

Når du genererer en rapport, bruges de indstillinger, du har angivet under fanen Rapportdefinition .

## <a name="generate-a-financial-report"></a>Generér en økonomisk rapport

Hvis du vil oprette en økonomirapport, skal du gå til **Finans** \> **Forespørgsler og rapporter** \> **Økonomirapporter**.

- Vælg en rapport, du vil generere, og vælg **Generer**.
- Udfyld feltet **Rapportdato**, og vælg **OK**.

Når rapporten er genereret, kan den ses i sektionen **Rapporter**.

Du kan vælge **Vis** eller **Slet** for rapporten.

Åbn den ønskede rapportdefinition for at generere en rapport ved hjælp af **Rapportdesigner**, og vælg derefter på knappen **Generer** på værktøjslinjen. Vinduet **Status for rapportkø** åbnes og angiver placeringen af rapporten i køen. Den genererede rapport åbnes som standard i Web Viewer.

## <a name="report-groups"></a>Rapportgrupper

Du kan bruge rapportgrupper til at oprette flere rapporter på én gang. Antag f.eks., at brugerne opretter otte rapporter hver måned ved udgangen af måneden. Opret en rapportgruppe, og i stedet for at vælge **Generer** for hver af de otte rapporter i gruppen, kan du vælge **Generer** for rapportgruppen, og de otte rapporter genereres i ét trin. Når rapporterne i den valgte rapportgruppe er genereret, kan du gå til **Finans** (**Finans > Forespørgsler og rapporter > Finansrapporter**) for at få vist de enkelte rapporter. Benyt følgende fremgangsmåde for at konfigurere eksemplet på den betingede rapport:

1. Vælg **Rapportgrupper** i rapportdesigner 
2. Vælg de eksisterende rapportdefinitioner, der skal medtages i rapportgruppen. 
3. Vælg overstyringsindstillinger for firma, detaljer og dato i hver af de rapporter, der skal inkluderes i gruppen.
   Det anbefales, at du angiver **Firma**, **Periode**, **År** og **Detaljeringsniveau** for hver rapport. 
4. Gem rapportgruppen.

## <a name="schedule-report-generation"></a>Planlægge rapportgenerering
Mange firmaer har en grundlæggende række rapporter, der køres på planlagte intervaller for at passe ind i deres forretningsprocesser. Du kan planlægge en rapport, der skal genereres regelmæssigt, f.eks. dagligt, ugentligt, månedligt eller årligt. Dette kan være en enkelt rapport eller en gruppe af rapporter, der indeholder flere virksomheder. Du skal indtaste dine legitimationsoplysninger for hvert firma, der er angivet, som f.eks. dem, der er i en trædiagramdefinition. Hvis legitimationsoplysningerne ikke er gyldige, viser rapporten kun de oplysninger, du har adgang til, f.eks. den virksomhed, som du er logget på, på tidspunktet. Outputoplysninger læses først fra rapportgruppen og derefter fra de enkelte rapporter.

Efterhånden som rapporttidsplaner oprettes og gemmes, vises de i navigationsruden under Rapporttidsplaner. Du kan oprette mapper til at organisere rapporterne. Selvom en enkelt rapport i en tidsplan ikke køres, fortsætter alle andre rapporter med at køre.

> [!IMPORTANT]
> For at oprette, redigere og slette rapporttidsplaner skal du have en rolle som designer eller administrator. Når du kører en rapport, bruges legitimationsoplysningerne for den bruger, der oprettede tidsplanen, til at generere rapporten.

### <a name="create-a-report-schedule"></a>Opret en ny rapporttidsplan

1. I Report Designer skal du vælge **Ny** i menuen **Filer**, og derefter skal du vælge **Rapporttidsplan**. Dialogboksen **Ny rapporttidsplan** åbnes.
2. Under **Indstillinger** skal du vælge en enkelt rapport eller en rapportgruppe for at planlægge. Kun rapporter eller rapportgrupper for det firma eller den rapportkomponent, som du er logget på for øjeblikket, er tilgængelige.
3. Vælg afkrydsningsfeltet **Aktiv** for at aktivere rapporttidsplanen. Kun den, der har oprettet rapporten, eller en administrator kan aktivere eller deaktivere en rapporttidsplan.
4. Vælg knappen **Tilladelser** for at angive firmaets legitimationsoplysninger. Som standard bruges dine logonoplysninger til det firma, som du er logget på. Hvis andre firmaer er inkluderet, f.eks som i definitioner af rapporteringstræ, skal du vælge **Brug separate legitimationsoplysninger** og derefter angiv legitimationsoplysningerne for andre virksomheder, der indgår i rapporttidsplanen. Du kan vælge **Windows-godkendelse** eller skrive et brugernavn og en adgangskode for hver virksomhed. Vælg afkrydsningsfeltet **Gem legitimationsoplysninger** for at gemme legitimationsoplysningerne for disse firmaer. Vælg derefter **OK** for at lukke dialogboksen.
5. Under **Frekvens** i feltet **Start gentagelse** skal du vælge den dato, hvor tidsplanen skal starte. Som standard er den aktuelle systemdato i klientcomputeren valgt:
6. I feltet **Kør rapport på** skal du vælge det tidspunkt, hvor rapporten skal køres. Hvis du angiver et tidspunkt, der er før den aktuelle tid i systemet, kører rapporten på den næste planlagte dato.
7. I området **Gentagelsesmønster** skal du angive, hvor ofte rapporten køres. Som standard vælges **Dagligt** med en Interval-værdi (dage) på 1. Andre muligheder omfatter Ugentligt, Månedligt og Årligt.
8. Vælg, hvornår rapporten ikke længere skal genereres, i området Gentagelsesperiode.

    - **Slutdato mangler** – Rapporttidsplanen kører på ubestemt tid.
    - **Angiv antallet af forekomster** – Rapporttidsplanen kører det angivne antal gange og er derefter deaktiveret.
    - **Slut den** – Rapporttidsplanen slutter på den angivne dato.

9. Vælg **Gem**. I dialogboksen **Gem som** skal du angive et unikt navn på og en beskrivelse af rapporttidsplanen.

Du skal have rollen som designer eller administrator for at kopiere en rapporttidsplan. Selvom en administrator ændrer rapporttidsplanen, beholder rapporten legitimationsoplysningerne for den bruger, der oprettede rapporten.

### <a name="copy-a-report-schedule"></a>Kopiér en rapporttidsplan

1. Vælg **Rapporttidsplaner** i navigationsruden Report Designer, og åbn en rapporttidsplan, der skal kopieres.
2. I menuen **Filer** skal du vælge **Gem som** og derefter indtaste et nyt navn og beskrivelse af tidsplanen i dialogboksen **Gem som**. Vælg **OK**, og den nye tidsplan vises i navigationsruden.
3. Ændr felter og oplysninger efter behov i den nye tidsplan, og vælg derefter **Gem** på værktøjslinjen, eller vælg **Gem** i menuen **Filer**.

Hvis du vil slette en rapporttidsplan, skal du være ejer af rapporttidsplanen eller have en rolle som administrator.

### <a name="delete-a-report-schedule"></a>Slet en rapporttidsplan

1. Vælg **Rapporttidsplaner** i navigationsruden i Report Designer.
2. Vælg rapporttidsplanen, du vil slette, og vælg derefter **Slet**, eller tryk på tasten **Delete**.
3. I dialogboksen til bekræftelse af sletning skal du vælge **Ja** for permanent at slette rapporttidsplanen. Hvis du ikke har tilladelse til at slette tidsplanen, vises en meddelelse, og rapporten slettes ikke.

### <a name="credentials-and-report-schedules"></a>Legitimationsoplysninger og rapporttidsplaner

Hvis du ikke angiver legitimationsoplysninger, der kræves for alle selskaber, der indgår i rapporterne, modtager du følgende meddelelse, når du gemmer rapporttidsplanen: "Du skal angive dine legitimationsoplysninger for de selskaber, der er indeholdt i denne rapporttidsplan. Vælg knappen Tilladelser for at indtaste dine legitimationsoplysninger."

En bruger logger f.eks. på firma A ved hjælp af et brugernavn og en adgangskode. Brugeren opretter en tidsplan for en rapport, der bruger en definition for et rapporteringstræ, for at indsamle data fra flere firmaer. Når denne rapporttidsplan er gemt, bliver brugeren bedt om at indtaste legitimationsoplysninger for det andet firma, som er angivet i trædiagramdefinitionen. Når dine legitimationsoplysninger udløber, genereres de berørte rapporter i rapporttidsplanen ikke, før legitimationsoplysningerne er blevet opdateret. Der vises en meddelelse i rapporteringskøen for at angive, at tilladelser skal opdateres. Rapporttidsplanen mislykkes, hvis en af følgende situationer opstår (fordi de kræver legitimationsoplysninger):

- En ny virksomhed er blevet føjet til en rapporttræ for en individuel rapport.
- En rapport i en rapportgruppe er blevet ændret.
- Der er føjet en ny rapport for et ekstra firma til en rapportgruppe.

Du kan fortsætte ved at vælge knappen **Tilladelser** i dialogboksen **Rapportplanlægning** og derefter angive de korrekte legitimationsoplysninger.

## <a name="missing-account-analysis-feature"></a>Funktion til analyse af manglende konto
Du kan søge efter finanskonti og økonomiske dimensioner, der kan mangle på tværs af alle rækkedefinitioner, definitioner af rapporteringstræ og rapportdefinitioner i en dokumentkomponentgruppe. Dette er nyttigt, når du opretter eller opdaterer flere konti eller dokumentkomponent i en kort tidsperiode, og du vil kontrollere, at alle nye oplysninger er inkluderet i dine rapporter.

Manglende konti bestemmes ved hjælp af de laveste og højeste værdier fra rækkedefinitionen eller definitionen af rapporteringstræet og derefter vises en liste over firmaer, som ikke er i rækkedefinitionen eller definitionen af rapporteringstræet, men som er i de økonomisk data. Hvis en manglende konto er højere eller lavere end værdierne i rækkedefinitionen, medtages kontoen ikke i oversigten over manglende konti.

> [!TIP]
> Af hensyn til valideringen skal denne proces køres, før du genererer månedlige rapporter, og når du opretter nye rapportkomponenter.

Rapporter, der har værdiintervaller, er mindre tilbøjelige til at have manglende konti. Når det er muligt, kan du bruge intervaller i dokumentkomponenten med nye konti, når de oprettes. Hvis en rapportdefinition er angivet til @ANY firma, kan du logge på et bestemt firma og køre en analyse for manglende konti for det pågældende firma.

> [!NOTE]
> Hvis der er tilføjet en ny virksomhed, skal du føje den nye virksomhed til rapporteringstræer i eventuelle eksisterende rapporter, ellers medtages virksomheden ikke i manglende kontoanalysen.

### <a name="run-missing-account-analysis"></a>Kør manglende kontoanalyse

1. I Report Designer skal du vælge **Værktøjer** og derefter vælge **Manglende kontoanalyse**.
2. I feltet **Firmafilter** skal du vælge en virksomhed, hvorpå resultaterne filtreres, eller vælge **Alle (intet filter)** for at få vist resultater fra alle tilgængelige firmaer.
3. I feltet **Dimensionsfilter** skal du vælge en dimension, hvorpå resultaterne filtreres, eller vælge **Alle (intet filter)** for at få vist alle dimensionsoplysninger for alle tilgængelige dimensioner.
4. Vælg en indstilling for at sortere resultaterne i feltet **Grupper efter**. Du kan sortere resultaterne i henhold til den rapportkomponent, der påvirkes, eller du kan sortere resultaterne efter dimensions- og værdigrupper.
5. Gennemse de vist resultater. Når du vælger et element i den øverste rude, vises der yderligere oplysninger om undtagelsen i den nederste rude. Dette omfatter tilknyttede dimensioner, værdier og rapporter.
6. For at åbne den pågældende vare skal du vælge det tilhørende ikon, der vises i listeruden, eller højreklikke på varen og vælge **Åbn**. Du kan markere flere varer ved at holde **Ctrl**-tasten nede, mens du markerer varerne i den nederste rude.
7. Hvis alle værdier, dokumentkomponenter eller rapporter returneres, som ikke skal indgå i analysen, skal du højreklikke på varen og vælge **Udeluk** eller markere afkrydsningsfeltet **Udeluk** ud for varen for at fjerne varen fra listen. Udeladte varer medtages ikke, når listen er blevet opdateret. Du kan markere flere varer ved at holde **Ctrl**-tasten nede, mens du markerer varerne i den nederste rude. Hvis du vil have vist alle elementer, herunder resultater, som du tidligere har valgt at udelade af analysen, skal du markere afkrydsningsfeltet **Vis udeladte rapportkomponenter og værdier**, og vælg **Opdater**.
8. Vælg **Opdater** for at opdatere undtagelser, som du har håndteret. Vælg **Ja** for at udføre en komplet opdatering af alle resultater, eller vælg **Nej** for at udføre en delvis opdatering af varer, der er behandlet.

    > [!NOTE]
    > Formularen opdateres automatisk, når den åbnes, medmindre formularen er blevet åbnet inden for de sidste 15 minutter.

9. Når problemerne er løst, skal du vælge **OK** for at lukke dialogboksen.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Tastaturgenveje til manglende kontoanalyse
Når du kører en manglende kontoanalyse, er følgende tastaturgenveje tilgængelige.

| Hvis du vil gøre dette                           | Tryk på  |
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
