---
title: Indkøbsordrer til et projekt
description: I denne artikel beskrives de forskellige metoder, du kan bruge til at oprette indkøbsordrer for et projekt. Den metode, du bruger, afhænger af formålet med indkøbsordren, og hvornår de købte varer forbruges og debiteres et projekt.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174552"
---
# <a name="purchase-orders-for-a-project"></a>Indkøbsordrer til et projekt

[!include [banner](../includes/banner.md)]

I denne artikel beskrives de forskellige metoder, du kan bruge til at oprette indkøbsordrer for et projekt. Den metode, du bruger, afhænger af formålet med indkøbsordren, og hvornår de købte varer forbruges og debiteres et projekt.

### <a name="methods-for-creating-a-purchase-order"></a>Metoder til oprettelse af en indkøbsordre

Du kan bruge en af forskellige metoder til at oprette en indkøbsordre i Projektstyring og regnskab. Formålet med indkøbsordren angiver, hvornår indkøbsordren bruges, og angiver derfor, hvornår varerne faktureres på et projekt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metode</th>
<th>Formål</th>
<th>Vareforbrug</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Oprette en indkøbsordre direkte fra et projekt.</td>
<td>Brug denne metode til at købe varer fra en ekstern leverandør til forbrug på et projekt. Du kan oprette indkøbsordren på to måder:
<ul>
<li>Fra selve projektet. I dette tilfælde er projektet allerede defineret for indkøbsordren.</li>
<li>Ved at gå til projektindkøbsordren. Du skal både vælge den leverandør og det projekt, som indkøbsordren skal oprettes for.</li>
</ul></td>
<td>Varer er forbrugt, når kreditorfakturaen opdateres.</td>
</tr>
<tr class="even">
<td>Opret en indkøbsordre fra en salgsordre.</td>
<td>Du kan bruge denne metode til at købe varer, når du opretter en salgsordre fra et projekt.</td>
<td>Varerne er brugt, når salgsordren faktureres til kunden.</td>
</tr>
<tr class="odd">
<td>Opret en indkøbsordre ud fra et varebehov.</td>
<td>Du kan bruge denne metode til at købe varer, når du opretter et varebehov fra et projekt.</td>
<td>Varerne bruges, når følgesedlen for varebehovet opdateres.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Når du opdaterer kreditorfakturaen eller følgesedlen, bliver du bedt om at opdatere følgesedlen for varebehovet.

Yderligere oplysninger finder du i [Modtage varer på indkøbsordre ud fra varebehov](tasks/receive-items-purchase-order-item-requirement.md).

