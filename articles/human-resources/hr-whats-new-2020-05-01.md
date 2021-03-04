---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (1. maj 2020)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 1. maj 2020.
author: Darinkramer
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 074c678d9d8294aabf4e78b2a6ee0fa53efbaf23
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417819"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (1. maj 2020)

I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.3196. Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a>Nye performancestyringsenheder er tilgængelige i Data Management Framework (DMF)

Følgende enheder er nu tilgængelige. Hvis disse enheder ikke vises på listen over enheder, skal du bruge indstillingen **Opdater enheder** i **Strukturparametre > Enhedsindstillinger > Opdater liste over enheder**.

- **Diskussionskompetence**
- **Diskussionsmål**
- **Diskussionsmåling**
- **Diskussionsemner**
- **Performancekladde**
- **Mål**
- **Måling af mål**

Derudover er **Samlet score** og **Gennemsnitsscore** føjet til enheden **Diskussion**.

## <a name="increase-length-of-leave-request-comments-275641"></a>Forøge længde på kommentarer til orlovsanmodninger (275641)

Kommentarer til orlovsanmodninger tillader nu mere end 100 tegn.

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a>Endelige kommentarer til gennemgange vises ikke, når lederen eller medarbejderen er logget på et andet firma (431688)

Alle kommentarer vil nu blive vist, når der vises gennemgange.

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a>Brugerdefinerede links understøttes ikke på den nye formular til Arbejder (390374)

Brugerdefinerede links er nu aktiveret på den strømlinede formular til **Arbejder**.

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a>HcmRatingLevelEntity forårsager OData API-nedbrud (439476)

Denne ændring retter API-nedbruddet. Denne fejl blev forårsaget af et duplikeret navn.

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

## <a name="known-issues"></a>Kendte problemer

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>Prøveversionen af SharePoint fungerer ikke i visse miljøer

Hvis visning af dokumenter, der er gemt i SharePoint, ikke fungerer, kan du prøve følgende procedure:

1. Kontroller, at administratorbrugerkontoen har en mail tilknyttet brugerposten. Du kan få vist disse oplysninger på siden **Bruger**. Hvis e-mail ikke er konfigureret, skal du tilføje e-mailadressen og udbyderen med OData Excel-tilføjelsesprogrammet. E-mailadressen findes som standard ikke i Excel-designet. Du skal redigere Excel-designet, tilføje alle felter, anvende og opdatere. Når du har fuldført disse trin, kan du opdatere administratorkontoen.

2. Når administratorkontoen har en tilknyttet mailkonto, skal du logge på Personale med administrator-legitimationsoplysninger.

3. Åbn en vedhæftet fil i SharePoint for at starte dokumentvisningen.

4. Log på med en anden brugerkonto, der har adgang til vedhæftede filer, og kontroller, at eksempelvisningen fungerer som forventet.

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]