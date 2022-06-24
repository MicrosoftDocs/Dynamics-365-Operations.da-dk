---
title: Startside for budgetplanlægning
description: Denne artikel indeholder en oversigt over budgetplanlægningsfunktionens komponenter, budgetplanlægningsværktøjer og funktioner i Microsoft Dynamics 365 Finance.
author: panolte
ms.date: 04/29/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanningWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom:
- "106043"
- intro-internal
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a6a00bdae34e2aebcc4a015626eb044d90cd2887
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864391"
---
# <a name="budgeting-home-page"></a>Startside for budgetplanlægning

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over budgetplanlægningsfunktionens komponenter, budgetplanlægningsværktøjer og funktioner. 

## <a name="components-of-budgeting-functionality"></a>Komponenter til budgetplanlægningsfunktionalitet

Ressourceplanlægningens cyklus for en virksomhed består typisk af planlægning, budgetplanlægning og prognoseaktiviteter.

[![Komponenter til budgetplanlægningsfunktionalitet.](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg)

Processerne for både langsigtet strategisk planlægning og årlig budgetplanlægning understøttes via et budgetplandokument. Budgetplansdokumenter er tæt integreret med Microsoft Excel. Brugerne kan konfigurere ubegrænsede monetære og kvantitative scenarier og definere et organisationshierarki for budgetplanlægning for at understøtte budgetplanlægningsmetoder oppefra og ned og nedefra og op. Når et budget er oprettet og godkendt i ansøgningen, kan du konvertere budgetplanen til en budgetregisterpost. Budgetregisterposter indeholder værktøjer til vedligeholdelse af budgettet og til at opbevare beløb, der kan spores gennem budgetkoder. Med budgetregisterposter kan du revidere oprindelige budgetter, foretage overførsler og overføre budgetbeløb fra det foregående år. Baseret på det budget, der er etableret, kan en virksomhed aktivere budgetstyring. Kontrolniveauet afhænger af organisationskulturen og organisationens forfaldsniveau. Organisationer, der har et lavt forfaldsniveau, kan lade budgettet være "som det er" og måske være mere reaktive end proaktive, hvis et budget ikke lever op til forventningerne. Andre organisationer kan aktivere politikker for budgetstyring, der forhindrer brugere i at købe noget, hvis der ikke er tilgængelige midler i budgettet.

Endelig kan meget modne organisationer etablere en organisatorisk kultur, hvor medarbejderne er uddannet i organisatoriske mål, og følge disse mål via politikker som "Overvej et onlinemøde i stedet for en rejse". Ansøgningen omfatter en budgetstyringsstruktur, der gør det muligt for virksomhedens ledelse at vælge enten stringent kontrol (der forhindrer posteringer, der vil overskride budgettet) eller blød kontrol (hvor brugere advares om, at de vil overskride de disponible budgetmidler, men selv kan bestemme, hvordan de vil fortsætte). Endelig kan du bruge rullende prognoser. En rullende prognose er en almindelig sammenligning af budget med faktiske oplysninger, der bruges til at definere, hvor godt virksomheden arbejder mod budgettet. En rullende prognose bruges også til at identificere tendenser. I Finans og drift understøttes rullende prognose via et budgetplansdokument som første planlægningsaktiviteter. Rullende prognoser kan udføres parallelt med planlægning af den kommende budgetcyklus.

-   [Budgetplanlægningsoversigt](basic-budgeting-overview-configuration.md)
-   [Budgetstyringsoversigt](budget-control-overview-configuration.md)
-   [Oversigt over budgetplanlægning](budget-planning-overview-configuration.md)
-   [Budgetteret stilling](position-forecasting.md)
-   [Berettigelsesdokumenter for budgetplanlægning](budget-planning-justification-docs.md)
-   [Budgetplanlægningsskabeloner til Excel](budget-planning-excel-templates.md)

## <a name="budgeting-tools"></a>Budgetplanlægningsværktøjer
[![Budgetplanlægningsværktøjer.](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg) 

Yderligere planlægnings- og budgetplanlægningsfunktioner er tilgængelige og er integreret med finansbudgetter.

-   **Budgetter for arbejdskraft** – Budgetplanlægning af arbejdskraft omfatter detaljeret planlægning af budgetomkostningskomponenter for stillinger, kompensationsgrupper osv.
-   **Anlægsaktivbudgetter** – Baseret på oplysninger om anlægsaktiver kan du beregne planlagt afskrivning og registrere andre planlagte transaktioner, der er relateret til anlægsaktiver.
-   **Projektbudgetter** – I projektmodulet kan du oprette detaljerede projektprognoser. Projektprognoserne skal indeholde nærmere oplysninger om de planlagte timer, udgifter, gebyrer og varer.
-   **Behovsprognose** – Du kan beregne fremtidigt lagerbehov og oprette behovsprognoser baseret på historiske transaktionsdata.

Oplysninger om, hvordan du bringer planlægningsdata fra andre moduler til budgetplaner, finder du under [Integration af budgetplanlægning med andre moduler](budget-planning-integration-other-modules.md).

## <a name="user-interface-and-reporting-capabilities"></a>Brugergrænseflade og rapporteringsværktøjer
Brugere kan oprette budgetplaner enten direkte i klienten (ved hjælp af en konfigurerbar budgetplandokumentside) eller via Excel. Excel indeholder flere ekstra funktioner. Du kan for eksempel bruge eksterne data som en kilde til en budgetplan, udføre brugerdefinerede beregninger og bruge Microsoft-pivottabeller og -diagrammer. De fleste af variablerne i budgetplanlægningsprocessen kan konfigureres. 

Du kan f.eks. definere, hvem der udfører budgetplanlægning, hvad der er budgetteret, og hvordan processen ser ud. Selvom du kan bruge Excel til budgetplanlægning, gemmes ansøgningen som en enkelt faktakilde og er med til at forhindre problemer med budgetstyring. Periodiske processer kan bruges til at overføre startdata for budgetplanlægning til budgetplanen. Til rapportering tilbyder ansøgningen et sæt standardundersøgelsessider, så du kan se og analysere data for budgetplanlægning. Budgetplandata kan åbnes via [Financial Reporting](../general-ledger/financial-reporting-getting-started.md), og separate budgetplanscenarier kan vises som kolonner i den økonomiske rapport.








[!INCLUDE[footer-include](../../includes/footer-banner.md)]
