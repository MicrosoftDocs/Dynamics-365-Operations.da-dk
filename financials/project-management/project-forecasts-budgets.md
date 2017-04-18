---
title: Projektprognoser og budgetter
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 9577a7058986d200073d66a5824fbba29efa5125
ms.lasthandoff: 03/31/2017


---

# <a name="project-forecasts-and-budgets"></a>Projektprognoser og budgetter



Microsoft Dynamics 365 for operationer er der to måder at administrere og styre dine projekter: projekt prognoser og projekt budgetter. 

Brug projektprognoser, hvis organisationen har et operationelt perspektiv, og hvis den fokuserer på indtægter og omkostninger, der er udledt af specifikke transaktioner. Brug projektbudgettering, hvis organisationen fokuserer mere på økonomiske beløb. 

Prognosemodeller anvendes i både projektprognoser og projektbudgetter til at rumme de budgetterede transaktionsbeløb. 

Hver metode har sine fordele. Du bør overveje følgende punkter, før du vælger en metode til din organisation.

|                           |                                                                                                                                                                                                                                                         |                                                                                                                                                                         |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                           | **Projektprognoser **                                                                                                                                                                                                                                 | **Projektbudgetter **                                                                                                                                                   |
| **Periodefordeling **     | Du kan ikke eksplicit fordele transaktioner på en regnskabsperiode. Prognosen og styringen af den er i stedet baseret på projektets levetid. Da prognoser er baseret på en bestemt dato, skal du derfor udlede perioden fra datoen. | Du kan fordele transaktioner på hele projektet eller på en regnskabsperiode. Hvis du fordeler hen over en periode, kan du overføre ikke-anvendte beløb til næste regnskabsperiode. |
| **Se transaktioner**  | Du kan få vist transaktioner i prognoseformularer, hvor du får vist prognoserne for hele firmaet og for alle projekter uanset hierarki. Hvis du vil fokusere på et bestemt projekt, skal du filtrere dataene.                                       | Du kan få vist budgetterede transaktioner for et enkelt projekthierarki. Du kan derfor få vist detaljer om transaktioner for et overordnet projekt eller dets underprojekter.                 |
| **Transaktionsvariabler ** | Når du angiver prognosetransaktioner, kan du bruge hver attribut, der findes til en faktisk transaktion: Det giver mulighed for større detaljering i prognosen. Du kan f.eks. angive detaljer vedrørende antal, arbejdere, varer eller linjeegenskaber.         | Når du angiver budgetoplysninger, kan du kun indtaste beløb, kategorier og aktiviteter.                                                                                    |
| **Sikkerhed **              | Prognoser er baseret på transaktioner, du indtaster i prognoseformularerne og involverer ingen mekanisme til processtyring. Alle arbejdere, der har tilladelser til en prognoseformular, kan revidere oplysninger uden godkendelse.                                        | Budgettering anvender arbejdsgangssystemet, som gør det muligt at anvende ændringsstyring og lader dig bevare en historik over revisionerne.                                                       |
| **Posttyper **           | Prognoseposteringer er baseret på antallet af enheder og på kost- og salgsenhedspriser.                                                                                                                                                       | Budgetoplysninger er baseret på beløb, der er fordelt på omkostninger og indtægter.                                                                                        |
| **Forecast models**       | Da hver prognose skal være tilknyttet en model, kan du oprette flere prognosemodeller, og du kan også definere undermodeller.                                                                                                                               | Projektbudgettering begrænser de prognosemodeller, der anvendes til budgettering. Færre prognosemodeller kan være med til at give øget konsistens i projektioner.                           |
| **Omkostningsoverskridelser **         | Du kan kun tillade eller forbyde indtastning af transaktioner, som vil resultere i en omkostningsoverskridelse.                                                                                                                                                                | I projektbudgettering har brugerne flere muligheder for styring. Du kan tillade advarsler og overskridelser.                                                                   |
| **Control**               | Prognosebaseret styring udføres ved brug af prognosereduktion. Faktiske beløb fratrækkes i saldi for prognoseposteringer uden noget revisionsspor. Det kan gøre det vanskeligere at spore, hvor posteringerne reelt fandt sted.                   | I projektbudgetstyring trækkes faktisk beløb fra beløb i det resterende budget. Det giver et klarere revisionsspor.                                   |

## <a name="project-forecasts"></a>Projektprognoser
Når du bruger projektprognosticering, kan du angive prognoseposteringer i prognoseforms for de enkelte posteringstyper. Alle de attributter, der er tilgængelige for en faktisk postering, kan bruges i en prognosepostering – f.eks. linjerentabilitet, linjeattributter, arbejdere eller beskrivelser. Du kan også projektere, hvor lang tid efter, at du har afholdt en omkostning, du vil fakturere en kunde. 

