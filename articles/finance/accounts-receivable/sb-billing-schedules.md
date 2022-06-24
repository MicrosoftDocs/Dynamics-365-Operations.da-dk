---
title: Oprette faktureringsplaner
description: Denne artikel forklarer, hvordan du opretter, sletter og redigerer faktureringsplaner.
author: JodiChristiansen
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 1248799f92dc6cbce8528a53cc8a3012d2a67b3c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903386"
---
# <a name="create-billing-schedules"></a>Oprette faktureringsplaner

[!include [banner](../includes/banner.md)]

På siden **Faktureringsplan** kan du oprette, slette eller redigere faktureringsplaner. Du kan også gennemse listen over faktureringsplaner. Når du opretter en faktureringsplan, bestemmes standardværdierne for den af den tilknyttede faktureringsgruppe. Der er konfigureret flere oplysninger på siden **Faktureringsparametre for tilbagevendende kontrakter**.

## <a name="create-a-billing-schedule"></a>Oprette en faktureringsplan

Følg disse trin for at oprette en faktureringsplan.

1. På siden **Faktureringsplan** skal du vælge **Ny**.
2. Vælg en faktureringsplangruppe i feltet **Faktureringsplangruppe** i dialogboksen **Opret faktureringsplan**.
3. Vælg en debitorkonto i feltet **Debitorkonto**.
4. Vælg startdatoen i feltet **Startdato**, og angiv derefter antallet af perioder i feltet **Antal perioder**. Feltet **Slutdato** opdateres på basis af det antal perioder, du angiver. Hvis du opdaterer feltet **Faktureringsslutdato**, opdateres feltet **Antal perioder** til **0** (nul).
5. Vælg **OK**.
6. Angiv en beskrivelse af faktureringsplanen i feltet **Beskrivelse** under fanen **Generelt** på siden **Faktureringsplan**.
7. Vælg en milepælsskabelon til **Milepælsfakturering** i feltet **Milepælsskabelon**.

Felter som **Fakturakonto** og **Valutakode** opdateres med oplysninger fra debitoren.

Felterne **Faktureringsfrekvens** og **Faktureringsinterval** angives automatisk på basis af den valgte faktureringsplangruppe.

8. Hvis du vil oprette separate fakturaer, skal du angive indstillingen **Fakturer separat** til **Ja**.
9. Hvis du automatisk vil forny en faktureringsplan efter den endelige faktureringsperiode, skal du angive indstillingen **Forny automatisk** til **Ja** og derefter angive feltet **Linjer at tilføje pr. fornyelse**.

Felterne **Parametre** angives automatisk på basis af værdierne på siden **Faktureringsparametre for tilbagevendende kontrakter**.

10. Hvis du vil beregne beløbet for en faktureringsplan forholdsmæssigt, skal du angive indstillingen **Beregn delvise perioder forholdsmæssigt** til **Ja**.
11. Hvis du vil justere linjerne i faktureringsplanen med slutningen af en måned, skal du angive indstillingen **Juster til måned** til **Ja**.
12. Angiv start- og slutdatoer for kontrakten i felterne **Kontraktstartdato** og **Kontraktslutdato**. Disse datoer er kun til orientering.

Feltet **Betaling** viser debitorbetalingsoplysninger fra debitoren. Når et linjeelement er på hold eller er afsluttet, kan betalingsoplysningerne ikke ændres.

> [!NOTE]
> Når du konsoliderer fakturaer efter vare, skal værdien af felterne **Betalingsbetingelser**, **Metode** og **Faktureringsplan** være ens. Ellers kan fakturaerne ikke konsolideres.

