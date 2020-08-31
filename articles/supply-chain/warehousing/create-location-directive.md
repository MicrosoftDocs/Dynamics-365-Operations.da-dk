---
title: Oprette lokationsvejledninger
description: Dette emne forklarer, hvordan du opretter lokationsvejledninger. Lokationsvejledninger er brugerdefinerede regler, der hjælper med at identificere pluk og læg-lokationer for lagerbevægelser.
author: Mirzaab
manager: tfehr
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-28
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: bdd99b5faefd7054023b45a91fad070aac055a26
ms.sourcegitcommit: ecad92c9cb7e9e57688e678f79f747673c921df5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2020
ms.locfileid: "3692132"
---
# <a name="create-location-directives"></a>Oprette lokationsvejledninger

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du opretter lokationsvejledninger. Lokationsvejledninger er brugerdefinerede regler, der hjælper med at identificere pluk og læg-lokationer for lagerbevægelser. I en salgsordretransaktion bestemmer en lokationsvejledning eksempelvis, hvor varerne plukkes, og hvor de plukkede varer skal lægges på lager.

> [!NOTE]
> Dette emne gælder for funktioner i modulet **Lagerstedsstyring**. Det gælder ikke for funktioner i modulet [Lagerstyring](../inventory/inventory-home-page.md).

Du kan bruge lokationsvejledninger til at udføre følgende opgaver:

- Lægge indgående varer væk.
- Plukke og lægge varer på midlertidigt lager til udgående transaktioner.
- Plukke og lægge råvarer på lager til produktion.
- Genopfylde lokationer.

## <a name="prerequisites"></a>Forudsætninger

Før du kan oprette en lokationsvejledning, skal du følge disse trin for at sikre, at forudsætningerne er på plads.

1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lagersteder**.
1. Opret et lagersted.
1. På oversigtspanelet **Lagersted** skal du for indstillingen **Brug lagerstedsstyringsprocesser** vælge *Ja*.
1. Opret lokationer, lokationstyper, lokationsprofiler og lokationsformater. Yderligere oplysninger finder du i afsnittet [Konfigurere lokationer i et WMS-aktiveret lagersted](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).
1. Opret steder, zoner og zonegrupper. Yderligere oplysninger finder du i [Konfigurere lagersted](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) og [Konfigurere lokationer i et WMS-aktiveret lagersted](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).

## <a name="setup"></a>Konfiguration

### <a name="create-location-directives"></a>Oprette lokationsvejledninger

Udfør følgende trin for at oprette en lokationsvejledning:

1. Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.
1. I listeruden skal du angive feltet **Arbejdsordretype** til den type lagertransaktion, du opretter en lokationsvejledning for.
1. Vælg **Ny** i handlingsruden for at oprette en lokationsvejledning.
1. I forbindelse med den nye lokationsvejledningskal du angive felterne som beskrevet i følgende tabel.

    | Felt | Betegnelse |
    |---|---|
    | Løbenummer | Angiv et heltal for lokationsvejledningens placering i rækkefølgen. Placeringen i rækkefølgen bestemmer, hvornår den enkelte lokationsvejledning behandles for den valgte arbejdsordretype. |
    | Navn | Angiv et navn til lokationsvejledningen. | 
    | Arbejdstype | Vælg den arbejdstype, der skal udføres. Listen over værdier afhænger af den type lagertransaktion, som du har valgt i feltet **Arbejdsordretype**. Følgende værdier kan være tilgængelige:<ul><li>**Læg på lager** – Lokationsvejledningen vil forsøge at finde den bedste lokation til at placere eller finde lager, som tilføres systemet gennem modtagelse, produktion eller lagerreguleringer. Lokationsvejledningen bruges også til at definere læg på midlertidigt lager-lokationen eller afsendelsesstedet for den endelige lagerport i det udgående flow.</li><li>**Pluk** – Lokationsvejledningen vil forsøge at finde de bedste mulige lokationer til fysisk reservation af lager (oprette arbejde). Plukket kan fuldføres (og plukarbejdslinjen kan lukkes), selvom arbejdet ikke er fuldført. Brugeren kan fuldføre fysiske pluk. I systemet er denne handling et pluktrin. Brugeren kan derefter annullere fra mobilenheden og fuldføre arbejdet (f.eks. læg på lager) senere. Arbejdshovedet lukkes imidlertid først, når det endelige læg på lager er fuldført.</li><li>**Optælling**, **Reguleringer**, **Brugerdefineret**, **Ændring af lagerstatus**, **Id-opbygning**, **Udskrivning**, **Statusændring** og **Pak til indlejrede id'er** – Disse værdier kan ikke bruges i nogen opsætning af lokationsvejledning.</li></ul> |
    | Lokation | Vælg det sted, hvor arbejdet skal udføres. |
    | Lagersted | Vælg det lagersted, hvor arbejdet skal udføres. |
    | Vejledningskode | Vælg en vejledningskode, der skal styre valget af lokationsvejledninger, som er relateret til arbejdsskabelonens læg på lager-linjer, hvor denne kode er tildelt. På siden **Vejledningskode** kan du oprette nye koder, som kan bruges til at oprette forbindelse mellem en arbejdsskabelon og en lokationsvejledning. Du kan også bruge den pågældende side til at oprette forbindelse mellem enhver arbejdsskabelonlinje og en lokationsvejledning (f.eks. lagerporten eller den midlertidige lagerlokation). Yderligere oplysninger om, hvordan du konfigurerer en vejledningskode med en arbejdsskabelon, finder du under [Styre lagerarbejde ved at bruge arbejdsskabeloner og lokationsvejledninger](control-warehouse-location-directives.md).<p>Hvis der er angivet en vejledningskode, når arbejde skal genereres, søger systemet i lokationsvejledninger ved hjælp af vejledningskoden i stedet for placering i rækkefølgen. På denne måde kan du være mere præcis om den lokationsskabelon, der bruges til et bestemt trin i en arbejdsskabelon , f.eks. trinnet for midlertidig lagring af materialer.</p> |
    | Dispositionskode | Vælg en vejledningskode for at omdirigere læg på lager for de varer, der modtages på en lokation. (Yderligere oplysninger finder du i [Konfigurere dispositionskoder](tasks/set-up-dispositions-codes.md) .) Dette felt er kun tilgængeligt, når feltet **Arbejdsordretype** er angivet til *Indkøbsordrer*, *Returvareordrer* eller *Færdige varer, læg på lager*. |
    | Flere SKU'er | Angiv denne indstilling til *Ja* for at bruge flere lagerenheder (SKU'er) på en lokation. Denne indstilling skal f.eks. angives til *Ja* for lagerporten.<p>Hvis indstillingen **Flere SKU'er** er angivet til *Ja*, angives lagerlokationen til igangværende (som forventet). Lokationen kan dog kun håndtere flere varer, hvis arbejdet indeholder forskellige lagerenheder, der skal plukkes og lægges på lager, og ikke hvis arbejdet indeholder en enkelt SKU, der skal lægges på lager.</p><p>Hvis indstillingen **Flere SKU'er** er angivet til *Nej*, vil læg på lager-lokationen kun være angivet, hvis den kun har én type SKU.</p><p>Hvis du vil bruge begge fremgangsmåder, skal du angive to linjer med samme struktur og opsætning, men angiv indstillingen **Flere SKU'er** til *Ja* for en af linjerne og *Nej* for den anden. Med andre ord kræves der to identiske lokationsvejledninger til læg på lager-handlinger, selvom du ikke behøver skelne mellem enkelte og flere SKU'er i arbejds-id'et. Du skal også konfigurere en lokationsvejledning for lag på lager, hvis du har en ordre, som omfatter mere end én vare.</p><p>**Bemærk!** Hvis du angiver indstillingen **Flere SKU'er** til *Ja* til en lokationsvejledning af arbejdstypen *Læg på lager*, vil systemet altid vælge den første lokationsvejledningslinje uden hensyntagen til andre begrænsninger, der er oprettet i linjerne.</p> |

