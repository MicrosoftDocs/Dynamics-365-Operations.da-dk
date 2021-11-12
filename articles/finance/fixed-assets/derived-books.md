---
title: Afledte bøger
description: Denne artikel indeholder en oversigt over funktionerne til afledte bøger.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32abfce013d0daa208138cf698b2abd1f96462f6
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674496"
---
# <a name="derived-books"></a>Afledte bøger

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over funktionerne til afledte bøger.

Formålet med afledte bøger er at forenkle bogføringen af transaktioner for aktivbog, der er planlagt til at finde sted med jævne mellemrum.  Du skal vælge en bog som den primære bog. Dette er normalt den bog, der bruges til regnskabsmæssige afskrivninger. Du kan derefter knytte den til andre bøger, der er konfigureret til at bogføre transaktioner i de samme som den primære bog. Bøger til skattemæssig afskrivning angives ofte som afledte bøger. 

De mest almindelige transaktioner, der angives, så der bogføres til afledte bøger, er anskaffelser, anskaffelsesreguleringer og afhændelser. 

## <a name="example"></a>Eksempel

Bog B og bog C er konfigureret som afledte bøger for bog A til posteringstypen Anskaffelse. I bog A skal du angive en anskaffelsespostering for aktiv 123 på 1.500,00. 

Ved posteringen oprettes der en anskaffelsespostering, som bogføres i aktiv 123 for bog B og i aktiv 123 for bog C med en værdi på 1.500,00. Når du forbereder transaktionerne til den primære bog for bogføring i anlægsaktivkladden, kan du også se og redigere transaktionerne til de afledte afskrivningsmodeller. Hvis du forbereder transaktionerne til den primære bog i en anden kladde, kan du ikke få vist posteringerne for den afledte værdi. De bogføres i stedet på de relevante konti og posteringslag, når du bogfører posteringer til den primære bog.

> [!NOTE]                                                                                                                               
> Bøger, der er konfigureret, så posteringer bogføres med andre intervaller end dem, der er angivet for den primære bog, skal tilknyttes anlægsaktivet som separate bøger og ikke som afledte bøger.  

Du kan finde flere oplysninger under [Bogfør med afledte bøger](post-derived-value-models.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
