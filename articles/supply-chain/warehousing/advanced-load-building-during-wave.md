---
title: Avanceret bølgelastopbygning
description: Dette emne giver oplysninger om avanceret bølgelastopbygning, der automatisk tildeler forsendelser til eksisterende bølger under bølgeudførelse. Derfor kan du oprette beskrivende laster, der repræsenterer lastvogne, uden at skulle bruge lastplanlægningspanelet.
author: mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPostMethod,WHSWaveTemplateTable,WHSLoadMixGroup,WHSLoadBuildTemplate, WHSWaveTableListPage, TMSLoadBuildTemplateApply, TMSLoadBuildTemplates, TMSLoadBuildTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 08e44b4e37f28ec91eeb8e53930de5133607bd66
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574731"
---
# <a name="advanced-load-building-during-wave"></a>Avanceret bølgelastopbygning

[!include [banner](../includes/banner.md)]

Avanceret bølgelastopbygning tildeler automatisk forsendelser til eksisterende bølger under bølgeudførelse. Derfor kan du oprette beskrivende laster, der repræsenterer lastvogne, uden at skulle bruge lastplanlægningspanelet. Denne funktion er nyttig for virksomheder, der vil bruge begrebet med laster til at spore og planlægge forsendelse af varer på en lastbil/et påhængskøretøj, men ikke vil oprette disse laster manuelt hver dag.

Under bølgebehandling opretter systemet normalt en ny last for hver forsendelse, hvortil der ikke er tildelt nogen last. Men når den avancerede bølgelastopbygning er slået til, tildeler systemet hver ikke-tildelt forsendelse til en eksisterende last (hvis der findes en relevant last), og der kun oprettes nye laster, når der er brug for dem. Avanceret bølgelastopbygning opretter automatisk de nye laster ud fra de kriterier, du definerer.

Hvis du vil bruge funktionen, skal du konfigurere systemet på følgende måde:

- Opret *bølgeskabeloner*, der indeholder den nye **buildLoads**-metode. Denne metode gør det muligt at opbygge en avanceret bølgelastopbygning, der bruger disse skabeloner.
- Konfigurer *lastopbygningsskabeloner*, som hver især er sammenkædet med en bestemt bølgeskabelon og metode. Lastopbygningsskabeloner styrer, hvilke laster (eksisterende eller nye) de lastlinjer, der bruges bølger til, føjes til. Du kan kombinere eller adskille forsendelser, baseret på kriterier som f. eks. lastskabelon, udstyr og andre feltværdier på lastlinjen.
- Definer *Blandingsgrupper for last* for at styre, hvilke varer der skal og ikke må kombineres på en enkelt last. Du kan også angive, om begrænsningen skal give en advarsel eller en fejl, og om lastskabelonens begrænsning skal evalueres.

## <a name="turn-on-advanced-wave-load-building-in-your-system"></a>Aktivér den avancerede bølgelastopbygning i systemet

Før du kan bruge avanceret lastopbygning underbølger, skal funktionen være aktiveret i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere statussen for disse funktioner og aktivere dem, hvis de skal bruges. I arbejdsområdet **Funktionsstyring** vises funktionerne på følgende måde:

- Funktion til bølgelastopbygning:

    - **Modul:** *Lokationsstyring*
    - **Funktionsnavn:** *Funktion til bølgelastopbygning*

- Bølgetrinkode for hele organisationen:

    - **Modul:** *Lokationsstyring*
    - **Funktionsnavn:** *Organization wide wave step code*

### <a name="make-sample-data-available"></a>Gøre eksempeldata tilgængelige

Hvis du vil arbejde gennem denne demo ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret. Derudover skal du vælge den juridiske enhed **USMF**, før du starter.

Du kan også bruge denne demo som vejledning til brug af denne funktion, når du arbejder i et produktionssystem. Du skal dog i det tilfælde erstatte dine egne værdier, og du mangler muligvis nogle typer påkrævede poster, som standarddemodataene giver.

### <a name="make-sure-that-the-scenario-setup-includes-enough-available-inventory"></a>Kontroller, at scenarieopsætningen indeholder en tilstrækkelig disponibel lagerbeholdning

Hvis du arbejder med **USMF**-demodataene, skal du først sikre dig, at systemet er konfigureret, så der er en tilstrækkelig lagerbeholdning på hver af de relevante lokationer. I denne demo er der en forventning om, at følgende lager er tilgængeligt på lagerstedet *62*:

