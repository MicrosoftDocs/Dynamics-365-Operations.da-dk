---
title: Omkostningskonfiguration for fordelt ordrestyring (DOM)
description: Denne artikel beskriver omkostningskonfiguration til fordelt ordrestyring (DOM) i Dynamics 365 Commerce.
author: josaw1
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9aaff8f627adcd00be174a0b5f7bd398300cfef9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862012"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a>Omkostningskonfiguration for fordelt ordrestyring (DOM)

[!include [banner](../includes/banner.md)]

Organisationer betragter flere omkostningskomponenter for at bestemme den optimale lokation, som ordren skal opfyldes fra. Nogle af disse omkostningskomponenter er forsendelsesomkostninger, håndteringsomkostninger og emballageomkostninger. Der beregnes en kombination af disse omkostninger for at bestemme opfyldelseslokationen.

Når den første gentagelse af den fordelte ordrestyring (DOM) i Dynamics 365 Commerce har optimeret tildelingen af ordrer på opfyldelseslokationer, er den kun indregnet i afstanden. Selvom afstanden kan korreleres med en omkostning, er det ikke det samme som omkostning. En forsendelsesmetode om natten koster f.eks. mere end tre dages forsendelse eller syv dages forsendelse over den samme afstand.

Med funktionen til omkostningskonfiguration kan detailforretninger definere og konfigurere yderligere omkostningskomponenter, der skal beregnes og medtages for at bestemme den optimale lokation, som ordrelinjer skal opfyldes fra.

Når omkostningskomponenter er konfigureret, bruger DOM-problemløseren kun disse omkostningsdefinitioner til at bestemme den optimale lokation for ordreopfyldelse. Den betragter ikke afstandskomponenten som en omkostning. Men, hvis ingen omkostningskomponenter er konfigureret, bruger DOM-problemløseren ikke afstandskomponenten som en omkostning til at bestemme den optimale lokation for ordreopfyldelse.

## <a name="set-up-cost-components"></a>Konfigurere omkostningskomponenter

Der kan defineres to overordnede typer af omkostningskomponenter i systemet: **Forsendelse** og **Anden**.

Begge typer af omkostningskomponent understøtter flere beregningsbasis, som vist i følgende tabel.

<table>
<thead>
<tr>
<th>Type af omkostningskomponent</th>
<th>Beregningsbasis</th>
</tr>
</thead>
<tbody>
<tr>
<td>Forsendelse</td>
<td>
<ul>
<li>Simpel</li>
<li>Lagdelt</li>
</ul>
</td>
</tr>
<tr>
<td>Anden</td>
<td>
<ul>
<li>Salgsordre</li>
<li>Salgslinje</li>
<li>Lokation</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a>Komponenttype af forsendelsesomkostning

Dette afsnit forklarer, hvordan du kan oprette hver enkelt kombination af omkostningskomponenttypen **Forsendelse** og beregningsbasis for forsendelsesomkostninger. Det forklarer også, hvordan DOM-problemløseren bruger de enkelte kombinationer.

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a>Omkostningskomponenttype = forsendelses- og beregningsbasis = simpel

Hvis der bruges en kombination af omkostningskomponenttypen **Forsendelse** og **Simpel** beregningsbasis, baseres forsendelsesomkostningerne for en leveringsmåde enten på en flad omkostning eller afstand.

Du skal konfigurere følgende felter for denne kombination:

- **Omkostningsfaktor** – Angiv et entydigt id for omkostningsfaktoren.
- **Beskrivelse** – Indtast navnet og beskrivelse for omkostningsfaktoren.
- **Startdato** og **Slutdato** – Du kan bruge disse felter til at begrænse omkostningsfaktoren til et bestemt datointerval. Hvis du ikke udfylder disse felter, gælder for omkostningsfaktoren for en uendelig periode.
- **Aktiv** – Angiv, om omkostningsfaktoren er aktiv. DOM benytter kun aktive omkostningsfaktorer, der er tilknyttet opfyldningsprofilen.
- **Regnskab** – Angiv den juridiske enhed, som omkostningsfaktoren er konfigureret til. Alle linjer i beregningskriterierne skal være for den samme juridiske enhed.
- **Leveringsmåder** – Angiv de leveringsmåder, som omkostningen er konfigureret for.
- **Beregningstype** – Angiv, hvordan omkostningen skal beregnes for en bestemt leveringsmåde. Der understøttes to beregningstyper:

    - **Fast** – En fast omkostning bruges til leveringsmåden. Hvis du vælger denne beregningstype, definerer feltet **Omkostning** de faste omkostninger.
    - **Pr. afstandsenhed** – Omkostningen for leveringsmåden beregnes som den kostværdi, der er angivet i feltet **Omkostning**, gange afstanden mellem leveringsadressen og lokationerne.

- **Omkostning** – Angiv den kostværdi, der skal bruges sammen med feltet **Beregningstype** til at beregne omkostningen for en leveringsmåde.

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a>Omkostningskomponenttype = forsendelses- og beregningsbasis = lagdelt

Hvis der bruges en kombination af omkostningskomponenttypen **Forsendelse** og **Lagdelt** beregningsbasis, baseres forsendelsesomkostningerne for en leveringsmåde enten på en flad omkostning eller afstand. Men i denne kombination baseres afstanden på et lagdelt interval af afstande.

Du skal konfigurere følgende felter for denne kombination:

- **Omkostningsfaktor** – Angiv et entydigt id for omkostningsfaktoren.
- **Beskrivelse** – Indtast navnet og beskrivelse for omkostningsfaktoren.
- **Standardomkostning** – Angiv den omkostning, der skal bruges til en leveringsmåde, hvis afstanden mellem leveringsadressen og lokationen ikke falder i nogen af de lagdelte afstande for leveringsmåden.
- **Startdato** og **Slutdato** – Du kan bruge disse felter til at begrænse omkostningsfaktoren til et bestemt datointerval. Hvis du ikke udfylder disse felter, gælder for omkostningsfaktoren for en uendelig periode.
- **Aktiv** – Angiv, om omkostningsfaktoren er aktiv. DOM benytter kun aktive omkostningsfaktorer, der er tilknyttet opfyldningsprofilen.
- **Regnskab** – Angiv den juridiske enhed, som omkostningsfaktoren er konfigureret til. Alle linjer i beregningskriterierne skal være for den samme juridiske enhed.
- **Leveringsmåder** – Angiv de leveringsmåder, som omkostningen er konfigureret for.
- **Afstandstype** – Angiv, om den lagdelte afstandsdefinition er en afstand i luftlinje eller en vejafstand.
- **Afstandsenheder** – Angiv den enhed, som den lagdelte afstand måles i.
- **Afstand fra** – Angiv startintervallet for den lagdelte afstand.
- **Afstand til** – Angiv slutintervallet for den lagdelte afstand.
- **Beregningstype** – Angiv, hvordan omkostningen skal beregnes for en bestemt leveringsmåde og lagdelt afstand. Der understøttes to beregningstyper:

    - **Fast** – En fast omkostning bruges til leveringsmåden. Hvis du vælger denne beregningstype, definerer feltet **Omkostning** de faste omkostninger.
    - **Pr. afstandsenhed** – Omkostningen for leveringsmåden og den lagdelte afstand beregnes som den kostværdi, der er angivet i feltet **Omkostning**, gange afstanden mellem leveringsadressen og lokationerne.

- **Omkostning** – Angiv den kostværdi, der skal bruges sammen med feltet **Beregningstype** til at beregne omkostningen for en leveringsmåde.

> [!NOTE]
> - Når du definerer lagdelte afstande, validerer systemet, at der ikke er nogen manglende eller overlappende afstande.
> - Den afstandstype, der bruges til leveringsmåden, skal være den samme på tværs af alle de lagdelte afstande.

### <a name="other-cost-component-type"></a>Anden type af omkostningskomponent