13. Under fanen **Adresse** kan du gennemse og opdatere felterne **Leveringsadresse** og **Faktureringsadresse**.
14. Under fanen **Kontaktoplysninger** kan du knytte en slutbrugerkonto til faktureringsplanen.
15. I felterne **Kontaktoplysninger** kan du angive en kontakt, en mailadresse og en internetadresse.
16. Hvis du vil spore oplysninger om provision for partnere, skal du angive felterne **Partnerkonto** og **Partnerprovisionsrate**. Disse felter er kun til orientering.
17. Under fanen **Total** kan du se de forskellige totaler, der er beregnet for faktureringsplanen.
18. Under fanen **Hold** kan du se revisionsoplysninger om, hvornår faktureringsplanen blev sat på hold, når hold er fjernet.
19. Under fanen **Ophør** kan du se en historik over de ophør, der er anvendt på eller fjernet fra faktureringsplanen.
20. Vælg **Gem**.
21. I oversigtspanelet **Faktureringsplanlinjer** skal du vælge **Tilføj linje**.
22. Vælg et varenummer i feltet **Varenummer**. Hvis den vare, der tilføjes, er en overordnet vare i en indtægtsopdelt vare, opdateres linjerne automatisk med de underordnede varer. Du kan kun redigere den overordnede vare i en indtægtsopdeling. Alle underordnede varer opdateres derefter tilsvarende.
23. Vælg varetypen i feltet **Varetype**.
24. Opdatere start- og slutdatoer.
25. Før fakturaerne oprettes, kan du ændre faktureringsfrekvensen ved at opdatere feltet **Faktureringsfrekvens**. Når den første faktura for faktureringsplanen er oprettet, kan faktureringsfrekvensen ikke ændres.
26. Vælg måleenheden for varen i feltet **Enhed**.
27. Vælg prissætningsmetoden for varen i feltet **Prissætningsmetode**.

Feltet **Enhedspris** angives automatisk fra lageret. Du kan dog opdatere den, hvis du ændrer prissætningsmetoden til **Flad**.

## <a name="remove-a-line-item"></a>Fjerne en linjevare

Hvis du vil fjerne en vare fra en faktureringsplan, skal du følge disse trin.

1. Vælg nummeret på den faktureringsplan, du vil redigere, i feltet **Planlæg nummer** på siden **Faktureringsplan**.
2. Vælg den linje, der skal slettes, i oversigtspanelet **Faktureringsplanlinjer**, og vælg derefter **Fjern**.
3. Vælg **Gem**.

Resten af denne artikel indeholder en beskrivelse af de handlinger og detaljer, der er tilgængelige for linjer i oversigtspanelet **Faktureringsplanlinjer**.

## <a name="billing-schedule-line-actions"></a>Handlinger for faktureringsplanlinje

Med knapperne i oversigtspanelet **Faktureringsplanlinjer** kan du anvende handlinger på de enkelte linjer.

