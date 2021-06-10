---
title: Nyheder eller ændringer i Dynamics 365 Human Resources 22. oktober 2020
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 22. oktober 2020.
author: jcart1106
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 69534ce0024986e0b78932b3957023fcb9b8a584
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055598"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-22-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources 22. oktober 2020

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives funktioner, som er nye eller ændrede, eller som kommer snart i Dynamics 365 Human Resources. Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2020-udgivelsesbølge 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.3680.

### <a name="new-features"></a>Nye funktioner

Følgende funktioner er generelt tilgængelige med denne udgivelse.

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Platform update 10.0.14(38) | -- | [Platformsopdateringer til version 10.0.14 af Finance and Operations-apps (november 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14.md) |
| Forbedringer af arbejdsprocesser for organisations- og personalestyring | [Forbedringer af arbejdsprocesser for organisations- og personalestyring](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurationsindstilling til placering af listen Workflowopgaver, der er tildelt til mig](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |


### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis dette emne, der omfatter fejlrettelser, som blev udført i buildet, efter at dette emne blev udgivet.

| Fejlnummer| Fejl  | Beskrivelse|
| --- | --- | --- |
| 437922 | Import af FMLA-timer ved hjælp af DMF-enheden resulterer i en skrivebeskyttelsesfejl. | Brug af FMLA-timerenheden til import af timer, der er knyttet til en FMLA-sag, mislykkedes. Vi har tilføjet logik for at sikre, at de importerede timer ikke overstiger de timer, der er tilbage i sagen. |
| 512019 | Forkert beløb for **Sidste overførsel**. | Hvis du på siden **Fritid** ændrede **Pr. dato** til den første dag i næste regnskabsperiode, blev der vist et forkert beløb i **Sidste overførsel** for typen **Årlig orlov**. Det korrekte beløb vises nu. |
| 458639 | Enheden **Arbejderkontakter** understøtter ikke ændringssporingstilstand. | Vi har opdateret enheden **Arbejderkontakter**, så du kan bruge den til dine egne database-scenarier (BYOD).|
| 505347 | Uddannelsesledere har kunnet sende en orlovsanmodning for en medarbejder, når den strømlinede arbejderfunktion var aktiveret. | Andre roller end personalemedarbejder og personalechef har ikke tilladelse til at sende time0off-anmodninger for medarbejdere. |
| 513490 | Logføring af frynsegodeadministration: Tilføj logføring for planer uden disponeringsindstillinger. | Vi har aktiveret logføringsresultater for **Plan uden disponeringsindstillinger**. De vises nu i tabellen **Procesresultater** og sorteres korrekt, så de vises øverst. |
| 517021 | Der kan ikke vælges flere planer med den samme **Plantype**-kode, hvis **Plantype** har én tilmelding pr. type. | Vi har ændret begrænsningerne for valg af planer, hvor kun én tilmelding er tilladt. Begrænsningerne er nu på **Kode for plantype**-niveau i stedet for **Plantype**. Denne ændring tillader planer som HSA og FSA, som har samme type, men du kan give dem en særskilt **Kode for plantype**. På denne måde kan du vælge dem begge til den samme tilmeldingsperiode. |
| 444791 | Kompensation vises ikke i Employee Self-Service, når **Begrænset adgang** er slået til i kompensationsplanen. | I **Kompensation**-kortet i Employee Self-Service vises det aktuelle kompensationsbeløb og stigningsprocenten som "0", hvis medarbejderen er tilmeldt en plan, hvor **Begrænset adgang** er aktiveret og tildelt til bestemte roller. Vi har løst dette problem, så medarbejderen og lederen altid kan se kompensationsdetaljer for sig selv og deres direkte rapporter. |
| 457542 | Opdatering af kursusoplysninger, når kurset er afsluttet, opdaterer ikke de samme oplysninger for den medarbejder, der har udført kurset. | Medarbejderoplysningerne opdateres nu korrekt, når du ændrer kursusdetaljer, efter at et kursus er afsluttet og genåbnet. |
| 515342 | Kan ikke indsætte data via **CDSLeaveRequestDetailEntity**. Firmaet blev ikke fundet eller findes ikke. | Du kan nu bruge **CDSLeaveRequestDetailEntity** til at indsætte data. |
| 514743 | Fejl i **E-mailparameter**-formular ved brug af Microsoft Exchange. | Meddelelsen "Filer eller assembly kan ikke indlæses..." vises på siden **E-mailparametre**, når e-mailudbyderen er indstillet til **Exchange**. Denne rettelse bevirker også, at siden **E-mailparametre** kan indlæses og gemmes som forventet. |


## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering og deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Human Resources-app i Microsoft Teams | [Medarbejderorlovs- og -fraværsoplevelse i Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app i Teams](./hr-admin-teams-leave-app.md)<br>[Administrere fraværsanmodninger i Teams](hr-teams-leave-app.md) |
| Udvidede anmodninger om og godkendelser af arbejdsprocesser | [Forbedringer af arbejdsprocesser for organisations- og personalestyring](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurationsindstilling til placering af listen Workflowopgaver, der er tildelt til mig](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Virtuelle enheder i Dataverse for Human Resources | [Udvide Dynamics 365 Human Resources-kernedata i Dataverse](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Konfigurere Dataverse virtuelle enheder](hr-admin-integration-common-data-service-virtual-entities.md) |
| Integration med LinkedIn Talent Hub | [Integration med LinkedIn Talent Hub](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integrere med LinkedIn Talent Hub](./hr-admin-integration-linkedin.md) |
| Brugerdefinerede links i selvbetjening for leder | [Brugerdefinerede links i selvbetjening for leder](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Brugerdefinerede links i selvbetjening for leder](./hr-employee-manager-self-service-custom-links.md) |

## <a name="coming-soon"></a>Kommer snart

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2020 udgivelsesbølge 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2020 frigivelsesbølge 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]