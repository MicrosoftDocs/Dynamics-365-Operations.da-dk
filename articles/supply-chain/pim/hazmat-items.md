---
title: Farlige materialer i produkter, ordrer, forsendelser og laster
description: Dette emne forklarer, hvordan du angiver egenskaber for farligt materiale for frigivne produkter, hvordan du kan lægge lagergrænser på farlige varer, og hvordan farligt materiale medtages i en salgsordre, forsendelse eller last.
author: dasani-madipalli
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 0bf4ff2188d98adb0052e40a77ff899d4da28063b042947bf124042dfa3fb8cd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758514"
---
# <a name="hazardous-materials-in-products-orders-shipments-and-loads"></a>Farlige materialer i produkter, ordrer, forsendelser og laster

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du angiver egenskaber for farligt materiale for frigivne produkter, hvordan du kan lægge lagergrænser på farlige varer, og hvordan farligt materiale medtages i en salgsordre, forsendelse eller last.

## <a name="set-hazardous-material-specifications-for-products"></a>Angive specifikationer af skadelige materiale for produkter

Når du har defineret en forordning for farligt materiale og konfigureret de relaterede referencekoder som beskrevet i afsnittet [Konfigurere farligt materiale](hazmat-setup.md), kan du knytte disse oplysninger til frigivne varer. Forsendelsesteksten til forsendelsesdokumenterne trækkes fra oplysningerne om farligt materiale for de frigivne varer.

Som en del af den proces, hvor en frigivet vare knyttes til farligt materiale, skal du angive forordningskoden og materialet. Forskellige forordningskoder kan knyttes til en vare, afhængigt af transportmåderne, og du kan knytte flere forordninger og materialekoder til hver vare.

Hvis du vil konfigurere et frigivet produkt som farligt materiale, skal du følge disse trin.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg eller opret et produkt for at åbne dets side for **Frigivne produktdetaljer**.
1. I oversigtspanelet **Styr lager** skal du angive indstillingen **Farligt materiale** til **Ja**. Denne indstilling identificerer varen som farligt gods og bruges, når forsendelsesdokumentationen udskrives.
1. I handlingsruden under fanen **Styr lager** skal du i gruppen **Overholdelse** vælge **Varen er farligt gods**.
1. Udfyld **Varen er farligt gods** for den valgte vare ved hjælp af de felter, der er beskrevet i følgende underafsnit.

### <a name="item-hazardous-materials-header"></a>Overskrift til vare med farligt gods

I følgende tabel beskrives de felter, der er tilgængelige øverst på siden **Varen er farligt gods**.

| Felt | Beskrivelse |
|---|---|
| varenummer | Det frigivne produkt, du arbejder med. |
| Forordningskode | Vælg den forordning for farligt materiale, der gælder for produktet. Forordningen definerer, hvordan den udskrevne forsendelsestekst oprettes for en vare og de tilhørende leveringsmåder. Når den er tildelt, kan koden ikke redigeres på denne side. Du kan dog tildele en ny forordningskode ved at vælge **Ny**. |
| Materialekode | (Valgfrit) Vælg den kode for farligt materiale, der gælder for produktet. Materialekoden har en skabelon, der indeholder standardværdier for mange andre felter på siden. Når du vælger en kode, kopieres alle specifikationer af farligt materiale til det aktuelle produkt. Systemet beder dig dog først om at bekræfte, at varematerialedata skal udfyldes fra materialekoden. |
| Gruppekode | (Valgfrit) Vælg den klassifikationsgruppekode for farligt materiale, der gælder for produktet. Når du vælger en kode i feltet **Materialekode**, kopieres alle specifikationer af farligt materiale til det aktuelle produkt. Systemet beder dig dog først om at bekræfte, at vareklassegruppedata skal udfyldes fra gruppekoden. |

### <a name="descriptions-fasttab"></a><a name="hazmat-description"></a>Oversigtspanelet Beskrivelser

I følgende tabel forklares de felter, der er tilgængelige i oversigtspanelet **Beskrivelser**.

