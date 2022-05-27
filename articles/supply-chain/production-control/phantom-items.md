---
title: Fantomvarer
description: Dette emne beskriver, hvordan fantomlinjetypen kan bruges til linjerne i en stykliste og en formel i Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 05/05/2022
ms.topic: article
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-05-05
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 5c9768381d35709611e4bec3d2b7793a4d896b34
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713240"
---
# <a name="phantom-items"></a>Fantomvarer

[!include [banner](../includes/banner.md)]

Dette emne beskriver, i detaljer, hvordan fantomlinjetypen kan bruges til linjerne i en stykliste og en formel.

I figur 1 er (a) styklisten for produktet H og delene F og G, og (b) er rutearket for produkt H og del F.

![Figur 1: Teknisk stykliste.](media/product-H-part-F.png)
*Figur 1: Teknisk stykliste*

I Figur 1 vises et eksempel på en styklistestruktur i to niveauer. Færdigvaren H repræsenterer et produkt til en maskinmontage. Maskinmontagen består af to dele, en elektrisk enhed (F), der har to materialer (A og B), og en gruppe af emballage (G), som også har to materialer (C og D). Et andet materiale (E) bruges under den generelle montage af maskinen.

Figur 1 repræsenterer Teknisk stykliste for produkt H. Denne struktur giver et godt overblik over delene og komponenterne til den overordnede maskinmontage. Men selvom produktudviklere måske foretrækker at få vist styklisten på denne måde, viser denne struktur måske ikke korrekt den måde, som maskinen opbygges på på fabrikken.

Teknisk stykliste i Figur 1 angiver f.eks., at den elektriske enhed F monteres som en separat del på en separat arbejdsordre. Men i produktionen kan det virke mere optimalt at montere den elektriske enhed som en del af den overordnede maskinmontage, og ikke som en separat arbejdsordre.

Styklisten Engineering angiver også, at del G er en separat del. Men i denne struktur er del G ikke en fysisk del, men en samling af emballagematerialer.

Derfor, selvom styklisten Engineering er meget værdifuld til designet af et produkt og vedligeholdelsen af designet, er det måske ikke den mest logiske måde at understøtte produktionsprocessen på for produktet. Derimod repræsenterer styklisten Manufacturing den bedste måde at opbygge et produkt på.

I Figur 2 vises, hvordan den foregående tekniske stykliste er overgået til styklisten Manufacturing. I Fgur 2 er (a) styklisten for produkt H, og b er rutearket for produkt H.

![Figur 2: Produktionsstykliste.](media/product-H-part-B.png)
*Figur 2: Produktionsstykliste*

I denne struktur kan du se, at delene F og G ikke findes, og de materialer, som delene består af, er hævet til næste niveau i styklisten.

I modsætning til Engineering-styklisten, som havde to driftsark, har styklisten Manufacturing kun ét driftsark. Emballagedriften, der var knyttet til del G, er også blevet forhøjet og er nu en del af driftsarket for produkt H. Montagen af den elektriske enhed er den første driftsoperation. Denne ordre er en god idé, da denne enhed bruges i den næste operation, som er maskinmontagen. Den sidste operation er emballagen, der forbruger to emballagematerialer (C og D).

Overgangen mellem Engineering-styklisten og Produktions-styklisten aktiveres via fantomstyklistens linjetype. Som betegnelsen "fantom" antyder, er delene F og G forsvundet i overgangen mellem de to typer af styklister. I dette eksempel anvendes fantomlinjetypen på styklistelinjerne for delene F og G i Engineering-styklisten. Når der oprettes en produktionsordre eller batchordre, kopieres styklisten Engineering til produktions- eller batchordren. Når ordren forkalkuleres, sker overgangen fra styklisten Engineering til styklisten Manufacturing, som vist i Figur 2. Fra driftsarket i Figur 2 indtastes emballagematerialerne C og D for driften.

## <a name="multilevel-phantom-bom-structures"></a>Flere strukturniveauer af fantomstykliste

Fantomlinjetypen kan bruges i flere niveauer styklisteniveauer, som vist i Figur 3. I Figur 3 er (a) styklisten for produkt G, og (b) er rutearket for del E og F og produkt G.

![Figur 3: Teknisk stykliste til del G.](media/product-G.png)
*Figur 3: Teknisk stykliste til del G*

I Figur 4 vises styklisten Manufacturing og rutearket, hvis styklistelinjerne for del E og F er konfigureret, så linjetypen er Fantom. I Figur 4 er (a) styklisten for produkt G, og (b) er rutearket for produkt G.

![Figur 4: Produktionsstykliste til del G.](media/product-G-route-sheet-G.png)
*Figur 4: Produktionsstykliste til del G*

## <a name="phantom-and-route-network"></a>Fantom- og rutenetværk

Fantomstyklister kan også bruges til en stykliste, der har et rutenetværk. I et rutenetværk køres en eller flere driftsoperationer parallelt. I Figur 5 vises et eksempel på et rutenetværk, der bruges i en stykliste med flere niveauer. I Figur 5 er (a) styklisten for produkt G og del F, og (b) er rutearket for produkt G og del F, som har et rutenetværk.

![Figur 5: Teknisk stykliste til del G, rutenetværk.](media/product-G-part-F.png)
*Figur 5: Teknisk stykliste til del G, rutenetværk*

I Figur 6 er (a) styklisten for produkt G og del F, og (b) er rutearket for del F og produkt G.

![Figur 6: Produktionsstykliste til del G, rutenetværk.](media/product-G-part-F-with-route-sheet.png)
*Figur 6: Produktionsstykliste til del G, rutenetværk*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]