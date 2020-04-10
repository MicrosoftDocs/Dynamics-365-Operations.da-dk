---
title: Oprette en plan for et sted
description: Produktionsplanlæggeren beregner materiale- og kapacitetskravene for produktionen af en bestemt vare.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13238818de10596de34eaf9d8cd7d55562a307eb
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150303"
---
# <a name="create-a-plan-for-a-site"></a>Oprette en plan for et sted

[!include [banner](../../includes/banner.md)]

Produktionsplanlæggeren beregner materiale- og kapacitetskravene for produktionen af en bestemt vare. Når forsyningsforslagene er oprettet, finder han ordrer på den lokation, som han planlægger og autoriserer ordrerne for, begyndende med dem, der haster. De mest hastende ordrer er dem, der skal autoriseres på den aktuelle dato. Brug demodatafirmaet USMF til at udføre disse opgaver.


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a>Oprette en materiale- og kapacitetsplan for en vare
1. Klik på Varedisponering.
    * Skal du gå til standarddashboardet.  
2. Klik på Kør.
3. Udvid posterne for at inkludere sektion.
4. Klik på Filtrér.
5. Markér den valgte række på listen.
6. Skriv en værdi i feltet Kriterier.
    * Eksempel: D0001  
7. Klik på OK.
8. Klik på OK.
    * Det kan tage nogle minutter.  
9. Opdater siden.

## <a name="identify-the-urgent-planned-orders-for-the-item"></a>Identificere de planlagte ordrer på varen, som haster
1. Åbn kolonnefilteret Varenummer.
2. Anvend et filter til feltet "Varenummer" med værdien "D0001" ved hjælp af filteroperatøren "begynder med".
3. Åbn kolonnefilteret Bestillingsdato.
4. Du kan anvende et filter på feltet "Bestillingsdato" med en værdi for dags dato ved hjælp af filteroperatoren "er præcis".

## <a name="firm-all-the-urgent-orders-for-the-item"></a>Autorisere alle hasteordrer på varen
1. Markér eller fjern markeringen af alle rækker på listen.
2. Klik på Autoriser.
3. Klik på OK.

