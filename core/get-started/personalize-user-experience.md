---
title: Tilpasse brugeroplevelsen
description: I denne artikel forklares det, hvordan du kan tilpasse Microsoft Dynamics 365 for Operations.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserSetup
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 734bf8a5cd71d218942e1a57fbb6af8fef4dc998
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="personalize-the-user-experience"></a>Tilpasse brugeroplevelsen

[!include[banner](../includes/banner.md)]


I denne artikel forklares det, hvordan du kan tilpasse Microsoft Dynamics 365 for Operations.

Der findes mange typer tilpasninger i Microsoft Dynamics 365 for Operations. Nogle tilpasninger er valg, du foretager på en liste over indstillinger på en konfigurationsside. Nogle tilpasninger er implicitte, f.eks. holder Dynamics 365 for Operations styr på bredden af kolonnerne i gitteret, hvis du vil justere dem, og tilstanden udvidet/minimeret for oversigtspaneler. Andre tilpasninger er eksplicitte. Når det gælder eksplicitte tilpasninger, aktiverer du en interaktiv tilpasningstilstand og ændrer udseendet af en side ved direkte at styre den måde, hvorpå elementer vises eller fungerer på siden. 

Alle tilpasninger af enhver type, som en bruger foretager i Dynamics 365 for Operations, gælder kun for den bruger, uanset det firma, brugeren interagerer med. Ændringer, som en bruger foretager på en side, påvirker ikke andre brugere i systemet.

## <a name="systemwide-options-for-the-current-user"></a>Systemindstillinger for den aktuelle bruger
I navigationspanelet finder du et tandhjulsbillede, der kaldes menuknappen **Indstillinger**. Når du åbner menuen **Indstillinger**, vises en række valgmuligheder. Hvis du vælger **Indstillinger**, åbnes brugersiden **Indstillinger**. Der findes du fire indstillingsfaner: **Visuel**, **Indstillinger**, **Firma** og **Arbejdsgang**.

-   **Visuel:**Bruges til at vælge et farvetema og standardstørrelsen på elementer på siderne.
-   **Indstillinger:** Her kan du angive standarder, for hver gang du åbner Dynamics 365 for Operations, herunder firma, første side og standardtilstand for visning/redigering (der bestemmer, om en side er låst til visning eller åben til redigering, hver gang du åbner den). Du kan også finde sprog, tidszone og dato, klokkeslæt samt formatindstillinger for tal. Slutteligt indeholder denne side en række forskellige indstillinger, der varierer fra version til version.
-   **Firma:**Bruges til at angive dit bruger-id og andre firmarelaterede indstillinger.
-   **Arbejdsgang:**Dette er stedet, hvor du kan vælge indstillinger, der er relateret til arbejdsgangen.

## <a name="implicit-personalizations"></a>Implicitte tilpasninger
Implicitte tilpasninger er de tilpasninger, som du udfører ved blot at interagere med visse kontrolelementer, som husker deres aktuelle tilstand for synlighed. 

**Gitterkolonner:** Du kan justere bredden på en kolonne på en liste ved at markere størrelseslinjen til venstre eller højre for kolonneoverskriften og skubbe den mod venstre eller højre til den ønskede bredde. Dynamics 365 for Operations gemmer den bredde, du ville have, og viser denne kolonne med den bredde, hver gang du åbner siden med den liste. 

**Oversigtspaneler:** Nogle sider har udvidelige sektioner, der kaldes oversigtspaneler. Dynamics 365 for Operations gemmer, hvilke oversigtspaneler du har udvidet, og hvilke oversigtspaneler du har skjult. Hver gang du vender tilbage til siden, bliver disse oversigtspaneler udvidet eller skjult baseret på sidste gang, du har brugte dem. I denne artikel gennemgår vi, hvordan du ændrer rækkefølgen af sektionerne i oversigtspanelet. I nogle tilfælde kan du ved at skjule et oversigtspanel forbedre ydeevnen, fordi Dynamics 365 for Operations ikke behøver at hente oplysningerne for dette oversigtspanel, før oversigtspanelet er udvidet. 

