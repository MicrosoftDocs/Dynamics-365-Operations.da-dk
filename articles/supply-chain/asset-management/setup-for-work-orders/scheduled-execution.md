---
title: Planlagt udførelse
description: I dette emne beskrives planlagt udførelse i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0ed61411920edebb1ab9b87856a5418fa43bc2f4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264916"
---
# <a name="scheduled-execution"></a>Planlagt udførelse

[!include [banner](../../includes/banner.md)]

 

Du kan bruge serviceniveauer for arbejdsordrer til at konfigurere planlagt udførelse. (Yderligere oplysninger om serviceniveauer for arbejdsordrer finder du under [Serviceniveau og -beskrivelse](service-level-and-description.md)). Planlagt udførelse giver fleksibilitet i arbejdsplanlægningen for vedligeholdelsesarbejdere, fordi du kan konfigurere mere eller mindre detaljerede krav for det interval, som en arbejdsordre skal fuldføres i. En vedligeholdelsesarbejder, der fuldfører et job hurtigere end forventet i en produktionsfacilitet, kan f.eks. gå videre til et andet job i nærheden, der er planlagt for den aktuelle uge, men ikke nødvendigvis for den aktuelle dag. Denne fremgangsmåde giver mulighed for optimering af arbejderplanlægningen og jobudførelsen.

Opsætning af planlagt udførelse, der er relateret til arbejdsordrer, kan være generisk eller specifik. Du kan oprette generiske linjer, der ikke er begrænset til bestemte arbejdsordretyper, aktivtyper osv. Du kan også oprette planlagte udførelseslinjer, der gælder for en bestemt arbejdsordretype, aktivtype, vedligeholdelsesjobtype osv.

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Arbejdsordrer** \> **Planlagt udførelse**.
2. Vælg **Ny** for at oprette en linje for planlagt udførelse.
3. Vælg værdier efter behov i felterne **Arbejdssted**, **Arbejdsordretype**, **Aktivtype** **Producent**, **Model**, **Vedligeholdelsesjobtypekategori**, **Vedligeholdelsesjobtype**, **Vedligeholdelsesjobtypevariant** og **Fag**.
4. Vælg et serviceniveau for arbejdsordren i feltet **Serviceniveau**. Hvis du lader dette felt være tomt, skal du angive den mest generelle linjetype for planlagt udførelse. Du kan se et eksempel på en generisk linje i den første post i illustrationen nedenfor. Denne linje gør det muligt, at planlægge alle arbejdsordrer, der ikke har et serviceniveau for arbejdsordren, til en bestemt dato og tidspunkt.
5. Vælg tidsinterval i feltet **Planlagt udførelse**.
6. Vælg **Gem**.

![Planlagt udførelse](media/20-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]