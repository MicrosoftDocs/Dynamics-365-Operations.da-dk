---
title: Der udskrives kun én label for flere arbejdshoveder på en enkelt kvittering
description: Der udskrives kun én label for flere arbejdshoveder på en enkelt kvittering.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026370"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>Der udskrives kun én label for flere arbejdshoveder på en enkelt kvittering

KB-nummer: 4614667

## <a name="symptoms"></a>Symptomer

Der oprettes flere arbejdshoveder for samme mål-id som del af en enkelt lagerstedsapp, der modtager hændelsen. Der udskrives dog kun én id-label, når produktet modtages.

## <a name="resolution"></a>Løsning

Systemet fungerer som designet.

I det aktuelle design oprettes der altid en enkelt id-label, uanset hvor mange arbejdshoved- og arbejdslinjekombinationer der findes. Den genererede label indeholder oplysninger om kun én kombination.

Du kan løse dette problem ved at sikre, at oprettelsen af arbejdshovedet altid kun er knyttet til ét mål-id.
