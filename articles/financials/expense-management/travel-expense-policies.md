---
title: Definer udgiftspolitikker
description: "Du kan definere udgiftspolitikker, som medarbejderne skal følge, når de registrerer og sender udgiftsrapporter og rejserekvisitioner i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9a5ce1a3b6519b510c9f5aa5618ab91f77a2d91a
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="expense-policies"></a>Udgiftspolitikker

[!include[banner](../includes/banner.md)]

Du kan definere politikker, som medarbejderne skal følge, når de registrerer og sender udgiftsrapporter og rejserekvisitioner. At implementere udgiftspolitikker kan gøre det lettere at administrere udgifter effektivt. 

Du kan f.eks. angive en politik for hoteludgifter i New York City, som angiver, at udgiften pr. nat ikke må overstige USD 250. Hvis en arbejder sender en udgiftsrapport eller en rejserekvisition, hvori værelsessatsen overskrider dette beløb, giver systemet arbejderen besked om, at politikbeløbet for udgiften er overskredet. Du kan konfigurere den meddelelse, som medarbejderen modtager, når du definerer politikken. 

Du kan definere tre typer politikker: 

 - Advarsel – Gør det muligt for medarbejderen at sende en udgiftsrapport eller rejserekvisition, men udgiften markeres for alle godkendere og  
 til senere rapportering. 
 - Fejl – kræver, at medarbejderen reviderer de udgifter, der i overensstemmelse med politikken, inden udgiftsrapporten eller rejserekvisitionen sendes. 
 - Justering – kræver, at medarbejderen eller en leder angiver en begrundelse for, hvorfor politikkens beløb er overskredet, inden udgiftsrapporten eller rejserekvisitionen sendes. 

Du kan også angive et datointerval, hvor udgiftspolitikkerne er gældende. For eksempel kan luftfartsselskabets billetpriser for flyvninger mellem Danmark og New York City være dyre i højsæsonen. Du kan definere en regel for flyudgifter, der begrænser omkostningerne ved flyvninger til New York City til en grænse på DKK 5000, og du kan angive, at denne regel er gældende mellem 15. marts og 15. september. 

