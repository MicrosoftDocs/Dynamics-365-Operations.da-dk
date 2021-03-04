---
title: Anlægsaktiver i den offentlige sektor
description: I denne artikel beskrives de funktioner til anlægsaktiver, der er tilgængelige for den offentlige sektor.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTransfer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 20891
ms.assetid: 552c7969-f044-4774-82ec-080aeae8cf3f
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dd706ca48b718f2737de404c4ae0b25ba7458cf
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407652"
---
# <a name="fixed-assets-in-the-public-sector"></a>Anlægsaktiver i den offentlige sektor

[!include [banner](../includes/banner.md)]

I denne artikel beskrives de funktioner til anlægsaktiver, der er tilgængelige for den offentlige sektor. 

<a name="what-do-i-need-to-know-about-disposing-of-fixed-assets"></a>Værd at vide om salg af anlægsaktiver
-------------------------------------------------------

Offentlige organisationer kan bruge spild og salgsforslag til at råde over mere end et enkelt anlægsaktiv ad gangen.

## <a name="why-do-i-have-to-enter-transfer-from-and-transfer-to-accounts-when-i-transfer-fixed-assets-between-funds"></a>Hvorfor er det nødvendigt at angive Overflyt fra og Overflyt til konti, når jeg overfører anlægsaktiver mellem midler?
Offentlige organisationer kræver typisk afstemte poster for den økonomiske dimension, der bruges til at angive midler. Når du overfører anlægsaktiver mellem midler, og middeldimensionen kræver afstemte poster, er felterne Overflyt fra og Overflyt til-konto på siden til aktivoverførsel påkrævet. 

> [!NOTE] 
> Dette er ikke en egenskab ved anlægsaktiver eller midler. Det er derimod en egenskab for den økonomiske dimension. Når du overfører et anlægsaktiv, og økonomiske dimensioner, som er tilknyttet aktivet, kræver afstemte poster, er Overflyt fra og Overflyt til-konto påkrævet. 

Overflyt fra og Overflyt til-konti er ikke de konti, hvor anlægsaktivets bogførte nettoværdi er indeholdt. Overflyt fra og Overflyt til-kontiene er derimod de hovedkonti, der bruges til at afstemme poster i økonomiske dimensioner. De bruges kun, når en økonomisk dimension for anlægsaktivet kræver afstemning. Overfør fra-kontoen har en debetpost, og overfør til-kontoen har en kreditpost.

Du kan få flere oplysninger i [Midler i den offentlige sektor](funds-public-sector.md).







[!INCLUDE[footer-include](../../includes/footer-banner.md)]