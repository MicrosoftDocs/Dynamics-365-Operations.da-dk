---
title: Rekruttere jobkandidater
description: Dette emne viser, hvordan du rekrutterer kandidater i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 77d37cba84fcd6fb8f93da79b10db2db91d91db0
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066594"
---
# <a name="recruit-job-candidates"></a>Rekruttere jobkandidater


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources hjælper dig med at administrere rekrutteringsanmodninger. Det hjælper dig også med en problemfri overgang fra kandidat til medarbejder. Hvis organisationen bruger et separat rekrutteringsprogram, kan rekrutteringsprocessen omfatte følgende trin:

- Angiv din rekrutteringsanmodning i Human Resources.
- Modtag henvisninger til kandidater i Human Resources fra rekrutteringsprogrammet.
- Gennemfør godkendelsesprocessen for kandidaten i Human Resources.

Hvis du ikke bruger et separat rekrutteringsprogram, kan du også manuelt administrere kandidater i Human Resources.

> [!NOTE]
> Hvis du er administrator eller udvikler og vil integrere Human Resources med et rekrutteringsprogram fra tredjepart, skal du se [Konfigurer Dataverse-integration](hr-admin-integration-common-data-service.md) og [Konfigurer Dataverse virtuelle tabeller](hr-admin-integration-common-data-service-virtual-entities.md)
>
> Du kan også finde apps til rekrutteringsintegration på [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).
>
## <a name="enable-recruiting-requests"></a>Aktiver rekrutteringsanmodninger

Hvis du vil sende rekrutteringsanmodninger i Human Resources, skal du først aktivere funktionaliteten i **Delte Human Resources-parametre**.

1. Vælg **Links** i arbejdsområdet **Personalestyring**.
2. Vælg **Delte parametre for personale** under **Konfiguration**.
3. Under fanen **Rekruttering** skal du under **Rekruttering** indstille **Aktivér rekrutteringsanmodninger** til **Ja**.

## <a name="add-a-recruiting-request-location"></a>Tilføje en lokation for en rekrutteringsanmodning

Hvis organisationen har flere lokationer, kan du tilføje dem, så anmodere kan vælge den lokation, hvor den nye rekrutterede skal arbejde. Lokationen medtages i jobopslaget.

1. Angiv en **Lokation for rekrutteringsanmodning** i søgepanelet.
2. Vælg **Ny**.
3. Angiv navnet på lokationen i feltet **Lokation for rekrutteringsanmodning**.

    ![Tilføj en lokation for en rekrutteringsanmodning.](./media/hr-recruit-0a-add-location.png)

4. Indtast en beskrivelse af lokationen i feltet **Beskrivelse**.
5. Vælg **Tilføj** under **Lokation**. Hvis dialogboksen **Ny adresse** vises, skal du angive adressen på lokationen.

    ![Indtast adresse.](./media/hr-recruit-0b-address.png)

6. Angiv oplysningerne om kontaktpersonen på lokationen under **Kontaktoplysninger**.
7. Vælg **Gem**.

## <a name="add-a-recruiting-request"></a>Tilføje en rekrutteringsanmodning

Ledere kan sende rekrutteringsanmodninger i Human Resources. Hvis du bruger et separat rekrutteringsprogram, vil disse trin sende en rekrutteringsanmodning og starte rekrutteringsprocessen i programmet. Ellers skal du udføre denne procedure for at starte arbejdsprocessen for din egen interne rekrutteringsproces.

1. Vælg **Medarbejderselvbetjening**.
2. Vælg fanen **Mit team**.
3. Vælg **Anmodning om rekruttering**.

    ![Start en rekrutteringsanmodning.](./media/hr-recruit-1-request-to-recruit.png)

4. Udfyld felterne **Beskrivelse**, **Job** og **Anslået startdato**.

    ![Fuldfør rekrutteringsanmodningen.](./media/hr-recruit-2-request-to-recruit.png)

5. Vælg **Fortsæt**. Rekrutteringsanmodningen for stillingen vises.
6. Vælg en rekrutteringsmedarbejder på rullelisten **Rekrutteringsmedarbejder** under **Generelt**, og vælg derefter en lokation på rullelisten **Lokation for rekrutteringsanmodning**.
7. Rediger oplysninger efter behov under **Job**, og vælg derefter **Opret detaljer fra job**.

    ![Opret detaljer fra job.](./media/hr-recruit-3-create-details-from-job.png)

    Resten af rekrutteringsanmodningen vil blive udfyldt med standardoplysninger for det job, du har angivet.

8. Angiv en beskrivelse af en ekstern stilling under **Ekstern beskrivelse**.
9. Under **Stillinger** skal du vælge **Tilføj** og derefter vælge en stilling for denne rekrutteringsanmodning.

    ![Tilføj en stilling.](./media/hr-recruit-4-select-position.png)

10. Vælg **Tilføj** under **Færdigheder**, og vælg derefter en færdighed.
11. Vælg **Tilføj** under **Uddannelseskrav**, og vælg derefter værdier på rullelisten **Uddannelse** og **Uddannelsesniveau**.

    ![Tilføj krav til uddannelse.](./media/hr-recruit-5-select-educational-requirements.png)