- **Vare A0001:** 10 stk.
- **Vare A0002:** 10 stk.
- **Vare M9200:** 10 hver

Vare **M9200** skal føjes til lagerstedet. Gennemfør procedurerne i følgende under afsnit for at tilføje varelageret.

#### <a name="create-a-new-license-plate-id"></a>Oprette et nyt nummerplade-id

1. Gå til **Lokalitetsstyring** \> **Konfiguration** \> **Lagersted** \> **Nummerplader**.
1. Gå til handlingsruden, og vælg **Ny**.
1. I den nye række skal du i feltet **Nummerplade** angive *LP6203*.
1. Vælg **Gem**.

#### <a name="create-a-standard-cost-for-item-m9200-in-site-6"></a>Oprette en standardomkostning for vare M9200 på lokation 6

1. Gå til **Administration af produktoplysninger** \> **Produkter** \> **Frigivne produkter**.
1. Søg på **M9200**.
1. Vælg rækken for varen, og gå derefter til handlingsruden ,og vælg **Varepris** i gruppen **Konfigurer** under fanen **Administrer omkostninger**.
1. Gå til siden **Varepris**, og vælg fanen **Afventende priser**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier på den nye linje:

    - **Efterkalkulationstype:** *Planlagt omkostning*
    - **Pristype:** *Kostpris*
    - **Version:** *10*
    - **Lokation:** *6*
    - **Pris:** *1,60*

1. Vælg **Gem** i handlingsruden.
1. Vælg **Aktiver afventende pris(er)** i handlingsruden.
1. Vælg fanen **Aktive priser** for at kontrollere, at den nye kostpris for lokation *6* er blevet tilføjet.

#### <a name="create-inventory-in-warehouse-62"></a>Oprette lager på lagersted 62

1. Gå til **Lagerstyring** \> **Kladdeposteringer** \> **Varer** \> **Lagerregulering**.
1. Gå til handlingsruden, og vælg **Ny**.
1. I dialogboksen **Opret lagerkladde** skal du i oversigtspanelet **Oversigt** i feltet **Lagersted** angive *62*. Accepter standardværdierne i alle de andre felter.
1. Vælg **OK** for at lukke dialogboksen.
1. Siden **Lagerregulering** åbnes. Gå til oversigtspanelet **Kladdelinjer**, og vælg **Ny** for at tilføje en linje.
1. Angiv følgende værdier på den nye linje. Accepter standardværdierne i alle de andre felter.

    - **Varenummer:** *M9200*
    - **Lokation:** *masse-003*
    - **Antal:** Skift værdien til *10*.

1. Vælg **Gem** i handlingsruden.
1. Vælg **Valider** i handlingsruden for at kontrollere for fejl.
1. I dialogboksen **Kontroller kladde** skal du vælge **OK** for at starte kontrollen. Du modtager en meddelelse, når kontrollen er fuldført.
1. I handlingsruden skal du vælge **Bogfør** for at udføre lagerreguleringen.
1. I dialogboksen **Bogfør kladde** skal du vælge **OK** for at starte bogføringen. Du modtager en meddelelse, når bogføringen er fuldført.

## <a name="set-up-advanced-wave-load-building"></a>Konfigurer bølgelastopbygning

### <a name="regenerate-wave-process-methods"></a>Genoprette bølgeprocesmetoder

Du skal muligvis oprette bølgeprocesmetoderne igen for at gøre lastopbygningsmetoden (**buildLoads**) tilgængelig.

1. Gå til **Lokationsstyring** \> **Konfiguration** \> **Bølger** \> **Bølgeprocesmetoder**.
2. Kontrollér, at **buildLoads** er på listen. Hvis den ikke findes, skal du vælge **Genopret metoder** i handlingsruden for at tilføje den.

### <a name="set-up-wave-templates"></a>Konfigurere bølgeskabeloner

Hvis du vil drage fordel af den avancerede bølgelastopbygning, skal du medtage metoden **buildLoads** i hver enkelt relevant [bølgeskabelon](tasks/configure-wave-processing.md).

1. Gå til **Lokationsstyring** \> **Konfiguration** \> **Bølger** \> **Bølgeskabeloner**.
1. Vælg en bølgeskabelon.

    Hvis du arbejder med **USMF**-demodataene , skal du vælge skabelonen **62 Forsendelsesstandard**.

