---
title: Føje en kanal til et organisationshierarki
description: Dette emne beskriver, hvordan du føjer en kanal til et organisationshierarki i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: f20b5c36b45fc0d242edb4e5305a4195d6dfbe94
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351219"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a>Føje en kanal til et organisationshierarki


[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du føjer en kanal til et organisationshierarki i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Kanaler skal knyttes til et eller flere organisationshierarkier. Før du opretter kanaler, skal du bekræfte, at organisationshierarkierne er konfigureret.  

Du kan finde flere oplysninger om oprettelse af organisationshierarkier i [Organisationshierarkier](channels-org-hierarchies.md).

## <a name="select-a-hierarchy"></a>Vælg et hierarki

Følg disse trin for at vælge et hierarki.

1. Gå til **Moduler \> Retail og Commerce \> Konfiguration af kanal \> Organisationshierarkier** i navigationsruden.
1. Vælg det organisationshierarki, du vil føje kanalen til, på listen.
1. Vælg **Vis** i handlingsruden for at få vist hierarkioplysninger.

Følgende billede viser detaljer om organisationshierarkiet for det valgte hierarki.

![Detaljer om organisationshierarkiet for det valgte hierarki.](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a>Føje en kanal til en hierarkinode

Følg disse trin for at føje en kanal til en hierarkinode.

1. Vælg **Rediger** i handlingsruden.
1. Vælg den hierarkinode, som kanalen skal føjes til, og vælg derefter **Detailkanal** på rullelisten **Indsæt**. 
1. Vælg den kanal, der skal tilføjes, og vælg derefter knappen **OK**.
1. Gå til handlingsruden, og vælg **Gem**.
1. Vælg **Udgiv** i handlingsruden, og angiv en **Ikrafttrædelsesdato** i fortiden, så denne handling træder i kraft med det samme.

Følgende billede viser, hvordan du vælger en kanal, som skal føjes til en hierarkinode.

![Vælge en kanal, som skal føjes til en hierarkinode.](media/channel-add-to-org-hierarchy-2.png)

Følgende billede viser et hierarki med forskellige kanaler tilføjet.

![Et hierarki med forskellige kanaler tilføjet.](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over kanaler](channels-overview.md)

[Forudsætninger for konfiguration af kanal](channels-prerequisites.md)

[Oversigt over organisationer og organisationshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Planlægge dit organisationshierarki](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Organisationshierarkier](channels-org-hierarchies.md)

[Konfigurer en detailkanal](channel-setup-retail.md)
    
[Konfigurere en onlinekanal](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]