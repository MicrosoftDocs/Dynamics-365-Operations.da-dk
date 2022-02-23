---
title: Produktparathed
description: I følgende emner forklares det, hvordan du kan bruge parathedskontroller til at sikre, at de nødvendige masterdata er fuldført for et produkt, før det bruges i transaktioner.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8321a0d8516a6c2c085ce9c1236f70af1cca98da
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967252"
---
# <a name="product-readiness"></a>Produktparathed

[!include [banner](../includes/banner.md)]

Du kan bruge parathedskontroller til at sikre, at alle de nødvendige masterdata er angivet for et produkt, før det bruges i transaktioner. Når der bruges parathedskontrol, bliver en bruger eller et team ansvarlig for at validere specifikke foruddefinerede produktrelaterede data. Hvis der er en åben parathedskontrol af et produkt, kan produktet ikke frigives eller bruges i transaktioner.

Afkrydsningsfelt **Aktiv** for et teknisk produkt, en variant eller en version er kun tilgængeligt, når alle nødvendige data er angivet og kontrolleret, og når alle parathedskontroller er blevet behandlet. På dette tidspunkt kan produktet, versionen eller varianten frigives til andre firmaer og bruges i transaktioner. Du kan oprette parathedskontroller for nye produkter, nye varianter og nye tekniske versioner.

## <a name="types-of-readiness-checks"></a>Typer af parathedskontrol

Der er tre typer parathedskontrol:

- **Systemkontrol** – Systemet kontrollerer, om der er en gyldig post. Posten kan f.eks. være en aktiv stykliste.
- **Manuel kontrol** – En bruger kontrollerer, om posten er gyldig. En parathedskontrol kan f.eks. kræve validering af standardordreindstillingerne. I nogle tilfælde, som f.eks. når produktet stadig udvikles og derfor ikke vil blive placeret på lager, kræves der ingen standardordreindstillinger. Det kan dog være nødvendigt med standardordreindstillinger for et andet produkt af samme type, fordi produktet kan opbevares på lager. Brugeren er ansvarlig for at vide, hvordan det kan afgøres korrekt, om der kræves en parathedskontrol.
- **Kontrolliste** – Brugeren besvarer en række spørgsmål fra en kontrolliste, og systemet bestemmer, om svarene opfylder forventningerne. Kontrollisten kan have et hvilket som helst emne. Den kan f.eks. bruges til at bestemme, om marketingmateriale eller produktdokumentation er fuldført.

## <a name="how-readiness-checks-are-created-for-a-new-product-variant-or-version"></a>Sådan oprettes parathedskontroller for et nyt produkt, en variant eller version

Når du opretter et nyt teknisk **produkt**, bestemmer systemet, om der er konfigureret en politik for parathedskontrol for den tekniske produktkategori. (Politikker for parathedskontrol kan anvendes på det frigivne produktniveau, det frigivne variantniveau og det tekniske versionsniveau). Hvis der er konfigureret en politik, indtræffer følgende hændelser:

- Der oprettes parathedskontroller for produktet i overensstemmelse med den gældende politik.
- Den tekniske version angives til inaktiv, så produktet forhindres i at blive brugt. Alle versionerne for det specifikke produkt, der er involveret, angives som inaktive.

Hvis der oprettes en ny **variant** for et produkt, kontrollerer systemet, om der er konfigureret parathedskontrol på den tekniske produkt kategori. (Parathedskontrol kan anvendes på det frigivne variantniveau og det tekniske versionsniveau). Hvis der er konfigureret en parathedskontrol, indtræffer følgende hændelser:

- Der oprettes parathedskontrol for produktet.
- Den tekniske version angives til inaktiv, så produktet forhindres i at blive brugt.

Hvis der oprettes en ny teknisk **version** for et produkt, kontrollerer systemet, om der er konfigureret parathedskontrol på den tekniske produkt kategori. (Parathedskontrol kan anvendes på det tekniske versionsniveau). Hvis der er konfigureret en parathedskontrol, indtræffer følgende hændelser:

- Der oprettes parathedskontrol for produktet.
- Den tekniske version angives til inaktiv, så produktet forhindres i at blive brugt.

## <a name="view-readiness-checks"></a>Se parathedskontrol

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>Se åbne parathedskontroller for et produkt eller en produktversion

Hvis du vil finde de åbne parathedskontroller for et produkt, skal du åbne siden **Detaljer om frigivne produkter**. Vælg derefter **Parathedskontrol** i gruppen **Parathedskontrol** under fanen **Produkt** i handlingsruden.

Hvis du vil finde de åbne parathedskontroller for en produktversion, skal du åbne siden **Tekniske versioner** for et frigivet produkt og vælge en version. Vælg **Parathedskontrol** i gruppen **Kontrolliste** under fanen **Produkt** i handlingsruden.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>Se åbne parathedskontroller, der er tildelt dig

