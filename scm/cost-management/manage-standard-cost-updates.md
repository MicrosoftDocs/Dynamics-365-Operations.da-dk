---
title: Administrere opdateringer af standardkostpris
description: "Opdateringer af standardkostpris data kan administreres ved hjælp af to forskellige metoder - tilgang med én version og metoden med to versioner."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 7e0f0817ff37c82ed98a51f10bcdde7e785a19a3
ms.lasthandoff: 03/31/2017


---

# <a name="manage-standard-cost-updates"></a>Administrere opdateringer af standardkostpris

Opdateringer af standardkostpris data kan administreres ved hjælp af to forskellige metoder - tilgang med én version og metoden med to versioner. 

Med metoden med én version bruges en enkelt efterkalkulationsversion, der indeholder alle omkostningsposter. Disse poster indeholder de oprindelige omkostninger og alle omkostningsopdateringer.
Med metoden med to versioner bruges én version, der indeholder posterne med de oprindelige omkostninger, og en anden version, der indeholder poster med alle omkostningsopdateringer. En væsentlig fordel ved metoden med to versioner er den klare fremstilling og sporing af omkostningsopdateringer i en særskilt efterkalkulationsversion, uden at den oprindelige efterkalkulationsversion påvirkes. Metoden med to versioner kan bruges til at identificere flere trinvise opdateringer, hvor de enkelte trinvise opdateringer har en særskilt efterkalkulationsversion, der indeholder de trinvise omkostningsposter. **Eksempel** I det følgende eksempel illustreres, hvordan metoderne med én version og to versioner kan bruges til opdatering af standardomkostninger i et produktionsmiljø. Det kan f.eks. være opdateringer, der afspejler nye varer eller fejlrettelser. Det antages, at en enkelt efterkalkulationsversion repræsenterer det aktuelle års standardomkostninger. Id'et for denne version er 2016-STD. Version 2016-STD indeholder de aktuelle aktive omkostninger for alle varer. Derudover indeholder den alle ruterelaterede omkostningskategorier og beregningsformler, som er kendt ved starten af år 2016. 2016-STD er den oprindelige efterkalkulationsversion.
-   **Metoden med én version til opdateringer af omkostningsoplysninger** – I metoden med én version indeholder den oprindelige efterkalkulationsversion 2016-STD alle omkostningsposter. Omkostningsopdateringer registreres i 2016-STD og angives til status "Afventer". De ventende omkostninger kan angives manuelt for nye købte varer, eller de kan beregnes for en produceret vare at afspejle korrektioner. Når der bruges en tilgang med én version, kræver styklisteberegningerne ikke en reservedatakilde, da alle aktive omkostninger findes i efterkalkulationsversionen. Når de ventende omkostninger bliver aktive, indeholder den oprindelige efterkalkulationsversion 2016-STD igen alle de aktuelle aktive omkostninger.
-   **Metoden med to versioner til opdateringer af omkostningsoplysninger** – I metoden med to versioner kræves en ekstra efterkalkulationsversion, der kun indeholder omkostningsopdateringerne. Id'et for denne version er 2016-STD-CHANGES. Omkostningsopdateringer registreres i 2016-STD-CHANGES og angives til statussen "Afventer". Med tilgangen med to versioner kræver styklisteberegningerne for ventende omkostninger for fremstillede varer en reservedatakilde. Det skyldes, at den ekstra efterkalkulationsversion 2016-STD-CHANGES kun indeholder en delmængde af omkostningsoplysninger. Reservedatakilden kan udtrykkes som de aktive omkostninger eller som efterkalkulationsversionen 2016-STD, da begge identificerer kilden til omkostningsoplysninger, når de ikke er medtaget i 2016-STD-CHANGES. Når de ventende omkostninger bliver aktive, indeholder de efterkalkulationsversion 2016-STD-CHANGES de aktuelle aktive omkostninger, der afspejler opdateringerne, mens den oprindelige efterkalkulationsversion 2016-STD ikke påvirkes. Når der bruges en tilgang med to versioner, skal blokeringspolitikker for den oprindelige efterkalkulationsversion konfigureres til at forhindre opdateringer. Der skal angives identiske blokeringspolitikker for den ekstra efterkalkulationsversion med undtagelse af den angivne fra-dato og den særlige brug af blokeringspolitikker, der tillader opdateringer. Den angivne fra-dato skal opdateres sammen med alle ændringsbatch for at afspejle den planlagte aktiveringsdato.

I dette eksempel bruges én ekstra efterkalkulationsversion til administration af opdateringer i hele år 2016. Der kan bruges mere end én ekstra efterkalkulationsversion, f.eks. en separat version til hver opdateringsbatch. Når der bruges mere end én ekstra efterkalkulationsversion, skal reservedatakilden udtrykkes som de aktive omkostninger, da de aktive omkostninger spredes ud over flere efterkalkulationsversioner.



