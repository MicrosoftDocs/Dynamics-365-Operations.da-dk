---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (20. september 2021)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 20. september 2021.
author: marcelbf
ms.date: 09/20/2021
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
ms.search.validFrom: 2021-09-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3f4fc4768f8c96678b216709f78af6d3ddfd4132
ms.sourcegitcommit: ba8ca42e43e1a5251cbbd6ddb292566164d735dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/25/2021
ms.locfileid: "7556927"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-20-2021"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (20. september 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I dette emne beskrives funktioner, som er nye eller ændrede, eller som kommer snart i Microsoft Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2021-udgivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.4464.

### <a name="new-features"></a>Nye funktioner

Følgende funktioner er generelt tilgængelige med denne udgivelse.

| Funktion | Frigivelsesplan | Dokumentation |
|---|---|---|
| Aktivere forenklet lønintegration (API'er for lønintegration) | [Aktivere forenklet integration med lønudbydere](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lønintegration API](hr-admin-integration-payroll-api-introduction.md) |
| Gøre det muligt for medarbejdere at blive markeret som klar til at blive betalt | [Gøre det muligt for medarbejdere at blive markeret som klar til at blive betalt](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Klar til at betale](/dynamics365/human-resources/hr-compensation-payroll) |

### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis dette emne for at medtage rettelser i buildet, som er foretaget, efter dette emne blev udgivet.

| Fejlnummer | Emne | Beskrivelse |
|---|---|---|
| 619774 | Redigering af adressebeskrivelsen synkroniseres ikke til Dataverse i realtid. | Når du redigerer beskrivelsen af en arbejderadresse, synkroniseres den opdaterede beskrivelse ikke i realtid til Dataverse. Abonnementet i tabellen **Logistiklokation** er opdateret, så der sendes en opdatering. |
| 614603| Der vises en fejl på siden **Arbejder**, når parameteren **Arbejders personalehandlinger** ikke er valgt. | Ved ansættelse af en ny arbejder eller ved navigering til **arbejdersiden** vises følgende fejl, "**Feltmedarbejderhandlingstype** skal udfyldes", også selvom **personalehandlinger** er deaktiveret. |
| 615367 | Under fanen **Godkendt fritid** vises en advarsel, og der vises en forkert visning. | Hvis orlovsenheden er angivet til **Dage**, før funktionen **Konfigurer orlovsenheder pr. orlovstype**, vises der en ugyldig advarsel og ugyldige kolonner under fanen **Godkendt fri**. |


## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering eller deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
|---|---|---|
| Arbejdsområde for personalegodeadministration | [Arbejdsområdet Administration af frynsegoder (forhåndsversion)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbejdsområde for frynsegodeadministration](hr-benefits-management-workspace.md) |
| Brugerdefinerede felter i Berettigelse |[Understøttelse af brugerdefinerede felter for behandling af berettigelse](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Bruge brugerdefinerede felter i behandling af berettigelse](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |
| Frynsegodeopgørelse |[Frynsegodeopgørelse](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) | [Frynsegodeopgørelse](hr-benefits-statement.md) |

### <a name="benefits-statement-known-issues"></a>Kendte problemer i forbindelse med opgørelse af frynsegoder

| Emne | Beskrivelse |
|---|---|
| Siden **Rapportparametre** i **Medarbejderselvbetjening** for frynsegodeopgørelse er ikke korrekt. | Når du navigerer til **Frynsegodeopgørelse** i **Medarbejderselvbetjening**, viser siden **Rapportparametre** de **poster, der skal medtages** og **køres i oversigtspanelerne i baggrunden**.  Disse skal fjernes. |
| Lukkede og fremtidige perioder vises på **parametersiden Rapporter** for oversigten over goder. | Når brugeren navigerer til destinationssiden med **Frynsegodeopgørelsesrapporten**, kan brugeren vælge perioder for de frynsegodeplaner, der er lukket eller dateret i fremtiden, hvilket resulterer i en tom side. Det er kun den aktuelle frynsegodeplanperiode, der skal vises på listen. |
|Fejl ved e-mailrapport med GER-rapporteringsdestination. | Opgørelsen af frynsegoder kan angives til at bruge e-mailparametre på siden **GER-rapporteringsdestinationer**. Når opsætningen og udskrivningen af rapporten er fuldført, modtager brugeren en formateringsfejl, og opgørelsen af frynsegoder vil ikke blive sendt.|


## <a name="coming-soon"></a>Kommer snart

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2021 udgivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funktion | Detaljer |
|---|---|
| Platform update 10.0.21 (45) | Udrulning af platformsopdatering 10.0.21 er planlagt til at starte med servicefrigivelse den 4. oktober 2021. Få flere oplysninger under [Platformsopdateringer for version 10.0.21 af Finance and Operations-apps (oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
|Vis udvidede rapporter om ydeevnejournaler | Denne funktion aktiveres som standard ved næste udrulning. |


## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2021 frigivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
