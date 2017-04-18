---
title: "Bogføre med afledte bøger"
description: "I denne artikel beskrives det, hvordan afledte bøger bruges."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: ca077727910059878fb16a3f78c5b9133c6c741f
ms.lasthandoff: 03/31/2017


---

# <a name="post-with-derived-books"></a>Bogføre med afledte bøger

I denne artikel beskrives det, hvordan afledte bøger bruges.

Når du bogfører posteringerne for en bog, der indeholder afledte bøger, bogføres posteringerne for den afledte bog automatisk i kladder, indkøbsordrer eller fritekstfakturaer. Men, hvis du forbereder posteringerne for den primære bog i anlægsaktivkladden , kan du se og redigere beløbene for de afledte posteringer, før de bogføres.
-   Visse konti, f.eks. moms og debitor- eller kreditorkonti, opdateres kun én gang af posteringer i den primære bog. De afledte bogposteringer bogføres til de konti, der er defineret for den afledte bog på siden med posteringsprofiler for anlægsaktiver.
-   Anskaffelse bruges ofte som posteringstype for de afledte bøger. Du kan bruge dette, når bogen og den afledte bog skal anvendes på anlægsaktivet fra anlægsaktivets anskaffelsestidspunkt.
-   Der kan også anvendes andre værdier for posteringstypen. Hvis den primære bog og de afledte bøger f.eks. har de samme intervaller mht. salg og kassation, er alle posteringstyperne for anlægsaktiver tilgængelige ved oprettelse af en afledt bog.

> [!WARNING]
> De afskrivninger, der bogføres i den afledte bog, vil have samme beløb som dem, der blev bogført for den primære bog. Hvis afskrivningsmetoderne er forskellige fra bog til bog, bør du ikke generere afskrivningsposteringer ved hjælp af den afledte proces. |

## <a name="example"></a>Eksempel 
I følgende oplysninger kan du finde en beskrivelse af, hvordan du definerer anskaffelsesposteringer med brug af funktionerne til den afledte bog.

1.  Opret bøgerne på siden Bøger.
    -   Regnskabsbogen: VM 1, aktuelt posteringslag
    -   Den skattemæssige bog: VM 2, skatteposteringslag

2.  Klik på fanen Afledte bøger for VM 1. Vælg VM 2 i feltet Bog og Anskaffelse i feltet Posteringstype.

Bøgerne kan derefter tilknyttes bestemte anlægsaktiver. 

Når en anskaffelse bogføres som et anlægsaktiv med bogen VM 1, bogføres anskaffelsen ikke kun for VM 1, men også på den afledte bog VM 2. Status for begge bøger for anlægsaktivet opdateres til åben.

> [!NOTE]                                                                                                         
> Hvis du ikke bruger afledte afledte bøger, skal du bogføre anskaffelsen af anlægsaktivet for både bogen VM 1 og bogen VM 2.

Yderligere oplysninger finder du [afledt bøger](derived-books.md)

