---
title: Kundeemne til kontanter
description: Dette emne indeholder en oversigt over Kundeemne til kontantløsningen mellem Dynamics 365 Supply Chain Management og Dynamics 365 Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: fb5abb983811ce736e3494bc85e8d9b23a2e373c
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814069"
---
# <a name="prospect-to-cash"></a>Kundeemne til kontanter

[!include [banner](../includes/banner.md)]

Kundeemne til kontantløsningen indeholder direkte synkronisering på tværs af Dynamics 365 Supply Chain Management og Dynamics 365 Sales. Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data til firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer. Når data flyder, kan du udføre salgs- og marketingaktiviteter i Sales, og du kan håndtere ordreopfyldelsen ved at bruge lagerstyring i Supply Chain Management. 

Du kan finde yderligere oplysninger om kundeemne til kontant-integration i denne korte YouTube-video [Kundeemne til kontant-integration](https://www.youtube.com/watch?v=AVV9x5x-XCg).

I den aktuelle version indeholder Kundeemne til kontanter-løsning følgende typer direkte synkronisering:

- [Synkronisere konti direkte fra Sales med kunder i Supply Chain Management](accounts-template-mapping-direct.md)
- [Synkronisere produkter direkte fra Supply Chain Management med produkter i Sales](products-template-mapping-direct.md)
- [Synkronisere kontakter direkte fra Sales med kontakter eller kunder i Supply Chain Management](contacts-template-mapping-direct.md)
- [Synkronisere salgstilbudshoveder og -linjer direkte fra Sales til Supply Chain Management](sales-quotation-template-mapping-sales-fin.md)
- [Synkronisering af salgsordrer direkte mellem Sales og Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)
- [Synkronisere salgsfakturahoveder og -linjer direkte fra Supply Chain Management til Sales](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a>Systemkrav til Supply Chain Management
Kundeemne til kontant-integration understøttes iå følgende versioner:

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (december 2017)

- Dynamics 365 for Finance and Operations, Enterprise Edition (december 2017) - programbuild 7.3.11971.56116 med platformsopdatering 12 (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017)

- Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) - med platformsopdatering 8 (programbuild 7.2.11792.56024 med platformsbuild 7.0.4565.16212).
- De følgende hotfixes er obligatoriske:

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – Dette hotfix muliggør salgsordresynkronisering fra Sales til Supply Chain Management via funktionen Dataintegration. Det indeholder også flere andre forbedringer.
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Dette hotfix muliggør synkronisering af salgsordrelinje fra Supply Chain Management til Sales via funktionen Dataintegration.
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Dette hotfix muliggør salgsordresynkronisering fra Supply Chain Management til Sales via funktionen Dataintegration.

    > [!NOTE]
    > Du behøver kun at installere KB4045570, fordi installationen omfatter ændringerne fra andre hotfixes. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations version 1611 (november 2016)

- Dynamics 365 for Finance and Operations version 1611 (november 2016) med platformsopdatering 8 eller nyere

- De følgende hotfixes er obligatoriske:

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** – Muliggør synkronisering af salgsordre med Dataintegrator fra Supply Chain Management til Sales. 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** – Muliggør synkronisering af salgsordrehoved og -linje med Dataintegrator fra Supply Chain Management til Sales.
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Understøttelse af Kundeemne til kontanter-integration via dataenheder er påkrævet.
    
    > [!NOTE]
    > Du skal udløse følgende batchjob fra formularen **SalesPopulateProspectToCash** efter installation af hotfixes. Denne formular er skjult, fordi du kun skal bruge den én gang. For at få adgang til formen skal du logge på miljøet og føje følgende til URL-adressen i din browseradresse: *&mi=action:SalesPopulateProspectToCash*, f.eks. `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. Når formularen åbnes, skal du klikke på OK. Dette udfylder et nyt **LineCreationSequnceNumber**-felt i tabellerne **SalesLine**, **SalesQuotationLine** og **CustInvoiceTrans** med entydige værdier og opdaterer produktlisten. Dette er nødvendigt, for at integration af Kundeemne til kontanter kan fungere.


## <a name="system-requirements-for-sales"></a>Systemkrav til Sales

Hvis du vil bruge løsningen Kundeemne til kontanter, skal du installere følgende komponenter:

- Dynamics 365 Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online eller en nyere version.
- Løsningen Kundeemne til kontanter til Dynamics 365 Sales, version 1.15.0.0 eller en nyere version. Løsningen kan hentes fra AppSource. [Hent Dynamics 365, Kundeemne til kontanter](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
