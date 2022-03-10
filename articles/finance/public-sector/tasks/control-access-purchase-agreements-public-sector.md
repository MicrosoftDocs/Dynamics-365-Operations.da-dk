---
title: Kontrollere adgang til købsaftaler i den offentlige sektor
description: Du kan sikre dig, at kun godkendte afdelinger kan få adgang til en købsaftale.
author: twheeloc
ms.date: 02/14/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementFinDimensionAccess_PSN
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.search.industry: Public sector
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95f6b5133d7bae1a93a709322e11ee1632aa4985
ms.sourcegitcommit: 6a269db08e8bb3bb3405c9f4a512091d13c80faa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119441"
---
# <a name="control-access-to-purchase-agreements-in-the-public-sector"></a>Kontrollere adgang til købsaftaler i den offentlige sektor

[!include [banner](../../includes/banner.md)]

Du kan sikre dig, at kun godkendte afdelinger kan få adgang til en købsaftale. Du kan også begrænse det beløb, som hver afdeling kan bruge forhold til købsaftalen. For at kunne gøre det skal kontostrukturen og de økonomiske dimensioner for afdelingsadgang indstilles på siden **Kreditorparametre**. Denne procedure er oprettet for franske offentlige organisationer med data fra PSUS-demofirmaet i den offentlige sektor partition.

1. Gå til **Kreditor > Indkøbsordrer > Købsaftaler**.
2. Vælg den indkøbsordre, du vil styre adgangen til, på listen.
3. Klik på **Købsaftale** i **handlingsruden**.
4. Klik på **Afdelingsadgang**.
5. Klik på **Ny**.
6. Klik på rullelisten i feltet **Afdeling** for at åbne opslaget.
7. Vælg den økonomiske dimension for en afdeling, der har adgang til denne købsaftale, på listen.
8. Angiv det samlede beløb, som denne afdeling er autoriseret til at frigive fra denne købsaftale, i feltet **Godkendt beløb**.
    * Tilføj flere afdelinger, indtil alle autoriserede afdelinger er føjet til købsaftalen.  
9. Klik på **Gem**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
