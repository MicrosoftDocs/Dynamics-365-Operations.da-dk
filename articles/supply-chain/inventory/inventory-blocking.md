---
title: Lagerblokering
description: Dette emne indeholder en oversigt over lagerblokering, som er en del af kvalitetsinspektionsprocessen i Supply Chain Management. Du kan bruge lagerblokering til at forhindre elementer i at blive behandlet eller forbrugt.
author: perlynne
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58dd5c5b3d7b2f077305fa4d420fc55702acbe7ebba049ae9ac78a1362ff2523
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770282"
---
# <a name="inventory-blocking"></a>Lagerblokering

[!include [banner](../includes/banner.md)]

Dette emne indeholder en oversigt over lagerblokering, som er en del af kvalitetsinspektionsprocessen i Supply Chain Management. Du kan bruge lagerblokering til at forhindre elementer i at blive behandlet eller forbrugt.

Du kan blokere lagervarer på følgende måder:

- Manuelt
- Ved at oprette en kvalitetsordre
- Ved at bruge en proces, der genererer en kvalitetsordre
- Ved at bruge blokering af lagerstatus

## <a name="blocking-items-manually"></a>Blokering af varer manuelt

Du kan blokere et antal varer ved at oprette en postering på siden **Lagerblokering**. Du kan kun manuelt blokere varer, der er en del af den disponible lagerbeholdning. For at blokere et antal manuelt skal du først overveje, om planlagte aktiviteter inkluderer forventede tilgange som et forventet disponibelt antal. Forventede tilgange er blokerede varer, du forventer er tilgængelige som disponibel lagerbeholdning efter en inspektion er fuldført. Du kan opretholde den forventede dato. Indstillingen **Forventede tilgange** er som standard markeret for varer, der er blokeret via en kvalitetsordre. Du kan annullere et manuelt blokeret antal ved at slette posteringen på siden **Lagerblokering**.

## <a name="blocking-items-by-creating-a-quality-order"></a>Blokering af varer ved at oprette en kvalitetsordre

Du kan angive varer, der skal undersøges ved at oprette en kvalitetsordre på siden **Kvalitetsordrer**. Når du opretter en kvalitetsordre, er antallet, som du angiver for en vare, blokeret. Prøveplanen, der er knyttet til en kvalitetsordre kontrollerer kun antallet af varer, der skal inspiceres, ikke antallet, der er blokeret. Antallet, der er angivet på kvalitetsordren, er det antal, der er blokeret, uanset det antal, som prøveplanen angiver skal sendes til inspektion.

> [!NOTE]
> Brug af både batch-udløbsdatoen og funktionen til blokering af lagerstatus understøttes ikke af varedisponering. Dette kan resultere i dobbelt udelukkelse af disponibel lagerbeholdning, som kan opstå under varedisponering. Det anbefales, at du bruger batchdispositionskoder i stedet for lagerstatus til blokering af udløbne batches.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Blokering af varer ved at bruge en proces, der genererer en kvalitetsordre

Hvis en kvalitetsproces angiver, at en vare skal inspiceres, blokeret et antal varen automatisk. Så når der automatisk genereres en kvalitetsordre, kontrollerer den vareprøveplan, der er tilknyttet kvalitetsordren, både antallet af varer, der blokeres, og antal varer, der skal inspiceres. Hvis indstillingen **Fuld spærring** på siden **Vareprøve** er markeret, blokeres det fulde antal på f.eks. en indkøbsordrelinje under inspektionen, uanset vareprøveantallet.

### <a name="example"></a>Eksempel

I følgende eksempel genereres, der en kvalitetsordre, når der bogføres en følgeseddel for en indkøbsordre. På siden **Kvalitetstilknytninger** angav du, at bogføringen af en følgeseddel for en indkøbsordre er den proces, der aktiverer en kvalitetsordre.

|Konfiguration |Brugerhandling |Resultat |
|----|---|---|
| En kvalitetstilknytning angiver, at der ved bogføring af en følgeseddel for en indkøbsordre, skal genereres en kvalitetsordre. Vareprøveopsætningen for kvalitetsordren angiver, at 10 % af antallet på indkøbsordrelinjen skal inspiceres. Hvis indstillingen **Fuld spærring** derudover er markeret i vareprøveopsætningen, skal det fulde antal på indkøbsordrelinjen blokeres under inspektionen, uanset hvilket antal der sendes til inspektion. | Følgesedlen er bogført. | Der genereres en kvalitetsordre. 10 % af indkøbsordreantallet for varen sendes til inspektion. Det fulde antal på indkøbsordrelinjen blokeres. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Blokering af varer ved at bruge blokering af lagerstatus

Du kan angive, hvilke lagerstatusser, der er spærringsstatusser ved hjælp af parameteren **Lagerblokering** på siden **Lagerstatusser**. Du kan ikke bruge lagerstatusser som spærringsstatusser for produktionsordrer, salgsordrer, flytteordrer, udgående posteringer eller projektintegrationer. Brug varer, der har lagerstatus disponibel, til udgående arbejde. Hvis du har varer med statussen **Ødelagt**, og varedisponering køres på disse varer, anses varerne for manglende, og lageret genopfyldes automatisk.

