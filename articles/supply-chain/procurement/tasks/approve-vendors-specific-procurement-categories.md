---
title: Godkende kreditorer til specifikke indkøbskategorier
description: Dette emne forklarer, hvordan du kan godkende kreditorer for bestemte indkøbskategorier i Dynamics 365 Supply Chain Management.
author: mkirknel
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e53102d732e9befcaca183adfd2a756c12e0162b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424573"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>Godkende kreditorer til specifikke indkøbskategorier

[!include [banner](../../includes/banner.md)]

Dette emne forklarer, hvordan du kan godkende kreditorer for bestemte indkøbskategorier i Dynamics 365 Supply Chain Management. Når en indkøbsrekvisition oprettes, kan det være et krav, at der skal vælges en godkendt eller foretrukken leverandør, afhængigt af hvordan indkøbspolitikkerne er konfigureret. Denne fremgangsmåde viser, hvordan du kan angive, at en leverandør er godkendt eller foretrukket for en bestemt indkøbskategori. Denne opgave vil normalt udføres af en professionel indkøb. Du kan bruge denne procedure i USMF-demodatafirmaet.

1. Gå i navigationsruden til **Moduler > Indkøb og forsyning > Kreditorer > Alle kreditorer**.
2. Vælg den kreditor, du vil angive som en godkendt eller foretrukken leverandør for en kategori.
3. Vælg **Generelt** i handlingsruden.
4. Vælg **Kategorier**.
5. Vælg **Tilføj kategori**.
6. Vælg **KONTOR OG SKRIVEBORDSTILBEHØR (KONTOR OG SKRIVEBORDSTILBEHØR)** i feltet **Kategori**.
7. Vælg **Foretrukket** i feltet **Status for kreditorkategori**. Det er muligt at angive mere end én foretrukket leverandør til en kategori.  
8. Vælg **Gem**.
9. Gå i navigationsruden til **Moduler > Indkøb og forsyning > Indkøbskategorier**.
10. Vælg **FIRMAS INDKØBSKATEGORIER\KONTOR OG SKRIVEBORDSTILBEHØR** i træet.
11. Udvid sektionen **Kreditorer**. Kontrollér, om den leverandør, du har valgt, vises som en foretrukken leverandør for kategorien Kontor og skrivebordstilbehør. Hvis du kører denne procedure som en opgaveguide, skal du muligvis vælge knappen **Lås op** for at kunne rulle ned til listen over kreditorer.  Det er også muligt at tilføje foretrukne og godkendte leverandører på denne side.  
12. Udvid **KONTOR OG SKRIVEBORDSTILBEHØR** i træet, og vælg **Saks**.
13. Vælg **Nej** i feltet **Arv kreditorer fra overordnet kategori**.
14. Vælg **Ja** i feltet **Arv kreditorer fra overordnet kategori**.

