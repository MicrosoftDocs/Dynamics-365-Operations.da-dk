---
title: Tilpasse brugeroplevelsen
description: I dette emne beskrives, hvordan du kan tilpasse Microsoft Dynamics 365 for Finance and Operations.
author: TLeforMicrosoft
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78c96c58b8c3331fcadb3e5c9b25dfef3b1b4cbc
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1528838"
---
# <a name="personalize-the-user-experience"></a>Tilpasse brugeroplevelsen

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

I dette emne beskrives, hvordan du kan tilpasse Microsoft Dynamics 365 for Finance and Operations.

Der findes tre grundlæggende tilpasningsklasser i Finance and Operations.

- Tilpasninger, der er foretaget på en konfigurationsside. Der er eksempler på farvetema og tidszone.
- Tilpasninger, der er relateret til brug af siden, kaldes *implicitte* tilpasninger. Finance and Operations holder f.eks. styr på bredden af kolonnerne i gitteret, hvis du justerer dem, og tilstanden udvidet eller minimeret for oversigtspaneler.
- Tilpasninger, som en bruger udfører for at ændre udseendet af en side ved at ændre den måde, et element vises eller fungerer på siden, ofte via en interaktiv tilpasningstilstand. Disse tilpasninger kaldes *eksplicitte* tilpasninger. Brugeren kan f.eks. tilføje, skjule eller ændre rækkefølgen af elementer på siden.

Hver tilpasning, som en bruger foretager i Finance and Operations, gælder kun for den pågældende bruger, uanset typen af tilpasning eller det firma, brugeren aktuelt interagerer med. De ændringer, som én bruger foretager på en side, påvirker ikke andre brugere i systemet.

## <a name="system-wide-options-for-the-current-user"></a>Systemindstillinger for den aktuelle bruger

Siden **Brugerindstillinger** indeholder flere systemindstillinger for den aktuelle bruger. Du kan åbne siden **Brugerindstillinger** ved at vælge menuen **Indstillinger** (tandhjulsymbolet) på navigationslinjen og derefter vælge **Brugerindstillinger**. Siden **Brugerindstillinger** har fire faner, der indeholder forskellige brugerindstillinger:

- **Visuel** – Vælg et farvetema og standardstørrelsen på elementer på sider.
- **Præferencer** – Vælg de standardværdier, der bruges, hver gang du åbner Finance and Operations. Disse værdier omfatter firmaet, den første side og standardvisnings- eller redigeringstilstanden. (Visnings-/redigeringstilstanden bestemmer, om en side er låst for visning eller åben for redigering, hver gang du åbner den). Denne fane indeholder også indstillinger for sproget, tidszonen samt dato-, klokkeslæts- og talformat. Endelig indeholder denne fane flere forskellige indstillinger, som varierer fra version til version.
- **Firma** – Juster dit brugernavn og andre kontorelaterede indstillinger.
- **Arbejdsgang** – Vælg indstillinger, der er relateret til arbejdsgangen.

I tillæg til at modificere dine brugerindstillinger kan du også gennemse og slette dine brugerdata og personlige tilpasninger ved at klikke på knappen **Brugerdata**. Når du benytter programmet, lagres mange af de valg, du foretager dig, for at gøre det lettere for dig at bruge systemet fremadrettet. Fanen **Personlig tilpasning** giver dig i særlig grad mulighed for at gennemse og styre de personlige ændringer, du har foretaget på siderne i systemet. Billedforklaringerne til funktioner, pop op-vinduerne, der præsenterer dig for nye funktioner i produktet (tilgængelig i platformsopdatering 26), kan ligeledes nulstilles fra denne fane, således at du igen bliver notificeret om funktioner, du tidligere er stødt på.  

## <a name="implicit-personalizations"></a>Implicitte tilpasninger

Implicitte tilpasninger er tilpasninger, som du udfører ved blot at interagere med visse kontrolelementer, som "husker" deres aktuelle tilstand for synlighed.

