---
title: Oversigt over avanceret bankafstemning
description: I denne artikel beskrives forløbet for den avancerede bankafstemningsproces. Med funktionen Avanceret bankafstemning kan du importere bankkontoudtog, der kan afstemmes automatisk fra bankposteringerne.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c76b38e957c1c76a80c76782f45405573b7f191
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842601"
---
# <a name="advanced-bank-reconciliation-overview"></a>Oversigt over avanceret bankafstemning

[!include [banner](../includes/banner.md)]

I denne artikel beskrives forløbet for den avancerede bankafstemningsproces. Med funktionen Avanceret bankafstemning kan du importere bankkontoudtog, der kan afstemmes automatisk fra bankposteringerne.

Med funktionen til avanceret afstemning kan du importere bankkontoudtog. De importerede bankkontoudtog kan derefter afstemmes automatisk fra inden for bankposteringer. Her er trinene i arbejdsgangen til avanceret bankafstemning.

1.  Konfigurer import af et kontoudtog.
    -   Importer bankkontoudtog gennem dataenhedsstrukturen.
    -   Tre typiske bankkontoudtogsformater er indbygget: ISO20022, BAI2 og MT940.
    -   Funktionaliteten kan udvides til et vilkårligt format.

2.  Opret en nummerserie, der skal bruges til avanceret bankafstemning, og definer sammenholdningsregler for bankafstemning.
    -   En sammenholdningsregel for afstemning er et sæt af kriterier, der anvendes til at filtrere kontoudtogslinjer og Microsoft Dynamics 365 for Finance and Operations-banktransaktionslinjer under afstemningsprocessen. Du kan oprette mere end én sammenholdningsregel for at automatisere og optimere dine afstemningsprocesser, afhængigt af din forretningspraksis.

3.  Afstem bankkontoudtog med bankposteringer i Finance and Operations.
    -   Udfør automatisk sammenholdning og oprettelse af kladder til afstemning.
    -   Få vist bankkontoudtog og bankposteringer i Finance and Operations side om side.
    -   Bogføre automatisk Finance and Operations-banktransaktioner, hvis de vises på bankens kontoudtog, men ikke i Finance and Operations.
    -   Generere en afstemningsopgørelse.





