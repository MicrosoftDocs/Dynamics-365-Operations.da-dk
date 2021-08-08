---
title: Konfigurere rollen Fraværsadministrator
description: I dette emne forklares det, hvordan rollen Fraværsadministrator defineres for styring af medarbejderorlov.
author: hasrivas
ms.date: 07/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace, LeaveAbsenceManager
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8a8250b36d2774ac308637253b780592df316cd
ms.sourcegitcommit: 86d38cf57abe768e5bccde48b28280bc2224080c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/19/2021
ms.locfileid: "6639600"
---
# <a name="configure-the-absence-manager-role"></a>Konfigurere rollen Fraværsadministrator

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

I nogle organisationer administrerer personalechefer muligvis ikke orlov for deres team. I stedet kan en fraværsadministrator håndtere denne proces for teammedlemmer på tværs af flere afdelinger og teams. Fraværsadministratorer har følgende muligheder for orlovsstyring:

- Gennemse og godkend fridage baseret på et alternativt hierarki.
- Få vist saldi for teammedlemmer.
- Få vist fraværskalenderen.

## <a name="turn-on-the-feature"></a>Slå funktionen til

1. I arbejdsområdet **Systemadministration** skal du vælge **Funktionsstyring**.

2. Aktivér **(Forhåndsversion) Fraværsadministrator for at administrere orlov** under fanen **Funktionsstyring**.

## <a name="define-a-custom-hierarchy"></a>Definere et brugerdefineret hierarki

Funktionen for fraværsadministrator bruger et brugerdefineret hierarki, der skal konfigureres.

1. Vælg **Stillingshierarkityper** i arbejdsområdet **Organisationsadministration**.

2. Opret en stillingshierarkitype med navnet **Orlov**.

3. Vælg **Parametre for orlov og fravær** under **Links** i arbejdsområdet **Orlov og fravær**.

4. Vælg den hierarkitype **Orlov**, som du oprettede tidligere, på rullelisten **Fraværshierarki** under fanen **Generelt**. Denne tilknytning af orlovshierarki skal fuldføres for hver juridisk enhed, hvor funktionen til fraværsstyring anvendes.

Når hierarkitypen er defineret, skal stillingshierarkirapporten tildeles stillingen.

1. Vælg **Alle stillinger** i arbejdsområdet **Organisationsadministration**.

2. Vælg den stilling, som orlovshierarkiet skal føjes til.

3. Vælg **Tilføj** på fanen **Relationer**.

4. I feltet **Hierarkinavn** skal du vælge **Orlov**.

5. Vælg en stilling i feltet **Rapporter til stilling**. Arbejderens navn udfyldes automatisk, når du har valgt en stilling.

## <a name="assign-the-absence-manager-role-to-a-user"></a>Tildele rollen Fraværsadministrator til en bruger

Rollen Fraværsadministrator skal tildeles medarbejdere, for at de kan godkende eller afvise orlovsanmodninger.

1. Vælg **Links** i arbejdsområdet **Systemadministrator**.

2. Vælg linket **Brugere** under **Brugere**.

3. Vælg den bruger på listen, der skal tildeles rollen Fraværsadministrator.

4. Vælg **Tildel roller** på fanen **Brugers rolle**.

5. Vælg rollen **Fraværsadministrator** på listen. Vælg derefter **OK**.

    > [!IMPORTANT]
    > Kontrollér, at rollen Medarbejder også er tildelt til den bruger, du tildeler rollen Fraværsadministrator. Ellers kan arbejderen ikke bruge funktionen.

6. Når du har oprettet orlovshierarkiet, kan du få vist den ved at følge disse trin:

    1. Vælg **Stillingshierarki** i arbejdsområdet **Organisationsadministration**.
    
    2. I feltet **Hierarkitype** skal du vælge **Orlov**.

## <a name="absence-manager-workspace"></a>Arbejdsområde for fraværsadministrator

I arbejdsområdet **Medarbejderselvbetjening** viser fanen **Fraværsadministrator** fraværsoplysninger om de medarbejdere, der er tildelt fraværsadministratoren i orlovshierarkiet.

Under fanen **Orlov og fravær** er følgende indstillinger tilgængelige for hver medarbejder:

- **Fridage** – Få vist saldi, godkendt fritid, fritidsanmodninger for den valgte medarbejder.
- **Orlovssaldi** – Få vist en liste over saldi for de forskellige orlovsplaner for den valgte medarbejder.

## <a name="approve-time-off-requests"></a>Godkende anmodninger om fridage

Fraværsadministratorer kan godkende eller afvise anmodninger om fridage for medarbejdere. De kan også oprette anmodninger på vegne af medarbejdere efter behov.

> [!IMPORTANT]
> Før fraværsadministratorer kan godkende eller afvise anmodninger om fridage, skal arbejdsgangen for orlovsanmodninger være konfigureret til at tildele dem arbejdselementer for orlovsanmodninger med henblik på gennemsyn.
>
> 1. Vælg eller opret arbejdsgangen for orlovsanmodning på siden **Arbejdsgange for Human Ressources**.
> 2. Vælg indstillingen **Tilknyt hierarki**, og vælg derefter **Orlov** i feltet **Hierarkinavn**.
> 3. Opdater arbejdsgangen i arbejdsgangsdesigneren. Vælg indstillingen **Hierarki** under **Tildelingstype**, og vælg derefter **Konfigurerbart hierarki** under fanen **Valg af hierarki**.
>
> Du kan finde flere oplysninger om oprettelse af arbejdsgangen for orlovsanmodninger i [Oprette en arbejdsgang for orlovsanmodning](hr-leave-and-absence-workflow.md).

1. Vælg fanen **Fraværsadministrator** i arbejdsområdet **Medarbejderselvbetjening**.

2. Vælg den ønskede medarbejder under fanen **Fraværsadministrator**.

3. Vælg **Detaljer** og derefter **Fridage**.

4. Find anmodningen om fridage, og vælg indstillingen **Godkendelse**. Du kan derefter vælge en indstilling for at godkende eller annullere anmodningen om fridage.

Statussen **Annuller** angiver, at anmodningen er blevet afvist. Statussen **Fuldført** angiver, at anmodningen er blevet godkendt.

## <a name="view-time-off-in-the-calendar"></a>Få vist fridage i kalenderen

Brugere i rollen Fraværsadministrator kan få vist anmodninger om fridage i kalenderen. Følg disse trin for at få adgang til orlovskalenderen.

> [!IMPORTANT]
> En systemadministrator skal konfigurere visningsindstillingerne i kalenderen for fraværsadministratorer. På siden **Parametre for orlov og fravær** under fanen **Kalender** findes der indstillinger til at skjule eller vise fødselsdage, fravær uden detaljer, fraværsanmodninger og ventende orlovsanmodninger. Der er også en indstilling til filtrering af kalendervisningen efter arbejdertype.

1. I arbejdsområdet **Medarbejderselvbetjening** skal du vælge **Fraværsadministrator** og derefter **Kalender for fraværsadministratorer**.

2. Angiv de ønskede datoer i feltet **Dato**.

3. Opdater visningsindstillingerne efter behov.

Kalenderen for fraværsadministratorer viser alle poster for de medarbejdere, der rapporterer til fraværsadministratoren i orlovshierarkiet.

## <a name="see-also"></a>Se også

- [Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)
- [Oprette en arbejdsgang for orlovsanmodning](hr-leave-and-absence-workflow.md)
- [Vise team- og firmakalendere](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
