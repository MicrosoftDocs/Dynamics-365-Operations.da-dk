---
title: "Bedste fremgangsmåder til import af bilag ved hjælp af objektet finanskladde"
description: "Dette emne indeholder tip til import af data til finanskladden ved hjælp af generelt kladde enhed."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 81a52acd1d9baa12fcfe9d848441901894fa5682
ms.lasthandoff: 03/31/2017


---

# <a name="best-practices-for-importing-vouchers-using-the-general-journal-entity"></a>Bedste fremgangsmåder til import af bilag ved hjælp af objektet finanskladde

Dette emne indeholder tip til import af data til finanskladden ved hjælp af generelt kladde enhed.  

Du kan bruge objektet finanskladden til at importere bilag, der har kontotypen konto eller forskydning af **Finans, debitor, kreditor eller banken**. Bilaget kan angives som én linje, der bruger begge **konto** felt og **modkonto** -felt, eller som en flerlinjet bilag, hvor der kun de **konto** bruges (og **modkonto** er tom på hver linje). Den finanskladde enhed understøtter ikke hver kontotype. I stedet findes andre enheder for scenarier, hvor der kræves forskellige kombinationer af kontotyper. Hvis du vil importere en projekttransaktion, f.eks. projekt udgift journal-enhed. Hver enhed er udviklet til at understøtte specifikke scenarier, hvilket betyder, at flere felter kan være tilgængelige i enheder i disse situationer, men ikke i enheder for et andet scenarie.

## <a name="setup"></a>Konfiguration
Før du importerer ved hjælp af objektet i finanskladden, validere følgende opsætning:

-   **Opsætningen af nummerserien for kladdebatchnummer** - som standard, når du importerer ved hjælp af finanskladden enhed, kladden batch nummer anvendes den nummerserie, der er defineret i de generelle økonomiparametre. Hvis du indstiller nummerserien for kladdebatchnummeret til **Manuel**, anvendes der ikke et standardnummer. Denne opsætning understøttes ikke.
-   **Konfiguration af økonomiske dimensioner** -alle virksomheder skal definere rækkefølgen af økonomiske dimensioner, når enheder bruges til at importere posteringer. Rækkefølgen, der er defineret for den **Finans dimensioner integration** format, på **Finans**&gt;**kontoplanen**&gt;**dimensioner**&gt;**konfiguration af økonomisk dimension for at integrere programmer**&gt;**vælge data-enheder**. Segmenterne i finanskontoen, der importeres, skal have samme rækkefølge. I modsat fald opstår der en fejl under importen.

## <a name="general-journal-entity-setup"></a>Konfiguration af enheden Finanskladde
To indstillinger i administration af Data påvirker, hvordan standard kladdebatchnummer eller bilagsnummer anvendes:

-   **Sæt-baseret behandling** (på dataenhed)
-   **Auto-genereret** (på felttilknytningen)

De følgende afsnit beskriver virkningen af disse indstillinger og forklarer også, hvordan kladdebatchnumre og bilagsnumre genereres.

### <a name="journal-batch-number"></a>Kladdebatchnummer

-   Indstillingen **Angivet på basis af-behandling** på enheden Finanskladde påvirker ikke den måde, kladdebatchnumre genereres på.
-   Hvis feltet **Kladdebatchnummer** er indstillet til **Auto-genereret**, oprettes der et nyt kladdebatchnummer for hver linje, der importeres. Denne funktionsmåde anbefales ikke. Indstillingen **Auto-genereret** findes i importprojektet under **Vis tilknytning**under fanen **Tilknytning af oplysninger**.
-   Hvis feltet **Kladdebatchnummer** ikke er indstillet til **Auto-genereret**, oprettes kladdebatchnummeret på følgende måde:
    -   Hvis det kladdebatchnummer, der er defineret i den importerede fil svarer til en eksisterende, ikke-bogførte kassekladden i Microsoft Dynamics 365 for operationer, importeres alle linjer, der har en tilsvarende kladdebatchnummer til eksisterende kladde. Linjerne importeres aldrig til et bogført kladdebatchnummer. I stedet oprettes et nyt nummer.
    -   Hvis det kladdebatchnummer, der er defineret i den importerede fil svarer ikke til en eksisterende, ikke-bogførte kassekladden i Dynamics 365 for operationer, grupperes alle linjer, der har det samme kladdebatchnummer under en ny kladde. For eksempel importeres alle linjer, der har kladdebatchnummer 1, til en ny kladde, og alle linjer, der har kladdebatchnummer 2, importeres til en anden ny kladde. Kladdebatchnummeret oprettes ved hjælp af den nummerserie, der er defineret i finansparametrene.