- **Gitterkolonner** – Du kan justere bredden på en kolonne i et gitter ved at markere størrelseslinjen til venstre eller højre for kolonneoverskriften og derefter skubbe den mod venstre eller højre, indtil kolonnen har den ønskede bredde. Finance and Operations gemmer den bredde, du angiver for en kolonne. Derefter ændres størrelsen på kolonnen til denne bredde, hver gang du åbner den side, der indeholder dette gitter.
- **Oversigtspaneler** – Nogle sider har udvidelige sektioner, der kaldes *oversigtspaneler*. Finance and Operations gemmer oplysninger om de oversigtspaneler, som du har udvidet og skjult. Hver gang du vender tilbage til siden, bliver de samme oversigtspaneler enten vist eller skjult baseret på din seneste interaktion med siden. I nogle tilfælde kan du forbedre systemets ydeevne ved at skjule et oversigtspanel, fordi Finance and Operations ikke behøver at hente oplysningerne for dette oversigtspanel, før oversigtspanelet er udvidet. Som det forklares senere i dette emne, kan du også ændre rækkefølgen af oversigtspanelerne på en side.
- **Faktabokse** – Nogle sider har en sektion, der kaldes en *faktaboksrude*. Denne rude indeholder skrivebeskyttede oplysninger, der er relateret til sidens aktuelle emne. Hver sektion i faktaboksruden kaldes en *Faktaboks*. Du kan skjule eller vise hele faktaboksruden, og du kan også udvide eller skjule individuelle faktabokse. Finance and Operations gemmer dine indstillinger. Hver gang du vender tilbage til siden, gendannes tilstanden for faktaboksruden, og de enkelte faktabokse gendannes baseret på din seneste interaktion med siden. I nogle tilfælde kan du forbedre systemets ydeevne ved at skjule en faktaboks, fordi Finance and Operations ikke behøver at hente oplysningerne for denne faktaboks, før faktaboksen er udvidet.
- **Handlingsruder** – Øverst på de fleste sider vises en *handlingsrude*. Handlingsruden indeholder knapper for mange af de handlinger, som du kan udføre på den aktuelle side. Disse knapper er ofte organiseret under faner. Du kan fastgøre hele den åbne handlingsrude, eller du kan lade den være skjult som standard. Næste gang du derefter åbner siden, gendanner Finance and Operations handlingsruden i fastgjort tilstand. Hvis handlingsruden er fastgjort åben, viser Finance and Operations også den handlingsfane, som du brugte sidst.
- **QuickFilters** – Der vises et *QuickFilter* over mange gitre. Med QuickFilter kan du filtrere gitteret baseret på en kolonne, du vælger. Finance and Operations gemmer den kolonne, du filtrerede på. Når du derefter næste gang åbner den side, der indeholder det pågældende gitter, filtreres gitteret på den samme kolonne. Du kan derefter filtrere gitteret på en anden kolonne.
- **Filtre til kolonneoverskrift** – Når du filtrerer et gitter ved hjælp af *Filtre til kolonneoverskrift*, kan du ændre filteroperatoren efter behov for at finde de data, du vil. Du kan for eksempel ændre operatoren fra **begynder med** til **er præcis**. Hver gang du bruger et kolonneoverskriftsfilter og redigerer filteroperatoren, gemmer Finance and Operations ændringen. Det gendanner derefter filteroperatoren, næste gang du filtrerer på den pågældende kolonne.
- **Navigationsrude** – Du kan åbne *navigationsruden* ved at vælge knappen **Menu** i venstre rude på enhver side. (**Menu**-knappen kaldes undertiden *hamburger*, *hamburgermenu* eller *hamburgerknap*). Du kan fastgøre navigationsruden åbne, eller kan du holde den skjult som standard. Når du fastgør navigationsruden åben, holder Finance and Operations den åben, indtil du skjuler den.

## <a name="explicit-personalizations"></a>Eksplicitte tilpasninger

