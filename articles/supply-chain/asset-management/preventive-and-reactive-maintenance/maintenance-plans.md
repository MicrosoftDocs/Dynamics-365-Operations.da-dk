---
title: Vedligeholdelsesplaner
description: Denne artikel beskriver vedligeholdelsesplaner i Styring af aktiver.
author: johanhoffmann
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectType, EntAssetCounterType, EntAssetWorkOrderLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6303af9a9d4d4565deba9ca8893535554d03c274
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335009"
---
# <a name="maintenance-plans"></a>Vedligeholdelsesplaner

[!include [banner](../../includes/banner.md)]

En vedligeholdelsesplan definerer, hvornår et forud planlagt præventivt vedligeholdelsesjob skal udføres på et aktiv. Vedligeholdelsesplaner kan knyttes til aktiver, aktivtyper, arbejdssteder eller arbejdsstedstyper, men du skal først oprette de vedligeholdelsesplaner, der skal bruges i firmaet.

En vedligeholdelsesplan kan have flere vedligeholdelsesplanlinjer. Vedligeholdelsesjobtype og -interval er angivet på vedligeholdelsesplanlinjen. Der findes to typer vedligeholdelsesplanlinjer:

- Tid
- Tæller

Vedligeholdelsesplanlinjer af typen "Tid" bruges til tilbagevendende planlagt vedligeholdelse baseret på et fast tidsinterval. Vedligeholdelsesplanlinjer af typen "Tæller" bruges til planlagt vedligeholdelse eller reaktiv vedligeholdelse baseret på aktivtællerens registreringer. En vedligeholdelsesplan kan omfatte flere vedligeholdelsesplanlinjer af begge typer.

>[!NOTE]
>Hvis der ikke er registreret nogen tællerværdier for en tællertype på et aktiv, udelades vedligeholdelsesplanlinjerne.

Først skal du oprette de vedligeholdelsesplaner, du har brug for til dine præventive vedligeholdelsesjob, og vælge aktivtyper, aktiver, arbejdsstedstyper og arbejdssteder, der skal knyttes til hver vedligeholdelsesplan. Efterfølgende, hvis det er nødvendigt, kan du også føje vedligeholdelsesplaner til et aktiv eller et arbejdssted. Vælg **Alle aktiver** \> vælg oversigtspanelet \> **Vedligeholdelsesplaner** for aktiver, eller **Alle arbejdssteder** \> vælg arbejdssted \> oversigtspanelet **Vedligeholdelsesplaner**.

Hvis du føjer en vedligeholdelsesplan til aktivtyper eller arbejdsstedstyper, betyder det, at når du opretter nye aktiver eller arbejdssteder med disse aktivtyper eller arbejdsstedstyper, føjes aktivet eller arbejdsstedet automatisk til vedligeholdelsesplanen. Startdatoen for tilknytningen til en vedligeholdelsesplan vil være den aktuelle dato, der evt. skal tilpasses.

## <a name="set-up-maintenance-plans"></a>Konfigurer vedligeholdelsesplaner

I dette afsnit beskrives, hvordan du opretter vedligeholdelsesplanlinjer, og afsnittet indeholder eksempler på, hvordan de kan bruges.

1. Gå til **Styring af aktiver \> Opsætning \> Forebyggende vedligeholdelse \> Vedligeholdelsesplaner**.

1. Vælg **Ny** for at oprette en ny sekvens.

1. Indsæt et id i feltet **Vedligeholdelsessekvens** og et navn i feltet **Navn**.

1. Indsæt den startdato, hvorfra planlægningen kan udføres på vedligeholdelsesplanen, i feltet **Plandato**. Bemærk, at tidsbaserede vedligeholdelsesplanlinjer kan have andre plandatoer.

1. Vælg "Ja" under til/fra-knappen **Aktiv** for at aktivere vedligeholdelsesplanen.

    >[!NOTE]
    >Hvis du deaktiverer en vedligeholdelsesplan, vil der ikke blive oprettet nogen planlægningsposter i vedligeholdelsestidsplanen, når du kører et vedligeholdelsesplanlægningsjob.

1. Felterne **Tolerancedage før** og **Tolerancedage efter** er tilknyttet de vedligeholdelsesplanlinjer, hvor afkrydsningsfeltet **Undertryk overlappende vedligeholdelsesjob** er markeret (se trin 17). Hvis flere vedligeholdelsesplaner overlapper, bruges felterne "Tolerance" til at forlænge det interval i dage, hvor det mest omfattende eller største job oprettes som en vedligeholdelsestidsplanslinje under planlægningen af vedligeholdelsesplanen, mens hyppigere, overlappende job udelades under vedligeholdelsesplanlægningen. Indsæt antallet af dage i feltet **Tolerancedage før**, f.eks. "2".

