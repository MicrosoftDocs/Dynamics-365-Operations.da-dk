---
title: Oprette lagersteder for flytteordrer
description: Denne artikel beskriver, hvordan du kan konfigurere lagersteder for flytteordrer.
author: Mirzaab
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation,CustVendTransportPoint2Point
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 984f90343805d35833b7ddd1a175af5833c23dd5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905509"
---
# <a name="set-up-warehouses-for-transfer-orders"></a>Oprette lagersteder for flytteordrer 

[!include [banner](../includes/banner.md)]

Du kan bruge lagerstedsniveauer til at oprette et hierarki, der understøtter flytteforslag mellem lagerstederne. På baggrund af denne opsætning beregner behovsplanlægningen varebehov på de enkelte lagerstedsniveauer, og der genereres flytteforslag fra et tilknyttet kildelagersted, der skal opfylde disse forslag.

1.  Klik på **Lagerstyring > Opsætning > Lageropdeling > Lagersteder**.

2.  Vælg det lagersted, der skal opfyldes.

3.  I oversigtspanelet **Varedisponering** skal du markere afkrydsningsfeltet **Opfyldning**.

4.  Vælg i feltet **Hovedlagersted** det lagersted, du vil tilknytte som opfyldningslagerstedet. I behovsplanlægningen beregnes et flyttebehov for det valgte lagersted, og der oprettes et flytteordreforslag fra det tilknyttede **Hovedlagersted**.
   
    > [!NOTE]
    > <P>Hvis du fjerner markeringen i feltet <STRONG>Opfyldning</STRONG>, tildeles det valgte lagersted et lagerstedsniveau i forbindelse med <STRONG>Hovedlagersted</STRONG>, men <STRONG>Hovedlagersted</STRONG> konfigureres ikke som et opfyldningslagersted.</P>

5.  Luk siden for at anvende den nye konfiguration.


> [!TIP]
> <P>Hvis du vil angive et lagersted til opfyldning, skal du først oprette lagerstedet som en lagringsdimension på siden <STRONG>Lagringsdimensionsgrupper</STRONG>. På denne side skal du markere feltet <STRONG>Aktiv</STRONG> og feltet <STRONG>Disponer pr. dimension</STRONG> for lagerstedet.</P>

## <a name="set-up-transport-lead-time"></a>Angive leveringstid for transport

Du skal også angive transportleveringstiden mellem lagerstederne på siden **Transportdage**. 
1. Gå til **Lagerstyring > Opsætning > Distribution > Transportdage**.
2. Vælg **lagersted** i feltet **Tilgangssted**.
3. Vælg **Forsendelseslagersted**, **Tilgangslagersted** og **Transportdage**. 
4. (Valgfrit) Du kan også angive transporttiden, afhængigt af leveringsmåden, under fanen **Transportdage pr. leveringsmåde**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]