---
title: Konfigurere virtuelle enheder i Common Data Service
description: I dette emne vises, hvordan du konfigurerer virtuelle enheder til Dynamics 365 Human Resources. Opret og opdater eksisterende virtuelle enheder, og analysér oprettede og tilgængelige enheder.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0848b7556100fba38fcab0aa2a1a109e2e055fc9
ms.sourcegitcommit: b89baab13e530b5b1f079231619c628309a4742d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/05/2020
ms.locfileid: "3959569"
---
# <a name="configure-common-data-service-virtual-entities"></a>Konfigurere virtuelle enheder i Common Data Service

[!include [banner](includes/preview-feature.md)]

Dynamics 365 Human Resources er en virtuel datakilde i Common Data Service. Den giver fuld adgang til at oprette, læse, opdatere og slette data fra Common Data Service og Microsoft Power Platform. Dataene for de virtuelle enheder gemmes ikke i Common Data Service, men i programdatabasen. 

Hvis du vil aktivere disse handlinger på Human Resources-enheder fra Common Data Service, skal du gøre enhederne tilgængelige som virtuelle enheder i Common Data Service. På denne måde kan du udføre disse handlinger fra Common Data Service og Microsoft Power Platform på data i Human Resources. Handlingerne understøtter også fulde valideringer af forretningslogik i Human Resources for at sikre dataintegritet, når der skrives data til enhederne.

## <a name="available-virtual-entities-for-human-resources"></a>Tilgængelige virtuelle enheder for Human Resources

Alle OData-enheder (Open data Protocol) under Human Resources er tilgængelige som virtuelle enheder i Common Data Service. De er også tilgængelige i Power Platform. Nu kan du opbygge apps og oplevelser med data direkte fra Human Resources med fulde handlingsmuligheder uden at kopiere eller synkronisere data til Common Data Service. Du kan bruge Power Apps-portaler til at opbygge eksterne websteder, der giver mulighed for samarbejdsscenarier til forretningsprocesser i Human Resources.