Hvis du vil have vist de åbne parathedskontroller, som du er tildelt, skal du følge et af disse trin.

- Gå til **Styring af teknisk ændring \> Fælles \> Produktparathed \> Mine åbne parathedskontroller**.
- Gå til **Administration af produktoplysninger \> Arbejdsområder \> Produktparathed til diskret produktion**.

Den opsætning, der angiver, hvem der er knyttet til en parathedskontrol, udføres for den tekniske produktkategori. Der kan tildeles parathedskontrol til en person eller et team. Hvis et team har fået en parathedskontrol, er der én person på det team, der skal behandle parathedskontrollen. Du kan finde flere oplysninger under [Tekniske versioner og tekniske produktkategorier](engineering-versions-product-category.md).

## <a name="process-open-readiness-checks"></a>Behandle åbne parathedskontroller

### <a name="process-system-and-manual-readiness-checks"></a>Behandle systemparathedskontroller og manuelle parathedskontroller

Når du har åbnet siden **Parathedskontrol**, kan du se emnet for systemets og manuelle parathedskontroller ved at vælge **Vis relaterede oplysninger** i handlingsruden. Du kan derefter fuldføre og/eller validere dataene for parathedskontrollen. Åbne parathedskontroller har **Status**-værdien *Afventer*. Denne status angiver, at parathedskontrollen stadig skal behandles. Hvis du vil behandle en parathedskontrol, skal du benytte en af følgende fremgangsmåder.

- I handlingsruden skal du vælge **Kontrollér/fuldfør** for at gennemgå og fuldføre parathedskontrollen. Når du er færdig, opdateres feltet **Status** til *Bestået*.
- Vælg **Spring over** i handlingsruden , hvis du vil springe en parathedskontrol over, der ikke er obligatorisk. Du kan f.eks. konfigurere en parathedskontrol af prisberegninger. Du beslutter dog at springe denne kontrol over, mens produktet stadig er i designfasen. I dette tilfælde opdateres feltet **Status** til *Sprunget over*.

Afhængigt af konfigurationen af parathedspolitikken, når feltet **Status** for en parathedskontrol opdateres til *Bestået*, kan det være nødvendigt med et ekstra trin for at godkende parathedskontrollen. I dette tilfælde skal du vælge **Godkendelse** for at fuldføre kontrollen af parathed. Dette godkendelsestrin er altid obligatorisk, når parathedskontrollen springes over.

Når alle åbne parathedskontroller for et nyt produkt, en variant eller version er blevet behandlet og godkendt som krævet, aktiveres varen automatisk og er derfor klar til brug.

### <a name="process-checklist-readiness-checks"></a>Behandle kontrolliste til parathedskontroller

Hvis du vil åbne en kontrolliste, skal du åbne siden **Parathedskontrol** og derefter vælge **Start kontrolliste** i handlingsruden. Når du er færdig med kontrollisten, kontrollerer systemet, om parathedskontrollen er bestået, baseret på indstillingerne i spørgeskemaet. Hvis kontrollen er bestået, opdateres feltet **Status** til *Bestået*. Hvis parathedskontrollen ikke er obligatorisk, kan du springe den over. I dette tilfælde opdateres feltet **Status** til *Sprunget over*.

Afhængigt af konfigurationen af parathedspolitikken, når feltet **Status** for en parathedskontrol opdateres til *Bestået*, kan det være nødvendigt med et ekstra trin for at godkende parathedskontrollen. I dette tilfælde skal du vælge **Godkendelse** for at fuldføre kontrollen af parathed. Dette godkendelsestrin er altid obligatorisk, når parathedskontrollen springes over.

Når alle åbne parathedskontroller for et nyt produkt, en variant eller version er blevet behandlet og godkendt som påkrævet, aktiveres varen automatisk og er derfor klar til brug.

## <a name="create-and-manage-product-readiness-policies"></a>Oprette og administrere politikker for produktparathed

Brug politikker for produktparathed til at administrere de parathedskontroller, der gælder for et produkt. Da der er tildelt en parathedspolitik til den tekniske kategori, gælder alle kontroller i parathedspolitikken for alle de tekniske produkter, der er baseret på den tekniske kategori. Du kan finde flere oplysninger under [Tekniske versioner og tekniske produktkategorier](engineering-versions-product-category.md).

Hver parathedspolitik indeholder et sæt parathedskontroller. Når en parathedspolitik tildeles en teknisk produktkategori, vil alle de produkter, der oprettes ud fra den tekniske produktkategori, have de parathedskontroller, der er angivet i parathedspolitikken.

Hvis du vil arbejde med produkters parathedspolitikker, skal du gå til **Styring af tekniske ændringer \> Konfiguration \> Politikker for produktparathed**. Udfør derefter ét af følgende trin.

