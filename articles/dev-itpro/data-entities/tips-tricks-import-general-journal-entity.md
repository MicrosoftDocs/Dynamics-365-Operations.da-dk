---
title: Bedste fremgangsmåder for import af bilag ved hjælp af enheden Finanskladde
description: Dette emne indeholder tip om import af data til finanskladden ved hjælp af enheden Finanskladde.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29cb4b940875b96cabaff540360674da528f8f39
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550978"
---
# <a name="best-practices-for-importing-vouchers-by-using-the-general-journal-entity"></a>Bedste fremgangsmåder for import af bilag ved hjælp af enheden Finanskladde

[!include [banner](../includes/banner.md)]

Dette emne indeholder tip om import af data til finanskladden ved hjælp af enheden Finanskladde.

Du kan bruge enheden Finanskladde til at importere bilag, der har kontotypen eller modkontotypen **Finans, Kunde, Kreditor eller Bank**. Bilaget kan angives som én linje, der bruger både feltet **Konto** og feltet **Modkonto**, eller som et flerlinjet bilag, hvor kun feltet **Konto** bruges (og **Modkonto** er tomt på hver linje). Enheden Finanskladde understøtter ikke alle kontotyper. I stedet findes andre enheder for scenarier, hvor der kræves forskellige kombinationer af kontotyper. Hvis du f.eks. vil importere en projekttransaktion, skal du bruge enheden Projektudgiftskladde. Hver enhed er udviklet til at understøtte specifikke scenarier, hvilket betyder, at flere felter kan være tilgængelige i enheder i disse scenarier, men ikke i enheder for et andet scenarie.

## <a name="setup"></a>Konfiguration
Før du importerer ved hjælp af enheden Finanskladde, skal du validere følgende opsætning:

- **Opsætning af nummerserien for kladdebatchnummeret** – Når du importerer ved hjælp af enheden Finanskladde, anvender kladdebatchnummeret som standard den nummerserie, der er defineret i de generelle finansparametre. Hvis du indstiller nummerserien for kladdebatchnummeret til **Manuel**, anvendes der ikke et standardnummer. Denne opsætning understøttes ikke.
- **Konfiguration af økonomiske dimensioner** – Hver organisation skal definere rækkefølgen af økonomiske dimensioner, når der bruges enheder til at importere posteringer. Rækkefølgen defineres for formatet **Integration af finansdimensioner** på **Finans** &gt; **Kontoplaner** &gt; **Dimensioner** &gt; **Konfiguration af økonomisk dimension til integrering af programmer** &gt; **Vælg dataenheder**. Segmenterne i finanskontoen, der importeres, skal have samme rækkefølge. I modsat fald opstår der en fejl under importen.

## <a name="general-journal-entity-setup"></a>Konfiguration af enheden Finanskladde
To indstillinger i Datastyring påvirker, hvordan standardkladdebatchnummer eller bilagsnummer anvendes:

- **Sætbaseret behandling** (på dataenheden)
- **Auto-genereret** (på felttilknytningen)

De følgende afsnit beskriver virkningen af disse indstillinger og forklarer også, hvordan kladdebatchnumre og bilagsnumre genereres.

### <a name="journal-batch-number"></a>Kladdebatchnummer

