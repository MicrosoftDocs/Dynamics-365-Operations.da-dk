---
title: Tilpasse brugeroplevelsen
description: I dette emne beskrives, hvordan du kan tilpasse appen.
author: jasongre
manager: AnnBe
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e46c392c43b63ef443f66d8ea8f9e91a9df3d126
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693226"
---
# <a name="personalize-the-user-experience"></a>Tilpasse brugeroplevelsen

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du kan tilpasse appen, og dækker følgende emner: 

- **Indstillinger for hele systemet** – Disse indstillinger for tilpasning foretages på en opsætningsside og er tilgængelige for alle brugere. Der er eksempler på farvetema og tidszone. 
- **Begrænset adgang til brugertilpasning** – På dette adgangsniveau gemmes brugerhandlinger, der er tilknyttet typisk sideforbrug, automatisk af appen, og næste gang du besøger siden, er de gendannet. Appen gemmer f.eks. bredden af kolonnerne i gitteret, hvis du justerer dem, og tilstanden udvidet eller minimeret for oversigtspaneler. 
- **Fuld adgang til brugertilpasning** – På dette adgangsniveau har brugere adgang til alle muligheder for tilpasning i appen. De har adgang til værktøjslinjen **Brugertilpasning**. 
- **Deling af brugertilpasninger** – Brugere med fuld adgang til brugertilpasning kan eksportere deres sidetilpasninger og dele dem med andre brugere.
- **Administration af brugertilpasninger** – Privilegerede brugere kan få adgang til siden **Brugertilpasning** for at administrere alle tilpasninger på et organisationsniveau. 

## <a name="system-wide-options-for-the-current-user"></a>Systemindstillinger for den aktuelle bruger

Siden **Brugerindstillinger** indeholder flere systemindstillinger for den aktuelle bruger. Disse indstillinger er tilgængelige for alle brugere, selv brugere, som ikke har fået adgang til brugertilpasning. Du kan åbne siden **Brugerindstillinger** ved at vælge knappen **Indstillinger** på navigationslinjen og derefter vælge **Brugerindstillinger**. Siden **Brugerindstillinger** har fire faner, der indeholder forskellige brugerindstillinger:

- **Visuel** – Vælg et farvetema og standardstørrelsen på elementer på sider.
- **Præferencer** – Vælg de standardværdier, der bruges, hver gang du åbner systemet. Disse værdier omfatter standardfirmaet, den første side og standardvisnings- eller redigeringstilstanden. (Visnings-/redigeringstilstanden bestemmer, om en side er låst for visning eller åben for redigering, hver gang du åbner den). Denne fane indeholder også indstillinger for sproget, tidszonen samt dato-, klokkeslæts- og talformater. Endelig indeholder denne fane flere forskellige indstillinger, som varierer fra version til version.
- **Firma** – Se eller juster dit brugernavn og andre kontorelaterede indstillinger.
- **Arbejdsgang** – Vælg indstillinger, der er relateret til arbejdsgangen.

I tillæg til at ændre dine brugerindstillinger kan du også se og slette dine brugsdata og personlige tilpasninger på siden **Brugerindstillinger**. Hvis du vil have vist dine brugsdata, skal du vælge **Brugsdata** i handlingsruden. Under fanen **Brugertilpasning** kan du se og styre de personlige ændringer, du har foretaget på siderne i systemet. Under denne fane kan du også nulstille billedforklaringer til funktioner (dvs. pop op-vinduer, der introducerer nye systemfunktioner). Derefter får du igen en påmindelse om de tidligere registrerede funktioner.

> [!NOTE]
> Hvis funktionen [Gemte visninger](saved-views.md) er slået til, kan du se og administrere dine personlige indstillinger ved at vælge **Brugertilpasning** i handlingsruden på siden **Brugerindstillinger**.

## <a name="restricted-personalization-access-formerly-implicit-personalizations"></a>Begrænset adgang til brugertilpasning (tidligere implicitte tilpasninger)

