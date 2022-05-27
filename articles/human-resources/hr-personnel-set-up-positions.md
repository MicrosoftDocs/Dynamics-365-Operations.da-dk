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
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9121df9571b037478fb901cb6ac9f3298177548a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694789"
---
# <a name="set-up-positions"></a>Konfigurere stillinger


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Stillinger er et vigtigt element i et organisationshierarkis lavere niveau. En stilling er en individuel forekomst af et job. For eksempel er stillingen "Salgschef (øst)" én af de stillinger, der er tilknyttet jobbet "Salgschef". En stilling findes i en afdeling og har muligvis kun én tilknyttet arbejder. I denne opgave vil vi gennemgå de trin, der kræves for at oprette en stilling. Denne procedure er beregnet til personalespecialister.

1. Vælg **Styring af arbejdskraft**.
2. Vælg **Ledige stillinger**.
3. Vælg **Ny** for at åbne dialogboksen med rullemenu.
4. Indtast eller vælg en værdi i feltet **Job**.

    Felterne **Jobbeskrivelse**, **Titel** og **Ansættelsesfaktor svarende til fuld tid** bliver automatisk kopieret fra det valgte job til stillingen.

5. Vælg **Opret stilling**.
6. Indtast eller vælg en værdi i feltet **Afdeling**.
7. Indtast eller vælg en værdi i feltet **Stillingstype**.
8. Indtast eller vælg en værdi i feltet **Kompensationsområde**.

    Feltet **Kompensationsområde** bestemmer reglerne for kompensationsberettigelse og budgetter med fast stigning, der gælder for en medarbejder i den pågældende stilling.

9. Indtast en dato og et klokkeslæt i feltet **Tilgængelig for tildeling**.
10. Udvid sektionen **Stillings varighed**.

    Stillingens varighed angives som standard ud fra de aktiverings- og pensioneringsdatoer, der er angivet tidligere.

11. Udvid sektionen **Rapporterer til stilling**.

    Når du tildeler en medarbejder til en stilling, der refererer til en anden stilling, opretter du en direkte rapporteringsrelation mellem de arbejdere, der er tildelt til to stillinger.

12. Vælg **Ny** for at åbne dialogboksen med rullemenu.
13. Indtast eller vælg en værdi i feltet **Rapportér til**.
14. Vælg **Opret**.
15. Udvid sektionen **Medarbejdertildeling**.
16. Udvid sektionen **Relationer**.

    Hvis organisationen bruger et matrixhierarki eller et andet brugerdefineret hierarki, kan du konfigurere stillingshierarkityper og derefter tilføje rapporteringsforhold for hver enkelt hierarki, du har angivet.

17. Vælg **Tilføj**.
18. Markér den valgte række på listen.
19. Indtast eller vælg en værdi i feltet **Hierarkinavn**.
20. Indtast eller vælg en værdi i feltet **Rapporterer til stilling**.
21. Udvid sektionen **Løn**.
22. Indtast eller vælg en værdi i feltet **Betalingscyklus**.
23. Indtast eller vælg en værdi i feltet **Betalt af**.
24. Indtast et tal i feltet **Normaltimer på årsbasis**.

    Den værdi, du indtaster, er faste antal betalte timer, som arbejderen i denne stilling forventes at arbejde hvert år.

25. Udvid sektionen **Fagforening**.
26. Skjul sektionen **Fagforening**.
27. Udvid sektionen **Økonomiske dimensioner**.
28. Indtast eller vælg en værdi i feltet **Distributionsskabelon**.
29. Indtast eller vælg en værdi i feltet **Afdeling**.
30. Vælg **Gem**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
