--- 
title: "Overføre et anlægsaktiv"
description: "Denne opgaveguide overfører de økonomiske oplysninger for en anlægsaktivbog fra et økonomisk dimensionssæt til et nyt økonomisk dimensionssæt."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
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
ms.openlocfilehash: ebde1e8bd8a87b44dd77b9050d05d6c2f4774ef2
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="transfer-a-fixed-asset"></a>Overføre et anlægsaktiv

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide overfører de økonomiske oplysninger for en anlægsaktivbog fra et økonomisk dimensionssæt til et nyt økonomisk dimensionssæt.  Den bruger rollen Revisor og demodata for den juridiske enhed USMF.

1. Gå til Anlægsaktiver > Anlægsaktiver > Anlægsaktiver.
2. På listen skal du finde og vælge det anlægsaktiv, der skal overføres.
3. Klik på Anlægsaktiv i handlingsruden.
4. Klik på Overfør anlægsaktiver.
5. Angiv en dato i feltet Overførselsdato.
6. Angiv kommentarer, der skal beskrive overførslen.
    * Denne liste viser alle bøger for anlægsaktivet.  
7. Marker de bøger, du vil overføre til et nyt økonomisk dimensionssæt.
    * Denne liste viser de eksisterende økonomiske dimensionsværdier for den valgte bog.  
    * Vælg den økonomiske dimension, du vil opdatere for den valgte anlægsaktivbog.  
8. Klik på rullelisten i feltet Økonomisk dimension for at åbne opslaget.
    * Angiv andre økonomiske dimensionsværdier efter behov.  
    * Alle økonomiske dimensionsværdier ændres, når der sker en overførsel, uanset om der er angivet en værdi eller ej. For eksempel hvis du har angivet en værdi for BusinessUnit og ikke har angivet de økonomiske dimensionsværdier CostCenter og afdeling. Hvis din kontostruktur tillader tomme værdier for CostCenter og Afdeling, bør overførslen resultere i, at hver værdimodel har den nye værdi for BusinessUnit og en tom værdi for CostCenter og Afdeling.  
9. Klik på Opdater.
    * Du har mulighed for at se en forhåndsvisning af ændringerne, før overførslen fuldføres.  
    * Gennemgå resultaterne, før du overfører anlægsaktivbøgerne.  
10. Klik på Overførsel.

