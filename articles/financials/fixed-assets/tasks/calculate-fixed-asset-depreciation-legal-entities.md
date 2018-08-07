--- 
title: "Beregne afskrivning af anlægsaktiver på tværs af juridiske enheder"
description: "Denne fremgangsmåde viser, hvordan du konfigurerer og kører afskrivningsprocessen for flere juridiske enheder."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d804480167414cd038f8229db312dc9c52d131f8
ms.openlocfilehash: 4c45da124136b7fecb916d2ff9098c8ffeff6cb1
ms.contentlocale: da-dk
ms.lasthandoff: 11/02/2017

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Beregne afskrivning af anlægsaktiver på tværs af juridiske enheder

[!include [task guide banner](../../includes/task-guide-banner.md)]

Afskrivning af anlægsaktiver kan køres på tværs af juridiske enheder i et enkelt trin. Denne fremgangsmåde viser, hvordan du konfigurerer og kører processen for flere juridiske enheder. Rollen Bogholder bruges.  

Denne registrering anvender demofirmaet USMF.


Trin (16) underopgave: Konfigurer kladder for kørsel af afskrivning på tværs af virksomheden. 

1. Du skal først oprette de kladder, der skal bruges til kørsel af afskrivning på tværs af virksomheden, i hver juridisk enhed. Gå til Anlægsaktiver > Opsætning > Anlægsaktivparametre. 
2. Udvid sektionen Forslag til anlægsaktiver. 
3. Opret en post med kladdenavnet, der skal bruges for hvert posteringslag i den juridiske enhed. Hvis bøgerne ikke bogfører til Finans, så skal posteringslaget Ingen vælges i den tilknyttede kladde. Klik på Tilføj. 
4. I feltet Posteringslag skal du angive eller vælge en værdi. 
5. Indtast eller vælg en værdi i feltet Kladdenavn. 
6. Gentag kladdeopsætningen på siden med parametre for anlægsaktiver i hver juridisk enhed. 

Underopgave: Beregn afskrivning

1. Brug forslagssiden Opret afskrivning til at starte din afskrivning på tværs af juridiske enheder. Gå til Anlægsaktiver > Kladdeposteringer > Opret afskrivningsforslag. 
2. I feltet Posteringslag skal du angive eller vælge en værdi. 
3. Kladdenavnet dannes som standard fra parametrene for anlægsaktivet. Det kan ændres her for den aktuelle juridiske enhed. 
4. Indtast en dato i feltet Til dato. 
5. Vælg de juridiske enheder, der skal medtages i afskrivningskørslen. Kun juridiske enheder med kladder, der er angivet for anlægsaktivforslag på siden med parametre for anlægsaktiver, vises på listen. 
6. Når den er aktiveret, vil indstillingen Bogfør kladder automatisk bogføre afskrivningskladderne, når de oprettes. Når de ikke er markeret, vil kladderne blive oprettet, men ikke bogført, så du kan gennemgå oplysningerne inden bogføringen. Vælg Ja i feltet Bogfør kladder. 
7. Filtreringsfelterne omfatter alle anlægsaktiver, grupper og bøger for de juridiske enheder, der er valgt for denne kørsel af afskrivning. 
8. Indstillingen for batchbehandling er aktiveret som standard. Når denne indstilling er aktiveret, kører oprettelse og bogføring af afskrivningskladden i baggrunden. 
9. Klik på Opret kladde. 
10. Du skal få vist de afskrivningskladder, der er oprettet i de respektive juridiske enheder. Gå til Anlægsaktiver > Kladdepostering > Anlægsaktivkladde.

