---
title: Designe ER-konfigurationer til at udelade tegn for byterækkefølgemærke i genererede filer
description: I dette emne forklares det, hvordan du kan konfigurere et ER-format (elektronisk rapportering), så der genereres rapporter, hvor tegn for byterækkefølgemærke udelades.
author: NickSelin
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19fbbdea4bfdf30b1313a47e65056b536ed73dbe
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060813"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a>Designe ER-konfigurationer til at udelade tegn for byterækkefølgemærke i genererede filer

[!include [banner](../includes/banner.md)]

Du kan designe [elektronisk rapportering (ER)](general-electronic-reporting.md) som [løsning](er-quick-start1-new-solution.md) for at oprette udgående dokumenter. Hvis du vil generere dokumenterne som tekst- eller XML-filer, skal løsningen indeholde en ER-[konfiguration](general-electronic-reporting.md#Configuration), der indeholder en ER-[formatkomponent](general-electronic-reporting.md#FormatComponentOutbound). Hvis du vil angive den [tegnkodning](https://docs.microsoft.com/windows/win32/intl/character-sets), der repræsenterer sættet af tegn i genererede filer, skal ER-formatet indeholde formatelementet **Common\\File**. Hvis du vil konfigurere ER-formatkomponenten, skal du åbne [kladde](general-electronic-reporting.md#component-versioning)-versionen af ER-konfigurationen i ER-formatdesigneren og tilføje elementet **Common\\File**. I feltet **Kodning** skal du angive kodningen af udgående filer, der genereres under kørsel ved hjælp af denne komponent.

> [!NOTE]
> Hvis formatet indeholder et forkert kodningsnavn, vises der en fejl, når du gemmer ændringerne i indstillingerne af formatet.

![Tilføje et rodelement på siden Formatdesigner](./media/er-suppress-bom-characters-image1.gif)

Hvis du angiver **UTF-8**, **UTF-16** eller **UTF-32** som kodning, bliver indstillingen **Undertryk BOM-tegn** tilgængelig. Angiv denne indstilling til **Ja** for at udelade [byterækkefølgemærketegn (BOM)](https://docs.microsoft.com/globalization/encoding/byte-order-mark) i udgående filer, der genereres under kørslen, når det redigerbare ER-format køres.

> [!NOTE]
> Hvis du ikke udfylder feltet **Kodning**, bruges standardkodningen **UTF-8**.

![Angive indstillingen Undertryk BOM-tegn på siden Formatdesigner](./media/er-suppress-bom-characters-image2.gif)

Hvis du vil gennemse funktionaliteten under kørslen, skal du gennemføre den relevante procedure. Udfør f.eks. trinnene i emnet [Udskyde udførelse af XML-elementer i ER-formater](er-defer-xml-element.md). Når du har fuldført trinnene i sektionen [Rediger formatet, så beregningen er baseret på genereret output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) i dette emne, skal du følge disse ekstra trin.

1. Angiv UTF-kodningen:

    1. Vælg **Rapport**-elementet af typen **Common\\File**.
    2. Angiv **UTF-8**-kodningen i **Kodning**-feltet.

2. Opret en XML-fil, der indeholder et BOM-tegn:

    1. Angiv indstillingen **Undertryk BOM-tegn** til **Nej** for at medtage BOM-tegn i genererede XML-filer.
    2. Udfør trinnene i sektionen [Udskyde udførelsen af oversigts-XML-elementet, så den beregnede total bruges](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) af emnet [Udskyde udførelse af XML-elementer i ER-formater](er-defer-xml-element.md), og gem den genererede fil som **SampleXmlReport.xml**.

3. Opret en XML-fil, der ikke indeholder et BOM-tegn:

    1. Angiv indstillingen **Undertryk BOM-tegn** til **Ja** for at udelade BOM-tegn i genererede XML-filer.
    2. Udfør trinnene i sektionen [Udskyde udførelsen af oversigts-XML-elementet, så den beregnede total bruges](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) af emnet [Udskyde udførelse af XML-elementer i ER-formater](er-defer-xml-element.md), og gem den genererede fil som **SampleXmlReport (1).xml**.

4. Sammenlign de genererede filer i et filsammenligningsværktøj.

    Den første forskel, du bemærker, er i filhovedet. Filen SampleXmlReport.xml indeholder et BOM-tegn, mens filen SampleXmlReport (1).xml ikke gør.

    ![Sammenligning af genererede filer med et filsammenligningsværktøj](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a>Se også

- [Udskyde udførelse af XML-elementer i ER-formater](er-defer-xml-element.md)
