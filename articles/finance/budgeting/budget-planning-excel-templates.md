---
title: Budgetplanlægningsskabeloner til Excel
description: Denne artikel beskriver, hvordan du kan oprette Microsoft Excel-skabeloner, der kan bruges sammen med budgetplaner.
author: panolte
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: kfend
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8996ad5d03327b9273be7860a3905dc25efa7e90
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070658"
---
# <a name="budget-planning-templates-for-excel"></a>Budgetplanlægningsskabeloner til Excel

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du kan oprette Microsoft Excel-skabeloner, der kan bruges sammen med budgetplaner.

Denne artikel viser, hvordan du opretter Excel-skabeloner, der skal bruges med budgetplaner ved hjælp af standarddemodatasæt og logon som administratorbruger. Du kan finde flere oplysninger om budgetplanlægning under [Budgetplanlægningsoversigt](budget-planning-overview-configuration.md). Du kan også følge selvstudiet [Budgetplanlægning](budget-plan.md) for at lære grundlæggende principper for modulkonfiguration og -brug.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Automatisk generere et regneark ved hjælp af dokumentlayout til budgetplan

Budgetplandokumenter kan ses og redigeres ved hjælp af et eller flere layout. Hvert layout kan have en tilknyttet skabelon til et budgetplandokument for at få vist og redigere budgetplandata i et Excel-regneark. I denne artikel vil der blive genereret en skabelon til et budgetplandokument ved hjælp af en eksisterende layoutkonfiguration. 

1. Åbn **listen over budgetplaner** (**Budgettering** &gt; **Budgetplaner**). 
2. Klik på **Ny** for at oprette et nyt budgetplandokument. 

   [![Budgetplanliste.](./media/bpt11-1024x552.png)](./media/bpt11.png) 

