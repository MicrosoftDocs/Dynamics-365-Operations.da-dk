---
title: Administrere livscyklus for elektroniske indberetningskonfigurationer
description: "I dette emne beskrives, hvordan du administrerer livscyklussen for elektroniske rapporteringskonfigurationer (ER) for Microsoft Dynamics 365 for Finance and Operations-løsningen."
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f3d6463ab07aaaf69a16aa0d59840cbe47427335
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Administrere livscyklus for konfiguration af elektronisk rapportering

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du administrerer livscyklussen for elektroniske rapporteringskonfigurationer (ER) for Microsoft Dynamics 365 for Finance and Operations-løsningen.

<a name="overview"></a>Overblik
--------

Elektronisk rapportering (ER) er et program, der understøtter lovgivningsmæssigt påkrævede og landespecifikke elektroniske dokumenter i Microsoft Dynamics 365 for Finance and Operations. Generelt forudsætter ER evnen til at udføre følgende opgaver for en enkelt elektronisk dokument. Du kan finde flere oplysninger under [Oversigt over elektronisk rapportering](general-electronic-reporting.md).

-   Designe en skabelon til et elektronisk dokument:
    -   Identificer de nødvendige datakilder, der kan præsenteres i dokumentet:
        -   Underliggende Finance and Operations-data som f.eks. datatabeller, dataenheder og klasser.
        -   Processpecifikke egenskaber som f.eks. afviklingsdato og -klokkeslæt og tidszone.
        -   Brugerinputparametre, angivet af slutbrugeren ved kørsel.
    -   Definer de nødvendige dokumentelementer og deres topologi for at angive et endeligt dokumentformat.
    -   Konfigurer den ønskede datastrøm fra markerede datakilder til definerede dokumentelementer (via datakildebindinger til dokumentets formatkomponenter), og angiv processtyringslogik.
-   Gør en skabelon tilgængelig, så den kan bruges i andre forekomster af Finance and Operations:
    -   Transformér en dokumentskabelon, der blev oprettet i Finance and Operations, til en ER-konfiguration, og eksportér konfigurationen fra den aktuelle forekomst af Finance and Operations som et XML-pakke, der kan gemmes lokalt eller i LCS.
    -   Transformér en ER-konfiguration til en Finance and Operations-dokumentskabelon.
    -   Importér en XML-pakke, der er gemt lokalt eller i LCS, til den aktuelle forekomst af Finance and Operations.
-   Tilpas skabelonen for et elektronisk dokument:
    -   Bring en skabelon fra LCS til den aktuelle Finance and Operations-forekomst som en som en ER-konfiguration:
    -   Design en brugerdefineret version af en ER-konfiguration, og bevar en reference til basisversionen.
-   Integrer en skabelon med en bestemt forretningsproces, så den er tilgængelig i Finance and Operations:
    -   Konfigurere indstillinger, så Finance and Operations begynder at bruge en ER-konfiguration, ved at referere til denne konfiguration i en procesrelateret parameter. Se for eksempel ER-konfigurationen i en bestemt kreditorbetalingsmetode for at generere en elektronisk betalingsmeddelelse til behandling af fakturaer.
-   Brug en skabelon i en bestemt forretningsproces:
    -   Kør en ER-konfiguration i en bestemt forretningsproces. For eksempel for at generere en elektronisk betalingsmeddelelse til behandling af fakturaer, når betalingsmåde, der refererer til ER-konfigurationen, er markeret.

## <a name="concepts"></a>Begreber
Følgende roller og relaterede aktiviteter er tilknyttet ER-konfigurations livscyklus.

| Rolle                                       | Aktiviteter                                                      | Betegnelse                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funktionel konsulent i elektronisk rapportering | Opret og administrer ER-komponenter (modeller og formater).           | En forretningsmand, som designer ER domæne-specifikke datamodeller, designer de krævede skabeloner til elektroniske dokumenter og binder dem i overensstemmelse hermed.                                                                           |
| Udvikler til elektronisk rapportering             | Opret og administrer datamodeltilknytninger.                          | En Finance and Operations-specialist, der vælger de nødvendige Finance and Operations-datakilder og binder dem til ER domæne-specifikke datamodeller.                                                                 |
| Regnskabsansvarlig                      | Konfigurer procesrelaterede indstillinger, der refererer til ER-artefakter. | For eksempel rollen **Regnskabsansvarlig**, der gør det muligt, at bruge indstillingerne for en ER-konfiguration i en bestemt kreditorbetalingsmetode til at generere en elektronisk betalingsmeddelelse til behandling af fakturaer. |
| Ansvarlig for kreditorbetalinger            | Brug ER-artefakter i en bestemt forretningsproces.                | For eksempel rollen **Ansvarlig for kreditorbetalinger**, der gør det muligt at generere elektroniske betalingsmeddelelser til behandling af fakturaer baseret på det ER-format, som er konfigureret til en specifik betalingsmetode.           |

## <a name="er-configuration-development-lifecycle"></a>Udviklingsfase i ER-konfiguration
Af følgende ER-relaterede årsager anbefales du at designe ER-konfigurationer i udviklingsmiljøet som en adskilt forekomst af Finance and Operations:

-   Brugere i rollen som **Udvikler til elektronisk rapportering** eller **Funktionel konsulent i elektronisk rapportering** kan redigere konfigurationer og køre dem til testformål. Denne situation kan medføre kald af metoder for klasser og tabeller, der kan være skadelige for virksomhedens data og Finance and Operations-forekomstens ydeevne.
-   Kald af metoder for klasser og tabeller som ER-datakilder til ER-konfigurationer er ikke begrænset af Finance and Operations-indførselssteder og logført firmaindhold. Derfor kan brugere i rollen **Udvikler til elektronisk rapportering** eller rollen **Funktionel konsulent i elektronisk rapportering** få adgang til forretningsfølsomme data.

ER-konfigurationer, der designet i udviklingsmiljøet, kan overføres til testmiljøet til konfigurationen af evaluering (korrekt procesintegration, rigtigheden af resultater og ydeevne) og kvalitetssikring som f.eks. rigtigheden af rollebaserede adgangsrettigheder og opdeling af opgaver. De funktioner, der aktiverer ER-konfigurationsudvekslingen, kan bruges til dette formål. Endelig kan afprøvede ER-konfigurationer overføres til enten LCS, hvor de kan deles med serviceabonnenter, eller til produktionsmiljøet til intern brug som vist i følgende illustration. ![Livscyklus for ER-konfiguration](./media/ger-configuration-lifecycle.png)

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)




