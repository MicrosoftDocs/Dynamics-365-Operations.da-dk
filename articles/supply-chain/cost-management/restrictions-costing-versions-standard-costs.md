---
title: Begrænsninger for en efterkalkulationsversioner for standardkostpriser
description: I dette emne beskrives de begrænsninger, der gælder for en efterkalkulationsversion for standardkostpriser.
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2348d7721cd281bb2a1b5af007c98ce69377a412
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424711"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Begrænsninger for en efterkalkulationsversioner for standardkostpriser

[!include [banner](../includes/banner.md)]

I dette emne beskrives de begrænsninger, der gælder for en efterkalkulationsversion for standardkostpriser. 

Følgende begrænsninger hjælper med til at sikre, at standardefterkalkulationsprincipperne overholdes:

-  Gebyrer skal inkluderes i varens omkostninger. Gebyrerne for en produceret vare afspejler de amortiserede konstante omkostninger på styklisten og ruteoplysninger. Derfor skal gebyrerne inkluderes i enhedsomkostningen. Gebyrerne for en købt vare medtages også i varens enhedsomkostning.

-  Beregningen af standardkostpriser for produceret varer skal baseres på kostprisposter i en efterkalkulationsversion for standardkostpriser. Der kan kun bruges alternative kostprisdata i en efterkalkulationsversion for planlagte omkostninger, f.eks. indkøbsprisaftaler for købte varer. Alternative kostprisdata defineres af styklisteberegningsgruppen.

-  Styklisteberegninger skal udføres med udfoldning på enkeltniveau.

Oplysninger om varens kostpris for standardkostpriser kan kopieres til andre efterkalkulationsversioner, som indeholder standardkostpriser eller planlagte omkostninger. Oplysninger om varekostpriser for planlagte omkostninger kan dog ikke kopieres til en efterkalkulationsversion, der indeholder standardkostpriser, da den begrænsning, der vises tidligere i dette emne, ikke ville kunne anvendes på planlagte omkostninger.

<a name="related-topics"></a>Relaterede emner
--------

[Oversigt over efterkalkulationsversioner](costing-versions.md)

[Opdatere standardomkostninger i et ikke-produktionsmiljø](update-standard-costs-non-manufacturing-environment.md)

[Forberede at vedligeholde standardomkostninger for producerede varer](update-standard-costs-manufacturing-environment.md)

