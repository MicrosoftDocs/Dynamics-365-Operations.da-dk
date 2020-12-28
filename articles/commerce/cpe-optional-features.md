---
title: Konfigurere valgfrie funktioner for et Dynamics 365 Commerce-evalueringsmiljø
description: I dette emne beskrives det, hvordan du konfigurerer valgfrie funktioner for et Microsoft Dynamics 365 Commerce-evalueringsmiljø.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6f7ba7e6de3791720458b509059f008423c73a82
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410975"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a>Konfigurere valgfrie funktioner for et Dynamics 365 Commerce-evalueringsmiljø

[!include [banner](includes/banner.md)]

I dette emne beskrives det, hvordan du konfigurerer valgfrie funktioner for et Microsoft Dynamics 365 Commerce-evalueringsmiljø.

## <a name="prerequisites"></a>Forudsætninger

Hvis du vil evaluere transaktionsfunktionerne for mail, skal følgende forudsætninger være opfyldt:

- Du har en tilgængelig mailserver (Simple Mail Transfer Protocol \[SMTP\]-server), som kan bruges fra Microsoft Azure-abonnementet, hvor du har klargjort evalueringsmiljøet.
- Du har serverens fulde domænenavn (FQDN)/IP-adresse, SMTP-portnummer og godkendelsesdetaljer ved hånden.

## <a name="configure-the-image-back-end"></a>Konfigurer backend-billedet

### <a name="find-your-media-base-url"></a>Find din URL-basisadresse til dit medie

> [!NOTE]
> Før du kan fuldføre denne procedure, skal du udføre trinnene i [Konfigurer dit websted i Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).