1. Vælg **Rediger** i handlingsruden for at sætte siden i redigeringstilstand.
1. Gå til oversigtspanelet **Metoder**, og vælg **buildLoads** i gitteret **Resterende metoder**.
1. Vælg knappen Højre pil for at flytte metoden **buildLoads** til gitteret **Valgte metoder**.
1. Hvis du vil tildele en værdi for **Bølgetrinkode** for metoden **buildLoads**, skal du først oprette en kode på siden **Bølgetrinskoder**. Du kan bruge en hvilken som helst værdi, men du skal huske at notere den, da du skal bruge den senere. Følg disse trin for at oprette koden **WSC2112**:

    1. I rækken for metoden **buildLoads** skal du højreklikke på pil ned i feltet **Bølgetrinskode** og derefter vælge **Vis detaljer**.
    1. Gå til siden **Bølgetrinskoder**, og vælg **Ny** i handlingsruden.
    1. I feltet **Bølgetrinskode** skal du angive *WSC2112*.
    1. I feltet **Bølgetrinsbeskrivelse** skal du angive *WSC2112*.
    1. I feltet **Bølgetrinstype** skal du vælge *Lastopbygning*.

1. Vælg **Gem**, og luk siden.
1. I rækken for metoden **buildLoads** i feltet **Bølgetrinskode** skal du vælge den kode, du netop har oprettet (**WSC2112**).
1. Vælg **Gem** i handlingsruden.

> [!NOTE]
> Bølgetrinskoder er koder, som brugerne kan konfigurere og bruge til at knytte bestemte forekomster af bølgemetoder til tilsvarende skabeloner. Skabelonerne indeholder skabeloner til genopfyldning, containerisering, etiketudskrivning, lastopbygning og sortering.
>
> Når der ikke bruges bølgetrinskoder, skal brugerne angive en fri tekst for at referere til en bestemt skabelon fra forekomsten af bølgemetoden. Der er fejlrisiko for fri tekst, fordi brugerne skal sørge for, at den bølgetrinstekst, som de føjer til en bestemt bølgetrinsmetode i en bølgeskabelon, nøjagtigt svarer til bølgetrinsteksten i destinationsskabelonen.
>
> Bølgetrinskoder for en specifik bølgetrinstype oprettes på en separat side. For hver forekomst af en bølgetrinsmetode i en bølgeskabelon, der kræver en bølgetrinskode, skal bølgetrinskoden være valgt på en rulleliste. Valg på en rulleliste erstatter indtastning af fritekst og hjælper med at reducere risikoen og virkningerne af menneskelige fejl. Opsætningskoder bruges til at sammenkæde en bølgetrinsmetode i en bølgeskabelon med en destinationsskabelon for metoden.

### <a name="set-up-load-mix-groups"></a>Konfigurere blandingsgrupper for last

Blandingsgrupper for last opretter regler for de varetyper, der kan kombineres i en enkelt last. Du kan oprette så mange blandingsgrupper for last, som du har brug for. Men hvis du vil bruge avanceret bølgeopbygning, skal du have mindst én. Følg disse trin for at oprette en blandingsgruppe for last:

1. Gå til **Lokationsstyring** \> **Opsætning** \> **Last** \> **Blandingsgrupper for last**.
1. Vælg **Ny** i handlingsruden for at oprette en lastgruppe.
1. I feltet **Id for blandingsgruppe for last** skal du angive et navn til den nye gruppe.

    Hvis du arbejder med **USMF**-demodataene, skal du angive følgende værdier:

    - **Id for blandingsgruppe for last:** *TV*
    - **Beskrivelse:** *TV*

1. I handlingsruden skal du vælge **Gem** for at gøre oversigtspanelet **Kriterier for blandingsgruppe for last** tilgængeligt.
1. I oversigtspanelet **Kriterier for blandingsgruppe for last** skal du vælge **Ny** for at føje en række til gitteret.
1. Angiv de ønskede værdier i hvert felt i den nye række. Disse værdier bestemmer, hvilke varegrupper der medtages i lastblandingen.

    Hvis du arbejder med **USMF**-demodataene, skal du vælge *TV & video* i feltet **Varegruppe**.

