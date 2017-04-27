---
title: "Ordrer på hold"
description: "Dette emne beskriver tilbageholdte ordrer ved hjælp af Detail og handel i Dynamics AX."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1cb18e3275b8dcdf0a61531ee056995f6e8fbc8d
ms.lasthandoff: 03/31/2017


---

# <a name="order-holds"></a>Ordrer på hold

[!include[banner](includes/banner.md)]


Dette emne beskriver tilbageholdte ordrer ved hjælp af Detail og handel i Dynamics AX.

En ordre kan holdes tilbage af forskellige årsager. Du kan for eksempel holde en ordre tilbage, indtil debitoradressen eller betalingsmetoden er kontrolleret, eller indtil en chef leder kan gennemse debitorens kreditmaksimum. I løbet af salgsprocessen er der tidspunkter, hvor salgsordrer skal holdes tilbage. En salgsordre kan for eksempel holdes tilbage på grund af problemer med en debitorbetaling, der skyldes mistanke om svig, eller fordi en chef skal gennemgå ordren. Når en salgsordre holdes tilbage, tildeles en ordretilbageholdelseskode til salgsordren for at angive årsagen til tilbageholdelsen. Koder for tilbageholdelse af salgsordrer er konfigureret under **Salg og marketing** &gt; **Konfiguration** &gt; **Salgsordrer** &gt; **Koder for ordrer på hold**. En salgsordre kan tilbageholdes manuelt på tidspunktet for oprettelse af ordren eller senere. Desuden kan en ordre automatisk tilbageholdes baseret på reglerne for svig. Når en salgsordre tilbageholdes, kan det være nødvendigt at opdatere den med yderligere oplysninger. Alternativt kan det være en god ide at tjekke salgsordren, når du fortsætter med at arbejde på den. Du kan tjekke en salgsordre ud, tjekke den tilbage igen og endda tilsidesætte en anden brugers udtjekning ved hjælp af panelet for tilbageholdte ordrer (**Detail og handel** &gt; **Kunder** &gt; **Ordrer på hold**). Når en ordre er klar til at blive fuldført, skal du fjerne hold, før du kan fuldføre bestillingsprocessen.




