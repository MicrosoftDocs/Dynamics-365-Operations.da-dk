--- 
title: "Tilføje en eksisterende aktivitet til en produktionsflowversion"
description: "Når du opretter nye versioner af produktionsflow, kan du vælge at føje aktiviteter, der er oprettet for de ældre versioner, til den nye version."
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a74fb34db71ba4b539c1b6ede361329aaeb94920
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a>Tilføje en eksisterende aktivitet til en produktionsflowversion

[!include [task guide banner](../../includes/task-guide-banner.md)]

Når du opretter nye versioner af produktionsflow, kan du vælge at føje aktiviteter, der er oprettet for de ældre versioner, til den nye version. Denne fremgangsmåde viser, hvordan du kan oprette en ny version for et eksisterende produktionsflow uden at kopiere aktiviteterne. I næste trin føjes der en eksisterende aktivitet til den nye version. 

Denne opgave kræver et produktionsflow, hvor version og aktiviteter allerede er oprettet.


## <a name="create-a-new-production-flow-version"></a>Opret en ny version af produktionsflowet
1. Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
4. Klik på Rediger.
5. Markér den valgte række på listen.
6. Angiv dato og klokkeslæt i feltet Udløbsdato.
    * Bemærk, at før du opretter en ny produktionsflowversion, skal du sørge for at kontrollere udløbsdato og klokkeslæt for den aktive version. Den nye version oprettes med en ikrafttrædelsesdato, som opretter knyttes til udløbsdatoen for den valgte version.  
7. Klik på Tilføj.
8. Vælg Nej i feltet Kopier fra version.
    * Vælg Nej for at starte med en tom version, hvis de fleste af aktiviteterne i den kopierede version erstattes af nye aktiviteter. Tilføj de uændrede aktiviteter manuelt i formen Tilføj eksisterende funktion i aktiviteten.  
9. Vælg Nej i feltet Dupliker kanban-regler.
    * Når aktiviteterne ikke kopieres til den nye version, er det ikke muligt at kopiere kanban-reglerne på tidspunktet for oprettelse af den nye version.   I stedet skal du bruge funktionen til udskiftning af kanban-regler senere i formen for kanban-regler til at erstatte kanban-regler i den gamle version af produktionsflowet med kanban-regler, der bruger aktiviteterne i den nye version.  
10. Klik på OK.
11. Find og vælg den ønskede post på listen.

## <a name="add-an-existing-activity"></a>Tilføj en eksisterende aktivitet
1. Klik på Aktiviteter.
2. Klik på Tilføj eksisterende for at åbne dialogboksen.
    * Find og vælg en eksisterende aktivitet, der skal føjes til den nye produktionsflowversion.  Bemærk, at listen viser alle aktiviteter, der er oprettet for denne produktionsflow for alle tidligere versioner af flowet.  
3. Indtast eller vælg en værdi i feltet Aktivitet.
4. Klik på OK.


