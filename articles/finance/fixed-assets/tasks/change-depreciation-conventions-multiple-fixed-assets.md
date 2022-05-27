---
title: Ændre afskrivningsprincipper for flere anlægsaktiver
description: Denne opgave opdaterer afskrivningsprincippet for en angivet gruppe anlægsaktiver.
author: moaamer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31d499f55652377b91dd6ef9d3ece13806fbcee3
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710523"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a>Ændre afskrivningsprincipper for flere anlægsaktiver

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
