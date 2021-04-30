---
title: Integrere med LinkedIn Talent Hub
description: I dette emne forklares, hvordan du kan konfigurere integration mellem Microsoft Dynamics 365 Human Resources og LinkedIn Talent Hub.
author: jaredha
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 208998b5c09416407612352da7a8ef5dd9491914
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889974"
---
# <a name="integrate-with-linkedin-talent-hub"></a>Integrere med LinkedIn Talent Hub

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) er en platform med et ansøgersporingssystem (ATS). Her kan du rekruttere, administrere og ansætte medarbejdere på ét sted. Ved at integrere Microsoft Dynamics 365 Human Resources med LinkedIn Talent Hub kan du nemt oprette medarbejderposter i Human Resources for ansøgere, der er blevet ansat i en stilling.

## <a name="setup"></a>Konfiguration

En systemadministrator skal fuldføre installationsopgaverne, for at integrationen med LinkedIn Talent Hub kan finde sted. Først skal du i Power Apps-miljøet oprette en bruger- og sikkerhedsrolle for at tildele LinkedIn Talent Hub de relevante tilladelser til at skrive data i Human Resources.

### <a name="link-your-environment-to-linkedin-talent-hub"></a>Knytte miljøet til LinkedIn Talent Hub

1. Åbn [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).

2. Vælg **Produktindstillinger** i brugerrullemenuen.

3. Vælg **Integrationer** i sektionen **Avanceret** i navigationsruden til venstre.

4. Vælg **Autoriser** for Microsoft Dynamics 365 Human Resources-integrationen.

5. Vælg det miljø, som du vil knytte LinkedIn Talent Hub til, på siden **Dynamics 365 Human Resources**, og vælg derefter **Link**.

    ![LinkedIn Talent Hub-onboarding](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > Du kan kun tilknytte miljøer, hvor din brugerkonto har administratoradgang til både Human Resources-miljøet og det tilknyttede Power Apps-miljø. Hvis der ikke vises nogen miljøer på siden med Human Resources-link, skal du sikre dig, at du har licens til Human Resources-miljøer i lejeren, og at den bruger, du loggede på linksiden som, har administratorrettigheder til både Human Resources-miljøet og Power Apps-miljøet.

### <a name="create-a-power-apps-security-role"></a>Oprette en Power Apps-sikkerhedsrolle

1. Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com).

2. På listen **Miljøer** skal du vælge det miljø, der er knyttet til det Human Resources-miljø, som du vil knytte din forekomst af LinkedIn Talent Hub til.

3. Vælg **Indstillinger**.

4. Udvid noden **Brugere + tilladelser**, og vælg **Sikkerhedsroller**.

5. Vælg **Ny rolle** på værktøjslinjen på siden **Sikkerhedsroller**.

6. Angiv et navn til rollen under fanen **Detaljer**, f.eks. **LinkedIn Talent Hub HRIS-integration**.

7. Vælg tilladelse til at **Læse** på organisationsniveau under fanen **Tilpasning** for følgende enheder:

    - Enhed
    - Felt
    - Relation

8. Gem og luk sikkerhedsrollen.

### <a name="create-a-power-apps-application-user"></a>Oprette en Power Apps-applikationsbruger

Der skal oprettes en applikationsbruger, hvis LinkedIn Talent Hub-adapteren skal give tilladelser til, at kortet skriver kandidatposter ind i Power Apps-miljøet.

1. Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com).

2. På listen **Miljøer** skal du vælge det miljø, der er knyttet til det Human Resources-miljø, som du vil knytte din forekomst af LinkedIn Talent Hub til.

3. Vælg **Indstillinger**.

4. Udvid noden **Brugere + tilladelser**, og vælg **Brugere**.

5. Vælg **Administrer brugere i Dynamics 365**.

6. Brug rullemenuen over listen til at ændre visningen fra standardvisningen **Aktiverede brugere** til **Applikationsbrugere**.

    ![Visningen Applikationsbrugere](./media/hr-admin-integration-power-apps-application-users.jpg)

7. Vælg **Ny** på værktøjslinjen.

8. På siden **Ny bruger** skal du følge disse trin:

    1. Ret værdien i feltet **Brugertype** til **Applikationsbruger**.
    2. Indstil feltet **Brugernavn** til **DYNAMICS365 HR LinkedIn HRIS-integration**.
    3. Indstil feltet **Program-id** til **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    4. Angiv en værdi i felterne **Fornavn**, **Efternavn** og **Primær mailadresse**.
    5. Vælg **Gem \& Luk** på værktøjslinjen.

### <a name="assign-a-security-role-to-the-new-user"></a>Tildele en sikkerhedsrolle til den nye bruger

