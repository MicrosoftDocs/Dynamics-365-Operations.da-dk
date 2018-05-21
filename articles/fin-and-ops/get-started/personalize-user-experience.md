---
title: Tilpasse brugeroplevelsen
description: I dette emne forklares det, hvordan du kan tilpasse Microsoft Dynamics 365 for Finance and Operations.
author: TLeforMicrosoft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 7a828090fa34eb96d2b557eb06e48ad05b421ae8
ms.openlocfilehash: 3d969069dd5f447b449df84b097527d3814aa338
ms.contentlocale: da-dk
ms.lasthandoff: 11/20/2017

---

# <a name="personalize-the-user-experience"></a>Tilpasse brugeroplevelsen

[!include [banner](../includes/banner.md)]

I dette emne forklares det, hvordan du kan tilpasse Microsoft Dynamics 365 for Finance and Operations.

Der findes mange typer tilpasninger i Dynamics 365 for Finance and Operations. Nogle tilpasninger er valg, du foretager på en liste over indstillinger på en konfigurationsside. Nogle tilpasninger er implicitte, f.eks. holder Finance and Operations styr på bredden af kolonnerne i gitteret, hvis du vil justere dem, og tilstanden udvidet/minimeret for oversigtspaneler. Andre tilpasninger er eksplicitte. Når det gælder eksplicitte tilpasninger, aktiverer du en interaktiv tilpasningstilstand og ændrer udseendet af en side ved direkte at styre den måde, hvorpå elementer vises eller fungerer på siden. 

Alle tilpasninger af enhver type, som en bruger foretager i Finance and Operations, gælder kun for den bruger, uanset det firma, brugeren interagerer med. Ændringer, som en bruger foretager på en side, påvirker ikke andre brugere i systemet.

## <a name="system-wide-options-for-the-current-user"></a>Systemindstillinger for den aktuelle bruger
I navigationspanelet finder du et tandhjulsbillede, der kaldes menuknappen **Indstillinger**. Når du åbner menuen **Indstillinger**, vises en række valgmuligheder. Hvis du vælger **Indstillinger**, åbnes brugersiden **Indstillinger**. Der kan finde fire faner med forskellige muligheder: 

-   **Visuel** - Bruges til at vælge et farvetema og standardstørrelsen på elementer på siderne.
-   **Indstillinger** - Her kan du angive standarder, for hver gang du åbner Finance and Operations, herunder firma, første side og standardtilstand for visning/redigering (der bestemmer, om en side er låst til visning eller åben til redigering, hver gang du åbner den). Du kan også finde sprog, tidszone og dato, klokkeslæt samt formatindstillinger for tal. Slutteligt indeholder denne side en række forskellige indstillinger, der varierer fra version til version.
-   **Firma** - Bruges til at angive dit bruger-id og andre firmarelaterede indstillinger.
-   **Arbejdsgang** - Dette er stedet, hvor du kan vælge indstillinger, der er relateret til arbejdsgangen.

## <a name="implicit-personalizations"></a>Implicitte tilpasninger
Implicitte tilpasninger er de tilpasninger, som du udfører ved blot at interagere med visse kontrolelementer, som husker deres aktuelle tilstand for synlighed. 

- **Gitterkolonner** - Du kan justere bredden på en kolonne på en liste ved at markere størrelseslinjen til venstre eller højre for kolonneoverskriften og skubbe den mod venstre eller højre til den ønskede bredde. Finance and Operations gemmer den bredde, du ville have, og viser denne kolonne med den bredde, hver gang du åbner siden med den liste. 