| Felt | Beskrivelse |
|---|---|
| Korrekt forsendelsesnavn | Angiv standardbeskrivelsen af materialet, som er specificeret i den gældende forordning. Du kan angive oversættelser af denne værdi i oversigtspanelet **Oversættelse af tekst til vareforsendelse** som beskrevet i næste afsnit. |
| Teknisk navn | Vælg det almindelige eller generelle navn til materialet. Dette navn kan være et navn, som dit firma bruger internt for materialet. |
| N.O.S. | Markér dette afkrydsningsfelt for at angive, at værdien af **Korrekt forsendelsesnavn** er et andet end-specifikt (N.O.S.) forsendelsesnavn for varen. N.O.S. forsendelsesnavne bruges til grupper af lignende kemikalier og materialer, der har specifikke slutanvendelser, men som ikke vises efter navn i tabellen over farlige materialer i en bestemt forordning. |

### <a name="item-ship-text-translation-fasttab"></a>Oversigtspanelet Oversættelse af tekst til vareforsendelse

Oversigtspanelet **Oversættelse af tekst til vareforsendelse** indeholder et gitter, der viser oversættelser af de værdier af **Korrekt forsendelsesnavn**, der er defineret for det primære sprog i oversigtspanelet **Beskrivelse**. Disse oversættelser kan bruges til forsendelsers trykte tekst på et eller flere ekstra sprog.

I følgende tabel forklares de felter, der er tilgængelige i oversigtspanelet **Oversættelse af tekst til vareforsendelse**.


| Felt | Beskrivelse |
|---|---|
| Sprog | Den sprogkode, som rækken bruger. F.eks. angiver **pt-br** brasiliansk portugisisk. |
| Tekst til forsendelsesudskrift | Den oversatte værdi af **Korrekt forsendelsesnavn** på det sprog, som rækken bruger. |

Hvis du vil tilføje eller redigere en oversættelse, skal du vælge **Oversættelser** over gitteret for at åbne siden **Tekstoversættelser**. Udfør derefter ét af følgende trin:

- Hvis du vil tilføje en ny oversættelse, skal du vælge **Tilføj** i handlingsruden. Vælg det sprog, du vil tilføje, og angiv derefter den oversatte tekst i feltet **Oversat tekst**.
- Hvis du vil redigere en eksisterende oversættelse, skal du vælge et målsprog i feltet **Sprog** og redigere den oversatte tekst i feltet **Oversat tekst** efter behov.

### <a name="material-management-fasttab"></a><a name="material-management"></a>Oversigtspanelet Materialestyring

I følgende tabel forklares de felter, der er tilgængelige i oversigtspanelet **Materialestyring**.

| Felt | Beskrivelse |
|---|---|
| Klasse | Vælg den farlige materialeklasse, som produktet tilhører og er defineret i den forordning, du skal være i overensstemmelse med. Du skal knytte både en division og en klasse til hvert produkt, der indeholder farligt materiale. |
| Beskrivelse | Den beskrivelse, der er defineret for den klasse, der er valgt i feltet **Klasse**. Feltet er skrivebeskyttet. |
| Division | Vælg den farlige materialedivision, som produktet tilhører og er defineret i den forordning, du skal være i overensstemmelse med. Divisionen er et undersæt af klassen. Du skal knytte både en division og en klasse til hvert produkt, der indeholder farligt materiale. |
| Identifikation | Vælg identifikationskoden for farligt materiale. Denne kode er typisk baseret på en FN-standard. |
| Pakkegruppe | Vælg den pakkegruppe, der gælder for varen. |
| Beskrivelse | Den beskrivelse, der er defineret for den gruppe, der er valgt i feltet **Pakkegruppe**. Feltet er skrivebeskyttet. |
| Pakkebeskrivelser | Vælg den relevante pakkebeskrivelseskode. Denne kode refererer til en beskrivelse, der angiver, hvordan produktet skal pakkes. |
| Etiketter for farligt materiale | Vælg en kode, der refererer til den relevante etiket for farligt gods, som skal anvendes til produktet. |
| Begrænset antal | Angiv denne indstilling til **Ja** for at rapportere den samlede produktvægt, der er medtaget i hver last og på hver lastlinje. |
| Kvantitet | Angiv mængden af farligt materiale i produktet i den angivne enhed. Denne værdi bruges til at beregne den samlede score af farligt materiale for laster og forsendelser, der indeholder produktet. |
| Multiplikator | Angiv den multiplikator, der anvendes, når score for farligt materiale beregnes for hver lastlinje, der indeholder produktet. Denne værdi er specificeret i den gældende forordning, afhængigt af hvilken type farligt materiale der findes i produktet. |
| Enhed | Vælg den måleenhed, der gælder for mængden af farligt materiale i produktet, som angivet i feltet **Antal**. Denne værdi bruges til at beregne den samlede score af farligt materiale for laster og forsendelser, der indeholder produktet. |

