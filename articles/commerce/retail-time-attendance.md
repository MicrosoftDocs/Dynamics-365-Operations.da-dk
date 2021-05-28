---
title: Tids- og fremmødestyring i Retail
description: Dette emne beskriver de scenarier, der understøttes for styring af tid og fremmøde i Dynamics 365 Commerce.
author: aamirallaqaband
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7ac7eec69bda7ad2fa41a7311a71a969eddeafb6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021482"
---
# <a name="time-and-attendance-management-in-retail"></a>Tids- og fremmødestyring i Retail

[!include [banner](includes/banner.md)]

Dette emne beskriver de scenarier, der understøttes for styring af tid og fremmøde i Dynamics 365 Commerce.

## <a name="manage-worker-setup-and-scheduling"></a>Administrer arbejderopsætning og -planlægning

### <a name="initial-configuration"></a>Indledende konfiguration

- Kør konfigurationsguiden.
- Registrer arbejdere som arbejdere, der registrerer tid

### <a name="plan-worker-schedules"></a>Planlæg tidsplaner for arbejdere

- Anvende profiler ved hjælp af arbejdsplanlægningen. Du kan finde flere oplysninger om arbejdstidsprofiler i [Anvende profiler ved hjælp af arbejdsplanlægning](/dynamicsax-2012/appuser-itpro/apply-profiles-using-work-planner).

Du kan finde oplysninger om konfigurationstrin under [Opsætning af tid og fremmøde](/dynamicsax-2012/appuser-itpro/setting-up-time-and-attendance).

### <a name="commerce-specific-configuration"></a>Commerce-specifik konfiguration

- Aktivér en funktionalitetsprofil til ur, for arbejdere, som du vil aktivere tidsregistreringer for. Klik på **POS-funktionalitetsprofiler** &gt; **Funktioner** &gt; **POS-tidsregistreringer** &gt; **Aktivér tidsregistreringer**.
- Konfigurer POS-tilladelser for at aktivere tilladelsen Vis tidsursangivelser. Denne tilladelse lader en bruger at se tidsur-registreringer for andre arbejdere i butikken og fra alle de butikker, (som brugeren er knyttet til, via adressekartoteket). Det kan være, at du vil aktivere denne tilladelse for en chefrolle, men ikke for en kasseassistentrolle. Klik på **POS-rettighedsgrupper** &gt; **Vis tidsursangivelser**.

## <a name="register-time"></a>Registrer tid

### <a name="cashier-and-non-cashier-time-registrations"></a>Tidsregistreringer for kassereren og andre

- Om POS:

    - Komme-handlinger:

        - Log på med en handling uden pengeskuffe eller et nyt skift.
        - Vælg en tidsurshandling.
        - Vælg en ønsket handling:

            - Komme
            - Arbejdspause
            - Frokostpause
            - Gå

        <table>
        <thead>
        <tr>
        <th>Aktuel status</th>
        <th>Tilgængelige handlinger</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td>Komme</td>
        <td>
        <ul>
        <li>Arbejdspause</li>
        <li>Frokostpause</li>
        <li>Gå</li>
        </ul>
        </td>
        </tr>
        <tr>
        <td>Arbejdspause</td>
        <td>Komme</td>
        </tr>
        <tr>
        <td>Frokostpause</td>
        <td>Komme</td>
        </tr>
        <tr>
        <td>Gå</td>
        <td>Komme</td>
        </tr>
        </tbody>
        </table>

        [![Tidsurstilstande](./media/timeclockstates.png)](./media/timeclockstates.png)

- Få vist en bekræftelsesmeddelelse, og kontrollér, at den aktuelle aktivitetstid er korrekt.
- Logbog:

    - Klik på **Logbog** for at få vist tidsuraktivitet.
    - Du kan bruge tidsfiltre til at vælge forskellige tidsvinduer.
    - Hvis du arbejder i flere butikker på forskellige steder, kan du se dine tidsregistreringer fra alle de butikker, hvor du har registreret tid. Du kan bruge butiksfiltret til at få vist tidsregistreringer fra en valgt butik.

- Forskellige tidszoner:

    - Hvis du får vist tid fra et andet sted (for kasseassistentens logbog eller ved hjælp af **Vis tidsursangivelser** i et chefscenarie), og den placering er i en anden tidszone, konverteres de tidsregistreringer, som du kan se, til din lokale tidszone. Du er f.eks. leder for to butikker, en i Arizona og den anden i Nevada. En kasserer registrerer en mødetid klokken 9:00 i Arizona. På dette tidspunkt er tiden 8.00 om morgenen i Nevada. Hvis du derfor er i Nevada-butikken og ser på tidsregistreringsposter, er tidsregistreringen markeret som 08:00 om morgenen.

## <a name="view-worker-time-registrations"></a>Få vist tidsregistrering for arbejder

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Få vist tidsregistrering for arbejdere, og filtrer efter butik eller aktivitetstype

Om POS:

- Vælg **Vis tidsursangivelser**.
- Du kan se tidsursregistreringsaktiviteter fra alle arbejdere, der er tildelt til de samme butikker, du er tilknyttet.
- Du kan bruge aktivitetstypen og butiksfiltre til at filtrere tidsregistreringer.

## <a name="process-and-manage-time-registrations"></a>Behandl og administrer tidsregistreringer

En Commerce-bruger følger arbejdsgangen for at beregne, godkende og overføre tidsregistreringer til løn.

### <a name="primary-operations"></a>Primære handlinger

- Beregn
- Godkend
- Sende til løn

### <a name="other-common-operations"></a>Andre almindelige handlinger

- Flere udklokninger
- Registrere fravær

Du kan finde flere oplysninger om, hvordan du behandler registreringer af tid og fremmøde, under [Behandle registreringer af tid og fremmøde](/dynamicsax-2012/appuser-itpro/process-time-and-attendance-registrations).


[!INCLUDE[footer-include](../includes/footer-banner.md)]