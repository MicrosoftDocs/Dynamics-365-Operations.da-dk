---
title: Handlingsmeddelelser
description: En aktionsmeddelelse er et systemgenereret forslag om ændring af en eksisterende planlagt eller autoriseret ordre.
author: ChristianRytt
manager: tfehr
ms.date: 10/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6eb65f0cf97490177d38001e5ac793aa584f33bb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203957"
---
# <a name="action-messages"></a>Handlingsmeddelelser

[!include [banner](../includes/banner.md)]

En aktionsmeddelelse er et systemgenereret forslag om ændring af en eksisterende planlagt eller autoriseret ordre.

## <a name="introduction"></a>Introduktion

Handlingsmeddelelser genereres af beregningen af behovsplanlægning som reaktion på ændrede behov. For eksempel kan afsendelsesdato eller antal være ændret på en salgsordre, som du allerede har oprettet en indkøbsordre for at opfylde behovet for. I så fald genereres en eller flere handlingsmeddelelser ved beregning af behovsplanlægning for at opdatere indkøbsordren. Du bestemmer, om du vil foretage de ændringer, der foreslås.

Du kan konfigurere, hvordan handlingsmeddelelser skal beregnes for en disponeringsgruppe, som du knytter til en vare.

## <a name="select-action-messages"></a>Vælge handlingsmeddelelser

På siden **Disponeringsgrupper** kan du vælge de handlingsmeddelelser, som systemet skal generere, og de disponeringsgrupper eller varer, som meddelelserne skal gælde for. Du kan vælge følgende aktionsmeddelelser.

| Meddelelse             | Beskrivelse                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fremskynd**         | Hvis du vælger denne meddelelse, oprettes der handlingsmeddelelser, når det er nødvendigt, for at flytte ordrer til en tidligere dato. I feltet **Fremskynd margen** kan du også angive det maksimale antal dage mellem tilgang og afgang uden fremskyndelseshandling. |
| **Udskyd**        | Hvis du vælger denne meddelelse, oprettes der handlingsmeddelelser, når det er nødvendigt, for at flytte ordrer til en senere dato. I feltet **Udskyd margen** kan du angive det maksimale antal dage mellem tilgang og afgang uden udskydelseshandling.       |
| **Nedskriv**        | Hvis du vælger denne meddelelse, skal produktionsordrer, købsordrer og andre tilgangstransaktioner nedskrives for at undgå høje lagerniveauer.                                                                                                   |
| **Opskriv**        | Hvis du vælger denne meddelelse, skal produktionsordrer, købsordrer og andre tilgangstransaktioner opskrives for at undgå lave lagerniveauer.                                                                                                    |
| **Afledte aktioner** | Hvis du vælger denne meddelelse, oprettes handlingsmeddelelser for afledte behov for eksempel handlinger for komponentordrer, der opfylder produktionen.                                                                                                   |





