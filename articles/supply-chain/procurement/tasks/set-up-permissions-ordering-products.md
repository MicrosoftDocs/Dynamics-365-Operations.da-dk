--- 
title: "Konfigurere tilladelser til bestilling af produkter på vegne af en anden person"
description: "Denne fremgangsmåde viser, hvordan du kan give arbejdere tilladelse til at oprette indkøbsrekvisitioner på vegne af andre arbejdere."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9e003f953c05facd5516e2bfa6d1c83ba6381c15
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Konfigurere tilladelser til bestilling af produkter på vegne af en anden person

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du kan give arbejdere tilladelse til at oprette indkøbsrekvisitioner på vegne af andre arbejdere. Med andre ord kan "klargøreren" af en indkøbsrekvisition oprette en rekvisition for en anden "anmoder." Proceduren viser også, hvordan du kan tildele en arbejder rettigheder til at bestille varer og tjenester i forskellige juridiske enheder eller driftsenheder. Disse opgaver udføres typisk af en indkøbschef. Du kan enten bruge denne procedure dataene i USMF-demodatafirmaet eller dine egne data.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Tildel tilladelse til at indtaste indkøbsrekvisitioner på vegne af en anden arbejder
1. Gå til Indkøb og forsyning > Konfiguration > Politikker > Tilladelser til indkøbsrekvisitioner.
    * Sørg for, at feltet Aktuel visning er angivet til Efter klargører.  På listen i venstre rude vises de personer, der kan gives tilladelse til at oprette indkøbsrekvisitioner på vegne af andre personer.  
2. Vælg den person, du vil give tilladelse til (klargøreren).
3. Klik på Tilføj.
4. Find og vælg den person, der skal tilføjes som anmoder.
    * Anmoderen er den person, der klargøreren kan oprette indkøbsrekvisitioner på vegne af.  
    * Vælg Specifik i feltet Godkendelse, hvis klargøreren skal være i stand til at oprette indkøbsrekvisitioner på vegne af den valgte arbejder. Vælg Rapportering, hvis klargøreren også skal være i stand til at oprette indkøbsrekvisitioner på vegne af alle arbejdere, der rapporterer til denne arbejder.  
5. Angiv en dato i feltet Gældende.
6. Angiv en dato i feltet Udløb.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Vis klargørere, der har tilladelse til at oprette indkøbsrekvisitioner for en valgt arbejder
1. Vælg 'Efter anmoder' i feltet Aktuel visning.
    * I denne visning kan du få vist en liste over klargørere, der har fået tilladelse til at oprette indkøbsrekvisitioner på vegne af en valgt arbejder.  
2. Brug Quick Filter til at finde den medarbejder, som du netop har tilføjet, som anmoder.
3. Vælg anmoderen.
    * Listen Klargører viser de personer, der har tilladelse til at bestille varer på vegne af den anmoder, der er valgt i venstre rude.   Du kan tilføje yderligere klargørere her.   I denne visning kan du også give anmoderen tilladelse til at oprette indkøbsrekvisitioner i juridiske enheder og driftsenheder, der ikke er den pågældende persons primære juridiske enhed eller driftsenhed.  


