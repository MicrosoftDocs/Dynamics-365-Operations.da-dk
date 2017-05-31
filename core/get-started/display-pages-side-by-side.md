---
title: "Vise sider side om side ved hjælp af ikonet Åbn i et nyt vindue"
description: "I denne artikel beskrives det, hvordan du får vist siderne side om side i Microsoft Dynamics 365 for Operations."
author: aneesmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b6985b600fb7eb84f7e3db8d49561eab24341a03
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a>Vise sider side om side ved hjælp af ikonet Åbn i et nyt vindue

[!include[banner](../includes/banner.md)]


I denne artikel beskrives det, hvordan du får vist siderne side om side i Microsoft Dynamics 365 for Operations.

Microsoft Dynamics 365 for Operations hjælper dig med at udføre opgaver effektivt. I nogle tilfælde kan du få vist flere sider side om side for at udføre opgaver hurtigt. Som et eksempel vil du måske validere eller angive linjer i mere end én kladde. For at gøre det vil du typisk være nødt til at gå skulle gå frem og tilbage mellem den side, der viser en liste over kladder, og den side, der viser linjer for en given kladde. Men funktionen **Åbn i et nyt vindue** gør det muligt for dig at få vist disse sider side om side, så du hurtigt kan udføre opgaver. Hvis du fortsætter med det eksempel, der er nævnt ovenfor, så kan du, når du får vist linjerne, klikke på ikonet **Åbn i et nyt vindue**. [![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png) Når du klikker på ikonet **Åbn i et nyt vindue**, åbnes siden med linjer i en ny pop op-browser, og derefter navigerer den oprindelige browser tilbage i historikken til siden, der viste oversigten over kladder. Du kan derefter få vist begge sider på samme tid. Når du er færdig med at få vist en kladde, kan du ændre den valgte kladde på siden med journallisten, og så viser siden med linjer i pop op-vinduet automatisk linjerne i den nyligt valgte kladde. [![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png) Den dynamiske sammenkædning og opdatering sker på grund af de forbindelser, der findes mellem de data, der sikkerhedskopierer disse sider. Hvis systemet ikke er opmærksom på relationen mellem dataene, opdateres pop up-vinduet ikke automatisk som reaktion på en ændring i det vindue, hvor den stammer fra. Nogle sider har flere visninger som gittervisning, overskriftsvisning og detaljeret visning. Ikonet **Åbn i et nyt vindue** bevirker, at hele siden skal åbnes i det nye browservindue. Du kan derfor ikke have to visninger af den samme side parallelt, mens du bruger funktionen **Åbn i et nyt vindue**. Næsten alle sådanne sider har dog en liste til navigation, som du kan bruge til at skifte mellem poster og opnå en lignende oplevelse. Før du bruger funktionen **Åbn i et nyt vindue**, skal du konfigurere browserens pop op-blokering for at tillade pop op-vinduer fra URL-adressen på Dynamics 365 for Operations-webstedet. Som et eksempel kan du tillade pop op-vinduer fra "\*.dynamics.com". Funktionen **Åbn i et nyt vindue** er kun tilgængelig, når der er mere end én side åben i vinduet. Desuden lukkes pop-up-vinduet automatisk, når der ikke er flere sider åbent (når den sidste side i dette vindue er lukket). Dynamics 365 for Operations lukker også åbne sider, når du navigerer til et andet område i programmet. Derfor, hvis du har åbne pop op-vinduer og navigere til et andet område i programmet, lukkes pop op-vinduerne lukkes automatisk, fordi siderne i disse vinduer blev lukket af systemet. Topbjælken i pop op-vinduerne viser oplysninger om den virksomhed, som siden blev åbnet i, og er skrivebeskyttet. Pop op-vinduer er også afhængige af hovedbrowservinduet i Dynamics 365 for Operations. Hvis hovedvinduet er lukket eller opdateres, bliver alle åbne pop op-vinduer skrivebeskyttet. Det betyder, at du kan stadig få vist oplysninger i disse vinduer, men du kan ikke interagere med dem.




