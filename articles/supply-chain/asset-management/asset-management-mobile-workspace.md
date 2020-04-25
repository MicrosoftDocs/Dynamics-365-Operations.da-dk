---
title: Arbejdsområdet Styring af aktiver på mobilenheder
description: Dette emne indeholder oplysninger om arbejdsområdet Styring af aktiver på mobilenheder.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: 525f21d076027f1bf339e59fd0e346706044839c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216499"
---
# <a name="asset-management-mobile-workspace"></a>Arbejdsområdet Styring af aktiver på mobilenheder

[!include [banner](../../includes/banner.md)]


Dette emne indeholder oplysninger om arbejdsområdet Styring af aktiver på mobilenheder. I dette arbejdsområde kan brugerne se og oprette vedligeholdelsesanmodninger og arbejdsordrer. Brugere kan også få vist de tildelte job i arbejdsordrejob i en kalender- eller listevisning. Aktiver og arbejdssteder kan også ses og søges efter.


## <a name="overview"></a>Overblik

Styring af aktiver er et avanceret modul til administration af aktiver og arbejdsordrejob i Dynamics 365 Supply Chain Management. Med arbejdsområdet **Styring af aktiver** på mobilenheder kan brugerne hurtigt få vist arbejdsordrejob på en mobilenhed efter eget valg. Brugerne kan også oprette og administrere vedligeholdelsesanmodninger, opdatere livscyklustilstand og se detaljer om aktiver og arbejdssted ved hjælp af deres mobilenhed.

Med arbejdsområdet **Styring af aktiver** på mobilenheder kan brugerne udføre disse opgaver:

- Oprette, få vist og redigere vedligeholdelsesanmodninger, tage et billede eller vedhæfte et eksisterende billede til vedligeholdelsesanmodningen, ændre livscyklustilstanden for vedligeholdelsesanmodningen. 
- Oprette, få vist og redigere arbejdsordrer, tage et billede eller vedhæfte et eksisterende billede til arbejdsordren, ændre livscyklustilstanden for arbejdsordren, få vist arbejdsordrejob.
- Få vist tildelte arbejdsordrejob i en kalendervisning.
- Oprette, få vist og redigere arbejdsordrejob, opdatere aktivtællere, få vist vedligeholdelsestjekliste, få vist og redigere notater til arbejdsordrer, få vist de nødvendige værktøjer til arbejdsordrejobbet.
- Få vist eller søge efter et bestemt aktiv eller et arbejdssted.


## <a name="prerequisites"></a>Forudsætninger

