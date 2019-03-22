---
title: Angive en brugerdefineret placering, hvor oprettede dokumenter kan gemmes
description: I dette emne beskrives, hvordan du kan udvide listen over placering til lagring af dokumenter, som genereres ved elektronisk rapportering (ER).
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 3ea9de81045dfd01ffec2c8a1d98ea2ba4f2c49a
ms.sourcegitcommit: 0e01d3907b70261aee2df3e3ce0dde2f1343a43a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/27/2019
ms.locfileid: "770082"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a>Angive en brugerdefineret placering, hvor oprettede dokumenter kan gemmes

[!include[banner](../includes/banner.md)]

Med API'en (application programming interface) i den elektroniske rapporteringsstruktur (ER) kan du udvide listen over lagerplaceringer til dokumenter, som ER-formater genererer. Dette emne indeholder en oversigt over de vigtigste opgaver, du skal udføre for at tilføje en brugerdefineret lagerplacering.

## <a name="prerequisites"></a>Forudsætninger

Du skal installere en Microsoft Dynamics 365 for Finance and Operations topologi, der understøtter fortløbende build. (Yderligere oplysninger finder du i [Installere topologier, der understøtter fortløbende build og automatisering af test](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation)). Du skal have adgang til denne Finance and Operations-topologi for en af følgende roller:

- Udvikler til elektronisk rapportering
- Funktionel konsulent i elektronisk rapportering
- Systemadministrator

Du skal også have adgang til udviklingsmiljøet for denne Finance and Operations-topologi.

## <a name="create-or-import-an-er-format-configuration"></a>Oprette eller importere en konfiguration af ER-format

I den aktuelle Finance and Operations-topologi skal du [oprette et nyt ER-format](tasks/er-format-configuration-2016-11.md) for at oprette dokumenter, du vil tilføje en brugerdefineret lagerplacering for. Du kan også [importere et eksisterende ER-format til denne topologi](general-electronic-reporting-manage-configuration-lifecycle.md).

![Siden Formatdesigner](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> Det ER-format, som du opretter eller importerer, skal indeholde mindst ét af følgende formatelementer:
>
> - Fil
> - Mappe
> - Fletning
> - Vedhæftet fil

## <a name="create-a-new-document-type"></a>Oprette en ny dokumenttype

Hvis du vil angive, hvordan dokumenter, der genereres af et ER-format, skal sendes, skal du konfigurere [ER-destinationer](electronic-reporting-destinations.md). I hver ER destination, der er konfigureret til at gemme genererede dokumenter som filer, skal du angive en dokumenttype i dokumentstyringsstrukturen. Der kan bruges forskellige dokumenttyper til at sende dokumenter, som forskellige ER-formater genererer.

1. Tilføj en ny [dokumenttype](../../fin-and-ops/organization-administration/configure-document-management.md) for det ER-format, som du har oprettet eller tidligere har importeret. I følgende illustration er dokumenttypen **FileX**.
2. For at skelne denne dokumenttype fra andre dokumenttyper skal du medtage et bestemt nøgleord i dens navn. F.eks. i illustrationen, der følger, er navnet **(LOKAL) mappe**.
3. I feltet **Klasse** skal du angive **Vedhæft fil**.
4. I feltet **Gruppe** skal du angive **Fil**.

![Siden Dokumenttyper](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> Dokumenttyper er firmaspecifikke. Du kan bruge et ER-format med en destination, der er konfigureret, i flere firmaer, hvis du konfigurerer en separat dokumenttype i hvert firma.

## <a name="review-source-code"></a>Gennemgå kildekode

Gennemse koden for metoden **insertFile()** i klassen **ERDocuManagement**. Bemærk, at hændelsen **AttachingFile()** udføres, mens den oprettede fil er knyttet til en post.

```
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

Hændelsen **AttachingFile()** udføres, når de følgende ER-destinationer behandles:

- **Arkiv** – Når denne destination anvendes, oprettes en ny post for ER-formatet, der køres i tabellen ERFormatMappingRunJobTable. Feltet **Arkiveret** i denne post er indstillet til **Falsk**. Hvis ER-formatet er kørt korrekt, er det genererede dokument tilknyttet denne post, og **AttachingFile()** hændelsen udføres. Den dokumenttype, der er valgt i denne ER-destination, bestemmer lagerplaceringen for den vedhæftede fil (Microsoft Azure Storage eller en Microsoft SharePoint-mappe).
- **Jobarkiv** – Når denne destination anvendes, oprettes en ny post for ER-formularen, der køres i tabellen ERFormatMappingRunJobTable. Feltet **Arkiveret** i denne post er indstillet til **Sand**. Hvis ER-formatet er kørt korrekt, er det genererede dokument tilknyttet denne post, og **AttachingFile()** hændelsen udføres. Den dokumenttype, der er konfigureret i ER-parametrene, bestemmer lagerplaceringen for den vedhæftede fil (Azure Storage eller en SharePoint-mappe).

![Siden Parametre til elektronisk rapportering](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a>Konfigurere en ER-destination

1. Konfigurer den arkiverede destination for et af de tidligere nævnte elementer (fil, mappe, fletning eller vedhæftet fil) for det ER-format, du har oprettet eller importeret. Du kan finde en vejledning i [Konfigurere ER-destinationer](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).
2. Brug den dokumenttype, du har tilføjet tidligere for den konfigurerede destination. (I dette emne f.eks. er dokumenttypen **FileX**).

![Dialogboksen Indstillinger for destination](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a>Ændre kildekode

1. Tilføj en ny klasse til dit Microsoft Visual Studio-projekt, og skriv kode for at abonnere på den **AttachingFile()** hændelse, der blev nævnt tidligere. (Du kan finde flere oplysninger om det anvendte mønster for udvidelsesmuligheder i [Svare ved hjælp af EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result)). Skriv f.eks. kode, der udfører følgende handlinger, i den nye klasse:

    1. Du kan gemme genererede filer i en mappe i det lokale filsystem på den server, der kører Applikationsobjektserver-tjenesten (AOS).
    2. Du skal kun gemme de genererede filer, når den nye dokumenttype (f.eks. typen **FileX**, der har nøgleordet "(lokal)" i navnet) bruges, mens en fil er knyttet til posten i logfilen for ER-kørselsjobbet.

    ```
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. Gendan dit projekt.

## <a name="run-the-er-format-that-you-created-or-imported"></a>Køre det ER-format, som du har oprettet eller importeret

1. Kør det ER-format, som du har oprettet eller importeret.
2. Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Elektroniske rapporteringsjob**. Find den post, der blev oprettet til dette kørselsjob, og som har den genererede fil tilknyttet.
3. Søg i den lokale **C:\\0**-mappe for at finde samme genererede fil.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Destinationer for elektronisk rapportering](electronic-reporting-destinations.md)
- [Startside for udvidelsesmuligheder](../extensibility/extensibility-home-page.md)
