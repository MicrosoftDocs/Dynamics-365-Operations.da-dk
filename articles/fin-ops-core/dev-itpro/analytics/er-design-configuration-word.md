---
title: Designe en ny ER-konfigurationer til generering af rapporter i Word-format
description: Dette emne forklarer, hvordan brugere kan konfigurere et nyt ER-format (elektronisk rapportering) for at oprette rapporter som Microsoft Word-dokumenter.
author: NickSelin
ms.date: 12/17/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 98d28c39b2923afecc851299a07aa3b93ef2edce
ms.sourcegitcommit: ac23a0a1f0cc16409aab629fba97dac281cdfafb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/29/2021
ms.locfileid: "7867288"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a>Designe en ny ER-konfigurationer til generering af rapporter i Word-format

[!include [banner](../includes/banner.md)]

Hvis du vil oprette rapporter som Microsoft Word-dokumenter, skal du designe en skabelon til rapporterne ved f.eks. at bruge Word-skrivebordsprogrammet. I følgende illustration vises eksempelskabelonen til kontrolrapporten, der kan genereres for at vise oplysninger om behandlede kreditorbetalinger.

![Eksempelskabelon til kontrolrapporten i Word-skrivebordsapplikationen.](./media/er-design-configuration-word-image1.png)

Hvis du vil bruge et Word-dokument som skabelon til rapporter i Word-format, kan du konfigurere en ny [Elektronisk rapportering (ER)](general-electronic-reporting.md) som [løsning](er-quick-start1-new-solution.md). Denne løsning skal omfatte en ER-[konfiguration](general-electronic-reporting.md#Configuration), der indeholder en ER-[formatkomponent](general-electronic-reporting.md#FormatComponentOutbound).

> [!NOTE]
> Når du opretter en konfiguration af et nyt ER-format til generering af rapporter i Word-format, skal du enten vælge **Word** som formattype på rullelisten **Opret konfiguration** eller lade feltet **Formattype** være tomt.

![Oprettelse af en formatkonfiguration på siden Konfigurationer.](./media/er-design-configuration-word-image2.gif)

Løsningens ER-formatkomponent skal indeholde formatelementet **Excel\\Fil**, og det pågældende formatelement skal knyttes til Word-dokumentet, der skal bruges som skabelon for genererede rapporter under kørslen. Hvis du vil konfigurere ER-formatkomponenten, skal du åbne [kladde](general-electronic-reporting.md#component-versioning)-versionen af den oprettede ER-konfiguration i ER-formatdesigneren. Tilføj derefter elementet **Excel\\Fil**, knyt Word-skabelonen til det ER-format, der kan redigeres, og knyt skabelonen til det **Excel\\File**-element, du har tilføjet.

> [!NOTE]
> Når du manuelt tilknytter en skabelon, skal du bruge en [dokumenttype](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types), der er [konfigureret](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) i ER-parametrene til lagring af skabeloner i ER-formater.

![Tilknytte en skabelon på siden Formatdesigner.](./media/er-design-configuration-word-image3.gif)

Du kan tilføje indlejrede elementer **Excel\\Område** og **Excel\\Celle** elementet **Excel\\Fil** for at angive strukturen for data, der skal indtastes i genererede rapporter under kørslen. Du skal derefter knytte disse elementer til datakilder i det redigerbare ER-format for at angive de faktiske data, der skal indtastes i genererede rapporter under kørslen.

![Tilføjelse af indlejrede element på siden Formatdesigner.](./media/er-design-configuration-word-image4.gif)

Når du gemmer ændringerne i ER-formatet på designtidspunktet, gemmes den hierarkiske formatstruktur i den tilknyttede Word-skabelon som en [brugerdefineret XML-del](/visualstudio/vsto/custom-xml-parts-overview) med navnet **Rapport**. Du skal åbne den ændrede skabelon, hente den fra Finans, gemme den lokalt og åbne den i Word-skrivebordsapplikationen. I følgende illustration vises den lokalt gemte eksempelskabelon til kontrolrapporten, der indeholder den brugerdefinerede XML-del **Rapport**.

![Visning af eksempelrapportskabelon i Word-skrivebordsapplikationen.](./media/er-design-configuration-word-image5.gif)

Når bindinger af formatelementerne **Excel\\Område** og **Excel\\Celle** køres, kommer de data, som hver binding leverer, ind i det genererede Word-dokument som et individuelt felt i den brugerdefinerede XML-del **Rapport**. Hvis du vil angive værdierne fra felterne i den brugerdefinerede XML-del i et genereret dokument, skal du føje de relevante Word-[indholdskontrolelementer](/office/client-developer/word/content-controls-in-word) til Word-skabelonen, så de fungerer som pladsholdere for data, der udfyldes under kørslen. Hvis du vil angive, hvordan indholdskontrolelementer skal udfyldes, skal du knytte alle indholdskontroller til det relevante felt i den brugerdefinerede XML-del **Rapport**.

![Tilføjelse og tilknytning af indholdskontrolelementer i Word-skrivebordsapplikationen.](./media/er-design-configuration-word-image6.gif)

Du skal derefter erstatte den oprindelige Word-skabelon i det redigerbare ER-format med den redigerede skabelon, der nu indeholder Word-indholdskontrolelementer, som er knyttet til felterne i den brugerdefinerede XML-del **Rapport**.

![Erstatning af skabelonen på siden Formatdesigner.](./media/er-design-configuration-word-image7.gif)

Når du kører det konfigurerede ER-format, bruges den vedhæftede Word-skabelon til at generere en ny rapport. De faktiske data gemmes i Word-rapporten som en brugerdefineret XML-del, der kaldes **Rapport**. Når den genererede rapport åbnes, udfyldes Word-indholdet med data fra den brugerdefinerede XML-del **Rapport**.

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

**Spørgsmål:** Jeg har konfigureret et ER-format til at udskrive et Word-dokument, der indeholder en firmaadresse. I Word-skabelonen til dette ER-format har jeg indsat et kontrolelement til RTF-indhold for at vise en firmaadresse. I Finans har jeg angivet firmaadressen som flere tekstlinjer og valgt **Enter** for at tilføje en vognretur for hver linje, jeg har indtastet. Jeg forventer derfor, at firmaadressen vises som flere tekstlinjer i oprettede dokumenter. Adressen vises dog som en enkelt linje med tekst, der indeholder specialsymboler i stedet for vognretur. Hvad er der galt med mine indstillinger?

**Svar:** I stedet for at bruge et kontrolelement til RTF-indhold skal du bruge et kontrolelement til almindelig tekst og markere afkrydsningsfeltet **Tillad vognretur (flere afsnit)** i kontrolelementets egenskaber.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Genbruge ER-konfigurationer med Excel-skabeloner til generering af rapporter i Word-format](./tasks/er-design-configuration-word-2016-11.md)
- [Integrere billeder og figurer i de dokumenter, du opretter ved hjælp af ER](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