1. Valgfrit: Vælg **Rediger forespørgsel** i handlingsfruden for at vælge lokationer, eller angiv eventuelle begrænsninger, der gælder, når du vælger en bestemt lokationsvejledning.
1. I oversigtspanelet **LInjer** skal du oprette en eller flere linjer for at angive enheder og finde eller reservere antal på et lagersted.
1. På hver ny linje skal du angive felterne som beskrevet i følgende tabel.

    | Felt | Betegnelse |
    |---|---|
    | Løbenummer | Angiv et heltal for lokationsvejledningens placering i rækkefølgen. Placeringen i rækkefølgen bestemmer, hvornår den enkelte lokationsvejledning behandles for den valgte arbejdstype. |
    | Fra antal | Angiv starten på antalsintervallet for, hvornår den midterste gitterrækkefølge skal være valgt. Angiv antallet i den måleenhed, der er valgt i feltet **Enhed**. |
    | Antal til | Angiv slutningen på antalsintervallet for, hvornår den midterste gitterrækkefølge skal være valgt. Angiv antallet i den måleenhed, der er valgt i feltet **Enhed**. |
    | Enhed | Vælg måleenheden for varerne.<p>Du kan angive et minimumantal og et maksimumantal, som vejledningen skal gælde for. Du kan også angive, at vejledningen skal bruges til en bestemt lagerenhed. Feltet **Enhed** bruges kun til evaluering af antal.</p><p>Systemet evaluerer antallet ved hjælp af værdien **Enhed**, der er angivet på linjen, for at afgøre, om en lokationvejledningslinje gælder. Hver gang en lokationsvejledningslinje åbnes, forsøger systemet at konvertere efterspørgselsenheden til den enhed, der er angivet på linjen. Hvis enhedsomregningen ikke findes, vil systemet gå videre til næste linje.</p> |
    | Angiv lokalitet for antal | Dette felt er kun gyldigt, når du forsøger at lægge eller finde et antal på lagerstedet. Med andre ord er det kun gyldig for *Læg på lager*-arbejde. Vælg den metode, der bruges til at evaluere, om mængden er inden for det område, der er angivet i felterne **Fra antal** og **Til antal**. Hvis lokationsvejledningen er for en indgående transaktion, kan du vælge en af følgende indstillinger:<ul><li>**Id-antal** – For at evaluere, om et antal er inden for målantalintervallet kan du anvende antallet på det id-nummer, der modtages.</li><li>**Enhedsopdelt antal** – For at evaluere, om et antal er inden for målantalintervallet, kan du anvende det antal, der enhedsopdeles under transaktionen. Hvis du for eksempel på et lagersted kan modtage et antal på 1.000 og bryde det op i 10 id-numre, som hver har et antal på 100, kan du bruge et antal på 1.000 varer i stedet for id'ets antal på 100.</li><li>**Resterende antal** – For at evaluere, om et antal er inden for målantalintervallet, kan du bruge det antal, som stadig ikke er modtaget for den indkøbsordrelinje, der i øjeblikket modtages.</li><li>**Forventet antal** – For at evaluere, om et antal er inden for målantalintervallet, kan du bruge det samlede antal på indkøbsordrelinjen, uanset hvilket antal, der allerede er modtaget.</li></ul> |

