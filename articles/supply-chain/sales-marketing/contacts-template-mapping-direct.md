---
title: Synkronisere kontakter direkte fra Sales med kontakter eller kunder i Supply Chain Management
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere enhederne Kontakt (kontakter) og Kontakt (kunder) fra Dynamics 365 Sales til Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
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
ms.openlocfilehash: 7d3a4602a3d8462666dfcb26b97a4f652891f7bc
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249960"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a>Synkronisere kontakter direkte fra Sales med kontakter eller kunder i Supply Chain Management

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Før du kan bruge kundeemne til kontant-løsningen, skal du have kendskab til [Integrere data i Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere enhederne Kontakt (kontakter) og Kontakt (kunder) direkte fra Dynamics 365 Sales til Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflow i kundeemne til kontant

Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Supply Chain Management og Sales. Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om konti, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Supply Chain Management og Sales. I følgende illustration vises, hvordan data synkroniseres mellem Supply Chain Management og Sales.

[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

For at få adgang til de tilgængelige skabeloner skal du åbne [PowerApps Administration](https://preview.admin.powerapps.com/dataintegration). Vælg **Projekter**, og vælg derefter i øverste højre hjørne **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabeloner og underliggende opgaver bruges til at synkronisere enhederne Kontakt (kontakter) i Sales med enhederne Kontakt (kunder) i Supply Chain Management:

- **Navne på skabeloner i dataintegration:**

    - Kontakter (Sales til Supply Chain Management) - Direkte
    - Kontakter til kunde (Sales til Supply Chain Management) - Direkte

- **Navnene på opgaverne i dataintegrationsprojekt**

    - Kontaktpersoner
    - ContactToCustomer

Følgende synkroniseringsopgave skal udføres før synkronisering af kontakter kan finde sted: Konti (Sales til Supply Chain Management)

## <a name="entity-sets"></a>Enhedssæt

| Salg    | Supply Chain Management |
|----------|------------------------|
| Kontaktpersoner | CDS kontakter           |
| Kontaktpersoner | Debitorer V2           |

## <a name="entity-flow"></a>Enhedsflow

Kontakter administreres i Sales og synkroniseres tol Supply Chain Management.

En kontakt i Sales kan enten blive en kontakt eller en kunde i Supply Chain Management. For at bestemme om en kontakt i Sales skal synkroniseres til Supply Chain Management som en kontakt eller en kunde, ser systemet på følgende egenskaber på kontakten i Sales:

- **Synkronisering til en kunde i Supply Chain Management:** Kontakter hvor **Er aktiv kunde** er angivet til **Ja**
- **Synkronisering til en kontakt i Supply Chain Management:** Kontakter hvor **Er aktiv kunde** er angivet til **Nej** og **Firma** (overordnet konto/kontakt) peger på en konto (ikke en kontakt)

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemne til kontantløsning for Sales

Et nyt felt **Er aktiv kunde** er føjet til kontakten. Dette felt bruges til at skelne mellem kontakter, der har salgsaktivitet, og kontakter, der ikke har en salgsaktivitet. **Er aktiv kunde** er kun indstillet til **Ja** for kontakter, der har relaterede tilbud, ordrer eller fakturaer. Kun disse kontakter synkroniseres med Supply Chain Management som kunder.

Et nyt felt **IsCompanyAnAccount** er føjet til kontakten. Dette felt angiver, om en kontakt er tilknyttet et firma (overordnet konto/kontakt) af typen **Konto**. Disse oplysninger bruges til at identificere kontakter, der skal synkroniseres med Supply Chain Management som kontakter.

Et nyt felt, **Kontaktnummer**, er føjet til kontakten for at sikre en naturlig og entydig nøgle til integrationen. Når der oprettes en ny kontakt, genereres der automatisk en værdi for **Kontaktnummer** ved hjælp af en nummerserie. Værdien består af **CON** efterfulgt af en stigende nummerserie og et suffiks på seks tegn. Her er et eksempel: **CON-01000-BVRCPS**

Når integrationsløsningen for Sales anvendes, indstiller et opgraderingsscript feltet **Kontaktnummer** for eksisterende kontakter ved hjælp af den nummerserie, der blev omtalt tidligere. Opgraderingsscriptet indstiller også feltet **Er aktiv kunde** til **Ja** for alle kontakter, der har salgsaktivitet.

## <a name="in-supply-chain-management"></a>I Supply Chain Management

Kontaktpersoner mærkes ved hjælp af egenskaben **IsContactPersonExternallyMaintained**. Denne egenskab angiver, at en given kontakt vedligeholdes eksternt. I dette tilfælde vedligeholdes eksternt vedligeholdte kontakter i Sales.

## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning

### <a name="contact-to-customer"></a>Kontakt til kunde

- **CustomerGroup** er påkrævet i Supply Chain Management. For at hjælpe med til at undgå synkroniseringsfejl kan du angive en standardværdi i tilknytningen. Denne standardværdi bruges derefter, hvis feltet er tomt, i Sales.

    Standardskabelonværdien er **10**.

- Ved at tilføje følgende tilknytninger kan du hjælpe med at reducere antallet af manuelle påkrævede opdateringer i Supply Chain Management. Du kan bruge en standardværdi eller en værditilknytning fra f.eks. **Land/område** eller **By**.

    - **SiteId** - Der kan også defineres et standardwebsted for produkter i Supply Chain Management. Et sted er påkrævet for at generere tilbud og salgsordrer i Supply Chain Management.

        En skabelonværdi for **SiteId** er ikke defineret.

    - **WarehouseId** - Der kan også defineres et lagersted for produkter i Supply Chain Management. Et lagersted er påkrævet for at generere tilbud og salgsordrer i Supply Chain Management.

        En skabelonværdi for **WarehouseId** er ikke defineret.

    - **LanguageId** - Et sprog er påkrævet for at generere tilbud og salgsordrer i Supply Chain Management.
    
        Standardskabelonværdien er **da**.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser et eksempel på en skabelontilknytning i dataintegration. 

> [!NOTE]
> Tilknytningen viser, hvilke oplysninger der synkroniseres fra Sales til Supply Chain Management.

### <a name="contact-to-contact"></a>Kontakt til kontakt

![Skabelontilknytning i dataintegrator](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>Kontakt til kunde

![Skabelontilknytning i dataintegrator](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>Relaterede emner

[Kundeemne til kontanter](prospect-to-cash.md)

[Synkronisere konti direkte fra Sales med kunder i Supply Chain Management](accounts-template-mapping-direct.md)

[Synkronisere produkter direkte fra Supply Chain Management med produkter i Sales](products-template-mapping-direct.md)

[Synkronisere salgshoveder og -linjer direkte fra Supply Chain Management til Sales](sales-order-template-mapping-direct-two-ways.md)

[Synkronisere salgsfakturahoveder og -linjer direkte fra Supply Chain Management til Sales](sales-invoice-template-mapping-direct.md)


