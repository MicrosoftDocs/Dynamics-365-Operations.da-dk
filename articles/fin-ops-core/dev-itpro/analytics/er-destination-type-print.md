---
title: ER-destinationstype for printer
description: Denne artikel indeholder oplysninger om, hvordan du konfigurerer en printerdestination for de enkelte MAPPE- eller FIL-komponenter i et ER-format (elektronisk rapportering).
author: NickSelin
ms.date: 02/14/2022
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
ms.openlocfilehash: 826455d0901a45ef26755fd323ee2a2737b5eec0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845564"
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

#### <a name="pdf-printing"></a>PDF-udskrivning

I versioner af Finans før version 10.0.18 kan **Printer**-destinationen kun konfigureres for filkomponenter, der bruges til at generere output i PDF-format, der kan udskrives (**PDF-fletning** eller **PDF-fil**-formatelementer) eller Microsoft Office Excel- og Word-format (**Excel-fil**-formatelement). Når der genereres output i PDF-format, sendes det til en printer. Når der genereres output i Office-format ved hjælp af formatelementet **Excel-fil**, konverteres det automatisk til PDF-format og sendes derefter til en printer.

Fra og med version 10.0.18 kan du dog konfigurere **Printer**-destinationen til formatelementet **Fælles fil**. Dette formatelement bruges oftest til at generere output i enten TXT- eller XML-format. Du kan konfigurere et ER-format , der indeholder formatelementet **Fælles fil** som rodformatelement og formatelementet **Binært indhold** som det eneste indlejrede element under det. I dette tilfælde producerer formatelementet **Fælles fil** output i det format, der er angivet af den binding, du konfigurerer til formatelementet **Binært indhold**. Du kan f.eks. konfigurere denne binding til at [udfylde](tasks/er-document-management-files-5.md#modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format) dette element med indholdet af en vedhæftet [Dokumentstyring](../../fin-ops/organization-administration/configure-document-management.md) i PDF- eller Office-format (Excel eller Word). Du kan udskrive outputtet ved hjælp af den konfigurerede **Printer**-destination. 

> [!NOTE]
> Når du vælger formatelementet **Fælles\\fil** for at konfigurere **Printer**-destinationen, kan du på designtidspunktet ikke garantere, at det valgte element vil producere output i PDF-format eller output, der kan konverteres til PDF-format. Du får derfor følgende advarselsmeddelelse: "Sørg for, at det output, der genereres af den valgte formatkomponent, kan konverteres til PDF. Ellers skal du fjerne markeringen i afkrydsningsfeltet 'Konverter til PDF'." Du skal hjælpe med at forhindre kørselsproblemer, når der ikke er angivet PDF- eller PDF-konverteringsbart output til udskrivning under kørsel. Hvis du forventer at modtage output i Office-format (Excel eller Word), skal indstillingen **Konverter til PDF** være valgt.
>
> I version 10.0.26 og senere skal du for at bruge **Konverter til PDF** vælge **PDF** for parameteren **Dokumentrutetype** for den konfigurerede **Printer**-destination.

#### <a name="zpl-printing"></a>ZPL-udskrivning

I version 10.0.26 og senere kan du konfigurere **Printer**-destinationen til formatelementet **Fælles\\fil** ved at vælge **ZPL** til parameteren **Dokumentrutetype**. I dette tilfælde ignoreres indstillingen **Konverter til PDF** ved kørsel, og TXT- eller XML-outputtet sendes direkte til en valgt printer ved hjælp af ZPL-kontrakten (Zebra Programming Language) for [dokumentets ruteplanlægningsagent (DRA)](install-document-routing-agent.md). Du kan bruge denne funktion til et ER-format, der repræsenterer et ZPL II-labellayout, til at udskrive forskellige labels.

[![Konfigurere parameteren Dokumentrutetype i dialogboksen Destinationsindstillinger.](./media/ER_Destinations-SetDocumentRoutingType.png)](./media/ER_Destinations-SetDocumentRoutingType.png)

Du kan finde flere oplysninger om denne funktion i [Designe en ny ER-løsning til udskrivning af ZPL-labels](er-design-zpl-labels.md).

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
