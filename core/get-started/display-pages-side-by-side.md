---
title: "Vise sider side om side ved hjælp af ikonet Åbn i et nyt vindue"
description: "I denne artikel beskrives det, hvordan du får vist siderne side om side i Microsoft Dynamics 365 for Operations."
author: aneesmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 940d086f9c99af54bfcc7911ee7272f9eccba464
ms.lasthandoff: 03/31/2017


---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a>Vise sider side om side ved hjælp af ikonet Åbn i et nyt vindue

I denne artikel beskrives det, hvordan du får vist siderne side om side i Microsoft Dynamics 365 for Operations.

Microsoft Dynamics 365 for Operations hjælper dig med at udføre opgaver effektivt. I nogle tilfælde kan du få vist flere sider side om side for at udføre opgaver hurtigt. Som et eksempel vil du måske validere eller angive linjer i mere end én kladde. For at gøre det vil du typisk være nødt til at gå skulle gå frem og tilbage mellem den side, der viser en liste over kladder, og den side, der viser linjer for en given kladde. Men funktionen **Åbn i et nyt vindue** gør det muligt for dig at få vist disse sider side om side, så du hurtigt kan udføre opgaver. Hvis du fortsætter med det eksempel, der er nævnt ovenfor, så kan du, når du får vist linjerne, klikke på ikonet **Åbn i et nyt vindue**. [![Åbn-i-ny-vindue-ikonet](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png) på den **Åbn i nyt vindue** ikon åbner siden linjer i en ny, pop op-browser og derefter navigerer den oprindelige browser tilbage i historikken til siden, vises oversigten over kladder. Du kan derefter få vist begge sider på samme tid. Når du er færdig med at få vist en kladde, kan du ændre den valgte kladde på siden med journallisten, og så viser siden med linjer i pop op-vinduet automatisk linjerne i den nyligt valgte kladde. [![sider-show-side ved side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png) dynamisk sammenkædning- og opdatering sker på grund af de forbindelser, der findes mellem de data, der sikkerhedskopiering disse sider. Hvis systemet ikke er opmærksom på relationen mellem dataene, opdateres pop up-vinduet ikke automatisk som reaktion på en ændring i det vindue, hvor den stammer fra. Nogle sider har flere visninger som gittervisning, overskriftsvisning og detaljeret visning. Ikonet **Åbn i et nyt vindue** bevirker, at hele siden skal åbnes i det nye browservindue. Du kan derfor ikke have to visninger af den samme side parallelt, mens du bruger funktionen **Åbn i et nyt vindue**. Næsten alle sådanne sider har dog en liste til navigation, som du kan bruge til at skifte mellem poster og opnå en lignende oplevelse. Før du bruger funktionen **Åbn i et nyt vindue**, skal du konfigurere browserens pop op-blokering for at tillade pop op-vinduer fra URL-adressen på Dynamics 365 for Operations-webstedet. Som et eksempel, kan du tillade pop-up-vinduer fra "\*. dynamics.com". Funktionen **Åbn i et nyt vindue** er kun tilgængelig, når der er mere end én side åben i vinduet. Desuden lukkes pop-up-vinduet automatisk, når der ikke er flere sider åbent (når den sidste side i dette vindue er lukket). Dynamics 365 for Operations lukker også åbne sider, når du navigerer til et andet område i programmet. Derfor, hvis du har åbne pop op-vinduer og navigere til et andet område i programmet, lukkes pop op-vinduerne lukkes automatisk, fordi siderne i disse vinduer blev lukket af systemet. Topbjælken i pop op-vinduerne viser oplysninger om den virksomhed, som siden blev åbnet i, og er skrivebeskyttet. Pop op-vinduer er også afhængige af hovedbrowservinduet i Dynamics 365 for Operations. Hvis hovedvinduet er lukket eller opdateres, bliver alle åbne pop op-vinduer skrivebeskyttet. Det betyder, at du kan stadig få vist oplysninger i disse vinduer, men du kan ikke interagere med dem.

