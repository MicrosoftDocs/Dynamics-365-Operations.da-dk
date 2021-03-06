---
title: Bogfør anlægsaktivposteringer i posteringslag
description: Denne artikel giver et overblik over bogføringslagets funktionalitet for anlægsaktivposteringer.
author: moaamer
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d1c66df39c9712a5d4d26ba4eaa1ce079719c31
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832988"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Bogfør anlægsaktivposteringer i posteringslag

[!include [banner](../includes/banner.md)]

Denne artikel giver et overblik over bogføringslagets funktionalitet for anlægsaktivposteringer.

Et anlægsaktiv afskrives ofte på forskellige måder til forskellige formål. Afskrivningen til skattemæssige formål beregnes ud fra de aktuelle skatteregler for at opnå den højest mulige afskrivning før skat, mens afskrivning til bogføringsmæssige formål beregnes ud fra regnskabslove og -standarder. De forskellige slags afskrivning beregnes og bogføres separat i posteringslagene.

Hver bog, der tilknyttes et anlægsaktiv, oprettes til et bestemt posteringslag med et overordnet afskrivningsformål. Der er ti posteringslag: aktuelle, operationer, skat og syv brugerdefinerede lag. Du kan også deaktivere bogføring i finansmodulet for bogen ved at angive feltet Bogfør i finans felt til Nej. Feltet Posteringslag, angives derefter automatisk til Ingen. Typisk bruges bøger, der ikke bogføres i finansmodulet, til momsrapporteringen. Denne fremgangsmåde giver dig yderligere fleksibilitet til at slette historiske posteringer for anlægsaktivkartoteket, fordi de ikke er gemt i finansmodulet.

Anlægsaktivkladder defineres ved hjælp af siden Kladdenavne via Finans > Konfiguration af kladde > Kladdenavne. Hver af de kladder, som du kan bogføre afskrivninger i, defineres ud fra sit kladdenavn for kun ét posteringslag. Posteringslaget i kladden kan ikke ændres. Denne begrænsning hjælper med at sikre, at posteringerne for hvert posteringslag holdes adskilt. Der skal oprettes mindst ét kladdenavn for hvert posteringslag. Hvis du bruger bøger, der ikke bogføres i finansmodulet, skal du også oprette en kladde, hvor posteringslaget er angivet til Ingen.

Du kan angive finanskonti for anlægsaktivposter på siden Posteringsprofiler for anlægsaktiver. For hver posteringsprofil skal du vælge den relevante posteringstype og bog og derefter tildele finanskontiene. Opret en bogføringsprofilpost for hver bog, der skal bogføres i finansmodulet.

Anlægsaktivet kan angives i dokumenter, der kun understøtter det **Aktuelle** posteringslag, f. eks. **Indkøbsordre**, **Ventende kreditorfaktura**, **Salgsordre** eller **Fritekstfaktura**. Når du vælger et anlægsaktiv-ID i et af disse dokumenter, filtreres anlægsaktivet til kartoteket med det **Aktuelle** posteringslag og udfyldes automatisk under bogføringen, når systemet kontrollerer, at posteringslaget for anlægsaktiver er **Aktuelt**. Hvis denne validering ikke kan fuldføres, vil bogføringsprocessen blive stoppet. 

> [!NOTE] 
> Hvis du bruger afledte bøger, kan du bogføre posteringer på forskellige posteringslag samtidig. Transaktionerne for det primære kartotek oprettes i en kladde eller kildedokument, der svarer til posteringslaget for kartotekets posteringslag. Under posteringen bogføres de afledte bogposteringer på deres respektive posteringslag. 


Yderligere oplysninger finder du i afsnittet [Afledte bøger](derived-books.md) og [Bogfør med afledte bøger](post-derived-value-models.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]