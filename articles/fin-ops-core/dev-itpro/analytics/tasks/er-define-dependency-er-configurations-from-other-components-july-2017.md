---
title: Definere afhængigheden af ER-konfigurationer for andre komponenter
description: I dette emne beskrives, hvordan du designer en ER-konfiguration (elektronisk rapportering), og angiver dens afhængighed af andre softwarekomponenter.
author: NickSelin
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd9516ac68c46649ebc50711357b97179bfc1b2c
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092144"
---
# <a name="define-the-dependency-of-er-configurations-on-other-components"></a>Definere afhængigheden af ER-konfigurationer for andre komponenter

[!include [banner](../../includes/banner.md)]

For at fuldføre disse trin skal du først fuldføre trinnene i opgaveguiden ER Administrere konfigurationer for modeltilknytning, og du skal have adgang til Microsoft Dynamics Lifecycle Services (LCS).

Denne procedure viser, hvordan du designer en konfiguration af elektronisk rapportering (ER) og angiver dens afhængighed fra andre softwarekomponenter, så du kan hjælpe med at sikre, at konfigurationen er hentet korrekt til en bestemt version af Finance and Operations, Enterprise Edition. I dette eksempel skal du oprette de krævede ER-konfigurationer for eksempelfirmaet Litware Inc. 

Denne procedure er beregnet til brugere, der har fået tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler. Trinene kan udføres i alle firmaer, fordi ER-konfigurationer deles mellem firmaer. 

1. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
    * Kontroller, at konfigurationstræet indeholder 'Eksempeldatamodel'-konfigurationen og underordnede elementer. Udfør ellers trinnene i opgaveguiden ER Administrere konfigurationer for modeltilknytning, og start derefter denne guide igen.   

## <a name="define-the-dependency-of-er-configurations-from-other-components"></a>Definere afhængigheden af ER-konfigurationer fra andre komponenter
1. Udvid 'Eksempeldatamodel' i træet.
2. Vælg i træet 'Eksempeldatamodel\Eksempeltilknytning'.
    * Vi valgte kladdeversionen af modeltilknytningskonfigurationen 'Eksempeltilknytning'. Vi vil nu definere denne afhængighed fra andre softwarekomponenter. Dette trin betragtes som en forudsætning for at kontrollere overførslen af denne konfigurations version fra et ER-lager og yderligere anvendelse af denne version.   
3. Udvid eller skjul sektionen Forudsætninger.
    * Bemærk, at forudsætningsgruppen 'Implementeringer' er tilføjet automatisk på dette stadie. Denne gruppe indeholder den påkrævede komponent, der refererer til konfigurationen af datamodellen, og hvor implementeringsflaget er slået til. Dette flag angiver, at tilknytningskonfigurationen 'Eksempeltilknytning' betragtes som implementeringen af datamodellen 'Eksempeldatamodel'. Denne komponent tvinger ER til at hente tilknytningskonfigurationen 'Eksempeltilknytning' fra et ER-lager, hver gang modelkonfigurationen 'Eksempeldatamodel' hentes.   
4. Klik på Rediger.
    * En enkelt afhængighed af den aktuelle konfigurationsversion fra en softwarekomponent kan angives ved hjælp af definitionen af komponentens type og enten versionen af komponenten eller et interval af versioner af komponenten.  
    * Ønskede afhængigheder kan grupperes sammen. Når grupperingstypen 'Alle af' er valgt, betragtes afhængighedsbetingelsen for denne gruppe som opfyldt, når hver afhængighedsbetingelse fra denne gruppe og den underordnede gruppe er opfyldt. Når grupperingstypen 'En af' er valgt, betragtes afhængighedsbetingelsen for denne gruppe som opfyldt, når mindst en afhængighedsbetingelse fra denne gruppe er opfyldt.   
5. Klik på Ny.
6. Vælg den nødvendige Produkt-komponent.
7. Vælg Microsoft Dynamics 365 for Operations (1611).
8. Skriv '[7.1.1541.3036,8)' i feltet Version.
    * [7.1.1541.3036,8)  
    * De afhængigheder, du angiver, evalueres, når denne konfiguration hentes fra ethvert ER-lager. Denne konfigurationsversion hentes fra ER-lageret, når version 1 af konfigurationen 'Eksempeldatamodel' enten allerede er på plads eller er hentet på forhånd. Hvis den er hentet på forhånd, skal den være fuldført i Finance and Operations, version 7.1.1541.3036 eller nyere, men ikke nyere end hovedversion 8.   
9. Klik på Gem.
10. Luk siden.
11. Klik på Skift status.
12. Klik på Fuldført.
13. Klik på OK.
14. Vælg i træet 'Eksempeldatamodel\Eksempeltilknytning (alternativ)'.
15. Klik på Rediger.
16. Klik på Ny.
17. Vælg den nødvendige Produkt-komponent.
18. Vælg Microsoft Dynamics AX 7.0 RTW.
19. Skriv '[7.0.1265.3015,7.1)' i feltet Version.
    * [7.0.1265.3015,7.1)  
    * Afhængigheder evalueres, når konfigurationen hentes fra et ER-lager. Denne konfigurationsversion hentes fra ER-lageret, når version 1 af konfigurationen 'Eksempeldatamodel' enten allerede er på plads eller er hentet på forhånd. Hvis den er hentet på forhånd, skal den være fuldført i Microsoft Dynamics 365 for Finance and Operations Enterprise edition, version 7.0.1265.3015 eller nyere, men ikke nyere end mindre version 1.   
