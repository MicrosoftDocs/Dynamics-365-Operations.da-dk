--- 
title: Oprette og anskaffe aktiver fra kreditorer
description: "Denne opgaveguide fører gennem oprettelse og anskaffelse af et anlægsaktiv med indkøbsprocessen."
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f814d20bc16bb3334ae4bc449cc0d45843487023
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Oprette og anskaffe aktiver fra kreditorer

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide fører gennem oprettelse og anskaffelse af et anlægsaktiv med indkøbsprocessen.  Den bruger bogholder- og kreditorassistenter og demofirmaet USMF.


## <a name="set-fixed-assets-parameters"></a>Konfigurere parametre for anlægsaktiver
1. Gå til Anlægsaktiver > Opsætning > Anlægsaktivparametre.
2. Udvis eller skjul sektionen Indkøbsordrer .
3. Markér afkrydsningsfeltet Tillad aktivanskaffelse fra Indkøb.
4. Markér afkrydsningsfeltet Opret aktiv under bogføring af produktkvittering eller faktura

## <a name="create-a-new-vendor-invoice"></a>Opret en ny kreditorfaktura
1. Gå til Kreditor > Arbejdsområder > Kreditorfakturapostering.
2. Klik på Ny kreditorfaktura.
3. Klik på rullelisten i feltet Fakturakonto for at åbne opslaget.
4. Klik op linket i den valgte række på listen.
5. Skriv en værdi i feltet Nummer.
6. Angiv en dato i feltet Bogføringsdato.
7. Klik på Tilføj linje.
8. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
    * Ikke-lagerførte varer eller indkøbskategorier kan bruges til anskaffelse af anlægsaktiver.  
9. Klik op linket i den valgte række på listen.
10. Angiv et tal i feltet Antal.
    * En fakturalinje opretter kun ét anlægsaktiv uanset antal.  Feltværdien Fakturaantal overføres til anlægsaktivantallet.  
11. Angiv et tal i feltet Enhedspris.
12. Udvis eller skjul sektionen Linedetaljer.
13. Klik på fanen Anlægsaktiver.
14. Markér afkrydsningsfeltet Opret et nyt anlægsaktiv.
15. Klik på rullelisten i feltet Anlægsaktivgruppe for at åbne opslaget.
16. Vælg på listen den anlægsaktivgruppe, der skal bruges ved oprettelse af det nye anlægsaktiv.
17. Klik op linket i den valgte række på listen.
18. Klik på Bogfør.
    * Anlægsaktivet oprettes og anskaffes, når fakturaen bogføres.  


