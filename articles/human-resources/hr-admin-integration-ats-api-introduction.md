---
title: Introduktion til API-integration for ansøgersporingssystem
description: Dette emne beskriver Dynamics 365 Human Resources ATS-integrations-API (Applicant Tracking System).
author: andreabichsel
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61d8502a8f420d387b5b7f48fca2f8a680f6f3f8
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464026"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a>Introduktion til API-integration for ansøgersporingssystem

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver Dynamics 365 Human Resources ATS-integrations-API (Applicant Tracking System). Formålet med API er at aktivere strømlinet integration mellem Dynamics 365 Human Resources og partner-ATS'er.

![ATS-integrationsflow](media/hr-admin-integration-ats-api-introduction-flow.png)

Den integrerede erfaring begynder i Human Resources, når en ansættelseschef opretter en rekrutteringsanmodning. Når anmodningen aktiveres, trækker ATS detaljerne for anmodningen om oprettelse af et rekrutteringsprojekt. Derefter følger rekrutteringspipelinen for at vælge og ansætte en kandidat til stillingerne. Endelig fuldfører ATS rundtur-integrationen ved at sende den valgte kandidats registrering til Human Resources. Kandidatposten kan derefter gennemgå flere valideringer og arbejdsgange for at oprette medarbejderposten.

Human Resources har tilføjet følgende komponenter for at aktivere integrationen:

1.  Funktioner til oprettelse af en rekrutteringsanmodning.
2.  En udvidet kandidatprofil og relaterede arbejdsgange.
3.  En API til integration, der åbner de nye funktioner for integration af applikationer.

Du kan finde flere oplysninger om, hvordan du konfigurerer og bruger funktionerne til rekrutteringsanmodninger og ansøger, i [Rekrutteringsjobansøgere](hr-personnel-recruit.md).

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Denne API er baseret på Microsoft Dataverse (tidligere Common Data Service). Al RESTful interaktion med denne API sker via Microsoft Dataverse Web-API, der bruger OData. Denne API er et undersæt af Dataverse Web-API. Dataverse Web-API definerer egenskaber som f.eks. godkendelse, servicespecifikationer, batch, samtidighedsstyring og håndtering af fejl.

Yderligere generelle oplysninger om Microsoft Dataverse Web-API finder du i:

- [Hvad er Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)
- [Brug Microsoft Dataverse Web-API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse-vejledning for udvikler](https://docs.microsoft.com/powerapps/developer/data-platform)

Dokumentationen ovenfor indeholder detaljer og udviklervejledning vedrørende brug af Dataverse Web-API, som f.eks. [administration af godkendelse](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [udførelse af handlinger](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [brug af Postman med API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api) og [brug af sporing af ændring eller delta-tokens](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) med API.

### <a name="option-sets"></a>Grupperede indstillinger

Datamodellen for ATS integrations-API, som beskrives i dette dokument, omfatter den indstilling, der er angivet til at indeholde nummererede værdier, der er tilknyttet enhedsegenskaber. Yderligere oplysninger om, hvordan du kan arbejde med de indstillinger, der er angivet i Dataverse Web-API, finder du i [Opret og opdater indstillinger, der er angivet ved hjælp af Web-API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets). De indstillinger, der skal definere de enkelte Dataverse-miljøer.

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Virtuelle tabeller i Dataverse Human Resources

Slutpunkterne for ATS integrations-API bruger funktionerne for den virtuelle Microsoft Dataverse-tabelplatform. Som standard anvendes de virtuelle tabeller og de tilknyttede API-slutpunkter ikke i Human Resources-miljøer, hvilket gør det muligt for organisationer at bestemme, hvilke OData-slutpunkter der vises for miljøet. Hvis du vil bruge API'en, skal de virtuelle tabeller for Human Resources-enhederne oprettes for miljøet. 

Oplysninger om generering af virtuelle tabeller til API finder du i [Konfigurere Dataverse-virtuelle tabeller](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).

## <a name="data-model"></a>Datamodel

Datamodellen er fokuseret på to hovedenheder:

- **RecruitingRequest** repræsenterer en anmodning til ATS om at rekruttere til en eller flere ledige stillinger. Du kan finde en eksempelforespørgsel i [Eksempelforespørgsel til rekrutteringsanmodning](hr-admin-integration-ats-api-recruiting-request-example-query.md).
- **CandidateToHire** repræsenterer oplysninger om en kandidat, der har accepteret et tilbud om en stilling. **Person** repræsenterer den person, der er kandidat. En person kan have flere roller i firmaet, f.eks. kandidat, ansat, medarbejder eller kontrahent. Du kan finde en forespørgsel om et eksempel i [Eksempelforespørgsel til kandidat til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).

I følgende diagram vises forholdene i API grafisk. Flere typer har fremmede nøgler til andre allerede eksisterende enheder i Human Resources, som ikke illustreres her. Dette dokument indeholder oplysninger om enheder, der er specifikke for scenarier for rekrutteringsintegration. Men der er mange andre enheder i Dataverse Web-API til Dynamics 365 Human Resources, som også kan være relevante for din integration. Du har f.eks. også brug for detaljer for arbejdere, job, stillinger eller andre enheder, der ikke er defineret her. Mange af disse enheder refereres til i relationer med fremmede nøgler eller navigationsegenskaber.

![ATS-integration, API-datamodel](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a>Rekrutteringsanmodning og relaterede enheder og indstillinger, der er angivet

Eksempelforespørgsel: 

- [Eksempelforespørgsel til anmodning om rekruttering](hr-admin-integration-ats-api-recruiting-request-example-query.md)

Enheder:

- [Rekrutteringsanmodning](hr-admin-integration-ats-api-recruiting-request.md)
- [Stilling til rekrutteringsanmodning](hr-admin-integration-ats-api-recruiting-request-position.md)
- [Rekrutteringsanmodningsfærdighed](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [Rekrutteringsanmodningsuddannelse](hr-admin-integration-ats-api-recruiting-request-education.md)
- [Lokation af rekrutteringsanmodning](hr-admin-integration-ats-api-recruiting-request-location.md)

Indstillingssæt:

- [Status for jobfritagelse](hr-admin-integration-ats-api-job-exempt-status.md)
- [Status for rekrutteringsanmodningsstilling](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [Status for rekrutteringsanmodning](hr-admin-integration-ats-api-recruiting-request-status.md)
- [Kategori af lovpligtigt job](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a>Kandidat til ansættelse og relaterede enheder og de indstillinger, der er angivet

Eksempelforespørgsel:

- [Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

Enheder:

- [Kandidat, der kan ansættes](hr-admin-integration-ats-api-candidate-to-hire.md)
- [Person](hr-admin-integration-ats-api-person.md)
- [Personuddannelse](hr-admin-integration-ats-api-person-education.md)
- [Persons erhvervserfaring](hr-admin-integration-ats-api-person-professional-experience.md)
- [Personadresse](hr-admin-integration-ats-api-person-address.md)
- [Kontakt til part](hr-admin-integration-ats-api-party-contact.md)
- [Personkompetence](hr-admin-integration-ats-api-person-skill.md)
- [Rangeringsniveau](hr-admin-integration-ats-api-rating-level.md)
- [Personcertifikat](hr-admin-integration-ats-api-person-certificate.md)
- [Certifikattype](hr-admin-integration-ats-api-certificate-type.md)
- [Personscreening](hr-admin-integration-ats-api-person-screening.md)
- [Screeningstyper](hr-admin-integration-ats-api-screening-types.md)
- [Personidentifikationsnummer](hr-admin-integration-ats-api-person-identification-number.md)

Indstillingssæt:

- [Resultat af ansøgerintegration](hr-admin-integration-ats-api-applicant-integration-result.md)
- [Tomt ja-nej](hr-admin-integration-ats-api-blank-yes-no.md)
- [Status for færdiggørelse](hr-admin-integration-ats-api-completion-status.md)
- [Kontakttype](hr-admin-integration-ats-api-contact-type.md)
- [Uddannelseskreditgrundlag](hr-admin-integration-ats-api-education-credit-basis.md)
- [Køn](hr-admin-integration-ats-api-gender.md)
- [Ægteskabelig status](hr-admin-integration-ats-api-marital-status.md)
- [Måneder i året](hr-admin-integration-ats-api-months-of-year.md)
- [Nej-Ja](hr-admin-integration-ats-api-no-yes.md)
- [Periodeenhed](hr-admin-integration-ats-api-period-unit.md)
- [Screeningfrekvens](hr-admin-integration-ats-api-screening-frequency.md)
- [Screeningfrekvensen genereres fra](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [Færdighedsniveautype](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a>Se også

[Rekruttere jobkandidater](hr-personnel-recruit.md)<br>
[Hvad er Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[Brug Microsoft Dataverse Web-API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)<br>
[Opret og opdater de indstillinger, der er angivet ved hjælp af Web-API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]