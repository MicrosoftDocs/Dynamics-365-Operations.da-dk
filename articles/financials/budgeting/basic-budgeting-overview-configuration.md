---
title: Budgetteringsoversigt
description: Næsten alle firmaer, der bruger Finans-funktionaliteten i Microsoft Dynamics 365 for Finance and Operations, skal kunne oprette rapporter over budget vs. faktiske tal. I denne artikel beskrives den minimumkonfiguration, der kræves for at oprette budgetter i Finance and Operations eller indlæse dem fra et tredjepartsprogram.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9871d41c8e0c8f05acfd6618ca537a98ab0dd71b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834265"
---
# <a name="budgeting-overview"></a>Budgetteringsoversigt 

[!include [banner](../includes/banner.md)]

Næsten alle firmaer, der bruger Finans-funktionaliteten i Microsoft Dynamics 365 for Finance and Operations, skal kunne oprette rapporter over budget vs. faktiske tal. I denne artikel beskrives den minimumkonfiguration, der kræves for at oprette budgetter i Finance and Operations eller indlæse dem fra et tredjepartsprogram.

<a name="overview"></a>Overblik
--------

Det godkendte budget for en juridisk enhed bevares i et dokument, der er kendt som en *Budgetregisterpost*. Linjerne i et budgetregisterpostdokument kaldes *budgetkonto*-poster og indeholder oplysninger om økonomiske dimensioner, datoer og beløb for det godkendte budget. Budgetregisterpostdokumentet integreres med grundlæggende økonomiske rapporter og forespørgselssider, hvor faktiske finansbeløb sammenlignes med budgetbeløb. 

Der er flere metoder til at oprette budgetregisterposter i Finance and Operations:

-   Du kan manuelt angive dokumentoplysninger på siden **Budgetregisterposter**.
-   Brug Microsoft Excel-skabelon, som du kan åbne ved at klikke på knappen **Åbn i Excel** på siden **Budgetregisterposter**.
-   Brug dataenheden **Budgetkontoposter** i Datastyring til at importere budgetregisterposter. Du bør overveje at bruge denne metode og slå parameteren **Sætbaseret** **behandling** til, når du skal importere mange budgetkontoposter i systemet.
-   Hvis firmaet bruger budgetplanlægningsfunktionen til at forberede budgetdata, kan du bruge den periodiske proces **Generér budgetregisterpost**.

Posten i budgetregisteret betragtes som afsluttet, når budgetsaldi er blevet opdateret. På siden **Budgetregisterposter** skal du klikke på **Opdater budgetsaldi** for en valgt budgetregisterpost eller flere poster. Når du har opdateret budgetsaldiene, ændres status på budgetregisterposten til **Fuldført**. Fuldført budgetregisterpost kan ikke åbnes igen til redigering. Hvis budgetdataene skal justeres, skal du derfor oprette en ny budgetregisterpost i stedet for at korrigere data i den færdige budgetregisterpost.

## <a name="configuration"></a>Konfiguration
Når du konfigurerer budgettering, skal du starte på siden **Budgetparametre**. På denne side skal du definere budgetkladden, nummerserien for budgetregisterposter og standardfunktionsmåden i arbejdsområderne.

Næste skal du oprette arbejdsgange for budgetregisterpost på siden **Arbejdsgang for budgettering**, hvis der er politikker, der styrer godkendelse af budgetregistrerposter, baseret på budgettype (for eksempel overførsler eller revisioner). Hvis der er situationer, hvor overførsler kan tillades uden godkendelse via arbejdsgang, kan du definere regler for budgetoverførsel for at understøtte disse scenarier. 

På siden **Budgetteringsdimensioner** skal du vælge de økonomiske dimensioner, der bruges til budgettering, baseret på de dimensioner, der bruges i kontoplanen. Du kan vælge blandt alle økonomiske dimensioner, eller underopsætninger til disse, til budgettering.

