---
title: Funktion til opdeling af faktura
description: Dette emne beskriver, hvordan du opsætter og bruger funktionen til opdeling af fakturaer efter leveringsadresse og skattekontonummer (TAN – Tax Account Number).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: f9bb4db14cbb7c9abb33ccee532ed73b378317bb
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2022
ms.locfileid: "8408349"
---
# <a name="split-invoice-functionality"></a>Funktion til opdeling af faktura

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du opsætter og bruger funktionen til opdeling af fakturaer efter leveringsadresse og skattekontonummer (TAN – Tax Account Number).

På siden **Kreditorparametre** under fanen **Generelt** skal du markere afkrydsningsfeltet **Produktkvittering** eller **Faktura** for at bogføre og opdele en produktkvittering eller faktura, der har forskellige leveringsadresser og skattekontonumre på siden **Indkøbsordre**. Den bogførte faktura opdeles derefter efter leveringsadresse og skattekontonummer.

På fanen **Samleopdatering** op oversigtspanelet **Deling basering på** i rækken **Leveringsoplysninger** skal du angive indstillingen **Bekræftelse**, **Plukliste**, **Følgeseddel** eller **Faktura** til **Ja** for at bogføre og opdele en bekræftelse, plukliste, følgeseddel eller faktura, når der er defineret forskellige leveringsadresser og skattekontonumre for forskellige fakturalinjer på siden **Salgsordre**. Fakturaen opdeles først efter leveringsadresse og dernæst efter skattekontonummer.

> [!IMPORTANT]
> - Hvis ingen indstillinger for **Leveringsoplysninger** er angivet til **Ja**, bogføres fakturaen som en enkelt faktura. Der foretages ingen opdeling af fakturaen.
> - Hvis du vil opdele og bogføre en følgeseddel, hvor fakturalinjerne har forskellige leveringsadresser og skattekontonumre, skal du angive indstillingen **Følgeseddel** for **Leveringsoplysninger** til **Ja**.
> - Hvis du vil opdele og bogføre en faktura, hvor fakturalinjerne har forskellige leveringsadresser og skattekontonumre, skal du angive indstillingen **Faktura** for **Leveringsoplysninger** til **Ja**.
> - Hvis du vil bogføre en faktura, hvor fakturalinjerne har forskellige leveringsadresser men samme skattekontonummer, skal du angive indstillingen **Faktura** for **Leveringsoplysninger** til **Nej**. Fakturaen opdeles efter leveringsadresse.

## <a name="example"></a>Eksempel

I dette eksempel er indstillingen **Faktura** for **Leveringsoplysninger** angivet til **Ja** under fanen **Samleopdatering** på siden **Kreditorparametre**. Der bogføres en indkøbsfaktura med følgende opsætning for leveringsadresser og skattekontonumre på linjerne:

- **Varelinje 1:** Leveringsadresse 1, skattekontonummer-ABCD12345A
- **Varelinje 2:** Leveringsadresse 1, skattekontonummer-ABCD12345A
- **Varelinje 3:** Leveringsadresse 2, skattekontonummer-ABCE12345B
- **Varelinje 4:** Leveringsadresse 3, skattekontonummer-ABCD12345A

I dette tilfælde opdeles den oprindelige faktura i to fakturaer og bogføres på følgende måde:

- Faktura 1 bogføres for varelinje 1 og varelinje 2, fordi de to linjer har samme leveringsadresse og skattekontonummer.
- Faktura 2 bogføres for varelinje 3.
- Faktura 3 bogføres for varelinje 4.
