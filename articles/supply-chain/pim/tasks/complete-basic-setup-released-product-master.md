---
title: Fuldføre grundlæggende konfiguration af en frigivet produktmaster
description: Denne artikel viser, hvordan du fuldfører opsætningen, der som minimum kræves, før produktmasteren kan bruges i styklisteversioner.
author: t-benebo
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a403600bfdc257587441b5b5a907981d5eebaf58
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844846"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a>Fuldføre grundlæggende konfiguration af en frigivet produktmaster

[!include [banner](../../includes/banner.md)]

Denne artikel viser, hvordan du fuldfører opsætningen, der som minimum kræves, før produktmasteren kan bruges i styklisteversioner.

Dette er den tredje procedure ud af otte, som forklarer, hvordan du kan opbygge kombinationer til dimensionsbaseret konfiguration. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.

1. Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Produkter > Frigivne produkter**.
2. Find og vælg den ønskede post på listen. Vælg produktmasteren, der er frigivet i den anden procedure. Denne produktmaster er oprettet med teknologien Dimensionsbaseret konfiguration.  
3. Vælg **Produkt** i handlingsruden.
4. Vælg **Dimensionsgrupper** for at åbne dialogboksen.
5. Vælg rullelisten i feltet **Lagringsdimensionsgruppe** for at åbne opslaget.
6. Find og vælg den ønskede post på listen. Lagringsdimensionsgruppen bestemmer, hvilke lagringsdimensioner, der bruges til transaktion af produktet. Vælg **Sted** til denne procedure.  
7. Vælg rullelisten i feltet **Sporingsdimensionsgruppe** for at åbne opslaget.
8. Find og vælg den ønskede post på listen. Sporingsdimensionsgruppen bestemmer, hvilke sporingsdimensioner der bruges til transaktion af produktet. Vælg **Ingen** til denne procedure.  
9. Klik på **OK**.
10. Klik på **Rediger**.
11. Vælg rullelisten i feltet **Varemodelgruppe** for at åbne opslaget.
12. Find og vælg den ønskede post på listen. Varemodelgrupper indeholder indstillinger, der bestemmer, hvordan varerne kontrolleres og håndteres i forbindelse med indgående varer og vareafgange. De bestemmer også, hvordan der beregnes vareforbrug. Vælg **FIFO** til denne procedure.  
13. Udvid sektionen **Administrer omkostninger**.
14. Vælg rullelisten i feltet **Varegruppe** for at åbne opslaget.
15. Find og vælg den ønskede post på listen. Varegrupper anvendes til at styre lagerbeholdningen ved at opdele lagervarer i grupper. Vælg **CarAudio** til denne procedure.  
16. Vælg **Plan** i handlingsruden.
17. Vælg **Standardindstillinger for ordre**.
18. Vælg en indstilling i feltet **Standardordretype**. Vælg **Produktion** for at angive, at standardindstillingen for denne produktmaster er at producere den.  
19. Vælg **Gem**.
20. Luk siden.
21. Luk formularen **Frigivne produktdetaljer**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]