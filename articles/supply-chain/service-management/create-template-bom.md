---
title: Oprette en styklisteskabelon
description: Du kan oprette en skabelonstykliste ved hjælp af forskellige fremgangsmåder.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2e06283f3b95c5ff6b4376bba63cf5a42d5feeb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424749"
---
# <a name="create-a-template-bom"></a>Oprette en styklisteskabelon   

[!include [banner](../includes/banner.md)]


Du kan oprette en skabelonstykliste ved hjælp af følgende fremgangsmåder. Uanset hvilken fremgangsmåde du vælger, er felterne **Fra dato** og **Til dato** valgfrie og kan kun bruges som ekstra oplysninger.

## <a name="create-a-template-bom-manually"></a>Oprette en styklisteskabelon manuelt

1.  Klik på **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.

2.  Tryk på CTRL+N for at åbne formularen **Opret styklisteskabelon**.

3.  Under **Kopier styklistelinjer fra reference** skal du vælge indstillingen **Manuel**.

4.  Angiv en vare af typen **Stykliste** i feltet **Varenummer**.

5.  Angiv et navn til skabelonen i feltet **Navn**.

6.  Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.

7.  Klik på **OK**.

Der oprettes en ny tom styklisteskabelon.

## <a name="create-a-template-bom-based-on-another-template-bom"></a>Oprette en styklisteskabelon ud fra en anden styklisteskabelon

1.  Klik på **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.

2.  Tryk på CTRL+N for at åbne formularen **Opret styklisteskabelon**.

3.  Under **Kopier styklistelinjer fra reference** skal du vælge indstillingen **Styklisteskabelon**.

4.  I feltet **Referencenummer** skal du vælge en eksisterende styklisteskabelon, som skal kopieres til den nye styklisteskabelon.

5.  Angiv et navn til skabelonen i feltet **Navn**.

6.  Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.

7.  Klik på **OK**.

Der oprettes en ny styklisteskabelon med linjer, der svarer til linjerne i den oprindelige styklisteskabelon.

## <a name="create-a-template-bom-based-on-an-item-bom"></a>Oprette en styklisteskabelon ud fra en varestykliste

1.  Klik på **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.

2.  Tryk på CTRL+N for at åbne formularen **Opret styklisteskabelon**.

3.  Under **Kopier styklistelinjer fra reference** skal du vælge **Stykliste**.

4.  I feltet **Referencenummer** skal du vælge en styklisteversion. En vare af typen stykliste kopieres til feltet **Varenummer**.

5.  Angiv et navn til skabelonen i feltet **Navn**.

6.  Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.

7.  Klik på **OK**.

Der oprettes en ny styklisteskabelon vha. de linjer, der svarer til linjerne i den stykliste, der er vist i **Styklister**.

## <a name="create-a-template-bom-based-on-a-production-bom"></a>Oprette en styklisteskabelon ud fra en produktionsstykliste

1.  Klik på **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.

2.  Tryk på CTRL+N for at åbne formularen **Opret styklisteskabelon**.

3.  Under **Kopier styklistelinjer fra reference** skal du vælge **Produktion**.

4.  I feltet **Referencenummer** skal du vælge en produktionsstykliste.

5.  Angiv et navn til skabelonen i feltet **Navn**.

6.  Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.

7.  Klik på **OK**.

Der oprettes en ny styklisteskabelon vha. de linjer, der svarer til linjerne i den stykliste, der er vist i **Stykliste**.

## <a name="see-also"></a>Se også

[Styklisteskabeloner](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]