---
title: Ordrestatus forbliver Delvist frigivet, også efter at salgsordren er faktureret
description: En salgsordres frigivelsesstatus forbliver Delvist frigivet i nogle tilfælde, selv efter at salgsordren er faktureret. Denne side indeholder en forklaring på og en mulig løsning.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8bfe7ecfd4beb6e77e8dd1e23ccd896d067bdb51
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475914"
---
# <a name="order-status-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Ordrestatus forbliver Delvist frigivet, også efter at salgsordren er faktureret

## <a name="symptoms"></a>Symptomer

En salgsordre er en leveringsordre, men en eller flere varer på den har en anden leveringsmåde. Når ordren er faktureret, har den stadig frigivelsesstatussen *Delvist frigivet*.

En salgsordre har f.eks. to varer: én til levering og én til afhentning. Både levering og afhentning er udført. Derfor er begge linjer faktureret. Frigivelsesstatussen vises dog stadig som *Delvist frigivet*, hvilket er misvisende.

## <a name="workaround"></a>Løsning

Frigivelsesstatussen gælder kun for de ordrelinjer, hvor varerne er aktiveret til Warehouse Management. Derfor forbliver frigivelsesstatus *Delvist frigivet* i dette scenario. Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning. En udvidelse kan tilføjes som en del af følgesedlen og faktureringsprocessen for at opdatere frigivelsesstatussen.
