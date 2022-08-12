---
title: Budgetteringsoversigt
description: Næsten alle firmaer, der bruger Finans-funktionaliteten i Microsoft Dynamics 365 Finance, skal kunne oprette rapporter over budget vs. faktiske tal. I denne artikel beskrives den minimumkonfiguration, der kræves for at oprette budgetter i finans og drift eller indlæse dem fra et tredjepartsprogram.
author: panolte
ms.date: 04/29/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetParameters
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60113"
- intro-internal
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 380afc399a050215bb2d7b1e5ddb20088226f654
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068954"
---
# <a name="budgeting-overview"></a>Oversigt over budgetplanlægning

[!include [banner](../includes/banner.md)]

Næsten alle firmaer, der bruger Finans-funktionaliteten i Microsoft Dynamics 365 Finance, skal kunne oprette rapporter over budget vs. faktiske tal. I denne artikel beskrives den minimumkonfiguration, der kræves for at oprette budgetter i finans og drift eller indlæse dem fra et tredjepartsprogram.

## <a name="overview"></a>Overblik

Det godkendte budget for en juridisk enhed bevares i et dokument, der er kendt som en *Budgetregisterpost*. Linjerne i et budgetregisterpostdokument kaldes *budgetkonto*-poster og indeholder oplysninger om økonomiske dimensioner, datoer og beløb for det godkendte budget. Budgetregisterpostdokumentet integreres med grundlæggende økonomiske rapporter og forespørgselssider, hvor faktiske finansbeløb sammenlignes med budgetbeløb. 

Der er flere metoder til at oprette budgetregisterposter:

-   Du kan manuelt angive dokumentoplysninger på siden **Budgetregisterposter**.
-   Brug Microsoft Excel-skabelon, som du kan åbne ved at klikke på knappen **Åbn i Excel** på siden **Budgetregisterposter**.
-   Brug dataenheden **Budgetkontoposter** i Datastyring til at importere budgetregisterposter. Du bør overveje at bruge denne metode og slå parameteren **Sætbaseret behandling** til, når du skal importere mange budgetkontoposter i systemet.
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

Funktioner, der blev introduceret i Microsoft Dynamics 365 Finance version 10.0.7 (januar 2020), gav ekstra kapacitet og fleksibilitet for budgetregisterposter. Hvis du vil aktivere disse forbedringer, skal du gå til arbejdsområdet **Administration af funktioner** og vælge **Kun budgetregisterposter for antal** og/eller **Budgetregisterposter med beløbstype som standard**.

Du kan bruge funktionen **Kun budgetregisterposter for antal**, hvis du kun vil bogføre en budgetregisterpost med beløb, der kun er antal. Du kan f.eks. bogføre en budgetpost med et antal på 32 og en pris på nul, hvilket giver et beløb på nul. Du kan derefter bruge dette antal inden for rammerne af en økonomisk rapport til at bestemme en pris pr. antal. Bemærk, at ingen forespørgsler eller rapporter er opdateret som en del af denne funktion. Med funktionen kan du kun bogføre et beløb på nul.

Med **Budgetregisterposter med beløbstype som standard**-funktionen kan standardbeløbstypen i en budgetregisterpost være en anden beløbstype end udgift. Postlinjen i budgetregisteret vil nu som standard være udgift, når hovedkontotypen er udgift, den vil som standard være omsætning, når hovedkontotypen er omsætning, og den vil som standard være udgift for alle andre kontotyper.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Bruge arbejdsområder og forespørgselssider til at spore budget vs. faktiske tal
Budgetadministratoren kan gennemgå den aktuelle tilstand for et budget i arbejdsområdet **Finansbudgetter og budgetter**. Fanerne **Udgifter over budget** og **Omsætning under budget** giver et hurtigt overblik over de økonomiske dimensionskombinationer, hvor budgetmål ikke opfyldes eller nærmer sig grænsen. Du kan tilpasse budgettærskelprocent og økonomiske dimensionssæt, der bruges på disse faner ved at klikke på **Konfigurer mit arbejdsområde**. Du kan klikke på **Afdelingsledere** for at se de arbejdere, der er ansvarlige for bestemte økonomiske dimensionskombinationer, der er valgt under disse faner. Hvis du f.eks. kan se, at driftsafdelingens udgiftsbudget overskrider budgettærsklen, kan du nemt finde og kontakte driftsafdelingens leder for at diskutere problemet. 

> [!NOTE] 
> Feltet **Afdelingsleder** på siden **Organisationsenheder** afgør, hvilke ledere der understøtter bestemte økonomiske dimensionskombinationer. Klik på **Se mere** nederst på fanen for at åbne forespørgselssiden **Budget vs. faktiske tal** for at få yderligere oplysninger om budgetbeløb versus faktiske beløb. 

Forespørgselssiden **Faktisk vs. budget** giver dig mulighed for at dykke ned i detaljer om budget versus faktiske beløb. Vælg en linje på forespørgselssiden, og klik derefter på **Periodesaldi,** for at se budgettet og faktiske beløb, der er spredt over regnskabsperioder. Siden **Budgetkontoposter** indeholder detaljeadgang til detaljerne i budgetbeløbet i budgetregisterposter. Siden **Finanskladdeposter** åbner de finansposteringer, der er inkluderet i det beregnede **faktiske** beløb. 

En virksomhed, der bruger budgetplanlægningsfunktionen kan oprette og bruge *budgetprognoser* i arbejdsområdet **Finansbudgetter og budgetter**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

