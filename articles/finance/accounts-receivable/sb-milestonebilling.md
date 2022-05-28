---
title: Skabeloner for milepæl
description: Dette emne indeholder en forklaring på, hvordan du kan konfigurere milepælsfakturering i Abonnementsfakturering.
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
ms.openlocfilehash: ecc4ddbb4d22eefac36f8cf8205d3b6084bd7d9d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686485"
---
# <a name="milestone-billing"></a>Milepælsfakturering

[!include [banner](../includes/banner.md)]

Dette emne indeholder en forklaring på, hvordan du definerer skabeloner til funktionen milepælsfakturering i Abonnementsfakturering. For hver linje i milepælsskabelonen kan du definere fordelingsprocenten eller -beløbet. Du kan derefter tildele milepælsskabelonen til faktureringsplanelementer, der bruger funktionen til milepælsfakturering.

## <a name="add-a-template"></a>Tilføj en skabelon

Følg disse trin for at tilføje en milepælsskabelon.

1. Gå til **Abonnementsfakturering \> Fakturering af tilbagevendende kontrakter \> Konfiguration \> Milepælsskabeloner**.
2. Vælg **Ny**.
3. Angiv et entydigt id for den nye skabelon i feltet **Milepælsskabelon**.
4. Indtast en beskrivelse i feltet **Beskrivelse**.
5. Vælg en fordelingsmetode i feltet **Fordelingsmetode**.
6. Valgfrit: Angiv det samlede beløb for skabelonen i feltet **Samlet beløb**.
7. Vælg **Tilføj** for at tilføje en linje. Vælg varenummeret for den nye linje i feltet **Varenummer**.
8. Benyt en af følgende fremgangsmåder, afhængigt af den værdi du valgte i feltet **Fordelingsmetode**:

    - Hvis du har valgt **Procent** som fordelingsmetode, skal du angive fordelingsprocenten for hver linje i feltet **Procent**. Hvis du angiver procenter, skal summen af procenter, der vises i feltet **Samlet procent**, være lig med **100**.
    - Hvis du har valgt **Variabelt beløb** som fordelingsmetode, skal du angive beløbet for hver linje i feltet **Beløb**.
    - Hvis du har valgt **Lige stort beløb** som fordelingsmetode, behøver du ikke angive et beløb. Hver linje opdateres med den korrekte procentdel og det korrekte beløb baseret på antallet af varer, der føjes til skabelonen.

9. Vælg **Gem**.

## <a name="delete-a-template"></a>Slette en skabelon

Følg disse trin for at slette en milepælsskabelon.

1. Vælg en eller flere linjer til sletning, og vælg derefter **Slet**.
2. Vælg **Ja**, når du bliver bedt om at bekræfte handlingen.

## <a name="milestone-template-fields"></a>Felter med milepælsskabeloner

Siden **Milepælsskabelon** indeholder følgende felter.

