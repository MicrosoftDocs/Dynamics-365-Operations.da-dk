---
title: Definer udgiftspolitikker
description: Du kan definere udgiftspolitikker, som medarbejderne skal følge, når de registrerer og sender rejserekvisitioner og udgiftsrapporter i Microsoft Dynamics 365 for Finance and Operations.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04eaff110fea021ddee32be650be540894eb703b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "342425"
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
 
  Du kan også angive et datointerval, hvor udgiftspolitikkerne er gældende. For eksempel kan luftfartsselskabets billetpriser for flyvninger mellem Danmark      
  og New York City være høje i højsæsonen. Du kan definere en regel for udgifter til flyvning, der begrænser      
  omkostningerne ved flyvninger til New York til DKK 5000, og du kan angive, at denne regel er gældende mellem 15. marts og      
  15. september.
