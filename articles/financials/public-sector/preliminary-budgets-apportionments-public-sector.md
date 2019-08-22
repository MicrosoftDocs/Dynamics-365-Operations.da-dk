---
title: Foreløbige budgetter og fordelinger i den offentlige sektor
description: I dette emne beskrives oprettelsen af et foreløbigt budget og konfiguration af budgetlægning og budgetstyring for fordelinger og et foreløbigt budget.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetBalancesActuals, BudgetControlConfiguration, BudgetTransactionCode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 19701
ms.assetid: 8885478d-67f5-4db8-b97b-c0734216f8dd
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f992df9927b09b039c232794f6190496af793527
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845801"
---
# <a name="preliminary-budgets-and-apportionments-in-the-public-sector"></a>Foreløbige budgetter og fordelinger i den offentlige sektor

[!include [banner](../includes/banner.md)]

I dette emne beskrives oprettelsen af et foreløbigt budget og konfiguration af budgetlægning og budgetstyring for fordelinger og et foreløbigt budget. 

I de følgende afsnit i dette emne beskrives de budgetteringsfunktioner, der er tilgængelige for den offentlige sektor.  Før du læser dette emne, skal du også læse [Budgettering i den offentlige sektor](budgeting-public-sector.md).

-   Opsætning af budgettering og budgetstyring for fordelinger – Du kan definere en eller flere budgetkoder for fordelingsbudgettypen og konfigurere budgetstyring for fordelinger.
-   Opsætning af budgettering og budgetstyring for et foreløbigt budget – Du kan definere en eller flere budgetkoder for den foreløbige budgettype og konfigurere budgetstyring for foreløbige budgetter.
-   Oprettelse, visning og tilbageførsel af et foreløbigt budget – Du kan oprette poster til foreløbigt budget samt oprette oprindelige budgetposter.


## <a name="set-up-budgeting-and-budget-control-for-apportionments"></a>Konfigurere budgettering og budgetstyring for fordelinger
Fordelinger er den del af det oprindelige budget, der er godkendt til forbrug. En organisation i den offentlige sektor kan f.eks. have et oprindeligt budget på $ 1.000.000, men kun have tilladelse til at bruge $ 150.000 i første kvartal af regnskabsåret. Du kunne registrere en oprindelig budgetregisterpost for $ 1.000.000 for regnskabsåret. Derefter kunne du registrere en fordelingsbudgetregisterpost på $ 150.000 for de første tre måneder af året. Kun de $ 150.000, der blev fordelt, vil så kunne bruges i løbet af første kvartal. 

> [!NOTE] 
> Du kan ikke fordele mere end det oprindelige budgetbeløb for de økonomiske dimensionsværdier. 

Når du har konfigureret grundlæggende budgettering og budgetstyring, kan du bruge følgende til at føje oplysninger om fordelinger til grundlæggende budgettering og budgetstyring.

### <a name="how-do-i-define-budget-codes-for-the-apportionment-budget-type"></a>Hvordan definerer jeg budgetkoder for fordelingsbudgettypen?

Du kan definere en eller flere budgetkoder for fordelingsbudgettypen på siden **Budgetkoder**. Du skal definere budgetkoderne for den oprindelige budgettype under opsætningen af den grundlæggende budgettering. Når du opretter en ny budgetkode og en beskrivelse, skal du også vælge fordelingsbudgettypen.

Brug budgetkoder for fordelingsbudgettypen, når du angiver budgetregisterposteringer for de fordelte budgetbeløb. Brug budgetkoder for den oprindelige budgettype, når du angiver budgetregisterposteringer for de oprindelige budgetbeløb.

### <a name="how-do-i-configure-budget-control-for-apportionments"></a>Hvordan konfigurerer jeg budgetstyring for fordelinger?

Siden **Konfiguration af budgetstyring** indeholder indstillinger for arbejde med fordelinger. 

I afsnittet **Disponible budgetmidler** når du vælger indstillingen **Brug kun fordelt beløb**, bliver de andre indstillinger under **Beløb, der skal summeres** utilgængelige. Desuden indeholder beregningen af disponible budgetmidler kun fordelte beløb i beløbene, der skal summeres. Normalt vil du medtage faktiske udgifter, budgetreservationer for behæftelser, budgetreservationer for ubekræftede behæftelser og budgetreservationer for budgetreservationer i beløbene, som skal fratrækkes. 

