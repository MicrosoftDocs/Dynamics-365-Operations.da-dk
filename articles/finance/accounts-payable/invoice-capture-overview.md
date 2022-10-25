---
title: Oversigt over løsningen Invoice Capture
description: Denne artikel indeholder oplysninger om løsningen Invoice Capture.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76441220b93744527f412110db536601a2fa1dd9
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691163"
---
# <a name="invoice-capture-solution"></a>Løsningen Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikel indeholder oplysninger om løsningen Invoice Capture, der automatisk opretter kreditorfakturaer ud fra digitale fakturabilleder.

Kreditorbogholderiet administrerer og behandler fakturaer for modtagne varer og tjenester. Kreditorbogholderen kontrollerer kreditorfakturadata af følgende årsager:

- For at undgå ekstra arbejde med reguleringer eller rettelser i forbindelse med lukning af en periode
- For at betale kreditorfakturaer rettidigt og forhindre økonomisk tab som følge af fejl eller svindel

OCR (Optical Character Recognition - optisk tegngenkendelse) er blevet udbredt i forskellige brancher de seneste år. Det er nu almindeligt, at udskrevne tekster digitaliseres, så de kan redigeres elektronisk, søges i, opbevares mere kompakt og vises online. Den digitale tekst kan bruges i maskinprocesser som f.eks. kognitiv computing, maskinoversættelse, tekst til tale, nøgledata og tekst-mining.

Med udbredelsen af teknologi med kunstig intelligens (AI) er det blevet muligt at læse forskellige fakturaformater fra forskellige leverandører i moderne OCR-løsninger uden at kræve særlig menneskelig indgriben. Flere firmaer oplever, at de kan spare tid og blive mere nøjagtige ved at behandle fakturaer via automatisering i stedet for at udføre manuel behandling.

## <a name="system-landscape"></a>Systemlandskab

I følgende illustration vises de vigtigste komponenter og trin i løsningen Invoice Capture.

[![Komponenter og trin i løsningen Invoice Capture.](./media/Invoice-capture2.png)](./media/Invoice-capture2.png)

## <a name="required-roles"></a>Påkrævede roller

Følgende tabel viser de roller, der kræves for at konfigurere og bruge løsningen Invoice Capture.

| Rolle          | Handlinger | Systemer | Rollenavne |
|---------------|---------|---------|-----------|
| Administrator | <ul><li>Konfigurere miljøer i Microsoft Power Platform.</li><li>Installere løsninger i Microsoft Power Platform.</li><li>Oprette forbindelser mellem Dynamics 365 og AI Builder.</li><li>Konfigurere Azure Data Lake Storage-lokationer.</li></ul> | <ul><li>Dynamics 365</li><li>Microsoft Power Platform</li><li>Azure Data Lake Storage</li></ul> | <ul><li>Dynamics 365-administrator</li><li>Power Platform-administrator</li><li>Ejer af Blob Storage-datalager</li></ul> |
| AI-udvikler      | <ul><li>Vedligeholde flow.</li><li>Oprette tilpassede modeller til kunstig intelligens.</li></ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Borgerbeslutningstagere</li></ul> |
| Kreditorassistent      | <ul><li>Gennemse og udføre handlinger i det midlertidige område for kreditorfakturaer.</li><ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Ny kreditorassistentrolle i Power Platform</li></ul> |
| Kreditorassistent      | <ul><li>Udføre daglige operationer som kreditorassistent.</li><li>Navigere til det midlertidige område for kreditorfakturaer.</li></ul> | <ul><li>Dynamics 365</li></ul> | <ul><li>Kreditorassistent</li></ul> |
  
Yderligere oplysninger om installation af Invoice Capture finder du under [Installere Invoice Capture](../accounts-payable/install-invoice-capture.md).  
