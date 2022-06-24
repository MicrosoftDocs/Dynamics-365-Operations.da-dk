---
title: Forsyningsplan
description: Denne artikel indeholder oplysninger om siden Forsyningsplan og dens funktioner.
author: t-benebo
ms.date: 9/3/2021
ms.topic: article
ms.search.form: ReqSupplyDemandSchedule, ReqSupplyDemandScheduleFilters, ReqSupplyDemandItemDetails, ReqTransFuturesActionsPart, ReqSupplyDemandOverviewLegendPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0e3937dd4cffc464f38b5770674364579bdb06d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851733"
---
# <a name="supply-schedule"></a>Forsyningsplan

[!include [banner](../includes/banner.md)]

Siden **Forsyningsplan** viser en omfattende oversigt over udbud og efterspørgsel for et produkt eller en produktfamilie. Oplysningerne filtreres efter lokation, behovsplan og perioder. Du kan også bruge siden til at oprette nye ordrer, redigere eksisterende ordreforslag og køre varedisponering.

## <a name="open-the-supply-schedule-page"></a>Åbne siden Forsyningsplan

Du kan åbne siden **Forsyningsplan** på en af følgende måder:

- Gå til **Varedisponering \> Varedisponering \> Forsyningsplan**. I dialogboksen **Rediger filter** skal du angive den plan og det produkt, du leder efter, ved at angive filterværdier i de felter, der vises. (I resten af denne artikel kaldes den samling filterværdier, du angiver, for "filteret" eller "det aktuelle filter"). Når du er færdig, skal du vælge **OK**.
- Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**. Vælg eller åbn et produkt. Vælg derefter **Forsyningsplan** i gruppen **Vis** under fanen **Plan** i handlingsruden.
- Gå til **Varedisponering \> Konfiguration \> Behovsprognose \> Varefordelingsnøgler**. Vælg en varefordelingsnøgle, der skal bruges som produktfamilie. Vælg derefter **Forsyningsplan** i handlingsruden.
- Gå til **Varedisponering \> Varedisponering \> Ordreforslag**. Vælg eller åbn et ordreforslag. Vælg derefter **Forsyningsplan** i gruppen **Vis** under fanen **Vis** i handlingsruden.

> [!NOTE]
> Når du åbner siden **Forsyningsplan** fra et produkt, en produktfamilie eller et ordreforslag, behøver du ikke angive filterværdier. Systemet bruger standardperiodeskabelonen.

## <a name="use-the-supply-schedule-page"></a>Bruge siden Forsyningsplan

Siden **Forsyningsplan** består af et øverste afsnit, oversigtspanelet **Lager ved periodeafslutning**, et ekstra oversigtspanel, der vises, baseret på den linje, der er valgt i det øverste afsnit, og ruden med faktaboksen. (Hvis du vil åbne ruden med faktaboksen for at se en faktaboks, skal du vælge **Relaterede oplysninger** ved højre kant på siden).

### <a name="upper-section"></a>Øvre sektion

Den øverste del af siden **Forsyningsplan** indeholder et gitter, der viser følgende data for et produkt eller en produktfamilie. Disse data opdeles efter perioder, der er defineret af værdien i **Periodeskabelon** fra filteret.

- **Periodestartlager** – Denne linje viser den forventede lagersaldo ved periodens start, hvis alle ordrer i systemet optræder.
- **Lager ved periodeafslutning** – Denne linje viser den forventede lagersaldo ved periodens afslutning, hvis alle ordrer i systemet optræder.
- **Udlignet lager ved periodeafslutning** – Denne linje viser lagerbeløbet ved afslutningen af den periode, der er udlignet i forhold til fremtidig efterspørgsel.
- **Periodens nettoforsyning** – Denne linje viser forskellen mellem udbud og efterspørgsel i perioden.
- **Minimumlager** – Denne node viser sikkerhedslageret for et produkt eller en produktfamilie. Hvis du vil udvide eller skjule denne node, skal du markere den og derefter vælge **Udvid** eller **Skjul** på værktøjslinjen. Denne node vises kun, når der er sikkerhedslager for produktet eller produktfamilien.
- **Efterspørgsel** – Denne node viser efterspørgslen på et produkt eller en produktfamilie. Efterspørgslen grupperes efter transaktionstype. Hvis du vil udvide eller skjule denne node, skal du markere den og derefter vælge **Udvid** eller **Skjul** på værktøjslinjen. Efterspørgselstransaktionstyper omfatter salg, overførsler og lagerkladder. Denne node vises kun, når der er efterspørgsel på produktet eller produktfamilien.
- **Forsyning** – Denne node viser forsyning af et produkt eller en produktfamilie. Forsyningen grupperes efter transaktionstype. Hvis du vil udvide eller skjule denne node, skal du markere den og derefter vælge **Udvid** eller **Skjul** på værktøjslinjen. Forsyningstransaktionstyper inkluderer produktion, indkøb og overførsler. Denne node vises kun, når der er forsyning af produktet eller produktfamilien.

