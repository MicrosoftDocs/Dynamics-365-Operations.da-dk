---
title: Konfigurere en kanal for at bruge et navigationshierarki for en kanal
description: Dette emne beskriver, hvordan du konfigurerer en kanal for at bruge et navigationshierarki for en kanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3dcba743e6557b1bd366ac79ecb49ead831dceb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001019"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a>Konfigurere en kanal for at bruge et navigationshierarki for en kanal


[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du konfigurerer en kanal for at bruge et navigationshierarki for en kanal i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Navigationshierarkier for en kanal organiserer produkter i kategorier, så produkterne kan gennemses på et e-handelswebsted eller ved POS. Detail- og onlinekanaler skal konfigureres med navigationshierarkier for en kanal.

## <a name="configure-the-channel"></a>Konfigurere kanalen

Du kan konfigurere en kanal for at bruge et navigationshierarki for en kanal ved at følge disse trin.

1. Gå til **Moduler \> Retail og Commerce \> Konfiguration af kanal \> Kanalkategorier og produktattributter** i navigationsruden.
1. Vælg den kanal, der skal konfigureres.
1. I handlingsruden skal du vælge **Angiv attributmetadata**.
1. På rullelisten **Kategorihierarki** skal du vælge det relevante kanalnavigationshierarki.
1. Gå til handlingsruden, og vælg **Gem**.
1. Under **Attributgruppe** skal du tilføje alle attributgrupper, der skal være globale attributter for alle noder.

Følgende billede viser, hvordan du konfigurerer en kanal for at bruge et navigationshierarki for en kanal.

![Eksempel på kanalkonfiguration](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a>Angiv attributmetadata

Angivelse af attributmetadataene giver mulighed for konfiguration af attributter på de enkelte noder.

Du kan angive attributmetadataene ved at følge disse trin.

1. I handlingsruden skal du vælge **Angiv attributmetadata**.
1. Vælg **Kanalproduktattributter** for hver node.
1. Angiv **Vis attribut på kanal** til **Ja** og **Kan redigeres** til **Ja**, hvis du vil aktivere afgrænsere på denne kanal.
1. Når du har konfigureret hver enkelt node efter behov, skal du vælge knappen **Gem** i **handlingsruden**.
1. Vælg **X** i øverste højre hjørne for at forlade dette skærmbillede og vende tilbage til siden **Kanalkategorier og produktattributter**.

Følgende billede viser et sæt af kanalproduktattributter, der er konfigureret på en kanalkategorinode.

![Kanalattributter på en kanalkategorinode](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a>Publicere ændringer

Du skal publicere ændringerne, for at ændringerne træder i kraft.

Følg disse trin for at publicere ændringer.

1. Vælg **Publicer kanalopdateringer** i handlingsruden.
1. Vælg **OK** i ruden **Publicer kanalopdateringer**.

Følgende billede viser, hvordan du kan publicere kanalopdateringer.

![Publicer kanalopdateringer](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette et navigationshierarki for kanal](create-channel-hierarchy.md)


