---
title: Manuelt håndtere undtagelser for pluk af salgs- og flyttelinjer
description: Denne artikel beskriver, hvordan administratorer manuelt kan plukke (eller fjerne pluk) lagertransaktioner for at løse problemer, der er forårsaget af ødelagte salgs- og flytteordredata.
author: perlynne
ms.date: 08/19/2022
ms.topic: article
ms.search.form: WHSManualSalesLinePicking, WHSManualInventTransferLinePicking, InventTransPick, WHSLoadLineManualCorrection, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d2f89a7109060e69aca6a06eadaedc017728bbae
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403652"
---
# <a name="manually-handle-sales-and-transfer-line-picking-exceptions"></a>Manuelt håndtere undtagelser for pluk af salgs- og flyttelinjer

[!include [banner](../includes/banner.md)]

Manuel håndtering af plukundtagelser for salgs- og flyttelinjer sætter administratorer i stand til at løse problemer, der skyldes ødelagte salgs- og flytteordredata. Det giver betroede brugere manuelt pluk (eller fortryde) af lagerposteringer, der er relateret til salgs- og flytteordrelinjer, mens lagerprocesserne allerede er i gang.

Den funktionalitet, der er beskrevet her, skal kun bruges, hvis systemet ikke kan afslutte behandlingen af lagerstedets processer som normalt. Som standard er det kun brugere med rollen Systemadministrator, der har tilladelse til at bruge den. Du kan dog give adgang til den ved at tildele rettigheden *Vælg salgslinjer manuelt* til andre roller efter behov.

## <a name="turn-on-this-feature-for-your-system"></a>Aktivere denne funktion i dit system

Før du kan bruge en af de funktioner, der er beskrevet i denne artikel, skal de være aktiveret i systemet. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere status for disse funktioner og slå dem til. I arbejdsområdet **Funktionsstyring** vises funktionerne med følgende navne:

- *Manuel udvalgstjeneste for salgslinjer for administratorer eller lignende betroede brugere*<br>(Fra og med Supply Chain Management version 10.0.25 er denne funktion obligatorisk og kan ikke deaktiveres.)
- *Manuel udvalgstjeneste for overførselslinjer for administratorer eller lignende betroede brugere*

## <a name="correct-transactions-related-to-sales-or-transfer-order-lines"></a>Rette transaktioner, der er relateret til salgs- eller flytteordrelinjer

Benyt følgende fremgangsmåde for at rette transaktioner, der er relateret til salgs- eller flytteordrelinjer.

1. Afhængigt af den ordretype, du skal rette, skal du følge et af disse trin:

    - Hvis du vil rette en transaktion, der er relateret til en salgsordre, skal du gå til **Lagerstedsstyring \> Periodiske opgaver \> Oprydning \> Vælg salgslinjer manuelt**.
    - Hvis du vil rette en transaktion, der er relateret til en flytteordre, skal du gå til **Lagerstedsstyring \> Periodiske opgaver \> Oprydning \> Vælg overførselslinjer manuelt**.

1. Brug filtrene øverst i gitteret på siden **Vælg salgslinjer manuelt** eller **Vælg overførselslinjer manuelt** til at finde den linje, du søger efter, og vælg derefter målordrelinjen i øverste gitter.
1. Brug fanerne **Lagertransaktioner**, **Lastlinjer**, **Arbejdslinjer** og **Containerlinjer** i nederste sektion for at få vist flere oplysninger om den valgte linje. Oplysningerne under disse faner giver en grundlæggende oversigt over de relaterede lagerprocesser og statusserne for dem.
1. På siden **Pluk** for lagertransaktioner skal du i handlingsruden vælge **Pluk** for at åbne den valgte ordrelinje. Du kan tilmed udføre dette trin for ordrelinjer, der allerede er frigivet til lagerstedet. (Normalt kan ordrelinjer, der er frigivet til lagerstedet, ikke åbnes på siden **Pluk**).

    > [!NOTE]
    > Du kan få vist forskellige advarsler, når du åbner siden **Pluk**. Udfør de eventuelle handlinger, som disse advarsler anbefaler. Du kan f.eks. modtage en advarsel om ordrelinjer, der er knyttet til lagerstedsarbejde. I dette tilfælde er det en god ide at prøve at annullere arbejdet ved at bruge standardfunktionen [Annuller arbejde](cancel-warehouse-work.md), før du foretager manuel rettelse.

1. Marker linjen i gitteret **Transaktioner**, og vælg derefter **Tilføj pluklinje** på værktøjslinjen **Transaktioner**.
1. Linjen flyttes til gitteret **Pluklinjer**. Angiv passende værdier for kolonner, der mangler nødvendige oplysninger. (Angiv f.eks. den lokation og id-nummerplade, som varen skal plukkes/ikke plukkes fra).
1. Vælg **Bekræft plukning af alt** på værktøjslinjen **Pluklinjer**.

## <a name="correct-load-line-quantities"></a>Rette lastlinjeantal

Du kan bruge følgende procedure til at rette antallet på lastlinjen.

1. Afhængigt af den ordretype, du skal rette, skal du følge et af disse trin:

    - Hvis du vil rette en transaktion, der er relateret til en salgsordre, skal du gå til **Lagerstedsstyring \> Periodiske opgaver \> Oprydning \> Vælg salgslinjer manuelt**.
    - Hvis du vil rette en transaktion, der er relateret til en flytteordre, skal du gå til **Lagerstedsstyring \> Periodiske opgaver \> Oprydning \> Vælg overførselslinjer manuelt**.

1. Brug filtrene øverst i gitteret på siden **Vælg salgslinjer manuelt** eller **Vælg overførselslinjer manuelt** til at finde den linje, du søger efter, og vælg derefter målordrelinjen i øverste gitter.
1. Under fanen **Lastlinjer** i den nederste sektion skal du vælge **Korriger lastlinjer manuelt** på værktøjslinjen.
1. Gennemse de lagertransaktioner, der er relateret til den valgte lastlinje, i gitteret **Lagertransaktioner** på siden **Korriger lastlinjer manuelt**.
1. Ret antallet på lastlinjen i følgende kolonner i det øverste gitter efter behov:

    - **Mængde af oprettet arbejde**
    - **Antal, der er plukket**
    - **Planlagt antal til cross-docking**

    Systemet validerer alle ændringer, du foretager i disse kolonner.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
