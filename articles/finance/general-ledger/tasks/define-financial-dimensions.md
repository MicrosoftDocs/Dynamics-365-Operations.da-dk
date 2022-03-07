---
title: Definere økonomiske dimensioner
description: Denne opgave vejledning demonstrerer tilføjelse af en enhedsunderstøttet økonomisk dimension og en brugerdefineret økonomisk dimension.
author: aprilolson
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c93a67d0c4a8443eaf40b094770ed6ce29da527b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834446"
---
# <a name="define-financial-dimensions"></a>Definere økonomiske dimensioner

[!include [banner](../../includes/banner.md)]

Denne opgave vejledning demonstrerer tilføjelse af en enhedsunderstøttet økonomisk dimension og en brugerdefineret økonomisk dimension.  Guiden bruger demofirmaet USMF.


## <a name="create-an-entity-backed-financial-dimension"></a>Oprette en enhedsunderstøttet økonomisk dimension
1. Gå til **Navigationsrude > Moduler > Finans > Kontoplan > Dimensioner > Økonomiske dimensioner**.
2. Klik på **Ny**.
3. Vælg en systemdefineret enhed, som den økonomiske dimension skal baseres på, i feltet **Brug værdier fra**. 
4. Skriv en værdi i feltet **Dimensionsnavn** for at beskrive den økonomiske dimension. Navnet kan være anderledes end det systemdefinerede objekt, men det må ikke indeholde mellemrum eller specialtegn.
5. Klik på **Aktiver**. Aktivering af den økonomiske dimension opdaterer tabellen med navnet på den økonomiske dimension og fjerner slettede dimensioner. Du kan angive dimensionsværdier, før du aktiverer en økonomisk dimension, men en økonomisk dimension kan ikke bruges, før den aktiveres.  
6. Klik på **Luk** i aktiveringsmeddelelsen.
7. Klik på **Aktiver**. Dimensionsaktivering kan planlægges til at køre i batch på en bestemt dato og et bestemt klokkelslæt.  
8. Klik på **Dimensionsværdier** i **handlingsruden**. Nogle dimensionsværdier er firmaspecifikke. Du kan kontrollere, om de er firmaspecifikke, hvis firmanavnet vises på listen med dimensionsværdier.  

## <a name="create-a-custom-financial-dimension"></a>Oprette en brugerdefineret økonomisk dimension
1. Luk siden.
2. Klik på **Ny**.
3. Vælg **Brugerdefineret dimension** i feltet **Brug værdier fra**.
4. Skriv en værdi i feltet **Dimensionsnavn** for at beskrive den økonomiske dimension.
    - Navnet må ikke indeholde mellemrum eller specialtegn.  
    - Du kan også angive en kontomaske for at begrænse mængden og typen af oplysninger, som du kan du angive for dimensionsværdier.   
    - Du kan skrive tegn, der forbliver ens for hver dimensionsværdi, f.eks. bogstaver eller en bindestreg. Du kan også angive nummertegn (#) og &-tegn (&) som pladsholdere for bogstaver og tal, som ændres, hver gang der oprettes en dimensionsværdi. Brug et nummertegn (#) som pladsholder for et tal, og tegnet (&) som pladsholder for et bogstav.  Eksempel: Hvis du vil begrænse dimensionsværdien til bogstaverne CC og tre tal, skal du angive CC-### som formatmaske.  
5. Klik på **Aktiver**. Aktivering af den økonomiske dimension opdaterer tabellen med navnet på den økonomiske dimension og fjerner slettede dimensioner. Du kan angive dimensionsværdier, før du aktiverer en økonomisk dimension, men en økonomisk dimension kan ikke bruges, før den aktiveres.     
6. Klik på **Aktiver**. Dimensionsaktivering kan planlægges til at køre i batch på en bestemt dato og et bestemt klokkelslæt.      
7. Klik på **Dimensionsværdier** i **handlingsruden**.
8. Klik på **Ny**.
9. Skriv en værdi i feltet **Dimensionsværdi** for at beskrive din økonomiske dimensionsværdi.
10. Skriv en beskrivelse i feltet **Beskrivelse**, som beskriver din økonomiske dimensionsværdi.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]