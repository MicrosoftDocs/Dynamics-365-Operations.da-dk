---
title: Forudbetalingsfakturaer vs. forudbetalinger
description: "Denne artikel beskriver de to metoder, som organisationer kan bruge til betaling af forskud (forudbetalinger) og stiller også kontrasterne op mellem dem. I den ene metode, kan du oprette en forudbetalingsfaktura, der er tilknyttet en indkøbsordre. I den anden metode kan du oprette kladdebilag for forudbetaling ved at oprette kladdeposteringer og markere dem som kladdebilag for forudbetaling."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 07199a9ca178df3dc3809fe4e498cf5f6928a321
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="prepayment-invoices-vs-prepayments"></a>Forudbetalingsfakturaer vs. forudbetalinger

[!include[banner](../includes/banner.md)]


Denne artikel beskriver de to metoder, som organisationer kan bruge til betaling af forskud (forudbetalinger) og stiller også kontrasterne op mellem dem. I den ene metode, kan du oprette en forudbetalingsfaktura, der er tilknyttet en indkøbsordre. I den anden metode kan du oprette kladdebilag for forudbetaling ved at oprette kladdeposteringer og markere dem som kladdebilag for forudbetaling.

Organisationer kan udstede forudbetalinger til kreditorer for varer eller tjenester, før varerne eller tjenesterne er opfyldt. To metoder kan bruges til at udstede forudbetalinger til kreditorer. Hvis du vil minimere risikoen, kan du spore forudbetalinger ved at definere forudbetalingen i en indkøbsordre. I forbindelse med denne metode skal du oprette en forudbetalingsfaktura, der er tilknyttet en indkøbsordre. Denne metode kaldes forudbetalingsfakturering. Organisationer, der ikke ønsker at spore forudbetalinger så tæt, eller som ikke modtager en forudbetalingsfaktura fra deres leverandør, kan bruge kladdebilag for forudbetaling i stedet for metoden til forudbetalingsfaktura. Du kan oprette kladdebilag for forudbetaling ved at oprette kladdeposteringer og markere dem som kladdebilag for forudbetaling. I forbindelse med denne metode kan du ikke spore, hvilke forudbetalinger der foretages til en kreditor i forhold til hvilke indkøbsordrer. Du kan dog markere en bogført forudbetaling som udlignet mod en indkøbsordre.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Hvornår skal jeg bruge forudbetalingsfakturering vs. forudbetalinger
| Forudbetalingsfakturering                                                                | Forudbetalinger                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Definer forudbetalingsværdi på en indkøbsordre.                                    | Der er ikke defineret en forudbetalingsværdi på en indkøbsordre.                    |
| Nøgle: En forudbetalingsfaktura og en endelig faktura skal bogføres.                       | Ingen forudbetalingsfaktura skal bogføres.                                    |
| Ansvar for forudbetalingen er på forudbetalingskontoen, ikke på kreditorkontoen. | Ansvar for forudbetalingen er på kreditorkontoen.                  |
| Kreditorsaldoen afspejler ikke forudbetalingsværdien under hele processen.     | Kreditorsaldoen afspejler forudbetalingsværdien under hele processen. |
| Forudbetalingsfakturering er kun tilgængelig i Kreditor.                         | Forudbetalinger er også tilgængelige i Debitor og Kreditor.    |

## <a name="overview-of-the-prepayment-process"></a>Oversigt over forudbetalingsprocessen
I mange lande/områder er det regnskabspraksis, at forudbetalinger fra en debitor eller til en kreditor ikke bogføres på de sædvanlige samlekonti for den pågældende debitor eller kreditor. Disse forudbetalinger bogføres i stedet på særlige finanskonti til forudbetalinger. Når der oprettes en salgsordre eller indkøbsordre, udstedes en faktura til debitoren eller fra kreditoren. Når fakturaen betales, tilbageføres kladdebilaget for forudbetaling og bilaget for forudbetalt moms på finanskontiene for forudbetalinger, og fakturabeløbene bogføres automatisk på de sædvanlige samlekonti. Benyt følgende fremgangsmåde for at oprette en forudbetaling.

1.  Konfigurer posteringsprofiler til forudbetalinger.
2.  I debitorparametre og kreditorparametre, under **Finans og moms** skal du vælge den nye posteringsprofil ved hjælp af parameteren for **posteringsprofilen til betalingskladden med forudbetaling**.
3.  Opret en betalingskladde, og opret derefter en ny betaling.
4.  Du kan markere betalingen som forudbetaling. Hvis en betaling er markeret som en forudbetaling, er betalingen bogført på finanskonti, der er defineret på den posteringsprofil, du har oprettet i trin 1 og 2. Og hvis betalingen er markeret som en forudbetaling, beregnes der moms. Nogle regeringer kræver, at momsen betales, når der registreres en forudbetaling, selvom der ikke er en faktura.
5.  Bogfør forudbetalingen.
6.  Valgfrit: Du kan udligne forudbetaling på indkøbsordren eller salgsordren, før du opretter fakturaen. På siden for salgsordren eller indkøbsordren i handlingsruden skal du bruge **Udlign transaktioner**.
7.  Når kreditoren leverer varerne eller tjenesterne, kan du registrere fakturaen. Hvis du har udlignet forudbetaling mod indkøbsordren eller salgsordren i trin 6, udlignes forudbetalingen automatisk mod den faktura, du har oprettet. Hvis du ikke har udlignet forudbetaling mod indkøbsordren eller salgsordren, kan du manuelt udligne den mod fakturaen ved hjælp af **Udlign transaktioner** på debitor- eller kreditorsider. Forudbetalingsbeløbet tilbageføres derefter fra den midlertidige debitor- eller kreditorfinanskonto. Og hvis der blev beregnet moms, ændres de, da fakturaen indeholder de faktiske momsafgifter.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Oversigt over processen for forudbetalingsfakturering
Forudbetalingsfakturaer er en del af almindelig forretningspraksis. En kreditor udsteder forudbetalingsfakturaer for at kræve et depositum for køb, før indkøbsordren er opfyldt. Nogle kreditorer kan f.eks. kræve forudbetaling for bestemte varer eller tjenester. Hvis en kreditor udsteder en faktura, der kræver forudbetaling, kan du bruge forudbetalingsfakturering. En værdi for forudbetaling kan defineres på indkøbsordren, der registreres og betales en forudbetalingsfaktura, og derefter anvendes forudbetalingsfakturaen på den endelige faktura. Benyt følgende fremgangsmåde for at oprette en forudbetaling.

1.  Indkøberen opretter, bekræfter og sender derefter en indkøbsordre, som kreditoren har anmodet om forudbetaling for. Værdien af forudbetalingen er defineret på indkøbsordren som en del af aftalen.
2.  Kreditoren sender en forudbetalingsfaktura.
3.  Kreditorkoordinatoren registrerer forudbetalingsfakturaen på indkøbsordren, og derefter betales forudbetalingsfakturaen.
4.  Når kreditoren leverer varerne eller tjenesterne, og de tilhørende kreditorfakturaer er modtaget, anvender kreditorkoordinatoren det forudbetalingsbeløb, der allerede er betalt på fakturaen.
5.  Kreditorkoordinatoren betaler og udligner det resterende beløb på fakturaen.





