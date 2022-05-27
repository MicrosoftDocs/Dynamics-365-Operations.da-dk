---
title: Indtægtsfordeling
description: Dette emne indeholder en forklaring på, hvordan du kan konfigurere udskydelse af indtægter i Abonnementsfakturering.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 09d3e9295f1fb753156aa603b00372316173721e
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695240"
---
# <a name="revenue-allocation"></a>Indtægtsfordeling

Dette emne indeholder en forklaring på, hvordan du kan konfigurere udskydelse af indtægter i Abonnementsfakturering. Du kan konfigurere eller redigere omsætningsfordeling, når du opretter faktureringsplanen. Når du åbner siden **Indtægtsfordeling** for en aktiv eller fratrådt faktureringsplan, er felterne skrivebeskyttede.

## <a name="specify-the-revenue-allocation-for-a-billing-schedule"></a>Angive omsætningsfordelingen for en faktureringsplan

Følg disse trin for at redigere milepælsfordeling på en faktureringsplanlinje.

1. Vælg en faktureringsplan eller en faktureringsplanlinje på listesiden **Alle/aktive faktureringsplaner**.
2. Vælg **Indtægtsfordeling** under fanen **Indtægtsfordeling** øverst på siden.
3. Vælg typen af flere elementer-arrangement (MEA) i feltet **Flere element arrangementstyper**.
4. Angiv MEA-nummeret i feltet **Nummer på flere elementer**. Derefter skal du angive kontoen udskudt kontraktomsætning i feltet **Udskudt kontraktomsætningskonto**.

    Hvis du angiver feltet **Opsætningstype for flere elementer** til **Enkelt**, gælder samme kontonummer for **flere elementer** og **Indtægtskonto for udskudt kontrakt** for hver linje. Hvis du angiver feltet **Opsætningstype for flere elementer** til **Flere**, kan du angive forskelligt **Nummer på opsætning med flere varer** og **Indtægtskonto for udskudt kontrakt** for hver linje.
    
    Et MEA-nummer kan kun tildeles to eller flere varer. En enkelt linje kan ikke have sit eget MEA-nummer.

5. Vælg **Gem**.

### <a name="fields"></a>Felter

Siden **Opsætning med flere varer** indeholder følgende felter.

