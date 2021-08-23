---
title: Nyheder eller ændringer i Dynamics 365 Human Resources 8. marts 2021
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 8. marts 2021.
author: marcelbf
ms.date: 03/08/2021
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
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 133cfffadabade8f7770b4853e14b769c5b961370546e3104d6db26bc0c6331a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719062"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-08-2021"></a>Nyheder eller ændringer i Dynamics 365 Human Resources 8. marts 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I dette emne beskrives funktioner, som er nye eller ændrede, eller som kommer snart i Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2021-udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.4017.

### <a name="new-features"></a>Nye funktioner

Følgende funktioner er generelt tilgængelige med denne udgivelse.

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Visning af orlov for ledere på tværs af firmaet | [Visning af orlov for medarbejdere på tværs af firmaet](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurere parametre for orlov og fravær](./hr-leave-and-absence-parameters.md) |

### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis dette emne, der omfatter fejlrettelser, som blev udført i buildet, efter at dette emne blev udgivet.

| Fejlnummer | Udsted |  Beskrivelse |
| --- | --- | --- |
| 486611 | Orlov vises på orlovskalenderen, når **Deaktiver orlov på alle kalendere** er aktiveret | Hvis **Deaktiver orlov på alle kalendere** er aktiveret, vises orlovsoplysningerne ikke længere, når funktionen til forbedringer af orlovskalenderen er aktiveret.|
| 508972 | Enheden Banktransaktion for orlov og fravær mangler validering af tilmelding | Når du bruger enheden Banktransaktion for orlov og fravær, kan de medarbejdere, der ikke er tilmeldt en plan, ikke længere importeres. |
| 554854 | Opdatere kalender i fejl for ansættelsesenheden, hvis standarden af Juridisk enhed i Brugerindstillinger er forskellig | Hvis du bruger enheden Ansættelse til at opdatere kalenderen for en medarbejder, vises der ikke længere en fejl, hvis den juridiske standardenhed i brugerindstillingerne er forskellig. |
| 558347 | "Der kan ikke oprettes en post i Formkonfigurationer (FormRunConfiguration)" vises, når startsiden indlæses. | Personlige tilpasninger viser fejlen "Der kan ikke oprettes en post i Formkonfigurationer (FormRunConfiguration)", når startsiden indlæses. |
| 557327 | Arbejdsområdet Frynsegodeadministration: Mellemrum vises over gitteret. | Har løst problemer med brugeroplevelse af et uønsket mellemrum, der vises i tabelgittergrænserne i arbejdsområdet Frynsegoder. |
| 557334 | Arbejdsområdet Frynsegodeadministration: Rullelisten **Periode** skal kun vises under fanen **Oversigt** | Rullelisten **Periode** vises nu kun for frynsegolder, når fanen **Oversigt** er aktiv i arbejdsområdet Frynsegoder, og ikke i afsnittene **Procesresultater** og **Links**. |
| 557336 | Arbejdsområdet Frynsegodeadministration: Teksten **Åbn tilmelding med planer, der er tjekket ud** er afkortet i feltvisningen | Har ændret tekst i feltvisningen til **Planer, der er tjekket ud...åben tilmelding** for at undgå unødig afkortning af kontekst. |

## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering og deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Arbejdsområde for personalegodeadministration | [Arbejdsområdet Administration af frynsegoder (forhåndsversion)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbejdsområde for personalegodeadministration](hr-benefits-management-workspace.md) |
| Begrænse medarbejdere i at redigere forretningskontaktoplysninger | [Begrænse medarbejdere i at redigere forretningskontaktoplysninger](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Begrænse redigering af personlige oplysninger](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Kommer snart

| Funktion | Detaljer |
| --- | --- |
| Færdigheder, der angives af en leder for deres medarbejdere, kan godkendes automatisk af et arbejdsflow | Kommer snart. |

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2021 udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2021 frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]