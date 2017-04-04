---
title: Oprette sammenholdningsregler for bankafstemning
description: "I denne artikel beskrives det, hvor du konfigurerer sammenholdningsregler for afstemning og sammenholdningsregelsæt for afstemning for at lette bankafstemningsprocessen. Sammenholdningsregler for afstemning er et sæt af kriterier, der anvendes til at filtrere kontoudtogslinjer og bankdokumentlinjer under afstemningsprocessen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: e4c07a6afb90535c57f372d5b850919b5b34aaa4
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bank-reconciliation-matching-rules"></a>Oprette sammenholdningsregler for bankafstemning

I denne artikel beskrives det, hvor du konfigurerer sammenholdningsregler for afstemning og sammenholdningsregelsæt for afstemning for at lette bankafstemningsprocessen. Sammenholdningsregler for afstemning er et sæt af kriterier, der anvendes til at filtrere kontoudtogslinjer og bankdokumentlinjer under afstemningsprocessen.

Du kan konfigurere sammenholdningsregler for afstemning og sammenholdningsregelsæt for afstemning for at lette bankafstemningsprocessen. En tilsvarende afstemningsregel er et sæt af kriterier, der bruges til at filtrere kontoudtogslinjer og Microsoft Dynamics 365 for operationer bank posteringslinjer under afstemningen. Brug siden **Sammenholdningsregler for afstemning** til at konfigurere sammenholdningsregler for afstemning. Du kan oprette mere end en sammenholdningsregel og derefter oprette et sammenholdningsregelsæt for afstemning på siden **Sammenholdningsregelsæt for afstemning**. 

> [!NOTE] 
> Sammenholdningsregler bruges, hvis du skal afstemme et bankkontoudtog med elektronisk ved hjælp af avanceret bankafstemning. 

På siden **Sammenholdningsregler for afstemning** kan du vælge, hvilke handlinger og udvælgelseskriterier der bruges, når sammenholdningsreglen køres. I den **handlinger**, skal du vælge den handling, der skal udføres, når sammenholdningsreglen køres under afstemningen.  

> [!NOTE] 
> Den indstilling, du vælger, bestemmer de felter, der vises.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Handling**                         |                                                                                                                                                                                                                                                                                                               | **Udvælgelseskriterier, der er tilgængelige, når handlingen er markeret**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Sammenhold med bankdokument **       | Opret kriterier for at angive, hvordan bankdokumenter og kontoudtogslinjer sammenholdes, når sammenholdningsreglen køres fra siden **Bankafstemningsarbejdsark**. Posteringslinjerne vælges efter de yderligere kriterier, der er angivet i oversigtspanelerne.                                | **Trin 1: Angiv den tilsvarende regel** – Vælg criterias for at angive, hvilke kontoudtog fra banken, skal sammenholdes med Dynamics 365 for operationer bankposteringer. **Trin 2 (valgfrit): Vælg de opgørelseslinjer, som sammenholdningsregler skal køres mod:**  Anvend et filter for de opgørelseslinjer, som reglerne skal køres mod.                                                                                                                                                                                                                                                                                                               |
| **Ryd opgørelseslinjer til tilbageførsel ** | Opret kriterier for at angive, hvordan opgørelseslinjer til tilbageførsel skal fjernes fra siden **Bankafstemningsarbejdsark**, når sammenholdningsreglen køres. Denne indstilling bruges, når en bankfejl medfører, at der er angivet to kontoudtogslinjer i det importerede kontoudtog, og linjerne skal afstemmes. | **Trin 1**:** Finde opgørelseslinjer til tilbageførsel **– Tilføj udvælgelseskriterier for at vælge tilbageførselslinjer for bankens kontoudtog. Hvis du f.eks. kun vil vælge checks, skal du markere**Banktransaktionskode** i feltet Felt, vælge plustegnet (+) i feltet **Operatør** og derefter angive **Checks** i feltet Værdi. **Trin 2: Søg efter oprindelige opgørelseslinjer** – Du kan tilføje kriterier til sammenholdning af bankdokumentlinjer med kontoudtogslinjer. ** Trin 3: Find Dynamics 365 til transaktioner på bankens operationer ** – du kan føje kriterier til at sammenholde Dynamics 365 operationer bankposteringer med kontoudtogslinjer. |
| **Mark new transactions**          | Opret kriterier for at angive, hvordan nye transaktioner skal markeres på siden **Bankafstemningsarbejdsark**, når sammenholdningsreglen køres.                                                                                                                                                                 | **Trin 1: Søg efter opgørelseslinjer **– Tilføj markerede felter for at angive, hvilken kontoudtogslinjer der skal vælges fra siden **Bankafstemningsregneark**. ** Trin 2: Finde Dynamics 365 for operationer bankposteringer ** – du kan tilføje kriterier for at søge bankdokumentlinjer. Hvis der ikke findes noget bankdokument, markeres en opgørelseslinje som en ny postering.                                                                                                                                                                                                                                             |

 





