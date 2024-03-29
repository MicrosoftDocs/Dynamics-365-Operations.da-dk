---
title: Oprette og tildele avancerede regelstrukturer
description: Denne artikel forklarer, hvordan du opretter og tildeler en avanceret regelstruktur i en kontostruktur.
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72688642936f9428c96aebb34bf9f240dd48b46b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896313"
---
# <a name="create-and-assign-advanced-rule-structures"></a>Oprette og tildele avancerede regelstrukturer

[!include [banner](../../includes/banner.md)]

Denne artikel forklarer, hvordan du opretter og tildeler en avanceret regelstruktur i en kontostruktur. Denne guide anvender demofirmaet USMF.

## <a name="create-an-advanced-rule-structure"></a>Opret en avanceret regelstruktur
1. Gå til Finans **Navigationsrude > Moduler > Finans > Kontoplan > Strukturer > Avancerede regelstrukturer**.
2. Vælg **Ny** for at åbne dialogboksen Slip.
3. I feltet **Avanceret regelstruktur** skal du skrive et navn, som beskriver regelstrukturen.
4. Vælg **OK**.
5. Vælg **Tilføj segment**.
6. Listen over segmenter, skal du vælge en økonomisk dimension. For eksempel **Butik**.  
7. Vælg **Tilføj segment**.
8. Vælg **Aktivér**.

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a>Anvende en avanceret regelstruktur for en kontostruktur
1. Gå til **Navigationsrude > Moduler > Finans > Kontoplan > Strukturer > Konfigurer kontostrukturer**.
2. Søg på listen, og vælg den kontostruktur, som du vil anvende den avancerede regel for.
3. Vælg **Rediger**. Du kan også vælge **Avancerede regler**, hvorefter du bliver bedt om at sætte kontostrukturen i **Kladdetilstand**.  
4. Vælg **Avancerede regler**.
5. Vælg **Ny** for at åbne dialogboksen Slip.
6. Skriv en værdi i feltet **Avanceret regel**.
7. Skriv en værdi i feltet **Navn**.
8. Vælg **Opret**.
9. Klik på **Tilføj nyt kriterie**.
10. Vælg hovedkontoen eller en økonomisk dimension i feltet **Hvor**.
11. Vælg en indstilling i feltet **Operatør**, f.eks. er **mellem** eller **inkluderer**.
12. Skriv en værdi i feltet **Værdi**.
13. Skriv en værdi i feltet **værdi**.
14. Vælg **Tilføj** for at åbne dialogboksen.
15. På listen, kan du finde den avancerede regelstruktur, som du vil bruge, når de kriterier, du har angivet, er opfyldt.
16. Vælg **Tilføj**.
17. Luk siden.
18. Vælg **Aktivér**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
