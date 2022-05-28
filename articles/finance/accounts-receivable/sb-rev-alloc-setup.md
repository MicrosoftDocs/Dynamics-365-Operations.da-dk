---
title: Konfigurer indtægtsfordeling af flere varer
description: Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere parametrene for indtægtsfordeling af flere varer i abonnementsfakturering.
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
ms.openlocfilehash: bb5b220dd941cbb9f1fda5d0eb821a86a9135309
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685793"
---
# <a name="set-up-multiple-element-revenue-allocation"></a>Konfigurer indtægtsfordeling af flere varer

Med indtægtsfordeling af flere varer kan du oprette forskellige skabeloner, der bruges til at beregne og fordele indtægt på tværs af flere varer. Denne funktionalitet kan hjælpe dig med at overholde Accounting Standards Codification Topic 606 (ASC 606) og/eller International Financial Reporting Standard 15 (IFRS 15).

## <a name="multiple-element-revenue-allocation-parameters"></a>Parametre for indtægtsfordeling af flere varer

Brug siden **Parametre for indtægtsfordeling af flere varer** til at konfigurere parametrene for indtægtsfordeling af flere varer.

### <a name="standalone-selling-price-origin"></a>Enkeltstående salgsprisoprindelse

I feltet **Enkeltstående salgsprisoprindelse** angives det, hvor den enkeltstående salgspris kommer fra. Du kan opdatere værdien på siden **Enkeltstående varesalgspris** og på transaktionen. Følgende indstillinger er tilgængelige.

| Indstilling | Beskrivelse |
|--------|-------------|
| Antal | Den enkeltstående salgspris er et beløb, du angiver, som er over 0 (nul). Beløbet omregnes mellem de funktionelle og de oprindelige valutaer efter behov. |
| Basissalgspris | Den enkeltstående salgspris svarer til varens basissalgspris. |
| Fakturapris | Den enkeltstående salgspris svarer til varens fakturapris. |
| Procent af vare | Den enkeltstående salgspris angives som en procentværdi og beregnes ud fra varens pris. Hvis du vælger denne indstilling, skal du angive standardprocenten. |
| Fordel afrundingsbeløb | <p>Oprindelsen af den enkeltstående salgspris beregnes som *Samlet kontraktværdi af overordnet vare* – *Samlet enkeltstående salgspris for underordnede varer*:</p><ul><li>*Samlet kontraktværdi af overordnet vare* er nettobeløbet eller faktureret beløb.</li><li>*Samlet enkeltstående salgspris for underordnede varer* er summen af den udvidede salgspris eller kontraktens enkeltstående salgspris for alle underordnede varer, undtagen den underordnede vare, der bruger denne enkeltstående salgsprisoprindelse.</li></ul><p>Hvis det beregnede beløb er en negativ værdi, angives beløbet til 0 (nul).</p><p>**Bemærk:** Denne indstilling kan kun vælges for én underordnet vare i indtægtsopdelingen.</p> |
| Ingen | Oprindelsen af den enkeltstående salgspris er baseret på de underordnede varer. Denne indstilling gælder for varer, der er defineret som overordnede varer i en skabelon til indtægtsopdeling. Hvis afkrydsningsfeltet **Indtægtsopdeling** er markeret, er denne indstilling automatisk markeret, og indstillingen kan ikke ændres. |
| Procent af overordnet fakturapris | Oprindelsen af den enkeltstående salgspris er en procentdel af fakturaprisen for den overordnede vare. Du kan ændre standardværdien. Denne indstilling er kun tilgængelig for underordnede varer i en skabelon til indtægtsopdeling. |
| Procent af overordnet standardpris | Oprindelsen af den enkeltstående salgspris er en procentdel af standardprisen for den overordnede vare. Du kan ændre standardværdien. Denne indstilling er kun tilgængelig for underordnede varer i en skabelon til indtægtsopdeling. Det er standardindstillingen for underordnede varer. Når indstillingen for en underordnet vare ændres fra **Procent af overordnet standardpris** til **Procent af overordnet fakturapris** eller fra **Procent af overordnet fakturapris** til **Procent af overordnet standardpris**, opdateres de beregnede værdier også. |

### <a name="account-for-revenue-allocation-rounding-differences"></a>Konto til afrundingsforskelle ved indtægtsfordeling

