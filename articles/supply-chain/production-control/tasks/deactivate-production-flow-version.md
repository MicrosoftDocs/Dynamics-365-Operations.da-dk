---
title: Deaktivere en produktionsflowversion
description: Når en aktiv produktionsflowversion ikke længere er nødvendig, kan den være deaktiveret.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e47cb950ce488d8b6170f829e1fedc664b921a1a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811552"
---
# <a name="deactivate-a-production-flow-version"></a>Deaktivere en produktionsflowversion

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]