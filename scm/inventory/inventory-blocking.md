---
title: "Lagerspærring"
description: Denne artikel indeholder en oversigt over lagerblokering, som er en del af kvalitetsinspektionsprocessen i Microsoft Dynamics AX. Du kan bruge lagerblokering til at forhindre elementer i at blive behandlet eller forbrugt.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 0d7e37de63e6c63b5d7942a84de60ef8f3984cde
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-blocking"></a>Lagerspærring

[!include[banner](../includes/banner.md)]


Denne artikel indeholder en oversigt over lagerblokering, som er en del af kvalitetsinspektionsprocessen i Microsoft Dynamics AX. Du kan bruge lagerblokering til at forhindre elementer i at blive behandlet eller forbrugt.

Du kan blokere lagervarer på følgende måder:
-   Manuelt
-   Ved at oprette en kvalitetsordre
-   Ved at bruge en proces, der genererer en kvalitetsordre
-   Ved at bruge blokering af lagerstatus

## <a name="blocking-items-manually"></a>Blokering af varer manuelt
Du kan blokere et antal varer ved at oprette en postering på siden **Lagerblokering**. Du kan kun manuelt blokere varer, der er en del af den disponible lagerbeholdning. For at blokere et antal manuelt skal du først overveje, om planlagte aktiviteter inkluderer forventede tilgange som et forventet disponibelt antal. Forventede tilgange er blokerede varer, du forventer er tilgængelige som disponibel lagerbeholdning efter en inspektion er fuldført. Du kan opretholde den forventede dato. Indstillingen **Forventede tilgange** er som standard markeret for varer, der er blokeret via en kvalitetsordre. Du kan annullere et manuelt blokeret antal ved at slette posteringen på siden **Lagerblokering**.

## <a name="blocking-items-by-creating-a-quality-order"></a>Blokering af varer ved at oprette en kvalitetsordre
Du kan angive varer, der skal undersøges ved at oprette en kvalitetsordre på siden **Kvalitetsordrer**. Når du opretter en kvalitetsordre, er antallet, som du angiver for en vare, blokeret. Prøveplanen, der er knyttet til en kvalitetsordre kontrollerer kun antallet af varer, der skal inspiceres, ikke antallet, der er blokeret. Antallet, der er angivet på kvalitetsordren, er det antal, der er blokeret, uanset det antal, som prøveplanen angiver skal sendes til inspektion.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Blokering af varer ved at bruge en proces, der genererer en kvalitetsordre
Hvis en kvalitetsproces angiver, at en vare skal inspiceres, blokeret et antal varen automatisk. Så når der automatisk genereres en kvalitetsordre, kontrollerer den vareprøveplan, der er tilknyttet kvalitetsordren, både antallet af varer, der blokeres, og antal varer, der skal inspiceres. Hvis indstillingen **Fuld spærring** på siden **Vareprøve** er markeret, blokeres det fulde antal på f.eks. en indkøbsordrelinje under inspektionen, uanset vareprøveantallet.
### <a name="example"></a>Eksempel

I følgende eksempel genereres, der en kvalitetsordre, når der bogføres en følgeseddel for en indkøbsordre. På siden **Kvalitetstilknytninger** angav du, at bogføringen af en følgeseddel for en indkøbsordre er den proces, der aktiverer en kvalitetsordre.

|Konfiguration                                                                     |Brugerhandling                 |Resultat             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| En kvalitetstilknytning angiver, at der ved bogføring af en følgeseddel for en indkøbsordre, skal genereres en kvalitetsordre. Vareprøveopsætningen for kvalitetsordren angiver, at 10 % af antallet på indkøbsordrelinjen skal inspiceres. Hvis indstillingen **Fuld spærring** derudover er markeret i vareprøveopsætningen, skal det fulde antal på indkøbsordrelinjen blokeres under inspektionen, uanset hvilket antal der sendes til inspektion. | Følgesedlen er bogført. | Der genereres en kvalitetsordre. 10 % af indkøbsordreantallet for varen sendes til inspektion. Det fulde antal på indkøbsordrelinjen blokeres. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Blokering af varer ved at bruge blokering af lagerstatus
Du kan angive, hvilke lagerstatusser, der er spærringsstatusser ved hjælp af parameteren **Lagerblokering** på siden **Lagerstatusser**. Du kan ikke bruge lagerstatusser som spærringsstatusser for produktionsordrer, salgsordrer, flytteordrer, udgående posteringer eller projektintegrationer. Brug varer, der har lagerstatus disponibel, til udgående arbejde. Hvis du har varer med statussen **Ødelagt**, og varedisponering køres på disse varer, anses varerne for manglende, og lageret genopfyldes automatisk.



<a name="see-also"></a>Se også
--------

[Opret og vedligehold en lagerblokering (opgaveguide)](https://ax.help.dynamics.com/en/wiki/create-and-maintain-an-inventory-blocking/)

[Processer for kvalitetsstyring](quality-management-processes.md)

[Kontrollere kvaliteten af varer (opgaveguide)](https://ax.help.dynamics.com/en/wiki/inspect-the-quality-of-goods/)




