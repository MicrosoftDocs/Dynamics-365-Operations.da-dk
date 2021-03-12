---
title: Importere ISO20022 Direct Debit-konfiguration
description: Denne procedure viser, hvordan du importerer konfigurationen af rapportering af betaling elektronisk fra kunde.
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
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d68e5a63ea3b037cc111d6732857f0aae1ce7e5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989943"
---
# <a name="import-iso20022-direct-debit-configuration"></a>Importere ISO20022 Direct Debit-konfiguration

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du importerer konfigurationen af rapportering af betaling elektronisk fra kunde. Denne procedure bruger formatet ISO 20022 for Direct Debit som eksempel. 



Denne procedure er oprettet ved hjælp af demodatafirmaet DEMF, men du kan bruge et hvilket som helst demodatafirma til dette formål.



Det er den første procedure af fem, der illustrerer kundens betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.

1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. På listen over tilgængelige konfigurationsudbydere skal du vælge Microsoft.
3. Klik på Angiv som aktiv.
4. Klik på Lagre.
5. Klik på Åbn.
6. Klik på Vis filtre.
7. Anvend følgende filtre: Angiv filterværdien "ISO20022 Direct debit (DE)" i feltet "Konfigurationsnavn" ved hjælp af filteroperatøren "begynder med".
    * Du kan også finde konfigurationen på listen, vælge den og springe dette trin over.  
8. Klik på Importer.
    * Hvis knappen Importer ikke er tilgængelig, betyder det, at denne konfiguration allerede er importeret.  
9. Klik på Ja.

