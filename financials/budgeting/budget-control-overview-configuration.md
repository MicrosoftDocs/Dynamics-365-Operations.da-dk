---
title: Oversigt over budgetstyring
description: "Denne artikel introducerer budgetstyring og oplysninger for at hjælpe dig med at konfigurere budgetstyring i Microsoft Dynamics 365 for Operations, så du kan administrere finansielle midler."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 60493
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 4caef8eb4d11ad5d2ba1ce0e23d869c0b26b5466
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="budget-control-overview"></a>Oversigt over budgetstyring

[!include[banner](../includes/banner.md)]


Denne artikel introducerer budgetstyring og oplysninger for at hjælpe dig med at konfigurere budgetstyring i Microsoft Dynamics 365 for Operations, så du kan administrere finansielle midler.

<a name="overview"></a>Overblik
--------

Budgetstyring i Microsoft Dynamics 365 for Operations understøtter administration af en organisations økonomiske ressourcer via kontoplanen, arbejdsgange, brugergrupper, kildedokumenter og kladder, konfigurerbar beregning af budgetmidler, budgetcyklusser og tærskler. Med kontrol på plads kan en organisation planlægge, måle, styre og forudse sine finansielle ressourcer i hele regnskabsåret. 

Når budgetter er blevet godkendt i Dynamics 365 for Operations, kan du bruge budgetplaner til at generere budgetregisterposter for at registrere udgiftsbudgettet for en organisation. Du kan også oprette eller importere poster i budgetregisteret fra et tredjepartsprogram i stedet for ved hjælp af budgetplanlægningens funktioner. 

Udgifter kan registreres ved hjælp af hovedkonti og økonomiske dimensioner. Du kan konfigurere styring af de samlede udgifter til at opfylde organisationens politikker og behov ved at gruppere kombinationer af økonomiske dimensioner og hovedkonti. 

I følgende diagram vises budgetstyringens plads i faserne for en typisk budgetcyklus.

[![BudgetingCycle](./media/budgetingcycle-300x198.png)](./media/budgetingcycle.png) 

Du kan konfigurere budgetstyring ud fra flere faktorer:

-   **Økonomiske dimensioner** – Hvilke økonomiske dimensioner skal bruges til rapportering af budget og faktiske oplysninger, og hvilke økonomiske dimensioner kræves der for at styre budgettet? Er der visse kombinationer af dimensioner eller hovedkonti, der kræver særlig opmærksomhed? Er der for eksempel et krav om at spore budget i forhold til faktiske værdier efter bærer og program? Kræver rejseudgifter særlig opmærksomhed?
-   **Tid** – Hvilken tidsramme (regnskabsperiode, regnskabsperiode til dato osv.) vil blive anvendt til at vurdere tilgængelige budgetmidler?
-   **Kildedokumenter** – Hvilke kildedokumenter skal evalueres for budgetstyring? Skal dokumenterne evalueres pr. linje eller pr. dokument?
-   **Budgetmidler ved beregning** – Bør dokumenter som indkøbsrekvisitioner (budgetreservation) og indkøbsordrer (behæftelser) tages i betragtning ved beregningen af tilgængelige midler? Skal dokumenter i en kladdetilstand medtages i beregningen?
-   **Tilsidesætte rettighed** – Hvem har tilladelse til at overskride det disponible budget?

Budgetstyring er fuldt integreret med Dynamics 365 for Operations. Derfor kan du evaluere det disponible budget for både planlagte køb og faktiske køb. Budgetforespørgsler og -rapporter er tilgængelige. Derfor kan brugeren efter behov vurdere budgettet i hele budgetcyklussen og derefter foretage nødvendige justeringer i form af budgetrevisioner eller overflytninger. En budgetadministrator kan også eksportere budgettet og faktiske oplysninger til Microsoft Excel for bedre at kunne analysere og beregne prognose efter behov.

## <a name="configuring-budget-control"></a>Konfigurere budgetstyring
### <a name="budget-cycle-time-span"></a>Tidsperiode for budgetcyklus

Når grundlæggende budgettering er konfigureret, kan du definere tid eller start- og slutperioderne for budgettering og budgetstyring på siden **Tidsperiode for budgetcyklus**. Budgetcyklusser svarer ofte til regnskabskalendere, men det kan spænde over flere regnskabsår.

De næste trin i konfigurationen er fuldført på de forskellige faner på siden **Konfiguration af budgetstyring**.

### <a name="define-parameters"></a>Definer parametre

Baseret på de økonomiske dimensioner, der er aktiveret for budgettet, kan du bruge alle eller en del af de økonomiske dimensioner til budgetstyring. 

