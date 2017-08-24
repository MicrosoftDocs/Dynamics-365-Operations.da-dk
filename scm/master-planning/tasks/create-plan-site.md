--- 
title: Oprette en plan for et sted
description: "Produktionsplanlæggeren beregner materiale- og kapacitetskravene for produktionen af en bestemt vare."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d89d34d4d429faf87c70943961f7141a6258d482
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-plan-for-a-site"></a>Oprette en plan for et sted

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


