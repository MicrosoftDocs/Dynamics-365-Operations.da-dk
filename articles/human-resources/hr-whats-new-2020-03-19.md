---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (19. marts 2020)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 19. marts 2020.
author: andreabichsel
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4f88a3a83794cc46f670143bdb97c9624cff8dd0
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694739"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-19-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (19. marts 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.3014. Tallene i parenteser i nogle overskrifter henviser til Lifecycle Services (LCS)-supportnumre til reference.

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Grænser for miljøer i Human Resources er nu baseret på licensopdateringer (394595)

Grænsen for antallet af miljøer pr. projekt i Lifecycle Services (LCS) er blevet ændret. Den forrige grænse var to miljøer. Grænsen for det antal produktions- og sandkassemiljøer, du kan oprette til Human Resources i LCS, er nu baseret på licensopdateringer. Du kan nu oprette så mange miljøer, der er behov for, pr. LCS-projekt, afhængigt af antal købte licenser. Den nye licensering, der blev opdateret den 1. februar 2020, giver kunderne mulighed for at købe flere miljøer. Yderligere oplysninger om licenskrav til andre miljøer finder du i [licensvejledningen til Dynamics 365](https://dynamics.microsoft.com/pricing/#HumanResources).

## <a name="provide-cross-company-viewing-of-compensation-data-for-employees-and-managers-403904"></a>Visning af kompensationsdata på tværs af firmaer for medarbejdere og ledere (403904)

Slå denne funktion til i arbejdsområdet **Funktionsstyring**. Du kan finde flere oplysninger i [Aktivere eller deaktivere funktioner i prøveversion](hr-admin-manage-features.md#enable-or-disable-preview-features).

Når du aktiverer denne funktion, kan ledere se direkte og udvidede underordnedes kompensation uden at skulle logge på ansættelsesfirmaet. Den fulde kompensationshistorik er tilgængelig fra påloggede firmaer, som lederen har adgang til. Yderligere oplysninger finder du i [Oversigt over selvbetjening for medarbejdere og ledere](hr-employee-manager-self-service-overview.md).

## <a name="enable-global-address-book-merge-functionality-427189"></a>Aktivere funktionen til fletning af globale adressekartoteker (427189)

Du kan nu flette identiske poster i adressekartoteket ved at vælge de dublerede poster og vælge **Flet** fra siden **Globalt adressekartotek**.

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-the-multiple-leave-type-feature-on-419635"></a>Kunne ikke regulere saldoen for en plan uden periodiseringer, der er oprettet med funktionen til flere orlovstype slået til (419635)

Du kan nu justere saldi for orlovsplaner, der er oprettet med prøvefunktionen **Flere orlovstyper** aktiveret i Funktionsstyring.

## <a name="primary-position-field-in-the-workerpositionassignmententity-when-an-employee-is-terminated-420774"></a>Feltet Primær stilling i WorkerPositionAssignmentEntity, når en medarbejder er fratrådt (420774)

For medarbejdere, hvis ansættelse er ophørt, vises den primære stilling, der var aktiv på ophørstidspunktet, i enheden. Der vil ikke længere blive oprettet en dubletpost for medarbejderens stillingstildeling i forbindelse med integrationer. 

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

3.  Find det miljø, du vil opgradere. Miljøet skal svare til **Miljønavn** i sektionen **Common Data Service-oplysninger** i formularen **Om** i HR.

4.  Vælg miljøet for at få vist miljødetaljerne.

5.  Vælg **Administrer løsninger** på handlingslinjen i toppen. Der åbnes et nyt browservindue, hvor du kan navigere til **Dynamics 365 Administration** i konteksten af dit miljø.

6.  Vælg **Dynamics 365 Human Resources Anchor** i listen **Løsning**.

7.  Vælg **Opgrader** for at anvende den seneste løsning.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>Prøveversionen af SharePoint fungerer ikke i visse miljøer

Hvis visning af dokumenter, der er gemt i SharePoint, ikke fungerer, kan du prøve følgende procedure:

1. Kontroller, at administratorbrugerkontoen har en mail tilknyttet brugerposten. Du kan få vist disse oplysninger på siden **Bruger**. Hvis e-mail ikke er konfigureret, skal du tilføje e-mailadressen og udbyderen med OData Excel-tilføjelsesprogrammet. E-mailadressen findes som standard ikke i Excel-designet. Du skal redigere Excel-designet, tilføje alle felter, anvende og opdatere. Når du har fuldført disse trin, kan du opdatere administratorkontoen.

2. Når administratorkontoen har en tilknyttet mailkonto, skal du logge på Human Resources med administrator-legitimationsoplysninger.

3. Åbn en vedhæftet fil i SharePoint for at starte dokumentvisningen.

4. Log på med en anden brugerkonto, der har adgang til vedhæftede filer, og kontroller, at eksempelvisningen fungerer som forventet.

## <a name="coming-soon"></a>Kommer snart

### <a name="platform-update-33"></a>Platform update 33

- Fuld side-apps (eksempel) – denne eksempelfunktion, som kræver, at du aktiverer funktionen Gemte visninger, tillader, at Power Apps og tredjeparts apps tilføjes som en fuld sideoplevelse via dashboardet.

- Gemte visninger (eksempel) – Denne eksempelfunktion gør det muligt at gemme visninger, hvilket giver en væsentlig forbedring af det personligt tilpassede undersystemet. Denne funktion giver brugere mulighed for at have flere navngivne sæt af tilpasninger pr. side. Du kan også publicere visninger til sikkerhedsroller.

- Optimeret "er en af"-filtreringsoplevelse – Denne funktion aktiverer en optimeret "er en af"-filtreringsoplevelse, der gør det nemmere at angive flere filterværdier, har en enklere mekanisme til at fjerne enkelte eller alle filterværdier og har en mere kompakt og intuitiv visualisering af filterværdier.

- Anbefalede felter – brugere skal ofte føje felter til et gitter eller en side. Det kan være svært med så mange tilgængelige felter. I stedet for at skulle søge gennem en stor liste, gør denne funktion det muligt for systemet at placere et sæt anbefalede felter øverst baseret på, hvad andre brugere oftest tilføjer i lignende scenarier.

- Træge standardhandlinger i gitre – Denne funktion sikrer, at standardhandlingen i et gitter sammenkædes med en bestemt kolonne i et gitter, uanset om den pågældende kolonne flyttes eller skjules.

## <a name="new-production-release-cadence"></a>Ny udgivelsestakt for produktionsudgivelser

Fra og med april skifter udgivelsestakten for Human Resources fra en ugentlig opdatering til en opdatering hver anden uge. Dette sikrer overholdelse af implementeringspraksis og vedligeholdelse af de høje standarder for stabilitet og pålidelighed i tjenesten. Vi sørger for yderligere test og skærme for at sikre en vellykket implementering på hvert trin i processen. Yderligere oplysninger om frigivelsestakt finder du i [Opdateringsproces](hr-admin-setup-update-process.md).

## <a name="in-preview"></a>Som eksempel

Følgende prøvefunktioner er tilgængelige den 3. februar 2020:

- **Visningsfunktioner for orlov og fravær** - Du kan finde flere oplysninger under [Visningsfunktioner for orlov og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Prøveversionsfunktion: Administration af frynsegoder** – Der er flere oplysninger, herunder kendte problemer, under [Oversigt over Administration af frynsegoder](hr-benefits-management-overview.md).

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]