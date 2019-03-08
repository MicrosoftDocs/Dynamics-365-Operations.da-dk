---
title: Synkronisere produkter direkte fra Finance and Operations med produkter i Sales
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Sales.
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
ms.openlocfilehash: feb9fbc066162e2caa9fc5dbaeec2c063ae23060
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "348244"
---
# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a>Synkronisere produkter fra Finance and Operations direkte med produkter i Sales

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Før du kan bruge kundeemne til kontant-løsningen, skal du have kendskab til [Integrere data i Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter direkte fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflow i kundeemne til kontant

Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Finance and Operations og Sales. Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Finance and Operations og Sales. I følgende illustration vises, hvordan data synkroniseres mellem Finance and Operations og Sales.

[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

For at få adgang til de tilgængelige skabeloner, skal du åbne [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration). Vælg **Projekter**, og vælg derefter i øverste højre hjørne **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabeloner og underliggende opgaver bruges til at synkronisere produkter fra Finance and Operations til Sales:

- **Navnet på skabelonen i dataintegration:** Produkter (Fin and Ops til Sales) - Direkte
- **Navnet på opgaven i dataintegrationsprojektet:** Produkter

Der kræves ingen synkroniseringsopgaver, før der kan forekomme synkronisering af produkt.

## <a name="entity-set"></a>Enhedssæt

| Finance and Operations     | Salg    |
|----------------------------|----------|
| Salgbare frigivne produkter | Produkter |

## <a name="entity-flow"></a>Enhedsflow

Produkter administreres i Finance and Operations og synkroniseres til Sales. Dataenheden **Salgbare frigivne produkter** i Finance and Operations eksporterer kun produkter, der er *salgbare*. Salgbare produkter er produkter med de oplysninger, de skal bruge for at kunne bruges på en salgsordre. De samme regler gælder, når et produkt valideres ved brug af funktionen **Valider** på siden **Frigivet produkt**.

Produktnummeret bruges som en nøgle. Når produktvarianter synkroniseres til Sales, har hver produktvariant derfor et individuelt produkt-id.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemne til kontantløsning for Sales

I Sales er tilføjet et nyt felt **Vedligeholdes eksternt** for produkterne, for at angive, at et bestemt produkt vedligeholdes eksternt. Som standard er værdien indstillet til **Ja** under import til Sales. Følgende værdier er tilgængelige:

- **Ja** – Produktet stammer fra Finance and Operations, og kan ikke redigeres i Sales.
- **Nej** – Produktet blev angivet direkte i Sales.
- **(Tom)** – Produktet fandtes i Sales, før kundeemne til kontanter-løsningen blev aktiveret.

Feltet **Vedligeholdes eksternt** bruges til at sikre, at det kun er tilbud og salgsordrer med eksternt vedligeholdte produkter, der synkroniseres til Finance and Operations.

Eksternt vedligeholdte produkter føjes automatisk til den første gyldige prisliste, der har den samme valuta. Prislister organiseres alfabetisk efter navn. Produktets salgspris fra Finance and Operations bruges som prisen på prislisten. Derfor skal der være en prisliste i Sales for hver produktsalgsvaluta i Finance and Operations. Valutaen for de frigivne salgbare produkter indstilles til regnskabsvalutaen i den juridiske enhed, som produktet eksporteres fra.

> [!NOTE]
> - Produktsynkronisering lykkes ikke, medmindre der er en prisliste, der har en tilsvarende valuta.
> - Du kan styre den anvendte prisliste til integrationen ved at tilknytte pricelevelid.name [standardprisliste (navn)] i dataintegrationsprojektet. Inputtet skal skrives med små bogstaver. For eksempel vil standarden for en prisliste i Sales, der hedder 'Standard', være: Destinationsfelt: pricelevelid.name [standardprisliste (navn)] og tilknytningstype: [ { "transformType": "Standard", "defaultValue": "standard" } ].

## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning

- Inden du kører synkronisering for første gang, skal du udfylde tabellen Specifikt produkt for de eksisterende produkter i Finance and Operations. Eksisterende produkter bliver ikke synkroniseret, før dette job er fuldført.

    1. I Finance and Operations skal du bruge funktionen Søg til at søge efter **Udfyld tabel for specifik produkt**.
    2. Vælg **Udfyld tabel for specifikt produkt** for at køre jobbet. Dette job skal kun køres én gang.

- Sørg for, at den krævede værditilknytning for salgsmåleenheden (UOM) mellem Finance and Operations og Sales findes i tilknytningen for **SalesUnitSymbol** til **DefaultUnit (Name)**.
- Opdater værditilknytningen for **Enhedsgruppe** (**defaultuomscheduleid.name**), så den svarer til **Enhedsgrupper** i Sales.

    Standardskabelonværdien er **Standardenhed**.

- Sørg for, at salgsmåleenhederne for alle produkter fra Finance and Operations findes i Sales.
- Sørg for, at der findes prislister i Sales for alle produktsalgsvalutaer i Finance and Operations.
- Når produkter oprettes i Sales, kan de have statussen **Kladde** eller **Aktiv**. Denne funktion styres i **Indstillinger** > **Administration** > **Systemindstillinger** > **Sales** i Sales.

    Produkter, der har status **Kladde**, når de oprettes, skal aktiveres, før de kan føjes til tilbud eller salgsordrer.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser et eksempel på en skabelontilknytning i dataintegration. 

> [!NOTE]
> Tilknytningen viser, hvilke oplysninger der synkroniseres fra Sales til Finance and Operations.

![Skabelontilknytning i dataintegrator](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Relaterede emner

[Kundeemne til kontanter](prospect-to-cash.md)

[Synkronisere konti fra direkte fra Sales med debitorer i Finance and Operations](accounts-template-mapping-direct.md)

[Synkronisere kontakter direkte fra Sales med kontakter eller debitorer i Finance and Operations](contacts-template-mapping-direct.md)

[Synkronisere salgsordrehoveder og linjer fra Finance and Operations direkte med Sales](sales-order-template-mapping-direct-two-ways.md)

[Synkronisere salgsfakturahoveder og -linjer direkte fra Finance and Operations til Sales](sales-invoice-template-mapping-direct.md)



