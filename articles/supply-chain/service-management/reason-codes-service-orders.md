---
title: Årsagskoder for serviceordrer
description: Brug årsagskoder til at forklare statussen for en serviceordre, når fasen for en serviceordre opdateres.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b059ad5b2ea9cd577624355cf17925cfb9b4867b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258512"
---
# <a name="reason-codes-for-service-orders"></a>Årsagskoder for serviceordrer   

[!include [banner](../includes/banner.md)]


Du kan bruge årsagskoder til at forklare statussen for en serviceordre, når fasen for en serviceordre opdateres. Hvis du eksempelvis annullerer en serviceordre, kan du vælge en årsagskode for annulleringen.

Hvis du vil have vist oplysninger om årsagskoder, der bruges til at spore statussen for serviceordrer, skal du køre rapporten Status for serviceordre. I denne rapport kan du se alle serviceordrer, uanset hvor i processen de befinder sig, og de årsagskoder, der er angivet i forbindelse med opdateringen af et serviceordrestadie.

## <a name="turn-reason-codes-on-or-off"></a>Aktivere og deaktivere årsagskoder

Det er valgfrit, om du vil bruge årsagskoder. Du kan bestemme, om du vil kræve en årsagskode, når du opdaterer en serviceordre til et bestemt servicestadie.

1.  Klik på **Servicestyring** \> **Opsætning** \> **Serviceordrer** \> **Servicestadier**.

2.  I formularen **Servicestadier** skal du vælge et servicestadie, og marker derefter afkrydsningsfeltet **Årsag** for servicestadiet.

3.  Luk formen for at gemme ændringerne.

## <a name="see-also"></a>Se også

[Konfigurer serviceordrestadier](set-up-service-order-stages.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]