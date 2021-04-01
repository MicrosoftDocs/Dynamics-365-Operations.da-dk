---
title: Konfigurere tillægsgebyrer og tilbehørsmastere for hub
description: Denne fremgangsmåde viser, hvordan du opretter en tillægsmaster for en hub og bruger denne master til at oprette et gebyr for hubtillæg.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb2e9125c7a38d1dc5e6866a056fb71f25e40928
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233673"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a>Konfigurere tillægsgebyrer og tilbehørsmastere for hub

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du opretter en tillægsmaster for en hub og bruger denne master til at oprette et gebyr for hubtillæg. Proceduren bruger USMF-datasættet. Denne konfiguration vil normalt blive udført af en transportkoordinator.


## <a name="set-up-a-hub-master"></a>Konfigurer en hubmaster
1. Gå til Transportstyring > Opsætning > Klassificering > Tilbehørsmastere.
2. Klik på Ny.
3. Skriv en værdi i feltet Tilbehørsmaster.
4. Skriv en værdi i feltet Navn.
5. Vælg "Hub" i feltet Tilbehørstype.
6. Klik på Gem.
7. Luk siden.

## <a name="set-up-a-hub-accessorial-charge"></a>Konfigurer et gebyr for hubtillæg
1. Gå til Transportstyring > Opsætning > Klassificering > Gebyrer for hubtillæg.
2. Klik på Ny.
3. Indtast en værdi i feltet Id for hubtilbehør.
4. Klik på rullelisten i feltet Hub for at åbne opslaget.
5. Find og vælg den ønskede post på listen.
6. Vælg en indstilling i feltet Hubposition.
    * Du kan enten oprette gebyret som en afhentning eller levering. Afhængigt af dit valg anvendes gebyret på det tilsvarende transportsegment på ruten.  
7. Klik på rullelisten i feltet Tilbehørsmaster for at åbne opslaget.
8. Klik op linket i den valgte række på listen.
    * Vælg den master, du lige oprettet.  
9. Klik på Gem.
10. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]