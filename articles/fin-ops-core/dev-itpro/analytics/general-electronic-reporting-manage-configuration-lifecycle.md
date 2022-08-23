---
title: Administrere livscyklus for konfigurationen af elektronisk rapportering (ER)
description: Denne artikel beskriver, hvordan du administrerer livscyklussen for elektroniske rapporteringskonfigurationer (ER) til Dynamics 365 Finance.
author: kfend
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: fe23d4cb2b293af466df2236b153974f95f636f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271577"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Administrere livscyklus for konfigurationen af elektronisk rapportering (ER)

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du administrerer livscyklussen for [elektroniske rapporteringskonfigurationer](general-electronic-reporting.md) [(ER)](general-electronic-reporting.md#Configuration) til Dynamics 365 Finance.

## <a name="overview"></a>Overblik

Elektronisk rapportering (ER) er et program, der understøtter lovgivningsmæssigt påkrævede og landespecifikke elektroniske dokumenter. Generelt forudsætter ER evnen til at udføre følgende opgaver for en enkelt elektronisk dokument. Du kan finde flere oplysninger under [Oversigt over Elektronisk rapportering (ER)](general-electronic-reporting.md).

- Designe en skabelon til et elektronisk dokument:

    - Identificer de nødvendige datakilder, der kan præsenteres i dokumentet:

        - Underliggende data som f.eks. datatabeller, dataenheder og klasser.
        - Processpecifikke egenskaber som f.eks. afviklingsdato og -klokkeslæt og tidszone.
        - Brugerinputparametre, angivet af slutbrugeren ved kørsel.

    - Definer de nødvendige dokumentelementer og deres topologi for at angive et endeligt dokumentformat.
    - Konfigurer den ønskede datastrøm fra markerede datakilder til definerede dokumentelementer (via datakildebindinger til dokumentets formatkomponenter), og angiv processtyringslogik.

- Gør en skabelon tilgængelig, så den kan bruges i andre forekomster:

    - Transformér en dokumentskabelon, der er oprettet til en ER-konfiguration, og eksportér konfigurationen fra den aktuelle programforekomst som en XML-pakke, der kan gemmes lokalt eller i Lifecycle Services (LCS).
    - Transformér en ER-konfiguration til en programdokumentskabelon.
    - Importér en XML-pakke, der er gemt lokalt eller i LCS, til den aktuelle forekomst.

- Tilpas skabelonen for et elektronisk dokument:

    - Bring en skabelon fra LCS til den aktuelle forekomst som en ER-konfiguration:
    - Design en brugerdefineret version af en ER-konfiguration, og bevar en reference til basisversionen.

- Integrer en skabelon med en bestemt forretningsproces, så den er tilgængelig i programmet:

    - Konfigurer indstillinger, så programmet begynder at bruge en ER-konfiguration, ved at referere til denne konfiguration i en procesrelateret parameter. Se for eksempel ER-konfigurationen i en bestemt kreditorbetalingsmetode for at generere en elektronisk betalingsmeddelelse til behandling af fakturaer.

- Brug en skabelon i en bestemt forretningsproces:

    - Kør en ER-konfiguration i en bestemt forretningsproces. For eksempel for at generere en elektronisk betalingsmeddelelse til behandling af fakturaer, når betalingsmåde, der refererer til ER-konfigurationen, er markeret.

## <a name="concepts"></a>Begreber
Følgende roller og relaterede aktiviteter er tilknyttet ER-konfigurations livscyklus.

| Rolle                                       | Aktiviteter                                                      | Beskrivelse |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| Funktionel konsulent i elektronisk rapportering | Opret og administrer ER-komponenter (modeller og formater).           | En forretningsmand, som designer ER domæne-specifikke datamodeller, designer de krævede skabeloner til elektroniske dokumenter og binder dem i overensstemmelse hermed. |
| Udvikler til elektronisk rapportering             | Opret og administrer datamodeltilknytninger.                          | En specialist, der vælger de nødvendige Finance-datakilder og binder dem til ER-domænespecifikke datamodeller. |
| Regnskabsansvarlig                      | Konfigurer procesrelaterede indstillinger, der refererer til ER-artefakter. | For eksempel rollen **Regnskabsansvarlig**, der gør det muligt, at bruge indstillingerne for en ER-konfiguration i en bestemt kreditorbetalingsmetode til at generere en elektronisk betalingsmeddelelse til behandling af fakturaer. |
| Ansvarlig for kreditorbetalinger            | Brug ER-artefakter i en bestemt forretningsproces.                | For eksempel rollen **Ansvarlig for kreditorbetalinger**, der gør det muligt at generere elektroniske betalingsmeddelelser til behandling af fakturaer baseret på det ER-format, som er konfigureret til en specifik betalingsmetode. |

## <a name="er-configuration-development-lifecycle"></a>Udviklingsfase i ER-konfiguration
Af følgende ER-relaterede årsager anbefales du at designe ER-konfigurationer i udviklingsmiljøet som en adskilt forekomst af finans og drift:

- Brugere i rollen som **Udvikler til elektronisk rapportering** eller **Funktionel konsulent i elektronisk rapportering** kan redigere konfigurationer og køre dem til testformål. Denne situation kan medføre kald af metoder for klasser og tabeller, der kan være skadelige for virksomhedens data og forekomstens ydeevne.
- Kald af metoder for klasser og tabeller som ER-datakilder til ER-konfigurationer er ikke begrænset af indgangspunkter og logført firmaindhold. Derfor kan brugere i rollen **Udvikler til elektronisk rapportering** eller rollen **Funktionel konsulent i elektronisk rapportering** få adgang til forretningsfølsomme data.

ER-konfigurationer, der designet i udviklingsmiljøet, kan [uploades](#data-persistence-consideration) til testmiljøet til konfigurationen af evaluering (korrekt procesintegration, rigtigheden af resultater og ydeevne) og kvalitetssikring som f.eks. rigtigheden af rollebaserede adgangsrettigheder og opdeling af opgaver. De funktioner, der aktiverer ER-konfigurationsudvekslingen, kan bruges til dette formål. Afprøvede ER-konfigurationer kan uploades til LCS, hvor de kan deles med serviceabonnenter, eller de kan [importeres](#data-persistence-consideration) til intern brug i produktionsmiljøet.

![Livscyklus for ER-konfiguration.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>Overvejelse af datafastholdelse

Du kan [importere](tasks/er-import-configuration-lifecycle-services.md) forskellige [versioner](general-electronic-reporting.md#component-versioning) af en ER-[konfiguration](general-electronic-reporting.md#Configuration) individuelt til din Finance-forekomst. Når en ny version af en ER-konfiguration importeres, styrer systemet indholdet af kladdeversionen af denne konfiguration:

- Når den importerede version er lavere end den højeste version af denne konfiguration i den aktuelle Finance-forekomst, forbliver indholdet af kladdeversionen af denne konfiguration uændret.
- Når den importerede version er højere end nogen anden version af denne konfiguration i den aktuelle Finance-forekomst, kopieres indholdet af den importerede version til kladdeversionen af denne konfiguration, så du kan fortsætte med at redigere den sidste fuldførte version.

Hvis denne konfiguration ejes af den [konfigurationsudbyder](general-electronic-reporting.md#Provider), der er aktiveret i øjeblikket, er kladdeversionen af denne konfiguration synlig for dig i oversigtspanelet **Versioner** på siden **Konfigurationer** (**Organisationsadministration** > **Elektronisk rapportering** > **Konfigurationer**). Du kan vælge kladdeversionen af konfigurationen og [redigere](er-quick-start2-customize-report.md#ConfigureDerivedFormat) dens indhold ved hjælp af den relevante ER-designer. Når du har redigeret kladdeversionen af ER-konfigurationen, matcher indholdet ikke længere indholdet af den højeste version af denne konfiguration i den aktuelle Finance-forekomst. For at forhindre, at du mister ændringerne, vises der en fejl om, at importen ikke kan fortsætte, da versionen af denne konfiguration er højere end den højeste version af denne konfiguration i den aktuelle Finance-forekomst. Når det sker, f.eks. i forbindelse med formatkonfiguration **X**, vises fejlen **Format 'X' version er ikke fuldført**.

Hvis du vil fortryde de ændringer, du har foretaget i kladdeversionen, skal du vælge den højeste fuldførte eller delte version af din ER-konfiguration i Finance i oversigtspanelet **Versioner** og derefter vælge indstillingen **Hent denne version**. Indholdet af den valgte version kopieres til kladdeversionen.

## <a name="applicability-consideration"></a>Overvejelse af anvendelighed

Når du designer en ny version af en ER-konfiguration, kan du definere dens [afhængighed](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) af andre softwarekomponenter. Dette trin betragtes som en forudsætning for at kontrollere overførslen af denne konfigurations version fra et ER-lager eller en ekstern XML-fil og yderligere anvendelse af denne version. Når du forsøger at importere en ny version af en ER-konfiguration, bruger systemet de konfigurerede forudsætninger til at styre, om versionen kan importeres.

I visse tilfælde kan du kræve, at systemet ignorerer de konfigurerede forudsætninger, når du importerer nye versioner af ER-konfigurationer. Hvis du ønsker, at systemet skal ignorere forudsætningerne under importen, skal du følge disse trin.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
3. Angiv indstillingen **Spring over produktopdateringer og kontrol af forudsætninger for version under import** til **Ja**.

    > [!NOTE]
    > Denne parameter er bruger- og virksomhedspecifik.

## <a name="dependencies-on-other-components"></a>Afhængigheder af andre komponenter

ER-konfigurationer kan konfigureres som værende [afhængige](er-download-configurations-global-repo.md#import-filtered-configurations) af andre konfigurationer. Du kan f.eks. [importere](er-download-configurations-global-repo.md) en ER-[datamodelkonfiguration](er-overview-components.md#data-model-component) fra det globale lager til din forekomst af [Microsoft Regulatory Configuration Services (RCS)](../../../finance/localizations/rcs-overview.md) eller Dynamics 365 Finance og derefter oprette en ny ER-[formatkonfiguration](er-overview-components.md#format-component), der er [afledt](er-quick-start2-customize-report.md#DeriveProvidedFormat) af den importerede ER-datamodelkonfiguration. Den afledte ER-formatkonfiguration afhænger af konfigurationen af ER-basisdatamodellen.

![Afledt ER-formatkonfiguration på siden Konfigurationer.](./media/ger-configuration-lifecycle-img1.png)

Når du er færdig med at designe formatet, kan du ændre status for den første [version](general-electronic-reporting.md#component-versioning) af ER-formatkonfigurationen fra **Kladde** til **Fuldført**. Derefter kan du dele den fuldførte version af ER-formatkonfigurationen ved at [publicere](../../../finance/localizations/rcs-global-repo-upload.md) den til det globale lager. Derefter kan du få adgang til det globale lager fra enhver forekomst af RCS eller Finance i skyen. Du kan derefter importere enhver ER-konfigurationsversion, der gælder for programmet, fra det globale lager til det pågældende program.

![Publiceret ER-formatkonfiguration på siden Konfigurationslager.](./media/ger-configuration-lifecycle-img2.png)

Når du vælger ER-formatkonfigurationen i globalt lager for at importere den til en nyligt udrullet RCS- eller Finance-forekomst baseret på konfigurationsafhængigheden, findes grundlæggende ER-datamodelkonfigurationen automatisk i globalt lager og importeres sammen med den valgte ER-formatkonfiguration som basiskonfiguration.

Du kan også eksportere ER-formatkonfigurationsversionen fra den aktuelle RCS- eller Finance-forekomst og gemme den lokalt som en XML-fil.

![Eksport af ER-formatkonfigurationsversion som XML på siden Konfiguration.](./media/ger-configuration-lifecycle-img3.png)

I versioner af Finance **før version 10.0.29**, når du forsøger at importere ER-formatkonfigurationsversionen fra den pågældende XML-fil eller fra andre lagre end globallageret til en nyligt implementeret RCS- eller Finance-forekomst, der endnu ikke indeholder nogen ER-konfigurationer, vil følgende undtagelse opstå for at oplyse dig om, at der ikke kan opnås en basiskonfiguration:

> Der er uløste referencer tilbage<br>
Reference fra objektet '\<imported configuration name\>' til objektet 'Base! (\<globally unique identifier of the missed base configuration\>'\<version of the missed base configuration\>) kan ikke oprettes

![Import af ER-formatkonfigurationsversion på siden Konfigurationslager.](./media/ger-configuration-lifecycle-img4.gif)

I version **10.0.29 og senere**, når du forsøger at udføre samme konfigurationsimport, vil ER-strukturen automatisk forsøge at finde navnet på den manglende basiskonfiguration i den globale lagercache, når du forsøger at udføre den samme konfigurationsimport, hvis der ikke findes en basiskonfiguration i den aktuelle applikationsforekomst eller i det kildelager, du aktuelt bruger. Derefter vises navnet på og den Globally Unique Identifier (GUID) for den manglende basiskonfiguration i teksten til den undtagelse, der aktiveres.

> Der er uløste referencer tilbage<br>
Reference fra objektet '\<imported configuration name\>' til objektet 'Base' (\<name of the missed base configuration\> \<globally unique identifier of the missed base configuration\>,\<version of the missed base configuration\>) kan ikke oprettes

![Undtagelsen på siden Konfigurationslager, når basiskonfigurationen ikke kan findes.](./media/ger-configuration-lifecycle-img5.png)

Du kan bruge det angivne navn til at finde basiskonfigurationen og derefter importere den manuelt.

> [!NOTE]
> Denne nye indstilling fungerer kun, når mindst én bruger allerede er logget på det globale lager ved hjælp af siden [Konfigurationslagre](er-download-configurations-global-repo.md#open-configurations-repository) eller et af [opslagsfelterne](er-extended-format-lookup.md) for det globale lager i den aktuelle Finance-forekomst, og når indholdet af globalt lager er blevet cachelagret.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Definere afhængigheden af ER-konfigurationer for andre komponenter](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

