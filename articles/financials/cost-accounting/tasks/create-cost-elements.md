---
title: Oprette omkostningselementer .
description: Du kan oprette omkostningselementer i omkostningsregnskab på flere måder.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cceec1d52e1b5b2a05525c8d96f46dece17363b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841291"
---
# <a name="create-cost-elements"></a>Oprette omkostningselementer . 

[!include [task guide banner](../../includes/task-guide-banner.md)]

Du kan oprette omkostningselementer i omkostningsregnskab på flere måder. Denne procedure viser, hvordan du opretter omkostningselementer ved at importere hovedkonti via en dataconnector. Demofirmaet USMF bruges til at oprette denne procedure. Denne fremgangsmåde er til en funktion for omkostningsregnskab, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="create-new-cost-elements"></a>Opret nye omkostningselementer
1. Gå til Omkostningsregnskab > Dimensioner > Dimensioner for omkostningselement.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
4. Indtast eller vælg en værdi i feltet Dataconnector for dimensionsmedlemmer.
5. Skriv en værdi i feltet Beskrivelse.
6. Klik på Gem.

## <a name="configure-the-data-connector"></a>Konfigurer dataconnectoren
1. Klik på Konfigurer leverandør af dimensionsmedlem.
2. Indtast eller vælg en værdi i feltet Kontoplan.
    * Vælg Delt for at bruge den delte kontoplan.  
3. Klik på Ny.
4. Markér den valgte række på listen.
    * Du kan anvende filtre på konti, der opfylder dine kriterier.  
5. Indtast eller vælg en værdi i feltet Fra hovedkonto.
6. Indtast eller vælg en værdi i feltet Til hovedkonto.
7. Klik på OK.

## <a name="import-main-accounts"></a>Importér hovedkonti
1. Klik på Importér dimensionsmedlemmer.
    * Hovedkonti importeres til omkostningsregnskab og bruges som omkostningselementer.  
2. Klik på OK.

## <a name="view-the-imported-accounts-as-cost-elements"></a>Se importerede konti som omkostningselementer
1. Klik på Vis dimensionsmedlemmer.
    * Se de importerede finanskonti som omkostningselementer i din virksomhed, som omkostninger kan flyde til.  

