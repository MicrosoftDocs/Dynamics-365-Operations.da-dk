--- 
title: "Tilføje en foregående aktivitet til en produktionsflowversion"
description: "Alle aktiviteter skal angives i rækkefølge i en produktionsflowversion."
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d19fb20e8cc941daeaa506e4bf1cb0c7031cf2ee
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Tilføje en foregående aktivitet til en produktionsflowversion

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Alle aktiviteter skal angives i rækkefølge i en produktionsflowversion. En aktivitet kan have en eller flere foregående eller efterfølgende opgaver. 

Denne fremgangsmåde viser, hvordan du knytter en foregående opgave til en aktivitet. 

Hvis du vil udføre denne opgave, skal du bruge et produktionsflow, der har kladdeversionen med mindst to aktiviteter, som kan forbindes. 

Du kan få mere at vide ved at læse hvidbogen "Production flows and activities in lean manufacturing".


## <a name="find-the-production-flow-and-version"></a>Find produktionsflow og -version
1. Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
4. Find og vælg den ønskede post på listen.
5. Klik på Aktiviteter.

## <a name="select-an-activity-and-add-a-predecessor"></a>Vælg en aktivitet, og tilføj en foregående opgave
1. Find og vælg den ønskede post på listen.
2. Klik på Tilføj foregående aktivitet.
3. Indtast eller vælg en værdi i feltet Aktivitet.
4. Angiv et tal i feltet Procestidsforhold.
    * Standardprocestidsforholdet for en aktivitetsrelation er 1. Dette forudsætter, at begge aktiviteter kører i samme tempo eller takttid. Hvis den foregående opgave kører i et højere tempo (lavere takttid), skal forholdet være mindre end 1, hvis den foregående opgave kører i et langsommere tempo (højere takttid) og procestidsforholdet er større end 1.  
5. Klik på OK.