### <a name="voucher-number"></a>Bilagsnummer

-   Når du bruger indstillingen **Angivet på basis af-behandling** på enheden Finanskladde, skal bilagsnummeret gives i den importerede fil. Hver transaktion i finanskladden tildeles det bilagsnummer, der er angivet i den importerede fil, også selvom bilaget ikke er afstemt. Hvis du vil bruge set-baseret behandling, men du også vil bruge den nummerserie, der er defineret for bilagsnumre i Dynamics 365 for operationer, der er oprettet et hotfix til februar 2016-versionen. Hotfix-nummer er 3170316 og kan hentes fra Lifecycle Services (LCS). Du kan finde flere oplysninger i [Download hotfixes fra Lifecycle Services](..\migration-upgrade\download-hotfix-lcs.md).
    -   For at aktivere denne funktion på det kladdenavn, der bruges til import i Dynamics 365 for operationer, angive **nummer tildeling, når du bogfører** til **Ja**.
    -   Et bilagsnummer skal stadig defineres i den importerede fil. Men dette nummer er midlertidige og overskrives af Dynamics-365 for operationer bilagsnummer, når kladden bogføres. Du skal sikre dig, at linjerne i kladden er grupperet korrekt efter midlertidigt bilagsnummer. For eksempel under bogføring findes tre linjer, der har en midlertidig bilagsnummeret for 1. Midlertidig bilagsnummeret for alle tre linjer er overskrevet med det næste nummer i nummerserien. Hvis disse tre linjer ikke er en afstemt indgang, bogføres bilaget ikke. Hvis linjer, der har det midlertidige bilagsnummer 2, overskrives dette nummer derefter med det næste bilagsnummer i nummerserien, og så videre.

<!-- -->

-   Når du ikke bruger den **sæt-baseret behandling** indstilling, behøver du ikke at angive et bilagsnummer i den importerede fil. Bilagsnumrene oprettes under importen baseret på opsætningen af kladdenavnet (**Kun ét bilagsnummer**, **Ved saldo** osv.). For eksempel, hvis kladdenavnet er defineret som **Ved saldo** i den første linje, modtages et nyt standardbilagsnummer. Systemet evaluerer derefter linjen for at afgøre, om debiteringer er lig med kreditterne. Hvis der findes en modkonto på linjen, modtager den næste linje, der importeres, et nyt bilagsnummer. Hvis der ikke findes en modkonto, evaluerer systemet, om debiteringer er lig med krediteringer, efterhånden som hver ny linje importeres.
-   Hvis feltet **Bilagsnummer** er indstillet til **Auto-genereret**, vil importen ikke lykkes. Indstillingen **Auto-genereret** for feltet **Bilagsnummer** understøttes ikke.

Som standard bruger finanskladdeenheden sætbaseret behandling. Når du har evalueret forretningsbehovet for din organisation, kan du ændre indstillingen **Angivet på basis af-behandling** ved at klikke på **Dataenheder** i arbejdsområdet **Datastyring**. Sætbaseret behandling bruges til at gøre importprocessen hurtigere. Hvis du ikke bruger sætbaseret behandling, bliver import af finanskladdeenheden langsommere.


