---
title: Dokumenttilstande og -livscyklus
description: Dette emne omhandler de forskellige dokumenttilstande for sideelementer i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a34d10edbf84ac1814afdc7107727aea68a303e0
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770429"
---
# <a name="document-states-and-lifecycle"></a>Dokumenttilstande og -livscyklus

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne omhandler de forskellige dokumenttilstande for sideelementer i Microsoft Dynamics 365 Commerce.

## <a name="document-state-descriptions"></a>Beskrivelser af dokumenttilstande

Emnelisten i [Sideelementer](page-elements-overview.md) indeholder forskellige dokumenttyper i CMS (Content Management System). Disse dokumenttyper kan have flere forskellige tilstande i oprettelsesværktøjet. Dokumenttilstandene hjælper med at forhindre datakonflikter og gennemtvinge versionskontrol. De bestemmer, hvem der kan ændre dokumenterne, hvornår dokumenterne kan ændres, og hvornår ændringer kan ses af andre personer.

I følgende tabel vises de mulige dokumenttilstande for sideelementer i Commerce.

| Dokumenttilstand | Beskrivelse |
|---|---|
| Checket ud | Når et CMS-element er checket ud til dig, kan det ikke redigeres af andre godkendte systembrugere. De ændringer, du foretager af elementet, er kun synlige for dig. |
| Checket ind | Når et CMS-element checkes ind, er alle ændringer synlige for andre godkendte systembrugere, og disse brugere kan derefter checke elementet ud og redigere det. Ved hver check-ind oprettes en dokumentversionspost i elementets historik. |
| Udgivet | Når et CMS-element udgives, flyttes det til dit aktive websted og kan registreres på internettet af ikke-godkendte eksterne brugere. Elementer kan kun udgives, hvis de er blevet checket ind. |
| Gemt | Ændringer, der er foretaget af et element, der er checket ud, kan gemmes i CMS, før elementet tjekkes ind eller publiceres. Disse gemte ændringer er ikke synlige for andre godkendte systembrugere, før elementet er tjekket ind. De er ikke synlige for eksterne brugere, før elementet er publiceret. |
| Kasseret udcheckning | Når et element, der er checket ud af CMS, kasseres, slettes alle gemte ændringer, og elementet tilbageføres til den version, der senest blev checket ind. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Metoder til at tilføje indhold](add-manage-content.md)

[Ordliste til sidemodel](page-elements-overview.md)

[Arbejde med moduler](work-with-modules.md)

[Arbejde med fragmenter](work-with-fragments.md)

[Oversigt over skabeloner og layout](templates-layouts-overview.md)

[Tilpasse navigation på webstedet](customize-site-navigation.md)
