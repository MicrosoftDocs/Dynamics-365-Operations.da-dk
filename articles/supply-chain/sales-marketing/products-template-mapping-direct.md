---
title: Synkronisere produkter direkte fra Supply Chain Management med produkter i Sales
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Dynamics 365 Supply Chain Management til Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: ecee843b6c09c86b4e40ab34cc113e5a7e7c76f8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977682"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a>Synkronisere produkter direkte fra Supply Chain Management med produkter i Sales

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Før du kan bruge kundeemne til kontant-løsningen, skal du have kendskab til [Integrere data i Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter direkte fra Dynamics 365 Supply Chain Management til Dynamics 365 Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflow i kundeemne til kontant

Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Supply Chain Management og Sales. Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om konti, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Supply Chain Management og Sales. I følgende illustration vises, hvordan data synkroniseres mellem Supply Chain Management og Sales.

[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

For at få adgang til de tilgængelige skabeloner skal du åbne [Power Apps Administration](https://admin.powerapps.com/dataintegration). Vælg **Projekter**, og vælg derefter i øverste højre hjørne **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabelon og underliggende opgaver bruges til at synkronisere produkter fra Supply Chain Management til Sales.

- **Navnet på skabelonen i dataintegration:** Produkter (Supply Chain Management til Sales) - Direkte
- **Navnet på opgaven i dataintegrationsprojektet:** Produkter

Der kræves ingen synkroniseringsopgaver, før der kan forekomme synkronisering af produkt.

## <a name="entity-set"></a>Enhedssæt

| Supply Chain Management    | Salg    |
|----------------------------|----------|
| Salgbare frigivne produkter | Produkter |

## <a name="entity-flow"></a>Enhedsflow

Produkter administreres i Supply Chain Management og synkroniseres til Sales. Dataenheden **Salgbare frigivne produkter** i Supply Chain Management eksporterer kun produkter, der er *salgbare*. Salgbare produkter er produkter med de oplysninger, de skal bruge for at kunne bruges på en salgsordre. De samme regler gælder, når et produkt valideres ved brug af funktionen **Valider** på siden **Frigivet produkt**.

Produktnummeret bruges som en nøgle. Når produktvarianter synkroniseres til Sales, har hver produktvariant derfor et individuelt produkt-id.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemne til kontantløsning for Sales

I Sales er tilføjet et nyt felt **Vedligeholdes eksternt** for produkterne, for at angive, at et bestemt produkt vedligeholdes eksternt. Som standard er værdien indstillet til **Ja** under import til Sales. Følgende værdier er tilgængelige:

- **Ja** – Produktet stammer fra Supply Chain Management, og det kan ikke redigeres i Sales.
- **Nej** – Produktet blev angivet direkte i Sales.
- **(Tom)** – Produktet fandtes i Sales, før kundeemne til kontanter-løsningen blev aktiveret.

Feltet **Vedligeholdes eksternt** bruges til at sikre, at det kun er tilbud og salgsordrer med eksternt vedligeholdte produkter, der synkroniseres til Supply Chain Management.

Eksternt vedligeholdte produkter føjes automatisk til den første gyldige prisliste, der har den samme valuta. Prislister organiseres alfabetisk efter navn. Produktets salgspris fra Supply Chain Management bruges som prisen på prislisten. Derfor skal der være en prisliste i Sales for hver produktsalgsvaluta i Supply Chain Management. Valutaen for de frigivne salgbare produkter indstilles til regnskabsvalutaen i den juridiske enhed, som produktet eksporteres fra.

> [!NOTE]
> - Produktsynkronisering lykkes ikke, medmindre der er en prisliste, der har en tilsvarende valuta.
> - Du kan styre den anvendte prisliste til integrationen ved at tilknytte pricelevelid.name [standardprisliste (navn)] i dataintegrationsprojektet. Inputtet skal skrives med små bogstaver. For eksempel vil standarden for en prisliste i Sales, der hedder 'Standard', være: Destinationsfelt: pricelevelid.name [standardprisliste (navn)] og tilknytningstype: [ { "transformType": "Standard", "defaultValue": "standard" } ].

## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning

- Inden du kører synkronisering for første gang, skal du udfylde tabellen Specifikt produkt for de eksisterende produkter i Supply Chain Management. Eksisterende produkter bliver ikke synkroniseret, før dette job er fuldført.

    1. I Supply Chain Management skal du bruge funktionen Søg til at søge efter **Udfyld tabel for specifikt produkt**.
    2. Vælg **Udfyld tabel for specifikt produkt** for at køre jobbet. Dette job skal kun køres én gang.

- Sørg for, at den krævede værditilknytning for salgsmåleenheden mellem Supply Chain Management og Sales findes i tilknytningen af **SalesUnitSymbol** til **DefaultUnit (Name)**.
- Opdater værditilknytningen for **Enhedsgruppe** (**defaultuomscheduleid.name**), så den svarer til **Enhedsgrupper** i Sales.

    Standardskabelonværdien er **Standardenhed**.

- Sørg for, at salgsmåleenhederne for alle produkter fra Supply Chain Management findes i Sales.
- Sørg for, at der findes prislister i Sales for alle produktsalgsvalutaer i Supply Chain Management.
- Når produkter oprettes i Sales, kan de have statussen **Kladde** eller **Aktiv**. Denne funktion styres i **Indstillinger** > **Administration** > **Systemindstillinger** > **Sales** i Sales.

    Produkter, der har status **Kladde**, når de oprettes, skal aktiveres, før de kan føjes til tilbud eller salgsordrer.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser et eksempel på en skabelontilknytning i dataintegration. 

> [!NOTE]
> Tilknytningen viser, hvilke oplysninger der synkroniseres fra Sales til Supply Chain Management.

![Skabelontilknytning i dataintegrator](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Relaterede emner

[Kundeemne til kontanter](prospect-to-cash.md)

[Synkronisere konti direkte fra Sales med kunder i Supply Chain Management](accounts-template-mapping-direct.md)

[Synkronisere kontakter direkte fra Sales med kontakter eller kunder i Supply Chain Management](contacts-template-mapping-direct.md)

[Synkronisering af salgsordrer direkte mellem Sales og Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[Synkronisere salgsfakturahoveder og -linjer direkte fra Supply Chain Management til Sales](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]