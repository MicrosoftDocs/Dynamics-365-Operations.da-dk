---
title: Oprette en regel for fastmængde-kanban til produktion
description: Denne procedure fokuserer på den opsætning, der er nødvendig for at oprette en fast produktions-kanban-regel til udløsning af transformeringsaktiviteter i en arbejdscelle i et leanmiljø.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af912ecfb07a7af2f299e354243ba0d80c063a9e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981300"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a>Oprette en regel for fastmængde-kanban til produktion

[!include [banner](../../includes/banner.md)]

Denne procedure fokuserer på den opsætning, der er nødvendig for at oprette en fast produktions-kanban-regel til udløsning af transformeringsaktiviteter i en arbejdscelle i et leanmiljø. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder produktionen af et nyt eller ændret produkt.


## <a name="create-new-kanban-rule"></a>Opret en ny kanban-regel
1. Gå til kanban-regler.
2. Klik på Ny.
    * Bemærk, at standardtypen er Produktion, og Genopfyldningsstrategi er Fast. Du behøver ikke at ændre disse parametre.  
3. Angiv eller vælg en værdi i feltet Første planaktivitet.
    * Dette er den aktivitet, der udføres for kanbans, der er oprettet ud fra denne kanban-regel.  Vælg "SpeakerTestAndPackaging".  
4. Udvid afsnittet Detaljer.
5. Indtast eller vælg en værdi i feltet Produkt.
    * Vælg L0050.  
6. Indtast eller vælg en værdi i feltet Måleenhed.
    * Vælg minutter.  
7. Angiv et tal i feltet Leveringstid.
    * Angiv 5.  

## <a name="set-quantities"></a>Angiv antal
1. Udvid afsnittet Antal.
2. Angiv Standardmængde til "10".
    * Dette er det antal, der skal overføres for hver kanban.  
3. Marker feltet Afvigelse i produktantal.
    * Dermed kan valgte kanbans fuldføres med en afvigelse fra standardmængden.  Angiv begge afvigelser til 2 for at tillade, at kanbans fuldføres med et antal fra 8 til 12.  
4. Angiv Afvigelse nedenfor til "2".
    * Dette tillader fuldførelse ned til 10 - 2 = 8  
5. Angiv Afvigelse ovenfor til "2".
    * Dette tillader fuldførelse op til 10 + 2 = 12  
6. Skriv et tal i feltet Fast kanban-mængde.
    * Dette er antallet af kanbans, der skal være aktive. I dette tilfælde 5 kanbans, som behandler 10 hver.  
7. Angiv "2" i feltet Minimum for påmindelsesgrænse.
    * Bruges til at holde styr på det mindste antal fulde kanbans, der skal være på destinationen. Den bruges f.eks. på oversigten over kanban-mængde.  
8. Angiv "4" i feltet Maksimum for påmindelsesgrænse.
    * Bruges til at holde styr på det maksimale antal fulde kanbans, der må være på destinationen. Den bruges f.eks. på oversigten over kanban-mængde.  
9. Angiv "1" i feltet Automatisk planlægningsantal.
    * Hvis dette angives til 1 betyder det, at alle kanbans automatisk planlægges.   Hvis vi angav 3, ville kanbans ikke blive planlagt, før 3 tomme kanbans var klar til planlægning. Dette er nyttigt til at gruppere arbejde og undgå for meget opsætning.  

## <a name="create-kanbans"></a>Opret kanbans
1. Udvid afsnittet Kanbans.
2. Klik på Gem.
    * Kanban-reglen skal gemmes, før du kan oprette kanbans.  
3. Klik på Tilføj.
    * Bemærk, at der ikke er nogen aktive kanbans, og derfor er det foreslåede 'antal nye kanbans' 5. Dette er lig med 'Fast kanban-mængde'.  
4. Klik på Opret.
    * Dette opretter 5 kanbans.  
    * Bemærk, at der blev oprettet 5 kanbans for 10 hver for denne produktions-kanban-regel. Dette er det sidste trin i denne procedure.  

