---
title: Synkronisere produkter fra Finance and Operations til produkter i Sales
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations Enterprise edition til Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2f14b06b57930256f9211f2085512aa589df083e
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a>Synkronisere produkter fra Finance and Operations til produkter i Sales

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Før du kan bruge kundeemnet til kontantløsning, skal du have kendskab til [Dynamics 365-dataintegration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration). 

Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations Enterprise edition til Microsoft Dynamics 365 for Sales.

## <a name="template-and-task"></a>Skabelon og opgaver

Følgende skabeloner og underliggende opgaver bruges til at synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations Enterprise edition (Finance and Operations) til Microsoft Dynamics 365 for Sales (Sales).

-   Navnet på skabelonen: Produkter (Finance and Operations til Sales)

-   Navnet på opgaven i projektet: Produkter

Synkroniseringsopgaver, der kræves før produktsynkronisering: Ingen

## <a name="entity-set"></a>Enhedssæt

| **Finance and Operations** | **CDS** | **Sales**  |
|----------------------------|---------|------------|
| Salgbare frigivne produkter | Produkt | Produkter   |

## <a name="entity-flow"></a>Enhedsflow

Produkter administreres i Finance and Operations og synkroniseres til Sales. Dataenheden **Salgbare frigivne produkter** i Finance and Operations eksporterer kun produkter, der er salgbare, hvilket betyder, at produkter de oplysninger, der skal bruges i en salgsordre. De samme regler gælder, når et produkt valideres med funktionen **Valider** på siden **Frigivet produkt**.

**Produktnummer** bruges som nøgle, hvilket betyder, at produktvarianter synkroniseres til CDS og Sales med individuelle **Produkt-id'er** pr. **Produktvariant**.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemne til kontantløsning for Sales

I Sales tilføjes et nyt felt for produkterne, **Vedligeholdes eksternt**, for at angive, at et bestemt produkt vedligeholdes eksternt. Værdien er indstillet til **Ja** som standard under import til Sales.

-   **Vedligeholdes eksternt = Ja**: Produktet stammer fra Finance and Operations og kan ikke redigeres i Sales.

-   **Vedligeholdes eksternt = Nej**: Produkt angives direkte i Sales.

-   **Vedligeholdes eksternt = Tom**: Produktet findes i Sales før aktivering af løsningen Kundeemne-til-kontant.

Oplysningerne i **Vedligeholdes eksternt** bruges til at sikre, at det kun er **Tilbud** og **Salgsordrer** med **eksternt vedligeholdte produkter** der synkroniseres til Finance and Operations.

**Eksternt vedligeholdte produkter** føjes automatisk til den første gyldige **Prisliste** med den samme valuta. Bemærk, at listen er organiseret alfabetisk efter **Navn**. Produktets salgspris fra Finance and Operations bruges som pris på **Prisliste**. Det betyder, at det er nødvendigt at have en **prisliste** i Sales for hver **Produktsalgsvaluta** i Finance and Operations. Valutaen for de endelige salgbare produkter indstilles til regnskabsvalutaen i den juridiske enhed, som produktet eksporteres fra.

> [!NOTE]
> Produktsynkroniseringen mislykkes uden en **prisliste** med den tilsvarende valuta.

## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning

-   Inden du kører den allerførste synkronisering, skal du udfylde de **Tabel for specifik produkt** for eksisterende produkter i Finance and Operations. Eksisterende produkter bliver ikke synkroniseret, før dette job er fuldført.

    -   I Finance and Operations skal du bruge funktionen Søg til at søge efter **Udfyld tabel for specifik produkt**.

    -   Klik på **Udfyld tabel for specifik produkt** for at køre jobbet. Dette job skal kun køres én gang.

-   Kontroller, at den påkrævede **ValueMap** for salg af **Måleenhed** (UOM) i Finance and Operations findes i **Kilde -\> CDS-tilknytning af SalesUnitSymbol/DefaultSellingUnitOfMeasure**.

-   Kontroller, at **Understøttede decimaler** for måleenheden opfylder dit behov i **CDS -\> Destination**. Hvis du har brug for forskellige værdier pr. måleenhed, kan dette gøres med **ValueMap** fra Enhed, f.eks. [Hver: 0] & [Pund: 2].

    -   Standardskabelonværdien 0 anvendes.

-   Opdater **CDS-organisations-id Organization_OrganizationId** i **Kilde -\> CDS**.

    -   Standardskabelonværdien ORG001 anvendes.

-   Opdater **ValueMap** for **Enhedsgruppe** (**defaultuomscheduleid.name**) i **CDS -\> Destination**, s den stemmer overens med **Enhedsgrupper** i Sales.

    -   Standardskabelonværdien for **Standardenhed** anvendes.

-   Kontroller, at alle produkter, der sælger måleenheder fra Finance and Operations, findes i Sales med værdien **CDS-pluklister**.

-   Kontroller, at **Prislister** findes i Sales for hvert produktsalgsvaluta i Finance and Operations.

-   Du kan oprette produkter i Sales med status **Kladde** eller **Aktiv**. Dette styres i **Systemindstillinger** under **Salg** i Sales.

    -   Produkter, der er oprettet med kladdestatus, skal aktiveres, før de kan føjes til **Tilbud** eller **Salgsordre**.

## <a name="template-mapping-in-data-integrator"></a>Tilknytning af skabelon i dataintegrator

Følgende illustration viser et eksempel på en skabelontilknytning i dataintegrator.

![tilknytning af skabelon i dataintegrator](./media/products-template-mapping-data-integrator-1.png)

![tilknytning af skabelon for produkter i dataintegrator](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Relaterede emner

[Synkronisere konti fra Sales med kunder i Finance and Operations](accounts-template-mapping.md)

[Synkronisere kontaktpersoner fra Sales med kontaktpersoner eller kunder i Finance and Operations](contacts-template-mapping.md)

[Synkronisere salgstilbudshoveder og -linjer fra Sales til Finance and Operations](sales-quotation-template-mapping.md)