1. Hvis du har indsat en værdi i **Tolerancedage før**, skal du også indsætte et antal dage i feltet **Tolerancedage efter**, f.eks. "2".

    >[!NOTE]
    >Det eksempel, der beskrives i dette og det foregående trin, betyder, at hvis flere vedligeholdelsesplanlinjer overlapper hinanden, og **Undertryk overlappende vedligeholdelsesjob** er markeret for en eller flere linjer, udvides perioden for udeladelse af vedligeholdelsestidsplanslinjer til i alt fem dage (den forventede startdato på vedligeholdelsesplanlinjen *og* to dage før *og* to dage efter denne dato).

1. Felterne i gruppen **Detaljer** i oversigtspanelet **Detaljer** viser antallet af vedligeholdelsesplanlinjer, der er oprettet i vedligeholdelsesplanen, og antallet af aktiver og arbejdssteder, der er knyttet til vedligeholdelsesplanen.

1. Vælg **Tilføj tidslinje** eller **Tilføj aktivtællerlinje** i oversigtspanelet **Linjer** for at oprette en ny vedligeholdelsesplanlinje.

1. Indsæt en beskrivelse for linjen i feltet **Beskrivelse af arbejdsordre**. Beskrivelsen overføres til de tilknyttede arbejdsordrer.

1. Vælg den jobtype, som vedligeholdelsesplanlinjen er knyttet til, i feltet **Vedligeholdelsesjobtype**.

1. I felterne **Vedligeholdelsesjobtypevariant** og **Fag** skal du vælge den variant og det fag, der er relateret til vedligeholdelsesjobtypen.

1. I felterne **Afslut inden for dage** og **Afslut inden for timer** kan du indsætte den forventede slutdato i dage eller timer. Den forventede slutdato indsættes i forhold til den forventede startdato, som beregnes, når der oprettes vedligeholdelsestidsplanlinjer. Du kan f.eks. indsætte "7" i feltet **Afslut inden for dage** for at angive, at det relaterede job skal fuldføres inden for en uge fra den forventede startdato.

