---
title: Oversigt over avanceret bankafstemning
description: "I denne artikel beskrives forløbet for den avancerede bankafstemningsproces. Med funktionen Avanceret bankafstemning kan du importere bankkontoudtog, der kan afstemmes automatisk fra bankposteringerne."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e069bf65e7dcab7f3b049aa786f3daff07383f4c
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="advanced-bank-reconciliation-overview"></a>Oversigt over avanceret bankafstemning

[!include[banner](../includes/banner.md)]


I denne artikel beskrives forløbet for den avancerede bankafstemningsproces. Med funktionen Avanceret bankafstemning kan du importere bankkontoudtog, der kan afstemmes automatisk fra bankposteringerne.

Med funktionen til avanceret afstemning kan du importere bankkontoudtog. De importerede bankkontoudtog kan derefter afstemmes automatisk fra inden for bankposteringer. Her er trinene i arbejdsgangen til avanceret bankafstemning.

1.  Konfigurer import af et kontoudtog.
    -   Importer bankkontoudtog gennem dataenhedsstrukturen.
    -   Tre typiske bankkontoudtogsformater er indbygget: ISO20022, BAI2 og MT940.
    -   Funktionaliteten kan udvides til et vilkårligt format.

2.  Opret en nummerserie, der skal bruges til avanceret bankafstemning, og definer sammenholdningsregler for bankafstemning.
    -   En sammenholdningsregel for afstemning er et sæt af kriterier, der anvendes til at filtrere kontoudtogslinjer og Microsoft Dynamics 365 for Finance and Operations, Enterprise edition-banktransaktionslinjer under afstemningsprocessen. Du kan oprette mere end én sammenholdningsregel for at automatisere og optimere dine afstemningsprocesser, afhængigt af din forretningspraksis.

3.  Afstem bankkontoudtog med bankposteringer i Finance and Operations.
    -   Udfør automatisk sammenholdning og oprettelse af kladder til afstemning.
    -   Få vist bankkontoudtog og bankposteringer i Finance and Operations side om side.
    -   Bogføre automatisk Finance and Operations-banktransaktioner, hvis de vises på bankens kontoudtog, men ikke i Finance and Operations.
    -   Generere en afstemningsopgørelse.






