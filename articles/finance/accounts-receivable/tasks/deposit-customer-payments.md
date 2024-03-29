---
title: Deponere debitorbetalinger
description: Deponer debitorbetalinger.
author: ShivamPandey-msft
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ed692d9c82fd496e31258a70415db1838d99313
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714027"
---
# <a name="deposit-customer-payments"></a>Deponere debitorbetalinger

[!include [banner](../../includes/banner.md)]

Deponer debitorbetalinger. Denne opgave bruger demofirmaet USMF.

1. Gå til **Navigationsrude > Moduler > Debitor > Betalinger > Betalingskladde**.
2. Vælg **Ny**.
3. Vælg **CustPay** i rullemenuen i feltet **Navn**.
4. Vælg **Linjer**.
5. Vælg den kunde, du registrerer betalingen for, i feltet **Konto**.
6. Angiv betalingsbeløbet i feltet **Kredit**. Du kan vælge at undlade at udfylde beløbet og få systemet til at beregne det ved at vælge de fakturaer, der blev betalt.  
7. Indtast en værdi i feltet **Betalingsreference**. Betalingsreferencen kunne være checknummeret for den betaling, som du indtaster. Betalingsreferencen er påkrævet, hvis betalingen skal medtages på et indbetalingsbilag.  
8. Marker afkrydsningsfeltet Brug et indbetalingsbilag. Hvis betalingen skal medtages i indbetalingen, kan du ændre indstillingen til Ja.  
9. Vælg **Ny**.
10. Vælg kunden for den næste betaling i feltet **Konto**.
11. Angiv betalingsbeløbet i feltet **Kredit**.
12. Indtast en værdi i feltet **Betalingsreference**.
13. Markér afkrydsningsfeltet **Brug et indbetalingsbilag**.
14. Vælg **Bogfør**. Betalinger skal bogføres, før der kan oprettes et indbetalingsbilag. Dette er for at sikre, at betalingerne ikke ændres, når der genereres et indbetalingsbilag.  
15. Vælg **Funktioner**.
16. Vælg **Indbetalingsbilag**.
17. Vælg **OK**. Den første side bruges til at oprette et indbetalingsbilag.  
18. Vælg **OK**. Det andet trin er at udskrive indbetalingsbilaget, men dette trin er ikke påkrævet.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
