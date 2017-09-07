--- 
title: Vedligeholde styklisten for en produktkonfigurationsmodel
description: "Kørsel af denne procedure kræver en eksisterende model til produktkonfiguration."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 645d748235935ae67867295a87a84a6539710ab0
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Vedligeholde styklisten for en produktkonfigurationsmodel

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kørsel af denne procedure kræver en eksisterende model til produktkonfiguration. Højttaler af topkvalitet-modellen i demofirmaet USMF bruges til at oprette denne procedure.


## <a name="add-a-bom-line"></a>Tilføj en styklistelinje
1. Klik på Definition af produktvariantmodel.
2. Klik på Produktkonfigurationsmodeller.
3. Find og vælg den ønskede post på listen.
    * Vælg Højttaler af topkvalitet for denne procedure.  
4. Klik op linket i den valgte række på listen.
5. Udvid afsnittet Styklistelinjer.
6. Klik på Tilføj.
7. Skriv en værdi i feltet Navn.
8. Skriv en værdi i feltet Beskrivelse.
9. Klik på Gem.

## <a name="add-bom-line-details"></a>Tilføj Linjedetaljer i stykliste
1. Klik på Linjedetaljer i stykliste.
2. Indtast eller vælg en værdi i feltet Varenummer.
    * Du kan f.eks. vælge elementet M0055.  
    * For hver stykliste linjeegenskab kan du vælge, om den har en fast værdi eller er knyttet til en attribut.  
3. Marker afkrydsningsfeltet Indstil.
4. Vælg Ja i feltet Beregning.
    * Når du indstiller egenskaben Beregning til Ja sikrer du, at styklistelinjen medtages i omkostningsberegninger.  
5. Klik på fanen Opsætning.
6. Marker afkrydsningsfeltet Indstil.
7. Angiv et tal i feltet Antal.
    * Antalsfeltet bestemmer, hvor meget af elementet, der skal medtages i styklisten. Dette kunne være en oplagt kandidat til en attributtilknytning.  
8. Klik på fanen Dimension.
    * Kontroller, hvis nogen af produktdimensionerne er aktive og derfor skal have en værdi eller en attribut tildelt.  
9. Klik på OK.

