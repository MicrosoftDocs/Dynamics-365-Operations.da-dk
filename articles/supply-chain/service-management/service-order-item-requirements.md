---
title: "Varebehov på serviceordre"
description: Hvis du vil reservere bestemte varer til en serviceordre, kan du oprette lager lagervarebehov for den.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 880d41a5b3d8c9200a0a1f4b13af2d6d24d30766
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

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

[Varebehov (form)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\))


