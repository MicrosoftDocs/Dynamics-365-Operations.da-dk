---
title: Konfigurere sammenholdningsregler for bankafstemning
description: Denne artikel beskriver, hvor du konfigurerer sammenholdningsregler for afstemning og sammenholdningsregelsæt for afstemning for at lette bankafstemningsprocessen. Sammenholdningsregler for afstemning er et sæt af kriterier, der anvendes til at filtrere kontoudtogslinjer og bankdokumentlinjer under afstemningsprocessen.
author: angelad116
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: kfend
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac5ab5e2bcb9a63bb52d5a74bd5e4b5db51ba603
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803931"
---
# <a name="set-up-bank-reconciliation-matching-rules"></a>Konfigurere sammenholdningsregler for bankafstemning

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvor du konfigurerer sammenholdningsregler for afstemning og sammenholdningsregelsæt for afstemning for at lette bankafstemningsprocessen. Sammenholdningsregler for afstemning er et sæt af kriterier, der anvendes til at filtrere kontoudtogslinjer og bankdokumentlinjer under afstemningsprocessen.

Du kan konfigurere sammenholdningsregler for afstemning og sammenholdningsregelsæt for afstemning for at lette bankafstemningsprocessen. En sammenholdningsregel for afstemning er et sæt af kriterier, der anvendes til at filtrere kontoudtogslinjer og Dynamics 365 Finance-banktransaktionslinjer under afstemningsprocessen. Brug siden **Sammenholdningsregler for afstemning** til at konfigurere sammenholdningsregler for afstemning. Du kan oprette mere end en sammenholdningsregel og derefter oprette et sammenholdningsregelsæt for afstemning på siden **Sammenholdningsregelsæt for afstemning**. 

> [!NOTE] 
> Sammenholdningsregler for bankafstemning bruges ved afstemning af et elektronisk bankkontoudtog vha. avanceret bankafstemning. 

På siden **Sammenholdningsregler for afstemning** kan du vælge, hvilke handlinger og udvælgelseskriterier der bruges, når sammenholdningsreglen køres. I feltgruppen **Handlinger** skal du vælge den handling, der skal udføres, når sammenholdningsreglen køres under afstemningsprocessen.  

Sammenholdningsregler vil som standard matche det første bankdokument, der opfylder kriterierne i sammenholdningsreglen. Hvis flere bankdokumenter opfylder regelkriterierne, kan parameteren, der kræver manuel sammenholdelse, aktiveres ved at gå til **Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre > Bankafstemning > Kræv manuel sammenholdelse, når avancerede sammenholdelsesregler for bankafstemning finder flere dokumenter, der svarer til beløbet**.

> [!NOTE] 
> Den indstilling, du vælger, bestemmer de felter, der vises.

| Handling | Betegnelse   | Udvælgelseskriterier, der er tilgængelige, når handlingen er markeret     |
|--------|---------------|----------------------------------------------------------|
| **Sammenhold med bankdokument**       | Opret kriterier for at angive, hvordan bankdokumenter og kontoudtogslinjer sammenholdes, når sammenholdningsreglen køres fra siden **Bankafstemningsarbejdsark**. Posteringslinjerne vælges efter de yderligere kriterier, der er angivet i oversigtspanelerne. | <ul><li>**Trin 1: Angiv sammenholdningsreglen** – Vælg kriterier for at angive, hvilke bankkontoudtog der skal sammenholdes med Finance-banktransaktioner.</li><li> **Trin 2 (valgfrit): Vælg de opgørelseslinjer, som sammenholdningsregler skal køres mod:**  Anvend et filter for de opgørelseslinjer, som reglerne skal køres mod.</li></ul>                                       |
| **Ryd opgørelseslinjer til tilbageførsel** | Opret kriterier for at angive, hvordan opgørelseslinjer til tilbageførsel skal fjernes fra siden **Bankafstemningsarbejdsark**, når sammenholdningsreglen køres. Denne indstilling bruges, når en bankfejl medfører, at der er angivet to kontoudtogslinjer i det importerede kontoudtog, og linjerne skal afstemmes. |<ul><li> **Trin 1**: **Finde opgørelseslinjer til tilbageførsel** – Tilføj udvælgelseskriterier for at vælge tilbageførselslinjer for bankkontoudtog. Hvis du f.eks. kun vil vælge checks, skal du markere **Banktransaktionskode** i feltet **Felt**, vælge plustegnet (+) i feltet **Operatør** og derefter angive **Checks** i feltet **Værdi**. </li><li>**Trin 2: Søg efter oprindelige opgørelseslinjer** – Du kan tilføje kriterier til sammenholdning af bankdokumentlinjer med kontoudtogslinjer. </li><li>**Trin 3: Søg efter Finance-banktransaktioner** – Du kan tilføje kriterier til sammenholdning af Finance-banktransaktioner med bankkontoudtogslinjer.</li></ul>  |
| **Markér nye transaktioner**          | Opret kriterier for at angive, hvordan nye transaktioner skal markeres på siden **Bankafstemningsarbejdsark**, når sammenholdningsreglen køres.                                                                                                                                                                 | <ul><li>**Trin 1: Søg efter opgørelseslinjer**– Tilføj markerede felter for at angive, hvilken kontoudtogslinjer der skal vælges fra siden **Bankafstemningsregneark**.</li><li> **Trin 2: Søg efter finans og drift** – Du kan tilføje udvælgelseskriterier for at søge efter bankdokumentlinjer. Hvis der ikke findes noget bankdokument, markeres en opgørelseslinje som en ny postering. </li></ul>         |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

