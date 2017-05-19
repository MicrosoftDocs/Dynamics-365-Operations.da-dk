---
title: "Finanskladdehåndtering"
description: "I denne artikel beskrives funktionerne i Microsoft Dynamics 365 for Operations, der kan hjælpe med at gøre finanskladdebehandling lettere og være med til at sikre, at de korrekte data bliver hentet og den interne kontrol ikke bliver forringet."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c020566928cecc15bd7de504164f5adbf34eda44
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="general-journal-processing"></a>Finanskladdehåndtering

[!include[banner](../includes/banner.md)]


I denne artikel beskrives funktionerne i Microsoft Dynamics 365 for Operations, der kan hjælpe med at gøre finanskladdebehandling lettere og være med til at sikre, at de korrekte data bliver hentet og den interne kontrol ikke bliver forringet.  

Kladdenavne

Et af de vigtigste områder, der skal konfigureres, er kladdenavne. Det er en god idé at definere bestemte kladdenavne til hvert formål, såsom intern, periodiseringsregulering og fejlretning. Du kan skræddersy hvert kladdenavn for at gøre det nemt og sikkert at indtaste data til hvert formål. 

Du kan konfigurere følgende elementer på siden **Kladdenavne**:

-   **Arbejdsgangsgodkendelse** – for at øge den interne kontrol skal du definere arbejdsgange, der fastsætter materialitetsgrænser for fremgangsmåder for gennemsyn og godkendelse, baseret på kriterier såsom samlet debetbeløb. Du konfigurerer arbejdsgange for finanskladder på siden **Arbejdsgange i Finans**.
-   **Standardværdier** – vælg standardværdier for modkonti, valuta og økonomiske dimensioner.
-   **Kladdekontrol** – du kan oprette begrænsninger på regnskabs- og kontotypen samt segmentværdier. 

**Eksempler**

Et kladdenavn kan kun anvendes til reguleringer. I dette tilfælde kan du angive, at kun kontotypen **Finans** er gyldig på tværs af alle regnskaber. [![Kontotyper for kladdekontrol](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Et kladdenavn kan kun bruges til et bestemt segment eller til et interval for hovedkonti. [![Kladdekontrolsegment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

Indstillingen **Automatisk tilbageførsel** er tilgængelig i finanskladder. Du har for eksempel en periodiseringsregulering, hvor det faktiske dokuments endnu ikke er behandlet, som vist i følgende illustration.
[![Tilbageførsel af finanskladde](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Microsoft Excel-tilføjelsesprogrammet til kladdepostering giver et ekstra niveau af automatisering og gør dataindtastningen lettere. Handlingen **Åbn linjer i Excel** er tilgængelig på siden **Finanskladde** og **Kladdebilag**. 

På siden **Periodiske kladder** kan du oprette gentagelseskladder for at automatisere behandling af finanskladder. 

Du kan bruge bilagsskabeloner til enhver tid. På siden **Finanskladder** findes handlingerne **Gem** og **Vælg bilagsskabelon** på siden **Kladdebilag** under **Funktioner** for bilagslinjerne.

## <a name="related-setup"></a>Relateret opsætning
Følgende opsætning er ikke specifik for finanskladder men hjælper med at sikre, at data indtastes korrekt og nemt.

### <a name="main-account"></a>Hovedkonto

Opsætningen af hovedkontoen giver mange muligheder for behandling af finanskladden:

-   **Krav til DC/CR** – brug denne indstilling, hvis en hovedkonto er begrænset til debet- eller kredittransaktioner. Opsætningen kontrolleres, når en kladde valideres eller bogføres.
-   **Standardmodkonto**
-   **Suspenderet** – suspenderer en hovedkonto, så der ikke kan indtastes data, på tværs af alle regnskaber eller for et bestemt regnskab eller for bestemte juridiske enheder.
-   **Tillad ikke manuel angivelse** – Sørg for, at brugere ikke kan angive en værdi for kontoen manuelt i kladder.
-   **Standard/Valider valuta**
-   **Tilsidesæt juridisk enhed** – denne opsætning er specifik for det definerede regnskab eller den juridiske enhed:
    -   **Standard/Valider moms**
    -   **Standarddimension** – **Ikke fast** eller **Fast værdi**. **Fast værdi** hjælper med at sikre, at alle posteringer for denne hovedkonto altid bruger en dimensionsværdi, der er konfigureret som **fast**.
-   **Bogføringsvalidering**
    -   **Validering af bruger** – denne indstilling styrer, hvilke brugere der har tilladelse til at bogføre på en hovedkonto.
    -   **Validering af bogføringstype** – denne indstilling styrer, hvilke bogføringstyper der er tilladte for en hovedkonto.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Regnskabsmæssige strukturer og avancerede regelstrukturer

Regnskabsmæssige strukturer og avancerede regelstrukturer er meget vigtige for at garantere, at de data, der kræves til økonomisk rapportering og sporing af ydeevne er hentet under behandling af finanskladde og enhver dokumentation. Med regnskabsmæssige strukturer og avancerede regelstrukturer kan du skræddersy dataindtastningsoplevelsen. Du kan kun tillade dataindtastning for økonomiske dimensioner, der er relevante i hver situation, og kan også gennemtvinge kravet om, at obligatoriske og korrekte data altid registreres.

Du kan finde flere oplysninger under [Planlægning: Kontoplan](plan-chart-of-accounts.md). 




