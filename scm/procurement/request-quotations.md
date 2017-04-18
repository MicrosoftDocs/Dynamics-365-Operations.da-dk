---
title: Anmodningen om tilbud (tilbudsanmodninger)
description: "Denne artikel har en oversigt over tilbudsanmodninger, som organisationer udsteder, når de skal købe varer eller tjenesteydelser, og de ønsker at modtage konkurrencedygtige tilbud fra flere leverandører. I en tilbudsanmodning kan du bede leverandører om oplysninger om priser og leveringstider for det angivne antal varer. Du kan også bede leverandører angive, om der er ekstra gebyrer som f.eks. forsendelsesomkostninger eller eventuelle rabatter på store ordrer eller tidlig betaling af kreditorfakturaen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: d70b4ae0a6b177508021ee72481333cf6f265069
ms.lasthandoff: 03/31/2017


---

# <a name="request-for-quotations-rfqs"></a>Anmodningen om tilbud (tilbudsanmodninger)

Denne artikel har en oversigt over tilbudsanmodninger, som organisationer udsteder, når de skal købe varer eller tjenesteydelser, og de ønsker at modtage konkurrencedygtige tilbud fra flere leverandører. I en tilbudsanmodning kan du bede leverandører om oplysninger om priser og leveringstider for det angivne antal varer. Du kan også bede leverandører angive, om der er ekstra gebyrer som f.eks. forsendelsesomkostninger eller eventuelle rabatter på store ordrer eller tidlig betaling af kreditorfakturaen.

Anmodningsprocessen for tilbudsanmodning omfatter følgende opgaver:

-   Oprettelse og afsendelse af en tilbudsanmodning til en eller flere leverandører
-   Modtagelse og registrering af svar på tilbudsanmodning (bud)
-   Overførsel af accepterede bud på en indkøbsordre, købsaftale eller indkøbsrekvisition

I følgende illustration vises en oversigt over processen for anmodninger om tilbud.  

