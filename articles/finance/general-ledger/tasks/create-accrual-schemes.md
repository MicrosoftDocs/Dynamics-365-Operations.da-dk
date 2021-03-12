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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457be741dfd3b44cb963db37857d6a7bceecc14e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994659"
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

