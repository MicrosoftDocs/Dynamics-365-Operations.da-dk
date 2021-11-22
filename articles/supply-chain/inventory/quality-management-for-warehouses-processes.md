---
title: Kvalitetsstyring for lagerstedsprocesser.
description: Dette emne indeholder oplysninger om kvalitetsstyring af funktionen for lagerstedsprocesser. Denne funktion udvider funktionerne til kvalitetsstyring og giver brugerne mulighed for at integrere kontrolelementer til vareprøver i modtagelsesprocessen på lagerstedet ved hjælp af den avancerede lokationsstyring.
author: Henrikan
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-02
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d81441fcc8cb86927923e76bd1a4d16a141ddc75
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571875"
---
# <a name="quality-management-for-warehouse-processes"></a>Kvalitetsstyring for lagerstedsprocesser.

[!include [banner](../includes/banner.md)]

Med funktionen _Kvalitetsstyring for lagerstedsprocesser_ kan du integrere kontrolelementer til vareprøver i modtagelsesprocessen på lagerstedet ved hjælp af den avancerede lokationsstyring. Lagerstedsarbejde kan genereres til automatisk at flytte lager til kvalitetskontrolstedet på basis af en procentdel eller et fast antal eller baseret på hver af *n*'te id. Når en kvalitetsordre er fuldført, kan arbejde automatisk genereres for at flytte lageret til det næste sted i processen, afhængigt af kvalitetsresultaterne.

Funktionen _Kvalitetsstyring for lagerstedsprocesser_ udvider funktionerne i forhold til grundlæggende kvalitetsstyring. Den giver mulighed for at oprette kvalitetsordrer for det lager, der sendes til kvalitetskontrolstedet, selvom der ikke altid kræves kvalitetsordrer. Derfor giver det mulighed for en let kvalitetskontrolproces, der er baseret på lagerstedsarbejde.

## <a name="turn-on-the-quality-management-for-warehouse-processes-feature"></a>Aktivere funktionen Kvalitetsstyring for lagerstedsprocesser

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Kvalitetsstyring for lagerstedsprocesser*

## <a name="key-benefits"></a>Vigtigste fordele

Funktionen _Kvalitetsstyring for lagerstedsprocesser_ genererer automatisk arbejde som en del af modtagelsesprocessen for at flytte det lagerantal, der kræves for kvalitetskontrol, til et kvalitetskontrolsted. Hvis det modtagne antal overstiger det antal, der kræves til kvalitetskontrol (ifølge vareprøveopsætningen), flyttes det overskydende antal til et indgående sted, der er defineret i opsætningen af lokationsvejledning. Når kvalitetsordren er valideret, genereres arbejdet automatisk for at flytte antallet af kvalitetsordren til en ny indgående eller en returlokation, baseret på valideringsresultatet og opsætning af lokationsvejledning. Den automatiske generering af arbejde, der kun har det antal, der skal flyttes til og fra kvalitetskontrol, udgør en integreret procesoplevelse.

> [!NOTE]
> Når funktionen _Kvalitetsstyring for lagerstedsprocesser_ er slået til, kan du stadig drage fordel af den manuelle proces. I den manuelle proces bruges lagerbevægelse og bevægelse efter skabelon til at få en lagermedarbejder til at oprette lagerstedsarbejde for at flytte lager fra et kvalitetskontrolsted til et nyt sted. Du kan også stadig oprette en indgående lokationsvejledning, der flytter lageret i sin helhed fra et modtagelsessted til et kvalitetskontrolsted uden at tage højde for opsætningen af vareprøven.

## <a name="quality-management-and-the-quality-management-for-warehouse-processes-feature"></a>Kvalitetsstyring og funktionen Kvalitetsstyring for lagerstedsprocesser

Når funktionen _Kvalitetsstyring for lagerstedsprocesser_ er slået til, ændres opsætningen af enheder for nøglelokationsstyring og kvalitetsstyring. I følgende illustration vises en oversigt over de enheder, der muliggør kvalitetsordrer for lagerstedsprocesser. Tekst i parentes angiver anbefalede handlinger, når kvalitetsstyringen blev anvendt, før funktionen _Kvalitetsstyring for lokationsstyringsprocesser_ blev aktiveret.

![Enheder for kvalitetsstyring.](media/quality-management-entity-diagram.png "Enheder for kvalitetsstyring")

## <a name="enablers-the-quality-item-sampling-and-quality-order-work-order-types"></a>Aktiveringer: Arbejdsordretyperne Kvalitetsvareprøve og Kvalitetsordre

Funktionen _Kvalitetsstyring for lagerstedsprocesser_ introducerer to typer af arbejdsordrer, der gør det muligt at oprette arbejde:

- **Kvalitetsvareprøve** – Denne arbejdsordretype bruges til at oprette arbejde, der flytter registreret lager til kvalitetskontrol.
- **Kvalitetsordre** – Denne arbejdsordretype bruges til at oprette arbejde, der flytter lager fra kvalitetskontrol til en ny lokation på basis af opsætningen af lokationsvejledning.

### <a name="work-classes-location-directives-and-work-templates"></a>Arbejdsklasser, lokationsvejledninger og arbejdsskabeloner

Arbejdsordretyperne _Kvalitetsvareprøve_ og _Kvalitetsordre_ bruges i lokationsvejledninger, arbejdsklasser og arbejdsskabeloner.

Før der automatisk kan oprettes lagerstedsarbejde for at flytte lager til kvalitetskontrol, skal du udføre disse trin for at konfigurere systemet.

1. Opret separate arbejdsklasser for arbejdsordretyperne _Kvalitetsvareprøve_ og _Kvalitetsordre_. På denne måde sikrer du, at det rette arbejde kan genereres automatisk ud fra de to arbejdsordretyper, og at dette arbejde derefter kan køres ved hjælp af mobilappen Lokationsstyring.
1. Konfigurer en arbejdsskabelon for hver arbejdsordretype:

    - Konfigurer en arbejdsskabelon, der bruger arbejdsordretypen _Kvalitetsvareprøve_, til automatisk at flytte registreret lager til et kvalitetskontrolsted.
    - Konfigurer en arbejdsskabelon, der bruger arbejdsordretypen _Kvalitetsordre_, til at flytte registreret lager fra et kvalitetskontrolsted, når kvalitetskontrollen er fuldført.

1. For hver arbejdsordretype skal du konfigurere lokationsvejledninger, der anvender de rette kvalitetskontrolsteder, som lageret skal flyttes til. Når kvalitetskontrollen er fuldført, sikrer lokationsvejledningen til arbejdsordretypen _Kvalitetsordre_, at der vælges et nyt destinationssted, så lageret kan flyttes væk fra kvalitetskontrolstedet.
1. Konfigurer de relevante menupunkter i mobilenheden, der skal understøtte flytning af modtaget lager til kvalitetskontrolstedet og flytning af lager, der består eller dumper kvalitetskontrollen, fra kvalitetskontrolstedet til et nyt sted.