3. Brug indstillingen på linjen **Tilføj** for at tilføje linjer. Klik på **Layout** for at få vist konfigurationen af dokumentlayout til budgetplan. 

   [![Budgetplantilføjelse.](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Du kan gennemgå layoutkonfigurationen og justere den efter behov. 
1. Gå til **Skabelon** &gt; **Generer** for at oprette en Excel-fil for dette layout. 
2. Når skabelonen er oprettet, kan du gå til **Skabelon** &gt; **Vis** for at åbne og gennemse skabelonen til budgetplandokumentet. Du kan gemme Excel-filen til den lokale harddisk. 

[![Gem som.](./media/bpt3-1024x545.png)](./media/bpt3.png)

> [!NOTE] 
> Dokumentlayout til budgetplaner kan ikke redigeres, når der er knyttet en Excel-skabelon til det. Hvis du vil ændre layoutet, skal du slette den tilknyttede Excel-skabelonfil og oprette den igen. Dette er påkrævet for at holde felterne i layoutet og regnearket synkroniseret. 

Excel-skabelonen indeholder alle elementerne fra dokumentlayoutet til budgetplanen, hvor kolonnen **Tilgængelig i regneark** er indstillet til Sand. Overlappende elementer er ikke tilladt i Excel-skabelonen. For eksempel hvis layoutet indeholder kolonner med anmodningen Første kvartal, anmodningen Andet kvartal, anmodningen Tredje kvartal og anmodningen Fjerde kvartal, og en kolonne med alle anmodninger, der repræsenterer summen af alle 4 kvartalsvise kolonner, er kun de kvartalsvise kolonner eller kolonnen med alle anmodninger tilgængelig og kan bruges i Excel-skabelonen. Excel-filen kan ikke opdatere overlappende kolonner under opdateringen, fordi dataene i tabellen bliver forældede og upræcise.

> [!NOTE] 
> For at undgå potentielle problemer med visning og redigering af budgetplandata ved hjælp af Excel skal den samme bruger være logget på både Microsoft Dynamics 365 Finance og Microsoft Dynamics Office-tilføjelsesprogrammet Dataconnector.

## <a name="add-a-header-to-budget-plan-document-template"></a>Tilføje et sidehoved til skabelon til budgetplandokument
Hvis du vil tilføje sidehovedoplysninger, skal du vælge den øverste række i Excel-filen og indsætte tomme rækker. Klik på **Design** i **Dataconnector** for at tilføje sidehovedfelter i Excel-filen.

Under fanen **Design** skal du klikke på **Tilføj** felter og derefter vælge **BudgetPlanHeader** som enhedsdatakilden.

Peg med markøren på den ønskede placering i Excel-filen. Klik på **Tilføj etiket** for at føje feltetiketten til den valgte placering. Vælg **Tilføj værdi** for at føje værdifeltet til det valgte sted. Klik på **Udført** for at lukke designeren.

## <a name="select-add-valuemediabpt7png"></a>[![Vælg Tilføj Værdi.](./media/bpt7.png)](./media/bpt7.png)

## <a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Tilføje en beregnet kolonne i skabelontabel til budgetplandokument

Derefter føjes beregnede kolonner til den genererede dokumentskabelon til budgetplanen. En **Anmodet i alt**-kolonne, som opsummerer kolonner med anmodningen Første kvartal til anmodningen Fjerde kvartal, og en **Regulering**-kolonne, der genberegner **Anmodet i alt**-kolonnen med en foruddefineret faktor.

Klik på **Design** i **Dataconnector** for at tilføje kolonner i tabellen. Klik på **Rediger** ud for **BudgetPlanWorksheet**-datakilden for at begynde at tilføje kolonner.

[![Begynd med at tilføje kolonner.](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Den markerede feltgruppe viser de kolonner, der er tilgængelige i skabelonen. Klik på **Formel** for at tilføje en ny kolonne. Navngiv den nye kolonne, og indsæt derefter formlen i feltet **Formel**. Klik på **Opdater** for at indsætte kolonnen.

[![Tilføj og indsæt kolonne.](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> For at definere formlen skal du oprette formlen i regnearket og derefter kopiere det til **Design** vinduet. En tabel, der er bundet til finans og drift, får typisk navnet "AXTable1". For at opsummere kolonnerne for anmodningen Første kvartal til anmodningen Fjerde kvartal i regnearket bruges formlen = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].

Gentag disse trin for at indsætte kolonnen **Regulering**. Brug formlen = AxTable1\[Total request\]\*$I$ 1 for denne kolonne. Dette vil tage værdien i celle I1 og multiplicere værdierne i kolonnen **Anmodet i alt** for at beregne reguleringsbeløb.

Gem og luk Excel-filen. Klik i **Layout** på **Skabelon &gt; Overfør** for at uploade den gemte Excel-skabelon, der skal bruges til budgetplanen. 

[![Overfør Excel-skabelon.](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Luk **Layout** skyderen. Klik i dokumentet **Budgetplan** på **Regneark** for at få vist og redigere dokument i Excel. Bemærk, at den justerede Excel-skabelon, der blev brugt til at oprette dette budgetplansregneark og beregnede kolonner, opdateres ved hjælp af formler, der blev defineret i de forrige trin. 

[![Få vist og rediger dokument i Excel.](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Tips og tricks til oprettelse af skabeloner for budgetplan
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Kan jeg tilføje og bruge flere datakilder til en budgetplansskabelon?

Ja, du kan bruge menuen **Design** til at føje flere enheder til det samme eller andre regneark i Excel-skabelonen. For eksempel kan du tilføje **BudgetPlanProposedProject**-datakilden for at oprette og vedligeholde en liste over foreslåede projekter på samme tid, når du arbejder med budgetplandata i Excel. Bemærk, at hvis du inkluderer store datakilder, kan det påvirke ydeevnen af Excel-projektmappen. 

Du kan bruge indstillingen **Filter** i **Dataconnector** til at føje ønskede filtre til flere datakilder.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Kan jeg skjule designindstillinger i Dataconnector for andre brugere?

Ja, åbn **Dataconnector**-indstillingerne for at skjule **Design**-indstillingen fra andre brugere.

[![Indstillinger for Åbn Data Connector.](./media/bpt13-1024x565.png)](./media/bpt13.png)

Udvid **Indstillinger for Dataconnector**, og fjern markeringen i afkrydsningsfeltet **Aktivér design**. Derved skjules **Design** indstilling fra **Dataconnector**.

[![Skjul indstillingen Design fra Data Connector.](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Er det muligt at forhindre brugere i ved et uheld at lukke Dataconnector, mens de arbejder med data?

Vi anbefaler at låse skabelonen for at forhindre brugere i at lukke den. Hvis du vil aktivere låsen, skal du klikke på **Dataconnector**. Der vises en pil i øverste højre hjørne. 

[![Aktiver låsen.](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Klik på pilen for at åbne en ekstra menu. Vælg **Lås**.

### <a name="select-lockmediabpt16png"></a>[![Vælg Lås.](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Er det muligt at bruge andre Excel-funktioner, som celleformatering, farver, betinget formatering og diagrammer med mine budgetplanskabeloner?

Ja, de fleste af de almindelige Excel-funktioner fungerer i budgetplanskabeloner. Det anbefales at bruge farvekodning, så brugerne kan skelne mellem skrivebeskyttede og redigerbare kolonner. Betinget formatering kan bruges til at fremhæve problematiske områder af budgettet. Kolonnetotaler kan let vises ved hjælp af standard Excel-formler oven over tabellen.

Du kan også oprette og bruge pivottabeller og -diagrammer til supplerende grupperinger og visualiseringer af budgetdata. Under fanen **Data** i gruppen **Forbindelser** skal du klikke på **Opdater alle** og derefter klikke på **Forbindelsesegenskaber**. Klik på fanen **Anvendelse**. Under **Opdater** skal du markere afkrydsningsfeltet **Opdater data, når filen åbnes**. 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