1. I feltet **Intervaltype** skal du vælge den type interval, der skal bruges på vedligeholdelsesplanlinjen, f.eks. "Gentagne gange..." eller "Én gang...". Du kan se en beskrivelse af relationen mellem intervaltyper og linjetyper i tabellen [Oversigt over intervaltyper](#interval-types) nedenfor.

1. Feltet **Periode** er kun knyttet til tidsbaserede linjetyper. Vælg den periodetype, der er knyttet til periodefrekvensen.

1. Indsæt det antal gange, linjen skal bruges til planlægning af præventive vedligeholdelsesjob, i feltet **Periodefrekvens**. Eksempel: Hvis du har oprettet en linje af typen "Tæller", og tælleren er produktionsantallet, og du indsætter tallet "20000" i dette felt, oprettes der nye vedligeholdelsessekvenslinjer under planlægning af præventiv vedligeholdelse, hver gang du forventes at producere 20.000 flere varer.

1. Afkrydsningsfeltet **Undertryk overlappende vedligeholdelsesjob** er relateret til både tidsbaserede og tællerbaserede linjetyper. Marker afkrydsningsfeltet for at slette poster i vedligeholdelsestidsplanen, der er oprettet på samme dato. Dette er relevant, hvis du f.eks. har oprettet en 1-måneds inspektionslinje, en 6-måneders inspektionslinje og en 1-års inspektionslinje. For 1-års inspektion ønsker du kun, at denne inspektion skal udføres, ikke de to andre inspektioner, der også ville passe ind i tidsrammen. For at oprette dette eksempel korrekt skal du oprette 1-års inspektionslinjen som første linje, 6-måneders linjen som den anden linje og 1-måneds linjen som den tredje linje, og du skal markere afkrydsningsfeltet **Undertryk overlappende vedligeholdelsesjob** for 1-måneds og 6-måneders linjerne. På denne måde kan du sikre, at, når du kommer til 1-årsmærket, udelades inspektionerne for 1-måned og 6-måneder, og der oprettes kun en vedligeholdelsestidsplanslinje for 1-års inspektionslinjen.

    >[!NOTE]
    >Det eksempel, der beskrives i dette trin, viser, at det mest omfattende job, som indeholder det største antal opgaver, og som ikke udføres så ofte, altid skal indsættes som første linje. De hyppigere job indsættes derefter som separate linjer i frekvensrækkefølgen, så det mest almindelige job placeres nederst på listen.

1. Feltet **Tæller** er kun knyttet til tællerbaserede linjetyper. Vælg den tællertype, der skal bruges på linjen. Hvis en tællertype ikke er aktiv på et relateret aktiv, udelades vedligeholdelsesplanlinjen.

1. Feltet **Aktivtællerens tidshorisont i dage** er kun relateret til tællerbaserede linjetyper. Indsæt et tal, der definerer, hvor mange dage tilbage tællerregistreringer kontrolleres, når der foretages planlægning af vedligeholdelsesplanen. Det betyder, hvor langt tilbage der er data (eksisterende tællerregistreringer), der bruges som grundlag for beregning af den tendens, der bestemmer, hvor mange vedligeholdelsestidsplanslinjer der oprettes.

    >*Eksempel:* Hvis registreringen af tællere forventes at blive foretaget en gang om måneden, kan du indsætte tallet '365' i dette felt, da planlægning af vedligeholdelsesplanen altid er baseret på de seneste 12 måneder, og dermed oprette vedligeholdelsestidsplanslinjer på baggrund af tendensen for det sidste år. Hvis du derimod indsætter tallet '10' i dette felt, forventer du, at tællerregistreringer skal foretages hyppigere, f.eks. dagligt. Det betyder, at når du planlægger en vedligeholdelsesplan, bruges tællerregistreringerne for de seneste 10 dage som udgangspunkt for planlægningen af vedligeholdelsestidsplanslinjer.

1. Feltet **Plandato** er kun knyttet til tidsbaserede linjetyper. Hvis vedligeholdelsesplanlinjen har en anden planlægningsdato end hele vedligeholdelsesplanen, skal du vælge en dato i feltet **Plandato** på linjen.

1. I feltet **Serviceniveau** kan du vælge et serviceniveau for en arbejdsordre som en yderligere afgrænsning på linjen for vedligeholdelsesplanen – til brug som serviceniveau i en arbejdsordre.

1. Marker afkrydsningsfeltet **Automatisk oprettelse**, hvis der automatisk skal oprettes en arbejdsordre i henhold til den valgte vedligeholdelsesplanlinje, når du planlægger vedligeholdelsesplaner.

1. Hvis du har markeret afkrydsningsfeltet **Automatisk oprettelse**, kan du vælge en arbejdsordretype for den automatisk oprettede arbejdsordre i feltet **Arbejdsordretype**. Hvis du har markeret afkrydsningsfeltet **Automatisk oprettelse**, og du ikke vælger en arbejdsordretype i dette felt, vælges den arbejdsordretype, der er valgt i **Aktivadministration \> Opsætning \> Parametre til aktivstyring \> Arbejdsordrer**-linket \> feltet **Forebyggende arbejdsordretype**.

1. Brug felterne **Sæson fra** og **Sæson til** til at oprette en gentaget tidsbaseret vedligeholdelsesplanlinje i en periode på 12 måneder. *Eksempel:* Udstyr, der bruges til vedligeholdelse af grønne områder, kræver service hvert forår i en foruddefineret periode. Indsæt startdatoen for den periode, der skal gentages, i feltet **Sæson fra**.

1. Indsæt slutdatoen for den periode, der skal gentages, i feltet **Sæson til**.

1. I feltet **Resultatperiode** vises den aktuelle periode, der skal gentages. Når den aktuelle periode er overskredet, og du starter et nyt år, bliver den periode, der vises i dette felt, opdateret, så den afspejler den næste periode i gentagelsessekvensen.

1. I oversigtspanelet **Aktiver** skal du vælge de aktiver, der skal relateres til vedligeholdelsesplan.

1. I oversigtspanelet **Aktivtyper** skal du vælge de aktivtyper, der skal relateres til vedligeholdelsesplanen.

1. I oversigtspanelet **Arbejdssteder** skal du vælge de arbejdssteder, der skal tilknyttes vedligeholdelsesplanen. Hvis det er nødvendigt, kan du gøre opsætningen mere specifik ved at vælge en tilknyttet aktivtype, producent og model.

1. I oversigtspanelet **Arbejdsstedstyper** skal du vælge de arbejdsstedstyper, der skal tilknyttes vedligeholdelsesplanen.

>[!NOTE]
>Når der oprettes arbejdsordrer manuelt for aktiver, der er dækket af en leverandørgaranti, vises der en dialogboks for at gøre brugeren opmærksom på garantien. Oprettelsen af arbejdsordren kan derefter annulleres. Kontrollen af en garantirelation udelades for arbejdsordrer, der oprettes automatisk.

<a id="interval-types"></a>

## <a name="interval-types-overview"></a>Oversigt over intervaltyper

| Intervaltype og beskrivelse | Linjetype: Tid | Linjetype: Tæller |
|---|---|---|
| **Intervaltype: gentaget fra plandato** Optællingen starter fra den anvendte plandato. Når du planlægger vedligeholdelsesplaner, oprettes der vedligeholdelsestidsplanslinjer, når intervallet er nået. | **Plandato** på vedligeholdelsesplanlinjen bruges. Hvis der ikke er valgt en plandato på linjen, bruges **Plandato** for vedligeholdelsesplanen. Eksempel: Hvis tallet "3" indsættes i feltet **Periodefrekvens**, og "År" er valgt i feltet **Periode**, oprettes der en ny vedligeholdelsestidsplanslinje én gang hvert tredje år. | **Plandato** for vedligeholdelsesplanen bruges. Hvis tælleren er udskiftet, bruges den seneste udskiftningsdato som plandatoen. |
| **Intervaltype: Gentaget fra startdato** Optællingen starter fra startdatoen i aktivrelationen. Datoen vælges i detaljevisningen **Alle aktiver** \> oversigtspanelet **Vedligeholdelsesplaner** for aktiver \> feltet **Startdato** eller i detaljevisningen **Alle arbejdssteder** \> oversigtspanelet **Vedligeholdelsesplaner** \> feltet **Startdato**. Når du planlægger vedligeholdelsesplaner, oprettes der en vedligeholdelsestidsplanslinje, når intervallet er nået. | Startdatoen for vedligeholdelsesplanlinjen for aktiv eller arbejdssted bruges. Hvis dette felt er tomt, bruges **Plandato** for vedligeholdelsesplanen. | Startdatoen for vedligeholdelsesplanlinjen for aktiv eller arbejdssted bruges. Hvis dette felt er tomt, bruges **Plandato** for vedligeholdelsesplanen. |
| **Intervaltype: gentaget fra sidste arbejdsordre** Optællingen starter fra den faktiske slutdato og -tidspunkt for den seneste arbejdsordre, der blev fuldført på aktivet med denne specifikke kombination af vedligeholdelsesjobtype/variant af vedligeholdelsesjobtype/fag. Datoen og klokkeslættet vises i feltet **Faktisk slutning** i detaljevisningen **Alle arbejdsordrer**. | Den faktiske slutdato og -tidspunkt for den arbejdsordre, der er fuldført på aktivet med denne specifikke kombination af vedligeholdelsesjobtype/variant af vedligeholdelsesjobtype/fag. Hvis der ikke findes nogen fuldført arbejdsordre, bruges en af de datoer, der bruges i intervaltypen "Gentaget fra startdato", der er beskrevet ovenfor, i stedet. | Den faktiske slutdato og -tidspunkt for den arbejdsordre, der er fuldført på aktivet *og* vedligeholdelsesjobtypen/varianten af vedligeholdelsesjobtypen/fagkombinationen bruges. Hvis der ikke er angivet en slutdato og et sluttidspunkt på arbejdsordren, bruges en af de datoer, der bruges i intervaltypen "Gentaget fra startdato", der er beskrevet ovenfor, i stedet. |
| **Intervaltype: én gang fra plandato** Se beskrivelse til intervaltypen "gentaget fra plandato" ovenfor. Den eneste forskel er, at denne intervaltype kun skal bruges én gang. | Se beskrivelsen af intervaltypen "gentaget fra plandato" ovenfor. Dette interval bruges typisk til et engangsvedligeholdelses- eller servicejob. | Se beskrivelsen af intervaltypen "gentaget fra plandato" ovenfor. Dette interval bruges typisk til et engangsvedligeholdelses- eller servicejob. **Note 1:** Denne intervaltype er kun relevant, hvis tælleren erstattes, hver gang du udfører et vedligeholdelses- eller service job. Hvis en tæller af en eller anden grund er blevet udskiftet før afslutningen af det planlagte interval, beregnes der en ny tid for jobbet fra tidspunktet for udskiftningen af tælleren. **Note 2:** Hvis tælleren erstattes, når vedligeholdelses- eller servicejobbet er fuldført, fungerer denne intervaltype som intervaltypen "gentaget fra plandato" ovenfor. |
| **Intervaltype: én gang fra startdato** Se beskrivelse til intervaltypen "gentaget fra startdato" ovenfor. Den eneste forskel er, at denne intervaltype kun skal bruges én gang. | Se beskrivelsen af intervaltypen "gentaget fra startdato" ovenfor. Dette interval bruges typisk til et engangsvedligeholdelses- eller servicejob. | Se beskrivelsen af intervaltypen "gentaget fra startdato" ovenfor. Dette interval bruges typisk til et engangsvedligeholdelses- eller servicejob. **Note 1** ovenfor gælder også for denne intervaltype. **Note 3:** Hvis tælleren erstattes, når vedligeholdelses- eller servicejobbet er fuldført, fungerer denne intervaltype som intervaltypen "gentaget fra startdato" ovenfor. |
| **Interval type: Når nået over** Denne intervaltype er kun knyttet til tællere og bruges til at angive en øvre grænse, der er konfigureret på vedligeholdelsesplanlinjen. Poster i vedligeholdelsestidsplanen har den forventede startdato og -klokkeslæt for tællerregistreringen, hvilket betyder, at disse poster oprettes med en forventet startdato, der er lig med eller tidligere end systemdatoen. | Ikke anvendelig | Tællerintervallet angiver en øvre grænse. Hvis denne grænse overskrides, når du opretter en tællerregistrering, oprettes der en vedligeholdelsestidsplanslinje, når du planlægger forebyggende vedligeholdelse. |
| **Interval type: når nået under** Denne intervaltype er kun knyttet til tællere og bruges til at angive en nedre grænse, der er konfigureret på vedligeholdelsesplanlinjen. Poster i vedligeholdelsestidsplanen har den forventede startdato og -klokkeslæt for tællerregistreringen, hvilket betyder, at disse poster oprettes med en forventet startdato, der er lig med eller tidligere end systemdatoen. | Ikke anvendelig | Tællerintervallet angiver en nedre grænse. Hvis denne grænse er passeret, når du opretter en tællerregistrering, oprettes der en vedligeholdelsestidsplanslinje, når du planlægger forebyggende vedligeholdelse. |
| **Intervaltype: sammenkædet fra startdato** Denne intervaltype opretter kun en vedligeholdelsestidsplanslinje én gang. En vedligeholdelsesplan kan indeholde flere vedligeholdelsesplanslinjer, der bruger denne intervaltype, og disse linjer er sammenkædet. Du vil typisk oprette en vedligeholdelsesplan, der kun indeholder linjer med denne intervaltype. Vedligeholdelsestidsplanslinjer oprettes ved at identificere den vedligeholdelsesplanslinje, der har den første forventede startdato og -tidspunkt. | Se beskrivelsen af "én gang fra startdato" ovenfor. Eksempel: Du opretter to linjer i en vedligeholdelsesplan for et service job på en bil: én tidsbaseret linje med en 1-års periode og én tællerbaseret linje med en grænse på 25.000 km. Der oprettes en vedligeholdelsestidsplanslinje for den grænse, der nås først. For denne linjetype opretter du linjen med 1 års-perioden. | Se beskrivelsen af "én gang fra startdato" ovenfor. Eksempel: Du opretter to linjer i en vedligeholdelsesplan for et service job på en bil: én tidsbaseret linje med en 1-års periode og én tællerbaseret linje med en grænse på 25.000 km. Der oprettes en vedligeholdelsestidsplanslinje for den grænse, der nås først. For denne linjetype opretter du linjen med 25.000 km-grænsen. Eksempel på oprettelse af to tællerlinjer: Du kan også oprette en vedligeholdelsesplan med to tilknyttede tællerbaserede linjer, hvor den første linje har en grænse på 10.000 stk. af de varer, der produceres, og den anden linje er relateret til den maskine eller ressource, der kræver service efter 3.000 timers kørsel. |
| **Intervaltype: sammenkædet fra sidste arbejdsordre** Denne intervaltype opretter nye vedligeholdelsestidsplanlinjer efter hver fuldførte arbejdsordre. En vedligeholdelsesplan kan indeholde flere linjer, der bruger denne intervaltype, og disse linjer er sammenkædet. Du vil typisk oprette en vedligeholdelsesplan, der kun indeholder vedligeholdelsesplanlinjer af denne intervaltype. Vedligeholdelsestidsplanslinjer oprettes ved at identificere den vedligeholdelsesplanslinje, der har den første forventede startdato og -tidspunkt. | Denne intervaltype fungerer grundlæggende som "sammenkædet fra startdato" som beskrevet ovenfor. Den eneste forskel er den dato, som intervaltypen er baseret på. Den dato, der bruges, er den faktiske dato og -tidspunkt i den seneste arbejdsordre, der er fuldført på aktivet *og* vedligeholdelsesjobtypen/varianten af vedligeholdelsesjobtypen/fagkombinationen, | Denne intervaltype fungerer grundlæggende som "sammenkædet fra startdato" som beskrevet ovenfor. Den eneste forskel er den dato, som intervaltypen er baseret på. Den dato, der bruges, er den faktiske dato og -tidspunkt i den seneste arbejdsordre, der er fuldført på aktivet *og* vedligeholdelsesjobtypen/varianten af vedligeholdelsesjobtypen/fagkombinationen, |
| **Intervaltype: Gentages på samlet værdi (kun tæller)** Når vedligeholdelsesplanen køres, oprettes der en planlagt vedligeholdelseslinje, hver gang den akkumulerede værdi for en aktivtæller når periodefrekvensen eller et lige multiplum af periodefrekvensen. (Periodefrekvensen angives på vedligeholdelsesplanlinjen).<p>Du kan finde flere oplysninger om aktivering og brug af denne funktionalitet i afsnittet [Forbedringer af tællerbaseret vedligeholdelse](#counter-based-maintenance) senere i denne artikel. | Ikke relevant | **Eksempel:** Der er konfigureret en timetæller for aktivet AK-101. Der konfigureres også en aktivplanlinje for aktivet. Intervaltypen for denne linje *Gentages på samlet værdi (kun tæller)*, og periodefrekvensen er *1000*. Når vedligeholdelsesplanen køres, oprettes der en planlagt vedligeholdelseslinje, når den samlede værdi for tælleren overstiger 1.000 timer. Når den samlede værdi for tælleren derefter overstiger 2.000 timer, oprettes der endnu en planlagt vedligeholdelseslinje osv. for hver ekstra 1.000 timer. |
| **Intervaltype: Én gang på samlet værdi (kun tæller)** Når vedligeholdelsesplanen køres, oprettes der en planlagt vedligeholdelseslinje, når den akkumulerede værdi for en aktivtæller når periodefrekvensen, der er angivet på vedligeholdelsesplanlinjen.<p>Du kan finde flere oplysninger om aktivering og brug af denne funktionalitet i afsnittet [Forbedringer af tællerbaseret vedligeholdelse](#counter-based-maintenance). | Ikke anvendelig | **Eksempel:** Der er konfigureret en timetæller for aktivet AK-101. Der konfigureres også en aktivplanlinje for aktivet. Intervaltypen for denne linje *Én gang på samlet værdi (kun tæller)*, og periodefrekvensen er *1000*. Når vedligeholdelsesplanen køres, oprettes der en planlagt vedligeholdelseslinje, når den samlede værdi for tælleren overstiger 1.000 timer. |

>[!NOTE]
>Når der oprettes vedligeholdelsestidsplanslinjer for tidsbaserede vedligeholdelsesplanlinjer, er den forventede tid altid dagens starttidspunkt. For tællerbaserede vedligeholdelsesplanlinjer kan den forventede tid blive når som helst i løbet af dagen.

Nedenfor finder du eksempler på opsætningen af tidsbaserede og tællerbaserede vedligeholdelsesplanlinjer:

**Eksempel 1 - tidsbaseret vedligeholdelsesplanlinje:** Et smøreapparatjob kan konfigureres med et fast interval, der forekommer én gang om ugen. Til dette formål skal du vælge "gentaget fra plandato" i feltet **Intervaltype**. Se et eksempel i følgende illustration.

![Et servicejob, der er konfigureret i et fast interval og forekommer én gang om ugen.](media/02-preventive-maintenance.png "Et servicejob, der er konfigureret i et fast interval og forekommer én gang om ugen")

**Eksempel 2 - tidsbaseret vedligeholdelsesplanlinje** Der kan oprettes et inspektionsjob, som skal udføres ca. en gang om ugen. Til dette formål skal du vælge "gentaget fra sidste arbejdsordre" i feltet **Intervaltype**. Se et eksempel i følgende illustration.

![Et inspektionsjob, der er konfigureret til at blive udført ca. én gang om ugen.](media/03-preventive-maintenance.png "Et inspektionsjob, der er konfigureret til at blive udført ca. én gang om ugen")

**Eksempel 3 - tællerbaseret vedligeholdelsesplanlinje:** Følgende grafik illustrerer en timetæller, for hvilken der oprettes en ny vedligeholdelsestidsplanslinje, hver gang der er gået 250 timer. Intervaltypen for denne tællerbaserede linje er "gentaget fra startdato". Startdatoen er startdatoen for de tilknyttede aktiver i detaljevisningen **Alle aktiver** \> oversigtspanelet **Vedligeholdelsesplaner for aktiver** \> feltet **Startdato** eller i detaljevisningen **Arbejdssted** \> oversigtspanelet **Vedligeholdelsesplaner** \> feltet **Startdato**. Dette er et eksempel på en *forebyggende* vedligeholdelsesplan, fordi vedligeholdelsestidsplanslinjen automatisk oprettes, hver gang tærsklen (+ 250) nås.

![En timetæller, der opretter linjer for vedligeholdelsestidsplan periodisk.](media/04-preventive-maintenance.png "En timetæller, der opretter vedligeholdelsesplanlinjer periodisk")

**Eksempel 4 - tællerbaseret vedligeholdelsesplanlinje:** Følgende grafik illustrerer et fald i tællerværdi ved måling af slitage på bremseklods. Der oprettes en vedligeholdelsestidsplanslinje, når der oprettes en tællerregistrering på under 20 mm på bremseklodsen. Intervaltypen for denne tællerbaserede linje er "når nået under" eller "én gang fra den sidste startdato". Dette er et eksempel på en *reaktiv* vedligeholdelsesplan, fordi vedligeholdelsestidsplanslinjen ikke automatisk oprettes, før der er registreret en måling på under 20 mm.

![Et fald i tællerværdien ved måling af slitage på bremseklods.](media/05-preventive-maintenance.png "Et fald i tællerværdien ved måling af slitage på bremseklods")

**Eksempel 5 - tællerbaseret vedligeholdelsesplanlinje:** Følgende grafik illustrerer en tæller med en tærskel på -18 ° Celsius. Der oprettes en vedligeholdelsestidsplanslinje, når der foretages en tællerregistrering over -18 ° Celsius. Intervaltypen for denne tællerbaserede linje er "Når nået over". Dette er et eksempel på en *reaktiv* vedligeholdelsesplan, fordi vedligeholdelsestidsplanslinjen ikke automatisk oprettes, før der er registreret en måling på over -18 ° Celsius.

![En tæller med en grænse på -18 °Celsius.](media/06-preventive-maintenance.png "En tæller med en grænse på -18 °Celsius")

- Når du opretter et nyt aktiv, og det pågældende aktiv bruger en aktivtype, der er knyttet til en vedligeholdelsesplan, indsættes vedligeholdelsesplanen automatisk i oversigtspanelet **Alle objekter \> Vedligeholdelsesplaner** for aktiver. I **Standarder for aktivtype** i oversigtspanelet **Vedligeholdelsesplaner** bliver de relaterede vedligeholdelsesplaner også indsat automatisk.
- Hvis du tilføjer eller fjerner aktivtyper eller arbejdsstedtyper i **Vedligeholdelsesplaner**, vil ændringen kun afspejles på nye aktiver, der er oprettet, efter at du har foretaget ændringen.
- Hvis du tilføjer eller fjerner aktiver eller arbejdssteder i **Vedligeholdelsesplaner**, opdateres den pågældende ændring automatisk i **Alle aktiver \> Vedligeholdelsesplaner** for aktiver-oversigtspanelet eller i **Alle arbejdssteder \> Vedligeholdelsesplaner**-oversigtspanelet.

I følgende illustration vises et eksempel på en vedligeholdelsesplan for "lastbilservice" på siden **Vedligeholdelsesplaner**.

![Et eksempel på vedligeholdelsesplan for truckservice.](media/07-preventive-maintenance.png "Et eksempel på vedligeholdelsesplan for truckservice")

## <a name="add-a-maintenance-plan-to-an-asset"></a>Føje en vedligeholdelsesplan til et aktiv

1. Gå til **Styring af aktiver \> Almindelig \> Aktiver \> Alle aktiver** eller **Aktive aktiver**.

1. Vælg det aktiv, som du vil oprette en vedligeholdelsesplan for, og vælg **Rediger**.

1. I oversigtspanelet **Vedligeholdelsesplaner for aktiver** skal du vælge **Tilføj linje** for at føje en vedligeholdelsesplan til aktivet.

1. Vælg den relevante vedligeholdelsesplan i feltet **Vedligeholdelsesplan**.

1. Vælg den startdato, hvorfra planlægningen af det præventive vedligeholdelsesjob kan udføres, i feltet **Startdato**. 

1. Vælg **Gem**. Feltet **Aktiv** opdateres automatisk.

I følgende illustration vises et eksempel på vedligeholdelsesplaner på et aktiv på siden **Alle aktiver**.

![Et eksempel på vedligeholdelsesplaner, der er konfigureret for et aktiv.](media/08-preventive-maintenance.png "Et eksempel på vedligeholdelsesplaner, der er konfigureret for et aktiv")

<a id="counter-based-maintenance"></a>

## <a name="counter-based-maintenance-enhancements"></a>Tællerbaserede forbedringer af vedligeholdelse

Funktionen *Forbedringer af tællerbaseret vedligeholdelse* introducerer følgende funktionalitet:

- Indstillingen til automatisk at indsætte en tæller, der har en værdi på *0* (nul), når der oprettes et aktiv. Denne indstilling kan være nyttig, når du bruger forventet vedligeholdelse, der er baseret på tællere. Når funktionen *Forbedringer af tællerbaseret vedligeholdelse* ikke bruges, skal tællere med en værdi på *0* (nul) indsættes manuelt.
- Muligheden for at konfigurere en tæller, så den automatisk nulstilles, når en arbejdsordre er fuldført. Denne funktionalitet er nyttig, når du vil planlægge vedligeholdelse baseret på den samlede værdi, siden den sidste arbejdsordre blev fuldført.
- En ny type vedligeholdelsesplaninterval, der kaldes *Gentages på samlet værdi (kun tæller)*. Denne type udløser vedligeholdelse, hver gang en samlet tæller når et multiplum af en bestemt værdi. Der kan f.eks. udløses vedligeholdelse for hver 10.000 timer. Du kan finde flere oplysninger i afsnittet [Oversigt over intervaltyper](#interval-types) tidligere i denne artikel.
- En anden type vedligeholdelsesplaninterval, der kaldes *Én gang på samlet værdi (kun tæller)*. Denne type udløser vedligeholdelse, når en samlet tæller når et multiplum af en bestemt værdi, f.eks. 8.000 timer. Du kan finde flere oplysninger i afsnittet [Oversigt over intervaltyper](#interval-types).

### <a name="turn-on-the-counter-based-maintenance-enhancements-feature"></a>Aktivere funktionen Forbedringer af tællerbaseret vedligeholdelse

Før du kan bruge denne funktion, skal den være aktiveret for dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Aktivadministration*
- **Funktionsnavn:** *Forbedringer af tællerbaseret vedligeholdelse*

### <a name="create-and-initialize-counters-when-an-asset-is-created"></a>Oprette og initialisere tællere, når et aktiv oprettes

Hver gang du opretter et aktiv, kan relaterede aktivtællere, der initialiseres til en værdi på *0* (nul), oprettes automatisk, forudsat at du konfigurerer systemet og opretter aktivet korrekt.

1. Gå til **Aktivadministration \> Konfiguration \> Aktivtyper**.
1. Sørg for, at der er en aktivtype, der kan anvendes for dit planlagte nye aktiv. Opret en aktivtype efter behov. Kontrollér, at alle relevante tællere er valgt i oversigtspanelet **Tællere**.
1. Gå til **Aktivadministration \> Konfiguration \> Aktivtyper \> Tællere**.
1. For hver relevant tæller skal du kontrollere, at feltet **Samlet aggregering** er angivet til *Sum*.
1. Opret aktivet på siden **Alle aktiver**.
1. Indstil feltet **Aktivtype** til den aktivtype, du har identificeret eller oprettet i trin 2.
1. Afslut opsætningen af det nye aktiv efter behov.
1. Gå til **Aktivadministration \> Forespørgsler \> Aktiver \> Tællere**. Du skal kunne finde de initialiserede tællere, der er konfigureret for det nye aktiv.

> [!NOTE]
> Når der oprettes initialiserede aktivtællere, antages det, at aktivet aldrig har været anvendt, før det blev føjet til systemet. Første gang vedligeholdelsesplanen køres, bruges datoen og tællerværdien *0* (nul) som udgangspunkt for beregningen af fremtidig vedligeholdelse. Hvis aktivet ikke er nyt, da det blev føjet til systemet, kan du manuelt justere tællerværdien, så den svarer til den faktiske tællerværdi. Hvis du vil regulere en tællerværdi, skal du åbne det relevante aktiv på siden **Alle aktiver** og derefter vælge **Tællere** på fanen **Aktiv** i gruppen **Forebyggende** i handlingsruden. På siden **Aktivtællere** for det valgte aktiv skal du regulere værdien i kolonnen **Værdi** for den første tællerpost efter behov.

### <a name="automatically-reset-a-counter-value"></a>Nulstille en tællerværdi automatisk

Du kan konfigurere systemet til automatisk at nulstille en tæller, hver gang en relevant arbejdsordre når en valgt statusværdi.

1. Gå til **Styring af aktiver \> Opsætning \> Forebyggende vedligeholdelse \> Vedligeholdelsesplaner**.
1. Vælg en vedligeholdelsesplan i listeruden. Nulstillingen af tælleren gælder for alle aktiver, der bruger denne plan.
1. I sektionen **Linjer** skal du finde en aktivtællerlinje, som du vil nulstille en tæller for, og markere afkrydsningsfeltet **Nulstil tæller** for den pågældende linje. (Aktivtællerlinjer har en værdi i kolonnen **Tæller**. Den tæller, der er angivet i denne kolonne, er den tæller, der skal nulstilles for det relevante aktiv).
1. Gå til **Aktivadministration \> Opsætning \> Arbejdsordrer \> Livscyklustilstande**.
1. Vælg den livscyklus for en arbejdsordre i listeruden, som den relevante tæller skal nulstilles ved.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Nulstil tæller** til *Ja*.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]