- Hvis du vil oprette en ny politik, skal du vælge **Ny** i handlingsruden og derefter angive felterne som beskrevet i følgende underafsnit.
- Hvis du vil redigere en eksisterende politik, skal du vælge den i listeruden, vælge **Rediger** i handlingsruden og derefter angive felterne som beskrevet i følgende underafsnit.
- Hvis du vil slette en eksisterende politik, skal du vælge den i listeruden, vælge **Rediger** i handlingsruden og derefter kontrollere, at **Aktiv**-indstillingen er angivet til **Nej**, i oversigtspanelet *Generelt*. Vælg derefter **Slet** i handlingsruden.

### <a name="header"></a>Overordnet

Angiv følgende felter i overskriften på et produkts parathedspolitik.

| Felt | Beskrivelse |
|---|---|
| Navn | Angiv et navn til politikken. |
| Beskrivelse | Angiv en beskrivelse af politikken. |

### <a name="general-fasttab"></a>Oversigtspanelet Generelt

Angiv følgende felter i oversigtspanelet **Generelt** på et produkts parathedspolitik.

| Felt | Beskrivelse |
|---|---|
| Produkttype | Vælg, om politikken gælder for produkter af typen *Vare* eller *Service*. Du kan ikke ændre denne indstilling, når du har gemt posten. |
| Aktive | Brug denne indstilling som en hjælp til at vedligeholde dine parathedspolitikker. Angiv *Ja* for alle de parathedspolitikker, du bruger. Angiv den til *Nej* for at markere en parathedspolitik som inaktiv, når den ikke bruges. Bemærk, at du ikke kan inaktivere en parathedspolitik, der er tildelt en teknisk produktkategori, og du kan kun slette inaktive frigivelsespolitikker. |

### <a name="readiness-control-fasttab"></a>Oversigtspanelet Parathedsstyring

For hver type parathedskontrol, du vil medtage i politikken, skal du tilføje en række i oversigtspanelet **Parathedsstyring**. Brug følgende knapper på værktøjslinjen i oversigtspanelet til at tilføje og fjerne rækker efter behov:

- **Tilføj kontrol** – Føj en standardparathedskontrol til politikken. Når du vælger denne knap, vises dialogboksen **Tilføj kontrol**. Her kan du vælge på en liste over tilgængelige kontroller.
- **Tilføj eksisterende spørgeskema** – Føj en tom række til gitteret. Du kan derefter tildele et eksisterende spørgeskema ved at angive felterne i følgende tabel.
- **Kopiér** – Tilføj en kopi af den valgte række i gitteret.
- **Slet** – Slet den valgte række fra gitteret.

For hver række, du tilføjer, skal du angive følgende felter.

| Felt | Beskrivelse |
| --- | --- |
| Procesområde | Vælg det område, som kontrollen er relateret til. |
| Type | Vælg, om kontrollen er en systemkontrol, en manuel kontrol eller en kontrolliste (spørgeskema). |
| Navn | Hvis kontrollen er en kontrolliste, skal du angive et navn. I forbindelse med systemkontrol og manuel kontrol angives dette felt automatisk. |
| Beskrivelse | Hvis kontrollen er en kontrolliste, skal du angive en beskrivelse. I forbindelse med systemkontrol og manuel kontrol angives dette felt automatisk, og beskrivelsen forklarer kontrollens fokus. |
| Anvend kontroller på | Vælg, om rækken skal generere parathedskontroller som svar på et nyt frigivet produkt, en frigivet variant eller en frigivet version. |
| Udfør i | Vælg, om parathedskontrollen, som rækken opretter, gælder for alle firmaer eller et enkelt firma. |
| Firma | Hvis du angiver feltet **Udfør i** til *Enkelt firma*, skal du vælge firmaet. |
| Ejertype | Vælg, om parathedskontroller, som rækken genererer, skal tildeles til en person eller et team. |
| Ejer | Vælg den person eller det team, som parathedskontrollerer den genererede række, skal tildeles. |
| Spørgeskema | Vælg det spørgeskema, der skal bruges til kontrollisten. Kontrollisten er en lokal kontrolliste i det firma, hvor parathedskontrollen udføres. Systemet skal kunne evaluere, om kontrollisten er besvaret korrekt. Derfor skal kontrollisten konfigureres, så der udføres en evaluering ud fra korrekte svar. Yderligere oplysninger om, hvordan du opretter spørgeskemaer, finder du i [Bruge spørgeskemaer](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/using-questionnaires) og relaterede emner. |
| Automatisk godkendelse | Poster til parathedskontrol omfatter et **Godkendt**-afkrydsningsfelt, der angiver godkendelsesstatus. Markér afkrydsningsfeltet **Automatisk godkendelse** for kontroller, der skal godkendes, umiddelbart efter at den tildelte bruger har afsluttet dem. Fjern markeringen i dette afkrydsningsfelt for at kræve udtrykkelig godkendelse som et ekstra trin. |
| Obligatorisk | Markér dette afkrydsningsfelt for de kontroller, der skal udføres af den tildelte bruger. Obligatoriske kontroller kan ikke springes over. |
