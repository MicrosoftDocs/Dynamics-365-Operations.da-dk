---
title: Elektronisk fakturering for Egypten
description: Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med elektronisk fakturering for Egypten i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6fe1dd4254db8b390c17558320a6eaff2b0dcd19
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371350"
---
# <a name="electronic-invoicing-for-egypt"></a>Elektronisk fakturering for Egypten

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med elektronisk fakturering for Egypten. Det fører dig gennem de konfigurationstrin, der er lande-/områdeafhængige i Regulatory Configuration Service (RCS). Disse trin supplerer de trin, der er beskrevet i [Konfigurere elektronisk fakturering](e-invoicing-set-up-overview.md).

## <a name="prerequisites"></a>Forudsætninger

Før du indleder procedurerne i dette emne, skal du opfylde følgende forudsætninger:

- Bliver fortrolig med elektronisk fakturering, som den beskrives i [Oversigt over elektronisk fakturering](e-invoicing-service-overview.md).
- Tilmeld dig RCS, og konfigurer elektronisk fakturering. Du kan finde flere oplysninger under følgende emner:

    - [Tilmelde og installere elektronisk faktureringstjeneste](e-invoicing-sign-up-install.md)
    - [Konfigurere Azure-ressourcer til elektronisk fakturering](e-invoicing-set-up-azure-resources.md)
    - [Installere tilføjelsesprogrammet til mikroservices i Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md)
    
