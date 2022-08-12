---
title: Nyheder eller ændringer i Dynamics 365 Human Resources 5. oktober 2021
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 5. oktober 2021.
author: marcelbf
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba24afd16a471abb36a6f7bc9a8610acec374190
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067965"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-5-2021"></a>Nyheder eller ændringer i Dynamics 365 Human Resources 5. oktober 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I denne artikel beskrives funktioner, der enten er nye, ændrede eller kommer snart i Microsoft Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2021-udgivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.4485.

### <a name="new-features"></a>Nye funktioner

Følgende funktioner er generelt tilgængelige med denne udgivelse.

| Funktion | Frigivelsesplan | Dokumentation |
|---|---|---|
| Platform update 10.0.21 (45) | -- | [Platformsopdateringer til version 10.0.21 af programmer til finans og drift (oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) |


### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis denne artikel til at omfatte fejlrettelser, som blev udført i buildet, efter at denne artikel blev udgivet.

| Fejlnummer | Problem | Beskrivende tekst |
|---|---|---|
| 598896 | Medarbejderbeløbet vises først, når medarbejderen har fuldført tilmeldingen. | På siden **Medarbejderselvbetjening** blev medarbejderbeløbet for frynsegodet ikke vist. Siden **Frynsegodeselvbetjening** viser nu medarbejderbeløbet.  |
| 613440 | Kan ikke eksportere data fra **Datastyring** | Når data eksporteres for et projekt i **Datastyring**, mislykkes eksporten uventet. |
| 618327 | Lukkede og fremtidige perioder vises på **parametersiden Rapporter** for oversigten over frynsegoder | Når du navigerer til **Frynsegodeopgørelse** i **Medarbejderselvbetjening**, viser siden **Rapportparametre** de **poster, der skal medtages** og **køres i oversigtspanelerne i baggrunden**. Disse afsnit blev fjernet.|
| 618326 | Forkerte **Rapportparametre** vises i **Medarbejderselvbetjening** for frynsegodeopgørelse.| Når brugeren navigerer til destinationssiden med **Frynsegodeopgørelsesrapporten**, kan brugeren vælge perioder for de frynsegodeplaner, der er lukket eller dateret i fremtiden, hvilket resulterer i en tom side. Det er kun den aktuelle frynsegodeplanperiode, der skal vises på listen. |

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
|Fejl ved e-mailrapport med **GER-rapporteringsdestination**. | Opgørelsen af frynsegoder kan angives til at bruge e-mailparametre på siden **GER-rapporteringsdestinationer**. Når opsætningen og udskrivningen af rapporten er fuldført, modtager brugeren en formateringsfejl, og opgørelsen af frynsegoder vil ikke blive sendt.|

## <a name="feature-management-changes"></a>Ændringer i funktionsstyring

| Funktion | Beskrivelse |
|---|---|
|Vis udvidede rapporter om ydeevnejournaler | Denne funktion aktiveres som standard i denne version. |

## <a name="coming-soon"></a>Kommer snart

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2021 udgivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funktion | Detaljer |
|---|---|
| Platform update 10.0.22 (46) | Opdatering med platformsopdatering 10.0.22 er planlagt til at starte med servicefrigivelse den 1. november 2021. Du kan få mere at vide i [Platformsopdateringer til version 10.0.22 af programmer til finans og drift (november 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22). |



## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2021 frigivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

