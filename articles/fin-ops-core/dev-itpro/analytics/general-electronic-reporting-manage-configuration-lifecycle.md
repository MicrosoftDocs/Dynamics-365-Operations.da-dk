---
title: Administrere livscyklus for konfigurationen af elektronisk rapportering (ER)
description: I dette emne beskrives, hvordan du administrerer livscyklussen for elektroniske rapporteringskonfigurationer (ER) for Dynamics 365 Finance.
author: NickSelin
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52aba53b5323a9c6c4331cd8de7e932bb9c3547e
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893195"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Administrere livscyklus for konfigurationen af elektronisk rapportering (ER)

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du administrerer livscyklussen for elektroniske rapporteringskonfigurationer (ER) for Dynamics 365 Finance.

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
Af følgende ER-relaterede årsager anbefales du at designe ER-konfigurationer i udviklingsmiljøet som en adskilt forekomst af Finance and Operations:

- Brugere i rollen som **Udvikler til elektronisk rapportering** eller **Funktionel konsulent i elektronisk rapportering** kan redigere konfigurationer og køre dem til testformål. Denne situation kan medføre kald af metoder for klasser og tabeller, der kan være skadelige for virksomhedens data og forekomstens ydeevne.
- Kald af metoder for klasser og tabeller som ER-datakilder til ER-konfigurationer er ikke begrænset af indgangspunkter og logført firmaindhold. Derfor kan brugere i rollen **Udvikler til elektronisk rapportering** eller rollen **Funktionel konsulent i elektronisk rapportering** få adgang til forretningsfølsomme data.

ER-konfigurationer, der designet i udviklingsmiljøet, kan [uploades](#data-persistence-consideration) til testmiljøet til konfigurationen af evaluering (korrekt procesintegration, rigtigheden af resultater og ydeevne) og kvalitetssikring som f.eks. rigtigheden af rollebaserede adgangsrettigheder og opdeling af opgaver. De funktioner, der aktiverer ER-konfigurationsudvekslingen, kan bruges til dette formål. Afprøvede ER-konfigurationer kan uploades til LCS, hvor de kan deles med serviceabonnenter, eller de kan [importeres](#data-persistence-consideration) til intern brug i produktionsmiljøet.

![Livscyklus for ER-konfiguration](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a><a name="data-persistence-consideration" />Overvejelse af datafastholdelse

Du kan [importere](tasks/er-import-configuration-lifecycle-services.md) forskellige [versioner](general-electronic-reporting.md#component-versioning) af en ER-[konfiguration](general-electronic-reporting.md#Configuration) individuelt til din Finance-forekomst. Når en ny version af en ER-konfiguration importeres, styrer systemet indholdet af kladdeversionen af denne konfiguration:

   - Når den importerede version er lavere end den højeste version af denne konfiguration i den aktuelle Finance-forekomst, forbliver indholdet af kladdeversionen af denne konfiguration uændret.
   - Når den importerede version er højere end nogen anden version af denne konfiguration i den aktuelle Finance-forekomst, kopieres indholdet af den importerede version til kladdeversionen af denne konfiguration, så du kan fortsætte med at redigere den sidste fuldførte version.

Hvis denne konfiguration ejes af den [konfigurationsudbyder](general-electronic-reporting.md#Provider), der er aktiveret i øjeblikket, er kladdeversionen af denne konfiguration synlig for dig i oversigtspanelet **Versioner** på siden **Konfigurationer** (**Organisationsadministration** > **Elektronisk rapportering** > **Konfigurationer**). Du kan vælge kladdeversionen af konfigurationen og [redigere](er-quick-start2-customize-report.md#ConfigureDerivedFormat) dens indhold ved hjælp af den relevante ER-designer. Når du har redigeret kladdeversionen af ER-konfigurationen, matcher indholdet ikke længere indholdet af den højeste version af denne konfiguration i den aktuelle Finance-forekomst. For at forhindre, at du mister ændringerne, vises der en fejl om, at importen ikke kan fortsætte, da versionen af denne konfiguration er højere end den højeste version af denne konfiguration i den aktuelle Finance-forekomst. Når det sker, f.eks. i forbindelse med formatkonfiguration **X**, vises fejlen **Format 'X' version er ikke fuldført**.

Hvis du vil fortryde de ændringer, du har foretaget i kladdeversionen, skal du vælge den højeste fuldførte eller delte version af din ER-konfiguration i Finance i oversigtspanelet **Versioner** og derefter vælge indstillingen **Hent denne version**. Indholdet af den valgte version kopieres til kladdeversionen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