Derudover kan du angive standardtidsintervallet (eksempelvis **Regnskabsår**, **Regnskabsår til dato**, **Regnskabsperiode** eller **Kvartalsvis**), der skal udføres budgetstyring for i den relaterede tidsperiode for budgetcyklus. Du kan også angive en standardbudgetadministrator og den tærskel, der bruges til at give brugerne besked, når grænsen er nået. Værdierne i disse felter bruges som standardværdier i den nye budgetstyringsregel eller budgetgruppe, der oprettes. Standardværdierne kan dog ændres for enkelte grupper eller regler. 

De måder, budgetter oprettes og registreres på i budgetregisteret, spiller en rolle ved bestemmelse af, hvilken tidsperiode der skal vælges ved evaluering af tilgængelige budgetmidler. Hvis et årligt beløb til en dimensionsværdikombination er udviklet og anvendes, giver det evt. mening af anvende et regnskabsår eller regnskabsår til dato. Men hvis en organisation opretter budgetter efter regnskabsperiode eller tildeler regnskabsperioder og ønsker mere detaljeret styring, kan den eventuelt overveje at anvende regnskabsperiode til dato eller kvartalsvise tidsperioder. 

Desuden spiller en organisations kultur med hensyn til budgettering og budgetstyring en rolle for konfigurationen.

### <a name="over-budget-permissions"></a>Tilladelser til budgetoverskridelse

Dernæst kan du under fanen **Rettigheder til budgetoverskridelse** angive brugergrupper. Du kan også angive, om brugere, der er medlemmer af en gruppe, har tilladelse til at overskride budgettet. Du kan forhindre brugere i at overskride budgettet forbi den budgettærskel, der er angivet på siden **Budgetparametrene**, eller du kan forhindre dem i at overskride budgettet med et beløb, uanset tærsklen. Afhængigt af, hvor proaktivt en organisation administrerer sine udgifter, kan disse tilladelser hjælpe med at administrere organisationens finansielle midler. 

### <a name="budget-funds-available"></a>Tilgængelige budgetmidler

Dernæst kan du under fanen **Disponible budgetmidler** definere den formel, der bruges til at beregne de disponible budgetmidler. Alt efter, hvor konservativt en organisation administrerer sine finansielle midler eller under hensyntagen til forordninger eller branchemæssige krav, kan beregningen omfatte kladde- eller ikke-bogførte dokumenter. 

> [!NOTE] 
> Hvis denne beregning ændres i løbet af en budgetcyklus, påvirker det ikke dokumenter, der tidligere er godkendt under budgetstyring og bogført eller udført.

### <a name="documents-and-journals"></a>Dokumenter og journaler

Dernæst kan du under fanen **Dokumenter og journaler** vælge, hvilke kildedokumenter og journaler der skal underkastes budgetstyringskontroller, og om kontrollen sker for en linjepost eller for hele dokumentet. 

Du skal sammenholde de kildedokumenter, der er valgt, med de afkrydsningsfelter for balancer, der er medtaget i beregningen af de tilgængelige budgetmidler. Hvis du for eksempel har valgt **Budgetreservationer for behæftelser**, skal du vælge indstillingen **Indkøbsordrer**. Når der udføres en budgetkontrol for beløbene og kontiene i en indkøbslinje, er den budgetstyringskategori, der er tildelt reservationen **Behæftelse**. Når der udføres en budgetstyring for beløbene og kontiene i en indkøbsrekvisition, er den budgetstyringskategori, der tildeles reservationen, **Budgetreservation**. 

Hvis **Budgetreservationer for behæftelser** og/eller **Budgetreservationer for budgetreservation** er inkluderet i beregningen af tilgængelige budgetmidler og skal afspejles i bogføringer i finansmodulet, skal rammeaftale være aktiveret på siden **Finansparametre**.  

### <a name="assign-budget-models"></a>Tildel budgetmodeller

Dernæst kan du under fanen **Tildel budgetmodeller** tildele budgetmodeller for den tidsperiode for budgetcyklus, der skal medtages i budgetstyring.

### <a name="define-budget-control-rules"></a>Definer budgetstyringsregler

Dernæst skal du under fanen **Definer budgetstyringsregler** oprette specifikke regler baseret på budgetstyringsaktiverede økonomiske dimensioner. Hvis der for eksempel er fokus på udgifterne eller udgiftsintervallet for en afdeling, kan du bruge indstillingerne under denne fane til at definere og evaluere disse udgifter. Du kan definere forskellige tærskler for hver budgetstyringsregel. 