[![Anmodningen om tilbudsproces](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)  

Du kan oprette en tilbudsanmodning ud fra ordreforslag, ud fra en indkøbsrekvisition eller ud fra en manuel indtastning. Den tilbudsanmodning, du opretter, kaldes en tilbudsanmodningssag, og det er det grundlæggende dokument, som du bruger til at udstede en tilbudsanmodning til de enkelte leverandører. Når du forbereder tilbudsanmodningssagen og føje leverandører, skal du klikke på **sende** kladden oprettes på tilbudsanmodningssagen og en Tilbudsanmodning for hver leverandør, du har sendt Tilbudsanmodningen til. Du kan konfigurere indstillinger for udskriftsstyring for handlingen Send for at udskrive en rapport for hver kreditor til et arkiv, eller sende en rapport til e-mail-adresse for hver kreditor. Tilbudsanmodningskladden til hver leverandør kan desuden bruges til at generere en rapport, som du kan sende eller gensende til en kreditor senere. Du kan også konfigurere handlingen Send for at oprette et svarark, som kreditoren kan udfylde.  

Hvis du skal ændre en tilbudsanmodning, når du har sendt den, kan du sende tilbudsanmodningen til leverandører, når du er færdig.  

Når du modtager bud, skal du angive dem på siden **Svar på tilbudsanmodninger**. Hvis du vælger indstillingen **Kopiér data til svar**, kopieres data såsom antal og datoer fra tilbudsanmodningssagen til svaret. Du kan ændre disse data for at afspejle leverandørens bud.  

Hvis en anden gentagelse af et svar kræves for en bestemt kreditor, skal du klikke på **Returner** på siden **Svar på tilbudsanmodning**. Handlingen Returner genererer en ny kladde og en rapport, der udskrives, arkiveres og sendes i henhold til dine indstillinger for udskriftsstyring.  

Hvis du har føjet scorekriterier til din tilbudsanmodningssag, har svaret på tilbudsanmodningen et scorepanel, hvor du kan angive scorer. De samlede scorer vises, når du sammenligner svarene på siden **Sammenlign svar**, hvor du også kan sammenligne andre svardata, f.eks. linjepris og leveringsdato og den samlede pris.  

Når du har besluttet dig for et bud eller et delvist bud, kan du acceptere dem og afvise resten. Acceptkladder, afvisningskladder og tilsvarende rapporter genereres. Disse vil blive udskrevet, arkiveres og sendt i overensstemmelse med dine indstillinger for udskriftsstyring. Når du accepterer et tilbud eller bestemte linjer i et tilbud, en aftale eller køb indkøbsordre genereres, eller en indkøbsrekvisition opdateres, afhængigt af typen Tilbudsanmodningen køb. Du kan oprette en samhandelsaftale, der senere kan bruges til alle svarene, uanset om du har accepteret eller afvist dem.  

Status for tilbudsanmodningen vises i tilbudsanmodningens overskrift og afhænger af status for tilbudsanmodningens linjer. Status angiver, i hvilket omfang du har behandlet tilbudsanmodningen. Hver tilbudsanmodning har to statusværdier: laveste og højeste. Den laveste status er det mindst fremskredne stadie for en linje i tilbudsanmodningen, mens den højeste status er det mest fremskredne stadie for en linje i tilbudsanmodningen. Hvis f.eks. den mindst fremskredne fase i en tilbudsanmodning gælder en linje, der er blevet oprettet, er **Oprettet** den laveste status for tilbudsanmodningen. Hvis f.eks. den mest fremskredne fase i en tilbudsanmodning gælder en linje, der er blevet sendt til kreditorer, er **Sendt** den højeste status for tilbudsanmodningen. Status opdateres automatisk, mens tilbudsanmodningen behandles.  

Du kan få vist den laveste og højeste status for en tilbudsanmodnings hoved på siden **Alle tilbudsanmodninger**. Du kan få vist den laveste og højeste status for en linje på tilbudsanmodningen under fanen **Linjer** på siden **Tilbudsanmodninger**.  

Her er sekvensen af statusser for behandling af tilbudsanmodninger:

1.  **Oprettet**
2.  **Sent**
3.  **Received**
4.  **Accepteret**/**annulleret**/**afvist**

Statusserne beskrives mere detaljeret i andre afsnit senere i denne artikel.

## <a name="setting-up-rfq-functionality"></a>Konfigurere funktioner for tilbudsanmodning
Før du kan oprette en tilbudsanmodningssag, skal du konfigurere oplysninger om tilbudsanmodningen på siden **Indkøbs- og forsyningsparametre**. Når du opretter en tilbudsanmodningssag, kan du angive standardværdier, der kopieres til tilbudsanmodningen. Du kan angive følgende standardværdier:

-   Indkøbstypen af nye tilbudsanmodninger: **Indkøbsordre** eller **Købsaftale**
-   Indstillinger for udløbsdato og -klokkeslæt
-   Leveringsoplysninger og betalingsbetingelser.
-   Felter, der skal medtages i svaret på tilbudsanmodningen

Du kan tilsidesætte disse værdier for en bestemt tilbudsanmodningssag. Du skal også konfigurere ændringsprocessen. Som en del af denne konfiguration kan du aktivere feltlåsning. Når feltlåsning er aktiveret, skal en indkøber, der ønsker at ændre en tilbudsanmodning, først klikke på **Opret** i sektionen **Ændring** under fanen **Tilbud**. Når Tilbudsanmodningen er blevet opdateret med ændringer, professionelle indkøb skal fuldføre processen ved at klikke på **Færdiggør**. ** ** de færdiggør handling genererer en e-mail, der underretter kreditorerne om ændrede Tilbudsanmodningen. Du kan vælge skabelonen til den mailmeddelelse, der sendes til kreditorer, på siden **Indkøbs- og forsyningsparametre**. Når der oprettes en skabelon, kan den indeholde følgende erstatningstokens:

-   %Årsag til returnering af bud%
-   %Årsag til ændring%
-   %Ændring udarbejdet af%
-   %Firma%

De angivne tokens %Årsag til returnering af bud% og %Årsag til ændring% erstattes af tekst, der indkøberen kan skrive, når han eller hun afslutter ændringen i guiden **Ændring**. Værdierne for tokenerne %Ændring udarbejdet af% og %Firma% hentes automatisk fra tilbudsanmodningen.  

Hvis du vil bruge årsagskoder på en tilbudsanmodning til at angive, hvorfor et tilbud blev afvist eller godkendt, skal du oprette årsagskoder på siden **Leverandørårsager**.  

Du kan konfigurere udseendet af dine udskrevne eller gemte dokumenter med tilbudsanmodninger på siden **Formularopsætning** i Indkøb og forsyning.  

Når du opretter en tilbudsanmodning til en indkøbsordre og føjer en lagervare til tilbudsanmodningen, oprettes der en lagerpostering med tilgangsstatussen **Tilbudskvittering**. Kun linjer i tilbudsanmodninger med denne status kommer i betragtning når du bruger en masterplan til beregning af forsyninger. Hvis du ønsker, at behovsplanen skal omfatte tilbudsanmodningslinjer som en forventet tilgang, skal du konfigurere denne funktionsmåde i opsætningen af varedisponering.  

Som indkøbschef eller -agent kan du oprette og vedligeholde anmodningstyper, der passer til indkøbskravene i din organisation. Hver anmodningstype kan baseres på scoremetoder. Scoremetoder består af et sæt af kriterier, der kan bruges, når du scorer bud. Du skal oprette anmodningstyper, scoremetoder og scorekriterier på siderne den **Anmodningstype** og **Scoremetode**.

## <a name="creating-and-sending-an-rfq"></a>Oprette og sende en tilbudsanmodning
Du skal oprette en tilbudsanmodning, vælge de leverandører, som skal byde på tilbudsanmodningen, og derefter sende tilbudsanmodningen til leverandørerne. Du kan bruge udskriftsstyring til at sende rapporten over tilbudsanmodningen og rapporterne med svarark til din foretrukne destination.  

Du kan oprette en tilbudsanmodning for indkøbstypen **Indkøbsordre** eller **Købsaftale**.  

Hvis tilbudsanmodningen oprettes ud fra en indkøbsrekvisition, tildeles typen **Indkøbsrekvisition** automatisk. Du kan manuelt oprette en tilbudsanmodning af typen **Indkøbsrekvisition**. Hvis tilbudsanmodningen er af typen **Indkøbsordre**:

-   Når der oprettes linjer i en tilbudsanmodning, oprettes der lagerposter, der har tilgangsstatussen **Tilbudskvittering**.
-   Når du accepterer et tilbud, genereres der en indkøbsordre.

Hvis tilbudsanmodningen er af typen **Købsaftale**:

-   Tilbudsanmodningen bruges til en aftale om at købe et bestemt antal eller for en bestemt værdi af et produkt over tid. Du skal vælge det datointerval, der gælder for indkøbsaftalen, og navnet på den person, der håndterer indkøbsaftalen.
-   Når du accepterer et tilbud, genereres der en købsaftale.

Du kan kun oprette en tilbudsanmodning ud fra en indkøbsrekvisition, hvis status for indkøbsrekvisitionen er **Til gennemsyn**, og du er tildelt til den næste opgave i arbejdsgangen. Linjerne i indkøbsrekvisitionen opdateres automatisk, når du accepterer linjer fra svar på tilbudsanmodninger (bud), du har modtaget fra leverandører. Du kan ikke udføre, afvise, godkende eller udføre nogen handlinger på indkøbsrekvisitionen, mens anmodningen om tilbud behandles.  

Når du opretter en tilbudsanmodning, kan du vælge en bestemt anmodningstype. Anmodningstypen bestemmer det sæt scorekriterier, der bruges til at give scoresvar på tilbudsanmodningen.  

Du kan føje et spørgeskema til en tilbudsanmodningssag. Dette spørgeskema vises derefter på alle svar, når du har sendt tilbudsanmodningen.  

Du kan vælge kreditorerne, der skal føjes til en tilbudsanmodningssag, på tre måder:

-   Tilføj kreditorerne én efter én.
-   Søg efter alle de leverandører, der opfylder bestemte kriterier.
-   Tilføj automatisk alle kreditorer, der er godkendt til de indkøbskategorier, der bruges på linjerne i tilbudsanmodningen.

Når tilbudsanmodningssagen er klar, skal du klikke på **Send**. Handlingen Send genererer kladder og rapporter, der udskrives, arkiveres og sendes i henhold til dine indstillinger for udskriftsstyring.  

Hvis du har markeret afkrydsningsfelterne **Brug kreditor til genberegning af priser** og **Brug kreditorspecifikke vareoplysninger** på siden afkrydsningsfelterne i den **Sender tilbudsanmodning**, når du har sendt anmodningen til kreditorer, angives nogle af de leverandørspecifikke oplysninger automatisk. Du kan redigere oplysningerne på siden **Svar på tilbudsanmodning**.  

Følgende tabel viser, hvordan status for tilbudsanmodningen ændres, når du opretter en tilbudsanmodning og sender den til kreditorer.

|                                    |                              |                                                 |                            |                             |
|------------------------------------|------------------------------|-------------------------------------------------|----------------------------|-----------------------------|
| **Action**                         | **Lowest RFQ header status** | **Highest RFQ header status**                   | **Lowest RFQ line status** | **Highest RFQ line status** |
| Opret sidehoved og linje for Tilbudsanmodning.    | Oprettet                      | Oprettet                                         | Oprettet                    | Oprettet                     |
| Sende tilbudsanmodningen til en bestemt kreditor. | Sendt                         | Sendt                                            | Sendt                       | Sendt                        |
| Tilføj en anden kreditor.                | Oprettet                      | Sendt (tilbudsanmodningen er kun sendt til én kreditor). | Oprettet                    | Sendt                        |
| Sende tilbudsanmodningen til den anden leverandør. | Sendt                         | Sendt                                            | Sendt                       | Sendt                        |

**Bemærk!** Du kan føje flere leverandører til en tilbudsanmodning efter behov, og laveste og højeste status ændres til at afspejle de nye leverandører. Hvis du f.eks. har modtaget tilbud fra alle kreditorerne, og du har accepteret mindst én linje i et tilbud, vil laveste status for tilbudsanmodningens header være **Afvist**, og højeste status vil være **Accepteret**. Hvis du tilføjer en ny kreditor, vil den laveste status på en linje nu være **Oprettet**. Derefter ændrer den laveste status i tilbudsanmodnings hoved til **Oprettet**, mens den højeste status forbliver **Accepteret**.

## <a name="amending-an-rfq"></a>Ændring af en tilbudsanmodning
Nogle gange skal du ændre en tilbudsanmodning, når du har sendt den. Dette kan f.eks. ske, fordi leveringsdatoerne er ændret, eller du ønsker yderligere produkter eller forskellige mængder af produkter. Du kan konfigurere ændringsprocessen, så den er mere restriktiv eller mindre restriktiv.  

Hvis du bruger den mere restriktive ændringsproces, skal du klikke på **Opret** på tilbudsanmodningssagen for at starte en ændring, før du kan redigere felterne på tilbudsanmodningssagen. Når du har foretaget dine ændringer, skal du klikke på **Færdiggør**. Derefter føres du gennem processen for tilføjelse af oplysninger i den mail, der sendes for at give leverandørerne besked om ændringen. Den opdaterede tilbudsanmodningsrapport, som indeholder en ændringsnote, knyttes automatisk til meddelelsen.  

Hvis du bruger den mindre restriktive ændringsproces, behøver du ikke at oprette en ændring, før du kan redigere felterne på en tilbudsanmodningssag, der allerede er sendt. Du skal dog manuelt føje en ændringsnote til tilbudsanmodningen.

## <a name="receiving-and-registering-rfq-replies"></a>Modtagelse og registrering af svar på tilbudsanmodningen
Når du sender en tilbudsanmodning, oprettes der automatisk et svarark. Når du modtager svar (bud) på en tilbudsanmodning, skal du angive svaroplysningerne fra hver enkelt leverandør i et leverandørspecifikt ark med tilbudsanmodningssvar. Hvis du har tilføjet scorekriterier, kan du angive score for svarene. Du kan derefter sammenligne leverandørbuddene og rangere dem ud fra scorekriterier som f.eks. bedste samlede pris eller bedste samlede leveringstid.  

Hvis der er knyttet et spørgeskema til tilbudsanmodningssagen, skal du manuelt angive svarene på spørgsmålene i svararket.  

Hvis du skal angive alternative linjer, og tilbudsanmodningssagen tillader dette, skal du klikke på **Tilføj linje** på oversigtspanelet **Købstilbudslinjer **. Angiv derefter oplysninger om produktet, f.eks. vareantal eller indkøbskategori, antal, pris og rabat.  

Hvis du har skrevet et svar, men det kræver et nyt tilbud fra leverandøren, kan du sende Tilbudsanmodningen. Der oprettes en ny kladde og en rapport, som du kan bruge til at anmode om ændringer fra leverandøren.  

Du kan se en oversigt over alle tilbudsanmodninger og statusser for deres svar på siden **Opfølgning på tilbudsanmodning**.  

I følgende tabel vises, hvordan status for tilbudsanmodningen ændres, efterhånden du modtager tilbud og registrerer oplysningerne i svararket til tilbudsanmodningen.

|                                                |                       |                        |                              |                               |                            |                             |
|------------------------------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Action**                                     | **Lowest bid status** | **Highest bid status** | **Lowest RFQ header status** | **Highest RFQ header status** | **Lowest RFQ line status** | **Highest RFQ line status** |
| Registrer én kreditors tilbud, og gem det.        | Sendt                  | Modtaget               | Sendt                         | Modtaget                      | Sendt                       | Modtaget                    |
| Registrer den anden kreditors tilbud, og gem det. | Modtaget              | Modtaget               | Modtaget                     | Modtaget                      | Modtaget                   | Modtaget                    |

**Bemærk!** Hvis du returnerer et bud til en kreditor for at forhandle yderligere, forbliver laveste og højeste status begge **Modtaget**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Acceptere og afvise bud og overføre accepterede bud til downstream-dokumenter

Når du har fundet det bedste bud, f.eks. buddet med den bedste samlede pris, kan du acceptere buddet. Status for tilbudsanmodningssvaret for leverandøren opdateres til **Accepteret**. Når du accepterer et bud eller bestemte linjer i et bud, oprettes der automatisk en indkøbsordre eller en købsaftale, og du kan afvise buddene fra de øvrige leverandører.  

Når du accepterer et tilbudsanmodningssvar af typen **Indkøbsrekvisition**, opdaterer svarlinjerne for tilbudsanmodningen indkøbsrekvisitionslinjerne med følgende oplysninger:

-   Enhedspris
-   Rabatprocent
-   Rabatbeløb
-   Indkøbstillæg
-   Linjetillæg
-   Kreditor
-   Eksternt nummer
-   Ekstern beskrivelse

I svaret kan du tilføje en årsagskode for at forklare, hvorfor du har accepteret eller afvist et bud.  

Du kan acceptere nogle af linjerne i et bud og afvise andre. Du kan også acceptere linjer fra forskellige leverandører. Bare vær opmærksom på, at hvis du accepterer nogle linjer, vil du blive bedt om at afvise alle andre linjer. Så hvis du vil acceptere andre linjer, skal du klikke på **Annuller**, når du bliver spurgt om det.  

I følgende tabel vises, hvordan status for tilbudsanmodningen ændres, efterhånden som du accepterer eller afviser bud fra kreditorer.

|                         |                       |                        |                              |                               |                            |                             |
|-------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Action**              | **Lowest bid status** | **Highest bid status** | **Lowest RFQ header status** | **Highest RFQ header status** | **Lowest RFQ line status** | **Highest RFQ line status** |
| Acceptér et af tilbuddene. | Modtaget              | Accepteret               | Modtaget                     | Accepteret                      | Modtaget                   | Accepteret                    |
| Afvis de andre bud.  | Afvist              | Accepteret               | Afvist                     | Accepteret                      | Afvist                   | Accepteret                    |



