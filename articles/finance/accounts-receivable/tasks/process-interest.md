---
title: Behandle rente
description: Denne procedure viser, hvordan du kan oprette, udskrive og bogføre rentenotaer.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 093fbd23f9fcaf62db9988a98a94b8cebf582768
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441581"
---
# <a name="process-interest"></a>Behandle rente

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du kan oprette, udskrive og bogføre rentenotaer. Denne opgave bruger demofirmaet USMF.


## <a name="set-up-interest-on-the-posting-profile"></a>Konfigurer rente i posteringsprofilen
1. Gå i **Navigationsrude** til **Moduler > Kredit > Opsætning > Debitorposteringsprofiler**.
2. Klik på **Rediger**.
3. Vælg en rentekode på rullelisten i feltet **Rentekode** i **oversigtspanelet Opsætning**. Hvis du ikke vil have beregnet rente for transaktioner med denne posteringsprofil, skal du undlade at udfylde feltet. Under fanen **Tabelbegrænsninger** kan du ændre den måde, som renter behandles på. Hvis dette felt er indstillet til Ja, beregnes der rente for denne posteringsprofil.  

## <a name="calculate-interest"></a>Beregn renter
1. Gå i **Navigationsrude** til **Moduler > Kredit > Rente > Opret rentenotaer**.
2. Du skal vælge de transaktionstyper, du vil beregne rente for. Alle åbne transaktioner for disse typer medtages i beregningen.  
3. Hvis du vælger "Ja" i **Rente**, skal du beregne renters rente. Du bør kontrollere lovgivning vedrørende beregning af renters rente, før du inkluderer disse transaktioner.  
4. Indtast en dato, som denne aftale skal beregnes fra, i feltet **Fra dato**. Hvis du ikke angiver en **Fra dato**, annulleres alle ikke-bogførte rentenotaer, og rente genberegnes fra transaktionsdatoen.
5. Indtast en dato, som denne aftale skal beregnes til, i feltet **Til dato**.
6. Vælg en indstilling i feltet **Anvend posteringsprofil fra**. Der er tre indstillinger for posteringsprofiler:
    - Konto – Brug den posteringsprofil, der er tildelt debitorens konto for hver rentenota. 
    - Vælg – Brug den posteringsprofil, som du vælger i feltet Posteringsprofil.
    - Transaktion – Brug den individuelle posteringsprofil fra transaktioner, som der beregnes rente på for hver rentenota. For transaktioner, som ikke har en tildelt posteringsprofil, anvendes den posteringsprofil, der er angivet i området Finans og moms i formen Debitorparametre.  
7. Udvid oversigtspanelet **Poster, der skal indgå**.
8. Klik på **Filtrér**.
9. Angiv et debitor-id i feltet **Kriterier**. Indtast for eksempel "US-001".
6. Klik på **OK**.
7. Klik på **OK**.

## <a name="print-interest-notes"></a>Udskrivning af rentenotaer
1. Gå i **Navigationsrude** til **Moduler > Kredit > Rente > Gennemse og behandl rentenotaer**.
2. Vælg "Oprettet" i feltet **Status**.
3. Vælg "Ikke udskrevet" i feltet **Udskrevet**.
4. Klik på **Udskriv**.
5. Udvid oversigtspanelet **Poster, der skal indgå**.
6. Klik på **OK**.
7. Luk siden.

## <a name="post-the-interest-note"></a>Bogfør rentenotaen
1. Vælg en rentenota, der er klar til at blive bogført (status er Oprettet).
2. Klik på **Bogfør**.
3. Angiv bogføringsdatoen for rentenotaen. Vælg Ja for at oprette en transaktion i finansmodulet for hver enkelt rentenota. Hvis du ikke vælger Ja, samles renten fra alle rentenotaer til debitoren, og den bogføres til finansmodulet i én transaktion.  
4. Udvid oversigtspanelet **Poster, der skal indgå**.
5. Klik på **OK**.
6. Vælg "Bogført" i feltet **Status**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]