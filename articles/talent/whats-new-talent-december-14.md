---
title: Nyheder eller ændringer i Dynamics 365 for Talent Core HR (14. december 2018)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c2d209cac52665053b664a93bfb6c35e171b0948
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/12/2019
ms.locfileid: "949845"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a>Nyheder eller ændringer i Dynamics 365 for Talent Core HR (14. december 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.2085**

Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.

## <a name="changes"></a>Ændringer

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a>USA - ACA-understøttelse (Affordable Care Act) med formularerne 1095-B og C-1095 for skatteåret 2018

Hvert år skal ALE (Applicable Large Employers) levere en 1095-C til hver fuldtidsansat. Hvis arbejdsgiveren derudover har sygesikringsordning med egendækning, skal han eller hun levere 1095-C (hvis det er en ALE) og 1095-B (hvis det er en lille arbejdsgiver) til en medarbejder på fuld tid eller på deltid, der er omfattet af et af deres tilbudte sygesikringsprogrammer. Denne funktion leverer formularer, der kan udskrives, til både 1095-C- og 1095 B.

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a>Feltet SubmittedByPersonId i HcmPerfJournalEntity ignoreres under import

Når kladdeposteringer importeres eller eksporteres, ignoreres feltet **Sendt af**. Med denne ændring afspejler værdien **importeret/eksporteret** værdien i tabellen under eksport. Under import opdateres systemet med den værdi, der er angivet i importfilen.

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a>Fanen Analyser i 'Orlov og fravær' arbejdsområdet viser "OpenConnectionError"-fejl for ikke-system-administratorroller

Med denne opdatering opstår der ikke fejl, når du åbner fanen **Analyser** i **Orlov og fravær**-arbejdsområdet.

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Medarbejderselvbetjening, Stillingshierarki-detailudledning fra felt kan ikke hente overordnet node

Der er foretaget en ændring for at rette fejlen "Den overordnede node kunne ikke hentes", når stillingshierarkiet er blevet tilpasset, så det kan vises i et eksisterende arbejdsområde, og der er valgt en stilling i hierarkiet.  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a>Du skal være systemadministrator for at få vist fanen Løn på siden Stilling.

Der er foretaget en ændring, så de korrekte sikkerhedselementer medtages i den eksisterende rettighed: "Vedligehold oplysninger om lønarbejder og stilling". Med denne ændring får lønadministratoren som standard adgang til Løn-felterne på siden Stilling.

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a>Der opstod en fejl under afsendelse af performancegennemgang til chef, og pladsholderen %Reviews.PerfPeriod% bruges i indgivelsesinstruktionerne

Der er foretaget en ændring, der retter fejlen "Null-reference", når du bruger pladsholderen %Reviews.PerfPeriod% i indgivelsesinstruktionerne.

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a>Power BI-personalerapporten viser fejl, når arbejderens anciennitetsdato er en skuddag

Med denne ændring understøttes skuddage nu i Power BI.

### <a name="integration-between-core-hr-and-attract"></a>Integration mellem Core HR og Attract

Der er foretaget en ændring, så den integration mellem Core HR og Attract, der er relateret til ansøgere, der skal ansættes, opdateres. For at gøre de kandidater, der skal ansættes, synlige i arbejdsområdet **Personalestyring** anvendes følgende Common Data Service-enheder:

Jobansøgning
- Statusårsag skal være indstillet til Tilbud accepteret
-   Indeholder en ansøger og jobmuligheder

Kandidat
-   Angiver oplysninger om kandidaten

Jobmulighed
-   Angiver id for jobmulighed og deltagere i jobmulighed

Deltagere i jobmulighed
-   Angiver ansættelseschef

Når en ansøger føjes til Personalestyring, kan vedkommende nu også afskediges ved hjælp af en ny indstilling, der er tilgængelig på kandidatkortet.

## <a name="coming-soon"></a>Kommer snart

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>Orlov og fravær: fremtidig orlov og budgettering af orlovssaldi

Med de ændringer, der foretages, så medarbejderne kan budgettere fritid og anmode om fremtidig fritid, uden at det påvirker deres aktuelle fritidssaldi, ændres den måde, som fritidssaldi vises på, også. 

Den disponible saldo, der aktuelt vises, er mængden af fritid, der er tilgængelig for anmodninger, herunder periodiseringer, til og med i dag og alle godkendte orlovsanmodninger og i al fremtid. 

Når der gives mulighed for budgettering, ændres den viste saldo til den aktuelle fritidssaldo, herunder periodiseringer til og med i dag og anmodninger til og med dags dato. Medarbejdere og ledere kan se disse opdaterede saldi i medarbejdernes og ledernes selvbetjeningsportal på kortet **Fridage** og i vinduet **Saldi for fritid**. Personalechefer kan se disse opdaterede saldi i arbejdsområdet **Personer** og i medarbejderens vindue **Tildelte orlovsplaner**.

## <a name="known-issue"></a>Kendt problem

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a>Tilknytningsfejl i integrationen med Finance and Operations

Følgende problemer er identificeret i den aktuelle skabelon til integration af Talent med Dynamics 365 for Finance and Operations. En ny skabelon offentliggøres snart og anvendes på alle nye integrationsprojekter, der oprettes. For eksisterende integrationsprojekter kan opgavetilknytningerne opdateres. Du kan finde opdaterede tilknytninger i følgende tabel. 

>[!NOTE]
> Den overordnede tildelingsopgave Jobstillinger til stillinger kan ikke integrere data. Dette er et problem, der er i øjeblikket undersøges. Der findes ingen løsning i den aktuelle tilknytning. 

I opgaven Afdelinger til driftsenhed skal følgende tilknytninger opdateres.

| Eksisterende kildefelt          | Nyt kildefelt |
| -------------------------------|------------------|
| cdm_description (beskrivelse)  | cdm_name (navn)  |

En yderligere tilknytning skal også tilføjes. Vælg det sidste **Ingen**-felt for at tilføje følgende tilknytning.

| Kildefelt                   | Destinationsfelt    |
| -------------------------------|----------------------|
| cdm_description (beskrivelse)  | NAMEALIAS (NAMEALIAS)|

De opdaterede tilknytninger skal se ud som på følgende billede.

![Opgaven Afdelinger til driftsenheder](./media/DepartmentMapping.png)


I opgaven Job til stillingsdetaljer skal følgende tilknytninger opdateres.

| Eksisterende kildefelt          | Nyt kildefelt                   |
| -------------------------------|------------------------------------|
| cdm_name (navn)                | cdm_description (beskrivelse)      |
| cdm_name (beskrivelse)         | cdm_jobdescription (stillingsbeskrivelse)|


De opdaterede tilknytninger skal se ud som på billedet nedenfor.

![Opgaven Job til stillingsdetaljer](./media/JobMapping.png)

I opgaven Arbejdere til arbejde skal følgende tilknytninger opdateres.

| Eksisterende kildefelt                 | Nyt kildefelt                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (e-mailadresse 1)   | cdm_primaryemailaddress (primær e-mailadresse) |
| cdm_telephone1 (telefon 1)          | cdm_primarytelephone (primær telefon)       |

Transformeringen af feltet Køn skal også opdateres. Vælg tilknytningstypen **fn** (funktion) for Køn, og opdater følgende værditilknytninger.

| Common Data Service-værdi                   | Finance and Operations-værdi                     |
| ----------------------------|--------------------------------------------------|
| 75440000                    | Mand                                             |
| 75440001                    | Kvinde                                           |
| 75440002                    | Ingen                                             | 
| 75440003                    | Ikke-specifik                                      |

De opdaterede tilknytninger skal se ud som på følgende billeder.

![Opgaven Arbejdere til arbejde](./media/WorkerMapping.png)

![Transformering af feltet Køn](./media/WorkerTransform.png)
