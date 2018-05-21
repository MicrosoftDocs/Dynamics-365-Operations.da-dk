--- 
title: " Gemme konfigurationer for detailopgørelser"
description: "Denne procedure viser konfigurationer for detailbutikken, der påvirker, hvordan detailopgørelser oprettes og bogføres."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 441ba692f559f9966f3e2512c7760ad2f732b768
ms.contentlocale: da-dk
ms.lasthandoff: 02/07/2018

---
# <a name="store-configurations-for-retail-statements"></a> Gemme konfigurationer for detailopgørelser

[!include [task guide banner](../includes/task-guide-banner.md)]

Denne procedure viser konfigurationer for detailbutikken, der påvirker, hvordan detailopgørelser oprettes og bogføres. Økonomiske dimensioner i detailbutikker er omfattet af en anden procedure. Denne procedure bruger demofirmaet USRT.

1. Gå til Detail og handel > Kanaler > Detailbutikker > Alle detailbutikker.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
    * Indstillingerne i sektionen Opgørelse/ultimo påvirker oprettelse, validering og bogføring af opgørelsen for butikken.  Åbn sektionen Opgørelse/Ultimo.  
    * Vælg den metode, du vil bruge til at gruppere linjerne i opgørelsen efter.  
    * Vælg "Ja", hvis der kun skal oprettes én opgørelse pr. dag, når der oprettes opgørelser fra batchjobbet til oprettelse af opgørelser.  
    * Feltet Beregning af kasseoptælling definerer, om kasseoptællinger skal lægges sammen, eller om den sidste skal bruges.  
    * Vælg finanskontoen, som afrundingsdifferencer skal bogføres på.  
    * I feltet Maksimal afrundingsdifference kan du angive den afrundingsdifference, der maksimalt tillades.  
    * I feltet Bogføring kan du angive den maksimale samlede bogføringsdifference, der er tilladt for en opgørelse.  
    * I feltet Skift kan du angive den maksimale samlede difference i et skift i en opgørelse.  
    * I feltet Transaktion kan du angive den maksimale samlede difference på en linje i opgørelsen.  
    * I feltet Lukkemetode kan du definere, om transaktioner, der skal medtages i en opgørelse, skal være en del af et lukket skift, eller om de kan være alle transaktioner inden for det definerede interval for dato/klokkeslæt.  
    * I feltet Afslutning på forretningsdag kan du angive et tidspunkt, hvis transaktioner, der foregår efter midnat, skal bogføres med et tidspunkt den foregående dag.  
    * Vælg "Ja", hvis transaktioner, der foregår efter midnat, skal bogføres som en del af den foregående dag.  
    * Vælg "Ja" for at få oprettet opgørelser for hver defineret opgørelsesmetoden. Dette kan være nyttigt, hvis bogføringens ydeevne skal forbedres for butikker med store transaktionsmængder, da den opretter mange mindre opgørelser, som kan behandles parallelt.  
    * I feltet Standardkunde kan du vælge den debitorkonto, der skal bruges til salg til kunder, der kommer ind fra gaden.  


