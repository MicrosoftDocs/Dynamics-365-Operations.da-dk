---
title: Konfigurere og vedligeholde kreditorsamarbejde
description: I dette emne forklares, hvordan du konfigurerer kreditorsamarbejde i Dynamics 365 Supply Chain Management. Det forklares også, hvordan du klargør nye brugere af kreditorsamarbejde og administrerer sikkerhedsrollerne for disse brugere.
author: GalynaFedorova
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirExternalRole, SysUserRequestListPage, VendVendorPortalUsers, WorkflowTableListPageRnr
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 220774
ms.assetid: 69d05e8b-7dc2-48ea-bc24-bea9ac963579
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4b59513d86426d3c1bfd759b9aabc331e58d5423
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677556"
---
# <a name="set-up-and-maintain-vendor-collaboration"></a>Konfigurere og vedligeholde kreditorsamarbejde

[!include [banner](../includes/banner.md)]

Grænsefladen for kreditorsamarbejde viser begrænsede oplysninger om indkøbsordrer, fakturaer og konsignationslager til eksterne kreditorbrugere. Fra denne brugergrænseflade kan en kreditor også besvare tilbudsanmodninger og få vist og redigere grundlæggende firmaoplysninger.

I dette emne forklares, hvordan du konfigurerer kreditorsamarbejde i Dynamics 365 Supply Chain Management. Det forklares også, hvordan du konfigurerer en arbejdsgang for at klargøre nye brugere af kreditorsamarbejde, og hvordan du administrerer sikkerhedsrollerne for disse brugere.

> [!NOTE]
> Oplysningerne om opsætning af sikkerhedsroller til kreditorsamarbejde gælder kun for den aktuelle version af Finans og drift. I Microsoft Dynamics AX 7.0 (februar 2016) og Microsoft Dynamics AX-programversion 7.0.1 (maj 2016), samarbejder du med kreditorer ved hjælp af modulet **Kreditorportal**. Du kan finde oplysninger om brugerrettigheder for kreditorportalen i Microsoft Dynamics AX, under [Brugersikkerhed på kreditorportal](configure-security-vendor-portal-users.md).

## <a name="set-up-vendor-collaboration-security-roles"></a>Konfigurere sikkerhedsroller for kreditorsamarbejde

En indkøbsmedarbejder eller en kreditor, der har tilstrækkelige rettigheder, kan anmode om, at en kontaktperson klargøres som bruger, ved at aktivere **Klargør kreditorbruger** på kontaktpersonposten. Under klargøringsprocessen vælges brugerrettigheder til den nye eksterne bruger, og den nye kreditorbrugeranmodning sendes. Det er vigtigt, at du konfigurerer de brugerrettigheder, der kan vælges i kreditorbrugeranmodningen, korrekt. Ellers kan kreditorer få adgang til oplysninger, som de ikke skal have adgang til, i Supply Chain Management.

### <a name="set-up-the-security-roles-that-are-available-for-selection-when-a-new-user-request-is-used-for-a-contact-person"></a>Konfigurere de sikkerhedsroller, der kan vælges, når der bruges en ny brugeranmodning for en kontaktperson

1. Vælg **Systemadministration** &gt; **Sikkerhed** &gt; **Eksterne roller**.
2. Vælg **Ny**, og vælg derefter en sikkerhedsrolle og partrollen **Kreditor**.

Du kan tilføje rollerne **Kreditoradministrator (ekstern)** og **Kreditor (ekstern)**, der findes i Supply Chain Management. Du kan også bruge de sikkerhedsroller, som firmaet har oprettet.

Du skal kun gøre rollen **Kreditoradministrator (ekstern)** tilgængelig, hvis kreditorer skal kunne oprette nye kontaktpersoner, sende brugeranmodninger om kreditorsamarbejde for nye brugere og ændringer i brugeroplysninger samt håndtere disse anmodninger via en arbejdsgang.

Hvis du planlægger at konfigurere kreditorkontakter og -brugere manuelt, kan du nøjes med at gøre rollen **Kreditor (ekstern)** tilgængelig. Denne rolle vil derefter være den eneste rolle, der kan anmodes om via en kreditorbrugeranmodning.

