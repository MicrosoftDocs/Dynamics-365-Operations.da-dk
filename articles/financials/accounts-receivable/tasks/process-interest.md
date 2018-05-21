--- 
title: Behandle rente
description: "Denne procedure viser, hvordan du kan oprette, udskrive og bogføre rentenotaer."
author: ShivamPandey-msft
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
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 543ac29ac1b1cbad52f1c155ac90b04d0c122a1f
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="process-interest"></a>Behandle rente

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du kan oprette, udskrive og bogføre rentenotaer. Denne opgave bruger demofirmaet USMF.


## <a name="set-up-interest-on-the-posting-profile"></a>Konfigurer rente i posteringsprofilen
1. Gå til Kredit og inkasso > Opsætning > Debitorposteringsprofiler.
2. Klik på Rediger.
    * Vælg en rentekode på rullelisten. Hvis du ikke vil have beregnet rente for transaktioner med denne posteringsprofil, skal du undlade at udfylde feltet.  
    * Under fanen Tabelbegrænsninger kan du ændre den måde, som rente behandles på. Hvis dette felt er indstillet til Ja, beregnes der rente for denne posteringsprofil.  

## <a name="calculate-interest"></a>Beregn renter
1. Gå til Kredit og inkasso > Rente > Opret rentenotaer.
    * Du skal vælge de transaktionstyper, du vil beregne rente for. Alle åbne transaktioner for disse typer medtages i beregningen.  
    * Hvis du vælger Rente, skal du beregne renten af renten. Du bør kontrollere lovgivning vedrørende beregning af renters rente, før du inkluderer disse transaktioner.  
    * Rente beregnes fra denne dato til "Til dato". Hvis du ikke angiver en "Fra dato", annulleres alle ikke-bogførte rentenotaer, og rente genberegnes fra transaktionsdatoen.  
2. Angiv datoen for rentenotaen.
    * Der findes tre posteringsprofilindstillinger: Konto – Brug den posteringsprofil, der er tildelt kundekontoen for hver rentenota.   Vælg – Brug den posteringsprofil, som du vælger i feltet Posteringsprofil.   Transaktion – Brug den individuelle posteringsprofil fra transaktioner, som der beregnes rente på for hver rentenota. For transaktioner, som ikke har en tildelt posteringsprofil, anvendes den posteringsprofil, der er angivet i området Finans og moms i formen Debitorparametre.  
    * Vælg en posteringsprofil her, hvis du har ændret "Anvend posteringsprofil fra" til Vælg.  
3. Udvis eller skjul sektionen Poster, der skal indgå.
4. Klik på Filtrér.
5. Angiv i feltet kriterier et kunde-ID. Indtast for eksempel "US-001".
6. Klik på OK.
7. Klik på OK.

## <a name="print-interest-notes"></a>Udskrivning af rentenotaer
1. Gå til Kredit og inkasso > Rente > Gennemse og behandl rentenotaer.
2. Vælg "Oprettet" i feltet Status.
3. Vælg "Ikke udskrevet" i feltet Udskrevet.
4. Klik på Udskriv.
5. Udvis eller skjul sektionen Poster, der skal indgå.
6. Klik på OK.
7. Luk siden.

## <a name="post-the-interest-note"></a>Bogfør rentenotaen
1. Vælg en rentenota, der er klar til at blive bogført (status er Oprettet).
2. Klik på Bogfør.
3. Angiv bogføringsdatoen for rentenotaen.
    * Vælg Ja for at oprette en transaktion i finansmodulet for hver enkelt rentenota.     Hvis du ikke vælger Ja, samles renten fra alle rentenotaer til debitoren, og den bogføres til finansmodulet i én transaktion.  
4. Udvis eller skjul sektionen Poster, der skal indgå.
5. Klik på OK.
6. Vælg "Bogført" i feltet Status.


