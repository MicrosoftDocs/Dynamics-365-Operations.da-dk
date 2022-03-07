---
title: Arbejdsprocesser for godkendelse af lagerkladder
description: I dette emne beskrives det, hvordan du kan konfigurere og bruge arbejdsprocesser for godkendelse af lagerkladder til forskellige typer fysiske lagertransaktioner. Arbejdsprocesser for lagerkladder sikrer, at kun godkendte lagerkladder kan bogføres på transaktioner.
author: sherry-zheng
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTableWorkflowDropDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-21
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b53ecec4bb7593cb0a0cae72e4132c49d6ec6a68
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826005"
---
# <a name="inventory-journal-approval-workflows"></a>Arbejdsprocesser for godkendelse af lagerkladder

[!include [banner](../includes/banner.md)]

I dette emne beskrives det, hvordan du kan konfigurere og bruge arbejdsprocesser for godkendelse af lagerkladder til forskellige typer fysiske lagertransaktioner som f.eks. afgange og tilgange, lagerbevægelser, styklister og afstemning af det fysiske lager. Arbejdsprocesser for lagerkladder sikrer, at kun godkendte lagerkladder kan bogføres på transaktioner.

> [!NOTE]
> Godkendelsesarbejdsprocesser for lagerkladder gælder kun for transaktioner, der er registreret ved hjælp af modulet Lagerstyring. De fungerer ikke med de lagerkladder, der udløses fra modulet Lokationsstyring.

## <a name="turn-on-the-inventory-journal-approval-workflows-feature"></a>Aktivere funktionen til arbejdsgange for godkendelse af lagerkladde

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Under Lager- og lokationsstyring*
- **Funktionsnavn:** *Arbejdsgang til godkendelse af lagerkladder*

## <a name="create-your-inventory-journal-approval-workflows"></a>Oprette dine arbejdsprocesser for godkendelse af lagerkladder

Hvis du vil konfigurere denne funktion, skal du oprette en arbejdsproces for hver af de lagerkladdetyper, du vil kontrollere. Da forskellige lagerkladdetyper kan have forskellige godkendelseshierarkier og arbejdsprocestrin, kan du konfigurere individuelle arbejdsprocesser for de enkelte lagerkladdetyper.

Arbejdsprocesser understøtter versionskontrol, og de har hver især et arbejdsproces-id og en aktiv version. Du kan vælge at aktivere hver ny arbejdsprocesversion umiddelbart efter oprettelsen eller holde den inaktiv. Hvis du har brug for flere arbejdsprocesser for den samme kladdetype, skal du oprette flere arbejdsprocesser for kladdetypen og derefter knytte hver af disse til et andet kladdenavn, der bruger den pågældende type.

Sådan opretter du dine arbejdsprocesser for godkendelse af lagerkladder:

1. Gå til **Lagerstyring \> Konfiguration\> Arbejdsprocesser for lagerstyring**.
1. Vælg **Ny** i handlingsrude.
1. Vælg den lagerkladdetype, som du vil konfigurere en arbejdsproces for:
    - **Lagermærkatoptællingskladde**
    - **Ændringskladde for beholdningsejerskab**
    - **Lagerbevægelseskladde**
    - **Lageroverførselskladde**
    - **Lageroptællingskladde**
    - **Lagerkladde for stykliste**
    - **Lagerreguleringskladde**

    ![Dialogboksen Opret arbejdsproces](media/journal-workflow-create-workflow.png "Dialogboksen Opret arbejdsproces")

1. Appen med arbejdsproceseditor starter på din computer. (Du kan blive bedt om at godkende denne handling). Brug den til at designe arbejdsprocessen efter behov. Du kan finde flere oplysninger om, hvordan du bruger arbejdsproceseditoren, under [Oversigt i arbejdsprocessystem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).
1. Når du har gemt og lukket arbejdsproceseditorens app, skal du vælge, om denne arbejdsprocesversion skal aktiveres, eller om den skal forblive inaktiv.

> [!NOTE]
> Arbejdsprocesser giver versionskontrol, hvilket betyder, at du kan få vist en liste over versioner, du har oprettet, og vælge, hvilken der er aktiv. Hvis du vil have vist listen over tilgængelige versioner og vælge, hvilken der skal aktiveres, skal du vælge en arbejdsproces på siden **Arbejdsprocesser for lagerstyring**. Åbn fanen **Arbejdsproces** i handlingsruden , og vælg **Versioner**. Der kan kun være én aktiv version ad gangen for hvert arbejdsproces-id.

## <a name="assign-approval-workflows-to-inventory-journal-names"></a>Tildele lagerkladdenavne arbejdsprocesser for godkendelse

Det næste trin er at tildele hvert lagerkladdenavn en lagerkladdearbejdsproces. Du kan konfigurere flere lagerkladdenavne for hver lagerkladdetype.

Sådan knytter du en lagerkladdearbejdsproces til et lagerkladdenavn:

1. Gå til **Lagerstyring \> Konfiguration \> Kladdenavne \> Lager**.
1. Vælg et kladdenavn i listekolonnen for at åbne siden Indstillinger.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Godkendelsesarbejdsgang** til **Ja**. Vælg **Ja**, hvis du bliver bedt om at godkende handlingen.

    ![Tildele et kladdenavn en arbejdsproces](media/journal-workflow-journal-name.png "Tildele et kladdenavn en arbejdsproces")

1. Åbn rullelisten **Arbejdsproces**, og vælg den ønskede arbejdsproces. På listen vises de aktive arbejdsprocesser, du har oprettet ved hjælp af arbejdsproceseditorens app.

## <a name="create-an-inventory-journal-and-send-it-for-approval"></a>Oprette en lagerkladde og sende den til godkendelse

Når du har knyttet et lagerkladdenavn til den tilsvarende arbejdsproces for lagerkladdegodkendelse, vil du kunne oprette nye lagerkladder, der bruger det pågældende navn, og derefter sende disse kladder til godkendelse ved hjælp af den pågældende arbejdsproces. Du kan ikke bogføre lagerkladden, før den er godkendt af de godkendere, der er konfigureret i arbejdsprocessen.

1. Udvid i navigationsruden **Lagerstyring \> Kladdeposteringer \> Varer**, og vælg derefter en lagerkladdetype.
1. Vælg **Ny** for at oprette en ny kladde af den valgte type.
1. Dialogboksen **Opret lagerkladde** åbnes. Udfyld formularen efter behov, og vælg derefter **OK** for at gemme kladden.
1. Fuldfør kladden efter behov.
1. Når du opretter eller åbner en lagerkladde med en tilknyttet godkendelsesarbejdsproces, vil knappen **Arbejdsproces** være aktiv i handlingsruden. Når du er klar til at sende kladden til godkendelse, skal du vælge knappen **Arbejdsproces** for at åbne en rulleliste og derefter vælge **Send**. Godkendelsesanmodningen sendes til den relevante godkender, som vil blive påmindet ved hjælp af den beskedmetode, der er konfigureret for arbejdsprocessen.

    ![Sende en kladde til godkendelse](media/journal-workflow-inventory-journal.png "Sende en kladde til godkendelse")

Hvis du vil tilbagekalde en godkendelsesanmodning, skal du åbne den relevante kladde, vælge knappen **Arbejdsproces** og derefter vælge **Tilbagekald**. Dette vil nulstille arbejdsprocessen.

Når kladden er blevet godkendt, kan du bogføre den. Vælg **Bogfør** i handlingsruden for at bogføre kladden. Hvis knappen **Bogfør** ikke er aktiveret, er kladden ikke godkendt endnu.

## <a name="respond-to-an-inventory-journal-approval-request"></a>Besvare en anmodning om lagerkladdegodkendelse

Hvis du er godkender, skal du modtage en meddelelse, hver gang din godkendelse er nødvendig (som konfigureret i den relevante arbejdsproces). Du kan derefter godkende eller afvise en anmodning om kladdegodkendelse ved at benytte følgende fremgangsmåde:

1. Udvid i navigationsruden **Lagerstyring \> Kladdeposteringer \> Varer**, og vælg derefter en lagerkladdetype.
1. Åbn den relevante kladde, og gennemse den.
1. Vælg knappen **Arbejdsproces** i handlingsruden for at åbne en rulleliste i en dialogboks. Vælg en af følgende indstillinger:
    - **Godkend** for at godkende anmodningen.
    - **Afvis** for at afvise anmodningen.
    - **Flere \> Anmod om ændring** for at sende en meddelelse til anmoderen, der beder dem om at ændre noget bestemt og derefter sende igen.
    - **Flere \> Stedfortræder** for at delegere godkendelsen til en anden bruger.
    - **Flere \> Tilbagekald** for at tilbagekalde godkendelsesanmodningen (nulstiller arbejdsprocessen).
    - **Flere \> Arbejdsgangshistorik** for at få vist historikken for denne godkendelsesarbejdsproces indtil nu.

## <a name="review-the-approval-history"></a>Gennemse godkendelseshistorikken

Som med andre typer arbejdsgange kan du bruge siden **Arbejdsgangshistorik** til at få vist historikken over godkendelsesarbejdsgangen for en hvilken som helst kladde.

Sådan gennemgår du arbejdsgangshistorikken for en kladde:

1. Udvid i navigationsruden **Lagerstyring \> Kladdeposteringer \> Varer**, og vælg derefter en lagerkladdetype.
1. Åbn den relevante kladde.
1. Vælg knappen **Arbejdsproces** i handlingsruden for at åbne en rulleliste i en dialogboks. Vælg **Arbejdsgangshistorik**. Du kan finde flere oplysninger under [Vise arbejdsgangshistorik](../../fin-ops-core/fin-ops/organization-administration/tasks/view-workflow-history.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]