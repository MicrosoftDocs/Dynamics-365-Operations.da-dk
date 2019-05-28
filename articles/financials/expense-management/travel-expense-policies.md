---
title: Definer udgiftspolitikker
description: Du kan definere udgiftspolitikker, som medarbejderne skal følge, når de registrerer og sender rejserekvisitioner og udgiftsrapporter i Microsoft Dynamics 365 for Finance and Operations.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f0ff56f0ff106bc168b6a27612e08743a539a07
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1514433"
---
# <a name="expense-policies"></a>Udgiftspolitikker

[!include [banner](../includes/banner.md)]

Du kan definere politikker, som medarbejderne skal følge, når de registrerer og sender udgiftsrapporter og rejserekvisitioner.         
At implementere udgiftspolitikker kan gøre det lettere at administrere udgifter effektivt.         

Du kan f.eks. angive en politik for hoteludgifter i New York City, som angiver, at udgiften pr. nat ikke må overstige USD 250.       
Hvis en arbejder sender en udgiftsrapport eller en rejserekvisition, hvori værelsessatsen overskrider dette beløb, giver systemet arbejderen besked om,        
at udgiftsbeløbet i henhold til politikken er overskredet. Du kan konfigurere den meddelelse, som medarbejderen modtager, når du definerer        
politikken.      
        
Du kan definere tre typer politikker:         
        
- Advarsel – Gør det muligt for medarbejderen at sende en udgiftsrapport eller rejserekvisition, men udgiften markeres for alle godkendere og        
  til senere rapportering.        

- Fejl – kræver, at medarbejderen reviderer de udgifter, der i overensstemmelse med politikken, inden udgiftsrapporten eller rejserekvisitionen sendes.       
 
 - Justering – kræver, at medarbejderen eller en leder angiver en begrundelse for, hvorfor politikkens beløb er overskredet, inden udgiftsrapporten eller rejserekvisitionen sendes.        

# <a name="policy-tips"></a>Tip om politik
Her er nogle få forslag, der kan hjælpe dig med at oprette nye politikker for udgiftsstyring. 
* Politikker er datostyrede og træder ikke i kraft, hvis politikken oprettes med en dato efter den dato, hvor udgiften opstod. Hvis du f.eks. opretter en ny politik i dag for at gennemtvinge en maksimal måltidsudgift på $50, kontrolleres eventuelle eksisterende udgifter, der er angivet pr. i går, ikke med denne politik.
* Når du opretter en politik for en udgiftskategori, der kan specificeres, skal du overveje at tilføje en betingelse for udgiftslinjetypen. Visse politikker, som f.eks. kræver en kvittering, giver muligvis ikke mening for specificerede linjer og bør kun anvendes på hovedlinjen eller en ikke-specificeret linje. 

# <a name="when-to-evaluate-policies"></a>Hvornår politikker skal evalueres

I parametrene for udgiftsstyring er der mulighed for enten at evaluere politikker for udgiftsstyring, når en linje gemmes, eller når en udgiftsrapport sendes. Hvis du vælger at evaluere, når en linje gemmes, sikrer det brugerne en tidligere indsigt i, hvad de skal gøre for at fuldføre deres udgiftsrapporter på én gang. Ellers kan du forsinke evalueringen af en politik og spare tid, hvis du får foretaget valideringen ved afslutningen, under afsendelse til arbejdsgang.
