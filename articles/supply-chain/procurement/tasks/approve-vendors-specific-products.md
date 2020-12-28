---
title: Godkende kreditorer til specifikke produkter
description: Denne fremgangsmåde viser, hvordan du godkender kreditorer for bestemte produkter.
author: mkirknel
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fafa2f7da5575206d452f31bb297790874369dfd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424574"
---
# <a name="approve-vendors-for-specific-products"></a>Godkende kreditorer til specifikke produkter

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du godkender kreditorer for bestemte produkter. Dette gør det muligt at styre, hvilke kreditorer der kan bruges, når produktet føjes til en indkøbsordre. Du kan bruge denne procedure på demofirmaet USMF eller dine egne data. Denne opgave vil typisk blive udført af en indkøbschef.

1. I navigationsruden skal du gå til **Moduler > Administration af produktoplysninger > Produkter > Frigivne produkter**.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
4. Udvid oversigtspanelet **Indkøb**. Hvis der ingen primær kreditor vises i feltet **Kreditor**, skal du tilføje denne kreditor som en godkendt kreditor med følgende fremgangsmåde. Noter kreditornummeret ned, hvis der vises et.  
5. Klik på **Køb** i handlingsruden.
6. Klik på **Konfiguration**.
7. Klik på **Tilføj**.
8. Indtast eller vælg en værdi i feltet Kreditor. Vælg den godkendte kreditor. Mindst én af linjerne skal vise den primære leverandør, hvis der var en i produktposten. Hvis du tidligere har noteret kreditornummeret ned, kan du vælge det her.  
9. Angiv en dato i feltet **Udløb**. Vælg en dato, der ligger et par måneder frem.  
10. Klik på **Tilføj**.
11. Indtast eller vælg en værdi i feltet **Kreditor**.
12. Angiv en dato i feltet **Udløb**. Vælg en dato, der er forskellig fra den forrige udløbsdato.  
13. Luk siden.
14. Klik på **Godkendte kreditorer** i handlingsruden.
15. Angiv en dato i feltet **Udløb**. Denne dato fungerer som et filter, så du kan se, hvem de godkendte leverandører er frem til en bestemt dato.  
16. Luk siden.
17. Klik på **Gyldighedsperiode** i handlingsruden.
18. Angiv en dato i feltet **Vis kreditorer, der er udløbet efter**. Du kan bruge denne side til at identificere kreditorer, hvor godkendelsesstatussen udløber efter en bestemt dato.  
19. Luk siden.
20. Klik på **Rediger**.
21. Vælg en indstilling i feltet **Godkendt kontrolmetode for kreditorer**. I dette felt kan du vælge politikken for, hvad der skal ske, hvis produktet er føjet til en indkøbsordrelinje, hvor kreditoren ikke er en godkendt kreditor.  
22. Klik på **Gem**.
23. Luk siden.
24. Luk siden.
25. Gå i navigationsruden til **Moduler > Indkøb og forsyning > Kreditorer > Leverandør-/varerelationer > Godkendt kreditorliste efter vare**. Denne side giver dig en oversigt over alle produkter og godkendte kreditorer.  
26. Luk siden.
27. Gå i navigationsruden til **Moduler > Indkøb og forsyning > Kreditorer > Alle kreditorer**. Du kan også starte fra en kreditor og derefter gå til listen over godkendte produkter for den pågældende kreditorkonto.  
28. Find og vælg den ønskede post på listen.
29. Klik på fanen **Indkøb** i handlingsruden.
30. Klik på **Godkendt kreditorliste efter kreditor**.
31. Luk siden.
32. Luk siden.

