---
title: Angive leasingbogføringskonti
description: Denne artikel indeholder de bogføringskonti, der kræves til Aktivleasingtransaktioner, og forklarer, hvordan du kan definere bogføringskonti på siden Leasingbogføringsparametre.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6e3a0d8dd3bb3e58ca10b2efce0cc88a2f48d2de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859908"
---
# <a name="set-up-lease-posting-accounts"></a>Angive leasingbogføringskonti

[!include [banner](../includes/banner.md)]

Denne artikel indeholder de bogføringskonti, der kræves til Aktivleasingtransaktioner og forklarer, hvordan du kan definere bogføringskonti på siden **Leasingbogføringsparametre**.

For at overholde Accounting Standards Codification Topic 842 (ASC 842) og International Financial Reporting Standard 16 (IFRS 16), kan det være nødvendigt at oprette konti i din kontoplan. Alle konti, som du opretter for at overholde ASC- og IFRS-standarder, er dog ikke anlægsaktivkonti. Under ASC 842 registreres et ROU (Right-of-Inuse)-aktivet for både finans- og driftsleasingaftaler. Disse leasingaftaler er adskilt fra anlægsaktiver. (Du kan stadig vedligeholde et ROU-aktiv ved hjælp af anlægsaktiver).

Du kan finde flere oplysninger om at oprette kontostrukturer i [Oprette kontostrukturer](../general-ledger/tasks/create-account-structures.md). Du kan finde flere oplysninger om at oprette hovedkonto i [Oprette kontostrukturer](../general-ledger/tasks/create-main-account.md).

I følgende tabel vises eksempler på konti, du skal oprette for leasede aktivposteringer, hvis de ikke allerede er oprettet. Under IFRS 16 bruges driftsleasingrelationer stadig til leasingaftaler med lav værdi og som er kortsigtede.

| Finanskontonummer | Kontotype  | Kontonavn                                          |
|-----------------------|---------------|-------------------------------------------------------|
| 180150                | Aktiv         | Vehicle ROU-aktiv                                     |
| 180160                | Aktiv         | Opbygger ROU-aktiv                                    |
| 180250                | Aktiv         | Akkumuleret afskrivning - køretøjer                   |
| 180260                | Aktiv         | Akkumuleret afskrivning - bygninger                  |
| 222300                | Passiv     | Kortfristet forpligtelse - finansiel leasingaftale                |
| 222310                | Balance | Kortfristet forpligtelse - Operationelle leasingaftaler              |
| 250200                | Passiv     | Vekselgæld                                         |
| 250601                | Balance | Langfristet forpligtelse - finansiel leasingaftaler                 |
| 250602                | Balance | Langfristet forpligtelse - operationelle leasingaftaler               |
| 250606                | Balance | Udskudt leje                                         |
| 300160                | Balance | Overført resultat                                     |
| 604500                | Expense       | Leasingudgift                                         |
| 604501                | Expense       | Køretøj, driftsleasing, udgifts - rentetillæg  |
| 604502                | Expense       | Køretøj, driftsleasingudgift - amortisering        |
| 605200                | Expense       | bygning, driftsleasingudgift - rentetillæg |
| 605201                | Expense       | Bygning, driftsleasingudgift - amortisering       |
| 607101                | Expense       | Køretøj, leasingamortiseringsudgift                    |
| 607102                | Expense       | Bygning, leasingamortiseringsudgift                   |
| 607103                | Expense       | Udgift til værdiforringelse - finansiel leasingaftale                   |
| 607104                | Expense       | Udgift til værdiforringelse - driftsleasingaftaler                 |
| 618910                | Expense       | Leasingudgift - finansiel leasingaftale                        |
| 618920                | Expense       | Variable betalinger - finansiel leasingaftale                    |
| 618930                | Expense       | Variable betalinger - driftsleasingaftale                  |
| 800600                | Expense       | Køretøj, leasingrenteudgift                        |
| 800601                | Expense       | Bygning, leasingrenteudgift                       |
| 801201                | Balance | Gevinst og tab - leasingændring                      |

## <a name="configure-posting-accounts"></a>Konfigurere bogføringskonti

Hvis du vil tildele konti til de leasingaftaler og de grupper, der er oprettet, skal du konfigurere parametre til aktivleasing.

1. Gå til **Aktivleasing \> Opsætning \> Parametre til leasingpostering**.
2. Åbn oversigtspanelet **Leasingkonti** på fanen **Konti** . Fastsætte hovedkontiene til finansiel og driftsleasingaftaler til tilsvarende **Bogføringstype**. I ovenstående tabel vises de konti, der er knyttet til drifts- og finansiel leasingaftaler.

    > [!NOTE]
    > Dette trin kræver, at du konfigurerer separate konti for både drifts- og finansielle leasingaftaler for hver bogføringstype undtagen **Forskudt leasingaftaleudgift** og **Leasingaftalestigning/-reduktion**. Firmaer, der overholder IFRS 16-regnskabsstrukturen, skal tilføje en hovedkonto til driftsleasingaftalen. Men systemet vil ikke bruge denne konto, selvom det er et obligatorisk felt, da alle rettigheder i IFRS 16 er klassificeret som finansielle leasingaftaler.
    >[!NOTE]
    > **Leasingaftalestigning/-reduktion** bruges som bogføringstype for yderligere anlægsaktiver, herunder **Indledende købspris, Leasingincitamenter, forudbetalinger ved leasing og reduktion af omkostninger**, men bogføres under brugsretsaktivets hovedkonto, som sætter standard til **Leasingaktiv**.        
    
3. Hvis du vil vælge en bestemt leasinggruppe, der svarer til hovedkontoen, skal du i feltet **Kontokode** vælge **Gruppe**. Vælg derefter den leasinggruppe, der skal tilknyttes hovedkontoen, i feltet **Konto/gruppenummer**.
4. Hvis du vil tildele kontokoder til de administrative omkostninger, der er oprettet i systemet, skal du i oversigtspanelet vælge **Udligningsomkostninger** i feltet **Udgiftstype** for at vælge en udgift. Tildel derefter de finans- og driftskonti, der skal bruges til hvert enkelt kartotek.

    > [!NOTE]
    > Den valgte finans- eller driftskonto debiteres, når fakturaen for den planlagte udgift bogføres.
    > **Forskudt leasingaftaleudgift** bruges som bogføringstype for udligningsomkostninger, men bogføres på defineret **Modkonto** i **Betalingsplanlinjerne for udligningsomkostninger** i formen leasingoplysninger eller leasingkartotek.   


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
