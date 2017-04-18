---
title: "Detailtid og fremmøde"
description: "Dette emne beskriver de scenarier, der understøttes til administration af tid og fremmøde i Microsoft Dynamics 365 for operationer – Retail."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: eac0b85a17df33c860333c5c19d4fb58f160930f
ms.lasthandoff: 03/31/2017


---

# <a name="retail-time-and-attendance"></a>Detailtid og fremmøde

Dette emne beskriver de scenarier, der understøttes til administration af tid og fremmøde i Microsoft Dynamics 365 for operationer – Retail. 

<a name="manage-worker-setup-and-scheduling"></a>Administrere arbejder opsætning og planlægning
----------------------------------

### <a name="initial-configuration"></a>Indledende konfiguration

-   Kør konfigurationsguiden.
-   Registrer arbejdere som arbejdere, der registrerer tid

### <a name="plan-worker-schedules"></a>Planlæg tidsplaner for arbejdere

-   Anvende profiler ved hjælp af arbejdsplanlægningen. Få flere oplysninger under <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Få oplysninger om konfigurationstrinnene under <https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### <a name="retail-specific-configuration"></a>Detailspecifik konfiguration

-   Aktivér en funktionalitetsprofil til ur, for arbejdere, som du vil aktivere tidsregistreringer for. Klik på **POS-funktionalitetsprofiler**&gt;**funktion**&gt;**POS tid registreringer**&gt;**aktivere tidsregistreringer**.
-   Konfigurer POS-tilladelser for at aktivere tilladelsen Vis tidsursangivelser. Denne tilladelse lader en bruger at se tidsur-registreringer for andre arbejdere i butikken og fra alle de butikker, som brugeren er knyttet til, via adressekartoteket). Det kan være, at du vil aktivere denne tilladelse for en chefrolle, men ikke for en kasseassistentrolle. Klik på **POS-rettighedsgrupper**&gt;**se urposter**.

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
    -   Hvis du får vist tid fra et andet sted (for kasseassistentens logbog eller ved hjælp af **Vis tidsursangivelser** i et chefscenarie), og den placering er i en anden tidszone, konverteres de tidsregistreringer, som du kan se, til din lokale tidszone. For eksempel er en leder for to butikker, i Arizona og den anden i Nevada. En kasserer registrerer en mødetid klokken 9:00 I Arizona. På dette tidspunkt er tiden 8.00 om morgenen i Nevada. Hvis du derfor er i Nevada-butikken og ser på tidsregistreringsposter, er tidsregistreringen markeret som 08:00 om morgenen.

## <a name="view-worker-time-registrations"></a>Få vist arbejderregistreringer tid
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Få vist tidsregistrering for arbejdere, og filtrer efter butik eller aktivitetstype

Om POS:

-   Vælg **Vis tidsursangivelser**.
-   Du kan se tidsursregistreringsaktiviteter fra alle arbejdere, der er tildelt til de samme butikker, du er tilknyttet.
-   Du kan bruge aktivitetstypen og butiksfiltre til at filtrere tidsregistreringer.

## <a name="process-and-manage-time-registrations"></a>Behandle og administrere tidsregistreringer
En Dynamics 365 for operationer – Retail bruger følger arbejdsgangen til at beregne, godkende og overføre tidsregistreringer til løn.

### <a name="primary-operations"></a>Primære handlinger

-   Beregn
-   Godkend
-   Sende til løn

### <a name="other-common-operations"></a>Andre almindelige handlinger

-   Flere udklokninger
-   Registrere fravær

Få flere oplysninger om, hvordan du behandler tids- og fremmøderegistreringer, under <https://technet.microsoft.com/en-us/library/aa573180.aspx>.

