---
title: Foretage fejlfinding af delvise frigivelser og delvise forsendelser
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med delvise frigivelser og delvise forsendelser i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5534099f81a97a1dcf4908784fd71dd03cf94eaf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828148"
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