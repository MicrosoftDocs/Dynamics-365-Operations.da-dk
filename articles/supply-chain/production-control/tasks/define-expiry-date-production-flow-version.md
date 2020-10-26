---
title: Definere en udløbsdato for en produktionsflowversion
description: For at afslutte gyldigheden og behandlingen af en version af produktionsflowet på en given dato eller for at planlægge udskiftningen af en aktiv version med en ny version, skal du angive en udløbsdato for versionen.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97ac33d28a49ad0f2a3956ad65b159e4ec4785c7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983248"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>Definere en udløbsdato for en produktionsflowversion

[!include [banner](../../includes/banner.md)]

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

