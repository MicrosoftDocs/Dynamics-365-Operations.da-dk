---
title: Administrere forretningspartnerbrugere på B2B-e-handelswebsteder
description: Dette emne beskriver, hvordan du kan tilføje, redigere og slette forretningspartnerbrugere på Microsoft Dynamics 365 Commerce business-to-business (B2B)-e-handelswebsteder og i Commerce-hovedkontoret.
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c2fb4846a8457296a2ce758198ade5f4b0df8124
ms.sourcegitcommit: 96e2fb26efd2cd07bbf97518b5c115e17b77a0a8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2022
ms.locfileid: "8616851"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Administrere forretningspartnerbrugere på B2B-e-handelswebsteder

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du kan tilføje, redigere og slette forretningspartnerbrugere på Microsoft Dynamics 365 Commerce business-to-business (B2B)-e-handelswebsteder og i Commerce-hovedkontoret.

> [!NOTE]
> - Emnet [Administrere B2B-forretningspartnere, der bruger kundehierarkier](partners-customer-hierarchies.md), er en forudsætning for dette dokument.
> - Sørg for, at du initialiserer dokumenttyperne i Commerce Headquarters ved at åbne formen **Dokumenttyper** på **Organisationsadministration \> Dokumentstyring \> Dokumenttyper**.

B2B-e-handelswebsteder kræver, at organisationer registrerer sig som forretningspartnere. Når en organisation har indsendt registreringsoplysninger til et B2B-e-handelswebsted, gennemgår registreringsanmodningen en kvalifikationsproces. Hvis organisationen er kvalificeret, er den startet som forretningspartner.

Når en organisation er startet som forretningspartner, identificeres den organisationsbruger, der startede anmodningen om at blive forretningspartner, som administratorbruger og tildeles rettigheder til at modtage yderligere autoriserede brugere af webstedet for B2B-e-handel. Disse autoriserede brugere kan derefter placere ordrer på vegne af forretningspartneren.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Konfigurere administratorbrugeren til en ny forretningspartner

Potentielle forretningspartnere kan igangsætte onboardingprocessen på et B2B-e-handelswebsted ved at sende en anmodning om onboarding via et link til B2B-webstedet. De kan derefter bruge den formular, der kan tilpasses, til at levere de detaljer, der kræves til onboarding og tilmelding. Når anmodningen er sendt, vises siden med bekræftelse af afsendelse. Hvis afsendelsen godkendes, bliver det firma, som anmodningen blev afsendt til, til en forretningspartner, og anmoderen (den bruger, der startede anmodningen om onboarding) bliver administrator af forretningspartneren.

Følg disse trin for at godkende en forretningspartneranmodning i Commerce-hovedkontoret.

1. Gå til **Detail og handel-it \> Distributionsplan**.
1. Kør **P-0001**-jobbet for at trække alle forretningspartneranmodninger til Commerce Headquarters.
1. Når **P-0001**-jobbet er kørt korrekt, skal du gå til **Retail og Commerce IT \> Kunde**, og køre jobbet **Synkroniser kunder og kanalanmodninger**. Når jobbet er kørt korrekt, oprettes anmodningerne om onboarding som kundeemner af typen **B2B-kundeemne** i Commerce-hovedkontoret. 
1. Gå til **Kunder \> Alle kundeemner**, og vælg kundeemneposten for den nye forretningspartner for at åbne siden med kundeemnedetaljer.
1. Under fanen **Generelt** skal du vælge **Konverter \> Godkend/Afvis** for at godkende anmodningen om onboarding. Når der vises en bekræftelsesmeddelelse, skal du bekræfte, at du vil fortsætte med processen, og derefter godkende anmodningen. Godkendelsen ændrer feltet **Status** for kundeemneposten til **Godkendt**. Der sendes derefter en e-mail til anmoderens e-mail-adresse for at bekræfte, at deres organisation er blevet godkendt som forretningspartner. Der oprettes også et debitorhierarki, hvor anmoderen tilføjes som administrator for forretningspartneren.

    > [!NOTE]
    > I øjeblikket sendes bekræftelsesmailen med det samme efter godkendelse. Funktionaliteten i fremtidig Commerce vil dog give administratoren mulighed for at udløse mailene manuelt.

1. Gå til **Retail og Commerce IT \> Distributionsplan**, og kør jobbet **1010 (Kunder)** for at flytte de nyoprettede debitor- og debitorhierarkiposter til kanaldatabasen.

