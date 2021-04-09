---
title: Registrere udskudt indtægt
description: Dette emne indeholder oplysninger om at registrere udskudt indtægt ved hjælp af funktionen Indtægtsføring.
author: kweekley
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 8d9b5e1248497ec74e1c7125b2395c0ed4c825c2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820515"
---
# <a name="recognize-deferred-revenue"></a>Registrere udskudt indtægt

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Funktionen Indtægtsføring kan ikke aktiveres via Funktionsstyring. I øjeblikket skal du bruge konfigurationsnøgler til at aktivere funktionen.

Dette emne beskriver processen for indtægtsføring i tidsplanen for indtægtsføring. Når en faktura er blevet bogført for en salgsordre, oprettes der en plan for indtægtsføring for hver salgsordrelinje, der har en tidsplan for indtægtsføring. Indtægtstidsplanen på en linje bruges til at bestemme, om linjens indtægt skal udskydes.

## <a name="view-revenue-recognition-schedule-details"></a>Få vist oplysninger om tidsplanen for indtægtsføring

Du kan få adgang til oplysningerne om tidsplanen for indtægtsføring på to måder.

- Du kan åbne tidsplanen for indtægtsføring direkte fra en faktureret salgsordre. I dette tilfælde filtreres oplysningerne i indtægtstidsplanen, så der kun vises oplysninger for den valgte salgsordre. Denne fremgangsmåde er nyttig, når du validerer tidsplanoplysningerne for en salgsordre.
- Du kan åbne tidsplanen for indtægtsføring fra siden **Indtægtsføring \> Periodiske opgaver**. Denne fremgangsmåde bruges ofte, når der registreres indtægt ved slutningen af en periode. Når siden åbnes første gang, vises der ingen oplysninger. Brug filtrene over gitteret til at definere kriterier for de tidsplanoplysninger, der skal vises. Du kan filtrere på fakturadatoerne ved at angive et datointerval, en salgsordre, en kunde, et projekt-id eller en tilstand.

[![Illustration af siden Omsætningsplaner](./media/revenue-recognition-schedule-page.png)](./media/revenue-recognition-schedule-page.png)

I oversigtspanelet **Økonomisk dimension** under gitteret vises salgsordrelinjens økonomiske dimensioner. Disse dimensioner blev taget i betragtning under bogføringen til udskudt indtægt. De tages også i betragtning, når indtægten registreres. Hvilke dimensionsværdier der bruges, afhænger af den kontostruktur, der er tildelt til hovedkontiene for indtægt og udskudt indtægt.

## <a name="recognize-revenue"></a>Registrer indtægt

Du registrerer indtægten ved at køre processen **Opret kladde** fra siden **Registrer indtægt**. Du kan åbne denne side enten fra salgsordren eller **Periodiske opgaver**. Hvis processen køres fra salgsordren, registrerer den kun indtægt for den valgte salgsordre. Processen køres typisk fra **Periodiske opgaver** i stedet for, så den registrerer indtægt for alle bogførte salgsordrefakturaer.

Hvis du vil definere kriterierne for valg og bogføring af indtægt, skal du vælge **Opret kladde** for at åbne dialogboksen **Opret kladde**.

[![Opret indstillinger for kladdeparametre](./media/revenue-recognition-create-journal.png)](./media/revenue-recognition-create-journal.png)

Brug indstillingerne i feltgruppen **Behandlingsdato** i dialogboksen til at angive den bogføringsdato, der skal bruges, når indtægterne registreres. Hvis du vælger **Valgt dato**, kan du angive en bogføringsdato i feltet **Transaktionsdato**. Hvis du vælger **Dato for indtægtstidsplan**, anvendes transaktionsdatoen ikke. I stedet bruges værdien i feltet **Recognize date** (Registrer dato) på de enkelte linjer i tidsplanen som bogføringsdato.

Derefter skal du angive "fra og med"-datoen for indtægtsføring i feltet **Fra og med dato**. De linjer i tidsplanen, hvor registreringsdatoen er den samme som eller tidligere end "fra og med"-datoen, registreres, hvis de ikke er på hold.

Når du er færdig med at angive datoerne, skal du vælge **OK** i dialogboksen for at oprette kladden. Du modtager en meddelelse med oplysninger om det antal transaktioner, der er oprettet, og den kladde, hvor de blev oprettet. Kladden bogføres ikke automatisk. Den ansvarlige for indtægtsføring har derfor tid til at validere, hvilke linjer i planen der registreres.

