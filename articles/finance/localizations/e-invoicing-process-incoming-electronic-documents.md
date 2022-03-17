---
title: Behandle af indgående elektroniske dokumenter
description: Dette emne indeholder en oversigt over behandlingen af indgående elektroniske dokumenter.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9701367e1ba1f9dbd1e53deb863c10af4213a359
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371536"
---
# <a name="processing-of-incoming-electronic-documents"></a>Behandle af indgående elektroniske dokumenter

[!include [banner](../includes/banner.md)]

Indgående elektroniske dokumenter, f.eks. elektroniske kreditorfakturaer, kan importeres og behandles på to måder:

- Filerne hentes fra eksterne kanaler og overføres direkte til det tilsluttede program. Her sker yderligere transformation, og de importeres derefter til databasen.
- Filer skal forbehandles i tjenesten Elektronisk fakturering og overføres derefter til det tilknyttede program.

Elektronisk fakturering understøtter to kanaler til indgående dokumenter: mail og Microsoft SharePoint-mapper.

Der findes to opsætningstyper til angivelse af, om dokumenter skal forbehandles eller overføres direkte til det tilknyttede program:

- **Datakanal** – Systemet sender dokumentet direkte til det tilknyttede program.
- **Datakanal med behandlingspipeline** – Du kan konfigurere yderligere handlinger, der skal køres, før dokumentet sendes til det tilknyttede program.

Du kan finde oplysninger om, hvordan du konfigurerer scenarier for behandling af indgående elektroniske dokumenter til de forskellige kanaler, i [Konfigurere en mailkanal](e-invoicing-configure-email.md) og [Konfigurere en SharePoint-kanal](e-invoicing-configure-sharepoint-channel.md).
