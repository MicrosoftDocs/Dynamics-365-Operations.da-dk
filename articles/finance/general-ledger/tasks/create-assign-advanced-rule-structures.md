---
title: Oprette og tildele avancerede regelstrukturer
description: I dette emne forklares, hvordan du opretter og tildeler en avanceret regelstruktur i en kontostruktur.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb18b96d6d7db84262f8fcfadb15afa80e2fa3d8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441442"
---
# <a name="create-and-assign-advanced-rule-structures"></a>Oprette og tildele avancerede regelstrukturer

[!include [banner](../../includes/banner.md)]

I dette emne forklares, hvordan du opretter og tildeler en avanceret regelstruktur i en kontostruktur. Denne guide anvender demofirmaet USMF.

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

