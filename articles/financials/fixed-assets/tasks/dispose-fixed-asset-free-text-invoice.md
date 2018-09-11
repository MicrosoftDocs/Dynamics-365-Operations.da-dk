--- 
title: "Fjerne et anlægsaktiv ved hjælp af en fritekstfaktura"
description: "Denne procedure viser, hvordan du henter et anlægsaktiv ved hjælp af anskaffelsesforslaget i anlægsaktivkladden."
author: saraschi2
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 24c7721a1e5467e98e6c4d245f1d8e24a973f5aa
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="dispose-of-a-fixed-asset-using-a-free-text-invoice"></a>Fjerne et anlægsaktiv ved hjælp af en fritekstfaktura

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du henter et anlægsaktiv ved hjælp af anskaffelsesforslaget i anlægsaktivkladden. Den bruger rollen Revisor og demodata for den juridiske enhed USMF.

1. Gå til Anlægsaktiver > Kladdepostering > Anlægsaktivkladde.
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Navn.
4. Klik på Linjer.
5. Klik på Forslag.
6. Klik på Anskaffelsesforslag.
7. Klik på Filtrér.
8. Klik på Nulstil for at rydde tidligere værdier.
9. Vælg rækken med anlægsaktivnummeret.
10. Indtast eller vælg en værdi i feltet Kriterier.
    * Angiv de resterende kriterier for anlægsaktiverne, du vil hente med dette forslag.  
11. Klik på OK.
12. Klik på OK.
    * Bekræft de oprettede transaktionslinjer.  
    * Kun anlægsaktiver med anskaffelsesdatoen og anskaffelsesprisen angivet i bogen medtages i anskaffelsesforslaget.  
13. Klik på fanen Bøger.
14. Klik på Bogfør.


