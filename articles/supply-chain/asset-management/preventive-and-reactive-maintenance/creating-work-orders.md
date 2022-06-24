---
title: Oprette arbejdsordrer
description: Denne artikel beskriver, hvordan du opretter arbejdsordrer i Styring af aktiver.
author: johanhoffmann
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b1b8b3d8d83bdad2efe49bd4e878793cca6c49f4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891199"
---
# <a name="creating-work-orders"></a>Oprette arbejdsordrer

[!include [banner](../../includes/banner.md)]

Når du har planlagt præventive vedligeholdelsesjob, er næste trin at oprette arbejdsordrer til dem. Du kan udføre dette trin ved at bruge en af vedligeholdelsestidsplanerne. De planlagte job i en vedligeholdelsestidsplan kan have forskellige referencetyper som beskrevet i følgende tabel.

| Referencetype | Beskrivelse |
|---|---|
| Vedligeholdelsesplaner | Præventivee vedligeholdelsesjob, der er baseret på vedligeholdelsesplantypen *Tid* eller *Tæller*. |
| Vedligeholdelsesrunder | Præventive vedligeholdelsesjob, der indeholder flere aktiver, der kræver en lignende form for vedligeholdelse. |
| Vedligeholdelsesanmodning | En manuelt oprettet anmodning om vedligeholdelse eller reparation af et aktiv. Denne anmodning kan konverteres til en arbejdsordre. |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a>Oprette arbejdsordrer på baggrund af din vedligeholdelsestidsplan

Hvis du vil oprette arbejdsordrer, der er baseret på din vedligeholdelsestidsplan, skal du udføre følgende trin.

1. Åbn en af følgende sider, afhængigt af hvordan du vil vælge tidsplanselementer til dine arbejdsordrer:

    - Hele vedligeholdelsestidsplanen (**Aktivstyring \> Administration af tidsplaner \> Hele vedligeholdelsestidsplanen**)
    - Åbne vedligeholdelsestidsplanslinjer (**Aktivstyring \> Administration af tidsplaner \> Åbn vedligeholdelsestidsplanslinjer**)
    - Åbn vedligeholdelsestidsplanspuljer (**Aktivstyring \> Administration af tidsplaner \> Åbn vedligeholdelsestidsplanspuljer**)

1. I gitteret skal du markere afkrydsningsfeltet for alle planlagte vedligeholdelsesjob, du vil oprette en arbejdsordre for. Vælg **Arbejdsordre** i handlingsruden.

    Dialogboksen **Opret arbejdsordrer** vises. Det samlede antal budgetterede timer for de valgte linjer vises i feltet **Vedligeholdelsesprognosetimer**.

    ![Dialogboksen Opret arbejdsordrer.](media/18-preventive-maintenance.png)

1. Angiv det antal arbejdsordrer, der skal oprettes, under **Parametre**. Vælg en af følgende indstillinger:

    - **Én arbejdsordre pr. linje** – Opret én arbejdsordre pr. vedligeholdelsesplanlinje.
    - **én arbejdsordre pr.** – Opret arbejdsordrer, der er grupperet i henhold til indstillingerne for de andre indstillinger, der bliver tilgængelige, når du vælger denne indstilling.

1. Vælg den arbejdsordretype, der skal bruges til alle de arbejdsordrer, du opretter, i feltet **Arbejdsordretype**.
1. Vælg **OK** for at oprette arbejdsordrerne i overensstemmelse med indstillingerne.

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a>Gruppere arbejdsordrelinjer, som oprettes automatisk, mens vedligeholdelsesplanen køres

Denne funktion giver dig mulighed for at definere regler for gruppering af arbejdsordrelinjer under en enkelt arbejdsordre, når systemet er konfigureret til at generere arbejdsordrer automatisk på baggrund af en vedligeholdelsesplan. Tidligere kunne automatisk genererede arbejdsordrer kun indeholde én linje. Men du kan nu gruppere arbejdsordrer efter f.eks. aktiv, aktivtype eller arbejdssted. (Manuelt genererede arbejdsordrer kan allerede være grupperet på denne måde som beskrevet i forrige afsnit i denne artikel).

### <a name="enable-grouping-for-automatically-generated-work-orders"></a>Aktivere gruppering for automatisk genererede arbejdsordrer

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Aktivadministration*
- **Funktionsnavn:** *Anvende regler for gruppering af arbejdsordrer, mens en vedligeholdelsesplan køres*

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a>Konfigurere gruppering for automatisk genererede arbejdsordrer

Følg disse trin for at konfigurere gruppering for automatisk genererede arbejdsordrer.

1. Gå til **Styring af aktiver \> Opsætning \> Forebyggende vedligeholdelse \> Vedligeholdelsesplaner**.
1. Benyt følgende fremgangsmåde for hver plan, hvor du vil generere grupperede arbejdsordrer:

    1. Vælg planen i listeruden.
    1. Kontrollér, at afkrydsningsfeltet **Opret automatisk** er markeret på alle linjer i oversigtspanelet **Linjer**.

1. Gå til **Styring af aktiver \> Periodisk \> Forebyggende vedligeholdelse \> Planlæg vedligeholdelsesplaner**.
1. I dialogboksen **Planlæg vedligeholdelsesplaner** i sektionen **Periode** skal du angive tidshorisont for planen (hvor langt der skal kigges frem, når der skal søges efter planlagte vedligeholdelsesjob, der skal genereres arbejde for).
1. Angiv indstillingen **Opret arbejdsordre automatisk fra tidsplan** til *Ja*.
1. Vælg en af følgende indstillinger i sektionen **Arbejdsordre**:

    - **Én arbejdsordre pr. linje** – Opret én arbejdsordre pr. vedligeholdelsesplanlinje. (Denne indstilling giver den samme funktionalitet, som er tilgængelig, når funktionen *Anvend regler for gruppering af arbejdsordrer, mens en vedligeholdelsesplan køres* er deaktiveret).
    - **én arbejdsordre pr.** – Opret arbejdsordrer, der er grupperet i henhold til indstillingerne for de andre indstillinger, der bliver tilgængelige, når du vælger denne indstilling.

1. Hvis du ønsker, at indstillingerne skal anvendes, når du kun kører nogle af dine vedligeholdelsesplaner, skal du tilføje filtre efter behov i oversigtspanelet **Poster, der skal indgå** på samme måde som ved andre batchjob i Microsoft Dynamics 365 Supply Chain Management.
1. I oversigtspanelet **Kør i baggrunden** skal du konfigurere batch- og planlægningsindstillinger efter behov på samme måde som ved andre batchjob i Supply Chain Management.
1. Vælg **OK** for at køre og/eller planlægge de valgte vedligeholdelsesplaner.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]