- **Oversigtspaneler** - Nogle sider har udvidelige sektioner, der kaldes *oversigtspaneler*. Finance and Operations gemmer, hvilke oversigtspaneler du har udvidet, og hvilke oversigtspaneler du har skjult. Hver gang du vender tilbage til siden, bliver disse oversigtspaneler udvidet eller skjult baseret på sidste gang, du har brugte dem. I denne artikel gennemgår vi, hvordan du ændrer rækkefølgen af sektionerne i oversigtspanelet. I nogle tilfælde kan du ved at skjule et oversigtspanel forbedre ydeevnen, fordi Finance and Operations ikke behøver at hente oplysningerne for dette oversigtspanel, før oversigtspanelet er udvidet. 

- **Faktabokse** - Nogle sider har en sektion, der kaldes en rude med *faktaboks*. Denne rude indeholder skrivebeskyttede oplysninger, der er relateret til sidens aktuelle emne. Hver sektion i ruden Faktaboks kaldes en Faktaboks. Du kan udvide eller skjule en faktaboks, og Finance and Operations gemmer dine indstillinger. I nogle tilfælde kan du ved at skjule en faktaboks forbedre ydeevnen, fordi Finance and Operations ikke behøver at hente oplysningerne for denne faktaboks, før faktaboksen er udvidet.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Eksplicitte tilpasninger ved hjælp af værktøjslinjen Brugertilpasning
Hver enkelt person og hvert enkelt firma har sit eget syn på, hvilke data der er vigtigst for dem, hvilke data der ikke er nødvendige for den måde, de driver deres forretning på. Muligheden for at tilpasse den måde, dine oplysninger er arrangeret på, interageret med eller endda skjult, er helt afgørende for at kunne gøre Finance and Operations til en personlig og produktiv oplevelse. 

Eksplicitte tilpasninger er de tilpasninger, som du eksplicit udfører med det formål at ændre udseende eller funktionsmåde for et element eller en side, ved at vælge en tilpasningsmenu. Den mest grundlæggende type af eksplicit brugertilpasning er, hvor du højreklikker på et element og vælger **Tilpas**. (Bemærk, at ikke alle elementer på din side kan tilpasses). Når du vælger denne metode for tilpasning, kan du se elementets egenskabsvindue. 