| Felt | Beskrivelse |
|-------|-------------| 
| Skabelon for milepæl | Entydigt id for milepælsskabelonen. |
| Beskrivelse | Beskrivelsen af milepælsskabelonen. |
| Fordelingsmetode | <p>Vælg fordelingsmetoden:</p><ul><li>**Færdiggørelsesgrad** – En akkumuleret færdiggørelsesværdi bruges til hver linje.</li><li>**Procent** – Der kan angives et procentbeløb til fordelingen. Summen af alle procenterne skal være 100.</li><li>**Variabelt beløb** – Der kan angives et beløb til fordelingen. Fordelingsbeløbet angives på transaktionsniveau.</li><li>**Lige stort beløb** – Fordelingsprocenterne beregnes automatisk og fordeles ligeligt mellem varerne i skabelonen.</li></ul> |
| Samlet beløb | Angiv milepælsbeløbet for skabelonen. |
| **Linjer** | |
| Varenummer | Vælg varenummeret for milepælsskabelonen. |
| Produktnavn | Varens navn. |
| Procentdel | <p>Angiv fordelingsprocenten for linjen:</p><ul><li>Hvis feltet **Fordelingsmetode** er angivet til **Procent**, skal du angive procenten for linjen.</li><li>Hvis feltet **Fordelingsmetode** er angivet til **Lige stort beløb**, deles procenten automatisk i lige store procentdele baseret på antallet af varer i skabelonen.</li></ul><p>Summen af alle procenterne skal være 100.</p><p>Hvis der er angivet en værdi for et **Samlet beløb** i hovedet, og du ændrer **Procent**-værdien for linjen, opdateres **Beløb**-værdien. Omvendt, hvis du ændrer værdien **Beløb**, opdateres **Procent**-værdien.</p> |
| Beløb | <p>Linjens fordelingsbeløb:</p><ul><li>Hvis feltet **Fordelingsmetode** er angivet til **Variabelt beløb**, skal du angive beløbet for linjen.</li><li>Hvis feltet **Fordelingsmetode** er angivet til **Lige store beløb**, deles beløbet automatisk i lige store beløb baseret på antallet af varer i skabelonen og værdien af **Samlet beløb**, der er angivet i hovedet.</li></ul><p>Summen af alle beløb skal være lig med den **Samlet beløb**-værdi, der er angivet i hovedet.</p><p>Hvis der er angivet en værdi for et **Samlet beløb** i hovedet, og du ændrer **Beløb**-værdien for linjen, opdateres **Procent**-værdien. Omvendt, hvis du ændrer værdien **Procent**, opdateres **Beløb**-værdien.</p> |
| **I alt** | |
| Samlet procentdel | Summen af procenter. Summen af alle procenterne skal være 100. |
| Samlet beløb | Summen af **Beløb**-værdier for alle linjer. Summen skal være lig med den **Samlet beløb**-værdi, der er angivet i hovedet. |
| Restbeløb | Resterende beløb. Værdien beregnes som værdien af **Samlet beløb** fra hovedet minus summen af **Beløb**-værdier for alle linjer.|

## <a name="milestone-allocation"></a>Milepælsfordeling

Før du begynder at bruge milepælsfunktionen, skal du udføre disse opgaver.

1. Tilføj en eller flere milepælsskabeloner.
2. Opret en faktureringsplangruppe. Angiv **Milepæl** som varetype, og vælg en skabelon.
3. Vælg en varerelation og en milepælsskabelon for vareopsætningen på siden **Vareopsætning** (**Abonnementsfakturering \> Fakturering af tilbagevendende kontrakt \> Konfiguration \> Varer**).

Når du har oprettet milepælsskabelonerne, faktureringsplangrupperne og varerne, kan du oprette en faktureringsplan, der bruger milepælsfunktionen.

Hvis du vil konfigurere en faktureringsplan, der bruger milepæle, skal du følge disse trin.

1. Vælg **Ny** på listen **Alle/Aktive faktureringsplaner** på siden **Faktureringsplaner**.
2. Opret en ny faktureringsplan på siden **Alle faktureringsplaner**, og angiv en debitorkonto og en startdato.
3. I sektionen **Faktureringsplanlinjer** skal du vælge **Tilføj linje**. Tilføj derefter et varenummer, og angiv feltet **Varetype** til **Milepæl**.

    Hvis der er konfigureret en standardskabelon for milepæle for varen, føjes milepælshændelserne automatisk til faktureringsplanlinjerne. Der er ikke angivet slutdatoer for milepælslinjer.

    Hvis der ikke er oprettet en milepælsskabelon til varen, skal du vælge **Milepælsfordeling**. Vælg derefter en milepælsskabelon på siden **Milepælsfordeling**, og foretag eventuelle nødvendige opdateringer. Vælg derefter **Luk** for at vende tilbage til faktureringsplanen, og afslut oprettelsen af faktureringsplanen.

