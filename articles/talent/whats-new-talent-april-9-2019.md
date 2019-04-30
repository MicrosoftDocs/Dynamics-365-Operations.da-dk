---
title: Nyheder eller ændringer i Dynamics 365 for Talent (9. april 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 25ef0d49c2600833aefa84d404e00c0c57cfbf52
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/12/2019
ms.locfileid: "989954"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-april-9-2019"></a>Nyheder eller ændringer i Dynamics 365 for Talent (9. april 2019)

[!include [banner](includes/banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Integration af Lifecycle Services (LCS) med "rapporter et problem"
I Attract og Onboard vil problemer, der bliver rapporteret af slutbrugere ved hjælp af funktionen "rapporter et problem", nu automatisk oprette supportproblemer i kundens LCS-projekt. Administratorer kan derefter tildele problemerne og om fornødent indsende dem til Microsoft. Dette er i overensstemmelse med Core HR's håndtering af slutbrugernes supportproblemer.

### <a name="relevance-search"></a>Relevanssøgning
I talentpuljer kan du nu søge i hele din kandidatdatabase efter særlige færdigheder, navne eller uddannelsesmæssige baggrunde. Du behøver ikke længere at angive, hvilken sektion af en kandidats profil du ønsker at søge i. Attract søger i hele profilen og fremhæver alle de fundne resultater. Attract søger ligeledes i alle de dokumenter, der er tilgængelige for en kandidat, og rangerer søgeresultaterne på en intelligent måde. Derudover kan du filtrere resultaterne efter kilde, eller efter om de er modtagere af sølvmedaljer. Du kan finde yderligere oplysninger under [Søg efter og se kandidatprofiler](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-talent-pools#search-and-view-candidate-profiles).

### <a name="prospect-recommendations"></a>Kandidatemneanbefalinger
Attract kan hjælpe dig med at sætte gang i kildeindsamling til et job, så snart du har aktiveret jobbet, ved at fremsætte intelligente kandidatanbefalinger fra din organisations kandidatdatabase. Anbefalingerne omfatter de færdigheder og uddannelsesoplysninger, der blev identificeret under søgningen efter relevante kandidatemner. Disse anbefalinger fremgår af fanen **Kandidatemner** under et job, hvis du slår det til i forbindelse med det pågældende jobs ansættelsesproces. Du kan finde flere oplysninger under [Kandidatemneanbefalinger](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/intelligent-recommendations#prospect-recommendations).

### <a name="interviewer-availability-statuses"></a>Interviewerens tilgængelighedsstatus
Samtaleplanlæggere kan snart se statusserne **Ude af kontoret, arbejder andetsteds** for interviewere med henblik på at hjælpe dem med at planlægge tidspunkter, der potentielt passer interviewerne bedre.

### <a name="candidate-interview-experience-save-calendar-invites"></a>Kandidaters samtaleoplevelse: gem kalenderinvitationer
Kandidater kan nu downloade og gemme deres samtalehændelser i deres personlige kalendere ved hjælp af den .ics-fil, der er vedhæftet e-mailen med samtaleoversigten, som fremsendes til kandidaten.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Integration af Lifecycle Services (LCS) med rapportering af problemer
I Attract og Onboard vil problemer, der bliver rapporteret af slutbrugere ved hjælp af funktionen "rapporter et problem", nu automatisk oprette supportproblemer i kundens LCS-projekt. Administratorer kan derefter tildele problemerne og om fornødent indsende dem til Microsoft. Dette er i overensstemmelse med Core HR's håndtering af slutbrugernes supportproblemer.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR
Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2225.

### <a name="percent-of-basis-variable-plans-load-incorrect-amount"></a>Procentandelen af de variable basisplaner, der indlæser det forkerte beløb
Denne uges frigivelse korrigerer et problem med indlæsningen af variable kompensationer, der tildeles på grundlag af en procentandel af basisplanerne.
 
### <a name="date-picker-on-last-day-worked-doesnt-work-correctly"></a>Datavælger på "Sidste arbejdsdag" virker ikke korrekt
Denne ændring korrigerer problemet: når en brugere redigerer **Ansættelsesforholdets slutdato** og vælger dato ved hjælp af kalenderkontrol, tilføjes der en ekstra dag til valget.

###  <a name="limit-personnel-action-types-by-the-action-taken"></a>Begræns personalehandlingstyper ved hjælp af den udførte handling
Denne ændring begrænser de viste handlingstyper i forbindelse med udførelsen af bestemte handlinger. F.eks. vil alene de nye stillingshandlinger fremgå af listen over valgbare handlinger, når der anmodes om en ny stilling. Tidligere fremgik både nye og redigerede handlinger. 

### <a name="transferring-an-employee-with-compensation-in-a-second-legal-entity"></a>Overførelse af en medarbejder med kompensation i en anden juridisk enhed
Denne udgivelse giver mulighed for at afslutte en kompensation i en anden juridisk enhed, såfremt overførelsen sker på tværs af virksomheder.

### <a name="unable-to-select-compensation-for-a-future-employment-during-a-transfer"></a>Ikke muligt at vælge kompensation for en kommende medarbejder under en overførelse
Du kan nu angive kompensationen for den nye juridiske enhed under overførelsesprocessen, når du overfører en medarbejder til en ny juridisk enhed.

### <a name="user-isnt-able-to-assign-compensation-during-position-assignment"></a>Brugeren er ikke i stand til at tildele kompensation i forbindelse med tildeling af stillingen
Tilføjelse af en ny stillingstildeling giver nu mulighed for at konfigurere poster vedrørende fast løn. 

## <a name="in-preview"></a>Som eksempel

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Tilladelse til angivelse af årsagskoder for orlovstyper
Organisationer har muligvis behov for yderligere oplysninger om fritidsanmodninger. Du kan nu angive årsagskoder for orlovstyper og give medarbejderne mulighed for at vælge en årsagskode på deres fritidsanmodninger.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Krav om årsagskoder for visse orlovstyper på fritidsanmodninger
Organisationer kræver muligvis årsagskoder for specifikke orlovstyper, når medarbejderne anmoder om fri. Dette kan skyldes firmapolitik eller lovkrav. Du kan nu angive, hvilke orlovstyper der kræver en årsagskode, og du kan kræve, at medarbejderne oplyser en årsagskode på deres fritidsanmodninger for den pågældende orlovstype.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Udarbejdelse af en transaktionsliste over orlov og fravær til Personale
Sporing af medarbejdernes fridage og forståelse af, hvordan fridagene beregnes, hjælper ikke blot Personale med at besvare medarbejdernes spørgsmål, men sikrer endvidere, at medarbejderne tildeles den korrekte mængde fridage. Personale har nu fået et nyt indblik i transaktionerne (tilskud, periodiseringer, reguleringer og anmodninger) og kan derved se de bagvedliggende årsager til saldiene. 

## <a name="coming-soon"></a>Kommer snart

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Forbedringer i brugergrænsefladen for duplikeret medarbejderkontrol
Med denne ændring opdages dubletter i forbindelse med din indtastning i navnefelter, og der vises en status over antallet af fundne dubletter. Du kan vælge, at det angivne link skal åbne en ny side for at vurdere, om du ønsker at anvende det fundne match. Dubletformularen åbner ikke automatisk for at undgå forstyrrelser i forbindelse med indtastning af data.

###  <a name="email-support-for-alerts"></a>E-mailunderstøttelse til påmindelser
Med platformsopdatering 25 kan brugerne oprette påmindelsesregler, som automatisk fremsender e-mailbeskeder til kontaktpersoner, når de udløses af en hændelse. 
