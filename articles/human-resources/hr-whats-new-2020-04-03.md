---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (3. april 2020)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 3. april 2020.
author: andreabichsel
manager: tfehr
ms.date: 04/03/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 715de76e9920bcb6cca7cabf053f649d27094149
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465360"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-3-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (3. april 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.3111. Tallene i parenteser i nogle overskrifter henviser til Lifecycle Services (LCS)-supportnumre til reference.

## <a name="features-that-are-generally-available-the-week-of-april-6"></a>Funktioner, der generelt er tilgængelige i ugen med d. 6. april

- **Orlovs- og fraværsfunktioner** – Du kan få flere oplysninger i [Oversigt over orlov og fravær](hr-leave-and-absence-overview.md).

- **Funktioner til administration af frynsegoder** – Du kan få flere oplysninger i [Oversigt over administration af frynsegoder](hr-benefits-management-overview.md).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Grænser for miljøer i Human Resources er nu baseret på licensopdateringer (394595)

Grænsen for antallet af miljøer pr. projekt i LCS er blevet ændret. Den forrige grænse var to miljøer. Grænsen for det antal produktions- og sandkassemiljøer, du kan oprette til Human Resources i LCS, er nu baseret på licensopdateringer. Du kan nu oprette så mange miljøer, der er behov for, pr. LCS-projekt, afhængigt af antal købte licenser. Den nye licensering, der blev opdateret den 1. februar 2020, giver kunderne mulighed for at købe flere miljøer. Yderligere oplysninger om licenskrav til andre miljøer finder du i [licensvejledningen til Dynamics 365](https://dynamics.microsoft.com/pricing/#HumanResources).
 
## <a name="error-when-trying-to-delete-a-questionnaire-428603"></a>Der opstod en fejl under forsøg på at slette et spørgeskema (428603)

I denne uges opdatering rettes et problem, hvor følgende fejl vises, når du forsøger at slette et spørgeskema:

Der er fundet et skævt X++ TTSBEGIN/TTSCOMMIT-par.

## <a name="performance-journal-and-professional-certificates-security-issue-428499"></a>Sikkerhedsproblem i performancekladde og professionelle certifikater (428499)

Denne ændring begrænser synligheden af performancekladde og professionelle certifikater baseret på de virksomheder, de har adgang til. 

## <a name="the-abbreviation-for-quebec-and-manitoba-387510"></a>Forkortelsen af Quebec og Manitoba (387510)

Startdata er blevet opdateret, så de afspejler den korrekte forkortelse for Manitoba og Quebec.

## <a name="new-entities-available-in-data-management-framework"></a>Nye enheder er tilgængelige i Data Management Framework

Følgende enheder er nu tilgængelige. Hvis disse enheder ikke vises på listen over enheder, skal du bruge indstillingen **Opdater enheder** i **Strukturparametre > Enhedsindstillinger > Opdater liste over enheder**.

 - Banktransaktion for orlov og fravær V2
 - Orlovs- og fraværstilmelding V2
 - Orlovs- og fraværsplanniveau V2
 - Orlovs- og fraværsplan V2

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse-løsning er nu tilgængelig med følgende ændringer:

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
| Nyt objekt **Titel** | <ul><li>**Titel** er tilføjet</li></ul>Den nye enhed **Titel** er inkluderet i Dataverse, men den er ikke refereret fra enhederne **Stilling** eller **Job** i øjeblikket. |

> [!NOTE]
> Økonomiske dimensioner for både stillinger og beskæftigelse giver en integration med én retning for opdateringer fra HR til Dataverse. Opdateringer af økonomiske dimensioner synkroniseres i øjeblikket ikke fra Dataverse til HR.

I løbet af de næste par uger vil disse enhedsændringer være tilgængelige i alle miljøer. Sådan installeres den nyeste Dataverse-løsning til HR manuelt:

1.  Gå til [Power Platform Administration](https://admin.powerplatform.microsoft.com).

2.  Vælg **Miljøer**.

3.  Find det miljø, du vil opgradere. Miljøet skal svare til **Miljønavn** i sektionen **Dataverse-oplysninger** i formularen **Om** i HR.

4.  Vælg miljøet for at få vist miljødetaljerne.

5.  Vælg **Administrer løsninger** på handlingslinjen i toppen. Der åbnes et nyt browservindue, hvor du kan navigere til **Dynamics 365 Administration** i konteksten af dit miljø.

6.  Vælg **Dynamics 365 Human Resources Anchor** i listen **Løsning**.

7.  Vælg **Opgrader** for at anvende den seneste løsning.

## <a name="in-preview"></a>Som prøveversion

## <a name="leave-suspension"></a>Forlad suspension

Du kan afbryde orlov og fravær i Human Resources for en medarbejder. Når du suspendere orlov, stoppes orloven for de valgte orlovstyper. Hvis suspensionen finder sted, når en periodisering er blevet behandlet, opretter suspensionen en forholdsmæssig justering til medarbejderens orlov. Du kan finde flere oplysninger i [Suspender orlov](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Overføre regler

Du kan angive en orlovstype for overførselssaldi, hvor gennemførte reguleringer overføres. Hvis en medarbejder f.eks. overfører 10 dage, kan du vælge en anden orlovstype for disse 10 dage. Du kan finde flere oplysninger i [Konfigurere orlovs- og fraværstyper](hr-leave-and-absence-types.md).

## <a name="coming-soon"></a>Kommer snart

## <a name="new-production-release-cadence"></a>Ny udgivelsestakt for produktionsudgivelser

Fra og med april skifter udgivelsestakten for Human Resources fra en ugentlig opdatering til en opdatering hver anden uge. Hvis du vil sikre en justering med sikker implementeringspraksis og vedligeholde høje standarder for stabilitet og pålidelighed i tjenesten, vil processen med at implementere tjenesteopdateringer til alle områder være en fase på to uger. Yderligere test og skærme vil være på plads for at sikre en vellykket implementering på hvert trin i processen. Du kan få flere oplysninger om frigivelsestakt i [Opdateringsproces](hr-admin-setup-update-process.md).

## <a name="known-issues"></a>Kendte problemer

## <a name="employment-detail-entity"></a>Enhed med ansættelsesdetaljer

Enheden **Ansættelsesoplysningerne** er blevet opdateret med følgende felter: **Betalingsfrekvens**, **Ansættelseskategori-id**, **Ansættelsestype**, **Ansættelsestype-id** og **Status for frynsegodeansættelse**. Opsætningsdataene for disse felter afhænger af, at administration af frynsegoder er aktiveret i Funktionsstyring. Disse felter må ikke udfyldes eller opdateres i enheden **Ansættelsesoplysninger**, da det vil resultere i fejl under importen.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>Prøveversionen af SharePoint fungerer ikke i visse miljøer

Hvis visning af dokumenter, der er gemt i SharePoint, ikke fungerer, kan du prøve følgende procedure:

1. Kontroller, at administratorbrugerkontoen har en mail tilknyttet brugerposten. Du kan få vist disse oplysninger på siden **Bruger**. Hvis e-mail ikke er konfigureret, skal du tilføje e-mailadressen og udbyderen med OData Excel-tilføjelsesprogrammet. E-mailadressen findes som standard ikke i Excel-designet. Du skal redigere Excel-designet, tilføje alle felter, anvende og opdatere. Når du har fuldført disse trin, kan du opdatere administratorkontoen.

2. Når administratorkontoen har en tilknyttet mailkonto, skal du logge på Human Resources med administrator-legitimationsoplysninger.

3. Åbn en vedhæftet fil i SharePoint for at starte dokumentvisningen.

4. Log på med en anden brugerkonto, der har adgang til vedhæftede filer, og kontroller, at eksempelvisningen fungerer som forventet.

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]