---
title: Planer på baggrund af tilbud og tilbudsanmodninger
description: I denne artikel beskrives, hvordan du kan konfigurere varedisponering til at tage tilbud og tilbudsanmodninger med i betragtning, når der genereres ordreforslag.
author: t-benebo
ms.date: 09/20/2022
ms.topic: article
ms.search.form: SalesQuotationListPage, ReqPlanSched, SalesQuotationTable, smmOpportunityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-20
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: eaeb3c26a562c1daebe8296b26077ee5a3223e4d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690080"
---
# <a name="plan-based-on-quotations-and-rfqs"></a>Planlægge på baggrund af tilbud og tilbudsanmodninger

[!include [banner](../../includes/banner.md)]

Tilbud og tilbudsanmodninger repræsenterer mulige eller ligefrem sandsynlige fremtidige ordrer. Derfor er det en god ide at overveje dem under varedisponering, så ekstra forsyning kan planlægges på baggrund af eksisterende tilbudsanmodninger og sandsynligheden for, at hvert enkelt tilbud bliver en faktisk ordre. I denne artikel beskrives, hvordan du kan konfigurere varedisponering til at tage tilbud og tilbudsanmodninger med i betragtning, når der genereres ordreforslag.

## <a name="set-up-master-planning-to-consider-sales-quotations-andor-rfqs"></a>Konfigurere varedisponering til at tage salgstilbud og/eller tilbudsanmodninger med i betragtning

Du kan bruge følgende procedure til at konfigurere varedisponering til at tage salgstilbud og/eller tilbudsanmodninger med i betragtning.

1. Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**.
1. Vælg en eksisterende plan i listeruden, eller vælg **Ny** i handlingsruden for at oprette en ny.
1. I oversigtspanelet **Generelt** skal du indstille følgende felter:

    - **Medtag salgstilbud** – Angiv denne indstilling til *Ja*, hvis du vil tage salgstilbud i betragtning, når den aktuelle plan køres. Angiv det til *Nej*, hvis du vil ignorere dem.
    - **Sandsynlighed %** – Angiv det minimale tillidsniveau, der kræves for, at et tilbud kan inkluderes i varedisponeringen. Beregningen af varedisponeringen medtager alle tilbud, der er oprettet ud fra salgsmuligheder, som har denne eller en højere sandsynlighedsprocent. Hvis du vil medtage alle tilbud, herunder tilbud, hvor der ikke er knyttet sandsynlighed til dem, eller som ikke har nogen salgsmulighed tilknyttet, skal du angive dette felt til *0* (nul). Du kan finde flere oplysninger om sandsynligheder for tilbud i næste afsnit.
    - **Medtag tilbudsanmodninger** – Angiv denne indstilling til *Ja*, hvis du vil tage tilbudsanmodninger i betragtning, når den aktuelle plan køres. Angiv det til *Nej*, hvis du vil ignorere dem. Hvis du vælger at overveje tilbudsanmodninger, opretter systemet indkøbsordreforslag for dem, men leverandøren angives ikke, før tilbudsanmodningen er løst. Indkøbsordreforslag, der oprettes til tilbudsanmodningerne, kan påvirke antallet i andre ordreforslag.

1. Fortsæt med at konfigurere behovsplanen på den sædvanlige måde.

## <a name="assign-and-view-probabilities-for-quotations"></a>Tildele og se sandsynligheder for tilbud

Som nævnt i det foregående afsnit vil en behovsplan kun overveje tilbud, der opfylder eller overskrider den sandsynlighedsgrænse, der er defineret for planen (hvis der er defineret en grænse). Sandsynligheden angives dog ikke direkte i hvert enkelt tilbud. Den nedarves i stedet fra den salgsmulighed, der blev brugt til at oprette tilbuddet. Derfor er der ikke knyttet en sandsynlighed til tilbud, der er oprettet direkte på siden **Alle tilbud**, eller en salgsmulighed tilknyttet, og de vil aldrig blive taget i betragtning ved varedisponering ( medmindre feltet **Sandsynlighed %** er angivet til *0* \[nul\]). Hvis der skal knyttes en sandsynlighed til den, skal der genereres et tilbud fra en salgsmulighed.

### <a name="create-a-quotation-from-an-opportunity"></a>Oprette et tilbud ud fra en salgsmulighed

Benyt følgende fremgangsmåde for at tildele en sandsynlighed til en salgsmulighed og derefter oprette et tilbud ud fra den pågældende salgsmulighed.

1. Gå til **Salg og marketing \> Relationer \> Salgsmuligheder \> Alle salgsmuligheder**.
1. Vælg **Ny** i handlingsruden for at oprette en ny salgsmulighed, eller vælg en eksisterende salgsmulighed.
1. Udfyld siden Salgsmulighed for at identificere salgsmuligheden, som du ønsker. Sørg for, at feltet **Sandsynlighed** er angivet til en passende værdi. Kun behovsplaner, der er konfigureret til at søge efter sandsynligheder for denne værdi eller højere, vil overveje tilbud, der er genereret ud fra denne salgsmulighed.
1. Vælg **Gem** i handlingsruden.
1. I gruppen **Ny** under fanen **Salgsmulighed** i handlingsruden skal du vælge **Salgstilbud** eller **Projekttilbud**, afhængigt af den type tilbud du vil oprette.
1. Angiv felterne efter behov i dialogboksen **Opret tilbud**, og vælg derefter **OK**.
1. Der oprettes og åbnes et nyt tilbud. Brug værktøjslinjen i oversigtspanelet **Linjer** til at tilføje salgslinjer eller projektlinjer efter behov for at definere indholdet af tilbuddet.
1. Vælg **Gem** i handlingsruden. Luk derefter tilbuddet.

### <a name="view-the-probability-that-is-assigned-to-a-quotation"></a>Få vist sandsynligheden, der er knyttet til et tilbud

Den eneste måde at få vist sandsynligheden for et tilbud på er at åbne den salgsmulighed, der blev brugt til at oprette tilbuddet, som beskrevet i følgende procedure.

1. Gå til **Salg og marketing \> Salgstilbud \> Alle tilbud**.
1. Hvis kolonnen **Salgsmuligheds-id** ikke vises (den er skjult i en standardinstallation), skal du følge disse trin for midlertidigt at få vist den. (Alternativt, hvis du vil beholde kolonnen **Salgsmuligheds-id** tilgængelig, skal du oprette en [gemt visning](../../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json), der indeholder den).

    1. Vælg og hold (eller højreklik på) gitterhovedet, og vælg derefter **Indsæt kolonner**.
    1. Find den række, hvor feltet **Felt** er angivet til **Salgsmulighed**, i dialogboksen *Indsæt kolonner*, og markér afkrydsningsfeltet **Vælg** for den pågældende række.
    1. Vælg **Opdater** for at føje den markerede kolonne til siden **Alle tilbud**.

1. Find rækken for det relevante tilbud i gitteret. Vælg derefter værdien for den pågældende række i kolonnen **Salgsmuligheds-id**.

    > [!NOTE]
    > Hvis du leder efter et projekttilbud, skal du måske vælge kolonneoverskriften **Tilbudstype** og rydde dens filter. I en standardinstallation angives dette filter, så det kun er salgstilbud, der vises.

1. Den relaterede salgsmulighed åbnes. Du kan nu se og redigere **Sandsynlighed**-værdien efter behov.
