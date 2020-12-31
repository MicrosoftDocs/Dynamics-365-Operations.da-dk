---
title: Importere opdaterede versioner af ER-konfigurationer
description: Dette emne forklarer, hvordan du kan importere ER-konfigurationer (elektronisk rapportering) fra det globale lager til Konfigurationstjeneste.
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 897663998c6c95ff6d7172de2abc4d4dd6ec5f12
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679504"
---
# <a name="import-updated-versions-of-er-configurations"></a>Importere opdaterede versioner af ER-konfigurationer

[!include [banner](../includes/banner.md)]

ER-[lagre](general-electronic-reporting.md#Repository) (Elektroniske rapportering) bruges til at dele [ER-konfigurationer](general-electronic-reporting.md#Configuration). Du kan [importere](download-electronic-reporting-configuration-lcs.md) ER-konfigurationer fra forskellige lagre i din forekomst af Microsoft Dynamics 365 Finance. Når du importerer ER-konfigurationer, [kan konfigurationsudbydere](general-electronic-reporting.md#Provider) udgive nye [versioner](general-electronic-reporting.md#component-versioning) af lagrene, så de kan deles.

Dette emne forklarer, hvordan du kan importere ER-fra det globale lager til Konfigurationstjeneste. Du kan finde flere oplysninger under [Microsoft Dynamics 365 for Finance and Operations – Regulatory Services, konfigurationstjeneste](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="review-the-available-updated-versions"></a>Gennemse de tilgængelige opdaterede versioner

1. Log på Finance ved hjælp af en af følgende roller:

    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

2. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
3. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Importer opdateringer af konfigurationsversioner** i sektionen **Relaterede links**.

    ![Siden Lokaliseringskonfigurationer](./media/er-download-updated-versions-global-repo1.png)

4. Gå til dialogboksen **Importer opdateringer af versioner af konfigurationer af elektronisk rapportering** og vælg **Vis kun tilgængelige opdateringer** i feltet **Kørselstilstand**. Vælg derefter **OK**. 

    ![Feltet Kørselstilstand er angivet til kun at vise tilgængelige opdateringer](./media/er-download-updated-versions-global-repo2.png)

5. Gennemse de meddelelser, du modtager. Disse meddelelser indeholder følgende oplysninger om de ER-konfigurationer i den aktuelle forekomst af Finance, og hvordan de sammenligner indholdet af det globale lager:

    - Det samlede antal ER-konfigurationer
    - ER-konfigurationer, der ikke findes i det globale lager
    - ER-konfigurationer, for hvilke den seneste version allerede er tilgængelig i den aktuelle forekomst af Finance (hvis du vil have vist den fulde liste over disse ER-konfigurationer, skal du vælge linket **Meddelelsesdetaljer**).

        ![Meddelelsen "Seneste versioner af følgende konfigurationer er allerede importeret" og meddelelsesdetaljer](./media/er-download-updated-versions-global-repo3.png)

    - ER-konfigurationer, for hvilke den seneste version allerede er tilgængelig i det globale lager og kan importeres ind i den aktuelle forekomst af Finance (hvis du vil have vist den fulde liste over disse ER-konfigurationer, skal du vælge linket **Meddelelsesdetaljer**).

        ![Meddelelsen "Tilgængelige opdateringer" og meddelelsesdetaljer](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a>Importere tilgængelige opdaterede versioner

1. Log på Finance ved hjælp af en af følgende roller:

    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

2. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
3. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Importer opdateringer af konfigurationsversioner** i sektionen **Relaterede links**.
4. Gå til dialogboksen **Importer opdateringer af versioner af konfigurationer af elektronisk rapportering** i feltet **Kørselstilstand**, vælg **Importer seneste opdateringer** for at importere de seneste versioner af ER-konfigurationer fra det globale lager i den aktuelle forekomst af Finance.
5. Hvis du vil planlægge et batchjob til importen, skal du i oversigtspanelet **Kør i baggrunden** angive indstillingen **Batchbehandling** til **Ja**. Hvis du vil gentage importen med jævne mellemrum, skal du konfigurere den nødvendige gentagelse.

    ![Feltet Kørselstilstand er angivet til Import seneste opdateringer](./media/er-download-updated-versions-global-repo5.png)

6. Vælg **OK**.
7. Du kan finde ud af, hvilke konfigurationsversioner der er importeret, ved at følge et af disse trin:

    - Hvis du kører import interaktivt i stedet for at bruge et batchjob, skal du gennemse de meddelelser, du modtager.

        ![Meddelelser, der modtages under en interaktiv importkørsel](./media/er-download-updated-versions-global-repo6.png)

    - Hvis du kører importen i batchtilstand, skal du følge disse trin:

        1. Gå til **Almindeligt** \> **Forespørgsler** \> **Batchjob** \> **Mine batchjob**.
        2. Find og vælg jobbet **Importer opdateringer af versioner af konfigurationer af elektronisk rapportering**, og klik derefter på **Batchjob** i handlingsruden, og vælg **Batchjobhistorik** for at få vist jobhistorikken.
        3. Gå til siden **Batchjobhistorik**, og vælg **Logfil**. Vælg derefter linket **Meddelelsesdetaljer** i den meddelelse, du modtager, for at få vist jobbets logfil.

        ![Joblogfil](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> Vi anbefaler ikke, at du planlægger et tilbagevendende batchjob for at importere opdaterede versioner af ER-konfigurationer direkte fra det globale lager til et produktionsmiljø, da de importerede versioner med det samme vil være tilgængelige til anvendelse. Brug i stedet denne fremgangsmåde til at implementere versioner af ER-konfigurationer til et sandkassemiljø. De kan derefter evalueres i sandkassemiljøet, før de installeres i et produktionsmiljø.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [Hente ER-konfigurationer fra det globale lager til Konfigurationstjenesten](er-download-configurations-global-repo.md)