| Knap | Beskrivelse |
|--------|-------------|
| Tilføj linje | Føj en linje til faktureringsplanen. |
| Tilføj fra vareliste | Føj flere varer til en faktureringsplan ved at vælge dem på en liste. |
| Fjern | <p>Fjern den valgte linje fra faktureringsplanen.</p><p>For varer, der er en del af en indtægtsopdelt vare, kan du kun fjerne den overordnede vare. Alle tilknyttede underordnede varer fjernes derefter automatisk.</p> |
| Vis faktureringsdetaljer | Vis faktureringsoplysningerne. |
| Fratræd | <p>Fratræd de valgte linjer. Denne knap er kun tilgængelig, når de valgte linjer har statussen **Aktiv**.</p><p>For varer, der er en del af en indtægtsopdelt vare, kan du kun afslutte den overordnede vare.</p> |
| Fjern fratrædelse | <p>Fjern fratrædelsen fra de valgte linjer. Denne knap er kun tilgængelig, når de valgte linjer har statussen **Fratrådt**.</p><p>For varer, der er en del af en indtægtsopdelt vare, kan du kun fjerne fratrædelsen fra den overordnede vare.</p> |
| Placer på hold | <p>Vælg oplysninger om, hvordan den valgte linje skal sættes på hold.</p><p>For varer, der er en del af en indtægtsopdelt vare, kan du kun placere den overordnede vare på hold.</p> |
| Fjern på hold | <p>Fjern den valgte linje fra at være på hold.</p><p>For varer, der er en del af en indtægtsopdelt vare, kan du kun fjerne den overordnede vare fra hold.</p> |
| Eskalering og rabat | Denne knap er ikke tilgængelig for varer, der er en del af en indtægtsopdeling, undtagen overordnede varer, hvor indtægtsopdelingen bruger **Nulbeløb** som fordelingsmetode. |
| Udskydelser | <p>Angiv indstillinger for udskydelse af den valgte linje.</p><p>Denne knap er ikke tilgængelig for overordnede varer i en indtægtsopdeling.</p> |
| Milepælsfordeling | <p>Gennemse og opdater oplysningerne om milepælsfordelingen for den valgte linje.</p><p>Denne knap er kun tilgængelig, når varen i faktureringsplanlinjen er en milepælsvare.</p> |
| Supplement og fornyelse | <p>Gennemse og opdater oplysningerne om supplement og fornyelse for den valgte linje.</p><p>Denne knap er kun tilgængelig, når varen i faktureringsplanlinjen er en supplerende eller fornyende vare.</p> |
| Vis dimensioner | Vis eller skjul de dimensionskolonner, der vises i gitteret **Faktureringsplanlinjer**. |
| Beregn pris pr. enhed | <p>Beregn varens enhedspris, så kunden kan betale kontraktbeløbet i afdrag (f.eks. dagligt, månedligt, kvartalsvist, halvårligt eller én gang om året). Du kan vælge kontraktprisen og prisfrekvensen.</p><p>Du kan få vist et revisionsspor over ændringerne: den gamle kontraktpris og -frekvens, den nye kontraktpris og -frekvens, den bruger, der har foretaget ændringen, samt dato og klokkeslæt for ændringen.</p> |
| Reguleringsdato | <p>Angiv justeringsdatoen for fornyelsesvarer.</p><p>Hvis du vælger en varegruppe i feltet **Varegruppe**, bruger alle varer justeringsdatoen for det første element i varegruppen i faktureringsplanen. Hvis feltet **Varegruppe** er tomt, kan du angive en justeringsdato, der skal bruges for alle varer.</p><p>Denne knap er kun tilgængelig, når feltet **Faktureringsfrekvens** er angivet til **Årlig**.</p> |
| Ikke-afregnet indtægt | <p>Angiv varen, så den bruger funktionen til ikke-faktureret omsætning. Du kan derefter angive kontiene for ikke-faktureret omsætning og ikke-fakturerede rabatbeløb for varen.</p><p>Denne knap er kun tilgængelig for varer, hvor feltet **Varetype** er angivet til **Standard**. Den er ikke tilgængelig for eksisterende faktureringsplaner eller faktureringsplanlinjer, hvor fakturaen allerede er oprettet.</p> |
| Tilføj indtægtsopdelt underordnet | <p>Vælg en underordnet vare, der skal føjes til salgsordren.</p><p>Denne knap er kun tilgængelig for overordnede varer i en indtægtsopdeling.</p> |
| Indstillinger for avanceret prissætning | Rediger prissætningsindstillingerne for en vare. |

## <a name="billing-schedule-line-details"></a>Detaljer om faktureringsplanlinje

Når du vælger en linje i oversigtspanelet **Faktureringsplanlinjer**, kan du få vist specifikke oplysninger for den pågældende linje. Disse detaljer er opdelt under forskellige faner.

### <a name="general-tab"></a>Fanen Generelt

Følgende oplysninger er tilgængelige under fanen **Generelt**:

| Felt eller sektion | Beskrivelse |
|------------------|-------------|
| Anvendelse | <p>Denne sektion indeholder oplysninger om forbrugsvarer. Den indeholder følgende felter:</p><ul><li>**Forbrugs-id** – Id'et for måleren eller forbrugsvaren.</li><li>**Aflæsningsindstilling** – Indstillingen af forbrugsaflæsning: **Aflæsning** eller **Forbrug**.</li><li>**Forventet forbrug** – Angiv det forventede forbrug for en forbrugsvare, der har perioder, hvor fakturaen ikke er oprettet. På siden **Faktureringsdetaljer** kan du gennemgå faktureringsdetaljelinjerne for det forventede forbrug.</li></ul> |
| Eksterne referencer\* | Dette afsnit indeholder felterne **Ekstern** og **Linjenummer**, hvor du kan angive eksterne referenceoplysninger. |
| Milepæl | <p>Denne sektion indeholder oplysninger om milepælsvarer. Den indeholder feltet **Forventet slutdato**, som viser slutdatoen for varen.</li></ul> |
| Tekst | En kommentar til linjen. Teksten oversættes til standardsproget for kunden eller den juridiske enhed. |
| Varegruppe | Varegruppen for linjevaren. |
| Reguleringsdato | Justeringsdatoen for faktureringsplanen. |

