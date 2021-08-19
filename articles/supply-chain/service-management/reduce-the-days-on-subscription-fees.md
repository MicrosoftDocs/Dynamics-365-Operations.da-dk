---
title: Reducere dagene på abonnementsgebyrer
description: Hvis du vil reducere antallet af dage i et eksisterende abonnementsgebyr, kan du oprette en ny transaktion, hvor du fjerner den periode, der ikke længere skal være del af intervallet for abonnementsgebyret.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69a4ea4a70749d75ce5f894bcf3a3adfe7c2077e368c18679bf3169c74feef25
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726627"
---
# <a name="reduce-the-days-on-subscription-fees"></a>Reducere dagene på abonnementsgebyrer 

[!include [banner](../includes/banner.md)]


Hvis du vil reducere antallet af dage i et eksisterende abonnementsgebyr, kan du oprette en ny transaktion, hvor du fjerner den periode, der ikke længere skal være del af intervallet for abonnementsgebyret.

## <a name="reduce-the-days-on-a-subscription-fee"></a>Reducere dagene i et abonnementsgebyr

1.  Klik på **Servicestyring** \> **Almindelige** \> **Serviceabonnementer** \> **Alle serviceabonnementer**. Vælg serviceabonnementet, og klik på **Abonnementsgebyrer** i handlingsruden.

2.  I feltet **Abonnementstype** skal du vælge **Reduktionsdage**.

3.  Angiv datointervallet for det abonnementsgebyr, du vil fjerne fra abonnementsgebyrperioden, i feltet **Fra dato** og **Til dato**, og klik derefter på **OK**.

Hvis du vil have vist den transaktion, der er oprettet, skal du i formularen **Abonnement** klikke på **Gebyrtransaktioner**.

## <a name="example"></a>Eksempel

Hvis en periode for en abonnementstransaktion løber fra 1. til 31. januar, og du vil reducere perioden med 10 dage, skal du oprette en ny transaktion, hvor reduktionsperioden er 1. til 10. januar. (Reduktionsperioden kunne også være 5. til 15. januar).

Hvis **Fra dato** i reduktionsperioden desuden er 21. januar (31 minus 10), kan du indstille **Til dato** til en vilkårlig dato efter 31. januar, så fjernes der 10 dage fra gebyrtransaktionsperioden.

## <a name="see-also"></a>Se også

[Eksempel på reduktionsdage](reduction-days-example.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]