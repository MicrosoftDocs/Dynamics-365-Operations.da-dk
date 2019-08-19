---
title: Se kladdeposter eller -posteringer
description: Denne procedure viser, hvordan du kan bruge forespørgsler på bilagstransaktioner til at søge efter kladdeposteringer eller transaktioner.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, LedgerTransVoucher, LedgerTransBase, Originaldocuments
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c93b581e22665b27c1b99503cc91c20ead14ac81
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834678"
---
# <a name="view-journal-entries-or-transactions"></a>Se kladdeposter eller -posteringer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du kan bruge forespørgsler på bilagstransaktioner til at søge efter kladdeposteringer eller transaktioner.

1. Gå til Finans > Forespørgsler og rapporter > Bilagstransaktioner.
2. Vælg det felt, som du vil definere filtreringskriterier for.
3. Angiv dine filtreringskriterier for det markerede felt.
    * Du kan filtrere på en enkelt værdi eller et område. Kontrollér, at den korrekte syntaks bruges, når du definerer et område. Værdierne skal adskilles af en dobbelt punktum (..).  
4. Klik på fanen Joinforbindelser for at tilføje flere tabeller, som skal filtreres.
5. Vælg 'Tabeller\Finanskladdepostering' i træet.
6. Klik på Tilføj tabeljoin.
7. Klik på Annuller, hvis du beslutter, at du ikke vil tilføje en ekstra tabel.
8. Klik på fanen Område.
9. Kør forespørgslen ved at klikke på OK.
10. Klik på Transaktionsoprindelse.
    * Forskellige knapper om gitteret kan bruges til at undersøge flere oplysninger om den valgte post i bilaget. Nogle af knapperne er muligvis ikke tilgængelige, afhængigt af posteringstypen og posteringens egenskaber.  
11. Luk siden.
12. Klik på Originaldokument.
13. Luk siden.

