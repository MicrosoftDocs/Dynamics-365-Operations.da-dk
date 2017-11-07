---
title: "Budgetplanlægningsskabeloner til Excel"
description: I dette emne beskrives, hvordan du opretter Microsoft Excel-skabeloner, der kan bruges sammen med budgetplaner.
author: ryansandness
manager: AnnBe
ms.date: 07/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cec40859a8c68cb8a9751c5531c67cef7706258
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="budget-planning-templates-for-excel"></a>Budgetplanlægningsskabeloner til Excel

[!include[banner](../includes/banner.md)]


I dette emne beskrives, hvordan du opretter Microsoft Excel-skabeloner, der kan bruges sammen med budgetplaner.

I dette emne kan du se, hvordan du opretter Excel-skabeloner, der skal bruges med budgetplaner ved hjælp af standarddemodatasæt og logon som administratorbruger. Du kan finde flere oplysninger om budgetplanlægning under [Budgetplanlægningsoversigt.](budget-planning-overview-configuration.md) Du kan også følge selvstudiet [Budgetplanlægning 101](budget-plan.md) for at lære grundlæggende principper for modulkonfiguration og -brug.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Automatisk generere et regneark ved hjælp af dokumentlayout til budgetplan

Budgetplandokumenter kan ses og redigeres ved hjælp af et eller flere layout. Hvert layout kan have en tilknyttet skabelon til et budgetplandokument for at få vist og redigere budgetplandata i et Excel-regneark. I dette emne vil der blive genereret en skabelon til et budgetplandokument ved hjælp af en eksisterende layoutkonfiguration. 

1. Åbn **listen over budgetplaner** (**Budgettering** &gt; **Budgetplaner**). 
2. Klik på **Ny** for at oprette et nyt budgetplandokument. 

  [![Budgetplanliste](./media/bpt11-1024x552.png)](./media/bpt11.png) 

