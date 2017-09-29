---
title: Indbetalingskortrapport for Europa
description: Dette emne indeholder oplysninger om indbetalingskortrapporter for Europa.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 264604
ms.search.region: Belgium, Denmark, Finland, Norway, Switzerland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: e3fcef720fb38de45ed357e53c1ec6923f72fd63
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017

---

# <a name="payment-slip-report-for-europe"></a>Indbetalingskortrapport for Europa

[!include[banner](../includes/banner.md)]


Dette emne indeholder oplysninger om indbetalingskortrapporter for Europa.

Funktionerne for indbetalingskortrapporter er tilgængelige for juridiske enheder, der har deres primære adresse i Danmark, Belgien, Norge, Schweiz eller Finland. Virksomheder vedhæfter ofte udskrevne indbetalingskort til fakturaer for at angive en betalingsreference til brug ved bogføring og betaling. Indbetalingskortet kan bruges til projekt- eller servicefakturaer, rykkere, rentenotaer og kontoopgørelser samt til salgsfakturaer og fritekstfakturaer.

## <a name="set-up-a-creditor-id-number-denmark-only"></a>Oprette et kreditor-id-nummer (kun Danmark)
Følg disse trin for at angive din virksomheds kreditoridentifikationsnummer (ID). Dit pengeinstitut leverer dette nummer. Nummeret bruges som reference, når der modtages debitorbetalinger gennem pengeinstitutter.

1.  Klik på **Virksomhedsadministration** &gt; **Organisationer** &gt; **Organisation** &gt; **Juridiske enheder**.
2.  På oversigtspanelet **Bankkontooplysninger** i feltet **FI-kreditor-ID** skal du angive dit entydige otte-cifrede kreditor-id.
3.  Luk formen for at gemme ændringerne.

## <a name="set-up-a-payment-slip-attachment-format-for-invoices-interest-notes-collection-letters-and-account-statements"></a>Oprette et formater for vedhæftning af indbetalingskort for fakturaer, rentenotaer, rykkere og kontoudtog
Følg disse trin for at oprette et format for indbetalingskort til vedhæftning til salgsfakturaer, fritekstfakturaer, rentenotaer, rykkere og kontoopgørelser.

1.  Klik på **Debitor** &gt; **Opsætning** &gt; **Formularer** &gt; **Formularopsætning**.
2.  Under fanen **Faktura** i feltet **Tilknyttet betalingsbilag på debitorfaktura** skal du vælge formatet for vedhæftning af indbetalingskortet.
3.  Under fanerne **Fritekstfaktura**, **Rentenota**, **Rykker** og **Kontoudtog** skal du vælge et format for vedhæftning af indbetalingskort for hver dokumenttype.
4.  Luk formen for at gemme ændringerne.

Følg disse trin for at oprette et format for vedhæftning af indbetalingskort til projektfakturaer.

1.  Klik på **Projektstyring og regnskab** &gt; **Konfiguration** &gt; **Formularer** &gt; **Formularopsætning**.
2.  I feltet **Tilknyttet betalingsbilag** skal du vælge formatet for vedhæftningen af indbetalingskortet.

## <a name="assign-a-payment-slip-attachment-format-to-a-customer-account"></a>Tildele et format for vedhæftning af indbetalingskort til en debitorkonto
Når du har oprettet formatet for et indbetalingskort til vedhæftning til salgsfakturaer, fritekstfakturaer, rentenotaer, rykkere, kontoopgørelser og projektfakturaer, kan du tildele specifikke formater til en udvalgt debitor.

1.  Klik på **Debitor** &gt; **Generelt** &gt; **Kunder** &gt; **Alle kunder**.
2.  Opret en ny debitor, eller vælg en eksisterende debitor.
3.  I oversigtspanelet **Faktura og levering** i felterne **På en debitorfaktura**, **På en fritekstfaktura**, **På en rentenota**, **På en rykker**, **På en projektfaktura** og **På en kontoopgørelse** skal du vælge formatet for vedhæftning af indbetalingskort, der skal ledsage hver type dokument, der sendes til den valgte debitor.
4.  Luk formen for at gemme ændringerne.




