---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (08. juli 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 8. juli 2020.
author: andreabichsel
ms.date: 07/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a574436bc7762fbee722af8be2f923d18d01e5b
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060783"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (8. juli 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.3382. Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.

## <a name="database-logging"></a>Databaselogføring

Databaselogning gør det muligt at bestemme, hvilke tabeller og felter der skal overvåges. Du kan også bestemme, hvilke hændelser der skal udløse ændringssporing. Du kan bruge logføringsfunktioner for databasen til at se disse ændringer over tid. Du kan finde flere oplysninger under [Konfigurere og administrere databaselogning](hr-admin-database-logging.md).

## <a name="configure-the-name-of-employee-self-service"></a>Konfigurere navnet på medarbejderselvbetjening

I **Parametre for Human Resources** kan du nu ændre navnet på arbejdsområdet **Medarbejderselvbetjening** til **Selvbetjening**. Yderligere oplysninger finder du i [Skifte arbejdsområdenavn for medarbejderselvbetjening](hr-employee-self-service-workspace-name.md).

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a>Adgang til styring af åben tilmelding til frynsegoder uden for periode

Denne frigivelse løser en fejl, hvor medarbejdere kan få adgang til åben tilmelding til frynsegoder uden for tilmeldingsperioden eller uden en livshændelse. Derfor skal du justere de åbne tilmeldingsdatoer til i dag (eller tidligere) for at gøre den tilgængelig, hvis du har brug for at demonstrere den åbne tilmelding i Medarbejderselvbetjening. Du kan ændre denne indstilling under **Frynsegodeadministration > Regler og indstillingsperioder**.

## <a name="email-employee-enrollment-confirmation"></a>Bekræftelse af tilmelding på e-mail til medarbejdere

Du kan nu sende mails til medarbejdere, når de har fuldført valget af frynsegoder. Du kan enten sende en standardmeddelelse eller bruge en e-mailskabelon fra organisationen. Disse indstillinger er under **Parametre for Human Resources > Frynsegodeadministration**.

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a>Annulleret orlov vises stadig i forestående fritid i arbejdsområdet Personer (441358)

Annulleret orlov vises ikke længere som kommende fritid på orlovskortene i arbejdsområdet **Personer**.

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a>Kan ikke bruge egenskaben for afdelingsenhed i PositionV2-enhed (456486)

Du kan nu tilføje en afdeling uden at oprette en dubleret relation.

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a>PayrollWorkerEnrolledBenefitDetailEntity må kun bruge beregnet felt til pensionsordninger (459779)

Når du eksporterer enheden **LønArbejderTilmeldtFrynsegodeDetaljeEnhed**, bestemmer eksporten, om det skal bruge et beregnet felt, der er baseret på en satstabel, eller ved hjælp af feltet **BidragBeløbVal** i den understøttende tabel. Den logik, der bruges af dataenheden, bruger satstabellen i situationer, hvor programmet normalt ikke gør. Denne logik medfører, at enhedseksporten returnerer en nulværdi til denne kolonne, da der ikke findes nogen beregningssatstabel, og produktet ikke giver kunden mulighed for at angive en.
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a>Forvirrende oversættelser på tjekkisk i Personalestyring og Medarbejderselvbetjening (400276)

Denne udgivelse retter de oversættelser for **Firmaadressekartotek**, **Næste registrerede kursus**, **Job** og **Stilling**.
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a>Systemfelterne Oprettet og Redigeret er ikke aktiveret i tabellen ArbejdkalenderAnsættelse (460171)

Systemfelter Oprettet og Ændret er nu aktiveret i tabellen **ArbejdkalenderAnsættelse** i Human Resources.
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a>Null-referenceundtagelse for ansættelse, og tilføj oplysninger om fremtidig medarbejder (455475)

Denne version retter en fejl (null-reference) i strømlinet medarbejderpost, når du ansætter en medarbejder med mulighed for at **ansætte og tilføje oplysninger**.

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a>Ændringer, der foretages i Dataverse-arbejderenheden, afspejles ikke i Human Resources (455652)

Ændringer, der foretages af følgende felter i enheden **Arbejder** i Dataverse, vises nu i Human Resources:

- **Arbejder hjemmefra**
- **Anciennitetsdato**
- **Jubilæumsdato**
- **Oprindelig ansættelsesdato**

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a>Korrekt kompensationsniveau er ikke standard baseret på det job, der er tildelt stillingen (394136)

Med denne ændring anvender det korrekte kompensationsniveau standardindstillingen baseret på **Gældende dato**-poster for **Detaljer for stilling** og **Startdato** for **Tildeling af kompensationsordning**.

## <a name="in-preview"></a>Som eksempel

## <a name="mandatory-fields"></a>Obligatoriske felter 

Du kan nu gøre felter obligatoriske ved hjælp af funktionerne til tilpasning til personale. Denne funktion kræver **Gemte visninger**.

## <a name="human-resources-application-in-teams"></a>Human Resources-app i Teams

Medarbejderne kan få vist og anmode om fri fra arbejde i Microsoft Teams. De kan interagere med en bot for at oprette orlovsanmodninger. Yderligere oplysninger finder du i [Human Resources-appen i Teams](./hr-admin-teams-leave-app.md). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>DMF-enheder (Data Management Framework) til styring af frynsegoder
 
Enheder til håndtering af frynsegoder frigives. Med DMF-enheder kan du importere og eksportere data, så du nemt kan konfigurere frynsegodestyring. En skabelon til frynsegodestyring kan også bruges til at flytte data. Skabelonen eksporterer og importerer dataene sekventielt for at respektere dataafhængigheder.

## <a name="buy-and-sell-leave"></a>Købe og sælge orlov 

Nogle organisationer giver et frynsegode, der giver medarbejderne mulighed for at købe eller sælge deres orlov. Denne proces styres ofte manuelt. Denne funktion automatiserer administration af politikker og anmodninger for HR-afdelingen. Den effektiviserer orlovsprocessen og medvirker til at eliminere fejltagelser. Du kan finde flere oplysninger i:

- [Administrere politikker for køb og salg af orlov](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Købe og sælge orlov](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Orlovsperiodisering for et enkelt firma eller en enkelt plan

Kunderne kan behandle periodiseringer for et enkelt firma eller en enkelt orlovs- fraværsplan. Denne mulighed giver klarhed over periodiseringsprocessen for kunder med forskellige sabbatår eller politikker for orlovsperiodisering. Du kan finde flere oplysninger under [Periodiseret orlov pr. firma eller pr. orlovsplan](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Føje vedhæftede filer til anmodninger om fravær

Muligheden for at føje vedhæftede filer til anmodninger om godkendt orlov er afgørende i det aktuelle COVID-19-miljø. Medarbejderne kan nu tilføje disse vedhæftede filer. De har også en mere indsigt i, hvordan der foretages opdateringer af anmodninger om orlov. Du kan finde flere oplysninger under [Føje en vedhæftet fil til en eksisterende anmodning](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Føje årsagskode til periodiseringssuspenderinger 

Årsagskoder er føjet til periodiseringssuspenderingen.

## <a name="carry-forward-rules"></a>Overføre regler 

Du kan angive en orlovstype for overførselssaldi, hvor gennemførte reguleringer overføres. Hvis en medarbejder f.eks. overfører 10 dage, kan du vælge en anden orlovstype for disse 10 dage. Du kan finde flere oplysninger i [Konfigurere orlovs- og fraværstyper](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Suspendere orlovsperiodisering for angivne orlovstyper

Du kan oprette en regel om suspendering af orlovsperiodiseringer for medarbejdere med orlovsanmodninger, der er angivet til ubetalt orlov. Ubetalt orlov kan være en type, men behøver ikke at være det. Du kan suspendere enhver orlov baseret på en anden orlovstype.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-enhed er tilgængelig for periodiseringssuspenderinger 

En DMF-enhed er nu tilgængelig for periodiseringssuspenderinger.

## <a name="coming-soon"></a>Kommer snart

## <a name="checklist-entities-included-in-dataverse"></a>Kontrollisteenheder inkluderet i Dataverse

Der vil snart være tilgængelige kontrollisteenheder til processer til onboarding, offboarding, overførsler og forretning i Dataverse.

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]