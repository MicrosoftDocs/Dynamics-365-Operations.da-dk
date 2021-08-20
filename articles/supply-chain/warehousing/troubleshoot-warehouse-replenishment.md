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
ms.openlocfilehash: 251dc174d52d754a0c488d5becf63f1a43f9bd30034036d10086c9803060b5a0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758394"
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