| Felt | Beskrivende tekst |
|---|---| 
| Opsætning med flere varer | <p>Vælg transaktionen til MEA-anmodningen.</p><ul><li>**Multiplum** – Linjeelementerne i transaktionen er en del af MEA, eller der findes mere end én aftale.</li><li>**Ingen** – Posteringen er en standardpostering, der ikke har nogen omsætningsfordeling.</li><li>**Enkelt** – Alle varerne i transaktionen er del af en enkelt MEA.</li></ul> |
| Nummer på opsætning med flere varer | <p>MEA-nummeret for linjen. Dette felt er kun tilgængeligt, når feltet **Opsætning med flere varer** er angivet til **Flere**.</p><p>Hvis dette felt er tomt, og du tildeler et MEA-nummer, opdateres felterne **Enkeltstående salgspris** og **Enkeltstående salgspris** automatisk på basis af værdierne fra siden **Varens enkeltstående salgspris**. Kun de MEA-numre, der tildeles andre linjer på salgsordren, er tilgængelige.</p> |
| Indtægtskonto for udskudt kontrakt | Angiv den konto, der skal bruges til kladdeposter, når der oprettes en MEA-kontraktfaktura. Dette felt er kun tilgængeligt, når fakturering af tilbagevendende kontrakter er aktiveret og i brug. |
| **Linjer** | |
| Variantnummer | Variantnummeret fra salgsordren. |
| Varenummer | Varenummeret fra salgsordren. |
| Faktureringsfrekvens | Vælg frekvensen af fordeling af rabat: **Daglig**, **Månedlig**, **Kvartalsvis**, **Halvårlig** eller **Årlig**. |
| Quantity | Værdien er fra salgsordren. |
| Kontraktværdi | Kontraktværdi. |
| Nummer på opsætning med flere varer | <p>MEA-nummeret for linjen. Dette felt er kun tilgængeligt, når feltet **Opsætning med flere varer** er angivet til **Flere**.</p><p>Hvis dette felt er tomt, og du tildeler et MEA-nummer, opdateres felterne **Enkeltstående salgspris** og **Enkeltstående salgspris** automatisk på basis af værdierne fra siden **Varens enkeltstående salgspris**. Kun de MEA-numre, der tildeles andre linjer på salgsordren, er tilgængelige. Hvis disse værdier ikke er konfigureret for varen, bruges værdierne fra siden **Omsætningsfordelingsparametre for flere elementer**.</p> | 
| Enkeltstående salgsprisoprindelse | <p>Vælg oprindelsen af den enkeltstående salgspris:</p><ul><li>**Beløb** – Den enkeltstående salgspris er et beløb, du angiver, som er over 0 (nul). Beløbet omregnes mellem de funktionelle og de oprindelige valutaer efter behov.</li><li>**Basissalgspris** – Den enkeltstående salgspris svarer til varens basissalgspris.</li><li>**Fakturapris** – Den enkeltstående salgspris svarer til varens fakturapris.</li><li>**Procent af vare** – Den enkeltstående salgspris angives som en procentværdi og beregnes ud fra varens pris. Hvis du vælger denne indstilling, skal du angive standardprocenten.</li><li>**Fordel afrundingsbeløb** – Oprindelsen af den enkeltstående salgspris beregnes som *Samlet kontraktværdi af overordnet vare* – *Samlet enkeltstående salgspris for underordnede varer*:</p><ul><li>*Samlet kontraktværdi af overordnet vare* er nettobeløbet eller faktureret beløb.</li><li>*Samlet enkeltstående salgspris for underordnede varer* er summen af den udvidede salgspris eller kontraktens enkeltstående salgspris for alle underordnede varer, undtagen den underordnede vare, der bruger denne enkeltstående salgsprisoprindelse.</li></ul><p>Hvis det beregnede beløb er en negativ værdi, angives beløbet til 0 (nul).</p><p>**Bemærk:** Denne indstilling kan kun vælges for én underordnet vare i indtægtsopdelingen.</p></li><li>**Ingen** – Oprindelsen af den enkeltstående salgspris er baseret på de underordnede varer. Denne indstilling gælder for varer, der er defineret som overordnede varer i en skabelon til indtægtsopdeling. Hvis afkrydsningsfeltet **Indtægtsopdeling** er markeret, er denne indstilling automatisk markeret, og indstillingen kan ikke ændres.</li><li>**Procent af overordnet fakturapris** – Oprindelsen af den enkeltstående salgspris er en procentdel af fakturaprisen for den overordnede vare. Denne indstilling er kun tilgængelig for underordnede varer i en skabelon til indtægtsopdeling.</li><li>**Procent af overordnet standardpris** – Oprindelsen af den enkeltstående salgspris er en procentdel af standardprisen for den overordnede vare. Denne indstilling er kun tilgængelig for underordnede varer i en skabelon til indtægtsopdeling. Når indstillingen for en underordnet vare ændres fra **Procent af overordnet standardpris** til **Procent af overordnet fakturapris** eller fra **Procent af overordnet fakturapris** til **Procent af overordnet standardpris**, opdateres de beregnede værdier også.</li></ul> |
| Enkeltstående salgspris | <p>Den enkeltstående salgspris for linjen, i transaktionsvalutaen.</p><p>Værdien i feltet **Beløb** angives eller beregnes.</p> |
| Enkeltstående kontraktsalgspris | Enkeltstående kontraktsalgspris. |
| Resterende kontraktindtægt | Kontraktens resterende omsætningsbeløb. Dette beløb er summen af alle de linjer, der endnu ikke er oprettet fakturaer for. |
| Samlet kontraktindtægt | Kontraktens samlede omsætningsbeløb for linjen. Dette beløb er summen af alle de linjer, uanset om der er oprettet fakturaer for dem. |
| Indtægtskonto for udskudt kontrakt | <p>Angiv den konto, der skal bruges til kladdeposter, når der oprettes en MEA-kontraktfaktura.</p><p>Dette felt er kun tilgængeligt, når fakturering af tilbagevendende kontrakter er aktiveret og i brug.</p> |
| Fejl | Eventuelle fejl, der opstod for indtægtsfordelingen. |

## <a name="use-revenue-allocation-on-a-sales-order"></a>Brug indtægtsfordeling på en salgsordre

Hvis du vil bruge funktionen til indtægtsfordeling på en salgsordre, skal du følge disse trin.

1. Opret en salgsordre med varer på siden **Alle salgsordrer**.
2. Vælg **Omsætningsfordeling** under **Indtægtsfordeling** under fanen **Faktura**.
3. Angiv MEA-typen i feltet **Typen på flere elementer**.
4. Angiv MEA-nummeret i feltet **Nummer på flere elementer**.
5. Hvis feltet **Opsætningstype for flere elementer** er angivet til **Flere**, skal du markere de ønskede linjer og derefter vælge **Anvend på valgt**.
6. Vælg **Gem**.

Hvis du bruger indtægts- og udgiftsafregninger, oprettes udskydelsesplanen automatisk. Du kan få vist den på siden **Alle udskydelsesplaner**.
