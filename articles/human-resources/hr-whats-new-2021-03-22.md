---
title: Nyheder eller ændringer i Dynamics 365 Human Resources 22. marts 2021
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 22. marts 2021.
author: marcelbf
ms.date: 03/22/2021
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
ms.search.validFrom: 2021-03-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0f08dc966353cc612c8145f29e2cd8c303da5b359292a8f928d97f0e0de99585
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777082"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-22-2021"></a>Nyheder eller ændringer i Dynamics 365 Human Resources 22. marts 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I dette emne beskrives funktioner, som er nye eller ændrede, eller som kommer snart i Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2021-udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.4049.

### <a name="new-features"></a>Nye funktioner

Følgende funktioner er generelt tilgængelige med denne udgivelse.

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Mulighed for at gennemtvinge annullering og nulstilling af fastsiddende batchjob (560976) | NA | [Nulstille fastsiddende batchjob](./hr-admin-troubleshooting-batch-execution.md) |
| Mindre opdateringer af brugeroplevelsen til oprettelse af ny frynsegodeplan (419941) | NA | [Oprette en frynsegodeplan](hr-benefits-plans-setup.md) |

### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis dette emne, der omfatter fejlrettelser, som blev udført i buildet, efter at dette emne blev udgivet.

| Fejlnummer | Udsted |  Betegnelse |
| --- | --- | --- |
| 554239 | Forbedringer af ydeevne for enheder, der er relateret til tabellen **BusinessProcessTaskAssignment** | Forbedret ydeevne af enheder, der er relateret til tabellen **BusinessProcessTaskAssignment**, ved at føje foreslåede indeks til tabellen. |
| 566061 | Fjerne V2-enheds reservekode fra synkronisering om natten | Fjern V2-reservekoden til Dataverse-synkronisering om natten. Reserven er ikke længere nødvendig og forhindrer filtreret synkronisering i at fungere som forventet. Ændringen forbedrer ensartetheden af Dataverse-datasynkronisering. |
| 538024 | Frynsegodeplaner for medarbejdere > Fjern fejl ved udtjekning | Fejl er rettet, når du fjerner udtjekning for indstillingen Frynsegodeplan i formularen Medarbejderfrynsegoder. |
| 557965 | Arbejdsområdet **Frynsegoder**: Linket **Aktive livshændelser** skal altid være synligt i afsnittet **Links** | Har løst problem, hvor linket **Aktive livshændelser** var synligt i afsnittet **Links**, men der opstod en fejl under forsøget på at navigere, hvis funktionen **(forhåndsversion) Arbejdsområde for frynsegodeadministration** ikke var aktiveret. Du kan finde flere oplysninger om aktivering af arbejdsområdet i [Arbejdsområde for frynsegodeadministration](hr-benefits-management-workspace.md). |
| 556672 | Det er ikke muligt at behandle periodiseringer for en fratrådt medarbejder, når **Strømlinet medarbejderindtastning** er aktiveret i Funktionsstyring | Indstillingen for periodisering af orlovs- og fraværsplaner er føjet til **Flere indstillinger** under **Arbejdshistorik** for medarbejdere, når **Strømlinet medarbejderangivelse** er aktiveret i Funktionsstyring. |
| 562656 | Menupunktet **SysRecordChangeLogValidTimeState** skal medtages i en sikkerhedsrettighed og en udvidelse af sikkerhedsafgiften **SystemExternalBasicMaintain** | Rollerne for ikke-systemadministratorer mangler knappen **Vis ændringer** i formularer til datostyring. |
| 505989 | Behandling af livshændelser: Ændring af berettigelse ikke behandlet korrekt grundet anvendt dato | Har løst problem, hvor ændringen i berettigelsesbehandlingen var afhængig af stillingens startdato og ikke kun af den aktuelle stilling. |
| 562286 | Lad arbejder fratræde sender flere opdateringer til Dataverse | Når en arbejder fratræder, sendes der mere end én opdateringshandling til Dataverse, hvilket medfører to opdateringsbeskeder for samme ændring. Dette kan medføre flere udløsere, hvis et Power Automate-flow er konfigureret som udløser fra handlingen. |
| 527340 | Fejlen "DateTime, som ikke kan repræsenteres" vises, når der åbnes orlovs- og fraværstilmeldinger | Når du vælger orlovs- og fraværstilmelding, vises fejlen ikke længere. |
| 561663 | Øge ventetidsintervallet for klyngeklargøring | Forbedre infrastrukturens stabilitet og klargøringskonsistens med opdateringer til klyngeklargøring. |
| 486129 | Brugerdefinerede felter i **Stillinger > Administrer ændringer** kan ikke redigeres | Har løst et problem, hvor brugerdefinerede felter ikke kan redigeres under fanen **Administrer ændringer** for **Stillinger**. |

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