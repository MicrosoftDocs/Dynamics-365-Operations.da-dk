--- 
title: Registrere en kreditorfaktura i fakturakladden
description: "Denne opgaveguide viser, hvordan du kan registrere kreditorfakturaer, der ikke er knyttet til indkøbsordrer."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 127875443da1d43783440083b11afd423f2a12fe
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Registrere en kreditorfaktura i fakturakladden

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide viser, hvordan du kan registrere kreditorfakturaer, der ikke er knyttet til indkøbsordrer. Eksempler på denne type faktura omfatter udgifter til vareleverancer og tjenesteydelser.  Denne registrering anvender demofirmaet USMF.

1. Gå til Kreditor > Arbejdsområder > Kreditorfakturapostering.
2. Klik på Ny fakturakladde.
3. Klik på Ny.
4. Indtast kladdenavnet eller klik på rullelisten i feltet Navn for at åbne opslaget.
5. Skriv en værdi i feltet Beskrivelse.
6. Klik på Linjer.
    * Indtast den bogføringsdato, der opdaterer Finans, i feltet Dato.  
7. Angiv kreditorkontoen i feltet Konto.
8. Angiv fakturanummeret i feltet Faktura.
9. Indtast en værdi i feltet Beskrivelse.
10. Angiv et tal i feltet Kredit.
11. Indtast kontonummeret, eller klik på rullelisten i feltet Modkonto for at åbne opslaget.
    * Momsgruppen hentes som standard fra kreditorkontoen.  
    * Varemomsgruppen hentes som standard fra den hovedkonto, der er angivet i feltet Modkonto.  
    * Forfaldsdatoen beregnes på basis af betalingsbetingelserne.  
    * Kasserabatten hentes som standard fra kreditorkontoen.  
12. Klik på Bogfør.
13. Luk siden.