I feltet **Konto til afrundingsforskelle ved indtægtsfordeling** angives den konto, der bruges til at registrere eventuelle afrundingsreguleringer af et indtægtsbeløb i kontrakten. Den er tilgængelig, når der bruges fakturering af tilbagevendende kontrakter.

## <a name="item-standalone-selling-price"></a>Enkeltstående varesalgspris

Brug siden **Enkeltstående varesalgspris** til at angive den oprindelige og enkeltstående salgspris for en vare. De værdier, der er angivet på denne side, bruges som standardværdier på siden **Indtægtsfordeling** i indtægtsfordeling af flere varer og fakturering af tilbagevendende kontrakter.

### <a name="specify-item-standalone-selling-price"></a>Angive enkeltstående varesalgspris

Benyt følgende fremgangsmåde for at angive en enkeltstående pris for en vare.

1. På siden **Enkeltstående varesalgspris** skal du i feltet **Enkeltstående salgsprisoprindelse** vælge oprindelsen af den enkeltstående salgspris.
2. Benyt en af følgende fremgangsmåder, afhængigt af den værdi du valgte i feltet **Enkeltstående salgsprisoprindelse**:

    * Hvis du har valgt **Procent af vare**, skal du angive procentdelen i feltet **Procent**.
    * Hvis du har valgt **Beløb**, skal du angive beløbet i feltet **Enkeltstående salgspris**.

2. Vælg **Tilføj** for hver vare, du vil tilføje på listen.
3. Vælg varekoden i feltet **Varekode**. Vælg varerelationen i feltet **Varerelation**. For varer, hvor afkrydsningsfeltet **Indtægtsopdelt** er ryddet, skal den valgte kombination af en varekode og en varerelation være entydig.
4. Rediger standardværdien af feltet **Enkeltstående salgsprisoprindelse**, **Enkeltstående salgspris** eller **Procent** efter behov.
5. Vælg **Tilføj** for hver overordnede vare, du vil tilføje på listen.
6. Vælg varekoden i feltet **Varekode**. Vælg varerelationen i feltet **Varerelation**.
7. Markér afkrydsningsfeltet **Indtægtsopdelt**.
8. Vælg varerelationen i feltet **Varerelation**. Listen opdateres med den overordnede vare og alle underordnede varer.
9. For den underordnede vare skal du ændre standardværdien af feltet **Enkeltstående salgsprisoprindelse**, **Procent af overordnet standardpris**, **Procent af overordnet fakturapris** eller **Fordel afrundingsbeløb** efter behov.
10. Hvis du vil tilføje flere varer på én gang, skal du vælge **Tilføj varer**.
11. Opdater forespørgslen for at vælge det område af varer, du vil tilføje.
12. Vælg **OK**, gennemse listen over varer, du har tilføjet, og vælg **OK**.

### <a name="fields"></a>Felter

Siden **Enkeltstående varesalgspris** indeholder følgende felter.

