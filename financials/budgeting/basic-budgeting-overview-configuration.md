---
title: Budgetteringsoversigt
description: "Næsten alle firmaer, der bruger Navision Financials funktionalitet i Microsoft Dynamics 365 for operationer vil skulle være i stand til at oprette rapporter over budget vs. faktiske oplysninger. I denne artikel forklares minimumkonfigurationen, der kræves for at oprette budgetter i Dynamics 365 for operationer eller indlæse dem fra et tredjepartsprogram."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a639e509cf6a3d2f1b850f27481d7b95546522b8
ms.openlocfilehash: b62e14f7c91692ae97bb332b38b0deeb328cc1bd
ms.lasthandoff: 03/31/2017


---

# <a name="budgeting-overview"></a>Budgetteringsoversigt

Næsten alle firmaer, der bruger Navision Financials funktionalitet i Microsoft Dynamics 365 for operationer vil skulle være i stand til at oprette rapporter over budget vs. faktiske oplysninger. I denne artikel forklares minimumkonfigurationen, der kræves for at oprette budgetter i Dynamics 365 for operationer eller indlæse dem fra et tredjepartsprogram.

<a name="overview"></a>Overblik
--------

Det godkendte budget for en juridisk enhed bevares i et dokument, der er kendt som en *Budgetregisterpost*. Linjerne i et budget register posten dokument er kendt som *budgetkonto* poster, og indeholder oplysninger om økonomiske dimensioner, datoer og beløb for det godkendte budget. Budget register post-dokument er integreret med grundlæggende økonomiske rapporter og undersøgelse sider, hvor finansbeløb faktiske sammenlignes med budgetbeløb. 

Der er flere metoder til oprettelse af budgetregisterposter i Dynamics 365 for operationer:

-   Du kan manuelt angive dokumentoplysninger på siden **Budgetregisterposter**.
-   Brug Microsoft Excel-skabelon, som du kan åbne ved at klikke på knappen **Åbn i Excel** på siden **Budgetregisterposter**.
-   Brug dataenheden **Budgetkontoposter** i Datastyring til at importere budgetregisterposter. Du bør overveje ved hjælp af denne metode og aktivere den **indstilles på grundlag** ** behandling ** parameter, når du skal importere mange budgetkontoposterne i systemet.
-   Hvis firmaet bruger budgetplanlægningsfunktionen til at forberede budgetdata, kan du bruge den periodiske proces **Generér budgetregisterpost**.

Posten i budgetregisteret betragtes som afsluttet, når du har opdateret budgetsaldi. På den **poster i budgetregisteret** skal du klikke på **opdatere budgetsaldi** for det valgte budget at registrere flere poster. Når du har opdateret budgetsaldiene, ændres status på budgetregisterposten til **Fuldført**. Fuldført budgetregisterpost kan ikke åbnes igen til redigering. Hvis budgetdataene skal justeres, skal du derfor oprette en ny budgetregisterpost i stedet for at korrigere data i den færdige budgetregisterpost.

## <a name="configuration"></a>Konfiguration
Når du konfigurerer budgettering, skal du starte på siden **Budgetparametre**. På denne side skal du definere budgetkladden, nummerserien for budgetregisterposter og standardfunktionsmåden i arbejdsområderne.

Næste skal du oprette arbejdsgange for budgetregisterpost på siden **Arbejdsgang for budgettering**, hvis der er politikker, der styrer godkendelse af budgetregistrerposter, baseret på budgettype (for eksempel overførsler eller revisioner). Hvis der er situationer, hvor overførsler kan tillades uden godkendelse via arbejdsgang, kan du definere regler for budgetoverførsel for at understøtte disse scenarier. 

På siden **Budgetteringsdimensioner** skal du vælge de økonomiske dimensioner, der bruges til budgettering, baseret på de dimensioner, der bruges i kontoplanen. Du kan vælge blandt alle økonomiske dimensioner, eller underopsætninger til disse, til budgettering.

