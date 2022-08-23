---
title: Designe et ER-format for at holde rækker sammen på samme Excel-side
description: Denne artikel forklarer, hvordan du designer et elektronisk rapporteringsformat (ER), der holder rækker sammen på samme Microsoft Excel-side.
author: kfend
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-03-01
ms.dyn365.ops.version: Version 10.0.26
ms.custom: 220314
ms.assetid: ''
ms.search.form: EROperationDesigner
ms.openlocfilehash: 7ecc4358a0d4d9ae9e729393bd3ac4cefbf15ad2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287952"
---
# <a name="design-an-er-format-to-keep-rows-together-on-the-same-excel-page"></a>Designe et ER-format for at holde rækker sammen på samme Excel-side

[!include [banner](../includes/banner.md)]


Denne artikel forklarer, hvordan en bruger i rollen Systemadministrator eller Funktionel konsulent i elektronisk rapportering kan konfigurere et [ER-format (elektronisk rapportering)](general-electronic-reporting.md) som et [format](er-overview-components.md#format-component), der genererer udgående dokumenter i Microsoft Excel og administrerer sideinddeling af dokumenter, så rækker, der oprettes, bevares på samme side.

I dette eksempel skal du redigere det ER-format, der leveres af Microsoft, og som bruges til at udskrive fritekstfakturaer i Excel. Dine ændringer giver dig mulighed for at administrere sideinddelingen i en genereret fritekstfakturarapport, så alle rækkerne i en enkelt fakturalinje bevares på samme side, når det er muligt.

Procedurerne i denne artikel kan fuldføres i **USMF**-firmaet. Der kræves ingen kodning.

I dette eksempel opretter du de krævede ER-[konfigurationer](general-electronic-reporting.md#Configuration) for **Litware, Inc.**- eksempelvirksomheden. Sørg for, at konfigurationsudbyderen for eksempelfirmaet **Litware, Inc.** (`http://www.litware.com`) er angivet for ER-strukturen og er markeret som **Aktiv**. Hvis denne konfigurationsudbyder ikke er angivet, eller hvis den ikke er markeret som **Aktiv**, skal du følge trinnene i emnet [Opret en konfigurationsudbyder, og markér den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="enter-a-new-free-text-invoice"></a>Indtaste en ny fritekstfaktura

1. Benyt fremgangsmåden i [Opret en fritekstfaktura](../../../finance/accounts-receivable/create-free-text-invoice-new.md#create-a-free-text-invoice-1) for at tilføje en fritekstfaktura.

    1. Føj en enkelt linje til fakturaen.
    2. Føj fem noter til fakturalinjen.

    ![Gennemse fakturalinjenoterne på siden Vedhæftede filer.](./media/er-keep-excel-rows-together-notes.png)

2. Benyt fremgangsmåden i [Kopiér linjer](../../../finance/accounts-receivable/create-free-text-invoice-new.md#copy-lines) til at oprette fem ekstra fakturalinjer, som er kopier af den fakturalinje, du tilføjede i det forrige trin.

    ![Gennemse fritekstfakturalinjerne på siden Fritekstfaktura.](./media/er-keep-excel-rows-together-invoice.png)

## <a name="configure-the-er-framework"></a>Konfigurere ER-strukturen

Følg trinnene i [Konfigurere ER-strukturen](er-quick-start2-customize-report.md#ConfigureFramework) for at konfigurere det minimale sæt af ER-parametre. Du skal fuldføre denne opsætning, før du begynder at bruge ER-strukturen til at designe en tilpasset version af et ER-standardformat.

## <a name="import-the-standard-er-format-configuration"></a>Importere standardkonfigurationen af ER-format

Følg trinnene i [Importere standardkonfigurationen af ER-format](er-quick-start2-customize-report.md#ImportERSolution1) for at føje ER-standardkonfigurationerne til den aktuelle forekomst af Dynamics 365 Finance. Importér f.eks. version **252.116** af **Fritekstfaktura (Excel)**-formatkonfigurationen. Basisversion **252** af basiskonfigurationen **Fakturamodel** importeres automatisk fra lageret sammen med den nødvendige konfiguration af **Fakturamodeltilknytning**.

## <a name="set-up-print-management-to-use-the-standard-er-format"></a>Konfigurere udskriftsstyring til at bruge standard ER-format

Følg trinnene i [Konfigurere udskriftsstyring](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement1) for at konfigurere udskriftsstyring for modulet **Debitor**, så standard ER-formatet bruges til at udskrive fritekstfakturaer.

## <a name="configure-a-format-destination-for-the-standard-er-format"></a>Konfigurere en formatdestination for standard ER-formatet

Følg trinnene i [Konfigurer en formatdestination til eksempelvisning på skærmen](er-quick-start1-new-solution.md#ConfigureDestination) for at konfigurere [Skærm](er-destination-type-screen.md)-ER-destinationen for standard ER-formatet, så genererede rapporter konverteres til PDF-format og vises som eksempel under en ny fane i en browser.

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a>Udskrive en fritekstfaktura ved hjælp af standard ER-format

1. Benyt fremgangsmåden i [Udskrive en fritekstfaktura](er-embed-images-header-footer-excel-reports.md#ProcessInvoice1), hvis du vil bruge standard ER-formatet til at generere en rapport over fritekstfakturaer i Excel-format til den ekstra faktura.
2. Download den genererede Excel-projektmappe, og gennemse den i Excel-skrivebordsapplikationen.

    Bemærk, at den sjette linje i fakturaen starter på første side i rapporten og fortsætter på anden side. Den sidste note vises på den anden side, og det er ikke indlysende, at den tilhører den sjette fakturalinje. Sideskiftet midt i indholdet af fakturalinjen gør det derfor sværere at læse dette dokument.

    ![Gennemse sideinddelingen af den oprettede fritekstfaktura i Excel-skrivebordsprogrammet.](./media/er-keep-excel-rows-together-invoice1.gif)

De resterende procedurer i denne artikel viser, hvordan du kan tilpasse standard ER-formatet for at forbedre fakturarapportens udseende og læsbarhed ved at beholde alt indholdet for en enkelt fakturalinje på samme side.

## <a name="create-a-custom-format"></a>Oprette et brugerdefineret format

Følg trinnene i [Oprette et brugerdefineret format](er-embed-images-header-footer-excel-reports.md#DeriveProvidedFormat) for at aflede et format fra det importerede ER-format og oprette en **Brugerdefineret fritekstfaktura (Excel)** som ER-konfiguration, der kan redigeres.

## <a name="edit-the-custom-format"></a>Redigere brugerdefineret format

1. Følg trinnene i [Opret et brugerdefineret format](er-embed-images-header-footer-excel-reports.md#ConfigureDerivedFormat) for at åbne det afledte ER-format til redigering i ER-formatdesigneren.
2. På siden **Formatdesigner** skal du i formatkomponenttræet i venstre rude udvide **Fritekstfaktura \> Ark \> InvoiceLines** og vælge komponenten **InvoiceLines_Values**.
3. Vælg **Ja** i indstillingen **Hold rækker sammen** under fanen **Format**.

    ![Indstilling af Hold rækker sammen for det ER-format, der kan redigeres, på siden Formatdesigner.](./media/er-keep-excel-rows-together-format.png)

4. Vælg **Gem**, og luk siden.

## <a name="mark-the-custom-format-as-runnable"></a>Markere det brugerdefineret format som kørbart

Følg trinnene i [Markere det brugerdefinerede format som kørbart](er-embed-images-header-footer-excel-reports.md#MarkFormatRunnable) for at gøre den ændrede version af det brugerdefinerede ER-format kørbart.

## <a name="set-up-print-management-to-use-the-custom-er-format"></a>Konfigurere udskriftsstyring til at bruge det brugerdefinerede ER-format

Følg trinnene i [Konfigurere udskriftsstyring](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement2) for at konfigurere udskriftsstyring for modulet **Debitor**, så det brugerdefinerede ER-format bruges til at udskrive fritekstfakturaer.

## <a name="configure-a-format-destination-for-the-custom-er-format"></a>Konfigurere en formatdestination for det brugerdefinerede ER-format

Følg trinnene i [Konfigurer en formatdestination til eksempelvisning på skærmen](er-quick-start1-new-solution.md#ConfigureDestination) for at konfigurere **Skærm**-ER-destinationen for det brugerdefinerede ER-format, så genererede rapporter konverteres til PDF-format og vises som eksempel under en ny fane i en browser.

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a>Udskrive en fritekstfaktura ved hjælp af det brugerdefinerede ER-format

1. Benyt fremgangsmåden i [Udskrive en fritekstfaktura](er-embed-images-header-footer-excel-reports.md#ProcessInvoice2), hvis du vil bruge det brugerdefinerede ER-format til at generere en rapport over fritekstfakturaer i Excel-format til den ekstra faktura.
2. Download den genererede Excel-projektmappe, og gennemse den i Excel-skrivebordsapplikationen.

    Bemærk, at den sjette linje i fakturaen starter på den anden side, og alle de Excel-rækker, der repræsenterer denne fakturalinje, vises sammen på denne side.

    ![Gennemse af den opdaterede sideinddeling af den oprettede fritekstfaktura i Excel-skrivebordsprogrammet.](./media/er-keep-excel-rows-together-invoice2.gif)

## <a name="additional-resources"></a>Yderligere ressourcer

[Designe en konfiguration til at generere dokumenter i Excel-format](er-fillable-excel.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
