---
title: Indstillinger for Varetrækprincip på styklistelinjer overholdes ikke
description: Indstillinger for Varetrækprincip på styklistelinjer overholdes ikke.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026373"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a>Indstillinger for Varetrækprincip på styklistelinjer overholdes ikke

KB-nummer: 4612725

## <a name="symptoms"></a>Symptomer

Dette problem opstår, når feltet **Automatisk styklisteforbrug** under fanen **Automatisk opdatering** på siden **Produktionsstyringsparametre** er indstillet til *Varetrækprincip*. Denne indstilling angiver, at alle styklistelinjer automatisk skal forbruges, når der modtages en indkøbsordre. Hvis feltet **Varetrækprincip** på styklistelinjer udtrykkeligt er indstillet til *Manuel*, kan du forvente, at styklistelinjerne ikke forbruges automatisk. Når dette problem opstår, forbruges styklistelinjer, hvor feltet **Varetrækprincip** er indstillet til *Manuel*, dog automatisk.

## <a name="resolution"></a>Løsning

Hvis du ønsker at løse dette problem, kan produktionsstyringsparametrene konfigureres til at overstyre indstillingen af **Varetrækprincip** på styklistelinjer. Kontroller værdien i feltet **Automatisk styklisteforbrug** under fanen **Automatisk opdatering** på siden **Produktionsstyringsparametre**. Hvis indstillingen er *Altid*, ignorerer systemet indstillingen **Varetrækprincip** på alle styklistelinjer og rydder altid linjerne. Hvis systemet skal overholde indstillingen i **Varetrækprincip** på styklistelinjer, skal du ændre værdien i feltet **Automatisk styklisteforbrug** til *Varetrækprincip*.
