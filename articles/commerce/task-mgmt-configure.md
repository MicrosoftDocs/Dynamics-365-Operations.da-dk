---
title: Konfigurer opgavestyring
description: Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere funktioner til opgavestyring i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 9a4775c2dba2b9aa8e671ab6c246000303b3a37e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411145"
---
# <a name="configure-task-management"></a>Konfigurer opgavestyring

[!include [banner](includes/banner.md)]

Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere funktioner til opgavestyring i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Før Dynamics 365 Commerce-ledere og -medarbejdere kan bruge funktionerne til opgavestyring i Commerce, skal du konfigurere opgavestyring. Konfigurationstrin omfatter tildeling af rettigheder til ledere og medarbejdere, distribution af tilladelser til POS-klienter, opsætning af POS-beskeder og konfiguration af feltet **Opgave** på startsiden for et POS-program.

## <a name="configure-permissions-for-store-managers"></a>Konfigurere rettigheder for butikschefer

Alle arbejdere i en bestemt butik kan få vist alle opgaver, der er knyttet til den pågældende butik. De kan også opdatere status for de opgaver, der er tildelt til dem. Personer, f.eks. butikschefer, skal imidlertid have rettigheder til styring af opgaver for at kunne administrere de opgaver, der er tildelt til lageret, og til at oprette opgaver med et enkelt formål.

Udfør følgende trin for at konfigurere indstillinger for opgavestyring for butikschefer.

1. Gå til **Retail og Commerce \> Medarbejdere \> Rettighedsgrupper**.
1. Vælg en bestemt rettighedsgruppe (f.eks **Chef**), og vælg derefter **Rediger**.
1. Indstil **Tillad opgavestyring** til **Ja** i oversigtspanelet **Rettigheder**.
1. Tilføj handlingen **Opgavestyring** på oversigtspanelet **Beskeder**, og angiv en værdi i feltet **Visningsrækkefølge**. Skriv f.eks. **2**, hvis handlingen **Ordreopfyldelse** allerede har en værdi af **1** for **Visningsrækkefølge**.
    
> [!NOTE]
> Hvis en person, der ikke er chef, skal have tilladelse til styring af opgaver i kasseapparatet, kan du give rettigheder til den person. Du kan også oprette en ny tilladelsesgruppe for ikke-ledere og angive indstillingen **Tillad Opgavestyring** til **Ja**.

Følgende illustration viser, hvordan du konfigurerer indstillinger for opgavestyring for butikschefer.

![Konfigurere indstillinger for opgavestyring for butikschefer](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a>Konfigurere rettigheder for medarbejdere

Medarbejdere skal have rettigheder til at oprette opgavelister, administrere tildelingskriterier og konfigurere gentagelsen af en opgaveliste. Hvis du vil konfigurere disse rettigheder, skal du tildele medarbejdere rollen **Retail Jobliste**.

Du kan konfigurere rettigheder for en medarbejder ved at følge disse trin.

1. Gå til **Retail og Commerce \> Medarbejdere \> Brugere**.
1. Vælg medarbejderen.
1. Klik på **Tildel roller** i oversigtspanelet **Brugers roller**.
1. Vælg rollen **Retail Jobliste** i dialogboksen **Tildel roller til bruger**, og vælg derefter **OK**.

## <a name="distribute-permissions-to-pos-clients"></a>Distribuere rettigheder til POS-klienter

Før medarbejderne kan bruge POS-klienter, skal rettighederne distribueres og synkroniseres til disse klienter.

Udfør følgende trin for at distribuere rettigheder til POS-klienter:

1. Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.
1. Vælg distributionsplanen **1060** (**Personale**), og vælg derefter **Kør nu**.
1. Vælg distributionsplanen **1070** (**Kanalkonfiguration**), og vælg derefter **Kør nu**.

## <a name="configure-pos-notifications-for-tasks"></a>Konfigurere POS-beskeder for opgaver

Opgavestyring skal være konfigureret, så beskeder er tilgængelige i POS-programmet.

Du kan konfigurere POS-beskeder for opgaver ved at følge disse trin.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS \> POS-handlinger**.
1. Find handlingen **1400** (**Opgavestyring**), og markér afkrydsningsfeltet **Aktivér beskeder** for den.

I følgende illustration vises handlingen **Opgavestyring** på siden **POS-handlinger**.

![Handlingen Opgavestyring på siden POS-handlinger](media/HQ-POS-Tasks-Notifications.png)

Du kan finde flere oplysninger om, hvordan du konfigurerer POS-beskeder, i [Vis ordrebeskeder på POS](notifications-pos.md).

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a>Konfigurere feltet Opgaver på en startside for POS-programmet

Før du konfigurerer feltet **Opgaver** på startsiden for et POS-program, kan du se [Skærmlayout til POS](pos-screen-layouts.md) for at få oplysninger om, hvordan du konfigurerer og føjer nye knapper til et POS-skærmlayout.

Du konfigurerer feltet **Opgaver** på en startside for POS-programmet ved at følge disse trin.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS \> Screenlayout**.
1. Vælg et skærmlayout, vælg en layout størrelse, og vælg en knapmatrix.
1. Vælg **Designer** i oversigtspanelet **Knapmatrix** for at redigere den valgte knapmatrix.
1. Føj en **Opgave**-flise til det relevante afsnit på startsiden.

Følgende illustration viser et eksempel på et **Opgave**-felt på en POS-startside.

![Opgavefelt på en POS-startside](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over opgavestyring](task-mgmt-overview.md)

[Oprette opgavelister og tilføje opgaver](task-mgmt-create-lists.md)

[Tildele opgavelister til butikker eller medarbejdere](task-mgmt-assign-lists.md)

[Opgavestyring i POS](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]