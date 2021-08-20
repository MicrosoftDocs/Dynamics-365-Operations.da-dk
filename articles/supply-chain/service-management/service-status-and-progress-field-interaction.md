---
title: Interaktion mellem felter med servicestatus og fremskridt
description: I formularen Serviceordrer afspejler feltet Status i serviceordrens header status for hele serviceordren, og Status rapporterer status for de enkelte linjer i serviceordren.
author: ShylaThompson
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 210ff82a904e9657d9808a0994c70683e9126622d279aae94e946be0c4f484c1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756046"
---
# <a name="service-status-and-progress-field-interaction"></a>Interaktion mellem felter med servicestatus og fremskridt 

[!include [banner](../includes/banner.md)]


I formularen **Serviceordrer** afspejler feltet **Status** i serviceordrens header status for hele serviceordren, og **Status** rapporterer status for de enkelte linjer i serviceordren.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Status</p></th>
<th><p>Status for linje 1</p></th>
<th><p>Status for linje 2</p></th>
<th><p>Status for linje 3</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Under behandling</strong></p></td>
<td><p><strong>Oprettet</strong></p></td>
<td><p><strong>Oprettet</strong></p></td>
<td><p><strong>Oprettet</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Under behandling</strong></p></td>
<td><p><strong>Annulleret</strong></p></td>
<td><p><strong>Oprettet</strong></p></td>
<td><p><strong>Oprettet</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Under behandling</strong></p></td>
<td><p><strong>Oprettet</strong></p></td>
<td><p><strong>Annulleret</strong></p></td>
<td><p><strong>Bogført</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Annulleret</strong></p></td>
<td><p><strong>Annulleret</strong></p></td>
<td><p><strong>Annulleret</strong></p></td>
<td><p><strong>Annulleret</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Bogført</strong></p></td>
<td><p><strong>Bogført</strong></p></td>
<td><p><strong>Bogført</strong></p></td>
<td><p><strong>Bogført</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Bogført</strong></p></td>
<td><p><strong>Bogført</strong></p></td>
<td><p><strong>Annulleret</strong></p></td>
<td><p><strong>Annulleret</strong></p></td>
</tr>
</tbody>
</table>


En serviceordre er igangværende, hvis status for alle linjer er **Oprettet**. Den er stadig igangværende, hvis status for nogle af linjerne er **Annulleret** eller **Bogført**.

Hvis alle linjerne i en serviceordre er mærket **Bogført**, er status for ordren **Bogført**. Hvis nogle linjer er **Bogført**, og nogle er **Annulleret**, er status stadig **Bogført**.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]