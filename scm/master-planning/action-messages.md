---
title: udokumenteret
description: "En aktionsmeddelelse er et systemgenereret forslag om ændring af en eksisterende planlagt eller autoriseret ordre."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 21 - 54
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f2ac69ddf485139b057dafa20e5f1a961fc32067
ms.lasthandoff: 03/29/2017


---

# <a name="undocumented"></a>udokumenteret

En aktionsmeddelelse er et systemgenereret forslag om ændring af en eksisterende planlagt eller autoriseret ordre.

### <a name="introduction"></a>Introduktion

Handlingsmeddelelser genereres af beregningen af behovsplanlægning som reaktion på ændrede behov. For eksempel kan afsendelsesdato eller antal være ændret på en salgsordre, som du allerede har oprettet en indkøbsordre for at opfylde behovet for. I så fald genereres en eller flere handlingsmeddelelser ved beregning af behovsplanlægning for at opdatere indkøbsordren. Du bestemmer, om du vil foretage de ændringer, der foreslås.

Du kan konfigurere, hvordan handlingsmeddelelser skal beregnes for en disponeringsgruppe, som du knytter til en vare.

 <a name="selecting-action-messages"></a>Vælge handlingsmeddelelser
==========================

På siden **Disponeringsgrupper** kan du vælge de handlingsmeddelelser, som systemet skal generere, og de disponeringsgrupper eller varer, som meddelelserne skal gælde for. Du kan vælge følgende aktionsmeddelelser.

| Meddelelse             | Beskrivelse                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fremskynd**         | Hvis du vælger denne meddelelse, oprettes der handlingsmeddelelser, når det er nødvendigt, for at flytte ordrer til en tidligere dato. I feltet **Fremskynd margen** kan du også angive det maksimale antal dage mellem tilgang og afgang uden fremskyndelseshandling. |
| **Udskyd**        | Hvis du vælger denne meddelelse, oprettes der handlingsmeddelelser, når det er nødvendigt, for at flytte ordrer til en senere dato. I feltet **Udskyd margen** kan du angive det maksimale antal dage mellem tilgang og afgang uden udskydelseshandling.       |
| **Nedskriv**        | Hvis du vælger denne meddelelse, skal produktionsordrer, købsordrer og andre tilgangstransaktioner nedskrives for at undgå høje lagerniveauer.                                                                                                   |
| **Opskriv**        | Hvis du vælger denne meddelelse, skal produktionsordrer, købsordrer og andre tilgangstransaktioner opskrives for at undgå lave lagerniveauer.                                                                                                    |
| **Afledte aktioner** | Hvis du vælger denne meddelelse, oprettes handlingsmeddelelser for afledte behov for eksempel handlinger for komponentordrer, der opfylder produktionen.                                                                                                   |




