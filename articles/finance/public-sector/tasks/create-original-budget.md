---
title: Oprette et oprindeligt budget og derefter tilbageføre foreløbige budgetposter i den offentlige sektor
description: Dette emne indeholder oplysninger om, hvordan du opretter og tilbagefører en oprindelig budgetpost ved hjælp af budgetmodel- og dimensionsværdier med foreløbige budgetbeløb.
author: twheeloc
ms.date: 02/14/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7758a1c9edfa129ba8b63a146b38ed3f119fd051
ms.sourcegitcommit: 6a269db08e8bb3bb3405c9f4a512091d13c80faa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119420"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a>Oprette et oprindeligt budget og derefter tilbageføre foreløbige budgetposter i den offentlige sektor

[!include [banner](../../includes/banner.md)]

Når du opretter en oprindelig budgetpost og bruger budgetmodellen og dimensionsværdierne, der indeholder foreløbige budgetbeløb, kan de foreløbige budgetbeløb tilbageføres. Denne procedure er oprettet med PSUS-demodatafirmaet i den offentlige sektor partition.

1. Gå til **Budgettering > Budgetregisterposter**.
2. Klik på **Ny**.
3. Klik på rullelisten i feltet **Budgetmodel** for at åbne opslaget.
4. Find og vælg den ønskede post på listen.
5. Klik på rullelisten i feltet **Budgetkode** for at åbne opslaget.
6. På listen skal du klikke på **Oprindeligt budget**.
7. Klik på **Gem**.
8. Klik på **Tilføj linje**.
9. Valgfrit: Angiv en ny dato, hvis du vil ændre datoen i forhold til den i overskriften. Datoen bestemmer den regnskabsperiode, som budgettet registreres for.
10. Klik på rullelisten i feltet **Kontostruktur** for at åbne opslaget.
11. Find og vælg den ønskede post på listen.
12. I feltet **Dimensionsværdier** skal du specificere de ønskede værdier.
13. Angiv et tal i feltet **Beløb**.
14. Klik på rullelisten i feltet **Valuta** for at åbne opslaget.
15. Klik op linket i den valgte række på listen.
16. Klik på **Gem**.
17. Klik på **Opdater budgetsaldi**.
    * Valgfrit: Du kan vælge indstillingen **Tilbagefør foreløbigt budget**. Bemærk, at du kan tilbageføre alle foreløbige budgetposter eller kun de foreløbige budgetposter, der har den budgetkode, du angiver.  
    * For at angive valgfrie indstillinger skal du klikke på ikonet **Lås op** øverst på siden.  
18. Klik på **Opdater**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
