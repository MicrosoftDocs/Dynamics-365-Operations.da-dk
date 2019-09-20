---
title: Sikkerheds- og rollestyring i Attract
description: Dette emne indeholder oplysninger om rollesikkerhed i Microsoft Dynamics 365 for Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 03/08/2019
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
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 3f804b5f79b813cf504c3deb4a95e678c6fcbf87
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739834"
---
# <a name="set-user-permissions"></a>Angive brugerrettigheder

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent: Attract-brugerrollebaseret sikkerhed. Der gives med andre ord ikke adgang til individuelle brugere, men til de sikkerhedsroller, brugerne er tildelt til. En bruger, der er tildelt en sikkerhedsrolle, har adgang til det sæt rettigheder, der er knyttet til den pågældende rolle.

Attract indeholder fem grundlæggende brugerroller:

- Administrator
- Ansvarlig for ansættelse
- Rekrutteringsmedarbejder
- Interviewer
- Skrivebeskyttet

Rollen Administrator er den eneste rolle, der har rettighed til at tilføje andre brugere og ændre deres rettigheder.

- **Tilføj** – I Administration skal du under fanen **Brugerrettigheder** vælge **Tildel roller**, søge efter den bruger, du vil tilføje og derefter tildele rettigheder til den pågældende bruger.
- **Rediger** – Søg efter brugeren, eller find brugeren på listen, og vælg derefter **Rediger** for at ændre brugerens rettigheder.
- **Slet** – Hvis du sletter en brugers rettigheder, kan du ikke fjerner brugeren fra systemet. Men du begrænser brugerens adgang og rettigheder i Attract. F.eks. er Hilda blevet tildelt rollen som Ansvarlig for ansættelse, og hun føjes til et job som ansættelsesansvarlig. Hvis Hilda senere fjernes fra rollen Ansvarlig for ansættelse, forbliver hun ansættelsesansvarlig for jobbet og har stadig adgang til jobbet. Men hun kan ikke oprette andre job.

De følgende afsnit indeholder en kort beskrivelse af hver rolle. Tabellerne senere i emnet indeholder mere detaljerede oplysninger.

> [!NOTE]
> Nogle funktioner er kun tilgængelige med tilføjelsesprogrammet til omfattende ansættelse i Attract.

## <a name="administrator"></a>Administrator

Brugere, der er tildelt til rollen Administrator kan få adgang til og ændre alle data i Attract. Administratorer kan oprette, læse, opdatere og slette data. De har også adgang til administrationssiden, hvor de kan konfigurere programmet Attract og angive brugeroplysninger. Det anbefales, at mindst én person tildeles rollen Administrator. Miljøadministratoren i Microsoft PowerApps angives som standard som administrator i Attract. Hvis du har tilmeldt dig prøveversionen af Attract, tildeles rollen Administrator automatisk til dig. I øjeblikket, for at oprette job skal brugere, der har rollen Administrator også have enten rollen som rekrutteringsmedarbejder eller ansættelsesansvarlig.

## <a name="hiring-manager"></a>Ansvarlig for ansættelse

Brugere, der er tildelt rollen Ansvarlig for ansættelse kan oprette job og opdater job, de tidligere har oprettet. Ansættelsesansvarlige kan kun udføre et begrænset antal handlinger på et job og de ansøgninger, der er tilknyttet jobbet. Kun brugere, der er tildelt rollen som ansættelsesansvarlig kan føjes til et ansættelsesteam som ansættelsesansvarlige.

## <a name="recruiter-role"></a>Rollen Rekrutteringsmedarbejder

Brugere, der er tildelt rollen som rekrutteringsmedarbejder har fuld læse-, oprettelses-, opdaterings- og sletterettigheder til de job, de selv har oprettet. De også har fuld oprettelses-, læse-, opdaterings- og sletterettigheder til de ansøgninger, der er tilknyttet job, de ejer. Kun brugere, der er tildelt rollen som rekrutteringsmedarbejder kan føjes til et ansættelsesteam som rekrutteringsmedarbejdere.

## <a name="interviewer"></a>Interviewer

Alle brugere, der har en Microsoft Azure Active Directory (Azure AD) konto i organisationen, kan føjes til et ansættelsesteam som interviewer. Brugere, der er tildelt rollen Interviewer kan få vist joboplysninger og ansøgerdata for job, som de er i ansættelsesteamet for. For disse job kan interviewere også give ansættelsesanbefalinger og tilbagemeldinger om kandidater. De kan dog ikke opdatere oplysninger om job eller ansøgerdata.

