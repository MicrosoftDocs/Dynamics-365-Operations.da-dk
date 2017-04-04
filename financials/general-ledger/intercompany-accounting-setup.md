---
title: "Intern mellemregning opsætning"
description: "Dette emne forklarer, hvordan du kan konfigurere mellemregning, så du kan bruge IC-kladder til Finans fordelinger og økonomikladder daglige kladder, kreditor fakturajournaler og betalingskladder."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5fd279327013f26230146be38e23e9955c6f12c7
ms.lasthandoff: 03/31/2017


---

# <a name="intercompany-accounting-setup"></a>Intern mellemregning opsætning

Dette emne forklarer, hvordan du kan konfigurere mellemregning, så du kan bruge IC-kladder til Finans fordelinger og økonomikladder daglige kladder, kreditor fakturajournaler og betalingskladder.

IC-kladder kan oprettes i forskellige scenarier, som for daglige kladder, fakturajournaler kreditor, Finans tildelinger og centraliserede betalinger. Hvis du vil aktivere disse scenarier, skal du konfigurere mellemregning.

## <a name="define-main-accounts"></a>Definere hovedkonti
Først skal du oprette hovedkontoen for mellemregningen, som skal bruges til regnskabsposterne Forfalden til og forfalden fra. Det er en god ide at bruge entydige hovedkonti for hver virksomhed for at forenkle afstemning og eliminering af interne regnskabsposter. Hvis du bruger en samhandelspartner eller et modstykke dimension til at identificere den interne part, kan du definere dimensionen som en fast dimension på hovedkontoen, der er defineret i mellemregning. Når du har oprettet de hovedkonti, skal du indstille den **Main kontotype** til **balancen** på den **hovedkonti** side.

## <a name="define-journal-names"></a>Definere kladdenavne
Derefter skal du angive et kladdenavn. Angiv den **kladdetype** til **daglige** på den **kladdenavne** side. Det er en god ide at bruge et bestemt kladdenavn til mellemregning.

## <a name="define-intercompany-accounting-setup"></a>Definere interne regnskab opsætning
Den **mellemregning** side bruges til at oprette par af juridiske enheder, der kan udføre med hinanden. Den interne regnskab opsætning er delt, så opsætningen er synlig fra inden for alle juridiske enheder. Når du opretter en ny juridisk enhedspar, sikre, at du er opmærksom på, hvilken juridisk enhed er defineret som det oprindelige firma kontra destinationsregnskabet. Når du angiver IC-transaktioner, bestemmer transaktionen, hvilken juridisk enhed er iværksættelse eller med oprindelse i transaktionen. Eksempelvis er til brug ved mellemregning angivet for USMF (med oprindelse) og USSI (destination). Hvis brugeren er aktiv i USSI og indtaster en IC-transaktion med USMF, bogføres posteringen ikke fordi de mellemregninger er kun defineret for USMF der igangsætter. Hvis enten regnskab stammer kan en transaktion, skal du oprette et andet par juridiske enhed for den gensidige opsætning. 

Vælg den **debitere konto (skylder)** og **kreditkonto (at)** for både fra, og destinationslagerstedet juridiske enhed. Angive, hvilke **kladdenavn** der skal bruges, når posteringen oprettes i destinationsregnskabet. Kladde til det oprindelige firma allerede er kendt, da den er valgt af brugeren, når du opretter den interne transaktion. 

Vælg, hvilken juridisk enhed modtager regnskab til supplerende beløb, som kasserabatten eller realiserede gevinster/tab for centraliserede betalinger. 

En gensidig relation kan nemt konfigureres på den **mellemregning** side ved hjælp af den **opretter gensidig relation** knappen, når du har oprettet det første par juridiske enhed. Når parret gensidige oprettes, kopieres oplysningerne for destinationsregnskabet, til det oprindelige regnskab og omvendt. Den kladde, der er defineret for destinationsregnskabet forbliver. De fleste organisationer bruger samme navngivningskonventionen for deres kladdenavne, så kladdenavnet er den samme. Hvis kladdenavnet er forskellige, vises en advarsel på feltet for at fortælle dig, at kladden ikke findes, og du kan vælge en anden kladde.


