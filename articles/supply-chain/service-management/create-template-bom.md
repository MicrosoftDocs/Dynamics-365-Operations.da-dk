---
title: Oprette en styklisteskabelon
description: Du kan oprette en skabelonstykliste ved hjælp af forskellige fremgangsmåder.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 169b54a0509a2e11ce2e888404da10fd81db475e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678200"
---
# <a name="create-a-template-bom"></a>Oprette en styklisteskabelon   

[!include [banner](../includes/banner.md)]


Du kan oprette en skabelonstykliste ved hjælp af følgende fremgangsmåder. Uanset hvilken fremgangsmåde du vælger, er felterne **Fra dato** og **Til dato** valgfrie og kan kun bruges som ekstra oplysninger.

## <a name="create-a-template-bom-manually"></a>Oprette en styklisteskabelon manuelt

1.  Gå til **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.

2.  Vælg **Ny** for at åbne formularen **Opret styklisteskabelon**.

3.  Under **Kopier styklistelinjer fra reference** skal du vælge indstillingen **Manuel**.

4.  Angiv en vare af typen **Stykliste** i feltet **Varenummer**.

5.  Angiv et navn til skabelonen i feltet **Navn**.

6.  Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.

7.  Vælg **OK**.

Der oprettes en ny tom styklisteskabelon.

## <a name="create-a-template-bom-based-on-another-template-bom"></a>Oprette en styklisteskabelon ud fra en anden styklisteskabelon

1.  Vælg **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.

2.  Vælg **Ny** for at åbne formularen **Opret styklisteskabelon**.

3.  Under **Kopier styklistelinjer fra reference** skal du vælge indstillingen **Styklisteskabelon**.

4.  I feltet **Referencenummer** skal du vælge en eksisterende styklisteskabelon, som skal kopieres til den nye styklisteskabelon.

5.  Angiv et navn til skabelonen i feltet **Navn**.

6.  Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.

7.  Vælg **OK**.

Der oprettes en ny styklisteskabelon med linjer, der svarer til linjerne i den oprindelige styklisteskabelon.

## <a name="create-a-template-bom-based-on-an-item-bom"></a>Oprette en styklisteskabelon ud fra en varestykliste

1.  Vælg **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.

2.  Vælg **Ny** for at åbne formularen **Opret styklisteskabelon**.

3.  Under **Kopier styklistelinjer fra reference** skal du vælge **Stykliste**.

4.  I feltet **Referencenummer** skal du vælge en styklisteversion. En vare af typen stykliste kopieres til feltet **Varenummer**.

5.  Angiv et navn til skabelonen i feltet **Navn**.

6.  Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.

7.  Vælg **OK**.

Der oprettes en ny styklisteskabelon vha. de linjer, der svarer til linjerne i den stykliste, der er vist i **Styklister**.

## <a name="create-a-template-bom-based-on-a-production-bom"></a>Oprette en styklisteskabelon ud fra en produktionsstykliste

1.  Vælg **Servicestyring** \> **Opsætning** \> **Serviceobjekter** \> **Styklisteskabeloner**.

2.  Vælg **Ny** for at åbne formularen **Opret styklisteskabelon**.

3.  Under **Kopier styklistelinjer fra reference** skal du vælge **Produktion**.

4.  I feltet **Referencenummer** skal du vælge en produktionsstykliste.

5.  Angiv et navn til skabelonen i feltet **Navn**.

6.  Angiv det datointerval, hvor styklisteskabelonen skal gælde, i felterne **Fra dato** og **Til dato**.

7.  Vælg **OK**.

Der oprettes en ny styklisteskabelon vha. de linjer, der svarer til linjerne i den stykliste, der er vist i **Stykliste**.

## <a name="see-also"></a>Se også

[Styklisteskabeloner](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]