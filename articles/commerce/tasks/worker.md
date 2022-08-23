---
title: " Konfigurere en arbejder"
description: Denne fremgangsmåde viser, hvordan du konfigurerer en arbejder som en sælger, der er berettiget til provision på salg i POS.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
ms.openlocfilehash: 8bbd3899da8e289dcf82fabc0fd21370655f38e0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276041"
---
# <a name="configure-a-worker"></a> Konfigurere en arbejder

[!include [banner](../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du konfigurerer en arbejder som en sælger, der er berettiget til provision på salg i POS. Proceduren bruger USRT-demodatafirmaet.


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
1. Gå til Retail og Commerce > Medarbejdere > Arbejdere.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
4. Klik på fanen Commerce.
    * En arbejder kan tildeles til en standardsalgsgruppe. Standardsalgsgruppen føjes automatisk til salgslinjerne i POS, hvis indstillingen er aktiveret i funktionalitetsprofilen for butikken.  
5. Klik på Rediger.
6. Indtast eller vælg en værdi i feltet Standardgruppe.
7. Klik på Gem.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