Forudsætningerne varierer, afhængigt af hvilken version af Dynamics 365 Supply Chain Management der er installeret i organisationen.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-supply-chain-management"></a>Forudsætninger, hvis du bruger Microsoft Dynamics 365 Supply Chain Management 
Hvis Microsoft Dynamics 365 Supply Chain Management er installeret for organisationen, skal systemadministratoren publicere arbejdsområdet **Styring af aktiver** til mobilenheder. Du kan finde flere oplysninger under [Publicere et arbejdsområde til mobilenheder](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

## <a name="download-and-install-the-mobile-app"></a>Downloade og installere mobilappen
Download og installer Dynamics 365 for Unified Operations-mobilappen:

- [Til Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
- [Til iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Log på mobilappen
1. Start appen på din mobilenhed.

2. Angiv URL-adressen til din Dynamics 365.

3. Første gang du logger på, bliver du bedt om at angive brugernavn og adgangskode. Angiv dine legitimationsoplysninger.

4. Når du har logget på, vises de arbejdsområder, der er tilgængelige for din virksomhed. Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, skal du opdatere listen over arbejdsområder til mobilenheder.

![Figur 1](media/am-mobile-01.png)


## <a name="view-assigned-work-order-jobs-in-calendar-view"></a>Få vist tildelte arbejdsordrejob i en kalendervisning

1. På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.

2. Vælg **Min kalender over arbejdsordrejob**.

3. Vælg den dato, som du vil have vist arbejdsordrejob for. På listen kan du se aktiv-id'et og arbejdssteds-id'et for hvert arbejdsordrejob.

4. Vælg et arbejdsordrejob på listen for at se joboplysninger: oplysninger om aktiv og arbejdssted samt andre navigationslinks for at få vist **vedhæftede filer**, **kontrollister**, **værktøjer**, **aktivtællere**, **notater**, **kladder**.

![Figur 2](media/am-mobile-02.png)


## <a name="create-a-work-order-job"></a>Opret et arbejdsordrejob

1. På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.

2. Vælg **Alle vedligeholdelsesarbejdsordrer**.

3. Vælg den arbejdsordre, du vil oprette et nyt arbejdsordrejob for.

4. Vælg knappen **Tilføj linje**.

5. Vælg det **aktiv**, du vil oprette et nyt arbejdsordrejob for.

6. Vælg **Vedligeholdelsesjobtype**, **Vedligeholdelsesjobtypevariant** og **Fag**.

7. Vælg **Udført**.

![Figur 3](media/am-mobile-03.png)


## <a name="add-attachment-to-a-work-order-job"></a>Føj en vedhæftet fil til et arbejdsordrejob

1. På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.

2. Vælg **Alle vedligeholdelsesarbejdsordrer**.

3. Vælg arbejdsordren > arbejdsordrejobbet, du vil føje en vedhæftet fil til.
    - Alternativt kan du også vælge **Min kalender over arbejdsordrejob** eller **Min liste over arbejdsordrejob** på startsiden for at navigere til siden **Oplysninger om arbejdsordrejob**.

4. Vælg **Vedhæftede filer** på siden **Oplysninger om arbejdsordrejob**.

5. Du vil se eksisterende vedhæftede filer i arbejdsordrejobbet. Vælg **Tilføj vedhæftet fil**.

6. Angiv **Navn** og **Notater** for den vedhæftede fil.

7. Vælg **Vælg billede** for at vælge et billede i mobilgalleriet eller **Tag foto** for at tage et billede.

8. Vælg **Udført**.

![Figur 4](media/am-mobile-04.png)


## <a name="view-maintenance-checklist-on-a-work-order-job"></a>Få vist vedligeholdelsestjeklisten for et arbejdsordrejob

1. På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.

2. Vælg **Alle vedligeholdelsesarbejdsordrer**.

3. Vælg den arbejdsordre > arbejdsordrejob, du vil se tjeklister for.
    - Alternativt kan du også vælge **Min kalender over arbejdsordrejob** eller **Min liste over arbejdsordrejob** på startsiden for at navigere til siden **Oplysninger om arbejdsordrejob**.

4. Vælg **Kontrollister** på siden **Oplysninger om arbejdsordrejob**.

5. Der vises en liste over tjeklistelinjer, der er relateret til arbejdsordrejobbet. Vælg en tjeklistelinje for at få vist **Instruktioner** og tilføje **notater**.

6. Vælg knappen Tilbage (**<**) for at vende tilbage til den forrige side.

![Figur 5](media/am-mobile-05.png)


## <a name="view-and-update-asset-counters-on-a-work-order-job"></a>Få vist og opdatere aktivtællere på et arbejdsordrejob

1. På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.

2. Vælg **Alle vedligeholdelsesarbejdsordrer**.

3. Vælg den arbejdsordre > arbejdsordrejob, du vil se aktivtællere for.
    - Alternativt kan du også vælge **Min kalender over arbejdsordrejob** eller **Min liste over arbejdsordrejob** på startsiden for at navigere til siden **Oplysninger om arbejdsordrejob**.

4. Vælg **Aktivtællere** på siden **Oplysninger om arbejdsordrejob**.

5. Der vises en liste over aktivtællere, der er relateret til arbejdsordrejobbet. Vælg blyantikonet på en aktivtællerlinje for at opdatere tællerværdien.

6. Angiv en ny tællerværdi, og vælg **Udført**.

![Figur 6](media/am-mobile-06.png)


## <a name="register-consumption-on-a-work-order-job"></a>Registrer forbrug på et arbejdsordrejob

1. På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.

2. Vælg **Alle vedligeholdelsesarbejdsordrer**.

3. Vælg den arbejdsordre > arbejdsordrejob, du vil tilføje forbrugsregistreringer for.
    - Alternativt kan du også vælge **Min kalender over arbejdsordrejob** eller **Min liste over arbejdsordrejob** på startsiden for at navigere til siden **Oplysninger om arbejdsordrejob**.

4. Vælg **Kladder** på siden **Oplysninger om arbejdsordrejob**.

5. Vælg **Tilføj timer** for at oprette arbejdstidsregistreringer.
    1. Vælg **Kategori** fra opslaget.
    2. Angiv det antal arbejdstimer, der er brugt på arbejdsordrejobbet, i feltet **Timer**.
    3. Vælg den relevante **Linjeegenskab**.
    4. Vælg **Udført**.

6. Vælg **Tilføj varer** for at oprette vareregistreringer.
    1. Vælg **Varenummer** fra opslaget.
    2. Vælg **Sted** fra opslaget.
    3. Angiv forbrugte varer under **Antal**.
    4. Vælg **Udført**.

7. Vælg **Tilføj udgift** for at oprette udgiftsregistreringer.
    1. Vælg **Kategori** fra opslaget.
    2. Angiv antallet for udgiftsregistreringen.
    3. Vælg **Salgsvaluta** fra opslaget.
    4. Angiv **Kostpris** for udgiftsregistreringen.
    5. Vælg **Udført**.

![Figur 7](media/am-mobile-07.png)


## <a name="update-lifecycle-state-on-a-work-order"></a>Opdater livscyklustilstand på en arbejdsordre

1. På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.

2. Vælg **Alle vedligeholdelsesarbejdsordrer**.

3. Vælg den arbejdsordre, du vil opdatere livscyklustilstand for.

4. Vælg knappen **Opdater tilstand** nederst på skærmen.

5. Vælg en ny livscyklustilstand på listen.

6. Vælg **Udført**.

![Figur 8](media/am-mobile-08.png)


## <a name="create-a-maintenance-request"></a>Oprette en vedligeholdelsesanmodning

1. På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.

2. Vælg **Alle vedligeholdelsesanmodninger**.

3. Vælg **Handlinger** nederst på skærmen, og vælg **Opret vedligeholdelsesanmodning**.

4. Hvis nummerserien er aktiveret for vedligeholdelsesanmodninger i **Styring af aktiver** er feltet **Vedligeholdelsesanmodning** skjult, fordi det udfyldes automatisk. Hvis feltet **Vedligeholdelsesanmodning** er synligt, skal du angive et id for vedligeholdelsesanmodningen.

5. Vælg en **Vedligeholdelsesanmodningstype**.

6. Angiv en **Beskrivelse** af vedligeholdelsesanmodningen.

7. Vælg det **Aktiv**, som du vil oprette anmodningen for.

8. Vælg **Serviceniveau** for vedligeholdelsesanmodningen.

9. Vælg **Udført**.

![Figur 9](media/am-mobile-09.png)


## <a name="add-attachment-to-a-maintenance-request"></a>Føj en vedhæftet fil til en vedligeholdelsesanmodning

1. På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.

2. Vælg **Alle vedligeholdelsesanmodninger**.

3. Vælg den vedligeholdelsesanmodning, du vil føje en vedhæftet fil til.

4. Vælg **Vedhæftede filer** nederst på skærmen.

5. Vælg **Tilføj vedhæftede filer**.

6. Angiv **Navn** og **Notater** for den vedhæftede fil.

7. Vælg **Vælg billede** for at vælge et billede i mobilgalleriet eller **Tag foto** for at tage et billede.

8. Vælg **Udført**.

![Figur 10](media/am-mobile-10.png)