1. I handlingsruden skal du vælge **Gem** for at gøre oversigtspanelet **Begrænsninger for blandingsgruppe for last** tilgængeligt.
1. I oversigtspanelet **Begrænsninger for blandingsgruppe for last** skal du vælge **Ny** for at føje en række til gitteret.
1. Angiv de ønskede værdier i hvert felt i den nye række.

    Hvis du arbejder med **USMF**-demodataene, skal du angive følgende værdier:

    - **Varegruppe:** *CarAudio*
    - **Lastopbygningshandling:** *Begræns* (Denne værdi vil forhindre, at elementer, der tilhører varegruppen **CarAudio**, er i samme last som varer, der tilhører varegruppen **TV & video**).

1. Fortsæt med at arbejde med reglerne, indtil du har tilføjet alle de kriterier og begrænsninger, du skal bruge for blandingsgruppen for last.

Hvis du arbejder med **USMF**-demodataene, er du nu færdig med denne opsætning.

### <a name="set-up-load-build-templates"></a>Konfigurer lastopbygningsskabeloner

Du kan oprette så mange lastopbygningsskabeloner, som du har brug for. Men hvis du vil bruge avanceret bølgeopbygning, skal du have mindst én. Følg disse trin for at oprette en lastopbygningsskabelon.

1. Gå til **Lokationsstyring** \> **Konfiguration** \> **Last** \> **Skabeloner til bølgelastopbygning**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.
1. Angiv følgende værdier i den nye række.

    | Felt | Beskrivende tekst | Værdi i USMF-demodataene |
    |---|---|---|
    | Løbenummer | Den rækkefølge, som skabelonen evalueres i. | *1* |
    | Navn på lastopbygningsskabelon | Angiv det entydige id for lastopbygningsskabelonen. Du skal angive navnet på den skabelon, du har oprettet eller opdateret tidligere i denne opsætning. | *62 Forsendelsesstandard* |
    | Kode for bølgetrin | Angiv bølgetrinskoden, der skal bruges til at sammenkæde skabelonen med en bølgemetode. Du skal angive den kode, du valgte for metoden **buildLoads**, da du konfigurerede bølgeskabelonen tidligere i denne opsætning. | *WSC2112* |
    | Id for lastskabelon | Vælg den lastskabelon, der skal bruges, når der oprettes nye laster, og som der skal sammenlignes med, når du tildeler til eksisterende laster. Lastskabelonen definerer den maksimale vægt og den tilladte volumen, der er tilladt for hele lasten. | *Standardlastskabelon* |
    | Udstyr | Det udstyr, der skal sammenlignes med, når du tildeler til eksisterende belastninger, og som skal angives for nye laster, der oprettes. | Lad feltet være tomt. |
    | Id for lastblandingsgruppe | Vælg den blandingsgruppe for last, der skal bruges, hvis varen er tilladt i last. Blandingsgruppen opretter regler for de varetyper, der kan kombineres i en enkelt last. Du skal vælge en af de blandingsgrupper, du oprettede tidligere i denne opsætning. | *TV* |
    | Brug åbne laster | Vælg, om eksisterende laster skal tilføjes. Der findes følgende indstillinger:<ul><li>**Ingen** – føj ikke åbne laster til eksisterende laster.</li><li>**Enhver** – føjer laster til eventuelle eksisterende laster, der gælder for linjen.</li><li>**Tildelt** – føjer åbne laster til den last, der er tildelt bølgen.</li></ul> | *Alle* |
    | Opret laster | Angiv, om der skal oprettes nye laster, hvis ingen eksisterende laster opfylder kriterierne. | Markeret (= *Ja*) |
    | Tillad opdeling af forsendelseslinje | Angiv, om en enkelt lastlinje kan opdeles på tværs af flere laster, hvis den fulde linje den maksimale kapacitet for lastskabelonen. | Ikke angivet (= *Nej*) |
    | Valider volumenmålinger | Angiv, om lastopbygning skal kontrollere vægten og volumen, efterhånden som hver lastlinje tilføjes, for at sikre, at lastskabelonens volumemæsssige grænser overholdes. | Ikke angivet (= *Nej*) |

1. I handlingsruden skal du vælge **Gem** for at gøre indstillingen **Rediger forespørgsel** tilgængelig.
1. I handlingsruden skal du vælge **Rediger forespørgsel** for at redigere forespørgslen.
1. I dialogboksen skal du under fanen **Sortering** vælge **Tilføj** for at føje en række til gitteret.
1. Definer de sorteringsregler, du vil bruge, i den nye række. Angiv f.eks. følgende værdier for at sortere søgeresultaterne i stigende rækkefølge efter ordrenummer:

    - **Tabel:** *Lastdetaljer*
    - **Afledt tabel:** *Lastdetaljer*
    - **Felt:** *Ordrenummer*
    - **Søgeretning:** *Stigende*

