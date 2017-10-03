---
title: "Ordrer på hold"
description: "Dette emne beskriver tilbageholdte ordrer ved hjælp af Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: c0c0e9a0f863eb33d544f63e40e0531cdaaf6426
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017

---

# <a name="order-holds"></a>Ordrer på hold

[!include[banner](includes/banner.md)]


Dette emne beskriver tilbageholdte ordrer ved hjælp af Dynamics 365 for Retail.

En ordre kan holdes tilbage af forskellige årsager. Du kan for eksempel holde en ordre tilbage, indtil debitoradressen eller betalingsmetoden er kontrolleret, eller indtil en chef leder kan gennemse debitorens kreditmaksimum. I løbet af salgsprocessen er der tidspunkter, hvor salgsordrer skal holdes tilbage. En salgsordre kan for eksempel holdes tilbage på grund af problemer med en debitorbetaling, der skyldes mistanke om svig, eller fordi en chef skal gennemgå ordren. Når en salgsordre holdes tilbage, tildeles en ordretilbageholdelseskode til salgsordren for at angive årsagen til tilbageholdelsen. Koder for tilbageholdelse af salgsordrer er konfigureret under **Salg og marketing** &gt; **Konfiguration** &gt; **Salgsordrer** &gt; **Koder for ordrer på hold**. En salgsordre kan tilbageholdes manuelt på tidspunktet for oprettelse af ordren eller senere. Desuden kan en ordre automatisk tilbageholdes baseret på reglerne for svig. Når en salgsordre tilbageholdes, kan det være nødvendigt at opdatere den med yderligere oplysninger. Alternativt kan det være en god ide at tjekke salgsordren, når du fortsætter med at arbejde på den. Du kan tjekke en salgsordre ud, tjekke den tilbage igen og endda tilsidesætte en anden brugers udtjekning ved hjælp af panelet for tilbageholdte ordrer (**Detail** &gt; **Kunder** &gt; **Ordrer på hold**). Når en ordre er klar til at blive fuldført, skal du fjerne hold, før du kan fuldføre bestillingsprocessen.




