---
title: Arbejdsgang for indkøbsrekvisitioner
description: I arbejdsgangsprocessen flyttes indkøbsrekvisitionen gennem evalueringsprocessen fra den første status Kladde til statussen Godkendt. Når en indkøbsrekvisition sendes til gennemsyn, starter arbejdsgangsprocessen. Når en indkøbsrekvisition er godkendt, kan der oprettes en indkøbsordre for indkøbsrekvisitionslinjerne, som sendes til leverandøren til ordreopfyldning.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, WorkflowParticipantExpenToken
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2234
ms.assetid: dad3ba5a-2892-45d2-874a-300896f59b34
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6069e2ab93e1ce4299669850bdae37e82b17428
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021974"
---
# <a name="purchase-requisition-workflow"></a>Arbejdsgang for indkøbsrekvisitioner

[!include [banner](../includes/banner.md)]

I arbejdsgangsprocessen flyttes indkøbsrekvisitionen gennem evalueringsprocessen fra den første status Kladde til statussen Godkendt. Når en indkøbsrekvisition sendes til gennemsyn, starter arbejdsgangsprocessen. Når en indkøbsrekvisition er godkendt, kan der oprettes en indkøbsordre for indkøbsrekvisitionslinjerne, som sendes til leverandøren til ordreopfyldning.

Før en indkøbsrekvisition kan sendes til gennemsyn, skal du konfigurere en arbejdsgang. Arbejdsgangsprocessen kan omfatte et eller flere gennemsynstrin i vilkårlig rækkefølge. Arbejdsgangsprocessen kan også konfigureres til at springe gennemsynsopgaver over, så indkøbsrekvisitionen automatisk godkendes. Du kan konfigurere, at arbejdsgangen skal omdirigere indkøbsrekvisitionen som et enkelt dokument, eller du kan omdirigere individuelle indkøbsrekvisitionslinjer til de rette validatorer. Du kan også oprette et scenario, hvor indkøbsrekvisitionen leveres som et enkelt dokument til nogle validatorer, og udvalgte indkøbsrekvisitionslinjer leveres til andre validatorer.  

Hvis indkøbsrekvisitionslinjerne gennemses enkeltvist, skal gennemsynsprocessen fuldføres for alle indkøbsrekvisitionslinjer, før arbejdsgangsprocessen kan gå til næste trin, og før gennemsynsprocessen for indkøbsrekvisitionen kan fuldføres samlet. Når gennemsynsprocessen er fuldført for indkøbsrekvisitionen og alle linjerne, opdateres indkøbsrekvisitionens overordnede status til **Godkendt**.  

Du kan konfigurere arbejdsgangen til at repræsentere forretningsprocessen for indkøbsrekvisitioner i din organisation. Når du konfigurerer din arbejdsgangsproces for indkøbsrekvisitioner, skal du overveje følgende spørgsmål:

-   Hvilke udgifter skal evalueres?
-   Hvilke udgifter kan godkendes automatisk?
-   Hvem skal evaluere og godkende udgiftsanmodninger? Hvilken rolle er disse brugere tildelt?
-   Hvilken proces skal følges, hvis der ikke er en validator til rådighed?

Følgende eksempler illustrerer to metoder, du kan bruge til at konfigurere arbejdsgange for indkøbsrekvisitioner.

## <a name="example-1-route-a-purchase-requisition-as-a-single-document-for-review"></a>Eksempel 1: Sende en indkøbsrekvisition som et enkelt dokument til gennemsyn
Følgende illustration viser, hvordan en indkøbsrekvisition kan bevæge sig gennem evalueringsprocessen i arbejdsgangen som et enkelt dokument. Linjerne på indkøbsrekvisitionen sendes ikke enkeltvist. Følgende roller er medtaget i arbejdsprocessen for dette eksempel:

-   **Anmoder** – Den bruger, der anmoder om varerne eller tjenesterne. Anmoderen kan klargøre indkøbsrekvisitionen, eller en anden arbejder kan klargøre indkøbsrekvisitionen på vegne af anmoderen. Denne arbejder kaldes klargøreren. Klargøreren er ansvarlig for at administrere indkøbsrekvisitionen i hele evalueringsprocessen. Det er kun indkøbsrekvisitionens klargører, der kan ændre den.

**Bemærk!** En arbejder skal have de relevante tilladelser for at kunne oprette en indkøbsrekvisition på vegne af en anden. Brug siden **Tilladelse til indkøbsrekvisition** til at konfigurere disse tilladelser.

-   **Indkøbsassistent** – Den bruger, der udfører en indkøbsevaluering, og som kan godkende dokumentet.
-   **Anmoderens chef** – Den bruger, der udfører en evaluering på lederniveau, og som kan godkende dokumentet.

![Gennemsynsproces for indkøbsrekvisitioner](./media/purchreqworkflowoverview_submission.gif)  
I dette eksempel omfatter arbejdsgangsprocessen for indkøbsrekvisitionen følgende trin:

1.  Klargøreren sender en indkøbsrekvisition til evaluering.
2.  Indkøberen modtager en besked. I beskeden bliver indkøberen bedt om at kontrollere oplysningerne i indkøbsrekvisitionen. Hvis der mangler påkrævede oplysninger, kan indkøberen enten tilføje dem eller returnere indkøbsrekvisitionen til klargøreren, som kan tilføje oplysningerne. Når alle de nødvendige oplysninger er udfyldt, kan indkøbsrekvisitionen flyttes til næste trin i evalueringsprocessen.
3.  Anmoderens chef evaluerer og godkender indkøbsrekvisitionen. Indkøbsrekvisitionen kan sendes til anmoderens chef, hvis f.eks. beløbet i indkøbsrekvisitionen overstiger anmoderens forbrugsgrænse for indkøbsrekvisitioner. Anmoderens chef kan godkende eller afvise indkøbsrekvisitionen eller returnere den til klargøreren for ændringer.

## <a name="example-2-route-the-individual-purchase-requisition-lines-for-review"></a>Eksempel 2: Sende de enkelte indkøbsrekvisitionslinjer til evaluering
Følgende illustration viser, hvordan de enkelte indkøbsrekvisitionslinjer kan sendes gennem en arbejdsgang. Processen for hver enkelt linje er stort set magen til processen for en indkøbsrekvisition, der betragtes som et enkelt dokument. Dog skal hver enkelt linje fuldføre arbejdsgangsprocessen, før arbejdsgangen kan fuldføres for den samlede indkøbsrekvisition.  

I dette eksempel, angiver en arbejder en anmodning om plakater og t-shirts til en marketingkampagne. Omkostningen til plakaterne deles mellem marketingafdelingen og salgsafdelingen. Hvis omkostningen for plakater og t-shirts overstiger den tilladte signeringsgrænse for afdelingsledere, skal indkøbsrekvisitionen også evalueres af gruppelederen.  

Følgende roller er medtaget i arbejdsprocessen for dette eksempel:

-   **Anmoder** – Den bruger, der anmoder om varerne eller tjenesterne. Anmoderen kan klargøre indkøbsrekvisitionen, eller en anden arbejder kan klargøre indkøbsrekvisitionen på vegne af anmoderen. Denne arbejder kaldes klargøreren. Klargøreren er ansvarlig for at administrere indkøbsrekvisitionen i hele evalueringsprocessen. Det er kun indkøbsrekvisitionens klargører, der kan ændre den.

**Bemærk!** En arbejder skal have de relevante tilladelser for at kunne oprette en indkøbsrekvisition på vegne af en anden. Brug siden **Tilladelse til indkøbsrekvisition** til at konfigurere disse tilladelser.

-   **Indkøbsassistent** – Den bruger, der udfører en indkøbsevaluering, og som kan godkende dokumentet.
-   **Anmoderens chef** – Den bruger, der udfører en evaluering på lederniveau, og som kan godkende dokumentet.
-   **Afdelingschef** – Den bruger, der udfører en udgiftskontrol, og som kan godkende dokumentet.
-   **Gruppeleder** – Den bruger, der udfører en kontrol af udskriftsmyndigheden, og som kan godkende dokumentet.

![Gennemsynsproces for indkøbsrekvisitionslinjer](./media/purchreqlineworkflowoverview.gif)  
I dette eksempel omfatter arbejdsgangsprocessen for indkøbsrekvisitionslinjer følgende trin:

1.  Klargøreren sender en indkøbsrekvisition til evaluering. Hver linje sendes til den validator, som er konfigureret til at modtage dem i arbejdsgangsprocessen.
2.  Indkøberen modtager en besked. I beskeden bliver indkøberen bedt om at kontrollere oplysningerne i indkøbsrekvisitionen og på indkøbsrekvisitionslinjerne. Alle linjer er synlige, når indkøbsrekvisitionen åbnes af indkøberen, men en visuel indikator viser, hvilke linjer der er sendt til indkøbsagenten til gennemsyn. Hvis der mangler påkrævede oplysninger, kan indkøberen enten tilføje dem eller en returnere indkøbsrekvisitionslinje til klargøreren, som kan tilføje oplysningerne. Når alle de nødvendige oplysninger er udfyldt, kan indkøbsrekvisitionslinjen flyttes til næste trin i evalueringsprocessen. Indkøbsrekvisitionslinjer kan fortsætte gennem evalueringsprocessen, uafhængigt af hinanden.
3.  Anmoderens linjechef gennemser og godkender indkøbsrekvisitionslinjerne. Godkendelsen kan sendes til anmoderens chef, hvis f.eks. beløbet i en indkøbsrekvisitionslinje overstiger anmoderens forbrugsgrænse for indkøbsrekvisitionslinjer. Chefen kan godkende eller afvise en eller begge indkøbsrekvisitionslinjer.
4.  Afdelingslederen for marketingafdelingen gennemser indkøbsrekvisitionslinjerne for både plakater og t-shirts. Afdelingschefen for salgsafdelingen gennemser kun indkøbsrekvisitionslinjen for plakaterne, fordi det er den eneste omkostning, som salgsafdelingen bliver faktureret for.
5.  Gruppelederen gennemser og godkender kun indkøbsrekvisitionslinjen for t-shirts, hvis gruppelederens godkendelse er påkrævet, fordi beløbet på indkøbsrekvisitionslinjen f.eks. overstiger afdelingslederens godkendelsesgrænse. Gruppelederen behøver ikke at godkende indkøbsrekvisitionslinjen for plakaterne.

