---
title: Direkte leveringer
description: Denne artikel indeholder oplysninger om direkte leveringer. Direkte leveringer sendes direkte fra leverandøren til kunden.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchCreateFromSalesOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 9704
ms.assetid: 64c51384-8a4e-45d0-83c1-12cea22902f9
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70919409cac0b6318e4f95c27bfa005306ef02380a165df5ad302b0396ba9769
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776260"
---
# <a name="direct-deliveries"></a>Direkte leveringer

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om direkte leveringer. Direkte leveringer sendes direkte fra leverandøren til kunden.

Direkte leveringer sparer leveringstid og reducerer de omkostninger der er forbundet med at føre lager, fordi du ikke opbevarer varerne på lagerstedet, inden de sendes til kunden.  

Du kan oprette direkte leveringer fra siden **Salgsordre**. Først skal du oprette en salgsordre og ordrelinjer. Derefter skal du vælge **Direkte levering** under fanen **Salgsordre** i handlingsruden. Til sidst skal du angive de linjer, der skal håndteres som en direkte levering. Der er nu oprettet en tilknytning mellem salgsordrelinjerne til direkte levering og deres tilsvarende indkøbsordrelinjer.  

**Bemærk!** Hvis en del af det bestilte antal er allerede blevet leveret, skal du opdele den resterende mængde. Opret en ny linje for det antal, der skal leveres direkte, og fratræk det antal fra antallet på den oprindelige linje. Hvis f.eks. det oprindelige antal var 15, og fem er blevet leveret, skal du oprette en ny linje for det resterende antal, 10, og derefter reducere det oprindelige antal med dette antal.  

Når du har oprettet tilknytningen for den direkte levering mellem salgsordrelinjerne og indkøbsordren, kan du opdatere den salgsordren ved hjælp af en følgeseddel. Kør enten en opdatering af følgesedlen eller fakturaopdatering fra indkøbsordren. Du skal opdatere fakturaen til salgsordren fra formen **Salgsordre**. En fakturaopdatering kan ikke medføre, at antallet i salgsordren overstiger det antal, der er registreret som modtaget. Hvis f.eks. salgsordrelinjen er 10 styk, men kun fem styk fra salgsordrelinjen opdateres ved hjælp af en følgeseddel. Hvis du vælger **Alle** på listen **Antal**, når du fakturaopdaterer salgsordren, er det kun de varer, der fysisk er modtaget, eller opdateret ved hjælp af en følgeseddel, der fakturaopdateres. Hele salgsordrelinjen opdateres ikke.

## <a name="delivery-date"></a>Leveringsdato
Når du opdaterer feltet **Ønsket modtagelsesdato** på salgsordrelinjen, opdateres feltet **Leveringsdato** på den tilsvarende indkøbsordrelinje også. Omvendt, hvis du opdaterer feltet **Bekræftet** på indkøbsordrelinjen, opdateres felterne **Bekræftet modtagelsesdato** og **Bekræftet afsendelsesdato** også på den tilsvarende salgsordrelinje.

## <a name="delivery-address"></a>Leveringsadresse
Leveringsadressen for en indkøbsordre er som sædvanligvis firmaets adresse. Når du opretter en direkte levering, bliver kundens adresse dog angivet som leveringsadressen. Hvis du ændrer leveringsadressen for en indkøbsordre med leveringstypen **Direkte levering**, vil leveringsadressen for den tilsvarende salgsordrelinje også blive opdateret. Hvis du ændrer leveringsadressen på salgsordrelinjen, vil leveringsadressen på indkøbsordrelinjen også blive opdateret.

## <a name="deleting-order-lines"></a>Slette ordrelinjer
Hvis du prøver at slette en salgsordrelinje, der har leveringstypen **Direkte levering**, vises et meddelelsesfelt, der angiver, at indkøbsordrelinjer er knyttet til linjen. Hvis salgsordrelinjen er blevet delvist leveret, kan du hverken slette salgsordrelinjen eller de tilknyttede indkøbsordrelinjer.

## <a name="warehouse"></a>Lagersted
Når du opretter en direkte levering, ankommer de varer, du sælger, aldrig fysisk til dit lager. Du skal dog stadig angive et lager på salgsordrelinjen. På samme måde kan plukkrav angives til varens varemodelgruppe. Men da varerne aldrig fysisk ankommer til lageret, ignoreres disse krav, når salgsordren er en direkte levering.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]