3. Brug indstillingen på linjen **Tilføj** for at tilføje linjer. Klik på **Layout** for at få vist konfigurationen af dokumentlayout til budgetplan. 

  [![Budgetplantilføjelse](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Du kan gennemgå layoutkonfigurationen og justere den efter behov. 
1. Gå til **Skabelon** &gt; **Generer** for at oprette en Excel-fil for dette layout. 
2. Når skabelonen er oprettet, kan du gå til **Skabelon** &gt; **Vis** for at åbne og gennemse skabelonen til budgetplandokumentet. Du kan gemme Excel-filen til den lokale harddisk. 

[![Gem som](./media/bpt3-1024x545.png)](./media/bpt3.png)

> [!NOTE] 
> Dokumentlayout til budgetplaner kan ikke redigeres, når der er knyttet en Excel-skabelon til det. Hvis du vil ændre layoutet, skal du slette den tilknyttede Excel-skabelonfil og oprette den igen. Dette er påkrævet for at holde felterne i layoutet og regnearket synkroniseret. 

Excel-skabelonen indeholder alle elementerne fra dokumentlayoutet til budgetplanen, hvor kolonnen **Tilgængelig i regneark** er indstillet til Sand. Overlappende elementer er ikke tilladt i Excel-skabelonen. For eksempel hvis layoutet indeholder kolonner med anmodningen Første kvartal, anmodningen Andet kvartal, anmodningen Tredje kvartal og anmodningen Fjerde kvartal, og en kolonne med alle anmodninger, der repræsenterer summen af alle 4 kvartalsvise kolonner, er kun de kvartalsvise kolonner eller kolonnen med alle anmodninger tilgængelig og kan bruges i Excel-skabelonen. Excel-filen kan ikke opdatere overlappende kolonner under opdateringen, fordi dataene i tabellen bliver forældede og upræcise.

[![Eksempel](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> For at undgå potentielle problemer med visning og redigering af budgetplandata ved hjælp af Excel skal den samme bruger være logget på både Microsoft Dynamics 365 for Finance and Operations, Enterprise edition og Microsoft Dynamics Office-tilføjelsesprogrammet Dataconnector.

## <a name="add-a-header-to-budget-plan-document-template"></a>Tilføje et sidehoved til skabelon til budgetplandokument
Hvis du vil tilføje sidehovedoplysninger, skal du vælge den øverste række i Excel-filen og indsætte tomme rækker. Klik på **Design** i **Dataconnector** for at tilføje sidehovedfelter i Excel-filen.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

Under fanen **Design** skal du klikke på **Tilføj** felter og derefter vælge **BudgetPlanHeader** som enhedsdatakilden.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Peg med markøren på den ønskede placering i Excel-filen. Klik på **Tilføj etiket** for at føje feltetiketten til den valgte placering. Vælg **Tilføj værdi** for at føje værdifeltet til det valgte sted. Klik på **Udført** for at lukke designeren.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Tilføje en beregnet kolonne i skabelontabel til budgetplandokument
--------------------------------------------------------------

Derefter føjes beregnede kolonner til den genererede dokumentskabelon til budgetplanen. En **Anmodet i alt**-kolonne, som opsummerer kolonner med anmodningen Første kvartal til anmodningen Fjerde kvartal, og en **Regulering**-kolonne, der genberegner **Anmodet i alt**-kolonnen med en foruddefineret faktor.

Klik på **Design** i **Dataconnector** for at tilføje kolonner i tabellen. Klik på **Rediger** ud for **BudgetPlanWorksheet**-datakilden for at begynde at tilføje kolonner.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Den markerede feltgruppe viser de kolonner, der er tilgængelige i skabelonen. Klik på **Formel** for at tilføje en ny kolonne. Navngiv den nye kolonne, og indsæt derefter formlen i feltet **Formel**. Klik på **Opdater** for at indsætte kolonnen.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> For at definere formlen skal du oprette formlen i regnearket og derefter kopiere det til **Design** vinduet. En tabel, der er bundet til Finance and Operations, får typisk navnet "AXTable1". For at opsummere kolonnerne for anmodningen Første kvartal til anmodningen Fjerde kvartal i regnearket bruges formlen = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].

Gentag disse trin for at indsætte kolonnen **Regulering**. Brug formlen = AxTable1\[Total request\]\*$I$ 1 for denne kolonne. Dette vil tage værdien i celle I1 og multiplicere værdierne i kolonnen **Anmodet i alt** for at beregne reguleringsbeløb.

Gem og luk Excel-filen. Gå tilbage til Finance and Operations og klik i **Layout** på **Skabelon &gt; Overfør** for at overføre den gemte Excel-skabelon, der skal bruges til budgetplanen. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Luk **Layout** skyderen. Klik i dokumentet **Budgetplan** på **Regneark** for at få vist og redigere dokument i Excel. Bemærk, at den justerede Excel-skabelon, der blev brugt til at oprette dette budgetplansregneark og beregnede kolonner, opdateres ved hjælp af formler, der blev defineret i de forrige trin. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Tips og tricks til oprettelse af skabeloner for budgetplan
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Kan jeg tilføje og bruge flere datakilder til en budgetplansskabelon?

Ja, du kan bruge menuen **Design** til at føje flere enheder til det samme eller andre regneark i Excel-skabelonen. For eksempel kan du tilføje **BudgetPlanProposedProject**-datakilden for at oprette og vedligeholde en liste over foreslåede projekter på samme tid, når du arbejder med budgetplandata i Excel. Bemærk, at hvis du inkluderer store datakilder, kan det påvirke ydeevnen af Excel-projektmappen. 

Du kan bruge indstillingen **Filter** i **Dataconnector** til at føje ønskede filtre til flere datakilder.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Kan jeg skjule designindstillinger i Dataconnector for andre brugere?

Ja, åbn **Dataconnector**-indstillingerne for at skjule **Design**-indstillingen fra andre brugere.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Udvid **Indstillinger for Dataconnector**, og fjern markeringen i afkrydsningsfeltet **Aktivér design**. Derved skjules **Design** indstilling fra **Dataconnector**.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Er det muligt at forhindre brugere i ved et uheld at lukke Dataconnector, mens de arbejder med data?

Vi anbefaler at låse skabelonen for at forhindre brugere i at lukke den. Hvis du vil aktivere låsen, skal du klikke på **Dataconnector**. Der vises en pil i øverste højre hjørne. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Klik på pilen for at åbne en ekstra menu. Vælg **Lås**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Er det muligt at bruge andre Excel-funktioner, som celleformatering, farver, betinget formatering og diagrammer med mine budgetplanskabeloner?

Ja, de fleste af de almindelige Excel-funktioner fungerer i budgetplanskabeloner. Det anbefales at bruge farvekodning, så brugerne kan skelne mellem skrivebeskyttede og redigerbare kolonner. Betinget formatering kan bruges til at fremhæve problematiske områder af budgettet. Kolonnetotaler kan let vises ved hjælp af standard Excel-formler oven over tabellen.

Du kan også oprette og bruge pivottabeller og -diagrammer til supplerende grupperinger og visualiseringer af budgetdata. Under fanen **Data** i gruppen **Forbindelser** skal du klikke på **Opdater alle** og derefter klikke på **Forbindelsesegenskaber**. Klik på fanen **Anvendelse**. Under **Opdater** skal du markere afkrydsningsfeltet **Opdater data, når filen åbnes**. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)




