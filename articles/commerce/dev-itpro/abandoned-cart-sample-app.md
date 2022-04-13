---
title: Registrere forladte vogne og sende beskeder til kunder
description: Dette emne beskriver, hvordan du tilpasser eksemplet med Microsoft Dynamics 365 Commerce-appen til forladte vogne for at registrere forladte vogne og sende påmindelsesmail til kunder.
author: bicyclingfool
ms.date: 02/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1db4e988653aa55db2b18fb201edeafc4d16a1bc
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/26/2022
ms.locfileid: "8489024"
---
# <a name="detect-abandoned-carts-and-send-notifications-to-customers"></a>Registrere forladte vogne og sende beskeder til kunder

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du tilpasser eksemplet med Microsoft Dynamics 365 Commerce-appen til forladte vogne for at registrere forladte vogne og sende påmindelsesmail til kunder.

Muligheden for at få indtægter og bevare kunderne via meddelelser om forladte vogne er en vigtig egenskab, som Dynamics 365 Commerce understøtter. Ved at tilpasse eksempelappen til Commerce-connectoren til forladte indkøbsvogne, kan detailhandlende få adgang til indkøbsvogne på Retail Server, som ikke er blevet ændret i løbet af et tidsvindue, som detailforretningerne definerer. Disse vogne kan derefter hentes, suppleres med produkt- og kundedata og overføres til en tredjeparts mailmarketingudbyder, der kan generere mailbeskeder og sende dem til kunder.

Mailmeddelelsen om forladt indkøbsvogn, som kunderne modtager, kan indeholde følgende oplysninger:

- Kundens fornavn.
- Kundens efternavn.
- Kundens e-mail-adresse.
- En URL-adresse, der returnerer kunden til sin indkøbsvogn.
- Transaktionsvalutaen.
- En liste over produkter i kundens indkøbsvogn. For hvert produkt er der inkluderet følgende oplysninger:

    - Produktets viste navn
    - Produkt-id'et (bruges til at samle en URL-adresse på produktbeskrivelsessiden)
    - Et produktbillede, der automatisk kan få ændret størrelse, så der er plads til forskellige billedstørrelser
    - Den alternative tekst til produktbilledet
    - Produktets enhedspris

## <a name="abandoned-cart-connector-sample"></a>Eksempel på connector til forladte indkøbsvogne

