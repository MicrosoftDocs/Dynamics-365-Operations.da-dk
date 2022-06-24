---
title: Oprette nummerserier ved hjælp af en guide
description: Denne artikel beskriver, hvordan du konfigurerer alle krævede nummerserier på samme tid ved hjælp af en guide.
author: SunilGarg
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cae739aad1166eee1abebe3c0adc7939bca55bc4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847057"
---
# <a name="set-up-number-sequences-using-a-wizard"></a>Oprette nummerserier ved hjælp af en guide

[!include [banner](../../includes/banner.md)]

Nummerserier bruges til generering af læselige, entydige id'er for masterdataposter og transaktionsposter, der kræver id'er. En masterdata- eller transaktionspost, der kræver et id, kaldes en reference. Før du kan oprette nye poster til en reference, skal du konfigurere en nummerserie og knytte den til referencen. Denne artikel beskriver, hvordan du konfigurerer alle krævede nummerserier på samme tid ved hjælp af en guide. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.

1. Gå til **Navigation > Moduler > Organisationsadministration > Nummerserier > Nummerserier**.
2. Vælg **Generer**.
3. Vælg **Næste**.

   - På denne side kan du redigere identifikationskoden, den laveste værdi og den højeste værdi. Du kan også angive, om nummerserien skal være fortløbende.   
   - Du skal ikke markere indstillingen **Fortløbende**, hvis du skal forudallokere numre til nummerserien. Hvis du vil føje et områdesegment til en nummerseries format, skal du vælge formatet på listen og derefter vælge **Medtager område i format**. Hvis du vil fjerne et områdesegment fra en nummerseries format, skal du vælge formatet på listen og derefter vælge **Fjerner område fra format**. Hvis du vil udelukke en nummerserie fra automatisk generering, skal du vælge nummerserien på listen og derefter vælge **Slet**.  

4. Vælg **Næste**.
5. Vælg **Udfør**.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
