---
title: Gemme konfigurationer for detailopgørelser
description: Denne procedure viser konfigurationer for detailbutikken, der påvirker, hvordan detailopgørelser oprettes og bogføres.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbedcda59f503b103d5448e59038e4ed8ca0b51d
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916524"
---
# <a name="store-configurations-for-retail-statements"></a>Gemme konfigurationer for detailopgørelser

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne procedure viser konfigurationer for detailbutikken, der påvirker, hvordan detailopgørelser oprettes og bogføres. Økonomiske dimensioner i detailbutikker er omfattet af en anden procedure. Denne procedure bruger demofirmaet USRT.

1. I **navigationsruden** skal du gå til **Moduler > Detail og handel > Kanaler > Detailbutikker > Alle detailbutikker**.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
4. Klik på **Rediger**.
5. Indstillingerne i oversigtspanelet **Opgørelse/ultimo** påvirker oprettelse, validering og bogføring af opgørelsen for butikken. Udvid oversigtspanelet **Opgørelse/ultimo**.  
6. I feltet **Opgørelse/ultimo** skal du vælge den metode, du vil bruge til at gruppere linjerne i opgørelsen efter.  
7. Vælg "Ja" i **Én opgørelse pr. dag**, hvis der kun skal oprettes én opgørelse pr. dag, når der oprettes opgørelser fra batchjobbet til oprettelse af opgørelser.  
8. Feltet **Beregning af kasseoptælling** definerer, om kasseoptællinger skal lægges sammen, eller om den sidste skal bruges.  
9. I feltet **Afrunding** skal du vælge finanskontoen, som afrundingsdifferencer skal bogføres på.  
10. I feltet **Maksimal afrundingsdifference** skal du angive den afrundingsdifference, der maksimalt tillades.
11. I feltet **Bogføring** skal du angive den maksimale samlede bogføringsdifference, der er tilladt for en opgørelse.
12. I feltet **Skift** skal du angive den maksimale samlede difference i et skift i en opgørelse.  
13. I feltet **Transaktion** skal du angive den maksimale samlede difference på en linje i opgørelsen.  
14. I feltet **Lukkemetode** skal du definere, om transaktioner, der skal medtages i en opgørelse, skal være en del af et lukket skift, eller om de kan være alle transaktioner inden for det definerede interval for dato/klokkeslæt.  
15. I feltet **Afslutning på forretningsdag** skal du angive et tidspunkt, hvis transaktioner, der foregår efter midnat, skal bogføres med et tidspunkt den foregående dag.  
16. Vælg "Ja" i **Bogfør som arbejdsdag**, hvis transaktioner, der foregår efter midnat, skal bogføres som en del af den foregående dag.  
17. Vælg "Ja" i **Opdel efter opgørelsesmetode** for at få oprettet opgørelser for hver defineret opgørelsesmetoden. Dette kan være nyttigt, hvis bogføringens ydeevne skal forbedres for butikker med store transaktionsmængder, da den opretter mange mindre opgørelser, som kan behandles parallelt.  
18. I feltet **Standardkunde** i oversigtspanelet **Generelt** skal du vælge den debitorkonto, der skal bruges til salg til kunder, der kommer ind fra gaden.  

