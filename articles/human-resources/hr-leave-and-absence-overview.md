---
title: Oversigt
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 9a36f6b6ba696fa926ab3d6298568dddfce43a57
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008528"
---
# <a name="overview"></a>Oversigt

Dynamics 365 Human Resources hjælper dig med at give medarbejderne store orlovsfordele. Arbejdsområdet **Orlov og fravær** giver en fleksibel struktur til oprettelse af nye orlovsplaner, arbejdsgange til administration af anmodninger og en intuitiv selvbetjeningsside, hvor medarbejdere kan anmode om fritid. Analyse hjælper din organisation med at måle og overvåge orlovssaldi og forbrug for dine orlovsplaner.

## <a name="set-up-leave-and-absence"></a>Konfigurere orlov og fravær

Før du kan oprette orlovsplaner for dine medarbejdere, skal du udføre et par opsætningstrin:

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

- [Anmode om fridag](hr-employee-self-service-request-time-off.md)
- [Administrere anmodninger om orlov og fravær](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-preview-features"></a>Visningsfunktioner for orlov og fravær

Du kan afprøve nye visningsfunktioner for orlov og fravær i et **sandkasse**-miljø. Du kan finde oplysninger om aktivering af visningsfunktioner under [Administrere funktioner](hr-admin-manage-features.md). Visningsfunktionerne omfatter:

- **Orlovs- og fraværskalender** – Orlovs- og fraværsparametre flyttes fra **Personaleparametre** til en ny skærm kaldet **Orlovs- og fraværsparametre**. Den nye skærm indeholder en ny fane **Kalender**. Denne forhåndsvisning aktiverer kun et undersæt af parametrene. Du kan få adgang til den nye skærm fra fanen **Links** i arbejdsområdet **Orlov og fravær**. Kalenderne omfatter:
  - **Firmakalender** – viser alle anmodninger om medarbejderfridage. Personer med rollen **Personale** kan få adgang til denne kalender fra fanen **Links** i arbejdsområdet **Orlov og fravær**.
  - **Kalender for lederteam** – viser alle anmodninger om fridage i direkte rapporter. Ledere kan få adgang til kalenderen fra fanen **Mit team** i Medarbejderselvbetjening under **Orlov og fravær**. 

- **Feriekalendere for orlov og fravær** – Orlovstyper omfatter en ny indstilling, **Ferie**, der bruges sammen med arbejdstidskalenderen. Dage, der er defineret af helligdage og lukninger, er nu angivet som **Ferie**, når der genereres arbejdsdage. Når periodiseringer behandles, foretages der reguleringer af medarbejdere, der er tildelt til kalenderen, for at tage højde for helligdage, der ligger på en arbejdsdag.

- **Revision af orlovsperiodisering** – En ny skærm giver dig mulighed for at se, hvornår periodiseringer er behandlet og slettet, både af alle medarbejdere og individuelle medarbejdere. Du kan få adgang til denne nye skærm fra fanen **Links** i arbejdsområdet **Orlov og fravær**.

- **Sletning af orlovsperiodisering** – Du kan nu slette periodiseringsposter for bestemte orlovsplaner. Du kan få adgang til denne nye indstilling fra fanen **Links** i arbejdsområdet **Orlov og fravær**. For de enkelte medarbejdere vises denne indstilling i **Orlov og fravær**-grupperingen i medarbejderprofilen. 

- **Afrunding af orlovsperiodisering** – Nye indstillinger for **Orlovstype** definerer, hvilken type afrundingsperiodisering der skal bruges, plus decimalpræcisionen i afrunding under periodiseringsprocessen. Når periodiseringer behandles, anvendes afrundingen og præcisionen til periodiseringsposterne. 

- **Konfigurer flere orlovstyper i en enkelt orlovsplan** – En ny kolonne i orlovsperiodiseringtidsplanen for orlovstyper giver dig mulighed for at definere flere orlovstyper i en orlovs- og fraværsplan med forskellige periodiseringstidsplaner. Det tidligere felt **Orlovstype** er fjernet. I medarbejderens tilmelding vises saldi for orlovstyperne nu i en tabel i stedet for øverst på skærmen.

  > [!IMPORTANT]
  > Du kan ikke deaktivere denne funktion, når du har aktiveret den.

- **Brug en medarbejders fuldtidsækvivalent for periodisering**– En ny kolonne i orlovsperiodiseringtidsplanen gør det muligt at bruge fuldtidsækvivalent til periodisering. Når periodiseringer behandles, bruger programmet medarbejderens primære stilling og den angivne fuldtidsækvivalent til at fastlægge det forholdsmæssige periodiseringsbeløb.

  > [!NOTE]
  > Denne funktion er kun tilgængelig, hvis du aktiverer **Konfigurer flere orlovstyper i en enkelt orlovsplan**. 
