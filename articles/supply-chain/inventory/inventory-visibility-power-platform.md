---
title: Appen Lagersynlighed
description: Denne artikel beskriver, hvordan du bruger appen Lagersynlighed.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: db158e3b6ae76f69149db04096f99d3dc4251146
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895751"
---
# <a name="use-the-inventory-visibility-app"></a>Bruge App til Inventory Visibility

[!include [banner](../includes/banner.md)]


Denne artikel beskriver, hvordan du bruger appen Lagersynlighed.

Lagersynlighed indeholder en modelbaseret app til visualisering. Appen indeholder tre sider: **Konfiguration**, **Operationel synlighed** og **Lageroversigt**. Den har følgende funktioner:

- Den leverer en brugergrænseflade (UI) til konfiguration af disponibel lagerbeholdning og konfiguration af foreløbige reservationer.
- Den understøtter forespørgsler om disponibel lagerbeholdning i realtid for forskellige dimensionskombinationer.
- Den indeholder en brugergrænseflade til bogføring af reservationsanmodninger.
- Den tilbyder en tilpasset visning af den disponible lagerbeholdning for produkter sammen med alle dimensioner.

## <a name="prerequisites"></a>Forudsætninger

Før du går i gang, skal du installere og konfigurere tilføjelsesprogrammet Lagersynlighed som beskrevet i [Installere og konfigurere lagersynlighed](inventory-visibility-setup.md).

## <a name="open-the-inventory-visibility-app"></a>Åbne en app til lagersynlighed

Hvis du vil åbne appen Lagersynlighed, skal du logge på dit Power Apps-miljø og åbne **Lagersynlighed**.

## <a name="configuration"></a><a name="configuration"></a>Variantkonfiguration

Siden **Konfiguration** på Lagersynlighed-appen hjælper med at konfigurere konfigurationen af disponibel lagerbeholdning og konfigurationen af foreløbige reservationer. Når tilføjelsesprogrammet er installeret, indeholder standardkonfigurationen en standardopsætning fra Microsoft Dynamics 365 Supply Chain Management (datakilden `fno`). Du kan gennemse standardindstillingen. Afhængigt af forretningsbehovene og det eksterne systems krav til lagerbogføring kan du herefter redigere konfigurationen for at standardisere, hvordan lagerændringer kan bogføres, organiseres og forespørges på på tværs af flere systemer.