> [!NOTE]
> For at sikre, at de nye kundeposter sendes til kanaldatabasen, skal mindst ét af de adressekartoteker, der er knyttet til kunden, være medtaget i det kundeadressekartotek, der er tilknyttet onlinebutikken. Du kan automatisere denne proces ved at konfigurere adressekartoteket hos onlinebutikkens standardkunde, så systemet kopierer værdien i adressekartoteket til alle nye kunder.

Når debitorhierarkiposterne er synkroniseret til kanaldatabasen, kan anmoderen logge på webstedet for B2B-e-handel ved hjælp af den mailadresse, de har angivet, da de sendte anmodningen om onboarding. Brugere kan bruge tilmeldingsflowet til at definere adgangskoden til deres konto. Du kan finde oplysninger om aktivering af Azure Active Directory-posten for (Azure AD) B2C-identitetsudbyderen til den B2B-kundepost, der blev oprettet i forbindelse med godkendelse af kundeemne, under [Aktivere automatisk sammenkædning](../identity-record-linking.md).

## <a name="notify-b2b-prospects-when-they-are-approved-or-rejected"></a>Give B2B-kundeemner besked, når de godkendes eller afvises

Når du godkender eller afviser en anmodning om onboarding af et B2B-kundeemne, kan du automatisk sende en mailbesked til kundeemnet.

Hvis du vil konfigurere mailbeskeder i Commerce-hovedkontoret for hændelser af **B2B-kundeemnet, der er godkendt**, eller **B2B-kundeemnet, der er afvist**, skal du følge disse trin.

