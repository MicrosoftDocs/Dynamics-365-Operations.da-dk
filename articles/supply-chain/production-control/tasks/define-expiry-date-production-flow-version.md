---
title: Definere en udløbsdato for en produktionsflowversion
description: For at afslutte gyldigheden og behandlingen af en version af produktionsflowet på en given dato eller for at planlægge udskiftningen af en aktiv version med en ny version, skal du angive en udløbsdato for versionen.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10260290fba02ebf9313d0d1355c9aa28e3509d7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843691"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>Definere en udløbsdato for en produktionsflowversion

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

