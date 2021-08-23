---
title: Finanskladdehåndtering
description: I dette emne beskrives funktionerne i Microsoft Dynamics 365 Finance, der kan hjælpe med at gøre finanskladdebehandling lettere og være med til at sikre, at de korrekte data bliver hentet, og den interne kontrol ikke bliver forringet.
author: ShylaThompson
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7e9c8981968cbe36070c336d57f0b086b9ab930d0287d11faaeb0f32ee46364
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742873"
---
# <a name="general-journal-processing"></a>Finanskladdehåndtering

[!include [banner](../includes/banner.md)]

I dette emne beskrives de funktioner, der kan hjælpe med at gøre finanskladdebehandling lettere og være med til at sikre, at de korrekte data bliver hentet, og den interne kontrol ikke bliver forringet.  

## <a name="journal-names"></a>Kladdenavne

Et af de vigtigste områder, der skal konfigureres, er kladdenavne. Det er en god idé at definere bestemte kladdenavne til hvert formål, såsom intern, periodiseringsregulering og fejlretning. Du kan skræddersy hvert kladdenavn for at gøre det nemt og sikkert at indtaste data til hvert formål. 

Du kan konfigurere følgende elementer på siden **Kladdenavne**:

-   **Arbejdsgangsgodkendelse** – for at øge den interne kontrol skal du definere arbejdsgange, der fastsætter materialitetsgrænser for fremgangsmåder for gennemsyn og godkendelse, baseret på kriterier såsom samlet debetbeløb. Du konfigurerer arbejdsgange for finanskladder på siden **Arbejdsgange i Finans**.
-   **Standardværdier** – vælg standardværdier for modkonti, valuta og økonomiske dimensioner.
-   **Kladdekontrol** – du kan oprette begrænsninger på regnskabs- og kontotypen samt segmentværdier. 

**Eksempler**

Et kladdenavn kan kun anvendes til reguleringer. I dette tilfælde kan du angive, at kun kontotypen **Finans** er gyldig på tværs af alle regnskaber. 

