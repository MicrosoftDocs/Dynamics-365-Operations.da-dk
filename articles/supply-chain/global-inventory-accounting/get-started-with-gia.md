---
title: Start her med globalt lagerregnskab
description: Denne artikel indeholder en beskrivelse af, hvordan du kommer i gang med Global Inventory Accounting.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 493e0be8ab56abc2a3253876107b7f4fefabf4ad
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891083"
---
# <a name="get-started-with-global-inventory-accounting"></a>Kom i gang med Global Inventory Accounting

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Med Global Inventory Accounting kan du udføre flere lagerregnskaber i de Global Inventory Accounting-finansposter, som du har oprettet. Du skal knytte hver Global Inventory Accounting-finanspost til et *princip*. En konvention er en samling af følgende typer regnskabspolitikker:

- Omkostningsobjekt
- Basis for inputmål
- Forudsætning for omkostningsforløb
- Omkostningselement

> [!NOTE]
> Selv efter at du har slået Global Inventory Accounting til, kan du stadig udføre lagerregnskab i Microsoft Dynamics 365 Supply Chain Management, som du plejer.

Global Inventory Accounting er et tilføjelsesprogram. For at gøre dets funktioner tilgængelige skal du installere det fra Microsoft Dynamics Lifecycle Services (LCS). Du kan vælge at evaluere det i et testmiljø, før du slår det til i produktionsmiljøer.

Global Inventory Accounting understøtter i øjeblikket ikke alle funktioner til omkostningsstyring, der er indbygget i Supply Chain Management. Det er derfor vigtigt, at du evaluerer, om det funktionssæt, der aktuelt er tilgængeligt, opfylder dine behov.

## <a name="how-to-get-the-global-inventory-accounting-add-in"></a><a name="sign-up"></a>Sådan får du et tilføjelsesprogram til Global Inventory Accounting

> [!IMPORTANT]
> Hvis du vil bruge Global Inventory Accounting, skal du have et LCS-aktiveret miljø med høj tilgængelighed (ikke et OneBox-miljø). Derudover skal du køre Supply Chain Management version 10.0.19 eller nyere.

### <a name="supply-chain-management-version-10019-to-10026"></a>Supply Chain Management version 10.0.19 til 10.0.26

