---
title: Foreslå anskaffelser af anlægsaktiver
description: I dette emne beskrives, hvordan du henter et anlægsaktiv ved hjælp af anskaffelsesforslaget i Anlægsaktivkladden.
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9259c9bbf52c1c09a7092db6976fc3fabca6601
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990433"
---
# <a name="propose-fixed-asset-acquisitions"></a>Foreslå anskaffelser af anlægsaktiver

[!include [banner](../../includes/banner.md)]

I dette emne beskrives, hvordan du henter et anlægsaktiv ved hjælp af anskaffelsesforslaget i Anlægsaktivkladden. Den bruger rollen Revisor og demodata for den juridiske enhed USMF. Hvis du vil erhverve et anlægsaktiv via en forslagskladde, skal du først oprette anlægsaktivposten og derefter definere anskaffelsesprisen i anlægskartoteket.

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
