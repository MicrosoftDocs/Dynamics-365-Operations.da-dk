---
title: Oversigt over avanceret bankafstemning
description: I denne artikel beskrives forløbet for den avancerede bankafstemningsproces. Med funktionen Avanceret bankafstemning kan du importere bankkontoudtog, der kan afstemmes automatisk fra bankposteringerne.
author: panolte
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: kfend
ms.custom:
- "22104"
- intro-internal
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6dadc5fd49a7103df8e1cacfd3be09c24a06e67
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711402"
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
    -   En sammenholdningsregel for afstemning er et sæt af kriterier, der anvendes til at filtrere kontoudtogslinjer og Microsoft Dynamics 365 Finance-banktransaktionslinjer under afstemningsprocessen. Du kan oprette mere end én sammenholdningsregel for at automatisere og optimere dine afstemningsprocesser, afhængigt af din forretningspraksis.

3.  Afstem bankkontoudtog med Finance-banktransaktioner.
    -   Udfør automatisk sammenholdning og oprettelse af kladder til afstemning.
    -   Få vist bankkontoudtog og Finance-banktransaktioner side om side.
    -   Bogføre automatisk Finance-banktransaktioner, hvis de vises på bankkontoudtog, men ikke i Finance-appen.
    -   Generere en afstemningsopgørelse.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
