---
title: Batchattributter
description: "Denne artikel indeholder oplysninger om batchattributter. Batchattributter er karakteristika for de råvarer og færdigvarer, der udgør lagerbatches. I artiklen forklares også, hvordan du tildeler batchattributter, og hvordan du kan søge efter dem, når du reserverer batchnumre."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 80e64323700dad5cb93539a46fdc858a6f555a34
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017

---

# <a name="batch-attributes"></a>Batchattributter

[!include[banner](../includes/banner.md)]


Denne artikel indeholder oplysninger om batchattributter. Batchattributter er karakteristika for de råvarer og færdigvarer, der udgør lagerbatches. I artiklen forklares også, hvordan du tildeler batchattributter, og hvordan du kan søge efter dem, når du reserverer batchnumre.

Batchattributter er karakteristika for de råvarer og færdigvarer, der udgør lagerbatches. Batchattributter kan være forskellige, afhængigt af faktorer, som f.eks. miljømæssige forhold eller kvaliteten af de råvarer, der bruges til batchfremstillingen, eller udfaldet at færdigvarer. Antallet og typerne af batchattributter, der bruges, kan variere meget fra branche til branche. Her er to eksempler på, hvordan du kan bruge batchattributter:

-   Inden for osteindustrien, hvor mælk, der er en af de råvarer, der bruges til fremstillingen af ost, kan have attributter som f.eks. fedtindhold og vægtet procent. Den ost, der fremstilles af mælken, kan have andre attributter, som fugtighed og alder.
-   Inden for stålindustrien kan det jern, der fremstilles, have attributter som f.eks. procentvis indhold af magnesium, indhold af sølv og indhold af zink.

For bedre at administrere antallet og typerne af attributter kan du bruge batchattributgrupper. På denne måde kan du ikke tilføje attributterne enkeltvist.

## <a name="assign-batch-attributes"></a>Tilknyt batchattributter
Du kan knytte batchattributter til de enkelte produkter, der opbevares i lagerbatches, eller du kan tildele dem til produkter, der er knyttet til bestemte debitorer. Før du kan tildele en batchattribut på debitorniveau, skal du først tildele den på produktniveau. Batchdimensionen for produktet skal være angivet til **Aktiv** i sporingsdimensionsgruppen. Hvis du vil tildele en batchattribut til et enkelt produkt, skal du bruge den produktspecifikke side. Hvis attributten er specifik for et produkt til en debitor, skal du bruge den debitorspecifikke side. Når du føjer en attribut til et produkt, skal du også definere andre parametre. Her er nogle eksempler:

-   Minimum- og maksimumintervallerne for attributten **Heltal** eller **Del**.
-   Tolerancehandlingerne for en attribut af typen **Heltal** eller **Del**. Hvis attributten falder uden for minimum- og maksimumintervallet, kan handlingen være enten en advarsel eller en fejlmeddelelse.
-   Destinationsværdien for attributten. Denne værdi er den valgfri værdi for attributten, og den gælder for alle attributtyper.

Du kan åbne siderne for produkter, du vælger på siden **Frigivne produkter** i Administration af produktoplysninger. Når du har føjet batchattributter til et produkt, kan du føje specifikke værdier til attributterne på siden **Lagerbatchattributter**.

## <a name="reserve-batches"></a>Reservere batches
Du kan søge efter batchattributter, når du foretager batchreservationer for en salgsordre for at opfylde en kundeordre, eller når du plukker og reserverer batches til en produktionsordre. Du kan bruge søgningen til at finde en lagerbatch, der indeholder produktet med den ønskede batchattribut. Når du har fundet den eller de ønskede batches, kan du reservere produktet til den oprindelige lagertransaktionslinje.