\* Når du konsoliderer fakturaer efter vare på siden **Generér faktura**, skal felterne **Ekstern reference** matche. Hvis bare ét tegn er anderledes, konsolideres varerne ikke på fakturaen. Der udføres ingen valideringskontrol af noget felt i sektionen **Ekstern reference**, og værdien i feltet **Linjenummer** skal være et positivt heltal.

### <a name="address-tab"></a>Fanen Adresse

Følgende oplysninger er tilgængelige under fanen **Adresse**.

| Felt | Beskrivelse |
|-------|-------------|
| Leveringsadresse | <p>Vælg leveringsadressen for linjevaren. Standardleveringsadressen er den primære leveringsadresse i oversigtspanelet **Adresse**.</p><p>Når du ændrer adressen, kan du vælge følgende adresseindstillinger:</p><ul><li>**Adresser** – Vælg en adresse til den aktuelle kunde.</li><li>**I brug** – Vælg en adresse, der aktuelt bruges til den aktuelle kunde.</li><li>**Anden adresse** – Vælg en adresse til en kundepost.</li></ul><p>I forbindelse med varer, der bruger omsætningsopdeling, er det kun adressen til den overordnede vare, der kan redigeres. Adressen på de underordnede elementer svarer til adressen for den overordnede post og kan ikke redigeres separat.</p> |
| Faktureringsadresse | <p>Vælg faktureringsadressen for linjevaren. Standardleveringsadressen er den primære leveringsadresse i oversigtspanelet **Adresse**. Du kan ændre adressen efter behov på baggrund af formålet med de tilgængelige adresser:</p><ul><li>Hvis ingen af adresserne har formålet **Faktura**, er standardfaktureringsadresse kundens primære adresse uanset formålet.</li><li>Hvis en eller flere af adresserne har formålet **Faktura**, er standardfaktureringsadressen den adresse, der senest er angivet.</li><li>Hvis en eller flere af adresserne har formålet **Faktura**, og en af fakturaadresserne er angivet som den primære adresse, er standardfaktureringsadressen den adresse, der har formålet **Faktura**, og som er angivet som den primære adresse.</li><li>I forbindelse med varer, der bruger omsætningsopdeling, er det kun adressen til den overordnede vare, der kan redigeres. Adressen på de underordnede elementer svarer til adressen for den overordnede post og kan ikke redigeres separat.</li></ul> |

### <a name="product-tab"></a>Fanen Produkt

Følgende oplysninger er tilgængelige under fanen **Produkt**.

| Felt eller sektion | Beskrivelse |
|------------------|-------------|
| Lagringsdimensioner | <p>I denne sektion vises lageroplysningerne om varen. Den indeholder feltet **Serienummer**, som viser varens serienummer.</p><p>Serienummeret kopieres fra den første salgsordre under supplements- og fornyelsesprocessen. Ved varer, der bruger indtægtsfordeling, kopieres serienummeret for den overordnede vare til alle underordnede varer. Serienummeret kopieres, når indstillingen **Kopiér serienummer** er angivet til **Ja** på siden **Faktureringsparametre for tilbagevendende kontrakter**.</li></ul> |
| Produktdimensioner | Produktoplysningerne for varen og værdierne opdateres automatisk på baggrund af den værdi af **Variantnummer**, der er valgt for faktureringsplanlinjen. |

### <a name="account-tab"></a>Fanen Konto

Følgende oplysninger er tilgængelige under fanen **Konto**.

| Felt | Beskrivelse |
|-------|-------------|
| Hovedkonto | Den hovedkonto, der er oprettet på salgslinjen. Standardværdien er fra salgsordren. Dette felt kan være tomt. |
| Økonomiske varedimensioner | <p>De økonomiske standarddimensionsværdier, der er baseret på kunde- og vareposten.</p><p>Til varer, der bruger indtægtsfordeling, bruger de underordnede varer de økonomiske dimensionsværdier for kunde- og vareposterne som beskrevet tidligere. Hvis du skal opdatere de økonomiske dimensionsværdier for underordnede varer, kan du importere dataenheden.</p> |

### <a name="renewals-tab"></a>Fanen Fornyelser

Følgende oplysninger er tilgængelige under fanen **Fornyelser**.

