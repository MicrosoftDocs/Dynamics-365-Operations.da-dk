---
title: Komprimere store dokumenter, der er genereret i elektronisk rapportering
description: Denne artikel forklarer, hvordan du komprimerer store dokumenter, der genereres af et elektronisk rapporteringsformat (ER).
author: NickSelin
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERFormatDestinationTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 9a4995879717e715f8ebadb6a80e00949df7545c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864801"
---
# <a name="compress-large-documents-that-are-generated-in-electronic-reporting"></a>Komprimere store dokumenter, der er genereret i elektronisk rapportering 

[!include [banner](../includes/banner.md)]

Du kan bruge [strukturen for elektronisk rapportering (ER)](general-electronic-reporting.md) til at konfigurere en løsning, der henter transaktionsdata for at oprette et udgående dokument. Dette oprettede dokument kan være temmelig stort. Når denne dokumenttype oprettes, bruges hukommelsen fra [Microsoft Dynamics AX Application Object Server (AOS)](../dev-tools/access-instances.md#location-of-packages-source-code-and-other-aos-configurations) til at opbevare den. På et tidspunkt skal dokumentet downloades fra dit Microsoft Dynamics 365 Finance-program. I øjeblikket er maksimumstørrelsen på et enkelt dokument, der er oprettet i ER, begrænset til 2 gigabyte (GB). Finance sætter i øjeblikket en [begrænsning](https://fix.lcs.dynamics.com/Issue/Details?kb=4569432&bugId=453907&dbType=3) på størrelsen af en downloadet fil til 1 GB. Derfor skal du konfigurere en ER-løsning, der reducerer sandsynligheden for, at disse begrænsninger overskrides, og at du modtager en af undtagelserne **Streamen er for lang** eller **Overløb eller underløb i den aritmetiske handling**.

Når du konfigurerer en løsning, kan du justere dit ER-format i Operationsdesigner ved at tilføje et rodelement af typen **Mappe** for at komprimere det indhold, der oprettes af de indlejrede elementer. Komprimering fungerer via "JIT (just in time)", så det maksimale hukommelsesforbrug og størrelsen på den fil, der skal downloades, kan reduceres.

> [!NOTE]
> Filkomprimering tager ekstra procent af CPU-brugen.

Hvis du vil vide mere om denne tilgang, skal du fuldføre eksemplet i denne artikel.

## <a name="example-compress-an-outbound-document"></a>Eksempel: Komprimer et udgående dokument

I dette eksempel vises, hvordan en bruger, der er tildelt rollen **Systemadministrator** eller **Funktionel konsulent i elektronisk rapportering**, kan konfigurere et ER-format til at komprimere et oprettet dokument.

### <a name="prerequisites"></a>Forudsætninger

Du skal fuldføre følgende trin, før du kan fuldføre procedurerne i denne artikel.

1. [Aktivér en konfigurationsudbyder](er-defer-xml-element.md#activate-a-configuration-provider).
2. [Importere ER-eksempelkonfigurationerne](er-defer-xml-element.md#import-the-sample-er-configurations).
3. [Gennemse det importerede format](er-defer-xml-element.md#review-the-imported-format).

> [!NOTE]
> Formatstrukturen starter i øjeblikket fra elementet **Rapport** for typen **Fil** og indeholder XML-elementer. Derfor oprettes der et udgående dokument i XML-format, og der bruges ingen komprimering.

### <a name="generate-an-er-format-to-get-an-uncompressed-document"></a>Oprette et ER-format for at hente et ukomprimeret dokument

1. [Køre det importerede format](er-defer-xml-element.md#run-the-imported-format).
2. Bemærk, at størrelsen på det oprettede dokument i XML-format er 3 kilobyte (KB).

    ![Forhåndsvisning af det ukomprimerede udgående dokument.](./media/er-compress-outbound-files1.png)

### <a name="modify-the-format-to-compress-the-generated-output"></a>Redigere formatet for at komprimere det oprettede output

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet udvide **Model til at lære udskudte elementer**.
3. Vælg konfigurationen **Format til at lære afledte XML-elementer**.
4. Vælg **Designer** for at redigere formatstrukturen.
5. På siden **Formatdesigner** under fanen **Format** skal du vælge **Tilføj rod** for at tilføje et rodformatelement.
6. I dialogboksen **Tilføj** skal du vælge **"Common\\Folder**.
7. Vælg **OK** for at bekræfte tilføjelsen af det nye rodelement.
8. Vælg **Gem**.

> [!NOTE]
> Formatstrukturen starter fra elementet af type **Mappe**. Dette element opretter outputtet som en komprimeret (zip) fil. Når et dokument, der oprettes af elementet **Rapport**, placeres i en udgående zip-fil, komprimeres indholdet for at reducere størrelsen på den udgående fil.

### <a name="generate-an-er-format-to-get-a-compressed-document"></a>Oprette et ER-format for at hente et komprimeret dokument

1. På siden **Formatdesigner** skal du vælge **Kør**.
2. Download den zip-fil, som webbrowseren tilbyder, og åbn den til gennemsyn.
3. Bemærk, at størrelsen på det oprettede dokument i ZIP-format er 1 KB.

    > [!NOTE] 
    > Komprimeringsforholdet for den XML-fil, som denne zip-fil indeholder, er 87 %. Komprimeringsforholdet afhænger af de data, der komprimeres.

    ![Forhåndsvisning af det komprimerede udgående dokument.](./media/er-compress-outbound-files2.png)

> [!NOTE]
> Hvis ER-[destinationen](electronic-reporting-destinations.md) er konfigureret for det formatelement, der opretter outputtet (elementet **Rapport** i dette eksempel), springes komprimeringen over.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Destinationer for elektronisk rapportering (ER)](electronic-reporting-destinations.md)

[Udskyde udførelse af XML-elementer i ER-formater](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]