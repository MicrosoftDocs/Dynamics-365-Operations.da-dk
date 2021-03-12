---
title: Batchattributter
description: Dette emne indeholder oplysninger om batchattributter. Batchattributter er karakteristika for de råvarer og færdigvarer, der udgør lagerbatches. I dette emne forklares også, hvordan du tildeler batchattributter, og hvordan du kan søge efter dem, når du reserverer batchnumre.
author: ShylaThompson
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5e2a27fe73ddd9fcd7cafc0ded05fd8a15841fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966499"
---
# <a name="batch-attributes"></a>Batchattributter

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om batchattributter. Batchattributter er karakteristika for de råvarer og færdigvarer, der udgør lagerbatches. I dette emne forklares også, hvordan du tildeler batchattributter, og hvordan du kan søge efter dem, når du reserverer batchnumre.

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



