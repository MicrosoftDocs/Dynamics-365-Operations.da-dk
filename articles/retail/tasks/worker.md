--- 
title: " Konfigurere en arbejder"
description: "Denne fremgangsmåde viser, hvordan du konfigurerer en detailarbejder som en sælger, der er berettiget til provision på salg i POS."
author: jblucher
manager: AnnBe
ms.date: 02/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 27b075cf1152f16fc4726b224e877eacb2f2572c
ms.contentlocale: da-dk
ms.lasthandoff: 02/07/2018

---
# <a name="configure-a-worker"></a> Konfigurere en arbejder

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du konfigurerer en detailarbejder som en sælger, der er berettiget til provision på salg i POS. Proceduren bruger USRT-demodatafirmaet.


## <a name="create-a-commission-sales-group-for-the-worker"></a>Opret en provisionssalgsgruppe for arbejderen
1. Gå til Salg og marketing > Provisioner > Salgsgrupper.
    * Arbejdere kan tildeles til en eller flere salgsgrupper. I POS kan du vælge en salgsgruppe, der indeholder arbejdere fra butikkens adressekartotek.  
2. Klik på Ny.
3. Skriv en værdi i feltet Gruppe.
4. Skriv en værdi i feltet Navn.
5. Klik på Gem.
6. Klik på Generelt i handlingsruden.
7. Klik på Sælger.
    * En salgsgruppe kan indeholde mere end én medarbejder. Provisioner kan opdeles mellem arbejdere baseret på, hvordan du definerer kommissionen.  
8. Indtast eller vælg en værdi i feltet Navn.
9. Angiv et tal i feltet Provisionsandel.
10. Klik på Gem.
11. Luk siden.
12. Luk siden.

## <a name="assign-the-workers-default-sales-group"></a>Tildel standardsalgsgruppen for arbejdere
1. Gå til Detail og handel > Medarbejdere > Alle arbejdere.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
4. Klik på fanen Detail.
    * En arbejder kan tildeles til en standardsalgsgruppe. Standardsalgsgruppen føjes automatisk til salgslinjerne i POS, hvis indstillingen er aktiveret i funktionalitetsprofilen for butikken.  
5. Klik på Rediger.
6. Indtast eller vælg en værdi i feltet Standardgruppe.
7. Klik på Gem.


