---
title: ER-destinationstype for arkiv
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere en arkivdestination for hver komponent af typen MAPPE eller FIL i et elektronisk rapporteringsformat (ER), der er konfigureret til at generere udgående dokumenter.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
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
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 15611a4f0000ca5ccb0ac3f4012251d5bf5689ec
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019688"
---
# <a name="ArchiveDestinationType">Arkivdestination</a>

[!include [banner](../includes/banner.md)]

Du kan konfigurere en arkivdestination for hver komponent af typen MAPPE eller FIL i et elektronisk rapporteringsformat (ER), der er konfigureret til at generere udgående dokumenter. På baggrund af destinationsindstillingen gemmes et genereret dokument som en vedhæftet fil til en post på ER-joblisten.

Du kan bruge denne indstilling til at sende det genererede dokument til en Microsoft SharePoint-mappe eller Microsoft Azure Storage. Indstil **Aktiveret** til **Ja** for at sende output til en destination, der er defineret af den valgte dokumenttype. Kun dokumenttyper, hvor gruppen er indstillet til **Fil**, kan vælges. Du definerer dokumentets [typer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) i **Organisationsadministration** \> **Dokumentstyring** \> **Dokumenttyper**. Konfigurationen for ER-destinationer svarer til konfigurationen for dokumentstyringssystemet.

[![Siden Dokumenttyper](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Lokaliteten bestemmer, hvor filen gemmes. Når destinationen **Arkiv** er aktiveret, kan resultaterne gemmes i jobarkivet. Du kan få vist resultaterne i **Virksomhedsadministration** \> **elektronisk rapportering** \> **Elektronisk rapportering af arkiverede job**.

> [!NOTE]
> Vælg en dokumenttype til jobarkivet ved at navigere til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering** \> **Parametre til elektronisk rapportering**. Du kan finde flere oplysninger under [Konfigurere den elektroniske rapporteringsstruktur (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>SharePoint

Du kan gemme en fil i en angivet SharePoint-mappe. Når du vil definere SharePoint-standardserveren, skal du gå til **Organisationsadministration** \> **Dokumentstyring** \> **Dokumentstyringsparametre**. Under fanen **SharePoint** skal du konfigurere SharePoint-mappen. Derefter kan du vælge den som den mappe, hvor ER-outputtet skal gemmes. **SharePoint**-placeringen skal vælges i denne dokumenttype.

[![Valg af en SharePoint-mappe](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure Storage

Når dokumenttypens placering er angivet til **Azure-lager**, kan du gemme en fil på Azure Storage.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [Destinationer for elektronisk rapportering (ER)](electronic-reporting-destinations.md)
- [Konfigurere dokumentstyring](../../fin-ops/organization-administration/configure-document-management.md)
