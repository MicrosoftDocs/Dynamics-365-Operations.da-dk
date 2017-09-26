--- 
title: "Godkende kreditorer til specifikke indkøbskategorier"
description: "Når en indkøbsrekvisition oprettes, kan det være et krav, at der skal vælges en godkendt eller foretrukken leverandør, afhængigt af hvordan indkøbspolitikkerne er konfigureret."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 75486202c3fdcaff78a5592389c624d8e21fa969
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="approve-vendors-for-specific-procurement-categories"></a>Godkende kreditorer til specifikke indkøbskategorier

[!include[task guide banner](../../includes/task-guide-banner.md)]

Når en indkøbsrekvisition oprettes, kan det være et krav, at der skal vælges en godkendt eller foretrukken leverandør, afhængigt af hvordan indkøbspolitikkerne er konfigureret. Denne fremgangsmåde viser, hvordan du kan angive, at en leverandør er godkendt eller foretrukket for en bestemt indkøbskategori. Denne opgave vil normalt udføres af en professionel indkøb. Du kan bruge denne procedure i USMF-demodatafirmaet.

1. Gå til Indkøb og forsyning > Kreditorer > Alle kreditorer.
2. Vælg den kreditor, du vil angive som en godkendt eller foretrukken leverandør for en kategori.
3. Klik på Generelt i handlingsruden.
4. Klik på Kategorier.
5. Klik på Tilføj kategori.
6. Vælg KONTOR OG SKRIVEBORDSTILBEHØR (KONTOR OG SKRIVEBORDSTILBEHØR) i feltet Kategori.
7. Vælg 'Foretrukket' i feltet Status for kreditorkategori.
    * Det er muligt at angive mere end én foretrukket leverandør til en kategori.  
8. Klik på Gem.
9. Gå til Indkøb og forsyning > Indkøbskategorier.
10. Vælg 'FIRMAS INDKØBSKATEGORIER\KONTOR OG SKRIVEBORDSTILBEHØR i træet.
11. Vis sektionen Kreditorer.
    * Kontroller, om den leverandør, du har valgt, vises som en foretrukket leverandør for kategorien Kontor og skrivebordstilbehør. Hvis du kører denne procedure som en opgaveguide, skal du muligvis klikke på knappen Lås op for at kunne rulle ned til listen over kreditorer.  Det er også muligt at tilføje foretrukne og godkendte leverandører på denne side.  
12. Udvid 'KONTOR OG SKRIVEBORDSTILBEHØR' i træet.
13. Vælg 'Saks' i træet.
14. Vælg Nej i feltet Arv kreditorer fra overordnet kategori.
15. Vælg Ja i feltet Arv kreditorer fra overordnet kategori.


