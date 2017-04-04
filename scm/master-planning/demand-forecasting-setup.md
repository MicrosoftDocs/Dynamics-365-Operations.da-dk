---
title: Konfigurere behovsprognoser
description: "Dette emne omhandler de konfigurationsopgaver, du skal udføre, for at forberede behovsprognoser."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f629329f4f50bd7c8edcfd70641bace01a1c53aa
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-setup"></a>Konfigurere behovsprognoser

Dette emne omhandler de konfigurationsopgaver, du skal udføre, for at forberede behovsprognoser.  

Konfigurationsopgaverne omfatter angivelse af følgende data og parametre.

## <a name="item-allocation-key"></a>Varefordelingsnøgle
En behovsprognose beregnes kun for en vare og dens dimensioner, hvis varen er en del af en varefordelingsnøgle. Denne regel håndhæves til gruppe et stort antal elementer, så der kan oprettes efterspørgselsprognoser hurtigere. Varens fordelingsprocent af nøgler ignoreres, når der genereres efterspørgselsprognoser. Prognoser oprettes udelukkede ud fra historiske data. 

En vare og dens dimensioner må kun være en del af én varefordelingsnøgle, hvis varefordelingsnøglen anvendes under prognoseoprettelsen. 

For at tilføje en aktie enhed (SKU) i en varefordelingsnøgle, gå til **Master planning**&gt;**Setup**&gt;**efterspørgsel prognoser**&gt;**vare fordelingsnøgler**. Brug siden **Tildel varer** til at tildele en vare til en fordelingsnøgle.

## <a name="intercompany-planning-groups"></a>Interne planlægningsgrupper
Behovsprognoser genererer prognoser på tværs af firmaet. I Microsoft Dynamics 365 for operationer, er virksomheder, der er planlagt sammen grupperet i én interne planlægningsgruppe. For at angive pr. firma, skal betragtes som varefordelingsnøgler til budgettering af behov, kan du knytte en varefordelingsnøgle til den interne planlægning gruppemedlem ved at gå til **Master planning**&gt;**Setup**&gt;**interne planlægningsgrupper**. 

Hvis ingen varefordelingsnøgler tildeles medlemmer af intern planlægningsgruppe, beregnes en efterspørgselsprognose som standard for alle varer, der er knyttet til alle varefordelingsnøgler fra alle Dynamics 365 for operationer virksomheder. Der er flere filtreringsindstillinger for firmaer og varefordelingsnøgler på den siden **Generér statistisk budgetgrundlag**. 

Gennemse antallet varer, der er lavet prognose for. Unødvendige varer kan medføre øgede omkostninger, når du bruger Microsoft Azure Machine Learning.

## <a name="demand-forecasting-parameters"></a>Parametre til behovsprognoser
Hvis du vil konfigurere efterspørgsel, prognoser parametre, gå til **Master planning**&gt;**Setup**&gt;**efterspørgsel, prognoser parametre**. Da behovsprognoser kører på tværs af firmaet, er konfigurationen global. Med andre ord gælder konfigurationen for alle virksomheder. 

Behovsprognose genererer prognosen i antal. Måleenheden, antallet skal udtrykkes i, skal derfor angives i feltet **Behovsprognoseenhed**. Måleenheden skal være entydig for at sikre, at aggregering og procentvis fordeling giver mening. Få flere oplysninger om aggregering og procentvis fordeling under [Foretage manuelle justeringer af prognosegrundlaget](manual-adjustments-baseline-forecast.md). Når det gælder hver måleenhed, der bruges til lagerenheder, der er inkluderet i behovsprognose, skal du sørge for, at der er en omregningsregel for måleenheden og den generelle måleenhed for prognoser. Når prognosen er kørt, logføres listen over varer, der ikke har omregning af måleenhed, så du kan nemt rette konfigurationen. 