> [!Important]
> Budgetstyring aktiveres for alle hovedkonti af typen **Drift**, **Udgift**, **Indtægter, Balance, Passiv, Egenkapital** eller **Aktiv**. Hvis denne fane indeholder en regel, der har tomme kriterier, bliver budgetstyring aktiveret for **alle**kombinationer af økonomiske dimensioner, der omfatter hovedkonti af disse typer. Det er derfor vigtigt at oprette budgetstyringsregler, der kun definerer områder for kombinationer af økonomiske dimensioner, hvor det er vigtigt at aktivere budgetstyring.  

### <a name="select-main-accounts"></a>Vælg hovedkonti

Hvis **Hovedkonto** ikke er valgt som budgetstyringsdimension på siden **Definer parametre**, men bestemte udgifter administreres, kan du vælge disse udgifter under fanen **Vælg hovedkonti**. Hvis **Hovedkonto** er valgt som budgetstyringsdimension, kræves ingen poster.  

### <a name="define-budget-groups"></a>Definer budgetgrupper

Dernæst kan du under fanen **Definer budgetgrupper** evt. definere entydige kombinationer af økonomiske dimensioner, hvor budgetressourcer er grupperet til sekundær budgetkontrol. Du kan oprette en enkelt post, der omfatter hele organisationen, eller du kan definere flere grupper for at repræsentere de enkelte afdelinger eller bærere.  

### <a name="define-message-levels"></a>Definer meddelelsesniveauer

Hvis advarsler om budgetstyring skal undertrykkes for brugergrupper, kan du angive de pågældende grupper på siden **Definer meddelelsesniveauer**. Medlemmer af brugergrupperne modtager fortsat fejlmeddelelser, når de tilgængelige budgetmidler overskrides, afhængigt af deres tilladelser i forbindelse med overbudgettering.

### <a name="activate-budget-control"></a>Aktivér budgetstyring

Når budgetstyring er konfigureret, kan du slå den til og aktivere den under fanen **Aktivér budgetstyring**. Kladdeversionen træder derefter i kraft.
> [!Important]
> Når budgetstyring er aktiveret, og transaktioner er bogført, bør den ikke deaktiveres midt på året. Hvis budgetstyring deaktiveres, registreres aktiviteter ikke til budgetstyring, og der udføres ikke længere budgetkontrol. Derfor afspejler dokumenter, der allerede er bogført, muligvis ikke eftergivelse af beløb eller saldi i forespørgsler og rapporter, der er relateret til budgetstyring. Disse omfatter statistik for budgetstyring for enhver downstream eller tilpasning af bilag og kladder. 

Bemærk også, at transaktioner, herunder budgetregisterposter, der er bogført før budgetstyring aktiveres, ikke medtages i budgetstyring. Derfor anbefales det kun at aktivere budgetstyring i begyndelsen af en ny budgetcyklus. Sørg for, at budgetregisterposter, der indeholder startbudgetsaldi for budgetstyring, kun får opdateret budgetsaldi, når budgetstyring er aktiveret. Et åbent dokument (f.eks. en indkøbsordre) vil blive kontrolleret for disponible budgetmidler og får en budgetreservation til budgetstyring, når brugeren manuelt udløser budgetstyringskontrol i dokumentet.

## <a name="using-budget-control"></a>Brug af budgetstyring
Når budgetstyring er slået til, får brugerne budgetstyringsadvarsels- og -fejlmeddelelser i bilag og kladder, der er konfigureret til budgetstyring. Husk, at du kan konfigurere budgetstyring, så brugerne advares, når de overstiger budgetmidler, men kan stadig fortsætte med at bekræfte eller bogføre transaktionen. Brugerne kan få vist detaljer om mislykket budgetkontrol på siden **Fejl og advarsler i budgetstyring**.   

Fra denne side kan brugerne analysere ned i siden **Statistik for budgetstyring fordelt på periode** for at få vist oplysninger om budgettilgængelighed og reservationer for en valgt dimensionskombination i budgetstyring. Brugere kan også analysere ned i siden **Statistik for budgetstyring**for at få vist tilgængeligheden af budgettet for alle kombinationer af økonomiske dimensioner, der bruges i budgetstyring. 

Hvis budgetstyring er aktiveret for indkøbsordrer, kan budgetadministratoren bruge arbejdsområdet **Finansbudgetter og budgetter** til at gennemse køen af alle ikke-bekræftede indkøbsordrer med budgetkontroladvarsler og -fejl. Hvis budgetadministratoren har tilladelser til budgetoverskridelse, kan han eller hun bekræfte indkøbsordre direkte i arbejdsområdet.    