Når du har gemt og lukket den nye applikationsbruger i forrige afsnit, kommer du tilbage til siden **Brugerliste**.

1. På siden **Brugerliste** kan du ændre visningen til **Applikationsbrugere**.

2. Vælg den applikationsbruger, du oprettede i foregående afsnit.

3. Vælg **Administrer roller** på værktøjslinjen.

4. Vælg den sikkerhedsrolle, du oprettede tidligere til integrationen.

5. Vælg **OK**.

### <a name="add-an-azure-active-directory-app-in-human-resources"></a>Tilføje en Azure Active Directory-app i Human Resources

1. I Dynamics 365 Human Resources skal du åbne siden **Azure Active Directory-applikationer**.
2. Føj en ny post til listen, og indstil følgende felter:

    - **Klient-id**: Angiv **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    - **Navn**: Angiv navnet på den Power Apps-sikkerhedsrolle, du oprettede tidligere, f.eks. **LinkedIn Talent Hub HRIS-integration**.
    - **Bruger-id**: Vælg en bruger, der har rettigheder til at skrive data i personalestyring.

### <a name="create-the-table-in-dataverse"></a>Oprette tabellen i Dataverse

> [!IMPORTANT]
> Integrationen med LinkedIn Talent Hub afhænger af virtuelle tabeller i Dataverse for Human Resources. Som en forudsætning for dette trin i konfigurationen, skal du konfigurere virtuelle tabeller. Du kan finde oplysninger om, hvordan du konfigurerer virtuelle tabeller i [Konfigurere Dataverse virtuelle tabeller](./hr-admin-integration-common-data-service-virtual-entities.md).

1. I Human Resources skal du åbne siden **Dataverse-integration**.

2. Vælg fanen **Virtuelle tabeller**.

3. Filtrer enhedslisten efter enhedslabel for at finde **Kandidat eksporteret fra LinkedIn**.

4. Vælg enheden, og vælg derefter **Generer/Opdater**.

## <a name="exporting-candidate-records"></a>Eksport af kandidatposter

Når du har fuldført opsætningen, kan rekrutteringsmedarbejdere og medarbejdere i personaleafdelingen bruge funktionen **Eksportér til HRIS** i LinkedIn Talent Hub til at eksportere posterne for de hyrede kandidat fra LinkedIn Talent Hub til Human Resources.

### <a name="export-records-from-linkedin-talent-hub"></a>Eksportere poster fra LinkedIn Talent Hub

Når en ansøger har gennemgået rekrutteringsprocessen og er blevet ansat, kan du eksportere kandidatposten fra LinkedIn Talent Hub til Human Resources.

1. Åbn det projekt, som du har ansat den nye medarbejder til, i LinkedIn Talent Hub.

2. Vælg en kandidatpost.

3. Vælg **Skift stadie**, og vælg derefter **Ansat**.

4. Vælg **Eksportér til HRIS** i ellipsemenuen (**...**) for kandidaten.

5. Angiv de oplysninger, der skal eksporteres, i ruden **Eksportér til HRIS**:

    - I feltet **HRIS-udbyder** skal du vælge **Microsoft Dynamics 365 Human Resources**.
    - Vælg en startdato for den nye medarbejder i feltet **Startdato**.
    - Angiv en stillingsbetegnelse for den nye medarbejders job i feltet **Stillingsbetegnelse**.
    - Angiv den adresse, hvor medarbejderen bliver baseret, i feltet **Adresse**.
    - Angiv eller kontroller medarbejderens mailadresse.

![Ruden Eksportér til HRIS i LinkedIn Talent Hub](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a>Færdiggøre onboardingen i Human Resources

Kandidatposter, der eksporteres fra LinkedIn Talent Hub til Human Resources, vises i sektionen **Kandidater, der skal ansættes** på siden **Personalestyring**.

1. Åbn siden **Personalestyring** i Human Resources.

2. Vælg **Ansættelse** for den valgte kandidat i sektionen **Kandidater, der skal ansættes**.

3. Gennemse posten i dialogboksen **Ansæt ny arbejder**, og tilføj evt. påkrævede oplysninger. Du kan også vælge det stillingsnummer, som kandidaten er ansat til.

Når de nødvendige oplysninger er angivet, kan du fortsætte med dine standardprocesser til oprettelse af medarbejderposter og onboarding af medarbejdere.

Følgende oplysninger importeres og medtages i den nye medarbejderpost:

- Fornavn
- Efternavn
- Startdato for ansættelse
- E-mailadresse
- Telefonnummer

## <a name="see-also"></a>Se også

[Konfigurere virtuelle Dataverse-tabeller](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Hvad er Microsoft Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]