> [!NOTE] 
> Når **Brug kun fordelt beløb** er valgt, spores det oprindelige budget, overførsler og revisioner stadig, men de bruges ikke i beregningen. 

Bemærk, at i afsnittet **Dokumenter og journaler** når du vælger **Indkøbsrekvisitioner**, er indstillingerne for indkøbsordrer og kreditorfakturaer valgt automatisk. 

Når du har defineret budgetregisterposter for grundlæggende budgettering og konfigureret budgetstyring for fordelinger, kan du oprette budgetregisterposter for det oprindelige budget og fordelingsbudgettyper. Du kan finde flere oplysninger under "Hvordan opretter jeg og få vist et foreløbigt budget?" senere i dette emne.

### <a name="tips"></a>Tip!

På siden **Budgetposteringer** kan du spore og overvåge budgetaktiviteter for fordelinger ved at få vist:

-   Budgetsaldi
-   Statistik for budgetstyring
-   Faktiske totaler vs. budgettotaler
-   Budgetregisterposteringer, der omfatter oprindelige budget og fordelinger

Du kan også spore og overvåge budgetaktiviteter for fordelinger fra følgende sider:

-   Siden **Periodernes budget** viser saldi for budget og fordelinger efter periode, akkumulerede beløb og den akkumulerede procent af summen af budgettet og fordelingerne for alle perioder.
-   Siden **Statistik for budgetstyring** viser budgetsaldiene for en budgetcyklus og budgetmodel. Du kan se flere oplysninger ved at vælge en linje i gitteret og derefter klikke på **Fordelinger**. Efter indkøbsrekvisitioner og indkøbsordrer er blevet bogført, kan du bruge siden **Statistik for budgetstyring** til at få vist budgetreservationer for behæftelser og budgetreservationer. **Bemærk!** Felterne **Fordelinger** og **Foreløbigt budget** vises kun, hvis du har valgt **Foreløbigt budget** og **Brug kun fordelt beløb** i afsnittet **Disponible budgetmidler** på siden **Konfiguration af budgetstyring**.
-   Siden **Faktisk vs. budget fordelt på periode** viser faktiske udgifter sammenlignet med summen af posterne i budgetregisteret for perioden:
    -   Feltet **Fordelinger** indeholder en sum af alle fordelingsbudgetregisterposterne for budgetmodel og dimensionsværdier.
    -   Kolonnen **Afvigelsesbeløb** viser resultatet af følgende beregning: fordeling for perioden - faktisk for perioden = afvigelsesbeløbet for perioden.
    -   Feltet **Foreløbigt budget** indeholder en sum af alle de foreløbige budgetregisterposter for budgetmodellen og dimensionsværdier.

## <a name="set-up-budgeting-and-budget-control-for-a-preliminary-budget"></a>Konfigurere budgettering og budgetstyring for et foreløbigt budget
Når du har konfigureret grundlæggende budgettering og budgetstyring, kan du bruge følgende til at føje oplysninger om foreløbige budgetter til grundlæggende budgettering og budgetstyring. 

Du kan oprette et midlertidigt foreløbigt budget, mens det faktiske budget er ved at blive gennemset og godkendt. Hvis du bruger budgetstyring, kan du vælge kildedokumenter og regnskabskladder til at evaluere i forhold til budgetstyring, mens du bruger det foreløbige budget. Du kan spore beløbene i det foreløbige budget ved hjælp af separate budgetkoder for den foreløbige budgettype, og derefter, når det godkendte budget er vedtaget, kan de foreløbige budgetbeløb reduceres, når de godkendte budgetbeløb forhøjes.

### <a name="how-do-i-define-budget-codes-for-the-preliminary-budget-type"></a>Hvordan definerer jeg budgetkoder for den foreløbige budgettype?

Du kan definere en eller flere budgetkoder for den foreløbige budgettype på siden **Budgetkoder**. Hvis du vil spore forskellige kategorier af foreløbige budgetregisterposter, kan du definere flere budgetkoder for den foreløbige budgettype. 