Når processen er kørt, markeres de linjer i tidsplanen, der blev overført til kladden, som **Behandlet**. Flaget **Behandlet** angiver, at linjerne er blevet overført til kladden, men de kan være bogført eller ikke-bogført. Når indtægtsføringskladden er bogført, fjernes flaget **Behandlet** ikke. Hvis indtægtsføringskladden slettes, eller hvis en linje slettes, fjernes flaget **Behandlet**. På denne måde kan linjen registreres, når processen **Opret kladde** køres igen.

[![Siden Tidsplaner for indtægtsføring](./media/revenue-recognition-rev-recog-schedule-02.png)](./media/revenue-recognition-rev-recog-schedule-02.png)

På siden **Indtægtsføringskladde** (**Indtægtsføring \> Kladdeposteringer \> Indtægtsføringskladde**) skal du åbne **Linjer** for at få vist oplysningerne om, hvad der registreres. Der oprettes altid en separat transaktion for hver linje i den tidsplan, der registreres, selvom alle linjerne bogføres på den samme dato ved hjælp af de samme finanskonti.

[![Siden Kladdebilag](./media/revenue-recognition-journal-voucher.png)](./media/revenue-recognition-journal-voucher.png)

Kolonnen **Konto** viser finanskontoen for udskudt indtægt. Denne finanskonto kan ikke redigeres. Denne begrænsning er en hjælp til at sikre, at den korrekte finanskonto for udskudt indtægt eftergives. Denne finanskonto er ikke valideret i forhold til kontostrukturen, da den kan være ændret, siden den seneste bogføring til finanskontoen for udskudt indtægt.

Kolonnen **Modkonto** viser finanskontoen for indtægt. Finanskontoen for indtægt tages som standard fra Lagerpostering-profiler, og de økonomiske dimensioner hentes fra salgsordrelinjen. Denne finanskonto valideres i forhold til den aktuelle kontostruktur. Den kan dog redigeres, hvis kontostrukturen er blevet ændret og kræver yderligere økonomiske dimensioner.

Standardbeløbet hentes fra den tilsvarende linje i tidsplanen, og det kan ikke ændres.

Hvis salgsordren er en salgsordre med flere valutaer, angives valutakursen som standard til valutakursen fra fakturaen. Denne funktionsmåde er en hjælp til at sikre, at beløbene for regnskabsvaluta og rapporteringsvaluta eftergives fuldt ud. På grund af afrunding kan valutakursen for den sidste linje i tidsplanen afvige en smule fra kursen på fakturaen.

Når indtægtsføringskladden er bogført, angives bilaget i tidsplanen. Hvis der er mere end ét bilag for samme linje i tidsplanen, vises der en stjerne (\*) på linjen. Hvis du vil have vist de bilag, der er bogført for den pågældende linje, skal du vælge bilagsposteringer **Posteringer på bilag**.

## <a name="modify-the-revenue-recognition-schedule-details"></a>Rediger oplysningerne om tidsplanen for indtægtsføring

De fleste af dataene i oplysningerne om tidsplanen for indtægtsføring kan ikke redigeres. Der kan ikke føjes nye linjer til tidsplanen, og eksisterende linjer kan ikke slettes. Oplysningerne om indtægtstidsplanen for hver salgsordrelinje skal vedligeholdes for at sikre, at en organisation registrerer det samme beløb som det, der blev udskudt.

### <a name="edit-schedule-lines"></a>Rediger tidsplanlinjer

Visse redigeringer er tilladt på linjerne i tidsplanen. Følgende felter kan ændres på linjerne:

- **På hold** – dette flag kan angives eller fjernes, før linjen behandles. Hvis du vil fjerne flaget, skal du markere rækken og derefter vælge **Fjern på hold**. Indtægt kan ikke registreres på linjer, der er på hold. Linjer kan automatisk sættes på hold, hvis indtægtstidsplanen er konfigureret til automatisk at være på hold.

    [![Indtægtstidsplaner - rediger tidsplanlinjer](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)

- **Registrer dato** – registreringsdatoen kan ændres, før linjen behandles. Når processen til oprettelse af indtægtsføringskladden køres, angives der en dato i feltet **Registrer indtægt pr. dato**. Denne dato sammenlignes med datoen i feltet **Registrer dato** for at bestemme, hvilke linjer der skal registreres.
- **Beløb, der skal frigives** – det beløb, der vil blive frigivet, kan ændres, før linjen behandles. Du kan reducere det indtægtsbeløb, der registreres, men du kan ikke øge det. Dette felt giver en organisation mulighed for at registrere en del af indtægten på registreringsdatoen. Hvis beløbet ændres, viser beløbet i feltet **Restbeløb**, hvor meget indtægt der stadig skal registreres.
- **Antal til frigivelse** – hvis indtægtstidsplanen er oprettet for én forekomst eller en måned, viser feltet **Antal til frigivelse** antallet for salgsordrelinjen. Dette felt kan også redigeres og giver en anden metode til at genkende en del af indtægten på. Hvis antallet på linjen f.eks. er 5, kan du tilsidesætte antallet, så det er mindre end 5. Beløbet i feltet **Beløb, der skal frigives** opdateres proportionalt.

### <a name="update-contract-terms"></a>Opdatere kontraktvilkår

Oplysningerne om indtægtstidsplanen oprettes på baggrund af den indtægtstidsplan, der er knyttet til salgsordrelinjen, når fakturaen bogføres. Hvis indtægtstidsplanen på salgsordrelinjen er forkert, kan den ikke ændres på salgsordren, efter at salgsordren er faktureret. Du skal i stedet bruge knappen **Opdater kontraktvilkår** til at ændre indtægtstidsplanen. Indtægtstidsplanen kan ændres, enten før eller efter at indtægten er blevet registreret.

Hvis du vil ændre tidsplanen, skal du vælge en planlægningslinje for den vare, du er ved at ændre. I følgende illustration er linjen valgt for vare S0008, der blev bogført ved hjælp af en 12-måneders indtægtstidsplan. Når du vælger **Opdater kontraktvilkår**, vises der en dialogboks med kontraktens start- og slutdato samt indtægtstidsplanen.

[![Start- og slutdato for kontrakt](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)

Rediger kontraktens start- og slutdato, så de afspejler det korrekte datointerval. Når du ændrer datointervallet, skal værdien i feltet **Antal forekomster** svare til en indtægtstidsplan, der er defineret i systemet. I dette eksempel skal der oprettes en indtægtstidsplan på 24 måneder, da kontrakten blev ændret til en 24-måneders kontrakt. Da indtægtstidsplanen på 24 måneder findes, angives den som standard, og kontrakten kan ændres. Hvis der ikke findes en indtægtstidsplan med et tilsvarende antal forekomster, kan kontrakten ikke ændres. Når du er færdig med at opdatere kontraktvilkårene og indtægtstidsplanen, skal du vælge **OK** i dialogboksen for at gemme ændringerne.

[![Datointerval for kontrakt blev opdateret](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)

Kontraktændringerne har følgende indvirkninger på oplysningerne i indtægtstidsplanen:

- Hvis der ikke er registreret nogen indtægt for produktet, fjernes de tidligere tidsplanoplysninger, og de erstattes med oplysninger om den nye indtægtstidsplan. Vare S0008 havde f.eks. oprindelig 12 linjer i tidsplanoplysningerne. Disse 12 linjer fjernes og erstattes med 24 linjer baseret på den nye indtægtstidsplan.
- Hvis der er registreret indtægt for produktet, blev en del af indtægten fejlagtigt registreret, fordi registreringen blev baseret på den forkerte indtægtstidsplan. Disse linjer skal tilbageføres og registreres igen på baggrund af den nye tidsplan. I dette scenarie oprettes der nye indtægtstidsplanlinjer med negative beløb på den oprindelige registreringsdato. Der oprettes derefter nye linjer for at registrere beløbene ud fra den nye indtægtstidsplan. D. 8. august 2019 registrerede du f.eks. indtægt på 10,53 USD. Den 8. september 2019 registrerede du indtægt på 13,16 USD. Derfor oprettes der to nye linjer på samme dato. Én linje er for 10,53 USD, og den anden linje er for 13,16 USD. Der oprettes derefter fireogtyve nye linjer, og den samlede udskudte indtægt på 160,61 USD tildeles på tværs af dem. Du kan bogføre tilbageførselslinjerne ved at køre processen **Opret kladde**.

[![Tidsplan for indtægtsføring](./media/revenue-recognition-rev-recog-schedule-03.png)](./media/revenue-recognition-rev-recog-schedule-03.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]