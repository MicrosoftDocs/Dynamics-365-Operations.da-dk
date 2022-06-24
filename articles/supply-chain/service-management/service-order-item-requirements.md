---
title: Varebehov på serviceordre
description: Denne artikel beskriver varebehov for tjenesteordrer.
author: sorenva
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
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6f12b0dd1facc753bfcde820eea26a4052caf67
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882396"
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