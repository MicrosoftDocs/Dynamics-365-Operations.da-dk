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
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 994f4ca578de970876f714bb397afeea1f39c15c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240335"
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