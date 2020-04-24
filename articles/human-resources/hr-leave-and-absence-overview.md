---
title: Overblik
description: I Dynamics 365 Human Resources giver arbejdsområdet Orlov og fravær en fleksibel struktur til oprettelse af nye orlovsplaner, arbejdsgange til administration af anmodninger og en intuitiv selvbetjeningsside, hvor medarbejdere kan anmode om fritid.
author: andreabichsel
manager: AnnBe
ms.date: 04/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5f7ba32b31a67d81ee5be568b0e64842f343f96b
ms.sourcegitcommit: 9940ca772807d3c4e1ff3bf47f45b7251c4469ac
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/04/2020
ms.locfileid: "3226224"
---
# <a name="overview"></a>Overblik

Dynamics 365 Human Resources hjælper dig med at give medarbejderne store orlovsfordele. Arbejdsområdet **Orlov og fravær** giver en fleksibel struktur til oprettelse af nye orlovsplaner, arbejdsgange til administration af anmodninger og en intuitiv selvbetjeningsside, hvor medarbejdere kan anmode om fritid. Analyse hjælper din organisation med at måle og overvåge orlovssaldi og forbrug for dine orlovsplaner.

## <a name="set-up-leave-and-absence"></a>Konfigurere orlov og fravær

Før du opretter orlovsplaner for dine medarbejdere, skal du udføre et par opsætningstrin:

- [Konfigurere parametre for orlov og fravær](hr-leave-and-absence-parameters.md)
- [Oprette en arbejdstidskalender](hr-leave-and-absence-working-time-calendar.md)
- [Oprette en arbejdsgang for orlovsanmodninger](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>Oprette og administrere orlovsplaner

Før du opretter orlovsplaner for medarbejderne, skal du oprette orlovs- og fraværstyper. Når du har oprettet en orlovsplan, kan du tilmelde medarbejderne til planen. Du kan også køre periodiseringsprocessen, oprette påmindelser og få vist analyser for dine planer.

- [Konfigurere orlovs- og fraværstyper](hr-leave-and-absence-types.md)
- [Oprette en orlovs- og fraværsplan](hr-leave-and-absence-plans.md)
- [Tildele arbejdere til en orlovsplan](hr-leave-and-absence-enroll.md)
- [Periodisere orlovs- og fraværsplaner](hr-leave-and-absence-accrue.md)
- [Få vist analyse for orlov og fravær](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>Anmode om fridage og administrere anmodninger

Dine medarbejdere kan sende anmodninger om fritid, og du kan administrere dem i arbejdsområdet **Medarbejderselvbetjening**.

- [Anmod om fridag](hr-employee-self-service-request-time-off.md)
- [Administrere anmodninger om orlov og fravær](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-known-issues"></a>Kendte problemer ved Orlov og fravær

### <a name="rounding-precision"></a>Afrundingspræcision

Du kan ikke indstille **Afrundingspræcision**, når du indstiller **Afrundingstype**. Du kan kun indstille **Afrundingspræcision** vha. enheden **Orlov- og fraværstype** . 

1. Fra **Orlovs- og fraværstyper** skal du vælge **Åbn i Excel** for at åbne objektet **Orlov og fraværstype**.

2. Når filen er åbnet og er aktiveret, skal du vælge **Design**.

3. Vælg blyanten for at redigere i tabellen **Orlovs- og fraværstype**.

4. Vælg **Afrundingspræcision** og **Afrundingstype**, og vælg derefter **Tilføj** for at føje til listen over felter.

5. Vælg **Opdater**, og vælg derefter **Udført**.

6. Angiv eller vælg **Afrundingstype** for hver orlovstype, hvis de ikke allerede er angivet. 

7. Angiv **Afrundingspræcisionen** for de relevante typer.

8. Vælg **Udgiv** for at sende ændringerne til Human Resources.

## <a name="leave-and-absence-preview-features"></a>Visningsfunktioner for orlov og fravær

Du kan afprøve nye visningsfunktioner for orlov og fravær i et **sandkasse**-miljø. Du kan få oplysninger om aktivering af visningsfunktioner under [Administrere funktioner](hr-admin-manage-features.md). Visningsfunktionerne omfatter:

- **Orlovssuspension** – Du kan afbryde orlov og fravær i personale for en medarbejder. Når du suspendere orlov, stoppes orloven for de valgte orlovstyper. Hvis suspensionen finder sted, når der foretages en periodisering, opretter suspensionen en forholdsmæssig justering til medarbejderens orlov. 

- **Overføre regler** – Du kan angive en orlovstype for overførselssaldi, hvor gennemførte reguleringer overføres. Hvis en medarbejder f.eks. overfører 10 dage, kan du vælge en anden orlovstype for disse 10 dage. 