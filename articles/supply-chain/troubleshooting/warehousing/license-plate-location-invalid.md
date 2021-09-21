---
title: Ugyldigt id eller lokationsfejl i mobilappen
description: Når du scanner et nummerplade-id eller en lokation, kan du få vist denne fejlmeddelelse, der er ugyldig. Kontrollér, at nummerplade-id'et ikke er reserveret af noget andet.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f9f10dbade0d13b8fc4b0fc92981d84e6e28e83e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475955"
---
# <a name="invalid-license-plate-or-location-error-when-scanning-in-the-mobile-app"></a>Ugyldigt id eller lokationsfejl ved scanning af mobilappen

## <a name="symptoms"></a>Symptomer

Når du scanner et nummerplade-id eller en lokation, kan du få vist følgende fejlmeddelelse.

> Nummerpladen eller lokationen er ugyldig.

## <a name="resolution"></a>Løsning

Kontrollér, at nummerplade-id'et ikke er reserveret af noget andet. Dette problem opstod, når den værdi, som en bruger scannede i mobilappen Warehouse Management, både var en gyldig lokation og et gyldigt nummerplade-id. Dette problem blev dog løst i version 10.0.11.
