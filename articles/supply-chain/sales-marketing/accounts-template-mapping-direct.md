---
title: Synkronisere konti direkte fra Sales med kunder i Supply Chain Management
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere konti fra Dynamics 365 Sales med Supply Chain Management.
author: ChristianRytt
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 1bf0da5ba5274b61758bc0efdc2f2167327966ad
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831644"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a>Synkronisere konti direkte fra Sales med kunder i Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Før du kan bruge kundeemne til kontant-løsningen, skal du have kendskab til [Integrere data i Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere konti direkte fra Dynamics 365 Sales med Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflow i kundeemne til kontant

Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Supply Chain Management og Sales.  Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om konti, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Supply Chain Management og Sales. I følgende illustration vises, hvordan data synkroniseres mellem Supply Chain Management og Sales.

[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

For at få adgang til de tilgængelige skabeloner skal du åbne [Power Apps Administration](https://preview.admin.powerapps.com/dataintegration). Vælg **Projekter**, og vælg derefter i øverste højre hjørne **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabelon og underliggende opgave bruges til at synkronisere konti fra Sales med Supply Chain Management:

- **Navnet på skabelonen i dataintegration:** Accounts (Sales to Fin and Ops) - Direct
- **Navnet på opgaven i projektet:** Konti - Kunder

Der kræves ingen synkroniseringsopgaver, før der kan forekomme synkronisering af konto/kunde.

## <a name="entity-set"></a>Enhedssæt

| Salg    | Supply Chain Management |
|----------|------------------------|
| Konti | Debitorer V2           |

## <a name="entity-flow"></a>Enhedsflow

Konti administreres i Sales og synkroniseres med Supply Chain Management som kunder. Egenskaben **Vedligeholdes eksternt** for disse kunder er indstillet til **Ja** for at spore kunder, der stammer fra Sales. Under fakturering bruges disse oplysninger til at filtrere fakturaer, der synkroniseres med Sales.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemne til kontantløsning for Sales

Kolonnen **Kontonummer** er tilgængelig på siden **Konto**. Det er blevet gjort til en naturlig og entydig nøgle for at understøtte integrationen. Funktionen Naturlig nøgle i CRM-løsningen (Customer Relationship Management) kan påvirke kunder, der allerede anvender kolonnen **Kontonummer**, men som ikke bruger en entydige **Kontonummer**-værdier for hver konto. Integrationsløsningen understøtter i øjeblikket ikke denne sag.

Når en ny konto oprettes, og der ikke allerede findes en værdi for **Kontonummer**, oprettes den automatisk ved hjælp af en nummerserie. Værdien består af **ACC** efterfulgt af en stigende nummerserie og et suffiks på seks tegn. Her er et eksempel: **ACC-01000-BVRCPS**

Når integrationsløsningen for Sales anvendes, indstiller et opgraderingsscript kolonnen **Kontonummer** for eksisterende konti i Sales. Hvis der ikke er nogen **Kontonummer**-værdier, bruges den nummerserie, der blev nævnt tidligere.

## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning

- Tilknytningen **CustomerGroupId** skal opdateres til en gyldig værdi i Supply Chain Management. Du kan angive en standardværdi, eller du kan angive værdien ved hjælp af en værditilknytning.

    Standardskabelonværdien er **10**.

- Ved at tilføje følgende tilknytninger kan du hjælpe med at reducere antallet af manuelle påkrævede opdateringer i Supply Chain Management. Du kan bruge en standardværdi eller en værditilknytning fra f.eks. **Land/område** eller **By**.

    - **SiteId** - Et sted er påkrævet for at generere tilbud og salgsordrelinjer i Supply Chain Management. Et standardsted kan hentes fra produktet eller fra kunden fra ordrehovedet.

        Standardskabelonværdien er **1**.

    - **WarehouseId** - Et lagersted er påkrævet for at behandle tilbud og salgsordrelinjer i Supply Chain Management. Et standardlagersted kan hentes fra produktet eller fra kunden fra ordrehovedet i Supply Chain Management.

        Standardskabelonværdien er **13**.

    - **LanguageId** - Et sprog er påkrævet for at generere tilbud og salgsordrer i Supply Chain Management. Som standard bruges sproget fra ordrehovedet fra kunden.

        Standardskabelonværdien er **da**.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

> [!NOTE]
> Kolonnerne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** indgår ikke i standardtilknytningerne. Hvis du vil tilknytte disse kolonner, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som tabellen synkroniseres mellem.

Følgende illustration viser et eksempel på en skabelontilknytning i dataintegration. 

> [!NOTE]
> Tilknytningen viser, hvilke kolonneoplysninger der synkroniseres fra Sales til Supply Chain Management.

![Skabelontilknytning i dataintegration](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Relaterede emner


[Kundeemne til kontanter](prospect-to-cash.md)

[Synkronisere konti direkte fra Sales med kunder i Supply Chain Management](accounts-template-mapping-direct.md)

[Synkronisere kontakter direkte fra Sales med kontakter eller kunder i Supply Chain Management](contacts-template-mapping-direct.md)

[Synkronisering af salgsordrer direkte mellem Sales og Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[Synkronisere salgsfakturahoveder og -linjer direkte fra Supply Chain Management til Sales](sales-invoice-template-mapping-direct.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]