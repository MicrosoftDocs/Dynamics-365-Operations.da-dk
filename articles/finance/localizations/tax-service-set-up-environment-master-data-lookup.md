---
title: Aktivere masterdataopslag til konfiguration af momsberegning
description: Denne artikel indeholder en forklaring på, hvordan du kan konfigurere og aktivere funktionen til opslag af masterdata for momsberegning.
author: kai-cloud
ms.date: 07/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3642bb88d5b0570014513b64eef5fdab6d1ee9d3
ms.sourcegitcommit: 5b721f6fc1ba4350b5bd0eae457f71d80246db42
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/20/2022
ms.locfileid: "9181118"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Aktivere masterdataopslag til konfiguration af momsberegning 

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en forklaring på, hvordan du kan konfigurere og aktivere funktionen til opslag af masterdata for momsberegning. Der findes en rullemenu til valg af værdier i momsberegningskonfigurationen for felter som **Juridisk enhed**, **Kreditorkonto**, **Varekode** og **Leveringsbetingelse**. Disse værdier kommer fra det tilsluttede Microsoft Dynamics 365 Finance-miljø via Microsoft Dataverse-datakilde.

> [!NOTE] 
> Funktionaliteten for opslag efter stamdata for momsberegning er valgfri. Du kan springe følgende trin over, hvis du deaktiverer funktionen **Understøttelse af Dataverse-datakilder i momstjenesten** i RCS (Regulatory Configuration Service). Men i dette tilfælde er rullelisten ikke tilgængelig i konfigurationen af momsberegningen.

Hvis du vil aktivere rullelisten i funktionsversionen til konfiguration af Momsberegning, skal du udføre følgende trin.

