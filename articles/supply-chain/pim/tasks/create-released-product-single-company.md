---
title: Oprette et frigivet produkt for et enkelt firma
description: Denne fremgangsmåde beskriver, hvordan du opretter et enkelt frigivet produkt inden for rammerne af en enkelt juridisk enhed.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 371157aee389694d349ec4fe51af0d9bfbf08cb7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213241"
---
# <a name="create-a-released-product-for-a-single-company"></a>Oprette et frigivet produkt for et enkelt firma

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde beskriver, hvordan du opretter et enkelt frigivet produkt inden for rammerne af en enkelt juridisk enhed. Når et frigivet produkt er oprettet, er det umiddelbart kun tilgængelig i denne enhed. Du kan gennemgå denne procedure i USMF-demodatafirmaet. Denne opgave udføres normalt af en produktdesigner.


## <a name="create-a-released-product"></a>Opret et frigivet produkt
1. Gå til Frigivne produkter.
2. Klik på Ny.
3. Skriv en værdi i feltet Produktnummer.
    * Hvis der ikke automatisk er angivet et produktnummer i feltet Produktnummer, skal du skrive et entydigt produktnummer. Dette trin er kun påkrævet, hvis der ikke er oprettet nogen nummerserie for produktnumre.  
4. Angiv en værdi i feltet Produktnavn.
    * Produktets navn angives som standard til søgenavnet. Hvis det er nødvendigt, kan du vælge for at ændre søgenavnet.  
5. Klik på rullelisten i feltet Varemodelgruppe for at åbne opslaget.
    * Varemodelgrupper indeholder indstillinger, der bestemmer, hvordan varerne kontrolleres og håndteres i forbindelse med varetilgang og vareafgang. Indstillingerne bestemmer også beregningen af vareforbrug.  
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.
8. Klik på rullelisten i feltet Varegruppe for at åbne opslaget.
    * Varegrupper bruges til at styre lagerbeholdningen, fordi lagervarerne kan deles op i grupper med fælles karakteristiske træk. Hvis du f.eks. vil styre, hvordan oplysninger bogføres på hovedkonti, kan du oprette en række forskellige varegrupper, der er tilknyttet bestemte hovedkonti. På denne måde kan du spore lagerværdien af varer på forskellige stadier.  
9. Find og vælg den ønskede post på listen.
10. Klik op linket i den valgte række på listen.
11. Klik på rullelisten i feltet Lagringsdimensionsgruppe for at åbne opslaget.
    * Lagringsdimensionerne gør det lettere at styre, hvordan varer opbevares og plukkes på lageret. For eksempel kan en lagringsdimension være Sted og Lagersted.  
12. Find og vælg den ønskede post på listen.
13. Klik op linket i den valgte række på listen.
14. Klik på rullelisten i feltet Sporingsdimensionsgruppe for at åbne opslaget.
    * Sporingsdimensionsgruppen bestemmer, hvilke sporingsdimensioner du kan føje til et produkt. For eksempel bruges batchnummeret og serienummeret til at spore lagervarer.  
15. Find og vælg den ønskede post på listen.
16. Klik op linket i den valgte række på listen.
17. Klik på rullelisten i feltet Lagerenhed for at åbne opslaget.
    * Lagerenheden bestemmer, hvordan produktet skal kvantificeres, når det opbevares på lager.  
18. Find og vælg den ønskede post på listen.
19. Klik op linket i den valgte række på listen.
20. Klik på rullelisten i feltet Købsenhed for at åbne opslaget.
    * Købsenheden bestemmer, hvordan produktet kvantificeres, når det er købt hos en kreditor.  
21. Find og vælg den ønskede post på listen.
22. Klik op linket i den valgte række på listen.
23. Klik på rullelisten i feltet Salgsenhed for at åbne opslaget.
    * Salgsenheden bestemmer, hvordan produktet kvantificeres, når det sælges til en debitor.  
24. Find og vælg den ønskede post på listen.
25. Klik op linket i den valgte række på listen.
26. Klik på rullelisten i feltet Styklisteenhed for at åbne opslaget.
    * Styklisteenheden bestemmer, hvordan produktet kvantificeres, når det inkluderes på en stykliste.  
27. Find og vælg den ønskede post på listen.
28. Klik op linket i den valgte række på listen.
29. Klik på rullelisten i feltet Varemomsgruppe for at åbne opslaget.
    * Varemomsgruppen i gruppen Salgsskat bestemmer, hvordan momsen beregnes for hver vare.  
30. Find og vælg den ønskede post på listen.
31. Klik op linket i den valgte række på listen.
32. Klik på rullelisten i feltet Varemomsgruppe for at åbne opslaget.
    * Varemomsgruppen i gruppen Indkøbsskat bestemmer, hvordan købsmomsen beregnes for hver vare.  
33. Find og vælg den ønskede post på listen.
34. Klik op linket i den valgte række på listen.
35. Klik på OK.

## <a name="add-product-characteristics"></a>Tilføj produktegenskaber
1. Vis eller skjul sektionen Administrer lager.
2. Angiv et tal i feltet Nettovægt.
3. Angiv et tal i feltet Taravægt.
4. Angiv et tal i feltet Bruttodybde.
5. Angiv et tal i feltet Bruttobredde.
6. Angiv et tal i feltet Bruttohøjde.
7. Angiv et tal i feltet Volumen.

## <a name="add-financial-dimensions"></a>Tilføj økonomiske dimensioner
1. Udvid eller skjul sektionen Økonomiske dimensioner.
2. Klik på rullelisten i feltet BusinessUnit for at åbne opslaget.
3. Find og vælg den ønskede post på listen.
4. Klik op linket i den valgte række på listen.
5. Klik på rullelisten i feltet CostCenter for at åbne opslaget.
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.
8. Klik på rullelisten i feltet Afdeling for at åbne opslaget.
9. Find og vælg den ønskede post på listen.
10. Klik op linket i den valgte række på listen.
11. Klik på rullelisten i feltet Varegruppe for at åbne opslaget.
12. Find og vælg den ønskede post på listen.
13. Klik op linket i den valgte række på listen.

