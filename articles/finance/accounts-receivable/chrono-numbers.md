---
title: Nummerering af dokumenter og bilag kronologisk
description: Dette emne indeholder en forklaring på, hvordan du kan konfigurere og bruge kronologiske numre til relevante dokumenter og relaterede bilag.
author: ikond
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 31745632de7339d167ac9f18f02e6611e1a78b28
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104362"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a>Nummerering af dokumenter og bilag kronologisk

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

I nogle lande er der et juridisk krav om at nummerere dokumenter og relaterede bilag i kronologisk rækkefølge. Kronologien skal understøttes af perioder. Alle de tal, der tilhører tidligere perioder, skal være mindre end de tal, der tilhører senere perioder. For at opfylde dette krav er der implementeret kronologisk nummereringsfunktionalitet. Dette emne indeholder en forklaring på, hvordan du kan konfigurere og bruge kronologiske numre til relevante dokumenter og relaterede bilag.

## <a name="prerequisites"></a>Forudsætninger

I arbejdsområdet Funktionsstyring skal du aktivere funktionen **kronologisk nummerering**. Få flere oplysninger i [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-chronological-numbering"></a>Konfigurere kronologisk nummerering

Kronologisk nummerering påvirker følgende dokumenter.

**Debitor**
- Debitorfaktura
- Debitorfakturabilag
- Salgskreditnota
- Salgskreditnotabilag
- Fritekstfaktura
- Fritekstfakturabilag
- Fritekstkreditnota
- Fritekstkreditnotabilag
- Følgeseddel
- Følgeseddelsbilag
- Rettelsesbilag for følgeseddel
- Rentenotabilag
- Rykkerbilag

**Kreditor**
- Fakturabilag
- Kreditnotabilag
- Produktkvitteringsbilag

**Projektstyring**
- Fakturaer
- Fakturabilag
- Kreditnota
- Kreditnotabilag 

### <a name="define-number-sequences"></a>Definere nummerserier

Du kan definere nummerserier ved at gå til **Organisationsadministration** > **Nummerserier** > **Nummerserier**. Du kan definere lige så mange nummerserier, der kræves for at dække de påvirkede perioder for påkrævede dokumenter. 

Angiv et firma for hver nummerserie. Segmenter i nummerserierne skal defineres, så de giver kronologisk rækkefølge for perioder. Segmentnavnene kan f.eks. indeholde et særligt præfiks, der identificerer en bestemt periode.

![Konfiguration af nummerserie](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a>Konfigurere nummerseriegrupper

Hvis du vil konfigurere nummerseriegrupper, skal du gå til **Debitor** > **Konfiguration** > **Debitorparametre**. Under fanen **Nummerserier** skal du definere lige så mange nummerseriegrupper, der er behov for, for at dække de berørte perioder. 

For hver gruppe skal du vælge en af de understøttede dokumentreferencer i afsnittet **Reference**, og i feltet **Nummerseriekode** skal du referere til en nummerserie, der tidligere er oprettet for den relaterede periode.

![Konfiguration af nummerseriegruppe](media/chrono-num-sequence-group.jpg)

Konfigurer også nummerseriegrupper i modulerne **Kreditor** og **Projektstyring og regnskab**.

### <a name="configure-number-sequence-groups-chronology"></a>Konfigurere nummerseriegrupper kronologisk

Hvis du vil konfigurere nummerseriegruppers kronologi, skal du gå til **Organisationsadministration** > **Nummerserier** > **Kronologisk nummerseriegrupper**. Definer anvendelighedsbetingelserne for nummerseriegrupper.

![Kronologisk nummeropsætning](media/chrono-num-sequence-group-period.jpg)

| Felt            | Betegnelse                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gyldig fra  | Startdatoen for anvendelse af nummerseriegrupper. |
| Udløb      | Slutdatoen for anvendelse af nummerseriegrupper. Hvis der ikke anvendes en slutdato, skal du vælge **Aldrig**. |
| Nummerseriegruppe | Nummerseriegruppe, der skal bruges til generering af dokumentnumre i perioden. |
| Oprindelig nummerseriegruppe | Denne nummerseriegruppekode bruges til yderligere filtrering af sager, hvis dokumenter allerede har fået tildelt en bestemt *permanent* nummerseriegruppe. En tom værdi betragtes som en bestemt værdi. Hvis du vil ignorere en foreløbig tildelt gruppe, skal du bruge indstillingen **Standard** til denne opsætning. |
| Standard | Hvis den er aktiveret, ignorerer systemet den foreløbige tildelte dokumentnummerseriegruppe og bruger kun start- og slutdatoerne for perioderne til analyse af anvendelighed. Hvis de er deaktiveret, bruges den fulde kombination af **Gyldig fra** + **Udløb** + **Oprindelig nummerseriegruppe** til valg. |

## <a name="document-posting"></a>Bogføringsdokument
Når du bogfører et dokument, tildeles dokumentet den relevante nummerseriegruppe på grundlag af dokumentets bogføringsdato og bruges derefter til at generere et dokumentnummer baseret på den registrerede nummerserie. Systemet indeholder en meddelelse om tildeling af nummerseriegrupper.

![Dokumentnummer](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> I nogle lande er der allerede implementeret en bestemt logik til dokumentnummerering. I dette tilfælde tilsidesætter landespecifik logikfunktionen **Kronologisk nummerering**.
