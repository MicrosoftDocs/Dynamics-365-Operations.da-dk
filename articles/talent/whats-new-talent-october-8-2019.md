---
title: Nyheder eller ændringer i Dynamics 365 Talent (8. oktober 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 06758ff5eb1c00ae299b1b8849fcabb0cd9593e8
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896629"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-8-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (8. oktober 2019)

I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

De ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2542. Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="removal-of-benefits-open-enrollment-from-public-preview"></a>Fjernelse af åben tilmelding som frynsegoder fra offentlig prøveversion

Sammen med vores meddelelse i blogindlægget [Strategiske investeringer i Core HR som drivkraft bag ekspertise](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/) fjerner Microsoft frynsegoder som åben tilmeldingsfunktion fra offentlig prøveversion d. 18. oktober 2019. Der vil i stedet blive udgivet nye funktioner i fremtiden. Produktionens anvendelse af frynsegoder som åben tilmeldingsfunktion, der i øjeblikket findes i offentlig prøveversion, understøttes ikke. 

### <a name="common-data-service-integration-is-now-turned-off-by-default-on-new-provisions-343675"></a>Common Data Service-integration er nu som standard slået fra i nye hensættelser (343675)
 
Når der klargøres nye miljøer, er Common Data Service-integration nu slået fra. Du kan finde flere oplysninger under [Konfigurere Common Data Service-dataintegration](hr-common-data-service-integration.md).

### <a name="streamlined-employee-entry-and-navigation"></a>Strømlinet medarbejderangivelse og navigation

Funktionaliteten til medarbejdernes indtastning og navigation er nu tilgængelig i alle miljøer. Hvis du vil aktivere denne funktion, skal du gå til **Systemadministration \> Links \> Opsætning \> Systemparametre \> Funktioner i prøveversion** og vælge **Udvidet arbejderform og navigation**. Funktionen aktiveres derefter for alle brugere. Du kan deaktivere denne indstilling på et hvilket som helst tidspunkt.

Yderligere oplysninger finder du under [Strømlinet medarbejderangivelse](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry) i Dynamics 365: 2019 frigivelsesbølge 2-plan.

### <a name="attract-and-onboard-create-inactive-workers-in-core-hr-380517"></a>Attract og Onboard opretter inaktive arbejdere i Core HR (380517)

I denne uges udgivelse løses et problem, hvor Attract og Onboard opretter inaktive arbejdere i Core HR.

### <a name="the-workflow-fails-when-the-manager-is-signed-in-to-another-company-while-terminating-an-employee-346852"></a>Arbejdsgangen mislykkes, når lederen er logget på et andet firma, mens en medarbejderansættelse afsluttes (346852)

Arbejdsgangen mislykkes ikke længere på basis af den juridiske enhed, som lederen er logget på.

### <a name="missing-information-on-hcmonboardingworkerchecklisttaskentity-349591"></a>Der mangler oplysninger om HcmOnboardingWorkerChecklistTaskEntity (349591)

Denne version indeholder yderligere oplysninger om **HcmOnboardingWorkerChecklistTaskEntity**. Her er nogle eksempler:

- **Gruppenavn**, når den tildelte type er **gruppe**
- **Medarbejdernavn**, når den tildelte type er **medarbejder**
- **Ledernavn**, når den tildelte type er **leder**

### <a name="entities-arent-listed-in-alphabetical-order-in-common-data-service-administration-377414"></a>Enheder vises ikke i alfabetisk rækkefølge in Common Data Service Administration (377414)

Enheder vises nu i alfabetisk rækkefølge på siden **CDS Administration**.

### <a name="changing-the-employment-type-with-a-future-date-doesnt-allow-a-position-assignment-339958"></a>Ændring af ansættelsestypen med en fremtidig dato tillader ikke en stillingstildeling (339958)

Denne ændring giver mulighed for stillingstildelinger, når arbejdertyper ændres (f.eks. fra medarbejder til kontrahent).

### <a name="updating-the-common-data-service-leave-bank-transaction-entity-creates-a-new-record-in-talent-352938"></a>Når enheden for Common Data Service-orlovsbanktransaktion opdateres, oprettes en ny post i Talent (352938)

Orlovstransaktionen opdateres nu, når der oprettes en opdatering til Common Data Service i forbindelse med orlovsbanktransaktioner.

### <a name="the-title-of-attachments-for-feedback-items-shows-the-feedback-description-343765"></a>Titlen på vedhæftede filer til feedbackelementer viser beskrivelsen af feedback (343765)

Beskrivelsen af feedback vises ikke længere i titlen til vedhæftede filer.

### <a name="compensation-workflow-comments-field-shows-incorrect-content-339297"></a>Kompensationsarbejdsgangens kommentarfelt viser forkert indhold (339297)

Denne ændring viser indholdet af feltet **%HcmActionState.HcmWorkerActionComment.Comments%**.

### <a name="workcalendarentity-and-workcalendardayentity-arent-exposed-through-odata-376329"></a>WorkCalendarEntity og WorkCalendarDayEntity fremvises ikke gennem OData (376329)

I denne version er **WorkCalendarEntity** og **WorkCalendarDayEntity** nu tilgængelige via Open Data Protocol (OData).

### <a name="hcmworkerentity-is-slow-when-odata-is-used-375221"></a>HCMWorkerEntity er langsom, når OData bruges (375221)

Ændringer forbedrer ydeevnen af **HCMWorkerEntity**, når Microsoft Excel-projektmappedesigneren bruges.

### <a name="manager-performance-journal-entry-shows-an-error-after-deleting-a-performance-journal-and-creating-a-new-one-336061"></a>Kladdepost for leder-performance viser en fejl, efter at du har slettet en performance-kladde og oprettet en ny (336061)

Denne version retter et problem, der opstår, når én performance-kladde er slettet, og der oprettes en ny umiddelbart bagefter. Denne rettelse ændrer funktionaliteten i chefselvbetjening.

## <a name="coming-soon"></a>Kommer snart

### <a name="print-performance-reviews"></a>Udskiv performancegennemgange

Se [Udskrive performancegennemgange](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019 frigivelsesbølge 2-plan.
