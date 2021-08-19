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
ms.openlocfilehash: ee40eff53efd920ebe43a7b2dd28129f01e6ebb5e75bd480a91f758529f77fc5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716950"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a>Indstillinger for Varetrækprincip på styklistelinjer overholdes ikke

KB-nummer: 4612725

## <a name="symptoms"></a>Symptomer

Dette problem opstår, når feltet **Automatisk styklisteforbrug** under fanen **Automatisk opdatering** på siden **Produktionsstyringsparametre** er indstillet til *Varetrækprincip*. Denne indstilling angiver, at alle styklistelinjer automatisk skal forbruges, når der modtages en indkøbsordre. Hvis feltet **Varetrækprincip** på styklistelinjer udtrykkeligt er indstillet til *Manuel*, kan du forvente, at styklistelinjerne ikke forbruges automatisk. Når dette problem opstår, forbruges styklistelinjer, hvor feltet **Varetrækprincip** er indstillet til *Manuel*, dog automatisk.

## <a name="resolution"></a>Løsning

Hvis du ønsker at løse dette problem, kan produktionsstyringsparametrene konfigureres til at overstyre indstillingen af **Varetrækprincip** på styklistelinjer. Kontroller værdien i feltet **Automatisk styklisteforbrug** under fanen **Automatisk opdatering** på siden **Produktionsstyringsparametre**. Hvis indstillingen er *Altid*, ignorerer systemet indstillingen **Varetrækprincip** på alle styklistelinjer og rydder altid linjerne. Hvis systemet skal overholde indstillingen i **Varetrækprincip** på styklistelinjer, skal du ændre værdien i feltet **Automatisk styklisteforbrug** til *Varetrækprincip*.
