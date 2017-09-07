--- 
title: "Definere en udløbsdato for en produktionsflowversion"
description: "For at afslutte gyldigheden og behandlingen af en version af produktionsflowet på en given dato eller for at planlægge udskiftningen af en aktiv version med en ny version, skal du angive en udløbsdato for versionen."
author: cvocph
manager: AnnBe
ms.date: 10/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: b968502de357779b7d26a5780f3febc3076dd9ad
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>Definere en udløbsdato for en produktionsflowversion

[!include[task guide banner](../../includes/task-guide-banner.md)]

For at afslutte gyldigheden og behandlingen af en version af produktionsflowet på en given dato eller for at planlægge udskiftningen af en aktiv version med en ny version, skal du angive en udløbsdato for versionen. Det er ikke nødvendigt at deaktivere versionen.


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a>Angiv en udløbsdato for at afslutte en produktionsflowversion
1. Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.
2. Find og vælg den ønskede post på listen.
    * Vælg et produktionsflow med en version, der allerede er defineret.  
3. Klik op linket i den valgte række på listen.
4. Klik på Rediger.
5. Markér den valgte række på listen.
6. Angiv dato og klokkeslæt i feltet Udløbsdato.
    * For udløbsdatoen starter der ikke eller deaktiveres der ikke en ny version. Det vil heller ikke længere være muligt at oprette eller starte job for denne produktionsflow. Du kan stadig fuldføre igangsatte job efter udløbsdatoen.  

