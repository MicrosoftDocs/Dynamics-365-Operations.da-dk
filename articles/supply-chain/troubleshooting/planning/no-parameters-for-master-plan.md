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
ms.openlocfilehash: d039b79684f87e7791fb9dae7cbdc6ced220bc092d9a0ab624616c1c345986da
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756769"
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
