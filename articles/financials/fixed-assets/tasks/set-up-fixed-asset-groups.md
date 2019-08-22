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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8f52b73c07aad1047d6e6e7caf80daecc9c26e7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839779"
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

