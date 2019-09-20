---
title: Rekruttere kandidater med LinkedIn Recruiter i Microsoft Dynamics 365 for Talent - Attract
description: Brug LinkedIn-integrationen leveret af Microsoft Dynamics 365 for Talent - Attract til at rekruttere jobkandidater gennem LinkedIn Recruiter.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 14aba16fa81a8f25d0f88247319254407d428b2a
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739443"
---
# <a name="source-candidates-with-linkedin-recruiter"></a>Rekruttere kandidater med LinkedIn Recruiter
[!include[banner](../includes/banner.md)]

LinkedIn er verdens største professionelle onlinenetværk, der giver dig adgang til verdens største talenter. Microsoft Dynamics 365 for Talent: Attract giver dig mulighed for at rekruttere kandidater direkte fra LinkedIn. Derfor er det lettere end nogensinde at finde det talent, du har brug for til at besætte dine ledige stillinger. Når du har oprettet din forbindelse til LinkedIn gennem Attract, kan du se potentielle LinkedIn-kandidater til dine stillinger og eksportere dem til Attract med et enkelt klik.

Hvis du ikke ser ud til at have denne funktion, skal du kontakte din administrator. Før du kan drage fordel af LinkedIn Recruiter fra Attract, skal din administrator [konfigurere integration med LinkedIn](./attract-admin-linkedin.md). Du kan derefter konfigurere din forbindelse til LinkedIn Recruiter og begynde at finde kandidater.

## <a name="set-up-your-connection-with-linkedin-recruiter"></a>Konfigurere din forbindelse til LinkedIn Recruiter

Før du kan begynde at arbejde med LinkedIn Recruiter gennem Attract, skal du konfigurere din forbindelse til LinkedIn Recruiter. Til dette trin har du brug for dine LinkedIn Recruiter-legitimationsoplysninger.

1. Vælg knappen **Indstillinger** (tandhjulsikonet) i øverste højre hjørne af siden.
2. Vælg **Brugerindstillinger**.
3. Vælg **Tilslut** under fanen **Forbindelser** ved siden af **LinkedIn**. Følg instruktionerne fra LinkedIn.

    ![[Konfigurere forbindelse til LinkedIn Recruiter fra Attract](./media/attract-set-up-linkedin-recruiter-connection.png)](./media/attract-set-up-linkedin-recruiter-connection.png)

## <a name="view-linkedin-candidates-in-attract"></a>Se LinkedIn-kandidater i Attract

Når du er tilsluttet LinkedIn Recruiter, kan du se kandidaternes LinkedIn-profiler i Attract.

1. I Attract skal du vælge **Job** eller **Talentpuljer** til venstre og derefter vælge en ansøger.

    ![[Se LinkedIn-kandidater i Attract](./media/attract-view-linkedin-candidates.png)](./media/attract-view-linkedin-candidates.png)

2. I kandidatens profil skal du vælge **LinkedIn**-fanen. Du kan se kandidatens profil sammen med InMail-historik og LinkedIn-notehistorik.

Herfra kan du gemme kandidaten i et LinkedIn Recruiter-projekt, sende inMail eller bruge Opdater mig til at indstille en påmindelse i LinkedIn Recruiter.

> [!NOTE]
> En kandidats LinkedIn-profil vises i Attract, når kandidatens Attract-information matcher LinkedIn-oplysningerne. Her er de matchningsregler, der bruges:
> 
> 1. Hvis mailadressen og LinkedIn-medlems-ID matcher i Attract og LinkedIn, vises kandidatens profil. Kandidater har stadig muligheden for at tilknytte eller frakoble deres LinkedIn-profil fra Attract.
> 2. Hvis mailadressen eller LinkedIn-medlems-ID ikke stemmer overens, ser du en liste over mulige kandidater. Du kan derefter vælge en kandidat på listen og tilknytte profilen.
> 3. Hvis der ikke er nogen gode matcher, får du besked om, at der ikke blev fundet noget match.

## <a name="export-linkedin-candidates-to-attract-with-one-click"></a>Eksportere LinkedIn-kandidater til Attract med et enkelt klik

Mens du gennemgår kandidater i LinkedIn Recruiter, kan du eksportere dem til job, som du i øjeblikket har åbne i Attract. I dette trin har du brug for tilladelser som Rekrutteringsmedarbejder eller Ansvarlig for ansættelse i Attract. Du kan finde flere oplysninger om roller i Attract under [Sikkerheds- og rollestyring i Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract).

Du skal også sørge for, at jobbet har stadiet Jobkandidat. Du kan finde flere oplysninger under [Aktiviteten Jobkandidat](./activities-attract.md#prospect-activity).

1. I Attract skal du oprette et job, tildele de relevante roller og aktivere jobbet.
2. I LinkedIn Recruiter skal du finde en egnet kandidat til jobbet og gå til kandidatens profil.
3. Ved hjælp af søgefeltet i kontaktkortet skal du finde jobbet ved hjælp af titlen eller det job-id, der er aktiveret i Attract. Hvis du ikke finder jobbet, skal du vælge **Change ATS** (Skift ATS) for at finde den korrekte forekomst af Attract.
4. Vælg jobbet, og vælg derefter **Eksportér**.
5. Åbn jobbet i Attract. Den eksporterede kandidat vises under fanen **Jobkandidat** til jobbet.

## <a name="view-attract-information-in-linkedin-recruiter"></a>Vise Attract-oplysninger i LinkedIn Recruiter

I LinkedIn Recruiter kan du følge med i, om en kandidat har søgt andre job i organisationen, se, hvor kandidaten befinder sig i jobansøgningernes forskellige faser, og se feedback og kommentarer fra Attract.

1. Åbn LinkedIn Recruiter, og vælg en kandidatprofil.
2. Hold musen over **I ATS**.
3. Vælg en af følgende indstillinger for at se de kandidatoplysninger, der er gemt i Attract:

    - **Job og statusser** - Se job, som kandidaten er en del af, den seneste status, og hvordan kandidaten skrider frem for hvert job.
    - **Interview Feedback** – Se feedback, som interviewerne har sendt i Attract.
    - **Noter** – Se eventuelle noter, der er indtastet for denne kandidat i Attract.

    ![[Se Attract-oplysninger fra LinkedIn Recruiter](./media/attract-view-information-from-linkedin-recruiter.png)](./media/attract-view-information-from-linkedin-recruiter.png)

> [!NOTE]
> Kandidat- og ansøgningsdata synkroniseres ikke med LinkedIn Recruiter, hvis kandidaten ikke har passeret stadiet Jobkandidat.

## <a name="view-linkedin-talent-pools"></a>Se LinkedIn-talentpuljer

Hvis kandidater vil dele deres LinkedIn-profiler med enhver bruger i din organisation, oprettes en ny kandidatpost i Attract. Disse kandidater vises derefter i en systemoprettet LinkedIn-talentpulje.

1. I Attract skal du vælge **Talentpuljer** til venstre.
2. Vælg LinkedIn-talentpuljen. Du vil se en liste over kandidater og deres stubprofiler fra LinkedIn. Stubprofiler indeholder kandidatens for- og efternav og mailadresse, hvis kandidaten valgte at dele den.

## <a name="see-also"></a>Se også

[Ofte stillede spørgsmål om FAQ](./attract-linkedin-faq.md)

[Konfigurer integration med LinkedIn](./attract-admin-linkedin.md)

[Oprette job](./creating-jobs-attract.md)

[Slå job op på LinkedIn fra Attract](./attract-post-jobs-to-linkedin.md)

[Fejlfinding af integration med LinkedIn](./attract-troubleshoot-linkedin.md)
