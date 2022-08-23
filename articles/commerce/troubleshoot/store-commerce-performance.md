---
title: Foretage fejlfinding af ydeevneproblemer ved Store Commerce
description: Denne artikel forklarer, hvordan du kan foretage fejlfinding af ydeevneproblemer i Microsoft Dynamics 365 Commerce Store Commerce-appen.
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2022-05-12
ms.dyn365.ops.version: 10.0.25
ms.search.industry: Retail
ms.openlocfilehash: 0354fbac438ff00ba057993a466bbbbfdd99247d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286297"
---
# <a name="troubleshoot-store-commerce-performance-issues"></a>Foretage fejlfinding af ydeevneproblemer ved Store Commerce

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du kan foretage fejlfinding af ydeevneproblemer i Microsoft Dynamics 365 Commerce Store Commerce-appen.

- Når du foretager fejlfinding af problemer med ydeevnen for Store Commerce, skal du undgå fjern logon. Log i stedet direkte på Store Commerce.
- Hvis Store Commerce-appen kører langsomt, skal du kontrollere brugen af CPU, hukommelse, netværk og disk ved hjælp af Opgavestyring eller Ressourceovervågning. Sikre, at der ikke er noget betydeligt forbrug af enhedsressourcerne.
- Kontrollér status for netværksforbindelser, og bekræft, at HTTPS-anmodninger/svar ikke tager mere end et par sekunder.
