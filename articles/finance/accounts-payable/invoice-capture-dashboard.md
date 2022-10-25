---
title: Dashboard for løsningen Invoice Capture
description: Denne artikel beskriver dashboardet til løsningen Invoice Capture.
author: sunfzam
ms.date: 10/15/2022
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
ms.openlocfilehash: 4c9000039488c1290f4ab992d7fe79b8ccac7b19
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690113"
---
# <a name="invoice-capture-solution-dashboard"></a>Dashboard for løsningen Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

I Invoice Capture indeholder dashboardet diagrammer med en oversigt over fakturaer, der er importeret. Disse diagrammer kan hjælpe kreditorchefen med at analysere ydeevnen af fakturagenereringsprocessen. Kreditoradministratoren kan se status for processen til oprettelse af fakturaer og kan også se detaljer ved at anvende forskellige filtre.

## <a name="available-charts"></a>Tilgængelige diagrammer

Følgende diagrammer er tilgængelige på dashboardet:

- **Alle hentede fakturaer efter status** – I dette diagram vises følgende statusser for en hentet faktura. Når de vælger en status, kan brugerne filtrere de hentede fakturaer på den detaljerede liste.

    - Hentet
    - Fuldfør
    - Til gennemgang
    - Forældet

- **Samlet hentet fakturavolumen** – I dette diagram vises antallet af hentede fakturaer efter periode. Brugere kan ændre perioden ved hjælp af rullelisten.
- **Hentet faktura fra topleverandører** – I dette diagram vises det samlede antal fakturaer pr. leverandør. De kreditorer, der har de fleste fakturaer, vises øverst.
- **Dage til fuldførelse pr. faktura med undtagelser** – Dette diagram viser det gennemsnitlige antal dage, der kræves til at hente én faktura. Disse oplysninger kan hjælpe kreditorchefen med at analysere, hvor lang tid det tager at behandle en faktura, når der kræves manuel indgriben. Hvis der er en opadgående tendens, kan brugerne gennemgå procesdetaljerne og justere indstillingerne for at reducere antallet af dage, der kræves.
- **Ufuldstændige fakturaer efter ventetid** – Dette diagram viser det antal dage, en hentet faktura ikke er genereret i ERP-systemet (Enterprise Resource Planning). Jo større antallet af ventedage er, jo længere er processen til oprettelse af fakturaer. Kreditorchefen kan dykke ned i de detaljerede hentede fakturaer og generere fakturaer i ERP-systemet.
