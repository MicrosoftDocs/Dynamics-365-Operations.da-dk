---
title: Emballage og gebyrer
description: "Emballagegebyrer betales med bestemte intervaller til et genbrugsfirma. Der betales et beløb pr. vægtenhed for hvert materiale, som en pakkeenhed består af. Emballagegebyrer beregnes og rapporteres, men der bogføres ingen finansposteringer, da gebyrerne ikke anses som afgifter, der skal betales til en myndighed."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5d7cd7b3d60e9c265a766695b53d8d27ee2a8d0a
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="packing-materials-and-fees"></a>Emballage og gebyrer

[!include[banner](../includes/banner.md)]


Emballagegebyrer betales med bestemte intervaller til et genbrugsfirma. Der betales et beløb pr. vægtenhed for hvert materiale, som en pakkeenhed består af. Emballagegebyrer beregnes og rapporteres, men der bogføres ingen finansposteringer, da gebyrerne ikke anses som afgifter, der skal betales til en myndighed.

Der beregnes emballagevægt og -gebyrer for salgsordrelinjer og for indkøbsordrelinjer.

Du kan definere en eller flere pakkeenheder for en vare, for en pakningsgruppe med varer eller for alle varer. En pakkeenhed består af de emballage, deres vægt og det antal varer, der indgår i pakkeenheden. Der tildeles en emballagekode til hver type emballage, der er defineret. På baggrund af emballagekoden kan du angive en pris for en bestemt periode. Emballagegebyret beregnes på baggrund af disse oplysninger.

| **Bemærk!**                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Selvom firmaet ikke betaler emballagegebyrer, kan du bruge funktionen til at beregne statistik i forbindelse med emballagens vægt. |

## <a name="setup-requirements-for-packing-material-fees"></a>Nødvendige indstillinger for emballagegebyrer
Før du beregner emballagevægt eller emballagegebyrer, eller begge, skal du først oprette følgende stamdata:

-   Pakkegrupper – Opret emballagegrupper, som kan knyttes til varer.
-   Emballagekoder – Opret emballagekoder for hver type emballage, der er defineret.
-   Pakkeenheder – Angiv en pakkeenhed for en vare, for en pakkeenhedsgruppe eller for alle varer. Definer for hver pakkeenhed, hvilken emballage der skal medtages, tilknyt vægt, og angiv konverteringsfaktoren fra lagerenheden i feltet Pakkeenhedsfaktor.
-   Emballagegebyrer – Angiv emballagegebyrer pr. emballagekode. For hver type emballage skal du definere gyldighedsperioden, prisen pr. materiale, valutaen og enheden.

## <a name="packing-units-on-sales-order-lines"></a>Pakkeenheder på salgsordrelinjer
Når du opretter en salgsordrelinje, kontrolleres det, om der er angivet pakkeenheder for varen. Hvis der er angivet pakkeenheder, opdateres salgsordrelinjen med den angivne pakkeenhed og antallet af pakkeenheder. Antallet af pakkeenheder er baseret på det bestilte antal divideret med antallet af varer i den valgte pakkeenhed. Hvis der ikke allerede er angivet en pakkeenhed, kan du manuelt angive en pakkeenhed og et antal pakkeenheder på salgsordrelinjen. Du kan også ændre pakkeenheden og antallet af pakkeenheder, når salgsordrelinjen bogføres. Det er relevant, hvis salgsordrelinjen kun er delvist leveret eller delvist faktureret. Når du fakturerer salgsordren, oprettes der emballageposteringer. Emballageposteringer indeholder emballagevægten for salgslinjen. Du kan også ændre posteringerne, når du har faktureret dem, og derefter oprette nye posteringer.

## <a name="packing-units-on-purchase-order-lines"></a>Pakkeenheder på indkøbsordrelinjer
Emballageposteringer for en indkøbsordrelinje oprettes ikke af systemet. Du opretter transaktioner for fakturerede indkøbsordrelinjer manuelt på siden **Emballageposteringer**.

## <a name="set-up-customer-packagingmaterialfee-license-numbers"></a>Definer kundelicensnumre for emballagegebyr
Hvis kunderne betaler emballagegebyret, skal du angive kundelicensnumre for emballagegebyr på siden **Kunder**. Når en kunde er tildelt et licensnummer, beregnes emballagegebyrer automatisk, når salgsordrer faktureres. Når ordren er faktureret, fjernes markeringen i afkrydsningsfeltet **Beregn gebyr** på siden **Emballageposteringer**, da du ikke behøver at beregne og udskrive en rapport. Du kan udskrive emballagevægten på fakturaen og underrette kunderne om, at de kommer til at betale gebyrerne. 

Hvis firmaet betaler emballagegebyrerne, skal du ikke angive kundelicensnumrene. Når ordren er faktureret, markeres afkrydsningsfeltet **Beregn gebyr** på siden **Emballageposteringer**. Det angiver, at gebyrer beregnes, når der oprettes en rapport. Du kan udskrive vægtangivelserne på fakturaen og angive, at firmaet betaler gebyrerne.

## <a name="print-packaging-material-weights-on-invoices"></a>Udskrive emballagevægt på fakturaer
Du kan udskrive emballagevægten på fakturaen og angive, hvem der skal betale emballagegebyrerne. I rapporten opsummeres vægten efter emballagekoder.
 