1. Valgfrit: På oversigtspanelet **Linjer** kan du angive følgende supplerende felter.

    | Felt | Betegnelse |
    |---|---|
    | Begræns efter enhed | Markér dette afkrydsningsfelt for at begrænse de måleenheder, der betragtes som gyldige udvælgelseskriterier for lokationsvejledningslinjerne. Når måleenhederne er angivet, er det kun varer, hvor enheden svarer til mindst én enhed, der er defineret for enhedsseriegruppen, som betragtes som gyldige for linjevalget.<p>Enheden er f.eks. begrænset til paller, og varen er knyttet til en enhedsseriegruppe, der omfatter enheden *Paller*. I dette tilfælde anses varerne for at være en gyldig indstilling for lokationsvejledningen.</p><p>Afkrydsningsfeltet **Begræns efter enhed** bestemmer dog ikke, hvilken eller hvilke enheder der anvendes på arbejdslinjer. Enhedsbegrænsningen gælder kun for de enheder, der er tilgængelige via enhedsseriegruppen.</p><p>Eksempelvis en vare, der er tilknyttet en enhedsseriegruppe, der omfatter både enheden *Paller* og *stk.* Der er defineret en måleenhed, hvor 1 palle = 100 stk., og lokationsvejledningen kun bruger funktionen **Begræns pr . enhed** til paller. Desuden er der defineret en arbejdsskabelon, som begrænser oprettelsen af arbejdshoveder til 50 stk. I dette tilfælde oprettes der arbejdslinjer på 50 stk.</p><p>Benyt følgende fremgangsmåde for at angive måleenheden for begrænsning</p><ol><li>Vælg **Begræns pr. enhed** på oversigtspanelet **Linjer**. Denne knap bliver først tilgængelig, når du har markeret afkrydsningsfeltet **Begræns efter enhed** på linjen og derefter har valgt **Gem**.</li><li>I feltet **Enhed** skal du vælge den måleenhed for begrænsning for pluk og læg på lager-processer.</li></ol> |
    | Rund op til enhed | Vælg denne indstilling for at angive, at plukning af råvarer bør rundes op til et multiplum af den håndteringsenhed, der er angivet i feltet **Begræns efter enhed**. Dette felt gælder kun for pluk af råvarer og lokationsvejledninger af typen *Pluk*. |
    | Find emballagemængde | Markér dette afkrydsningsfelt, hvis en pakkeenheds antal er angivet på siden **Salgsordre**. Hvis du markerer dette afkrydsningsfelt, vælges kun de lokationer, der har med dette pakkeenhedsantal. |
    | Tillad opdeling | Markér dette afkrydsningsfelt for at opdele antallet på tværs af flere lokationer. |
    | Skabelon for øjeblikkelig genopfyldning. | Opret en forbindelse til en genopfyldningsskabelon, så opfyldningen startes, så snart varerne ikke er fordelt. Hvis du lader dette felt være tomt, starter varegenopfyldningen ikke, før alle linjer i lokationsvejledningen er blevet behandlet.<p>Dette felt er kun tilgængeligt for udvalgte arbejdsordretyper, hvor genopfyldning er tilladt, f.eks. *Salgsordrer* og *Råvarepluk*.</p> |

