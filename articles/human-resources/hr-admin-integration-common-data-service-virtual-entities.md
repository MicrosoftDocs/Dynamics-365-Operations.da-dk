---
title: Konfigurere virtuelle Dataverse-tabeller
description: I dette emne vises, hvordan du konfigurerer virtuelle tabeller til Dynamics 365 Human Resources. Opret og opdater eksisterende virtuelle tabeller, og analysér oprettede og tilgængelige tabeller.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f0dac25ede6c9b9dfcfa1be1f1a5f4d7a7752112
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344708"
---
# <a name="configure-dataverse-virtual-tables"></a>Konfigurere virtuelle Dataverse-tabeller

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Human Resources er en virtuel datakilde i Microsoft Dataverse. Den giver fuld adgang til at oprette, læse, opdatere og slette data fra Dataverse og Microsoft Power Platform. Dataene for de virtuelle tabeller gemmes ikke i Dataverse, men i programdatabasen.

Hvis du vil aktivere disse handlinger på Human Resources-enheder fra Dataverse, skal du gøre enhederne tilgængelige som virtuelle tabeller i Dataverse. På denne måde kan du udføre disse handlinger fra Dataverse og Microsoft Power Platform på data i Human Resources. Handlingerne understøtter også fulde valideringer af forretningslogik i Human Resources for at sikre dataintegritet, når der skrives data til enhederne.

