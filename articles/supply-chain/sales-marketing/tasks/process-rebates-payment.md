---
title: Behandle rabatter for betaling
description: Denne fremgangsmåde viser, hvordan godkendte og behandlede kunderabatter konverteres til kreditnotaer.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 981068d26d232b10efd8d7288daaf7358aee3728
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424753"
---
# <a name="process-rebates-for-payment"></a>Behandle rabatter for betaling

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan godkendte og behandlede kunderabatter konverteres til kreditnotaer. Du kan bruge denne guide i USMF-demofirmaet. Forudsætningen for denne guide er at have en eller flere rabatkrav med status "Markér". Hvis du bruger USMF, skal du køre guiden "Generer og behandl kunderabatter", før du starter guiden.


## <a name="convert-rebate-claims-to-credit-note"></a>Konverter rabatkrav til kreditnota
1. Gå til Alle kunder.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
4. Klik på Indsaml i handlingsruden.
5. Klik på Udlign transaktioner.
6. Klik på Funktioner.
7. Klik på Rabatprogram.
    * Siden Rabatter angiver de rabatkrav, du har behandlet i kunderabatpanelet, og som er i status Markér.    
8. Klik på Rediger.
    * Sæt hak i feltet Markér for krav, der skal indgå i kreditnotaen.   
9. Klik på Funktioner.
10. Klik på Opret kreditnota.
    * Der vises en meddelelse for at informere dig om, at der er bogført en kladde (dette er debitorforbrugskladden, som er angivet på siden Debitorparametre). Dette medfører, at det reelle skyldige beløb (kredit) skal flyttes til debitorsaldoen. Det betyder, at kundens konto er blevet krediteret, og periodiseringskontoen for rabatten er krediteret.  
11. Luk siden.
12. Klik på Annuller.
    * Dette opdaterer siden, så du kan se opdateringerne.  
13. Klik på Indsaml i handlingsruden.
14. Klik på Udlign transaktioner.
    * Bemærk, at en transaktion for negative beløb, der repræsenterer det samlede rabatbeløb uden fakturareference, er blevet tilføjet debitorbalancen.   
15. Klik på Annuller.

