---
title: "Bogføringskonti for kassation af anlægsaktiver"
description: "I denne artikel beskrives det, hvordan du konfigurerer finansbogføringskonti ved kassation af anlægsaktiver."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 111ff7ec677b699b8455b3a46a2866bd98970527
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="fixed-asset-disposal-posting-accounts"></a>Bogføringskonti for kassation af anlægsaktiver

[!include[banner](../includes/banner.md)]


I denne artikel beskrives det, hvordan du konfigurerer finansbogføringskonti ved kassation af anlægsaktiver.

På siden Posteringsprofiler for anlægsaktiver i oversigtspanelet Finanskonti skal du vælge Kassation - salg og Kassation - spild for at konfigurere bogføring til Finans.

I forbindelse med begge posteringstyper krediteres finanskontoen med anlægsaktivets kassationsværdi. Debet bogføres på en modkonto, som f.eks. kan være en bankkonto. Hvis et anlægsaktiv sælges til en kunde, bruges debitorkontoen i stedet for modkontoen.

Klik på Kassation, klik på Salg eller Spil, og opret derefter detaljerede konti for at tilbageføre anlægsaktivets bogførte nettoværdi. Du kan også angive oplysninger i felterne Efter-værdi og Salgsværdi på siden Kassationsparametre. 

Kassationsposteringen for et aktiv i en pulje for småaktiver reducerer kun den bogførte nettoværdi af puljen for småaktiver med det beløbet for kassationen. Hvis salget af aktivet overstiger den bogførte nettoværdi af puljen for småaktiver, nedskrives den bogførte nettoværdi til nul.






