---
title: Kombinere serviceordrer
description: Du kan kombinere serviceordrer.
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
ms.openlocfilehash: f89c60561746ac9f1c2e9d611089bfac69089081
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676769"
---
# <a name="combine-service-orders"></a>Kombinere serviceordrer   

[!include [banner](../includes/banner.md)]


Når du opretter serviceordrelinjer automatisk i formularen **Serviceaftaler**, kan du vælge en af følgende indstillinger for at angive, hvordan de skal grupperes:

  - **Efter serviceaftale**

  - **Efter serviceopgave**

  - **Efter medarbejder**

  - **Efter serviceobjekt**

## <a name="example"></a>Eksempel

Du opretter en serviceaftale med 31. marts 2007 som startdato. I feltet **Kombinere serviceordrer** skal du angive **Efter serviceobjekt**. Derefter opretter du følgende serviceaftalelinjer:

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Aftalelinjenummer</p></th>
<th><p>Posteringstype</p></th>
<th><p>Beskrivelse</p></th>
<th><p>Interval</p></th>
<th><p>Seriviceobjekt</p></th>
<th><p>Igangsæt dato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p><strong>Time</strong></p></td>
<td><p>SAL1</p></td>
<td><p>Ugentlig</p></td>
<td><p>X-1</p></td>
<td><p>01-04-2007</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p><strong>Time</strong></p></td>
<td><p>SAL2</p></td>
<td><p>Hver 14. dag</p></td>
<td><p>X-2</p></td>
<td><p>01-04-2007</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p><strong>Time</strong></p></td>
<td><p>SAL3</p></td>
<td><p>Ugentlig</p></td>
<td><p>X-2</p></td>
<td><p>01-04-2007</p></td>
</tr>
</tbody>
</table>


Du angiver ikke tidsvinduer for serviceaftalelinjer. Serviceaftalelinjerne flyttes derfor ikke fra den beregnede dag, de ligger på.

Derefter skal du oprette serviceordrelinjer fra formularen **Opret serviceordrer** fra 01-04-2007 til 30-04-2007.

Der oprettes i alt ti serviceordrer. Da den samlingsindstilling, du har valgt, var **Efter serviceobjekt**, har alle de serviceordrer, der oprettes, kun serviceordrelinjer med ét specifikt serviceobjekt. Serviceordrelinjer, der oprettes ud fra serviceaftalen, og som har samme servicedato og samme objekt, samles på samme serviceordre.


> [!NOTE]
> <P>I dette eksempel har den kalender, der er angivet i formularen <STRONG>Parametre for servicestyring</STRONG>, ingen lukkede dage.</P>



Der sker en yderligere gruppering af serviceordrelinjer efter eventuelle tidsvinduer, du har angivet på serviceaftalelinjerne.

## <a name="see-also"></a>Se også

[Oprette serviceordrer automatisk](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]