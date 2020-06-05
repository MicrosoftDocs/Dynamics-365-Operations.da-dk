---
title: Definer udgiftspolitikker
description: Du kan definere udgiftspolitikker, som medarbejderne skal følge, når de registrerer og sender rejserekvisitioner og udgiftsrapporter i Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22504e0e26c025d117f29dee3b59b41d508e7724
ms.sourcegitcommit: 4f90b9ddedf312e75a714e0ec7f7ee5fd43cac6a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/21/2020
ms.locfileid: "3389709"
---
# <a name="define-expense-policies"></a>Definer udgiftspolitikker

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

## <a name="policy-tips"></a>Tip om politik
Her er nogle få forslag, der kan hjælpe dig, når du opretter nye politikker for udgiftsstyring. 
* Politikker er datostyrede og træder ikke i kraft, hvis politikken oprettes med en dato efter den dato, hvor udgiften opstod. Hvis du f.eks. opretter en ny politik i dag for at gennemtvinge en maksimal måltidsudgift på $50, kontrolleres eventuelle eksisterende udgifter, der er angivet pr. i går, ikke med denne politik.
* Når du opretter en politik for en udgiftskategori, der kan specificeres, skal du overveje at tilføje en betingelse for udgiftslinjetypen. Visse politikker, som f.eks. kræver en kvittering, giver muligvis ikke mening for specificerede linjer og bør kun anvendes på hovedlinjen eller en ikke-specificeret linje. 
* Politikker for udgiftsstyring evalueres som standard i forhold til kildeenheden. I forbindelse med interne scenarier kan du angive den politik, der skal evalueres i forhold til destinationsenheden (låneenheden) i stedet. Hvis du vil køre politikkerne i forhold til destinationsenheden, skal du aktivere funktionen "Evaluere udgiftspolitik i forhold til juridisk enhed for udlån" i arbejdsområdet **Funktionsstyring**.

## <a name="when-to-evaluate-policies"></a>Hvornår politikker skal evalueres

I parametrene for udgiftsstyring er der mulighed for enten at evaluere politikker for udgiftsstyring, når en linje gemmes, eller når en udgiftsrapport sendes. Hvis du vælger at evaluere, når en linje gemmes, sikrer det brugerne en tidligere indsigt i, hvad de skal gøre for at fuldføre deres udgiftsrapporter på én gang. Ellers kan du forsinke evalueringen af en politik og spare tid, hvis du får foretaget valideringen ved afslutningen, under afsendelse til arbejdsgang.