Du kan finde alle oplysninger om, hvordan du konfigurerer løsningen, under [Konfigurere lagersynlighed](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Driftssynlighed

Siden **Driftssynlighed** indeholder resultaterne af en forespørgsel om lagerbeholdning i realtid baseret på forskellige dimensionskombinationer. Når funktionen *OnHandReservation* er aktiveret, kan du også bogføre reservationsanmodninger fra siden **Driftssynlighed**.

### <a name="on-hand-query"></a>Forespørgsel om disponibel lagerbeholdning

Fanen **Forespørgsel om disponibel lagerbeholdning** viser resultaterne af en forespørgsel om den disponible lagerbeholdning i realtid.

Når du vælger fanen **Forespørgsel om disponibel lagerbeholdning**, beder systemet om dine legitimationsoplysninger, så det kan hente det ihændebærertoken, der kræves for at kunne forespørge på tjenesten Lagersynlighed. Du kan nøjes med at indsætte i ihændehavertokenet i feltet **Ihændehavertoken** og lukke dialogboksen. Du kan derefter bogføre en anmodning om en forespørgsel på disponibel lagerbeholdning.

Hvis indhændehavertokenet ikke er gyldigt, eller hvis det er udløbet, skal du indsætte et nyt i feltet **Ihændehavertoken**. Angiv de korrekte værdier for **Klient-id**, **Lejer-id**, **Klienthemmelighed**, og vælg derefter **Opdater**. Systemet henter automatisk et nyt gyldigt ihændehavertoken.

Hvis du vil bogføre en forespørgsel om disponibel lagerbeholdning, skal du angive forespørgslen i brødteksten. Brug det mønster, der er beskrevet i [Forespørgsel ved hjælp af bogføringsmetoden](inventory-visibility-api.md#query-with-post-method).

![Indstillinger for forespørgsel om disponibel lagerbeholdning](media/inventory-visibility-query-settings.png "Indstillinger for forespørgsel om disponibel lagerbeholdning")

### <a name="reservation-posting"></a>Reservationsbogføring

Brug fanen **Reservationsbogføring** til at bogføre en reservationsanmodning. Før du kan bogføre en reservationsanmodning, skal du aktivere funktionen *OnHandReservation*. Du kan finde flere oplysninger om denne funktion i [Reservationer i Lagersynlighed](inventory-visibility-reservations.md).

Hvis du vil bogføre en reservationsanmodning, skal du angive en værdi i anmodningsteksten. Brug det mønster, der er beskrevet i [Oprette én reservationshændelse](inventory-visibility-api.md#create-one-reservation-event). Vælg derefter **Bogfør**. Hvis du vil have vist oplysninger om svaret på anmodningen, skal du vælge **Vis detaljer**. Du kan også hente værdien for `reservationId` fra svaroplysningerne.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Lageroversigt

**Lageroversigt** er en tilpasset visning for enheden *Opsummering af disponibel lagerbeholdning*. Den giver en lageroversigt for produkter sammen med alle dimensioner. Lageroversigtsdataene synkroniseres periodisk fra Lagersynlighed hvert 15. minut. Før du kan se data under fanen **Lageroversigt**, skal du aktivere funktionen *OnHandMostSpecificBackgroundService* under fanen **Funktionsstyring** og vælge **Opdater konfiguration**.

> [!NOTE]
> Funktionen *OnHandMostSpecificBackgroundService* sporer kun de ændringer i produktlageret, der er foretaget, efter at du aktiverede funktionen. Data for produkter, der ikke er ændret, siden du aktiverede funktionen, synkroniseres ikke fra lagertjenestecachen til Dataverse-miljøet. Hvis **lageroversigtssiden** ikke viser alle de beholdningsoplysninger, du forventer, skal du gå til **Lagerstyring > Periodiske opgaver > integration af Lagersynlighed**, deaktivere batchjobbet og genaktivere det. Derved sker det første push, og alle data synkroniseres med enheden *Lager onHand Sum* i løbet af de næste 15 minutter. Hvis du vil bruge denne funktion, anbefales det, at du aktiverer den, før du opretter eventuelle ændringer i lagerbeholdningen, og aktiverer batchjobbet **lagersynlighedsintegration**.

Ved hjælp af **Avanceret filter**, som findes i Dataverse, kan du oprette en tilpasset visning af de rækker, der er vigtige for dig. Med de avancerede filterindstillinger kan du oprette mange forskellige visninger, fra de mest simple til de mest komplekse. De gør det også muligt at føje grupperede og indlejrede betingelser til filtrene. Du kan få mere at vide om, hvordan du bruger **Avanceret filter**, i [Redigere eller oprette personlige visninger ved hjælp af avancerede gitterfiltre](/powerapps/user/grid-filters-advanced).

Øverst i den tilpassede visning er der tre felter: **Standarddimension**, **Brugerdefineret dimension** og **Måling**. Du kan bruge disse felter til at bestemme, hvilke kolonner der skal være synlige.

Du kan markere kolonneoverskriften for at filtrere eller sortere det aktuelle resultat.

Nederst i den tilpassede visning vises oplysninger som f.eks. "50 poster (29 valgte)" eller "50 poster". Disse oplysninger henviser til de poster, der er indlæst fra resultatet for **Avanceret filter**. Teksten "29 valgte" henviser til det antal poster, der er valgt ved hjælp af kolonneoverskriftens filter for de indlæste poster.

Nederst i visningen kan du bruge knappen **Indlæs mere** til at indlæse flere poster fra Dataverse. Standardantallet af indlæste poster er 50. Når du vælger **Indlæs mere**, indlæses de næste 1.000 tilgængelige poster i visningen. Tallet på knappen **Indlæs mere** angiver de aktuelt indlæste poster og det samlede antal poster i resultatet for **Avanceret filter**.

![Lageroversigt](media/inventory-visibility-onhand-list.png "Lageroversigt")
