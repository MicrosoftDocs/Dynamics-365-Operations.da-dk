---
title: Konfigurere behovsprognoser
description: "Dette emne omhandler de konfigurationsopgaver, du skal udføre, for at forberede behovsprognoser."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 74d520199410711b80b750a12ee726633e09d01c
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017


---

# <a name="demand-forecasting-setup"></a>Konfigurere behovsprognoser

[!include[banner](../includes/banner.md)]


Dette emne omhandler de konfigurationsopgaver, du skal udføre, for at forberede behovsprognoser.  

Konfigurationsopgaverne omfatter angivelse af følgende data og parametre.

## <a name="item-allocation-key"></a>Varefordelingsnøgle
En behovsprognose beregnes kun for en vare og dens dimensioner, hvis varen er en del af en varefordelingsnøgle. Denne regel håndhæves for at gruppere et stort antal varer, så der hurtigere kan oprettes behovsprognoser. Procentdelen af varefordelingsnøglen ignoreres, når behovsprognoser genereres. Prognoser oprettes udelukkede ud fra historiske data. 

En vare og dens dimensioner må kun være en del af én varefordelingsnøgle, hvis varefordelingsnøglen anvendes under prognoseoprettelsen. 

Hvis du vil tilføje en lagerenhed til en varefordelingsnøgle, skal du gå til **Varedisponering** &gt; **Konfiguration** &gt; **Behovsprognose** &gt; **Varefordelingsnøgler**. Brug siden **Tildel varer** til at tildele en vare til en fordelingsnøgle.

## <a name="intercompany-planning-groups"></a>Interne planlægningsgrupper
Behovsprognoser genererer prognoser på tværs af firmaet. I Microsoft Dynamics 365 for Finance and Operations grupperes firmaer, der er planlagt sammen, i én intern planlægningsgruppe. For at angive pr. firma hvilke varefordelingsnøgler der skal tages i betragtning ved behovsprognoser, skal en varefordelingsnøgle knyttes til medlemmet af den interne planlægningsgruppe. Det gøres ved at gå til **Varedisponering** &gt; **Konfiguration** &gt; **Interne planlægningsgrupper**. 

Hvis der ikke tildeles nogen varefordelingsnøgler til medlemmer af den interne planlægningsgruppe, beregnes en behovsprognose for alle varer, der er knyttet til alle varefordelingsnøgler fra alle Finance and Operations-firmaer. Der er flere filtreringsindstillinger for firmaer og varefordelingsnøgler på den siden **Generér statistisk budgetgrundlag**. 

Gennemse antallet varer, der er lavet prognose for. Unødvendige varer kan medføre øgede omkostninger, når du bruger Microsoft Azure Machine Learning.

## <a name="demand-forecasting-parameters"></a>Parametre til behovsprognoser
Hvis du vil konfigurere parametre for behovsprognoser, skal du gå til **Varedisponering** &gt; **Konfiguration** &gt; **Parametre til behovsprognoser**. Da behovsprognoser kører på tværs af firmaet, er konfigurationen global. Med andre ord gælder konfigurationen for alle virksomheder. 

Behovsprognose genererer prognosen i antal. Måleenheden, antallet skal udtrykkes i, skal derfor angives i feltet **Behovsprognoseenhed**. Måleenheden skal være entydig for at sikre, at aggregering og procentvis fordeling giver mening. Få flere oplysninger om aggregering og procentvis fordeling under [Foretage manuelle justeringer af prognosegrundlaget](manual-adjustments-baseline-forecast.md). Når det gælder hver måleenhed, der bruges til lagerenheder, der er inkluderet i behovsprognose, skal du sørge for, at der er en omregningsregel for måleenheden og den generelle måleenhed for prognoser. Når prognosen er kørt, logføres listen over varer, der ikke har omregning af måleenhed, så du kan nemt rette konfigurationen. 

Behovsprognoser kan bruges til at lave prognoser om både afhængigt og uafhængigt behov. Hvis f.eks. kun afkrydsningsfeltet **Salgsordre** er markeret, og hvis alle de varer, der tages i betragtning i forhold til behovsprognose, er varer, der sælges, beregner systemet uafhængigt behov. De kritiske underkomponenter kan imidlertid føjes til varefordelingsnøgler og medtages i behovsprognoser. Hvis afkrydsningsfeltet er markeret **Produktionslinje** i dette tilfælde, beregnes en behovsprognose. 

