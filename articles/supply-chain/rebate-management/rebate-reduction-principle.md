---
title: Fradragsprincipper for rabat
description: Dette emne beskriver, hvordan du konfigurerer fradragsprincipper. Fradragsprincipper styrer funktionaliteten, når der gælder flere rabatter for samme vare eller transaktion.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: a0cde0c22b69e7605708a647d47530840ce823b1
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270927"
---
# <a name="rebate-reduction-principles"></a>Fradragsprincipper for rabat

[!include [banner](../includes/banner.md)]

Du kan gruppere rabatstyringsaftaler i *fradragsprincipper* for at reducere andre hensættelser, der er knyttet til en vare, og/eller for at reducere resultatværdier i rabatberegninger. Når rabatfradragsprincipper er konfigureret, kan du vælge at tildele dem efter behov til linjerne i rabatstyringsaftalerne.

Reglerne for rabatfradragsprincipper anvendes kun, når rabataftaler overlapper hinanden. Derfor kan de tildele flere rabatter i situationer, hvor flere rabatter ikke skyldes.

## <a name="manage-rebate-reduction-principles"></a>Administrere fradragsprincipper for rabat

Du kan arbejde med rabatfradragsprincipper ved at gå til **Rabatstyring \> Konfiguration \> Fradragsprincipper for rabat**. Brug derefter knapperne i handlingsruden til at tilføje og fjerne fradragsprincipper efter behov. For hvert princip skal du angive felterne som beskrevet i følgende tabel.

| Felt | Betegnelse |
|---|---|
| Fradragsprincip for rabat | Angiv et entydigt navn til rabatfradragsprincippet for rabat. |
| Betegnelse | Indtast en beskrivelse af rabatfradragsprincippet. |
| Anvend fradrag | Markér dette afkrydsningsfelt for at anvende en fradragsbasis på rabatter, der tilhører dette rabatfradragsprincip. |
| Fradragsgrundlag | Hvis du har markeret afkrydsningsfeltet **Anvend fradrag**, skal du vælge fradragsgrundlaget (*Hensættelse*, *Rabatter* eller *Begge*). Hvis du vælger *Begge*, og hvis der både er bogført en hensættelse og en rabat for en tidligere aftale, er det kun rabatten, der anvendes. |
| Udelad fra fradrag | Hvis dette afkrydsningsfelt er markeret, udelukkes hensættelser og rabatter, der tilhører dette rabatfradragsprincip, fra efterfølgende fradrag. Indstillingen i feltet **Fradragsgrundlag** gælder ikke for denne indstilling. |

## <a name="examples-of-rebate-reduction-principle-setups"></a>Eksempler på opsætninger af rabatfradragsprincip

I følgende tabel vises nogle af de typiske eksempler på opsætninger af rabatfradragsprincip. Værdien i feltet **Beskrivelse** beskriver formålet med rabatfradragsprincippet for hvert af disse rabatfradragsprincipper.

| Fradragsprincip for rabat | Betegnelse | Anvend fradrag | Fradragsgrundlag | Udelad fra fradrag |
|---|---|---|---|---|
| Udskudt | Reducer rabat | Ja | Begge | Ingen |
| Exclreb | Udelad rabat | Ja | Rabat | Ja |
| Kvanti | Flere rabatter | Ja | Begge | Ja |
| None | Kun hensættelse og rabat | Ingen | Begge | Ja |
| Klargør | Kun hensættelse | Ja | Klargør | Ingen |
| Rabat | Kun rabat | Ja | Rabat | Ja |

## <a name="examples-of-rebate-reduction-principle-calculations"></a>Eksempler på beregninger af rabatfradragsprincip

Du har en salgsordre, der indeholder en enkelt salgsordrelinje. Denne linje har værdien 1.000 kr. Følgende aftaler gælder for ordren:

- **Aftale 1:** 10 procent af 1.000 kr
- **Aftale 2:** 15 procent af 1.000 kr
- **Aftale 3:** 20 procent af 1.000 kr
- **Aftale 4:** 25 procent af 1.000 kr

Rækkefølgen af behandling er meget vigtig. Behandlingsrækkefølgen er baseret på den måde, du arbejder på, som det er beskrevet i [Behandle, gennemgå og bogføre rabatter](process-review-post.md).

