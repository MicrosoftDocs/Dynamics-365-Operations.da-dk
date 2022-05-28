---
title: Overføre et anlægsaktiv
description: Denne opgaveguide overfører de økonomiske oplysninger for en anlægsaktivbog fra et økonomisk dimensionssæt til et nyt økonomisk dimensionssæt.
author: moaamer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c8428467d6e12b6d6af9023980b8cf8738d9294
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726999"
---
# <a name="transfer-a-fixed-asset"></a>Overføre et anlægsaktiv

[!include [banner](../../includes/banner.md)]

Denne opgaveguide overfører de økonomiske oplysninger for en anlægsaktivbog fra et økonomisk dimensionssæt til et nyt økonomisk dimensionssæt.  

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
