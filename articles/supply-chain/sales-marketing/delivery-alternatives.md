---
title: Leveringsalternativer
description: Salgordretagerne kan bruge siden Leveringsalternativer til at finde alternative indstillinger for ordreopfyldning.
author: Henrikan
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: henrikan
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: f58f7923d82f3aa371ba916352211195870f9a75
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572619"
---
# <a name="delivery-alternatives"></a>Leveringsalternativer

[!include [banner](../includes/banner.md)]

Salgordretagerne kan bruge siden **Leveringsalternativer** til at finde alternative indstillinger for ordreopfyldning.

Siden **Leveringsalternativer** giver et overblik over alle alternative indstillinger. Det giver også ordretagerne mulighed for at se opfyldningsmuligheder andre steder end i det aktuelle firma. De kan nu få vist både interne salgsmuligheder og salgsmuligheder fra eksterne leverandører. Ved at sortere indstillingerne pr. leveringsdato kan salgsordretagerne få vist en intelligent liste over leveringsalternativer. Desuden hjælper parametre dem med nemmere at administrere de foreslåede leveringer. Da transporttiden kan påvirke leveringsdatoer, kan salgsordretagerne udforske de forskellige transportsmuligheder, som fragtmænd tilbyder. Der vises detaljerede oplysninger om hvert forslag, og ordretagerne kan derfor træffe velfunderede beslutninger direkte fra siden **Leveringsalternativer**.

## <a name="open-the-delivery-alternatives-page"></a>Åbne siden Leveringsalternativer

Du kan åbne siden **Leveringsalternativer** fra salgsordrelinjen.

1. Vælg **Produkter og forsyning \> Leveringsalternativer**.
1. Vælg **Linjedetaljer \> Levering \> Leveringsalternativer**.

Du kan også åbne siden **Leveringsalternativer** ved at åbne arbejdsområdet **Salgsordrebehandling og -forespørgsel** og derefter vælge **Ordrer og favoritter \> Forsinkede ordrelinjer \> Leveringsalternativer** **Bemærk:** Du kan kun åbne siden **Leveringsalternativer**, hvis begge følgende betingelser er opfyldt:

- Alle obligatoriske oplysninger om salgslinjen er udfyldt.
- Feltet **Leveringsdatokontrol** er indstillet til en anden værdi end **Ingen**.

## <a name="delivery-date-control-methods"></a>Leveringsdatokontrolmetoder

Leveringsdatokontrolmetoden bestemmer, hvordan systemet fastsætter leveringsdatoer, hvordan leveringsalternativer beregnes, og hvilke oplysninger der vises. Bemærk, at leveringsdatokontrollen tager kalendere i betragtning. Derfor kan følgende kalendere påvirke den foreslåede modtagelsesdato: lagerstedkalender, transportkalender, kreditorkalender og debitorkalender. I følgende tabel beskrives hver metode for leveringsdatokontrol.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Metode</strong></td>
<td><strong>Beskrivelse</strong></td>
</tr>
<tr class="even">
<td><strong>None</strong></td>
<td><ul>
<li>Leveringsalternativer for salgslinjer understøttes ikke. Denne indstilling deaktiverer leveringsdatokontrollen.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Salgsleveringstid</strong></td>
<td><ul>
<li>Leveringsalternativer beregnes ud fra den foruddefinerede salgsleveringstid. Transportdage beregnes ud fra leveringsmåden.</li>
<li>Leveringsalternativer omfatter lagersteder, der har en disponibel lagerbeholdning og forsynings- og behovsordrer.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>DTT</strong></td>
<td><ul>
<li>Leveringsalternativer beregnes ud fra disponibel til tilsagn-logik (DTT). Den aktuelle tilgængelighed og den forventede fremtidige tilgængelighed indgår i betragtningerne. Transportdage beregnes ud fra leveringsmåden.</li>
<li>Leveringsalternativer omfatter lagersteder, der har en disponibel lagerbeholdning og forsynings- og behovsordrer.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>DTT + afgangsmargen</strong></td>
<td><ul>
<li>Leveringsalternativer beregnes som for DTT-metoden, men afgangsmargenen medtages i beregningen.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>LE</strong></td>
<td><ul>
<li>Leveringsalternativer beregnes ud fra leveringsevne-logik (LE). MPS-udfoldning bruges til at bestemme tilgængeligheden. Bemærk, at LE som minimum forskyder leveringsdatoer til salgsleveringstiden. Transportdage beregnes ud fra leveringsmåden.</li>
<li>Leveringsalternativer omfatter forslag for følgende lagersteder:
<ul>
<li>Aktuelt lagersted</li>
<li>Standardlagersted</li>
<li>Alle lagersteder, der har tilgængelig disponibel lagerbeholdning</li>
<li>Alle lagersteder, der har forsyningsordrer</li>
<li>Alle lagersteder, der har aktive styklisteversioner</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a>Få vist oplysninger om leveringsalternativer

I dette afsnit beskrives de oplysninger om leveringsalternativer, der er tilgængelige i hvert oversigtspanel på siden **Leveringsalternativer**.

### <a name="the-product-fasttab"></a>Oversigtspanelet Produkter

