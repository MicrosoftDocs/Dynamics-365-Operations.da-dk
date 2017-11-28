---
title: Synkronisere salgstilbudshoveder og -linjer fra Sales til Finance and Operations
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgstilbudshoveder og -linjer fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c8cfc484eed02423dbf0c7caaf8ac2337b6ac38d
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a>Synkronisere salgstilbudshoveder og -linjer fra Sales til Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Før du kan bruge kundeemnet til kontantløsning, skal du have kendskab til [Dynamics 365-dataintegration](/common-data-service/entity-reference/dynamics-365-integration). 

Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgstilbudshoveder og -linjer fra Microsoft Dynamics 365 for Sales (Sales) til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations). 

## <a name="template-and-tasks"></a>Skabelon og opgaver

Følgende skabeloner og underliggende opgaver bruges til at synkronisere salgstilbudshoveder og -linjer fra Sales til Finance and Operations:

- **Navnet på skabelonen:** Salgstilbud (Sales til Finance and Operations)
- **Navnene på opgaverne i projektet:**

    - QuoteHeader
    - QuoteLine

Følgende synkroniseringsopgaver kræves, før salgstilbudshoveder og -linjer kan synkroniseres:

- Produkter (Fin og Ops til Sales)
- Konti (Sales til Fin og Ops) (hvis det bruges)
- Kontakter til Debitorer (Sales til Fin and Ops) (hvis det bruges)

## <a name="entity-set"></a>Enhedssæt

| Salg        | CDS           | Finance and Operations    |
|--------------|---------------|---------------------------|
| Citater       | Tilbud     | Salgstilbudshoveder   |
| QuoteDetails | QuotationLine | CDS-salgstilbudslinjer |

## <a name="entity-flow"></a>Enhedsflow

Salgstilbud oprettes i Sales og synkroniseres til Finance and Operations.

Salgstilbud fra Sales synkroniseres kun, hvis følgende betingelser er opfyldt:

- Alle produkter på linjerne i salgstilbuddet vedligeholdes eksternt.
- Salgstilbuddet er aktivt eller aktiveret.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemne til kontantløsning for Sales

Feltet **Har kun eksternt vedligeholdte produkter** er føjet til objektet Tilbud for konsekvent at spore, om salgstilbuddet består af udelukkende eksternt vedligeholdte produkter. Hvis et salgstilbud kun har eksternt vedligeholdte produkter, vedligeholdes produkterne i Finance and Operations. Denne funktionsmåde er med til at sikre, at du ikke forsøger at synkronisere salgstilbudslinjer med produkter, der er ukendte i Finance and Operations.

Alle produkter og linjer i tilbuddet opdateres med **Har kun eksternt vedligeholdte produkter**-oplysningerne fra tilbudshovedet. Disse oplysninger findes i feltet **Tilbuddet indeholder kun eksternt vedligeholdte produkter** i enheden for tilbudslinjen.

Felterne **Rabat**, **Tillæg** og **Moms** styres af en kompleks opsætning i Finance and Operations. Denne opsætning understøtter ikke aktuelt integrationstilknytning. I det aktuelle design styres og håndteres felterne **Pris**, **Rabat**, **Tillæg** og **Moms** af Finance and Operations.

I Sales gør løsningen følgende felter skrivebeskyttet, fordi værdierne ikke synkroniseres for Finance and Operations:

- **Skrivebeskyttede felter i salgstilbudshovedet:** Rabatprocent, Rabat, Fragtbeløb
- **Skrivebeskyttede felter på linjer i salgstilbuddet:** Moms

## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning

Før du synkroniserer salgsordrer, er det vigtigt at opdatere systemerne med følgende indstilling:

### <a name="setup-in-sales"></a>Konfiguration i Sales

- Gå til **Indstillinger** &gt; **Administration** &gt; **Systemindstillinger** &gt; **Sales** og kontrollér, at feltet **Rabatberegningsmetode** er indstillet til **Pr. enhed**. Med denne indstilling kan du sikre, at rabatten for linjeelementet fra Sales svarer til indstillingen i Finance and Operations. I modsat fald er rabatten ikke korrekt i Finance and Operations, fordi Finance and Operations læser rabatten som en rabat på pr. enhed, selvom det var en rabat pr. linje i Sales.

### <a name="setup-in-finance-and-operations"></a>Konfiguration i Finance and Operations

- Gå til **Debitor** &gt; **Konfiguration** &gt; **Debitorparametre**. Under fanen **Nummerserie** skal du vælge nummerserien for salgstilbud og derefter klikke på **Vis detaljer**. Derefter skal du under **Generel opsætning** indstille feltet **Manuel** til **Ja**.
- Gå til **Debitor** &gt; **Konfiguration** &gt; **Debitorparametre**. Under fanen **Forsendelser** skal du derefter indstille feltet **Leveringsdatokontrol** til **Ingen**. Denne indstilling hjælper med at forhindre, at synkronisering mislykkes for salgstilbud.

