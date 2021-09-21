---
title: Id'en kan ikke flyttes, hvis Blank afgang og Blank kvittering er tilladt
description: Id'en kan ikke flyttes, hvis serienummeret har Blank afgang og Blank kvittering tilladt. Dette gøres fast ved at gøre serienummerfeltet valgfrit.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0047f79aa417c8fc910447505f07963d014f54e7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475896"
---
# <a name="cant-move-license-plate-if-serial-number-has-blank-issue-and-blank-receipt-allowed"></a>Id'en kan ikke flyttes, hvis serienummeret har Blank afgang og Blank kvittering tilladt

## <a name="symptoms"></a>Symptomer

Du kan ikke flytte et id ved at bruge menupunktet **Bevægelse**, hvis serienummeret har indstillingen *Blank afgang tilladt* og *Blank tilgang tilladt* i sporingsdimensionsgruppen, og hvis der er flere id'er på samme lokation, hvoraf nogle har serienumre og nogle ikke har dem.

## <a name="resolution"></a>Løsning

Dette problem løses af de ændringer, der implementeres i [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). Disse ændringer gør feltet **Serienummer** valgfrit, når blank tilgang og blank afgang er tilladt.