## <a name="take-care-when-blocking-items-that-use-both-inventory-status-blocking-and-quality-order-blocking"></a>Vær forsigtig med at blokere varer, der både bruger lagerstatusblokering og kvalitetsordreblokering

Du kan oprette en kvalitetsordre, der er tilknyttet lager, og som har en lagerstatus, hvor parameteren **Lagerblokering** er aktiveret. I dette tilfælde genererer kvalitetsordren en ekstra lagerblokeringspost ud over den, der er oprettet af lagerstatussen. Da lagerblokeringen for kvalitetsordren har parameteren **Forventede tilgange** aktiveret, genereres der en ekstratransaktion af *Bestilt lagerbeholdning*, som også blokeres af lagerstatussen. Denne kombination kan gøre det svært at forstå betydningen af genererede lagertransaktioner, fordi det vil se ud som, at det samlede blokerede antal overstiger det samlede disponible antal. Lad os undersøge transaktionerne for et eksempel på en tilgang på 10 styk af vare A0001 med en kvalitetsordre, der er genereret for en prøve på 1 styk. Funktionsmåden afhænger også af, om indstillingen **Reservér bestilte varer** er aktiveret på siden **Parametre for lager- og lokationsstyring**.

>[!NOTE]
>Hvis du bruger blokering af lagerstatus og kvalitetsordrer sammen, anbefales det på det kraftigste, at indstillingen **Reservér bestilte varer** er aktiveret.

### <a name="example-with-reserve-ordered-items-enabled"></a>Eksempel med "Reservér bestilte varer" aktiveret

Når **Reservér bestilte varer** er aktiveret, har alle lagerblokeringstransaktioner enten statussen *Reserveret fysisk* eller *Reserveret bestilt*.

| Lagertransaktionsreference | Tilgang | Udsted | Kvantitet | Lokation | Lagersted | Lagerstatus | Adresse | Nummerplade | Kommentar |
|---|---|---|---|---|---|---|---|---|---|
| Indkøbsordre | Købt | | 10 stk | 2 | 24 | Spærring | RECV | receiptLp1 | | 
| Lagerspærring | | Reserveret fysisk | -9 stk | 2 | 24 | Spærring | | | Transaktion genereret af blokering for lagerstatus |
| Lagerspærring | | Reserveret fysisk | -1 stk | 2 | 24 | Spærring | RECV | receiptLp1 | Transaktion, der er genereret af vareprøveblokering for kvalitetsordren |
| Lagerspærring | Bestilt | | 1 stk | 2 | 24 | Spærring | RECV | receiptLp1 | Forventede tilgange fra kvalitetsordrens prøveblokering |
| Lagerspærring | | Reserveret bestilt | 1 stk | 2 | 24 | Spærring | | | Transaktion genereret af blokering for lagerstatus

### <a name="example-with-reserve-ordered-items-disabled"></a>Eksempel med "Reservér bestilte varer" deaktiveret

Når **Reservér bestilte varer** er deaktiveret, kan de forventede tilgange ikke reserveres, da de har statussen *Bestilt*, så der vil være blokering tilbage med status som *I bestilling*.

| Lagertransaktionsreference | Tilgang | Udsted | Kvantitet | Lokation | Lagersted | Lagerstatus | Adresse | Nummerplade | Kommentar |
|---|---|---|---|---|---|---|---|---|---|
| Indkøbsordre | Købt | | 10 stk | 2 | 24 | Spærring | RECV | receiptLp1 | |
| Lagerspærring | | Reserveret fysisk | -9 stk | 2 | 24 | Spærring | | | Transaktion genereret af blokering for lagerstatus |
| Lagerspærring | | Reserveret fysisk | -1 stk | 2 | 24 | Spærring | RECV | receiptLp1 | Transaktion, der er genereret af vareprøveblokering for kvalitetsordren |
| Lagerspærring | Bestilt | | 1 stk | 2 | 24 | Spærring | RECV | receiptLp1 | Forventede tilgange fra kvalitetsordrens prøveblokering |
| Lagerspærring | | I bestilling | 1 stk | 2 | 24 | Spærring | RECV | receiptLp1 | Transaktion genereret af blokering for lagerstatus

Bemærk forskellen i transaktionsstatus og dimensioner mellem de to sager. Derfor anbefales det, at du aktiverer indstillingen **Reservér bestilte varer**.

<!-- KFM: (Enable this section when the feature leaves private preview)

### Disable expected receipts from quality orders that sample blocked inventory feature

To simplify the inventory transactions in the case of quality orders that sample inventory blocked as a consequence of inventory status, the system provides a feature that disables expected receipts from such quality orders. As the expected receipt is in any case immediately blocked by inventory status blocking, there is no reduction of on-hand inventory because of this change.

-->

## <a name="additional-resources"></a>Yderligere ressourcer

[Opret og vedligehold en lagerblokering](tasks/create-maintain-inventory-blocking.md)

[Processer for kvalitetsstyring](quality-management-processes.md)

[Kontrollere kvaliteten af varer](tasks/inspect-quality-goods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]