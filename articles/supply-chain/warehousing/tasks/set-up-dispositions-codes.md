---
title: Konfigurere dispositionskoder
description: Denne fremgangsmåde fokuserer på oprettelsen af en dispositionskode, der kan bruges på en mobil enhed for returordren modtager proces.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56117445df82a8f8a69287ed1cdfca04de7abf5b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216913"
---
# <a name="set-up-dispositions-codes"></a>Konfigurere dispositionskoder

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde fokuserer på oprettelsen af en dispositionskode, der kan bruges på en mobil enhed for returordren modtager proces. Dispositionskoder er en samling regler, der kan bruges, når der modtages varer. For eksempel når en arbejder bruger en mobilenhed til at modtage varer, der blev beskadiget, skal brugeren scanne en dispositionskode for beskadigede varer. Lagerstatus for varerne, der modtages, skabelonen arbejde og direktivet placering kan bestemmes ud fra den scannede dispositionskode. For den indkøbsordre, der er modtaget proces og rapporten produktion ordre som færdig proces, er brugen af en dispositionskode valgfrit. For salgsordren modtagende returvareprocessen, hvis varerne er registreret ved hjælp af en mobil enhed, er brug af dispositionskoden obligatorisk.  Denne vejledning blev oprettet ved hjælp af demodatafirmaet USMF. Denne procedure er beregnet til lagerchefen. 

1. Gå til Lagerstyring > Opsætning > Mobilenhed > Dispositionskoder.
2. Klik på Ny.
    * Opret en ny dispositionskode til brug til returneringer fra debitorer.  
3. Indtast en værdi i feltet Dispositionskode.
4. Vælg en lagerstatus i feltet Lagerstatus, hvis der er en lagerblokering.
    * Hvis du bruger USMF, skal du markere "Spærring". Du kan føje en lagerstatus til dispositionskoden for at tilsidesætte den standardstatus, der er på ordrelinjerne.  
5. Indtast en værdi i feltet Arbejdsskabelon.
    * Valgfrit: Vælg en skabelonkode, der er tilknyttet en returordre. Hvis ingen værdi er angivet, kan skabelonen arbejde vil blive løst ved hjælp af standardregler, der er konfigureret i systemet. At vælge en skabelon til arbejde vil begrænse denne dispositionskode kan bruges sammen med processerne. For eksempel, hvis en dispositionskode har en arbejde-skabelon med en arbejdsordre af typen indkøbsordre, kan den ikke bruges til at registrere varer, der returneres af kunder.  
6. Indtast en værdi i feltet Returdispositionskode.
    * Returdispositionskoden bestemmer resten af returordreprocessen for de varer, der er registreret. I dette eksempel bør debitoren modtage en kreditnota. Tilføj en returdispositionskode, der indeholder handlingen Kredit.  

