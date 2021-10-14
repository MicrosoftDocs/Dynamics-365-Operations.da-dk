---
title: Oprette en indkøbsordre fra en salgsordre
description: Denne procedure viser, hvordan du kan oprette en indkøbsordre, der er baseret på en salgsordre.
author: Henrikan
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ca91f17c13e210a4df6c22e0ed12370179bb866
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572466"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a>Oprette en indkøbsordre fra en salgsordre

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du kan oprette en indkøbsordre, der er baseret på en salgsordre. Produktmængderne på indkøbsordren angives derefter for at imødekomme efterspørgslen i den oprindelige salgsordre. Opfyldelse af salgsbehovet på denne måde er et alternativ til en mere omfattende og optimeret metode til planlægning af distributionskrav. Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.


## <a name="create-a-purchase-order-from-a-sales-order"></a>Oprette en indkøbsordre fra en salgsordre
1. Gå til **Navigationsrude > Moduler > Salg og marketing > Salgsordrer > Alle salgsordrer**.
2. Klik på **Ny**.
3. Klik på rullelisten i feltet **Kundekonto** for at åbne opslaget.
4. Find og vælg den ønskede post på listen.
5. Klik på **OK**.
6. Klik på rullelisten i feltet **Varenummer** for at åbne opslaget.
7. Find og vælg den ønskede post på listen. Hvis du bruger USMF, kan du vælge D0001.  
8. Angiv et tal i feltet **Antal**.
9. Klik på **Tilføj linje**.
10. Klik på rullelisten i feltet **Varenummer** for at åbne opslaget.
11. Find og vælg den ønskede post på listen. Hvis du bruger USMF, kan du vælge T0020.  
12. Klik op linket i den valgte række på listen.
13. Angiv et tal i feltet **Antal**.
14. Klik på **Gem**.
15. Klik på **Salgsordre** i **handlingsruden**.
16. Klik på **Indkøbsordre**. Siden **Opret indkøbsordre** indeholder alle åbne salgsordrelinjer, som er kopieret fra salgsordren. Du kan gennemse ordredetaljerne, og hvis det er nødvendigt, kan du ændre de valgte oplysninger som f.eks. købsmængde og prisvilkår, før du opretter indkøbene. 
17. Vælg indstillingen **Medtag alle**.
    - Hvis du vil generere en indkøbsordre for kun et undersæt af salgsordrelinjerne, skal du vælge disse individuelt.  
    - Feltet **Kreditorkonto** er muligvis allerede udfyldt med et leverandørnummer. Hvis standardkreditoren er konfigureret for produktet (på den tilknyttede varedisponering), kopieres denne kreditor til linjen. Ellers skal du angive en kreditor manuelt.  I denne vejledning, uanset om feltet **Kreditorkonto** allerede indeholder en værdi, får du i følgende trin en vejledning i at vælge en ny kreditor, der er forskellig for hver linje.  
18. I feltet **Kreditorkonto** skal du klikke på rullelisten for at åbne opslaget.
19. Find og vælg den ønskede post på listen.
20. Klik op linket i den valgte række på listen.
21. Vælg den anden ordrelinje.
22. I feltet **Kreditorkonto** skal du klikke på rullelisten for at åbne opslaget.
23. Find og vælg den ønskede post på listen.
24. Klik op linket i den valgte række på listen.
25. Klik på **Valider**.
26. Klik på **OK**. Meddelelsen fortæller dig, at der er oprettet en eller flere indkøbsordrer. Systemet genererer en separat indkøbsordre for hver kreditor, du har angivet for ordrelinjerne. Det betyder, at hvis flere salgsordrelinjer skal leveres af den samme leverandør, oprettes der en enkelt indkøbsordre med flere linjer.  

## <a name="review-purchase-orders-created-from-sales-orders"></a>Gennemse indkøbsordrer, der er oprettet ud fra salgsordrer
1. Klik på **Generelt** i **handlingsruden**.
2. Klik på **Relaterede ordrer**. Siden **Relaterede ordrer** indeholder en liste over alle de ordrer, der er oprettet fra salgsordren. I dette eksempel er der oprettet to indkøbsordrer for hver af to forskellige leverandører. 
3. Klik for at følge linket i feltet **Indkøbsordre**. Hver indkøbsordrelinje er tilknyttet den salgsordrelinje, der har resulteret i købet. Relationen til salgsordren er angivet under fanen **Produkt** i oversigtspanelet **Linjedetaljer**, i felterne **Referencetype**, **Referencenummer** og **Referenceparti**.  
4. Udvid eller skjul sektionen **Linjedetaljer**.
5. Klik på fanen **Produkt**.
    - **Referencepartiet** sikrer, at omkostningerne i forbindelse med det aktuelle indkøb debiteres den tilknyttede ordre.  
    - Du kan navigere til den oprindelige salgsordre ved at åbne linket i feltet **Nummer på reference**.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]