[![Kontotyper for kladdekontrol.](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Et kladdenavn kan kun bruges til et bestemt segment eller til et interval for hovedkonti. 

[![Kladdekontrolsegment.](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

Indstillingen **Automatisk tilbageførsel** er tilgængelig i finanskladder. Du har for eksempel en periodiseringsregulering, hvor det faktiske dokuments endnu ikke er behandlet, som vist i følgende illustration.
[![Tilbageførsel af finanskladde.](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Microsoft Excel-tilføjelsesprogrammet til kladdepostering giver et ekstra niveau af automatisering og gør dataindtastningen lettere. Handlingen **Åbn linjer i Excel** er tilgængelig på siden **Finanskladde** og **Kladdebilag**. 

På siden **Periodiske kladder** kan du oprette gentagelseskladder for at automatisere behandling af finanskladder. 

Du kan bruge bilagsskabeloner til enhver tid. På siden **Finanskladder** findes handlingerne **Gem** og **Vælg bilagsskabelon** på siden **Kladdebilag** under **Funktioner** for bilagslinjerne.

## <a name="related-setup"></a>Relateret opsætning
Følgende opsætning er ikke specifik for finanskladder, men hjælper med at sikre, at data indtastes korrekt og nemt.

### <a name="main-account"></a>Hovedkonto

Opsætningen af hovedkontoen giver mange muligheder for behandling af finanskladden:

-   **Krav til DC/CR** – brug denne indstilling, hvis en hovedkonto er begrænset til debet- eller kredittransaktioner. Opsætningen kontrolleres, når en kladde valideres eller bogføres.

-   **Standardmodkonto**
-   **Suspenderet** – suspenderer en hovedkonto, så der ikke kan indtastes data, på tværs af alle regnskaber eller for et bestemt regnskab eller en bestemt juridisk enhed.
-   **Tillad ikke manuel angivelse** – Sørg for, at brugere ikke kan angive en værdi for kontoen manuelt i kladder.
-   **Standard/Valider valuta**
-   **Tilsidesæt juridisk enhed** – denne opsætning er specifik for det definerede regnskab eller den juridiske enhed:
    -   **Standard/Valider moms**
    -   **Standarddimension** – **Ikke fast** eller **Fast værdi**. **Fast værdi** hjælper med at sikre, at alle posteringer for denne hovedkonto altid bruger en dimensionsværdi, der er konfigureret som **Fast**.
-   **Bogføringsvalidering**
    -   **Validering af bruger** – denne indstilling styrer, hvilke brugere der har tilladelse til at bogføre på en hovedkonto.
    -   **Validering af bogføringstype** – denne indstilling styrer, hvilke bogføringstyper der er tilladte for en hovedkonto.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Regnskabsmæssige strukturer og avancerede regelstrukturer

Regnskabsmæssige strukturer og avancerede regelstrukturer er meget vigtige for at sikre, at de data, der kræves til økonomisk rapportering og sporing af ydeevne, er hentet under behandling af finanskladde og enhver dokumentation. Med regnskabsmæssige strukturer og avancerede regelstrukturer kan du skræddersy dataindtastningsoplevelsen. Du kan kun tillade dataindtastning for økonomiske dimensioner, der er relevante i hver situation, og kan også gennemtvinge kravet om, at obligatoriske og korrekte data altid registreres.

Du kan finde flere oplysninger under følgende emner:
- [Planlægge din kontoplan](plan-chart-of-accounts.md) 
- [Oprette avancerede regler for kladder](tasks/create-advanced-rules-journals.md)
- [Oprette en kladdepostering ved hjælp af en skabelon](tasks/create-journal-entry-template.md)
- [Oprette og kontrollere kladder](tasks/create-validate-journals.md)
- [Bogføre periodiske kladder](tasks/post-periodic-journals.md)
- [Behandle finansfordelingskladde](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a>Simuler bogføring
Du kan finde **Simuler bogføring** i menuen **Valider** til de fleste kladder. Når du validerer en kladde ved hjælp af **Valider**-funktionen, tester systemet kladden for bestemte fejlbetingelser. Hvis du bruger **Simuler bogføring**-funktionen, vil systemet køre alle de samme processer, der køres under bogføringen, uden at bogføre kladden. Du kan derefter gennemse bogføringsmeddelelser, der vises, rette eventuelle fejl og derefter åbne menuen **Bogfør** for at bogføre kladden. 

**Simuler bogføring** findes ikke til batchbehandling. Men der er kode til at simulere bogføringen i batch, og udviklere kan udvide koden, hvis de vil tilføje denne funktionalitet.  

## <a name="journal-unlock"></a>Lås kladde op
Der er en knap tilgængelig på kladdesiden til at låse en kladde op, der har status "låst af system" angivet til Ja. Denne oplåsning kan udføres af en administrator af systemet, der har analyseret udførelsen af batchjob og bekræftet, at denne kladde ikke længere behandles af et batchjob. Denne knap aktiveres af funktionen ved navn **Lås kladde op-knap** på siden **Administration af funktioner**. 

## <a name="workflow-recall"></a>Tilbagekald af arbejdsgang 
Muligheden for at tilbagekalde en kladde i en arbejdsgang, der har statussen "uoprettelig", aktiveres ved at bruge knappen **Arbejdsgang** på en kladde og på siden **Arbejdsgangshistorik**. Dette aktiveres af funktionen med navnet **Nulstilling af arbejdsgangsstatus for kladder** på siden **Administration af funktioner**.

## <a name="delete-journal-lines"></a>Slet kladdelinjer
Muligheden for at slette alle kladdelinjer hurtigt aktiveres i en kladde under **Funktioner** > **Slet kladdelinjer**. Hvis du vil aktivere denne funktion, skal du under **Administration af funktioner** vælge **Slet kladdeoptimeringer for ydeevne**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]