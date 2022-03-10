---
title: ER-destinationstype for printer
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer en printerdestination for de enkelte MAPPE- eller FIL-komponenter i et ER-format (elektronisk rapportering).
author: NickSelin
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 672b1d70607a32d30c703ce39573d7480462fec45739b6e1e49ef27166a50e2c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712706"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Printerdestination

[!include [banner](../includes/banner.md)]

Du kan sende et genereret dokument direkte til en netværksprinter til direkte udskrivning.

## <a name="prerequisites"></a>Forudsætninger

Før du går i gang, skal du installere og konfigurere Dokumentets ruteplanlægningsagent og derefter registrere netværksprinterne. Du kan finde flere oplysninger i [Installere dokumentets ruteplanlægningsagent for at aktivere netværksudskrivning](./install-document-routing-agent.md).

## <a name="make-the-printer-destination-available"></a>Gør printerdestinationen tilgængelig

Hvis du vil gøre **Printer**-destinationen tilgængelig i den aktuelle forekomst af Microsoft Dynamics 365 Finance, skal du gå til arbejdsområdet **Funktionsstyring** og aktivere følgende funktioner i denne rækkefølge:

1. Konverter udgående dokumenter for elektronisk rapportering fra Microsoft Office-formater til PDF
2. Dokumentets ruteplanlægningsagent som elektronisk rapporteringsdestination for udgående dokumenter

[![Aktivere funktionen til ER-printerdestination i Funktionsstyring.](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Anvendelighed

**Printer**-destinationen kan kun konfigureres for filkomponenter, der bruges til at generere output enten i PDF-format, der kan udskrives (PDF-fletning eller PDF-filformatelementer) eller Microsoft Office Excel/Word-format (Excel-fil). Når der genereres output i PDF-format, sendes det til en printer. Når der genereres output i Microsoft Office-format, konverteres det automatisk til PDF-format og sendes derefter til en printer.

### <a name="limitations"></a>Begrænsninger

**Printer**-destinationen implementeres kun i forbindelse med installationer i skyen.

### <a name="use-the-printer-destination"></a>Brug printerdestinationen

1. Angiv indstillingen **Aktiveret** til **Ja** for at sende et genereret dokument til en printer.
2. I feltet **Printernavn** skal du vælge den ønskede netværksprinter.
3. Angiv indstillingen **Gem i udskriftsarkiv?** til **Ja** for at gemme det genererede output i udskriftsarkivet, så det er tilgængeligt til yderligere udskrivning. Hvis du senere vil have adgang til arkiveret, skal du gå til **Organisationsadministration** \> **Forespørgsler og rapporter** \> **Rapportarkiv**.

[![Brug af printerdestinationen.](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Indstillingen **Konverter til PDF** behøver ikke at blive aktiveret, når du konfigurer destinationen **Printer**. PDF-konvertering til udskrivningsformål sker, også selvom indstillingen er slået fra.

Hvis du vil bruge en bestemt [sideretning](electronic-reporting-destinations.md#SelectPdfPageOrientation), når du udskriver et udgående dokument i Excel-format, skal du aktivere indstillingen **Konverter til PDF**. Når du sætter indstillingen **Konverter til PDF** til **Ja**, bliver feltet **Sideretning** tilgængeligt. Du kan vælge en sideretning i feltet **Sideretning**.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [Destinationer for elektronisk rapportering (ER)](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]