12. Tilføj evt. kommentarer under **Kommentar**.
13. Vælg et niveau på rullelisten **Niveau** under **Kompensation**, og juster derefter **Laveste tærskel**, **Referencepunkt** og **Højeste tærskel** efter behov.
14. Når din rekrutteringsanmodning er fuldført, og du er klar til at starte rekrutteringsprocessen, skal du vælge **Aktivér** på menulinjen.

    ![Aktivér rekrutteringsanmodning.](./media/hr-recruit-6-activate-recruit-request.png)

15. Vælg **Gem**.

## <a name="view-and-edit-your-recruiting-requests"></a>Se og rediger dine rekrutteringsanmodninger

Hvis du er leder og ønsker at se dine egne anmodninger:

1. Vælg **Medarbejderselvbetjening**.
2. Vælg fanen **Mit team**.
3. Under **Mine teamoplysninger** skal du vælge fanen **Rekrutteringsanmodninger**.

    ![Vælg fanen rekrutteringsanmodninger.](./media/hr-recruit-7-recruiting-requests.png)

4. Hvis du vil have vist eller redigere en rekrutteringsanmodning, skal du vælge den i gitteret.

Hvis du er personalemedarbejder og vil have vist alle rekrutteringsanmodninger:

1. Vælg **Personalestyring**.
2. Vælg **Rekrutteringsanmodninger**.

    ![Få vist rekrutteringsanmodninger i Personalestyring.](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. Hvis du vil have vist eller redigere en rekrutteringsanmodning, skal du vælge den i gitteret.

## <a name="add-or-edit-a-candidate-profile"></a>Tilføje eller redigere en kandidatprofil

Hvis organisationen er integreret med et andet program for at administrere rekrutteringsanmodninger, videresendes rekrutteringsanmodninger til dette program. Rekrutteringsprogrammet sender derefter kandidatoplysninger tilbage til Human Resources. Ellers kan du følge dine egne interne rekrutteringsprocesser og angive kandidatoplysninger manuelt.

1. Vælg **Personalestyring**.
2. Vælg **Links**.
3. Vælg **Kandidater** under **Rekruttering**.

    ![Få vist kandidater.](./media/hr-recruit-9-candidates.png)

4. Vælg **Ny** for at tilføje en kandidat. Hvis du vil redigere en eksisterende kandidat, skal du vælge kandidat på listen og derefter vælge **Rediger**. Kandidatprofilen vises.
5. Angiv eller rediger kandidatoplysningerne efter behov under **Kandidatoversigt**.
6. Under **Rekrutteringsanmodning** skal du vælge en rekrutteringsanmodning, som kandidaten skal knyttes til. Udfyld derefter felterne **Anslået startdato**, **Ansættelseschef**, **Stilling** og **Beskrivelse** efter behov.

    ![Tilknytte til rekrutteringsanmodning.](./media/hr-recruit-10-link-to-recruiting-request.png)

7. Udfyld alle oplysningerne i følgende områder, som du vil medtage i kandidatens post:

    - **Bemærkninger**
    - **Erhvervserfaring**
    - **Kontaktpersonoplysninger**
    - **Uddannelser**
    - **Færdigheder**
    - **Certifikater**
    - **Screeninger**

8. Vælg **Gem**.

## <a name="hire-a-candidate"></a>Ansætte en kandidat

Når du er klar til at ansætte en kandidat, skal du følge denne procedure for at lade kandidaten overgå til medarbejder.

1. Vælg **Ansæt** på siden **Kandidat**.

    ![Ansætte en kandidat.](./media/hr-recruit-11-hire.png)

2. Udfyld alle felter på siden **Ansæt ny arbejder** under **Detaljer**.

    ![Angive oplysninger om ny ansættelse.](./media/hr-recruit-12-hire-new-worker.png)

3. Bekræft og rediger oplysninger efter behov under **Detaljer for stilling**.
4. Vælg de relevante onboarding-tjeklister for denne medarbejder under **Kontrollister for onboarding**.
5. Vælg **Fortsæt** for at oprette medarbejderposten.

    > [!NOTE]
    > Afhængigt af organisationens arbejdsgange kan kandidatposten gennemgå yderligere godkendelsestrin, før den bliver en medarbejderpost.

## <a name="decide-not-to-hire-a-candidate"></a>Beslutte ikke at ansætte en kandidat

Hvis du beslutter dig for ikke at ansætte en kandidat, skal du følge denne procedure for at fjerne vedkommende fra vurderingsprocessen. 

1. Vælg **Ansæt ikke** på siden **Kandidat**.

    ![Ikke ansætte kandidat.](./media/hr-recruit-13-do-not-hire.png)

2. Vælg en **Årsagskode**, og medtag eventuelle kommentarer.
3. Vælg **OK**.

## <a name="dismiss-a-candidate"></a>Afvise en kandidat

Hvis det er nødvendigt, kan du afvise en kandidat efter at have ansat vedkommende. En kandidat kan f.eks. afvise dit tilbud eller ikke møde op den første dag.

- Vælg **Afvis kandidat** på siden **Kandidat**.

    ![Afvise kandidat.](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>Se også

[Konfigurere virtuelle Dataverse-tabeller](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Organisere dine medarbejdere](hr-personnel-departments-jobs-positions.md)<br>
[Konfigurere komponenterne i et job](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