Behovsprognoser kan bruges til at lave prognoser om både afhængigt og uafhængigt behov. Hvis f.eks. kun afkrydsningsfeltet **Salgsordre** er markeret, og hvis alle de varer, der tages i betragtning i forhold til behovsprognose, er varer, der sælges, beregner systemet uafhængigt behov. De kritiske underkomponenter kan imidlertid føjes til varefordelingsnøgler og medtages i behovsprognoser. Hvis afkrydsningsfeltet er markeret **Produktionslinje** i dette tilfælde, beregnes en behovsprognose. 

Der findes to metoder til oprettelse af en oprindelig prognose i Dynamics 365 for operationer. Du kan bruge prognosemodeller over på historiske data, eller du kan blot kopiere de historiske data til prognosen. Feltet **Strategi for generering af prognose** gør det muligt at vælge mellem disse to metoder. Hvis du vil bruge prognosemodeller, skal du vælge **Azure Machine Learning**. 

Ved at klikke på **Prognosedimensioner** i venstre rude på siden **Parametre til behovsprognoser**, kan du også vælge sættet af prognosedimensioner, der skal bruges, når der oprettes behovsprognoser. En prognosedimension angiver det detaljeniveau, prognosen er defineret for. Firma, sted og varefordelingsnøgle er obligatoriske prognosedimensioner, men du kan også oprette prognoser ud fra lagersted, lagerstatus, debitorgruppe, debitorkonto, land, delstat og vare plus alle varedimensionsniveauer. 

Du kan når som helst tilføje prognosedimensioner til listen over dimensioner, der bruges til behovsprognoser. Du kan også fjerne prognosedimensioner fra listen. Manuelle justeringer går dog tabt, hvis du tilføjer eller fjerner en prognosedimension. 

Det er ikke alle varer, der fungerer på samme måde, hvis man ser det ud fra en behovsprognose. Lignende varer kan grupperes i en varefordelingsnøgle, og parametre som transaktionstyper og indstillinger for prognosemetode kan angives pr. varefordelingsnøgle. Klik på **Varefordelingsnøgler** i venstre rude på siden **Parametre til behovsprognoser**. 

For at oprette budgettet, bruger Dynamics 365 for operationer en Machine Learning-webtjeneste. Hvis du vil oprette forbindelse til tjenesten, skal du angive Dynamics 365 i forbindelse med følgende oplysninger Hvis du logger på Microsoft Azure Machine Learning Studio:

-   Webtjeneste-API-nøglen (application programming)
-   URL-adresse til webtjenesteslutpunkt
-   Kontonavn på Azure-lager
-   Nøgle til Azure-lagerkonto

**Bemærk!** Navn og nøgle til Azure-lageret er kun påkrævet, hvis du bruger en brugerdefineret lagerkonto. Hvis du installerer den lokale version, skal du have en brugerdefineret storage-konto på Azure, så tjenesten Machine Learning kan få adgang til de historiske data. 

For at oprette prognoser for efterspørgsel, kan du installere din egen service ved hjælp af Machine Learning Studio eller Dynamics-365 for operationer efterspørgsel, prognoser forsøg. Instruktioner til installation af Dynamics-365 for operationer efterspørgsel, prognoser forsøg som en webtjeneste er tilgængelige Dynamics 365 for operationer. På siden **Parametre til behovsprognoser** skal du klikke på fanen **Azure Machine Learning**.

## <a name="settings-for-the-dynamics-365-for-operations-demand-forecasting-machine-learning-service"></a>Indstillinger for Dynamics-365 for operationer kræver forudsigelse machine learning service
For at få vist de parametre, der kan konfigureres til Dynamics-365 for operationer kræver forudsigelse service, gå til **Varedisponering**&gt;**Setup**&gt;**efterspørgsel prognoser**&gt;**prognosticering algoritmeparametre**. Den **prognosticering algoritmeparametre** side vises standardværdierne for parametrene. Du kan overskrive disse parametre på den **efterspørgsel, prognoser parametre** side. Brug fanen **Generelt** for at overskrive parametrene globalt, eller brug fanen **Varefordelingsnøgler** til at overskrive parametrene pr. varefordelingsnøgle. Parametre, der er overskrevet for en varefordelingsnøgle, påvirker kun prognosen for varer, der er knyttet til den varefordelingsnøgle.

<a name="see-also"></a>Se også
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)


