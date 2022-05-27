---
title: Begrænsninger for en efterkalkulationsversioner for standardkostpriser
description: I dette emne beskrives de begrænsninger, der gælder for en efterkalkulationsversion for standardkostpriser.
author: JennySong-SH
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11bf14b2926fd4ff053697bef8b7dad781948a2c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672200"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Begrænsninger for en efterkalkulationsversioner for standardkostpriser

[!include [banner](../includes/banner.md)]

I dette emne beskrives de begrænsninger, der gælder for en efterkalkulationsversion for standardkostpriser. 

Følgende begrænsninger hjælper med til at sikre, at standardefterkalkulationsprincipperne overholdes:

-  Gebyrer skal inkluderes i varens omkostninger. Gebyrerne for en produceret vare afspejler de amortiserede konstante omkostninger på styklisten og ruteoplysninger. Derfor skal gebyrerne inkluderes i enhedsomkostningen. Gebyrerne for en købt vare medtages også i varens enhedsomkostning.

-  Beregningen af standardkostpriser for produceret varer skal baseres på kostprisposter i en efterkalkulationsversion for standardkostpriser. Der kan kun bruges alternative kostprisdata i en efterkalkulationsversion for planlagte omkostninger, f.eks. indkøbsprisaftaler for købte varer. Alternative kostprisdata defineres af styklisteberegningsgruppen.

-  Styklisteberegninger skal udføres med udfoldning på enkeltniveau.

Oplysninger om varens kostpris for standardkostpriser kan kopieres til andre efterkalkulationsversioner, som indeholder standardkostpriser eller planlagte omkostninger. Oplysninger om varekostpriser for planlagte omkostninger kan dog ikke kopieres til en efterkalkulationsversion, der indeholder standardkostpriser, da den begrænsning, der vises tidligere i dette emne, ikke ville kunne anvendes på planlagte omkostninger.

## <a name="related-topics"></a>Relaterede emner

[Oversigt over efterkalkulationsversioner](costing-versions.md)

[Opdatere standardomkostninger i et ikke-produktionsmiljø](update-standard-costs-non-manufacturing-environment.md)

[Forberede at vedligeholde standardomkostninger for producerede varer](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]