> [!NOTE]
> Enheder under Human Resources svarer til Dataverse-tabeller. Yderligere oplysninger om Dataverse (tidligere Common Data Service) og terminologiopdateringer finder du i [Hvad er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

## <a name="available-virtual-tables-for-human-resources"></a>Tilgængelige virtuelle tabeller for Human Resources

Alle OData-enheder (Open data Protocol) under Human Resources er tilgængelige som virtuelle tabeller i Dataverse. De er også tilgængelige i Power Platform. Nu kan du opbygge apps og oplevelser med data direkte fra Human Resources med fulde handlingsmuligheder uden at kopiere eller synkronisere data til Dataverse. Du kan bruge Power Apps-portaler til at opbygge eksterne websteder, der giver mulighed for samarbejdsscenarier til forretningsprocesser i Human Resources.

Du kan få vist listen over de virtuelle tabeller, der er aktiveret i miljøet, og starte med at arbejde med tabellerne i [Power Apps](https://make.powerapps.com), i løsningen **Dynamics 365 HR Virtual Tables**.

![Dynamics 365 HR Virtual Tables i Power Apps.](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a>Virtuelle tabeller vs. oprindelige tabeller

Virtuelle tabeller til Human Resources er ikke de samme som de oprindelige Dataverse-tabeller, der er oprettet til Human Resources. 

De oprindelige tabeller til Human Resources genereres separat og vedligeholdes i HCM Common-løsningen i Dataverse. Med de oprindelige tabeller gemmes dataene i Dataverse og kræver synkronisering med programdatabasen til Human Resources.

> [!NOTE]
> Du kan se en liste over de oprindelige Dataverse-tabeller til Human Resources i [Dataverse-tabeller](./hr-developer-entities.md).

## <a name="setup"></a>Konfiguration

Følg disse installationstrin for at aktivere virtuelle tabeller i dit miljø.

### <a name="enable-virtual-tables-in-human-resources"></a>Aktivere virtuelle tabeller i Human Resources

Først skal du aktivere virtuelle tabeller i arbejdsområdet **Funktionsstyring**.

1. I Human Resources skal du vælge **Systemadministration**.

2. Vælg felter **Funktionsstyring**.

3. Vælg **Virtuel tabelunderstøttelse til HR i Dataverse**, og vælg derefter **Aktivere**.

Du kan finde flere oplysninger om aktivering og deaktivering af funktioner i [Administrere funktioner](hr-admin-manage-features.md).

### <a name="register-the-app-in-microsoft-azure"></a>Registrere appen i Microsoft Azure

Du skal registrere dine forekomst af Human Resources i Azure-portalen, så Microsoft-identitetsplatformen kan levere godkendelse og autorisationstjenester til appen og brugerne. Du kan finde flere oplysninger om registrering af apps i Azure under [Hurtig start: Registrere et program med platformen Microsoft-identitet](/azure/active-directory/develop/quickstart-register-app).

1. Åbn [Microsoft Azure-portalen](https://portal.azure.com).

2. Vælg **Appregistreringer** på listen Azure-tjenester.

3. Vælg **Ny registrering**.

4. Angiv et sigende navn for appen i feltet **Navn**. F.eks. **Dynamics 365 Human Resources-virtuelle tabeller**.

5. Angiv URL-adressen til navneområdet for din forekomst af Human Resources i feltet **Omdirigerings-URI**.

6. Vælg **Registrer**.

7. Når registreringen er fuldført, viser Azure-portalen appregistreringens **Oversigt**-rude, som indeholder **Program-id (klient)**. Notér dig **Program-id (klient)** nu. Du skal angive disse oplysninger, når du vil [Konfigurere datakilden til den virtuelle tabel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

8. Vælg **Certifikater og hemmeligheder** i venstre navigationsrude.

9. Vælg **Ny klienthemmelighed** i afsnittet **Klienthemmeligheder** på siden.

10. Indtast en beskrivelse, vælg en varighed, og vælg **Tilføj**.

11. Registrer hemmelighedens værdi fra egenskaben **Værdi** i tabellen. Du skal angive disse oplysninger, når du vil [Konfigurere datakilden til den virtuelle tabel](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

    > [!IMPORTANT]
    > Husk at notere dig hemmelighedens værdi på dette tidspunkt. Hemmeligheden vises aldrig igen, når du forlader denne side.

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a>Installere appen Dynamics 365 HR Virtual Table

Installer appen Dynamics 365 HR Virtual Table i dit Power Apps-miljø for at udrulle den virtuelle tabelløsningspakke til Dataverse.

1. I Human Resources skal du åbne siden **Microsoft Dataverse-integration**.

2. Vælg fanen **Virtuelle tabeller**.

3. Vælg **Installer virtuel tabelapp**.

### <a name="configure-the-virtual-table-data-source"></a>Konfigurere datakilden til den virtuelle tabel

Det næste trin er at konfigurere datakilden til den virtuelle tabel i Power Apps-miljøet.

1. Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com).

2. Vælg det Power Apps-miljø, der er knyttet til din forekomst af Human Resources, på listen over **Miljøer**.

3. Vælg **URL-adressen til miljøet** i afsnittet **Detaljer** på siden.

4. I **Løsningstilstandshub** skal du vælge ikonet **Avanceret søgning** øverst til højre på programsiden.

5. Vælg **Finance and Operations-konfigurationer af virtuel datakilde** r på rullelisten **Søg efter** på siden **Avanceret søgning**.

   > [!NOTE]
   > Installationen af den virtuelle tabelapp fra det forrige opsætningstrin kan tage et par minutter. Hvis **Konfiguration af virtuel datakilde for Finance and Operations** ikke er tilgængelige på listen, skal du vente et minut og opdatere listen.

6. Vælg **Resultater**.

7. Vælg posten **Microsoft HR-datakilde**.

8. Angiv de nødvendige oplysninger til datakildens konfiguration:

   - **Mål-URL-adresse** URL-adressen til dit Human Resources-navneområde. Formatet for mål-URL-adressen er:
     
     https://\<hostname\>.hr.talent.dynamics.com/navneområder/\<namespaceID\>/

     F.eks.:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >Husk at medtage "**/**"-tegnet i slutningen af URL-adressen for at undgå at modtage en fejlmeddelelse.

   - **Lejer-id**: Azure Active Directory-lejer-id (Azure AD).

   - **AAD-program-id**: Det program-id (klient), der er oprettet for det program, der er registreret i Microsoft Azure-portalen. Du har modtaget disse oplysninger tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   - **AAD-programhemmelighed**: Den programklienthemmelighed, der er oprettet for det program, der er registreret i Microsoft Azure-portalen. Du har modtaget disse oplysninger tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   ![Microsoft HR-datakilde.](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. Vælg **Gem og luk**.

### <a name="grant-app-permissions-in-human-resources"></a>Give app-tilladelser i Human Resources

Give tilladelser til de to Azure AD-programmer i Human Resources:

- Appen, der er oprettet til din lejer i Microsoft Azure-portalen
- Appen Dynamics 365 HR Virtual Table, der er installeret i Power Apps-miljøet 

1. I Human Resources skal du åbne siden **Azure Active Directory-programmer**.

2. Vælg **Ny** for at oprette en ny programpost:

    - Angiv klient-id'et for den app, du har registreret i Microsoft Azure-portalen, i feltet **Klient-id**.
    - Angiv navnet på den app, du har registreret i Microsoft Azure-portalen, i feltet **Navn**.
    - I feltet **Bruger-id** skal du vælge bruger-id'et for en bruger med administratorrettigheder i Human Resources og Power Apps-miljøet.

3. Vælg **Ny** for at oprette endnu en programpost:

    - **Klient-id**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Navn**: Dynamics 365 HR Virtual Table
    - I feltet **Bruger-id** skal du vælge bruger-id'et for en bruger med administratorrettigheder i Human Resources og Power Apps-miljøet.

## <a name="generate-virtual-tables"></a>Generere virtuelle tabeller

Når installationen er fuldført, kan du vælge de virtuelle tabeller, du vil generere og aktivere i din Dataverse-forekomst.

1. I Human Resources skal du åbne siden **Microsoft Dataverse-integration**.

2. Vælg fanen **Virtuelle tabeller**.

> [!NOTE]
> Til/fra-knappen **Aktivér den virtuelle tabel** indstilles til **Ja** automatisk, når alle nødvendige konfigurationer er fuldført. Hvis knappen er indstillet til **Nej**, skal du gennemgå trinnene i tidligere afsnit af dette dokument for at sikre, at alle forudsætninger for installationen er opfyldt.

3. Vælg den tabel eller de tabeller, du vil oprette i Dataverse.

4. Vælg **Generer/Opdater**.

![Dataverse-integration.](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a>Kontrollere status for oprettelse af tabel

Virtuelle tabeller genereres i Dataverse via en asynkron baggrundsproces. Opdateringer af processen vises i handlingscenteret. Oplysninger om processen, herunder fejllogfiler, vises på siden **Procesautomatiseringer**.

1. Åbn listesiden **Procesautomatiseringer** i Human Resources.

2. Vælg fanen **Baggrundsprocesser**.

3. Vælg **Baggrundsproces i asynkron handling for virtuel tabelforespørgsel**.

4. Vælg **Vis seneste resultater**.

I slide-out-ruden vises de seneste udførelsesresultater for processen. Du kan se logfilen for processen, herunder eventuelle fejl, der returneres fra Dataverse.

## <a name="see-also"></a>Se også

[Hvad er Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)<br>
[Tabeller i Dataverse](/powerapps/maker/common-data-service/entity-overview)<br>
[Oversigt over tabelrelationer](/powerapps/maker/common-data-service/relationships-overview)<br>
[Oprette og redigere virtuelle tabeller, der indeholder data fra en ekstern datakilde](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Hvad er Power Apps-portaler?](/powerapps/maker/portals/overview)<br>
[Oversigt over oprettelse af apps i Power Apps](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