## <a name="read-only"></a>Skrivebeskyttet

Brugere, der er tildelt rollen Skrivebeskyttet have skrivebeskyttet adgang til alle data i Attract-miljøet. De kan dog ikke oprette eller redigere data.

## <a name="find-out-which-roles-you-have"></a>Find ud af, hvilke roller du har

1.  I Attract skal du klikke på spørgsmålstegnet (**?**) i øverste højre hjørne af siden.

2.  Klik på **Om**.

    Det vil fremgå af det vindue, der vises, hvilke roller du har i Attract:

    ![Se din licenstype til Attract](media/attract-license-types.png)
    
## <a name="delegated-roles"></a>Delegerede roller

For hvert job, de er i ansættelsesteamet for, kan rekrutteringsmedarbejdere og ansættelsesansvarlige udpege en eller flere delegerede for sig selv. De kan dog ikke udpege delegerede for andre personer i ansættelsesteamet.

Delegerede har de samme rettigheder som den person, der udpegede dem. Eksempelvis hvis den ansættelsesansvarlige udpeger en delegeret til sig selv for et job, har den delegerede de samme rettigheder som den ansættelsesansvarlige for det pågældende job. Delegerede kan ikke fjerne andre delegerede fra ansættelsesteamet. De kan heller ikke fjerne de personer, der er udpegede dem som delegerede.

## <a name="job-details-and-actions"></a>Joboplysninger og -handlinger

Brugere med rollen rekrutteringsmedarbejder eller ansættelsesansvarlig kan oprette job. Følgende rettigheder gælder for de joboplysninger og -handlinger, der kan udføres på job.

