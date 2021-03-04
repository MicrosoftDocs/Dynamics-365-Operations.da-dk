---
title: Dokumenttilstande og -livscyklus
description: Dette emne omhandler de forskellige dokumenttilstande for sideelementer i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
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
ms.openlocfilehash: 8aad7ef8425e46182c669686710dfc178abc418f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411085"
---
# <a name="document-states-and-lifecycle"></a>Dokumenttilstande og -livscyklus

[!include [banner](includes/banner.md)]

Dette emne omhandler de forskellige dokumenttilstande for sideelementer i Microsoft Dynamics 365 Commerce.

## <a name="document-state-descriptions"></a>Beskrivelser af dokumenttilstande

Emnelisten i [Sideelementer](page-elements-overview.md) indeholder forskellige dokumenttyper i CMS (Content Management System). Disse dokumenttyper kan have flere forskellige tilstande i oprettelsesværktøjet. Dokumenttilstandene hjælper med at forhindre datakonflikter og gennemtvinge versionskontrol. De bestemmer, hvem der kan ændre dokumenterne, hvornår dokumenterne kan ændres, og hvornår ændringer kan ses af andre personer.

I følgende tabel vises de mulige dokumenttilstande for sideelementer i Commerce.

| Dokumenttilstand      | Webstedsgeneratorhandling        | Beskrivende tekst                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| Tjekket ud         | Vælg **Rediger**.           | Det ønskede dokument er tjekket ud til dig. Mens et dokument er i denne tilstand, kan det ikke ændres af andre godkendte systembrugere, og eventuelle ændringer, du foretager i dokumentet, er kun synlige for dig. |
| Gemt               | Vælg **Gem**.           | Ændringer, der er foretaget i et dokument, der er tjekket ud, gemmes i databasen, men dokumentet er endnu ikke tjekket ind eller udgivet. De gemte ændringer er ikke synlige for andre godkendte systembrugere, før forfatteren vælger **Afslut redigering**. De er ikke synlige for eksterne brugere, før elementet er publiceret. |
| Kasseret udcheckning | Vælg **Kassér redigeringer**.  | Alle ændringer af dokumentet, der er tjekket ud, slettes, og varen vender tilbage til den seneste version, der blev tjekket ind. |
| Tjekket ind          | Vælg **Afslut redigering**. | Det redigerede dokument er tjekket ind. Alle ændringer er synlige for andre godkendte systembrugere, og disse brugere kan derefter redigere dokumentet. Ved hver check-ind oprettes en dokumentversionspost i elementets historik. |
| Udgivet           | Vælg **Publicer**.        | Dokumentet udgives, og ændringerne føres til dit direkte websted og bliver synlige for eksterne brugere. Varer kan kun udgives, hvis de først er tjekket ind ved at vælge **Afslut redigering**. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Metoder til at tilføje indhold](add-manage-content.md)

[Ordliste til sidemodel](page-elements-overview.md)

[Arbejde med publiceringsgrupper](publish-groups.md)

[Aktivere og bruge deling på tværs af kanaler](cross-channel-sharing.md)

[Arbejde med moduler](work-with-modules.md)

[Arbejde med fragmenter](work-with-fragments.md)

[Oversigt over skabeloner og layout](templates-layouts-overview.md)

[Tilpasse navigation på webstedet](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]