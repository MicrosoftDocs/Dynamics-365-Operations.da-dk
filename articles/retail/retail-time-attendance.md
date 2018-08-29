---
title: "Tids- og fremmødestyring i Retail"
description: "Dette emne beskriver de scenarier, der understøttes for styring af tids- og fremmødestyring i Microsoft Dynamics 365 for Retail."
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 21c29c3c37dfacdd98f5c3ec7698f07623da2285
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---

# <a name="time-and-attendance-management-in-retail"></a>Tids- og fremmødestyring i Retail

[!include [banner](includes/banner.md)]

Dette emne beskriver de scenarier, der understøttes for styring af tids- og fremmødestyring i Microsoft Dynamics 365 for Retail. 

<a name="manage-worker-setup-and-scheduling"></a>Administrer arbejderopsætning og -planlægning
----------------------------------

### <a name="initial-configuration"></a>Indledende konfiguration

-   Kør konfigurationsguiden.
-   Registrer arbejdere som arbejdere, der registrerer tid

### <a name="plan-worker-schedules"></a>Planlæg tidsplaner for arbejdere

-   Anvende profiler ved hjælp af arbejdsplanlægningen. Yderligere oplysninger finder du i <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Yderligere oplysninger om konfigurationstrinnene finder du under <https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### <a name="retail-specific-configuration"></a>Detailspecifik konfiguration

-   Aktivér en funktionalitetsprofil til ur, for arbejdere, som du vil aktivere tidsregistreringer for. Klik på **POS-funktionalitetsprofiler** &gt; **Funktioner** &gt; **POS-tidsregistreringer** &gt; **Aktivér tidsregistreringer**.
-   Konfigurer POS-tilladelser for at aktivere tilladelsen Vis tidsursangivelser. Denne tilladelse lader en bruger at se tidsur-registreringer for andre arbejdere i butikken og fra alle de butikker, som brugeren er knyttet til, via adressekartoteket). Det kan være, at du vil aktivere denne tilladelse for en chefrolle, men ikke for en kasseassistentrolle. Klik på **POS-rettighedsgrupper** &gt; **Vis tidsursangivelser**.

## <a name="register-time"></a>Registrer tid
### <a name="cashier-and-non-cashier-time-registrations"></a>Tidsregistreringer for kassereren og andre

-   Om POS:
    -   Komme-handlinger:
        -   Log på med en handling uden pengeskuffe eller et nyt skift.
        -   Vælg en tidsurshandling.
        -   Vælg en ønsket handling:
            -   Komme
            -   Arbejdspause
            -   Frokostpause
            -   Gå

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Aktuel status</th>
    <th>Tilgængelige handlinger</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Komme</td>
    <td><ul>
    <li>Arbejdspause</li>
    <li>Frokostpause</li>
    <li>Gå</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Arbejdspause</td>
    <td>Komme</td>
    </tr>
    <tr class="odd">
    <td>Frokostpause</td>
    <td>Komme</td>
    </tr>
    <tr class="even">
    <td>Gå</td>
    <td>Komme</td>
    </tr>
    </tbody>
    </table>

    [![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)
-   Få vist en bekræftelsesmeddelelse, og kontrollér, at den aktuelle aktivitetstid er korrekt.
-   Logbog:
    -   Klik på **Logbog** for at få vist tidsuraktivitet.
    -   Du kan bruge tidsfiltre til at vælge forskellige tidsvinduer.
    -   Hvis du arbejder i flere butikker på forskellige steder, kan du se dine tidsregistreringer fra alle de butikker, hvor du har registreret tid. Du kan bruge butiksfiltret til at få vist tidsregistreringer fra en valgt butik.

<!-- -->

-   Forskellige tidszoner:
    -   Hvis du får vist tid fra et andet sted (for kasseassistentens logbog eller ved hjælp af **Vis tidsursangivelser** i et chefscenarie), og den placering er i en anden tidszone, konverteres de tidsregistreringer, som du kan se, til din lokale tidszone. Du er f.eks. leder for to butikker, en i Arizona og den anden i Nevada. En kasserer registrerer en mødetid klokken 9:00 i Arizona. På dette tidspunkt er tiden 8.00 om morgenen i Nevada. Hvis du derfor er i Nevada-butikken og ser på tidsregistreringsposter, er tidsregistreringen markeret som 08:00 om morgenen.

## <a name="view-worker-time-registrations"></a>Få vist tidsregistrering for arbejder
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Få vist tidsregistrering for arbejdere, og filtrer efter butik eller aktivitetstype

Om POS:

-   Vælg **Vis tidsursangivelser**.
-   Du kan se tidsursregistreringsaktiviteter fra alle arbejdere, der er tildelt til de samme butikker, du er tilknyttet.
-   Du kan bruge aktivitetstypen og butiksfiltre til at filtrere tidsregistreringer.

## <a name="process-and-manage-time-registrations"></a>Behandl og administrer tidsregistreringer
En Dynamics 365 for Retail-bruger følger arbejdsgangen for at beregne, godkende og overføre tidsregistreringer til løn.

### <a name="primary-operations"></a>Primære handlinger

-   Beregn
-   Godkend
-   Sende til løn

### <a name="other-common-operations"></a>Andre almindelige handlinger

-   Flere udklokninger
-   Registrere fravær

Yderligere oplysninger om, hvordan du behandler tids- og fremmøderegistreringer, finder du under <https://technet.microsoft.com/en-us/library/aa573180.aspx>.




