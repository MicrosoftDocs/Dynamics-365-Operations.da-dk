---
title: Opgradere oversigt over afskrivning bog
description: "I tidligere versioner var der to værdiansættelse koncepter for anlægsaktiver - værdimodeller og afskrivningsmodeller. I Microsoft Dynamics 365 for Operations version 1611 opdager er funktionaliteten af værdimodellen og afskrivningsmodellen blevet flettet ind i et enkelt koncept, der er kendt som en bog. Dette emne indeholder nogle overvejelser for opgraderingen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: d29cb7bc5acc29be93332b4211adebc4486a7a25
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-book-upgrade-overview"></a>Opgradere oversigt over afskrivning bog

I tidligere versioner var der to værdiansættelse koncepter for anlægsaktiver - værdimodeller og afskrivningsmodeller. I Microsoft Dynamics 365 for Operations version 1611 opdager er funktionaliteten af værdimodellen og afskrivningsmodellen blevet flettet ind i et enkelt koncept, der er kendt som en bog. Dette emne indeholder nogle overvejelser for opgraderingen. 

Opgraderingsprocessen flytter din eksisterende installation og alle eksisterende transaktioner til den nye modelstruktur. Værdimodeller forbliver, som de er i øjeblikket, som en model, der bogføres i finans. Afskrivningsmodeller flyttes til en model, der har **Bogfør i finans**-indstillingen angivet til **Ingen**. Navne på Afskrivningskladder flyttes til et kladdenavn i Finans med det posteringslag, der er angivet til **ingen**. Posteringer i afskrivningsmodellen, der skal flyttes til posteringer for anlægsaktiver. 

Før du kører dataopgraderingen, bør du forstå de to indstillinger, der er tilgængelige for opgradering af afskrivningens kladdelinjer til transaktionsbilag og den nummerserie, der skal bruges for bilagsserien. 

Mulighed 1: **Systemdefineret nummerserie** - Dette er standardindstillingen for at optimere opgraderingens ydeevne. Opgraderingen bruger ikke nummerseriens struktur, men tildeler i stedet bilag med en sætbaseret tilgang. Efter opgraderingen, vil der blive oprettet nye nummerserie med den **næste angivet** korrekt baseret på de opgraderede posteringer. Som standard bliver den nummerserie, der bruges i FADBUpgr\#\#\#\#\#\#\#\#\# format. Der er nogle parametre til at justere diagrammets format, når du bruger denne fremgangsmåde:

-   **Nummerere nummerseriekode** – kode til at identificere den nummerserie. Denne nummerseriekode kan ikke eksistere, da det vil blive oprettet ved opgraderingen.
    -   Konstante navn: **NumberSequenceDefaultCode**
    -   Standardværdi: "FADBUpgr"
-   **Præfiks** – Den konstante strengværdi, der skal bruges som præfiks for bilagsnumrene.
    -   Konstante navn: **NumberSequenceDefaultParameterPrefix**
    -   Standardværdi: "FADBUpgr"
-   **Alfanumerisk længde** – Længden af alfanumerisk segment af nummerserien.
    -   Konstante navn: ** NumberSequenceDefaultParameterAlpanumericLength **
    -   Standardværdi: 9
-   **Startnummer** - Det første nummer i nummerserien.
    -   Konstante navn: ** NumberSequenceDefaultParameterStartNumber **
    -   Standardværdi: 1

Mulighed 2: **eksisterende brugerdefineret nummerserien** -denne indstilling giver dig mulighed at definere den nummerserie, der skal bruges til opgraderingen. Overvej at bruge denne indstilling, hvis du har brug for konfiguration af avancerede nummerserie. Hvis du vil bruge en nummerserie, skal du ændre den opgradering klasse ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans med følgende oplysninger:

-   **Nummerseriekode** – Koden for nummerserien.
    -   Konstante navn: ** NumberSequenceExistingCode **
    -   Standardværdi: ingen standard. Den skal være opdateret til nummerseriekoden.
-   **Delt nummerserie** – En boolesk værdi til at identificere omfanget af nummerserien. Brug "true" for delte nummerserier på tværs af alle virksomheder og "false" for en virksomhedens omfang. Når du bruger "falsk", skal nummerserien med det angivne navn findes i alle virksomheder, som indeholder afskrivningstransaktioner. Der findes delte nummerserier i hver partition, som indeholder afskrivningstransaktioner.
    -   Konstante navn: ** NumberSequenceExistingIsShared **
    -   Standardværdi: true

Parametrene, der er placeret i begyndelsen af ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans-klassen. 

*Angiv en bedre tilgang af bilag fordeling*<ph id="t1">
</ph>*/ / SAND, hvis du vil bruge en eksisterende nummerseriekode*<ph id="t2">
</ph>*/ / FALSK, hvis du vil bruge systemdefineret nummerserien (standard)* konstant boolean NumberSequenceUseExistingCode = false;  

*Hvis bruger tilgang systemdefinerede antallet sekvens, kan du angive parametre for nummerserien. *<ph id="t3">
</ph>*/ / Vil blive oprettet en ny nummerserie med disse parametre.* Konstant str NumberSequenceDefaultCode = 'FADBUpgr' konstant str NumberSequenceDefaultParameterPrefix = 'FADBUpgr' konstant int NumberSequenceDefaultParameterAlpanumericLength = 9; konstant int NumberSequenceDefaultParameterStartNumber = 1;   

*Hvis ved hjælp af de eksisterende tal sekvens fremgangsmåde, kan du angive den eksisterende nummerseriekode. *<ph id="t4">
</ph>*/ / Bilaget fordeling går række for række for eksisterende nummerserier.* Konstant str NumberSequenceExistingCode = ''; */ / Angiver omfanget af den eksisterende nummerseriekode*<ph id="t5">
</ph>*/ / SAND, hvis den angivne nummerserie deles*<ph id="t6">
</ph>*/ / FALSK, hvis den angivne nummerserie er pr. firma*<ph id="t7">
</ph>*/ / de systemdefinerede standardnummerserie, der skal bruges, hvis der ikke findes en nummerseriekode med det angivne område.* const boolean NumberSequenceExistingIsShared = true; 

Genopbyg det projekt, der indeholder klassen, når konstanterne er blevet ændret. 

Når du bruger den systemgenererede nummer sekvens tilgang (mulighed 1), bruger opgraderingen sæt-baseret behandling til at tildele bilagsnumre som angivet i parametrene for opgraderingsscriptet. Der oprettes desuden en ny nummerserie med angivne parametre efter tildelingen. 

Når du bruger den brugerdefinerede eksisterende nummerserie (mulighed 2), kontrollerer dataopgraderingen, om nummerserien med det angivne omfang findes i databasen for hver partition og virksomhed med afskrivningstransaktioner. Hvis den findes, bruger opgraderingen række for række behandling tildeles bilagsnumre som angivet af den nummerserie, der bruger ramme for nummerserier. Hvis nummerserien ikke findes med det angivne område, bruger den standard systemdefinerede tal sekvens tilgang til at allokere bilagsnumrene opgraderingen, og opretter en ny nummerserie med angivne standardparametre efter fordelingen.

Scriptet til dataopgradering bruger også nummerserien for begge metoder til feltet **Bilagsserie** på de nye finanskladdenavne, der er oprettet til de tidligere navne på afskrivningskladder.


