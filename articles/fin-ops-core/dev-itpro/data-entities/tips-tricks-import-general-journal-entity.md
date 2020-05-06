---
title: Bedste fremgangsmåder for import af bilag ved hjælp af enheden Finanskladde
description: Dette emne indeholder tip om import af data til finanskladden ved hjælp af enheden Finanskladde.
author: rcarlson
manager: AnnBe
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13ea54a6fc4ccdfbcc917b533fe9896d57bcb347
ms.sourcegitcommit: f1bef1cb4b3d2c9261e89820d624e4b0fe60d25c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/22/2020
ms.locfileid: "3281480"
---
# <a name="best-practices-for-importing-vouchers-by-using-the-general-journal-entity"></a>Bedste fremgangsmåder for import af bilag ved hjælp af enheden Finanskladde

[!include [banner](../includes/banner.md)]

Dette emne indeholder tip om import af data til finanskladden ved hjælp af enheden Finanskladde.

Du kan bruge enheden Finanskladde til at importere bilag, der har kontotypen eller modkontotypen **Finans**, **Debitor**, **Kreditor** eller **Bank**. Bilaget kan angives som én linje, der bruger både feltet **Konto** og feltet **Modkonto**, eller som et flerlinjet bilag, hvor kun feltet **Konto** bruges (og **Modkonto** er tomt på hver linje). Enheden Finanskladde understøtter ikke alle kontotyper. I stedet findes andre enheder for scenarier, hvor der kræves forskellige kombinationer af kontotyper. Hvis du f.eks. vil importere en projekttransaktion, skal du bruge enheden Projektudgiftskladde. De enkelte enheder er udviklet til at understøtte specifikke scenarier. Det betyder, at yderligere felter kan være tilgængelige i enheder for de pågældende scenarier. Yderligere felter er dog muligvis ikke tilgængelige i enheder for forskellige scenarier.

## <a name="setup"></a>Konfiguration
Før du importerer ved hjælp af enheden Finanskladde, skal du validere følgende opsætning:

- **Opsætning af nummerserien for kladdebatchnummeret** – Når du importerer ved hjælp af enheden Finanskladde, anvender kladdebatchnummeret som standard den nummerserie, der er defineret i de generelle finansparametre. Hvis du indstiller nummerserien for kladdebatchnummeret til **Manuel**, anvendes der ikke et standardnummer. Denne opsætning understøttes ikke.
- **Konfiguration af økonomiske dimensioner** – Hver organisation skal definere rækkefølgen af økonomiske dimensioner, når der bruges enheder til at importere posteringer. Rækkefølgen defineres for formatet **Integration af finansdimensioner** på **Finans** &gt; **Kontoplaner** &gt; **Dimensioner** &gt; **Konfiguration af økonomisk dimension til integrering af programmer** &gt; **Vælg dataenheder**. Segmenterne i finanskontoen, der importeres, skal have samme rækkefølge. I modsat fald opstår der en fejl under importen.

## <a name="general-journal-entity-setup"></a>Konfiguration af enheden Finanskladde
To indstillinger i Datastyring påvirker, hvordan standardkladdebatchnummer eller bilagsnummer anvendes:

- **Sætbaseret behandling** (på dataenheden)
- **Auto-genereret** (på felttilknytningen)

I følgende afsnit beskrives virkningen af disse indstillinger. Det forklares også, hvordan systemet genererer batchnumre til kladder og bilagsnumre.

### <a name="journal-batch-number"></a>Kladdebatchnummer

