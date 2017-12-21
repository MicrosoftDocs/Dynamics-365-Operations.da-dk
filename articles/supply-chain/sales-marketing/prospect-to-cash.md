---
title: Kundeemne til kontanter
description: "Dette emne indeholder en oversigt over kundeemne til kontanter-løsningen mellem Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 11/17/2017
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
ms.sourcegitcommit: 788e64476094e84eb4d438890776306c05b20582
ms.openlocfilehash: 762699cf68ec8a9df5db20d7dd33bc9248f0a36e
ms.contentlocale: da-dk
ms.lasthandoff: 12/11/2017

---

# <a name="prospect-to-cash"></a>Kundeemne til kontanter

[!include[banner](../includes/banner.md)]

Kundeemne til kontanter-løsningen giver direkte synkronisering på tværs af Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og Microsoft Dynamics 365 for Sales. Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data til firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Finance and Operations og Sales. Når data flyder mellem Finance and Operations og Sales, kan du udføre salgs- og marketingaktiviteter i Sales, og du kan håndtere ordreopfyldelsen ved at bruge lagerstyring i Finance and Operations.

I den aktuelle version indeholder Kundeemne til kontanter-løsning følgende typer direkte synkronisering:

- [Vedligehold konti i Sales, og synkroniser dem direkte fra Sales med Finance and Operations](accounts-template-mapping-direct.md)
- [Vedligehold produkter i Finance and Operations, og synkroniser dem direkte med Sales](products-template-mapping-direct.md)
- [Vedligehold kontakter i Sales, og synkroniser dem direkte med kontakter eller debitorer i Finance and Operations](contacts-template-mapping-direct.md)
- [Synkronisere salgstilbud direkte fra Sales med Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
- [Synkronisere salgsordrer direkte fra Finance and Operations med Sales](sales-order-template-mapping-direct.md)
- [Synkroniser salgsordrer direkte mellem Sales og Finance and Operations](sales-order-template-mapping-direct-two-ways.md)
- [Synkronisere salgsfakturaer direkte fra Finance and Operations med Sales](sales-invoice-template-mapping-direct.md)

I tidligere versioner indeholder Kundeemne til kontanter-løsning følgende typer ikke-direkte synkronisering:

- [Vedligehold konti i Sales, og synkroniser dem med Finance and Operations](accounts-template-mapping.md)
- [Vedligehold kontakter i Sales, og synkroniser dem med Finance and Operations](contacts-template-mapping.md)
- [Vedligehold produkter kontakter i Finance and Operations, og synkroniser dem med Sales](products-template-mapping.md)
- [Opret salgstilbud i Sales, og synkroniser dem med Finance and Operations](sales-quotation-template-mapping.md)
- [Opret salgsordrer i Finance and Operations, og synkroniser dem med Sales](sales-order-template-mapping.md)
- [Opret salgsfakturaer i Finance and Operations, og synkroniser dem med Sales](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a>Systemkrav til Finance and Operations

Hvis du vil bruge løsningen Kundeemne til kontanter, skal du installere følgende komponenter:

### <a name="july-2017"></a>Juli 2017 

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) med platformsopdatering 8 (programbuild 7.2.11792.56024 med platformbuild 7.0.4565.16212)
- Følgende hotfixes til Finance and Operations:

    - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – Dette hotfix muliggør salgsordresynkronisering fra Sales til Finance and Operations via funktionen Dataintegration. Det indeholder også flere andre forbedringer.
    - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Dette hotfix muliggør salgsordrelinjesynkronisering fra Sales til Finance and Operations til Sales via funktionen Dataintegration.
    - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Dette hotfix muliggør salgsordresynkronisering fra Sales til Finance and Operations til Sales via funktionen Dataintegration.

    > [!NOTE]
    > Du behøver kun at installere KB4045570, fordi installationen omfatter ændringerne fra andre videnbaseartikler (KB).

### <a name="november-2016-version-1611"></a>November 2016 (version 1611)

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (november 2016) med platformsopdatering 8 eller derover

- Følgende hotfixes til Finance and Operations:

    - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** – Aktiver synkronisering af salgsordre med Dataintegrator fra Microsoft Dynamics 365 for Finance and Operations til Sales 
    - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** – Aktiver synkronisering af salgsordresidehoved og -linje med Dataintegrator fra Microsoft Dynamics 365 for Finance and Operations til Sales
    - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Understøttelse af Kundeemne til kontanter-integration via dataenheder er påkrævet
    
    > [!NOTE]
    > Du skal udløse følgende batchjob fra formularen SalesPopulateProspectToCash efter installation af hotfixes. Denne formular er skjult, fordi du kun skal bruge den én gang. For at få adgang til den skal du tilføje følgende i din browseradresse, når du er logget på miljøet: &mi=action:SalesPopulateProspectToCash, f.eks. https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash Klik på OK i den formular, der åbnes.
    Dette udfylder et nyt "LineCreationSequnceNumber"-felt i tabellerne "SalesLine", "SalesQuotationLine" og "CustInvoiceTrans" med entydige værdier og opdaterer produktlisten. Dette er nødvendigt, for at P2C-integrationen kan fungere på 7.1


## <a name="system-requirements-for-sales"></a>Systemkrav til Sales

Hvis du vil bruge løsningen Kundeemne til kontanter, skal du installere følgende komponenter:

- Microsoft Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online
- Løsningen Kundeemne til kontanter til Microsoft Dynamics 365 for Sales, version 1.15.0.0 (v15) 

   > [!NOTE]
   >
   > Skabeloner med version 1.0.0.0 og 1.0.0.1 understøttes i Kundeemne til kontanter-løsning for Microsoft Dynamics 365 Sales, version 1.14.1.0
   >
   > Skabeloner med version 2.0.0.0 og 2.1.0.0 understøttes i Kundeemne til kontanter-løsning for Microsoft Dynamics 365 Sales, version 1.15.0.0

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Installer løsningen Kundeemne til kontanter til Sales

1. Hent [zip-filen med løsningspakken Kundeemne til kontanter til Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) fra CustomerSource.
2. Kontroller, at zip-filen ikke er blokeret. Ellers, når du forsøger at installere løsningspakken, modtager du følgende fejlmeddelelse: "Der blev ikke fundet nogen importpakker". For at fjerne blokeringen af zip-filen skal du højreklikke på filen og vælge **Egenskaber**. Vælg derefter **Ophæv blokering**.
3. Pak filen ud, og kør **PackageDeployer.exe**.
4. Installer løsningen Kundeemne til kontanter i din Sales-forekomst:

    1. Vælg installationstypen **Office 365**.
    2. Vælg **Vis avancerede**.
    3. For en hurtig installation skal du vælge et område. Hvis du vælger **Ved ikke**, vil systemet søge efter alle områder, og installationen vil tage længere tid.
    4. Angiv brugernavnet og adgangskoden for en administrator, der har installationsrettigheder.

