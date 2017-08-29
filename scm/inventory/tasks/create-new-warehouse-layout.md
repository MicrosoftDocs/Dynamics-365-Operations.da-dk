--- 
title: Oprette en ny lageropbygning
description: "Denne procedure viser, hvordan du kan angiver oplysninger om placeringer på et lagersted."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 15610bc797cf7e7abdec433d0a5cead60da7a555
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-new-warehouse-layout"></a>Oprette en ny lageropbygning

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du kan angiver oplysninger om placeringer på et lagersted. Dette gælder for kun for lagersteder, der er oprettet ved hjælp af "grundlæggende lagerfunktioner" i modulet Lagerstyring, ikke for lagersteder, der er oprettet i modulet Lagerstedsstyring. Du kan bruge denne procedure på demofirmaet USMF eller dine egne data.


## <a name="set-the-default-location-capacity"></a>Angiv lokalitetens standardkapacitet
1. Gå til lagerstyring > Opsætning > Parametre til lager- og lagerstedsstyring.
2. Klik på fanen Lokaliteter.
3. Angiv et tal i feltet Standardbredde.
4. Angiv et tal i feltet Standarddybde.
5. Angiv et tal i feltet Standardhøjde.
6. Klik på Gem.
7. Luk siden.

## <a name="define-the-location-name-format"></a>Definer formatet for navnet på lokaliteten
1. Gå til Lagerstyring > Opsætning > Lageropdeling > Lagersteder.
2. Klik på Ny.
3. Skriv en værdi i feltet Lagersted.
4. Skriv en værdi i feltet Navn.
5. Klik på rullelisten i feltet Sted for at åbne opslaget.
6. Find og vælg den ønskede post på listen.
7. Slå udvidelsen af sektionen Lokationsnavne til/fra.
    * Indstillingerne i denne sektion definerer standardformatet for navne på lokaliteter. I vores eksempel medtager vi gangnummer, reolnummer og hyldenummer.  
8. Du kan angive indstillingen Medtag gang til Ja.
9. Du kan angive indstillingen Medtag reol til Ja. 
10. Angiv en værdi for reolen i feltet Format.
    * For eksempel: -##  
11. Du kan angive indstillingen Medtag hylde til Ja.
12. Angiv en værdi for hylden i feltet Format.
    * For eksempel: -##  

## <a name="define-warehouse-locations"></a>Definer lagerstedslokationer
1. Klik på Lagersted i handlingsruden.
2. Klik på Guiden Lokation.
3. Klik på Næste.
4. Fjern markeringen af indstillingen Forsendelsesområder
5. Fjern markeringen af indstillingen Bulkvarelokationer
6. Klik på Næste.
7. Klik på Næste.
8. Klik på Næste.
9. Klik på Næste.
10. Klik på Næste.
11. Klik på Næste.
12. Klik på Næste.
    * Bemærk, at de fysiske dimensioner, der vises på denne side, er dem, du har angivet i starten af denne procedure.  
13. Klik på Næste.
14. Klik på Finish.
15. Luk siden.
16. Opdater siden.


