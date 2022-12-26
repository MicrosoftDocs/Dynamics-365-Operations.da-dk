---
title: Appen Lagersynlighed
description: Denne artikel beskriver, hvordan du bruger appen Lagersynlighed.
author: yufeihuang
ms.date: 09/15/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 0a4e436cc1af6b71049f75fb66bdfb89ca38df9f
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831768"
---
# <a name="use-the-inventory-visibility-app"></a>Bruge App til Inventory Visibility

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du bruger appen Lagersynlighed.

Lagersynlighed indeholder en modelbaseret app til visualisering. Appen indeholder tre sider: **Konfiguration**, **Operationel synlighed** og **Lageroversigt**. Den har følgende funktioner:

- Den leverer en brugergrænseflade (UI) til konfiguration af disponibel lagerbeholdning og konfiguration af foreløbige reservationer.
- Den understøtter forespørgsler om disponibel lagerbeholdning i realtid for forskellige dimensionskombinationer.
- Den indeholder en brugergrænseflade til bogføring af reservationsanmodninger.
- Den tilbyder en visning af den disponible lagerbeholdning for produkter sammen med alle dimensioner.
- Den tilbyder en visning af en disponible lagerbeholdningsliste for produkter sammen med foruddefinerede dimensioner. Visningen af den eksisterende liste kan enten være en fuld opsummering eller et forudindlæst resultat af en forespørgsel.

## <a name="prerequisites"></a>Forudsætninger

Før du går i gang, skal du installere og konfigurere tilføjelsesprogrammet Lagersynlighed som beskrevet i [Installere og konfigurere lagersynlighed](inventory-visibility-setup.md).

## <a name="open-and-authenticate-the-inventory-visibility-app"></a><a name="open-authenticate"></a>Åbne og godkende appen Lagersynlighed

Du kan åbne og godkende lagersynlighedsappen ved at følge disse trin.

1. Log på dit Power Apps-miljø.
1. Åbne en app til **lagersynlighed**.
1. Åbn siden **Driftssynlighed** fra venstre rude.
1. Vælg knappen **Indstillinger** (tandhjulsikonet) øverst på siden.
1. I dialogboksen **Indstillinger** skal du angive værdier for **Klient-id**, **Lejer-id** og **Klienthemmelighed**, som du noterede, da du [installerede og konfigurerede lagersynlighed](inventory-visibility-setup.md).
1. Vælg knappen **Opdater** ud for feltet **Token for bærer**. Systemet genererer et nyt ihændehaver-token baseret på de oplysninger, du har angivet.

    ![Indstillinger for forespørgsel om disponibel lagerbeholdning.](media/inventory-visibility-query-settings.png "Indstillinger for forespørgsel om disponibel lagerbeholdning")

1. Når du modtager et gyldigt ihændehaver-token, skal du lukke dialogboksen. Ihænderhaver-token udløber efter et stykke tid. Derfor skal du fra tid til anden opdatere den, når du skal opdatere konfigurationen, bogføre data eller forespørgselsdata.

## <a name="configure-the-inventory-visibility-app"></a><a name="configuration"></a>Konfigurere Lagersynlighed-app

Siden **Konfiguration** på Lagersynlighed-appen hjælper med at konfigurere den generelle datastyringskonfiguration og funktionskonfiguration. Når tilføjelsesprogrammet er installeret, indeholder standardkonfigurationen en standardopsætning fra Microsoft Dynamics 365 Supply Chain Management (datakilden `fno`). Du kan gennemse standardindstillingen. Derefter, afhængigt af forretningsbehovene og det eksterne systems krav til lagerbogføring kan du herefter redigere konfigurationen for at standardisere, hvordan lagerændringer kan bogføres, organiseres og forespørges på på tværs af flere systemer.

