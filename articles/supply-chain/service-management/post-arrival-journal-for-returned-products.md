---
title: Bogføre modtagelseskladde for returnerede produkter
description: Bogføre modtagelseskladde for returnerede produkter.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e07542a369506b810704012bd1b07557b79f50d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424804"
---
# <a name="post-arrival-journal-for-returned-products"></a>Bogføre modtagelseskladde for returnerede produkter 

[!include [banner](../includes/banner.md)]


Hvis du skal behandle varer, der er sendt retur, skal du først kontrollere det returnerede vareantal og opdatere antalsfeltet i varemodtagelseskladden. Derefter skal du vælge en dispositionskode eller angive, at de returnerede varer skal inspiceres. Når du har udført disse trin, kan du bogføre varemodtagelseskladden for returordren.

1.  Klik på **Lagerstyring** \> **Periodisk** \> **Modtagelsesoversigt**.

2.  I filteret **Opsætningsnavn** skal du vælge **Returordre**.

3.  Hvis listen over modtagere er lang, skal du bruge felterne i området **Afgrænsning** til at indsnævre listen.

4.  Find linjen for den returordre, du vil bogføre, markér afkrydsningsfeltet **Vælg til modtagelse** for linjen, og klik derefter på **Start modtagelse**.

5.  Klik på **Kladder** \> **Vis modtagelser fra tilgange** for at åbne formularen **Lokationskladde**.
    

    > [!TIP]
    > <P>Vælg en kladde, og klik derefter på <STRONG>Linjer</STRONG> for at få vist detaljerede oplysninger.</P>


6.  Foretag de nødvendige opdateringer, og klik derefter på **Bogfør**.

Når kladden er bogført, er de returnerede varer registreret i lageret, og det angives i formularen **Returordrer**, at varerne er modtaget på lagerstedet.

## <a name="see-also"></a>Se også

[Lokationskladde (form)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))

  


