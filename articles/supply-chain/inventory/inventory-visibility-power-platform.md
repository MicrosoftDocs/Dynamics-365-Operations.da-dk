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
ms.openlocfilehash: 674adb70cc4372a8c5ca8c75ed3ef840d8ec7b79
ms.sourcegitcommit: d2046cad5de570e6302a4390b41881a7ecb12e26
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/15/2022
ms.locfileid: "9520855"
---
# <a name="use-the-inventory-visibility-app"></a>Bruge App til Inventory Visibility

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du bruger appen Lagersynlighed.

Lagersynlighed indeholder en modelbaseret app til visualisering. Appen indeholder tre sider: **Konfiguration**, **Operationel synlighed** og **Lageroversigt**. Den har følgende funktioner:

- Den leverer en brugergrænseflade (UI) til konfiguration af disponibel lagerbeholdning og konfiguration af foreløbige reservationer.
- Den understøtter forespørgsler om disponibel lagerbeholdning i realtid for forskellige dimensionskombinationer.
- Den indeholder en brugergrænseflade til bogføring af reservationsanmodninger.
- Den tilbyder en visning af den disponible lagerbeholdning for produkter sammen med alle dimensioner.
- Den tilbyder en visning af en disponible lagerbeholdningsliste for produkter sammen med foruddefinerede dimensioner.


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

Når du åbner fanen **Disponibel forespørgsel** på siden **Driftssynlighed**, beder systemet om dine legitimationsoplysninger, så det kan hente det ihændebærertoken, der kræves for at kunne forespørge på tjenesten Lagersynlighed. Du kan nøjes med at indsætte i ihændehavertokenet i feltet **Ihændehavertoken** og lukke dialogboksen. Du kan derefter bogføre en anmodning om en forespørgsel på disponibel lagerbeholdning.

Hvis indhændehavertokenet ikke er gyldigt, eller hvis det er udløbet, skal du indsætte et nyt i feltet **Ihændehavertoken**. Angiv de korrekte værdier for **Klient-id**, **Lejer-id**, **Klienthemmelighed**, og vælg derefter **Opdater**. Systemet henter automatisk et nyt gyldigt ihændehavertoken.

