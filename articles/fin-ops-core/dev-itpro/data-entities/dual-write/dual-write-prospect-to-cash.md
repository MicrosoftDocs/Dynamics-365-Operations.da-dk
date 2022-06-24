---
title: Kundeemner til kontanter og dobbeltskrivning
description: Denne artikel indeholder oplysninger om kundeemner til kontanter i dobbeltskrivning.
author: RamaKrishnamoorthy
ms.date: 01/07/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: f0d5339190f7e2aff7b084fa73e559af28e10ee8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860103"
---
# <a name="prospect-to-cash-in-dual-write"></a>Kundeemner til kontanter og dobbeltskrivning

[!include [banner](../../includes/banner.md)]

Et vigtigt mål i de fleste virksomheder er at konvertere kundeemner til kunder og derefter vedligeholde et løbende forretningsforhold til disse kunder. I Microsoft Dynamics 365-apps sker kundeemne til kontant-processen gennem tilbud eller ordrebehandlingsarbejdsgange, og finanserne afstemmes og registreres. Integration af kundeemner til kontanter med to skrivninger opretter en arbejdsgang, der tager et tilbud og en ordre, der stammer fra Dynamics 365 Sales eller Dynamics 365 Supply Chain Management, og gør tilbuddet og ordren tilgængeligt i begge apps.

I-app-grænsefladerne kan du få adgang til behandlingsstatus og fakturaoplysninger i realtid. Du kan derfor nemmere administrere funktioner som produktlager, lagerekspedition og -udførelse i styring af Supply Chain Management, uden at skulle oprette tilbud og ordrer igen.

![Dataflow med to skrivninger til kundeemner til kontanter.](../dual-write/media/dual-write-prospect-to-cash[1].png)

Du kan finde oplysninger om integration af kunder og kontakter i [Integreret kundemaster](customer-mapping.md). Du kan finde oplysninger om produktintegration i [Samlet produktoplevelse](product-mapping.md).

> [!NOTE]
> I Dynamics 365 Sales refererer både kundeemne og kunde til en post i tabellen **Konto**, hvor kolonnen **RelationshipType** er enten **Kundeemne** eller **Kunde**. Hvis din forretningslogik omfatter en **Konto**-kvalificeringsproces, hvor posten **Konto** oprettes og kvalificeres som et kundeemne først og derefter som en kunde, synkroniseres denne post kun til Finans og drift-appen, når den er en kunde (`RelationshipType=Customer`). Hvis rækken **Konto** skal synkroniseres som et kundeemne, skal du have en brugerdefineret tilknytning til integration af kundeemnedataene.

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning

Før du kan synkronisere salgstilbud, skal du opdatere følgende indstillinger.

### <a name="setup-in-sales"></a>Konfiguration i Sales

Gå til **Indstillinger \> Administration \> Systemindstillinger \> Salg** i Sales, og sørg for, at der bruges til følgende indstillinger:

- Indstillingen **Brug systemets prisberegningssystem** er angivet til **Ja**.
- Kolonnen **Rabatberegningsmetode** er angivet til **Linjeelement**.

### <a name="sites-and-warehouses"></a>Websteder og lagersteder

I Supply Chain Management skal kolonnerne **Lokation** og **Lagersted** udfyldes for tilbudslinjer og ordrelinjer. Hvis du angiver lokationen og lagerstedet i standardordreindstillingerne, angives disse kolonner automatisk, når du føjer et produkt til en tilbudslinje eller en ordrelinje. 

### <a name="number-sequences-for-quotations-and-orders"></a>Nummerserier til tilbud og ordrer

Nummerserierne til Supply Chain Management og Sales forbindes ikke, når tilbud og ordrer oprettes og synkroniseres i Sales og Supply Chain Management. Hvis en salgsordre, der er oprettet i Sales, synkroniseres med Supply Chain Management, har den samme salgsordrenummer i Supply Chain Management. Du skal bruge forskellige nummerserie systemer i de to apps for at sikre, at salgsordrenummeret ikke er duplikeret.

Hvis nummerserien i Supply Chain Management f.eks. er **1, 2, 3, 4, 5,...**, og nummerserien i Sales er **100, 99, 98,...**. Hvis du opretter 100 salgsordrer i Sales, vil der efterhånden blive genereret et ordrenummer, som allerede findes i Supply Chain Management. Med andre ord vil de to nummerserier senere overlappe, efterhånden som der oprettes salgsordrer i Supply Chain Management og Sales. Du kan i stedet bruge en nummerserie som f.eks. **F1, F2, F3,...** i Supply Chain Management og en nummerserie som f.eks. **C1, C2, C3,...** i Sales. Disse nummerserier medfører aldrig identiske salgsordrenumre.

## <a name="sales-quotations"></a>Salgstilbud

Salgstilbud kan oprettes i Sales eller i Supply Chain Management. Hvis du opretter et tilbud i Sales, synkroniseres det med Supply Chain Management i realtid. Hvis du tilsvarende opretter et tilbud i Supply Chain Management, synkroniseres det med Sales i realtid. Vær opmærksom på følgende punkter:

+ Du kan føje en rabat til produktet i tilbuddet. I dette tilfælde synkroniseres rabatten med Supply Chain Management. Kolonnerne **Rabat**, **Gebyrer** og **Moms** i hovedet styres af en opsætning i Supply Chain Management. Denne opsætning understøtter ikke integrationstilknytning. I stedet administreres og håndteres kolonnerne **Pris**, **Rabat**, **Gebyr** og **Moms** af Supply Chain Management.
+ Kolonnerne **Rabatprocent**, **Rabat** og **Fragtbeløb** i salgstilbuddets overskrift er skrivebeskyttede kolonner.
+ Kolonnerne **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** er ikke del af standardtilknytningerne. Hvis du vil tilknytte disse kolonner, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som tabellen synkroniseres mellem.

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
    - Når en salgsordrelinje synkroniseres fra Sales til Supply Chain Management, bruges hele linjerabatbeløbet. Da Supply Chain Management ikke har nogen kolonne, der kan gemme det fulde rabatbeløb for en linje, divideres beløbet med antallet og gemmes i kolonnen **Linjerabat**. En eventuel afrunding, der opstår under denne division, gemmes i kolonnen **Salgsgebyrer** på salgslinjen.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Eksempel: Synkronisering fra Sales til Supply Chain Management

Du har følgende salgsordrer:

+ **Sales:** Antal = 3, pr. linje-rabat = $10,00
+ **Supply Chain Management:** antal = 3, linjerabatbeløb = $3,33, salgsgebyr = –$0,01

Hvis du synkroniserer fra Supply Chain Management til Sales, får du følgende resultat:

+ **Supply Chain Management:** antal = 3, linjerabatbeløb = $3,33, salgsgebyr = –$0,01
+ **Sales:** Antal = 3, pr. linje-rabat = (3 × $3,33) + $0,01 = $10,00

## <a name="dual-write-solution-for-sales"></a>Løsning med to skrivninger til Sales

Nye kolonner er føjet til tabellen **Ordre** og vises på siden. De fleste af disse kolonner vises under fanen **Integration** i Sales. Yderligere oplysninger om, hvordan statuskolonnerne tilknyttes, finder du under [Konfigurere tilknytningen af statuskolonner for salgsordre](sales-status-map.md).

+ Knapperne **Opret faktura** og **Annuller ordre** på siden **Salgsordre** er skjult i Sales.
+ Værdien **Salgsordrestatus** forbliver **Aktiv** for at sikre, at ændringer fra Supply Chain Management kan strømme til salgsordren i Sales. Standardværdien for **Statecode \[Status\]** skal angives til **Aktiv** for at styre denne funktion.

## <a name="invoices"></a>Fakturaer

Salgsfakturaer oprettes i Supply Chain Management og synkroniseres til Sales. Vær opmærksom på følgende punkter:

+ Kolonnen **Fakturanummer** er føjet til tabellen **Faktura** og vises på siden.
+ Knappen **Opret faktura** på siden **Salgsordre** er skjult, da fakturaer oprettes i Supply Chain Management og synkroniseres til Sales. Siden **Faktura** kan ikke redigeres, fordi fakturaer synkroniseres fra Supply Chain Management.
+ Værdien **Salgsordrestatus** ændres automatisk til **Faktureret**, når den relaterede faktura fra Supply Chain Management er blevet synkroniseret til Sales. Desuden tildeles ejeren af den salgsordre, hvorfra fakturaen blev oprettet, som ejer af fakturaen. Ejeren af salgsordren kan derfor få vist fakturaen.
+ Kolonnerne **Fragtvilkår**, **Leveringsbetingelser** og **Leveringstilstand** indgår ikke i standardtilknytningerne. Hvis du vil tilknytte disse kolonner, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som tabellen synkroniseres mellem.

## <a name="templates"></a>Skabeloner

Kundeemne til kontant omfatter en samling af centrale tabeltilknytninger, der arbejder sammen under datainteraktion, som vist i følgende tabel.

| Finans og drift-apps | Kundeengagementapps | Beskrivende tekst |
|-----------------------------|-----------------------------------|-------------|
[Alle produkter](mapping-reference.md#138) | msdyn_globalproducts | |
[Debitorer V3](mapping-reference.md#101) | konti | |
[Debitorer V3](mapping-reference.md#116) | kontakter | |
[Kontakter V2](mapping-reference.md#221) | msdyn_contactforparties | |
[CDS-salgsordrehoveder](mapping-reference.md#217) | salesorders | |
[CDS-salgsordrelinjer](mapping-reference.md#216) | salesorderdetails | |
[CDS-salgstilbudshoved](mapping-reference.md#215) | pristilbud | |
[CDS-salgstilbudslinjer](mapping-reference.md#214) | quotedetails | |
[Frigivne produkter V2](mapping-reference.md#189) | msdyn_sharedproductdetails | |
[Salgsfakturahoveder V2](mapping-reference.md#118) | fakturaer | Tabellen Salgsfakturahoveder V2 i Finans og drift-appen indeholder fakturaer for salgsordrer og fritekstfakturaer. Der anvendes et filter i Dataverse for dobbeltskrivning, der filtrerer alle dokumenter med fritekstfakturaer ud. |
[Salgsfakturalinjer V2](mapping-reference.md#117) | invoicedetails | |
[Koder for salgsordreoprindelse](mapping-reference.md#186) | msdyn_salesorderorigins | |

Du kan finde oplysninger om prislister i [Samlet produktoplevelse](product-mapping.md).

## <a name="limitations"></a>Begrænsninger

- Returordrer understøttes ikke.
- Kreditnotaer understøttes ikke.
- Økonomiske dimensioner skal angives for masterdata, f.eks. debitor og kreditor. Når en kunde føjes til et tilbud eller en salgsordre, flyttes de økonomiske dimensioner, der er knyttet til kundeposten, automatisk til ordren. Aktuelt omfatter dobbeltskrivning ikke økonomiske dimensionsdata for masterdata.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
