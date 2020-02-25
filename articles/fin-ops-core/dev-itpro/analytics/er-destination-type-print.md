---
title: ER-destinationstype for printer
description: Dette emne forklarer, hvordan du kan konfigurere en printerdestination for hver komponent af typen MAPPE eller FIL i et elektronisk rapporteringsformat (ER), der er konfigureret til at generere udgående dokumenter i enten PDF eller Microsoft Office-formater (Excel\Word).
author: NickSelin
manager: AnnBe
ms.date: 01/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58e067baa130458e3a8e788d978604f208140a03
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019687"
---
# <a name="PrinterDestinationType"></a>Printerdestination

[!include [banner](../includes/banner.md)]

Du kan sende et genereret dokument direkte til en netværksprinter til direkte udskrivning.

## <a name="prerequisites"></a>Forudsætninger

Før du går i gang, skal du installere og konfigurere Dokumentets ruteplanlægningsagent og derefter registrere netværksprinterne. Du kan finde flere oplysninger i [Installere dokumentets ruteplanlægningsagent for at aktivere netværksudskrivning](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).

## <a name="make-the-printer-destination-available"></a>Gør printerdestinationen tilgængelig

Hvis du vil gøre **Printer**-destinationen tilgængelig i den aktuelle forekomst af Microsoft Dynamics 365 Finance, skal du gå til arbejdsområdet **Funktionsstyring** og aktivere følgende funktioner i denne rækkefølge:

1. Konverter udgående dokumenter for elektronisk rapportering fra Microsoft Office-formater til PDF
2. Dokumentets ruteplanlægningsagent som elektronisk rapporteringsdestination for udgående dokumenter

[![Aktivere funktionen til ER-printerdestination i Funktionsstyring](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Anvendelighed

**Printer**-destinationen kan kun konfigureres for filkomponenter, der bruges til at generere output enten i PDF-format, der kan udskrives (PDF-fletning eller PDF-filformatelementer) eller Microsoft Office Excel/Word-format (Excel-fil). Når der genereres output i PDF-format, sendes det til en printer. Når der genereres output i Microsoft Office-format, konverteres det automatisk til PDF-format og sendes derefter til en printer.

### <a name="limitations"></a>Begrænsninger

Denne funktion er en prøveversionsfunktion og er underlagt de vilkår for anvendelse, der er beskrevet i [Supplerende vilkår for anvendelse for Microsoft Dynamics 365-prøveversioner](https://go.microsoft.com/fwlink/?linkid=2105274).

**Printer**-destinationen implementeres kun i forbindelse med installationer i skyen.

### <a name="use-the-printer-destination"></a>Brug printerdestinationen

1. Angiv indstillingen **Aktiveret** til **Ja** for at sende et genereret dokument til en printer.
2. I feltet **Printernavn** skal du vælge den ønskede netværksprinter.
3. Angiv indstillingen **Gem i udskriftsarkiv?** til **Ja** for at gemme det genererede output i udskriftsarkivet, så det er tilgængeligt til yderligere udskrivning. Hvis du senere vil have adgang til arkiveret, skal du gå til **Organisationsadministration** \> **Forespørgsler og rapporter** \> **Rapportarkiv**.

[![Brug af printerdestinationen](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Indstillingen **Konverter til PDF** behøver ikke at blive aktiveret, når du konfigurer destinationen **Printer**. PDF-konvertering til udskrivningsformål sker, også selvom indstillingen er slået fra.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [Destinationer for elektronisk rapportering (ER)](electronic-reporting-destinations.md)