Hvis du vil bogføre en forespørgsel om disponibel lagerbeholdning, skal du angive forespørgslen i brødteksten. Brug det mønster, der er beskrevet i [Forespørgsel ved hjælp af bogføringsmetoden](inventory-visibility-api.md#query-with-post-method).

![Indstillinger for forespørgsel om disponibel lagerbeholdning](media/inventory-visibility-query-settings.png "Indstillinger for forespørgsel om disponibel lagerbeholdning")

### <a name="reservation-posting"></a>Reservationsbogføring

Brug fanen **Reservationsbogføring** på siden **Driftssynlighed** til at bogføre en reservationsanmodning. Før du kan bogføre en reservationsanmodning, skal du aktivere funktionen *OnHandReservation*. Du kan finde flere oplysninger om denne funktion, og hvordan du slår den til, i [Reservationer i Lagersynlighed](inventory-visibility-reservations.md).

Hvis du vil bogføre en reservationsanmodning, skal du angive en værdi i anmodningsteksten. Brug det mønster, der er beskrevet i [Oprette én reservationshændelse](inventory-visibility-api.md#create-one-reservation-event). Vælg derefter **Bogfør**. Hvis du vil have vist oplysninger om svaret på anmodningen, skal du vælge **Vis detaljer**. Du kan også hente værdien for `reservationId` fra svaroplysningerne.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Lageroversigt

Denne funktion viser en **lageroversigt** for produkter sammen med alle dimensioner. Lageroversigt er en tilpasset visning for enheden *Sum af OnHand-lagerbeholdning*. Lageroversigtsdataene synkroniseres periodisk fra Lagersynlighed.

Aktivere **lageroversigten** og angive synkroniseringsfrekvensen ved at følge disse trin:

1. Åbn siden **Konfiguration**.
1. Åbn fanen **Funktionsadministration og indstillinger**.
1. Angiv skift for funktionen **OnHandMostSpecificBackgroundService** til *Ja*.
1. Når funktionen er aktiveret, bliver afsnittet **Servicekonfiguration** tilgængelig og indeholder en række til konfiguration af funktionen **OnHandMostSpecificBackgroundService**. Med denne indstilling kan du vælge, hvor ofte lageroversigtsdata synkroniseres. Brug knapperne **Op** og **Ned** i kolonnen **Værdi** til at ændre tiden mellem synkroniseringer (som kan være så lav som 5 minutter). Vælg derefter **Gem**.

    ![OnHandMostSpecificBackgroundService-indstillingen](media/inventory-visibility-ohms-freq.png "OnHandMostSpecificBackgroundService-indstillingen")

1. Vælg **Opdater konfiguration** for at gemme alle ændringerne.


> [!NOTE]
> Funktionen *OnHandMostSpecificBackgroundService* sporer kun de ændringer i den disponible lagerbeholdning, der er foretaget, efter at du aktiverede funktionen. Data for produkter, der ikke er ændret, siden du aktiverede funktionen, synkroniseres ikke fra lagertjenestecachen til Dataverse-miljøet. Hvis **lageroversigtssiden** ikke viser alle de beholdningsoplysninger, du forventer, skal du åbne Supply Chain Management, gå til **Lagerstyring > Periodiske opgaver > integration af Lagersynlighed**, deaktivere batchjobbet og genaktivere det. Derved sker det første push, og alle data synkroniseres med enheden *Sum af disponibel lagerbeholdning* i løbet af de næste 15 minutter. Hvis du vil bruge funktionen *OnHandMostSpecificBackgroundService*, anbefales det, at du aktiverer den, før du opretter eventuelle ændringer i lagerbeholdningen, og aktiverer batchjobbet **Integration af lagersynlighed**.

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-the-inventory-visibility-onhand-query"></a>Forudindlæse en strømlinet forespørgsel på disponibel lagerbeholdning

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Supply Chain Management gemmer mange oplysninger om din aktuelle disponible lagerbeholdning og gør den tilgængelig til en lang række formål. Men mange daglige operationer og tredjepartsintegrationer kræver kun en lille del af disse oplysninger, og hvis systemet forespørges efter dem alle, kan det resultere i store datasæt, der tager tid at samle og overføre. Lagersynlighedstjenesten kan derfor jævnligt hente og gemme et strømlinet sæt af disponible lagerdata, så optimerede oplysninger altid er tilgængelige. De gemte oplysninger om disponibel lagerbeholdning filtreres ud fra konfigurerbare forretningskriterier for at sikre, at kun de mest relevante oplysninger er inkluderet. Da de filtrerede lagerbeholdningslister gemmes lokalt i lagersynlighedstjenesten og opdateres jævnligt, understøtter de hurtig adgang, eksport af data efter behov og strømlinet integration med eksterne systemer.

> [!NOTE]
> Den aktuelle forhåndsversion af denne funktion kan kun give forudindlæste resultater, herunder lokation og placering. Den endelige version af funktionen forventes at give dig mulighed for at vælge andre dimensioner, som skal forudindlæses med resultaterne.

På siden **Forudindlæs oversigten over lagersynlighed** kan du se enheden for *resultaterne af forudindlæsning af forespørgslen om beholdningsindeks*. I modsætning til enheden *Lageroversigt* indeholder enheden for *resultaterne af forudindlæsning af forespørgslen om beholdningsindeks* en liste over lagerbeholdning for produkter sammen med valgte dimensioner. Lagersynlighed synkroniserer de forudindlæste oversigtsdata hvert 15. minut.

Hvis du vil have vist data under fanen **Forudindlæs oversigten over lagersynlighed**, skal du aktivere funktionen *OnHandIndexQueryPreloadBackgroundService* under fanen **Funktionsstyring** på siden **Konfiguration** og derefter vælge **Opdater konfiguration** (se også [Konfigurere lagersynlighed](inventory-visibility-configuration.md)).

> [!NOTE]
> Som med funktionen *OnhandMostSpecificBackgroudService* sporer funktionen *OnHandIndexQueryPreloadBackgroundService* kun de ændringer i lagerbeholdningen, der er foretaget, efter at du aktiverede funktionen. Data for produkter, der ikke er ændret, siden du aktiverede funktionen, synkroniseres ikke fra lagertjenestecachen til Dataverse-miljøet. Hvis **lageroversigtssiden** ikke viser alle de beholdningsoplysninger, du forventer, skal du gå til **Lagerstyring > Periodiske opgaver > integration af Lagersynlighed**, deaktivere batchjobbet og genaktivere det. Derved sker det første push, og alle data synkroniseres med enheden for *resultaterne af forudindlæsning af forespørgslen om beholdningsindeks* i løbet af de næste 15 minutter. Hvis du vil bruge denne funktion, anbefales det, at du aktiverer den, før du opretter eventuelle ændringer i lagerbeholdningen, og aktiverer batchjobbet **lagersynlighedsintegration**.

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a>Filtrere og gennemse lageroversigter

Ved hjælp af **Avanceret filter**, som findes i Dataverse, kan du oprette en tilpasset visning af de rækker, der er vigtige for dig. Med de avancerede filterindstillinger kan du oprette mange forskellige visninger, fra de mest simple til de mest komplekse. De gør det også muligt at føje grupperede og indlejrede betingelser til filtrene. Du kan få mere at vide om, hvordan du bruger det avancerede filter, i [Redigere eller oprette personlige visninger ved hjælp af avancerede gitterfiltre](/powerapps/user/grid-filters-advanced).

Siden **Lageroversigt** indeholder tre felter over gitteret (S **tandarddimension**, **Brugerdefineret dimension** og **Målepunkt**), som du kan bruge til at styre, hvilke kolonner der er synlige. Du kan også markere kolonneoverskrifter for at filtrere eller sortere det aktuelle resultat efter denne kolonne. På følgende skærmbillede fremhæves felterne for dimension, filtrering, resultatantal og "indlæsning af flere", der er tilgængelige på siden **Lageroversigt**.

![Siden Lageroversigt.](media/inventory-visibility-onhand-list.png "Siden Lageroversigt")

Da du har foruddefineret de dimensioner, der bruges til indlæsning af oversigtsdata, viser siden **Forudindlæs oversigten over lagersynlighed** dimensionsrelaterede kolonner. *Dimensionerne kan ikke tilpasses – systemet understøtter kun sted- og lokalitetsdimensioner til forudindlæste lagerbeholdningslister.* Siden **Forudindlæs oversigten over lagersynlighed** indeholder filtre, der ligner dem på siden **Lageroversigt**, med undtagelse af de dimensioner, der allerede er valgt. På følgende skærmbillede fremhæves de filtreringsfelter, der er tilgængelige på siden **Forudindlæs oversigten over lagersynlighed**.

![Siden Forudindlæs oversigten over lagersynlighed.](media/inventory-visibility-preload-onhand-list.png "Siden Forudindlæs oversigten over lagersynlighed")

Nederst på siderne **Forudindlæs oversigten over lagersynlighed** og **Lageroversigt** finder du oplysninger som f.eks. "50 poster (29 valgte)" eller "50 poster". Disse oplysninger henviser til de poster, der er indlæst fra resultatet for **Avanceret filter**. Teksten "29 valgte" henviser til det antal poster, der er valgt ved hjælp af kolonneoverskriftens filter for de indlæste poster. Du kan også se knappen **Indlæs mere**, som du kan bruge til at indlæse flere poster fra Dataverse. Standardantallet af indlæste poster er 50. Når du vælger **Indlæs mere**, indlæses de næste 1.000 tilgængelige poster i visningen. Tallet på knappen **Indlæs mere** angiver de aktuelt indlæste poster og det samlede antal poster i resultatet for **Avanceret filter**.
