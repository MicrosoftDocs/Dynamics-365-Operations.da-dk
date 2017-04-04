---
title: Startside for budgettering
description: "Dette emne indeholder en oversigt over budgettering funktionalitet komponenterne, budgettering værktøjer og rapportering funktioner i Microsoft Dynamics 365 for operationer."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: index-page
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106043
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: f7b4efc06b8e64c05da026850b41cb5b68c33ec3
ms.lasthandoff: 03/31/2017


---

# <a name="budgeting-home-page"></a>Startside for budgettering

Dette emne indeholder en oversigt over budgettering funktionalitet komponenterne, budgettering værktøjer og rapportering funktioner i Microsoft Dynamics 365 for operationer.

<a name="components-of-budgeting-functionality"></a>Komponenter til budgetteringsfunktionalitet
-------------------------------------

Ressourceplanlægningens cyklus for en virksomhed består typisk af planlægning, budgettering og prognoseaktiviteter.
[![Budgettering funktionalitet komponenter](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg) processer til både langsigtet strategisk planlægning og årlige budgetplanlægning understøttes via budgetplansdokument. Budgetplandokumenter er tæt integreret med Microsoft Excel. Brugerne kan konfigurere ubegrænset monetære og kvantitative scenarier og definere et organisationshierarki for budgettering for at understøtte budgetteringsmetoder oppefra og ned og nedefra og op. Når et budget er oprettet og godkendt i Microsoft Dynamics 365 for Operations, kan du konvertere budgetplanen til en budgetregisterpost. Budgetregisterposter indeholder værktøjer til vedligeholdelse af budgettet og til at opbevare beløb, der kan spores gennem budgetkoder. Med budgetregisterposter kan du revidere oprindelige budgetter, foretage overførsler og overføre budgetbeløb fra det foregående år. Baseret på det budget, der er etableret, kan en virksomhed aktivere budgetstyring. Kontrolniveauet afhænger af organisationskulturen og organisationens forfaldsniveau. Organisationer, der har et lavt forfaldsniveau, kan lade budgettet være "som det er" og måske være mere reaktiv end proaktiv, hvis et budget ikke lever op til forventningerne. Andre organisationer kan aktivere politikker for budgetkontrol, der forhindrer brugere i at købe, hvis der ikke er tilgængelige midler i budgettet. Endelig kan meget modent organisationer etablere en organisatorisk kultur, hvor medarbejderne er uddannet om organisatoriske mål og følge disse mål via politikker som "Overvej at onlinemøde i stedet for en rejse." Dynamics 365 for operationer, der omfatter en Budgetstyringsstrukturen, der gør det muligt for virksomhedens management, Vælg enten hard kontrolelement (der forhindrer posteringer, der vil overskride budgettet) eller bløde kontrolelement (hvor brugere advares om, at de vil overskride de disponible budgetmidler, men kan selv bestemme, hvordan du skal fortsætte). Endelig kan du bruge rullende forecasts. Et rullende budget er en almindelig sammenligning mellem det faktiske budget og bruges til at definere, hvor godt virksomheden arbejder mod budgettet. En rullende prognose bruges også til at identificere tendenser. I Microsoft Dynamics 365 for Operations understøttes rullende prognose via et budgetplansdokument som første planlægningsaktiviteter. Rullende prognoser kan udføres parallelt med planlægning af den kommende budgetcyklus.

-   [Grundlæggende budgettering: Oversigt og konfiguration](basic-budgeting-overview-configuration.md)
-   [Budgetstyring: Oversigt og konfiguration](budget-control-overview-configuration.md)
-   [Budgetplanlægning: Oversigt og konfiguration](budget-planning-overview-configuration.md)
-   [Stillingsprognose](position-forecasting.md)
-   [Budget planlægning berettigelsesdokumenter](budget-planning-justification-docs.md)
-   [Microsoft Excel-skabeloner til budgetplanlægning](budget-planning-excel-templates.md)

## <a name="budgeting-tools-in-dynamics-365-for-operations"></a>Budgetteringsværktøjer i Dynamics 365 for Operations
[![Budgettering værktøjer](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg) 

Yderligere planlægnings- og budgetteringsfunktioner er tilgængelige i hele Dynamics 365 for Operations og er integreret med finansbudgetter.

-   **Budgetter for arbejdskraft** – Budgettering af arbejdskraft omfatter detaljeret planlægning af budgetomkostningskomponenter for stillinger, kompensationsgrupper osv.
-   **Anlægsaktivbudgetter** – Baseret på oplysninger om anlægsaktiver kan du beregne planlagt afskrivning og registrere andre planlagte transaktioner, der er relateret til anlægsaktiver.
-   **Projektbudgetter** – I projektmodulet kan du oprette detaljerede projektprognoser. Projektprognoserne skal indeholde nærmere oplysninger om de planlagte timer, udgifter, gebyrer og varer.
-   ** Kræver prognosticering ** – baseret på historikdata for posteringer, kan du vurdere behovet for fremtidige lagerbeholdning og oprette efterspørgselsprognoser.

Oplysninger om, hvordan du bringer planlægningsdata fra andre moduler til budgetplaner, finder du under [Integration af budgetplanlægning med andre moduler](budget-planning-integration-other-modules.md).

## <a name="user-interface-and-reporting-capabilities"></a>Brugergrænseflade og rapporteringsværktøjer
I Microsoft Dynamics 365 for Operations kan brugere oprette budgetplaner enten direkte i Dynamics 365 for Operations-klienten (ved hjælp af en konfigurerbar budgetplandokumentside) eller via Excel. Excel indeholder flere ekstra funktioner. Du kan for eksempel bruge eksterne data som en kilde til en budgetplan, udføre brugerdefinerede beregninger og bruge Microsoft-pivottabeller og -diagrammer. De fleste af variablerne i budgetplanlægningsprocessen kan konfigureres. Du kan f.eks. definere, hvem der udfører budgettering, hvad der er budgetteret, og hvordan processen ser ud. Selvom du kan bruge Excel til budgetplanlægning, gemmes Dynamics 365 for Operations som en enkelt kilde til sandhed og hjælper med til at forhindre problemer med budgetkontrol. Periodiske processer kan bruges til at overføre startdata for budgettering til budgetplanen. Til rapportering tilbyder Dynamics 365 for Operations et sæt standardundersøgelsessider, så du kan få vist og analysere data for budgettering. Budgetplandata kan åbnes via Management Reporter, og separate budgetplanscenarier kan vises som kolonner i rapporten Management Reporter.





