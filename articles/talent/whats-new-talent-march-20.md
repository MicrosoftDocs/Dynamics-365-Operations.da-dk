---
title: Nyheder eller ændringer i Dynamics 365 Talent (20. marts 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-20
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a7a44e1c9d8dcb4b2cc81a682a044d26cdc1149e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460675"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-20-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (20. marts 2019)

[!include [banner](includes/banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

### <a name="setting-the-audience-on-activities"></a>Angivelse af publikum for aktiviteter
Publikummet for aktiviteterne i systemet kan nu defineres. Procesrelaterede aktiviteter (såsom interview, planlægning, tilbagemelding og EEO) kan angives til "Alle kandidater", "Interne kandidater" og "Eksterne kandidater". Brugertilpassede aktiviteter, såsom Microsoft-formularer, YouTube-videoer og webstedsindhold, kan fremsendes til "Alle kandidater", "Interne kandidater", "Eksterne kandidater" eller ansættelsesteamet.  

### <a name="improve-career-site-job-discoverability-search-engine-optimization"></a>Forbedret jobgenkendelse på karrierewebsted: optimering af søgemaskine
Denne funktion gør det muligt for søgemaskinecrawlere at nå ud til og indeksere jobopslag på Attract's karrierewebsted. Dette hjælper kandidaterne med at finde de opslåede jobs på Attract's karrierewebsted ved at anvende populære søgemaskiner.

### <a name="show-login-hint-to-candidates-who-forgot-their-credentials"></a>Vis tips til login til kandidater, der har glemt deres legitimationsoplysninger
Hvis en kandidat har glemt de sociale legitimationsoplysninger, denne har anvendt til at søge et job, mens de åbner et gemt link eller et link, der er blevet fremsendt til kandidaten i en e-mail, vil der nu blive vist et tip med udbyderens navn og brugernavn (tilsløret). Dette hjælper dem med at huske de korrekte legitimationsoplysninger, således at de kan tilgå deres jobansøgning.

### <a name="help-internal-candidates-explore-internal-jobs"></a>Hjælp interne kandidater med at udforske interne jobs
Problemet med, at de eksterne kandidater kunne se navnet på rekrutteringsmedarbejderen eller den ansættelsesansvarlige for et job, er blevet løst. Nu kan alene interne kandidater se medlemmerne af ansættelsesteamet for et job. Det er også nemmere for interne kandidater at se og søge jobs, der alene er slået op internt. Når en kandidat forsøger at tilgå linket for at se eller søge et job, der alene er slået op internt, er de nødsaget til at godkende med Azure Active Directory-legitimationsoplysninger. Interne kandidater har nu ligeledes mulighed for at kontakte medlemmerne af ansættelsesteamet for at udtrykke deres interesse for eller få flere oplysninger om jobbet. Denne mulighed er tilgængelig for alle jobs, der alene er tiltænkt interne kandidater. Du kan finde flere oplysninger i [Konfigurer dit karrierewebsted i Microsoft Dynamics 365 Talent - Attract](./career-site.md).

### <a name="designate-silver-medalists-to-assign-high-value-applicants-for-future-positions"></a>Udpeg modtagere af sølvmedaljer for at tildele ansøgere af høj værdi til fremtidige stillinger
Rekrutteringsmedarbejdere og ansættelsesansvarlige har ofte en liste med ansøgere, som passede godt til stillingen, men som ikke fik et ansættelsestilbud, da stillingen allerede var blevet besat. Disse ansøgere, betegnet som "modtagere af sølvmedaljer", er værdifulde, da de kan bidrage til at reducere den tid, der anvendes på at ansætte en ny medarbejder, næste gang en lignende stilling bliver ledig. Attract gør det nu muligt for rekrutteringsmedarbejdere og ansættelsesansvarlige at udpege modtagere af sølvmedaljer på ansøgningslisten, hvis ansøgeren er rykket videre til tilbudsstadiet. Udpegningen af modtageren af sølvmedaljen vil fremgå af ansøgerlisten for jobbet, men også af oversigten over talentpuljen, når de pågældende ansøgere er medlemmer af en af rekrutteringsmedarbejderens eller den ansættelsesansvarliges puljer. Derudover vil udpegningen fremgå af jobhistorikken som en del af en kandidats talentpuljeprofil. Du kan få forhåndsvist denne funktion ved at få en administrator til at slå den til ved hjælp af [Funktionen "Styring" i Administration](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="add-applicants-to-talent-pools"></a>Tilføj ansøgere til talentpuljer
Det er nu blevet nemmere at tilføje ansøgere til talentpuljer ved hjælp af en ny handling på ansøgerlisten. Ved at vælge ikonet **Tilføj til talentpulje** kan rekrutteringsmedarbejderen eller den ansættelsesansvarlige vælge blandt deres talentpuljelister og nemt tilføje ansøgere til talentpuljer direkte fra et jobs ansøgerliste.

### <a name="configure-whether-a-resume-is-required-to-apply-for-a-particular-job"></a>Konfigurer, hvorvidt der skal stilles krav om et CV for at kunne søge et bestemt job
På grundlag af kunders tilbagemelding kan rekrutteringsmedarbejdere nu konfigurere, hvorvidt et CV, i form af en uploadet fil, er et krav for at søge et bestemt job. Denne konfiguration er en del af ansøgningsaktiviteten, der kan tilgås under ansættelsesprocessen. Når indstillingen er slået til, vil alle potentielle ansøgere blive bedt om at uploade et CV, når de søger denne stilling. Ansøgningen anses ikke for at være fuldført, medmindre der uploades et CV. Dette bidrager til at reducere støjen i ansøgerpuljen ved at sikre, at alle ansøgere fremsender tilstrækkelige oplysninger til, at rekrutteringsmedarbejderen kan opdele dem.

### <a name="candidates-can-apply-to-a-job-using-their-linkedin-profile"></a>Kandidater kan søge et job ved hjælp af deres LinkedIn-profil
De kandidater, der allerede har en opdateret profil på LinkedIn, kan søge jobs med blot ét klik ved at anvende den pågældende profil.

### <a name="track-how-a-candidate-profile-originated-in-the-system-and-where-your-applicants-discover-the-jobs-they-applied-for"></a>Spor, hvordan en kandidats profil er opstået i systemet, og hvor dine ansøgere ser de jobs, de søger.
Du kan nu finde ud af, hvordan en bestemt kandidats profil er opstået i Attract, ved at kigge på profilkilden under kandidatdetaljer på en ansøgnings **Profil**-side eller talentpuljeprofil. Du kan på tilsvarende vis finde ud af, hvordan en ansøger har opdaget jobbet, ved at kigge på ansøgningskilden, der fremgår af **Ansøgningsaktivitet** i feedet for ansøgningsaktiviteten. Disse oplysninger er også tilgængelige i talentpuljeprofilens jobhistorik. Når rekrutteringsmedarbejdere eller ansættelsesansvarlige tilføjer kandidater manuelt, vil de ligeledes blive bedt om at angive kilden til ansøgningen eller kandidatprofilen. Når en kandidat søger for første gang, vil deres profilkilde være den samme som den oprindelige kilde til deres ansøgning. Du kan få forhåndsvist denne funktion ved at få en administrator til at slå den til ved hjælp af [Funktionen "Styring" i Administration](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature). Bemærk, at eksisterende kandidater og ansøgere ikke har kildeoplysninger. Rekrutteringsmedarbejdere kan dog tilføje disse oplysninger manuelt.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2195

### <a name="attract-integration-throws-duplicate-record-error-for-applications"></a>Attract-integration resulterer i fejl for ansøgninger pga. dubletposter
I denne opdatering er der blevet løst et problem med dubletposter. Problemet opstår, når man åbner arbejdsområdet **Personalestyring**.

### <a name="unable-to-close-form-when-editing-name-sequence"></a>Ikke muligt at lukke formular i forbindelse med redigering af navnesekvens
Der er foretaget ændringer for at løse et problem, som opstår i forbindelse med redigeringen af navnesekvensen på arbejderformularen.

## <a name="coming-soon"></a>Kommer snart

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Avanceret lønsikkerhed (fast og variabel)
I mange organisationer har de ansvarlige for kompensationer og frynsegoder muligvis kun har adgang til visse kompensationsposter. Disse kan være til ledere eller medarbejdere i bestemte områder. Med denne ændring kan Personale administrere og vedligeholde kompensationsplaner for forskellige medarbejdergrupper i organisationen. Du kan tildele sikkerhedsroller til faste og variable planer, som bestemmer adgangen til planerne og medarbejderdata tilknyttet til planerne, såsom løn eller bonusposter. Alene roller med den godkendte adgang kan behandle kompensation for de pågældende medarbejdere.

###  <a name="email-support-for-alerts"></a>E-mailunderstøttelse til påmindelser
Med Platform update 24 til Finance and Operations kan brugerne oprette påmindelsesregler, som automatisk fremsender mailbeskeder til kontaktpersoner, når de udløses af en hændelse.

### <a name="duplicate-employee-check-interface-changes"></a>Duplikerede medarbejderkontroller: ændringer i grænsefladen
Med denne ændring opdages dubletter i forbindelse med din indtastning i navnefelter, og der vises en status over antallet af fundne dubletter. Du kan vælge, at det angivne link skal åbne en ny side for at vurdere, om du ønsker at anvende det fundne match. For at undgå at forstyrre indtastningen af data åbner dubletformularen ikke automatisk.




[!INCLUDE[footer-include](../includes/footer-banner.md)]