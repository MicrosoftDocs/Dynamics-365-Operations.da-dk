---
title: Synkronisere kontaktpersoner fra Sales med kontaktpersoner eller kunder i Finance and Operations
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere kontaktpersoner (Kontaktpersoner) og kontaktpersoner (Kunder) fra Microsoft Dynamics 365 for Sales med Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.
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
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 41e27776b94df059ada13efb9a3dbf6a29d67f36
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Synkronisere kontaktpersoner fra Sales med kontaktpersoner eller kunder i Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Før du kan bruge kundeemnet til kontantløsning, skal du have kendskab til [Dynamics 365-dataintegration](/common-data-service/entity-reference/dynamics-365-integration). 

Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere kontaktpersonenheder (Kontaktpersoner) og kontaktpersoner (Kunder) fra Microsoft Dynamics 365 for Sales (Sales) med Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

Følgende skabeloner og underliggende opgaver bruges til at synkronisere kontaktpersoner (Kontaktpersoner) i Sales med kontaktpersoner (Kunder) i Finance and Operations:

- **Skabelonernes navne:**

    - Kontaktpersoner (Sales til Fin og Ops)
    - Kontaktpersoner til Kunder (Sales til Fin og Ops)

- **Navnene på opgaverne i projektet:**

    - Kontaktpersoner
    - ContactToCustomer

Følgende synkroniseringsopgave skal udføres før synkronisering af kontaktpersoner: Konti (Sales til Fin and Ops)

## <a name="entity-sets"></a>Enhedssæt

| Sales    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Kontaktpersoner | Kontakt | CDS kontakter           |
| Kontaktpersoner | Konto | Debitorer V2           |

## <a name="entity-flow"></a>Enhedsflow

Kontaktpersoner administreres i Sales og synkroniseres med CDS (Common Data Service) og Finance and Operations.

En kontaktperson i Sales kan blive en kontaktperson i CDS og Finance and Operations. Kontaktpersonen kan også blive en konto i CDS og en kunde i Finance and Operations. For at bestemme, om en kontaktperson skal hentes i Sales for at blive synkroniseret med CDS og Finance and Operations (f.eks. Kontaktpersoner i Sales &gt; Kontaktperson i CDS &gt; Kontaktpersoner i Finance and Operations), ser systemet på følgende egenskaber for Kontaktperson i Sales:

- **Synkroniser til Konto i CDS og Kunde i Finance and Operations:** Kontaktpersoner, hvor **Er aktiv kunde** er indstillet til **Ja**
- **Synkroniser til Kontaktperson i CDS og Kontaktperson i Finance and Operations:** Kontaktpersoner, hvor **Er aktiv kunde** er indstillet til **Nej** og **Firma** (overordnet konto/kontaktperson) peger på en konto (og ikke en kontaktperson)

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemne til kontantløsning for Sales 

Et nyt felt **Er aktiv kunde** er føjet til Kontaktperson. Dette felt bruges til at skelne mellem kontaktpersoner, der har salgsaktivitet, og kontaktpersoner, der ikke har en salgsaktivitet. **Er aktiv kunde** er kun indstillet til **Ja** for kontaktpersoner, der har relaterede tilbud, ordrer eller fakturaer. Kun disse kontaktpersoner synkroniseres med Finance and Operations som kunder.

Et nyt felt **IsCompanyAnAccount** er tilføjet i Kontaktperson. Dette felt bruges til at angive, om en kontaktperson er tilknyttet et firma (overordnet konto/kontaktperson) af typen **Konto**. Disse oplysninger bruges til at identificere kontaktpersoner, der skal synkroniseres med Finance and Operations som kontaktpersoner.

Et nyt felt, **Kontaktpersons nummer**, er føjet til kontaktpersonen for at sikre en naturlig og entydig nøgle til integrationen. Når der oprettes en ny kontaktperson, genereres der automatisk en værdi for **Kontaktpersons nummer** ved hjælp af en nummerserie. Værdien består af **CON** efterfulgt af en stigende nummerserie og et suffiks på seks tegn. Her er et eksempel: **CON-01000-BVRCPS**

Når integrationsløsningen for Sales føjes til Sales, indstiller et opgraderingsscript feltet **Kontaktpersons nummer** for eksisterende kontaktpersoner ved hjælp af den nummerserie, der blev beskrevet tidligere. Opgraderingsscriptet indstiller også feltet **Er aktiv kunde** til **Ja** for de kontaktpersoner, der har salgsaktivitet.

## <a name="in-finance-and-operations"></a>I Finance and Operations 

