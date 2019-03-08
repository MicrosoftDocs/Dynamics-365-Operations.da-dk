---
title: Godkende kreditorer til specifikke indkøbskategorier
description: Når en indkøbsrekvisition oprettes, kan det være et krav, at der skal vælges en godkendt eller foretrukken leverandør, afhængigt af hvordan indkøbspolitikkerne er konfigureret.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b783d1ce8f02ad119dc6768e6d9cd3c61ae07e70
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "308385"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>Godkende kreditorer til specifikke indkøbskategorier

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

