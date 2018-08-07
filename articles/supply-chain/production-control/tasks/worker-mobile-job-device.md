--- 
title: "Konfigurere en arbejder ved hjælp af den mobile jobenhed"
description: "Denne procedure viser, hvordan du tildeler de korrekte roller til brugerkontoen for en arbejder og derefter gør det muligt for arbejderen at foretage shop floor-registreringer."
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: f9de2f79c68fead5ede714ff05bba97118874aad
ms.contentlocale: da-dk
ms.lasthandoff: 02/06/2018

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Konfigurere en arbejder ved hjælp af den mobile jobenhed

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du tildeler de korrekte roller til brugerkontoen for en arbejder og derefter gør det muligt for arbejderen at foretage shop floor-registreringer.


## <a name="assign-roles-to-user-account"></a>Tildele roller til brugerkonto
1. Gå til Systemadministration > Brugere > Brugere.
2. Brug af Quick Filter til at filtrere på navnet på en arbejder, hvor brugerkontoen er tilknyttet rollen Maskinpasser. I eksempeldataene er navnet Shannon.
3. Fremhæv brugerkontoposten.
4. Klik på linket "Navn" i den markerede række på listen for at få vist oplysningerne om brugerkontoen.
5. Vælg Roles\Machine operator i træet.
6. Luk siden med detaljer om brugerkontoen.
7. Luk siden.

## <a name="configure-worker-account"></a>Konfigurer arbejderkonto.
1. Gå til Personale > Arbejdere > Arbejdere.
2. Brug af Quick Filter til at filtrere på navnet på en arbejder, hvor brugerkontoen er tilknyttet rollen Maskinpasser. I eksempeldataene er navnet Shannon.
3. Fremhæv brugerkontoposten.
4. Klik på linket "Navn" i den markerede række på listen for at få vist oplysningerne om brugerkontoen.
5. Klik på fanen Ansættelse.
6. Udvid oversigtspanelet Tidsregistrering, og klik på Aktivér på registreringsterminaler.
7. Klik på Aktivér på registreringsterminaler.
8. Skriv eller vælg en værdi i feltet Beregningsgruppe.
9. Skriv eller vælg en værdi i feltet Standardberegningsgruppe.
10. Indtast eller vælg en værdi i feltet Godkendelsesgruppe.
11. Indtast eller vælg en værdi i feltet Standardprofil.
12. Indtast eller vælg en værdi i feltet Profilgruppe.
13. Klik på OK.
14. Klik på Rediger for at angive et kortnummer for den nye tidsregistreringsarbejder.
15. Skriv en værdi i feltet Kort-id.
16. Klik på Gem.
17. Brug genvejen SaveRecord.
18. Luk siden med detaljer om arbejderen.
19. Luk siden.

## <a name="assign-worker-to-device-group"></a>Tildel arbejder til enhedsgruppe.
1. Gå til Produktionsstyring > Konfiguration > Produktionsudførelse > Konfigurer jobkort for enheder.
2. Klik på Tilføj.
3. Markér den valgte række på listen.
4. Klik på OK.
5. Klik på Rediger.
6. Du kan angive standardfilteret for arbejderen i feltet Produktionsenhed. Dette sikrer, at kun produktionsjob for den valgte produktionsenhed vises, når arbejderen logger på enheden.
7. Luk siden.

