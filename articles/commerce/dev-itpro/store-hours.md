---
title: Oprette og opdatere åbningstider
description: I dette emne beskrives, hvordan du opretter og opdaterer åbningstider i Commerce Headquarters.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 00c532dfa9ceed2cda6652496d874cb82785dc7b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230634"
---
# <a name="create-and-update-store-hours"></a>Oprette og opdatere åbningstider

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a>Oversigt

Detailhandlere kan på ét samlet sted oprette, vedligeholde og administrere åbningstider for forskellige butikker på tværs af geografiske områder. Åbningstiderne kan derefter vises i POS-terminaler. På denne måde kan kasserere dele åbningstider med kunder og bedre hjælpe dem, hvis de er interesserede i at vide, hvad andre butikker har på lager. Åbningstiderne kan også udskrives på kvitteringer, hvis kunderne senere vil vende tilbage til butikken.

Der kan konfigureres flere åbningstider på tværs af forskellige kanaler. Disse kanaler omfatter fysiske butikker, callcentre, mobilenheder og e-handelswebsteder.

Hvis en kunde har en afhentningsordre i en anden butik, kan kassereren vælge datoer, hvor varen til afhentning er tilgængelig i den pågældende butik. Butiksopslaget giver en reference til datoerne og åbningstiderne. Kassereren kan vælge en dato og et sted og kan også udskrive en afhentningskvittering, der omfatter åbningstiderne.

Denne funktionalitet er tilgængelig i Microsoft Dynamics 365 Retail version 8.1.2 og nyere.

## <a name="configure-store-hours"></a>Konfigurere åbningstider

Når du vil konfigurere åbningstider, skal du følge disse trin.

1. Gå til **Retail og Commerce** \> **Konfiguration af kanal** \> **Åbningstider**.
2. Vælg **Ny** for at oprette en ny åbningstidsskabelon. Hvis du vil bruge en eksisterende skabelon, skal du vælge skabelonen i venstre rude.
3. I dialogboksen **Tilføj et interval** skal du definere datointervallet, åbningstiderne og de helligdage, der kræves.

    - Hvis der ikke skal skiftes åbningstider, skal du vælge **Slutter aldrig** i feltet **Slutdato**.
    - Hvis åbningstiderne gælder for en bestemt måned, uge eller dag, skal du angive de relevante datoer i felterne **Startdato** og **Slutdato**.

    > [!NOTE]
    > Du kan oprette flere skabeloner med overlappende start- og slutdatoer. Du kan derfor f.eks. definere åbningstider for butikker i forskellige tidszoner.

    ![Dialogboksen Tilføj et interval](../dev-itpro/media/Storehours1.png "Dialogboksen Tilføj et interval")

4. Knyt åbningstidsskabelonen til de butikker, hvor den vil blive brugt. Vælg de butikker, områder og organisationer, skabelonen skal knyttes til, i dialogboksen **Vælg organisationsnoder**.

    - Der kan kun knyttes én åbningstidsskabelon til hver butik.
    - Brug pileknapperne til at vælge butikker, områder eller organisationer. Kalenderen vil være tilgængelig for butikkerne eller butiksgrupperne, og den vil være synlig på POS som reference.

    ![Dialogboksen Vælg organisationsnoder](../dev-itpro/media/Storehours2.png "Dialogboksen Vælg organisationsnoder")

5. På siden **Distributionsplan** skal du køre jobbene **1070** og **1090** for at gøre åbningstiderne tilgængelige for POS.

## <a name="add-store-hours-to-printed-receipts"></a>Føje åbningstider til udskrevne kvitteringer

Benyt følgende fremgangsmåde for at føje åbningstider til de udskrevne POS-kvitteringer.

1. Åbn kvitteringsdesigneren.
2. Vælg **Sidefod** i nederste venstre hjørne.
3. Træk elementet **Åbningstider** fra venstre rude til sidefoden nederst i kvitteringsskabelonen.
4. Du kan redigere standardlabelen på elementet **Åbningstider** efter behov.
5. Gem kvitteringen, og luk kvitteringsdesigneren.
6. På siden **Distributionsplan** skal du køre jobbene **1070** og **1090**.
7. Log på POS'et.
8. Udfør et salg, og vælg for at udskrive en kvittering.

POS-kvitteringer viser nu åbningstiderne. Hvis der er helligdage i skabelonen, vises de på kvitteringen.

![Kvitteringseksempel](../dev-itpro/media/Storehours3.png "Kvitteringseksempel")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]