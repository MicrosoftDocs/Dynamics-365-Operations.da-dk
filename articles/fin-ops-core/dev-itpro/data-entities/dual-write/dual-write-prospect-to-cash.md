---
title: Kundeemner til kontanter og to skrivninger
description: I dette emne får dig oplysninger om kundeemner til kontanter og to skrivninger.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 3b482a2754bb4bcaca5410da72c21897fd066a41
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683641"
---
# <a name="prospect-to-cash-in-dual-write"></a>Kundeemner til kontanter og to skrivninger

[!include [banner](../../includes/banner.md)]



Et vigtigt mål i de fleste virksomheder er at konvertere kundeemner til kunder og derefter vedligeholde et løbende forretningsforhold til disse kunder. I Microsoft Dynamics 365-apps sker kundeemne til kontant-processen gennem tilbud eller ordrebehandlingsarbejdsgange, og finanserne afstemmes og registreres. Integration af kundeemner til kontanter med to skrivninger opretter en arbejdsgang, der tager et tilbud og en ordre, der stammer fra Dynamics 365 Sales eller Dynamics 365 Supply Chain Management, og gør tilbuddet og ordren tilgængeligt i begge apps.

I-app-grænsefladerne kan du få adgang til behandlingsstatus og fakturaoplysninger i realtid. Du kan derfor nemmere administrere funktioner som produktlager, lagerekspedition og -udførelse i styring af Supply Chain Management, uden at skulle oprette tilbud og ordrer igen.

![Dataflow med to skrivninger til kundeemner til kontanter](../dual-write/media/dual-write-prospect-to-cash[1].png)

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning

Før du kan synkronisere salgstilbud, skal du opdatere følgende indstillinger.

### <a name="setup-in-sales"></a>Konfiguration i Sales

Gå til **Indstillinger \> Administration \> Systemindstillinger \> Salg** i Sales, og sørg for, at der bruges til følgende indstillinger:

- Systemindstillingen **Brug systemets prisberegningssystem** er angivet til **Ja**.
- Feltet **Rabatberegningsmetode** er angivet til **Linjeelement**.

### <a name="sites-and-warehouses"></a>Websteder og lagersteder

I Supply Chain Management skal felterne **Websted** og **Lagersted** udfyldes for tilbudslinjer og ordrelinjer. Hvis du angiver webstedet og lagerstedet i standardordreindstillingerne, angives disse felter automatisk, når du føjer et produkt til en tilbudslinje eller en ordrelinje. 

### <a name="number-sequences-for-quotations-and-orders"></a>Nummerserier til tilbud og ordrer

Nummerserierne til Supply Chain Management og Sales forbindes ikke, når tilbud og ordrer oprettes og synkroniseres i Sales og Supply Chain Management. Hvis en salgsordre, der er oprettet i Sales, synkroniseres med Supply Chain Management, har den samme salgsordrenummer i Supply Chain Management. Du skal bruge forskellige nummerserie systemer i de to apps for at sikre, at salgsordrenummeret ikke er duplikeret.

Hvis nummerserien i Supply Chain Management f.eks. er **1, 2, 3, 4, 5,...**, og nummerserien i Sales er **100, 99, 98,...**. Hvis du opretter 100 salgsordrer i Sales, vil der efterhånden blive genereret et ordrenummer, som allerede findes i Supply Chain Management. Med andre ord vil de to nummerserier senere overlappe, efterhånden som der oprettes salgsordrer i Supply Chain Management og Sales. Du kan i stedet bruge en nummerserie som f.eks. **F1, F2, F3,...** i Supply Chain Management og en nummerserie som f.eks. **C1, C2, C3,...** i Sales. Disse nummerserier medfører aldrig identiske salgsordrenumre.

## <a name="sales-quotations"></a>Salgstilbud

Salgstilbud kan oprettes i Sales eller i Supply Chain Management. Hvis du opretter et tilbud i Sales, synkroniseres det med Supply Chain Management i realtid. Hvis du tilsvarende opretter et tilbud i Supply Chain Management, synkroniseres det med Sales i realtid. Vær opmærksom på følgende punkter:

+ Du kan føje en rabat til produktet i tilbuddet. I dette tilfælde synkroniseres rabatten med Supply Chain Management. Felterne **Rabat**, **Gebyrer** og **Moms** i hovedet styres af en opsætning i Supply Chain Management. Denne opsætning understøtter ikke integrationstilknytning. I stedet administreres og håndteres felterne **Pris**, **Rabat**, **Tillæg** og **Moms** af Supply Chain Management.
+ Felterne **Rabatprocent**, **Rabat** og **Fragtbeløb** i salgstilbuddets overskrift er skrivebeskyttede.
+ Felterne **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** er ikke del af standardtilknytningerne. Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.

Hvis du også bruger løsningen Field Service, skal du sørge for at aktivere parameteren **Opret hurtigt tilbudslinjen** igen. Hvis du aktiverer parameteren igen, kan du fortsætte med at oprette tilbudslinjer ved hjælp af funktionen til hurtig oprettelse.
1. Naviger til dit Dynamics 365 Sales-program.
2. Vælg ikonet Indstillinger på den øverste navigationslinje.
3. Vælg **Avancerede indstillinger**.
4. Vælg indstillingen **Tilpas systemet**.
5. Vælg menupunktet **Tilbudslinje**.
6. Gå til området **Datatjenester**, og markér afkrydsningsfeltet **Tillad hurtig oprettelse**.

## <a name="sales-orders"></a>Salgsordre

