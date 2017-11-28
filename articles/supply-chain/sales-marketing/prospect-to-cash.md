---
title: Kundeemne til kontanter
description: "Emnet indeholder en oversigt over kundeemne til kontanter-løsningen mellem Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 2accf77c5241adff7ad1648737dde451153fde46
ms.contentlocale: da-dk
ms.lasthandoff: 11/14/2017

---

# <a name="prospect-to-cash"></a>Kundeemne til kontanter  

[!include[banner](../includes/banner.md)]

Kundeemne til kontanter-løsningen bruger [Dataintegration](/common-data-service/entity-reference/dynamics-365-integration) til at synkronisere data på tværs af Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales-forekomster via Common Data Service (CDS). Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Finance and Operations og Sales. Når dataene flyder mellem Finance and Operations og Sales, kan du udføre salgs- og marketingaktiviteter i Sales og håndtere ordreopfyldelsen med lagerstyring i Finance and Operations. 

Denne løsning giver integration på følgende områder: 

-   [Vedligehold konti i Sales, og synkroniser dem med Finance and Operations](accounts-template-mapping.md)
-   [Vedligehold kontakter i Sales, og synkroniser dem med Finance and Operations](contacts-template-mapping.md)
-   [Vedligehold produkter kontakter i Finance and Operations, og synkroniser dem med Sales](products-template-mapping.md)
-   [Opret salgstilbud i Sales, og synkroniser dem med Finance and Operations](sales-quotation-template-mapping.md)
-   [Opret salgsordrer i Finance and Operations, og synkroniser dem med Sales](sales-order-template-mapping.md)
-   [Opret salgsfakturaer i Finance and Operations, og synkroniser dem med Sales](sales-invoice-template-mapping.md)

Denne løsning giver direkte synkronisering på følgende områder:

-   [Vedligehold konti i Sales, og synkroniser dem direkte fra Sales med Finance and Operations](accounts-template-mapping-direct.md)
-   [Vedligehold produkter i Finance and Operations, og synkroniser dem direkte med Sales](products-template-mapping-direct.md)
-   [Vedligehold kontakter i Sales, og synkroniser dem direkte med kontakter eller debitorer i Finance and Operations](contacts-template-mapping-direct.md)
-   [Synkroniser hoveder og linjer i salgstilbud direkte fra Sales med Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
-   [Opret salgsordrer i Finance and Operations, og synkroniser dem direkte med Sales](sales-order-template-mapping-direct.md)
-  [Synkroniser hoveder og linjer i salgsordrer direkte mellem Sales og Finance and Operations](sales-order-template-mapping-between-sales-fin.md)
-   [Synkroniser salgsordrer direkte mellem Sales og Finance and Operations](sales-order-template-mapping-direct-two-ways.md)
-   [Opret salgsfakturaer i Finance and Operations, og synkroniser dem direkte med Sales](sales-invoice-template-mapping-direct.md)


## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Systemkrav til Dynamics 365 for Finance and Operations, Enterprise Edition

Hvis du vil bruge løsningen Kundeemne til kontanter, skal du installere følgende:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) med platformsopdatering 8 (App 7.2.11792.56024 med Platform 7.0.4565.16212)

- Hotfixes til Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017).
        
    -  [KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) – Dette hotfix aktiverer understøttelse af synkronisering af salgsordrer med funktionen Dataintegration fra Sales til Finance and Operations, sammen med en række andre forbedringer.

    -  [KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - dette hotfix muliggør salgsordrelinjesynkronisering med funktionen Dataintegration fra Finance and Operations til Sales.
        
    -  [KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - dette hotfix muliggør salgsordresynkronisering med funktionen Dataintegration fra Finance and Operations til Sales.

**Bemærk**: Du behøver kun at installere KB4045570, fordi installationen omfatter ændringerne fra andre KB'er.
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a>Systemkravene til Dynamics 365 for Sales

Hvis du vil bruge løsningen Kundeemne til kontanter, skal du installere følgende:

- Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online.
- Løsningen Kundeemne til kontanter til Dynamics 365 for Sales, version 1.14.0.0 (v14) eller nyere.

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Installer løsningen Kundeemne til kontanter til Sales

- Hent [zip-filen med løsningspakken Kundeemne til kontanter til Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) på CustomerSource.

- Sørg for, at blokeringen af zip-filen ophæves, så du ikke får fejlmeddelelsen "Der blev ikke fundet nogen importpakker", når du installerer løsningspakken. Du ophæver blokeringen af filen på følgende måde:

    -  Højreklik på zip-filen.
    -  Vælg **Egenskaber** og derefter vælge **Ophæv blokering**. 

- Pak filen ud, og kør PackageDeployer.exe.

- Installer løsningen Kundeemne til kontanter i din Sales-forekomst.

    - Vælg installationstypen **Office 365**.
    - Vælg **Vis avancerede**.
    - For en hurtig installation, skal du vælge et **område**. Hvis du vælger **Ved ikke**, vil systemet søge efter alle områder, og det tager længere tid at installere.
    - Angiv **Brugernavn** og **Adgangskode** for en administrator, der har de nødvendige rettigheder til at installere.

