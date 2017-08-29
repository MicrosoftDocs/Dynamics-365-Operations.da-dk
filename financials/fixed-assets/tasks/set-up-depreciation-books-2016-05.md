--- 
title: 'Konfigurere afskrivningsmodeller '
description: "Denne opgaveguide opretter en ny afskrivningsmodel og knytter den til en anlægsaktivgruppe."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f8ca9cc59df4eab5a476524e92200687e5979bc9
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-depreciation-books"></a>Konfigurere afskrivningsmodeller  

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide opretter en ny afskrivningsmodel og knytter den til en anlægsaktivgruppe.  Den bruger rollen Revisor og demodata for den juridiske enhed USMF.


## <a name="create-a-depreciation-book"></a>Opret en afskrivningsmodel
1. Gå til Anlægsaktiver > Opsætning > Afskrivningsmodeller.
2. Klik på Ny.
3. Skriv en værdi i feltet Afskrivningsmodel.
4. Skriv en værdi i feltet Beskrivelse.
5. Markér eller fjern markeringen af afkrydsningsfeltet Beregn afskrivning.
6. Klik på rullelisten i feltet Afskrivningsprofil for at åbne opslaget.
7. Find og vælg den ønskede afskrivningsprofil på listen.
8. Klik op linket i den valgte række på listen.
9. Klik på rullelisten i feltet Alternativ afskrivningsprofil for at åbne opslaget.
10. Vælg den ønskede afskrivningsprofil på listen.
11. Klik op linket i den valgte række på listen.
    * Afskrivningsprofilen Ekstraordinær bruges som yderligere afskrivningsmetode for et aktiv under usædvanlige omstændigheder. Du kan f.eks. bruge dette til at registrere afskrivning, der sker som følge af en naturkatastrofe.  
12. Markér eller fjern markeringen af afkrydsningsfeltet Opret reguleringer af afskrivning med basisreguleringer.
13. Klik på rullelisten i feltet Kalender for at åbne opslaget.
14. Klik op linket i den valgte række på listen.

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a>Knyt afskrivningsmodellen til en anlægsaktivgruppe
1. Klik på Anlægsaktivgrupper.
2. Klik på rullelisten i feltet Anlægsaktivgruppe for at åbne opslaget.
3. Find og vælg den ønskede post på listen.
4. Klik op linket i den valgte række på listen.
5. Vælg en indstilling i feltet Afskrivningsprincip.
6. Angiv et tal i feltet Levetid.
    * Bemærk, at værdien i Afskrivningsperioder beregnes efter angivelse af levetid.  


