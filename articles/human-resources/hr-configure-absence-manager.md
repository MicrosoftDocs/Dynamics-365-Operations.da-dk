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
ms.openlocfilehash: 050874628388629569751afae201ef346af020da09c81d24a69e1a4b5eb41b6f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732339"
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

I arbejdsområdet **Medarbejderselvbetjening** viser fanen **Orlovsstyring** fraværsoplysninger om de medarbejdere, der er tildelt fraværsadministratoren i orlovshierarkiet. Der er nogle få indstillinger tilgængelige for fraværschefen: 
 - Gennemgå anmodninger om fravær.</br>
 - Send en anmodning om fravær på vegne af en medarbejder.</br>
 - Se alle medarbejdere, der er knyttet til dem, som del af orlovshierarkiet.</br>
 - Se fraværschefens kalender.</br>

Der er to faner i arbejdsområdet **Orlovsstyring**:
 - **Anmodninger om fravær**: Under denne fane vises alle de anmodninger om fravær, som fraværschefen kan godkende. Fraværschefen kan vælge flere poster og handle på dem samtidig. Hvis orlovsvisningen på tværs af virksomheden er aktiveret, viser denne liste ventende anmodninger om fravær på tværs af alle de juridiske enheder, de har adgang til. Ellers vises de ventende anmodninger om fravær for den juridiske enhed, der aktuelt er valgt. </br>
 - **Alle medarbejdere**: Under denne fane vises alle de medarbejdere, der er knyttet til fraværschefen i orlovshierarkiet. Der er et par tilgængelige valgmuligheder for hver medarbejder:
    - **Anmod om fravær** – Send en ny fraværsanmodning for den valgte medarbejder.</br>
    - **Fridage** – Få vist saldi, godkendt fritid, fritidsanmodninger for den valgte medarbejder.</br>

## <a name="approve-time-off-requests"></a>Godkende anmodninger om fridage

Fraværsadministratorer kan godkende eller afvise anmodninger om fridage for medarbejdere. 

> [!IMPORTANT]
> Før fraværsadministratorer kan godkende eller afvise anmodninger om fridage, skal arbejdsgangen for orlovsanmodninger være konfigureret til at tildele dem arbejdselementer for orlovsanmodninger med henblik på gennemsyn.
>
> 1. Vælg eller opret arbejdsgangen for orlovsanmodning på siden **Arbejdsgange for Human Ressources**.
> 2. Vælg indstillingen **Tilknyt hierarki**, og vælg derefter **Orlov** i feltet **Hierarkinavn**.
> 3. Opdater arbejdsgangen i arbejdsgangsdesigneren. Vælg indstillingen **Hierarki** under **Tildelingstype**, og vælg derefter **Konfigurerbart hierarki** under fanen **Valg af hierarki**.
>
> Du kan finde flere oplysninger om oprettelse af arbejdsgangen for orlovsanmodninger i [Oprette en arbejdsgang for orlovsanmodning](hr-leave-and-absence-workflow.md).

1. Vælg fanen **Orlovsstyring** i arbejdsområdet **Medarbejderselvbetjening**.

2. Under fanen **Anmodninger om fravær** skal du vælge de anmodninger om fravær, som du vil gøre noget ved. Du kan vælge flere poster i denne listevisning.

3. Brug handlingsknapperne øverst i gitteret til at godkende, afvise eller uddelegere anmodningen om fravær. 

Alternativt kan brugeren også bruge feltet **Anmodninger om fravær** til venstre til at navigere til listen over alle arbejdselementer for anmodninger om fravær. 

## <a name="view-time-off-in-the-calendar"></a>Få vist fridage i kalenderen

Brugere i rollen Fraværsadministrator kan få vist anmodninger om fridage i kalenderen. Følg disse trin for at få adgang til orlovskalenderen.

> [!IMPORTANT]
> En systemadministrator skal konfigurere visningsindstillingerne i kalenderen for fraværsadministratorer. På siden **Parametre for orlov og fravær** under fanen **Kalender** findes der indstillinger til at skjule eller vise fødselsdage, fravær uden detaljer, fraværsanmodninger og ventende orlovsanmodninger. Der er også en indstilling til filtrering af kalendervisningen efter arbejdertype.

1. I arbejdsområdet **Medarbejderselvbetjening** skal du vælge **Orlovsstyring** og derefter **Kalender for fraværsadministratorer**.

2. Angiv de ønskede datoer i feltet **Dato**.

3. Opdater visningsindstillingerne efter behov.

Kalenderen for fraværsadministratorer viser alle poster for de medarbejdere, der rapporterer til fraværsadministratoren i orlovshierarkiet.

## <a name="see-also"></a>Se også

- [Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)
- [Oprette en arbejdsgang for orlovsanmodning](hr-leave-and-absence-workflow.md)
- [Vise team- og firmakalendere](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