En connector-model, som Microsoft leverer via Retail SDK (Software Development Kit), gør det muligt at hente og sende oplysninger om forladte vogne til en tredjeparts mailmarketingudbyder. Denne connector håndterer kommunikationen med Retail Server, bruger Azure Key Vault til sikkerhed, håndterer planlægning af hentning af indkøbsvogn i et bestemt tidsvindue og henter ordre- og produktdata. Den leverer også en eksempelimplementering af en integration med en tredjeparts mailmarketingudbyder. Connectoren er opbygget til at kommunikere med [Emarsys](https://emarsys.com) fra starten. Den kan dog nemt tilpasses, så den kan integreres med andre løsninger, f.eks. Constant Contact, Mailchimp og SendGrid.

I følgende illustration vises komponenterne i eksempelappen for connectoren til forladte indkøbsvogne.

![Komponenter i eksempelappen for connectoren til forladte indkøbsvogne](media/AbandonedCartConnector.png)

> [!IMPORTANT]
> Nogle geografiske områder kræver, at kunder kan fravælge at få deres indkøbsvognsdata sendt videre til en mailmarketingudbyder eller anmode om, at deres data fjernes. Microsoft giver dog ikke kunderne disse muligheder. Hvis du planlægger at gøre forretninger i områder, der giver dem bemyndigelse, skal du derfor levere den nødvendige infrastruktur og tilpasninger for at spore kundernes præferencer og på baggrund af dem forhindre, at kundedata sendes til din mailplatform. Du skal også definere en proces, der fjerner kundedata fra din mailmarketingudbyder på kundens anmodning.

## <a name="obtain-the-code-sample"></a>Anskaffe eksempelkoden

Eksempelappen for connectoren til forladte indkøbsvogne er inkluderet i Retail SDK fra og med version 10.0.16. Koden findes under **\\RetailSDK\\Code\\SampleExtensions\\RetailServer\\Extensions.AbandonedCartSample**. Du kan finde flere oplysninger om Retail SDK, og hvor du kan finde det, i [Retail SDK (Software Development Kit)](retail-sdk/retail-sdk-overview.md).

> [!NOTE]
> Selvom eksempelkoden blev tilgængelig i version 10.0.16-builds, er den kompatibel med version 10.0.13 og senere builds af Retail Server.

## <a name="prerequisites-and-dependencies"></a>Forudsætninger og afhængigheder

Før du kan udrulle og konfigurere eksempelkoden for connectoren til forladte indkøbsvogne, skal følgende forudsætninger være opfyldt.

### <a name="access-to-commerce-resources"></a>Adgang til Commerce-ressourcer

Hvis du vil konfigurere og udrulle connector-appen til forladte indkøbsvogne, skal du have adgang til følgende Commerce-ressourcer:

- Administratoradgang til Commerce-hovedkontoret for dit miljø
- Adgang til Microsoft Dynamics Lifecycle Services-projektet (LCS) for dit miljø

### <a name="azure-cosmos-db"></a>Azure Cosmos DB

Connector-appen til forladte indkøbsvogne bruger Azure Cosmos DB til at spore id og tidsstempel på indkøbsvogne, der tidligere er hentet. Du kan bruge Azure Cosmos DB til at bevare disse data, eller du kan tilpasse kodeeksemplet til integration med en anden mulighed for datalagring. Du kan finde flere oplysninger om Azure Cosmos DB under [Velkommen til Azure Cosmos DB](/azure/cosmos-db/introduction).

Før du kører eksemplet, skal følgende forudsætninger være opfyldt, hvis du bruger Azure Cosmos DB:

- Du skal have en Azure Cosmos DB-konto. Hvis du ikke har en konto, skal du se [Oprette en databasekonto](/azure/cosmos-db/create-sql-api-dotnet#create-a-database-account).
- Du skal hente værdierne af **URI** og **PRIMÆRNØGLE** (eller **SEKUNDÆRNØGLE**) fra bladet **Nøgler** i din Azure Cosmos DB-konto på Azure-portalen. Yderligere oplysninger om, hvordan du henter slutpunkt- og nøgleoplysninger om din Azure Cosmos DB-konto , finder du i [Se, kopiere og regenerere adgangsnøgler og adgangskoder](/azure/cosmos-db/manage-account#keys).

### <a name="azure-key-vault"></a>Azure Key Vault

Connector-appen til forladte indkøbsvogne bruger Key Vault til at gemme navnene og hemmelighederne på de forskellige komponenter, der kræver sikker adgang.

Benyt følgende fremgangsmåde for at konfigurere en Key Vault.

1. Følg instruktionerne i [Adminisrere Key Vault i Azure Stack-hub ved hjælp af portalen](/azure-stack/user/azure-stack-key-vault-manage-portal?view=azs-2002&preserve-view=true).
2. Opret hemmeligheder for følgende oplysninger:

    - Emarsys API-brugernavn (Application Programming Interface) og API-hemmelighed
    - Program-id og hemmelighed for forladt indkøbsvogn

Eksempelkoden for connectoren til forladte indkøbsvogne bruger Azure-standardlegitimationsoplysningerne til at få adgang til Key Vault. Du skal tildele **Liste**- og **Læse**-rettigheder til den identitet, du vil bruge for at få adgang til Key Vault.

Du kan finde flere oplysninger om Azure-standardlegitimationsoplysninger i [DefaultAzureCredential-klassen](/dotnet/api/azure.identity.defaultazurecredential?view=azure-dotnet&preserve-view=true).

## <a name="create-an-abandoned-cart-connector-sample-app-application-id-for-the-azure-ad-tenant"></a>Oprette et applikations-id for Azure AD-lejeren i eksempelappen for connectoren til forladte indkøbsvogne

Du skal oprette et applikations-id for Azure Active Directory-lejeren (AD) i eksempelappen for connectoren til forladte indkøbsvogne. Du kan finde oplysninger om, hvordan du opretter et program-id, i [Bruge portalen til at oprette et Azure AD-program og en tjenesteprincipal, der har adgang til ressourcer](/azure/active-directory/develop/howto-create-service-principal-portal).

## <a name="add-the-abandoned-cart-connector-sample-app-application-id-to-the-allow-list-for-the-retail-server-api"></a>Tilføje eksempelappens program-id for connectoren til forladte indkøbsvogne på listen over tilladte for Retail Server-API

Derefter skal du tilføje eksempelappens program-id for connectoren til forladte indkøbsvogne på listen over tilladte for Retail Server-API. Du kan finde flere oplysninger om, hvordan du føjer et program-id til listen over tilladte i Azure, under [Understøttelse af service til service-godkendelse i Retail Server](https://community.dynamics.com/ax/b/axforretail/posts/support-for-service-to-service-authentication-in-retail-server).

## <a name="configure-the-abandoned-cart-connector-sample-app"></a>Konfigurere eksempelappen for connectoren til forladte indkøbsvogne

Hvis du vil konfigurere eksempelappen for connectoren til forladte indkøbsvogne, skal du redigere konfigurationsfilen **appSettings.json**, der er placeret i roden af mappen **AbandonedCartDetectionSample**. I følgende tabeller beskrives egenskaberne for konfigurationsfilen.

### <a name="keyvaultoptions"></a>KeyVaultOptions

| Egenskab    | Beskrivelse |
| ----------- | ----------- |
| KeyVaultURI | DNS-navnet (Domain Name System) for den Key Vault, du bruger i Azure-portalen. |

### <a name="retailserverclientoptions"></a>RetailServerClientOptions

| Egenskab                                      | Beskrivelse |
| --------------------------------------------- | ----------- |
| TenantId                                      | Lejer-id i Azure AD for din Azure-lejer. |
| RetailServerAudienceId                        | Retail Server-målgruppe-id. Du kan beholde standardværdien. |
| AppIdKeyVaultSecretName                       | Navnet på hemmeligheden, du oprettede for program-id'et til eksempelappen for connectoren til forladte indkøbsvogne. |
| AppSecretKeyVaultSecretName                   | Navnet på hemmeligheden, der opbevarer apphemmeligheden for program-id'et til eksempelappen for connectoren til forladte indkøbsvogne. |
| RetailServerUrl                               | URL-adressen for din forekomst af Retail Server. Denne værdi findes i LCS. |
| OperatingUnitNumber                           | Driftsenhedsnummeret (OUN). Denne værdi findes i Commerce-hovedkontoret. |
| IncludeAbandonedCartsModifiedSinceLastMinutes | Starten af tidsvinduet for de forladte indkøbsvogne, du vil hente. Værdien angives som et antal minutter før det nuværende tidspunkt. Angiv f.eks. denne egenskab til **120** for at hente alle de vogne, der senest er ændret for mellem 120 minutter siden og slutningen af det tidsvindue, der er defineret af egenskaben **ExcludeAbandonedCartsModifiedSinceLastMinutes**. |
| ExcludeAbandonedCartsModifiedSinceLastMinutes | Slutningen af tidsvinduet for de forladte indkøbsvogne, du vil hente. Værdien angives som et antal minutter før det nuværende tidspunkt. Hvis egenskaben **IncludeAbandonedCartsModifiedSinceLastMinutes** f.eks. er angivet til **120**, skal du angive denne egenskab til **30** for at hente alle de indkøbsvogne, der er ændret for mellem 120 minutter siden og 30 minutter siden. I praksis definerer denne egenskab, hvor lang tid du vil vente, før en indkøbsvogn erklæres forladt. |
| ReturnToCartUrl                               | URL-adressen på indkøbsvognen på e-handelswebstedet i det format, der bruges i filen **app.config**. |

### <a name="azurecosmosoptions"></a>AzureCosmosOptions

Jobstatus for hentning af forladt indkøbsvogn, vogn-id'er og redigerede tidsstempler gemmes i Azure Cosmos DB. Indstillingerne i konfigurationsfilen peger som standard på den lokale emulatorforekomst af Azure Cosmos DB. Når du udruller connectoren i produktion, skal du opdatere disse indstillinger, så de peger på Azure Cosmos DB-forekomsten i dit Azure-abonnement. Ved lokale test eller sandkassetest kan du bruge [Azure Cosmos DB Emulator](/azure/cosmos-db/local-emulator).

| Egenskab    | Beskrivelse |
| ----------- | ----------- |
| EndPointUri | Den URI for slutpunktet, der leveres af Azure eller emulatoren. |
| PrimaryKey  | Den primærnøgle, der leveres af Azure eller emulatoren. |
| DatabaseId  | Databasens id. Du kan beholde standardværdien eller angive din egen. |
| ContainerId | Container-id'et. Du kan beholde standardværdien eller angive din egen. |

### <a name="emarsysclientoptions"></a>EmarsysClientOptions

> [!NOTE]
> Hvis du integrerer med en anden mailmarketingudbyder end Emarsys, skal du udvide grænsefladen **IEmailProvider**, så den kommunikerer med den pågældende udbyder.

| Egenskab                      | Beskrivelse |
| ----------------------------- | ----------- |
| ApiUrl                        | `https://api.emarsys.net/api/v2/event/{0}/trigger` |
| ExternalEventId               | Id'et for den eksterne hændelsespost, der er oprettet i Emarsys. Du kan finde værdien under **Udløserindstillinger** i den kampagne, du har oprettet for at sende mailbeskeder om forladte indkøbsvogne. |
| ApiUserNameKeyVaultSecretName | Navnet på den nøgle, hvor Emarsys API-brugernavnet er gemt. |
| ApiSecretKeyVaultSecretName   | Navnet på den nøgle, hvor Emarsys API-hemmeligheden er gemt. |
| EmarsysContactKeyId           | Id'et for mailkolonnen i Emarsys-kontaktdatabasen. Standardværdien er **3** og bør ikke ændres. |

### <a name="mediaoptions"></a>MediaOptions

Hvis du bruger funktionerne for e-handel i Commerce, kan du bruge Commerce-administration af digitale aktiver til at hente produktbilleder. Du kan finde flere oplysninger om egenskaberne for ændring af billedstørrelse i administration af digitale aktiver under [ImageSettings-billedkonfiguration](../e-commerce-extensibility/image-component.md#imagesettings-viewport-configuration).

| Egenskab                             | Beskrivelse |
| ------------------------------------ | ----------- |
| ImageServerUrl                       | Rod-URL-adressen til webstedets styring af digitale aktiver. Du kan finde værdien i egenskabsnøglen **URL-basisadresse til medieserver** under **Retail og Commerce \> Konfiguration af kanal \> Kanalprofiler** i Commerce-hovedkontoret. |
| ImageViewPorts                       | Containernoden til individuelle billedkonfigurationer. |
| ImageViewPorts/viewport              | Definitionen af visningsporten. Brug denne egenskab til at angive breddeintervallerne for visningsporten i pixel. Du kan finde et eksempel på, hvordan denne egenskab bruges, i konfigurationsfilen **appSettings.json**. |
| ImageViewPorts/imageWidth            | Billedbredden af visningsporten i pixel. |
| imageViewPorts/imageHeight           | Billedhøjden af visningsporten i pixel. |
| imageViewPorts/useForDefaultImageTag | En **sand**/**falsk**-værdi, der angiver, om de billeddimensioner, der er defineret af visningsporten, skal bruges, hvis HTML-mærkatet `<picture>` ikke understøttes for en webbrowser eller mailklient. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
