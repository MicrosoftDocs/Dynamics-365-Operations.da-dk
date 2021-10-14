---
title: Varebehov på serviceordre
description: Dette emne beskriver varebehov for tjenesteordrer.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ae211cb24e3ed0e9e54643448ee378a20658ad89
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573195"
---
# <a name="service-order-item-requirements"></a>Varebehov på serviceordre

[!include [banner](../includes/banner.md)]

Du kan oprette en serviceordre for at spore og administrere ydelser, du leverer til dine debitorer. Hvis du vil reservere bestemte varer til en serviceordre, kan du oprette lager lagervarebehov for den. Et varebehov kan forbruges straks fra lageret, eller det kan starte en produktionsordre for varen.

Når du bruger et varebehov i stedet for en varepostering, kan du planlægge leveringen, så den finder sted, umiddelbart før varen faktisk skal bruges. Du kan oprette en indkøbsordre, lade varen indgå i samhandelsaftaler og lade varebehovet indgå i produktionsplanlægningen.

Varebehov til serviceordrer behandles løbende igennem et projekt. Hvis du vil oprette et varebehov på en serviceordre, skal serviceordren knyttes til et projekt.

I samme øjeblik et varebehov oprettes til en serviceordre, kan du få det vist fra **Projekt** i de enkelte serviceordrer eller via formularen **Salgsordre**.

## <a name="view-an-item-requirement-from-a-service-order"></a>Få vist et varebehov fra en serviceordre

1. Gå til **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.
1. Vælg **Ekspedition**, og vælg derefter **Varebehov** for at åbne formularen **Varebehov**.
1. Vælg fanen **Projekt**, og marker feltet **Serviceordre** for at se serviceordrerne for varebehovet.

## <a name="delete-service-orders-with-item-requirements"></a>Slette serviceordrer med varebehov

Hvis der oprettes et varebehov på en serviceordre, kan du ikke slette serviceordren. Du skal slette varebehovet, før du kan slette serviceordren.

1. Gå til **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.
1. Vælg **Ekspedition**, og vælg derefter **Varebehov** for at åbne formularen **Varebehov**. I denne form vises de varebehov, der er oprettet på serviceordren.
1. Vælg det varebehov, der skal slettes, og vælg derefter **Slet**.

eller

1. Gå til **Projektstyring og regnskab** \> **Fælles** \> **Projekter** \> **Alle projekter**.
1. Åbn det projekt, der har den serviceordre, hvor der er oprettet et varebehov.
1. Vælg **Varebehov** i højre rude i formularen **Projekter**. Formularen **Varebehov** viser en oversigt over de varebehov, der er knyttet til det valgte projekt.
1. Vælg det varebehov, der skal slettes, og vælg derefter **Slet**.

## <a name="see-also"></a>Se også

[Varebehov (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))



[!INCLUDE[footer-include](../../includes/footer-banner.md)]