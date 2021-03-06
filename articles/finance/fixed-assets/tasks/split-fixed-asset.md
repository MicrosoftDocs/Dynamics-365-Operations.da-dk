---
title: Opdele et anlægsaktiv
description: I dette emne beskrives, hvordan du opdeler en procentdel af et anlægskartotek til et nyt anlægskartotek.
author: saraschi2
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa21d5698275ff691ca83d29abd297a796b652d1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823902"
---
# <a name="split-a-fixed-asset"></a>Opdele et anlægsaktiv

[!include [banner](../../includes/banner.md)]

I dette emne beskrives, hvordan du opdeler en procentdel af et anlægskartotek til et nyt anlægskartotek. Den bruger rollen Revisor og USMF demodata.

## <a name="create-a-new-fixed-asset"></a>Opret et nyt anlægsaktiv

1. I navigationsruden skal du gå til **Moduler \> Anlægsaktiver \> Anlægsaktiver \> Anlægsaktiver**.
2. Vælg **Ny**.
3. Skriv eller vælg en værdi i feltet **Anlægsaktivgruppe**. Bemærk nummeret på anlægsaktivet til senere brug i opdelingsprocessen.
4. Angiv en værdi i feltet **Navn**.
5. Luk formularen.

## <a name="split-a-fixed-asset"></a>Opdele et anlægsaktiv

Inden et fuldt afskrevet aktiv opdeles, skal status for aktivbogen ændres manuelt fra **Lukket** til **Åben**. Dette trin er nødvendigt, fordi status for bogen skal være **Åben**, hvis du skal bogføre transaktioner for aktivet (f.eks. til kassationssalg). Du skal også aktivere parameteren **Tillad flere posteringer inden for ét bilag** under fanen **Generelt** på siden **Fiannsparametre**. Når status for anlægskartoteket ændres, og flere posteringer inden for ét bilag er tilladt, skal du udføre følgende trin for at opdele aktivet.

1. På listen skal du finde og vælge linket for det anlægsaktiv, der skal opdeles.
2. Vælg **Bøger**. Vælg det kartotek, der skal opdeles til det nye aktiv.
3. Vælg **Funktioner**.
4. Vælg **Opdel anlægsaktiv**.
5. Skriv eller vælg en værdi i feltet **Til anlægsaktiv**.
6. Vælg rullelisteknappen i feltet **Til bog** for at åbne opslaget.
7. Angiv en dato i feltet **Transaktionsdato**.
8. Angiv et tal i feltet **Procent**.
9. Indtast eller vælg en værdi i feltet **Kladdenavn**.
10. Vælg **OK**.

## <a name="post-the-journal-transaction"></a>Bogfør kladdeposteringen

1. I navigationsruden skal du gå til **Moduler \> Anlægsaktiver \> Kladdeposteringer \> Anlægsaktivkladde**.
2. Vælg på listen den kladde, der er oprettet med opdelingsprocessen.
3. Vælg **Linjer**.

    - Bekræft de oprettede kladdelinjer.
    - Der oprettes en postering til anskaffelsesregulering for det oprindelige aktiv for at formindske værdien af den procentdel, der er angivet under opdelingsprocessen.
    - Der oprettes en anskaffelsespostering for det nye aktiv for det samme beløb.

4. Vælg **Bogfør**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]