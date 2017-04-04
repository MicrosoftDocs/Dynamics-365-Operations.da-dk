---
title: Administrere livscyklus for elektroniske indberetningskonfigurationer
description: "Dette emne beskriver, hvordan du administrerer livscyklus for elektronisk indberetning (ER) konfigurationer for Microsoft Dynamics 365 for løsning af transaktioner."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: f4d8994f6548119789715a4879b6bc02d25598e9
ms.lasthandoff: 03/31/2017


---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Administrere livscyklus for elektroniske indberetningskonfigurationer

Dette emne beskriver, hvordan du administrerer livscyklus for elektronisk indberetning (ER) konfigurationer for Microsoft Dynamics 365 for løsning af transaktioner.

<a name="overview"></a>Overblik
--------

Elektronisk rapportering (ER) er et program, der understøtter lovgivningsmæssigt påkrævede og landespecifikke elektroniske dokumenter i Microsoft Dynamics 365 for Operations. Generelt forudsætter ER evnen til at udføre følgende opgaver for en enkelt elektronisk dokument. Yderligere oplysninger finder du under [elektronisk rapportering oversigt](general-electronic-reporting.md).

-   Designe en skabelon til et elektronisk dokument:
    -   Identificer de nødvendige datakilder, der kan præsenteres i dokumentet:
        -   Underliggende Dynamics 365 for operationer, datatabeller, data, objekter og klasser.
        -   Proces-specifikke egenskaber, såsom udførelse af dato og klokkeslæt og tidszone.
        -   Brugerinputparametre, angivet af brugeren på kørselstidspunktet.
    -   Definer de nødvendige dokumentelementer og deres topologi for at angive et endeligt dokumentformat.
    -   Konfigurer den ønskede datastrøm fra markerede datakilder til definerede dokumentelementer (via datakildebindinger til dokumentets formatkomponenter), og angiv processtyringslogik.
-   Gør en skabelon tilgængelig, så den kan bruges i andre forekomster af Dynamics 365 for Operations:
    -   Transformér en dokumentskabelon, der blev oprettet i Dynamics 365 for Operations, til en ER-konfiguration, og eksportér konfigurationen fra den aktuelle forekomst af Dynamics 365 for Operations som et XML-pakke, der kan gemmes lokalt eller i LCS.
    -   Transformér en ER-konfiguration til en Dynamics 365 for Operations-dokumentskabelon.
    -   Importér en XML-pakke, der er gemt lokalt eller i LCS, til den aktuelle forekomst af Dynamics 365 for Operations.
-   Tilpas skabelonen for et elektronisk dokument:
    -   Bring en skabelon fra LCS til den aktuelle Dynamics 365 for Operations-forekomst som en som en ER-konfiguration:
    -   Design en brugerdefineret version af en ER-konfiguration, og bevar en reference til basisversionen.
-   Integrer en skabelon med en bestemt forretningsproces, så den er tilgængelig i Dynamics 365 for Operations:
    -   Konfigurere indstillinger, så Dynamics 365 for Operations begynder at bruge en ER-konfiguration, ved at referere til denne konfiguration i en procesrelateret parameter. Se eksempelvis ER konfigurationen i en bestemt konti kreditor betalingsmetode for at generere en elektronisk betaling meddelelse til behandling af fakturaer.
-   Brug en skabelon i en bestemt forretningsproces:
    -   Køre en konfiguration ER i en bestemt forretningsproces. For eksempel er for at generere en elektronisk betaling meddelelse til behandling af fakturaer, når en betalingsmetode, der henviser til konfigurationen, der ER markeret.

## <a name="concepts"></a>Begreber
Følgende roller og relaterede aktiviteter, der er knyttet til konfiguration ER livscyklus.

| Rolle                                       | Aktiviteter                                                      | Betegnelse                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funktionel konsulent i elektronisk rapportering | Opret og administrer ER-komponenter (modeller og formater).           | En person, virksomhed som designer ER domæne-specifikke datamodeller og designs kræves skabeloner til elektroniske dokumenter og binder dem i overensstemmelse hermed.                                                                           |
| Udvikler til elektronisk rapportering             | Opret og administrer datamodeltilknytninger.                          | En Dynamics 365 for operationer specialist, der vælger de nødvendige Dynamics 365 for operationer datakilder og binder dem til ER domæne-specifikke datamodeller.                                                                 |
| Regnskabsansvarlig                      | Konfigurer procesrelaterede indstillinger, der refererer til ER-artefakter. | For eksempel en **regnskabsmæssige tilsynsførende** rolle, der gør det muligt for indstillingerne for en konfiguration ER der skal bruges i en bestemt kreditor konti betalingsmetode til at generere en elektronisk betaling meddelelse til behandling af fakturaer. |
| Ansvarlig for kreditorbetalinger            | Brug ER-artefakter i en bestemt forretningsproces.                | For eksempel en **konti kreditorbetalinger medarbejder** rolle, der giver mulighed for elektronisk betaling meddelelser, der genereres for behandling af fakturaer, der er baseret på formatet ER, som er konfigureret til en specifik betalingsform.           |

## <a name="er-configuration-development-lifecycle"></a>Udviklingsfase i ER-konfiguration
Af følgende ER-relaterede årsager anbefales du at designe ER-konfigurationer i udviklingsmiljøet som en adskilt forekomst af Dynamics 365 for Operations:

-   Brugere i rollen som **Udvikler til elektronisk rapportering** eller **Funktionel konsulent i elektronisk rapportering** kan redigere konfigurationer og køre dem til testformål. Denne situation kan medføre kald af metoder for klasser og tabeller, der kan være skadelige for virksomhedens data og Dynamics 365 for Operations-forekomstens ydeevne.
-   Kald af metoder for klasser og tabeller som ER-datakilder til ER-konfigurationer er ikke begrænset af Dynamics 365 for Operations-indførselssteder og logført firmaindhold. Derfor kan brugere i rollen **Udvikler til elektronisk rapportering** eller rollen **Funktionel konsulent i elektronisk rapportering** få adgang til forretningsfølsomme data.

ER de konfigurationer, der er udviklet i udviklingsmiljøet kan overføres til testmiljøet til konfiguration af evaluering (korrekt procesintegration, rigtigheden af resultaterne og ydeevnen) og kvalitetssikring, som rigtigheden af rolle baseret adgangsrettigheder og opdeling af opgaver. De funktioner, der aktiverer ER konfigurationen udveksling kan bruges til dette formål. Endelig kan dokumenterede ER konfigurationer overføres til Remburser, hvor de deles med service-abonnenter, eller til produktionsmiljøet til intern brug, som vist i følgende illustration. ![ER configuration lifecycle](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Se også
--------

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)