Definer en *budgetmodel*, der svarer til alle eller nogle af budgetterne. Du kan bruge en enkelt budgetmodel til alle budgetregisterposter. Du kan også oprette separate modeller, der er baseret på budgettypen, geografisk beliggenhed eller anden måde, som et budget kan klassificeres på. 

> [!NOTE] 
> Hvis du bruger budgetstyring, kan du kun knytte én budgetmodel til en specifik tidsperiode for budgetcyklus. 

Opret *budgetkoder*, der identificerer typen af budgetposteringer, der skal bogføres og alle relaterede arbejdsgange. Budgetkoder kan understøtte følgende budgettyper:

-   Oprindeligt budget
-   Flytning
-   Revision
-   Behæftelse
-   Budgetreservation
-   Overført budget

Med budgetkoder kan du have et revisionsspor for godkendte budgetændringer gennem hele budgetcyklussen. Hvis en arbejdsproces er tilknyttet en budgetkode, bliver arbejdsprocessen aktiveret for alle budgetregisterposter, der bruger budgetkoden, og trin i arbejdsprocessen skal være fuldført, før du posten i budgetregisteret kan nå stadiet **Fuldført**.  

Du kan eventuelt også angive *regler for budgetoverførsel*. Vælg **Brug regler for budgetoverførsler** på siden **Budgetparametre** for at bruge regler for budgetoverførsel. Når regler for budgetoverførsel bruges, opdateres budgetsaldi ikke, hvis budgetoverførselsregler overtrædes, hvis en bruger opretter et dokument ved hjælp af en budgetkode for typen **Overførsel**. Du kan f.eks. tillade budgetoverførselsdokumenter hvor udgiftsbudgettet overføres mellem hovedkonti for Salg og marketing-afdelingen, men kan forhindre budget i at blive overført fra eller til den pågældende afdeling, medmindre der er givet godkendelse via arbejdsgangen for den pågældende type budgetkontopost.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Bruge arbejdsområder og forespørgselssider til at spore budget vs. faktiske tal
Budgetadministratoren kan gennemgå den aktuelle tilstand for et budget i arbejdsområdet **Finansbudgetter og budgetter**. Fanerne **Udgifter over budget** og **Omsætning under budget** giver et hurtigt overblik over de økonomiske dimensionskombinationer, hvor budgetmål ikke opfyldes eller nærmer sig grænsen. Du kan tilpasse budgettærskelprocent og økonomiske dimensionssæt, der bruges på disse faner ved at klikke på **Konfigurer mit arbejdsområde**. Du kan klikke på **Afdelingsledere** for at se de arbejdere, der er ansvarlige for bestemte økonomiske dimensionskombinationer, der er valgt under disse faner. Hvis du f.eks. kan se, at driftsafdelingens udgiftsbudget overskrider budgettærsklen, kan du nemt finde og kontakte driftsafdelingens leder for at diskutere problemet. 

> [!NOTE] 
> Feltet **Afdelingsleder** på siden **Organisationsenheder** afgør, hvilke ledere der understøtter bestemte økonomiske dimensionskombinationer. Klik på **Se mere** nederst på fanen for at åbne forespørgselssiden **Budget vs. faktiske tal** for at få yderligere oplysninger om budgetbeløb versus faktiske beløb. 

Forespørgselssiden **Faktisk vs. budget** giver dig mulighed for at dykke ned i detaljer om budget versus faktiske beløb. Vælg en linje på forespørgselssiden, og klik derefter på **Periodesaldi,** for at se budgettet og faktiske beløb, der er spredt over regnskabsperioder. Siden **Budgetkontoposter** indeholder detaljeadgang til detaljerne i budgetbeløbet i budgetregisterposter. Siden **Finanskladdeposter** åbner de finansposteringer, der er inkluderet i det beregnede **faktiske** beløb. 

En virksomhed, der bruger budgetplanlægningsfunktionen kan oprette og bruge *budgetprognoser* i arbejdsområdet **Finansbudgetter og budgetter**.