På niveauet **Begrænset adgang til brugertilpasning** gemmes brugerhandlinger, der er tilknyttet typisk sideforbrug, automatisk af appen, og næste gang du besøger siden, er de gendannet. Der kræves ingen eksplicit Gem-handling. 

Her er en liste over de handlinger, der falder ind under typisk sideanvendelse, og som dækkes af begrænset adgang til brugertilpasning: 

- **Gitterkolonnebredder** – Du kan justere bredden på en kolonne i et gitter ved at markere størrelseslinjen til venstre eller højre for kolonneoverskriften og derefter skubbe den mod venstre eller højre, indtil kolonnen har den ønskede bredde. Appen gemmer den bredde, du angiver for en kolonne. Derefter ændres størrelsen på kolonnen til denne bredde, næste gang du åbner denne side.
- **Gittersidefod og kolonnetotaler** - *(Kun tilgængelig med det nye gitterkontrol aktiveret)* Du kan bestemme, om der skal vises en total nederst i en numerisk kolonne i et gitter, og om sidefoden i gitteret er synlig. Appen gemmer disse indstillinger og anvende dem, næste gang du åbner siden. Du kan finde flere oplysninger under [Gitteregenskaber](grid-capabilities.md). 
- **Oversigtspaneler** – Nogle sider har udvidelige sektioner, der kaldes *oversigtspaneler*. Appen gemmer oplysninger om de oversigtspaneler, som du har udvidet eller skjult. Næste gang du åbner siden, bliver de samme oversigtspaneler enten vist eller skjult baseret på din seneste interaktion med siden. I nogle tilfælde kan du forbedre systemets ydeevne ved at skjule et oversigtspanel, fordi appen ikke behøver at hente oplysningerne for oversigtspaneler, før de er udvidet. Som det forklares senere i dette emne, kan du også ændre rækkefølgen af oversigtspanelerne på en side.
- **Faktabokse** – Nogle sider indeholder en **Relaterede oplysninger**-rude, der viser skrivebeskyttede oplysninger, der er relateret til sidens aktuelle emne. Hver sektion i ruden **Relaterede oplysninger** kaldes en *Faktaboks*. Du kan udvide eller skjule ruden **Relaterede oplysninger**, og du kan også udvide eller skjule individuelle faktabokse. Appen gemmer disse indstillinger. Næste gang du åbner siden,vil ruden **Relaterede oplysninger** og de enkelte faktabokse enten være udvidet eller skjult baseret på din seneste interaktion med siden. I nogle tilfælde kan du forbedre systemets ydeevne ved at skjule ruden **Relaterede oplysninger** eller en faktaboks, fordi appen ikke behøver at hente oplysningerne for faktabokse, før de er udvidet.
- **Handlingsruder** – Øverst på de fleste sider vises en *handlingsrude*. Handlingsruden indeholder knapper for mange af de handlinger, som du kan udføre på den aktuelle side. Disse knapper er ofte organiseret under faner. Du kan *fastgøre* hele den åbne handlingsrude, eller du kan lade den være skjult som standard. Næste gang du åbner siden, vil handlingsruden enten være open eller skjult baseret på din seneste interaktion med siden. Hvis du har fastgjort den åbne handlingsrude, vises den sidste fane, du har brugt.
- **QuickFilters** – Der vises et *QuickFilter* over mange gitre. Med QuickFilter kan du filtrere gitteret baseret på en enkelt kolonne, du vælger. Appen gemmer den kolonne, du filtrerede på. Når du næste gang åbner denne side, vil gitteret som standard filtrere den samme kolonne. Du kan stadig vælge at filtrere gitteret på en anden kolonne.
- **Filtre til kolonneoverskrift** – Når du filtrerer et gitter ved hjælp af *filtre til kolonneoverskrifter*, kan du ændre filteroperatoren efter behov for at finde de data, du vil. Du kan for eksempel ændre operatoren fra **begynder med** til **er præcis**. Hver gang du bruger et kolonneoverskriftsfilter og ændrer filteroperatoren, gemmer appen ændringen. Den gendanner filteroperatoren, næste gang du filtrerer på den pågældende kolonne.
- **Navigationsrude** – Du kan åbne *navigationsruden* ved at vælge knappen **Udvid navigationsruden** øverst til venstre på enhver side. (Knappen kaldes undertiden _**Menu**-knappen_, *hamburger*, *hamburgermenu* eller *hamburgerknap*). Du kan fastgøre navigationsruden åbne, eller du kan holde den skjult som standard. Når du fastgør navigationsruden åben, holder appen den åben, indtil du skjuler den.

