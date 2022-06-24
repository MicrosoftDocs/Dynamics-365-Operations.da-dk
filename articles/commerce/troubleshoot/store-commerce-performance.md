---
title: Foretage fejlfinding af ydeevneproblemer ved Store Commerce
description: Denne artikel forklarer, hvordan du kan foretage fejlfinding af ydeevneproblemer i Microsoft Dynamics 365 Commerce Store Commerce-appen.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2022-05-12
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: b690e35b2df736f3e277260e6f752ef5240b0938
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870486"
---
# <a name="troubleshoot-store-commerce-performance-issues"></a>Foretage fejlfinding af ydeevneproblemer ved Store Commerce

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Denne artikel forklarer, hvordan du kan foretage fejlfinding af ydeevneproblemer i Microsoft Dynamics 365 Commerce Store Commerce-appen.

- Når du foretager fejlfinding af problemer med ydeevnen for Store Commerce, skal du undgå fjern logon. Log i stedet direkte på Store Commerce.
- Hvis Store Commerce-appen kører langsomt, skal du kontrollere brugen af CPU, hukommelse, netværk og disk ved hjælp af Opgavestyring eller Ressourceovervågning. Sikre, at der ikke er noget betydeligt forbrug af enhedsressourcerne.
- Kontrollér status for netværksforbindelser, og bekræft, at HTTPS-anmodninger/svar ikke tager mere end et par sekunder.
