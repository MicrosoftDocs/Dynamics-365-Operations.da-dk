---
title: Varebehov på serviceordre
description: Hvis du vil reservere bestemte varer til en serviceordre, kan du oprette lager lagervarebehov for den.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a0ce40c26e3d3028064b73a80a247180d6a9009
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226659"
---
# <a name="service-order-item-requirements"></a>Varebehov på serviceordre   

[!include [banner](../includes/banner.md)]


Du kan oprette en serviceordre for at spore og administrere ydelser, du leverer til dine debitorer. Hvis du vil reservere bestemte varer til en serviceordre, kan du oprette lager lagervarebehov for den. Et varebehov kan forbruges straks fra lageret, eller det kan starte en produktionsordre for varen.

Når du bruger et varebehov i stedet for en varepostering, kan du planlægge leveringen, så den finder sted, umiddelbart før varen faktisk skal bruges. Du kan oprette en indkøbsordre, lade varen indgå i samhandelsaftaler og lade varebehovet indgå i produktionsplanlægningen.

Varebehov til serviceordrer behandles løbende igennem et projekt. Hvis du vil oprette et varebehov på en serviceordre, skal serviceordren knyttes til et projekt.

I samme øjeblik et varebehov oprettes til en serviceordre, kan du få det vist fra **Projekt** i de enkelte serviceordrer eller via formularen **Salgsordre**.

## <a name="view-an-item-requirement-from-a-service-order"></a>Få vist et varebehov fra en serviceordre

1.  Klik på **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.

2.  Klik på **Ekspedition**, og klik derefter på **Varebehov** for at åbne formularen **Varebehov**.

3.  Klik på fanen **Projekt**, og marker feltet **Serviceordre** for at se serviceordrerne for varebehovet.

## <a name="delete-service-orders-with-item-requirements"></a>Slette serviceordrer med varebehov

Hvis der oprettes et varebehov på en serviceordre, kan du ikke slette serviceordren. Du skal slette varebehovet, før du kan slette serviceordren.

1.  Klik på **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.

2.  Klik på **Ekspedition**, og klik derefter på **Varebehov** for at åbne formularen **Varebehov**. I denne form vises de varebehov, der er oprettet på serviceordren.

3.  Vælg det varebehov, der skal slettes, og klik derefter på **Slet**.

–eller–

1.  Klik på **Projektstyring og regnskab** \> **Generelt** \> **Projekter** \> **Alle projekter**.

2.  Åbn det projekt, der har den serviceordre, hvor der er oprettet et varebehov.

3.  Klik på **Varebehov** i højre rude i formularen **Projekter**. Formularen **Varebehov** viser en oversigt over de varebehov, der er knyttet til det valgte projekt.

4.  Vælg det varebehov, der skal slettes, og klik derefter på **Slet**.

## <a name="see-also"></a>Se også

[Varebehov (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))



[!INCLUDE[footer-include](../../includes/footer-banner.md)]