**Faktabokse:** Nogle sider har en sektion, der kaldes en rude med faktaboks. Denne rude indeholder skrivebeskyttede oplysninger, der er relateret til sidens aktuelle emne. Hver sektion i ruden Faktaboks kaldes en Faktaboks. Du kan udvide eller skjule en faktaboks, og 365 for Operations gemmer dine indstillinger. I nogle tilfælde kan du ved at skjule en faktaboks forbedre ydeevnen, fordi Dynamics 365 for Operations ikke behøver at hente oplysningerne for denne faktaboks, før faktaboksen er udvidet.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Eksplicitte tilpasninger ved hjælp af værktøjslinjen Brugertilpasning
Hver enkelt person og hvert enkelt firma har sit eget syn på, hvilke data der er vigtigst for dem, hvilke data der ikke er nødvendige for den måde, de driver deres forretning på. Muligheden for at tilpasse den måde, dine oplysninger er arrangeret på, interageret med eller endda skjult, er helt afgørende for at kunne gøre Dynamics 365 for Operations til en personlig og produktiv oplevelse. 

Eksplicitte tilpasninger er de tilpasninger, som du eksplicit udfører med det formål at ændre udseende eller funktionsmåde for et element eller en side, ved at vælge en tilpasningsmenu. Den mest grundlæggende type af eksplicit brugertilpasning er, hvor du højreklikker på et element og vælger **Tilpas**. (Bemærk, at ikke alle elementer på din side kan tilpasses). Når du vælger denne metode for tilpasning, kan du se elementets egenskabsvindue. 

