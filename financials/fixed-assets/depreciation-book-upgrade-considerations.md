---
title: Opgraderingsoversigt for afskrivningsmodel
description: "I tidligere versioner var der to værdiansættelseskoncepter for anlægsaktiver – værdimodeller og afskrivningsmodeller. I Microsoft Dynamics 365 for Operations (1611) opdager er funktionaliteten af værdimodellen og afskrivningsmodellen blevet flettet ind i et enkelt koncept, der er kendt som en bog. Dette emne indeholder nogle overvejelser for opgraderingen."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 116f9e8fbf8ed6ecbd2a1163f17e52ba80061694
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017


---

# <a name="depreciation-book-upgrade-overview"></a>Opgraderingsoversigt for afskrivningsmodel

[!include[banner](../includes/banner.md)]


I tidligere versioner var der to værdiansættelseskoncepter for anlægsaktiver – værdimodeller og afskrivningsmodeller. I Microsoft Dynamics 365 for Operations (1611) opdager er funktionaliteten af værdimodellen og afskrivningsmodellen blevet flettet ind i et enkelt koncept, der er kendt som en bog. Dette emne indeholder nogle overvejelser for opgraderingen. 

Opgraderingsprocessen flytter din eksisterende installation og alle eksisterende transaktioner til den nye modelstruktur. Værdimodeller forbliver, som de er i øjeblikket, som en model, der bogføres i finans. Afskrivningsmodeller flyttes til en model, der har **Bogfør i finans**-indstillingen angivet til **Ingen**. Navne på afskrivningskladder flyttes til et finanskladdenavn med posteringslag angivet til **Ingen**. Posteringer i afskrivningsmodellen skal flyttes til anlægsaktivposter. 

Før du kører dataopgraderingen, bør du forstå de to indstillinger, der er tilgængelige for opgradering af afskrivningens kladdelinjer til transaktionsbilag og den nummerserie, der skal bruges for bilagsserien. 

Mulighed 1: **Systemdefineret nummerserie** - Dette er standardindstillingen for at optimere opgraderingens ydeevne. Opgraderingen bruger ikke nummerseriens struktur, men tildeler i stedet bilag med en sætbaseret tilgang. Efter opgraderingen oprettes den nye nummerserie med **næste nummerserie** korrekt baseret på de opgraderede transaktioner. Som standard bliver nummerserien brugt i FADBUpgr\#\#\#\#\#\#\#\#\# format. Der er nogle parametre til at justere diagrammets format, når du bruger denne fremgangsmåde:

-   **Nummerseriekode** – Koden til identificering af nummerserien. Denne nummerseriekode kan ikke eksistere, da den vil blive oprettet af opgraderingen.
    -   Konstante navn: **NumberSequenceDefaultCode**
    -   Standardværdi: "FADBUpgr"
-   **Præfiks** – Den konstante strengværdi, der skal bruges som præfiks for bilagsnumrene.
    -   Konstante navn: **NumberSequenceDefaultParameterPrefix**
    -   Standardværdi: "FADBUpgr"
-   **Alfanumerisk længde** – Længden af alfanumerisk segment af nummerserien.
    -   Konstante navn: **NumberSequenceDefaultParameterAlpanumericLength **
    -   Standardværdi: 9
-   **Startnummer** - Det første nummer i nummerserien.
    -   Konstante navn: **NumberSequenceDefaultParameterStartNumber **
    -   Standardværdi: 1

Mulighed 2: **Eksisterende brugerdefineret nummerserie** - Denne indstilling giver dig mulighed at definere den nummerserie, der skal bruges til opgraderingen. Overvej at bruge denne indstilling, hvis du har brug for konfiguration af avanceret nummerserie. Hvis du vil bruge en nummerserie, skal du ændre opgradering klassen ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans med følgende oplysninger:

-   **Nummerseriekode** – Koden for nummerserien.
    -   Konstante navn: **NumberSequenceExistingCode **
    -   Standardværdi: ingen standard. Den skal være opdateret til nummerseriekoden.
-   **Delt nummerserie** – En boolesk værdi til at identificere omfanget af nummerserien. Brug "true" for delte nummerserier på tværs af alle virksomheder og "false" for en virksomhedens omfang. Når du bruger "false", skal nummerserien med det angivne navn findes i alle virksomheder, som indeholder afskrivningstransaktioner. Der findes delte nummerserier i hver partition, som indeholder afskrivningstransaktioner.
    -   Konstante navn: **NumberSequenceExistingIsShared **
    -   Standardværdi: true

Parametrene er placeret i begyndelsen af klassen ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans. 

*// Angiv en foretrukken tilgang af bilagsfordeling* 
*// true, hvis du vil bruge en eksisterende nummerseriekode* 
*// false, hvis du vil bruge den systemdefinerede nummerserie (standard)* const boolean NumberSequenceUseExistingCode = false;  

*// Hvis du bruger den systemdefinerede nummerserie, kan du angive parametre for nummerserien.*
*// Der oprettes en ny nummerserie med disse parametre.* const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;   

*// Hvis du bruger eksisterende nummerserie, kan du angive den eksisterende nummerseriekode.* 
*// Bilagsfordeling er række for række for eksisterende nummerserier.* const str NumberSequenceExistingCode = ''; *// Angiv omfanget af den eksisterende nummerseriekode* 
*// true, hvis den angivne nummerserie deles* 
*// false, hvis den angivne nummerserie er pr. virksomhed* 
*// Den systemdefinerede standardnummerserie, der skal bruges, hvis der ikke findes en nummerseriekode med det angivne omfang.* const boolean NumberSequenceExistingIsShared = true; 

Genopbyg det projekt, der indeholder klassen, når konstanterne er blevet ændret. 

Når du bruger den systemgenereret nummerserie (mulighed 1), bruger opgraderingen sætbaseret behandling til at tildele bilagsnumre som angivet i parametrene for opgraderingsscriptet. Der oprettes desuden en ny nummerserie med de angivne parametre efter tildelingen. 

Når du bruger den brugerdefinerede eksisterende nummerserie (mulighed 2), kontrollerer dataopgraderingen, om nummerserien med det angivne omfang findes i databasen for hver partition og virksomhed med afskrivningstransaktioner. Hvis den findes, bruger opgraderingen række for række-behandling ved tildeling af bilagsnumre som angivet af den nummerserie, der bruger strukturen for nummerserier. Hvis nummerserien ikke findes med det angivne omfang, bruger opgraderingen den systemdefinerede standardnummerserie til at fordele bilagsnumrene og opretter en ny nummerserie med angivne standardparametre efter fordelingen.

Scriptet til dataopgradering bruger også nummerserien for begge metoder til feltet **Bilagsserie** på de nye finanskladdenavne, der er oprettet til de tidligere navne på afskrivningskladder.