#### <a name="how-the-hazardous-material-score-is-calculated"></a>Sådan beregnes scoren for farligt materiale

Flere af de værdier, der er angivet i oversigtspanelet **Materialestyring** for et produkt, bruges til beregning af *score for farligt materiale* for hver lastlinje, der indeholder det pågældende produkt. Scoren beregnes ved hjælp af følgende formel:

Score for farligt materiale = *&lt;LineQty&gt;* × *&lt;HazmatQty&gt;* × *&lt;UnitConversion&gt;* × *&lt;Multiplier&gt;*

Her er en nøgle til formlen:

- *&lt;LineQty&gt;* er det produktantal, der er angivet for en lastlinje.
- *&lt;HazmatQty&gt;* er mængden af farligt materiale, der er angivet for et produkt i feltet **Antal** i oversigtspanelet **Materialestyring**.
- *&lt;UnitConversion&gt;* er en omregningsfaktor til omregning mellem den enhed, der bruges i lastlinjemængden, og den enhed, der er angivet for et produkt i feltet **Enhed** i oversigtspanelet **Materialestyring**.
- *&lt;Multiplier&gt;* er den multiplikator, der er angivet for et produkt i feltet **Multiplikator** i oversigtspanelet **Materialestyring**.

Denne score rapporteres for hver lastlinje, der indeholder et produkt, hvor disse værdier er angivet. Du kan finde flere oplysninger i afsnittet [Forsendelser, der indeholder farligt materiale](#hazmat-shipments) og [Laster, som indeholder farligt materiale](#hazmat-loads) senere i dette emne.

#### <a name="how-the-hazardous-material-weight-is-calculated"></a>Sådan beregnes vægten af farligt materiale

Laster og lastlinjer, der indeholder produkter, hvor indstillingen **Begrænset mængde** i oversigtspanelet **Materialestyring** er angivet til **Ja**, viser den samlede vægt af farligt materiale, som er beskrevet i afsnittet [Forsendelser, der indeholder farligt materiale](#hazmat-shipments) og [Laster, som indeholder farligt materiale](#hazmat-loads) senere i dette emne. Vægten af farligt materiale beregnes ved hjælp af følgende formel:

Vægt af farligt materiale = *&lt;LineQty&gt;* × *&lt;ProductWeight&gt;* × *&lt;UnitConversion&gt;*

Her er en nøgle til formlen:

- *&lt;LineQty&gt;* er det produktantal, der er angivet for en lastlinje.
- *&lt;ProductWeight&gt;* er den nettovægt, der er angivet for produktet, i den lagerenhed, der er angivet for produktet.
- *&lt;UnitConversion&gt;* er en omregningsfaktor til omregning mellem den enhed, der bruges til lastlinjemængden og den lagerenhed, der bruges til *&lt;ProductWeight&gt;*.

### <a name="transport-information-fasttab"></a>Oversigtspanelet Transportoplysninger

I følgende tabel forklares de felter, der er tilgængelige i oversigtspanelet **Transportoplysninger**.

| Felt | Beskrivelse |
|---|---|
| Transportkategori | Vælg den relaterede transportkategori. |
| Tunnelkode | Vælg den relaterede tunnelbegrænsningskode for varen. |
| Stuvning af farligt materiale | Vælg den referencekode, der skal bruges til håndtering af skibsfragt, når varen sendes via skibsfragt. |
| Luftfartøjstype | Vælg den flybegrænsning, der gælder for materialet, når det leveres via luftfragt. |
| Pakke - kun luftfragt | Baseret på den værdi, du har valgt i feltet **Flytype**, skal du vælge den pakkevejledningskode, der gælder, når produktet kun kan forsendes via fragtluftfartøj. |
| Pakning - luftfartøj til passagerer og gods | Baseret på den værdi, du har valgt i feltet **Flytype**, skal du vælge den pakkevejledningskode, der gælder, når produktet kan forsendes via enten fragtluftfartøj eller passagerfly. |
| IATA-stjerne | Angiv denne indstilling til **Ja** for at angive, at de lufttransportspecifikationer, der er angivet i dette oversigtspanel, er relateret til standarden for farligt gods hos den Internationale Luftfartssammenslutning (IATA). Dette felt er udelukkende til orientering. |
| Reaktion på nødstilfælde | Vælg den kode, der refererer til instruktioner for håndtering af materialet i en nødsituation. |

### <a name="environmental-information-fasttab"></a>Oversigtspanelet Miljøoplysninger

I følgende tabel forklares de felter, der er tilgængelige i oversigtspanelet **Miljøoplysninger**.

| Felt | Beskrivelse |
|---|---|
| Miljøfarligt | Angiv denne indstilling til **Ja** for at angive, at produktet er miljøfarligt. Brug dette felt til dine egne rapporteringsformål. |
| Forurenende marinestoffer | Angiv denne indstilling til **Ja** for at angive, at produktet giver havforurening. Brug dette felt til dine egne rapporteringsformål. |

## <a name="set-stock-limits-for-hazardous-products"></a><a name="stock-limits"></a>Angive lagerbeholdningsgrænser for farlige produkter

Af sikkerhedsårsager kan det være nødvendigt at begrænse den samlede mængde af et bestemt produkt, der kan lagres på en enkelt lokation. Hvis du vil angive lagergrænser for et frigivet produkt, skal du gøre følgende.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg et produkt for at åbne dets side for **Frigivne produktdetaljer**.
1. I handlingsruden under fanen **Styr lager** skal du i gruppen **Overholdelse** vælge **Rapporteringsdetaljer**.
1. Angiv de relevante værdier for det valgte produkt i felterne **Grænse for farlig lagerbeholdning** og **Grænse for advarsel om fare**.

Med rapporten **Grænse for farlig lagerbeholdning** kan du overvåge lagerbeholdningsniveauerne for de farlige materialer på lagerlokationen og sikre, at de forbliver under de sikkerhedsgrænser, der er fastsat her. Du kan finde flere oplysninger under [Rapporten Grænse for farlig lagerbeholdning](hazmat-reports.md#stock-limit-report).

## <a name="sales-order-transactions-that-include-hazardous-materials"></a>Salgsordretransaktioner med farligt materiale

Hvis du vil medtage et produkt, der er klassificeret som farligt materiale, på en salgsordre, skal du knytte den relevante fragtmand til salgsordren. Åbn salgsordren, og angiv derefter felterne for **Fragtmand** og **Fragttjeneste** efter behov i oversigtspanelet **Levering**.

Fragtmanden er også tilknyttet leveringsmåden. Derfor skal du sikre dig, at disse oplysninger er indrettet efter forordningen om farligt materiale. Med andre ord skal den leveringsmåde, der er angivet i forordningen om farligt materiale, svare til specifikationerne i salgsordrehovedet. På denne måde er forordningen, fragtmanden og tjenesten knyttet til de forsendelseslinjer, der bruges i en salgsordre.

Når en salgsordre er færdig og klar til at blive afsendt, kan den frigives til lagerstedet for at angive overførslen mellem salgs- og lagerstedsoperationer.

## <a name="shipments-that-include-hazardous-materials"></a><a name="hazmat-shipments"></a>Forsendelser, der omfatter farligt materiale

### <a name="view-hazardous-material-scores-for-each-shipment-line"></a>Se score for farligt materiale for hver forsendelseslinje

Siden **Forsendelsesdetaljer** for en forsendelse viser den samlede vægt af farligt materiale og pointværdier, der er beregnet for hver lastlinje, der er inkluderet i den pågældende forsendelse. Benyt følgende fremgangsmåde for at få vist score og vægt:

1. Gå til **Lagerstyringssted \> Forsendelser \> Alle forsendelser**.
1. Vælg en forsendelse for at åbne dens side for **Forsendelsesdetaljer**.
1. Inspicer linjerne i oversigtspanelet **Lastlinjer**. For hver linje kan du se beregninger af farligt materiale i følgende felter:

    - **Point for farligt materiale** – Dette felt viser det farlige materiales score for lastlinjen. Værdien beregnes ud fra de regler og værdier, der er fastsat for den gældende forordning og i opsætningen af frigivne produkter. Beregningen tager mængden på lastlinjen og henviser til multiplikatoren i [opsætningen af materialestyring](#material-management) for det frigivne produkt.
    - **Begrænset mængde af nettovægt** – For produkter, der er markeret med begrænsede mængder på grund af deres farlige materialeindhold, viser dette felt den samlede nettovægt for farligt indhold, der er medtaget på lastlinjen. Beregningen er baseret på de produkter, der er markeret som farligt materiale i opsætningen af frigivne produkter. Hvis en vare er markeret med begrænsede mængde, tager beregningen mængden på hver lastlinje og refererer til vægten i [opsætningen af materialestyring](#material-management) for det frigivne produkt.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-shipment"></a>Kontrollér, om der er kompatibilitet mellem farlige materialer, der er medtaget i en forsendelse

Systemet kan vurdere, om alle de farlige materialer, der er inkluderet i en forsendelse, er egnede til at blive leveret sammen. For at evaluere kompatibiliteten kontrollerer systemet den kompatibilitetsgruppe, der er tildelt hvert af de produkter, der er inkluderet i forsendelsen. Du kan finde flere oplysninger under [Kompatibilitetsgrupper for farligt materiale](hazmat-setup.md#compatibility-groups).

Udfør følgende trin for at køre kompatibilitetskontrollen.

1. Gå til **Lagerstyringssted \> Forsendelser \> Alle forsendelser**.
1. Vælg en forsendelse for at åbne dens side for **Forsendelsesdetaljer**.
1. I handlingsruden under fanen **Forsendelser** i gruppen **Handlinger** skal du vælge **Kompatibilitetskontrol**.

Du får vist en meddelelse, der oplyser dig om resultatet af kontrollen.

## <a name="loads-that-include-hazardous-materials"></a><a name="hazmat-loads"></a>Laster, som indeholder farligt materiale

### <a name="view-hazardous-material-scores-for-each-load-line"></a>Se score for farligt materiale for hver lastlinje

Siden **Lastdetaljer** for en last viser den samlede vægt af farligt materiale og pointværdier, der er beregnet for denne last og hver lastlinje. Benyt følgende fremgangsmåde for at få vist score og vægt:

1. Gå til **Lagerstyringssted \> Forsendelser \> Alle laster**.
1. Vælg en last for at åbne dens side med **Lastdetaljer**. (Du kan også åbne lastoplysninger ved at vælge et link fra en relateret forsendelse).
1. I oversigtspanelet **Last** kan du gennemgå den samlede score og vægt for farligt materiale for hele lasten ved at inspicere følgende felter:

    - **Point for farligt materiale** – Dette felt viser det farlige materiales score for lasten. Værdien beregnes ud fra de regler og værdier, der er fastsat for den gældende forordning og i opsætningen af frigivne produkter. Beregningen tager mængden i lasten og henviser til multiplikatoren i [opsætningen af materialestyring](#material-management) for det frigivne produkt.
    - **Begrænset mængde af nettovægt** – For produkter, der er markeret med begrænsede mængder på grund af deres farlige materialeindhold, viser dette felt den samlede nettovægt for farligt indhold, der er medtaget i lasten. Beregningen er baseret på de produkter, der er markeret som farligt materiale i opsætningen af frigivne produkter. Hvis en vare er markeret med begrænsede mængde, tager beregningen mængden i hver last og refererer til vægten i [opsætningen af materialestyring](#material-management) for det frigivne produkt.

1. Hvis du vil have vist score og vægt for individuelle linjer, skal du vælge oversigtspanelet **Lastlinjer**. De værdier, der er angivet for hver linje, ligner de værdier, der er angivet for hele lasten, som beskrevet i det foregående trin.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-load"></a>Kontrollér, om der er kompatibilitet mellem farlige materialer, der er medtaget i en last

Systemet kan vurdere, om alle de farlige materialer, der er inkluderet i en last, er egnede til at blive leveret sammen. For at evaluere kompatibiliteten kontrollerer systemet den kompatibilitetsgruppe, der er tildelt hvert af de produkter, der er inkluderet i lasten. Du kan finde flere oplysninger under [Kompatibilitetsgrupper for farligt materiale](hazmat-setup.md#compatibility-groups).

Udfør følgende trin for at køre kompatibilitetskontrollen.

1. Gå til **Lagerstyringssted \> Forsendelser \> Alle laster**.
1. Vælg en forsendelse for at åbne dens side med **Lastdetaljer**. (Du kan også åbne lastoplysninger ved at vælge et link fra en relateret forsendelse).
1. I handlingsruden under fanen **Laster** i gruppen **Handlinger** skal du vælge **Kompatibilitetskontrol**.

Du får vist en meddelelse, der oplyser dig om resultatet af kontrollen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]