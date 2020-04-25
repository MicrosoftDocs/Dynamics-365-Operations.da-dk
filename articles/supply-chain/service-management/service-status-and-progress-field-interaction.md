---
title: Interaktion mellem felter med servicestatus og fremskridt
description: I formularen Serviceordrer afspejler feltet Status i serviceordrens header status for hele serviceordren, og Status rapporterer status for de enkelte linjer i serviceordren.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd70d00f7ce531b225362065dfd9f1f5c1adc754
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207318"
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

  


