---
title: Konfigurere stillinger
description: Stillinger er et vigtigt element i et organisationshierarkis lavere niveau.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, HcmWorkforceWorkspace, HcmWorkerActivityChart, HcmAllWorkersListPart, HcmPosition, HcmPositionNewPosition, HcmJobLookup, HcmPositionReportsToDialog, HcmPositionLookup, FinancialDimensionDefaultTemplatesLookup, DimensionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4fd355fb6c3d2742e046a616585ca349c623341d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190252"
---
# <a name="set-up-positions"></a>Konfigurere stillinger

[!include [task guide banner](../../includes/task-guide-banner.md)]

Stillinger er et vigtigt element i et organisationshierarkis lavere niveau. En stilling er en individuel forekomst af et job. For eksempel er stillingen "Salgschef (øst)" én af de stillinger, der er tilknyttet jobbet "Salgschef". En stilling findes i en afdeling og har muligvis kun én tilknyttet arbejder. I denne opgave vil vi gennemgå de trin, der kræves for at oprette en stilling. Denne procedure er beregnet til personalespecialister.

1. Klik på Styring af arbejdskraft.
2. Klik på Ledige stillinger.
3. Klik på Ny for at åbne dialogboksen Fjern.
4. Indtast eller vælg en værdi i feltet Job.
    * Denne jobbeskrivelse, titel og ansættelsesfaktor svarende til fuld tid bliver automatisk kopieret fra det valgte job til stillingen.  
5. ResolveChanges-jobbet.
6. Klik på Opret stilling.
7. Indtast eller vælg en værdi i feltet Afdeling.
8. Indtast eller vælg en værdi i feltet Stilling.
9. Indtast eller vælg en værdi i feltet Kompensationsområde.
    * Feltet Kompensationsområde bestemmer reglerne for kompensationsberettigelse og budgetter med fast stigning, der gælder for en medarbejder i den pågældende stilling.  
10. Indtast en dato og et klokkeslæt i feltet Tilgængelig for tildeling.
11. Udvid sektionen Stillings varighed.
    * Stillingens varighed angives som standard ud fra de aktiverings- og pensioneringsdatoer, der er angivet tidligere  
12. Udvid sektionen Rapporterer til stilling.
    * Når du tildeler en medarbejder til en stilling, der refererer til en anden stilling, opretter du en direkte rapporteringsrelation mellem de arbejdere, der er tildelt til to stillinger.  
13. Klik på Ny for at åbne dialogboksen Fjern.
14. Indtast eller vælg en værdi i feltet Rapportér til.
15. Klik på Opret.
16. Udvid sektionen Medarbejdertildeling.
17. Udvid eller skjul sektionen Relationer.
    * Hvis organisationen bruger et matrixhierarki eller et andet brugerdefineret hierarki, kan du konfigurere stillingshierarkityper og derefter tilføje rapporteringsforhold for hver enkelt hierarki, du har angivet.  
18. Klik på Tilføj.
19. Markér den valgte række på listen.
20. Indtast eller vælg en værdi i feltet Hierarkinavn.
21. Indtast eller vælg en værdi i feltet Rapporterer til stilling.
22. Udvid sektionen Lønningsliste.
23. Indtast eller vælg en værdi i feltet Betalingscyklus.
24. Indtast eller vælg en værdi i feltet Betalt af.
25. Indtast et tal i feltet Normaltimer på årsbasis.
    * Dette det faste antal betalte timer, som arbejderen i denne stilling forventes at arbejde hvert år.  
26. Udvid sektionen Fagforening.
27. Skjul sektionen Fagforening.
28. Udvid sektionen Økonomiske dimensioner.
29. Indtast eller vælg en værdi i feltet Distributionsskabelon.
30. Indtast eller vælg en værdi i feltet Afdeling.
31. Klik på Gem.
