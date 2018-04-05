--- 
title: "Overføre en konfiguration til Lifecycle Services til elektronisk rapportering (ER)"
description: "Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny konfiguration af elektronisk rapportering (ER) og overføre den til Microsoft Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3d9c2192bac8477e9c9376aab3e3b561da777569
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---
# <a name="upload-a-configuration-into-lifecycle-services-for-electronic-reporting-er"></a>Overføre en konfiguration til Lifecycle Services til elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny konfiguration af elektronisk rapportering (ER) og overføre den til Microsoft Lifecycle Services (LCS).

I dette eksempel skal du oprette en konfiguration og overføre den til LCS for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i alle virksomheder, da ER-konfigurationer deles af alle firmaer. Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin. Adgang til LCS er også nødvendig for at udføre disse trin.

1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. Vælg "Litware, Inc." og indstil det som aktivt.
3. Klik på Konfigurationer.

## <a name="create-a-new-data-model-configuration"></a>Opret en ny datamodelkonfiguration
1. Klik på Opret konfiguration for at åbne dialogboksen.
    * Du skal oprette en konfiguration, der indeholder en eksempeldatamodel for elektroniske dokumenter. Denne datakonfigurationsmodel overføres senere til LCS.  
2. Skriv 'Eksempelmodelkonfiguration' i feltet Navn.
    * Eksempemodellkonfiguration  
3. Skriv 'Eksempelmodelkonfiguration' i feltet Beskrivelse.
    * Eksempemodellkonfiguration  
4. Klik på Opret konfiguration.
5. Klik på Modeldesigner.
6. Klik på Ny.
7. Skriv 'Indgangspunkt' i feltet Navn.
    * Indgangspunkt  
8. Klik på Tilføj.
9. Klik på Gem.
10. Luk siden.
11. Klik på Skift status.
12. Klik på Fuldført.
13. Klik på OK.

## <a name="register-a-new--repository"></a>Registrere et nyt lager
1. Luk siden.
2. Klik på Lagre.
    * Dette gør det muligt at åbne listen over lagre for konfigurationsudbyderen Litware, Inc.  
3. Klik på Tilføj for at åbne dialogboksen.
    * Her kan du tilføje et nyt lager.  
4. Vælg LCS i feltet Konfigurationslagertype.
5. Klik på Opretlager.
6. Indtast eller vælg en værdi i feltet Projekt.
    * Vælg det ønskede LCS-projekt. Du skal have adgang til projektet.  
7. Klik på OK.
    * Udfyld en ny lagerpost.  
8. Markér den valgte række på listen.
    * Vælg LCS-lagerposten.  
    * Bemærk, at et registreret lager er markeret af den aktuelle udbyder, dvs. at de eneste konfigurationer, der ejes af den pågældende udbyder, kan placeres på dette lager og derfor overføres til det valgte LCS-projekt.  
9. Klik på Åbn.
    * Åbn lageret for at få vist listen over ER-konfigurationer. Den vil være tom, hvis dette projekt endnu ikke er blevet brugt til deling af ER-konfigurationer.  
10. Luk siden.
11. Luk siden.

## <a name="upload-configuration-into-lcs"></a>Overføre konfiguration til LCS
1. Klik på Konfigurationer.
2. Vælg 'Eksempelmodelkonfiguration' i træet.
    * Vælg en oprettet konfiguration, der allerede er fuldført.  
3. Find og vælg den ønskede post på listen.
    * Vælg versionen af den valgte konfiguration med statussen 'Fuldført'.  
4. Klik på Skift status.
5. Klik på Del.
    * Konfigurationens status ændres fra 'Fuldført' til 'Delt', når den er udgivet i LCS.  
6. Klik på OK.
7. Find og vælg den ønskede post på listen.
    * Vælg konfigurationsversionen 'med statussen 'Delt'.  
    * Bemærk, at statussen for den valgte version er ændret fra 'Fuldført' til 'Delt'.  
8. Luk siden.
9. Klik på Lagre.
    * Dette gør det muligt at åbne listen over lagre for konfigurationsudbyderen Litware, Inc.  
10. Klik på Åbn.
    * Vælg LCS-lageret, og åbn det.  
    * Bemærk, at den valgte konfiguration vises som et aktiv for det valgte LCS-projekt.  
    * Åbn LCS ved brug af https://lcs.dynamics.com. Åbn et projekt, der tidligere blev brugt til registrering af lageret, åbn 'Aktivbibliotek' for dette projekt, og udvid indholdet af aktivtypen 'GER-konfiguration' – den overførte ER-konfiguration vil være tilgængelig. Bemærk, at den overførte LCS-konfiguration kan importeres til en anden forekomst af Microsoft Dynamics 365 for Finance and Operations, hvis udbyderne har adgang til dette LCS-projekt.  


