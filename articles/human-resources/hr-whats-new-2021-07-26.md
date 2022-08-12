---
title: Nyheder eller ændringer i Dynamics 365 Human Resources 26. juli 2021
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 26. juli 2021.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-26
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 14041dfc753b508a0d68b90ee99d79510d07e622
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070074"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-26-2021"></a>Nyheder eller ændringer i Dynamics 365 Human Resources 26. juli 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I denne artikel beskrives funktioner, der enten er nye, ændrede eller kommer snart i Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2021-udgivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.4384.

### <a name="new-features"></a>Nye funktioner

Følgende funktioner er generelt tilgængelige med denne udgivelse.

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Platform update 10.0.20 | -- | [Platformsopdateringer til version 10.0.20 af programmer til finans og drift (august 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20) |

### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis denne artikel til at omfatte fejlrettelser, som blev udført i buildet, efter at denne artikel blev udgivet.

| Fejlnummer | Problem |  Beskrivende tekst |
| --- | --- | --- |
| 600422 | Validering af lønadresser mislykkes for Klar til betaling. | Valideringen er opdateret, så der kun kræves én adresse af typen 'Bopælslokation for løn' og kun én adresse af typen 'Arbejdslokation for løn'. |
| 601226 | Problem med dataintegration: Eksportprojekt for lønintegration har ikke mulighed for at gøre det fulde push | Lønintegrationen med Ceridian DayForce foretog et trinvist push i stedet for et komplet push. Ceridian kræver altid fuld opdatering. Dette problem er nu løst, og enhederne i dataeksportprojektet vil ikke længere udføres med trinvist push. |
| 602272 | De felter, der er føjet til arbejdsområdet hos Medarbejderselvbetjening, mangler nu, og der kan ikke længere føjes felter til det | Vi har løst tilpasningsproblemet for Medarbejderselvbetjening. Der kan føjes nye felter til visningen, og eventuel eksisterende tilpasning kan ses af brugerne |
| 600711 | Felt til valg af halvdagsdefinition er aktiveret for anmodninger om orlov hele dagen | Dette problem er nu løst, så feltet til halvdagsdefinition nu kun er aktiveret, når medarbejdere vælger en orlovstype, hvor definitionen af en halv dag og halv dag som beløbsværdi er valgt |
| 602208 | Enheder for periodiseringssats viser timer i stedet for dage | Dette problem er nu løst. Formularen **Fravær** viser den korrekte orlovsenhed (timer eller dage) for kolonnen **Periodiseringssats**. |

## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering og deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Arbejdsområde for personalegodeadministration | [Arbejdsområdet Administration af frynsegoder (forhåndsversion)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbejdsområde for frynsegodeadministration](hr-benefits-management-workspace.md) |
| Aktivere forenklet lønintegration (API'er for lønintegration) | [Aktivere forenklet integration med lønudbydere](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lønintegration API](hr-admin-integration-payroll-api-introduction.md)|
|  Give en fraværsadministrator mulighed for at administrere orlov | [Give en fraværsadministrator mulighed for at administrere orlov](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Med denne version opdaterer vi visningen af arbejdsområdet for fraværsadministrator. Du kan finde flere oplysninger under [Konfigurere fraværschefrolle](https://go.microsoft.com/fwlink/?linkid=2168107).|
|  Konfigurere krav om vedhæftet fil pr. orlovstype | [Konfigurere krav om vedhæftet fil pr. orlovstype](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Konfigurere orlovs- og fraværstyper](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Konfigurer orlovsenheder pr. orlovstype | [Konfigurer orlovsenheder pr. orlovstype](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Konfigurere orlovs- og fraværstyper](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Gøre det muligt for medarbejdere at blive markeret som klar til at blive betalt | [Gøre det muligt for medarbejdere at blive markeret som klar til at blive betalt](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Klar til at betale](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Kommer snart

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2021 udgivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2021 frigivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