Mange af de tilgængelige værktøjslinjeknapper, faktaboksvisninger og visning af oversigtspaneler afhænger af dine valg i den øverste sektion. Du skal som regel vælge en transaktionstype ved at markere en af rækkerne under noden **Forsyning** eller **Efterspørgsel**. Derefter vælger du en periode ved at vælge en specifik kolonne til den valgte række.

Værktøjslinjen over gitteret i øverste del af siden **Forsyningsplan** indeholder følgende knapper:

- **Udvid/skjul** – Udvid eller skjul en valgt node, f.eks. **Efterspørgsel**-noden, **Forsyning**-noden og deres undernoder. (Noder viser et **\[+\]** eller **\[-\]** som præfiks for at angive, om de aktuelt er skjult eller udvidet).
- **Ny** – Åbn en menu, hvor hver kommando til gengæld åbner en dialogboks eller side, som giver dig mulighed for at tilføje en bestemt type element for det valgte. Tilgængelige kommandoer omfatter **Prognoseforsyning**, **Ordreforslag**, **Planlagt kanban**, **Ny produktionsordre**, **Indkøbsordre** og **Flytteordre**.
- **Varedisponering** – Kør varedisponering. Der vises en dialogboks, hvor du kan angive, hvilken plan der skal køres. Feltet **Behovsplan** er angivet til at matche det aktuelle filter.
- **Maks. færdigmelding** – Åbn siden **Maks. færdigmelding** for det produkt, der er defineret i det aktuelle filter.
- **Opdater ordreforslag** – Åbn siden **Ordreforslag**, der indeholder ordreforslag for det produkt eller den produktfamilie, der er defineret i det aktuelle filter.
- **Niveau** – Fordel ordreforslag i overensstemmelse med indstillingerne fra den dialogboks, der vises.
- **Materialeplanspolitik efter lokation** – Åbn siden **Varedisponering** for det produkt, der er defineret i det aktuelle filter.
- **Kanban-regel** – Åbn siden **Kanban-regler** for det produkt, der er defineret i det aktuelle filter.

### <a name="fasttabs"></a>Oversigtspaneler

Siden **Forsyningsplan** kan indeholde følgende oversigtspaneler:

- **Lager ved periodeafslutning** – I dette oversigtspanel vises lagerdataene for periodens afslutning i en grafisk fremstilling.
- **Forsyningsprofil** – Dette oversigtspanel viser forsyningsdataene i grafisk format. Det vises, når du vælger en **Forsyning**-node eller en linje under den i den øverste sektion.
- **Oversigt** – Dette oversigtspanel indeholder oversigtsdetaljer, der er relateret til den transaktionstype, som du valgte i den øverste sektion. Hvis du f.eks. vælger **Salg** under noden **Efterspørgsel**, viser dette oversigtspanel felter, der er relateret til salgsordrer, f.eks. **Ønskede salgsordrelinjer** eller **Totalbeløb**. Hvis du vælger **Produktionsordrer** i undernoden **Produktion** i noden **Forsyning**, viser dette oversigtspanel felter, der er relateret til produktionsordrer, f.eks. **Planlagte produktionsordrer** eller **Planlagt i alt**. Feltværdierne afhænger af den periode, du har valgt i den øverste sektion. 
- **\[Transaktionstype\] - \[Periode\]** – Dette oversigtspanel viser ordrer for den posteringstype og periode, som du har valgt i den øverste sektion. Navnet på oversigtspanelet afspejler disse valg. Det kan f.eks. hedde **Salgsordrer - Ordrebeholdning** eller **Produktionsordrer - Uge 37**.

### <a name="action-pane"></a>Handlingsrude

De følgende knapper er tilgængelige i handlingsruden:

- **Rediger filter** – Åbn dialogboksen **Rediger filter**, hvor du kan opdatere filterværdier og derefter åbne siden **Forsyningsplan** igen, der afspejler de opdaterede filterindstillinger.
- **Vis forsinkelser** – Fremhæv de relevante linjer i det øverste afsnit, hvis der er en forsinket ordre af den pågældende transaktionstype.

### <a name="factbox-pane"></a>Rude med faktaboks

Hvis du vil åbne ruden med faktaboksen for at se en faktaboks, skal du vælge **Relaterede oplysninger** ved højre kant på siden. Følgende faktabokse er tilgængelige på siden **Forsyningsplan**:

- **Varedetaljer** – Denne faktaboks viser grundlæggende oplysninger om det produkt, der er defineret i det aktuelle filter. Den er tom, hvis du har angivet en produktfamilie i filteret.
- **Handlinger** – Denne faktaboks viser handlinger for ordrer af den transaktionstype, du har valgt i den øverste sektion.
- **Forsinkelser** – Denne faktaboks viser forsinkelser for ordrer af den transaktionstype, du har valgt i den øverste sektion.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
