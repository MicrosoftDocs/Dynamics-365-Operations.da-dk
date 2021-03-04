---
title: Foretage fejlfinding af delvise frigivelser og delvise forsendelser
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med delvise frigivelser og delvise forsendelser i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e89a430f90374733b23fadaf53f5bab598d67d62
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645942"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a>Foretage fejlfinding af delvise frigivelser og delvise forsendelser

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med delvise frigivelser og delvise forsendelser i Microsoft Dynamics 365 Supply Chain Management.

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>En salgsordres frigivelsesstatus forbliver Delvist frigivet, selv efter at salgsordren er faktureret.

### <a name="issue-description"></a>Problembeskrivelse

En salgsordre er en leveringsordre, men en eller flere varer på den har en anden leveringsmåde. Når ordren er faktureret, har den stadig frigivelsesstatussen *Delvist frigivet*.

En salgsordre har f.eks. to varer: én til levering og én til afhentning. Både levering og afhentning er udført. Derfor er begge linjer faktureret. Frigivelsesstatussen vises dog stadig som *Delvist frigivet*, hvilket er misvisende.

### <a name="issue-resolution"></a>Problemløsning

Frigivelsesstatussen gælder kun for de ordrelinjer, hvor varerne er aktiveret til lokationsstyring. Derfor forbliver frigivelsesstatus *Delvist frigivet* i dette scenario. Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning. En udvidelse kan tilføjes som en del af følgesedlen og faktureringsprocessen for at opdatere frigivelsesstatussen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]