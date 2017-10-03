--- 
title: "Oprette en indkøbsordre fra en salgsordre"
description: "Denne procedure viser, hvordan du kan oprette en indkøbsordre, der er baseret på en salgsordre."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5c569b6e58507e3b7707e4a56b22d2d60660f144
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-order-from-a-sales-order"></a>Oprette en indkøbsordre fra en salgsordre

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du kan oprette en indkøbsordre, der er baseret på en salgsordre. Produktmængderne på indkøbsordren angives derefter for at imødekomme efterspørgslen i den oprindelige salgsordre. Opfyldelse af salgsbehovet på denne måde er et alternativ til en mere omfattende og optimeret metode til planlægning af distributionskrav. Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.


## <a name="create-a-purchase-order-from-a-sales-order"></a>Oprette en indkøbsordre fra en salgsordre
1. Gå til Salg og marketing > Salgsordrer > Alle salgsordrer.
2. Klik på Ny.
3. Klik på rullelisten i feltet Kundekonto for at åbne opslaget.
4. Find og vælg den ønskede post på listen.
5. Klik på OK.
6. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
7. Find og vælg den ønskede post på listen.
    * Hvis du bruger USMF, kan du vælge D0001.  
8. Angiv et tal i feltet Antal.
9. Klik på Tilføj linje.
10. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
11. Find og vælg den ønskede post på listen.
    * Hvis du bruger USMF, kan du vælge T0020.  
12. Klik op linket i den valgte række på listen.
13. Angiv et tal i feltet Antal.
14. Klik på Gem.
15. Klik på Salgsordre i handlingsruden.
16. Klik på indkøbsordre.
    * Siden Opret indkøbsordre indeholder alle åbne salgsordrelinjer, som er kopieret fra salgsordren. Du kan gennemse ordredetaljerne, og hvis det er nødvendigt, kan du ændre de valgte oplysninger som f.eks. købsmængde og prisvilkår, før du opretter indkøbene.  
17. Vælg indstillingen Medtag alle.
    * Hvis du vil generere en indkøbsordre for kun et undersæt af salgsordrelinjerne, skal du vælge disse individuelt.  
    * Feltet Kreditorkonto er muligvis allerede udfyldt med et leverandørnummer. Hvis standardkreditoren er konfigureret for produktet (på den tilknyttede varedisponering), kopieres denne kreditor til linjen. Ellers skal du angive en kreditor manuelt.  I denne vejledning, uanset om feltet Kreditorkonto allerede indeholder en værdi, får du i følgende trin en vejledning i at vælge en ny kreditor, der er forskellig for hver linje.  
18. Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.
19. Find og vælg den ønskede post på listen.
20. Klik op linket i den valgte række på listen.
21. Vælg den anden ordrelinje.
22. Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.
23. Find og vælg den ønskede post på listen.
24. Klik op linket i den valgte række på listen.
25. Klik på Valider.
26. Klik på OK.
    * Meddelelsen fortæller dig, at der er oprettet en eller flere indkøbsordrer. Systemet genererer en separat indkøbsordre for hver kreditor, du har angivet for ordrelinjerne. Det betyder, at hvis flere salgsordrelinjer skal leveres af den samme leverandør, oprettes der en enkelt indkøbsordre med flere linjer.  

## <a name="review-purchase-orders-created-from-sales-orders"></a>Gennemse indkøbsordrer, der er oprettet ud fra salgsordrer
1. Klik på Generelt i handlingsruden.
2. Klik på Relaterede ordrer.
    * Siden Relaterede ordrer indeholder en liste over alle de ordrer, der er oprettet fra ordren. I dette eksempel er der oprettet to indkøbsordrer for hver af to forskellige leverandører.  
3. Klik for at følge linket i feltet Indkøbsordre.
    * Hver indkøbsordrelinje er tilknyttet den salgsordrelinje, der har resulteret i købet. Relationen til salgsordren er angivet under fanen Produkt i linjedetaljerne i oversigtspanelet, i referencetypen, referencenummeret og i referencepartifelterne.  
4. Udvis eller skjul sektionen Linedetaljer.
5. Klik på fanen Produkt.
    * Referencepartiet sikrer, at omkostningerne i forbindelse med det aktuelle indkøb debiteres den tilknyttede ordre.  
    * Du kan navigere til den oprindelige salgsordre ved at åbne linket i feltet Nummer på reference.  


