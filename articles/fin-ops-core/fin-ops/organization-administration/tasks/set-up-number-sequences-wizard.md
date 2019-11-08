---
title: Oprette nummerserier ved hjælp af en guide
description: I dette emne beskrives, hvordan du konfigurerer alle krævede nummerserier på samme tid ved hjælp af en guide.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f97c4cd6cdb117ebdd67a155478bb6f8d1703541
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177057"
---
# <a name="set-up-number-sequences-using-a-wizard"></a>Oprette nummerserier ved hjælp af en guide

[!include [task guide banner](../../includes/task-guide-banner.md)]

Nummerserier bruges til generering af læselige, entydige id'er for masterdataposter og transaktionsposter, der kræver id'er. En masterdata- eller transaktionspost, der kræver et id, kaldes en reference. Før du kan oprette nye poster til en reference, skal du konfigurere en nummerserie og knytte den til referencen. I dette emne beskrives, hvordan du konfigurerer alle krævede nummerserier på samme tid ved hjælp af en guide. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.

1. Gå til **Navigation > Moduler > Organisationsadministration > Nummerserier > Nummerserier**.
2. Vælg **Generer**.
3. Vælg **Næste**.

   - På denne side kan du redigere identifikationskoden, den laveste værdi og den højeste værdi. Du kan også angive, om nummerserien skal være fortløbende.   
   - Du skal ikke markere indstillingen **Fortløbende**, hvis du skal forudallokere numre til nummerserien. Hvis du vil føje et områdesegment til en nummerseries format, skal du vælge formatet på listen og derefter vælge **Medtager område i format**. Hvis du vil fjerne et områdesegment fra en nummerseries format, skal du vælge formatet på listen og derefter vælge **Fjerner område fra format**. Hvis du vil udelukke en nummerserie fra automatisk generering, skal du vælge nummerserien på listen og derefter vælge **Slet**.  

4. Vælg **Næste**.
5. Vælg **Udfør**.
