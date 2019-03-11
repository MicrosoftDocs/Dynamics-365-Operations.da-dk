---
title: Fantomvarer
description: Dette emne beskriver, i detaljer, hvordan fantomlinjetypen kan bruges til linjerne i en stykliste og en formel i Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: shylaw
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a92dd82f309867586f047e0dfc36e452a44a0f9c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "341804"
---
# <a name="phantom-items"></a>Fantomvarer

[!include [banner](../includes/banner.md)]

Dette emne beskriver, i detaljer, hvordan fantomlinjetypen kan bruges til linjerne i en stykliste og en formel. I følgende illustration er (a) styklisten for produktet H og delene F og G, og (b) er rutearket for produkt H og del F.

![Produkt H og del F](media/product-H-part-F.png)


Følgende illustration vises et eksempel på en styklistestruktur i to niveauer. Færdigvaren H repræsenterer et produkt til en maskinmontage. Maskinmontagen består af to dele, en elektrisk enhed (F), der har to materialer (A og B), og en gruppe af emballage (G), som også har to materialer (C og D). Et andet materiale (E) bruges under den generelle montage af maskinen.

![Produkt H og del F](media/product-H-part-B.png)

Foregående illustration repræsenterer styklisten Engineering for produkt H. Denne struktur giver et godt overblik over delene og komponenterne til den overordnede maskinmontage. Men selvom produktudviklere måske foretrækker at få vist styklisten på denne måde, viser denne struktur måske ikke korrekt den måde, som maskinen opbygges på på fabrikken. 

Styklisten Engineering i foregående illustration angiver f.eks., at den elektriske enhed F monteres som en separat del på en separat arbejdsordre. Men i produktionen kan det virke mere optimalt at montere den elektriske enhed som en del af den overordnede maskinmontage, og ikke som en separat arbejdsordre.

Styklisten Engineering angiver også, at del G er en separat del. Men i denne struktur er del G ikke en fysisk del, men en samling af emballagematerialer. 

Derfor, selvom styklisten Engineering er meget værdifuld til designet af et produkt og vedligeholdelsen af designet, er det måske ikke den mest logiske måde at understøtte produktionsprocessen på for produktet. Derimod repræsenterer styklisten Manufacturing den bedste måde at opbygge et produkt på.

I følgende illustration vises, hvordan den foregående stykliste Engineering er overgået til styklisten Manufacturing. I denne illustration er (a) styklisten for produktet H, og b er rutearket for produkt H.

I denne struktur kan du se, at delene F og G ikke findes, og de materialer, som delene består af, er hævet til næste niveau i styklisten. 

I modsætning til Engineering-styklisten, som havde to driftsark, har styklisten Manufacturing kun ét driftsark. Emballagedriften, der var knyttet til del G, er også blevet forhøjet og er nu en del af driftsarket for produkt H. Montagen af den elektriske enhed er den første driftsoperation. Denne ordre er en god idé, da denne enhed bruges i den næste operation, som er maskinmontagen. Den sidste operation er emballagen, der forbruger to emballagematerialer (C og D).

I Microsoft Dynamics 365 for Finance and Operations aktiveres overgangen mellem Engineering-styklisten og Produktions-styklisten via fantomstyklistens linjetype. Som betegnelsen "fantom" antyder, er delene F og G forsvundet i overgangen mellem de to typer af styklister. I dette eksempel anvendes fantomlinjetypen på styklistelinjerne for delene F og G i Engineering-styklisten. Når der oprettes en produktionsordre eller batchordre, kopieres styklisten Engineering til produktions- eller batchordren. Når ordren forkalkuleres, sker overgangen fra styklisten Engineering til styklisten Manufacturing, som vist i de foregående illustrationer. Fra driftsarket i den anden illustration indtastes emballagematerialerne C og D for operationen. 

## <a name="multilevel-phantom-bom-structures"></a>Flere strukturniveauer af fantomstykliste
Fantomlinjetypen kan bruges i flere niveauer styklisteniveauer, som vist i følgende illustration. I denne illustration er (a) styklisten for produkt G, og (b) er rutearket for del E og F og produkt G. 

![Produkt G og del F med ruteark](media/product-G-route-sheet-G.png)


I følgende illustration vises styklisten Manufacturing og rutearket, hvis styklistelinjerne for del E og F er konfigureret, så linjetypen er Fantom. I denne illustration er (a) styklisten for produkt G, og (b) er rutearket for produkt G.

![Produkt G](media/product-G.png)


## <a name="phantom-and-route-network"></a>Fantom- og rutenetværk
Fantomstyklister kan også bruges til en stykliste, der har et rutenetværk. I et rutenetværk køres en eller flere driftsoperationer parallelt. I følgende illustration vises et eksempel på et rutenetværk, der bruges i en stykliste med flere niveauer. I denne illustration er (a) styklisten for produkt G og del F, og (b) er rutearket for produkt G og del F, som har et rutenetværk.

![Produkt G og del F](media/product-G-part-F.png)


I følgende illustration er (a) styklisten for produkt G og del F, og (b) er rutearket for produkt G og del F.

![Produkt G og del F med ruteark](media/product-G-part-F-with-route-sheet.png)