### <a name="setup-in-the-data-integration-project"></a>Opsætning af dataintegrationsprojektet

#### <a name="quoteheader"></a>QuoteHeader

- Feltet **Ønsket leveringsdato** er påkrævet i Finance and Operations, og synkroniseringen mislykkes, hvis feltet er tomt. For at undgå dette problem, hvis feltet er tomt, hentes en standarddato fra **Kilde &gt; CDS**. Datoen skal opdateres til en foretrukken værdi. I øjeblikket kan du ikke angive en værdi som **I dag** som dags dato. Du skal angive en konkret dato. Standardværdien i skabelonen for **Ønsket leveringsdato** er **01-01-2020**.
- Feltet **Adresse, lande-/områdekode** er påkrævet i Finance and Operations. For at forhindre synkroniseringsfejl kan du angive en standardværdi, der bruges, hvis feltet er tomt i Sales. Denne standardværdi er også nyttig, fordi du ikke manuelt skal indtaste en værdi i feltet **Land/område** for lokale adresser. Der er ingen standardskabelonværdi for **DeliveryAddressCountryRegionISOCode**.
- Opdater tilknytningen for **CDS-organisations-id** i **Kilde &gt; CDS**, så den passer til **CDS-organisation** i organisationsenheden:

    - Standardskabelonværdien for **Organization_OrganizationId** er **ORG001**.
    - Standardskabelonværdien for **Account_Organization_OrganizationId** er **ORG001**.
    - Standardskabelonværdien for **InvoiceAccount_OrganizationId** er **ORG001**.

#### <a name="quoteline"></a>QuoteLine

- Opdater tilknytningen for **CDS-organisations-id** i **Kilde &gt; CDS**, så den passer til **CDS-organisation** i organisationsenheden:

    - Standardskabelonværdien for **Organization_OrganizationId** er **ORG001**.
    - Standardskabelonværdien for **Product_Organization_Organization_OrganizationId** er **ORG001**.
    - Standardskabelonværdien for **Quotation_Organization_Organization_OrganizationId** er **ORG001**.

- Feltet **Ønsket leveringsdato** er påkrævet i Finance and Operations, og synkroniseringen mislykkes, hvis feltet er tomt. For at undgå dette problem, hvis feltet er tomt, hentes en standarddato fra **Kilde &gt; CDS**. Datoen skal opdateres til en foretrukken værdi. I øjeblikket kan du ikke angive en værdi som **I dag** som dags dato. Du skal angive en konkret dato. Standardværdien i skabelonen for **Ønsket leveringsdato** er **01-01-2020**.
- Du kan tilføje følgende tilknytninger fra **CDS &gt; Destination** for at sikre, at tilbudslinjerne importeres til Finance and Operations, hvis der ikke er nogen standardoplysninger fra debitoren eller produktet:

    - **SiteId** - Et sted er påkrævet for at generere tilbud og salgsordrelinjer i Finance and Operations. Der er ingen standardskabelonværdi for **SiteId**.
    - **WarehouseId** - Et lagersted er påkrævet for at behandle tilbud og salgsordrelinjer i Finance and Operations. Der er ingen standardskabelonværdi for **WarehouseId**.

- Sørg for, at den krævede værditilknytning for salgsmåleenheden (UOM) i Finance and Operations findes i **CDS &gt; Destination**-tilknytningen for **Quantity_UOM** til **SALESUNITSYMBOL**.

## <a name="template-mapping-in-data-integrator"></a>Tilknytning af skabelon i dataintegrator

> [!NOTE]
> - Felterne **Rabat**, **Tillæg** og **Moms** styres af en kompleks opsætning i Finance and Operations. Denne opsætning understøtter ikke aktuelt integrationstilknytning. I det aktuelle design håndteres felterne **Pris**, **Rabat**, **Tillæg** og **Moms** af Finance and Operations.
> - Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** er ikke en del af standardtilknytningerne. Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.

Følgende illustration viser et eksempel på en skabelontilknytning i dataintegrator.

### <a name="quoteheader"></a>QuoteHeader

![Tilknytning af skabelon i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Tilknytning af skabelon i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a>QuoteLine

![Tilknytning af skabelon i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Tilknytning af skabelon i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Relaterede emner

[Synkronisere produkter fra Finance and Operations til produkter i Sales](products-template-mapping.md)

[Synkronisere konti fra Sales med debitorer i Finance and Operations](accounts-template-mapping.md)

[Synkronisere kontaktpersoner fra Sales med kontaktpersoner eller kunder i Finance and Operations](contacts-template-mapping.md)



