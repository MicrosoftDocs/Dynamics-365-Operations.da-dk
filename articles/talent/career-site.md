---
title: Karrierewebsted i Attract
description: "Denne artikel indeholder en oversigt over funktioner for kandidater på karrierewebstedet i Microsoft Dynamics 365 for Talent - Attract. I artiklen beskrives også, hvordan du konfigurerer denne funktion."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: da-dk
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a>Karrierewebsted i Attract

[!include [banner](includes/banner.md)]

Denne artikel indeholder en oversigt over funktioner for kandidater på karrierewebstedet i Microsoft Dynamics 365 for Talent: Attract. I artiklen beskrives også, hvordan du konfigurerer denne funktion.

## <a name="overview"></a>Overblik

Attract indeholder ét karrierewebsted for de enkelte miljøer i en lejer. F.eks. hvis en organisation har et miljø til udvikling og et testmiljø, klargøres ét karrierewebsted til udviklingsmiljøet og et andet til testmiljøet. Hver karrierewebsted er **fuldstændigt isoleret** og har sit eget system til godkendelse. Job- og kandidatprofiler deles ikke mellem karrierewebstederne.

Som standard er karrierewebstedet offentlig. Derfor kan kandidater få vist alle job, der er markeret som eksterne, uden at skulle logge på. Alle andre handlinger kræver dog, at kandidaterne er logget på.

## <a name="career-site-management"></a>Administration af karrierewebsted

Følgende elementer på karrierewebstedet styres af indstillingerne:

- **Organisationsnavn:** Organisationens navn vises på navigationslinjen øverst i karrierewebstedet. Hvis kandidaterne vælger organisationsnavnet, kommer de til en side over alle ledige job.
- **Organisationslogo:** Et billede af organisationens logo vises øverst til venstre på karrierewebstedet. Hvis kandidaterne vælger logobilledet, kommer de til en side over alle ledige job.

For at angive værdierne for organisationsnavn og -logo skal brugeren logge på Attract som administrator, vælge **Administration** i menuen **Indstillinger** (tandhjulsymbolet) og derefter vælge fanen **Firmaoplysninger**.

> [!NOTE]
> Logobilledet, der vises på karrierewebstedet, har en fast højde på 20 pixel (px). Det billede, du føjer til administration, skaleres, så det passer i størrelsen. Afhængigt af billedet kan bredden evt. blive ændret.

## <a name="career-site-url"></a>URL-adresse til karrierewebsted

Når du [slå et eksternt job op](./Creating-jobs-Attract.md#postings) for første gang, kan du kopiere linket **Ansøg** fra programmet Attract. URL-adressen til dette link har følgende format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`

URL-adressen på karrierewebstedet er en understreng af **Ansøg** URL-adressen. Den består af alt op til og med firmanavnet. Derfor, for den foregående **Ansøg** URL-adresse, er karrierewebstedets URL-adresse `https://jobs.talent.dynamics.com/jobs/<company_name>/`.

## <a name="authentication-options"></a>Godkendelsesindstillinger

Kandidaterne har følgende logonmuligheder på et Attract-karrierewebsted:

- Personlig konto:

    - LinkedIn
    - Microsoft
    - Google
    - Facebook

- Arbejds- eller skolekonto:

    - Microsoft Azure Active Directory (Azure AD)

Azure AD-logon er kun beregnet til interne kandidater. Derfor fungerer det kun for interne kandidater, der bruger deres firmas Azure AD-legitimationsoplysninger. F.eks. ønsker en kandidat, der aktuelt er medarbejder hos Contoso, Ltd, at ansøge om et job i en ikke-relateret virksomhed, Alpine Ski House. I dette tilfælde kan medarbejderen ikke logge på, hvis han eller hun forsøger at bruge sine Azure AD-legitimationsoplysninger fra Contoso Ltd.

## <a name="create-and-maintain-a-profile"></a>Oprette og vedligeholde en profil

Når kandidater har logget på karrierewebstedet, kan de vælge **Min profil** på navigationslinjen øverst på siden for at oprette og vedligeholde deres profil. Profilen indeholder personlige oplysninger, oplysninger om arbejdserfaring og uddannelse, dokumenter, links og oplysninger om færdigheder. Når en profil er oprettet, kan den bruges til at ansøge om job, som kandidaten er interesseret i. Profiler hjælper også Attract med at anbefale de rigtige job til kandidater.

## <a name="find-the-right-job"></a>Finde det rette job

På joblistesiden kan kandidaterne søge efter et bestemt job ved at indtaste søgeord. Søgefunktionen leder efter søgeord i stillingsbetegnelser og jobbeskrivelser og viser de relevante job som resultat. Kandidaterne kan filtrere resultaterne når som helst baseret på jobstedet eller jobfunktionen.

Kandidaterne kan også se en række anbefalede job på karrierewebstedet. Hvilke job der anbefales til en kandidat, afhænger af kandidatens tidligere ansøgninger, profil og CV'er.

> [!NOTE]
> Jobanbefalinger vises kun, hvis der er opslået mindst 10 job på karrierewebstedet, og hvis kandidaten har fuldført sin profil.

## <a name="apply-for-jobs"></a>Ansøge om job

Når kandidaterne har fundet det rigtige job, kan de ansøge ved hjælp af knappen **Ansøg** på siden med jobdetaljer. På dette tidspunkt kan ansøgerne enten oprette en helt ny profil eller gennemse oplysningerne i deres eksisterende profil. De kan også overføre et CV efter behov og derefter sende jobansøgningen.

## <a name="check-application-status"></a>Kontrollere ansøgningsstatus

Når kandidaterne har ansøgt om et eller flere job, kan de vælge **Ansøgninger** på navigationslinjen øverst på siden for at få vist deres åbne og lukkede ansøgninger. Når kandidaterne åbner en af deres ansøgninger, kan de se det aktuelle stadie og evt. ventende handlinger, som de skal udføre. Hvis en kandidat f.eks. skal angive potentielle datoer for en personlig samtale, viser siden vedkommendes indstillinger.

## <a name="internal-jobs"></a>Interne job

Job, der er markeret som interne og opslået på Attract-karrierewebstedet, vises i øjeblikket ikke på karrierewebstedet. De er kun tilgængelige via en direkte **Ansøg** URL-adresse, der kan kopieres fra programmet Attract.

