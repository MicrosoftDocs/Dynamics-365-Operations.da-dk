---
title: Antal, der ikke er gyldigt til plukarbejde med flere LP'er
description: Antallet er ikke gyldigt for hver-enheden, når der er plukarbejde, der har flere id'er på én lokation. Kontroller, at følgende felter er korrekte.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5b245f71e80339fee3e42cfffa0396078a56926e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475863"
---
# <a name="quantity-not-valid-when-theres-picking-work-with-multiple-lps-in-one-location"></a>Antal ikke gyldigt, når der er plukarbejde med flere id'er på én lokation

## <a name="symptoms"></a>Symptomer

Antallet er ikke gyldigt for *ea*-enheden, når der er plukarbejde, der har flere id'er på én lokation, og du modtager følgende fejlmeddelelse.

> Antallet er ugyldigt for enheden 1%.

## <a name="resolution"></a>Løsning

Kontrollér, at felterne **Enhedsseriegruppe-id** og **Enhedsomregninger** på det frigivne produkt eller den frigivne produktvariant er angivet korrekt.

Bemærk, at fejlmeddelelsen er blevet forbedret i version 10.0.15 til at vise forventet antal (se [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Den nye fejlmeddelelse er:

> Antallet er ugyldigt. Forventet %1 %2.