Du kan få vist listen over de virtuelle enheder, der er aktiveret i miljøet, og starte med at arbejde med enhederne i [Power Apps](https://make.powerapps.com), i løsningen **Dynamics 365 HR Virtual Entities**.

![Dynamics 365 HR Virtual Entities i Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a>Virtuelle enheder i forhold til fysiske enheder

Virtuelle enheder til Human Resources er ikke de samme som de fysiske Common Data Service-enheder, der er oprettet for Human Resources. De fysiske enheder for Human Resources genereres separat og vedligeholdes i HCM Common-løsningen i Common Data Service. Med fysiske enheder gemmes dataene i Common Data Service og kræver synkronisering med programdatabasen til Human Resources.

> [!NOTE]
> Du kan se en liste over de fysiske Common Data Service-enheder for Human Resources i [Common Data Service-enheder](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).

## <a name="setup"></a>Konfiguration

Følg disse installationstrin for at aktivere virtuelle enheder i dit miljø. 

### <a name="register-the-app-in-microsoft-azure"></a>Registrere appen i Microsoft Azure

Først skal du registrere appen i Azure-portalen, så Microsoft-identitetsplatformen kan levere godkendelse og autorisationstjenester til appen og brugerne. Du kan finde flere oplysninger om registrering af apps i Azure under [Hurtig start: Registrere et program med platformen Microsoft-identitet](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

1. Åbn [Microsoft Azure-portalen](https://portal.azure.com).

2. Vælg **Appregistreringer** på listen Azure-tjenester.

3. Vælg **Ny registrering**.

4. Angiv et sigende navn for appen i feltet **Navn**. F.eks. **Dynamics 365 Human Resources-virtuelle enheder**.

5. Angiv URL-adressen til navneområdet for din forekomst af Human Resources i feltet **Omdirigerings-URI**.

6. Vælg **Registrer**.

7. Når registreringen er fuldført, viser Azure-portalen appregistreringens **Oversigt**-rude, som indeholder **Program-id (klient)**. Notér dig **Program-id (klient)** nu. Du skal angive disse oplysninger, når du [konfigurerer datakilden til den virtuelle enhed](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

8. Vælg **Certifikater og hemmeligheder** i venstre navigationsrude.

9. Vælg **Ny klienthemmelighed** i afsnittet **Klienthemmeligheder** på siden.

10. Indtast en beskrivelse, vælg en varighed, og vælg **Tilføj**.

11. Registrere værdien af hemmeligheden. Du skal angive disse oplysninger, når du [konfigurerer datakilden til den virtuelle enhed](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

    > [!IMPORTANT]
    > Husk at notere dig hemmelighedens værdi på dette tidspunkt. Hemmeligheden vises aldrig igen, når du forlader denne side.

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a>Installere appen Dynamics 365 HR Virtual Entity

Installer appen Dynamics 365 HR Virtual Entity i dit Power Apps-miljø for at udrulle den virtuelle enhedsløsningspakke til Common Data Service.

1. Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com).

2. Vælg det Power Apps-miljø, der er knyttet til din forekomst af Human Resources, på listen over **Miljøer**.

3. Vælg **Dynamics 365-apps** i sektionen **Ressourcer**.

4. Vælg handlingen **Installer app**.

5. Vælg **Dynamics 365 HR Virtual Entity**, og vælg **Næste**.

6. Gennemgå og markér, at du accepterer servicebetingelserne.

7. Vælg **Installer**.

Installationen tager et par minutter. Når den er fuldført, skal du fortsætte til de næste trin.

![Installer appen Dynamics 365 HR Virtual Entity fra Power Platform Administration](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a>Konfigurere datakilden til den virtuelle enhed 

Det næste trin er at konfigurere datakilden til den virtuelle enhed i Power Apps-miljøet. 

1. Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com).

2. Vælg det Power Apps-miljø, der er knyttet til din forekomst af Human Resources, på listen over **Miljøer**.

3. Vælg **URL-adressen til miljøet** i afsnittet **Detaljer** på siden.

4. I **Løsningstilstandshub** skal du vælge ikonet **Avanceret søgning** øverst til højre på programsiden.

5. Vælg **Finance and Operations-konfigurationer af virtuel datakilde** r på rullelisten **Søg efter** på siden **Avanceret søgning**.

6. Vælg **Resultater**.

7. Vælg posten **Microsoft HR-datakilde**.

8. Angiv de nødvendige oplysninger til datakildens konfiguration.

   - **Mål-URL-adresse** URL-adressen til dit Human Resources-navneområde.
   - **Lejer-id**: Azure Active Directory-lejer-id (Azure AD).
   - **AAD-program-id**: Det program-id (klient), der er oprettet for det program, der er registreret i Microsoft Azure-portalen. Du har modtaget disse oplysninger tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).
   - **AAD-programhemmelighed**: Den programklienthemmelighed, der er oprettet for det program, der er registreret i Microsoft Azure-portalen. Du har modtaget disse oplysninger tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

9. Vælg **Gem og luk**.

   ![Microsoft HR-datakilde](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a>Give app-tilladelser i Human Resources

Give tilladelser til de to Azure AD-programmer i Human Resources:

- Appen, der er oprettet til din lejer i Microsoft Azure-portalen
- Appen Dynamics 365 HR Virtual Entity, der er installeret i Power Apps-miljøet 

1. I Human Resources skal du åbne siden **Azure Active Directory-programmer**.

2. Vælg **Ny** for at oprette en ny programpost:

    - Angiv klient-id'et for den app, du har registreret i Microsoft Azure-portalen, i feltet **Klient-id**.
    - Angiv navnet på den app, du har registreret i Microsoft Azure-portalen, i feltet **Navn**.
    - I feltet **Bruger-id** skal du vælge bruger-id'et for en bruger med administratorrettigheder i Human Resources og Power Apps-miljøet.

3. Vælg **Ny** for at oprette endnu en programpost:

    - **Klient-id**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Navn**: Dynamics 365 HR Virtual Entity
    - I feltet **Bruger-id** skal du vælge bruger-id'et for en bruger med administratorrettigheder i Human Resources og Power Apps-miljøet.

## <a name="generate-virtual-entities"></a>Generere virtuelle enheder

Når installationen er fuldført, kan du vælge de virtuelle enheder, du vil generere og aktivere i din Common Data Service-forekomst.

1. Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com).

2. Vælg det Power Apps-miljø, der er knyttet til din forekomst af Human Resources, på listen over **Miljøer**.

3. Vælg **URL-adressen til miljøet** i afsnittet **Detaljer** på siden.

4. I **Løsningstilstandshub** skal du vælge ikonet **Avanceret søgning** øverst til højre på siden.

5. Vælg **Tilgængelige HR-enheder** på rullelisten **Søg efter** på siden **Avanceret søgning**.

6. Brug filterindstillingerne til at finde det eller de enheder, du vil aktivere.

7. Vælg en enhed på listen.

8. På enhedssiden skal du ændre egenskaben **Er genereret** til **Ja** for objektet.

9. Gem og luk enhedssiden.

> [!NOTE]
> Du kan oprette flere virtuelle enheder på én gang ved at bruge siden **Rediger flere poster**. Vælg flere poster på siden, og vælg **Rediger** på båndet. Du kan derefter ændre egenskaben **Er genereret** for alle valgte poster.

![Tilgængelige HR-enheder](./media/hr-admin-integration-virtual-entities-available.jpg)

> [!NOTE]
> For at strømline processen til generering af virtuelle enheder i fremtidige versioner vil processen finde sted på en side i Human Resources.

## <a name="see-also"></a>Se også

[Hvad er Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[Oversigt over enheder](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[Oversigt over enhedsrelationer](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[Oprette og redigere virtuelle enheder, der indeholder data fra en ekstern datakilde](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Hvad er Power Apps-portaler?](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[Oversigt over oprettelse af apps i Power Apps](https://docs.microsoft.com/powerapps/maker/)