> [!NOTE]
> Systemvalutaen skal være angivet, hvis hovedarbejdsgangen for en indkøbsrekvisition kræver godkendelser, der er relateret til signeringsgrænser.

## <a name="configuring-a-workflow-for-purchase-requisitions"></a>Konfigurere en arbejdsgang for indkøbsrekvisitioner
Hvis du skal sende en indkøbsrekvisition til gennemsyn, skal du konfigurere arbejdsgangsprocesserne for indkøbsrekvisitioner. Den arbejdsgangsproces, du definerer, styrer udvekslingen mellem den bruger, der har rekvireret varerne (anmoderen), og validatoren og godkenderen i arbejdsgangen. Ruten for indkøbsrekvisitionen afhænger af de betingelser, der er angivet i arbejdsgangskonfigurationen. Disse betingelser bestemmer f.eks., hvornår indkøbsrekvisitionen skal distribueres, den bruger eller rolle, den skal distribueres til, og de handlinger, som brugerne kan tage.  

Eksemplerne i dette emne viser en beskrivelse af, hvordan en indkøbsrekvisition kan sendes gennem en arbejdsgang som et enkelt dokument eller som individuelle indkøbsrekvisitionslinjer. Du kan også konfigurere en arbejdsgang for indkøbsrekvisitioner, der afspejler det interne kontrolgennemsyn af indkøbsrekvisitioner, som er defineret af organisationen.  

De deltagere eller validatorer, som en opgave er tildelt til i en arbejdsproces, kan være medlemmer af en bestemt brugergruppe, brugere, der har en bestemt sikkerhedsrolle, brugere, der er knyttet til afsenderen i et ledelseshierarki, eller navngivne brugere eller brugere, der har ansvar for bestemte udgifter.

### <a name="purchase-requisition-expenditure-reviewers"></a>Udgiftsvalidatorer for indkøbsrekvisitioner

Hvis du konfigurerer gennemsyn af udgifter, kan udgifter dynamisk sendes videre til gennemsyn på basis af den bruger, som er knyttet til en projektrolle eller en økonomisk dimension, hvor udgiften debiteres. Arbejdsgangen bruger den angivne projektrolle eller ejeren af den angivne økonomiske dimension til at afgøre, hvem udgiften skal sendes videre til.  

Du kan definere én eller flere konfigurationer til udgiftsvalidatorer og derefter vælge en konfiguration, mens du opretter en arbejdsgang. Du kan konfigurere udgiftsvalidatorens værdier for hver enkelt juridisk enhed i organisationen. Når du har defineret udgiftsvalidatorens konfigurationer, kan du knytte en konfiguration til din arbejdsgangsopgave.  

Du behøver ikke definere konfigurationer til en udgiftsvalidator. Du kan i stedet angive, at bestemte brugere eller brugergrupper skal fungere som validator, når du definerer arbejdsgangen. Men hvis du har en kompleks organisation, kan du effektivisere godkendelsesprocessen ved at angive udgiftsvalidatorer. Hvis du derudover angiver udgiftsvalidatorer, behøver du ikke at opdatere tildelingen af validatorer i arbejdsgangen, hver gang en validator skifter jobrolle.  

Du kan konfigurere udgiftsvalidatorer på siden **Udgiftsvalidatorer for indkøbsrekvisitioner**. Opret en konfigurationen til en udgiftsvalidator, og angiv værdier for hver af de juridiske enheder i din organisation. For indkøbsrekvisitioner, der er knyttet til et projekt, kan du angive den rolle, der er ansvarlig for validering af rekvisitionerne: projektleder, projektcontroller eller projektsalgsleder. Udgifter sendes til den bruger, der er tildelt den angivne rolle. Du kan også sende udgiften til ejeren af den økonomiske dimension ved at markere indstillingen for den relevante økonomiske dimension under fanen **Organisationsfordelinger**.  

Hvis du vil bruge en af de udgiftsvalidatorer, du har angivet i en arbejdsproces, skal du angive indstillingen **Deltagertype** til **Udgiftsdeltagere** i egenskaben **Tildeling** for det relevante arbejdsgangselement.

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Oprette en forbrugsrekvisition](tasks/create-requisition-consumption.md)

[Definition af forretningsprocesarbejdsgange for indkøbsrekvisitioner](https://www.microsoft.com/download/details.aspx?id=101821)

[Indkøbs- og forsyningsarbejdsgange](procurement-sourcing-workflows.md)

[Oversigt over indkøbsrekvisitioner](purchase-requisitions-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]