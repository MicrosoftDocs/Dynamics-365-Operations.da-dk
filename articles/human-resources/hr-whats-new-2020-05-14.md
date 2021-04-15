---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (14. maj 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 14. maj 2020.
author: andreabichsel
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e70d8fc62150d68503552754e94c7130d8960c76
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802353"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (14. maj 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.3244. Tallene i parenteser i nogle overskrifter henviser til Lifecycle Services (LCS)-supportnumre til reference.

## <a name="platform-changes"></a>Platformsændringer

Der er inkluderet platformsændringer i denne uges udgivelse. Få flere oplysninger i [Platformsopdateringer for version 10.0.10 af Finance and Operations-apps (maj 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34). Denne version inkluderer fejlrettelser og ændringer af gemte visninger.
 
## <a name="ensure-dataverse-picklists-are-consistent-with-leave-enums-436343"></a>Kontrollér, at Dataverse, at pluklister er konsekvente med orlov-fasttekst (436343)

Dataverse-pluklister er nu konsekvente med orlov-fasttekst.

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a>Tillad brugere at konfigurere en arbejdsproces for orlovsanmodninger baseret på anmodningsmængden (300044)

Brugere kan konfigurere arbejdsprocesser for orlovsanmodninger baseret på anmodningsmængder.
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a>Formularen Ny arbejder viser data via menuen Vis, når Avanceret sikkerhed er aktiveret (403185)

Denne version retter, hvordan visning af arbejdere på tværs af juridiske enheder fungerer, når avanceret adgang er aktiveret, og der kan opnås adgang til arbejdere i andre firmaer.

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a>Tillad kørsel af orlovperiodisering for en enkelt plan eller et enkelt firma (318844)

Med denne ændring kan du køre periodiseringer for en virksomhed eller plan.
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a>Vis stillingens fuldtidsstillingsværdi i formularen Tilmeldte arbejdere (414658)

Værdien for fuldtidsstilling fra en arbejders stilling bestemmer en arbejders periodiseringsandel, når indstillingen for fuldtidsstilling aktiveres for orlovstypen. Dette felt medtages nu i formularen **Tilmeldte arbejdere** og dialogboksen **Massetilmelding**.

## <a name="add-leave-balance-expiration-batch-job-431266"></a>Tilføj batchjob ved udløb af orlovssaldo (431266)

Der er nu et nyt batchjob tilgængeligt, som kører dagligt. Det reducerer den resterende saldo for orloven, når udløbsdatoerne bliver aktuelle.

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a>Når du eksporterer personlige kontaktpersoner for en medarbejder ved hjælp af objektet Arbejders personlige kontaktperson, eksporteres personlige kontakter med overordnet relationstype ikke (345893)

Dataobjektet **Arbejders personlige kontaktperson** (**HcmPersonalContactPersonEntity** i DMF og **PersonalContactPerson** i OData) kunne ikke eksportere personlige kontakter, der har relationstypen **Overordnet**. Dette problem er løst for de personlige kontaktpersoner, der oprettes efter ændringen. Eksisterende personlige kontaktpersoner af typen **Overordnet** kan rettes i en senere version.

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a>Årsagskoder vises på tværs af forskellige scenarier, når de er markeret som orlov og fravær, og den strømlinede medarbejderformular er aktiveret (434163)

Denne ændring begrænser årsagskoderne, så de kun kan være orlov og fraværskoder, når du aktiverer en strømlinet medarbejderpost.

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a>Eksempelvisningsfunktionen Tildel en orlovsplan til medarbejdere i fremtidige viser fejl (433555)

Denne ændring retter en fejl, når der er knyttet to orlovstyper til en orlovsplan, og du forsøger at tildele en medarbejder.

## <a name="getting-started-banner-appears-for-all-users-441731"></a>Banneret Introduktion vises for alle brugere (441731)

Med denne ændring skjules banneret Introduktion for brugere, der ikke er systemadministratorer eller datastyringsadministratorer. 

## <a name="the-dataverse-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a>Objektet Dataverse-arbejderadresse fungerer anderledes, når det gælder ikrafttrædelsesdatoer med dato/klokkeslæt i Human Resources (425071)

Denne ændring bevarer adresseoplysninger, der er justeret i bestemte scenarier, baseret på datoerne i adressen.

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a>Det var ikke muligt at føje en vedhæftet fil til en godkendt orlovsanmodning (425407)

Med denne uges udgivelse kan du føje vedhæftede filer til godkendte orlovsanmodninger uden at ændre orlovsanmodningen.

## <a name="in-preview"></a>Som eksempel

## <a name="leave-suspension"></a>Forlad suspension

Du kan afbryde orlov og fravær i Human Resources for en medarbejder. Når du suspendere orlov, stoppes orloven for de valgte orlovstyper. Hvis suspensionen finder sted, når en periodisering er blevet behandlet, opretter suspensionen en forholdsmæssig justering til medarbejderens orlov. Du kan finde flere oplysninger i [Suspender orlov](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Opdatere brugeroplevelsen for at angive, at periodiseringen er udsat (429550)

Brugeroplevelsen indikerer nu, at periodiseringen er blevet suspenderet for en plan.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>Suspendere orlovsperiodisering for angivne orlovstyper (272447)

I denne udgave kan HR oprette en regel om periodiseringer for suspendering af orlov for medarbejdere med orlovsanmodninger, der er angivet til ubetalt orlov. Ubetalt orlov kan være en type, men behøver ikke at være det. Du kan suspendere enhver orlov baseret på en anden orlovstype.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>DMF-enhed er tilgængelig for periodiseringssuspenderinger (429549)

En DMF-enhed er nu tilgængelig for periodiseringssuspenderinger.

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>Føje årsagskoder til periodiseringssuspensioner (429547)

Årsagskoder er føjet til periodiseringssuspenderingen.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>Begynde overgangen fra Human Resources-parametre til orlovs- og fraværsparametre

Denne version begynder at kombinere Human Resource-parametre med orlovs- og fraværsparametre.

## <a name="carry-forward-rules"></a>Overføre regler

Du kan angive en orlovstype for overførselssaldi, hvor gennemførte reguleringer overføres. Hvis en medarbejder f.eks. overfører 10 dage, kan du vælge en anden orlovstype for disse 10 dage. Du kan finde flere oplysninger i [Konfigurere orlovs- og fraværstyper](hr-leave-and-absence-types.md).

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]