Definere en * budgetmodel *, der svarer til alle eller nogle af budgetterne. Du kan bruge en enkelt budgetmodel til alle budgetregisterposter. Du kan også oprette separate modeller, der er baseret på budgettypen, geografisk beliggenhed eller anden måde, som et budget kan klassificeres på. 

> [!NOTE] 
> Hvis du bruger budgetstyring, kan du knytte kun én budgetmodel til en budgetcyklus for bestemte tidsrum. 

Opret *budgetkoder *, der identificerer typen af budgetposteringer, der skal bogføres og alle relaterede arbejdsgange. Budgetkoder kan understøtte følgende budgettyper:

-   Oprindeligt budget
-   Flytning
-   Revision
-   Behæftelse
-   Budgetreservation
-   Overført budget

Med budgetkoder kan du have et revisionsspor for godkendte budgetændringer gennem hele budgetcyklussen. Hvis en arbejdsproces, der er tilknyttet en budgetkode, arbejdsprocessen skal være aktiveret for alle budgetregisterposter, der bruger budgetkoden, og trin i arbejdsprocessen skal være fuldført, før du kan oprette forbindelse til posten i budgetregisteret på **fuldført** fase.  

Du kan eventuelt også angive *regler for budgetoverførsel*. Marker for at bruge regler for budgetoverførsel, **Brug regler for budgetoverførsler** på den **budgetparametrene** side. Når regler for budgetoverførsel bruges, opdateres budgetsaldi ikke, hvis budgetoverførselsregler overtrædes, hvis en bruger opretter et dokument ved hjælp af en budgetkode for typen **Overførsel**. Du kan f.eks. tillade budgetoverførselsdokumenter hvor udgiftsbudgettet overføres mellem hovedkonti for Salg og marketing-afdelingen, men kan forhindre budget i at blive overført fra eller til den pågældende afdeling, medmindre der er givet godkendelse via arbejdsgangen for den pågældende type budgetkontopost.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Bruge arbejdsområder og forespørgselssider til at spore budget vs. faktiske tal
Budgetadministratoren kan gennemgå den aktuelle tilstand for et budget i arbejdsområdet **Finansbudgetter og budgetter**. Fanerne **Udgifter over budget** og **Omsætning under budget** giver et hurtigt overblik over de økonomiske dimensionskombinationer, hvor budgetmål ikke opfyldes eller nærmer sig grænsen. Du kan tilpasse budgettærskelprocent og økonomiske dimensionssæt, der bruges på disse faner ved at klikke på **Konfigurer mit arbejdsområde**. Du kan klikke på **Afdelingsledere** for at se de arbejdere, der er ansvarlige for bestemte økonomiske dimensionskombinationer, der er valgt under disse faner. Hvis du f.eks. kan se, at driftsafdelingens udgiftsbudget overskrider budgettærsklen, kan du nemt finde og kontakte driftsafdelingens leder for at diskutere problemet. 

> [!NOTE] 
> Den **afdelingsleder** på den **organisationsenheder** side afgør, hvilke managers understøtter bestemte økonomiske dimensionskombinationer. Klik på **Se mere** nederst på fanen for at åbne forespørgselssiden **Budget vs. faktiske tal** for at få yderligere oplysninger om budgetbeløb versus faktiske beløb. 

Forespørgselssiden **Faktisk vs. budget** giver dig mulighed for at dykke ned i detaljer om budget versus faktiske beløb. Vælg en linje på forespørgselssiden, og klik derefter på **Periodesaldi,** for at se budgettet og faktiske beløb, der er spredt over regnskabsperioder. Siden **Budgetkontoposter** indeholder detaljeadgang til detaljerne i budgetbeløbet i budgetregisterposter. Siden **Finanskladdeposter **åbner de finansposteringer, der er inkluderet i det beregnede **faktiske** beløb. 

En virksomhed, der bruger budgetplanlægningsfunktionen kan oprette og bruge *budgetprognoser *i arbejdsområdet **Finansbudgetter og budgetter**.


