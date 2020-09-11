---
title: Konfigurere sammenholdningsregler for bankafstemning
description: I dette emne beskrives det, hvor du konfigurerer sammenholdningsregler for afstemning og sammenholdningsregelsæt for afstemning for at lette bankafstemningsprocessen. Sammenholdningsregler for afstemning er et sæt af kriterier, der anvendes til at filtrere kontoudtogslinjer og bankdokumentlinjer under afstemningsprocessen.
author: panolte
manager: AnnBe
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2dcff7abfaf71c9e5e73ec2ffbdc1b377babdb2
ms.sourcegitcommit: 1daa297b0c09090a9c30c5f84bd7000e5b948a26
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/25/2020
ms.locfileid: "3720687"
---
# <a name="set-up-bank-reconciliation-matching-rules"></a>Konfigurere sammenholdningsregler for bankafstemning

[!include [banner](../includes/banner.md)]

I dette emne beskrives det, hvor du konfigurerer sammenholdningsregler for afstemning og sammenholdningsregelsæt for afstemning for at lette bankafstemningsprocessen. Sammenholdningsregler for afstemning er et sæt af kriterier, der anvendes til at filtrere kontoudtogslinjer og bankdokumentlinjer under afstemningsprocessen.

Du kan konfigurere sammenholdningsregler for afstemning og sammenholdningsregelsæt for afstemning for at lette bankafstemningsprocessen. En sammenholdningsregel for afstemning er et sæt af kriterier, der anvendes til at filtrere kontoudtogslinjer og Dynamics 365 Finance-banktransaktionslinjer under afstemningsprocessen. Brug siden **Sammenholdningsregler for afstemning** til at konfigurere sammenholdningsregler for afstemning. Du kan oprette mere end en sammenholdningsregel og derefter oprette et sammenholdningsregelsæt for afstemning på siden **Sammenholdningsregelsæt for afstemning**. 

> [!NOTE] 
> Sammenholdningsregler for bankafstemning bruges ved afstemning af et elektronisk bankkontoudtog vha. avanceret bankafstemning. 

På siden **Sammenholdningsregler for afstemning** kan du vælge, hvilke handlinger og udvælgelseskriterier der bruges, når sammenholdningsreglen køres. I feltgruppen **Handlinger** skal du vælge den handling, der skal udføres, når sammenholdningsreglen køres under afstemningsprocessen.  

Sammenholdningsregler vil som standard matche det første bankdokument, der opfylder kriterierne i sammenholdningsreglen. Hvis flere bankdokumenter opfylder regelkriterierne, kan parameteren, der kræver manuel sammenholdelse, aktiveres ved at gå til **Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre > Bankafstemning > Kræv manuel sammenholdelse, når avancerede sammenholdelsesregler for bankafstemning finder flere dokumenter, der svarer til beløbet**.

> [!NOTE] 
> Den indstilling, du vælger, bestemmer de felter, der vises.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Handling**                         |                                                                                                                                                                                                                                                                                                               | **Udvælgelseskriterier, der er tilgængelige, når handlingen er markeret**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Sammenhold med bankdokument**       | Opret kriterier for at angive, hvordan bankdokumenter og kontoudtogslinjer sammenholdes, når sammenholdningsreglen køres fra siden **Bankafstemningsarbejdsark**. Posteringslinjerne vælges efter de yderligere kriterier, der er angivet i oversigtspanelerne.                                | **Trin 1: Angiv sammenholdningsreglen** – Vælg kriterier for at angive, hvilke bankkontoudtog der skal sammenholdes med Finance-banktransaktioner. **Trin 2 (valgfrit): Vælg de opgørelseslinjer, som sammenholdningsregler skal køres mod:**  Anvend et filter for de opgørelseslinjer, som reglerne skal køres mod.                                                                                                                                                                                                                                                                                                               |
| **Ryd opgørelseslinjer til tilbageførsel** | Opret kriterier for at angive, hvordan opgørelseslinjer til tilbageførsel skal fjernes fra siden **Bankafstemningsarbejdsark**, når sammenholdningsreglen køres. Denne indstilling bruges, når en bankfejl medfører, at der er angivet to kontoudtogslinjer i det importerede kontoudtog, og linjerne skal afstemmes. | **Trin 1**: **Finde opgørelseslinjer til tilbageførsel** – Tilføj udvælgelseskriterier for at vælge tilbageførselslinjer for bankkontoudtog. Hvis du f.eks. kun vil vælge checks, skal du markere **Banktransaktionskode** i feltet Felt, vælge plustegnet (+) i feltet **Operatør** og derefter angive **Checks** i feltet Værdi. **Trin 2: Søg efter oprindelige opgørelseslinjer** – Du kan tilføje kriterier til sammenholdning af bankdokumentlinjer med kontoudtogslinjer. **Trin 3: Søg efter Finance-banktransaktioner** – Du kan tilføje kriterier til sammenholdning af Finance-banktransaktioner med bankkontoudtogslinjer. |
| **Markér nye transaktioner**          | Opret kriterier for at angive, hvordan nye transaktioner skal markeres på siden **Bankafstemningsarbejdsark**, når sammenholdningsreglen køres.                                                                                                                                                                 | **Trin 1: Søg efter opgørelseslinjer**– Tilføj markerede felter for at angive, hvilken kontoudtogslinjer der skal vælges fra siden **Bankafstemningsregneark**. **Trin 2: Søg efter Finance and Operations** – Du kan tilføje udvælgelseskriterier for at søge efter bankdokumentlinjer. Hvis der ikke findes noget bankdokument, markeres en opgørelseslinje som en ny postering.                                                                                                                                                                                                                                             |
