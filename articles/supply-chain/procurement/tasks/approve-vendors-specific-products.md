--- 
title: Godkende kreditorer til specifikke produkter
description: "Denne fremgangsmåde viser, hvordan du godkender kreditorer for bestemte produkter."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ffc58d2afe73fa2290e4e73a058d47ffd64b8d54
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="approve-vendors-for-specific-products"></a>Godkende kreditorer til specifikke produkter

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du godkender kreditorer for bestemte produkter. Dette gør det muligt at styre, hvilke kreditorer der kan bruges, når produktet føjes til en indkøbsordre. Du kan bruge denne procedure på demofirmaet USMF eller dine egne data. Denne opgave vil typisk blive udført af en indkøbschef.

1. Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
4. Udvid sektionen Indkøb.
    * Hvis der ingen primær kreditor vises i feltet Kreditor, skal du tilføje denne kreditor som en godkendt kreditor med følgende fremgangsmåde. Noter kreditornummeret ned, hvis der vises et.  
5. Klik på Køb i handlingsruden.
6. Klik på Opsætning.
7. Klik på Tilføj.
8. Indtast eller vælg en værdi i feltet Kreditor.
    * Vælg den godkendte kreditor. Mindst én af linjerne skal vise den primære leverandør, hvis der var en i produktposten. Hvis du tidligere har noteret kreditornummeret ned, kan du vælge det her.  
9. Angiv en dato i feltet Udløb.
    * Vælg en dato, der ligger et par måneder frem.  
10. Klik på Tilføj.
11. Indtast eller vælg en værdi i feltet Kreditor.
12. Angiv en dato i feltet Udløb.
    * Vælg en dato, der er forskellig fra den forrige udløbsdato.  
13. Luk siden.
14. Klik på Godkendte kreditorer.
15. Angiv en dato i feltet Udløb.
    * Denne dato fungerer som et filter, så du kan se, hvem de godkendte leverandører er frem til en bestemt dato.  
16. Luk siden.
17. Klik på Gyldighedsperiode.
18. Angiv en dato i feltet Vis kreditorer, der er udløbet efter.
    * Du kan bruge denne side til at identificere kreditorer, hvor godkendelsesstatussen udløber efter en bestemt dato.  
19. Luk siden.
20. Klik på Rediger.
21. Vælg en indstilling i metodefeltet Godkendt kontrolmetode for kreditorer.
    * I dette felt kan du vælge politikken for, hvad der skal ske, hvis produktet er føjet til en indkøbsordrelinje, hvor kreditoren ikke er en godkendt kreditor.  
22. Klik på Gem.
23. Luk siden.
24. Luk siden.
25. Gå til Indkøb og forsyning > Kreditorer > Kreditor/varerelationer > Godkendt kreditorliste efter vare.
    * Denne side giver dig en oversigt over alle produkter og godkendte kreditorer.  
26. Luk siden.
27. Gå til Indkøb og forsyning > Kreditorer > Alle kreditorer.
    * Du kan også starte fra en kreditor og derefter gå til listen over godkendte produkter for den pågældende kreditorkonto.  
28. Find og vælg den ønskede post på listen.
29. Klik på fanen Indkøb i handlingsruden.
30. Klik på Godkendt kreditorliste efter kreditor.
31. Luk siden.
32. Luk siden.