## <a name="full-personalization-access-formerly-explicit-personalizations"></a>Fuld adgang til brugertilpasning (tidligere eksplicitte tilpasninger)

På niveauet **Fuld adgang til brugertilpasning** har brugere adgang til alle muligheder for tilpasning i appen. Da forskellige personer og virksomheder har forskellige behov, når de interagerer med appen, især i forbindelse med felter, der anvendes, indeholder brugertilpasning værktøjer, der giver brugere og organisationer mulighed for at tilpasse den måde, som oplysningerne sorteres og interageres i appen på. Disse funktioner er nøglen til at levere en forenklet, optimeret oplevelse i appen, der er skræddersyet til dig og din organisation. 

Hvis funktionen [Gemte visninger](saved-views.md) er aktiveret, skal du gemme en eksplicit lagring for at kunne overføre brugeroplevelsen i en bestemt visning. Når funktionen **Gemte visninger** er slået fra, gemmes disse ændringer automatisk.

I følgende afsnit beskrives omfanget af de brugertilpasningsfunktioner, der er tilgængelige for brugere med niveauet **fuld adgang til brugertilpasning**. Her er nogle af disse funktioner:

- Menupunkter i genvejsmenuer
- Værktøjslinjen **Brugertilpasning**
- Tilføje felter, lister og links til arbejdsområder
- Føje en oversigt fra et arbejdsområde til et dashboard
- Tilpasning af dashboardet

### <a name="shortcut-menu-options"></a>Menupunkter i genvejsmenuer

Genvejsmenuer giver mulighed for at ændre en sides grænseflade, så den passer bedre til dine behov eller din organisations behov. (En genvejsmenu kaldes også en *højrekliksmenu* eller *kontekstmenu*).

Nogle af de mest almindelige og vigtigste ændringer, der kan udføres på en side, er direkte tilgængelige som indstillinger i en genvejsmenu. Hvis du f.eks. vil tilføje eller skjule kolonner i et gitter, skal du blot højreklikke på en kolonneoverskrift og derefter vælge **Indsæt kolonner** eller **Skjul denne kolonne**.

De mest grundlæggende typer brugertilpasninger er desuden tilgængelige, hvis du højreklikker på et element og derefter vælger **Tilpas**. (Bemærk, at ikke alle elementer på din side kan tilpasses). Når du bruger denne metode for tilpasning, vises elementets *egenskabsvindue*.

![Tilpasning af et elements egenskaber](./media/cli-element-property-window.png)

Du kan bruge egenskabsvinduet til at tilpasse et element på følgende måder:

- Ændre elementets etiket.
- Skjule elementet, så det ikke vises på siden. Dataene i feltet slettes eller ændres ikke. Oplysningerne vises blot ikke på siden længere.
- Medtage oplysningerne i oversigtspanelets oversigtssektion (hvis elementet er i et oversigtspanel).
- Spring feltet over, så det aldrig får fokus, når du tabulerer gennem siden.
- Forhindre, at data i feltet redigeres (for enhver post).
- Angiv et felt, der skal bruges til dataindtastning. Hvis der ikke er angivet en værdi i dette felt, vises det med en rød kant og en stjerne for at angive denne tilstand. Denne indstilling er kun tilgængelig, hvis du starter i version 10.0.11, hvor funktionerne [Gemte visninger](saved-views.md) og **Relevante felter efter behov vha. tilpasning** er aktiveret.

