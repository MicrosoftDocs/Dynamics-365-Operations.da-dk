---
title: Fremdaterede checks
description: "Denne artikel indeholder oplysninger om understøttelse af fremdaterede checks i Microsoft Dynamics 365 for Finance and Operations. Fremdaterede checks er checks, der udstedes med det formål at foretage og modtage betalinger på en fremtidig dato. Derfor kan checken ikke indløses før den angivne dato."
author: twheeloc
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 8fd721dc3166dcd981b749c673d3c625b4e5ae36
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---

# <a name="postdated-checks"></a>Fremdaterede checks

[!INCLUDE [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om understøttelse af fremdaterede checks i Microsoft Dynamics 365 for Finance and Operations. Fremdaterede checks er checks, der udstedes med det formål at foretage og modtage betalinger på en fremtidig dato. Derfor kan checken ikke indløses før den angivne dato.

Microsoft Dynamics 365 for Finance and Operations understøtter hele administrationscyklussen for fremdaterede checks i både Debitor og Kreditor som vist i følgende tabel.
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
<td>Registrer detaljerne omkring en fremdateret check, før du udsteder til en kreditor. Når betalingen bogføres, genkendes kreditorens gæld, men bankkontoen er endnu ikke kredit. I stedet bruges en clearingkonto til dette formål. </td>
</tr>
<tr class="odd">
<td>Registrere og bogføre en fremdateret check til en debitor</td>
<td>Registrer oplysninger om en fremdateret check, du har modtaget fra en debitor. Når betalingen bogføres, er debitoren kredit, men bankkontoen er endnu ikke debet. I stedet bruges en clearingkonto til dette formål.</td>
</tr>
<tr class="even">
<td>Registrer og bogfør en fremdateret erstatningscheck for en debitor eller kreditor.</td>
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
<td>Du kan annullere en bogført, fremdateret check i disse situationer: - Checken returneres af banken.
- Checken anvendes til en forkert faktura.
- Der modtages et kontantbeløb til dækning af checkbeløbet.
  </td>
  </tr>
  <tr class="even">
  <td>Stands betaling af en fremdateret check.</td>
  <td>Du kan standse betalingen af en fremdateret check, der er udstedt til en leverandør, af forskellige årsager, f.eks. hvis du mangler midler at betale med, hvis aftalen med leverandøren er ændret, hvis leverandøren leverer defekte varer, eller hvis du har returneret varer til leverandøren. Du kan kun standse betalingen, hvis checken ikke allerede er clearet.</td>
  </tr>
  </tbody>
  </table>



Du kan finde flere oplysninger under følgende emner:

[Oprette fremdaterede checks](tasks/set-up-postdated-checks.md)

[Registrere og bogføre en fremdateret check for en debitor](tasks/register-post-postdated-check-customer.md)

[Udligne en fremdateret check fra en debitor](tasks/settle-postdated-check-customer.md)

[Registrere og bogføre en fremdateret check for en kreditor](tasks/register-post-postdated-check-vendor.md) 

[Udligne en fremdateret check for en kreditor](tasks/settle-postdated-check-vendor.md)




