---
title: Fastlægge gebyrer for debitorbetaling
description: Opret betalingsgebyrer for debitorbetalinger.
author: ShivamPandey-msft
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7daf2f5b976dbc300458b5cb3efd0c0420c4f5c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822317"
---
# <a name="establish-customer-payment-fees"></a>Fastlægge gebyrer for debitorbetaling

[!include [banner](../../includes/banner.md)]

Opret betalingsgebyrer for debitorbetalinger.

Denne opgave bruger demofirmaet USMF.

1. I **navigationsruden** skal du gå til **Moduler > Debitor > Betalingsopsætning > Betalingsgebyr**.
2. Klik på **Ny**.
3. Angiv et gebyr-id i feltet **Gebyr-id**. Gebyr-id'et vises i betalingskladder, så gør det så beskrivende, at det fremgår, hvilket gebyr der vurderes.  
4. Skriv et gebyrnavn i feltet **Navn**.
5. Indtast en beskrivelse af gebyret i feltet **Gebyrbeskrivelse**.
6. Vælg, om gebyret opkræves af kunden eller en finanskonto, i feltet **Gebyr**. Hvis kunden har vurderer gebyret, skal du vælge Kunde. Hvis gebyret skal henføres til din organisation som en udgift, skal du vælge Finans. For denne opgave skal du vælge Debitor.  
7. Vælg den kladdetype, der kan bruge dette betalingsgebyr, i feltet **Kladdetype**. Hvis disse gebyrer bruges til debitorbetalinger, vil kladdetypen sandsynligvis være Debitorbetaling.  
8. Klik på **Gem**.
9. Klik på **Opsætning af betalingsgebyr**. Opsætningen Betalingsgebyr bruges til at definere kriterier for, hvornår betalingsgebyret vil blive vurderet.  Du kan for eksempel definere, at gebyret beregnes, hvis bankkontoen er USMF OPER, og betalingsmetoden er check.  
10. Vælg enten Tabel, Gruppe eller Alle i feltet **Grupperinger** for at definere, hvilke bankkonti der skal pålignes dette gebyr. Hvis du vælger Alle, kan alle bankkonti blive pålignet dette gebyr.  Hvis du vælger Tabel, kan kun den bankkonto, som du vælger, blive pålignet dette gebyr. Hvis du vælger Gruppe, kan kun bankkontiene i den valgte bankgruppe blive pålignet dette gebyr.  
11. Vælg enten en bankgruppe eller en bankkonto i feltet **Bankrelation**. Hvis du valgte Tabel, vil opslaget vise bankkonti. Hvis du valgte Gruppe, vil opslaget vise bankgrupper.  
12. Klik op linket i den valgte række på listen.
13. Vælg den betalingsmåde, som dette gebyr skal vurderes for, i feltet **Betalingsmåde**. Du kan for eksempel påligne kunderne et gebyr, hvis de betaler via check i stedet for at bruge elektronisk betaling.  
14. Find og vælg den ønskede post på listen.
15. Angiv en betalingsvaluta i feltet **Betalingsvaluta**, hvis det er relevant. Betalingsvalutaen bruges som et yderligere kriterium for, om gebyret vil blive vurderet.  Banken kan for eksempel opkræve et ekstra gebyr for betalinger i USD, da de normalt kun foretager transaktioner i EUR.  
16. Vælg, om gebyret skal være en procent, et beløb eller et interval.
17. Angiv enten gebyrets procent eller beløb i feltet **Procent/beløb**. Hvis feltet Procent/Beløb er Procent, angives værdien her som en procent. Hvis feltet Procent/Beløb er Beløb, vil den værdi, du angiver her, være et beløb. Hvis feltet Procent/Beløb er Interval, kan du bruge fanen Interval til at definere niveauerne.  
18. Vælg valutaen for gebyret i feltet **Valuta for gebyr**. Dette er den valuta, som gebyret vil blive oprettet i.  
19. Klik på **Gem**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]