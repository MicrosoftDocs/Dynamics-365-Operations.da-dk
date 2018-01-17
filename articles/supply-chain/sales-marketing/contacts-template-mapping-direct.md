---
title: Synkronisere kontakter direkte fra Sales med kontakter eller debitorer i Finance and Operations
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere enhederne kontakt (kontakter) og kontakt (kunder) fra Microsoft Dynamics 365 for Sales med Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.openlocfilehash: 8de9a920f384b69c9b3764a0431208bbdcb395bf
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Synkronisere kontakter direkte fra Sales med kontakter eller debitorer i Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Før du kan bruge kundeemne til kontant-løsningen, skal du have kendskab til [Dynamics 365-dataintegration](/common-data-service/entity-reference/dynamics-365-integration).

Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere enhederne kontakt (kontakter) og kontakt (kunder) direkte fra Microsoft Dynamics 365 for Sales med Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflow i kundeemne til kontant

Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Finance and Operations og Sales. Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Finance and Operations og Sales. I følgende illustration vises, hvordan data synkroniseres mellem Finance and Operations og Sales.

[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

For at få adgang til de tilgængelige skabeloner, skal du åbne [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration). Vælg **Projekter**, og vælg derefter i øverste højre hjørne **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabeloner og underliggende opgaver bruges til at synkronisere enhederne kontakter (kontakter) i Sales med enhederne kontakter (kunder) i Finance and Operations:

- **Navne på skabeloner i dataintegration:**

    - Kontakter (Fin and Ops til Sales) - Direkte
    - Kontakter til kunder (Sales til Fin and Ops) - Direkte

- **Navne på opgaverne i dataintegrationsprojektet:**

    - Kontaktpersoner
    - ContactToCustomer

Følgende synkroniseringsopgave skal udføres før synkronisering af kontakter kan finde sted: Konti (Sales til Fin and Ops)

## <a name="entity-sets"></a>Enhedssæt

| Salg    | Finance and Operations |
|----------|------------------------|
| Kontaktpersoner | CDS kontakter           |
| Kontaktpersoner | Debitorer V2           |

## <a name="entity-flow"></a>Enhedsflow

Kontakter administreres i Sales og synkroniseres til Finance and Operations.

En kontakt i Sales kan enten blive en kontakt eller en kunde i Finance and Operations. For at bestemme om en kontakt i Sales skal synkroniseres til Finance and Operations som en kontakt eller en kunde, ser systemet på følgende egenskaber på kontakten i Sales:

- **Synkronisering til en kunde i Finance and Operations:** Kontakter hvor **Er aktiv kunde** er angivet til **Ja**
- **Synkronisering til en kontakt i Finance and Operations:** Kontakter hvor **Er aktiv kunde** er angivet til **Nej** og **Firma** (overordnet konto/kontakt) peger på en konto (ikke en kontakt)

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemne til kontantløsning for Sales

Et nyt felt **Er aktiv kunde** er føjet til kontakten. Dette felt bruges til at skelne mellem kontakter, der har salgsaktivitet, og kontakter, der ikke har en salgsaktivitet. **Er aktiv kunde** er kun indstillet til **Ja** for kontakter, der har relaterede tilbud, ordrer eller fakturaer. Kun disse kontakter synkroniseres med Finance and Operations som kunder.

Et nyt felt **IsCompanyAnAccount** er føjet til kontakten. Dette felt angiver, om en kontakt er tilknyttet et firma (overordnet konto/kontakt) af typen **Konto**. Disse oplysninger bruges til at identificere kontakter, der skal synkroniseres med Finance and Operations som kontakter.

Et nyt felt, **Kontaktnummer**, er føjet til kontakten for at sikre en naturlig og entydig nøgle til integrationen. Når der oprettes en ny kontakt, genereres der automatisk en værdi for **Kontaktnummer** ved hjælp af en nummerserie. Værdien består af **CON** efterfulgt af en stigende nummerserie og et suffiks på seks tegn. Her er et eksempel: **CON-01000-BVRCPS**

Når integrationsløsningen for Sales anvendes, indstiller et opgraderingsscript feltet **Kontaktnummer** for eksisterende kontakter ved hjælp af den nummerserie, der blev omtalt tidligere. Opgraderingsscriptet indstiller også feltet **Er aktiv kunde** til **Ja** for alle kontakter, der har salgsaktivitet.

## <a name="in-finance-and-operations"></a>I Finance and Operations

Kontaktpersoner mærkes ved hjælp af egenskaben **IsContactPersonExternallyMaintained**. Denne egenskab angiver, at en given kontakt vedligeholdes eksternt. I dette tilfælde vedligeholdes eksternt vedligeholdte kontakter i Sales.

## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning

### <a name="contact-to-customer"></a>Kontakt til kunde

- **CustomerGroup** er påkrævet i Finance and Operations. For at hjælpe med til at undgå synkroniseringsfejl kan du angive en standardværdi i tilknytningen. Denne standardværdi bruges derefter, hvis feltet er tomt, i Sales.

    Standardskabelonværdien er **10**.

- Ved at tilføje følgende tilknytninger kan du hjælpe med at reducere antallet af manuelle påkrævede opdateringer i Finance and Operations. Du kan bruge en standardværdi eller en værditilknytning fra f.eks. **Land/område** eller **By**.

    - **SiteId** - Der kan også defineres et standardwebsted for produkter i Finance and Operations. Et sted er påkrævet for at generere tilbud og salgsordrer i Finance and Operations.

        En skabelonværdi for **SiteId** er ikke defineret.

    - **WarehouseId** - Der kan også defineres et standardlagersted for produkter i Finance and Operations. Et lagersted er påkrævet for at generere tilbud og salgsordrer i Finance and Operations.

        En skabelonværdi for **WarehouseId** er ikke defineret.

    - **LanguageId** – Et sprog er påkrævet for at generere tilbud og salgsordrer i Finance and Operations.
    
        Standardskabelonværdien er **da**.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser et eksempel på en skabelontilknytning i dataintegration. 

> [!NOTE]
> Tilknytningen viser, hvilke oplysninger der synkroniseres fra Sales til Finance and Operations.

### <a name="contact-to-contact"></a>Kontakt til kontakt

![Skabelontilknytning i dataintegrator](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>Kontakt til kunde

![Skabelontilknytning i dataintegrator](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>Relaterede emner

[Kundeemne til kontanter](prospect-to-cash.md)

[Synkronisere konti fra direkte fra Sales med debitorer i Finance and Operations](accounts-template-mapping-direct.md)

[Synkronisere produkter direkte fra Finance and Operations med produkter i Sales](products-template-mapping-direct.md)

[Synkronisere salgsordrehoveder og -linjer direkte fra Finance and Operations til Sales](sales-order-template-mapping-direct.md)

[Synkronisere salgsfakturahoveder og -linjer direkte fra Finance and Operations til Sales](sales-invoice-template-mapping-direct.md)



