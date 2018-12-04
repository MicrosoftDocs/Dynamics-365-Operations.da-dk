--- 
title: "Ændre afskrivningsprincipper for flere anlægsaktiver"
description: "Denne opgave opdaterer afskrivningsprincippet for en angivet gruppe anlægsaktiver."
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0f711d2e18a13ab972e548d3304652dee3f2e406
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a>Ændre afskrivningsprincipper for flere anlægsaktiver

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne opgave opdaterer afskrivningsprincippet for en angivet gruppe anlægsaktiver. Denne opgaveguide anvender demofirmaet USMF.

1. Gå til Anlægsaktiver > Periodiske opgaver > Masseopdatering
2. Klik på rullelisten i feltet Afskrivningsmodel for at åbne opslaget.
3. Klik op linket i den valgte række på listen.
4. Indtast en dato i feltet Placeret først i ydelsen.
5. Indtast en dato i feltet Placeret sidst i ydelsen.
    * Kun aktiver, der er del af den valgte afskrivningsmode, og som er taget i brug mellem disse datoer, opdateres.  
6. Vælg en indstilling i feltet Aktuelt afskrivningsprincip.
    * Kun aktiver, der har det aktuelle afskrivningsprincip, opdateres.  
7. Vælg en indstilling i feltet Nyt afskrivningsprincip.
    * Bekræft, at rapporten udskrives til den ønskede destination.  
8. Udvid posterne for at inkludere sektion.
9. Klik på Filtrér.
10. Vælg Anlægsaktivgruppe på listen.
11. Klik på rullelisten i feltet Kriterier for at åbne opslaget.
12. Vælg den ønskede anlægsaktivgruppe.
13. Klik op linket i den valgte række på listen.
14. Klik på OK.
15. Klik på OK.
    *  Resultaterne af processen vises i rapporten Masseopdatering.     


