---
title: Bogføringskonti for kassation af anlægsaktiv
description: I dette emne beskrives det, hvordan du konfigurerer finansbogføringskonti ved kassation af anlægsaktiver.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: kfend
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8501bbb0fc47fb52e100d9086054db4831dae178
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/06/2022
ms.locfileid: "8720245"
---
# <a name="fixed-asset-disposal-posting-accounts"></a>Bogføringskonti for kassation af anlægsaktiv

[!include [banner](../includes/banner.md)]

I dette emne beskrives det, hvordan du konfigurerer finansbogføringskonti, når du kasserer anlægsaktiver.

Hvis du vil konfigurere finansbogføringskonti, der skal bruges, når du kasserer et aktiv, skal du vælge **Kassation - salg** og **Kassation - spild** i oversigtspanelet **Finanskonti** på siden **Posteringsprofiler for anlægsaktiver**.

I forbindelse med begge posteringstyper (kassation af et aktiv efter salg eller spild) krediteres finanskontoen med anlægsaktivets kassationsværdi. Debet bogføres på en modkonto, som f.eks. kan være en bankkonto (for eksempel). Hvis et anlægsaktiv sælges til en kunde, bruges debitorkontoen i stedet for modkontoen. Yderligere oplysninger finder du i [Afhænde et kasseret anlægsaktiv](dispose-of-a-fixed-asset-as-scrap.md).

Klik på **Kassation**, klik på **Salg** eller **Spild**, og konfigurer derefter detaljerede konti for at tilbageføre anlægsaktivets bogførte nettoværdi. Du kan også angive oplysninger i felterne **Bogført værdi** og **Salgsværditype** på siden **Kassationsparametre**. 

Kassationsposteringen for et aktiv i en pulje for småaktiver reducerer kun den bogførte nettoværdi af puljen for småaktiver med det beløbet for kassationen. Hvis salget af aktivet overstiger den bogførte nettoværdi af puljen for småaktiver, nedskrives den bogførte nettoværdi til nul.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