Et trinvist eksempel, der viser, hvordan denne konfiguration fuldføres, finder du i [eksempelscenariet](#example-scenario) sidst i dette emne.

## <a name="enable-a-warehouse-for-quality-management"></a>Aktivere et lagersted til kvalitetsstyring

Før funktionen _Kvalitetsstyring for lagerstedsprocesser_ kan anvendes på et bestemt lagersted, skal du udføre disse trin for at gøre funktionen tilgængelig for det pågældende lagersted.

1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lagersteder**.
1. Vælg det lagersted, du vil aktivere til kvalitetsstyring.
1. I oversigtspanelet **Lagersted** skal du angive indstillingen **Aktivér kvalitetsordre for lagerstedsprocesser** til _Ja_. (Bemærk, at denne indstilling kun kan angives til _Ja_ for lagersteder, der bruger lagerstyringsprocesser).

Når indstillingen **Aktivér kvalitetsordre for lagerstedsprocesser** er angivet til _Ja_, styrer opsætningen af kvalitetstilknytningen, om funktionen til _Kvalitetsstyring af lagerstedsprocesser_ faktisk anvendes for det valgte lagersted. Du kan til enhver tid ændre indstillingen til _Nej_. Hvis dette er tilfældet, gælder funktionen ikke længere for lagerstedet, uanset opsætningen af kvalitetstilknytningen.

## <a name="quality-control"></a>Kvalitetskontrol

Funktionen _Kvalitetsstyring for lagerstedsprocesser_ styrer flere nøgleindstillinger for kvalitetstilknytninger og vareprøver.

### <a name="quality-associations"></a>Kvalitetstilknytninger

De enkelte [kvalitetstilknytningsposter](enable-quality-management.md) definerer det sæt test, det acceptable kvalitetsniveau og den vareprøveplan, der gælder for de kvalitetsordrer, der oprettes. Gør følgende for at konfigurere en kvalitetstilknytningspost.

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Kvalitetstilknytninger**.
1. Opret eller vælg kvalitetstilknytningsposten for den vare eller gruppe, du arbejder med, eller for alle varer.
1. I oversigtspanelet **Betingelser** skal du indstille feltet **Gældende lagerstedstype** til en af følgende værdier:

    - **Kun kvalitetsstyring for lagerstedsprocesser** – Aktivér funktionen _Kvalitetsstyring for lagerstedsprocesser_. Du kan kun vælge denne værdi, hvis referencetypen enten er *Indkøb* eller *Produktion*.
    - **Alle** – Deaktiver funktionen _Kvalitetsstyring for lagerstedsprocesser_. Vælg denne værdi for alle referencetyper undtagen *Indkøb* og *Produktion*.

> [!NOTE]
> Funktionen _Kvalitetsstyring for lagerstedsprocesser_ træder kun i kraft, hvis varen på kildedokumentlinjen bruger avancerede lokationsstyringsprocesser, og hvis indstillingen **Aktivér kvalitetsordre for lagerstedsprocesser** er angivet til _Ja_ for lagerstedet på kildedokumentlinjen.

Efterhånden som hver vare registreres (eller færdigmeldes), bestemmer systemet, hvilke kvalitetstilknytninger der gælder for den.

Når funktionen _Kvalitetsstyring for lagerstedsprocesser_ er slået til, indsættes den pågældende lagerstedstype logisk i den fjerde søgegruppe for søgehierarkiet i kvalitetstilknytning. Følgende tabel giver en logisk repræsentation af søgehierarkiet.

| Søgegruppe | Beskrivende tekst |
|---|---|
| Gruppe 1 | For hver kvalitetstilknytning skal du kontrollere værdierne af **Referencetype**, **Hændelsestype** og **Udførelsesmatch** i forhold til varen. Hvis der er et match i kildedokumentlinjen, skal du gå videre til gruppe 2. |
| Gruppe 2 | For hver kvalitetstilknytning skal du kontrollere værdien af **Varekode** (_Tabel_, _Gruppe_ eller _Alle_) i forhold til varen. _Tabe_ er mere specifik end _Gruppe_, og _Gruppe_ er mere specifik end _Alle_. Hvis der er et match for _Tabel_ (en bestemt vare), skal du gå videre til gruppe 3. Hvis der ikke er noget match for _Tabel_, skal du søge efter et match for _Gruppe_. Hvis der ikke findes et match for _Gruppe_, anvendes _Alle_. Hvis der er et match, skal du gå videre til gruppe 3. |
| Gruppe 3 | For hver kvalitetstilknytning skal du kontrollere værdierne af **Kontokode** og **Ressourcekode** i forhold til varen. Den logik, der anvendes, ligner den logik, der anvendes for værdien af **Varekode**. |
| Gruppe 4 | For hver kvalitetstilknytning skal du kontrollere værdien af **Gældende lagerstedstype** (_Kun kvalitetsstyring for lagerstedsprocesser_ er _Alle_) i forhold til varen. Hvis indstillingen **Aktivér kvalitetsordre for lagerstedsprocesser** er angivet til _Ja_ for lagerstedet på kildedokumentet, og varen på kildedokumentlinjen er angivet til _Brug lokationsstyringsprocesser_, gælder begge tilknytninger, hvor der er et match for _Kun kvalitetsstyring for lagerstedsprocesser_ og de tilknytninger, hvor der findes et match for _Alle_, hvis begge findes. Hvis indstillingen **Aktivér kvalitetsordre for lagerstedsprocesser** er indstillet til _Nej_ for lagerstedet på kildedokumentet, og varen på kildedokumentlinjen er angivet til _Brug lagerstedsstyringsprocesser_, gælder kun kvalitetsstyring. |

Du har f.eks. defineret et lagersted, hvor indstillingen **Aktivér kvalitetsordre for lagerstedsprocesser** er angivet til _Ja_, og du har to kvalitetstilknytninger, der er defineret for referencetypen *Indkøb*: én for alle varer og én for hændelsestypen *Registrering*. Den eneste forskel mellem de to kvalitetstilknytninger er værdien af **Gældende lagerstedstype**: Den er angivet til _Alle_ for én kvalitetstilknytning og _Kun kvalitetsstyring for lagerstedsprocesser_ for den anden. I dette tilfælde er begge kvalitetstilknytninger lige specifikke, og begge vil være gældende.

Værdien i feltet **Testgruppe** for kvalitetstilknytningerne er også en faktor. Dette felt definerer den testprocedure, der skal anvendes. Hvis værdien af **Testgruppe** er den samme for begge tilknytninger, oprettes kun én kvalitetsordre, for den kvalitetstilknytning, hvor værdien af **Gældende lagerstedstype** er _Kun kvalitetsstyring for lagerstedsprocesser_. Hvis **Testgruppe**-værdien ikke er den samme for begge tilknytninger, oprettes der to kvalitetsordrer. Den første kvalitetsordre oprettes for den kvalitetstilknytning, hvor værdien af **Gældende lagerstedstype** er _Kun kvalitetsstyring for lagerstedsprocesser_. Den anden kvalitetsordre oprettes for den kvalitetstilknytning, hvor værdien af **Gældende lagerstedstype** er _Alle_.

> [!NOTE]
> Værdien af _Kun kvalitetsstyring for lagerstedsprocesser_ regnes for at være mere specifik end _Alle_, når kriterierne for kvalitetstilknytningerne for gruppe 1 og 2 er ens, og når testgruppen er den samme. Der oprettes kun to kvalitetsordrer, når testgrupperne er forskellige.

#### <a name="reference-types"></a>Referencetyper

Når **Referencetype**-værdien er _Indkøb_, og den **Gældende lagerstedstype**-værdi er _Kun kvalitetsstyring for lagerstedsprocesser_, skal feltet **Hændelsestype** i oversigtspanelet **Proces** være indstillet til _Registrering_. _Registrering_ er den eneste understøttede hændelsestype for _Indkøb_-referencetypen, når du bruger funktionen _Kvalitetsstyring for lagerstedsprocesser_.

#### <a name="quality-processing-policy"></a>Politik for kvalitetsbehandling

Funktionen _Kvalitetsstyring for lagerstedsprocesser_ gør det muligt at oprette arbejde, der kun er baseret på vareprøver. Det giver derfor mulighed for en letvægtsproces. Det lager, som arbejdet oprettes på, afhænger af den vareprøve, der er knyttet til kvalitetstilknytningen. Når letvægtsprocessen bruges, efter at en arbejder har placeret antallet på kvalitetskontrolstedet, kan kvalitetsafdelingen oprette en kvalitetsordre manuelt, hvis der kræves en kvalitetsordre.

Feltet **Kvalitetsbehandlingspolitik** i oversigtspanelet **Proces for kvalitetsordre** styrer, om der også oprettes en kvalitetsordre, når der oprettes arbejde til at flytte en vare til kvalitetskontrolstedet. Dette felt kan indstilles til _Opret kvalitetsordre_ eller _Opret kun arbejde_. Standardværdien er _Opret kvalitetsordre_.

> [!NOTE]
> Uanset om du opretter kvalitetsordrer manuelt eller automatisk, opretter systemet automatisk arbejde til flytning af varer fra kvalitetskontrolstedet, når kvalitetsordren markeres som valideret.

Oprettelsen af kvalitetsordrearbejde er ikke relateret til opsætningen af kvalitetstilknytningen. Hvis der findes en arbejdsskabelon, der har **Arbejdsordretype**-værdien *Kvalitetsordre*, og hvis forespørgselskriterierne opfyldes for den pågældende arbejdsskabelon, vil validering af en kvalitetsordre udløse oprettelsen af kvalitetsordrearbejde.

#### <a name="referenced-item-sampling"></a>Vareprøve, der refereres til

Hver kvalitetstilknytning skal referere til en vareprøve. En vareprøve definerer det antal, der vil blive sendt til kvalitetskontrol. Den kan oprettes, så den kun gælder for kvalitetstilknytninger, hvor værdien af **Gældende lagerstedstype** er _Kun kvalitetsstyring for lagerstedsprocesser_. Hvis **Prøveudtagningsområde**-værdien for en vareprøve er _Last_ eller _Forsendelse_, eller **Angivelse af antal**-værdien er _Fuldt id_, kan der kun refereres til vareprøven af kvalitetstilknytninger, hvor værdien af **Gældende lagerstedstype** er _Kun kvalitetsstyring for lagerstedsprocesser_.

Hvis du definerer en vareprøve, der bruger _Kun kvalitetsstyring for lagerstedsprocesser_ som lagerstedstype, vil du modtage en fejl, hvis du forsøger at referere til den fra en kvalitetstilknytning, der ikke bruger funktionen _Kvalitetsstyring for lagerstedsprocesser_.

> [!NOTE]
> Vareprøver, der bruger fuld blokering, understøttes ikke for kvalitetstilknytninger, hvor feltet **Gældende lagerstedstype**, er angivet til _Kun kvalitetsstyring for lagerstedsprocesser_.

### <a name="item-sampling"></a>Stikprøve af vare

Vareprøver bestemmer, hvor ofte varer sendes til kvalitetskontrol. Funktionen _Kvalitetsstyring for lagerstedsprocesser_ introducerer begrebet _prøveudtagningsområde_. Systemet bruger prøveudtagningsområdet, når det evaluerer, om og hvordan der skal oprettes kvalitetsordrer og/eller arbejde for kvalitetsvareprøver og kvalitetsordrearbejde.

Hvis du vil definere vareprøver, skal du gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Vareprøve** og indstille feltet **Prøveudtagningsområde** til en af følgende værdier:

- **Ordre** – Kildedokumentlinjen danner basis for evaluering af, om og hvordan der skal oprettes kvalitetsordrer og/eller arbejde for kvalitetsvareprøver og kvalitetsordrearbejde. Denne værdi er standardværdien, og når den er valgt, fungerer systemet på samme måde, som når funktionen _Kvalitetsstyring for lagerstedsprocesser_ er slået til.
- **Last** – Laster vil blive anvendt som grundlag for evalueringen af, om og hvordan en kvalitetsordre og/eller et arbejde oprettes. Denne værdi er kun tilgængelig, når funktionen _Kvalitetsstyring for lagerstedsprocesser_ er slået til.
- **Forsendelse** – Forsendelser vil blive anvendt som grundlag for evalueringen af, om og hvordan en kvalitetsordre og/eller et arbejde oprettes. Denne værdi er kun tilgængelig, når funktionen _Kvalitetsstyring for lagerstedsprocesser_ er slået til.

> [!NOTE]
> Når feltet **Prøveudtagningsområde** er angivet *Last* eller *Forsendelse*, vil lastenheden og forsendelsesenhederne blive brugt, hvis de er tilgængelige. Hvis de ikke er tilgængelige, vil ordreenheden blive brugt.

Funktionen _Kvalitetsstyring for lagerstedsprocesser_ introducerer også værdien *Fuldt id* for feltet **Angivelse af antal**. Denne værdi understøtter oprettelsen af arbejde for kvalitetsordrer og kvalitetsvareprøver baseret på id'er. Når du vælger denne værdi, sker der følgende ændringer:

- Indstillingen **Opdelingsantal efter vare** og feltet **Pr. n. id** i oversigtspanelet **Proces** bliver tilgængeligt.
- Feltet **Værdi** i oversigtspanelet **Prøveantal** bliver utilgængeligt.
- Indstillingerne **Pr. opdateret antal**, **Sted** og **Id** er angivet til *Ja*, og indstillingerne kan ikke ændres.

Indstillingen **Opdelingsantal efter vare** bestemmer, om id-antallet evalueres pr. vare eller på tværs af alle varer i prøveudtagningsområdet. Produktvarianter behandles som samme vare. Denne indstilling styrer også, om id-antallet nulstilles for hver vare.

Værdien i feltet **Pr. n. id** bestemmer, hvor ofte der oprettes kvalitetsordrer i forhold til antallet af varer, der er registreret. En værdi på *3* vil f.eks. sende hver tredje vare til kvalitetskontrol, startende med den første vare. Værdien skal være større end 0 (nul).

Mens arbejdere modtager varer ved hjælp af mobilappen Lokationsstyring, kontrollerer systemet, om der er konfigureret en kvalitetstilknytning for hver indgående vare. Hvis der er konfigureret en kvalitetstilknytning, bruger systemet den vareprøvepost, der er konfigureret for den pågældende kvalitetstilknytning, til at bestemme, hvordan den skal oprette kvalitetsordrer, arbejde for kvalitetsvareprøver og indkøbsordrearbejde.

> [!NOTE]
> Når modtagelsesregistrering er udført i webklienten (ved hjælp af den lille registreringsside eller varemodtagelseskladden for indkøbsordrelinjer), oprettes der ikke arbejde for kvalitetsvareprøver, uanset opsætningen. I stedet for varer, der svarer til en kvalitetstilknytning, bruges den vareprøve, der refereres til, kun til at styre oprettelsen af kvalitetsordrer.

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Eksempler på automatisk oprettelse af kvalitetsordrer

I følgende eksempler vises, hvordan opsætningen af en kvalitetstilknytning og en tilknyttet vareprøve påvirker genereringen af kvalitetsordrer, når feltet **Gældende lagerstedstype** er angivet til _Kun kvalitetsstyring for lagerstedsprocesser_.

Når **Angivelse af antal**-værdien er _Fuldt id_, bestemmer feltet **Pr. n. id**, hvilke id'er der skal bruges til at oprette arbejde for kvalitetsvareprøver. Det første id går altid til kvalitetskontrol, og værdien i dette felt angiver, at hver *n*. id efter dette id også skal til kontrol.

**Referencetype**-værdien for følgende eksempler er _Indkøb_, og værdien for **Hændelsestype** er *Registrering*.

| Prøveudtagningsområde | Angivelse af antal | Pr. opdateret antal | Pr. lagringsdimension | Opdelingsantal efter vare | Pr. n. id | Resultat |
|---|---|---|---|---|---|---|
| Bestilling | Fuldt id | Ja _(låst/ikke redigerbart)_ | <p>Lokation: Ja</p><p>Id: Ja _(låst/ikke redigerbart)_</p> | Nej | 3 | <p>**Ordrelinjeantal: 100 EA**</p><ol><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 20 EA, LP1<p>Arbejde til kvalitetsvareprøve for 20 EA</p><p>Kvalitetsordre 1 for 20 EA</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 20 EA, LP2<p>Indkøbsordrearbejde for 20 EA (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 20 EA, LP3<p>Indkøbsordrearbejde for 20 EA (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 20 EA, LP4<p>Arbejde til kvalitetsvareprøve for 20 EA</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 20 EA, LP5<p>Indkøbsordrearbejde for 20 EA (læg-på-lager)</p></li></ol> |
| Bestilling | Fast antal = 1 | Ja | <p>Lokation: Ja</p><p>Id: Ja</p> | Nej | Ikke anvendelig | <p>**Ordrelinjeantal: 100**</p><ol><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 20 EA, LP1<p>Arbejde til kvalitetsvareprøve for 1 EA</p><p>Kvalitetsordre 1 for 1 EA</p><p>Indkøbsordrearbejde for 19 EA (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 20 EA, LP2<p>Arbejde til kvalitetsvareprøve for 1 EA</p><p>Kvalitetsordre 1 for 1 EA</p><p>Indkøbsordrearbejde for 19 (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 20 EA, LP3<p>Arbejde til kvalitetsvareprøve for 1 EA</p><p>Kvalitetsordre 1 for 1 EA</p><p>Indkøbsordrearbejde for 19 EA (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 20 EA, LP4<p>Arbejde til kvalitetsvareprøve for 1 EA</p><p>Kvalitetsordre 1 for 1 EA</p><p>Indkøbsordrearbejde for 19 EA (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 20 EA, LP5<p>Arbejde til kvalitetsvareprøve for 1 EA</p><p>Kvalitetsordre 1 for 1 EA</p><p>Indkøbsordrearbejde for 19 EA (læg-på-lager)</p></li></ol> |
| Bestilling | Procent = 10 | Nej | <p>Lokation: Nej</p><p>Id: Nej</p> | Nej | Ikke anvendelig | <p>**Ordrelinjeantal: 100 EA**</p><ol><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 50 EA, LP1<p>Arbejde til kvalitetsvareprøve for 10 EA</p><p>Kvalitetsordre 1 for 10 EA</p><p>Indkøbsordrearbejde for 40 EA (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 50 EA, LP2<p>Indkøbsordrearbejde for 50 EA (læg-på-lager)</p></li></ol> |
| Læs | Procent = 5 | Ja _(låst/ikke redigerbart)_ | <p>Lokation: Nej</p><p>Id: Nej</p> | Nej | Ikke relevant | <p>**Ordrelinjeantal: 500 EA**</p><p>**To laster: første last 200 EA, anden last 300 EA**</p><ol><li>Registrere kvittering i mobilappen Lokationsstyring for første last for 100 EA<p>Arbejde til kvalitetsvareprøve for 5 EA</p><p>Kvalitetsordre 1 for 5 EA</p><p>Indkøbsordrearbejde for 95 EA (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for første last for 100 EA<p>Arbejde til kvalitetsvareprøve for 5 EA</p><p>Kvalitetsordre 1 for 5 EA</p><p>Indkøbsordrearbejde for 95 EA (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for anden last for 300 EA<p>Arbejde til kvalitetsvareprøve for 15 EA</p><p>Kvalitetsordre 1 for 15 EA</p><p>Indkøbsordrearbejde for 285 EA (læg-på-lager)</p></li></ol> |
| Sortér | Procent = 10 | Ja | <p>Lokation: Ja</p><p>Id: Ja</p> | Nej | Ikke anvendelig | <p>**Ordrelinjeantal: 100**</p><ol><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 50 EA, LP1<p>Arbejde til kvalitetsvareprøve for 5 EA</p><p>Kvalitetsordre 1 for 5 EA</p><p>Indkøbsordrearbejde for 45 EA (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 50 EA, LP2<p>Arbejde til kvalitetsvareprøve for 5 EA</p><p>Kvalitetsordre 1 for 5 EA</p><p>Indkøbsordrearbejde for 45 (læg-på-lager)</p></li></ol> |
| Læs | Fuldt id | Ja _(låst/ikke redigerbart)_ | <p>Lokation: Ja</p><p>Id: Ja _(låst/ikke redigerbart)_</p> | Nej | 3 | <p>**To varer:**</p><ul><li>**Ordrelinjeantal for vare A: 120 EA (4 paller)**</li><li>**Ordrelinjeantal for vare B: 90 EA (3 paller)**</li></ul><p>**Én last, to lastlinjer med hver ordrelinje**</p><ol><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 30 EA, LP1<p>Arbejde til kvalitetsvareprøve for 30 EA</p><p>Kvalitetsordre 1 for 30 EA</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 30 EA, LP2<p>Indkøbsordrearbejde for 30 EA (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 30 EA, LP3<p>Indkøbsordrearbejde for 30 EA (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 30 EA, LP4<p>Arbejde til kvalitetsvareprøve for 30 EA</p><p>Kvalitetsordre 1 for 30 EA</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare B, 30 EA, LP5<p>Indkøbsordrearbejde for 30 EA (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare B, 30 EA, LP6<p>Indkøbsordrearbejde for 30 EA (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 30 EA, LP7<p>Arbejde til kvalitetsvareprøve for 30 EA</p><p>Kvalitetsordre 1 for 30 EA</p></li></ol> |
| Læs | Fuldt id | Ja _(låst/ikke redigerbart)_ | <p>Lokation: Ja</p><p>Id: Ja _(låst/ikke redigerbart)_</p> | Ja | 3 | <p>**To varer:**</p><ul><li>**Ordrelinjeantal for vare A: 120 EA (4 paller)**</li><li>**Ordrelinjeantal for vare B: 90 EA (3 paller)**</li></ul><p>**Én last, to lastlinjer med hver ordrelinje**</p><ol><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 30 EA, LP1<p>Arbejde til kvalitetsvareprøve for 30 EA</p><p>Kvalitetsordre 1 for 30 EA</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 30 EA, LP2<p>Indkøbsordrearbejde for 30 EA (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 30 EA, LP3<p>Indkøbsordrearbejde for 30 EA (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 30 EA, LP4<p>Arbejde til kvalitetsvareprøve for 30 EA</p><p>Kvalitetsordre 1 for 30 EA</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare B, 30 EA, LP5<p>Arbejde til kvalitetsvareprøve for 30 EA</p><p>Kvalitetsordre 1 for 30 EA</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare B, 30 EA, LP6<p>Indkøbsordrearbejde for 30 EA (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 30 EA, LP7<p>Indkøbsordrearbejde for 30 EA (læg-på-lager)</p></li></ol> |
| Læs | Procent = 10 | Ja _(låst/ikke redigerbart)_ | <p>Lokation: Nej</p><p>Id: Nej</p> | Nej | Ikke relevant | <p>**Ordrelinjeantal: 100 EA**</p><p>**Der oprettes ingen laster. Ordrens omfang anvendes.**</p><ol><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 50 EA, LP1<p>Arbejde til kvalitetsvareprøve for 5 EA</p><p>Kvalitetsordre 1 for 5 EA</p><p>Indkøbsordrearbejde for 45 EA (læg-på-lager)</p></li><li>Registrere kvittering i mobilappen Lokationsstyring for vare A, 50 EA, LP2<p>Arbejde til kvalitetsvareprøve for 5 EA</p><p>Kvalitetsordre 1 for 5 EA</p><p>Indkøbsordrearbejde for 45 EA (læg-på-lager)</p></li></ol> |

Når en arbejder validerer en af de kvalitetsordrer, der vises i den forrige tabel, genererer systemet automatisk kvalitetsordrearbejde for at flytte lager fra kvalitetskontrollens lokation til den lokation, der er defineret i lokalitetsvejledningen til arbejdsordretypen _Kvalitetsordre_. Du kan konfigurere enhver lokation til dette formål, f.eks. en retur- eller lagerlokation, afhængigt af testresultatet for kvalitetsordren. Du kan se et eksempel på denne opsætning i [eksempelscenariet](#example-scenario) i slutningen af dette emne.

Du kan genåbne en kvalitetsordre, der allerede er valideret, hvis det kvalitetsordrearbejde, der er relateret til flytning af lageret fra kvalitetskontrollens lokation, ikke har **Arbejdsstatus**-værdien *Lukket* eller *I gang*.

## <a name="process-insights-when-multiple-quality-associations-coexist"></a>Behandle indsigt, når der findes flere kvalitetstilknytninger

Der kan defineres mere end én kvalitetstilknytning, som anvendes på samme kildedokumentlinje, og feltet **Gældende lagerstedstype** kan angives til _Kun kvalitetsstyring for lagerstedsprocesser_ for nogle af disse kvalitetstilknytninger og _Alle_ for andre.

I følgende eksempel er værdien af **Referencetype** lig med _Indkøb_.

1. Den første kvalitetstilknytning er konfigureret på følgende måde:

    - **Gældende lagerstedstype:** *Kun kvalitetsstyring for lagerstedsprocesser*
    - **Varekode:** *A0001*
    - **Kontokode:** *Alle*
    - **Testgruppe:** *Kabinet*
    - **Vareprøve:** *5 pc'er*

1. Den anden kvalitetstilknytning er konfigureret på følgende måde:

    - **Gældende lagerstedstype:** *Alle*
    - **Varekode:** *Alle*
    - **Kontokode:** *Alle*
    - **Testgruppe:** *Kabinet*
    - **Vareprøve:** *1 pc'er*

1. Den tredje kvalitetstilknytning er konfigureret på følgende måde:

    - **Gældende lagerstedstype:** *Kun kvalitetsstyring for lagerstedsprocesser*
    - **Varekode:** *Alle*
    - **Kontokode:** *104*
    - **Testgruppe:** *Impedans*
    - **Vareprøve:** *Hvert andet id* (denne indstilling betyder, at det første, tredje, femte osv. id, der er modtaget, opretter en kvalitetsordre).

1. Den fjerde kvalitetstilknytning er konfigureret på følgende måde:

    - **Gældende lagerstedstype:** *Alle*
    - **Varekode:** *Alle*
    - **Kontokode:** *Alle*
    - **Testgruppe:** *Impedans*
    - **Vareprøve:** *5 pc'er*

1. Den femte kvalitetstilknytning er konfigureret på følgende måde:

    - **Gældende lagerstedstype:** *Alle*
    - **Varekode:** *Alle*
    - **Kontokode:** *Alle*
    - **Testgruppe:** *Kegle*
    - **Vareprøve:** *10 %*

En indkøbsordre på et antal af 10 af vare A0001 er nu oprettet for leverandør 104. Derefter registreres en indkøbsordrelinje med antallet 10 som modtaget på et id ved hjælp af mobilappen Lokationsstyring. Her er resultatet:

- Der er én kvalitetsordre fra den første kvalitetstilknytning for testgruppen *Kabinet*. Antallet er 5. Der er ingen kvalitetsordre fra den anden kvalitetstilknytning, da kriterierne for den første kvalitetstilknytning er mere specifikke i forhold til testgruppen *Kabinet*.
- Der er én kvalitetsordre for den tredje kvalitetstilknytning for testgruppen *Impedans*. Antallet er 10. Der er ingen kvalitetsordre fra den fjerde kvalitetstilknytning, da kriterierne for den første kvalitetstilknytning er mere specifikke i forhold til testgruppen *Impedans*.
- Der er én kvalitetsordre for den femte kvalitetstilknytning for testgruppen *Kegle*. Antallet er 1.

I forbindelse med oprettelsen af en kvalitetsordre for hver af de tre kvalitetstilknytninger oprettes der også arbejde for kvalitetsvareprøver. Det registrerede antal er kun 10. Men på grund af vareprøveopsætningen er summen af det antal kvalitetsordrer, der er oprettet for *Kun kvalitetsstyring for lagerstedsprocesser* til den gældende lagerstedstype, lig med 16, hvilket overstiger det fysisk registrerede antal på 10. Derfor oprettes der ikke arbejde for hele kvalitetsordreantallet (16), da der kun er 10 fysisk disponible for flytningen til det pågældende kvalitetskontrolsted. Den prioritet, der bruges til at oprette kvalitetsvareprøver, følger rækkefølgen for oprettelse af kvalitetsordrer:

- **Første kvalitetsordre (antal = 5):** Der oprettes arbejde til kvalitetsvareprøve for 5. Et antal på 5 (10 – 5) resterer til efterfølgende oprettelse af arbejde for kvalitetsvareprøver.
- **Anden kvalitetsordre (antal = 10):** Der oprettes arbejde til kvalitetsvareprøve for 5. Et antal på 0 (nul) resterer til efterfølgende oprettelse af arbejde for kvalitetsvareprøver.
- **Tredje kvalitetsordre (antal = 1):** Der oprettes intet arbejde til kvalitetsvareprøve.

Som en del af processen med at oprette kvalitetsordrer oprettes der en lagerblokering for et antal på 10. Der refereres til denne lagerblokering i forhold til hver af de tre kvalitetsordrer. Summen af kvalitetsordreantallet er 16.

Når kvalitetsordrerne valideres, forsøger systemet at oprette kvalitetsordrearbejde for hver kvalitetsordre, der er valideret. Da summen af kvalitetsordreantallet overstiger det antal, der faktisk er blokeret, og derfor er tilgængeligt til oprettelse af arbejde, kan der ikke oprettes kvalitetsordrearbejde for det fulde antal kvalitetsordrer, som vist her. (Dette eksempel er en fortsættelse af det foregående eksempel).

1. **Valider den anden kvalitetsordre, der er oprettet (antal = 10). Der oprettes kvalitetsordrearbejde for et antal på 4.**

    Oprettelsen af kvalitetsordrearbejde udløses af en ændring i lagerblokeringsantallet. Da summen af kvalitetsordreantallet var 16, vil validering af et antal på 10 medføre, at de resterende kvalitetsordreantal valideres som værende lig med 6. Lagerblokeringsantallet reduceres fra 10 til 6. Det reducerede antal på 4 tildeles oprettelse af kvalitetsordrearbejde.

2. **Valider den første kvalitetsordre, der er oprettet (antal = 5). Der oprettes kvalitetsordrearbejde for et antal på 5.**

    Oprettelsen af kvalitetsordrearbejde udløses af en ændring i lagerblokeringsantallet. Da summen af kvalitetsordreantallet var 6, vil validering af et antal på 5 medføre, at de resterende kvalitetsordreantal valideres som værende lig med 1. Lagerblokeringsantallet reduceres fra 6 til 1. Det reducerede antal på 5 tildeles oprettelse af kvalitetsordrearbejde.

3. **Valider den tredje kvalitetsordre, der er oprettet (antal = 1). Der oprettes kvalitetsordrearbejde for et antal på 1.**

    Oprettelsen af kvalitetsordrearbejde udløses af en ændring i lagerblokeringsantallet. Da summen af kvalitetsordreantallet var 1, vil validering af et antal på 1 medføre, at de resterende kvalitetsordreantal valideres som værende lig med 0 (nul). Lagerblokeringen fjernes (da lagerblokeringsantallet reduceres fra 1 til 0). Det reducerede antal på 1 tildeles oprettelse af kvalitetsordrearbejde.

> [!NOTE]
> Oprettelsen af kvalitetsordrearbejde afhænger af det antal lagerblokeringer, der refereres til i en eller flere kvalitetsordrer. Hvis summen af kvalitetsordreantallet overstiger det referererede lagerblokeringsantal, bestemmer den rækkefølge, kvalitetsordrerne valideres i, oprettelsen af kvalitetsordrearbejdet.

## <a name="canceling-quality-item-sampling-work"></a>Annullering af arbejde til kvalitetsvareprøve

Du kan annullere det arbejde, der er oprettet til kvalitetsvareprøver. Følg disse trin for at kontrollere, hvad der sker, når dette arbejde annulleres.

1. Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**.
1. Under fanen **Generelt** i oversigtspanelet **Arbejde** skal du angive indstillingen **Fjern registrering af modtagelse, når du annullerer arbejde** til en af følgende værdier:

    - **Ja** – Når arbejde til kvalitetsvareprøve annulleres, slettes den tilknyttede kvalitetsordre, og lageret er ikke længere registreret.
    - **Nej** – Når arbejde til kvalitetsvareprøve annulleres, slettes den tilknyttede kvalitetsordre ikke, og lageret er stadig registreret.

## <a name="cross-docking"></a>Cross-docking

Du kan have en opsætning af en kvalitetstilknytning, der opretter vareprøvearbejde. Men når cross-docking findes parallelt med en kvalitetstilknytning, der opretter kvalitetsarbejde for vareprøver, og hvis der kun er et tilstrækkeligt antal til at opfylde cross-docking, oprettes der kun vareprøvearbejde. I de tilfælde, hvor indstillingen **Aktivér kvalitetsordre for lagerstedsprocesser** er angivet til _Ja_ for tilgangslagerstedet, og feltet **Gældende lagerstedstype** er angivet til _Kun kvalitetsstyring for lagerstedsprocesser_ for en kvalitetstilknytning, prioriteres oprettelsen af arbejde til kvalitetsvareprøve højere end oprettelsen af cross-docking-arbejde. Hvis antallet overskrider behovet for cross-docking, opretter systemet stadig kun vareprøvearbejde.

## <a name="destructive-testing"></a>Destruktiv test

Du kan definere en testgruppe, der udfører destruktive test. Hvis der er tale om en destruktiv test, antages det, at antallet af varen, der testes, vil blive destrueret som en del af testen uanset testresultatet. Den måde, som _Kvalitetsstyring for lagerstedsprocesser_ understøtter destruktive test på, minder om den måde, kvalitetsstyring understøtter det på, når funktionen ikke er aktiveret. Inden kvalitetsordren kan valideres, skal den ansvarlige for kvalitetssikringen angive plukpladsen for det antal, der er blevet destrueret. Du kan registrere plukning på siden med kvalitetsordre ved at vælge **Lager \> Pluk** i handlingsruden. Når plukket for kvalitetsordreantallet er registreret, kan valideringen fuldføres.

## <a name="example-scenario"></a>Eksempelscenario

### <a name="prepare-the-scenario"></a>Forberede scenariet

Hvis du vil arbejde gennem dette scenarie, skal du forberede systemet på følgende måde:

- Sørg for, at der er installeret demodata på systemet, og vælg den juridiske enhed **USMF**.
- Slå funktionen _Kvalitetsstyring for lagerstedsprocesser_ til i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Konfigurer lagersted 51 til at bruge funktionen _Kvalitetsstyring til lagerstedsprocesser_ ved at følge disse trin:

    1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lagersteder**.
    1. Vælg lagersted 51.
    1. I oversigtspanelet **Lagersted** skal du angive indstillingen **Aktivér kvalitetsordre for lagerstedsprocesser** til *Ja*.

### <a name="quality-in-setup--move-to-the-quality-control-location"></a>Opsætning af kvalitet ind – Flyt til kvalitetskontrolstedet

Du skal nu forberede en basisopsætning, der gør det muligt for systemet at understøtte _Kvalitetsstyring for lagerstedsprocesser_ for lagersted 51. (Demodataene definerer et kvalitetsstyringssted, der kaldes *QMS*. Der refereres til denne placering flere gange i dette scenario). Du skal forberede følgende elementer som beskrevet i undersektionerne i dette afsnit:

- Arbejdsklasse
- Arbejdsskabelon
- Lokalitetsvejledning
- Stikprøve af vare
- Kvalitetstilknytning
- Menupunkter i mobilenhed

#### <a name="work-class-for-quality-in"></a>Arbejdsklasse for kvalitet ind

1. Gå til **Lokationsstyring \> Opsætning \> Arbejde \> Arbejdsklasser**.
1. Opret en arbejdsklasse, og angiv følgende værdier:

    - **Arbejdsklasse-id:** _QualityIn_
    - **Beskrivelse:** _Kvalitetsvareprøve_
    - **Arbejdsordretype:** _Kvalitetsvareprøve_

#### <a name="work-template"></a>Arbejdsskabelon

1. Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.
1. Angiv feltet **Arbejdsordretype** til _Kvalitetsvareprøve_.
1. Opret en arbejdsskabelon, og angiv følgende værdier:

    - **Arbejdsskabelon:** _51 Kvalitet_
    - **Beskrivelse af arbejdsskabelon:** _51 Kvalitet_

1. Føj en linje til arbejdsskabelonen, og angiv følgende værdier:

    - **Arbejdstype:** _Pluk_
    - **Arbejdsklasse-id:** _QualityIn_

1. Føj en linje mere til arbejdsskabelonen, og angiv følgende værdier:

    - **Arbejdstype:** _Læg på lager_
    - **Arbejdsklasse-id:** _QualityIn_

#### <a name="location-directive"></a>Lokationsvejledning

1. Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.
1. Angiv feltet **Arbejdsordretype** til _Kvalitetsvareprøve_.
1. Opret en lokationsvejledning, og angiv følgende værdier:

    - **Navn:** _51 til kvalitet_
    - **Arbejdstype:** _Læg på lager_
    - **Lokation:** 5
    - **Lagersted:** _51_

1. Føj en linje til lokationsvejledningen, og angiv følgende værdier:

    - **Fra antal:** _1_
    - **Til antal:** _1000000_

1. Opret en handling for lokationsvejledning, og angiv følgende værdi:

    - **Navn:** _Kvalitet_

1. Til den nye handling for lokationsvejledning skal du vælge **Rediger forespørgsel** og angive en **Område**-post, der indeholder følgende værdier:

    - **Tabel:** *Lokationer*
    - **Felt:** _Lokationsprofil-id_
    - **Kriterier:** *QMS*

1. Vælg **OK** for at gemme forespørgslen, og gem den nye lokationsvejledning.

Derefter skal du ændre rækkefølgen af de eksisterende lokationsvejledninger for indkøbsordrer til lagersted 51. Demodataene indeholder to lokationsvejledninger, der har **Arbejdsordretype**-værdien _Indkøb_: Den ene hedder _51 QMS_, og den anden hedder _51 PO Direct_. Hvis du vil sikre, at funktionen *Kvalitetsstyring for lagerstedsprocesser* anvendes for lagersted 51, skal du sørge for, at lokationsvejledningen _51 QMS_ ikke anvendes. Men i stedet for at slette denne lokationsvejledning (da du måske skal bruge den i fremtiden), kan du blot ændre rækkefølgen.

1. Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.
1. Indstil feltet **Arbejdsordretype** til _Indkøbsordre_.
1. Vælg sekvensnummer 5 for lokationsvejledningen _51 PO Direct_ på sekvenslisten.
1. Flyt den valgte sekvens op til sekvensnummer 4.
1. Kontrollér, at sekvensnummeret for lokationsvejledning _51 QMS_ nu er mindst 5.

#### <a name="item-sampling"></a>Stikprøve af vare

Funktionen _Kvalitetsstyring for lagerstedsprocesser_ har nogle nye vareprøveegenskaber. Værdien af **Prøveudtagningsområde** kan nu være _Ordre_, _Forsendelse_ eller _Last_, og værdien af **Prøveantal** kan nu være _Fuldt id_.

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Vareprøve**.
1. Opret en vareprøvepost, og angiv følgende værdier:

    - **Vareprøve:** _3. id_
    - **Beskrivelse:** _Hvert tredje id_
    - **Prøveudtagningsområde:** _Ordre_

1. I oversigtspanelet **Prøveantal** skal du angive feltet **Angivelse af antal** til _Fuldt id_.
1. I oversigtspanelet **Proces** skal du angive feltet **Pr. n. id** til _3_.
1. I sektionen **Pr. lagerdimension** skal du aktivere både **Lagersted** og **Lagerstatus**.

#### <a name="quality-associations"></a>Kvalitetstilknytninger

Opret en kvalitetstilknytning, der skal bruge den nye vareprøve.

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Kvalitetstilknytninger**.
1. Opret en kvalitetstilknytningspost, og angiv følgende værdier:

    - **Referencetype:** _Indkøb_
    - **Varekode:** _Tabel_
    - **Vare:** _M9201_
    - **Lokation:** _5_

1. I oversigtspanelet **Proces** skal du angive feltet **Hændelsestype** til *Registrering*.
1. I oversigtspanelet **Betingelser** skal du angive feltet **Gældende lagerstedstype** til *Kun kvalitetsstyring for lagerstedsprocesser*.
1. I oversigtspanelet **Kvalitetsordreproces** skal du angive feltet **Politik for kvalitetsbehandling** til _Opret kvalitetsordre_.
1. Højreklik i feltet **Testgruppe** i oversigtspanelet **Specifikationer**, og vælg derefter **Vis detaljer** for at åbne siden **Testgrupper**.
1. Opret en testgruppe under fanen **Oversigt** i det øverste gitter på siden **Testgrupper**, og angiv følgende værdier:

    - **Testgruppe:** _QMS_
    - **Beskrivelse:** _QMS test_
    - **Acceptabelt antal:** _100_
    - **Vareprøve:** _3. id_ (Vælg)

1. Tilføj en post for én test under fanen **Oversigt** i det nederste gitter, og angiv følgende værdier:

    - **Sekvens:** *1*
    - **Test:** *Kabinetmåling*

1. Under fanen **Test** på det nederste gitter skal du angive følgende værdier:

    - **Testvariabler:** *Bestået/Dumpet*
    - **Standardudfald:** *Bestået*

1. Gem den nye testgruppe, og luk siden **Testgrupper**.
1. Tilbage på siden **Kvalitetstilknytninger** skal du i feltet **Testgruppe** vælge **QMS**.
1. Gem posten.

#### <a name="mobile-device-menu-items-for-quality-in"></a>Menupunkter i mobilenheder til kvalitet ind

Hvis du vil fuldføre konfigurationen for at flytte varer til kvalitetskontrolstedet, skal du gøre arbejde til kvalitetsvareprøve tilgængeligt fra et menupunkt i en mobilenhed.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Vælg menupunktet **Læg indkøb på lager** på mobilenheden.
1. Tilføj arbejdsklasse-id'et **QualityIn** i oversigtspanelet *Arbejdsklasser*.

#### <a name="summary-your-setup-to-move-goods-to-quality-control"></a>Oversigt: din konfiguration til at flytte varer til kvalitetskontrol

Du har nu defineret en kvalitetstilknytning, der bruger funktionen *Kvalitetsstyring for lagerstedsprocesser* til at udløse oprettelsen af en kvalitetsordre. Du har konfigureret arbejds- og lokalitetsdataene for lagersted 51 for at sikre, at der oprettes bestemt arbejde, når der registreres indkøb for vare M9201. Denne opsætning sikrer, at hvert tredje registrerede id flyttes til en lokation (_QMS_), og at der vil blive oprettet en kvalitetsordre for id-antallet. Alt andet vil blive flyttet til Læg på lager i stedet for kvalitetskontrollens lokation.

### <a name="process-quality-management-work"></a>Behandle kvalitetsstyringsarbejde

1. Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Opret en indkøbsordre, og angiv følgende værdier:

    - **Angiv kreditorkonto:** *104*
    - **Lagersted:** *51*

1. Tilføj en indkøbsordrelinje, og angiv følgende værdier:

    - **Vare:** *M9201*
    - **Antal:** *20*
    - **Måleenhed:** *styk*
    - **Lagersted:** *51*

1. Skriv indkøbsordrenummeret ned, så du kan bruge det senere.
1. Gå til en mobilenhed eller emulator, der kører mobilappen Lokationsstyring, og log på lagersted 51 ved at bruge *51* som bruger-id og *1* som adgangskode.
1. Gå til **Indgående \> Købsmodtagelse**, og angiv følgende værdier:

    - **IO-num:** Nummeret på den indkøbsordre, du lige har oprettet
    - **Antal:** *5*
    - **Enhed:** *Styk*

1. Fortsæt med at modtage på linjen, *5 styk* ad gangen, indtil linjen er fuldt modtaget. (I alt vil der blive oprettet fire id'er).
1. Log af mobilappen Lokationsstyring.
1. Tilbage i webklienten skal du gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Find og åbn indkøbsordren.
1. Marker linjen for varenummer **M9201** i afsnittet *Indkøbsordrelinjer*, og vælg derefter **Indkøbsordrelinjer \> Arbejdsdetaljer**.
1. Bemærk, at den anden og tredje arbejdsoverskrift, der er oprettet, er almindeligt læg på lager-arbejde, hvorimod den første og fjerde arbejdsoverskrift fungerer som arbejde til kvalitetsvareprøve. Dette resultat er i overensstemmelse med opsætningen af vareprøven, der er konfigureret til at indsamle stikprøver fra hvert tredje id.

#### <a name="move-to-the-quality-control-location"></a>Flytte til kvalitetskontrollens lokation

Du skal nu flytte id'erne til deres tildelte lokationer. Første og fjerde id går til kvalitetskontrollens lokation, mens andet og tredje id går direkte til legeret.

1. Gå til en mobilenhed eller emulator, der kører mobilappen Lokationsstyring, og log på lagersted 51 ved at bruge *51* som bruger-id og *1* som adgangskode.
1. Gå til **Indgående \> Læg indkøb på lager**, og læg de enkelte id'er på lager fra den forrige procedure, indtil du har lukket hele arbejdet.

#### <a name="summary-process-quality-management-work"></a>Oversigt: Behandle kvalitetsstyringsarbejde

Du har nu kørt arbejde til kvalitetsvareprøve for første og fjerde id ved at flytte dem til kvalitetskontrollens lokation. Du har også lagt andet og tredje id på lager. Det næste trin er at udføre kvalitetsordretesten og -kontrol.

### <a name="quality-out-setup-move-from-the-quality-control-location-to-storage-or-return"></a>Opsætning af kvalitet ud: flytte fra kvalitetskontrollens lokation til lager eller retur

Når arbejdere rapporterer resultater for kvalitetsordre, genererer systemet automatisk arbejde.

Du skal nu fortsætte med den nødvendige basisopsætning af arbejdsklassen, arbejdsskabelonen -og lokationsvejledningen for at aktivere kvalitetsstyring for lagerstedsprocesser, så det nødvendige arbejde kan oprettes for at flytte kvalitetsordreantallet fra kvalitetskontrollens lokation til en angivet lagerstedslokation.

#### <a name="work-class-for-quality-out"></a>Arbejdsklasse for kvalitet ud

1. Gå til **Lokationsstyring \> Opsætning \> Arbejde \> Arbejdsklasser**.
1. Opret en arbejdsklasse, og angiv følgende værdier:

    - **Arbejdsklasse-id:** *QualityOut*
    - **Beskrivelse:** *Kvalitet ud*
    - **Arbejdsordretype:** *Kvalitetsordre*

#### <a name="work-templates"></a>Arbejdsskabeloner

1. Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.
1. Ret værdien af **Arbejdsordretype** til *Kvalitetsordre*.
1. Opret en arbejdsskabelon, og angiv følgende værdier:

    - **Arbejdsskabelon:** *51 kvalitet ud*
    - **Beskrivelse af arbejdsskabelon:** *51 kvalitet ud*

1. Tilføj en linje, og angiv følgende værdier:

    - **Arbejdstype:** *Pluk*
    - **Arbejdsklasse-id:** **QualityOut**

1. Tilføj endnu en linje, og angiv følgende værdier:

    - **Arbejdstype:** *Læg på lager*
    - **Arbejdsklasse-id:** *QualityOut*

#### <a name="location-directives"></a>Lokationsvejledninger

1. Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.
1. Ret værdien af **Arbejdsordretype** til *Kvalitetsordre*.
1. Opret en lokationsvejledning, og angiv følgende værdier:

    - **Navn:** *51 Bestået*
    - **Arbejdstype:** *Læg på lager*
    - **Lokation:** *5*
    - **Lagersted:** *51*

1. I handlingsruden skal du vælge **Rediger forespørgsel** for at åbne dialogboksen med forespørgselseditoren.
1. På fanen **Område** skal du angive følgende værdier:

    - **Tabel:** *Kvalitetsordrer*
    - **Felt:** *Status*
    - **Kriterier:** *Bestået*

1. Vælg **OK** for at gemme forespørgslen og lukke dialogboksen.
1. Tilføj en linje i oversigtspanelet **Linjer**, og angiv følgende værdier:

    - **Fra antal:** *1*
    - **Til antal:** *1000000*

1. I oversigtspanelet **Handlinger i lokationsvejledning** skal du tilføje en række og angive følgende værdi:

    - **Navn:** *Bestået*

1. I handlingsruden oversigtspanelet **Handlinger i lokationsvejledning** skal du vælge **Rediger forespørgsel** for at åbne dialogboksen med forespørgselseditoren.
1. På fanen **Område** skal du angive følgende værdier:

    - **Tabel:** *Lokationer*
    - **Felt:** *Zone-id*
    - **Kriterier:** *Bulk*

1. Vælg **OK** for at gemme forespørgslen og lukke dialogboksen.
1. Vælg **Gem** i handlingsruden for at gemme den nye lokationsvejledning.
1. Opret en lokationsvejledning mere, og angiv følgende værdier:

    - **Navn:** *51 Dumpet*
    - **Arbejdstype:** *Læg på lager*
    - **Lokation:** *5*
    - **Lagersted:** *51*

1. I handlingsruden skal du vælge **Rediger forespørgsel** for at åbne dialogboksen med forespørgselseditoren.
1. På fanen **Område** skal du angive følgende værdier:

    - **Tabel:** *Kvalitetsordrer*
    - **Felt:** *Status*
    - **Kriterier:** *Dumpet*

1. Vælg **OK** for at gemme forespørgslen og lukke dialogboksen.
1. Tilføj en linje i oversigtspanelet **Linjer**, og angiv følgende værdier:

    - **Fra antal:** *1*
    - **Til antal:** *1000000*

1. I oversigtspanelet **Handlinger i lokationsvejledning** skal du tilføje en række og angive følgende værdi:

    - **Navn:** *Dumpet*

1. I handlingsruden oversigtspanelet **Handlinger i lokationsvejledning** skal du vælge **Rediger forespørgsel** for at åbne dialogboksen med forespørgselseditoren.
1. På fanen **Område** skal du angive følgende værdier:

    - **Tabel:** *Lokationer*
    - **Felt:** *Zone-id*
    - **Kriterier:** *Retur*

1. Vælg **OK** for at gemme forespørgslen og lukke dialogboksen.
1. Vælg **Gem** i handlingsruden for at gemme den nye lokationsvejledning.

#### <a name="mobile-device-menu-items-for-quality-out"></a>Menupunkter i mobilenheder til kvalitet ud

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Vælg menupunktet **Læg QMS på lager** på mobilenheden.
1. Tilføj arbejdsklasse-id'et **QualityPut** i oversigtspanelet *Arbejdsklasser*.

Lagermedarbejderne vil nu kunne plukke kvalitetsordrearbejde ved hjælp af menupunktet **Læg QMS på lager**. Varer, der har dumpet kvalitetskontrollen, kan lægges på en returlokation, og de varer, der er bestået, kan lægges på lokation bulk-001.

#### <a name="summary-your-setup-to-move-goods-from-quality-control"></a>Oversigt: din konfiguration til at flytte varer fra kvalitetskontrol

Du har konfigureret arbejds- og lokalitetsdataene for lagersted 51 for at sikre, at der automatisk oprettes arbejde, når kvalitetsordrer er fuldført. Denne opsætning sikrer, at hvert kvalitetskontrollerede id flyttes til enten en bulk-lokation eller en returlokation.

### <a name="process-quality-management-work"></a>Behandle kvalitetsstyringsarbejde

1. Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Kvalitetsordrer**.
1. Vælg den første kvalitetsordre for de antal, der er registreret.
1. Vælg **Valider**. Status for testen er opdateret til *Dumpet*.
1. Gå til **Lokationsstyring \> Alt arbejde**.
1. Åbn det arbejde, du lige har oprettet, og bemærk, at værdien af **Arbejdsordretype** er *Kvalitetsordre*. Arbejdet omfatter en linje, hvor lokationen er *Retur*, og statussen er *Dumpet*. (Hvis status for kvalitetsordren var *Bestået*, er læg på lager-lokationen i stedet *Bulk*).
1. Gå tilbage til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Kvalitetsordrer**.
1. Vælg den anden kvalitetsordre for de varer, der er registreret.
1. Vælg **Resultater** over det nederste gitter. Opdater værdien af **Antalsresultat** til *5*, og kontrollér, at værdien af **Testresultat** er ændret til en markering.
1. Vælg **Valider**, og luk siden.
1. Tilbage på siden **Kvalitetsordrer** skal du vælge **Valider** og foretage valideringen. Status opdateres til *Bestået*.

    > [!NOTE]
    > Valideringshændelsen udløser oprettelsen af kvalitetsordrearbejdet for at flytte antallet fra kvalitetskontrollokationen til en ny lokation.

1. Gå til **Lokationsstyring \> Alt arbejde**.
1. Vælg det arbejde, der netop er oprettet, og læg mærke til, at der er oprettet endnu et hoved for en kvalitetsordre, hvor læg på lager-lokationen er *BULK-001*.
1. Gå til en mobilenhed eller emulator, der kører mobilappen Lokationsstyring, og log på lagersted 51 ved at bruge *51* som bruger-id og *1* som adgangskode.
1. Gå til **Kvalitet \> Læg på lager fra QMS**, og behandl de to id'er, der er relateret til begge arbejdsopgaver, så alt arbejde er lukket.

> [!NOTE]
> Overvej at føje kvalitet ud-posten til et menupunkt i en mobilenhed, hvor aktivitetskoden er *Vis åben arbejdsliste*. Du kan finde et eksempel i menupunktet på mobilenheden, der hedder **Opgaveliste** i demodataene. Du skal først føje arbejdsklassen *Kvalitetsordre* til et brugerstyret menupunkt, da denne arbejdsopgave er nødvendig, for at arbejdet kan vises på opgavelisten. Føj derefter klassen *Kvalitetsordre* til menupunktet **Arbejdsliste**. Brugere, der har adgang til opgavelisten, vil derefter kunne plukke og behandle det arbejde, der automatisk genereres af en kvalitetsordrevalidering.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over styring af kvalitet og uoverensstemmelse](quality-management-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]