1. Log på Commerce-webstedsgenerator ved hjælp af den URL-adresse, som du noterede ned, da du initialiserede e-Commerce i forbindelse med klargøring (jf. [Initialiser e-Commerce](provisioning-guide.md#initialize-e-commerce)).
1. Åbn webstedet **Fabrikam**.
1. Vælg **Mediebibliotek** i menuen til venstre.
1. Vælg et enkelt billedaktiv.
1. Find egenskaben **Offentlig URL-adresse** i egenskabsfremviseren til højre. Værdien er en URL-adresse. Her er et eksempel:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.

1. Erstat den sidste identifikator i URL-adressen (**MA1nQC** i det foregående eksempel) med følgende streng **search?fileName=**. Eksempel-URL-adressen ser således ud, når denne ændring er foretaget:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    Denne URL-adresse er URL-basisadressen til dit medie. Notér det.

### <a name="update-the-media-base-url"></a>Opdater URL-basisadressen til mediet

1. Log på Commerce-hovedkontor.
1. Anvend menuen til venstre for at gå til **Moduler \> Retail og Commerce \> Konfiguration af kanal \> Kanalprofiler**.
1. Vælg **Rediger**.
1. Under **Profilegenskaber** skal du erstatte egenskabsværdien for **URL-basisadressen til medieserveren** med den URL-basisadresse til medie, som du oprettede tidligere.
1. Vælg den kanal, der hedder **scXXXXXXXXX**.
1. Under **Profilegenskaber** skal du vælge **Tilføj**.
1. For den egenskab, der blev tilføjet, skal du vælge **URL-basisadresse til medieserver** som egenskabsnøglen. Angiv som egenskabsværdi den URL-basisadresse til mediet, som du oprettede tidligere.
1. Vælg **Gem**.

## <a name="configure-and-test-the-email-server"></a>Konfigurer og test mailserveren

> [!NOTE]
> SMTP-serveren eller mailtjenesten, du angiver her, skal være tilgængelig fra det Azure-abonnement, som du bruger til miljøet.

1. Log på Commerce-hovedkontor.
1. Brug menuen til venstre, og gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> E-mailparametre**.
1. På fanen **SMTP-indstillinger** i feltet **Udgående mailserver** skal du indtaste FQDN- eller IP-adressen på din SMTP-server eller e-mailtjeneste.
1. I feltet **SMTP-portnummer** skal du indtaste portnummeret. (Hvis du ikke bruger SSL-certifikater (Secure Sockets Layer) \[SSL\], er standardportnummeret **25**.)
1. Hvis der kræves godkendelse, skal du angive værdier i felterne **Brugernavn** og **Adgangskode**.
1. Vælg **Gem**.
1. Vælg **Opdater**.
1. På fanen **Test e-mail** i feltet **E-mailudbyder** skal du vælge **SMTP**.
1. Angiv den mailadresse, som testmailen skal leveres til, i feltet **Send til**.
1. Vælg **Send testmail**.

## <a name="configure-email-templates"></a>Konfigurer mailskabeloner

For hver transaktionshændelse, du vil sende mails for, skal du opdatere mailskabelonen med en gyldig afsendermailadresse.

1. Log på Commerce-hovedkontor.
1. Brug menuen til venstre, og gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Skabeloner til organisationsmail**.
1. Vælg **Vis liste**.
1. Benyt følgende fremgangsmåde for hver skabelon på listen:

    1. I feltet **Afsenders e-mailadresse** skal du angive afsenderens e-mailadresse.
    1. Valgfrit: I feltet **Afsenders navn** skal du indtaste det navn, der skal bruges som afsendernavnet.

1. Vælg **Gem**.

## <a name="customize-email-templates"></a>Tilpas mailskabeloner

Du ønsker måske at tilpasse e-mail-skabelonerne, så de bruger forskellige billeder. Du kan også opdatere links i skabelonerne, så de fører til dit evalueringsmiljø. Denne procedure beskriver, hvordan du henter standardskabelonerne, tilpasser dem og opdaterer skabelonerne i systemet.

1. I en browser kan du downloade [Microsoft Dynamics 365 Commerce-evalueringens .zip-fil med standardmailskabeloner](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) til din lokale computer. Denne fil indeholder følgende HTML-dokumenter:

    - Skabelon til ordrebekræftelse
    - Skabelon til udstedelse af gavekort
    - Skabelon til ny ordre
    - Skabelon til pakkeordre
    - Skabelon til plukordre

1. Tilpas skabelonerne ved hjælp af en tekst- eller HTML-editor. Se listen over [understøttede tokens](#supported-tokens-in-the-email-template) senere i dette emne.
1. Log på Commerce.
1. Brug menuen til venstre for at gå til **Moduler \> Organisationsadministration \> Konfiguration \> Skabelon til organisationsmail**.
1. Udvid listen til venstre for at få vist alle skabelonerne.
1. Følg disse trin for hver skabelon, du vil tilpasse:

    1. Vælg skabelonen på listen.
    1. Vælg den relevante sprogversion på listen under **E-mailbeskedens indhold**. (Standardsproget er **da-dk**.)
    1. Under **E-mailbeskedens indhold** skal du vælge **Rediger**. Ruden **Overfør mailskabelon** vises.
    1. Vælg **Gennemse**, og find den HTML-fil, der har det tilpassede indhold.
    1. Vælg **Overfør**. Skabelonen overføres til systemet, og der vises et eksempel.
    1. Vælg **OK**.
    1. Valgfrit: Tilpas egenskaben **Emne** for skabelonen.
    1. Vælg **Gem**.

### <a name="supported-tokens-in-the-email-template"></a>Understøttede tokens i mailskabelonen

Når e-mail er gengivet, vil disse tokens blive erstattet af de faktiske værdier, der gælder for kunden og kundens ordre.

#### <a name="sales-order"></a>Salgsordre

Følgende tokens gælder for den overordnede salgsordre.

| Navn på token | Tokenet |
|-------------------|-------|
| Ordrenummer      | %salesid% |
| Debitors navn   | %customername% |
| Leveringsadresse  | %deliveryaddress% |
| Faktureringsadresse   | %customeraddress% |
| Bestillingsdato        | %shipdate% |
| Leveringstilstand     | %modeofdelivery% |
| Diskontering          | %discount% |
| Moms         | %tax% |
| Ordretotal       | %total% |

#### <a name="sales-line"></a>Salgslinje

For hvert produkt i ordren erstattes følgende tokens med værdier.

> [!NOTE]
> Placer token for **Produktlisten - start** i begyndelsen af den HTML-blok, der gentages for hvert produkt, og placer token for **Produktliste - slut** i slutningen af blokken.

| Navn på token      | Token |
|------------------------|-------|
| Produktliste - start   | \<!--%tablebegin.salesline% --\> |
| Produktliste - slut     | \<!--%tableend.salesline%--\> |
| Produktnavn           | %lineproductname% |
| Beskrivende tekst            | %lineproductdescription% |
| Mængde               | %linequantity% |
| Linjeprisenhed        | %lineprice% (verify) |
| linjevaretotal        | %linenetamount% |
| linjerabat          | %linediscount% |
| Afsendelsesdato              | %lineshipdate% |
| Indkøbsmetode     | %linedeliverymode% |
| leveringsadresse       | %linedeliveryaddress% |
| Salgsenhed for linjen | %lineunit% |

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over Dynamics 365 Commerce-evalueringsmiljø](cpe-overview.md)

[Klargøre et Dynamics 365 Commerce-evalueringsmiljø](provisioning-guide.md)

[Konfigurere et Dynamics 365 Commerce-evalueringsmiljø](cpe-post-provisioning.md)

[Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø](cpe-bopis.md)

[Ofte stillede spørgsmål om Dynamics 365 Commerce-evalueringsmiljø](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-websted](https://aka.ms/Dynamics365CommerceWebsite)