Resultatet opsummeres f.eks. i følgende tabel, hvis du bruger rækkefølgen *1, 2, 3, 4*, og hvis du kun behandler hensættelserne.

| Aftale | Beskrivelse og indstillinger | Hensættelsesresultat |
|---|---|---|
| 1 | <p>Klassifikationen kontrollerer ikke andre aftaler for fradrag. Kontrollen udføres både for hensættelser og rabatter.</p><ul><li>**Anvend fradrag:** *Nej*</li><li>**Fradragsgrundlag:** *Begge*</li><li>**Udelad fra fradrag:** *Nej*</li></ul> | 1.000 kr × 10 % = 100 |
| 2 | <p>Klassifikationen kontrollerer andre aftaler for fradrag, men markeres, så det selv ignoreres. Denne kontrol udføres kun for rabatter.</p><ul><li>**Anvend fradrag:** *Ja*</li><li>**Fradragsgrundlag:** *Rabat*</li><li>**Udelad fra fradrag:** *Ja*</li></ul> | 1.000 kr × 15 % = 150 |
| 3 | <p>Klassifikationen kontrollerer andre aftaler for fradrag. Kontrollen udføres både for hensættelser og rabatter.</p><ul><li>**Anvend fradrag:** *Ja*</li><li>**Fradragsgrundlag:** *Begge*</li><li>**Udelad fra fradrag:** *Nej*</li></ul> | (1.000 kr – Aftale 1) × 20 % = 180 kr |
| 4 | <p>Klassifikationen kontrollerer andre aftaler for fradrag. Kontrollen udføres både for hensættelser og rabatter.</p><ul><li>**Anvend fradrag:** *Ja*</li><li>**Fradragsgrundlag:** *Begge*</li><li>**Udelad fra fradrag:** *Nej*</li></ul> | (1.000 kr – Aftale 1 – Aftale 3) × 25 % = 180 kr |

Følgende tabel viser nogle eksempler på, hvor hensættelsen behandles i forskellige rækkefølger, og hvor der derfor opnås forskellige totaler. Afvigelsen i hensættelser afhænger af den rækkefølge, som systemet behandler aftalerne i. Det er vigtigt at forstå, hvordan behandlingsrækkefølgen påvirker det endelige rabatbeløb.

| Rækkefølge | Udregning |
|---|---|
| 1<br>(1, 2, 3, 4) | <ul><li>**Aftale 1:** 1.000 kr × 10 % = 100 kr</li><li>**Aftale 2:** 1.000 kr × 15 % = 150 kr</li><li>**Aftale 3:** (1.000 kr – Aftale 1) × 20 % = 180 kr</li><li>**Aftale 4:** (1.000 kr – Aftale 1 – Aftale 2) × 25 % = 180 kr</li><li>**Samlet hensættelse:** 610 kr</li></ul> |
| 2<br>(4, 3, 2, 1) | <ul><li>**Aftale 4:** 1.000 kr x 25 % = 250 kr</li><li>**Aftale 3:** (1.000 kr – Aftale 4) × 20 % = 150 kr</li><li>**Aftale 2:** 1.000 kr x 15 % = 150 kr</li><li>**Aftale 1:** 1.000 kr x 10 % = 100 kr</li><li>**Samlet hensættelse:** 650 kr</li></ul> |
| 3<br>(3, 2, 1, 4) | <ul><li>**Aftale 3:** 1.000 kr x 20 % = 200 kr</li><li>**Aftale 2:** 1.000 kr x 15 % = 150 kr</li><li>**Aftale 1:** 1.000 kr x 10 % = 100 kr</li><li>**Aftale 4:** (1.000 kr – Aftale 3 – Aftale 1) × 25 % = 175 kr</li><li>**Samlet hensættelse:** 625 kr</li></ul> |
| 4<br>(2, 4, 1, 3) | <ul><li>**Aftale 2:** 1.000 kr × 15 % = 150 kr</li><li>**Aftale 4:** 1.000 kr × 25 % = 250 kr</li><li>**Aftale 1:** 1.000 kr × 10 % = 100 kr</li><li>**Aftale 3:** (1.000 kr – Aftale 4 – Aftale 1) × 20 % = 130 kr</li><li>**Samlet hensættelse:** 630 kr</li></ul> |