1. [Aktiver Microsoft Power Platform-integration og åbn Dataverse-miljøet.](#enable)
2. [Installer virtuelle finans og drift-enheder](#install)
3. [Registrere en Azure Active Directory (Azure AD) applikation.](#register)
4. [Giv apptilladelser i programmer til finans og drift.](#grant)
5. [Konfigurere datakilden til den virtuelle enhed.](#configure)
6. [Aktivere virtuelle objekter i Dataverse.](#virtual)
7. [Konfigurer det tilknyttede program til momsberegning.](#set-up)
8. [Importér og konfigurer Dataverse -konfigurationsmodeltilknytningen](#import)

## <a name="enable-microsoft-power-platform-integration-and-open-the-dataverse-environment"></a><a name='enable'></a>Aktiver Microsoft Power Platform-integration og åbn Dataverse-miljøet.

Integrationen af programmer til finans og drift med Microsoft Power Platform kan aktiveres, når du opretter et nyt økonomi- og operationsappmiljø i Microsoft Dynamics Lifecycle Services (LCS). Du kan finde flere oplysninger under [Microsoft Power Platform integration - Oversigt over tilføjelsesprogrammer](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Når du har fuldført trinnet, vises navnet på et Microsoft Power Platform-miljø i sektionen **Power Platform-integration**.

1. I finans og drift-miljøet i **Power Platform-integration** skal du finde og notere værdien for det sammenkædede miljø i **Miljønavn** i LCS.

    [![Miljønavn-værdi](./media/tcs-dataverse-master-data-lookup-1.png)](./media/tcs-dataverse-master-data-lookup-1.png)

2. I [Power Platform Administration](https://admin.powerplatform.microsoft.com/environments) på fanen **Miljøer** skal du vælge det miljø, der svarer til den værdi for **miljønavnet**, du har notat om.
3. Find **URL-værdien for miljøet** på siden **Detaljer** i Dataverse-miljøet. Noter denne værdi, fordi du skal bruge den i [Trin 7. Konfigurer det tilknyttede program til momsberegning](#set-up).
4. Kontroller, at du kan åbne Dataverse-miljøet i browseren ved at vælge **URL-værdien for miljøet**.

    [![Dataverse-miljøside.](./media/tcs-dataverse-master-data-lookup-2.png)](./media/tcs-dataverse-master-data-lookup-2.png)

    > [!NOTE]
    > Hold Dataverse-miljøet åbent i din browser. Du skal bruge den i [Trin 5. Konfigurer datakilden for den virtuelle enhed](#configure).

Du kan finde flere oplysninger under [Aktivere Microsoft Power Platform-integration](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

## <a name="install-finance-and-operations-virtual-entities"></a><a name='install'></a>Installer virtuelle finans og drift-enheder

Løsningen Dataverse til virtuelle finans og drift-enheder skal installeres fra den Microsoft AppSource-virtuelle enhedsløsning.

1. I AppSource finde [Virtuelle finans og drift-enheder](https://appsource.microsoft.com/product/dynamics-365/mscrm.finance_and_operations_virtual_entity).
2. Vælg **Start nu**.
3. Angiv den værdi for det **miljønavn**, du noterede tidligere, i feltet **Vælg miljø**.
4. Marker afkrydsningsfelterne, og vælg derefter **Installer**.

Når installationen er fuldført, kan du finde programmet **Finans og drift-virtuel enhed** i [Power Platform Administration](https://admin.powerplatform.microsoft.com/), under **Ressourcer** \> **Dynamics 365**.

Du kan finde flere oplysninger i [Hent den virtuelle enhedsløsning](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution).

## <a name="register-an-azure-ad-application"></a><a name='register'></a>Registrere en Azure AD-applikation

Du skal registrere en Azure AD-applikation på samme lejer som programmer til finans og drift, så de kan kaldes af Dataverse.

1. I [Azure-portalen](https://portal.azure.com) skal du gå til **Azure Active Directory \> App-registreringer**.
2. Vælg **Ny registrering**, og angiv følgende oplysninger:

    - Angiv et entydigt navn under **Navn**.
    - **Kontotype** – Angiv et **vilkårligt Azure AD-bibliotek** (med en enkelt lejer eller flere lejere).
    - **Omdiriger URI** - Lad feltet være tomt.

3. Vælg **Registrer**.
4. Notér værdien i feltet **Applikations-id (klient)**, da du skal bruge den senere.

    [![Azure AD Azure (klient-id)-værdi.](./media/tcs-dataverse-master-data-lookup-3.png)](./media/tcs-dataverse-master-data-lookup-3.png)

5. Opret en symmetrisk nøgle til applikationen.
6. I den nye ansøgning skal du vælge **Certifikater og hemmeligheder**.
7. Vælg **Ny klient-hemmelighed**.
8. Angiv en beskrivelse, vælg en udløbsdato, og vælg derefter **Gem**. Der oprettes og vises en nøgle. Kopier værdien til senere brug.

Du kan finde flere oplysninger under [Registrer Azure AD-applikation](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#register-the-app-in-the-azure-portal).

## <a name="grant-app-permissions-in-finance-and-operations-apps"></a><a name='grant'></a>Giv app-tilladelser i programmer til finans og drift

Dataverse bruger det Azure AD-program, du har oprettet til at ringe til programmer til finans og drift. Derfor skal der være tillid til applikationen fra programmer til finans og drift og skal kunne tilknyttes en brugerkonto, der har de relevante rettigheder. I programmer til finans og drift skal du oprette en særlig servicebruger, der **kun** har rettigheder til den virtuelle enhedsfunktionalitet. Denne servicebruger må ikke have andre rettigheder. Når du har fuldført dette trin, vil alle applikationer, der har den hemmeligheden til den Azure AD-applikation, du har oprettet, kunne ringe til programmer til finans og drift-miljø og få adgang til den virtuelle enhedsfunktionalitet.

1. Gå til **Systemadministration** \> **Brugere** \> **Brugere** i dit miljø.
2. Vælg **Ny** for at tilføje en ny bruger, og angiv følgende feltoplysninger:

    - **Bruger-id** – Angiv **dataverseintegration** eller en anden værdi.
    - **Brugernavn** – Angiv **dataverse-integration** eller en anden værdi.
    - **Udbyder** - Angiv dette felt til **NonAAD**.
    - **E-mail** – Angiv **dataverse-integration** eller en anden værdi. (Værdien behøver ikke at være en gyldig e-mail-konto).

3. Tildel sikkerhedsrollen **Virtuel CDS-enhedsprogram** til brugeren.
4. Fjern alle andre roller, herunder **systembruger**.
5. Gå til **Systemadministration** \> **Opsætning** \> **Azure Active Directory-applikationer** for at registrere Dataverse. 
6. Tilføj en række, og angiv derefter i feltet **Klient-id** den værdi for **applikations-id**, som du noterede tidligere.
7. Indtast et navn i feltet **Navn**. Skriv eksempelvis **Dataverse-integration**.
8. Vælg det bruger-id, du lige har oprettet, i feltet **Bruger-id**.

Du kan finde flere oplysninger under [Tildel app-tilladelser i programmer til finans og drift](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#grant-app-permissions-in-finance-and-operations-apps).

## <a name="configure-the-virtual-entity-data-source"></a><a name='configure'></a>Konfigurere datakilden til den virtuelle enhed

Du skal angive til Dataverse den programforekomst til finans og drift, du vil oprette forbindelse til.

1. Miljøet Dataverse bør stadig være åbent i din browser fra [Trin 1. Aktiver Microsoft Power Platform-integration og åbn Dataverse-miljøet](#enable). Vælg knappen Indstillinger (tandhjulsymbolet) øverst til højre, og vælg derefter **Avancerede indstillinger**.

    [![Åbner Avancerede indstillinger i Dataverse-miljøet.](./media/tcs-dataverse-master-data-lookup-4.png)](./media/tcs-dataverse-master-data-lookup-4.png)

2. Vælg **Administration** i rullemenuen **Indstillinger**.

    [![Administration.](./media/tcs-dataverse-master-data-lookup-5.png)](./media/tcs-dataverse-master-data-lookup-5.png)

3. Vælg **datakilder for virtuel enhed**.

    [![Datakilder for virtuel enhed.](./media/tcs-dataverse-master-data-lookup-6.png)](./media/tcs-dataverse-master-data-lookup-6.png)

4. Vælg den datakilde, der har navnet **Finance and Operations**.

    [![Datakilde til finans og drift](./media/tcs-dataverse-master-data-lookup-7.png)](./media/tcs-dataverse-master-data-lookup-7.png)

5. Angiv følgende oplysninger fra tidligere trin:

    - **URL-adressedestination** – Angiv den URL-adresse, hvor du kan få adgang til programmer til finans og drift.
    - **URL-adresse til OAuth** – Angiv `https://login.windows.net/`.
    - **Lejer-id** – Angiv din lejer. Denne værdi kan være domænenavnet på firmaets e-mail (f.eks. contoso.com).
    - **AAD-applikations-id** - Angiv den **Applikation (klient)-id**-værdi, du har oprettet tidligere.
    - **AAD-applikationshemmelighed** – Angiv den hemmelighed, der blev genereret tidligere.
    - **AAD-ressource** – Angiv **00000015-0000-0000-c000-000000000000**. Denne værdi er det Azure AD-program , der repræsenterer programmer til finans og drift. Det skal altid være denne samme værdi.

6. Gem ændringerne.
7. Luk siden for at vende tilbage til **Administration**, hvor du starter [Trin 6. Aktivér virtuelle Dataverse-enheder](#virtual).

    [![Luk enheden for redigering.](./media/tcs-dataverse-master-data-lookup-8.png)](./media/tcs-dataverse-master-data-lookup-8.png)

Du kan finde flere oplysninger i [Konfigurer den virtuelle enhedsdatakilde](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#configure-the-virtual-entity-data-source).

## <a name="enable-dataverse-virtual-entities"></a><a name='virtual'></a>Aktiver virtuelle Dataverse-enheder

Synligheden af virtuelle enheder fra programmer til finans og drift skal angives til **Ja**, før de kan bruges af konfigurationen til Momsberegning.

> [!NOTE]
> Du kan springe dette trin over ved at aktivere de virtuelle enheder, der vedrører momsberegning, med blot et klik i [Trin 8. Konfigurer det tilknyttede program til momsberegning](#import). Det anbefales dog, at du aktiverer mindst én virtuel enhed manuelt for at angive, at forbindelsen mellem programmer til finans og drift og Dataverse er godt fastlagt.

1. I dit Dataverse-miljø skal du vælge **Administration**, vælge filterknappen (tragtsymbolet) øverst til højre på siden Administration.

    [![Filterknap.](./media/tcs-dataverse-master-data-lookup-9.png)](./media/tcs-dataverse-master-data-lookup-9.png)

2. Vælg **Tilgængelige enheder til finans og drift** i feltet **Søg efter** i vinduet **Avanceret søgning**.
3. Tilføj følgende regel: **Navn** – **Indeholder** – **CompanyInfoEntity**. Vælg **Resultater**.

    [![Vindue til avanceret søgning.](./media/tcs-dataverse-master-data-lookup-10.png)](./media/tcs-dataverse-master-data-lookup-10.png)

4. Vælg **CompanyInfoEntity** i søgeresultaterne, marker afkrydsningsfeltet **Synlig**, og vælg derefter **Gem**.

    [![Angive synlighed af enheden.](./media/tcs-dataverse-master-data-lookup-11.png)](./media/tcs-dataverse-master-data-lookup-11.png)

5. Gentag de foregående trin for følgende enheder, der henvises til i konfigurationen af Momsberegning:

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity
    - InventOperationalSiteV2Entity
    - TaxExemptCodeEntity
    - InventWarehouseEntity

    > [!NOTE]
    > Det er kun de første 5.000 poster i en enhed, der kan hentes af Dataverse og gøres tilgængelige på rullelisten til konfiguration af momsberegning.

Du kan finde flere oplysninger i [Aktivere virtuelle Microsoft Dataverse-enheder](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="set-up-the-connected-application-for-tax-calculation"></a><a name='set-up'></a>Konfigurer det tilknyttede program til momsberegning

1. I RCS skal du åbne arbejdsområdet **Funktionsstyring** og aktivere følgende funktioner:

    - Understøttelse af Dataverse-datakilder for elektronisk rapportering
    - Understøttelse af Dataverse-datakilder i momstjenesten
    - Globaliseringsfunktioner

2. Gå til **Elektronisk rapportering**, og vælg **Tilsluttede applikationer** i sektionen **Relaterede links**.

    [![Tilsluttede applikationer.](./media/tcs-dataverse-master-data-lookup-12.png)](./media/tcs-dataverse-master-data-lookup-12.png)

3. Vælg **Ny** for at tilføje en post, og angiv følgende oplysninger.

    - **Navn** – Angiv et navn.
    - **Type** – Vælg **Dataverse**.
    - **Applikation** – Angiv dit Dataverse-miljøs **Miljø-URL-adresse**, som du noterede i [Trin 1. Aktivér Microsoft Power Platform-integration, og åbn Dataverse-miljøet](#enable).
    - **Lejer** – Angiv din lejer.
    - **Brugerdefineret URL-adresse** – Angiv din Dataverse URL, og tilføj **/api/data/v9.1**.

4. Vælg **Kontroller forbindelsen**, og vælg derefter **Klik her i den dialogboks, der vises, for at oprette forbindelse til den valgte fjernapplikation**.

    [![Kontrollere forbindelsen.](./media/tcs-dataverse-master-data-lookup-13.png)](./media/tcs-dataverse-master-data-lookup-13.png)
5. Sørg for, at du får modtager "Succes" meddelelse, der angiver, at forbindelsen blev oprettet.

    [![Meddelelse om fuldført.](./media/tcs-dataverse-master-data-lookup-14.png)](./media/tcs-dataverse-master-data-lookup-14.png)

## <a name="import-and-set-up-the-dataverse-model-mapping-configuration"></a><a name='import'></a>Importér og konfigurer Dataverse-konfigurationsmodeltilknytningen

Microsoft leverer standardkonfigurationer til modeltilknytning af enheder fra programmer for finans og drift til momsberegning.

1. Gå til **Elektronisk rapportering** i RCS.
2. I sektionen **Konfigurationsudbydere** i feltet for **Microsoft**-udbyder skal du vælge **Lagre**.

    [![Lagre.](./media/tcs-dataverse-master-data-lookup-15.png)](./media/tcs-dataverse-master-data-lookup-15.png)

3. Vælg **Globalt konfigurationslager**, og vælg derefter **Åbn**.
4. Under **Momsdatamodel** \> **Datamodel til momsberegning** skal du vælge konfigurationen **Dataverse-modeltilknytning**.
5. I oversigtspanelet **Versioner** skal du vælge en version, der svarer til din version af programmer til finans og drift, og vælg derefter **Import**.

    [![Importerer konfigurationen Dataverse-modeltilknytning.](./media/tcs-dataverse-master-data-lookup-16.png)](./media/tcs-dataverse-master-data-lookup-16.png)

    > [!IMPORTANT]
    > Konfigurationen **Dataverse-modeltilknytning** gælder kun i sin højeste importerede version. Derfor bør du ikke importere en version af konfigurationen **Dataverse-modeltilknytning**, som er højere end versionen af den momsberegningskonfiguration, du vil implementere. Hvis du f.eks. planlægger at importere version 40.50.225 af konfigurationen til momsberegning, skal du kun importere version 40.50.13 fra konfigurationen **Dataverse-modeltilknytning**. Du skal ikke importere version 40.54.14. Ellers vil datamodellen ikke stemme overens i konfigurationen.

6. Gå tilbage til **Elektronisk rapportering** og vælg feltet **Momskonfigurationer**.
7. Vælg den importerede **Dataverse-modeltilknytning**-konfiguration, og vælg derefter **Rediger**.
8. Vælg **Ja** i indstillingen **Standard for modeltilknytning**.
9. I feltet **Tilknyttet applikation** skal du vælge den tilknyttede applikation, du konfigurerede i [Trin 7. Konfigurer den tilknyttede applikation til momsberegning](#set-up).
10. Angiv indstillingen **Sæt synlighed for virtuelle tabeller** til **Ja** for at angive, at alle momsberegningsrelaterede virtuelle enheder skal kunne ses.

Du har nu fuldført opsætningen af opslagsfunktionen til stamdata. En rulleliste til felter som f.eks. **Juridisk enhed**, **Kreditorkonto**, **Varekode** og **Leveringsbetingelser** fra Dynamics 365 Finance aktiveres nu i opsætningen **funktionsversionen til momsberegning**.

[![Rullelisten Juridisk enhed.](./media/tcs-dataverse-master-data-lookup-17.png)](./media/tcs-dataverse-master-data-lookup-17.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
