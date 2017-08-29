--- 
title: Deaktivere en produktionsflowversion
description: "Når en aktiv produktionsflowversion ikke længere er nødvendig, kan den være deaktiveret."
author: cvocph
manager: AnnBe
ms.date: 10/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 06daa5e7d2b8e88bca281dc9bcaa73927253553c
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

---
# <a name="deactivate-a-production-flow-version"></a>Deaktivere en produktionsflowversion

[!include[task guide banner](../../includes/task-guide-banner.md)]

Når en aktiv produktionsflowversion ikke længere er nødvendig, kan den være deaktiveret. Du skal kun bruge denne indstilling, hvis alle kanban-regler og aktiviteter er afsluttet og ikke aktiveres igen. Bemærk, at udløbsdatoen for alle kanban-regler, der er relateret til denne version af produktionsflowet, opdateres med dags dato og det aktuelle klokkeslæt. 

Hvis du vil redigere en aktiv produktionsflowversion, kan du overveje at angive en udløbsdato for den aktive version og oprette en ny version. Det gør det muligt at fortsætte dine produktionsoperationer, mens du udarbejder den nye version og relaterede kanban-regler. 

For at få en aktiv produktionsflowversion til at udløbe skal du angive en udløbsdato. Det betyder, at deaktivering er mere en undtagelse end en regel. 

I denne procedure skal du bruge en produktionsflow med en version, der kan deaktiveres. Prøv ikke dette i et produktionsmiljø, medmindre du er 100 % sikker på, at versionen er helt forældet.


## <a name="deactivate-a-production-flow-version"></a>Deaktivere en produktionsflowversion
1. Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
4. Find og vælg den ønskede post på listen.
5. Klik på Deaktiver.
    * Fortsæt ikke, hvis du ikke er 100 % sikker på, at denne version af produktionsflowet er forældet. Hvis du klikker på OK, udløber alle aktive kanban-regler, og alle produktions- og genopfyldningsaktiviteter for denne version af produktionsflowet standser øjeblikkeligt.  
6. Klik på OK.


