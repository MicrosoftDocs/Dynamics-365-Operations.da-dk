---
title: Angive gennemsnitskursen
description: Denne artikel indeholder oplysninger om gennemsnitskurser i Microsoft Dynamics 365 Finance.
author: abruer
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efb01948af2bcba9ca740e8bd0e12584cf021fce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889955"
---
# <a name="specify-the-cross-rate"></a>Angive gennemsnitskursen

[!include [banner](../includes/banner.md)]

Denne artikel forklarer formålet med en gennemsnitskurs, og hvordan du angiver gennemsnitskursen, når du udligner en betaling med en faktura. Du kan bruge en gennemsnitskurs, når følgende kriterier gælder: 
-   Du udligner en betaling med en faktura. 
-   Betalingslinjen og fakturalinjen anvender forskellige valutaer. 
-   Ingen af valutaerne er regnskabsvalutaen. 

Krydskursen bruges ikke til at beregne valutaomregning ved betalingstransaktioner til regnskabsvalutaen for betalingen. I stedet hentes valutakurserne fra valutakurstabellerne for at beregne værdien af valutabeløbet for betalingstransaktionen og betalingsbeløbet i regnskabsvalutaen. 

For eksempel er regnskabsvalutaen i USD, fakturavalutaen er i CAD, og betalingsvalutaen er i EUR. Med gennemsnitskursen kan du angive en valutakurs til at oversætte direkte mellem CAD og EUR og behøver ikke at oversætte via USD. Når du vælger en faktura og en primær betaling, kan du angive en gennemsnitskurs for fakturalinjen. Gennemsnitskursen er valutakursen mellem valutaer for disse transaktioner pr. afregningsdatoen.

1.  Gå til en af følgende sider:
- **Debitor > Generelt > Kunder > Alle kunder** 
- **Kreditor > Almindelige > Kreditorer > Alle kreditorer** 
- **Indkøb og forsyning > Almindelige > Kreditorer > Alle kreditorer**
2.  Vælg den debitor eller kreditor, hvis åbne posteringer skal afregnes. 
3.  For en debitor skal du på listesiden **Alle debitorer** gå til **Indsaml > Udlign åbne posteringer**. For en kreditor skal du på listesiden **Alle kreditorer** gå til **Faktura > Udlign åbne posteringer**. 
4.  Vælg den postering, der er den primære betaling, og klik derefter på **Marker betaling**. Afkrydsningsfeltet i kolonnen **Marker** markeres, og der vises et informationsikon i kolonnen **Primær betaling**. 
5.  I feltet **Krydskurs** skal du angive fakturavalutaen og betalingsvalutaen pr. udligningsdatoen. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