> [!NOTE]
> Rollen **Systembruger** tildeles automatisk, når du opretter en ny brugerkonto manuelt. Du skal derfor fjerne denne rolle og tildele rollen **SystemExternalUser**. Hvis der oprettes nye brugerkonti via den arbejdsgang, der startes af en kreditorbrugeranmodning om klargøring af en ny bruger, tildeles en eller flere af de roller, du har konfigureret til kreditorsamarbejde, og rollen **SystemExternalUser**.

#### <a name="vendor-admin-external-security-role"></a>Sikkerhedsrollen Kreditoradministrator (ekstern)

Rollen **Kreditoradministrator (ekstern)** kan bruges til eksterne kreditorer, der vedligeholder kontaktoplysninger for kreditorer og opretter anmodninger om klargøring af nye brugere til kreditorsamarbejde. Eksterne brugere, der har denne sikkerhedsrolle, kan udføre følgende opgaver:

- Få vist og redigere kontaktpersonoplysninger som for eksempel personens titel, mailadresse og telefonnummer.
- Føje en ny eller eksisterende kontaktperson til de kreditorkonti, de er kontaktperson for.
- Slette de kontaktpersoner, de har oprettet.
- Aktivere eller deaktivere tilknytningen mellem en kontaktperson og en kreditorkonto. Når tilknytningen mellem en kontaktperson og en kreditorkonto er deaktiveret, kan der ikke henvises til kontaktpersonen i nye indkøbsordrer eller andre dokumenter.
- Nægte eller give en kontaktperson adgang til dokumenter på brugergrænsefladen for kreditorsamarbejde, der er specifikke for kreditorkontoen. Når tilknytningen mellem en kontaktperson og en kreditorkonto er deaktiveret, afvises adgangen til dokumenter, der er specifikke for kreditorkontoen, altid.
- Anmode om en ny brugerkonto for en kontaktperson ved hjælp af handlingen **Klargør bruger**.
- Anmode om, at en kontaktpersons brugerkonto deaktiveres.
- Anmode om, at en kontaktpersons brugerkonto ændres for at tilføje eller fjerne sikkerhedsroller.
- Få vist tilbudsanmodninger.

#### <a name="vendor-external-security-role"></a>Sikkerhedsrollen Kreditor (ekstern)

**Rollen Kreditor (ekstern)** kan bruges til eksterne kreditorer, der skal arbejde med indkøbsordrer. Eksterne brugere, der har denne sikkerhedsrolle, kan udføre følgende opgaver:

- Besvare og få vist oplysninger om indkøbsordrer.
- Vedligeholde kreditorsamarbejdsfakturaer.
- Få vist konsignationslager.
- Få vist og besvare tilbudsanmodninger.
- Få vist kreditoroplysninger.

## <a name="set-up-security-roles-that-are-used-when-prospective-vendors-are-onboarded"></a>Konfigurere sikkerhedsroller, der bruges, når mulige kreditorer onboardes

