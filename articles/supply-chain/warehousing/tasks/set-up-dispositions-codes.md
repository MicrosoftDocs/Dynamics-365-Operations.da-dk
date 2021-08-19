---
title: Konfigurere dispositionskoder
description: Denne fremgangsmåde fokuserer på oprettelsen af en dispositionskode, der kan bruges på en mobil enhed for returordren modtager proces.
author: ShylaThompson
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0c7d4a6cc0b8850696f403e21e8dce5e0986c649f7a75d38be02fbee753f9e7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731739"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]