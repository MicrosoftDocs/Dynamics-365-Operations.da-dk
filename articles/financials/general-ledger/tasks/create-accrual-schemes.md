---
title: Oprette periodiseringsskemaer
description: Denne opgaveguide gennemgår oprettelse af en periodiseringsskema.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0ae55000a5cf1593d057d940dc3dbbf9e5cb3f3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834874"
---
# <a name="create-accrual-schemes"></a>Oprette periodiseringsskemaer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide gennemgår oprettelse af en periodiseringsskema. Denne opgave bruger demofirmaet USMF.

1. Gå til Finans > Kladdeopsætning > Periodiseringsskemaer.
2. Klik på Ny.
3. Skriv en værdi i feltet Periodiseringsidentifikation.
4. Skriv en værdi i feltet Beskrivelse af periodiseringsskema.
5. I feltet Debet skal du specificere de ønskede værdier.
    * Den hovedkonto, der defineres, erstatter debethovedkontoen på kladdebilagslinjen, og det bruges også til tilbageførsel af den udelukkelse, der er baseret på posteringer til periodisering af finans.  
6. I feltet Kredit skal du specificere de ønskede værdier.
    * Den hovedkonto, der defineres, erstatter kredithovedkontoen på kladdebilagslinjen, og det bruges også til tilbageførsel af den udelukkelse, der er baseret på posteringer til periodisering af finans.  
7. I feltet Bilag skal du vælge, hvordan bilaget skal bestemmes, når transaktionerne bogføres.
8. I feltet Beskrivelse skal du skrive en værdi for at beskrive de transaktioner, der skal bogføres.
9. I feltet Periodefrekvens skal du vælge, hvor ofte transaktionerne skal finde sted.
10. Angiv et tal i feltet Antal forekomster pr. periode.
11. I feltet Bogfør transaktioner skal du vælge, hvornår transaktionerne skal bogføres, f.eks. Månedligt.

