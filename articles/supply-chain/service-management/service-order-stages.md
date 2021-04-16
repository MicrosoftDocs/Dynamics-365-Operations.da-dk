---
title: Serviceordrestadier
description: Ved at definere stadier for en serviceordre og tildele dem til arbejdere styrer du forløbet for en serviceordre gennem de opgaver, som forskellige personer udfører i en serviceorganisation.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c46d4bb43c8f59a0ef55963ac9b453491a6112b0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817503"
---
# <a name="service-order-stages"></a>Serviceordrestadier   

[!include [banner](../includes/banner.md)]


Du kan oprette stadier for en serviceordre for at definere de opgaver, der skal udføres, den rækkefølge, hvori de færdiggøres, og de arbejdere, der er ansvarlige for at fuldføre dem. Ved at definere stadier for en serviceordre og tildele dem til arbejdere kan du styre forløbet for en serviceordre gennem de opgaver, som forskellige personer udfører i en serviceorganisation. Sekvensen af stadier skal indeholde et indledende stadie.

Du kan også definere de handlinger, der er tilladt i hvert stadie. Hvis du f.eks. fjerner markeringen i afkrydsningsfeltet **Bogfør** for alle stadier undtagen det endelige stadie, vil ingen serviceordrer blive bogført, før serviceordrerne har gennemgået behandlingen i hele sekvensen af stadier.

## <a name="branching-in-service-order-stages"></a>Forgrening i serviceordrestadier

Når du har oprettet et servicestadie, kan du oprette flere indstillinger, eller grene, som du kan vælge i det næste servicestadie. Du kan vælge fra alle de grene, du opretter, når det indledende stadie er fuldført. For eksempel kan du konfigurere **Planlægning** som et indledende stadie. Du opretter to stadier, **Igangværende** og **Annuller**, og derefter vælger du **Planlægning** som overordnet stadie for dem. Du kan tildele stadiet **Planlægning** til salgsordren. Når planlægningen for salgsordren er fuldført, kan du vælge stadiet **Igangværende**, hvis salgsordren er klar til at arbejde på, eller du kan vælge stadiet **Annuller**, hvis ordren er annulleret.

## <a name="see-also"></a>Se også

[Konfigurer serviceordrestadier](set-up-service-order-stages.md)

[Ændre serviceordrestadiet](change-service-order-stage.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]