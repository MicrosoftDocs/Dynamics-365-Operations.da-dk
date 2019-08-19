---
title: Oprette afskrivningsmodeller for anlægsaktiver (maj 2016)
description: Denne opgaveguide opretter en ny afskrivningsmodel og knytter den til en anlægsaktivgruppe.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6840e211847494598a81cd3228dbd3796447e18c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839851"
---
# <a name="set-up-depreciation-books-may-2016"></a>Oprette afskrivningsmodeller for anlægsaktiver (maj 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