[![Tilpasning af et elements egenskaber](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Du tilpasser et element på din side på denne måde, hvis du blot vil ændre elementets etiket, skjule elementet, så det ikke vises på siden (dette ændringer ikke nogen data, du får blot ikke vist oplysningerne), medtage oplysninger i oversigtssektionen for oversigtspaneler (hvis elementet er et oversigtspanel), springe feltet over under tabulering eller gøre det således, at dataene ikke kan ændres, ved at markere dem som "Rediger ikke." 

Når du vil flytte eller skjule elementer eller foretage flere ændringer, kan du bruge værktøjslinjen Brugertilpasning, der er tilgængelig fra elementvinduet Egenskaber. Det gør du ved at vælge **Tilpas denne formular**. Værktøjslinjen Brugertilpasning er også tilgængelig på formularens handlingsrude under gruppen Tilpas under fanen **Indstillinger**. Vælg **Tilpas denne formular**, hvorefter du ser værktøjslinjen Brugertilpasning. 

[![Værktøjslinjen Brugertilpasning](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Værktøjslinjen Brugertilpasning har en række tilpasningshandlinger. Vælg værktøjet **Marker**, når du markere og ændre egenskaberne for mange elementer én ad gangen. Klik først på markeringsværktøjet, og klik derefter på det element, hvis egenskaber du vil ændre. Når du vælger et element, åbnes elementets egenskabsvindue, og du kan redigere egenskaberne for det element. Du kan gentage processen for andre formularelementer, der kan tilpasses. I nogle tilfælde kan du vælge et element og se, at nogle af egenskaberne ikke kan ændres. Det betyder, at Dynamics 365 for Operations ikke lader dig ændre den egenskab på grund af den måde, det aktuelle element bruges på. Du kan f.eks. ikke skjule et felt, der er obligatorisk. 

Vælg værktøjet **Flyt**, når du vil vælge og flytte et element til et andet sted inden for den aktuelle gruppe elementer. (Du kan ikke flytte et element uden for dets overordnede gruppe). Klik først på værktøjet Flyt, og klik derefter på det element, hvis du vil flytte. Når du klikker på det element, du vil flytte, scanner Dynamics 365 for Operations formularen for at forstå, hvor dette element kan flyttes til, og oprette en række "slipzonerne", der vises som en farvet, fed streg ud for det område, hvor elementet kan blive slippes, når du trækker elementet omkring i den aktuelle gruppe. 

Vælg værktøjet **Skjul** for at markere og skjule et element. Hvis du vil skjule et element, skal du blot vælge værktøjet Skjul og klikke på det element, du vil skjule. Når du vælger værktøjet Skjul, bliver alle elementer, der aktuelt er skjulte, synlige og vises i en nedtonet beholder, så du kan vælge elementet for at få det vist. Vælg markeringsværktøjet for at se, hvordan siden vil se ud, hvis de valgte elementer er skjulte. Vælg værktøjet **Oversigt**, når du ønsker at få vist et numerisk felt eller strengfelt i oversigtsområdet i oversigtspanelet. Værktøjet Oversigt gælder kun felter, der er indeholdt i en oversigtspanelsektion. Når du vælger værktøjet Oversigt, viser Dynamics 365 for Operations alle felter, der er valgt som oversigtsfelter, ved at omslutte dem med en nedtonet beholder. Du kan interaktivt tilføje og fjerne felter fra en oversigtspanelets oversigt ved at klikke på feltet. 

Vælg værktøjet **Spring over** for at fjerne et element fra sidens tastaturtabuleringsrækkefølge. Når du vælger værktøjet Spring over, vises alle aktuelt udeladte elementer i en nedtonet beholder, så du kan vælge dem igen for at gøre dem til en del af tabuleringsrækkefølgen ved at vælge et element, der er sprunget over. 

Vælg værktøjet **Rediger**, når du vil markere et element som et, der kan redigeres eller ikke redigeres. Når du vælger værktøjet Rediger, vises alle aktuelle elementer, der ikke kan redigeres, i en nedtonet beholder, så du kan vælge dem og gøre dem redigerbare. Bemærk, at nogle af felterne er obligatoriske og kan ikke gøres til nogle, der ikke kan redigeres. Disse felter vises med et hængelåsikon ved siden af. 

Vælg værktøjet **Tilføj** for at føje et felt til din side. Med værktøjet Tilføj kan du oprette et nyt felt, men du kan tilføje felter, der er en del af den aktuelle sidedefinition, men som ikke vises på siden. Når du vælger værktøjet Tilføj, skal du først vælge den gruppe eller det område, hvor du vil tilføje et felt. En dialogboks viser listen over felter, der er relateret til den sektion, du har valgt. I denne dialogboks kan du vælge et eller flere felter, der skal tilføjes, og klikke på Indsæt. Hvis du senere vil fjerne et felt, som du tidligere har tilføjet, skal du gentage processen, men blot fjerne markeringen i det felt, du tidligere har tilføjet. 

Vælg knappen **Administrer** for at se en liste over administrationsindstillinger, der er relateret til alle tilpasninger til den aktuelle side. 

Vælg **Ryd** for at nulstille siden til dens installerede standardstatus. Alle tilpasninger på den aktuelle side slettes. Der er ingen fortrydelseshandling, så brug kun denne indstilling, når du er sikker på, at du vil nulstille din side. 

Vælg **Importer** for at bruge en personlig tilpasning fra en tilpasningsfil, som du eller en anden tidligere har oprettet for denne side. Import af en tilpasning rydder eventuelle tilpasninger, som du har udført på hele siden, og i stedet bruges alle tilpasninger fra den valgte fil. Hvis du vil gemme eller dele en tilpasning, skal du vælge indstillingen **Eksportér** for at gemme tilpasningerne i en fil. 

Vælg knappen **Luk** for at lukke værktøjslinjen og sætte siden tilbage til dens tidligere interaktive tilstand. 

Når du bruger værktøjslinjen Brugertilpasning, er lagring implicit. Dine tilpasninger aktiveres, så snart du foretager dem, og det er ikke nødvendigt at klikke på knappen **Gem**. I nogle tilfælde ser du et hængelåsikon ud for elementet, når du vælger et værktøj. Det betyder, at for at få siden til at fungere korrekt kan du ikke redigere de egenskaber, der er relateret til det valgte værktøj. Når værktøjslinjen Brugertilpasning er åbnet, bliver siden ikke-interaktiv. Du kan ikke indtaste data eller udvide eller skjule sektioner.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Eksplicit brugertilpasning: Tilføje et felt eller en liste til et arbejdsområde
Nogle sider med lister har en yderligere tilpasningsfunktion, der er tilgængelig i dens handlingsrude under gruppe Tilpas under fanen Indstillinger. Vælg **Føj til arbejdsområde** for at åbne den rulleliste, der gør det muligt at vise oplysninger på den aktuelle liste (filtreret og sorteret eller standard) i et arbejdsområde som en liste eller et oversigtsfelt (der kan bruges til at vise antallet af elementer på listen). 

[![Føj til arbejdsområde](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Hvis du vil føje en liste til et arbejdsområde, skal du først sortere eller filtrere listen med de oplysninger, du gerne vil se i dit arbejdsområde, og derefter vælge dialogboksen Føj til arbejdsområde. Vælg derefter det ønskede arbejdsrum, og vælg **Liste** på rullelisten Præsentation. Når du vælger **Liste** , åbnes en dialogboks, hvor du kan vælge de kolonner, du vil se på listen, og etiketten til listen, som den vises i arbejdsområdet. 

Hvis du vil føje et felt til et arbejdsområde, skal du først filtrere listen for at repræsentere de data, du vil opsummere (eller ønsker hurtig adgang til). Åbn derefter dialogboksen Føj til arbejdsområde. Vælg derefter det ønskede arbejdsrum, og vælg **Felt** på rullelisten Præsentation. Når du vælger **Felt**, åbnes en dialogboks, hvor du kan angive en feltetiket og beslutte, om feltet skal vise en optælling. Når feltet er placeret i et arbejdsområde, giver feltet dig mulighed for at åbne den aktuelle side i arbejdsområdet og vise listen over de oplysninger, der er relateret til feltet. 

Når din liste eller dit felt er føjet til et arbejdsområde, kan du derefter åbner det pågældende arbejdsområde og ændre rækkefølgen på listen eller feltet inden for den gruppe, hvor listen eller feltet var placeret.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Eksplicit brugertilpasning: Føje en oversigt fra et arbejdsområde til et dashboard
Nogle arbejdsområder indeholder optællingsfelter (felter med tal på dem), som du også gerne vil se på dashboardet. Højreklik på et optællingsfelt i et arbejdsområde, og vælg **Tilpas**. Vælg **Fastgør til dashboard**. Næste gang du navigerer til (og opdaterer) det valgte dashboard, kan du se den optælling under dette arbejdsområdes navigationsfelt på dashboardet.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Eksplicit brugertilpasning: tilpasning af dashboardet
Dashboardet er ofte den første side, du ser, når du åbner Dynamics 365 for Operations. Du kan tilpasse dashboardet for at omdøbe dit arbejdsområdes navigationsfelter, for kun at vise de felter, du gerne vil se, for at omdøbe felterne eller for at arrangere felterne i den rækkefølge, du foretrækker at se dem i. Hvis du vil tilpasse dashboardet, skal du vælge et felt og højreklikke på det for at åbne en genvejsmenu. Vælg **Tilpas** i genvejsmenuen. Hvis det valgte felter er, som du gerne vil skjule eller omdøbe eller overspringe, kan du foretage denne ændring direkte i det egenskabsvindue, der vises. Hvis du vil arrangere felterne, skal du vælge **Tilpas denne formular** i vinduet Egenskaber for at åbne værktøjslinjen Brugertilpasning. Du kan derefter bruge værktøjet Flyt til at arrangere felterne.

## <a name="administration-of-personalization"></a>Administration af brugertilpasning
Det er muligt at tilpasse en side og dele den med andre brugere ved blot at eksportere den tilpassede side og bede de andre brugere om at navigere til den tilpassede side og importere den tilpasningsfil, du har oprettet. Hvis en bruger har administratorrettigheder, kan de også administrere tilpasninger for andre brugere på siden **Konfiguration af brugertilpasning**. Gå til siden b. På siden **Brugertilpasning** er der to faner, hvor den ene har etiketten **System** og den anden **Brugere**. 

**System:** Det er stedet, hvor du midlertidigt kan deaktivere eller slå alle tilpasninger i systemet fra. Dette sletter ikke tilpasninger, men nulstiller i stedet alle formularer til deres standardtilstand. Du kan senere aktivere tilpasningen igen for at få alle tilpasninger anvendt igen på hver enkelt brugers formularer. Du kan også slette alle tilpasninger for alle brugere. Bemærk, at når du sletter brugertilpasninger, er der ingen mulighed for automatisk at aktivere brugertilpasninger igen fra systemet. Kontroller, at du har eksporteret de brugertilpasninger, som du eventuelt senere vil importere, før du udfører dette trin. 

**Brugere:** Det er stedet, hvor du for hver enkelt bruger bestemmer, om brugeren kan foretage implicitte eller eksplicitte brugertilpasninger. Du kan også bestemme, om hver bruger kan udføre implicitte eller eksplicitte brugertilpasninger på en bestemt formular. Endelig kan du importere eller eksportere eller slette en brugertilpasning for hver bruger. 

**Bemærk!** I dens oprindelige udgivelse tillader administration af brugertilpasning kun administration pr. bruger.