Hvis du vil installere Global Inventory Accounting for Supply Chain Management version 10.0.19 til 10.0.26, [skal du starte med at installere tilføjelsesprogrammet](#install). Send derefter LCS-miljø-id'et og firmanavnet i en e-mail til til det [globale lagerregnskabsteam](mailto:GlobalInvAccount@microsoft.com). Teamet sender dig en opfølgningsmail, der indeholder dine Global Inventory Accounting-tjenesteslutpunkter.

### <a name="supply-chain-management-version-10027-and-later"></a>Supply Chain Management version 10.0.27 og nyere

Hvis du vil installere Global Inventory Accounting for Supply Chain Management version 10.0.27 og senere, skal du blot [installere tilføjelsesprogrammet](#install). I forbindelse med disse versioner af Supply Chain Management oprettes slutpunkterne for den globale lagerregnskabstjeneste automatisk, så du ikke behøver at finde dem manuelt. Hvis du oplever problemer, mens du konfigurerer tilføjelsesprogrammet, skal du kontakte det [globale lagerregnskabsteam](mailto:GlobalInvAccount@microsoft.com).

## <a name="licensing"></a>Licensering

Global Inventory Accounting er givet i licens sammen med standardfunktionerne i lagerregnskabet, der er tilgængelige for Supply Chain Management. Du behøver ikke at købe en ekstra licens for at bruge Global Inventory Accounting.

## <a name="prerequisites"></a>Forudsætninger

### <a name="set-up-microsoft-power-platform-integration"></a>Konfigurer integration med Microsoft Power Platform

Før du kan aktivere tilføjelsesprogrammets funktioner, skal du integrere det med Microsoft Power Platform ved at følge disse trin.

1. Åbn det LCS-miljø, hvor du vil tilføje tjenesten.
1. Gå til **Alle detaljer**.
1. I sektionen **Integration af Power Platform** skal du vælge **Opsætning**.
1. I dialogboksen **Opsætning af Power Platform-miljø** skal du markere afkrydsningsfeltet og derefter vælge **Opsætning**. Det tager normalt mellem 60 og 90 minutter at udføre konfigurationen.
1. Når opsætningen af Microsoft Power Platform-miljøet er fuldført, vises navnet på miljøet på siden. Sektionen **Power Platform-integration** viser desuden sætningen "Opsætning af Power Platform-miljøet er fuldført". Global Inventory Accounting kræver ikke et program til dobbeltskrivning.

Du kan finde flere oplysninger i [Aktivere efter installation af miljøet](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md#enable-after-deploy).

### <a name="set-up-dataverse"></a>Konfigurer Dataverse

Før du konfigurerer Dataverse, skal du føje Global Inventory Accounting-serviceprincipperne til din lejer ved at følge disse trin.

1. Installer Azure AD-modul til Windows PowerShell v2 som beskrevet i [Installere Azure Active Directory PowerShell til Graph](/powershell/azure/active-directory/install-adv2).
1. Kør følgende PowerShell-kommando.

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

Derefter skal du oprette programbrugere til Global Inventory Accounting i Dataverse ved at følge disse trin.

1. Åbn URL-adressen til dit Dataverse-miljø.
1. Gå til **Avancerede indstillinger \> System \> Sikkerhed \> Brugere**, og opret en programbruger. Brug feltet **Vis** til at ændre sidevisningen til *Applikationsbrugere*.
1. Vælg **Ny**.
1. Indstil feltet **Program-id** til *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.
1. Vælg **Tildel rolle**, og vælg derefter *Systemadministrator*. Hvis der er en rolle med navnet *Common Data Service Bruger*, skal du også vælge den.
1. Gentag de foregående trin, men angiv feltet **Program-id** til *5f58fc56-0202-49a8-ac9e-0946b049718b*.

Du kan finde flere oplysninger under [Oprette en programbruger](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

Hvis standardsproget for installationen af Dataverse ikke er engelsk, skal du følge disse trin.

1. Gå til **Avancerede indstillinger \> Administration \> Sprog**.
1. Vælg *Engelsk* (*LanguageCode=1033*), og vælg derefter **Anvend**.

## <a name="install-the-add-in"></a><a name="install"></a>Installer tilføjelsesprogrammet

Benyt følgende fremgangsmåde for at installere tilføjelsesprogrammet, så du kan bruge Global Inventory Accounting.

1. Log på [LCS](https://lcs.dynamics.com/Logon/Index).
1. Åbn det LCS-miljø, hvor du vil tilføje tjenesten.
1. Gå til **Alle detaljer**.
1. Gå til **Power Platform-integration**, og vælg **Opsætning**.
1. I dialogboksen **Opsætning af Power Platform-miljø** skal du markere afkrydsningsfeltet og derefter vælge **Opsætning**. Det tager normalt mellem 60 og 90 minutter at udføre konfigurationen.
1. Når opsætningen af Microsoft Power Platform-miljøet er fuldført, skal du vælge **Installer et nyt tilføjelsesprogram** i oversigtspanelet **Miljøtilføjelsesprogrammer**.
1. Vælg **Globalt lagerregnskab**.
1. Følg installationsvejledningen, og accepter vilkårene og betingelserne.
1. Vælg **Installer**.
1. I oversigtspanelet **Miljøtilføjelsesprogrammer** kan du se, at Global Inventory Accounting er ved at blive installeret. Efter nogle få minutter skal status ændres fra *Installerer* til *Installeret*. (Du skal muligvis opdatere siden for at se ændringen). På dette tidspunkt er Global Inventory Accounting klar til brug.

## <a name="set-up-the-integration"></a>Konfigurere integrationen

Følg disse trin for at konfigurere integrationen mellem Global Inventory Accounting og Supply Chain Management.

1. Log på Supply Chain Management.
1. Gå til **Systemadministration \> Funktionsstyring**.
1. Vælg **Søg efter opdateringer**.
1. Søg efter den funktion, der kaldes *(Forhåndsversion) Globalt lagerregnskab*, under fanen **Alle**.
1. Vælg **Aktiver nu**.
1. Gå til **Globalt lagerregnskab \> Opsætning \> Parametre for globalt lagerregnskab \> Integrationsparametre**.
1. Afhængigt af den version af Supply Chain Management, du kører, skal du udføre et af følgende trin:
    - **Supply Chain Management version 10.0.19 til 10.0.26**: I **datatjenesteslutpunktet** og felterne for **globalt lagerregnskabsslutpunkter** skal du angive de URL-adresser, der er sendt til dig via e-mail fra det globale lagerregnskabsteam (se også [Sådan henter du tilføjelsesprogrammet Globalt Lagerregnskab](#sign-up)).
    - **Supply Chain Management version 10.0.27 og nyere**: Du behøver ikke angive slutpunkterne, så du kan springe dette trin over.

Global Inventory Accounting er nu klar til brug.
