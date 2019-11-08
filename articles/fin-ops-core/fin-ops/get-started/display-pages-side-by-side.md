---
title: Vise sider side om side ved hjælp af Åbn i ny vinduesfunktion
description: I denne artikel beskrives, hvordan du får vist sider side om side.
author: aneesmsft
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7144f26c0977fbc420b804728151262b2f166bc0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180685"
---
# <a name="show-pages-side-by-side-by-using-the-open-in-new-window-feature"></a>Vise sider side om side ved hjælp af Åbn i ny vinduesfunktion

[!include [banner](../includes/banner.md)]

I denne artikel beskrives, hvordan du får vist sider side om side.

Du ønsker måske at få vist flere sider side om side for at udføre opgaver hurtigt. Som et eksempel vil du måske validere eller angive linjer i mere end én kladde. For at gøre det vil du typisk være nødt til at gå skulle gå frem og tilbage mellem den side, der viser en liste over kladder, og den side, der viser linjer for en given kladde. Men funktionen **Åbn i et nyt vindue** gør det muligt for dig at få vist disse sider side om side, så du hurtigt kan udføre opgaver.

Hvis du fortsætter med det eksempel, der er nævnt ovenfor, så kan du, når du får vist linjerne, klikke på ikonet **Åbn i et nyt vindue**.

[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)

Når du klikker på ikonet **Åbn i et nyt vindue**, åbnes siden med linjer i en ny pop op-browser, og derefter navigerer den oprindelige browser tilbage i historikken til siden, der viste oversigten over kladder. Du kan derefter få vist begge sider på samme tid. Når du er færdig med at få vist en kladde, kan du ændre den valgte kladde på siden med journallisten, og så viser siden med linjer i pop op-vinduet automatisk linjerne i den nyligt valgte kladde.

[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)

Den dynamiske sammenkædning og opdatering sker på grund af de forbindelser, der findes mellem de data, der sikkerhedskopierer disse sider. Hvis systemet ikke er opmærksom på relationen mellem dataene, opdateres pop up-vinduet ikke automatisk som reaktion på en ændring i det vindue, hvor den stammer fra.

Nogle sider har flere visninger som gittervisning, overskriftsvisning og detaljeret visning. Ikonet **Åbn i et nyt vindue** bevirker, at hele siden skal åbnes i det nye browservindue. Du kan derfor ikke have to visninger af den samme side parallelt, mens du bruger funktionen **Åbn i et nyt vindue**. Næsten alle sådanne sider har dog en liste til navigation, som du kan bruge til at skifte mellem poster og opnå en lignende oplevelse.

Før du bruger funktionen **Åbn i et nyt vindue**, skal du konfigurere browserens pop op-blokering for at tillade pop op-vinduer fra URL-adressen på webstedet. Som et eksempel kan du tillade pop op-vinduer fra "\*.dynamics.com".

Funktionen **Åbn i et nyt vindue** er kun tilgængelig, når der er mere end én side åben i vinduet. Desuden lukkes pop-up-vinduet automatisk, når der ikke er flere sider åbent (når den sidste side i dette vindue er lukket). Systemet lukker også åbne sider, når du navigerer til et andet område i programmet. Derfor, hvis du har åbne pop op-vinduer og navigere til et andet område i programmet, lukkes pop op-vinduerne lukkes automatisk, fordi siderne i disse vinduer blev lukket af systemet.

Topbjælken i pop op-vinduerne viser oplysninger om den virksomhed, som siden blev åbnet i, og er skrivebeskyttet. Pop op-vinduer er også afhængige af hovedbrowservinduet. Hvis hovedvinduet er lukket eller opdateres, bliver alle åbne pop op-vinduer skrivebeskyttet. Det betyder, at du kan stadig få vist oplysninger i disse vinduer, men du kan ikke interagere med dem.