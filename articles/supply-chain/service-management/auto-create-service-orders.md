---
title: Oprette serviceordrer automatisk
description: Du kan generere serviceordrer ud fra en serviceaftale for den serviceaftalens gyldighedsperiode.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41f48e2156ea5f57e600cc5dec09a78a91992d60
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675789"
---
# <a name="automatically-create-service-orders"></a>Oprette serviceordrer automatisk 

[!include [banner](../includes/banner.md)]


Du kan generere serviceordrer ud fra en serviceaftale for den serviceaftalens gyldighedsperiode.

Alle de serviceordrer, du opretter ud fra en serviceaftale, knyttes til serviceaftalen.

Serviceordrer oprettes automatisk ud fra følgende indstillinger:

  - Det serviceaftaleinterval, der er angivet i serviceaftalelinjerne. Serviceaftaleintervallet angiver den hyppighed, serviceordrelinjer oprettes med. Du kan finde flere oplysninger under [Serviceintervaller](service-intervals.md).

  - Den periode, som du angiver for at definere serviceperioden i felterne **Fra dato** og **Til dato** i formularen **Opret serviceordrer**. Du kan finde flere oplysninger under [Oprette serviceordrer automatisk](create-service-orders-automatically.md).

  - Indstillingen **Kombiner serviceordrer** i sidehovedet for serviceaftalen. Denne indstilling angiver, om serviceordrelinjer, der er oprettet fra en serviceaftale, samler serviceordrer efter medarbejder, serviceopgave, serviceobjekt eller serviceaftale. Du kan finde flere oplysninger under [Kombinere serviceordrer](combine-service-orders.md).

  - Indstillingen **Tidsvindue** på serviceaftalelinjen. I tidsvinduet defineres, hvor langt en servicelinje kan flyttes i forhold til den beregnede dato. Du kan finde flere oplysninger under [Tidsvinduer](time-windows.md).


> [!NOTE]
> <P>Hvis den dag, der er angivet for en serviceordre, ikke er åben i den kalender, du har valgt i formularen <STRONG>Parametre for servicestyring</STRONG>, modtager du en meddelelse om, at der er opstået en kalenderkonflikt. Du kan blot ignorere meddelelsen. Serviceordren vil blive oprettet, selvom dagen er lukket i kalenderen.</P>

## <a name="example-1"></a>Eksempel 1

Serviceaftalen gælder fra 1. januar 2012 til 31. december 2012. Hvis den serviceperiode, du angiver i formularen **Opret serviceordrer**, gælder fra den 1. november 2012 til den 1. februar 2013, oprettes der serviceordrer fra den 1. november 2012 til den 31. december 2012.

## <a name="example-2"></a>Eksempel 2

Serviceaftalen gælder fra 1. januar 2012 til 31. december 2012. Der knyttes to serviceaftalelinjer til serviceaftalen. Den første serviceaftalelinje har startdato den 2. januar 2012 og slutdato den 1. marts 2012. Den anden serviceaftalelinje har startdato den 1. april 2012 og slutdato den 31. december 2012. Du angiver en periode i formularen **Opret serviceordrer**, der går fra 1. oktober 2012 til 31. december 2012. Derfor genereres der kun serviceordrer for den anden aftalelinje, da startdatoen og slutdatoen for den første aftalelinje ligger før den periode, du har angivet for serviceordren.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]