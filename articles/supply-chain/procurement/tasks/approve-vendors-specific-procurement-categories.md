---
title: Godkende kreditorer til specifikke indkøbskategorier
description: Dette emne forklarer, hvordan du kan godkende kreditorer for bestemte indkøbskategorier i Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 887905c35c684f2f60c3ce17eb652532831193cc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812440"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]