Egenskabsvinduet kan omfatte andre tilpasningsmuligheder, afhængigt af elementet. I egenskabsvinduet for et felt kan du f.eks. opgradere feltet til et dashboard, og i egenskabsvinduer for elementer på standarddashboardet kan du oprette et nyt tilpasset arbejdsområde i dette dashboard.

### <a name="the-personalization-toolbar"></a>Værktøjslinjen Tilpasning

Hvis du vil foretage flere ændringer på en side eller ændringer, der ikke er tilgængelige via andre mekanismer (f.eks. sortering af elementer), kan du bruge **Brugertilpasning**-værktøjslinjen. Benyt et af følgende fremgangsmåder for at åbne værktøjslinjen **Brugertilpasning**:

- Vælg **Ctrl + Skift + P** fra alle elementer på siden.
- Vælg **Tilpas denne side** i egenskabsvinduet for elementet.
- Vælg **Tilpas denne side** i gruppen **Personaliser** under fanen **Indstillinger** i handlingsruden på en side.
- Vælg knappen **Indstillinger** (tandhjulssymbolet) på navigationslinjen, og vælg derefter **Personaliser**.

[![Værktøjslinjen Tilpasning](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Navigering på siden

Når værktøjslinjen **Brugertilpasning** er åben, er den underliggende side skrivebeskyttet (med andre ord kan du ikke redigere data), men den er stadig interaktiv. Du kan specifikt udvide eller skjule **Relaterede oplysninger**-ruden, skifte faner og udvide eller skjule sektioner på samme måde, som du normalt udfører disse handlinger på siden. For at anvende en brugertilpasning på en sektion eller fane, der kan skjules (f.eks. for at skjule et oversigtspanel), skal du vælge knappen, der vises ud for denne sektion eller fane, der kan skjules, når den opnår tastaturfokus, eller når du peger på den.

#### <a name="personalization-tools"></a>Tilpasningsværktøjer

Følgende værktøjer er tilgængelige på værktøjslinjen **Brugertilpasning**:

- Brug værktøjet **Vælg** til at vælge og ændre et elements egenskaber. Hvis du vil bruge dette værktøj, skal du vælge knappen **Vælg** på værktøjslinjen og derefter vælge det ønskede element. Elementets egenskabsvindue åbnes, hvor du kan redigere egenskaberne for dette element. Du kan gentage processen for andre elementer, der kan tilpasses på siden. Bemærk, at nogle egenskaber for brugertilpasning muligvis ikke er tilgængelige i visse scenarier. Du kan f.eks. ikke låse et felt, der er obligatorisk.
- Brug værktøjet **Skjul** til at skjule et element på siden. Hvis du vil bruge dette værktøj, skal du vælge knappen **Skjul** på værktøjslinjen og derefter vælge det element, du vil skjule. Når du bruger værktøjet **Skjul**, gøres alle elementer, der i øjeblikket er skjult, synlige, men de vises i en nedtonet container. Du kan derefter gøre et element synligt ved at markere det. Hvis du vil se, hvordan siden vil se ud, når der skjules elementer, skal du skifte til et andet tilpasningsværktøj eller lukker værktøjslinjen for brugertilpasning.
- Brug værktøjet **Tilføj felter** for at tilføje felter på din side. Når du bruger dette værktøj, kan du kun tilføje felter, der er del af sidedefinitionen. Du kan finde oplysninger om, hvordan du opretter nye felter, der ikke er en del af den aktuelle sidedefinition, under [Opret og arbejd med brugerdefinerede felter](user-defined-fields.md). Når du har valgt knappen **Tilføj felter** på værktøjslinjen, skal du først markere det gitter eller den sektion, hvor du vil tilføje et felt. Der åbnes en dialogboks med listen over felter, der er relateret til det gitter eller den sektion, der er valgt. Vælg ét eller flere felter, som du vil tilføje, i dialogboksen, og vælg derefter **Opdater**. Gentag processen for at fjerne et felt, du tidligere har tilføjet, men fjern markeringen af feltet i dialogboksen.
- Brug værktøjet **Flyt** til at flytte et element til et andet sted inden i den aktuelle gruppe af elementer. Bemærk, at du ikke kan flytte et element uden for dets overordnede gruppe. Hvis du vil bruge dette værktøj, skal du vælge knappen **Flyt** på værktøjslinjen og derefter vælge det element, du vil flytte. Når du vælger et element, fastlægger appen de steder, hvor elementet kan flyttes hen. Disse steder kaldes *slipzoner*. Når du trækker elementet omkring i den aktuelle gruppe, vises hver slipzone som en farvet, fed linje ud for det område, hvor elementet kan slippes.
- Brug værktøjet **Spring over** for at fjerne et element fra sidens tastaturtabuleringsrækkefølge. Når du vælger knappen **Spring over** på værktøjslinjen, vises alle elementer, der i øjeblikket er sprunget over, i en nedtonet container. Du kan interaktivt fjerne eller tilføje felter i tabulatorsekvensen.
- Brug værktøjet **Vis i overskrift**, når du vil have vist et felt i oversigtspanelets oversigtssektion. Når du vælger knappen **Vis i overskrift** på værktøjslinjen, vises alle felter, der er valgt som oversigtsfelter, i en nedtonet container. Du kan interaktivt føje felter til oversigtspanelets oversigt og fjerne felter fra oversigten ved at markere felterne.
- Brug værktøjet **Kræv** for at udpege et element, der kræves til dataindtastning. Når du vælger knappen **Kræv** på værktøjslinjen, vises alle elementer, der er blevet tilpasset til at gøre dem påkrævet, i en nedtonet container. Du kan derefter gøre dem ikke påkrævet igen. Denne indstilling er kun tilgængelig i version 10.0.12 og senere, når funktionen **Relevante felter efter behov vha. tilpasning** er aktiveret.
- Brug værktøjet **Lås** til at markere et element som redigerbart eller ikke-redigerbart. Når du vælger knappen **Lås** på værktøjslinjen, vises alle elementer, der i øjeblikket ikke er redigerbare, i en nedtonet container. Du kan derefter gøre dem redigerbare igen. Bemærk, at nogle af felterne er obligatoriske og ikke kan gøres ikke-redigerbare. Der vises en hængelås ud for de pågældende felter.
- Brug værktøjet **Tilføj en app fra Power Apps** til at integrere en app, der er oprettet ved hjælp af Microsoft Power Apps, på siden. Du kan finde detaljerede oplysninger om, hvordan du integrerer en Power Apps-app på en side, under [Integrere apps fra Power Apps](embed-power-apps.md). Denne indstilling er kun tilgængelig, når funktionen [Gemte visninger](saved-views.md) er deaktiveret.
- Brug knappen **Tilføj en app** til at integrere en app, der enten er oprettet i Microsoft Power Apps eller en tredjepart, på siden. Denne indstilling er kun tilgængelig, når funktionen [Gemte visninger](saved-views.md) er aktiveret. 
- Brug værktøjet **Ryd** for at nulstille siden til dens installerede standardtilstand. Alle tilpasninger på den aktuelle side ryddes. Denne handling kan ikke fortrydes. Derfor skal du kun bruge dette værktøj, hvis du er sikker på, at du vil nulstille siden. Når funktionen **Gemte visninger** er slået til, rydder dette værktøj brugertilpasningerne for den aktuelle visning.
- Brug værktøjet **Importér** til at indlæse en personlig tilpasning fra en fil, som du eller en anden tidligere har oprettet. 

    - Når funktionen **Gemte visninger** er slået fra, kan du vælge, om du vil tilføje eller erstatte eksisterende brugertilpasninger med de tilpasninger, der importeres for siden. Denne handling kan ikke fortrydes. Når du har importeret personlige tilpasninger, skal du derfor manuelt fjerne eller fortryde de ændringer, du ikke har brug for.
    - Når funktionen **Gemte visninger** er slået til, bliver de importerede tilpasninger en visning på siden. Hvis visningen allerede findes, får du mulighed for at springe importen over, erstatte den aktuelle visning, der har det samme navn, eller omdøbe den importerede visning.

- Brug værktøjet **Eksportér** til at gemme dine personlige indstillinger for siden i en fil. Du kan derefter dele dine tilpasninger med andre brugere. Disse brugere skal kun importere filen, der indeholder dine personlige indstillinger for siden. Når funktionen **Gemte visninger** er slået til, gemmer dette værktøj den aktuelle visning i en fil til deling.
- Vælg knappen **Luk** for at lukke værktøjslinjen **Brugertilpasning** og sætte siden tilbage til dens tidligere interaktive tilstand.

Når værktøjslinjen **Brugertilpasning** bruges, træder dine personlige indstillinger i kraft, så snart du foretager dem. Men hvis funktionen [Gemte visninger](saved-views.md) er slået til, skal du eksplicit gemme tilpasninger i en visning, som du vælger.

I nogle tilfælde vises et hængelåsikon ud for en element, når du vælger et værktøj. Dette symbol angiver, at du ikke kan redigere egenskaberne for det element, der er relateret til det valgte værktøj, fordi ændringer af disse egenskaber vil forhindre, at siden fungerer korrekt.

### <a name="adding-tiles-lists-and-links-to-a-workspace"></a>Tilføje felter, lister og links i et arbejdsområde

For nogle sider, der indeholder lister, er tilpasningsfunktionen **Føj til arbejdsområde** tilgængelig i gruppen **Personaliser** under fanen **Indstillinger** i handlingsruden. Denne funktion giver dig mulighed for at skubbe relevante oplysninger fra den aktuelle liste til et bestemt arbejdsområde. De oplysninger, der vises i arbejdsområdet, kan være baseret på enten hele listen eller en filtreret og sorteret version af listen. Du kan også angive, om oplysningerne skal vises i arbejdsområdet som en liste, et oversigtsfelt, der kan vise antallet af elementer på listen, eller som et link.

> [!NOTE]
> Hvis funktionen [Gemte visninger](saved-views.md) er aktiveret, er det indhold, du skubber til et arbejdsområde, direkte knyttet til en visning. Forespørgslen i visningen bruges til at hente data i arbejdsområdet, og det tilhørende felt eller link i arbejdsområdet åbner siden i denne visning, så visningens forespørgsel og tilpasninger anvendes på den. Hvis visningen opdateres, justeres de tilsvarende arbejdsområdeelementer efter den nye visningsdefinition.

[![Føj til arbejdsområde](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Hvis du vil føje en liste til et arbejdsområde, skal du først sortere eller filtrere listen på siden, så den viser oplysningerne, som de skal vises i arbejdsområdet. (Hvis funktionen **Gemte visninger** er slået til, kan du ikke fortsætte, før du har gemt en visning, der har disse betingelser). Vælg derefter **Føj til arbejdsområde**. Vælg et arbejdsområde, og vælg derefter **Liste** i feltet **Præsentation**. Når du har valgt **Konfigurer**, åbnes en dialogboks, hvor du kan vælge de kolonner, der skal vises på listen i arbejdsområdet. Du kan også angive, hvilken label der bruges til listen i arbejdsområdet.
- Hvis du vil føje et felt til et arbejdsområde, skal du først filtrere listen på siden, så den viser de data, du vil opsummere eller ønsker hurtig adgang til. (Hvis funktionen **Gemte visninger** er slået til, kan du ikke fortsætte, før du har gemt en visning, der har disse betingelser). Vælg derefter **Føj til arbejdsområde**. Vælg et arbejdsområde, og vælg derefter **Felt** i feltet **Præsentation**. Når du har valgt **Konfigurer**, åbnes en dialogboks, hvor du kan angive, hvilken label der skal bruges til feltet i arbejdsområdet. Du kan også angive, om feltet skal vise en optælling. Når feltet er føjet til arbejdsområdet, kan du vælge det for at åbne den aktuelle side fra arbejdsområdet. Du kan derefter få vist den filtrerede liste, der er knyttet til feltet.
- Hvis du vil føje et link til et arbejdsområde, skal du først filtrere listen på siden, så den viser dataene, du er interesseret i. (Hvis funktionen **Gemte visninger** er slået til, kan du ikke fortsætte, før du har gemt en visning, der har disse betingelser). Vælg derefter **Føj til arbejdsområde**. Vælg et arbejdsområde, og vælg derefter **Link** i feltet **Præsentation**. Når du har valgt **Konfigurer**, åbnes en dialogboks, hvor du kan angive, hvilken label der skal bruges til linket. Du kan også vælge at angive en label til en ny sektion, der indeholder dette link.

Når du har tilføjet en liste, et felt eller link i et arbejdsområde, kan du åbne dette arbejdsområde og omarrangere elementerne i det, som du vil.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Føje en oversigt fra et arbejdsområde til et dashboard

Nogle arbejdsområder indeholder optællingsfelter (dvs. felter med angivelse af antal), og du kan også få vist disse felter i dashboardet. Højreklik på et antalsfelt i et arbejdsområde, vælg **Personaliser**, og vælg derefter **Fastgør til dashboard** i feltets egenskabsvindue. Næste gang du åbner og opdaterer dashboardet, vises optællingen under navigationsfeltet for dette arbejdsområde. Du kan vælge denne optælling for at gå direkte til de data, den repræsenterer.

### <a name="personalizing-your-dashboard"></a>Tilpasning af dit dashboard

Dashboardet er ofte den første side, du ser, når du åbner appen. Den kan tilpasses som enhver anden side i systemet ved hjælp af de samme mekanismer, der beskrives tidligere i dette emne. 

> [!WARNING]
> Når du i øjeblikket skjuler indhold på dashboardet, er det vigtigt, at du tilpasser et felt direkte og ikke om afstanden omkring det. Hvis du skjuler gruppen omkring et felt, kan der være uventede resultater, hvis der tilføjes flere felter senere, eller hvis systemet skifter til et andet sprog.

En entydig tilpasningsfunktion, der er tilgængelig på dashboardet, er muligheden for at tilføje felter. 

- Hvis funktionen **Helsides apps** er deaktiveret, tilføjer du et nyt felt ved at højreklikke på et element på dashboardet og derefter vælge **Tilføj et arbejdsområde**. Der oprettes et nyt felt i arbejdsområdet i bunden af dashboardet. Du kan omdøbe dette nye arbejdsområdefelt, som du vil. Du kan også føje lister, felter og links til arbejdsområdet som beskrevet i sektionen [Tilføje felter, lister og links i et arbejdsområde](personalize-user-experience.md#adding-tiles-lists-and-links-to-a-workspace) i dette emne.
- Hvis funktionen **Helsides apps** er aktiveret, tilføjer du et nyt felt ved at højreklikke på et element på dashboardet og derefter vælge **Tilføj en app**. Vælg i dialogboksen, om du vil tilføje et felt i et nyt arbejdsområde eller i et felt med indhold fra Power Apps eller et websted. Følg derefter trinnene for at konfigurere den valgte indstilling. Der oprettes et nyt felt i bunden af dashboardet. 

## <a name="sharing-personalizations"></a>Deling af tilpasninger

Når du har tilpasset en side, kan du dele dine tilpasninger med andre brugere ved at eksportere den tilpassede side. Du kan derefter bede andre brugere om at importere tilpasningsfilen. Alternativt kan du give tilpasningerne til en bruger med administratorrettigheder. Den bruger kan derefter anvende din tilpasningsfil på mange brugere samtidigt ved hjælp af administrationssiden **Tilpasning**.

## <a name="administration-of-personalizations"></a>Administration af brugertilpasninger

Siden **Tilpasning** er den centrale hub til administration af personlige indstillinger på et organisationsniveau. Indholdet og egenskaberne på denne side afhænger af, om funktionen **Gemte visninger** er blevet aktiveret.

For kunder, der har aktiveret funktionen **Gemte visninger** skal du se afsnittet "Administrere visninger globalt" i emnet [Gemte visninger](saved-views.md).

For kunder, der endnu ikke har aktiveret funktionen [Gemte visninger](saved-views.md), indeholder denne side fire faner:

- **Anvend** – Du kan importere eller vælge en tilpasning for en eller flere brugere. For at anvende en tilpasning på en eller flere brugere skal du først vælge en rolle og brugere, der har denne rolle. Vælg derefter en eksisterende tilpasning, der skal anvendes på de brugere, du har valgt, eller importér en tilpasningsfil. Tilpasningen valideres og anvendes på alle de markerede brugere, næste gang de åbner den valgte side.
- **Slet** – Du kan slette alle tilpasninger for en side eller et arbejdsområde for en eller flere brugere. Vælg først en side eller et arbejdsområde for at se en liste over de brugere, der har tilpasset siden eller området. Vælg de brugere, der skal have ryddet tilpasninger for siden eller arbejdsområdet, og vælg derefter **Ryd**. Alle tilpasninger, som de valgte brugere har anvendt på den valgte side eller det valgte arbejdsområde, slettes. Denne handling kan ikke fortrydes. Hvis der er gemt en tilpasning for siden eller arbejdsområdet, kan denne tilpasning dog importeres igen.
- **Brugere** – Vælg en bruger for at få vist listen over sider, som brugeren har tilpasset. Du kan derefter aktivere eller deaktivere den valgte brugers mulighed for at bruge personlige tilpasninger for bestemte sider eller for hele systemet. Du kan også importere, eksportere eller rydde en tilpasning for brugeren. Derudover kan du nulstille billedforklaringer til funktioner for brugeren. Hvis brugeren i så fald tidligere har lukket pop op-vinduer, der introducerede nye funktioner, vises de igen, næste gang brugeren støder på disse funktioner.
- **System** - Du kan midlertidigt deaktivere tilpasninger for alle brugere i systemet. I dette tilfælde slettes alle tilpasninger for alle brugere, og alle sider nulstilles til deres standardtilstand. Hvis du senere aktiverer tilpasninger igen, anvendes alle tilpasninger igen. Du kan også permanent slette alle tilpasninger for alle brugere i systemet. Det er ikke muligt at gendanne tilpasninger, som er blevet slettet. Før du udfører denne opgave, skal du derfor sørge for at eksportere de brugertilpasninger, som du eventuelt vil bruge senere.

## <a name="personalizing-inventory-dimensions"></a>Tilpasning af lagerdimensioner

Når du tilpasser opsætningen af lagerdimensioner på en side, skal du overveje de indstillinger, der er oprettet ved hjælp af indstillingen **Vis dimension**. Du kan f.eks. bruge personlige indstillinger til at skjule en kolonne for batchnummer-lagerdimensionen, men kolonnen vises, næste gang siden åbnes. Dette sker, fordi indstillingen **Dimensionsvisning** styrer de lagerdimensionskolonner, der vises. Indstillingerne i **Dimensionsvisning** gælder på tværs af alle sider og tilsidesætter den tilpassede opsætning af lagerdimensionsfelter på individuelle sider.

Hvis du derfor i det foregående eksempel ikke ønsker, at kolonnen for batchnummer-lagerdimensionen skal vises på en side, skal du rydde dimensionen som en del af indstillingen **Vis dimensioner** for denne side.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]