- Aktiver integrationen mellem Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management-programmet og tjenesten til elektronisk fakturering som beskrevet i [Aktivere og konfigurere integration med elektronisk fakturering](e-invoicing-activate-setup-integration.md).
- Opret et digitalt certifikats hemmelighed i Azure Key Vault, og konfigurer den som beskrevet i [Kundecertifikater og -hemmeligheder](e-invoicing-customer-certificates-secrets.md). Til testformål leverer de egyptiske skattemyndigheder specifikke test digitale certifikater, som kun skal bruges under test- og løsningsvalideringsfaser. Du kan finde flere oplysninger ved at gå til webstedet for de egyptiske skattemyndigheder ved hjælp af linket i [Egyptisk e-fakturering-SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-feature"></a>Den landespecifikke konfiguration til den egyptiske elektroniske faktura (EG)

Nogle af parametrene fra den elektroniske faktureringsfunktion **Egyptisk elektronisk faktura (EG)** er udgivet med standardværdier. Før du udruller funktionen Elektronisk fakturering til servicemiljøet, skal du gennemse og om nødvendigt opdatere standardværdierne, så de afspejler din forretningsdrift.

1. Importer den seneste version af globaliseringsfunktionen **Egyptisk elektronisk faktura (EG)** som beskrevet i [Importfunktioner fra det globale lager](e-invoicing-import-feature-global-repository.md).
2. Opret en kopi af den importerede funktion til globalisering, og vælg din konfigurationsudbyder til den som beskrevet i [Oprette en globaliseringsfunktion](e-invoicing-create-new-globalization-feature.md).
3. Kontroller, at **Kladde**-versionen er valgt under fanen **Versioner**.
4. Vælg funktionsopsætningen **Afledt salgsfaktura** i gitteret på fanen **Opsætninger**.
5. Vælg **Rediger**.
6. Vælg **Underskriv json-dokument for egyptiske momsmyndigheder** i sektionen **Behandlingspipeline** under fanen **Behandlingspipeline**.
7. Vælg **Certifikatnavn** i afsnittet **Parametre**, og vælg derefter navnet på det digitale certifikat, du har oprettet.
8. I sektionen **Behandlingspipeline** skal du vælge **Integrer med egyptisk ETA-tjeneste**. Gentag dette trin for de to forekomster af denne handling.
9. Vælg **URL-adressen til webtjenesten** og **URL-adressen til login på tjeneste** under **Parametre**. Gennemgå derefter URL-parametrene. Gå til de egyptiske momsmyndigheders websted for at finde URL-adressen til test og produktion ved hjælp af linket i [Egyptisk e-fakturering-SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).
10. Vælg **Gem**, og luk siden.
11. Gentag trin 4 til 10 for opsætningen af funktionen **Afledt projektfaktura**.

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-application-setup"></a>Den landespecifikke konfiguration til programopsætningen af den egyptiske elektroniske faktura (EG)

Der er parametre, der skal konfigureres i dit Finans- eller Supply Chain Management-miljø. Du kan fuldføre opsætningen et af to steder:

- Direkte i Finans- eller Supply Chain Management-miljøet. Du kan finde flere oplysninger i [Konfigurere parametre til elektronisk fakturering](e-invoicing-set-up-parameters.md).
- I RCS. Inden for funktionsopsætningen af elektronisk fakturering kan du definere alle parametre og derefter udrulle dem direkte til dit Finans- eller Supply Chain Management-miljø, når du udruller funktionen til elektronisk fakturering.

I begge tilfælde er parametrene ens. Hvis du konfigurerer din første funktion i tjenesten til elektronisk fakturering, anbefales det, at du følger disse trin for at konfigurere parametrene i RCS og derefter udruller dem til det tilknyttede program.

> [!NOTE]
> Nogle funktionsversioner til elektronisk fakturering kan indeholde et foruddefineret sæt programspecifikke parametre til Finans eller Supply Chain Management. I dette tilfælde skal du kontrollere, at dataene er korrekte. Ellers skal du angive parametrene manuelt.

1. Find kopien af den **Egyptisk elektronisk faktura (EG)**-globaliseringsfunktion, som du har oprettet.
2. Kontroller, at **Kladde**-versionen er valgt under fanen **Versioner**.
3. Under fanen **Opsætning af applikation** skal du vælge **Opsætninger**.
4. I feltet **Tilsluttede programmer** skal du vælge det program, hvor du vil udrulle parametrene.
5. Vælg **Tilføj** for at oprette en post på siden **Elektroniske dokumenttyper**.
6. Tilføj **CustInvoiceJour** i feltet **Tabelnavn**.
7. Tilføj en reference til tilknytningsnavnet **Debitorfakturakontekst** i feltet **Kontekst**. Konfigurationen er **Kontekstmodel for debitorfaktura**.
8. Tilføj en reference til tilknytningsnavnet **Debitorfaktura** i feltet **Tilknytning af elektronisk dokument**. Konfigurationen er **Fakturamodeltilknytning**.
9. Vælg **Gem**.
10. På siden **Svartyper** skal du vælge **Tilføj**.
11. I feltet **Svartype** skal du angive **Svar**.
12. Angiv **Foretag behandling af svar** i feltet **Beskrivelse**.
13. Vælg **Afventer** i feltet **Indsendelsesstatus**.
14. Vælg **Import af svarmeddelelse** i feltet **Modeltilknytning**. Konfigurationen er **Import af svarmeddelelse for Egypten (EG)**.
15. Vælg **Gem**.
16. Vælg **Tilføj**.
17. I feltet **Svartype** skal du angive **ResponseData**.
18. Angiv **Foretag behandling af svardata** i feltet **Beskrivelse**.
19. Vælg **Afventer** i feltet **Indsendelsesstatus**.
20. Vælg **SalesInvoiceHeaderV2Entity** i feltet **Navn på dataenhed**.
21. Vælg **Import af svardata** i feltet **Modeltilknytning**. Konfigurationen er **Importformat af svardata for Egypten (EG)**.
22. Vælg **Gem**, og luk siden.
23. Luk siden.

Hvis du vil udrulle en funktion til servicemiljøet og en programopsætning til det tilknyttede program Finans eller Supply Chain Management, skal du se [Fuldføre, publicere og implementere en globaliseringsfunktion](e-invoicing-complete-publish-deploy-globalization-feature.md)

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger

Aktivering af funktionen **Egyptisk elektronisk faktura (EG)** kræver måske, at der sendes begrænsede data. Disse data omfatter organisationens momsregistrerings-id. Disse data vil blive overført til tredjepartsorganer, der er godkendt af skattemyndighederne, med det formål at sende elektroniske fakturaer til denne skattemyndighed i det foruddefinerede format, der kræves til integration med myndighedernes webtjeneste. En administrator kan aktivere og deaktivere funktionen ved at gå til **Organisationsadministration** \> **Konfiguration** \> **Parametre for elektroniske dokumenter**. Under fanen **Funktioner** skal du markere den række, der indeholder funktionen **Egyptisk elektronisk faktura (EG)** og derefter foretage de relevante valg. Data, der importeres fra eksterne systemer til denne Dynamics 365-onlinetjeneste, er underlagt vores [erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=512132). Yderligere oplysninger finder du i sektionen "Erklæring om beskyttelse af personlige oplysninger" i den lande- eller områdespecifikke dokumentation til funktionen.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk fakturering](e-invoicing-service-overview.md)
- [Start her med serviceadministration i elektronisk fakturering](e-invoicing-get-started-service-administration.md)
- [Start her med elektronisk fakturering](e-invoicing-get-started.md)
- [Elektroniske fakturaer til kunder i Egypten](emea-egy-e-invoices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
