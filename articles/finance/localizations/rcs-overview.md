---
title: Regulatory Configuration Service
description: Dette emne indeholder en oversigt over funktionerne i Regulatory Configuration Service (RCS) og forklarer, hvordan du får adgang til tjenesten.
author: JaneA07
ms.date: 06/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 312fe318009a05de63fdba6aa8e6431836993957
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345167"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

RCS (Regulatory Configuration Service) er en enkeltstående designer- og livscyklusstyringstjeneste for funktionalitet til globalisering uden kode/lidt kode. Med RCS kan globaliseringsinteressenter udvide og tilpasse vigtige globaliseringsområder for moms, e-fakturering, lovpligtig rapportering, bank- og forretningsdokumenter uden at skulle involvere udviklere. Denne tilgang til globalisering uden kode/lidt kode gør det nemmere, hurtigere og mere omkostningseffektivt at oprette eller udvide globalisering.

RCS har følgende egenskaber:

- Understøttelse af alle funktioner, der leveres af Elektronisk rapportering (ER).
- En forudsætning for at kunne konfigurere nye mikrotjenester til globalisering.
- Understøttelse af elektronisk fakturering. Du kan finde flere oplysninger i [Elektronisk fakturering](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).
- Understøtter momsberegning. Du kan finde flere oplysninger under [Momstjeneste](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).
- Understøttelse af ny funktion til globalisering, hvilket forenkler livscyklusstyringen af funktioner for flere komponenter og giver en ekstra egenskab til at konfigurere handlinger og oprette funktionsparametre. Yderligere oplysninger finder du i [Regulatory Configuration Service – forenklet styring af globaliseringsfunktionen til globaliseringstjenester](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).
- Understøttelse af centraliseret publicering, lagring og deling af brugerdefinerede konfigurationer i det globale lager for at forenkle konfigurationsstyring uden at kræve brug af Microsoft Dynamics Lifecycle Services (LCS).

## <a name="access-rcs"></a>Adgang til RCS

Du kan tilmelde dig eller logge på RCS fra siden [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).

![RCS-tilmelding og logon.](media/202103_RCS%20Marketing%20page_updated_1.jpg)

På siden **Regulatory Configuration Service** skal du gennemgå og acceptere de supplerende vilkår og betingelser for brug af tjenesten og derefter vælge en af følgende knapper:

- **Tilmeld**, hvis du er førstegangsbruger af tjenesten, og du bruger en virksomheds mailadresse til at klargøre din organisations servicemiljø
- **Log på**, hvis du tidligere har tilmeldt dig tjenesten, og du vil have adgang til dit organisationsmiljø

> [!NOTE] 
> Når du har tilmeldt dig, anbefales du at føje endnu en SysAdmin-bruger til RCS-miljøet. Denne bruger klargøres som medadministrator for miljøet. På denne måde bliver det lettere at få adgang til RCS-miljøet, da rollen SysAdmin er at administrere brugere for det pågældende miljø. Du kan tilføje brugere ved hjælp af **RCS-arbejdsområde > Systemadministration**.

## <a name="regional-availability"></a>Regional tilgængelighed

RCS er generelt tilgængelig i følgende områder:

- United States
- Indien
- Frankrig
- Europa

Du kan se en komplet liste over områder i [Dynamics 365 og Power Platform : Tilgængelighed, dataplacering, sprog og lokalisering](https://aka.ms/dynamics_365_international_availability_deck).

## <a name="rcs-default-company"></a>RCS-standardfirma

Funktioner for designtid, der bruges i RCS, deles på tværs af alle firmaer. Der findes ingen firmaspecifikke funktioner. Vi anbefaler derfor, at du bruger ét firma, **DAT**, sammen med dit RCS-miljø.

I nogle scenarier kan det dog være en god ide at bruge parametre, der er relateret til en bestemt juridisk enhed, i ER-formater. Kun i disse scenarier skal du bruge standardfirmaskifte. Du kan se et eksempel i [Konfigurere ER-format til at bruge de parametre, der er angivet for den enkelte juridiske enhed](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).

## <a name="related-rcs-documentation"></a>Relateret RCS-dokumentation

Du kan finde flere oplysninger om relaterede komponenter i følgende emner:

- **RCS:**

    - [Oprette ER-konfigurationer i RCS og overføre dem til det globale lager](rcs-global-repo-upload.md)

- **Globalt lager:**

    - [Oprette ER-konfiguration og uploade til globalt lager](rcs-global-repo-upload.md)
    - [Dele konfiguration i globalt lager](rcs-global-repo-share-configuration.md)
    - [Udvidet filtrering i globalt lager](enhanced-filtering-global-repo.md)
    - [Hente ER-konfigurationer fra globalt lager](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [Afbryde konfigurationer i globalt lager](discontinuing-configurations-rcs-global-repo.md)
    - [RCS (Regulatory Configuration Service) – Lifecycle Services (LCS)-lagerudfasning](rcs-lcs-repo-dep-faq.md)

- **Globaliseringsfunktion:**

    - [Regulatory Configuration Service (RCS) – globaliseringsfunktion](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a>Fejlfinding af RCS-tilmelding

Når du tilmelder dig RCS fra tjenestesiden, kan der opstå et problem, der er relateret til Azure Active Directory (Azure AD). Den fejlmeddelelse, du modtager, angiver, at tilmelding til RCS i øjeblikket er slået fra og skal være slået til, før du kan fuldføre tilmeldingsprocessen.

![Fejlmeddelelse om RCS-tilmelding.](media/01_RCSSignUpError.jpg)

Problemet opstår, fordi du er spærret for tilmelding til ad hoc-abonnementer, og egenskaben `AllowAdHocSubscriptions` skal aktiveres i din lejer. 

- Hvis it-afdelingen administrerer din organisations Azure-lejere, skal du kontakte den pågældende afdeling for at rapportere problemet.
- Hvis du er ansvarlig for at administrere dine Azure-lejere, kan du løse problemerne ved at følge trinnene i [Hvad er tilmelding til selvbetjening i Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).
