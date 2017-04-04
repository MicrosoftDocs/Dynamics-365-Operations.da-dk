---
title: Betaling slip rapport for Europa
description: Dette emne indeholder oplysninger om betaling slip rapporter for Europa.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264604
ms.assetid: 551e047b-4581-4a77-b470-c4f8d395c375
ms.search.region: Belgium, Denmark, Finland, Norway, Switzerland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: c795466753ca1515790b7961b989aac6e7d63c2c
ms.lasthandoff: 03/31/2017


---

# <a name="payment-slip-report-for-europe"></a>Betaling slip rapport for Europa

Dette emne indeholder oplysninger om betaling slip rapporter for Europa.

Funktionalitet til betaling slip rapporter er tilgængelige for juridiske enheder, der har deres primære adresse i Danmark, Belgien, Norge, Schweiz eller Finland. Virksomheder vedhæfter ofte udskrevne indbetalingskort til fakturaer for at angive en betalingsreference for bogføring og betaling. Indbetalingskortet kan bruges til projekt- eller servicefakturaer, rykkere, rentenotaer og kontoopgørelser samt til salgsfakturaer og fritekstfakturaer.

## <a name="set-up-a-creditor-id-number-denmark-only"></a>Konfigurere en kreditor-id-nummer (kun Danmark)
Følg disse trin for at angive din virksomheds kreditor identifikationsnummer (ID). Dit pengeinstitut indeholder dette nummer. Det bruges som reference, når der modtages betalinger fra kunder via finansielle institutioner.

1.  Klik på **virksomhedsadministration**&gt;**Setup**&gt;**organisation**&gt;**juridiske enheder**.
2.  På den **bankkontooplysninger** oversigtspanelet i den **FI-kreditor-ID** skal du angive dit entydige otte-cifrede kreditor-id.
3.  Luk formen for at gemme ændringerne.

## <a name="set-up-a-payment-slip-attachment-format-for-invoices-interest-notes-collection-letters-and-account-statements"></a>Oprette et indbetalingskortformat, der vedhæftet fil til fakturaer, rentenotaer, rykkere og kontoopgørelser
Følg disse trin for at angive et format for betaling slip vedhæftede filer, der ledsager salgsfakturaer, fritekstfakturaer, rentenotaer, rykkere og kontoopgørelser.

1.  Klik på **tilgodehavender**&gt;**Setup**&gt;**formularer**&gt;**formopsætning**.
2.  På den **faktura** under fanen den **tilknyttet betalingsbilag på kundens faktura** skal du vælge indbetalingskortformat for vedhæftet fil.
3.  På den **fritekstfaktura**, **rentenota**, **rykker**, og **konto sætningen** faner, Vælg et indbetalingskortformat, der vedhæftet fil for hver dokumenttype.
4.  Luk formen for at gemme ændringerne.

Følg disse trin for at angive et format for betaling slip vedhæftede filer, projektfakturaer.

1.  Klik på **projektstyring og regnskab**&gt;**Setup**&gt;**formularer**&gt;**formopsætning**.
2.  I den **tilknyttet betalingsbilag** skal du vælge indbetalingskortformat for vedhæftet fil.

## <a name="assign-a-payment-slip-attachment-format-to-a-customer-account"></a>Tildele et indbetalingskortformat for vedhæftet fil til en debitorkonto
Når du opretter vedhæftede filer for indbetalingskortformat for salgsfakturaer, fritekstfakturaer, rentenotaer, rykkere, kontoudtog og projektfakturaer, kan du tildele specifikke formater til en udvalgt debitor.

1.  Klik på **tilgodehavender**&gt;**almindelige**&gt;**kunder**&gt;**alle kunder**.
2.  Opret en ny kunde, eller Vælg en eksisterende kunde.
3.  På den **faktura- og** i oversigtspanelet i den **på en debitorfaktura**, **på en fritekstfaktura**, **på en rentenota**, **på en rykker**, **på en projektfaktura**, og **på et kontoudtog** skal du vælge formatet for betaling slip vedhæftede filer, der skal ledsage hver type dokument, der sendes til den valgte debitor.
4.  Luk formen for at gemme ændringerne.



