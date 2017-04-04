---
title: "Forbind hjælpesystemet"
description: "I dette emne beskrives komponenterne i hjælpesystemet til Microsoft Dynamics 365 for Operations, og du får et overblik over, hvordan du tilslutter dem, og hvordan du opretter en brugerdefineret Hjælp."
author: margoc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 5ac5e30cff2239f601778001368fa7aaba478f5c
ms.lasthandoff: 03/31/2017


---

# <a name="connect-the-help-system"></a>Forbind hjælpesystemet

Dette emne beskriver komponenterne i Hjælp-systemet til Microsoft Dynamics 365 for operationer. Det giver et overblik over hvordan du tilslutter disse komponenter og en oversigt over, hvordan du opretter brugerdefinerede Hjælp. 

<a name="help-architecture"></a>Hjælp-arkitektur
-----------------

Følgende illustration viser delene af Dynamics-365 operationer Hjælp-systemet. Hjælpesystemet i produktet trækker artikler fra Dynamics-365 for operationer sted på https://docs.microsoft.com samt opgave hjælpelinjer, der er gemt i Forretningsplanlægningsmodel proces i livscyklus Services (LCS). 
**Bemærk:** funktionerne, der vises i diagrammet med en stjerne (\*) er planlagt, men er endnu ikke tilgængelige. [![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Tilslutning af Hjælp-systemet
Ved hjælp af den **systemparametre** side, systemadministratorer oprette forbindelse til delene af Hjælp-systemet til en implementering. [![Systemet parameterformen med indstillinger for Hjælp](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) på den **systemparametre** side, skal du følge disse trin:

1.  **Vigtigt:** første gang, du åbner den **at** under fanen skal du forbinde levetidsservices. Sørg for at klikke på hyperlinket i formularen, venter på forbindelsen, for at lukke dialogboksen og klik derefter på **OK** at komme til den **systemparametre** side. [![Forbindelse til LCS](./media/connect-to-lcs-crop-1024x365.png "forbindelse til LCS")](./media/connect-to-lcs-crop.png)
2.  Vælg det Lifecycle Services-projekt, der skal oprettes forbindelse til.
3.  Vælg BPM-biblioteker (inden for det valgte projekt), hvor der skal hentes opgaveregistreringer fra.
4.  Angiv visningsrækkefølgen for BPM-bibliotekerne. Dette bestemmer den rækkefølge, som opgaveregistreringer fra bibliotekerne vises i på ruden **Hjælp**.

Når du har udført disse trin, kan du åbne ruden **Hjælp** og klikke på fanen **Opgaveguider**. Nu kan du se opgaveguiderne, der gælder for den aktuelle side i Dynamics 365 for Operations. Hvis der ikke findes opgaveguider, kan du angive nøgleord for at indsnævre søgningen.

### <a name="showing-translated-task-guides"></a>Visning af oversatte opgaveguider

Oversatte opgave hjælpelinjer blev leveret i maj-2016 APQC samlet, og Kom godt i gang-biblioteket. Når du vil se den lokaliserede hjælp til opgaveguider i Dynamics 365 for Operations, skal du sørge for, at der er forbindelse til maj-biblioteket. Det sprog, der vises en vejledning til opgave i styres for hver bruger af sprogindstillinger under **indstillinger for**&gt;**indstillinger for**. **Bemærk:** Selvom mange opgaveguider er blevet oversat, vises navnene på de oversatte opgaveguider ikke i Dynamics 365 for Operations-klienten lige nu. Kun opgave hjælpelinjer, der blev udgivet i februar 2016 er også tilgængelig i oversættelse i maj biblioteket. Vi udsender et opdateret bibliotek med flere oversættelser.

-   Hvis en opgaveguide er blevet oversat, vises teksten i opgaveguiden på det valgte sprog, når du åbner denne opgaveguide.
-   Hvis en opgaveguide ikke er blevet oversat, er det kun noget af teksten (tekst i kontrolelementerne), der vises på det valgte sprog, når du åbner guiden.

## <a name="creating-custom-help"></a>Oprettelse af tilpasset hjælp
Du kan oprette en brugerdefineret hjælp til implementeringen af Dynamics 365 for Operations ved at oprette opgaveregistreringer, der afspejler din implementering, og gemme dem på et bibliotek i LCS Business Proces. Hvis du som partner fremmer et bibliotek til at være virksomhedens bibliotek og medtager det i en løsning, bliver det tilgængeligt for dine kunder. Du kan også oprette en kopi af det globale APQC Unified-bibliotek og derefter åbne kopien, åbne opgaveregistreringer fra det, redigere dem og gemme registreringerne med dine ændringer. Yderligere oplysninger finder du [hvordan du opretter en opgave optagelsen skal bruges som dokumentation eller uddannelse](../user-interface/task-recorder.md).

<a name="see-also"></a>Se også
--------

[Help overview](help-overview.md)

[Oversigt over optagelser](../user-interface/task-recorder.md)

[Sådan opretter du en opgaveregistrering, der kan bruges til dokumentation eller undervisning](../user-interface/task-recorder-training-docs.md)

[Oprette nye biblioteker til uddannelse for Dynamics 365 for operationer i levetidsservices ved hjælp af Arbejdsrutineoptager (eksternt link)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)


