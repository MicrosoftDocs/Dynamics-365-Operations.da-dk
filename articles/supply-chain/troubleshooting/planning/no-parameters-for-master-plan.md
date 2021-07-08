---
title: Der findes ikke parametre for behovsplanen
description: Når du forsøger at autorisere et ordreforslag, modtager du en fejlmeddelelse om, at der ikke findes parametre for behovsplanen.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294040"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a>Der findes ikke parametre for behovsplanen

Fejlkode: SYS25368

## <a name="symptoms"></a>Symptomer

Når du forsøger at autorisere et ordreforslag, får du vist følgende fejlmeddelelse:

> Parametre for behovsplan %1 findes ikke.

## <a name="cause"></a>Årsag

På grund af konfigurationsproblemer kan systemet ikke finde indstillingerne for den angivne plan.

## <a name="resolution"></a>Løsning

- Gå til **Varedisponering \> Konfiguration \> Planer \> Behovsplaner**, og kontrollér, at der findes en plan med det angivne navn.