Forskellige personer og virksomheder har forskellige perspektiver på de data, der er vigtigst for dem, eller de data, de har ikke brug for i den måde, de driver deres forretning på. I Finance and Operations kan du tilpasse den måde, dataene arrangeres på, og hvordan du interagerer med dem. Du kan også angive, at visse oplysninger skal være skjult. Disse funktioner er vigtige for en personlig og produktiv oplevelse og er eksempler på eksplicitte tilpasninger. Eksplicitte tilpasninger er tilpasninger, som du eksplicit udfører med det formål at ændre udseendet eller funktionsmåden for et element eller en side.

### <a name="shortcut-menu-options"></a>Menupunkter i genvejsmenuer

Genvejsmenuer indeholder måder at ændre en side, så den passer bedre til dine behov eller dit firmas behov. (En genvejsmenu kaldes også en *højrekliksmenu* eller *kontekstmenu*).

Nogle af de mest almindelige og vigtigste ændringer, der kan udføres på en side, er direkte tilgængelige som indstillinger i en genvejsmenu. Hvis du f.eks. fra og med platformsopdatering 17 vil tilføje eller skjule kolonner i et gitter, skal du blot højreklikke på en kolonneoverskrift i gitteret og derefter vælge **Tilføj kolonner** eller **Skjul denne kolonne**.

De mest grundlæggende typer eksplicitte tilpasninger er desuden tilgængelige, hvis du højreklikker på et element og derefter vælger **Tilpas**. (Bemærk, at ikke alle elementer på din side kan tilpasses). Når du bruger denne metode for tilpasning, vises elementets egenskabsvindue.

[![Tilpasning af et elements egenskaber](./media/personalization-element-properties.png)](./media/personalization-element-properties.png)

Du kan bruge egenskabsvinduet til at tilpasse et element på følgende måder:

- Ændre elementets etiket.
- Skjule elementet, så det ikke vises på siden. Dataene i feltet slettes eller ændres ikke. Oplysningerne vises blot ikke på siden længere.
- Omfatte oplysningerne i oversigtspanelets oversigtssektion (hvis elementet er i et oversigtspanel).
- Springe feltet over, når du trykker på Tab for at flytte mellem felterne på siden.
- Forhindre, at data i feltet (for enhver post) redigeres.

Egenskabsvinduet kan omfatte andre tilpasningsmuligheder, afhængigt af elementet. I egenskabsvinduet for et felt kan du f.eks. opgradere feltet til et dashboard, og i egenskabsvinduet for et dashboard kan du evt. oprette et nyt arbejdsområde i dette dashboard.

### <a name="the-personalization-toolbar"></a>Værktøjslinjen Tilpasning

Hvis du vil foretage flere ændringer på en side eller foretager ændringer, der ikke er tilgængelige via andre mekanismer (f.eks. genbestillingselementer), kan du bruge **Brugertilpasning**-værktøjslinjen. For at åbne værktøjslinjen **Brugertilpasning** skal du vælge **Personaliser denne formular** i egenskabsvinduet for et element. Du kan også vælge **Personaliser denne formular** i gruppen **Personaliser** under fanen **Indstillinger** i handlingsruden for hver side.

