---
title: Genopfyldningsmetoder og ændring af antal
description: Denne artikel indeholder oplysninger om genopfyldningmetoder. Det forklares også, hvordan antallet på flere ordrer på et produkt påvirker resultatet.
author: t-benebo
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1e0fe6c1f49bc0f6887f1b29118c1fee7a6222f
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739750"
---
# <a name="replenishment-methods-and-quantity-modification"></a>Genopfyldningsmetoder og ændring af antal

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder oplysninger om genopfyldningmetoder. Det forklares også, hvordan antallet på flere ordrer på et produkt påvirker resultatet.

Genopfyldningsmetoder kaldes også disponeringsmetoder og metoder til angivelse af partistørrelse.

## <a name="coverage-codes"></a>Disponeringskoder

Varedisponering kan konfigureres til at bruge forskellige genopfyldningsmetoder. Genopfyldningsmetoderne er de teknikker, som systemet bruger til at beregne behov for et produkt. Genopfyldningsmetoder defineres ud fra disponeringskoder, du kan angive for enten disponeringsgruppen eller produktet.

Følgende disponeringskoder kan bruges:

- **Periode** – Genopfyldningsmetoden kombinerer alle behov for en periode til én ordre for produktet. Ordren planlægges for den første dag i perioden, og dens antal vil opfylde nettobehovet i den oprettede periode. Perioden starter med det første behov for produktet og dækker den definerede varighed i tiden. Den næste periode vil starte med de næste behov for produktet. Disponeringskoden for *periode* bruges ofte til ikke-forudsigelige lagertræk, sæsonafhængige produkter eller produkter med høje omkostninger. Følgende illustration viser et eksempel.

    ![Eksempel på brug af periodedisponeringskode.](./media/coverage-code-period.png "Eksempel på brug af periodedisponeringskode")

- **Behov** – I genopfyldningsmetoden til opretter systemet en planlagt indkøbs-, overførsels- eller produktionsordre pr. behov for produktet. Denne metode bruges til dyre produkter, hvor efterspørgslen er periodisk. Disponeringskoden for *behov* bruges ofte til konfigurerbare produkter eller scenarier for fremstilling efter ordre. Følgende illustration viser et eksempel.

    ![Eksempel på brug af behovsdisponeringskode.](./media/coverage-code-requirement.png "Eksempel på brug af behovsdisponeringskode")

- **Min./Maks.** – Genopfyldningsmetoden er baseret på lagerniveauet. Den definerer genopfyldning af lageret op til et bestemt niveau, når den forventede beholdning er under en bestemt grænseværdi. Genopfyldningsantallet vil være forskellen mellem maksimumniveauet og det forventede disponible lagerniveau. Disponeringskoden for *Min./Maks.* bruges ofte til forudsigelige lagertræk, mest solgte produkter eller billigste produkter. Følgende illustration viser et eksempel.

    ![Eksempel på brug af disponeringskode for Min./Maks.](./media/coverage-code-min-max.png "Eksempel på brug af disponeringskode for Min./Maks.")

- **Manuel** – I genopfyldningsmetoden foreslår systemet ikke køb, overflytning eller produktionsordrer for produktet. I stedet er planlægningsmedarbejderen for produktet ansvarlig for oprettelse af de nødvendige ordrer til genopfyldning af produktet. Den *manuelle* disponeringskode bruges ofte til produkter, der ikke ønskes systemgenererede ordreforslag for.

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a>Effekten af ordreantallet fra standardordreindstillinger

På siden **Standardordreindstilling** for et frigivet produkt kan du angive hver af følgende indstillinger for antal i oversigtspanelerne **Indkøbsordre**, **Lager** og **Salgsordre**. (Oversigtspanelet **Lager** bruges til både flytteordrer og produktionsordrer).

- **Flere** – Ordreforslag er et multiplum af dette antal.

    Hvis feltet **Flere** for eksempel er angivet til *5*, kan en ordre være for et antal på 5, 10, 15, 20 osv.

- **Min. ordreantal** – Ordreforslag bliver ikke mindre end den angivne værdi.

    Hvis feltet **Min. ordreantal** for eksempel er angivet til *10*, oprettes der et ordreforslag på 10, også selvom der kun kræves fire for at opfylde behovet.

- **Maks. ordreantal** – Ordreforslag bliver ikke større end den angivne værdi. Hvis efterspørgslen er større end værdien **Maks. ordreantal**, oprettes der flere ordreforslag til at dække dette.

    Hvis feltet **Maks. ordreantal** for eksempel angivet til *100*, og behovet er 450, oprettes der fire ordreforslag for et antal på 100, og der oprettes et ordreforslag på 50.

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a>Eksempler på genopfyldning, hvor disponeringskoden Min./Maks. bruges

Hvis du ikke angiver en værdi i feltet **Flere** for et produkt på siden **Standardordreindstilling**, og hvis du bruger genopfyldningsmetoden *Min./Maks.*, foretager varedisponering genopfyldning af lageret op til et bestemt niveau, når den forventede beholdning er under en bestemt grænseværdi.

Hvis du definerer en multiplummængde for et produkt, vil genopfyldningsmetoden *Min./Maks.* ændrer funktionaliteten og tage værdien af **Flere** med i beregningen.

Med andre ord genopfylder varedisponering stadig lageret op til det definerede maksimumniveau, når den forventede beholdning er mindre end det definerede minimumniveau. Genopfyldningsantallet skal dog være et multiplum af værdien for **Flere**.

Hvis genopfyldningsantallet (forskellen mellem det maksimale niveau og det forventede beholdningsniveau) ikke er et multiplum af den definerede multiplummængde, bruger varedisponering den første mulige værdi, der sammen med den forventede beholdning vil være under det maksimale niveau. Hvis summen er mindre end minimumniveauet, bruger varedisponering den første værdi, der sammen med den forventede beholdning vil være over maksimumniveauet.

Følgende undersektioner indeholder nogle eksempler, der viser, hvordan multiplummængden for ordrer på et produkt påvirker resultatet af genopfyldningsmetoden *Min./Maks.* .

### <a name="example-1"></a>Eksempel 1

Et produkt har følgende konfiguration:

- **Disponeringskode:** *Min./Maks.*
- **Minimum:** *15*
- **Maksimum:** *22*
- **Multiplum:** *0*

Der er 10 styk af produktet i lagerbeholdningen, og der er ingen anden efterspørgsel eller forsyning.

Når varedisponering kører, oprettes der et ordreforslag på 12 styk for at genopfylde lageret med det maksimale antal.

### <a name="example-2"></a>Eksempel 2

Et produkt har følgende konfiguration:

- **Disponeringskode:** *Min./Maks.*
- **Minimum:** *15*
- **Maksimum:** *22*
- **Multiplum:** *5*

Der er 10 styk af produktet i lagerbeholdningen, og der er ingen anden efterspørgsel eller forsyning.

Når varedisponering kører, oprettes der et ordreforslag på 10 styk (fordi 15 styk af genopfyldning plus 10 styk af den disponible lagerbeholdning vil overstige det maksimale antal).

### <a name="example-3"></a>Eksempel 3

Et produkt har følgende konfiguration:

- **Disponeringskode:** *Min./Maks.*
- **Minimum:** *21*
- **Maksimum:** *24*
- **Multiplum:** *5*

Der er 10 styk af produktet i lagerbeholdningen, og der er ingen anden efterspørgsel eller forsyning.

Når varedisponering kører, oprettes ordreforslaget på 15 styk (fordi 10 styk af genopfyldning plus 10 styk af den disponible lagerbeholdning vil være mindre end det minimale antal).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