1. Opret mailskabeloner til mails, der sendes til kundeemner, når enten **B2B-kundeemnet er godkendt** eller **B2B-kundeemnet er afvist** udløses som beskedtype. Du kan finde oplysninger om de pladsholdere, som beskedtyperne understøtter, under [Beskedtyper](../email-templates-transactions.md#notification-types). Du kan finde oplysninger om, hvordan du opretter mailskabeloner, under [Oprette en mailskabelon](../email-templates-transactions.md#create-an-email-template).
1. Føj **B2B-kundeemnet er godkendt** og **B2B-kundeemnet er afvist** som beskedtyper til din mailbeskedprofil, og knyt dem til de mailskabeloner, du har oprettet. Du kan finde flere oplysninger om beskedprofiler i [Konfigurere en mailbeskedprofil](../email-notification-profiles.md).

## <a name="onboard-additional-business-partner-users"></a>Få flere forretningspartnerbrugere med i gang

Forretningspartneradministratoren kan efter behov få yderligere forretningspartnerbrugere med til webstedet for B2B-e-handel.

Hvis du vil have flere forretningspartnerbrugere med på et B2B-e-handelswebsted, skal du følge disse trin.

1. Log på B2B-e-handelswebstedet som administrator.
1. Gå til **Min konto \> Organisationsbrugere \> Vis oplysninger**, og vælg **Tilføj bruger**.
1. Angiv de nødvendige oplysninger, og klik derefter på **Gem**. Status for den nye bruger er **Afventer**.

Når **P-0001** og **Synkroniser kunder og kanalanmodninger** er kørt, oprettes der en kundepost af typen **Person** for den nye bruger i Commerce-hovedkontoret. Denne kundepost er også knyttet til den relevante forretningspartners kundehierarkipost. Desuden sendes der en e-mail til den nye brugers e-mail-adresse for at give dem besked om, at de er blevet tilføjet som bruger af forretningspartnerorganisationen og nu kan logge på B2B-e-commerce-webstedet.

Kør derefter jobbet **1010 (Kunder)** for at synkronisere den nye forretningspartnerbruger med kanaldatabasen.

Når kundeposten er synkroniseret, angives status for brugeren på B2B-e-handelswebstedet til **Aktiv**, og den nye bruger kan logge på webstedet for B2B-e-handel ved hjælp af deres e-mailadresse. Brugere kan bruge tilmeldingsflowet til at definere adgangskoden til deres konto. Du kan finde oplysninger om aktivering af Azure AD-posten for B2C-identitetsudbyderen til den B2B-kundepost, der blev oprettet i Commerce-hovedkontoret, under [Aktivere automatisk sammenkædning](/dynamics365/commerce/identity-record-linking.md).

## <a name="edit-business-partner-user-details"></a>Redigere brugeroplysninger for forretningspartner

Hvis du vil redigere detaljerne for forretningspartnerbrugere, skal du følge disse trin.

1. Log på B2B-e-handelswebstedet som administrator.
1. Gå til **Min konto \> Organisationsbrugere \> Vis detaljer**, vælg knappen **Rediger** (blyantssymbol), foretag de nødvendige ændringer, og vælg derefter **Gem**. Ændringerne træder først i kraft, når **P-0001**, **Synkroniser kunder og kanalanmodninger** og **1010 (Kunder)**-jobs er kørt.

## <a name="remove-a-business-partner-user"></a>Fjerne en forretningspartnerbruger

Efter behov kan en administrator fjerne eksisterende brugere af en forretningspartnerorganisation fra listen over brugere, der kan få adgang til B2B-e-handelswebstedet.
Hvis du vil fjerne en forretningspartnerbruger, skal du følge disse trin.
- Log på B2B-e-handelswebstedet som administrator.
- Gå til **Min konto > Organisationsbrugere \> Vis oplysninger**, og vælg knappen **Fjern** ("X"-symbol). Når der vises en bekræftelsesmeddelelse, skal du bekræfte, at du vil fjerne brugeren. Ændringen træder først i kraft, når **P-0001**, **Synkroniser kunder og kanalanmodninger** og **1010 (Kunder)**-jobs er kørt.

> [!NOTE]
> Når du fjerner en bruger fra listen over brugere, der har adgang til B2B-e-handelswebstedet, fjernes den tilsvarende debitorpost fra forretningspartnerens debitorhierarkipost. Selve kundeposten er dog ikke slettet fra Commerce Headquarters.

## <a name="onboard-existing-customers-as-business-partners-on-the-b2b-e-commerce-website"></a>Onboarde eksisterende kunder som forretningspartnere på B2B-e-handelswebstedet

Administratorer kan få forretningspartnere og brugere direkte i Commerce Headquarters. Denne egenskab er nyttig for onboarding af dine eksisterende forretningspartnere på B2B-e-handelswebstedet.

Følg disse trin for at administratorer kan få forretningspartnere og brugere direkte i Commerce Headquarters.

1. Opret eller vælg en kunde af typen **Organisation**, der skal tilføjes som forretningspartner.
1. Opret eller vælg en kunde af typen **Person**, der skal tilføjes som administrator eller bruger for forretningspartneren. Sørg for, at den primære mailadresse er tilknyttet kunderne. Disse mailadresser bruges til at logge på webstedet. 

    > [!NOTE]
    > Systemet skal kunne finde en entydig kundepost for brugere, der skal kunne logge på webstedet. Hvis systemet finder mere end én kunde, der har samme primære mailadresse i den juridiske enhed, kan brugeren ikke logge på webstedet.

1. Opret et debitorhierarki-id.
1. Indtast et navn i feltet **Navn**.
1. Angiv en kunde i forretningspartnerorganisationen i feltet **Organisation**.
1. Vælg **Tilføj** i oversigtspanelet **Hierarki**.
1. I feltet **Navn** skal du vælge en kunde af typen **Person**.
1. Vælg rollen **Administrator** for kunden, der skal udpeges som administrator.
1. Gentag denne proces for at føje flere kunder til hierarkiet.

## <a name="additional-information"></a>Yderligere oplysninger

- Alle de job, der nævnes i dette emne, kan konfigureres til at køre efter en plan i et batchformat. Det ønskes, at forretningspartnere vil konfigurere batchjob efter behov.
- I øjeblikket kan der kun udpeges én bruger-/kundepost som administratorbruger, og denne rolle kan kun ændres i Commerce Headquarters. Der er ingen understøttelse af selvbetjeningsfunktioner, der giver forretningspartnere mulighed for at udpege flere administratorer eller ændre administratorer fra B2B-e-handelswebsteder.
- Selvom forbrugsgrænser kan defineres for brugerne, er håndhævelsen af forbrugsgrænser i løbet af ordreindtastningsprocessen endnu ikke implementeret.
- Al forretningslogik og -validering for en brugers erfaring med et B2B-e-handelswebsted er baseret på konfigurationen af den kundepost, der er knyttet til brugeren i Commerce Headquarters.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette et B2B-e-handelswebsted](set-up-b2b-site.md)

[Administrere B2B-forretningspartnere ved hjælp af kundehierarkier](partners-customer-hierarchies.md)

[Konfigurere betalingsmåden for debitorkonti for B2B-e-handelswebsteder](payment-method.md)

[Angive produktantalsgrænser for B2B-e-handelswebsteder](quantity-limits.md)

[Oversigt over nummerserier](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
