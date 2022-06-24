---
title: Konfigurere organisationshierarkier
description: Denne artikel beskriver, hvordan du kan konfigurere organisationshierarkier i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 01ba05566e966eb62a4df0b7b97ee3a442027936
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847674"
---
# <a name="set-up-organization-hierarchies"></a>Konfigurere organisationshierarkier

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du kan konfigurere organisationshierarkier i Microsoft Dynamics 365 Commerce.

Før du opretter kanaler, skal du sikre, at du har konfigureret dine organisationshierarkier.

Du kan bruge organisationshierarkier for at få vist og rapportere om forskellige perspektiver i virksomheden. Du kan f.eks. oprette et hierarki til skattemæssig, juridisk eller lovpligtig rapportering. Derefter kan du oprette et andet hierarki for at afrapportere økonomiske oplysninger, der ikke er juridisk påkrævet, men bruges til interne afrapportering.

Før du opretter et organisationshierarki, skal du oprette organisationer. Du kan få flere oplysninger i [Oprette juridiske enheder](channels-legal-entities.md) eller [Oprette driftsenheder](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).


Du kan finde flere oplysninger i følgende artikler.
- [Oversigt over organisationer og organisationshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [Planlægge dit organisationshierarki](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [Oprette et organisationshierarki](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a>Oprette et organisationshierarki

Benyt følgende fremgangsmåde for at oprette et organisationshierarki for en kanal.

1. Gå til **Moduler \> Retail og Commerce \> Konfiguration af kanal \> Organisationshierarkier** i navigationsruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv en værdi i feltet **Navn**.
1. Vælg **Tildel formål** i sektionen **Formål**.
1. Find og vælg den ønskede post på listen. Vælg det formål, du vil tildele til organisationshierarkiet.
1. Vælg **Tilføj** i sektionen **Tildelte hierarkier**.
1. Markér den valgte række på listen. Find det hierarki, du netop har oprettet.
1. Vælg **OK**.

Følgende billede viser et eksempel på et organisationshierarki, der er oprettet for række af fiktive "Adventure Works"-butikker.

![Eksempel på organisationshierarki.](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a>Føje organisationer til et hierarki

Følg disse trin for at føje organisationer til et hierarki.

1. Find og vælg den ønskede post på listen. Vælg hierarkiet.
1. Gå til handlingsruden, og vælg **Vis**.
1. Tilføj organisationer efter behov.
1. Hvis du vil tilføje en organisation skal du vælge **Rediger** og derefter vælge **Indsæt**. Når du er færdig med at foretage ændringer, kan du gemme en kladde og udgive ændringerne.

Følgende billede viser en juridisk enhed, der er føjet til hierarkiroden, med fire bærere, som er tilføjet for kanalerne "Mall", "Udgang", "Online" og "Callcenter". Der kan føjes forskellige detailvarer, callcentre og onlinekanaler til hver enkelt.

![Eksempel på hierarkidesigner.](media/hierarchy-designer.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over organisationer og organisationshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Planlægge dit organisationshierarki](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Oprette juridiske enheder](channels-legal-entities.md)

[Oprette driftsenheder](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[Oversigt over kanaler](channels-overview.md)

[Forudsætninger for konfiguration af kanal](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
