---
title: Konfiguration af mellemregning
description: I dette emne beskrives, hvordan du kan konfigurere mellemregning, så du kan bruge interne kladder til finansfordelinger og økonomikladder, f.eks. kassekladder, kreditorfakturakladder og betalingskladder.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce07a29d7aa5057d0b61c7fcc6bb87a0a2755fc9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550276"
---
# <a name="intercompany-accounting-setup"></a>Konfiguration af mellemregning

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du kan konfigurere mellemregning, så du kan bruge interne kladder til finansfordelinger og økonomikladder, f.eks. kassekladder, kreditorfakturakladder og betalingskladder.

Interne kladder kan oprettes i forskellige scenarier, f.eks. for kassekladder, kreditorfakturakladder, finansfordelinger og centraliserede betalinger. Hvis du vil aktivere disse scenarier, skal du konfigurere mellemregning.

## <a name="define-main-accounts"></a>Definere hovedkonti
Først skal du oprette hovedkontoen for mellemregningen, som skal bruges til regnskabsposterne Forfalden til og forfalden fra. Det er en god ide at bruge entydige hovedkonti for hver virksomhed for at forenkle afstemning og eliminering af interne regnskabsposter. Hvis du bruger en samhandelspartner eller en modpartsdimension til at identificere den interne part, kan du definere denne dimension som en fast dimension i hovedkontoen, der er defineret i mellemregningen. Når du har oprettet hovedkontiene, skal du indstille feltet **Hovedkontotype** til **Balance** på siden **Hovedkonti**.

## <a name="define-journal-names"></a>Definere kladdenavne
Derefter skal du angive et kladdenavn. Indstil feltet **Kladdetype** til **Dagligt** på siden **Kladdenavne**. Det er en god ide at bruge et bestemt kladdenavn til mellemregning.

## <a name="define-intercompany-accounting-setup"></a>Definere konfiguration af mellemregning
Siden **Mellemregning** bruges til at oprette de par af juridiske enheder, der kan udføre transaktioner indbyrdes. Konfigurationen af mellemregning deles, så opsætningen er synlig fra alle juridiske enheder. Når du opretter et nyt juridisk enhedspar, skal du være opmærksom på, hvilken juridisk enhed der er defineret som den oprindelige virksomhed kontra modtagervirksomheden. Når du angiver mellemregninger, bestemmer transaktionen, hvilken juridisk enhed der iværksætter transaktionen, eller hvor transaktionen har sin oprindelse. Eksempelvis konfigureres det interne regnskab til USMF (oprindelse) og USSI (destination). Hvis brugeren er aktiv i USSI og indtaster en mellemregning med USMF, bogføres transaktionen ikke, fordi mellemregninger kun defineres, når USMF er oprindelsen. Hvis begge virksomheder kan være oprindelse til en transaktion, skal du oprette endnu et juridisk enhedspar til den reciprokke opsætning. 

Vælg **Debetkonto (forfalden til)** og **Kreditkonto (forfalden fra)** for både den juridiske oprindelses- og destinationsenhed. Angiv, hvilket **Kladdenavn** der skal bruges, når transaktionen oprettes i modtagervirksomheden. Kladden for den oprindelige virksomhed allerede er kendt, da den er valgt af brugeren, når du opretter den interne transaktion. 

Vælg til sidst, hvilken juridisk enhed der modtager regnskabet for supplerende beløb, som kasserabatten eller realiserede gevinster/tab for centraliserede betalinger. 

En gensidig relation kan nemt konfigureres på siden **Mellemregning** ved hjælp af knappen **Opret reciprok relation**, når du har oprettet det første juridiske enhedspar. Når det gensidige par er oprettet, kopieres oplysningerne for modtagervirksomheden til den oprindelige virksomhed og omvendt. Den kladde, der er defineret for modtagervirksomheden, forbliver. De fleste organisationer bruger samme navngivningskonvention til deres kladdenavne, så kladdenavnet er det samme. Hvis kladdenavnet er anderledes, vises en advarsel i feltet om, at kladden ikke findes, og du kan vælge en anden kladde.



