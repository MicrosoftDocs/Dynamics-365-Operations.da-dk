---
title: Bogføringskonti for kassation af anlægsaktiv
description: I dette emne beskrives det, hvordan du konfigurerer finansbogføringskonti ved kassation af anlægsaktiver.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9a46125dbe5262ba388e3958ea452975a98243f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187147"
---
# <a name="fixed-asset-disposal-posting-accounts"></a>Bogføringskonti for kassation af anlægsaktiv

[!include [banner](../includes/banner.md)]

I dette emne beskrives det, hvordan du konfigurerer finansbogføringskonti ved kassation af anlægsaktiver.

På siden Posteringsprofiler for anlægsaktiver i oversigtspanelet Finanskonti skal du vælge Kassation - salg og Kassation - spild for at konfigurere bogføring til Finans.

I forbindelse med begge posteringstyper krediteres finanskontoen med anlægsaktivets kassationsværdi. Debet bogføres på en modkonto, som f.eks. kan være en bankkonto. Hvis et anlægsaktiv sælges til en kunde, bruges debitorkontoen i stedet for modkontoen.

Klik på Kassation, klik på Salg eller Spil, og opret derefter detaljerede konti for at tilbageføre anlægsaktivets bogførte nettoværdi. Du kan også angive oplysninger i felterne Efter-værdi og Salgsværdi på siden Kassationsparametre. 

Kassationsposteringen for et aktiv i en pulje for småaktiver reducerer kun den bogførte nettoværdi af puljen for småaktiver med det beløbet for kassationen. Hvis salget af aktivet overstiger den bogførte nettoværdi af puljen for småaktiver, nedskrives den bogførte nettoværdi til nul.




