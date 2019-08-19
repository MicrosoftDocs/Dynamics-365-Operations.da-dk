---
title: Opdele et anlægsaktiv
description: Denne opgaveguide opdeler en procentdel af et anlægskartotek til et nyt anlægskartotek.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8e5fdc8a7b326daca1fc0f0962c69bb8fb1ff64
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839707"
---
# <a name="split-a-fixed-asset"></a>Opdele et anlægsaktiv

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide opdeler en procentdel af et anlægskartotek til et nyt anlægskartotek.  Den bruger rollen Revisor og USMF demodata.


## <a name="create-a-new-fixed-asset"></a>Opret et nyt anlægsaktiv
1. Gå til Anlægsaktiver > Anlægsaktiver > Anlægsaktiver.
2. Klik på Ny.
3. Skriv eller vælg en værdi i feltet Anlægsaktivgruppe.
4. Bemærk nummeret på anlægsaktivet til senere brug i opdelingsprocessen.
5. Skriv en værdi i feltet Navn.
6. Luk formularen.

## <a name="split-a-fixed-asset"></a>Opdele et anlægsaktiv
1. På listen skal du finde og vælge det anlægsaktiv, der skal opdeles.
2. Klik op linket i den valgte række på listen.
3. Klik på Bøger.
    * Vælg det kartotek, der skal opdeles til det nye aktiv.  
4. Klik på Funktioner.
5. Klik på Opdel anlægsaktiv.
6. Skriv eller vælg en værdi i feltet Til anlægsaktiv.
7. Klik på rullelisten i feltet Til bog for at åbne opslaget.
8. Angiv en dato i feltet Transaktionsdato.
9. Angiv et tal i feltet Procent.
10. Indtast eller vælg en værdi i feltet Kladdenavn.
11. Klik på OK.

## <a name="post-the-journal-transaction"></a>Bogfør kladdeposteringen
1. Gå til Anlægsaktiver > Kladdepostering > Anlægsaktivkladde.
2. Vælg på listen den kladde, der er oprettet med opdelingsprocessen.
3. Klik på Linjer.
    * Bekræft de oprettede kladdelinjer.  Der oprettes en postering til anskaffelsesregulering for det oprindelige aktiv for at formindske værdien af den procentdel, der er angivet under opdelingsprocessen.  Der oprettes en anskaffelsespostering for det nye aktiv for det samme beløb.  
4. Klik på Bogfør.