Der findes to metoder til oprettelse af et prognosegrundlag i Finance and Operations. Du kan bruge prognosemodeller over på historiske data, eller du kan blot kopiere de historiske data til prognosen. Feltet **Strategi for generering af prognose** gør det muligt at vælge mellem disse to metoder. Hvis du vil bruge prognosemodeller, skal du vælge **Azure Machine Learning**. 

Ved at klikke på **Prognosedimensioner** i venstre rude på siden **Parametre til behovsprognoser**, kan du også vælge sættet af prognosedimensioner, der skal bruges, når der oprettes behovsprognoser. En prognosedimension angiver det detaljeniveau, prognosen er defineret for. Firma, sted og varefordelingsnøgle er obligatoriske prognosedimensioner, men du kan også oprette prognoser ud fra lagersted, lagerstatus, debitorgruppe, debitorkonto, land, delstat og vare plus alle varedimensionsniveauer. 

Du kan når som helst tilføje prognosedimensioner til listen over dimensioner, der bruges til behovsprognoser. Du kan også fjerne prognosedimensioner fra listen. Manuelle justeringer går dog tabt, hvis du tilføjer eller fjerner en prognosedimension. 

Det er ikke alle varer, der fungerer på samme måde, hvis man ser det ud fra en behovsprognose. Lignende varer kan grupperes i en varefordelingsnøgle, og parametre som transaktionstyper og indstillinger for prognosemetode kan angives pr. varefordelingsnøgle. Klik på **Varefordelingsnøgler** i venstre rude på siden **Parametre til behovsprognoser**. 

For at generere prognosen anvender Finance and Operations en Machine Learning-webtjeneste. Hvis du vil oprette forbindelse til tjenesten, skal du angive følgende oplysninger i Finance and Operations, hvis du logger på Microsoft Azure Machine Learning Studio:

-   Webtjeneste-API-nøglen (application programming)
-   URL-adresse til webtjenesteslutpunkt
-   Kontonavn på Azure-lager
-   Nøgle til Azure-lagerkonto

**Bemærk!** Navn og nøgle til Azure-lageret er kun påkrævet, hvis du bruger en brugerdefineret lagerkonto. Hvis du installerer den lokale version, skal du have en brugerdefineret lagerkonto på Azure, så Machine Learning-tjenesten kan få adgang til de historiske data. 

Hvis du vil oprette prognoseforudsigelser, kan du installere din egen tjeneste ved hjælp af Machine Learning Studio eller forsøg med Finance and Operations-behovsprognoser. Instruktioner til installation af forsøg med Finance and Operations-behovsprognoser som en webtjeneste er tilgængelig i Finance and Operations. På siden **Parametre til behovsprognoser** skal du klikke på fanen **Azure Machine Learning**.

## <a name="settings-for-the-finance-and-operations-demand-forecasting-machine-learning-service"></a>Indstillinger for Machine Learning-tjenesten til Finance and Operations-behovsprognose
For at få vist de parametre, der kan konfigureres for tjenesten til Finance and Operations-behovsprognoser, skal du gå til **Varedisponering** &gt; **Konfiguration** &gt; **Behovsprognoser** &gt; **Parametre til prognosealgoritme**. Siden **Parametre til prognosealgoritme** viser standardværdierne for parametrene. Du kan overskrive disse parametre på siden **Parametre til behovsprognoser**. Brug fanen **Generelt** for at overskrive parametrene globalt, eller brug fanen **Varefordelingsnøgler** til at overskrive parametrene pr. varefordelingsnøgle. Parametre, der er overskrevet for en varefordelingsnøgle, påvirker kun prognosen for varer, der er knyttet til den varefordelingsnøgle.

<a name="see-also"></a>Se også
--------

[Introduktion til behovsprognoser](introduction-demand-forecasting.md)

[Generere et statistisk budgetgrundlag](generate-statistical-baseline-forecast.md)

[Foretage manuelle reguleringer af prognosegrundlaget](manual-adjustments-baseline-forecast.md)




