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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 33323a8aed44cf19db6c2c937abcb09f7e05b6c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993934"
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