[![Værktøjslinjen Tilpasning](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Navigering på siden

Muligheden for at navigere på siden, mens **Brugertilpasning-værktøjslinjen** er åben, afhænger af platformsversionen, du kører.

- Før platformsopdatering 19 er siden skrivebeskyttet, mens **Brugertilpasning**-værktøjslinjen er åben (du kan ikke angive noget) og ikke-interaktiv (du kan kun foretage ændringer af de synlige elementer på siden). Hvis du vil foretage ændringer af elementer i en skjult sektion eller på en anden fane, skal du lukke **Brugertilpasning**-værktøjslinjen, udvide en sektion eller skifte til den ønskede fane og derefter genåbne den **Brugertilpasning**-værktøjslinjen.

- Fra og med platformsopdatering 19 er siden stadig skrivebeskyttet, hvis **Brugertilpasning**-værktøjslinjen er åben, men den er meget mere interaktiv. Du kan udvide eller skjule ruden med faktaboksen, skifte faner og udvide eller skjule sektioner, mens **Brugertilpasning**-værktøjslinjen er åben, på samme måde, som du normalt ville på siden. For at anvende en ændring af tilpasning på en sektion eller fane, der kan skjules (f.eks. for at skjule et oversigtspanel), skal du udløse knappen, der vises ud for den sektion eller fane, der kan skjules, når den opnår tastaturfokus, eller når du peger på den.

#### <a name="personalization-tools"></a>Tilpasningsværktøjer

Følgende værktøjer er tilgængelige på værktøjslinjen **Brugertilpasning**:

- Brug værktøjet **Vælg** til at vælge og ændre et elements egenskaber. Vælg værktøjet **Vælg**, og vælg derefter det element, hvis egenskaber skal ændres. Når du vælger et element, åbnes elementets egenskabsvindue, og du kan redigere egenskaberne for det element. Du kan gentage processen for andre elementer, der kan tilpasses på denne side. Men på grund af den måde, nogle elementer bruges på, kan du ikke ændre alle deres egenskaber i Finance and Operations. Derfor når du vælger et element, du kan muligvis se, at nogle af dets egenskaber ikke kan ændres. Du kan f.eks. ikke skjule et felt, der er obligatorisk.
- Brug værktøjet **Flyt** til at flytte et element til et andet sted inden for den aktuelle gruppe elementer. (Du kan ikke flytte et element uden for dets overordnede gruppe). Vælg værktøjet **Flyt**, og vælg derefter elementet, der skal flyttes. Når du markerer et element, scanner Finance and Operations siden for at finde ud af, hvor elementet kan flyttes hen. Derefter oprettes en række "slipzoner". Når du trækker elementet omkring i den aktuelle gruppe, vises hver "slipzone" som en farvet, fed linje ud for det område, hvor elementet kan slippes.
- Brug værktøjet **Skjul** til at skjule et element på siden. Vælg værktøjet **Skjul**, og markér derefter elementet, der skal skjules. Når du vælger værktøjet **Skjul**, gøres alle elementer, der i øjeblikket er skjult, synlige og vises i en nedtonet container. Du kan derefter vise dem igen. Ved at vælge **markeringsværktøjet** kan du se, hvordan siden vil se ud, når de markerede elementer er skjult.

    - Fra og med platformsopdatering 18 kan du skjule obligatoriske felter og sektioner, der indeholder obligatoriske felter. Så kan du oprette en forenklet funktionsmåde, hvor obligatoriske felter, der er standard i forretningslogik, ikke vises. Skjulte obligatoriske felter er også midlertidigt synlige, hvis de er tomme, når lagring forsøges.

- Brug værktøjet **Oversigt**, når du vil have, at et elementvises i oversigtspanelets oversigtssektion. Værktøjet Oversigt kan kun bruges til felter, der er i en oversigtspanelsektion. Når du vælger værktøjet **Oversigt**, vises alle felter, der er valgt som oversigtsfelter, i en nedtonet container. Du kan interaktivt føje felter til oversigtspanelets oversigt og fjerne felter fra oversigtspanelets oversigt ved at markere felterne.
- Brug værktøjet **Spring over** for at fjerne et element fra sidens tastaturtabuleringsrækkefølge. Når du vælger værktøjet **Spring over**, vises alle elementer, der i øjeblikket er sprunget over, i en nedtonet container. Du kan derefter gøre dem til en del af tabuleringsrækkefølgen igen.
- Brug værktøjet **Rediger** til at markere et element som redigerbart eller ikke redigerbart. Når du vælger værktøjet **Rediger**, vises alle elementer, der i øjeblikket er ikke-redigerbare, i en nedtonet container. Du kan derefter gøre dem redigerbare igen. Bemærk, at nogle af felterne er obligatoriske, og at de ikke kan gøres redigerbare. Der vises en hængelås ud for de pågældende felter.
- Brug knappen **Indsæt** for at se en liste over elementer, der kan indsættes på en side.

    - Vælg værktøjet **Felt** under **Indsæt** for at tilføje et felt på siden. Når du bruger værktøjet **Felt**, kan du kun tilføje felter, som indgår i definitionen af siden, men som ikke i øjeblikket vises på siden. Du kan finde oplysninger om, hvordan du opretter nye felter, der ikke er en del af den aktuelle sidedefinition, under [Brugerdefinerede felter](user-defined-fields.md). Når du har valgt værktøjet **Felt**, skal du først markere den gruppe eller det område, hvor du vil tilføje et felt. Der åbnes en dialogboks med listen over felter, der er relateret til den valgte gruppe eller det markerede område. Vælg ét eller flere felter, som du vil tilføje, i dialogboksen, og vælg derefter **Indsæt**. Gentag processen for at fjerne et felt, du tidligere har tilføjet, men fjern markeringen af feltet i dialogboksen.
    - Vælg værktøjet **PowerApp** under **Indsæt** for at integrere en app, der er oprettet ved hjælp af Microsoft PowerApps, på siden. Du kan finde detaljerede oplysninger om, hvordan du integrerer en PowerApps-app på en side, under [Integrere PowerApps](embed-power-apps.md).

- Vælg knappen **Administrer** for at se en liste over administrationsindstillinger, der er relateret til alle tilpasninger for den aktuelle side.

    - Vælg **Ryd** for at nulstille siden til dens installerede standardtilstand. Alle tilpasninger på den aktuelle side slettes. Der er ingen fortrydelseshandling. Derfor skal du kun bruge denne indstilling, hvis du er sikker på, at du vil nulstille siden.
    - Vælg **Importer** for at indlæse en personlig tilpasning fra en fil, som du eller en anden tidligere har oprettet for siden. Alle dine aktuelle tilpasninger for siden erstattes med tilpasninger fra den valgte fil.
    - Vælg **Eksporter** for at gemme dine personlige indstillinger for siden i en fil. Du kan dele dine tilpasninger med andre brugere. Disse brugere skal kun importere filen, der indeholder dine personlige indstillinger for siden.

- Vælg knappen **Luk** for at lukke værktøjslinjen **Brugertilpasning** og sætte siden tilbage til dens tidligere interaktive tilstand.

Når værktøjslinjen **Brugertilpasning** bruges, er gemmehandlinger implicitte. Dine personlige indstillinger træder i kraft, så snart du udfører dem, og du behøver ikke at vælge **Gem**-knap. I nogle tilfælde vises et hængelåsikon ud for en element, når du vælger et værktøj. Dette symbol angiver, at du ikke kan redigere egenskaberne for det element, der er relateret til det valgte værktøj, fordi ændringer af disse egenskaber vil forhindre, at siden fungerer korrekt.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Tilføje et felt, en liste eller et link til et arbejdsområde

For nogle sider, der indeholder lister, findes en funktion til yderligere tilpasning. Ved hjælp af knappen **Føj til arbejdsområde** i gruppen **Personaliser** under fanen **Indstillinger** i handlingsruden kan du vise oplysningerne fra den aktuelle liste i et bestemt arbejdsområde. Du kan vise en filtreret og sorteret visning af oplysningerne i arbejdsområdet, eller du kan vise standardvisningen. Du kan også angive, om oplysningerne skal vises i arbejdsområdet som en liste, som et oversigtsfelt, der kan vise antallet elementer på listen, eller som et link.

[![Føj til arbejdsområde](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Hvis du vil føje en liste til et arbejdsområde, skal du først sortere eller filtrere listen på siden, så den viser oplysningerne, som de skal vises i arbejdsområdet. Vælg derefter **Føj til arbejdsområde**. Vælg et arbejdsområde, og vælg derefter **Liste** i feltet **Præsentation**. Når du har valgt **Konfigurer**, åbnes en dialogboks, hvor du kan vælge de kolonner, der skal vises på listen i arbejdsområdet. Du kan også angive, hvilken label der bruges til listen i arbejdsområdet.
- Hvis du vil føje et felt til et arbejdsområde, skal du først filtrere listen på siden, så den viser de data, du vil opsummere eller ønsker hurtig adgang til. Vælg derefter **Føj til arbejdsområde**. Vælg et arbejdsområde, og vælg derefter **Felt** i feltet **Præsentation**. Når du har valgt **Konfigurer**, åbnes en dialogboks, hvor du kan angive, hvilken label der skal bruges til feltet i arbejdsområdet. Du kan også angive, om feltet skal vise en optælling. Når feltet er føjet til arbejdsområdet, kan du markere det for at åbne den aktuelle side fra arbejdsområdet og få vist den filtrerede liste, der er knyttet til feltet.
- Hvis du vil føje et link til et arbejdsområde, skal du først filtrere listen på siden, så den viser dataene, du er interesseret i. Vælg derefter **Føj til arbejdsområde**. Vælg et arbejdsområde, og vælg derefter **Link** i feltet **Præsentation**. Når du har valgt **Konfigurer**, åbnes en dialogboks, hvor du kan angive, hvilken label der skal bruges til linket. Du kan også vælge at angive en label til en ny sektion, der skal indeholde dette link.

Når listen, feltet eller linket er blevet føjet til et arbejdsområde, kan du åbne dette arbejdsområde og ændre rækkefølgen af elementerne i det, som du vil.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Føje en oversigt fra et arbejdsområde til et dashboard

Nogle arbejdsområder indeholder optællingsfelter (dvs. felter med angivelse af antal), og du kan også få vist disse felter i dashboardet. Højreklik på et optællingsfelt i et arbejdsområde, og vælg derefter **Tilpas**. Vælg derefter i feltets egenskabsvindue **Fastgør til dashboard**. Næste gang du åbner (og opdaterer) det valgte dashboard, vises optællingen under navigationsfeltet for dette arbejdsområde. Du kan vælge denne optælling for at gå direkte til de data, den repræsenterer.

### <a name="personalizing-your-dashboard"></a>Tilpasning af dit dashboard

Dashboardet er ofte den første side, du ser, når du åbner Finance and Operations. Du kan tilpasse dashboardet, så det kun viser de arbejdsområdefelter, du vil have vist. Du kan også omarrangere felterne, så de er placeret i den rækkefølge, du foretrækker at se dem i, omdøbe dit arbejdsområdes navigationsfelter eller tilføje et helt nyt arbejdsområdefelt.

Hvis du vil tilpasse dashboardet, skal du højreklikke på et felt og derefter vælge **Personaliser** for at åbne feltets egenskabsvindue.

- Hvis du vil skjule eller omdøbe det valgte felt, kan du foretage denne ændring direkte i egenskabsvinduet.
- Hvis du vil omarrangere felterne i arbejdsområdet, skal du vælge **Tilpas denne formular** for at åbne værktøjslinjen **Brugertilpasning**. Du kan derefter bruge værktøjet **Flyt** til at arrangere felterne efter behov.
- For at oprette et nyt arbejdsområdefelt skal du vælge **Tilføj et arbejdsområde** i egenskabsvinduet. Der oprettes et nyt felt i arbejdsområdet i bunden af dashboardet. Du kan omdøbe dette nye arbejdsområdefelt, som du vil. Du kan også føje lister, felter og links til arbejdsområdet som beskrevet i sektionen [Føje lister, felter eller links til arbejdsområder](personalize-user-experience.md#adding-a-tile-list-or-link-to-a-workspace) i dette emne.

## <a name="administration-of-personalization"></a>Administration af brugertilpasning

Når du har tilpasset en side, kan du dele dine tilpasninger med andre brugere ved at eksportere den tilpassede side. Du kan bede de andre brugere om at åbne den tilpassede side og importere den tilpasningsfil, du har oprettet. Alternativt kan du give tilpasningen til en bruger med administratorrettigheder. Denne bruger kan derefter anvende din fil med personlige indstillinger til mange brugere på samme tid.

Brugere, der har administratorrettigheder, kan også administrere tilpasninger for andre brugere på siden **Brugertilpasning**. Denne side indeholder fire faner:

- **Anvend** – Du kan importere eller vælge en tilpasning for en eller flere brugere. For at anvende en tilpasning på en eller flere brugere skal du først vælge en rolle og brugere, der har denne rolle. Vælg derefter en eksisterende tilpasning, der skal anvendes på de brugere, du har valgt, eller importér en tilpasningsfil. Tilpasningen valideres og anvendes på alle de markerede brugere, næste gang de åbner den valgte side.
- **Slet** – Du kan slette alle tilpasninger for en side eller et arbejdsområde for en eller flere brugere. Vælg først en side eller et arbejdsområde for at se en liste over de brugere, der har tilpasset siden eller området. Vælg de brugere, der skal have ryddet tilpasninger for siden eller arbejdsområdet, og vælg derefter **Ryd**. Alle tilpasninger, som de valgte brugere har anvendt på den valgte side eller det valgte arbejdsområde, slettes. Denne handling kan ikke fortrydes. Hvis der er gemt en tilpasning for siden eller arbejdsområdet, kan denne tilpasning dog importeres igen.
- **Administration pr. bruger** – Marker en bruger for at få vist listen over sider, som brugeren har tilpasset. Du kan derefter aktivere eller deaktivere den valgte brugers evne til at bruge personlige indstillinger for bestemte sider eller for hele systemet. Du kan også importere, eksportere eller rydde en tilpasning for den valgte bruger. Du kan derudover nulstille billedforklaringer til funktioner for den valgte bruger, hvilket vil resultere i, at alle de pop op-vinduer, som introducerer nye funktioner, og som tidligere er blevet afvist, vises på ny næste gang brugeren støder på de pågældende funktioner.   
- **System** - Du kan midlertidigt deaktivere alle tilpasninger for alle brugere i systemet. Når du gør det, slettes tilpasningerne. Alle sider nulstilles blot til deres standardtilstand for alle brugere. Hvis du senere aktiverer tilpasningen igen, anvendes alle tilpasninger igen. Du kan også permanent slette alle tilpasninger for alle brugere i systemet. Det er ikke muligt at gendanne tilpasninger, som er blevet slettet. Før du udfører denne opgave, skal du derfor sørge for at eksportere de brugertilpasninger, som du eventuelt vil bruge senere.

## <a name="personalization-of-inventory-dimensions"></a>Tilpasning af lagerdimensioner

Når du tilpasser opsætningen af lagerdimensioner på en side, skal du overveje de indstillinger, der er oprettet ved hjælp af indstillingen **Vis dimension**. Du kan f.eks. bruge personlige indstillinger til at skjule en kolonne for batchnummer-lagerdimensionen, men kolonnen vises, næste gang siden åbnes. Dette sker, fordi indstillingen **Dimensionsvisning** styrer de lagerdimensionskolonner, der vises.

Indstillingerne i **Dimensionsvisning** gælder på tværs af alle sider og tilsidesætter den tilpassede opsætning af lagerdimensionsfelter på individuelle sider.

Hvis du derfor i det foregående eksempel ikke ønsker, at kolonnen for batchnummer-lagerdimensionen skal vises, skal du rydde dimensionen som en del af indstillingen **Vis dimensioner** for tabellen. Denne ændring vil desuden gælde ikke kun for en bestemt side, men på tværs af alle sider.
