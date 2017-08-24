--- 
title: "Oprettelse af udlånsemner"
description: "Udlånsemner er poster, der hjælper dig med at holde styr på fysiske emner, som f.eks. telefoner eller computere, som virksomheden udlåner til arbejdere."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 65655283c70c99b5d64289b319ecc69f6e414221
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-loan-items"></a>Oprettelse af udlånsemner

[!include[task guide banner](../../includes/task-guide-banner.md)]

Udlånsemner er poster, der hjælper dig med at holde styr på fysiske emner, som f.eks. telefoner eller computere, som virksomheden udlåner til arbejdere. Alle fysiske emner skal have et tilknyttet udlånsemne. Alle udlånsemneposter skal beskrive, hvad der udlånes, hvem der er ansvarlig for udlånet, og det antal dage, emnet kan udlånes. Du kan oprette flere udlånsemner f.eks. nøgler, adgangskort og uniformer, på samme tid. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="create-loan-types"></a>Opret udlånstyper
1. Gå til Personale > Arbejdere > Udlånsemner > Udlånstyper.
2. Klik på Ny.
3. Indtast en værdi i feltet Udlånstype.
4. Skriv en værdi i feltet Beskrivelse.
5. Angiv det antal dage, som emner, der er knyttet til denne udlånstype, kan være overskredet med. 
6. Klik på Gem.
7. Luk siden.
8. Opdater siden.

## <a name="create-loan-items"></a>Opret Udlånsemner
1. Gå til Personale > Arbejdere > Udlånsemner > Udlånsemner.
2. Klik på Opret udlånsemner.
3. I feltet Antal. skal du angive et tal.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på rullelisten i feltet Udlånstype for at åbne opslaget.
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.
8. Angiv antal dage, emnet kan lånes.
    * Standardværdien i feltet Planlagt retur på siden Lånt udstyr beregnes som den aktuelle dato plus dette tal.  
9. Klik på rullelisten i feltet Ansvarlig for at åbne opslaget.
10. Klik på Vælg.
11. Indtast et tal i feltet Startværdi, der skal tilføjes.
12. Angiv et tal i feltet Interval.
13. Skriv en værdi i feltet Format.
    * Hvis det højeste startnummer for et udlånt emne f.eks. er 10, skal du skrive to talsymboler i feltet Format.  
14. Klik på OK.
15. Opdater siden.


