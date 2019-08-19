---
title: Foreslå anskaffelser af anlægsaktiver
description: I dette emne beskrives, hvordan du henter et anlægsaktiv ved hjælp af anskaffelsesforslaget i Anlægsaktivkladden.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b35b13dc266fd5bccde437526400832d394b9aa
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839899"
---
# <a name="propose-fixed-asset-acquisitions"></a>Foreslå anskaffelser af anlægsaktiver

[!include [task guide banner](../../includes/task-guide-banner.md)]

I dette emne beskrives, hvordan du henter et anlægsaktiv ved hjælp af anskaffelsesforslaget i Anlægsaktivkladden. Den bruger rollen Revisor og demodata for den juridiske enhed USMF.

1. I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Kladdeposteringer > Anlægsaktivkladde**.
2. Vælg **Ny**.
3. Indtast eller vælg en værdi i feltet **Navn**.
4. Gå til handlingsruden, og vælg **Linjer**.
5. Vælg **Forslag**.
6. Vælg **Anskaffelsesforslag**.
7. Vælg **Filter**. Vælg **Nulstil** for at rydde tidligere værdier.
8. Vælg rækken **Anlægsaktivnummer**.
9. Indtast eller vælg en værdi i feltet **Kriterier**. Angiv de resterende kriterier for anlægsaktiverne, du vil hente med dette forslag.  
10. Vælg **OK** to gange for at forlade ruden.
- Bekræft de oprettede transaktionslinjer.  
- Kun anlægsaktiver med anskaffelsesdatoen og anskaffelsesprisen angivet i bogen medtages i anskaffelsesforslaget.  
11. Vælg fanen **Bøger** på siden.
12. Vælg **Bogfør**.