[![Tilpasning af et elements egenskaber](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Du tilpasser et element på din side på denne måde, hvis du blot vil ændre elementets etiket, skjule elementet, så det ikke vises på siden (dette ændringer ikke nogen data, du får blot ikke vist oplysningerne), medtage oplysninger i oversigtssektionen for oversigtspaneler (hvis elementet er et oversigtspanel), springe feltet over under tabulering eller gøre det således, at dataene ikke kan ændres, ved at markere dem som "Rediger ikke." 

Når du vil flytte eller skjule elementer eller foretage flere ændringer, kan du bruge værktøjslinjen Brugertilpasning, der er tilgængelig fra elementvinduet Egenskaber. Det gør du ved at vælge **Tilpas denne formular**. Værktøjslinjen Brugertilpasning er også tilgængelig i formularens handlingsrude under gruppen **Personaliser** under fanen **Indstillinger**. Vælg **Personaliser denne formular**, så får du vist værktøjslinjen Brugertilpasning. 

[![Værktøjslinjen Brugertilpasning](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Værktøjslinjen Brugertilpasning har en række tilpasningshandlinger. 

- Vælg værktøjet **Marker**, når du markere og ændre egenskaberne for mange elementer én ad gangen. Klik først på markeringsværktøjet, og klik derefter på det element, hvis egenskaber du vil ændre. Når du vælger et element, åbnes elementets egenskabsvindue, og du kan redigere egenskaberne for det element. Du kan gentage processen for andre formularelementer, der kan tilpasses. I nogle tilfælde kan du vælge et element og se, at nogle af egenskaberne ikke kan ændres. Det betyder, at Finance and Operations ikke lader dig ændre den egenskab på grund af den måde, det aktuelle element bruges på. Du kan f.eks. ikke skjule et felt, der er obligatorisk. 

- Vælg værktøjet **Flyt**, når du vil vælge og flytte et element til et andet sted inden for den aktuelle gruppe elementer. (Du kan ikke flytte et element uden for dets overordnede gruppe). Klik først på værktøjet Flyt, og klik derefter på det element, hvis du vil flytte. Når du klikker på det element, du vil flytte, scanner Finance and Operations formularen for at bestemme, hvor dette element kan flyttes til, og oprette en række "slipzonerne", der vises som en farvet, fed streg ud for det område, hvor elementet kan blive slippes, når du trækker elementet omkring i den aktuelle gruppe. 

- Vælg værktøjet **Skjul** for at markere og skjule et element. Hvis du vil skjule et element, skal du blot vælge værktøjet Skjul og klikke på det element, du vil skjule. Når du vælger værktøjet Skjul, bliver alle elementer, der aktuelt er skjulte, synlige og vises i en nedtonet beholder, så du kan vælge elementet for at få det vist. 

- Vælg **markeringsværktøjet** for at se, hvordan siden vil se ud, hvis de valgte elementer er skjulte. 

- Vælg værktøjet **Oversigt**, når du ønsker at få vist et numerisk felt eller strengfelt i oversigtsområdet i oversigtspanelet. Værktøjet Oversigt gælder kun felter, der er indeholdt i en oversigtspanelsektion. Når du vælger værktøjet Oversigt, viser Finance and Operations alle felter, der er valgt som oversigtsfelter, ved at omslutte dem med en nedtonet beholder. Du kan interaktivt tilføje og fjerne felter fra en oversigtspanelets oversigt ved at klikke på feltet. 

- Vælg værktøjet **Spring over** for at fjerne et element fra sidens tastaturtabuleringsrækkefølge. Når du vælger værktøjet Spring over, vises alle aktuelt udeladte elementer i en nedtonet beholder, så du kan vælge dem igen for at gøre dem til en del af tabuleringsrækkefølgen ved at vælge et element, der er sprunget over. 

- Vælg værktøjet **Rediger**, når du vil markere et element som et, der kan *redigeres* eller *ikke redigeres*. Når du vælger værktøjet Rediger, vises alle aktuelle elementer, der ikke kan redigeres, i en nedtonet beholder, så du kan vælge dem og gøre dem redigerbare. Bemærk, at nogle af felterne er obligatoriske og kan ikke gøres til nogle, der ikke kan redigeres. Disse felter vises med et hængelåsikon ved siden af. 

- Vælg værktøjet **Tilføj** for at føje et felt til din side. Med værktøjet Tilføj kan du oprette et nyt felt, men du kan tilføje felter, der er en del af den aktuelle sidedefinition, men som ikke vises på siden. Når du vælger værktøjet Tilføj, skal du først vælge den gruppe eller det område, hvor du vil tilføje et felt. En dialogboks viser listen over felter, der er relateret til den sektion, du har valgt. I denne dialogboks kan du vælge et eller flere felter, der skal tilføjes, og klikke på **Indsæt**. Hvis du senere vil fjerne et felt, som du tidligere har tilføjet, skal du gentage processen, men blot fjerne markeringen i det felt, du tidligere har tilføjet. 

- Vælg knappen **Administrer** for at se en liste over administrationsindstillinger, der er relateret til alle tilpasninger til den aktuelle side. 

- Vælg **Ryd** for at nulstille siden til dens installerede standardstatus. Alle tilpasninger på den aktuelle side slettes. Der er ingen fortrydelseshandling, så brug kun denne indstilling, når du er sikker på, at du vil nulstille din side. 

- Vælg **Importer** for at bruge en personlig tilpasning fra en tilpasningsfil, som du eller en anden tidligere har oprettet for denne side. Import af en tilpasning rydder eventuelle tilpasninger, som du har udført på hele siden, og i stedet bruges alle tilpasninger fra den valgte fil. Hvis du vil gemme eller dele en tilpasning, skal du vælge indstillingen **Eksportér** for at gemme tilpasningerne i en fil. 

- Vælg knappen **Luk** for at lukke værktøjslinjen og sætte siden tilbage til dens tidligere interaktive tilstand. 

Når du bruger værktøjslinjen Brugertilpasning, er lagring implicit. Dine tilpasninger aktiveres, så snart du foretager dem, og det er ikke nødvendigt at klikke på knappen **Gem**. I nogle tilfælde ser du et hængelåsikon ud for elementet, når du vælger et værktøj. Det betyder, at for at få siden til at fungere korrekt kan du ikke redigere de egenskaber, der er relateret til det valgte værktøj. Når værktøjslinjen Brugertilpasning er åbnet, bliver siden ikke-interaktiv. Du kan ikke indtaste data eller udvide eller skjule sektioner.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Eksplicit brugertilpasning: Tilføje et felt eller en liste til et arbejdsområde
Nogle sider med lister har en yderligere brugertilpasningsfunktion i handlingsruden under gruppen **Personaliser** under fanen **Indstillinger**. Vælg **Føj til arbejdsområde** for at åbne den rulleliste, der gør det muligt at vise oplysninger på den aktuelle liste (filtreret og sorteret eller standard) i et arbejdsområde som en liste eller et oversigtsfelt (der kan bruges til at vise antallet af elementer på listen). 

[![Føj til arbejdsområde](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Hvis du vil føje en liste til et arbejdsområde, skal du først sortere eller filtrere listen med de oplysninger, du gerne vil se i dit arbejdsområde, og derefter vælge dialogboksen **Føj til arbejdsområde**. Vælg derefter det ønskede arbejdsrum, og vælg **Liste** på rullelisten **Præsentation**. Når du vælger **Liste** , åbnes en dialogboks, hvor du kan vælge de kolonner, du vil se på listen, og etiketten til listen, som den vises i arbejdsområdet. 

Hvis du vil føje et felt til et arbejdsområde, skal du først filtrere listen for at repræsentere de data, du vil opsummere (eller ønsker hurtig adgang til). Åbn derefter menuen **Føj til arbejdsområde** i dialogboksen. Vælg derefter det ønskede arbejdsrum, og vælg **Felt** i menuen **Præsentation** på rullelisten. Når du vælger **Felt**, åbnes en dialogboks, hvor du kan angive en feltetiket og beslutte, om feltet skal vise en optælling. Når feltet er placeret i et arbejdsområde, giver feltet dig mulighed for at åbne den aktuelle side i arbejdsområdet og vise listen over de oplysninger, der er relateret til feltet. 

Når din liste eller dit felt er føjet til et arbejdsområde, kan du derefter åbner det pågældende arbejdsområde og ændre rækkefølgen på listen eller feltet inden for den gruppe, hvor listen eller feltet var placeret.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Eksplicit brugertilpasning: Føje en oversigt fra et arbejdsområde til et dashboard
Nogle arbejdsområder indeholder optællingsfelter (felter med tal på dem), som du også gerne vil se på dashboardet. Højreklik på et antalsfelt i et arbejdsområde, vælg **Tilpas**, og vælg derefter **Fastgør til dashboard**. Næste gang du navigerer til (og opdaterer) det valgte dashboard, kan du se den optælling under dette arbejdsområdes navigationsfelt på dashboardet.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Eksplicit brugertilpasning: tilpasning af dashboardet
Dashboardet er ofte den første side, du ser, når du åbner Finance and Operations. Du kan tilpasse dashboardet for at omdøbe dit arbejdsområdes navigationsfelter, for kun at vise de felter, du gerne vil se, for at omdøbe felterne eller for at arrangere felterne i den rækkefølge, du foretrækker at se dem i. 

Hvis du vil tilpasse dashboardet, skal du vælge et felt og højreklikke på det for at åbne en genvejsmenu. Vælg **Tilpas** i genvejsmenuen. Hvis det valgte felter er, som du gerne vil skjule eller omdøbe eller overspringe, kan du foretage denne ændring direkte i det egenskabsvindue, der vises. Hvis du vil arrangere felterne, skal du vælge **Tilpas denne formular** i vinduet Egenskaber for at åbne værktøjslinjen Brugertilpasning. Du kan derefter bruge værktøjet **Flyt** til at arrangere felterne.

## <a name="administration-of-personalization"></a>Administration af brugertilpasning
Når du har tilpasset en side, kan du dele dine tilpasninger med andre brugere ved at eksportere den tilpassede side. Derefter kan du bede de andre brugere om at gå til den tilpassede side og importere den tilpasningsfil, du har oprettet, eller du kan give dine personlige indstillinger til en bruger med administratorrettigheder, som derefter kan anvende tilpasningsfilen på mange brugere på én gang.

Brugere, der har administratorrettigheder, kan også administrere tilpasninger for andre brugere på siden **Brugertilpasning**. Denne side indeholder fire faner: 

- **Anvend** – Du kan importere eller vælge en tilpasning for en eller flere brugere. Hvis du vil anvende en tilpasning på en eller flere brugere, skal du vælge en rolle og brugere i den pågældende rolle. Vælg derefter en eksisterende tilpasning, eller importér en tilpasningsfil, der skal anvendes på de brugere, du har valgt. Tilpasningen valideres og anvendes på alle de markerede brugere, næste gang de åbner den valgte side.

- **Slet** – Du kan slette tilpasninger af sider eller arbejdsområder for en eller flere brugere. Vælg en side for at se listen over brugere, der har tilpasset denne side. Vælg de brugere, der skal have ryddet tilpasninger for den pågældende side, og vælg derefter **Ryd**. Alle tilpasninger, som de markerede brugere har anvendt på den valgte side eller det valgte arbejdsområde, slettes. Denne handling kan ikke fortrydes. Hvis der er en gemt tilpasning på siden eller i arbejdsområdet, kan denne tilpasning dog importeres igen.

- **Administration pr. bruger** – Vælg en bruger for at få vist listen over sider, denne person har tilpasset.  Du kan derefter vælge at aktivere eller deaktivere deres evne til at udnytte personlige indstillinger for bestemte sider eller for hele systemet.  Du kan også importere, eksportere eller rydde en tilpasning for denne bruger.

- **System** - Du kan midlertidigt deaktivere alle tilpasninger for alle brugere i systemet. Hvis du gør det, bliver tilpasningerne ikke slettet, men alle sider nulstilles til deres standardtilstand for alle brugere. Hvis du senere aktiverer tilpasningen igen, anvendes alle tilpasninger igen. Du kan også permanent slette alle tilpasninger for alle brugere i systemet. Sørg for at eksportere alle tilpasninger, som du måske får brug for senere, før du udfører dette trin, for det er ikke muligt at gendanne slettede tilpasninger senere. 

## <a name="personalization-of-inventory-dimensions"></a>Tilpasning af lagerdimensioner

Når du tilpasser opsætningen af lagerdimensioner på en side, skal du overveje de indstillinger, der er oprettet ved hjælp af indstillingen **Vis dimension**. F.eks. hvis du benytter tilpasning for at skjule en kolonne for batchnummer-lagerdimensionen, og kolonnen vises, næste gang siden åbnes, kan det skyldes, at indstillingerne for dimensionsvisning styrer, hvilke lagerdimensionskolonner der vises. 

Indstillingerne for dimensionsvisning gælder på tværs af alle sider, og disse indstillinger tilsidesætter den tilpassede opsætning af lagerdimensionsfelter på individuelle sider. 

I eksemplet med batchnummer-lagerdimensionen, skal denne dimension fjernes som en del af indstillingen **Vis dimensioner** for tabellen, hvis denne kolonne ikke skal vises. Denne ændring vil desuden gælde ikke kun for en bestemt side, men på tværs af alle sider.