Projektprognosticeringsposteringer er baseret på enheder og beløb. 

Du skal tilknytte hver projektprognose med en prognosemodel. Når du angiver en prognosepostering, foreslås der automatisk en prognosemodel. Prognosemodellen fungerer som beholder for prognoseposteringerne. 

Du kan angive prognosemodeller som undermodeller til en model. På denne måde kan du anvende en prognose efter region, tidsperiode eller afdeling. Du kan kopiere prognoseposteringerne i en model for at oprette en ny model, og du kan også overføre posteringerne til finansbogholderiet. Da der er en en til en-relation mellem en prognose og en model, udgør hver prognosemodel et separat budget i et projekt. 

I prognosemodeller kan prognosereduktion bruges som styremekanisme for projekter. I prognosereduktion reduceres saldiene i prognoseposteringer med de faktiske posteringer. Da prognosereduktion anvendes på det øverste projekt i hierarkiet, giver det dog et begrænset overblik over ændringer i prognosen. Hvis en arbejder f.eks. er tilknyttet et underprojekt, bogføres de faktiske posteringer for arbejderen på det overordnede projekt. Det kan gøre det vanskeligt at spore ændringer, fordi du nemt kan fastlægge, hvilken postering i hvilket underprojekt der medførte en reduktion af prognosebeløbet. Det er derfor en god ide at oprette en kopi af en prognosemodel for den prognosereduktion, der skal bruges. Du kan derefter bruge rapporter til at se, hvad der oprindeligt blev prognosticeret. 

Du kan revidere, kopiere, slette eller overføre projektprognoser til et finansbudget. Der er dog ingen processtyring. Alle arbejdere, der har tilladelse til en prognoseformular, kan foretage revisioner uden gennemsyn.

-   ** Revidere ** – du kan ændre en prognosepostering i de forms, hvor de oprindelige poster er angivet.
-   **Kopiér eller slet** – Når du kopierer prognoseposteringer, kopierer du posteringslinjerne i én prognosemodel til en anden prognosemodel. Når du sletter en prognose, sletter du prognoseposteringerne fra en prognosemodel. Hvis du vil begrænse mængden af prognoseposteringer, der kopieres eller slettes, skal du vælge bestemte posteringstyper og -datoer. Det giver dig mulighed for at kopiere eller slette kun bestemte dele af en prognose.
-   **Overfør** – Når du overfører en projektprognose til et finansbudget, overfører du prognoseposteringerne i en prognosemodel til et finansbudget. Du kan overskrive tidligere overførte posteringer i det finansbudget, som du overfører projektprognosen til.

## <a name="project-budgets"></a>Projektbudgetter
Projektbudgettering er en mere enkel metode end projektprognosticering, selvom den er integreret med prognosemodeller. Den bruger en formular med enkeltposter for oprindelige budgetoplysninger og for revisioner og tillader projekteringer, der alene er baseret på beløb, kategori eller aktivitet. 

I projektbudgettering skal alle de oprindelige budgetter og revisioner sendes til en projektarbejdsgang til godkendelse. Arbejdsgange giver dig øget kontrol over processen og opretter en post for ændringshistorikken. 

Projektbudgettering minder om finansbudgettering, men er hurtigere og nemmere at konfigurere. Mange af indstillingerne i finansbudgettering, f.eks. nummerserier eller valuta, skal ikke konfigureres separat for projekter.

Projektbudgetter knyttes automatisk til to prognosemodeller, én for det oprindelige budget og én for det resterende budget. Derfor kan rapporter, der er baseret på prognosemodeller, bruge budgetdata. Når et projektbudget bliver bindende, oprettes budgetposteringer på basis af de tilknyttede modeller, som bruges til rapportering og kontrol.

## <a name="forecast-models"></a>Budgetmodeller
Prognosemodeller har et hierarki af enkelt lag. Det betyder, at der skal tilknyttes én projektprognose med én prognosemodel.

Hvis du bruger prognosebaseret projektbudgettering, kan du identificere modeller som undermodeller. Du kan derefter oprette prognoser efter afdeling, tidsperiode eller region. Du kan f.eks. oprette en prognosemodel for et år og derefter oprette undermodeller for regionsprognoser for Nordøst, Sydøst, Nordvest og Sydvest, som indsendes af regionale ledere. Ved at vælge forskellige indstillinger i de tilgængelige rapporter, kan du se oplysninger efter samlet prognose eller efter undermodel.

