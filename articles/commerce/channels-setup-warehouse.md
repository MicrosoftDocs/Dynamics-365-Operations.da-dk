---
title: Konfigurer et lagersted
description: Dette emne beskriver, hvordan du kan konfigurere et lagersted til brug med en ny kanal i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 1fce2570e1b0cc334fc0e92e5e83c53a4566b4a4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345978"
---
# <a name="warehouse-set-up"></a>Konfigurere lagersted

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du kan konfigurere et lagersted til brug med en ny kanal i Microsoft Dynamics 365 Commerce.

Hver enkelt Commerce-kanal kræver, at den er tilknyttet et konfigureret lagersted. Følgende procedurer indeholder den minimumkonfiguration, der kræves for at konfigurere et lagersted til en Commerce-kanal. Du kan få yderligere oplysninger om opsætning af lagersteder i [Oversigt over lokationsstyring](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).

## <a name="configure-a-warehouse-site"></a>Konfigurer et sted til et lagersted

Før du konfigurerer et lagersted, skal du konfigurere et sted til lagerstedet.

Gør følgende for at konfigurere et sted til et lagersted.

1. Gå til **Moduler \> Detail og handel \> Konfiguration af kanal \> Steder** i navigationsruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv en værdi i feltet **Sted**.
1. Angiv en værdi i feltet **Navn**.
1. Angiv den relevante **Tidszone** i sektionen **Generelt**.
1. Angiv en adresse i feltet **Adresser**.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser et eksempel på et sted til et lagersted.

![Eksempel på et sted til et lagersted.](media/warehouse-site.png)

## <a name="set-up-a-warehouse&quot;></a>Konfigurer et lagersted

Gør følgende for at konfigurere et lagersted.

1. Gå til **Moduler \> Detail og handel \> Konfiguration af kanal \> Lagersteder** i navigationsruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. Indtast en værdi i feltet **Lagersted**.  Hvis dette er en 1:1-tilknytning til en butik, skal du overveje at bruge butiksnavnet eller navnet på et regionalt distributionscenter.
1. Angiv en værdi i feltet **Navn**.
1. Vælg det sted til lagerstedet, du tidligere har oprettet, på rullelisten **Sted**.
1. Vælg **Standard** i feltet **Type**.
    - Hvis du vil angive et **Karantænelagersted**, skal du først følge disse trin for at oprette et ekstra lagersted, hvor **Type** er indstillet til **Karantæne**.
    - Hvis du vil angive et **Transitlagersted**, skal du først følge disse trin for at oprette et ekstra lagersted, hvor **Type** er indstillet til **Transit**.
1. Gå til handlingsruden, og vælg **Gem**.

## <a name=&quot;set-up-inventory-aisles&quot;></a>Konfigurer lagergange

Følg disse trin for at konfigurere lagergange.

1. Gå til **Moduler \> Retail og Commerce \> Konfiguration af kanal \> Konfiguration af lokation \> Lagergange** i navigationsruden..
1. Gå til handlingsruden, og vælg **Ny**.
1. Vælg det lagersted, du tidligere har oprettet, på rullelisten **Lagersted**.
1. Angiv et navn i feltet **Gang** (f.eks. &quot;Def").
1. Angiv et navn i feltet **Navn** (f.eks. "Standardgang").
1. Gå til handlingsruden, og vælg **Gem**.

## <a name="set-up-warehouse-inventory-locations"></a>Konfigurer lokationer til lagerstedets lager

Gør følgende, hvis du vil oprette lokationer til lagerstedets lager for standard, beskadiget og returneret lager.

1. Gå til **Moduler \> Detail og handel \> Konfiguration af kanal \> Lagersteder** i navigationsruden.
1. Vælg det lagersted, som du oprettede tidligere.
1. Vælg **Rediger** i handlingsruden.
1. Vælg **Lagersted** i handlingsruden, og vælg derefter **Lagerlokation**.
1. Gå til handlingsruden, og vælg **Ny**. Rullelisten **Lagersted** bør som standard vise dit nye lagersted.
    1. Angiv navnet på den gang, du har angivet tidligere, i fetlet **Gang**. 
    1. Angiv **Manuel opdatering** til **Ja**
    1. Angiv navnet på lagerstedet i feltet **Sted**.
    1. Gå til handlingsruden, og vælg **Gem**.
 1. Gå til handlingsruden, og vælg **Ny**.  Rullelisten **Lagersted** bør som standard vise dit nye lagersted.
    1. Angiv navnet på den gang, du har angivet tidligere, i fetlet **Gang**.  
    1. Angiv **Manuel opdatering** til **Ja**
    1. Angiv "Beskadiget" i feltet **Sted**.
    1. Gå til handlingsruden, og vælg **Gem**.
 1. Gå til handlingsruden, og vælg **Ny**.  Rullelisten **Lagersted** bør som standard vise dit nye lagersted.
    1. Angiv navnet på den gang, du har angivet tidligere, i fetlet **Gang**. 
    1. Angiv **Manuel opdatering** til **Ja**
    1. Angiv "Returneringer" i feltet **Sted**.
    1. Gå til handlingsruden, og vælg **Gem**.
    
Følgende billede viser opsætningen af en lagerlokation til et lagersted i San Francisco.

![Eksempel på opsætning af lagerlokation.](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a>Akslut konfigurationen af lagerstedet

Gør følgende for at fuldføre konfigurationen af lagerstedet.

1. Gå til **Moduler \> Detail og handel \> Konfiguration af kanal \> Lagersteder** i navigationsruden.
1. Vælg det lagersted, som du oprettede tidligere.
1. Vælg **Rediger** i handlingsruden.
1. Under **Lager- og lokationsstyring**:
    1. Angiv **Standardplacering for modtagelse** til den standardlokalitet, der blev oprettet ovenfor.
    1. Vælg **Standardafgangslokation** til den standardlokalitet, der blev oprettet ovenfor.
1. Angiv en adresse på lagerstedet i sektionen **Adresser**.
1. Under sektionen **Detail**: 
    1. Angiv placeringen for returnering, der tidligere blev oprettet, i feltet **Placering af standardreturnering**.
    1. Angiv **Butik** til **Ja**.
    1. Angiv **Vægt** til **1,00**. 
    1. Angiv standardplaceringen, der tidligere blev oprettet, i feltet **Lagerdimensioner**.
1. Angiv **Fysisk negativt lager** til **Ja** under afsnittet **Lagersted**.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser oplysninger om et konfigureret lagersted.

![Eksempel på konfigureret lagersted.](media/warehouse-sample.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over lagerstedsstyring](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[Oversigt over kanaler](channels-overview.md)

[Forudsætninger for konfiguration af kanal](channels-prerequisites.md)

[Konfigurer en detailkanal](channel-setup-retail.md)
    
[Konfigurere en onlinekanal](channel-setup-online.md)

[Konfigurere en callcenter-kanal](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