1. Vælg **OK** for at gemme dine ændringer og lukke dialogboksen.
1. I oversigtspanelet **Opdel efter** kan du angive regler, der styrer, hvordan lasten deles op. Du vil måske typisk opdele ved de brugerdefinerede felter, der er udvidet på lastlinjen, **Rute**, **Tur** eller **Kørsel**. Hvis du f.eks. vil oprette én last pr. ordrenummer, skal du markere afkrydsningsfeltet **Opdel efter** for den række, der har følgende værdier:

    - **Navn på referencetabel:** *Lastdetaljer*
    - **Navn på referencefelt:** *Ordrenummer*

## <a name="scenario"></a>Scenario

Dette scenarie viser, hvordan de indstillinger, der blev beskrevet tidligere i dette emne, påvirker lagerstedshandlinger, mens en salgsordre behandles. I dette scenarie bruges **USMF**-demodataene sammen med de andre demoværdier, der findes i installationsinstruktionerne.

### <a name="create-sales-orders"></a>Oprette salgsordrer

1. Gå til **Salg og marketing** \> **Salgsordrer** \> **Alle salgsordrer**.
1. I handlingsruden skal du vælge **Nye** for at åbne dialogboksen **Opret salgsordre**.
1. I dialogboksen skal du angive følgende værdier:

    - Gå til oversigtspanelet **Kunde**, indstil feltet **Kundekonto** til *US-007*.
    - I oversigtspanelet **Generelt** skal du indstille **Lagersted** til *62*.

1. Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.
1. Din nye indkøbsordre åbnes. Den skal omfatte en ny tom linje i gitteret i oversigtspanelet **Salgsordrelinjer**. På den nye linje skal du angive feltet **Varenummer** til *A0001* og feltet **Antal** til *1*.
1. Vælg **reservation** i menuen **Lager** oven over gitteret.
1. På siden **Reservation** skal du i handlingsruden vælge **Reserve parti**.
1. Vælg knappen **Luk** (**X**) i øverste højre hjørne for at gå tilbage til salgsordren.
1. Vælg **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Lagersted** i handlingsruden. Systemet opretter en forsendelse og føjer den til en ny last, da ingen eksisterende laster indeholder lastlinjer, der har dette ordrenummer.

    Du modtager orienterende meddelelse, der angiver arbejdet, bølgen og forsendelsen, der oprettes for denne ordre.

1. Hvis du vil bekræfte lasten, forsendelsen og arbejdsdetaljerne på salgslinjen, skal du markere linjen og derefter vælge menuen **Lagersted** over gitteret, vælge **Lastdetaljer**, **Forsendelsesoplysninger** eller **Arbejdsdetaljer**.
1. I oversigtspanelet **Salgsordrelinjer** skal du vælge **Tilføj linje** for at tilføje en anden linje.
1. På den nye linje skal du angive feltet **Varenummer** til *A0002* og feltet **Antal** til *1*.
1. Gentag linjer 6 til 9 for at reservere linjen og frigive den til lagerstedet. Systemet opretter en **ny** forsendelse for den linje, du har tilføjet. Men da du bruger en avanceret bølgelastopbygning, tilføjer systemet den pågældende forsendelse og lastlinje til den eksisterende bølge. Hvis du ikke har brugt en avanceret bølgelastopbygning, vil systemet oprette en ny last for forsendelsen.
1. I oversigtspanelet **Salgsordrelinjer** skal du vælge **Tilføj linje** for at tilføje en anden linje.
1. På den nye linje skal du angive feltet **Varenummer** til *M9200* og feltet **Antal** til *1*.
1. Gentag linjer 6 til 9 for at reservere linjen og frigive den til lagerstedet. Som før opretter systemet en **ny** forsendelse for den linje, du har tilføjet. Men da varen er fra varegruppe **CarAudio**, kan det **ikke overføre de begrænsninger, du opretter for blandingsgruppen for last**. Derfor **føjes den til en ny last**. Hvis du ikke har angivet en blandingsgruppe for last på lastopbygningsskabelonen, skal denne forsendelse føjes til den nye last.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]