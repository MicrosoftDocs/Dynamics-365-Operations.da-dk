---
title: Oprette periodiseringsskemaer
description: Dette emne forklarer, hvordan du opretter et periodiseringsskema.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
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
ms.openlocfilehash: a83870c4cec4de2e51e90ff1889d4beff6c23f95
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441637"
---
# <a name="create-accrual-schemes"></a>Oprette periodiseringsskemaer

[!include [banner](../../includes/banner.md)]

Dette emne forklarer, hvordan du opretter et periodiseringsskema. Denne opgave bruger demofirmaet USMF.

1. Gå til **Navigationsrude > Moduler > Finans > Konfiguration af kladde > Periodiseringsskemaer**.
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Periodiseringsidentifikation**.
4. Skriv en værdi i feltet **Beskrivelse af periodiseringsskema**.
5. I feltet **Debet** skal du angive de ønskede værdier. Den hovedkonto, der defineres, erstatter debethovedkontoen på kladdebilagslinjen, og det bruges også til tilbageførsel af den udelukkelse, der er baseret på posteringer til periodisering af finans.  
6. I feltet **Kredit** skal du angive de ønskede værdier. Den hovedkonto, der defineres, erstatter kredithovedkontoen på kladdebilagslinjen, og det bruges også til tilbageførsel af den udelukkelse, der er baseret på posteringer til periodisering af finans.  
7. I feltet **Bilag** skal du vælge, hvordan bilaget skal bestemmes, når transaktionerne bogføres.
8. I feltet **Beskrivelse** skal du skrive en værdi for at beskrive de transaktioner, der skal bogføres.
9. I feltet **Periodefrekvens** skal du vælge, hvor ofte transaktionerne skal finde sted.
10. Angiv et tal i feltet **Antal forekomster pr. periode**.
11. I feltet **Bogfør transaktioner** skal du vælge, hvornår transaktionerne skal bogføres, f.eks. **Månedligt**.

