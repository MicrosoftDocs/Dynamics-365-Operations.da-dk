---
title: Behandle og spore kildedata
description: Al databehandling køres af job.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a23443c985ac681c8c31956ae5ea3e513337577
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441691"
---
# <a name="process-and-trace-source-data"></a>Behandle og spore kildedata

[!include [banner](../../includes/banner.md)]

Al databehandling køres af job. Der oprettes en kladde for hvert job og dataprovider for at dokumentere, at processen blev kørt, og at posterne blev behandlet i det aktuelle job. Du kan bruge denne procedure til at konfigurere en datakilde og derefter spore oprindelsen til en bestemt omkostningspost. Denne registrering bruger USP2-demodatafirmaet. Før du udfører denne opgave, skal du sørge for at afspille følgende opgaveguider: "Oprette en finanspost for omkostningsregnskab", "Definere kontrolenheder for omkostninger" og "Administrere datakilde til finansposten for omkostningsregnskabet".

1. Gå til Omkostningsregnskab > Opsætning Finans > Finansposter for omkostningsregnskab.
2. Find og vælg den ønskede post på listen.
    * Vælg den finanspost i omkostningsregnskabet, du oprettede tidligere.  
3. Klik på Faktiske versioner.
4. Klik på Behandling af kildedata i handlingsruden.
5. Klik på Overførselskladder for finansposteringer.
6. Find og vælg den ønskede post på listen.
7. Klik på Kladdeposteringer.
8. Markér den valgte række på listen.
9. Klik på Omkostningsposter.
10. Klik på Kildepost.
11. Klik på Behandling af kildedata i handlingsruden.
12. Klik på Finans.
13. Indtast eller vælg en værdi i feltet Regnskabskalenderperiode.
    * Vælg regnskabsårets 2017 periode 9 i dette eksempel.  
14. Klik på OK.

