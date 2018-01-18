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
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 42ab7beb8a269cd37fd9100385bd302e4945c1e0
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---

# <a name="requests-for-quotation-rfqs"></a>Tilbudsanmodning

[!include[banner](../includes/banner.md)]

Emnet giver et overblik over tilbudsanmodninger. Organisationer sender en tilbudsanmodning, når de ønsker at modtage konkurrencedygtige tilbud fra flere leverandører på de varer eller ydelser, de har brug for at købe. I en tilbudsanmodning kan du bede leverandører om oplysninger om priser og leveringstider for det angivne antal varer. Du kan også bede leverandører angive, om der er ekstra gebyrer som f.eks. forsendelsesomkostninger eller eventuelle rabatter på store ordrer eller tidlig betaling af kreditorfakturaen.

Tilbudsanmodningsprocessen består af følgende opgaver:

1. Oprette og sende en tilbudsanmodning til en eller flere leverandører.
2. Modtage og registrere svar på tilbudsanmodninger (bud).
3. Overføre bud, du accepterer, til en indkøbsordre, købsaftale eller indkøbsrekvisition.

I følgende illustration vises en oversigt over processen for anmodninger om tilbud.

[![RFQ-proces (Radio Frequency Identification-proces)](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Du kan oprette en tilbudsanmodning ud fra ordreforslag, ud fra en indkøbsrekvisition eller ved manuel indtastning. Den tilbudsanmodning, du opretter, kaldes en tilbudsanmodningssag. Tilbudsanmodningssagen er det grundlæggende dokument, du bruger til at udstede en tilbudsanmodning til hver leverandør.

Når du har forberedt tilbudsanmodningssagen og tilføjet leverandører, skal du vælge **Send** i tilbudsanmodningssagen. Der oprettes en tilbudsanmodningskladde for hver leverandør, som du sendte tilbudsanmodningen til. Du kan konfigurere indstillinger for Udskriftsstyring for handlingen Send, så der enten udskrives en rapport for hver leverandør til et arkiv, eller sendes en rapport til hver leverandørs mailadresse. Du kan desuden bruge tilbudsanmodningskladden til hver leverandør til at generere en rapport, som du kan sende eller gensende til leverandøren senere. Du kan også konfigurere handlingen Send, så den opretter et svarark, som leverandøren kan udfylde.

Dette emne beskriver processen til håndtering af tilbudsanmodninger, når der ikke bruges kreditorsamarbejde. Hvis dit system er konfigureret til kreditorsamarbejde, kan leverandører afgive bud direkte i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Du kan finde flere oplysninger i [Kreditorsamarbejde med kunder](vendor-collaboration-work-customers-dynamics-365-operations.md).
 
Hvis du skal ændre en tilbudsanmodning, når du har sendt den, du kan sende tilbudsanmodningen til leverandører igen, når du er færdig, ved hjælp af to ændringshandlinger: Opret og Færdiggør.

Når du modtager bud med e-mail, skal du angive dem på siden **Svar på tilbudsanmodninger**. Hvis du vælger indstillingen **Kopiér data til svar**, kopieres data såsom antal og datoer fra tilbudsanmodningssagen til svaret. Du kan ændre disse data for at afspejle leverandørens bud.

Hvis en anden gentagelse af et svar kræves for en kreditor, skal du vælge **Returner** på siden **Svar på tilbudsanmodning**. Handlingen Returner genererer en ny kladde og en rapport, der udskrives, arkiveres og sendes i henhold til dine indstillinger for Udskriftsstyring.

Hvis du har føjet scorekriterier til din tilbudsanmodningssag, har svaret på tilbudsanmodningen et scorepanel, hvor du kan angive scorer. De samlede resultater vises, når du sammenligner svarene på siden **Sammenlign svar**. Du kan også sammenligne andre svardata på siden, f.eks. linjepris, leveringsdato og den samlede pris.

Når du har valgt et bud eller et delvist bud, kan du acceptere dem og afvise resten. Der oprettes acceptkladder, afvisningskladder og tilsvarende rapporter, som udskrives, arkiveres og sendes i henhold til dine indstillinger for Udskriftsstyring. Når du accepterer et bud eller bestemte linjer i et bud, oprettes der enten en købsaftale eller indkøbsordre, eller en indkøbsrekvisition opdateres, afhængigt af indkøbstypen for tilbudsanmodningen. Du kan oprette en samhandelsaftale, der senere kan bruges til alle svarene, uanset om du har accepteret eller afvist dem.

Status for tilbudsanmodningen vises i tilbudsanmodningens overskrift og afhænger af status for tilbudsanmodningens linjer. Status angiver, hvor meget du har behandlet tilbudsanmodningen. Hver tilbudsanmodning har to statusværdier: laveste og højeste status. Den laveste status er det mindst fremskredne stadie for en linje i tilbudsanmodningen, mens den højeste status er det mest fremskredne stadie for en linje i tilbudsanmodningen. Hvis f.eks. den mindst fremskredne fase i en tilbudsanmodning gælder en linje, der er blevet oprettet, er **Oprettet** den laveste status for tilbudsanmodningen. Hvis f.eks. den mest fremskredne fase i en tilbudsanmodning gælder en linje, der er blevet sendt til kreditorer, er **Sendt** den højeste status for tilbudsanmodningen. Status opdateres automatisk, mens tilbudsanmodningen behandles.

Du kan få vist den laveste og højeste status for en tilbudsanmodnings hoved på siden **Alle tilbudsanmodninger**. Du kan få vist den laveste og højeste status for en linje på tilbudsanmodningen under fanen **Linjer** på siden **Tilbudsanmodninger**.

Her er sekvensen af statusser for behandling af tilbudsanmodninger:

1. **Oprettet**
2. **Afsendt**
3. **Modtaget**
4. **Accepteret**, **Annulleret** eller **Afvist**

Disse statusser beskrives mere detaljeret senere i dette emne.

## <a name="setting-up-rfq-functionality"></a>Konfigurere funktioner for tilbudsanmodning

Før du kan oprette en tilbudsanmodningssag, skal du konfigurere oplysninger om tilbudsanmodningen på siden **Indkøbs- og forsyningsparametre**. Når du opretter en tilbudsanmodningssag, kan du angive standardværdier, der kopieres til tilbudsanmodningen. Du kan angive følgende standardværdier:

- Indkøbstypen af nye tilbudsanmodninger: **Indkøbsordre** eller **Købsaftale**
- Udløbsdatoen og -klokkeslættet
- Leveringsoplysninger og betalingsbetingelser
- Felter, der skal medtages i svaret på tilbudsanmodningen

Du kan tilsidesætte disse værdier for en bestemt tilbudsanmodningssag.

Du skal også konfigurere ændringsprocessen. Som en del af denne konfiguration kan du aktivere feltlåsning. Når feltlåsning er aktiveret, skal en indkøber, der ønsker at ændre en tilbudsanmodning, først klikke på **Opret** i sektionen **Ændring** under fanen **Tilbud**. Når tilbudsanmodningen er blevet opdateret med ændringen, skal indkøberen fuldføre processen ved at vælge **Færdiggør**. Handlingen Færdiggør genererer en e-mail, der giver besked til leverandørerne om den ændrede tilbudsanmodning.

På siden **Indkøbs- og forsyningsparametre** kan du vælge, hvilken skabelon der skal bruges til den mailmeddelelse, der sendes til kreditorer. Når der oprettes en skabelon, kan den indeholde følgende erstatningstokens:

- %Tilbudsanmodningssag%
- %Årsag til returnering af bud%
- %Årsag til ændring%
- %Ændring udarbejdet af%
- %Firma%
- %Navn på tilbudsanmodningssag%
- %ExpiryDateTime%
- %Dato%

De angivne tokens %Årsag til returnering af bud% og %Årsag til ændring% erstattes af tekst, der indkøberen kan skrive, når han eller hun afslutter ændringen i guiden **Ændring**. Værdierne for tokenerne %Ændring udarbejdet af% og %Firma% hentes automatisk fra tilbudsanmodningen. %Dato%-tokenet erstattes af dags dato.

Der kræves også en e-mailskabelon, hvis du annullerer en tilbudsanmodning, når den er blevet sendt. Denne e-mailskabelon bruges til at sende besked om annulleringen til leverandørens kontaktpersoner. Skabelonen skal være markeret på siden **Indkøbs- og forsyningsparametre**. Når skabelonen er oprettet, kan den indeholde følgende erstatningstokens:

- %Årsag til annullering%
- %Tilbudsanmodningssag% 
- %Tilbudsanmodning annulleret af%
- %Firma%
- %Navn på tilbudsanmodningssag%
- %Dato%

Tokenet %Årsag til annullering% erstattes af tekst, som indkøberen kan angive i guiden **Annullering**. %Dato%-tokenet erstattes af dags dato.

Hvis du vil bruge årsagskoder på en tilbudsanmodning til at angive, hvorfor et tilbud blev afvist eller godkendt, skal du oprette årsagskoder på siden **Leverandørårsager**.

På siden **Formularopsætning** i Indkøb og forsyning kan du konfigurere udseendet af dine udskrevne eller gemte dokumenter med tilbudsanmodninger.

> [!NOTE]
> For en konfigurationen til offentlige institutioner skal du bruge ændringsprocessen til at ændre en tilbudsanmodning, der er allerede blevet sendt. Når en tilbudsanmodning er sendt, er felter skrivebeskyttede. Når du vil foretage ændringer af tilbudsanmodningen, skal du derfor vælge **Opret** for at starte ændringsprocessen som beskrevet tidligere. Låsningsfunktionen styres af indstillingen **Lås tilbudsanmodninger, når de er sendt** på siden **Indkøbs- og forsyningsparametre**. Denne parameter er som standard indstillet til **Ja**, og for en konfiguration til den offentlige sektor kan standardindstillingen ikke ændres. Derfor selvom ændringsprocessen kan håndteres manuelt i en ikke-offentlig sektor-konfiguration, skal den bruges til en offentlig sektor-konfiguration.

Når du opretter en tilbudsanmodning til en indkøbsordre og føjer en lagervare til tilbudsanmodningen, oprettes der en lagerpostering med tilgangsstatussen **Tilbudskvittering**. Kun linjer i tilbudsanmodninger med denne status kommer i betragtning når du bruger en masterplan til beregning af forsyninger. Hvis du ønsker, at behovsplanen skal omfatte tilbudsanmodningslinjer som en forventet tilgang, skal du konfigurere denne funktionsmåde i opsætningen af varedisponering.

Som indkøbschef eller -agent kan du oprette og vedligeholde anmodningstyper, der passer til indkøbskravene i din organisation. Hver anmodningstype kan knyttes til en scoremetode. Scoremetoder består af et sæt af kriterier, der kan bruges, når du scorer bud. Du skal oprette anmodningstyper, scoremetoder og scorekriterier på siderne den **Anmodningstype** og **Scoremetode**.

## <a name="creating-and-sending-an-rfq"></a>Oprette og sende en tilbudsanmodning

Du skal oprette en tilbudsanmodning, vælge de leverandører, som skal byde på tilbudsanmodningen, og derefter sende tilbudsanmodningen til leverandørerne. Du kan bruge Udskriftsstyring til at sende rapporten over tilbudsanmodningen og rapporterne med svarark til din foretrukne destination.

Du kan oprette en tilbudsanmodning af indkøbstypen **Indkøbsordre** eller **Købsaftale**.

Hvis tilbudsanmodningen er af typen **Indkøbsordre**, sker der følgende:

- Når der oprettes linjer i en tilbudsanmodning, oprettes der lagerposter, der har tilgangsstatussen **Tilbudskvittering**.
- Når du accepterer et tilbud, genereres der en indkøbsordre.

Hvis tilbudsanmodningen er af typen **Indkøbsaftale**, sker der følgende:

- Tilbudsanmodningen bruges til en aftale om at købe et bestemt antal eller for en bestemt værdi af et produkt over tid. Du skal vælge det datointerval, der gælder for indkøbsaftalen, og navnet på den person, der håndterer indkøbsaftalen.
- Når du accepterer et tilbud, genereres der en købsaftale.

Hvis tilbudsanmodningen oprettes ud fra en indkøbsrekvisition, tildeles typen **Indkøbsrekvisition** automatisk. Du kan manuelt oprette en tilbudsanmodning af typen **Indkøbsrekvisition**.

Du kan kun oprette en tilbudsanmodning ud fra en indkøbsrekvisition, hvis status for indkøbsrekvisitionen er **Til gennemsyn**, og du er tildelt til den næste opgave i arbejdsgangen. Linjerne i indkøbsrekvisitionen opdateres automatisk, når du accepterer linjer fra svar på tilbudsanmodninger (bud), du har modtaget fra leverandører. Du kan ikke udføre, afvise, godkende eller udføre nogen handlinger på indkøbsrekvisitionen, mens anmodningen om tilbud behandles.

Når du opretter en tilbudsanmodning, kan du vælge en anmodningstype. Anmodningstypen bestemmer det sæt scorekriterier, der bruges til at give scoresvar på tilbudsanmodningen.

Du kan føje et spørgeskema til en tilbudsanmodningssag. Dette spørgeskema vises derefter på alle svar, når du har sendt tilbudsanmodningen.

Du kan vælge kreditorerne, der skal føjes til en tilbudsanmodningssag, på tre måder:

- Tilføj kreditorerne én efter én.
- Søg efter alle de leverandører, der opfylder bestemte kriterier.
- Tilføj automatisk alle kreditorer, der er godkendt til de indkøbskategorier, der bruges på linjerne i tilbudsanmodningen.

Når tilbudsanmodningssagen er klar, skal du vælge **Send**. Handlingen Send genererer kladder og rapporter, der udskrives, arkiveres og sendes i henhold til dine indstillinger for Udskriftsstyring.

Hvis du indstillede **Brug kreditor til genberegning af priser** og **Brug kreditorspecifikke vareoplysninger** til **Ja** på siden **Sender tilbudsanmodning**, da du sendte tilbudsanmodningen til kreditorer, angives nogle af de leverandørspecifikke oplysninger automatisk. Du kan redigere oplysningerne på siden **Svar på tilbudsanmodning**.

Følgende tabel viser, hvordan status for tilbudsanmodningen ændres, når du opretter en tilbudsanmodning og sender den til kreditorer.

| Handling                             | Laveste hovedstatus for tilbudsanmodning | Højeste hovedstatus for tilbudsanmodning                        | Laveste linjestatus for tilbudsanmodning | Højeste linjestatus for tilbudsanmodning |
|------------------------------------|--------------------------|--------------------------------------------------|------------------------|-------------------------|
| Opret sidehoved og linje for Tilbudsanmodning.    | Oprettet                  | Oprettet                                          | Oprettet                | Oprettet |
| Sende tilbudsanmodningen til en bestemt kreditor. | Sendt                     | Sendt                                             | Sendt                   | Sendt |
| Tilføj en anden kreditor.                | Oprettet                  | Sendt (tilbudsanmodningen er kun sendt til én kreditor). | Oprettet                | Sendt |
| Sende tilbudsanmodningen til den anden leverandør. | Sendt                     | Sendt                                             | Sendt                   | Sendt |

> [!NOTE]
> Du kan føje flere leverandører til en tilbudsanmodning efter behov, og laveste og højeste status opdateres og afspejler de nye leverandører. Hvis du f.eks. har modtaget tilbud fra alle kreditorerne, og du har accepteret mindst én linje i et tilbud, vil laveste status for tilbudsanmodningens header være **Afvist**, og højeste status vil være **Accepteret**. Hvis du tilføjer en ny kreditor, vil den laveste status på en linje nu være **Oprettet**. Derefter opdateres den laveste status i tilbudsanmodnings hoved til **Oprettet**, mens den højeste status forbliver **Accepteret**.

## <a name="amending-an-rfq"></a>Ændring af en tilbudsanmodning

Nogle gange skal du ændre en tilbudsanmodning, når du har sendt den. Du skal evt. ændre en tilbudsanmodning, hvis f.eks. leveringsdatoerne er ændret, eller du ønsker yderligere produkter eller forskellige mængder af produkter. Du kan konfigurere ændringsprocessen, så den er mere restriktiv eller mindre restriktiv.

Hvis du har konfigureret ændringsprocessen, så den er mere restriktiv, skal du, før du kan ændre felterne i en tilbudsanmodningssag, der er allerede sendt, vælge **Opret** i tilbudsanmodningssagen for at starte en ændring. Når du har afsluttet dine ændringer, skal du vælge **Færdiggør**. Derefter føres du gennem processen med at tilføje oplysninger i den mail, der sendes for at give leverandørerne besked om ændringen. Den opdaterede tilbudsanmodningsrapport, som indeholder en ændringsnote, knyttes automatisk til e-mailen.

Hvis du har konfigureret ændringsprocessen, så den er mindre restriktiv, behøver du ikke at vælge **Opret**, før du kan redigere felterne i en tilbudsanmodningssag, der allerede er sendt. Du skal dog manuelt føje en ændringsnote til tilbudsanmodningen og sende sagen igen. Vær opmærksom på, at denne fremgangsmåde kun kan bruges, hvis ingen af svarene (buddene) er blevet redigeret. Hvis du har angivet et svar, og det er i **Modtaget**-tilstand, er knappen **Send** ikke tilgængelig. I så fald skal du vælge **Opret** og derefter **Færdiggør**, som du skal gøre i den mere restriktive proces. Svaret nulstilles derefter for at afspejle ændringerne af tilbudsanmodningssagen. 

Hvis kreditorer bruger grænsefladen til kreditorsamarbejde til at afgive bud, skal du altid bruge ændringsprocessen for at oplyse kreditorerne om ændringerne af tilbudsanmodningssagen. Dette hjælper med at forhindre en situation, hvor leverandører byder på en forældet tilbudsanmodningssag, mens de har et igangværende bud. Du kan finde flere oplysninger om kreditorsamarbejde under [Kreditorsamarbejde med eksterne kreditorer](vendor-collaboration-work-external-vendors.md). 

Hvis du vil invitere flere leverandører til at byde, og der ikke er foretaget nogen ændringer af tilbudsanmodningssagen, kan du bruge knappen **Send**. De leverandører, du har tilføjet, vises på siden **Send** og modtager e-mailinvitationen.

## <a name="receiving-and-registering-rfq-replies"></a>Modtagelse og registrering af svar på tilbudsanmodningen

Når du sender en tilbudsanmodning, oprettes der automatisk et svarark. Når du modtager svar (bud) på en tilbudsanmodning, skal du angive svaroplysningerne fra hver enkelt leverandør i et leverandørspecifikt ark med tilbudsanmodningssvar. Hvis du har tilføjet scorekriterier, kan du angive score for svarene. Du kan derefter sammenligne leverandørbuddene og rangere dem ud fra scorekriterier som f.eks. bedste samlede pris eller bedste samlede leveringstid.

Hvis der er knyttet et spørgeskema til tilbudsanmodningssagen, skal du manuelt angive svarene på spørgsmålene i svararket.

Du kan også angive alternative linjer, hvis tilbudsanmodningssagen tillader alternative linjer. Vælg **Tilføj linje** i oversigtspanelet **Købstilbudslinjer**. Angiv derefter oplysninger om produktet, f.eks. vareantal eller indkøbskategori, antal, pris og rabat.

Hvis du har skrevet et svar, men det kræver et nyt tilbud fra leverandøren, kan du sende tilbudsanmodningen igen. Der oprettes en ny kladde og rapport, som du kan bruge til at anmode om ændringer fra leverandøren.

Du kan se en oversigt over alle tilbudsanmodninger og statusser for deres svar på siden **Opfølgning på tilbudsanmodning**.

I følgende tabel vises, hvordan status for tilbudsanmodningen ændres, efterhånden du modtager tilbud og registrerer oplysningerne i svararket til tilbudsanmodningen.

| Handling                                         | Laveste tilbudsstatus | Højeste tilbudsstatus | Laveste hovedstatus for tilbudsanmodning | Højeste hovedstatus for tilbudsanmodning | Laveste linjestatus for tilbudsanmodning | Højeste linjestatus for tilbudsanmodning |
|------------------------------------------------|-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Registrer én kreditors tilbud, og gem det.        | Afsendt              | Modtaget           | Afsendt                     | Modtaget                  | Afsendt                   | Modtaget |
| Registrer den anden kreditors tilbud, og gem det. | Modtaget          | Modtaget           | Modtaget                 | Modtaget                  | Modtaget               | Modtaget |

> [!NOTE]
> Hvis du returnerer et bud til en kreditor for at forhandle yderligere, forbliver laveste og højeste status begge **Modtaget**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Acceptere og afvise bud og overføre accepterede bud til downstream-dokumenter

Når du har fundet det bedste bud, f.eks. buddet med den bedste samlede pris, kan du acceptere buddet. Du kan acceptere nogle af linjerne i et bud og afvise andre. Du kan også acceptere linjer fra forskellige leverandører. Vær opmærksom på, at hvis du accepterer nogle linjer, bliver du bedt om at afvise alle andre linjer. Så hvis du vil acceptere andre linjer, skal du vælge **Annuller**, når du bliver bedt om det. Status for svaret på tilbudsanmodningen for hver leverandør, du accepterer bud eller linjer fra, opdateres til **Godkendt**. 

Når du accepterer et bud eller bestemte linjer i et bud, oprettes der automatisk en indkøbsordre eller en købsaftale. Derefter kan du afvise bud fra de øvrige leverandører.

I svaret kan du tilføje en årsagskode for at forklare, hvorfor du har accepteret eller afvist et bud.

Når du accepterer et tilbudsanmodningssvar af typen **Indkøbsrekvisition**, opdaterer svarlinjerne for tilbudsanmodningen indkøbsrekvisitionslinjerne med følgende oplysninger:

- Enhedspris
- Rabatprocent
- Rabatbeløb
- Indkøbstillæg
- Linjetillæg
- Leverandør
- Eksternt nummer
- Ekstern beskrivelse

I følgende tabel vises, hvordan status for tilbudsanmodningen ændres, efterhånden som du accepterer eller afviser bud fra kreditorer.

| Handling                      | Laveste tilbudsstatus | Højeste tilbudsstatus | Laveste hovedstatus for tilbudsanmodning | Højeste hovedstatus for tilbudsanmodning | Laveste linjestatus for tilbudsanmodning | Højeste linjestatus for tilbudsanmodning |
|-------------------------    |-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Acceptér et af tilbuddene.     | Modtaget          | Accepteret           | Modtaget                 | Accepteret                  | Modtaget               | Accepteret |
| Afvis alle andre bud.  | Afvist          | Accepteret           | Afvist                 | Accepteret                  | Afvist               | Accepteret |

