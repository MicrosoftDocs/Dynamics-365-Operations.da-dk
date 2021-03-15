---
title: Periodisering af abonnementer
description: Med serviceabonnementer periodiserer du omsætning manuelt i de perioder, der kommer efter den dato, hvor du har faktureret en gebyrtransaktion.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6d0d6c25cc8a19f5ebea3477cd2c957876752fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966074"
---
# <a name="accruing-subscriptions"></a>Periodisering af abonnementer 

[!include [banner](../includes/banner.md)]


Med serviceabonnementer periodiserer du omsætning manuelt i de perioder, der kommer efter den dato, hvor du har faktureret en gebyrtransaktion.

Der oprettes periodiseringsperioder for den fakturaperiode, som du opretter til abonnementsgebyret. Periodiseringsperioderne er baseret på abonnementets periodekode.

Du kan periodisere og tilbageføre periodiseret omsætning.

## <a name="reverse-accruals-of-credit-amounts"></a>Tilbageføre periodiseringer af kreditbeløb

Hvis du krediterer fakturerede abonnementsbeløb, er der to metoder, du kan bruge til at tilbageføre de periodiserede beløb:

  - Du kan tilbageføre hver enkelt postering for periodiseret omsætning individuelt, før du opretter kreditnotaforslaget til posteringen. Dette er den manuelle fremgangsmåde. (manuel)

  - Du kan lade de periodiserede beløb tilbageføre på den dato, hvor kreditnotaen er bogført eller på den oprindelige bogføringsdato for periodiseringen.

Du kan finde flere oplysninger i [Abonnementsparametre (formular)](https://technet.microsoft.com/library/aa619615.aspx).

## <a name="setup-requirements"></a>Konfigurer behov

Hvis du vil periodisere omsætning, skal du sørge for, at følgende datakrav er opfyldt:

## <a name="account-setup"></a>Kontoopsætning

Kontiene **IGVA - Abonnement** og **Periodiseret omsætning - abonnement** skal være oprettet i modulet **Projekt**.

Når du bogfører periodiseret omsætning, debiteres kontoen **IGVA - Abonnement** med det periodiserede beløb, mens kontoen **Periodiseret omsætning - abonnement** krediteres med det periodiserede beløb.

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a>Oprette konti til periodisering af abonnementsindtægt

1.  Klik på **Projektstyring og regnskab** \> **Opsætning** \> **Bogføring** \> **Opsætning af finanskontering**.

2.  Klik på fanen **Omsætningskonti**, og vælg **IGVA - abonnement** eller **Periodiseret omsætning - abonnement** for at konfigurere kontiene.

## <a name="subscription-group-setup"></a>Oprette abonnementsgrupper

Hvis omsætning for abonnementer skal kunne periodiseres, skal afkrydsningsfeltet **Periodiser omsætning** være markeret. Feltet findes i formularen **Abonnementsgrupper** for den gruppe, som er knyttet til abonnementet. Klik på **Servicestyring** \> **Opsætning** \> **Serviceabonnementer** \> **Abonnementsgrupper**.

## <a name="enable-revenue-accrual-on-a-subscription-group"></a>Aktivere omsætningsperiodisering for en abonnementsgruppe

1.  Klik på **Servicestyring** \> **Opsætning** \> **Serviceabonnementer** \> **Abonnementsgrupper**.

## <a name="periods"></a>Perioder

Du skal oprette en periodekode til fakturering. Medmindre du vil periodisere omsætning i de samme tidsperioder, som du bruger til fakturering, skal du også oprette en periodiseringsperiode.

I oversigten nedenfor kan du se, hvilke periodiseringsperioder du kan oprette til hver enkelt faktureringsperiode:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Faktureringstermin</p></th>
<th><p>Periodiseringsperiode</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>År</strong></p></td>
<td><ul>
<li><p><strong>År</strong></p></li>
<li><p><strong>Kvartal</strong></p></li>
<li><p><strong>Måned</strong></p></li>
<li><p><strong>Dag</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Kvartal</strong></p></td>
<td><ul>
<li><p><strong>Kvartal</strong></p></li>
<li><p><strong>Måned</strong></p></li>
<li><p><strong>Dag</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Måned</strong></p></td>
<td><ul>
<li><p><strong>Måned</strong></p></li>
<li><p><strong>Dag</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Uge</strong></p></td>
<td><ul>
<li><p><strong>Dag</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Dag</strong></p></td>
<td><ul>
<li><p><strong>Dag</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>

Opsætning af faktureringsperioden er en obligatorisk del af den generelle opsætning af abonnementsgrupper. Du kan bestemme, om der også skal oprettes en periodiseringsperiode for abonnementsgruppen. Hvis du opretter en periodiseringsgruppe til abonnementsgruppen, foreslås denne periode i feltet **Periodekode**. Feltet findes i formularen **Periodiser abonnementsindtægt**, når du periodiserer abonnementsindtægt. Det er dog valgfrit, om du vil angive en periodiseringsperiode til abonnementsgruppen.


> [!NOTE]
> <P>Brug følgende sti til at åbne formularen <STRONG>Periodiser abonnementsindtægt</STRONG>. Klik på <STRONG>Servicestyring</STRONG> &gt; <STRONG>Periodisk</STRONG> &gt; <STRONG>Serviceabonnementer</STRONG> &gt; <STRONG>Periodiser abonnementsindtægt</STRONG>.</P>


## <a name="transactions"></a>Poster

Du kan styre antallet af finansposteringer, der oprettes, når du bogfører periodiseret omsætning. I forbindelse med abonnementer skal du definere, om finansposteringer skal oprettes som en total eller pr. linje.

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a>Angive, hvor detaljerede bogføringsoplysninger der skal vises om periodiserede posteringer

1.  Klik på **Projektstyring og regnskab** \> **Opsætning** \> **Parametre for projektstyring og regnskab**.

2.  Under fanen **Økonomisk** i feltet **Faktura** skal du vælge **Total** eller **Linje**.


## <a name="see-also"></a>Se også

[Periodiser abonnementsindtægt](accrue-subscription-revenue.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]