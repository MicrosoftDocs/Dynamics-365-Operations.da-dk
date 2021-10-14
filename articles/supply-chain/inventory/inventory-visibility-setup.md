---
title: Installere tilføjelsesprogrammet Lagersynlighed
description: Dette emne beskriver, hvordan du installerer og konfigurerer tilføjelsesprogrammet Lagersynlighed for Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d6f58eab38d1aee97a5d39704255bf06a168b36c
ms.sourcegitcommit: 79d19924ed736c9210fa9ae4e0d4c41c53c27eb5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2021
ms.locfileid: "7581859"
---
# <a name="install-and-set-up-inventory-visibility"></a>Installere og konfigurere lagersynlighed

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Dette emne beskriver, hvordan du installerer og konfigurerer tilføjelsesprogrammet Lagersynlighed for Microsoft Dynamics 365 Supply Chain Management.

Du skal bruge Microsoft Dynamics Lifecycle Services (LCS) til at installere tilføjelsesprogrammet Lagersynlighed. LCS er en samarbejdsportal, der leverer et miljø og et sæt regelmæssigt opdaterede tjenester, der hjælper dig med at administrere programlivscyklussen for dine Finance and Operations-apps.

Yderligere oplysninger finder du i [Ressourcer til Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

## <a name="inventory-visibility-prerequisites"></a>Forudsætninger for Lagersynlighed

Før du installerer Lagersynlighed, skal du fuldføre følgende opgaver:

- Få et LCS-implementeringsprojekt, hvor mindst ét miljø er installeret.
- Kontrollér, at forudsætningerne for opsætning af tilføjelsesprogrammer er fuldført. Du kan flere oplysninger om disse forudsætninger i [Oversigt over tilføjelsesprogrammer](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Lagersynlighed kræver ikke sammenkædning af dobbeltskrivning.

> [!NOTE]
> De lande og områder, der i øjeblikket understøttes, omfatter Canada (CCA, ECA), USA (WUS, EUS), Den Europæiske Union (NEU, WEU), Storbritannien (SUK, WUK) og Australien (EAU, SEAU), Japan (EJP, WJP) og Brasilien (SBR, SCUS).

Hvis du har spørgsmål om disse forudsætninger, skal du kontakte produktteamet for Lagersynlighed på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Installere tilføjelsesprogrammet Lagersynlighed

Før du installerer tilføjelsesprogrammet, skal du registrere et program og føje en klient til Azure Active Directory (Azure AD) under dit Azure-abonnement. Du kan finde instruktioner i [Registrere et program](/azure/active-directory/develop/quickstart-register-app) og [Tilføje en klienthemmelighed](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Du skal notere værdierne for **Program-id (klient)**, **Klienthemmelighed** og **Lejer-id**, da du skal bruge dem senere.

Når du har registreret et program og føjet en klienthemmelighed til Azure AD, skal du følge disse trin for at installere tilføjelsesprogrammet Lagersynlighed.

1. Log på [LCS](https://lcs.dynamics.com/Logon/Index).
1. Vælg det projekt, dit miljø skal implementeres i, på startsiden.
1. Vælg det miljø, som tilføjelsesprogrammet skal installeres i, på projektsiden.
1. Rul ned på miljøsiden, indtil sektionen **Miljøtilføjelsesprogrammer** vises i sektionen **Power Platform-integration**. Her kan du finde Dataverse-miljønavnet. Bekræft, at Dataverse-miljønavnet er det, du vil bruge til lagersynlighed.

    > [!NOTE]
    > I øjeblikket understøttes kun Dataverse-miljøer, der er oprettet ved hjælp af LCS. Hvis dit Dataverse-miljø er blevet oprettet på en anden måde (f.eks. ved hjælp af Power Apps Administration), og hvis det er knyttet til dit Supply Chain Management-miljø, skal du først kontakte produktteamet for Lagersynlighed på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for at rette tilknytningsfejlen. Derefter kan du installere Lagersynlighed.

1. Vælg **Installér et nyt tilføjelsesprogram** i afsnittet **Tilføjelsesprogrammer for miljø**.

    ![Miljøside i LCS](media/inventory-visibility-environment.png "Miljøside i LCS")

1. Vælg linket **Installer et nyt tilføjelsesprogram**. Der vises en liste over tilgængelige tilføjelsesprogrammer.
1. Vælg **Lagersynlighed** på listen.
1. Angiv følgende felter for dit miljø:

    - **AAD-program-id (klient)** – Angiv det Azure AD-program-id, du har oprettet og noteret tidligere.
    - **AAD-lejer-id** – Angiv det lejer-id, du har noteret tidligere.

    ![Konfigurere side for tilføjelsesprogram](media/inventory-visibility-setup.png "Konfigurere side for tilføjelsesprogram")

1. Acceptér vilkårene og betingelserne ved at markere afkrydsningsfeltet **Vilkår og betingelser**.
1. Vælg **Installer**. Status for tilføjelsesprogrammet vises som **Installerer**. Når installationen er fuldført, skal du opdatere siden. Status bør ændre sig til **Installeret**.
1. Vælg i Dataverse afsnittet **Apps** i venstre navigation, og kontroller, at **lagersynlighed** Power Apps er installeret korrekt. Hvis sektionen **Apps** ikke eksisterer, skal du kontakte produktteamet for Lagersynlighed på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

> [!IMPORTANT]
> Hvis du har mere end ét LCS-miljø, skal du oprette et andet Azure AD-program til hvert miljø. Hvis du bruger samme program-id og lejer-id til at installere tilføjelsesprogrammet Lagersynlighed i forskellige miljøer, vil der forekomme et tokenproblem for ældre miljøer. Det er kun den sidste, der er installeret, der er gældende.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Fjerne installationen af tilføjelsesprogrammet Lagersynlighed

Hvis du vil fjerne installationen af tilføjelsesprogrammet Lagersynlighed, skal du vælge **Afinstaller** på LCS-siden. Afinstallationsprocessen afslutter tilføjelsesprogrammet Lagersynlighed, fjerner registreringen af tilføjelsesprogrammet fra LCS og sletter eventuelle midlertidige data, der er gemt i datacachen for tilføjelsesprogrammet Lagersynlighed. De primære lagerdata, der er lagret i Dataverse-abonnementet, slettes dog ikke.

Hvis du vil afinstallere lagerdata, der er gemt i Dataverse-abonnementet, skal du åbne [Power Apps](https://make.powerapps.com), vælge **Miljø** på navigationslinjen og vælge det Dataverse-miljø, der er forbundet med LCS-miljøet. Gå derefter til **Løsninger**, og slet følgende fem løsninger i denne rækkefølge:

1. Fastgøre løsning til applikationen Lagersynlighed i Dynamics 365-løsninger
1. Løsning til Dynamics 365 FNO SCM Inventory Visibility-applikationer
1. Inventory Configuration Service
1. Lagersynlighedstjeneste
1. Basisløsning til Dynamics 365 FNO SCM Inventory Visibility

Når du har slettet disse løsninger, slettes også de data, der er gemt i tabeller.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Oprette lagersynlighed i Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Implementere integrationspakken Lagersynlighed

Hvis du kører Supply Chain Management version 10.0.17 eller tidligere, skal du kontakte supportteamet for onboarding af lagersynlighed på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for at hente pakkefilen. Implementer derefter pakken i LCS.

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
    - **Modifikator for reservation** – Vælg den lagertransaktionsstatus, der skal modpostere reservationer, der foretages ved lagersynlighed. Denne indstilling bestemmer det ordrebehandlingstrin, der udløser modregninger. Stadiet spores af ordrens lagerposteringsstatus. Vælg en af følgende muligheder:
        - *I bestilling* – For statussen *I transaktion* sender en ordre en anmodning om modkontering, når den oprettes. Modantallet er antallet for den oprettede ordre.
        - *Reserver* – For statussen *Reservér bestilt transaktion* sender en ordre en anmodning om modkontering, når den reserveres, plukkes, følgesedlen bogføres eller faktureres. Anmodningen udløses kun én gang for det første trin, når den nævnte proces finder sted. Modantallet er det antal, hvor lagertransaktionens status ændres fra *I bestilling* til *Reserveret bestilt* (eller senere status) på den tilsvarende ordrelinje.

1. Gå til **Lagerstyring \> Periodisk \> Integration af lagersynlighed**, og aktivér jobbet. Alle hændelser med lagerændringer fra Supply Chain Management vil nu blive bogført i Lagersynlighed.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