20. Klik på Gem.
21. Luk siden.
22. Klik på Skift status.
23. Klik på Fuldført.
24. Klik på OK.

## <a name="configure-the-er-repository"></a>Konfigurere ER-lageret
1. Luk siden.
2. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
    * Åbn listen over ER-lagre for den aktuelle ER-udbyder 'Litware, Inc.'.  
3. Markér den valgte række på listen.
4. Klik på Lagre.
5. Klik på Vis filtre.
6. Angiv filterværdien "LCS" i feltet "Typenavn" ved hjælp af filteroperatoren "indeholder".
    * Du kan springe de resterende trin i denne underopgave over, hvis LCS-lageret allerede er registreret for den aktuelle ER-udbyder. Hvis LCS-lageret ikke allerede er registreret, skal du udføre de resterende trin.   
7. Klik på Tilføj for at åbne dialogboksen.
8. Skriv LCS i feltet Konfigurationslagertype.
9. Klik på Opretlager.
10. Indtast eller vælg en værdi i feltet Projekt.
    * Vælg det ønskede LCS-projekt fra opslaget i feltet 'Projekt'.  
11. Klik på OK.
12. Luk siden.

## <a name="upload-configurations-to-lcs"></a>Overføre konfigurationer til LCS
1. Klik på Rapporteringskonfigurationer.
2. Vælg 'Eksempeldatamodel' i træet.
3. Vælg den færdige version af denne konfiguration.
4. Klik på Skift status.
5. Klik på Del.
6. Klik på OK.
    * Version 1 af denne modelkonfiguration er blevet overført til LCS ved hjælp af det LCS-projekt for ER-lageret, der blev konfigureret tidligere.   
7. Udvid 'Eksempeldatamodel' i træet.
8. Vælg i træet 'Eksempeldatamodel\Eksempeltilknytning'.
9. Vælg den færdige version af denne konfiguration.
10. Klik på Skift status.
11. Klik på Del.
12. Klik på OK.
    * Version 1.1 af denne modeltilknytningskonfiguration er blevet overført til LCS ved hjælp af det LCS-projekt for ER-lageret, der blev konfigureret tidligere.   
13. Vælg i træet 'Eksempeldatamodel\Eksempeltilknytning (alternativ)'.
14. Vælg den færdige version af denne konfiguration.
15. Klik på Skift status.
16. Klik på Del.
17. Klik på OK.
    * Version 1.1 af denne modeltilknytningskonfiguration er blevet overført til LCS ved hjælp af det LCS-projekt for ER-lageret, der blev konfigureret tidligere.   

## <a name="evaluate-er-configuration-dependencies"></a>Evaluere ER-konfigurationsafhængigheder
Vi sletter de oprettede konfigurationer fra systemet og henter dem igen fra LCS-lageret.  
1. Vælg i træet 'Eksempeldatamodel\Eksempeltilknytning'.
2. Klik på Slet.
3. Klik på Ja.
4. Vælg i træet 'Eksempeldatamodel\Eksempeltilknytning (alternativ)'.
5. Klik på Slet.
6. Klik på Ja.
7. Vælg i træet 'Eksempeldatamodel\Eksempelformat'.
8. Klik på Slet.
9. Klik på Ja.
10. Vælg 'Eksempeldatamodel' i træet.
11. Klik på Slet.
12. Klik på Ja.
13. Luk siden.
    * Åbn listen over ER-lagre for den aktuelle ER-udbyder 'Litware, Inc.'.  
14. Klik på Lagre.
15. Klik på Vis filtre.
16. Angiv filterværdien "LCS" i feltet "Typenavn" ved hjælp af filteroperatoren "indeholder".
17. Klik på Åbn.
18. Vælg 'Eksempeldatamodel' i træet.
    * Bemærk, at du kan få vist en vurdering af, om forudgående betingelser er opfyldt for hver version af ER-konfigurationerne for det aktuelle lager. Klik på Kontrollér forudsætninger for at få vist denne evaluering.   
19. Klik på Kontrollér forudsætninger.
20. Klik på Importer.
21. Klik på Ja.
22. Luk siden.
23. Luk siden.
24. Luk siden.
25. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
26. Udvid 'Eksempeldatamodel' i træet.
    * Bemærk, at tilknytningskonfigurationen 'Eksempeltilknytning' for modellen hentes sammen med konfiguration for den valgte datamodel. De to filer hentes sammen, fordi 'Eksempeltilknytning' er konfigureret til at implementere den valgte datamodel, og fordi det er relevant for programmet. Konfigurationen 'Eksempeltilknytning (alternativ)' er ikke hentet, fordi betingelsen for den nødvendige programversion ikke er opfyldt.   
    * Hvis du logger på Finance and Operations, registrerer den samme udbyder, åbner det samme LCS-projekt og henter den samme datamodelkonfiguration, hentes konfigurationen 'Eksempeltilknytning (alternativ)', mens konfigurationen 'Eksempeltilknytning' springes over.  