| Felt | Beskrivelse |
|-------|-------------|
| Enkeltstående salgsprisoprindelse | <p>Vælg oprindelsen af den enkeltstående salgspris:</p><ul><li>**Beløb** – Den enkeltstående salgspris er et beløb, du angiver, som er over 0 (nul). Beløbet omregnes mellem de funktionelle og de oprindelige valutaer efter behov.</li><li>**Basissalgspris** – Den enkeltstående salgspris svarer til varens basissalgspris.</li><li>**Fakturapris** – Den enkeltstående salgspris svarer til varens fakturapris.</li><li>**Procent af vare** – Den enkeltstående salgspris angives som en procentværdi og beregnes ud fra varens pris. Hvis du vælger denne indstilling, skal du angive standardprocenten.</li></ul>**Fordel afrundingsbeløb** – Oprindelsen af den enkeltstående salgspris beregnes som *Samlet kontraktværdi af overordnet vare* – *Samlet enkeltstående salgspris for underordnede varer*:</p><ul><li>*Samlet kontraktværdi af overordnet vare* er nettobeløbet eller faktureret beløb.</li><li>*Samlet enkeltstående salgspris for underordnede varer* er summen af den udvidede salgspris eller kontraktens enkeltstående salgspris for alle underordnede varer, undtagen den underordnede vare, der bruger denne enkeltstående salgsprisoprindelse.</li></ul><p>Hvis det beregnede beløb er en negativ værdi, angives beløbet til 0 (nul).</p><p>**Bemærk:** Denne indstilling kan kun vælges for én underordnet vare i indtægtsopdelingen.</p></li><li>**Ingen** – Oprindelsen af den enkeltstående salgspris er baseret på de underordnede varer. Denne indstilling gælder for varer, der er defineret som overordnede varer i en skabelon til indtægtsopdeling. Hvis afkrydsningsfeltet **Indtægtsopdeling** er markeret, er denne indstilling automatisk markeret, og indstillingen kan ikke ændres.</li><li>**Procent af overordnet fakturapris** – Oprindelsen af den enkeltstående salgspris er en procentdel af fakturaprisen for den overordnede vare. Du kan ændre standardværdien. Denne indstilling er kun tilgængelig for underordnede varer i en skabelon til indtægtsopdeling.</li><li>**Procent af overordnet standardpris** – Oprindelsen af den enkeltstående salgspris er en procentdel af standardprisen for den overordnede vare. Du kan ændre standardværdien. Denne indstilling er kun tilgængelig for underordnede varer i en skabelon til indtægtsopdeling. Det er standardindstillingen for underordnede varer. Når indstillingen for en underordnet vare ændres fra **Procent af overordnet standardpris** til **Procent af overordnet fakturapris** eller fra **Procent af overordnet fakturapris** til **Procent af overordnet standardpris**, opdateres de beregnede værdier også.</li></ul> |
| Enkeltstående salgspris | Vælg varens enkeltstående salgspris. Dette felt er tilgængeligt, når feltet **Enkeltstående salgsprisoprindelse** er angivet til **Beløb**. |
| Procent | Angiv procentdelen af den enkeltstående salgspris. Dette felt er tilgængeligt, når feltet **Enkeltstående salgsprisoprindelse** er angivet til **Procent af vare**, **Procent af overordnet fakturapris** eller **Procent af overordnet standardpris**. |
| Indtægtsopdelt | <p>Angiv, om der bruges indtægtsopdeling for en linje:</p><ul><li>**Udvalgt** – Der kan kun vælges varer, som en skabelon til indtægtsopdeling er konfigureret til, i feltet **Varerelation**. Du kan kun markere dette afkrydsningsfelt for overordnede varer i en indtægtsopdelt skabelon.</li><li>**Ryddet** – Varen er en standardvare, der ikke bruger indtægtsopdeling.</li></ul> |
| Relation | Et symbol angiver, om varen er en overordnet eller underordnet vare i en indtægtsopdeling. |
| Varekode | <p>Vælg varekoden: **Tabel** eller **Gruppe**.</p><p>Hvis afkrydsningsfeltet **Indtægtsopdelt** er markeret, er dette felt angivet til **Tabel**, og værdien kan ikke ændres.</p> |
| Varerelation | <p>Vælg et varenummer.</p><p>Hvis afkrydsningsfeltet **Indtægtsopdelt** er markeret, er det kun varer, der er overordnede varer, som der er konfigureret en skabelon til indtægtsopdeling for, der kan vælges. Når den overordnede vare er valgt, opdateres listen automatisk med de underordnede varer for den overordnede vare.</p> |
| Overordnet vare | I dette felt vises varenummeret for den overordnede vare. For underordnede varer i en indtægtsopdeling vises varenummeret for den overordnede vare. |

## <a name="mea-templates"></a>MEA-skabeloner

Du kan bruge siden **MEA-skabeloner** til at oprette og redigere MEA-skabelon-id'er (aftale med flere varer). Disse id'er bruges på siden **Indtægtsfordeling** til at samle varer i grupper.

### <a name="create-a-template"></a>Opret en skabelon

Du kan konfigurere en MEA-skabelon på følgende måde.

1. På siden **MEA-skabeloner** skal du vælge **Ny**.
1. Angiv et entydigt id i feltet **MEA-skabelon-id**.
1. Indtast en beskrivelse i feltet **Beskrivelse**.
1. I feltet **Indtægtskonto for udskudt kontrakt** skal du vælge den konto, du vil bruge til kladdeposteringer, når der oprettes en MEA-kontraktfaktura. Dette felt er tilgængeligt, når fakturering af tilbagevendende kontrakter er aktiveret og i brug.
1. Vælg **Gem**.
