---
title: Foretage fejlfinding i forbindelse med genopfyldning af lagersted
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med genopfyldning af lagersted i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8940f729e1115405e8d6e50eccc92d9fffe37f3e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828076"
---
# <a name="troubleshoot-warehouse-replenishment"></a>Foretage fejlfinding i forbindelse med genopfyldning af lagersted

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med genopfyldning af lagersted i Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>Jeg får følgende fejlmeddelelse: "Arbejdet %1 kan ikke ophæves, fordi det har uafsluttet genopfyldningsarbejde".

### <a name="issue-description"></a>Problembeskrivelse

Pluk af arbejde blokeres på grund af afhængigt genopfyldningsarbejde.

### <a name="issue-resolution"></a>Problemløsning

Når du bruger bølgeefterspørgsel til genopfyldning, opretter systemet både genopfyldningsarbejdet og plukarbejdet, hvis en plukplads skal genopfyldes for at opfylde kildeordrebehovet. Den blokerer dog plukarbejdet, indtil genopfyldningsarbejdet fuldføres. Denne funktionsmåde er bevidst, fordi plukpladsen ikke har nok lager, medmindre genopfyldningsarbejdet er fuldført. Fuldfør genopfyldningsarbejdet, og kør derefter plukarbejdet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]