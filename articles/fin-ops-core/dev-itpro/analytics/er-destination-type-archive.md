---
title: ER-destinationstype for arkiv
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer en arkivdestination for de enkelte MAPPE- eller FIL-komponenter i et ER-format (elektronisk rapportering).
author: NickSelin
ms.date: 11/30/2020
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
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: a9e0f07241de003dd2971e0d336f89795ad1319b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348014"
---
# <a name="archive-er-destination-type"></a>ER-destinationstype for arkiv

[!include [banner](../includes/banner.md)]

Du kan konfigurere en arkivdestination for hver komponent af typen **Mappe** eller **Fil** i et elektronisk rapporteringsformat (ER), der er konfigureret til at generere udgående dokumenter. På baggrund af destinationsindstillingen gemmes et genereret dokument som en vedhæftet fil til en post på ER-joblisten. Du kan få vist resultaterne ved at gå til **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Elektronisk rapportering af job**.

Du kan bruge denne indstilling til at sende det genererede dokument til en Microsoft SharePoint-mappe eller Microsoft Azure Storage. Indstil **Aktiveret** til **Ja** for at sende output til en destination, der er defineret af den valgte dokumenttype. Kun dokumenttyper, hvor gruppen er indstillet til **Fil**, kan vælges. Du definerer dokumentets [typer](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) i **Organisationsadministration** \> **Dokumentstyring** \> **Dokumenttyper**. Konfigurationen for ER-destinationer svarer til konfigurationen for dokumentstyringssystemet.

[![Siden Dokumenttyper.](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Lokaliteten bestemmer, hvor filen gemmes. Når destinationen **Arkiv** er aktiveret, kan resultaterne gemmes i jobarkivet. Du kan få vist resultaterne i **Virksomhedsadministration** \> **elektronisk rapportering** \> **Elektronisk rapportering af arkiverede job**.

> [!NOTE]
> Vælg en dokumenttype til jobarkivet ved at navigere til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering** \> **Parametre til elektronisk rapportering**. Du kan finde flere oplysninger under [Konfigurere den elektroniske rapporteringsstruktur (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>SharePoint

Du kan gemme en fil i en angivet SharePoint-mappe. Når du vil definere SharePoint-standardserveren, skal du gå til **Organisationsadministration** \> **Dokumentstyring** \> **Dokumentstyringsparametre**. Under fanen **SharePoint** skal du konfigurere SharePoint-mappen. Derefter kan du vælge den som den mappe, hvor ER-outputtet skal gemmes. **SharePoint**-placeringen skal vælges i denne dokumenttype.

[![Valg af en SharePoint-mappe.](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure Storage

Når dokumenttypens placering er angivet til **Azure-lager**, kan du gemme en fil på Azure Storage.

> [!NOTE] 
> ER-strukturen gemmer filer i Azure Blob Storage permanent i modsætning til dataadministrationsstrukturen, der anvender den syv-dages opbevaringspolitik for dokumenter, der skal behandles. Du kan finde flere oplysninger under [API til hentning af meddelelsesstatus](../data-entities/recurring-integrations.md#api-for-getting-message-status) og [API til statuskontrol](../data-entities/data-management-api.md#status-check-api). De ER-relaterede filer gemmes i Azure Blob Storage som vedhæftede filer i programtabelposter, hvis det er nødvendigt. En enkelt fil slettet fra Azure Blob Storage sammen med den programtabelpost, som denne fil var knyttet til.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [Destinationer for elektronisk rapportering (ER)](electronic-reporting-destinations.md)
- [Konfigurere dokumentstyring](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]