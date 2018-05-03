---
title: Tilbudsanmodning
description: "Emnet giver et overblik over tilbudsanmodninger. Organisationer sender en tilbudsanmodning, når de ønsker at modtage konkurrencedygtige tilbud fra flere leverandører på de varer eller ydelser, de har brug for at købe."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ac3c55ac56c800f6f4e8e593cce7fe0874d99a5d
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="requests-for-quotation-rfqs"></a>Tilbudsanmodning

[!INCLUDE [banner](../includes/banner.md)]

Emnet giver et overblik over tilbudsanmodninger. Organisationer sender en tilbudsanmodning, når de ønsker at modtage konkurrencedygtige tilbud fra flere leverandører på de varer eller ydelser, de har brug for at købe. I en tilbudsanmodning kan du bede leverandører om oplysninger om priser og leveringstider for det angivne antal varer.
Du kan også bede leverandører angive, om der er ekstra gebyrer som f.eks. forsendelsesomkostninger eller eventuelle rabatter på store ordrer eller tidlig betaling af kreditorfakturaen.

Tilbudsanmodningsprocessen består af følgende opgaver:

1.  Oprette og sende en tilbudsanmodning til en eller flere leverandører.

2.  Modtage og registrere bud (svar på tilbudsanmodninger)

3.  Overføre bud, du accepterer, til en indkøbsordre, købsaftale eller indkøbsrekvisition.

I følgende illustration vises en oversigt over processen for anmodninger om tilbud.

