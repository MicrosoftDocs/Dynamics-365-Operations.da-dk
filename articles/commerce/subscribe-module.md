---
title: Modulet Abonnement
description: I dette emne dækkes abonnementsmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e70bc01d4c662d08a9171a9d2feb0e2f7901ccbb
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479431"
---
# <a name="subscribe-module"></a>Modulet Abonnement

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

I dette emne dækkes abonnementsmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Du kan bruge abonnementsmoduler på webstedssider til at hente kundeoplysninger til nyhedsbreve eller kampagner.

I følgende illustration vises et eksempel på et abonnementsmodul i sidefoden på en Adventure Works-webstedsside.

![Eksempel på et abonnementsmodul i sidefoden på en Adventure Works-webstedsside](./media/Subscribe.PNG)

> [!IMPORTANT]
> - Abonnementsmodulet er tilgængeligt i Commerce-modulbiblioteket fra og med Dynamics 365 Commerce version 10.0.20-udgaven.
> - Abonnementsmodulet vises med temaet Adventure Works.
> - Abonnementsmodulet kræver en datahandlingsudvidelse for at kunne fungere sammen med visse markedsføringsmailudbydere, så der kan sendes nyhedsbreve eller markedsføringsmails, når kundeoplysningerne er registreret.

## <a name="subscribe-module-properties"></a>Egenskaber for abonnementsmodul

| Egenskabsbetegnelse | Værdier | Betegnelse |
|---------------|--------|-------------|
| Overskrift       | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | En tekstoverskrift for abonnementsmodulet, for eksempel **Abonner på nyhedsbrevet** eller **Tilmeld dig, og få en rabat på 10 %**. |
| Afsnit     | Afsnitstekst | Abonnementsmodulet understøtter afsnitstekst i RTF-format for at give flere oplysninger om handlingsplanen i overskriften. |

## <a name="add-a-subscribe-module-to-a-new-page"></a>Føje et abonnementsmodul til en ny side

Hvis du vil føje et abonnementslistemodul til en ny side og angive de påkrævede egenskaber i Commerce-webstedsgeneratoren, skal du følge disse trin.

1. Gå til **Skabeloner**, og åbn marketingskabelonen for webstedets startside (eller opret en ny marketingskabelon).
1. På pladsen **Hoved** på standardsiden skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Abonner** og derefter vælge **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til **Sider**, og åbn webstedets startside (eller opret en ny startside ved hjælp af marketingskabelonen).
1. Vælg pladsen **Hoved** på standardsiden, vælg ellipseknappen (**...**), og vælg derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Abonner** og derefter vælge **OK**.
1. Tilføj en overskrift i egenskabsruden for abonnementsmodulet, for eksempel **Abonner**.
1. Tilføj afsnitstekst, for eksempel **Seneste tendenser, stile og kampagner. Er du på listen? Abonner og få de seneste gode tilbud!**
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.
1. Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Adventure Works-tema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