Du skal definere budgetkoderne for den oprindelige budgettype under opsætningen af den grundlæggende budgettering. Når du opretter en budgetkode og en beskrivelse, skal du også vælge den foreløbige budgettype. 

Brug budgetkoder for den foreløbige budgettype, når du angiver budgetregisterposteringer for de foreløbige budgetbeløb. Brug budgetkoder for den oprindelige budgettype, når du angiver budgetregisterposteringer for de oprindelige budgetbeløb.

### <a name="how-do-i-configure-budget-control-for-preliminary-budgets"></a>Hvordan konfigurerer jeg budgetstyring for foreløbige budgetter?

Siden **Konfiguration af budgetstyring** indeholder indstillingerne for arbejde med foreløbige budgetter. I afsnittet **Disponible budgetmidler** skal du vælge indstillingen **Foreløbigt budget**. Bemærk, at du evt. skal klikke på **Opret udkast** for at fortsætte. 

> [!NOTE]
> Hvis foreløbige budgetter er medtaget i beregningen af de tilgængelige budgetmidler, er det vigtigt at tilbageføre de foreløbige budgetregisterposter, når de oprindelige budgetregisterposter registreres i budgetsaldiene. Hvis budgetregisterposter med foreløbige budgetkoder ikke tilbageføres, tilføjes både det foreløbige budget og de oprindelige budgettyper, som vil angive den disponible saldo for højt. Du kan finde flere oplysninger under "Hvordan tilbagefører jeg et foreløbigt budget?" senere i denne artikel. Bemærk, at i afsnittet **Dokumenter og journaler** når du vælger indstillingen **Indkøbsrekvisitioner**, er indstillingerne for indkøbsordrer og kreditorfakturaer valgt automatisk.


## <a name="create-view-and-reverse-a-preliminary-budget"></a>Opret, få vist og tilbagefør et foreløbigt budget
Når du har konfigureret grundlæggende budgettering og budgetstyring for det foreløbige budget, kan du oprette budgetregisterposter for den foreløbige budgettype.

### <a name="how-do-i-create-and-view-a-preliminary-budget"></a>Hvordan opretter og åbner jeg et foreløbigt budget?

Du kan oprette foreløbige budgetregisterposteringer for en specifik budgetmodel og dimensionsværdier. Når det faktiske budget er godkendt, kan du oprette oprindelige budgetregisterposter.

#### <a name="tips"></a>Tip!

For at få vist yderligere oplysninger om foreløbige budgetter skal du vælge følgende forespørgsler:

-   Brug siden **Statistik for budgetstyring** til at få vist budgetsaldiene for en budgetcyklus og budgetmodel. Efter indkøbsrekvisitioner og indkøbsordrer er blevet bogført, kan du få vist budgetreservationer for behæftelser og forudgående behæftelser.
-   Brug siden **Faktisk vs. budget fordelt på periode** til at få vist faktiske udgifter sammenlignet med summen af posterne i budgetregisteret for perioden: Feltet **Foreløbigt budget** indeholder en sum af alle de foreløbige budgetregisterposter for budgetmodellen og dimensionsværdier.

### <a name="how-do-i-reverse-a-preliminary-budget"></a>Hvordan tilbagefører jeg et foreløbigt budget?

Når du opretter en oprindelig budgetpost og bruger budgetmodellen og dimensionsværdierne, der indeholder foreløbige budgetbeløb, kan de foreløbige budgetbeløb tilbageføres. Du kan f.eks. angive et foreløbigt budgetbeløb på $2.500 på finanskonto 50000. Hvis du senere angiver en oprindelige budgetbeløb på $10.000 på finanskonto 50000, tilbageføres det foreløbige budgetbeløb på $2.500. Finanskontoen 50000 ville have et budgetbeløb på $ 10.000. 

Du kan få vist budgetregisterposter til det oprindelige budget ved at vælge budgetkontoposten i oversigtspanelet **Budgetkontoposter** på siden **Budgetregisterpost**. Klik på menulinjen på **Relaterede oplysninger**, og klik derefter på **Budgetregisterposter**.