[![RFQ-proces (Radio Frequency Identification-proces)](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Du kan oprette en sag for en tilbudsanmodning ud fra planlagte ordrer, en indkøbsrekvisition eller ved manuel indtastning. Tilbudsanmodningssagen er det grundlæggende dokument, du bruger til at udstede en tilbudsanmodning til hver kreditor.+

Når du forbereder tilbudsanmodningssagen og tilføjer kreditorer, skal du vælge **Send** (**Sende og udgiv** for offentlig sektor) for tilbudsanmodningssagen. Der oprettes en tilbudsanmodningskladde for hver leverandør, som du sendte tilbudsanmodningen til. Du kan konfigurere indstillingerne for Udskrivning for handlingen Send, så der enten udskrives en rapport for hver kreditor til et arkiv eller sendes en rapport til hver kreditors mailadresse. Du kan desuden bruge tilbudsanmodningskladden til hver leverandør til at generere en rapport, som du kan sende eller gensende til leverandøren senere. Du kan også konfigurere handlingen Send, så den opretter et svarark, som leverandøren kan udfylde.

Dette emne beskriver processen til håndtering af tilbudsanmodninger, når der ikke bruges kreditorsamarbejde. Hvis dit system er konfigureret til kreditorsamarbejde, kan leverandører afgive bud direkte i Microsoft Dynamics 365 for Finance and Operations. Du kan finde flere oplysninger under [Kreditorsamarbejde med kunder](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations) og [Kreditorsamarbejde med eksterne kreditorer](vendor-collaboration-work-external-vendors.md).

Hvis du skal ændre en tilbudsanmodning, når du har sendt den, kan du sende tilbudsanmodningen til kreditoren igen, når du er færdig, ved hjælp af to ændringshandlinger: Opret og Færdiggør.+

Når du modtager bud pr e-mail, skal du håndtere disse bud fra siden **Tilbudsanmodning**.

Hvis der kræves endnu et svar fra en kreditor, skal du vælge **Returner** på siden **Tilbudsanmodning**. Handlingen Returner genererer en ny kladde og en rapport, der udskrives, arkiveres og sendes i henhold til dine indstillinger for Udskrivning.

> [!NOTE]
> Navnet på siden **Tilbudsanmodning** er ændret. I tidligere versioner af Dynamics 365 for Finance and Operations kaldes denne side **Svar på tilbudsanmodning**.

Hvis du har føjet scorekriterier til din tilbudsanmodningssag, har tilbudsanmodningen et scorepanel, hvor du kan angive scorer. De samlede scorer vises på tilbudsanmodningen og når du sammenligner svarene på siden **Sammenlign svar**. På siden **Sammenlign svar** kan du også sammenligne andre svardata, f.eks. linjepris, leveringsdato og den samlede pris.

Når du vælger et bud eller et antal linjer i et bud, kan du acceptere alle eller nogle linjer og afvise resten. Der oprettes acceptkladder, afvisningskladder og tilsvarende rapporter, som udskrives, arkiveres og sendes i henhold til dine indstillinger for Udskrivning. Når du accepterer et bud eller bestemte linjer i et bud, oprettes der enten en købsaftale eller indkøbsordre, eller en indkøbsrekvisition opdateres, afhængigt af indkøbstypen for tilbudsanmodningen. Du kan oprette en samhandelsaftale, der senere kan bruges til alle svarene, uanset om du har accepteret eller afvist dem.

En tilbudsanmodningssag har to statusser: den laveste og den højeste. Du kan få vist status på listesiden for **Alle tilbudsanmodninger**. Den laveste status er det mindst fremskredne stadie for en linje i tilbudsanmodningssagen, mens den højeste status er det mest fremskredne stadie for en linje i tilbudsanmodningssagen. Antag f.eks., at en tilbudsanmodningssag med tre linjer sendes til to kreditorer, så der er to tilbudsanmodninger med tre linjer. Alle linjer er **Sendt**. Nu er der givet et bud fra en af kreditorerne, og linjerne i tilbudsanmodningen får statussen **Modtaget**. Det betyder, at ud af de tre linjer i tilbudsanmodningssagen er alle **Sendt** for en tilbudsanmodning og **Modtaget** for en anden tilbudsanmodning. Den laveste status bliver derefter **Sendt**, og den højeste status bliver **Modtaget.**

Disse statusser beskrives mere detaljeret senere i dette emne.

## <a name="setting-up-rfq-functionality"></a>Konfigurere funktioner for tilbudsanmodning

Før du kan oprette en tilbudsanmodningssag, skal du konfigurere oplysninger om tilbudsanmodningen på siden **Indkøbs- og forsyningsparametre**. Når du opretter en tilbudsanmodningssag, kan du angive standardværdier, der kopieres til tilbudsanmodningen. Du kan angive følgende standardværdier:

-   Indkøbstypen af nye tilbudsanmodninger: **Indkøbsordre** eller **Købsaftale**

-   Udløbsdato og -klokkeslæt for forskydningen fra den dag, hvor tilbudsanmodningssagen er oprettet

-   Anmodningstype, som kan fungere som standard for en bestemt vurderingsmetode for tilbudsanmodningssagen

-   Leveringsoplysninger og betalingsbetingelser

-   Felter, der skal medtages i buddet

Du kan tilsidesætte disse værdier for en bestemt tilbudsanmodningssag.

Du skal også konfigurere ændringsprocessen. Som en del af denne konfiguration kan du aktivere feltlåsning. Når feltlåsning er aktiveret, skal en indkøber, der ønsker at ændre en tilbudsanmodning, først klikke på **Opret** i sektionen **Ændring** under fanen **Tilbud** for tilbudsanmodningssagen. Når tilbudsanmodningen er blevet opdateret med ændringen, skal indkøberen derefter fuldføre processen ved at vælge **Færdiggør**. Handlingen Færdiggør genererer en e-mail, der giver besked til leverandørerne om den ændrede tilbudsanmodning.

På siden **Indkøbs- og forsyningsparametre** kan du vælge, hvilken skabelon der skal bruges til den mailmeddelelse, der sendes til kreditorer. Når der oprettes en skabelon i **E-mail-skabeloner**, kan den indeholde følgende erstatningstokens:

-   %Tilbudsanmodningssag%

-   %Årsag til returnering af bud%

-   %Årsag til ændring%

-   %Ændring udarbejdet af%

-   %Firma%

-   %Navn på tilbudsanmodningssag%

-   %ExpiryDateTime%

-   %Dato%

De angivne tokens %Årsag til returnering af bud% og %Årsag til ændring% erstattes af tekst, der indkøberen kan skrive, når han eller hun afslutter ændringen i guiden **Ændring**. Værdierne for tokenerne %Ændring udarbejdet af% og %Firma% hentes automatisk fra tilbudsanmodningen. %Dato%-tokenet erstattes af dags dato.

Hvis du vil annullere en tilbudsanmodning, efter den er blevet sendt, kan du gøre dette fra tilbudsanmodningssagen. Til annulleringen kræves det, at der sendes en e-mail-skabelon for at sende besked om annulleringen til kreditorens kontaktpersoner. Skabelonen skal være markeret på siden **Indkøbs- og forsyningsparametre**. Når skabelonen er oprettet, kan den indeholde følgende erstatningstokens:

-   %Årsag til annullering%

-   %Tilbudsanmodningssag%

-   %Tilbudsanmodning annulleret af%

-   %Firma%

-   %Navn på tilbudsanmodningssag%

-   %Dato%

Tokenet %Årsag til annullering% erstattes af tekst, som indkøberen kan angive i guiden **Annullering**. %Dato%-tokenet erstattes af dags dato.

Hvis du vil bruge årsagskoder for et bud for at at angive, hvorfor det blev afvist eller godkendt, skal du oprette årsagskoder på siden **Kreditorårsager**.

På siden **Formularopsætning** i Indkøb og forsyning kan du konfigurere udseendet af dine udskrevne eller gemte dokumenter med tilbudsanmodninger.

> [!NOTE]
> For en konfigurationen til offentlige institutioner skal du bruge ændringsprocessen til at ændre en tilbudsanmodning, der er allerede blevet sendt. Når en tilbudsanmodning er sendt, er felter skrivebeskyttede.
Når du vil foretage ændringer af tilbudsanmodningen, skal du derfor vælge **Opret** for at starte ændringsprocessen som beskrevet tidligere. Låsningsfunktionen styres af indstillingen **Lås tilbudsanmodninger, når de er sendt** på siden **Indkøbs- og forsyningsparametre**. Denne parameter er som standard indstillet til **Ja**, og for en konfiguration til den offentlige sektor kan standardindstillingen ikke ændres. Derfor selvom ændringsprocessen kan håndteres manuelt i en ikke-offentlig sektor-konfiguration, skal den bruges til en offentlig sektor-konfiguration.

Når du opretter en tilbudsanmodningssag af typen Indkøbsordre og føjer en lagervare til tilbudsanmodningen, oprettes der en lagertransaktion med tilgangsstatussen **Tilbudstilgang**. Kun linjer i tilbudsanmodningssager med denne status kommer i betragtning når du bruger en behovsplan til beregning af forsyninger. Hvis du ønsker, at behovsplanen skal omfatte tilbudsanmodningssagens linjer som en forventet tilgang, skal du konfigurere denne funktionsmåde i opsætningen af varedisponeringen.

Som indkøbschef eller -agent kan du oprette og vedligeholde anmodningstyper, der passer til indkøbskravene i din organisation. Hver anmodningstype kan knyttes til en scoremetode. Scoremetoder består af et sæt af kriterier, der kan bruges, når du scorer bud. Du skal oprette anmodningstyper, scoremetoder og scorekriterier på siderne den **Anmodningstype** og **Scoremetode**.

## <a name="creating-and-sending-an-rfq"></a>Oprette og sende en tilbudsanmodning

Du skal oprette en tilbudsanmodningssag, vælge de kreditorer, som skal byde på tilbudsanmodningenssagen, og derefter sende tilbudsanmodninger til kreditorerne. Du kan bruge indstillingerne for Udskrivning til at sende rapporten over tilbudsanmodningen og rapporterne med svarark til din foretrukne destination.

Du kan manuelt oprette en tilbudsanmodningssag af indkøbstypen **Indkøbsordre** eller **Købsaftale**.

Hvis tilbudsanmodningssagen er af typen **Indkøbsordre**, forekommer følgende funktionsmåde, der afviger fra andre typer tilbudsanmodningssager:

-   Når der oprettes linjer for en tilbudsanmodningssag, oprettes der lagertransaktioner med tilgangsstatussen **Tilbudstilgang**.

-   Når du accepterer et tilbud, genereres der en indkøbsordre.

Hvis tilbudsanmodningssagen er af typen **Købsaftale**, forekommer følgende funktionsmåde, der afviger fra andre typer tilbudsanmodningssager:

-   Tilbudsanmodningssagen bruges til en aftale om at købe et bestemt antal eller for en bestemt værdi af et produkt over tid. Du skal vælge det datointerval, der gælder for indkøbsaftalen, og navnet på den person, der håndterer indkøbsaftalen.

-   Når du accepterer et tilbud, genereres der en købsaftale.

Hvis tilbudsanmodningssagen oprettes ud fra en indkøbsrekvisition, tildeles typen **Indkøbsrekvisition** automatisk. Du kan manuelt oprette en tilbudsanmodningssag af typen **Indkøbsrekvisition**.

Du kan kun oprette en tilbudsanmodningssag ud fra en indkøbsrekvisition, hvis status for indkøbsrekvisitionen er **Til gennemsyn**, og du er tildelt den næste opgave i arbejdsgangen. Linjerne i indkøbsrekvisitionen opdateres automatisk, når du accepterer linjer fra bud (svar på tilbudsanmodninger), som du har modtaget fra kreditorer. Du kan ikke fuldføre, afvise, godkende eller udføre andre handlinger i indkøbsrekvisitionen, indtil rekvisitionslinjen opdateres med en accepteret linje i tilbudsanmodningen eller tilbudsanmodningssagen annulleres.

Når du opretter en tilbudsanmodningssag, kan du vælge en anmodningstype. Anmodningstypen bestemmer det sæt scorekriterier, der bruges til at give scoresvar på tilbudsanmodningssagen.

Du kan føje et spørgeskema til en tilbudsanmodningssag. Dette spørgeskema vises derefter på alle svar på tilbudsanmodningen, når du har sendt den. Udfyldelse af spørgeskemaet er en obligatorisk opgave, før et bud kan sendes.


Du kan vælge kreditorerne, der skal føjes til en tilbudsanmodningssag, på tre måder:

- Tilføj kreditorerne én efter én.
- Søg efter alle de leverandører, der opfylder bestemte kriterier.
- Tilføj automatisk alle kreditorer, der er godkendt til de indkøbskategorier, der bruges på linjerne i tilbudsanmodningssagen.

Når tilbudsanmodningssagen er klar, skal du vælge **Send**. Handlingen Send genererer kladder og rapporter, der udskrives, arkiveres og sendes i henhold til dine indstillinger for Udskrivning.

Hvis du har indstillet **Brug kreditor til genberegning af priser** og **Brug kreditorspecifikke vareoplysninger** til **Ja** på siden **Sender tilbudsanmodning**, da du sendte tilbudsanmodningen til en kreditor, angives nogle af de kreditorspecifikke oplysninger automatisk i tilbudsanmodningssagen for den pågældende kreditor.


## <a name="amending-an-rfq-case"></a>Ændring af en tilbudsanmodningssag

Nogle gange skal du ændre en tilbudsanmodningssag, når du har sendt den. Du skal evt. ændre en tilbudsanmodningssag, hvis f.eks. leveringsdatoerne er ændret, eller du ønsker yderligere produkter eller forskellige mængder af produkter. Du kan konfigurere ændringsprocessen, så den er mere restriktiv eller mindre restriktiv.

Hvis du har konfigureret ændringsprocessen, så den er mere restriktiv, skal du, før du kan ændre felterne i en tilbudsanmodningssag, der er allerede sendt, vælge **Opret** i tilbudsanmodningssagen for at starte en ændring. Når du har afsluttet dine ændringer, skal du vælge **Færdiggør**. Derefter føres du gennem processen med at tilføje oplysninger i den mail, der sendes for at give leverandørerne besked om ændringen. Den opdaterede tilbudsanmodningsrapport, som indeholder en ændringsnote, knyttes automatisk til e-mailen.

Hvis du har konfigureret ændringsprocessen, så den er mindre restriktiv, behøver du ikke at vælge **Opret**, før du kan redigere felterne i en tilbudsanmodningssag, der allerede er sendt. Du skal dog manuelt føje en ændringsnote til tilbudsanmodningen og sende sagen igen. Vær opmærksom på, at denne fremgangsmåde kun kan bruges, hvis ingen af svarene (buddene) er blevet redigeret. Hvis du har angivet et svar, og det er i **Modtaget**-tilstand, er knappen **Send** ikke tilgængelig. I så fald skal du vælge **Opret** og derefter **Færdiggør**, som du skal gøre i den mere restriktive proces. Svaret nulstilles derefter for at afspejle ændringerne af tilbudsanmodningssagen.

Hvis kreditorer bruger grænsefladen til kreditorsamarbejde til at afgive bud, skal du altid bruge ændringsprocessen for at oplyse kreditorerne om ændringerne af tilbudsanmodningssagen. Denne proces hjælper med at forhindre en situation, hvor kreditorer byder på en forældet tilbudsanmodningssag, mens de har et igangværende bud. Du kan finde flere oplysninger om kreditorsamarbejde under [Kreditorsamarbejde med eksterne kreditorer](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-external-vendors).

Hvis du vil invitere flere leverandører til at byde, og der ikke er foretaget nogen ændringer af tilbudsanmodningssagen, kan du bruge knappen **Send**. De leverandører, du har tilføjet, vises på siden **Send** og modtager e-mailinvitationen.


## <a name="receiving-and-registering-rfq-replies"></a>Modtagelse og registrering af svar på tilbudsanmodningen

Når du sender en tilbudsanmodning, oprettes der automatisk et svarark. Når du modtager bud på en tilbudsanmodning, skal du angive dem via siden **Tilbudsanmodning** ved at klikke på handlingen **Rediger svar på tilbudsanmodning**. Dette gør det muligt at angive budoplysninger i en dedikeret budformular. Først skal **Status for svar** være **Ikke startet**. Når du klikker på **Rediger svar på tilbudsanmodning** er statussen **Indkøber opdaterer**, indtil buddet er sendt. Klik på **Send** når du har angivet oplysningerne om buddet. Svarstatussen ændres til **Sendt af indkøber**. Når kreditorsamarbejde er aktiveret, opdateres **Status for svar**, når kreditoren interagerer med buddet. Status ændres derefter fra **Kreditor opdaterer** til **Sendt af kreditor**. Når der sendes et bud, oprettes der en kladde som **Modtaget**. Svaret (buddet) skal sendes for at blive registreret som modtaget, og derefter kan det kun behandles yderligere som accepteret eller afvist.

Hvis du vil opdatere buddet, skal du gennemgå den samme proces som ovenfor og sende igen.

Bemærk, at redigering af formen **Tilbudsanmodning** kun er tilladt for oplysninger, der vedrører behandling af buddet, ikke angivelse af buddet. For at angive eller ændre buddet, skal du klikke på **Rediger svar på tilbudsanmodning**.

Når du indtaster oplysningerne om buddet, og hvis tilbudsanmodningssagen tillader alternative linjer, kan du tilføje alternative linjer for linjer, der kun har en indkøbskategori og ingen angivet katalogvare. Klik på **Tilføj alternativ** for at føje alternative linjer.

Hvis du har angivet et svar, men det kræver et nyt tilbud fra kreditoren, kan du returnere tilbudsanmodningen. Der genereres en ny kladde og en rapport, der kan sendes til kreditoren.

Du kan se en oversigt over alle tilbudsanmodninger og statusser: **Sendt, Modtaget, Accepteret, Afvist, Annulleret, Afvist** på siden **Opfølgning på tilbudsanmodning**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Acceptere og afvise bud og overføre accepterede bud til downstream-dokumenter

Når du har fundet det bedste bud, f.eks. buddet med den bedste samlede pris, kan du acceptere buddet. Du kan acceptere nogle af linjerne i et bud og afvise andre.
Du kan også acceptere linjer fra forskellige leverandører. Vær opmærksom på, at hvis du accepterer nogle linjer, bliver du bedt om at afvise alle andre linjer. Så hvis du vil acceptere andre linjer, skal du vælge **Annuller**, når du bliver bedt om det. Status for svaret på tilbudsanmodningen for hver leverandør, du accepterer bud eller linjer fra, opdateres til **Godkendt**.

Når du opretter indkøbsordren eller købsaftalen, og har brug for at tilføje en ekstra linje til tilbudsanmodningen, kan klikke på **Tilføj linje** i linjegitteret på siden **Tilbudsanmodning**. Du kan kun få vist og redigere denne linje på siden **Tilbudsanmodning**. Den kan ses på budsiden, når den accepteres.

Når du accepterer et bud eller en eller flere linjer i et bud, oprettes der automatisk en indkøbsordre eller en købsaftale. Derefter kan du afvise bud fra de øvrige leverandører.

I svaret kan du tilføje en årsagskode for at forklare, hvorfor du har accepteret eller afvist et bud.

Når du accepterer et bud af typen **Indkøbsrekvisition**, opdateres indkøbsrekvisitionens linjer med følgende oplysninger, som afspejler disse oplysninger fra det accepterede bud:

-   Enhedspris

-   Rabat %

-   Rabatbeløb

-   Indkøbsgebyrer

-   Linjetillæg

-   Leverandør

-  Eksternt nummer

-   Ekstern beskrivelse


I følgende tabel vises, hvordan status for tilbudsanmodningen ændres, efterhånden som du accepterer eller afviser bud fra kreditorer.

<a name="statuses--highest-and-lowest"></a>Statusser – højeste og laveste
-----------------------------

Under fanen Kreditor for tilbudsanmodningssagen kan du se linjerne med den højeste og laveste status for en bestemt kreditor. Når kreditoren tilføjes, og ingen linjer endnu er sendt, er den laveste og højeste status <strong>Oprettet</strong>. Når tilbudsanmodningen er sendt til kreditoren med alle linjer, vil statussen for de to linjer være <strong>Sendt</strong>. Hvis nogle af linjerne i et bud fra en kreditor, der er accepteret, mens andre er afvist, får de afviste linjer den laveste status, som er <strong>Afvist</strong>, og de accepterede linjer får den højeste status, som er <strong>Accepteret</strong>.

På linjerne i tilbudsanmodningssagen kan du se den højeste og laveste status pr. linje på tværs af alle kreditorer. Hvis du har sendt en linje til alle kreditorer i tilbudsanmodningssagen og ingen har svaret endnu, er både den laveste og højeste status **Sendt.** Når mindst én kreditor svarer, ændres den højeste status til **Modtaget**. Hvis du føjer en ny kreditor til sagen, ændres den laveste status til **Oprettet**

Den højeste og laveste status for tilbudsanmodningssagen er en opsummering af statussen for fanen \<Kreditor og fanen linjer.

Statusserne rangeres på følgende måde fra laveste til højeste: Oprettet, Sendt, Modtaget, Afvist, Accepteret, Afvist, Annulleret.

Følgende tabel viser, hvordan status for tilbudsanmodningssagen ændres, når du opretter en tilbudsanmodningssag og derefter sender den til kreditorer.

| **Handling**                                | **Laveste status for tilbudsanmodningssag** | **Højeste status for tilbudsanmodningssag** | **Laveste status for linje i tilbudsanmodningssag** | **Højeste status for linje i tilbudsanmodningssag** |
|-------------------------------------------|----------------------------|-----------------------------|---------------------------------|----------------------------------|
| Opret sidehoved og linje for tilbudsanmodningssag.      | Oprettet den                    | Oprettet den                     | Oprettet den                         | Oprettet den                          |
| Send tilbudsanmodninger til alle kreditorer i tilbudsanmodningssagen. | Afsendt                       | Afsendt                        | Afsendt                            | Afsendt                             |
| Tilføj en anden kreditor.                       | Oprettet den                    | Afsendt                        | Oprettet den                         | Afsendt                             |
| Sende tilbudsanmodningen til den anden leverandør.        | Afsendt                       | Afsendt                        | Afsendt                            | Afsendt                             |

Alle linjer i de tilbudsanmodninger, der vedrører tilbudsanmodningssagen, vil være i tilstanden **Sendt**.

I følgende tabel vises, hvordan status for tilbudsanmodningen ændres, efterhånden du modtager tilbud og registrerer oplysningerne i svararket til tilbudsanmodningen.

| **Handling**                                               | **Laveste status på tværs af alle linjer i alle tilbudsanmodninger** | **Højeste status på tværs af alle linjer i alle tilbudsanmodninger** | **Laveste status for hoved i tilbudsanmodningssag** | **Højeste status for hoved i tilbudsanmodningssag** | **Laveste status for linje i tilbudsanmodningssag** | **Højeste status for linje i tilbudsanmodningssag** |
|----------------------------------------------------------|------------------------------------------------|-------------------------------------------------|-----------------------------------|------------------------------------|---------------------------------|----------------------------------|
| Registrer den ene kreditors bud på en tilbudsanmodning, og gem det.        | Afsendt                                           | Modtaget                                        | Afsendt                              | Modtaget                           | Afsendt                            | Modtaget                         |
| Registrer den anden kreditors bud på en tilbudsanmodning, og gem det. | Modtaget                                       | Modtaget                                        | Modtaget                          | Modtaget                           | Modtaget                        | Modtaget                         |


I eksemplet nedenfor kan du se højeste og laveste status for tilbudsanmodningssagen, hvor et bud er modtaget, og det andet bud er accepteret. Når et modtaget bud afvises, ændres den laveste status fra Modtaget til Afvist på linjen og i hovedet for tilbudsanmodningssagen.


|            <strong>Handling</strong>             | <strong>Laveste status på tværs af alle linjer i alle tilbudsanmodninger</strong> | <strong>Højeste status på tværs af alle linjer i alle tilbudsanmodninger</strong> | <strong>Laveste status for hoved i tilbudsanmodningssag</strong> | <strong>Højeste status for hoved i tilbudsanmodningssag</strong> | <strong>Laveste status for linje i tilbudsanmodningssag</strong> | <strong>Højeste status for linje i tilbudsanmodningssag</strong> |
|------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------|-------------------------------------------------|----------------------------------------------|-----------------------------------------------|
| Acceptér et af tilbuddene. (eller mindst én linje) |                          Modtaget                           |                           Accepteret                           |                    Modtaget                    |                    Accepteret                     |                   Modtaget                   |                   Accepteret                    |
|           Afvis alle andre bud.           |                          Afvist                           |                           Accepteret                           |                    Afvist                    |                    Accepteret                     |                   Afvist                   |                   Accepteret                    |


