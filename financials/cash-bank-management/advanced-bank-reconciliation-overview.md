---
title: Oversigt over avanceret bankafstemning
description: "I denne artikel beskrives forløbet for den avancerede bankafstemningsproces. Med funktionen Avanceret bankafstemning kan du importere bankkontoudtog, der kan afstemmes automatisk fra bankposteringerne."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 00f022da597b1de2454e93123de31731c6a65962
ms.openlocfilehash: 20363ef1917f7d0796cb0d5cd8e623c598b5ee01
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Oversigt over avanceret bankafstemning

I denne artikel beskrives forløbet for den avancerede bankafstemningsproces. Med funktionen Avanceret bankafstemning kan du importere bankkontoudtog, der kan afstemmes automatisk fra bankposteringerne.

Med funktionen til avanceret afstemning kan du importere bankkontoudtog. De importerede bankkontoudtog kan derefter afstemmes automatisk fra inden for bankposteringer. Her er trinene i arbejdsgangen til avanceret bankafstemning.

1.  Konfigurer import af et kontoudtog.
    -   Importer bankkontoudtog gennem dataenhedsstrukturen.
    -   Tre typiske bankkontoudtogsformater er indbygget: ISO20022, BAI2 og MT940.
    -   Funktionaliteten kan udvides til et vilkårligt format.

2.  Opret en nummerserie, der skal bruges til avanceret bankafstemning, og definer sammenholdningsregler for bankafstemning.
    -   En tilsvarende afstemningsregel er et sæt af kriterier, der bruges til at filtrere kontoudtogslinjer og Microsoft Dynamics 365 for operationer bank posteringslinjer under afstemningen. Du kan oprette mere end en tilsvarende regel til at automatisere og optimere dine afstemningen afhængigt af din forretningspraksis.

3.  Afstemme bankkontoudtog med Dynamics 365 for operationer bankposteringer.
    -   Udfør automatisk sammenholdning og oprettelse af kladder til afstemning.
    -   Får du vist bankkontoudtog og Dynamics 365 for operationer bankposteringer ved siden af hinanden.
    -   Automatisk bogføre Dynamics 365 for bankposteringer for operationer, hvis de vises på bankens kontoudtog, men vises ikke i Dynamics 365 for operationer.
    -   Generere en afstemningsopgørelse.




