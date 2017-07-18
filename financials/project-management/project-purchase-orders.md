---
title: "Indkøbsordrer til et projekt"
description: "I denne artikel beskrives de forskellige metoder, du kan bruge til at oprette indkøbsordrer for et projekt. Den metode, du bruger, afhænger af formålet med indkøbsordren, og hvornår de købte varer forbruges og debiteres et projekt."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 9715d33598c0749ff1ad2523f2fa8834987998ed
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017

---

# <a name="purchase-orders-for-a-project"></a>Indkøbsordrer til et projekt

[!include[banner](../includes/banner.md)]


I denne artikel beskrives de forskellige metoder, du kan bruge til at oprette indkøbsordrer for et projekt. Den metode, du bruger, afhænger af formålet med indkøbsordren, og hvornår de købte varer forbruges og debiteres et projekt.

Du kan i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition bruge flere metoder til at oprette indkøbsordrer for et projekt. Den metode, du bruger, afhænger af formålet med indkøbsordren, hvornår de købte varer forbruges og hvornår de købte varer debiteres et projekt.

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




