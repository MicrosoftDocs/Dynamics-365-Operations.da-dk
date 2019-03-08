---
title: Konfigurer anlægsaktivgrupper
description: Denne procedure viser, hvordan du opretter en ny anlægsaktivgruppe.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48784ef4eb12a4a1cae3387e3a45afdf34f2a0fd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "321794"
---
# <a name="set-up-fixed-asset-groups"></a>Konfigurer anlægsaktivgrupper

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter en ny anlægsaktivgruppe. Den bruger rollen Revisor og demodata for den juridiske enhed USMF.

1. Gå til Anlægsaktiver > Opsætning > Anlægsaktivgrupper.
2. Klik på Ny.
3. Indtast en værdi i feltet Anlægsaktivgruppe.
4. Skriv en værdi i feltet Navn.
    * Autonummerer anlægsaktiver og Nummerseriekode i anlægsaktivgruppen tilsidesætter indstillingerne for parametrene for anlægsaktiver. Du kan ændre den her, hvis aktiver i denne anlægsaktivgruppe får anden nummerering end andre grupper.  
5. Klik på Bøger.
6. Indtast eller vælg en værdi i feltet Bog.
    * Hvis feltet Beregn afskrivning er angivet til Ja, medtages aktivbogen i afskrivningsforslag. Hvis Beregn afskrivning er angivet til Nej, afskrives aktivet ikke automatisk.  
7. Angiv aktivets levetid i år.
    * Bemærk, at værdien i feltet Afskrivningsperioder beregnes efter angivelse af levetid.  
8. Vælg en indstilling i feltet Afskrivningsprincip.
9. Luk siden.

