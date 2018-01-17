---
title: Synkronisere konti fra Sales med kunder i Finance and Operations
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere konti fra Microsoft Dynamics 365 for Sales med Microsoft Dynamics 365 Finance and Operations, Enterprise edition.
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1fdbeaaba53cd439d9872be78b1cf67cbc5a57b9
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a>Synkronisere konti fra Sales med kunder i Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Før du kan bruge kundeemnet til kontantløsning, skal du have kendskab til [Dynamics 365-dataintegration](/common-data-service/entity-reference/dynamics-365-integration). 

Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere konti fra Microsoft Dynamics 365 for Sales (Sales) med Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).

## <a name="template-and-task"></a>Skabelon og opgaver

Følgende skabeloner og underliggende opgaver bruges til at synkronisere konti fra Sales med Finance and Operations:

- **Navnet på skabelonen:** Konti (Sales til Finance and Operations)
- **Navnet på opgaven i projektet:** Konti - Konto - Kunder

Synkroniseringsopgaver, der kræves før synkronisering af Konto/Kunde: Ingen

## <a name="entity-set"></a>Enhedssæt

| Salg    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Konti | Konto | Kunder              |

## <a name="entity-flow"></a>Enhedsflow

Konti administreres i Sales og synkroniseres med Finance and Operations som kunder. Egenskaben **Vedligeholdes eksternt** for disse kunder er indstillet til **Ja** for at spore kunder, der stammer fra Sales. Under fakturering bruges disse oplysninger til at filtrere fakturaer, der synkroniseres med Sales.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemne til kontantløsning for Sales

Feltet **Kontonummer** er tilgængeligt på siden **Konto**. Det er blevet gjort til en naturlig og entydig nøgle, som kan understøtte integrationen. Funktionen Naturlig nøgle i CRM-løsningen (Customer Relationship Management) kan påvirke kunder, der allerede anvender feltet **Kontonummer**, men som ikke bruger en entydige **Kontonummer**-værdier for hver konto. Integrationsløsningen understøtter i øjeblikket ikke denne sag.

Når en ny konto oprettes, og der ikke allerede findes en værdi for **Kontonummer**, oprettes den automatisk ved hjælp af en nummerserie. Værdien består af **ACC** efterfulgt af en stigende nummerserie og et suffiks på seks tegn. Her er et eksempel: **ACC-01000-BVRCPS**

Når integrationsløsningen for Sales anvendes, indstiller et opgraderingsscript feltet **Kontonummer** for eksisterende konti i Sales. Hvis der ikke er nogen **Kontonummer**-værdier, bruges den nummerserie, der blev beskrevet tidligere.

## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning

- **CustomerGroupId**-tilknytningen fra **CDS &gt; Destination** skal opdateres til en gyldig værdi i Finance and Operations. Du kan angive en standardværdi, eller du kan angive værdien ved hjælp af en værditilknytning. Standardskabelonværdien er **10**.
- **Adresse, lande-/områdekode** er påkrævet i Finance and Operations. For at undgå synkroniseringsfejl kan du angive en standardværdi i tilknytningen fra **CDS &gt; Destination**. Denne standardværdi bruges derefter, hvis feltet er tomt, i Sales.

    - Standardskabelonværdien for **AddressCountryRegionISOCode** er **USA**.
    - Standardskabelonværdien for **DeliveryAddressCountryRegionISOCode** er **USA**.

- Ved at tilføje følgende tilknytninger fra **CDS &gt; Destination** kan du hjælpe med at reducere antallet af manuelle påkrævede opdateringer i Finance and Operations. Du kan bruge en standardværdi eller en værditilknytning fra f.eks. **Land/område** eller **By**.

    - **SiteId** - Et sted er påkrævet for at generere tilbud og salgsordrelinjer i Finance and Operations. Et standardsted kan hentes fra produktet eller fra kunden fra ordrehovedet. Standardskabelonværdien for **SiteId** er **1**.
    - **WarehouseId** - Et lagersted er påkrævet for at behandle tilbud og salgsordrelinjer i Finance and Operations. Et standardlagersted kan hentes fra produktet eller fra kunden fra ordrehovedet i Finance and Operations. Standardskabelonværdien for **WarehouseId** er **13**.
    - **LanguageId** – Et sprog er påkrævet for at generere tilbud og salgsordrer i Finance and Operations. Som standard bruges sproget fra ordrehovedet fra kunden. Standardskabelonværdien for **LanguageId** er **en-us**.

- Opdater CDS-organisations-id'et (**Organization_OrganizationId**) i **Kilde &gt; CDS**-tilknytningen. Standardskabelonværdien er **ORG001**.

## <a name="template-mapping-in-data-integrator"></a>Tilknytning af skabelon i dataintegrator

> [!NOTE]
> Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** indgår ikke i standardtilknytningerne. Hvis du vil tilknytte disse felter, skal du konfigurere en værditilknytning. Værditilknytninger er specifikke for dataene i de organisationer, som enheden synkroniseres mellem.

Følgende illustration viser et eksempel på en skabelontilknytning i dataintegrator.

![Tilknytning af skabelon i dataintegrator](./media/accounts-template-mapping-data-integrator-1.png)

![Skabelontilknytning for konti i dataintegrator](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Relaterede emner

[Synkronisere produkter fra Finance and Operations til produkter i Sales](products-template-mapping.md)

[Synkronisere kontaktpersoner fra Sales med kontaktpersoner eller kunder i Finance and Operations](contacts-template-mapping.md)

[Synkronisere titler og linjer i salgstilbud fra Sales med Finance and Operations](sales-quotation-template-mapping.md)

[Synkronisere salgsordrehoveder og linjer fra Finance and Operations til Sales](sales-order-template-mapping.md)

[Synkronisere salgsfakturahoveder og linjer fra Finance and Operations til Sales](sales-invoice-template-mapping.md)