Dette oversigtspanel viser en oversigt over produktet og detaljer om den aktuelle salgslinje.

### <a name="the-delivery-alternatives-fasttab"></a>Oversigtspanelet Leveringsalternativer

I dette oversigtspanel vises en liste over leveringsalternativer, der er sorteret efter kvitteringsdato. Over listen kan du vælge, hvilke indstillinger du vil basere forslagene på. Du kan også vælge den leveringsmåde, der bestemmer transportdagene. Følgende valgmuligheder er tilgængelige:

- **Medtag andre produktvarianter** - Denne indstilling er tilgængelig for produkter, der har produktvarianter. Den omfatter leveringsalternativer til andre varianter af produktet. Denne indstilling er ikke tilgængelig for LE.
- **Inkluder delvis mængde** – Som standard medtages kun forslag, der opfylder det fulde antal på salgslinjen. Vælg denne indstilling for at medtage forslag, der kun delvist opfylder ordrelinjen. Denne indstilling er nyttig, når kunden anmoder om en tidligere leveringsdato og accepterer delvis levering.
- **Medtag senere datoer** – Som standard vises kun forslag, som er bedre (tidligere) end de aktuelle datoer på salgslinjen. Vælg denne indstilling for at medtage senere datoer. Denne indstilling kan være nyttigt i situationer, hvor andre parametre end datoen er prioriteret. For eksempel kan en bestemt leverandør eller et lagersted være foretrukket.
- **Leveringsmåde** – Vælg den foretrukne leveringsmåde for at optimere transporttid og omkostninger. Indvirkningen på de foreslåede leveringsalternativer fremgår med det samme. Det er derfor nemt at sammenligne alternativerne.
- **Medtag indkøb** – Når indkøb er markeret, omfatter de foreslåede leveringsalternativer muligheder for at købe fra både eksterne leverandører og andre firmaer i virksomheden (intern). Indstillingen **Medtag indkøb** understøttes for DTT og DTT + afgangsmargen-leveringsdatokontrol. Indstillinger for indkøb fra standardindskøbsleverandøren for produktet og alle godkendte kreditorer for produktet er inkluderet.
- For eksterne leverandører er beregningen baseret på leveringstiden for indkøbet.
- Internt indgår det i beregningen, hvad der er tilgængeligt fra forsyningsfirmaet, baseret på leveringsdatokontrol i forsyningsfirmaet.
- **Leveringstype** (Relevant for indkøb)
  - **Lager** - Produkterne leveres fra forsyningslagerstedet til lokationen/lagerstedet på salgslinjen. De sendes derefter fra lagerstedet til kunden.
  - **Direkte levering** - Produkterne leveres direkte til kunden fra forsyningslagerstedet.

### <a name="the-availability-information-fasttab"></a>Oversigtspanelet Oplysninger om tilgængelighed

Oplysningerne i dette oversigtspanel er relateret til den alternative leveringslinje, der er valgt. Følgende oplysninger vises, afhængigt af leveringsdatokontrollen for salgslinjen:

- **Salgsleveringstid**
  - **Til rådighed i dag** – Få vist den aktuelle disponible lagerbeholdning, fysisk reserveret og disponibelt fysisk lager.
  - **Parametre** - Viser lagerenheden og salgsleveringstiden.

- **DTT og DTT + afgangsmargen**
  - **Til rådighed i dag** – Få vist den aktuelle disponible lagerbeholdning, fysisk reserveret og disponibelt fysisk lager.
  - **Parametre** - Viser lagerenheden og salgsleveringstiden.
  - **Fremtidig tilgængelighed** – Få vist en grafisk repræsentation af den aktuelle og fremtidige tilgængelighed for valgt lokation og lagersted under **Leveringsalternativer**. Du kan vælge diagramsøjlerne for at se mere detaljerede oplysninger om produktets tilgængelighed fremover. Skyderen viser en liste over relevante behovs- og forsyningsordrer i en DTT-tidshorisont.

- **LE**
  - **Til rådighed i dag** – Få vist den aktuelle disponible lagerbeholdning, fysisk reserveret og disponibelt fysisk lager.
  - **Parametre** - Viser lagerenheden og salgsleveringstiden.
  - **Udfoldning** – Få vist forsyning for den valgte leveringsalternative udfoldet. Du kan bruge **Konfiguration** til at ændre felterne og de lagerdimensioner, der vises i udfoldningen.

### <a name="the-impact-of-selected-alternative-fasttab"></a>Oversigtspanelet Virkning af valgt alternativ

I dette oversigtspanel vises virkningen af det valgte leveringsalternativ. Hvis du vælger **OK**, opdateres salgslinjen med de fremhævede værdier i de valgte kolonner. Bemærk, at hvis antallet i det valgte leveringsalternativ er mindre end antallet på salgslinjen, oprettes en leveranceplan, og ordrelinjen opdeles i to linjer: én linje for det valgte antal og én linje for det resterende antal. Du kan også opdatere den kommercielle linje, så den svarer til linjerne for tidsplanen og påvirker prisfastsættelsen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Ordretilsagn](delivery-dates-available-promise-calculations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]