| Data eller handling    | Rekrutteringsmedarbejder | Ansvarlig for ansættelse | Interviewer |
|-------------------|-----------|----------------|-------------|
| Jobdetaljer       | Oprette, læse, opdatere og slette for job, som brugeren er i ansættelsesteamet for | Oprette, læse, opdatere og slette for job, som brugeren er i ansættelsesteamet for | Skrivebeskyttet |
| Ansættelsesteam       | Oprette, læse, opdatere og slette for job, som brugeren er i ansættelsesteamet for | Oprette, læse, opdatere og slette for job, som brugeren er i ansættelsesteamet for | Skrivebeskyttet |
| Jobopslag       | Oprette, læse, opdatere og slette for job, som brugeren er i ansættelsesteamet for | Skrivebeskyttet | Skrivebeskyttet |
| Proces           | Oprette, læse, opdatere og slette for job, som brugeren er i ansættelsesteamet for | Oprette, læse, opdatere og slette for job, som brugeren er i ansættelsesteamet for | Skrivebeskyttet |
| Tilføje ansøgere    | Tilføje ansøgere til job, som brugeren er i ansættelsesteamet for | Tilføje ansøgere til job, som brugeren er i ansættelsesteamet for | Ikke tilladt |
| Tilføje jobkandidater     | Tilføje jobkandidater, som brugeren er i ansættelsesteamet for | En konfigurationsindstilling i [opsætning af aktivitet for jobkandidat](./activities-attract.md#prospect-activity) styrer, om interviewere kan tilføje og få vist jobkandidater. | Ikke tilladt |
| Aktivere job      | Aktivere job, som brugeren er i ansættelsesteamet for | Aktivere job, som brugeren er i ansættelsesteamet for | Ikke tilladt |
| Luk job         | Lukke job, som brugeren er i ansættelsesteamet for | Ikke tilladt | Ikke tilladt |
| Slet job        | Slette job, som brugeren er i ansættelsesteamet for | Kun hvis der ikke er føjet nogen ansøgere til jobbet | Ikke tilladt |
| Slet ansøgere | Slette ansøgere, hvis brugeren er i ansættelsesteamet | Ikke tilladt | Ikke tilladt |

## <a name="application-details-and-actions"></a>Ansøgningsoplysninger og -handlinger

Følgende rettigheder gælder for de jobspecifikke data for ansøgninger og de handlinger, der kan udføres på ansøgninger.

| Data eller handling          | Rekrutteringsmedarbejder | Ansvarlig for ansættelse | Interviewer |
|-------------------------|-----------|----------------|-------------|
| Ansøgningsdokumenter   | Oprette, læse, opdatere og slette for job, som brugeren er i ansættelsesteamet for | Oprette, læse, opdatere og slette for job, som brugeren er i ansættelsesteamet for | Skrivebeskyttet |
| Bemærkninger til ansøgninger       | Oprette, læse, opdatere og slette for job, som brugeren er i ansættelsesteamet for | Oprette, læse, opdatere og slette for job, som brugeren er i ansættelsesteamet for | Skrivebeskyttet|
| Ansøgningsaktivitet    | Se, hvis brugeren er i ansættelsesteamet | Se, hvis brugeren er i ansættelsesteamet | Skrivebeskyttet |
| Tilbagemelding på ansøgning    | Tilføje og få vist al feedback, hvis brugeren er i ansættelsesteamet | Tilføje og få vist al feedback, hvis brugeren er i ansættelsesteamet | Kan tilføje tilbagemeldinger\*\* |
| Afvise ansøgning      | Kan afvise, hvis brugeren er i ansættelsesteamet | Ikke tilladt | Ikke tilladt |
| Flyt til næste trin           | Kan afvise, hvis brugeren er i ansættelsesteamet | Kan rykke frem, hvis brugeren er i ansættelsesteamet | Ikke tilladt |
| Starte tilbudsstyring | Kan starte tilbudsstyring | Der er en konfigurationsindstilling for tilbudsaktiviteten. | Ikke tilladt |


\*\* En konfigurationsindstilling i [opsætningen af tilbagemeldingsaktiviteten](./activities-attract.md) styrer, om interviewere kan se hinandens tilbagemeldinger.


## <a name="process-templates"></a>Processkabeloner

Følgende rettigheder gælder for ansættelsesprocesskabeloner. Muligheden for teammedlemmer for at oprette og redigere skabeloner konfigureres i **Skabelonstyring** i Administration. Hvis skabelonstyring er aktiveret, kan rekrutteringsmedarbejdere og ansættelsesansvarlige oprette og redigere deres egne processkabeloner. Hvis skabelonstyring er deaktiveret, er det kun administratorer, der kan oprette og redigere skabeloner. I tabellen nedenfor antages det, at skabelonstyring er aktiveret.

| Data              | Rekrutteringsmedarbejder                                           | Ansvarlig for ansættelse                                      | Interviewer |
|-------------------|-----------------------------------------------------|-----------------------------------------------------|-------------|
| Processkabeloner | Fulde rettigheder til skabeloner, som oprettes af brugeren | Fulde rettigheder til skabeloner, som oprettes af brugeren | Ingen adgang   |

## <a name="email-and-email-templates"></a>Mail og mailskabeloner

Følgende rettigheder gælder for de mailskabeloner og -handlinger, der kan udføres på mails. Kun administratorer kan oprette og redigere mailskabeloner.

| Data eller handling     | Rekrutteringsmedarbejder          | Ansvarlig for ansættelse     | Interviewer |
|--------------------|--------------------|--------------------|-------------|
| Mailskabeloner    | Skrivebeskyttet adgang   | Skrivebeskyttet adgang   | Ingen adgang   |
| Send mail         | Sende pr. aktivitet  | Sende pr. aktivitet  | Ingen adgang   |
| Redigere mailindhold | Redigere mailindhold | Redigere mailindhold | Ingen adgang   |

## <a name="talent-pools"></a>Talentpuljer

Følgende rettigheder gælder for talentpuljer. Talentpuljer er kun synlige for den person, der oprettede dem, medmindre vedkommende vælger at dele dem. Kandidatsøgning kan bruges til at søge efter kandidater, der ikke er føjet til en navngivet pulje.

| Data eller handling   | Rekrutteringsmedarbejder                                       | Ansvarlig for ansættelse                                  | Interviewer |
|------------------|-------------------------------------------------|-------------------------------------------------|-------------|
| Navngivet pulje       | Fulde rettigheder til puljer, som oprettes af brugeren | Fulde rettigheder til puljer, som oprettes af brugeren | Ingen adgang   |
| Dele pulje       | Kun de puljer, som brugeren opretter                | Kun de puljer, som brugeren opretter                | Ingen adgang   |
| Kandidatsøgning | Alle søgefunktioner                        | Alle søgefunktioner                        | Ingen adgang   |

## <a name="candidates"></a>Kandidater

Kandidater er personer, der er føjet til en talentpulje, men som ikke er tilknyttet et job.

| Data                        | Rekrutteringsmedarbejder                        | Ansvarlig for ansættelse                   | Interviewer |
|-----------------------------|----------------------------------|----------------------------------|-------------|
| Profil – detaljer om kandidat | Oprette, læse, opdatere og slette | Oprette, læse, opdatere og slette | Ingen adgang   |
| Dokumenter                   | Oprette, læse, opdatere og slette | Oprette, læse, opdatere og slette | Ingen adgang   |
