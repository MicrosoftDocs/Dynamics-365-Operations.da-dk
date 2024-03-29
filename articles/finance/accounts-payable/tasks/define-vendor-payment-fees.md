---
title: Definere kreditorbetalingsgebyrer
description: Konfigurer kreditorbetalingsgebyrer.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c490bb4d15fa03742b12f337046f26976ab70d29
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109814"
---
# <a name="define-vendor-payment-fees"></a>Definere kreditorbetalingsgebyrer

[!include [banner](../../includes/banner.md)]

Konfigurer kreditorbetalingsgebyrer. Denne opgave bruger demofirmaet USMF.

1. Gå til **Kreditor > Betalingsopsætning > Betalingsgebyr**.
2. Klik på **Ny**.
3. Indtast en værdi i feltet **Gebyr-id**.
    * **Gebyr-id** skal beskrive, hvor dette gebyr skal bruges, f.eks. "EFT_Fee".  
4. Skriv en værdi i feltet **Navn**.
5. Indtast en værdi i feltet **Gebyrbeskrivelse**.
    * Tilføj en beskrivelse for at give flere detaljer om, hvornår gebyret pålignes.  
6. Vælg enten **Kreditor** eller **Finans** i feltet **Gebyr**.
    * **Finans** bruges, når gebyret skal være udgiftsført til organisationen. **Kreditor** bruges, når gebyret vil blive pålignet kreditoren.  
7. Angiv en hovedkonto for, hvor gebyret være udgiftsført.
    * Denne indstilling kan kun vælges, når **Finans** vælges i indstillingen **Gebyr**.  
8. Vælg den kladde, som dette gebyr kan bruges i. 
    * For et betalingsgebyr for en kreditor skal du vælge kladden "Kreditorbetaling".  
9. Klik på **Gem**.
10. Klik på **Opsætning af betalingsgebyr**.
    * Fortsæt til **Opsætning af betalingsgebyr** for at definere, hvornår gebyret skal bruges som standard i den kladde, du har valgt.  
11. Vælg enten **Tabel**, **Gruppe** eller **Alle**.
    * **Tabel** bruges til at vælge en enkelt bankkonto, **Gruppe** bruges til at vælge en bankgruppe, og **Alle** er til brug af denne gebyropsætning for alle bankkonti.  
12. Vælg enten en bankgruppe eller en bankkonto.
    * Opslaget viser bankgruppe, hvis du har valgt **Gruppe** og vil vise bankkonti, hvis du har valgt **Tabel**.  
13. Vælg betalingsmåden, som dette gebyr pålignes for.
14. Vælg **Betalingsspecifikation** for den valgte betalingsmetode.
    * **Betalingsspecifikation** bruges med elektronisk pengeoverførsel som betalingsmåde.  
15. Vælg, om gebyret er en procent, et beløb eller et interval.
16. Angiv procentdelen eller beløbet af gebyret.
    * Hvis **Gebyr** er en procent, kan du indtaste procentdelen. Hvis **Gebyr** er et beløb, kan du angive beløbet for gebyret. Hvis **Gebyr** er et interval, skal du bruge fanen **Interval** til definerede niveauinddelte gebyrer.  
17. I feltet **Valuta for gebyr** skal du vælge den valuta, som gebyret pålignes i.
    * Denne valuta er til gebyret. Betalingsvalutaen bruges til at definere, hvornår gebyrreglen bør pålignes vurderet ud fra betalingens valuta. Din bank kan for eksempel opkræve et gebyr, når der foretages en betaling i EUR, men alle andre betalinger pålignes ikke et gebyr.  
18. Klik på **Gem**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