4. Hvis du vil oprette fakturaer til faktureringsplanen, skal du opdatere slutdatoen for hver milepælshændelse. Hvis du vil bruge en enkelt faktureringsplan, kan du opdatere slutdatoen for milepælshændelsen på faktureringsplanlinjerne. Hvis du vil opdatere flere faktureringsplaner, skal du vælge **Processen Opdater fuldførelsesdato**.
5. Når slutdatoen er opdateret, kan du oprette fakturaen. Hvis du vil oprette en enkelt faktureringsplan , skal du vælge **Generér faktura** på siden **Alle faktureringsplaner**. Hvis du vil oprette fakturaer for flere faktureringsplaner, skal du vælge **Generér faktura** eller **Generér fakturabatchbehandling** under **Periodiske opgaver**.

## <a name="edit-milestone-allocation-on-a-billing-schedule-line"></a>Redigere milepælsfordeling på en faktureringsplanlinje

Følg disse trin for at redigere milepælsfordeling på en faktureringsplanlinje.

1. Vælg nummeret på faktureringsplanen i feltet **Planlæg nummer** på siden **Faktureringsplaner** > **Alle eller aktive faktureringsplaner**.
2. Angiv en vare i sektionen **Faktureringsplanlinjer**, angiv **Milepæl** som vare, og vælg **Milepælsfordeling**.
3. Vælg en milepælsskabelon til i feltet **Milepælsskabelon**.
4. Vælg **Behandling**. Linjerne i milepælsskabelonen føjes automatisk til faktureringsplanlinjerne.

## <a name="milestone-allocation-fields"></a>Milepælsfordelingsfelter

Siden **Milepælsfordeling** indeholder følgende felter.

| Felt | Beskrivelse |
|-------|-------------|
| Overordnet vare | Det overordnede varenummer. |
| Udvidet pris | <p>Udvidet pris på varen. Værdien svarer til **Nettobeløb**-værdien for faktureringsplanlinjen.</p></p>Til en overordnet milepælsvare er standardværdien **Samlet beløb**, der er angivet for milepælsskabelonen. Hvis det samlede beløb er 0 (nul), er standardværdien **Nettobeløb** for faktureringsplanlinjen.</p> |
| Skabelon for milepæl | Milepælsskabelonens id for linjevaren. |
| Beskrivelse af skabelon | Beskrivelsen af milepælsskabelonen. |
| Fordelingsmetode | Den fordelingsmetode, der bruges til milepælsskabelonen. |
| **Linjer** | Standardværdierne for alle linjer er baseret på den valgte milepælsskabelon. Du kan ændre dem efter behov. |
| Varenummer | Varenummeret for milepælens fordelingsskabelon. |
| Produktnavn | Produktnavnet. |
| Procentdel | <p>Fordelingsprocenten for linjen. Summen af alle procenterne skal være 100.</p><p>Hvis du ændrer værdien **Procent** for linjen, opdateres **Nettobeløb**-værdien. Omvendt, hvis du ændrer værdien **Nettobeløb**, opdateres **Procent**.</p> |
| Nettobeløb | <p>Linjens fordelingsbeløb. Summen af nettobeløb for alle linjer skal være lig med den **Udvidet pris**-værdi, der er angivet i hovedet.</p><p>Hvis du ændrer værdien af **Nettobeløb** for linjen, opdateres **Procent**. Omvendt, hvis du ændrer værdien **Procent**, opdateres **Nettobeløb**-værdien.</p> |
| **I alt** | |
| Procent i alt | Summen af **Procent**-værdier for alle linjer. Denne sum skal være lig med 100. |
| Samlet beløb | Summen af **Nettobeløb**-værdier for alle linjer. Summen skal være lig med den **Udvidet pris**-værdi, der er angivet i hovedet. |
| Restbeløb | Resterende beløb. Værdien beregnes som værdien af **Udvidet pris** fra hovedet minus summen af **Nettobeløb**-værdier for alle linjer. Slutbeløbet skal være 0 (nul). |
