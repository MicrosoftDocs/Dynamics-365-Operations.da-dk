---
title: Kontrollere adgang til købsaftaler i den offentlige sektor
description: Du kan sikre dig, at kun godkendte afdelinger kan få adgang til en købsaftale.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementFinDimensionAccess_PSN
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Public sector
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6e3d335b021c366accdca50ed7ce496cefaa47e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557238"
---
# <a name="control-access-to-purchase-agreements-in-the-public-sector"></a>Kontrollere adgang til købsaftaler i den offentlige sektor

[!include [task guide banner](../../includes/task-guide-banner.md)]

Du kan sikre dig, at kun godkendte afdelinger kan få adgang til en købsaftale. Du kan også begrænse det beløb, som hver afdeling kan bruge forhold til købsaftalen. For at kunne gøre det skal kontostrukturen og de økonomiske dimensioner for afdelingsadgang indstilles i formularen Kreditorparametre. Denne procedure er oprettet for franske offentlige organisationer med data fra PSUS-demofirmaet i den offentlige sektor partition.

1. Gå til Kreditor > Indkøbsordrer > Købsaftaler.
2. Vælg den indkøbsordre, du vil styre adgangen til, på listen.
3. Klik på Købsaftale i handlingsruden.
4. Klik på Afdelingsadgang.
5. Klik på Ny.
6. Klik på rullelisten i feltet Afdeling for at åbne opslaget.
7. Vælg den økonomiske dimension for en afdeling, der har adgang til denne købsaftale, på listen.
8. Angiv det samlede beløb, som denne afdeling er autoriseret til at frigive fra denne købsaftale, i feltet Godkendt beløb.
    * Tilføj flere afdelinger, indtil alle autoriserede afdelinger er føjet til købsaftalen.  
9. Klik på Gem.

