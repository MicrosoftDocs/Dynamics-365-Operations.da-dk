--- 
title: "Indtaste fakturadata under kreditorer ved hjælp af en kreditorfaktura"
description: "Denne opgaveguide hjælper dig med at oprette en kreditorfaktura fra en indkøbsordre og få vist resultaterne af sammenholdelse af indkøbsordre, tilgang og faktura (trevejs-sammenholdelse)."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 48535a283cbdfdc7343a20105b139c527cac85f4
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-a-vendor-invoice"></a>Indtaste fakturadata under kreditorer ved hjælp af en kreditorfaktura

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide hjælper dig med at oprette en kreditorfaktura fra en indkøbsordre og få vist resultaterne af sammenholdelse af indkøbsordre, tilgang og faktura (trevejs-sammenholdelse).


## <a name="create-a-purchase-order"></a>Oprette en indkøbsordre
1. Gå til Kreditor > Indkøbsordrer > Alle indkøbsordrer.
2. Klik på Ny.
3. Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.
4. Find en kreditor, du vil vælge. Rul for eksempel ned til US-104.
5. Vælg kreditor US-104.
6. Klik på OK.
7. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
8. Vælg en lagervare. Du kan for eksempel vælge varenummer 1000.
9. Udvis eller skjul sektionen Linedetaljer.
10. Klik på fanen Opsætning.
    * Du kan tilsidesætte sammenholdelsespolitikken for at undlade at bruge sammenholdelse, tovejs-sammenholdelse eller trevejs-sammenholdelse .  
11. Udvis eller skjul sektionen Linedetaljer.
12. Klik på Køb i handlingsruden.
13. Klik på Bekræft.

## <a name="receive-the-products"></a>Modtage produkterne
1. Klik på Modtag i handlingsruden.
2. Klik på Produktkvittering.
3. Angiv nummeret på produktkvitteringen i feltet Produktkvittering. Angiv for eksempel PR123.
4. Klik på OK for at bogføre produktkvitteringen.
5. Luk siden.

## <a name="create-a-vendor-invoice"></a>Oprette en kreditorfaktura
1. Gå til Debitor > Indkøbsordrer > Indkøbsordrer, der er modtaget, men ikke faktureret.
2. Vælg den indkøbsordrelinje, du har oprettet.
3. Klik på Faktura i handlingsruden.
4. Klik på Faktura.
5. Angiv fakturanummeret i feltet Nummer.
6. Skriv en værdi i feltet Fakturabeskrivelse.
7. Indtast en dato i feltet Fakturadato.
8. Angiv 1200 i feltet Enhedspris.
9. Klik på Tilføj linje.
10. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
11. Find installationens gebyrvarenummer på listen. For eksempel S0001
12. Vælg installationens gebyrvarenummer.
    * Bemærk, at sammenholdelse ikke er blevet udført, siden du foretog ændringerne.  
13. Klik på Opdater status for sammenholdelse.
14. Klik på Gennemse i handlingsruden.
15. Klik på Detaljer om sammenholdelse.
    * Den nye linje med tjenester behøver ikke at blive sammenholdt, så status forbliver "Ikke udført".  
16. Vælg produktkvitteringen for den lagervare, du har modtaget.
    * Linjen med produktkvitteringen blev sammenholdt, men der er en uoverensstemmelse i antallet eller prisen, så den mislykkes.  
17. Angiv et tal i feltet Enhedspris.
    * Nu, da enhedsprisen passer, opdateres status til Fuldført. Hvis politikken tillader uoverensstemmelser, eller hvis sammenholdelse kun er en advarsel, kan du stadig bogføre fakturaen.  
18. Luk siden.
19. Klik på Bogfør.
20. Luk formularen.
    * Bemærk, at indkøbsordren ikke længere er angivet som modtaget, men ikke faktureret.  