Hvis du vil onboarde kreditorer, der er startet via en anmodning om registrering som mulig kreditor, skal du konfigurere en ekstern sikkerhedsrolle. Denne rolle tildeles til nye brugere under den klargøringsproces, der styres af arbejdsgangen af typen **Brugeranmodningsarbejdsgang (platform)**. Du kan finde flere oplysninger i afsnittet [Konfigurere arbejdsgange til behandling af brugeranmodninger om kreditorsamarbejde](#set-up-workflows-to-process-vendor-collaboration-user-requests) senere i dette emne.

Du kan finde flere oplysninger om, hvordan mulige kreditorer onboardes, under [Modtage kreditorer](vendor-onboarding.md).

### <a name="set-up-a-security-role-that-is-used-when-a-new-prospective-vendor-user-request-is-submitted"></a>Opret en sikkerhedsrolle, der skal bruges, når en ny anmodning fra en mulig kreditorbruger sendes

1. Vælg **Systemadministration** > **Sikkerhed** > **Eksterne roller**.
2. Vælg **Ny**, og vælg derefter en sikkerhedsrolle og partrollen **Mulig kreditor**.

Du skal tilføje rollen **Kreditoremne (ekstern)**, der findes i Supply Chain Management.

Sikkerhedsrollen giver kun adgang til den nye guide til kreditorregistrering.

## <a name="set-up-workflows-to-process-vendor-collaboration-user-requests"></a>Oprette arbejdsgange til behandling af brugeranmodninger til kreditorsamarbejde

Som en hjælp til at sikre, at alle relevante opgaver bliver fuldført, og at de relevante godkendelser gives, skal du oprette arbejdsgange til håndtering af brugeranmodninger om kreditorsamarbejde.

Brugeranmodninger om kreditorsamarbejde sendes enten af eksterne kreditorer, der har sikkerhedsrollen **Kreditoradministrator (ekstern)** eller lignende rettigheder, eller af indkøbsmedarbejderne i firmaet. De kan også genereres ud fra anmodninger om registrering af mulige kreditorer under processen til onboarding af kreditorer.

Der er tre typer anmodninger:

- Anmodninger om at klargøre en ny bruger
- Anmodninger om at deaktivere en eksisterende bruger
- Anmodninger om at redigere sikkerhedsrollerne for en eksisterende bruger

Du kan finde flere oplysninger om brugeranmodninger om kreditorsamarbejde i [Administrere brugere af kreditorsamarbejde](manage-vendor-collaboration-users.md).

Du skal oprette to eller flere arbejdsgange for at behandle alle tre typer brugeranmodninger til kreditorsamarbejde. Nye arbejdsgange oprettes på siden **Brugerarbejdsgange**.

### <a name="example-of-a-workflow-for-provisioning-new-users-and-modifying-security-roles"></a>Eksempel på en arbejdsgang til klargøring af nye brugere og redigering af sikkerhedsroller

Når du skal håndtere kreditorbrugeranmodninger om at oprette nye brugere og redigere sikkerhedsroller, kan du oprette en forgreningsbetingelse i starten af arbejdsgangen. På denne måde bruges der en anden forgrening i arbejdsgangen, afhængigt af om der anmodes om at oprette en ny bruger eller redigere en eksisterende bruger.

Hvis du vil konfigurere denne forgrening, skal du oprette en ny arbejdsgang af typen **Brugeranmodningsarbejdsgang (platform)**. Forgreningerne i denne arbejdsgang kan indeholde følgende elementer.

#### <a name="branch-to-provision-new-users"></a>Forgrening til klargøring af nye brugere

1. Tildel en godkendelsesopgave til den person, der er ansvarlig for at godkende, at nye brugere skal have adgang til oplysninger om kreditorsamarbejde.
2. Tildel en opgave til den person, der er ansvarlig for at anmode om nye Microsoft Azure Active Directory-brugerkonti (Azure AD) på Azure-portalen. Brug den foruddefinerede opgave **Send invitation til Azure B2B-bruger** til dette trin. B2B-brugere kan eksporteres automatisk til Azure AD. Brug den foruddefinerede **Klargøring Azure AD B2B-bruger**. Du kan finde flere oplysninger under [Eksportere B2B-brugere til Azure AD](../../fin-ops-core/dev-itpro/sysadmin/implement-b2b.md).
3. Tildel en godkendelsesopgave til den person, der overfører til Azure. Hvis der ikke er oprettet en konto, afviser denne person opgaven og afslutter arbejdsgangen. Denne godkendelsesopgave kan springes over, hvis du har medtaget det trin, der automatisk eksporterer nye brugerkonti til Azure via B2B-API'en (Application Programming Interface).
4. Tilføj en automatiseret opgave, der klargør en ny bruger. Brug den foruddefinerede opgave **Klargør bruger automatisk** til dette trin.
5. Tilføj en opgave, der giver den nye bruger besked. Du kan sende den nye bruger en velkomstmail med en URL-adresse til Supply Chain Management. I denne mail kan du bruge en skabelon, som du opretter på siden **E-mailbeskeder**, og derefter vælge den på siden **Parametre for brugerarbejdsgange**. Skabelonen kan indeholde tagget **%portalURL%**. Når velkomstmailen genereres, erstattes dette tag af URL-adressen til Supply Chain Management-lejeren.

    > [!NOTE]
    > Denne arbejdsgang kan bruges i flere scenarier, der involverer brugeronboarding. Den kan for eksempel bruges, når mulige kreditorer eller kontaktpersoner kræver en konto til kreditorsamarbejde. Du skal derfor formulere mailen som en generel erklæring, der kan bruges til flere formål.

#### <a name="branch-to-modify-security-roles"></a>Forgrening til redigering af sikkerhedsroller

1. Tildel en godkendelsesopgave til den person, der er ansvarlig for at godkende ændringer af sikkerhedsroller.
2. Tilføj en automatiseret opgave, der tilføjer eller fjerner de relevante sikkerhedsroller. Brug opgaven **Klargør bruger automatisk** til dette trin.

### <a name="example-of-a-workflow-for-inactivating-a-user"></a>Eksempel på en arbejdsgang til deaktivering af en bruger

Opret en arbejdsgang af typen **Platform til deaktivering af brugeranmodningsarbejdsgang**, og tilføj derefter følgende opgaver.

1. Tildel en godkendelsesopgave til den person, der er ansvarlig for at acceptere anmodninger om at deaktivere brugere. Du kan tilføje betingelser for at automatisere dette godkendelsestrin.
2. Tilføj en automatiseret opgave, der deaktiverer brugeren. Brug opgaven **Deaktiver bruger automatisk** til dette trin.
3. Tilføj eventuelle oprydningsopgaver, der er påkrævet. Du kan for eksempel tilføje en opgave, der fjerner kontoen fra dit bibliotek på Azure-portalen.

## <a name="enable-vendor-collaboration-for-a-specific-vendor"></a>Aktivere kreditorsamarbejde for en bestemt kreditor

Før du opretter en brugerkonto til en person, der bruger kreditorsamarbejde, skal du konfigurere kreditoren til at bruge kreditorsamarbejde. Indstil feltet **Aktivering af samarbejde** under fanen **Generelt** på siden **Kreditorer**. Der findes følgende indstillinger:

- **Aktiv (IO bekræftes automatisk)** – Indkøbsordrer bekræftes automatisk, hvis kreditoren accepterer dem uden at anmode om ændringer.
- **Aktiv (IO bekræftes ikke automatisk)** – Din organisation skal manuelt bekræfte indkøbsordrer, når kreditoren har godkendt dem.

> [!NOTE]
> Indkøbsmedarbejdere i dit firma kan også udføre denne opgave.

## <a name="troubleshoot-the-provisioning-of-new-vendor-collaboration-users"></a>Foretage fejlfinding af klargøring af nye brugere af kreditorsamarbejde

Nye brugere af kreditorsamarbejde klargøres via den arbejdsgang, du har konfigureret til at behandle brugeranmodninger om kreditorsamarbejde af typen **Klargør kreditorbruger**.

Hvis mailadressen for en ny bruger af kreditorsamarbejde er medlem af et domæne, der er registreret med Azure som lejer (dvs. en administreret domænekonto), skal mailadressen være en eksisterende Azure AD-konto. Ellers kan klargøringsprocessen ikke fuldføres.

Du kan finde flere oplysninger om den proces, der bruges i opgaven **Send invitation til Azure B2B-bruger** i arbejdsgangen for Azure AD-kontostyring, under [Azure Active Directory B2B-samarbejde](/azure/active-directory/external-identities/what-is-b2b).

## <a name="additional-resources"></a>Yderligere ressourcer

[Kreditorsamarbejde med eksterne kreditorer](vendor-collaboration-work-external-vendors.md)

Se en kort video om processen til onboarding af kreditorer: [Onboarde en ny kreditor](https://www.youtube.com/watch?v=0KUc3AGaTKk&feature=youtu.be)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
