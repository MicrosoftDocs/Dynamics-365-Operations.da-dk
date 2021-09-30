---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (6. september 2021)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 6. september 2021.
author: marcelbf
ms.date: 09/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2add53b4b014cb65caacff03bf175078d2b70d8f
ms.sourcegitcommit: a73df4ddc7f8ddc9e37269c0236dc1bb9b7c7966
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485901"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-6-2021"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (6. september 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I dette emne beskrives funktioner, som er nye eller ændrede, eller som kommer snart i Microsoft Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2021-udgivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.4443.

### <a name="new-features"></a>Nye funktioner

Følgende funktioner er generelt tilgængelige med denne udgivelse.

| Funktion | Frigivelsesplan | Dokument |
|---|---|---|
| Give en fraværsadministrator mulighed for at administrere orlov | [Give en fraværsadministrator mulighed for at administrere orlov](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | I denne version opdaterer vi visningen af arbejdsområdet for fraværsadministrator. Du kan finde flere oplysninger under [Konfigurere fraværschefrolle](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Konfigurere krav om vedhæftet fil pr. orlovstype | [Konfigurere krav om vedhæftet fil pr. orlovstype](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) | [Konfigurere orlovs- og fraværstyper](https://go.microsoft.com/fwlink/?linkid=2168108) |
| Konfigurer orlovsenheder pr. orlovstype | [Konfigurer orlovsenheder pr. orlovstype](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) | [Konfigurere orlovs- og fraværstyper](https://go.microsoft.com/fwlink/?linkid=2168215) |

### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis dette emne for at medtage rettelser i buildet, som er foretaget, efter dette emne blev udgivet.

| Fejlnummer | Emne | Betegnelse |
|---|---|---|
| 610128 | Fejl under udgivelse af data ved brug af HcmDiscussionOverallCommentEntity | Når data publiceres fra en Excel-projektmappe til enheden HcmDiscussionOverallCommentEntity, opstår følgende fejl: "Der kan ikke findes datakildepost af typen HcmTopicOverrall." |
| 589073 | EEO-1 rapporten tæller "Ikke specifik" og tomme værdier for **Køn** som "Hunkøn"-værdi. | Hvis **Hankøn** ikke er angivet i feltet **Køn**, vil rapporten EEO-1 generere en standardværdi af **Hunkøn**. |
| 589617 | Kortsaldoen for fritid, Tilgængelig for køb- og Tilgængelig for salg-saldi vises ikke, når brugerroller er begrænset til en bestemt juridisk enhed. | Hvis brugeren (medarbejderrollen) er begrænset til en bestemt juridisk enhed, vises saldi ikke korrekt på kortet **Fritidssaldi** og i felterne **Tilgængelig for køb** og **Tilgængelig for salg**. |
| 604310 | Fanen Fraværsadministrator skal være skjult, når brugeren ikke har fået tildelt et fraværshierarki. | Fanen **Fraværsadministrator** skal være skjult for en given juridisk enhed på selvbetjeningsportalen, medmindre parameteren for hele firmaet er aktiveret, og der er knyttet mindst ét fraværshierarki til brugeren. |

## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering eller deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
|---|---|---|
| Aktivere forenklet lønintegration (API'er for lønintegration) | [Aktivere forenklet integration med lønudbydere](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lønintegration API](hr-admin-integration-payroll-api-introduction.md) |
| Arbejdsområde for frynsegodeadministration | [Arbejdsområdet Administration af frynsegoder (forhåndsversion)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbejdsområde for frynsegodeadministration](hr-benefits-management-workspace.md) |
| Gøre det muligt for medarbejdere at blive markeret som klar til at blive betalt | [Gøre det muligt for medarbejdere at blive markeret som klar til at blive betalt](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Klar til at betale](/dynamics365/human-resources/hr-compensation-payroll) |
| Brugerdefinerede felter i Berettigelse |[Understøttelse af brugerdefinerede felter for behandling af berettigelse](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Bruge brugerdefinerede felter i behandling af berettigelse](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |

## <a name="coming-soon"></a>Kommer snart

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2021 udgivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funktion | Detaljer |
|---|---|
| Platform update 10.0.21 (45) | Udrulning af platformsopdatering 10.0.21 er planlagt til at starte med servicefrigivelse den 4. oktober 2021. Få flere oplysninger under [Platformsopdateringer for version 10.0.21 af Finance and Operations-apps (oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
| Frynsegodeopgørelse | Frynsegodeopgørelse til visning af en medarbejders aktuelle valg af frynsegode. Yderligere oplysninger finder du i [Frynsegodeopgørelse](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) i frigivelsesbølgens dokument. |

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2021 frigivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
