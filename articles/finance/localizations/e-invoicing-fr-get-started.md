---
title: Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Frankrig
description: Denne artikel indeholder oplysninger, der hjælper dig med at komme i gang med tilføjelsesprogrammet til elektronisk fakturering for Frankrig.
author: dkalyuzh
ms.date: 07/07/2022
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-00-02
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: 365316b204b6d76fa6ee6b2402fefee50c8ff3ef
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220645"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-france"></a>Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Frankrig

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Denne artikel indeholder oplysninger, der hjælper dig med at komme i gang med elektronisk fakturering for Frankrig. Det fører dig gennem de konfigurationstrin, der er lande-/områdeafhængige i Regulatory Configuration Service (RCS). Disse trin supplerer de trin, der er beskrevet i [Introduktion til tilføjelsesprogrammet til elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Den landespecifikke konfiguration til den franske Chorus Pro (FR) elektroniske fakturafunktion

Der kræves nogle trin for at konfigurere den elektroniske faktureringsfunktionen **Fransk Chorus Pro-afsendelse (FR)**. Nogle af parametrene fra konfigurationen publiceres med standardværdier. Disse værdier skal gennemses og opdateres, så de bedre afspejler din virksomheds drift.

### <a name="prerequisites"></a>Forudsætninger

Før du indleder procedurerne i denne artikel, skal du opfylde følgende forudsætninger:

- Bliver fortrolig med elektronisk fakturering. Du kan finde flere oplysninger i [Oversigt over elektronisk fakturering](e-invoicing-service-overview.md).
- Tilmeld dig RCS, og konfigurer elektronisk fakturering. Du kan finde flere oplysninger i følgende artikler:

    - [Tilmelde og installere elektronisk faktureringstjeneste](e-invoicing-sign-up-install.md)
    - [Konfigurere Azure-ressourcer til elektronisk fakturering](e-invoicing-set-up-azure-resources.md)
    - [Installere tilføjelsesprogrammet til mikroservices i Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md)
    - [Aktivere og konfigurere integration med elektronisk fakturering](e-invoicing-activate-setup-integration.md) – Du kan bruge oplysningerne i denne artikel til at aktivere integrationen mellem Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management-app og elektronisk faktureringstjeneste.
    - [NAF-koder og siret-numre](emea-fra-naf-codes-siret-numbers.md) og [Konfigurere NAF-koder og Siret-numre](tasks/fr-00003-naf-codes-siret-numbers.md) – Brug oplysningerne i disse artikler til at konfigurere NAF-koder og Siret-numre i dine juridiske enheder. 

- Din organisation skal være registreret til drift med Chorus Pro. Microsoft leverer integration med Chorus Pro i OAuth2-tilstand via en API (Application Programming Interface). Detaljerede oplysninger om tilmelding til Chorus Pro og programaktivering finder du i den [officielle dokumentation](https://communaute.chorus-pro.gouv.fr/documentation/help-for-api-developers-in-oauth2-mode/).

    Følg disse trin for at tilmelde dig Chorus Pro.

    1. Gå til [PISTE-portalen](https://piste.gouv.fr/en/component/apiportal/registration) for at starte din registrering. 
    2. Registrer et program, og aktivér legitimationsoplysningerne for Open Authorization (OAuth).
    3. Kopiér og gem klient-id'et for OAuth-legitimationsoplysningerne og hemmelig nøgle. Du skal bruge disse oplysninger i senere trin.
    4. Gå til [Chorus Pro-portalen](https://portail.chorus-pro.gouv.fr/aife_csm/?id=aife_enrollment) for at blive registreret. 
    5. Opret en teknisk konto til API-adgang. Du kan finde flere oplysninger under [Oprette en teknisk konto til API-adgang i produktionen](https://communaute.chorus-pro.gouv.fr/documentation/creation-of-a-technical-account-for-an-api-access-in-production/).
    6. Kopiér bruger-id'et for den tekniske konto og adgangskoden. Du skal bruge disse oplysninger i senere trin.

## <a name="country-specific-configuration-of-the-application-setup-for-the-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Landespecifik konfiguration af programopsætningen til funktionen Fransk Chorus Pro-afsendelse (FR) for elektronisk fakturering

Nogle af parametrene fra den elektroniske faktureringsfunktion **Fransk Chorus Pro-afsendelse (FR)** er udgivet med standardværdier. Før du udruller funktionen elektronisk fakturering til servicemiljøet, skal du gennemse og om nødvendigt opdatere standardværdierne, så de afspejler din forretningsdrift.

1. Opret hemmeligheder og reference til dem i Azure Key Vault. Yderligere oplysninger finder du i [Kundecertifikater og -hemmeligheder](e-invoicing-customer-certificates-secrets.md).
2. Importér den seneste version af globaliseringsfunktionen **Fransk Chorus Pro-afsendelse (FR)** som beskrevet i [Importfunktioner fra det globale lager](e-invoicing-import-feature-global-repository.md).
3. Opret en kopi af den importerede globaliseringsfunktion, og vælg konfigurationsudbyder. Du kan finde flere oplysninger i [Oprette en globaliseringsfunktion](e-invoicing-create-new-globalization-feature.md).
4. Kontroller, at **Kladde**-versionen er valgt under fanen **Versioner**.
5. Vælg funktionsopsætningen **Afledt UBL-salgsfaktura** i gitteret på fanen **Opsætninger**.
6. Vælg **Rediger**, og gå derefter til fanen **Behandling af pipeline** i sektionen **Behandling af pipeline**, og vælg **(Forhåndsversion) Integrer med fransk Chorus Pro** med handlingsnavnet **Fransk Chorus Pro-afsendelse**.
7. Vælg det hemmelige navn, du oprettede for klient-id'et i Key Vault, i feltet **Navn på hemmelighed for klient-id** i sektionen **Parametre**.
8. Vælg det hemmelige navn, du oprettede for klienthemmelighed i Key Vault, i feltet **Navn på hemmelighed for klienthemmelighed**.
9. Vælg det hemmelige navn, du oprettede for teknisk kontologon i Key Vault, i feltet **Navn på teknisk logonhemmelighed**.
10. Vælg det hemmelige navn, du oprettede for teknisk kontoadgangskode i Key Vault, i feltet **Navn på teknisk adgangskodehemmelighed**.
11. Under fanen **Behandling af pipeline** i sektionen **Behandling af pipeline** skal du vælge **Integrer med fransk Chorus Pro** med handlingsnavnet **Fransk Chorus Pro-anmodningsstatus**.
12. Vælg det hemmelige navn, du oprettede for klient-id'et i Key Vault, i feltet **Navn på hemmelighed for klient-id** i sektionen **Parametre**.
13. Vælg det hemmelige navn, du oprettede for klienthemmelighed i Key Vault, i feltet **Navn på hemmelighed for klienthemmelighed**.
14. Vælg det hemmelige navn, du oprettede for teknisk kontologon i Key Vault, i feltet **Navn på teknisk logonhemmelighed**.
15. Vælg det hemmelige navn, du oprettede for teknisk kontoadgangskode i Key Vault, i feltet **Navn på teknisk adgangskodehemmelighed**.
16. Vælg **Gem**, og luk derefter siden.
17. Gentag trin 6 til 16 for funktionsopsætningen **Afledt UBL-projektfaktura**, **Afledt UBL-salgskreditnota** og **Afledt UBL-projektkreditnota**.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Tilføjelsesprogrammet til oversigt over elektronisk fakturering](e-invoicing-service-overview.md)
- [Introduktion til tilføjelsesprogrammet til serviceadministration i elektronisk fakturering](e-invoicing-get-started-service-administration.md)
- [Introduktion til tilføjelsesprogrammet til elektronisk fakturering](e-invoicing-get-started.md)
