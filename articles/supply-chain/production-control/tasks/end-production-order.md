---
title: Afslut en produktionsordre
description: Denne procedure viser, hvordan du afslutter en produktionsordre.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fade659c320e0ea1059644324859c9a3cb273c96
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424327"
---
# <a name="end-a-production-order"></a>Afslut en produktionsordre

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du afslutter en produktionsordre. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Dette er den sidste procedure ud af syv, der beskriver produktionsordrelivscyklussen.


## <a name="end-a-production-order"></a>Afslut en produktionsordre
1. Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.
    * Vælg en produktionsordre, som har statussen Færdigmeldt.  
2. Klik på Produktionsordre i handlingsruden.
3. Klik på Afslut.
    * På denne side kan du bekræfte, at du vil afslutte produktionsordren.  
4. Klik på fanen Generelt.
5. Indtast en dato i feltet Dato.
6. Vælg "Tildeling" i feltet Spildmetode.
    * Når du vælger metoden Tildeling, føjes omkostninger fra kasserede materialer til de færdige varer.  
7. Klik på OK.

## <a name="validate-calculation-results"></a>Valider beregningsresultater
1. Klik på Administrer omkostninger i handlingsruden.
2. Klik på Vis omkostningssammenligning.
    * Når du har afsluttet produktionsordren, kan du sammenligne den forkalkulerede kostpris i forhold til den realiserede kostpris for at få et overblik over produktionsafvigelser.  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]