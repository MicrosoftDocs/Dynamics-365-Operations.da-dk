---
title: Importere konfiguration for ISO20022-kreditoverførsel
description: Denne procedure viser, hvordan du importerer konfigurationen af rapportering af betaling elektronisk fra kreditor.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 01f44c49b6623cbcc2f08cfd6e4978c9a1676b83
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140035"
---
# <a name="import-iso20022-credit-transfer-configuration"></a>Importere konfiguration for ISO20022-kreditoverførsel

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du importerer konfigurationen af rapportering af betaling elektronisk fra kreditor. Det tyske ISO 20022-format for kreditoverførsel bruges som eksempel. Denne procedure kan bruges til andre tilgængelige elektroniske rapporteringsformater. 

Denne opgave er oprettet ved hjælp af demodatafirmaet DEMF, men du kan bruge et hvilket som helst demodatafirma til at udføre denne opgave.

Det er den første af fem opgaver, der tilsammen illustrerer kreditors betalingsproces ved hjælp af konfigurationer af elektronisk rapportering. Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.

1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. På listen over tilgængelige konfigurationsudbydere skal du vælge Microsoft.
3. Klik på Angiv som aktiv.
4. Klik på Lagre.
5. Klik på Åbn.
6. Klik på Vis filtre.
7. Anvend følgende filtre: Angiv filterværdien "ISO20022-overførsel (DE)" i feltet "Konfigurationsnavn" ved hjælp af filteroperatøren "begynder med".
    * Du kan også finde konfigurationen på listen, markere den og derefter flytte den til importopgaven.  
8. Klik på Importer.
    * Hvis knappen Importer ikke er tilgængelig, betyder det, at denne konfiguration allerede er importeret.  
9. Klik på Ja.