Salgstilbud kan oprettes i Sales eller i Supply Chain Management. Hvis du opretter et salgstilbud i Sales, synkroniseres det med Supply Chain Management i realtid. Hvis du tilsvarende opretter et salgstilbud i Supply Chain Management, synkroniseres det med Sales i realtid. Vær opmærksom på følgende punkter:

+ Produkter, der skal rekvireres på Dynamics 365 Sales, vises som produktkategorier i Dynamics 365 Supply Chain Management.
+ Beregning og afrunding af rabat:

    - Rabatberegningsmodellen i Sales adskiller sig fra rabatberegningsmodellen i Supply Chain Management. I Supply Chain Management kan det endelige rabatbeløb på en salgslinje være resultatet af en kombination af rabatbeløb og rabatprocenter. Hvis dette endelige rabatbeløb divideres med antallet på linjen, kan afrunding forekomme. Denne afrunding tages imidlertid ikke i betragtning, hvis et afrundet rabatbeløb pr. enhed synkroniseres med Sales. Det fulde beløb skal synkroniseres uden at blive divideret med linjeantallet for at sikre, at det fulde rabatbeløb fra en salgslinje i Supply Chain Management synkroniseres korrekt til Sales. Derfor skal du definere rabatberegningsmetoden som **Linjeelement** i Sales.
    - Når en salgsordrelinje synkroniseres fra Sales til Supply Chain Management, bruges hele linjerabatbeløbet. Da Supply Chain Management ikke har noget felt, der kan gemme det fulde rabatbeløb for en linje, divideres beløbet med antallet og gemmes i feltet **Linjerabat**. En eventuel afrunding, der opstår under denne division, gemmes i feltet **Salgsgebyrer** på salgslinjen.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Eksempel: Synkronisering fra Sales til Supply Chain Management

Du har følgende salgsordrer:

+ **Sales:** Antal = 3, pr. linje-rabat = $10,00
+ **Supply Chain Management:** antal = 3, linjerabatbeløb = $3,33, salgsgebyr = –$0,01

Hvis du synkroniserer fra Supply Chain Management til Sales, får du følgende resultat:

+ **Supply Chain Management:** antal = 3, linjerabatbeløb = $3,33, salgsgebyr = –$0,01
+ **Sales:** Antal = 3, pr. linje-rabat = (3 × $3,33) + $0,01 = $10,00

## <a name="dual-write-solution-for-sales"></a>Løsning med to skrivninger til Sales

Nye felter er føjet til enheden **Ordre** og vises på siden. De fleste af disse felter vises under fanen **Integration** i Sales. Yderligere oplysninger om, hvordan statusfelterne tilknyttes, finder du under [Konfigurere tilknytningen af statusfelter for salgsordre](sales-status-map.md).

+ Knapperne **Opret faktura** og **Annuller ordre** på siden **Salgsordre** er skjult i Sales.
+ Værdien **Salgsordrestatus** forbliver **Aktiv** for at sikre, at ændringer fra Supply Chain Management kan strømme til salgsordren i Sales. Standardværdien for **Statecode \[Status\]** skal angives til **Aktiv** for at styre denne funktion.

## <a name="invoices"></a>Fakturaer

Salgsfakturaer oprettes i Supply Chain Management og synkroniseres til Sales. Vær opmærksom på følgende punkter:

+ Feltet **Fakturanummer** er føjet til enheden **Faktura** og vises på siden.
+ Knappen **Opret faktura** på siden **Salgsordre** er skjult, da fakturaer oprettes i Supply Chain Management og synkroniseres til Sales. Siden **Faktura** kan ikke redigeres, fordi fakturaer synkroniseres fra Supply Chain Management.
+ Værdien **Salgsordrestatus** ændres automatisk til **Faktureret**, når den relaterede faktura fra Supply Chain Management er blevet synkroniseret til Sales. Desuden tildeles ejeren af den salgsordre, hvorfra fakturaen blev oprettet, som ejer af fakturaen. Ejeren af salgsordren kan derfor få vist fakturaen.
+ Felterne **Fragtvilkår**, **Leveringsbetingelser** og **Leveringstilstand** indgår ikke i standardtilknytningerne. Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.

## <a name="templates"></a>Skabeloner

Kundeemne til kontant omfatter en samling af centrale tabeltilknytninger, der arbejder sammen under datainteraktion, som vist i følgende tabel.

| Finance and Operations-apps | Modelstyrede apps i Dynamics 365 | Beskrivende tekst |
|-----------------------------|-----------------------------------|-------------|
| Salgsfakturahoveder V2    | fakturaer                          |             |
| Salgsfakturalinjer V2      | invoicedetails                    |             |
| CDS-salgsordrehoveder     | salesorders                       |             |
| CDS-salgsordrelinjer       | salesorderdetails                 |             |
| Koder for salgsordreoprindelse    | msdyn\_salgsordreoprindelser          |             |
| CDS-salgstilbudshoved  | pristilbud                            |             |
| CDS-salgstilbudslinjer   | quotedetails                      |             |

Her er de relaterede kernetabeltilknytninger for kundeemne til kontant:

+ [Debitorer V3 til konti](customer-mapping.md#customers-v3-to-accounts)
+ [CDS kontakter V2 til kontakter](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [Debitorer V3 til kontakter](customer-mapping.md#customers-v3-to-contacts)
+ [Frigivne produkter V2 til msdyn_sharedproductdetails](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [Alle produkter til msdyn_globalproducts](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [Prisliste](product-mapping.md)

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]