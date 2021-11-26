---
title: Konfigurere stillinger
description: I dette emne beskrives, hvorfor stillinger er et vigtigt element i et organisationshierarkis lavere niveau.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, HcmWorkforceWorkspace, HcmWorkerActivityChart, HcmAllWorkersListPart, HcmPosition, HcmPositionNewPosition, HcmJobLookup, HcmPositionReportsToDialog, HcmPositionLookup, FinancialDimensionDefaultTemplatesLookup, DimensionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4b9f09db8465cc55c9b0c4dc403c2c7a3647d7e
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728706"
---
# <a name="set-up-positions"></a>Konfigurere stillinger

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Stillinger er et vigtigt element i et organisationshierarkis lavere niveau. En stilling er en individuel forekomst af et job. For eksempel er stillingen "Salgschef (øst)" én af de stillinger, der er tilknyttet jobbet "Salgschef". En stilling findes i en afdeling og har muligvis kun én tilknyttet arbejder. I denne opgave vil vi gennemgå de trin, der kræves for at oprette en stilling. Denne procedure er beregnet til personalespecialister.

1. Vælg **Styring af arbejdskraft**.
2. Vælg **Ledige stillinger**.
3. Vælg **Ny** for at åbne dialogboksen med rullemenu.
4. Indtast eller vælg en værdi i feltet **Job**.

    Felterne **Jobbeskrivelse**, **Titel** og **Ansættelsesfaktor svarende til fuld tid** bliver automatisk kopieret fra det valgte job til stillingen.

5. ResolveChanges-jobbet.
6. Vælg **Opret stilling**.
7. Indtast eller vælg en værdi i feltet **Afdeling**.
8. Indtast eller vælg en værdi i feltet **Stillingstype**.
9. Indtast eller vælg en værdi i feltet **Kompensationsområde**.

    Feltet **Kompensationsområde** bestemmer reglerne for kompensationsberettigelse og budgetter med fast stigning, der gælder for en medarbejder i den pågældende stilling.

10. Indtast en dato og et klokkeslæt i feltet **Tilgængelig for tildeling**.
11. Udvid sektionen **Stillings varighed**.

    Stillingens varighed angives som standard ud fra de aktiverings- og pensioneringsdatoer, der er angivet tidligere.

12. Udvid sektionen **Rapporterer til stilling**.

    Når du tildeler en medarbejder til en stilling, der refererer til en anden stilling, opretter du en direkte rapporteringsrelation mellem de arbejdere, der er tildelt til to stillinger.

13. Vælg **Ny** for at åbne dialogboksen med rullemenu.
14. Indtast eller vælg en værdi i feltet **Rapportér til**.
15. Vælg **Opret**.
16. Udvid sektionen **Medarbejdertildeling**.
17. Udvid sektionen **Relationer**.

    Hvis organisationen bruger et matrixhierarki eller et andet brugerdefineret hierarki, kan du konfigurere stillingshierarkityper og derefter tilføje rapporteringsforhold for hver enkelt hierarki, du har angivet.

18. Vælg **Tilføj**.
19. Markér den valgte række på listen.
20. Indtast eller vælg en værdi i feltet **Hierarkinavn**.
21. Indtast eller vælg en værdi i feltet **Rapporterer til stilling**.
22. Udvid sektionen **Løn**.
23. Indtast eller vælg en værdi i feltet **Betalingscyklus**.
24. Indtast eller vælg en værdi i feltet **Betalt af**.
25. Indtast et tal i feltet **Normaltimer på årsbasis**.

    Den værdi, du indtaster, er faste antal betalte timer, som arbejderen i denne stilling forventes at arbejde hvert år.

26. Udvid sektionen **Fagforening**.
27. Skjul sektionen **Fagforening**.
28. Udvid sektionen **Økonomiske dimensioner**.
29. Indtast eller vælg en værdi i feltet **Distributionsskabelon**.
30. Indtast eller vælg en værdi i feltet **Afdeling**.
31. Vælg **Gem**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
