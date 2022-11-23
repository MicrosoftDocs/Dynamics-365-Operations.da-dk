---
title: Installere tilføjelsesprogrammet Lagersynlighed
description: Denne artikel beskriver, hvordan du installerer og konfigurerer tilføjelsesprogrammet Lagersynlighed for Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: c08568b14d7f5c79a1d3609107a88f905498ce2b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762775"
---
# <a name="install-and-set-up-inventory-visibility"></a>Installere og konfigurere Inventory Visibility

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du installerer og konfigurerer tilføjelsesprogrammet Lagersynlighed for Microsoft Dynamics 365 Supply Chain Management.

Du skal bruge [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/v2) til at installere tilføjelsesprogrammet Lagersynlighed. Lifecycle Services er en samarbejdsportal, der leverer et miljø og et sæt regelmæssigt opdaterede tjenester, der hjælper dig med at administrere programlivscyklussen for dine Finans og drift-apps. Yderligere oplysninger finder du i [Ressourcer til Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

> [!TIP]
> Det anbefales, at du deltager i brugergruppen Tilføjelsesprogrammet Lagersynlighed, hvor du kan finde nyttige vejledninger, hente de seneste opdateringer og indsende eventuelle spørgsmål, du måtte have om brug af lagersynlighed. Hvis du vil deltage, skal du sende en mail til produktteamet for lagersynlighed på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) og medtage dit Supply Chain Management-miljø-id.

## <a name="inventory-visibility-prerequisites"></a>Forudsætninger for Lagersynlighed

Før du installerer Lagersynlighed, skal du fuldføre følgende opgaver:

- Få et Lifecycle Services-implementeringsprojekt, hvor mindst ét miljø er installeret.
- Kontrollér, at forudsætningerne for opsætning af tilføjelsesprogrammer er fuldført. Du kan flere oplysninger om disse forudsætninger i [Oversigt over tilføjelsesprogrammer](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Lagersynlighed kræver ikke sammenkædning af dobbeltskrivning.

> [!NOTE]
> De lande og områder, der i øjeblikket understøttes, omfatter Canada (CCA, ECA), USA (WUS, EUS), Den Europæiske Union (NEU, WEU), Storbritannien (SUK, WUK) og Australien (EAU, SEAU), Japan (EJP, WJP) og Brasilien (SBR, SCUS).

Hvis du har spørgsmål om disse forudsætninger, skal du kontakte produktteamet for Lagersynlighed på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Installere tilføjelsesprogrammet Lagersynlighed

Før du installerer tilføjelsesprogrammet, skal du registrere et program og føje en klient til Azure Active Directory (Azure AD) under dit Azure-abonnement. Du kan finde instruktioner i [Registrere et program](/azure/active-directory/develop/quickstart-register-app) og [Tilføje en klienthemmelighed](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Du skal notere værdierne for **Program-id (klient)**, **Klienthemmelighed** og **Lejer-id**, da du skal bruge dem senere.

> [!IMPORTANT]
> Hvis du har mere end ét Lifecycle Services-miljø, skal du oprette et andet Azure AD-program til hvert miljø. Hvis du bruger samme program-id og lejer-id til at installere tilføjelsesprogrammet Lagersynlighed i forskellige miljøer, vil der forekomme et tokenproblem for ældre miljøer. Det er kun den sidste, der er installeret, der er gældende.

Når du har registreret et program og føjet en klienthemmelighed til Azure AD, skal du følge disse trin for at installere tilføjelsesprogrammet Lagersynlighed.

1. Log på [Lifecycle Services](https://lcs.dynamics.com/Logon/Index).
1. Vælg det projekt, dit miljø skal implementeres i, på startsiden.
1. Vælg det miljø, som tilføjelsesprogrammet skal installeres i, på projektsiden.
1. Rul ned på miljøsiden, indtil sektionen **Miljøtilføjelsesprogrammer** vises i sektionen **Power Platform-integration**. Her kan du finde Dataverse-miljønavnet. Bekræft, at Dataverse-miljønavnet er det, du vil bruge til lagersynlighed.

    > [!NOTE]
    > I øjeblikket understøttes kun Dataverse-miljøer, der er oprettet ved hjælp af Lifecycle Services. Hvis dit Dataverse-miljø er blevet oprettet på en anden måde (f.eks. ved hjælp af PowerApps Administration), og hvis det er knyttet til dit Supply Chain Management-miljø, skal du først rette tilknytningsfejlen, før du installerer Lagersynlighed.
    >
    > Det er muligt, at dit dobbeltskrivningsmiljø er kædet sammen med en forekomst af Dataverse, mens Lifecycle Services ikke er konfigureret til Power Platform-integration. En sådan uoverensstemmelse kan forårsage uventet funktionalitet. Vi anbefaler, at Lifecycle Services-miljøoplysningerne stemmer overens med det, du er tilsluttet i forbindelse med dobbeltskrivning, så den samme forbindelse kan bruges af forretningshændelser, virtuelle tabeller og tilføjelsesprogrammer. Se [Uoverensstemmende sammenkædning](../../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#linking-mismatch) for oplysninger om løsning af tilknytningsproblemet. Når tilknytningsproblemet er løst, kan du fortsætte med at installere Lagersynlighed.

1. Vælg **Installér et nyt tilføjelsesprogram** i afsnittet **Tilføjelsesprogrammer for miljø**.

    ![Lifecycle Services-miljøside](media/inventory-visibility-environment.png "Lifecycle Services-miljøside")

1. Vælg linket **Installer et nyt tilføjelsesprogram**. Der vises en liste over tilgængelige tilføjelsesprogrammer.
1. Vælg **Lagersynlighed** på listen.
1. Angiv følgende felter for dit miljø:

    - **AAD-program-id (klient)** – Angiv det Azure AD-program-id, du har oprettet og noteret tidligere.
    - **AAD-lejer-id** – Angiv det lejer-id, du har noteret tidligere.

    ![Konfigurere side for tilføjelsesprogram](media/inventory-visibility-setup.png "Konfigurere side for tilføjelsesprogram")

1. Acceptér vilkårene og betingelserne ved at markere afkrydsningsfeltet **Vilkår og betingelser**.
1. Vælg **Installer**. Status for tilføjelsesprogrammet vises som **Installerer**. Når installationen er fuldført, skal du opdatere siden. Status bør ændre sig til **Installeret**.
1. Vælg i Dataverse afsnittet **Apps** i venstre navigation, og kontroller, at **lagersynlighed** Power Apps er installeret korrekt. Hvis sektionen **Apps** ikke eksisterer, skal du kontakte produktteamet for Lagersynlighed på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

> [!NOTE]
> Hvis systemet advarer dig om, at du ikke har rettigheder til at installere Lagersynlighed på Lifecycle Services, skal du kontakte administratoren for at ændre din tilladelse.
>
> Hvis det tager mere end en time at installere fra Lifecycle Services-siden, mangler brugerkontoen sandsynligvis rettigheder til at installere løsninger i Dataverse-miljøet. Følg disse trin for at løse dette problem:
>
> 1. Hvis du vil fjerne installationen af tilføjelsesprogrammet Lagersynlighed, skal du vælge Afinstaller på Lifecycle Services-siden.
> 1. Log på [Microsoft 365 Administration](https://admin.microsoft.com), og kontroller, at den brugerkonto, du vil bruge til at installere tilføjelsesprogrammet, har licensen "Dynamics 365 Unified Operations Plan" tildelt. Tildel licensen, hvis det er nødvendigt.
> 1. Log på [Power Platform Administration](https://admin.powerplatform.microsoft.com) med den relevante brugerkonto. Installer derefter tilføjelsesprogrammet Lagersynlighed ved at gøre følgende:
>     1. Vælg det miljø, hvor du vil installere tilføjelsesprogrammet.
>     1. Vælg **Dynamics 365-apps**.
>     1. Vælg **Installer app**.
>     1. Vælg **Lagersynlighed**
>
> 1. Når installationen er fuldført, skal du gå tilbage til Lifecycle Services-siden og prøve igen at geninstallere tilføjelsesprogrammet **Lagersynlighed**.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Oprette lagersynlighed i Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Implementere integrationspakken Lagersynlighed

Hvis du kører Supply Chain Management version 10.0.17 eller tidligere, skal du kontakte supportteamet for onboarding af lagersynlighed på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for at hente pakkefilen. Implementer derefter pakken i Lifecycle Services.

> [!NOTE]
> Hvis der opstår uoverensstemmelse mellem versioner under installationen, skal du importere projektet X++ manuelt til udviklingsmiljøet. Opret derefter implementeringspakken i udviklingsmiljøet, og implementer den i produktionsmiljøet.
>
> Koden er inkluderet i Supply Chain Management version 10.0.18. Hvis du kører denne version eller en senere, er det ikke påkrævet.

Sørg for, at følgende funktioner er aktiveret i dit Supply Chain Management-miljø. (Som standard er de aktiveret).

| Funktionsbeskrivelse | Kodeversion | Skifte klasse |
|---|---|---|
| Aktivere eller deaktivere ved hjælp af lagerdimensioner i tabellen InventSum      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Aktivere eller deaktivere ved hjælp af lagerdimensioner i tabellen InventSumDelta | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Konfigurer integration af lagersynlighed

Når du har installeret tilføjelsesprogrammet, kan du forberede Supply Chain Management-systemet til at arbejde med det ved at gøre følgende trin.

1. I Supply Chain Management skal du åbne arbejdsområdet **[Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og aktivere følgende funktioner.
    - *Integration af lagersynlighed* – påkrævet.
    - *Integration af lagersynlighed med reservationsmodkonto* – Anbefales, men valgfri. Kræver version 10.0.22 eller nyere. Du kan finde flere oplysninger i [Reservationer i Lagersynlighed](inventory-visibility-reservations.md).

1. Gå til **Lagerstyring \> Opsætning \> Parametre for integration af lagersynlighed**.
1. Åbn fanen **Generelt**, og foretag følgende indstillinger:
    - **Slutpunkt for lagersynlighed** – Angiv URL-adressen for det miljø, hvor du kører lagersynlighed. Du kan finde flere oplysninger i [Finde tjenestens slutpunkt](inventory-visibility-configuration.md#get-service-endpoint).
    - **Maksimalt antal poster i en enkelt anmodning** – Angiv det maksimale antal poster, der skal medtages i en enkelt anmodning. Du skal angive et positivt heltal, der er mindre end eller lig med 1000. Standardværdien er 512. Det anbefales på det kraftigste, at du beholder standardværdien, medmindre du har modtaget et råd fra Microsoft Support, eller hvis du på anden måde er sikker på, at du skal ændre den.

1. Hvis du har aktiveret den valgfrie funktion til *lagersynlighedsintegration med reservationsmodkonto*, skal du åbne fanen **Reservationsmodkonto** og foretage følgende indstillinger:
    - **Aktiver reservationsmodkonto** – Angiv til *Ja* for at aktivere denne funktion.
    - **Modifikator for reservation** – Vælg den lagertransaktionsstatus, der skal modpostere reservationer, der foretages ved lagersynlighed. Denne indstilling bestemmer det ordrebehandlingstrin, der udløser modregninger. Stadiet spores af ordrens lagerposteringsstatus. Vælg en af følgende indstillinger:
        - *I bestilling* – For statussen *I transaktion* sender en ordre en anmodning om modkontering, når den oprettes. Modantallet er antallet for den oprettede ordre.
        - *Reserver* – For statussen *Reservér bestilt transaktion* sender en ordre en anmodning om modkontering, når den reserveres, plukkes, følgesedlen bogføres eller faktureres. Anmodningen udløses kun én gang for det første trin, når den nævnte proces finder sted. Modantallet er det antal, hvor lagertransaktionens status ændres fra *I bestilling* til *Reserveret bestilt* (eller senere status) på den tilsvarende ordrelinje.

1. Gå til **Lagerstyring \> Periodisk \> Integration af lagersynlighed**, og aktivér jobbet. Alle hændelser med lagerændringer fra Supply Chain Management vil nu blive bogført i Lagersynlighed.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Fjerne installationen af tilføjelsesprogrammet Lagersynlighed

For at afinstallere tilføjelsesprogrammet Lagersynlighed skal du gøre følgende:

1. Log på Supply Chain Management.
1. Gå til **Lagerstyring \> Periodisk \> Integration af lagersynlighed**, og deaktivér jobbet.
1. Gå til Lifecycle Services, og åbn siden i det miljø, hvor du vil afinstallere tilføjelsesprogrammet ( [se også Installere tilføjelsesprogrammet Lagersynlighed](#install-add-in)).
1. Vælg **afinstaller**.
1. Afinstallationsprocessen afslutter nu tilføjelsesprogrammet Lagersynlighed, fjerner registreringen af tilføjelsesprogrammet fra Lifecycle Services og sletter eventuelle midlertidige data, der er gemt i datacachen for tilføjelsesprogrammet Lagersynlighed. De primære lagerdata, der er lagret i Dataverse-abonnementet, slettes dog ikke. Slet disse data ved at fuldføre denne procedure.
1. Åbn [Power Apps](https://make.powerapps.com).
1. Vælg **miljø** på navigationslinjen.
1. Vælg det Dataverse-miljø, der er bundet sammen med dit Lifecycle Services-miljø.
1. Gå derefter til **Løsninger**, og slet følgende løsninger i denne rækkefølge:
    1. Dynamics 365 Inventory Visibility – Anker
    1. Dynamics 365 Inventory Visibility - Plug-ins
    1. Dynamics 365 Inventory Visibility - Program
    1. Dynamics 365 Inventory Visibility - Kontrolelementer
    1. Dynamics 365 Inventory Visibility - Grundlag 

    Når du har slettet disse løsninger, slettes også de data, der er gemt i tabeller.

> [!NOTE]
> Hvis du gendanner en Supply Chain Management-database efter afinstallering af tilføjelsesprogrammet Lagersynlighed og derefter vil geninstallere tilføjelsesprogrammet, skal du kontrollere, at du har slettet de gamle data for Lagersynlighed, der er gemt i dit Dataverse-abonnement (som beskrevet i forrige procedure), før du geninstallerer tilføjelsesprogrammet. På den måde undgås problemer med uoverensstemmelser i data, der ellers kunne forekomme.

## <a name="clean-inventory-visibility-data-from-dataverse-before-restoring-the-supply-chain-management-database"></a><a name="restore-environment-database"></a>Rense data for lagersynlighed fra Dataverse, før du gendanner Supply Chain Management-databasen

Hvis du har brugt lagersynlighed og derefter gendanner Supply Chain Management-databasen, kan den gendannede database indeholde data, der ikke længere er i overensstemmelse med data, der tidligere er synkroniseret med Lagersynlighed til Dataverse. Denne uoverensstemmelse med data kan forårsage systemfejl og andre problemer. Det er derfor vigtigt, at du altid rydder alle data for lagersynlighed, fra Dataverse, før du gendanner en Supply Chain Management-database.

Hvis du har brug for at gendanne en Supply Chain Management-database, skal du benytte følgende fremgangsmåde:

1. Afinstaller tilføjelsesprogrammet Lagersynlighed og fjern alle relaterede data i Dataverse, som beskrevet i [Afinstallere tilføjelsesprogrammet Lagersynlighed](#uninstall-add-in)
1. Gendan din Database Supply Chain Management, f.eks. som det beskrives i [PITR (Database point-in-time restore)](../../fin-ops-core/dev-itpro/database/database-point-in-time-restore.md) eller [tidsbestemt gendannelse af produktionsdatabasen i et sandkassemiljø](../../fin-ops-core/dev-itpro/database/database-pitr-prod-sandbox.md).
1. Hvis du stadig vil bruge den, kan du geninstallere og konfigurere tilføjelsesprogrammet Lagersynlighed som beskrevet i [Installere tilføjelsesprogrammet Lagersynlighed](#install-add-in) og [Konfigurere integration af Lagersynlighed](#setup-inventory-visibility-integration)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
