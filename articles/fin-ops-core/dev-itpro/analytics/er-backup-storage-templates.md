---
title: Sikkerhedskopilager til ER-skabeloner
description: I dette emne forklares det, hvordan du bruger sikkerhedskopilageret for elektroniske rapporter (ER) til genoprettelse af skabeloner.
author: NickSelin
manager: AnnBe
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 136a81e661590d7af879e816c1142de85fb72e06
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681394"
---
# <a name="backup-storage-of-er-templates"></a>Sikkerhedskopilager til ER-skabeloner

[!include [banner](../includes/banner.md)]

[Oversigten over Elektronisk rapportering (ER)](general-electronic-reporting.md) gør det muligt for erhversbrugere at konfigurere formater for udgående dokumenter i overensstemmelse med de lovgivningsmæssige krav i forskellige lande/områder. Konfigurerede ER-formater kan bruge foruddefinerede skabeloner til at oprette udgående dokumenter i forskellige formater, f.eks. Microsoft Excel-projektmapper, Microsoft Word-dokumenter eller PDF-dokumenter. Skabelonerne er fyldt med data, som det konfigurerede dataflow til genererede dokumenter kræver.

Hvert konfigureret format kan udgives som en del af en ER-løsning. Hver ER-løsning kan eksporteres fra én forekomst af Finance and Operations og importeres til en anden forekomst.

ER-strukturen bruger [Konfigurere dokumentstyring](../../fin-ops/organization-administration/configure-document-management.md) til at bevare de krævede skabeloner for den aktuelle Finance and Operations-forekomst. Afhængigt af indstillingerne for ER-strukturen kan der vælges et Microsoft Azure Blob-lager eller en Microsoft SharePoint-mappe som fysisk primær lagringslokation for skabeloner. (Yderligere oplysninger finder du under [Konfigurer den Elektroniske rapporteringsstruktur (ER)](electronic-reporting-er-configure-parameters.md).) Tabellen DocuValue indeholder en individuel post for hver skabelon. I hver post indeholder feltet **AccessInformation** stien til en skabelonfil, der er placeret på den konfigurerede lagerlokation.

Når du administrerer dine Finance and Operations-forekomster, kan du vælge at flytte den aktuelle forekomst til en anden lokation. Du kan f.eks. flytte produktionsforekomsten til et nyt sandkassemiljø. Hvis du har konfigureret ER-strukturen til at gemme skabeloner i blob-lageret, henviser DocuValue-tabellen i det nye sandkassemiljø til forekomsten af blob-lager i produktionsmiljøet. Men der er ikke adgang til denne forekomst fra sandkassemiljøet, fordi overførselsprocessen ikke understøtter overflytning af artefakter i blob-lageret. Hvis du derfor forsøger at køre et ER-format, der bruger en skabelon til at generere forretningsdokumenter, indtræffer der en undtagelse, og du får besked om den manglende skabelon. Du bliver også guidet til at bruge ER-oprydningsværktøjet til at slette og derefter importere den ER-formatkonfiguration, der indeholder skabelonen, igen. Da du kan have flere ER-formatkonfigurationer, kan denne proces være tidskrævende.

Funktionen sikkerhedskopilager for ER-skabeloner kan hjælpe dig med at oprette dine skabeloner, så de altid er tilgængelige til oprettelse af forretningsdokumenter.

> [!NOTE]
> Denne funktion kan kun bruges, når blob-lagerstedet er valgt som fysisk lagerplacering for ER-skabeloner.

## <a name="automated-recovery-and-notification"></a>Automatiseret genoprettelse og besked

I forbindelse med denne funktion gemmes hver skabelon for en ny ER-formatkonfiguration i det aktuelle miljø automatisk på sikkerhedskopiens lagerplacering for skabeloner (ERDocuDatabaseStorage-databasetabellen), når følgende hændelser indtræffer:

- Du importerer en ny ER-formatkonfiguration, der indeholder en skabelon.
- Du fuldfører kladdeversionen af en ER-formatkonfiguration, der indeholder en skabelon.

Sikkerhedskopier af skabeloner overflyttes til en ny forekomst af Finance and Operations som en del af programdatabasen.

Hvis der kræves en skabelon med et ER-format til generering af udgående dokumenter til at behandle leverandørbetalinger, herunder generering af betalingsadviseringer og kontrolrapporter, men den ønskede skabelon ikke findes på den primære lagringsplacering, indtræffer følgende hændelser:

- Hvis skabelonen er tilgængelig på lagerstedets sikkerhedskopiplacering, hentes den automatisk fra sikkerhedskopiplaceringen, gendannes til den primære lagringsplacering og bruges til den aktuelle kørsel.
- Alle brugere, der er tildelt rollen som **Udvikler til elektronisk rapportering** eller **Systemadministrator**, får besked om det manglende skabelonproblem via Handlingscenter. Den viste meddelelse afhænger af værdien i parameteren **Kør automatisk proceduren for gendannelse af de brudte skabeloner i batch**:

    - Hvis denne parameter er angivet til **Fra**, anbefaler meddelelsen, at du starter batchprocessen for automatisk at løse lignende problemer for andre ER-formatkonfigurationsskabeloner. Meddelelsen indeholder et link, som du kan bruge til at starte batchprocessen.
    - Hvis denne parameter er angivet til **Til**, giver meddelelsen dig besked om, at der er fundet et problem med manglende skabeloner, og at en ny batchproces, **Gendan brudte skabeloner fra intern databasesikkerhedskopi**, automatisk er planlagt. Denne batchproces retter automatisk lignende problemer i forbindelse med andre skabeloner.

Hvis du vil opsætte parameteren **Kør automatisk proceduren for gendannelse af de brudte skabeloner i batch**, skal du fuldføre følgende trin:

1. I Finance and Operations skal du åbne siden **Organisationsadministration \> Elektronisk rapportering \> Konfigurationer**.
2. På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
3. I dialogboksen **Brugerparametre** skal du angive den påkrævede værdi for parameteren **Kør automatisk proceduren for gendannelse af de brudte skabeloner i batch**.

> [!NOTE]
> Denne parameter er defineret som programbruger og logføres firmaspecifikt.

![Siden ER-konfigurationer](./media/GER-BackupTemplates-1.png)

I følgende illustration vises et eksempel på den meddelelse, der vises, når parameteren **Kør automatisk proceduren for gendannelse af de brudte skabeloner i batch** er angivet til **Til**.

![Siden Kreditorbetalingskladde](./media/GER-BackupTemplates-2.png)

Følgende illustration viser batchprocessen **Gendan brudte skabeloner fra intern databasesikkerhedskopi** på siden **Batchjob**.

![Siden Batchjob](./media/GER-BackupTemplates-3.png)

Udførelsesloggen for den fuldførte batchproces **Gendan brudte skabeloner fra intern databasesikkerhedskopi** indeholder oplysninger om de skabeloner, der er blevet gendannet fra sikkerhedskopiplaceringen til det primære lagringssted.

![Siden Batchjobhistorik](./media/GER-BackupTemplates-4.png)

Processen til automatisk oprettelse af sikkerhedskopier af skabeloner, der er placeret i ER-formatkonfigurationer, er som standard aktiveret. Hvis du ikke længere vil oprette sikkerhedskopier af skabeloner, skal du angive indstillingen **Stop med at oprette sikkerhedskopier af skabelon** til **Ja** under fanen **Vedhæftede filer** på siden **Parametre til elektronisk rapportering**. Du kan åbne denne side fra arbejdsområdet **Elektronisk rapportering**.

Hvis du angiver indstillingen **Stop med at oprette sikkerhedskopier af skabeloner** til **Ja** og ikke vil beholde de sikkerhedskopier, der tidligere er oprettet af skabeloner, skal du vælge **Ryd op i sikkerhedskopilager** på siden **Parametre til elektronisk rapportering**.

Hvis du har opgraderet miljøet til Finance and Operations version 10.0.5 (oktober 2019) og vil overflytte til et nyt miljø, der indeholder ER-formatkonfigurationer, der kan køres, skal du vælge **Udfyld sikkerhedskopilager** på siden **Parametre til elektronisk rapportering**, før overførslen sker. Denne knap starter processen med at tage sikkerhedskopier af alle tilgængelige skabeloner, så de kan gemmes på ER-sikkerhedskopiplaceringen for skabeloner.

![Siden Parametre til elektronisk rapportering](./media/GER-BackupTemplates-5.png)

## <a name="manual-recovery"></a>Manuel gendannelse

Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Gendan brudte skabeloner** for at starte processen med at gendanne ER-skabeloner fra sikkerhedskopiplaceringen til den primære lagerplacering. Før du starter denne proces kan du på siden **Gendan brudte skabeloner** angive, om den skal udføres interaktivt, eller om batchprocessen skal planlægges for dette.

## <a name="supported-deployments"></a>Understøttede installationer

I Finance and Operations version 10.0.5 er funktionen Sikkerhedskopilager til ER-skabeloner kun tilgængelig i skyinstallationer.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Konfigurer den Elektroniske rapporteringsstruktur (ER)](electronic-reporting-er-configure-parameters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]