Du kan finde alle oplysninger om, hvordan du konfigurerer løsningen, under [Konfigurere lagersynlighed](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Driftssynlighed

Siden **Driftssynlighed** indeholder resultaterne af en forespørgsel om lagerbeholdning i realtid, reservationsregistrering og allokering baseret på forskellige dimensionskombinationer. Når funktionen *OnHandReservation* er [aktiveret](inventory-visibility-configuration.md), kan du også bogføre reservationsanmodninger fra siden **Driftssynlighed**.

### <a name="on-hand-query"></a>Forespørgsel om disponibel lagerbeholdning

Fanen **Forespørgsel** om **disponibel lagerbeholdning** viser resultaterne af en forespørgsel om den disponible lagerbeholdning i realtid. Følg disse trin for at konfigurere og køre en forespørgsel.

1. Åbne en app til **lagersynlighed**.
1. Åbn siden **Driftssynlighed** fra venstre rude.
1. Angiv de værdier for **organisations-id**, **websteds-id** og **lokations-id**, du vil forespørge på, under fanen **Onhand-forespørgsel**.
1. Angiv et eller flere produkt-id'er i feltet **Produkt-id** for at få nøjagtigt match til forespørgslen. Hvis du lader feltet **Produkt-id** være tomt, omfatter resultaterne alle produkter på den angivne websted og lokation.
1. Hvis du vil have et mere detaljeret resultat (f.eks. en visning efter dimensionsværdier, f.eks. farve og størrelse), skal du vælge grupper efter dimensioner i feltet **Grupperesultat efter**.
1. Hvis du vil finde varer med en bestemt dimensionsværdi (f.eks. farve = rød), skal du vælge dimensionen i feltet **Filterdimensioner** og derefter angive en dimensionsværdi.
1. Vælg **Forespørgsel**. Du modtager enten en grøn (grøn) meddelelse eller en mislykket (rød) meddelelse. Hvis forespørgslen mislykkes, skal du kontrollere forespørgselskriterierne og sikre dig, at dit [ihændehaver-token](#open-authenticate) ikke er udløbet.

Du kan også foretage direkte API-anmodninger ved at foretage en on-hand-forespørgsel. Du kan bruge `/api/environment/{environmentId}/onhand/indexquery` eller `/api/environment/{environmentId}/onhand`. Du kan finde flere oplysninger i [Offentlige API'er til lagersynlighed](inventory-visibility-api.md).

### <a name="reservation-posting"></a>Reservationsbogføring

Brug fanen **Reservationsbogføring** på siden **Driftssynlighed** til at bogføre en reservationsanmodning. Før du kan bogføre en reservationsanmodning, skal du aktivere funktionen *OnHandReservation*. Du kan finde flere oplysninger om denne funktion, og hvordan du slår den til, i [Reservationer i Lagersynlighed](inventory-visibility-reservations.md).

> [!NOTE]
> Muligheden for at foretage en forhåndsreservation via brugergrænsefladen er beregnet til, at du kan teste funktionen. Hver anmodning om forhåndsreservation skal knyttes til en linjeændring i en posteringsordre (oprettelse, redigering, sletning, så videre). Det anbefales derfor, at du kun foretager blød reservationer, der er knyttet til en back-end-ordre. Du kan finde flere oplysninger i [Reservationer i Lagersynlighed](inventory-visibility-reservations.md).

Følg disse trin for at bogføre en anmodning om forhåndsreservation ved hjælp af brugergrænsefladen.

1. Åbne en app til **lagersynlighed**.
1. Åbn siden **Driftssynlighed** fra venstre rude.
1. Angiv det antal, du vil forhåndsreservere i feltet **Antal** under fanen **Reservationsbogføring**.
1. Fjern markeringen i afkrydsningsfeltet **Aktivér negativt lager for at understøtte oversalg** for at forhindre, at lageret oversælges eller der reserveres for meget.
1. Vælg datakilden og den fysiske måling, der gælder for det forhåndsreserverede antal, i feltet **Operator**.
1. Angiv de værdier for **organisations-id**, **websteds-id** , **lokations-id** og **Produkt-id**, du vil forespørge på.
1. Hvis du vil have et mere detaljeret resultat, skal du vælge en datakilde, dimensioner og dimensionsværdier.

Du kan også bogføre en forhåndsreservation ved at foretage direkte API-anmodninger. Brug det mønster, der er beskrevet i [Oprette én reservationshændelse](inventory-visibility-api.md#create-one-reservation-event). Vælg derefter **Bogfør**. Hvis du vil have vist oplysninger om svaret på anmodningen, skal du vælge **Vis detaljer**. Du kan også hente værdien for `reservationId` fra svaroplysningerne.

### <a name="allocation"></a>Fordeling

Oplysninger om, hvordan fordelinger administreres fra brugergrænsefladen og API'er, finder du i [lagerfordelingen for lagersynlighed](inventory-visibility-allocation.md).

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Lageroversigt

Denne funktion viser en **lageroversigt** for produkter sammen med alle dimensioner. Lageroversigt er en tilpasset visning for enheden *Sum af OnHand-lagerbeholdning*. Lageroversigtsdataene synkroniseres periodisk fra Lagersynlighed.

Aktivere **lageroversigten** og angive synkroniseringsfrekvensen ved at følge disse trin:

1. Åbn siden **Konfiguration**.
1. Åbn fanen **Funktionsadministration og indstillinger**.
1. Angiv skift for funktionen *OnHandMostSpecificBackgroundService* til *Ja*.
1. Når funktionen er aktiveret, bliver afsnittet **Servicekonfiguration** tilgængelig og indeholder en række til konfiguration af funktionen **OnHandMostSpecificBackgroundService**. Med denne indstilling kan du vælge, hvor ofte lageroversigtsdata synkroniseres. Brug knapperne **Op** og **Ned** i kolonnen **Værdi** til at ændre tiden mellem synkroniseringer (som kan være så lav som 5 minutter). Vælg derefter **Gem**.

    ![OnHandMostSpecificBackgroundService-indstillingen](media/inventory-visibility-ohms-freq.png "OnHandMostSpecificBackgroundService-indstillingen")

1. Vælg **Opdater konfiguration** for at gemme alle ændringerne.

> [!NOTE]
> Funktionen *OnHandMostSpecificBackgroundService* sporer kun de ændringer i den disponible lagerbeholdning, der er foretaget, efter at du aktiverede funktionen. Data for produkter, der ikke er ændret, siden du aktiverede funktionen, synkroniseres ikke fra lagertjenestecachen til Dataverse-miljøet. Hvis **lageroversigtssiden** ikke viser alle de beholdningsoplysninger, du forventer, skal du åbne Supply Chain Management, gå til **Lagerstyring > Periodiske opgaver > integration af Lagersynlighed**, deaktivere batchjobbet og genaktivere det. Derved sker det første push, og alle data synkroniseres med enheden *Sum af disponibel lagerbeholdning* i løbet af de næste 15 minutter. Hvis du vil bruge funktionen *OnHandMostSpecificBackgroundService*, anbefales det, at du aktiverer den, før du opretter eventuelle ændringer i lagerbeholdningen, og aktiverer batchjobbet **Integration af lagersynlighed**.

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-streamlined-onhand-query"></a>Forudindlæse en strømlinet forespørgsel på disponibel lagerbeholdning

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Supply Chain Management gemmer mange oplysninger om din aktuelle disponible lagerbeholdning og gør den tilgængelig til en lang række formål. Men mange daglige operationer og tredjepartsintegrationer kræver kun en lille del af disse oplysninger, og hvis systemet forespørges efter dem alle, kan det resultere i store datasæt, der tager tid at samle og overføre. Lagersynlighedstjenesten kan derfor jævnligt hente og gemme et strømlinet sæt af disponible lagerdata, så optimerede oplysninger altid er tilgængelige. De gemte oplysninger om disponibel lagerbeholdning filtreres ud fra konfigurerbare forretningskriterier for at sikre, at kun de mest relevante oplysninger er inkluderet. Da de filtrerede lagerbeholdningslister gemmes lokalt i lagersynlighedstjenesten og opdateres jævnligt, understøtter de hurtig adgang, eksport af data efter behov og strømlinet integration med eksterne systemer.

På siden **Forudindlæs oversigten over lagersynlighed** kan du se enheden for *resultaterne af forudindlæsning af forespørgslen om beholdningsindeks*. I modsætning til enheden *Lageroversigt* indeholder enheden for *resultaterne af forudindlæsning af forespørgslen om beholdningsindeks* en liste over lagerbeholdning for produkter sammen med valgte dimensioner. Lagersynlighed synkroniserer de forudindlæste oversigtsdata hvert 15. minut.

Hvis du vil se data på fanen **Forudindlæs oversigten over lagersynlighed** skal du aktivere og konfigurere funktionen *OnHandIndexQueryPreloadBackgroundService*. Se [Aktivere og konfigurere forudindlæste disponible forespørgsler](inventory-visibility-configuration.md#query-preload-configuration) til vejledning.

> [!NOTE]
> Som med funktionen *OnHandMostSpecificBackgroundService* sporer funktionen *OnHandIndexQueryPreloadBackgroundService* kun de ændringer i lagerbeholdningen, der er foretaget, efter at du aktiverede funktionen. Data for produkter, der ikke er ændret, siden du aktiverede funktionen, synkroniseres ikke fra lagertjenestecachen til Dataverse-miljøet. Hvis **lageroversigtssiden** ikke viser alle de beholdningsoplysninger, du forventer, skal du gå til **Lagerstyring > Periodiske opgaver > integration af Lagersynlighed**, deaktivere batchjobbet og genaktivere det. Derved sker det første push, og alle data synkroniseres med enheden for *resultaterne af forudindlæsning af forespørgslen om beholdningsindeks* i løbet af de næste 15 minutter. Hvis du vil bruge denne funktion, anbefales det, at du aktiverer den, før du opretter eventuelle ændringer i lagerbeholdningen, og aktiverer batchjobbet **lagersynlighedsintegration**.

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a>Filtrere og gennemse lageroversigter

Ved hjælp af **Avanceret filter**, som findes i Dataverse, kan du oprette en tilpasset visning af de rækker, der er vigtige for dig. Med de avancerede filterindstillinger kan du oprette mange forskellige visninger, fra de mest simple til de mest komplekse. De gør det også muligt at føje grupperede og indlejrede betingelser til filtrene. Du kan få mere at vide om, hvordan du bruger det avancerede filter, i [Redigere eller oprette personlige visninger ved hjælp af avancerede gitterfiltre](/powerapps/user/grid-filters-advanced).

Siden **Lageroversigt** indeholder tre felter over gitteret (S **tandarddimension**, **Brugerdefineret dimension** og **Målepunkt**), som du kan bruge til at styre, hvilke kolonner der er synlige. Du kan også markere kolonneoverskrifter for at filtrere eller sortere det aktuelle resultat efter denne kolonne. På følgende skærmbillede fremhæves felterne for dimension, filtrering, resultatantal og "indlæsning af flere", der er tilgængelige på siden **Lageroversigt**.

![Siden Lageroversigt.](media/inventory-visibility-onhand-list.png "Siden Lageroversigt")

Da du har foruddefineret de dimensioner, der bruges til indlæsning af oversigtsdata, viser siden **Forudindlæs oversigten over lagersynlighed** dimensionsrelaterede kolonner. *Dimensionerne kan ikke tilpasses – systemet understøtter kun sted- og lokalitetsdimensioner til forudindlæste lagerbeholdningslister.* Siden **Forudindlæs oversigten over lagersynlighed** indeholder filtre, der ligner dem på siden **Lageroversigt**, med undtagelse af de dimensioner, der allerede er valgt. På følgende skærmbillede fremhæves de filtreringsfelter, der er tilgængelige på siden **Forudindlæs oversigten over lagersynlighed**.

![Siden Forudindlæs oversigten over lagersynlighed.](media/inventory-visibility-preload-onhand-list.png "Siden Forudindlæs oversigten over lagersynlighed")

Nederst på siderne **Forudindlæs oversigten over lagersynlighed** og **Lageroversigt** finder du oplysninger som f.eks. "50 poster (29 valgte)" eller "50 poster". Disse oplysninger henviser til de poster, der er indlæst fra resultatet for **Avanceret filter**. Teksten "29 valgte" henviser til det antal poster, der er valgt ved hjælp af kolonneoverskriftens filter for de indlæste poster. Du kan også se knappen **Indlæs mere**, som du kan bruge til at indlæse flere poster fra Dataverse. Standardantallet af indlæste poster er 50. Når du vælger **Indlæs mere**, indlæses de næste 1.000 tilgængelige poster i visningen. Tallet på knappen **Indlæs mere** angiver de aktuelt indlæste poster og det samlede antal poster i resultatet for **Avanceret filter**.