- Indstillingen **Angivet på basis af-behandling** på enheden Finanskladde påvirker ikke den måde, kladdebatchnumre genereres på.
- Hvis feltet **Kladdebatchnummer** er indstillet til **Auto-genereret**, oprettes der et nyt kladdebatchnummer for hver linje, der importeres. Denne funktionsmåde anbefales ikke. Indstillingen **Auto-genereret** findes i importprojektet under **Vis tilknytning** under fanen **Tilknytning af oplysninger**.
- Hvis feltet **Kladdebatchnummer** ikke er indstillet til **Auto-genereret**, oprettes kladdebatchnummeret på følgende måde:

    - Hvis det kladdebatchnummer, der er defineret i den importerede fil, svarer til en eksisterende, ikke-bogført kassekladde, importeres alle linjer, der har et tilsvarende kladdebatchnummer, til den eksisterende kladde. Linjerne importeres aldrig til et bogført kladdebatchnummer. I stedet oprettes et nyt nummer.
    - Hvis det kladdebatchnummer, der er defineret i den importerede fil, ikke svarer til en eksisterende, ikke-bogført kassekladde, grupperes alle linjer, der har det samme kladdebatchnummer, i en ny kladde. For eksempel importeres alle linjer, der har kladdebatchnummer 1, til en ny kladde, og alle linjer, der har kladdebatchnummer 2, importeres til en anden ny kladde. Kladdebatchnummeret oprettes ved hjælp af den nummerserie, der er defineret i finansparametrene.

### <a name="voucher-number"></a>Bilagsnummer

- Når du bruger indstillingen **Angivet på basis af-behandling** på enheden Finanskladde, skal bilagsnummeret gives i den importerede fil. Hver transaktion i finanskladden tildeles det bilagsnummer, der er angivet i den importerede fil, også selvom bilaget ikke er afstemt. Bemærk følgende punkter, hvis du vil bruge sætbaseret behandling, men også vil bruge den nummerserie, der er defineret for bilagsnumre.

    - Hvis du vil aktivere denne funktion, skal du på det kladdenavn, der bruges til import, indstille **Nummertildeling under bogføring** til **Ja**.
    - Et bilagsnummer skal stadig defineres i den importerede fil. Men dette nummer er midlertidigt og overskrives af bilagsnummeret, når kladden bogføres. Sørg for, at linjerne i kladden er grupperet korrekt efter midlertidigt bilagsnummer. Under bogføring findes der f.eks. tre linjer, der har det midlertidige bilagsnummer 1. Det midlertidige bilagsnummer for alle tre linjer overskrives med det næste nummer i nummerserien. Hvis disse tre linjer ikke er en afstemt indgang, bogføres bilaget ikke. Hvis linjer har det midlertidige bilagsnummer 2, overskrives dette nummer derefter med det næste bilagsnummer i nummerserien, og så videre.

- Når du ikke bruger indstillingen **Angivet på basis af-behandling**, behøver du ikke at angive et bilagsnummer i den importerede fil. Bilagsnumrene oprettes under importen baseret på opsætningen af kladdenavnet (**Kun ét bilagsnummer**, **Ved saldo** osv.). For eksempel, hvis kladdenavnet er defineret som **Ved saldo** i den første linje, modtages et nyt standardbilagsnummer. Systemet evaluerer derefter linjen for at afgøre, om debiteringer er lig med kreditterne. Hvis der findes en modkonto på linjen, modtager den næste linje, der importeres, et nyt bilagsnummer. Hvis der ikke findes en modkonto, evaluerer systemet, om debiteringer er lig med krediteringer, efterhånden som hver ny linje importeres.
- Hvis feltet **Bilagsnummer** er indstillet til **Auto-genereret**, vil importen ikke lykkes. Indstillingen **Auto-genereret** for feltet **Bilagsnummer** understøttes ikke.

Som standard bruger finanskladdeenheden sætbaseret behandling. Når du har evalueret forretningsbehovet for din organisation, kan du ændre indstillingen **Angivet på basis af-behandling** ved at klikke på **Dataenheder** i arbejdsområdet **Datastyring**. Sætbaseret behandling bruges til at gøre importprocessen hurtigere. Hvis du ikke bruger sætbaseret behandling, bliver import af finanskladdeenheden langsommere.
