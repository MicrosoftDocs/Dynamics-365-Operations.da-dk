---
title: Rapportere en produktionsordre som færdig
description: Denne procedure viser, hvordan du færdigmelder en produktionsordre.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4848093bd4901d3aa801fc09d7ee3e79d65ebb0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204445"
---
# <a name="report-a-production-order-as-finished"></a>Rapportere en produktionsordre som færdig

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du færdigmelder en produktionsordre. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Dette er den sjette procedure ud af syv, der beskriver produktionsordrelivscyklussen.


## <a name="report-a-production-order-as-finished"></a>Rapportere en produktionsordre som færdig
1. Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.
    * Vælg en produktionsordre, som har statussen Påbegyndt.  
2. Klik på Produktionsordre i handlingsruden.
3. Klik på Færdigmelding.
    * På denne side kan du bekræfte mængden af det færdige produkt, der skal færdigmeldes.  
4. Klik på fanen Generelt.
5. Indstil Antal gode til '18'.
6. Indstil Antal fejl til '2'.
7. Vælg 'Materiale' i feltet Fejlårsag.
8. Markér eller fjern markering af afkrydsningsfeltet Slutkørsel.
9. Markér eller fjern markeringen i afkrydsningsfeltet Accepter fejl.
10. Klik på OK.

## <a name="verify-the-report-as-finished-journal"></a>Bekræft færdigmeldingskladden
1. Klik på Vis i handlingsruden.
2. Klik på Færdigmeldt.
3. Markér den valgte række på listen.
4. Klik op linket i den valgte række på listen.
    * Færdigmeldingskladden bogføres. Hvis du vil foretage ændringer i kladden, kan du oprette en ny kladde, hvor du kan foretage ændringer manuelt.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]