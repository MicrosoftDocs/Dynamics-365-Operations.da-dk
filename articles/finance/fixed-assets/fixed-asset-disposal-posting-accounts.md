---
title: Bogføringskonti for kassation af anlægsaktiv
description: I denne artikel beskrives det, hvordan du konfigurerer finansbogføringskonti ved kassation af anlægsaktiver.
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
ms.openlocfilehash: 1272cdb16396d24b5495f023e7b9fe3dee341507
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871327"
---
# <a name="fixed-asset-disposal-posting-accounts"></a>Bogføringskonti for kassation af anlægsaktiv

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du konfigurerer finansbogføringskonti, når du kasserer anlægsaktiver.

Hvis du vil konfigurere finansbogføringskonti, der skal bruges, når du kasserer et aktiv, skal du vælge **Kassation - salg** og **Kassation - spild** i oversigtspanelet **Finanskonti** på siden **Posteringsprofiler for anlægsaktiver**.

I forbindelse med begge posteringstyper (kassation af et aktiv efter salg eller spild) krediteres finanskontoen med anlægsaktivets kassationsværdi. Debet bogføres på en modkonto, som f.eks. kan være en bankkonto (for eksempel). Hvis et anlægsaktiv sælges til en kunde, bruges debitorkontoen i stedet for modkontoen. Yderligere oplysninger finder du i [Afhænde et kasseret anlægsaktiv](dispose-of-a-fixed-asset-as-scrap.md).

Klik på **Kassation**, klik på **Salg** eller **Spild**, og konfigurer derefter detaljerede konti for at tilbageføre anlægsaktivets bogførte nettoværdi. Du kan også angive oplysninger i felterne **Bogført værdi** og **Salgsværditype** på siden **Kassationsparametre**. 

Kassationsposteringen for et aktiv i en pulje for småaktiver reducerer kun den bogførte nettoværdi af puljen for småaktiver med det beløbet for kassationen. Hvis salget af aktivet overstiger den bogførte nettoværdi af puljen for småaktiver, nedskrives den bogførte nettoværdi til nul.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