Dette afsnit forklarer, hvordan du kan oprette hver enkelt kombination af omkostningskomponenttypen **Anden** og en anden omkostningstype for ikke-forsendelsesomkostninger. Det forklarer også, hvordan DOM-problemløseren bruger de enkelte kombinationer.

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a>Omkostningskomponent type = anden og anden omkostningstype = salgsordre

En kombination af omkostningskomponenttypen **Anden** og den anden omkostningstype **Salgsordre** bruges til at definere ikke-forsendelsesomkostninger på salgsordreniveau.

Du skal konfigurere følgende felter for denne kombination:

- **Omkostningsfaktor** – Angiv et entydigt id for omkostningsfaktoren.
- **Beskrivelse** – Indtast navnet og beskrivelse for omkostningsfaktoren.
- **Startdato** og **Slutdato** – Du kan bruge disse felter til at begrænse omkostningsfaktoren til et bestemt datointerval. Hvis du ikke udfylder disse felter, gælder for omkostningsfaktoren for en uendelig periode.
- **Aktiv** – Angiv, om omkostningsfaktoren er aktiv. DOM benytter kun aktive omkostningsfaktorer, der er tilknyttet opfyldningsprofilen.
- **Omkostninger** – Angiv kostværdien for en ikke-forsendelsesomkostning på salgsordreniveau.

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a>Omkostningskomponent type = anden og anden omkostningstype = salgslinje

En kombination af omkostningskomponenttypen **Anden** og den anden omkostningstype **Salgslinje** bruges til at definere ikke-forsendelsesomkostninger på salgsordrelinjeniveau.

Du skal konfigurere følgende felter for denne kombination:

- **Omkostningsfaktor** – Angiv et entydigt id for omkostningsfaktoren.
- **Beskrivelse** – Indtast navnet og beskrivelse for omkostningsfaktoren.
- **Startdato** og **Slutdato** – Du kan bruge disse felter til at begrænse omkostningsfaktoren til et bestemt datointerval. Hvis du ikke udfylder disse felter, gælder for omkostningsfaktoren for en uendelig periode.
- **Aktiv** – Angiv, om omkostningsfaktoren er aktiv. DOM benytter kun aktive omkostningsfaktorer, der er tilknyttet opfyldningsprofilen.
- **Omkostninger** – Angiv kostværdien for en ikke-forsendelsesomkostning på salgsordrelinjeniveau.

#### <a name="cost-component-type--other-and-other-cost-type--location"></a>Omkostningskomponent type = anden og anden omkostningstype = lokation

En kombination af omkostningskomponenttypen **Anden** og den anden omkostningstype **Lokation** bruges til at definere ikke-forsendelsesomkostninger for en gruppe af lokationer eller en enkelt lokation.

Du skal konfigurere følgende felter for denne kombination:

- **Omkostningsfaktor** – Angiv et entydigt id for omkostningsfaktoren.
- **Beskrivelse** – Indtast navnet og beskrivelse for omkostningsfaktoren.
- **Startdato** og **Slutdato** – Du kan bruge disse felter til at begrænse omkostningsfaktoren til et bestemt datointerval. Hvis du ikke udfylder disse felter, gælder for omkostningsfaktoren for en uendelig periode.
- **Aktiv** – Angiv, om omkostningsfaktoren er aktiv. DOM benytter kun aktive omkostningsfaktorer, der er tilknyttet opfyldningsprofilen.
- **Opfyldelsesgruppe** – Angiv den gruppe af lokationer, som ikke-forsendelsesomkostningen er defineret for.
- **Opfyldelseslokation** – Angiv den lokation, som ikke-forsendelsesomkostningen er defineret for.

    > [!NOTE]
    > Du kan ikke angive en opfyldelsesgruppe og en opfyldelseslokation på den samme linje for lokationsbaserede beregningskriterier.

- **Omkostninger** – Angiv kostværdien for en ikke-forsendelsesomkostning på opfyldelsesgruppeniveau eller opfyldelseslokationsniveau.

> [!IMPORTANT]
> Hvis DOM skal medtage disse omkostninger, når de køres, skal du føje omkostningsfaktoren til den relevante opfyldelsesprofil.


[!INCLUDE[footer-include](../includes/footer-banner.md)]