Kontaktpersoner mærkes ved hjælp af egenskaben **IsContactPersonExternallyMaintained**. Denne egenskab angiver, at en given kontaktperson vedligeholdes eksternt. I dette tilfælde vedligeholdes eksternt vedligeholdte kontaktpersoner i Sales.

## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning

### <a name="contact-to-contact"></a>Kontaktperson til kontaktperson

- Opdater **CDS-organisations-id** i **Kilde &gt; CDS**-tilknytningen.

    - Standardskabelonværdien for **Organization_OrganizationId [Organisations-ID]** er **ORG001**.
    - Standardskabelonværdien for **PrimaryAccount_Organization_OrganizationId [Organisations-ID]** er **ORG001**.

- **Adresse, lande-/områdekode** er påkrævet i Finance and Operations. For at undgå synkroniseringsfejl kan du angive en standardværdi i **CDS &gt; Operations**-tilknytningen. Denne standardværdi bruges derefter, hvis feltet er tomt, i Sales. Standardskabelonværdien for **PrimaryAddressCountryRegionISOCode** er **USA**.
- Sørg for, at der findes en værdi for følgende felt i Finance and Operations. Hvis oplysningerne ikke er nødvendige i Finance and Operations, kan du fjerne tilknytningen fra **CDS &gt; Destination**-tilknytningen.

    - **Feltnavn i Finance and Operations:** Beslutning
    - **Tilknytning:** PrimaryAccountRole = DecisionMakingRole

### <a name="contact-to-customer"></a>Kontaktperson til kunde

- Opdater **CDS-organisations-id** i **Kilde &gt; CDS**-tilknytningen. Standardskabelonværdien for **Organization_OrganizationId [Organisations-ID]** er **ORG001**.
- **Adresse, lande-/områdekode** er påkrævet i Finance and Operations. For at undgå synkroniseringsfejl kan du angive en standardværdi i **CDS &gt; Destination**-tilknytningen. Denne standardværdi bruges derefter, hvis feltet er tomt, i Sales. Standardskabelonværdien for **PrimaryAddressCountryRegionISOCode** er **USA**.
- **CustomerGroup** er påkrævet i Finance and Operations. For at undgå synkroniseringsfejl kan du angive en standardværdi i **CDS &gt; Destination**-tilknytningen. Denne standardværdi bruges derefter, hvis feltet er tomt, i Sales. Standardskabelonværdien for **CustomerGroupId** er **10**.
- Ved at tilføje følgende tilknytninger fra **CDS &gt; Destination** kan du hjælpe med at reducere antallet af manuelle opdateringer i Finance and Operations. Du kan bruge en standardværdi eller en værditilknytning fra f.eks. **Land/område** eller **By**.

    - **SiteId** - Der kan også defineres et standardsted for produkter i Finance and Operations. Et sted er påkrævet for at generere tilbud og salgsordrer i Finance and Operations. En skabelonværdi for **SiteId** er ikke defineret.
    - **WarehouseId** - Der kan også defineres et standardlagersted for produkter i Finance and Operations. Et lagersted er påkrævet for at generere tilbud og salgsordrer i Finance and Operations. En skabelonværdi for **WarehouseId** er ikke defineret.
    - **LanguageId** - Et sprog er påkrævet for at generere tilbud og salgsordrer i Finance and Operations. Standardskabelonværdien for **LanguageId** er **en-us**.

## <a name="template-mapping-in-data-integrator"></a>Tilknytning af skabelon i dataintegrator

Følgende illustration viser et eksempel på en skabelontilknytning i dataintegrator.

### <a name="contact-to-contact"></a>Kontaktperson til kontaktperson

![Tilknytning af skabelon i dataintegrator](./media/contacts-template-mapping-data-integrator-1.png)

![Skabelontilknytning for kontaktpersoner i dataintegrator](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a>Kontaktperson til kunde

![Tilknytning af skabelon i dataintegrator](./media/contacts-template-mapping-data-integrator-3.png)

![Skabelontilknytning for kontaktpersoner i dataintegrator](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Relaterede emner

[Synkronisere produkter fra Finance and Operations til produkter i Sales](products-template-mapping.md)

[Synkronisere konti fra Sales med kunder i Finance and Operations](accounts-template-mapping.md)

[Synkronisere titler og linjer i salgstilbud fra Sales med Finance and Operations](sales-quotation-template-mapping.md)

[Synkronisere salgsordrehoveder og linjer fra Finance and Operations til Sales](sales-order-template-mapping.md)

[Synkronisere salgsfakturahoveder og linjer fra Finance and Operations til Sales](sales-invoice-template-mapping.md)

