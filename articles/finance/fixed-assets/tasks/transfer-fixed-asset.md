---
title: Overføre et anlægsaktiv
description: Denne opgaveguide overfører de økonomiske oplysninger for en anlægsaktivbog fra et økonomisk dimensionssæt til et nyt økonomisk dimensionssæt.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 167591cf160916f256e2d10f122eca312ba07639
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186825"
---
# <a name="transfer-a-fixed-asset"></a>Overføre et anlægsaktiv

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide overfører de økonomiske oplysninger for en anlægsaktivbog fra et økonomisk dimensionssæt til et nyt økonomisk dimensionssæt.  Den bruger rollen Revisor og demodata for den juridiske enhed USMF.

1. I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Anlægsaktiver > Anlægsaktiver**.
2. På listen skal du finde og vælge det anlægsaktiv, der skal overføres.
3. Klik på **Anlægsaktiv** i handlingsruden.
4. Klik på **Overfør anlægsaktiver**.
5. Angiv en dato i feltet **Overførselsdato**.
6. Angiv kommentarer, der skal beskrive overførslen.
    
    Denne liste viser alle bøger for anlægsaktivet.  
7. Marker de bøger, du vil overføre til et nyt økonomisk dimensionssæt.
    * Denne liste viser de eksisterende økonomiske dimensionsværdier for den valgte bog.  
    * Vælg den økonomiske dimension, du vil opdatere for den valgte anlægsaktivbog.  
8. Klik på rullelisten i feltet **Økonomisk dimension** for at åbne opslaget.
    * Angiv andre økonomiske dimensionsværdier efter behov.  
    * Alle økonomiske dimensionsværdier ændres, når der sker en overførsel, uanset om der er angivet en værdi eller ej. For eksempel hvis du har angivet en værdi for BusinessUnit og ikke har angivet de økonomiske dimensionsværdier CostCenter og afdeling. Hvis din kontostruktur tillader tomme værdier for CostCenter og Afdeling, bør overførslen resultere i, at hver værdimodel har den nye værdi for BusinessUnit og en tom værdi for CostCenter og Afdeling.  
9. Klik på **Opdater**.
    * Du har mulighed for at se en forhåndsvisning af ændringerne, før overførslen fuldføres.  
    * Gennemgå resultaterne, før du overfører anlægsaktivbøgerne.  
10. Klik på **Overfør**.
