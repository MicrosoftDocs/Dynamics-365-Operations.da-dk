---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (10. marts 2020)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 10. marts 2020.
author: Darinkramer
manager: AnnBe
ms.date: 03/10/2020
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
ms.search.validFrom: 2020-03-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 944481727f3222a10f128ac3078c117f5ae7d193
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526902"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-10-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (10. marts 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.2985. Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.

## <a name="cant-access-skill-gap-analysis-report-394460"></a>Kan ikke få adgang til analyserapporten for kompetencekløft (394460)

Denne rapport understøttes ikke i Dynamics 365 Human Resources. Menupunktet til at udskrive SSRS-rapporten er fjernet.

## <a name="incorrect-message-accessing-the-getting-started-page-417950"></a>Forkert meddelelse, når siden Introduktion åbnes (417950)

Når denne ændring er foretaget, skjuler sikkerheden dette menupunkt, hvis du ikke har adgang til formularen.

## <a name="streamlined-task-maintenance-for-employees-380538"></a>Strømlinet opgavevedligeholdelse for medarbejdere (380538)

I formularen til vedligeholdelses af arbejderopgave vises alle opgaver for en medarbejder på tværs af onboarding, offboarding, overgange og forretningsprocesser. Du kan nu slette, gentildele eller opdatere status af opgaver.

Eksempel: Benjamin Martin er administrator af frynsegoder. Under medarbejderens onboarding oprettes der opgaver, så Benjamin kan gennemgå den nye medarbejders valg af frynsegoder. Benjamin har tidligere opgaver, som han har afsluttet, og fremtidige opgaver, som han skal afslutte. Benjamin beslutter at forlade firmaet, så hans opgaver skal tildeles igen eller fjernes. I formularen til vedligeholdelse af opgave (i handlingsruden i formularen **Arbejder**) kan alle Benjamins opgaver tildeles en anden arbejder eller fjernes.  

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service-løsning er nu tilgængelig med følgende ændringer:

| Beskrivende tekst | Forskydning |
| --- | --- |
| Ændringer i objektet **Job/Stilling** | <ul><li>**Kompensationsområde** er tilføjet</li>|
| Enheden **Stillingsdimension** er tilføjet | <ul><li>**Økonomiske dimensioner** er tilføjet</li>
| Ændringer i objektet **Arbejder** | <ul><li>**Navnerækkefølge** er tilføjet</li><li>**Arbejder hjemmefra** er tilføjet</li><li>**Sprog** er tilføjet</li><li>**Anciennitetsdato** er tilføjet</li><li>**Jubilæumsdato** er tilføjet</li><li>**Oprindelig ansættelsesdato** er tilføjet</li></ul> |
| Ændringer af objektet **Ansættelse** | <ul><li>**Økonomiske dimensioner** er tilføjet</li><li>**Årsag til fratrædelse** er tilføjet</li><li>**Fratrædelsesdato** er omdøbt fra **Overførselsdato**</li><li>**Datoer for prøvetid** er tilføjet</li></ul> |
| Ændringer i objektet **Arbejders adresse** | <ul><li>**Gadenavn** er tilføjet</li><li>**Adresselinje 1**, **Adresselinje 2** og **Adresselinje 3** er markeret til udfasning</li></ul> |
| Nye konfigurationsobjekter til variabel kompensation | <ul><li>**Type af variabel kompensationsplan**</li><li>**Kompensation - variabel struktur**</li><li>**Fordelingsregler**</li><li>**Niveau i variabel kompensationsplan**</li></ul> |
| Nyt objekt **Arbejderkalender for ansættelse** | <ul><li>**Arbejdskalenderobjekt** er tilføjet</li></ul> |
| Nyt objekt **Lønoplysninger for stillinger** | <ul><li>**Lønoplysninger for stillinger** er tilføjet</li></ul> |
| Nyt objekt **Titel** | <ul><li>**Titel** er tilføjet</li></ul> Den nye enhed **Titel** er inkluderet i Common Data Service, men den er ikke refereret fra enhederne **Stilling** eller **Job** i øjeblikket. |

> [!NOTE]
> Økonomiske dimensioner for både stillinger og beskæftigelse giver en integration med én retning for opdateringer fra HR til Common Data Service. Opdateringer af økonomiske dimensioner synkroniseres i øjeblikket ikke fra Common Data Service til HR.

I løbet af de næste par uger vil disse enhedsændringer være tilgængelige i alle miljøer. Sådan installeres den nyeste Common Data Service-løsning til HR manuelt:

1.  Gå til [Power Platform Administration](https://admin.powerplatform.microsoft.com).

2.  Vælg **Miljøer**.

3.  Find det miljø, du vil opgradere. Miljøet skal svare til **Miljønavn** i sektionen **Common Data Service-oplysninger** i formularen **Om** i HR.

4.  Vælg miljøet for at få vist miljødetaljerne.

5.  Vælg **Administrer løsninger** på handlingslinjen i toppen. Der åbnes et nyt browservindue, hvor du kan navigere til **Dynamics 365 Administration** i konteksten af dit miljø.

6.  Vælg **Dynamics 365 Human Resources Anchor** i listen **Løsning**.

7.  Vælg **Opgrader** for at anvende den seneste løsning.

## <a name="in-preview"></a>Som eksempel

Følgende prøvefunktioner er tilgængelige den 3. februar 2020:

- **Visningsfunktioner for orlov og fravær** - Du kan finde flere oplysninger under [Visningsfunktioner for orlov og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Prøveversionsfunktion: Administration af frynsegoder** – Der er flere oplysninger, herunder kendte problemer, under [Oversigt over Administration af frynsegoder](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Kommer snart

### <a name="platform-update-33"></a>Platform update 33

- Fuld side-apps (eksempel) – denne eksempelfunktion, som kræver, at du aktiverer funktionen Gemte visninger, tillader, at Power Apps og tredjeparts apps tilføjes som en fuld sideoplevelse via dashboardet.

- Gemte visninger (eksempel) – Denne eksempelfunktion gør det muligt at gemme visninger, hvilket er en væsentlig forbedring af det personligt tilpassede undersystemet. Denne funktion giver brugere mulighed for at have flere navngivne sæt af tilpasninger pr. side. Du kan også publicere visninger til sikkerhedsroller.

- Optimeret "er en af"-filtreringsoplevelse – Denne funktion aktiverer en optimeret "er en af"-filtreringsoplevelse, der gør det nemmere at angive flere filterværdier, har en enklere mekanisme til at fjerne enkelte eller alle filterværdier og har en mere kompakt og intuitiv visualisering af filterværdier.

- Anbefalede felter – brugere skal ofte føje felter til et gitter eller en side. Det kan være svært med så mange tilgængelige felter. I stedet for at skulle søge gennem en stor liste, gør denne funktion det muligt for systemet at placere et sæt anbefalede felter øverst baseret på, hvad andre brugere oftest tilføjer i lignende scenarier.

- Træge standardhandlinger i gitre – Denne funktion sikrer, at standardhandlingen i et gitter sammenkædes med en bestemt kolonne i et gitter, uanset om den pågældende kolonne flyttes eller skjules.

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)