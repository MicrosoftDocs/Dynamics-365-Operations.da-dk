---
title: Annullerede indkøbsordrer vises på kladdelisten i arbejdsområdet
description: Annullerede indkøbsordrer vises på kladdelisten i arbejdsområdet til forberedelse af indkøbsordrer
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f1dc23cd7e5b4b99cb7a9440d7d4666d8396511f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475926"
---
# <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-workspace"></a>Annullerede indkøbsordrer vises på kladdelisten i arbejdsområdet

## <a name="symptoms"></a>Symptomer

Når du har annulleret indkøbsordrer, der er i en *Bekræftet* tilstand, vises de annullerede indkøbsordrer stadig på listen over kladdeindkøbsordrer i arbejdsområdet **Forberedelse af indkøbsordre**.

## <a name="resolution"></a>Løsning

Dette problem opstår kun ved indkøbsordrer, der er omfattet af en ændringsstyring. Det sker, fordi annulleringen betragtes som en ændring, der skal godkendes. Godkendelsen kan foretages automatisk af systemet. Derfor er processen at sende den annullerede indkøbsordre til godkendelsesarbejdsgangen, så den kan gå til en *Godkendt* tilstand. På dette tidspunkt vises indkøbsordren ikke længere på listen over kladdeindkøbsordrer i arbejdsområdet **Forberedelse af indkøbsordre**.