| Felt | Beskrivelse |
|-------|-------------|
| Forny automatisk | <p>En værdi, der angiver, om faktureringsplanlinjen fornys automatisk for den næste faktureringsperiode:</p><ul><li>**Ja** – Faktureringsplanlinjen fornys automatisk for den næste faktureringsperiode, når du opretter en faktura.</li><li>**Nej** – Faktureringsplanlinjen fornys ikke automatisk. Du skal forny faktureringsplanen manuelt.</li></ul> |
| Linjer, der skal tilføjes pr. fornyelse | Det antal linjer, der skal føjes til fornyelsen af en faktureringsplan. |

De følgende knapper er desuden tilgængelige under fanen **Fornyelser**.

| Knap | Beskrivelse |
|--------|-------------|
| Revision af ikke-faktureret omsætningskladde | Få vist alle ændringer for varer, der bruger funktionen til ikke-faktureret omsætning. |
| Tilføj fornyelsesvilkår | Tilføj en fornyelsesperiode for varen. Startdatoen for den nye fornyelsesperiode er den næste dato efter slutdatoen for den foregående periode. **Slutdato for fornyelse**, **Startdato for udskydelse**, **Slutdato for for udskydelse**, **Vareantal** og **Enhedspris** er felter, der kan opdateres. |
| Rediger fornyelsesperiode | <p>Rediger en fornyelsesperiode. For den første periode kan du ændre udskydelsens start- og slutdato, før den første kladdepost oprettes. For efterfølgende perioder kan startdatoen ikke ændres. Den er altid den næste dato efter slutningen af den forrige periode.</p><p>Hvis en fornyelsesperiode findes efter den periode, du redigerer, kan datoerne for perioden ikke ændres. I dette tilfælde er det kun felterne **Antal** og **Enhedspris** for fornyelsesvaren, der kan opdateres.</p><p>Der findes f.eks. tre perioder. <ul><li>Den første periode kan ikke ændres, fordi den allerede er startet.</li><li>Det er kun antallet og enhedsprisen, der kan ændres for den anden periode.</li><li>For den tredje periode kan alle værdier undtagen startdatoen ændres. Indstillingen **Planlæg fra skabelon** giver dig desuden mulighed for at oprette en udskydelsesplan, der er baseret på skabelonen for varen med den ikke-fakturerede omsætning. Når denne indstilling er angivet til **Ja**, skal du vælge udskydelsesskabelonen i feltet **Skabelon** og ændre start- og slutdatoerne efter behov. Efterfølgende fornyelsesperioder bruger samme udskydelsesskabelon. Udskydelsesskabelonen kan dog ændres.</p></li></ul> |

### <a name="termination-tab"></a>Fanen Ophør

Følgende oplysninger er tilgængelige under fanen **Ophør**.

| Felt | Beskrivelse |
|-------|-------------|
| Ophørsdato | Dato for, hvornår faktureringsplanlinjen ophører. Standardværdien kommer fra feltet **Ophørsdato** i overskriften. Du kan ændre værdien efter behov. |
| Ophørstype | Ophørstypen. Standardværdien kommer fra feltet **Ophørstype** i overskriften. |

### <a name="hold-tab"></a>Fanen Hold

Hvis der bruges udskydelse af indtægter og udgifter, viser fanen **Hold** datoen.

### <a name="escalation-and-discount-tab"></a>Fanen Eskalering og rabat

Følgende oplysninger er tilgængelige under fanen **Eskalering og rabat**.

| Felt | Beskrivelse |
|-------|-------------|
| Eskalering | <p>Vælg, om eskaleringer er tilladt for faktureringsplanlinjen. En eskaleringslinje fra overskriften anvendes, når faktureringsplanlinjen oprettes.</p><ul><li>**Ja** – Eskaleringer kan anvendes på linjen. Når denne indstilling er valgt, kan du konfigurere eskaleringerne for faktureringsplanlinjerne på siden **Eskalering og rabat**.</li><li>**Nej** – Eskaleringer kan ikke anvendes på linjen.</li></ul><p>Standardindstillingen er baseret på den valgte **Faktureringsplangruppe**.</p> |

### <a name="price-changes-tab"></a>Fanen Prisændringer

I forbindelse med linjer, der ændres fra **Standard**-pris til **Flad** pris, indeholder gitteret under fanen **Prisændringer** følgende kolonner:

- Ændring af dato
- Ændret af bruger
- Standardpris
- Flad pris
- Prisopdatering