1. I oversigtspanelet **Handlinger for lokationsvejledninger** skal du klikke på **Ny** for at vælge lokationen eller serien af lokationer.
1. I feltet **Sekvensnummer** vises den rækkefølge, som lokationsvejledningen behandles i for den valgte arbejdstype. Du kan ændre rækkefølgen. Du skal dog være forsigtig med løbenumre til lokationsvejledningens handlinger, fordi locationsvejledningens handlinger altid køres i denne rækkefølge.
1. Angiv navnet på lokationsvejledningens handling i feltet **Navn**. Vær specifik, så det er tydeligt, hvad handlingen er.
1. Valgfrit: Vælg **Rediger forespørgsel** for at ændre lagerstederne og andre kriterier.
1. Valgfrit: Du kan angive følgende supplerende felter i for en lokationsvejledning.

    | Felt | Betegnelse |
    |---|---|
    | Anvendelse af fast lokation | Vælg, hvilke lokationer lokationsvejledningen skal tage i betragtning:<ul><li>**Faste og ikke-faste lokationer** – Lokationsvejledningen tager alle lokationer i betragtning.</li><li>**Kun faste lokationer for produktet** – Lokationsvejledningen tager kun faste lokationer for produkter i betragtning.</li><li>**Kun faste lokationer for produktvarianten** – Lokationsvejledningen tager kun faste lokationer for produktvarianter i betragtning.</li></ul> |
    | Tillad negativ lagerbeholdning | Markér dette afkrydsningsfelt for at tillade negativt lager på den angivne lagerlokation. |
    | Batchaktiveret | Marker dette afkrydsningsfelt for at bruge batchstrategier til de varer, der er batchaktiverede. Hvis dette afkrydsningsfelt er markeret, og feltet **Strategi** er angivet til *Ingen*, går systemet videre til den næste handlingslinje. |
    | Strategi | Vælg den strategi, som lokationsvejledningen skal anvende:<ul><li>**Ingen** – Der anvendes ingen strategi.</li><li>**Match emballagemængde** – Denne strategi kontrollerer, om en pluklokation har den angivne emballagemængde. Denne strategi er kun gyldig, når feltet **Arbejdstype** er angivet til *Pluk*.</li><li>**Konsolider** – Denne strategi konsoliderer varer på en bestemt lokation, når tilsvarende varer allerede er tilgængelige. Denne strategi er kun gyldig, når feltet **Arbejdstype** er angivet til *Læg på lager*. I en typisk opsætning til læg på lager, forsøger systemet at konsolidere på den første handlingslinje og forsøger derefter at lægge på lager uden konsolidering på den anden aktionslinje. Konsolidering af varer gør senere pluk mere effektive.</li><li>**FEFO-batchreservation** – Denne strategi bruges, når lageret lokaliseres ved hjælp af en batchudløbsdato, og det tildeles en batchreservation. Batchreservationsstrategien First Expiry, First Out (FEFO) anvendes også, når lageret lokaliseres ved hjælp af en sidste holdbarhedsdato for batchet ud over udløbsdatoen. Du kan kun bruge denne strategi til batchaktiverede varer. Denne strategi er kun gyldig, når feltet **Arbejdstype** er angivet til *Pluk*. Når du vælger denne strategi, tilsidesætter du enhver forespørgselssortering for de batchnumre, der anvendes.</li><li>**Rund op til fuld LP** – Denne strategi runder op til lagerantallet, så det svarer til antallet af id-numre, som er tildelt de varer, der skal plukkes. Denne strategi kan kun bruges til genopfyldningstypen for lokationsvejledninger, og kun når feltet **Arbejdstype** er angivet til *Pluk*.</li><li>**Tom lokation uden indgående arbejde** – Denne strategi bruges til at finde tomme lokationer. En lokation anses som tom, hvis den ikke har noget fysisk lager og intet forventet indgående arbejde. Denne strategi er kun gyldig, når feltet **Arbejdstype** er angivet til *Læg på lager*.</li></ul> |

## <a name="example-of-the-use-of-location-directives"></a>Eksempel på brug af lokationsvejledninger

I dette eksempel ser vi på en indkøbsordreproces, hvor lokationsvejledningen skal finde ledig kapacitet inden for et lagersted for lagervarer, der netop er registreret i modtagelsesområdet. Du skal først prøve at finde ledig kapacitet på lagerstedet ved at konsolidere med eksisterende disponibel lagerbeholdning. Hvis konsolideringen ikke er muligt, skal du finde en tom lokation.

I dette scenarie skal du definere to handlinger i lokationsvejledningen. Den første handling i rækken skal bruge strategien **Konsolider**, og den anden skal bruge strategien **Tom lokation uden indgående arbejde**. Medmindre du definerer en tredje handling for at håndtere et overløbsscenarie, er der to mulige udfald, når der ikke er mere kapacitet på lagerstedet. Arbejde kan oprettes, selvom ingen lokationer er defineret, eller processen til oprettelse af arbejde kan mislykkes. Resultatet bestemmes af opsætningen på siden **Fejl i lokationsvejledning**, hvor du kan beslutte, om du vil vælge indstillingen **Stop arbejdet ved fejl i lokationsvejledning** for hver arbejdsordretype.

## <a name="next-step"></a>Næste trin

Når du opretter lokationsvejledninger, kan du knytte hver vejledningskode til en arbejdsskabelonkode med henblik på arbejdsoprettelse. Få flere oplysninger under [Styre lagerarbejde ved hjælp af arbejdsskabeloner og lokationsvejledninger](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).

## <a name="technical-information-for-system-admins"></a>Tekniske oplysninger til systemadministratorer

Hvis du ikke har adgang til de sider, der bruges til at fuldføre denne opgave, skal du kontakte din systemadministrator og angive de oplysninger, der vises i følgende tabel.

| Kategori | Forudsætning |
|---|---|
| Konfigurationsnøgler | Gå til **Systemadministration \> Opsætning \> Licenskonfiguration**. Udvid licensnøglen **Handel**, og vælg derefter konfigurationsnøglen **Lagersteds- og transportstyring**. |