- Indstillingen **Angivet på basis af-behandling** på enheden Finanskladde påvirker ikke den måde, kladdebatchnumre genereres på.
- Hvis feltet **Kladdebatchnummer** er indstillet til **Auto-genereret**, oprettes der et nyt kladdebatchnummer for hver linje, der importeres. Denne funktionsmåde anbefales ikke. Indstillingen **Auto-genereret** findes i importprojektet under **Vis tilknytning** under fanen **Tilknytning af oplysninger**.
- Hvis feltet **Kladdebatchnummer** ikke er indstillet til **Auto-genereret**, oprettes kladdebatchnummeret på følgende måde:

    - Hvis det kladdebatchnummer, der er defineret i den importerede fil, svarer til en eksisterende, ikke-bogført kassekladde, importeres alle linjer, der har et tilsvarende kladdebatchnummer, til den eksisterende kladde. Linjerne importeres aldrig til et bogført kladdebatchnummer. I stedet oprettes et nyt nummer.
    - Hvis det kladdebatchnummer, der er defineret i den importerede fil, ikke svarer til en eksisterende, ikke-bogført kassekladde, grupperes alle linjer, der har det samme kladdebatchnummer, i en ny kladde. For eksempel importeres alle linjer, der har kladdebatchnummer 1, til en ny kladde, og alle linjer, der har kladdebatchnummer 2, importeres til en anden ny kladde. Kladdebatchnummeret oprettes ved hjælp af den nummerserie, der er defineret i finansparametrene.

### <a name="voucher-number"></a>Bilagsnummer

- Når du bruger indstillingen **Angivet på basis af-behandling** på enheden Finanskladde, skal bilagsnummeret gives i den importerede fil. Hver transaktion i finanskladden tildeles det bilagsnummer, der er angivet i den importerede fil, også selvom bilaget ikke er afstemt. Hvis du vil bruge sætbaseret behandling, men også vil bruge den nummerserie, der er defineret for bilagsnumre, er der et hotfix i frigivelsen fra februar 2016. Hotfix-nummer er 3170316 og kan hentes fra Lifecycle Services (LCS). Du kan finde flere oplysninger i [Download hotfixes fra Lifecycle Services](../migration-upgrade/download-hotfix-lcs.md).

    - Hvis du vil aktivere denne funktion, skal du på det kladdenavn, der bruges til import, indstille **Nummertildeling under bogføring** til **Ja**.
    - Et bilagsnummer skal stadig defineres i den importerede fil. Men dette nummer er midlertidigt og overskrives af bilagsnummeret, når kladden bogføres. Du skal sikre dig, at linjerne i kladden er grupperet korrekt efter midlertidigt bilagsnummer. Under bogføring findes der f.eks. tre linjer, der har det midlertidige bilagsnummer 1. Det midlertidige bilagsnummer for alle tre linjer overskrives med det næste nummer i nummerserien. Hvis disse tre linjer ikke er en afstemt indgang, bogføres bilaget ikke. Hvis linjer, der har det midlertidige bilagsnummer 2, overskrives dette nummer derefter med det næste bilagsnummer i nummerserien, og så videre.

- Når du ikke bruger indstillingen **Angivet på basis af-behandling**, behøver du ikke at angive et bilagsnummer i den importerede fil. Bilagsnumrene oprettes under importen baseret på opsætningen af kladdenavnet (**Kun ét bilagsnummer**, **Ved saldo** osv.). For eksempel, hvis kladdenavnet er defineret som **Ved saldo** i den første linje, modtages et nyt standardbilagsnummer. Systemet evaluerer derefter linjen for at afgøre, om debiteringer er lig med kreditterne. Hvis der findes en modkonto på linjen, modtager den næste linje, der importeres, et nyt bilagsnummer. Hvis der ikke findes en modkonto, evaluerer systemet, om debiteringer er lig med krediteringer, efterhånden som hver ny linje importeres.
- Hvis feltet **Bilagsnummer** er indstillet til **Auto-genereret**, vil importen ikke lykkes. Indstillingen **Auto-genereret** for feltet **Bilagsnummer** understøttes ikke.

Som standard bruger finanskladdeenheden sætbaseret behandling. Når du har evalueret forretningsbehovet for din organisation, kan du ændre indstillingen **Angivet på basis af-behandling** ved at klikke på **Dataenheder** i arbejdsområdet **Datastyring**. Sætbaseret behandling bruges til at gøre importprocessen hurtigere. Hvis du ikke bruger sætbaseret behandling, bliver import af finanskladdeenheden langsommere.
