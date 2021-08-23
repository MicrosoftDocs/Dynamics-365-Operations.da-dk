---
title: Foreslå anskaffelser af anlægsaktiver
description: I dette emne beskrives, hvordan du henter et anlægsaktiv ved hjælp af anskaffelsesforslaget i Anlægsaktivkladden.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99202763ae32d02f94f1590783727d4f2cf7a7bbe45963d0e175bfc449b134d9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742923"
---
# <a name="propose-fixed-asset-acquisitions"></a>Foreslå anskaffelser af anlægsaktiver

[!include [banner](../../includes/banner.md)]

I dette emne beskrives, hvordan du henter et anlægsaktiv ved hjælp af anskaffelsesforslaget i Anlægsaktivkladden. Den bruger rollen Revisor og demodata for den juridiske enhed USMF. Hvis du vil erhverve et anlægsaktiv via en forslagskladde, skal du først oprette anlægsaktivposten og derefter definere anskaffelsesprisen i anlægskartoteket.

## <a name="create-an-asset-acquisition-proposal"></a>Oprette et forslag til anskaffelse af aktiver

Gennemfør følgende trin for at oprette et forslag til anskaffelse af et aktiv. 

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
- Bekræft, at transaktionslinjerne er oprettet.  
- Kun anlægsaktiver med anskaffelsesdatoen og anskaffelsesprisen angivet i bogen medtages i anskaffelsesforslaget.  
11. Vælg fanen **Bøger** på siden.
12. Vælg **Bogfør**.

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a>Medtage økonomiske standarddimensioner i et anskaffelsesforslag

Anskaffelsestransaktionen kan oprettes ved hjælp af tilføjelsesprogrammet Excel ved at gå til **Anlægsaktiver > Kladdeposteringer > Anlægsaktivkladde**. Opret en ny kladde, og flyt til sektionen **Linjer** på siden, vælg Excel-ikonet, og vælg derefter en kladdelinje for anlægsaktiver. Systemet opretter og åbner en Excel-skabelon, der repræsenterer kladdelinjer. Du kan føje data til de kladdelinjer, du føjer til skabelonen, og derefter publicere disse oplysninger tilbage i systemet. 

Hvis der er konfigureret standarddimensioner for det valgte anlægskartotek og de tilsvarende anlægsaktiver, der er angivet i Excel-skabelonen, vil de økonomiske standarddimensioner blive kaldt fra masterdata i anlægskartoteket, når kladden publiceres fra Excel til systemet. Hvis der automatisk skal indgå økonomiske dimensioner i et anlægskartotek, når anlægsaktivkladden udgives fra tilføjelsesprogrammet Excel, skal standarddimensionerne være konfigureret på forhånd.  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
