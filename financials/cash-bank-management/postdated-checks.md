---
title: Fremdaterede checks
description: "Denne artikel indeholder oplysninger om understøttelse af fremdaterede checks i Microsoft Dynamics 365 for operationer. Fremdaterede checks er checks, der udstedes med det formål at foretage og modtage betalinger på en fremtidig dato. Derfor kan checken ikke indløses før den angivne dato."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 7349771b7f9a1ad4cd5b239f1d10bd3229d2d0df
ms.lasthandoff: 03/31/2017


---

# <a name="postdated-checks"></a>Fremdaterede checks

Denne artikel indeholder oplysninger om understøttelse af fremdaterede checks i Microsoft Dynamics 365 for operationer. Fremdaterede checks er checks, der udstedes med det formål at foretage og modtage betalinger på en fremtidig dato. Derfor kan checken ikke indløses før den angivne dato.

Microsoft Dynamics 365 for operationer understøtter fuldt ud cyklussen for fremdaterede checks i både debitor og kreditor, som vist i følgende tabel.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenarie</th>
<th>Oplysninger</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Oprette fremdaterede checks</td>
<td>Du skal oprette en ny betalingsmetode og angive betalingsrutine for clearingkonti til udstedte checks, modtagne checks og A-skat.</td>
</tr>
<tr class="even">
<td>Registrere og bogføre en fremdateret check for en kreditor</td>
<td>Registrer detaljerne omkring en fremdateret check, før du udsteder til en kreditor. Når betalingen bogføres, genkendes kreditorens gæld, men bankkontoen ikke endnu er kredit. I stedet bruges en clearingkonto til dette formål.</td>
</tr>
<tr class="odd">
<td>Registrere og bogføre en fremdateret check til en debitor</td>
<td>Registrer oplysninger om en fremdateret check, du har modtaget fra en debitor. Når betalingen bogføres, kunden debitor er kredit, men bankkontoen ikke endnu debitering. I stedet bruges en clearingkonto til dette formål.</td>
</tr>
<tr class="even">
<td>Registrere og bogføre en fremdateret erstatningscheck for en debitor eller kreditor</td>
<td>
Hvis din oprindelige check til en kreditor eller fra en debitor går tabt eller beskadiges, kan du udstede en fremdateret erstatningscheck til. Når du registrerer checkoplysningerne, skal du angive en reference til den oprindelige check og angive, at den nye check er en erstatning for den oprindelige. Du kan også bogføre erstatningschecken.</td>
</tr>
<tr class="odd">
<td>Overføre en fremdateret debitorcheck til en kreditor</td>
<td>Når du modtager en fremdateret check fra en debitor, kan du overføre den pågældende check til en kreditor som betaling.</td>
</tr>
<tr class="even">
<td>Udligne en fremdateret check for en debitor eller kreditor</td>
<td>Du kan udligne en fremdateret check, der er bogført på en mellemkonto, for en debitor eller en kreditor, når checken forfalder. Når checken er udlignet, er banken endelig debet eller kredit mod den clearingkonto, der blev brugt tidligere.</td>
</tr>
<tr class="odd">
<td>Annullere en fremdateret check for en kreditor</td>
<td>Du kan annullere en bogført, fremdateret check i disse situationer:-checken returneres af banken.
-Kontrollen er anvendt på en forkert faktura.
-En kontantbetaling foretages dækning af checkbeløbet.
</td>
</tr>
<tr class="even">
<td>Standse betalingen for en fremdateret check</td>
<td>Du kan standse betalingen af en fremdateret check, der er udstedt til en leverandør, af forskellige årsager, f.eks. hvis du mangler midler at betale med, hvis aftalen med leverandøren er ændret, hvis leverandøren leverer defekte varer, eller hvis du har returneret varer til leverandøren. Du kan kun standse betalingen checks, der ikke har fjernet.</td>
</tr>
</tbody>
</table>





