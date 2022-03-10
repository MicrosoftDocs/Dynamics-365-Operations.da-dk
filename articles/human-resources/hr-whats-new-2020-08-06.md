---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (06. august 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 6. august 2020.
author: andreabichsel
ms.date: 08/06/2020
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
ms.search.validFrom: 2020-08-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dbcf854330b7c5ba6ca812a5aed384584c05ce8d
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062180"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-06-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (06. august 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.3444. Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.

## <a name="platform-update-1001236-is-now-available"></a>Platformsopdatering 10.0.12(36) er nu tilgængelig

Du kan få mere at vide i [Platformsopdateringer til version 10.0.12 af Finans- og driftsapps (august 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-12.md).

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>DMF-enheder (Data Management Framework) til styring af frynsegoder
 
Enheder til håndtering af frynsegoder frigives. Med DMF-enheder kan du importere og eksportere data, så du nemt kan konfigurere frynsegodestyring. En skabelon til frynsegodestyring kan også bruges til at flytte data. Skabelonen eksporterer og importerer dataene sekventielt for at respektere dataafhængigheder. Du kan finde flere oplysninger i:

- [Understøttelse af DMF-enhed](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/dmf-entity-support) i Dynamics 365 2020-frigivelsesplan bølge 1
- [Oversigt over datastyring](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md)


## <a name="claire-creates-a-workflow-for-buying-and-selling-leave-requests-446557"></a>Claire opretter en arbejdsproces for køb og salg af orlovsanmodninger (446557)

Du kan finde flere oplysninger i:

- [Tillade medarbejdere at købe og sælge orlov](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) i Dynamics 365 2020 frigivelsesplan bølge 2
- [Administrere politikker for køb og salg af orlov](./hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Købe og sælge orlov](./hr-employee-self-service-buy-sell-leave.md)


## <a name="worker-postal-addresses-v2-entity-has-access-across-legal-entities-with-restricted-access-459126"></a>V2-enheden har adgang til arbejderes postadresser på tværs af juridiske enheder med begrænset adgang (459126)

Med denne ændring begrænses enheden **Arbejders postadresse v2** ud fra den juridiske enhedsadgang, som brugeren har fået tildelt.

## <a name="workflow-email-hyperlink-fails-to-open-relevant-reviews-437398"></a>Maillinket for arbejdsprocessen kan ikke åbne relevante gennemgange (437398)

Når du bruger pladsholderen til at åbne en ydeevnegennemgang i arbejdsprocessen for gennemgange, åbner det link, der er oprettet i mailen, nu den valgte post.

## <a name="new-entities-for-buying-and-selling-leave-473180"></a>Nye enheder til køb og salg af orlov (473180)

Enheder i struktur for dataadministration er nu tilgængelige for køb og salg af orlov. Få flere oplysninger i [Oversigt over dataadministration](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

## <a name="when-viewing-record-information-and-using-advanced-filters-a-user-could-gain-access-to-other-employees-records-472490"></a>Ved visning af postoplysninger og brug af avancerede filtre kan en bruger få adgang til andre medarbejderes poster (472490)

Med denne ændring har brugere af Medarbejderselvbetjening kun få adgang til deres egne poster, når de bruger Medarbejderselvbetjening. Visning af postoplysninger ved ændring af filtreringsindstillingen fremviser ikke længere yderligere data.

## <a name="personnel-management-analytics-include-exited-worker-records-382893"></a>Personalestyringsanalyse omfatter afsluttede arbejderposter (382893)

Med denne udgivelse omfatter personalestyring nu kun aktive arbejdere. 
 
## <a name="unable-to-process-a-merit-increase-for-an-employee-473125"></a>Der kan ikke behandles en meritstigning for en medarbejder (473125)

Denne ændring gør det muligt at angive meritstigninger, når du ændrer ikrafttrædelsesdatoen for den nye meritstigning.

## <a name="review-workflow-can-be-started-more-than-once-467541"></a>Arbejdsprocessen for gennemgang kan startes mere end én gang (467541)

Med denne ændring kan du kun starte arbejdsgangen for ydeevnegennemgang én gang. Status for styringsfunktionen viser ikke længere den indstilling, der starter gennemgangen.

## <a name="leave-request-work-flow-ends-in-error-when-canceling-an-approved-leave-request-472063"></a>Arbejdsgangen for anmodning afsluttes med en fejl, når en godkendt orlovsanmodning annulleres (472063)

Når du i denne version annullerer en godkendt orlovsanmodning, forbliver anmodningstilstanden ikke længere godkendt, og arbejdsprocessen fortsætter.

## <a name="system-suggests-exited-workers-when-creating-a-new-review-form-the-template-460624"></a>Systemet foreslår afsluttede arbejdere, når der oprettes en gennemgangsformular fra skabelonen (460624)

Med denne ændring er afsluttede arbejdere ikke længere tilgængelige, når der oprettes nye gennemgange fra en skabelon. Du kan ikke oprette gennemgange for medarbejdere, der ligger uden for deres ansættelsesperiode.

## <a name="position-hierarchy-circular-reference-detection-415879"></a>Registrering af cirkulær reference for stillingshierarki (415879)

Med denne ændring er den cirkulære reference til stillingshierarkiet begrænset til et enkelt tidspunkt. Du kan køre registrering af cirkulære referencer for forskellige datoer for at bekræfte, at rapporteringsstrukturen ikke har cirkulære referencer.

## <a name="buy-and-sell-leave"></a>Købe og sælge orlov 

Nogle organisationer giver et frynsegode, der giver medarbejderne mulighed for at købe eller sælge deres orlov. Denne proces styres ofte manuelt. Denne funktion automatiserer administration af politikker og anmodninger for HR-afdelingen. Den effektiviserer orlovsprocessen og medvirker til at eliminere fejltagelser. Du kan finde flere oplysninger i:

- [Tillade medarbejdere at købe og sælge orlov](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) i Dynamics 365 2020 frigivelsesplan bølge 2
- [Administrere politikker for køb og salg af orlov](./hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Købe og sælge orlov](./hr-employee-self-service-buy-sell-leave.md)

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

## <a name="in-preview"></a>Som eksempel

### <a name="mandatory-fields"></a>Obligatoriske felter

Du kan nu gøre felter obligatoriske ved hjælp af tilpasningsfunktionerne for personale. Denne funktion kræver **Gemte visninger**. Du kan finde flere oplysninger om gemte visninger i:

- [Gemte visninger – generel tilgængelighed](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) i Dynamics 365 2020-frigivelsesplan bølge 2
- [Opbygge formularer, der fuldt ud anvender gemte visninger](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>Human Resources-app i Teams

Medarbejderne kan få vist og anmode om fri fra arbejde i Microsoft Teams. De kan interagere med en bot for at oprette orlovsanmodninger. Du kan finde flere oplysninger i:

- [Løsning til medarbejderes orlov og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020-frigivelsesplan bølge 1
- [Human Resources-app i Teams](./hr-admin-teams-leave-app.md)

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-enhed er tilgængelig for periodiseringssuspenderinger

En DMF-enhed er nu tilgængelig for periodiseringssuspenderinger.

## <a name="coming-soon"></a>Kommer snart

## <a name="checklist-entities-included-in-dataverse"></a>Kontrollisteenheder inkluderet i Dataverse

Der vil snart være tilgængelige kontrollisteenheder til processer til onboarding, offboarding, overførsler og forretning i Dataverse.

## <a name="known-issues"></a>Kendte problemer

Arbejdsområdet **Funktionsstyring** viser muligvis funktioner, der er deaktiveret som visningsfunktioner, når de generelt er tilgængelige. Nedenfor vises en liste over de mest almindeligt tilgængelige funktioner, der viser en forkert status. 

1.  Frynsegodeadministration
2.  Sagsstyring
3.  Databaselogføring (overvågning)
4.  Orlovsperiodisering for et enkelt firma eller en enkelt plan
5.  Afbrydelse af periodisering af orlov og fravær
6.  Årsagskode og kommentar for saldoregulering
7.  Købe og sælge orlov
8.  Kalender for orlov og fravær
9.  Regler for orlovsoverførsel
10. Revision af orlovsperiodisering
11. Sletning af orlovsperiodisering
12. Afrunding af orlovsperiodisering
13. Konfigurer flere orlovstyper på en enkelt orlovsplan
14. Forbedringer af opdatering af fravær
15. Bruge en medarbejders FTE-analyse til periodiseringer
16. Visning af kompensation på tværs af firmaer
17. Udskiv performancegennemgange
18. Korrektioner for feriedage ved orlovsperiodisering

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]