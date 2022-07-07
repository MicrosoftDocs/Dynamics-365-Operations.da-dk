---
title: Commerce-bogføringsparametre
description: Denne artikel beskriver de parametre, der gælder specifikt for bogføringen af økonomiske og fysiske posteringer i Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 56a2d1d2bcafdcdd9d88c132986e8ef485bf6b24
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027222"
---
# <a name="commerce-posting-parameters"></a>Commerce-bogføringsparametre

[!include [banner](includes/banner.md)]

Denne artikel beskriver de parametre, der gælder specifikt for bogføringen af økonomiske og fysiske posteringer i Microsoft Dynamics 365 Commerce. Parametre til handelsbogføring findes i Commerce headquarters i **Detail og handel \> Headquarters-konfiguration \> Parametre \> Commerce-parametre \> Bogføring**.

## <a name="periodic-discount-parameters"></a>Periodiske rabatparametre

Følgende tabel viser de periodiske rabatparametre, der gælder specifikt for bogføringen af økonomiske og fysiske posteringer.

| Parameter | Beskrivende tekst |
|-----------|-------------|
| Bogfør periodisk rabat | Denne indstilling kontrollerer, om periodiske tilbud bogføres på finanskontiene. Periodiske rabatter omfatter mix og match-rabatter, mængderabatter og rabattilbud. Når denne parameter er aktiveret, kan der angives flere felter i afsnittet **Periodiske rabatter**. |
| Finanskontotype | <p>Vælg, hvilken type finanskonto bruger til at bogføre periodiske rabatter:</p><ul><li>**Standard** – Systemet bruger ikke de rabatrelaterede felter på denne side. I stedet bruger programmet de konti, der er defineret på **bogføringssiden** i Commerce headquarters (**Lagerstyring \> Konfiguration \> Bogføring \> Bogføringsformularer**).</li><li>**Periodisk** – Systemet bruger de handelsrabatkonti, der er angivet af de rabatrelaterede felter på denne side. Hvis du vælger denne indstilling, skal du angive en finanskonto (GL) for hver type tilbud (rabat, mix og match-rabat, mængde og tærskel). Når du konfigurerer hver rabat, kan du definere en konto. Når funktionen til rabatkontobogføring bruges på opsætningssiden til rabat, foretages der en yderligere debetpost og kreditpost for at genklassificere rabatposteringen fra kontoen Commerce Discount GL til kontoen discount GL. Du kan finde flere oplysninger under [Detailrabatter](retail-discounts-overview.md).</li></ul> |
| Bogfør rabatinformationskode | Denne indstilling bruges ikke længere i standardløsningen Handel og vil blive frarådet. |
| Bogfør periodisk rabat for ordrer | Denne funktion angiver, om periodiske detailrabatter bogføres i Finans for kundeordrer og callcenterordrer. |

## <a name="inventory-update-parameters"></a>Lageropdateringsparametre

Følgende tabel viser de lageropdateringsparametre, der gælder specifikt for bogføringen af økonomiske og fysiske posteringer.

| Parameter | Beskrivende tekst |
|-----------|-------------|
| Brug standardbatch-id, når der ikke findes batchnumre | Denne funktion kontrollerer, om en standard-id bruges til batch-aktiverede varer, hvis batchnumrene ikke findes, og negativt lager er tilladt. |
| Standard batch-id | Batchnummer, der skal bruges, når der ikke findes batchnumre og **Brug standard-batch-id når batchnumre ikke findes**-parameteren er aktiveret. |

## <a name="aggregation-parameters"></a>Aggregeringsparametre

Følgende tabel viser de aggregeringsparametre, der gælder specifikt for bogføringen af økonomiske og fysiske posteringer.

| Parameter | Beskrivende tekst |
|-----------|-------------|
| Deponering til pengeskab | Aktiver denne parameter for at samle alle posteringer under bogføring af opgørelsen, og opret en enkelt linje i kladden til bogføring i stedet for en separat linje for hver drop. |
| Indsættelse i banken | Aktiver denne parameter for at samle alle posteringer under bogføring af opgørelsen, og opret en enkelt linje i kladden til bogføring i stedet for en separat linje for hver drop. |
| Salgstransaktioner | Aktiver denne parameter for at konsolidere posteringerne som en del af posteringsopgørelsen. Det anbefales, at du aktiverer dette parameter. Det har tidligere fået navnet **Bilagsposteringer**. |
| Returneringer må ikke samles | Hvis denne indstilling er markeret, bogføres hver returtransaktion som en separat salgsordre, når du bogfører en detailopgørelse. |

## <a name="batch-processing-parameters"></a>Behandler batchparametre

Følgende tabel viser de batch-behandlingsparametre, der gælder specifikt for bogføringen af økonomiske og fysiske posteringer.

| Parameter | Beskrivende tekst |
|-----------|-------------|
| Det maksimale antal parallelle opgørelser | Dette felt definerer antallet af batchopgaver, der bruges til at bogføre flere opgørelser. |
| Maksimalt antal tråde til ordrebehandling pr. opgørelse | Maks. antal tråde til ordrebehandling pr. opgørelse – Dette felt repræsenterer det maksimale antal tråde, der bruges af batchjobbet for opgørelsesbogføringen til at oprette og fakturere salgsordrer for en enkelt opgørelse. Det samlede antal tråde, der bruges af bogføringsprocessen for opgørelser, beregnes ved at gange værdien i denne parameter med værdien i parameteren **Det maksimale antal parallelle opgørelsesbogføringer**. Hvis værdien af denne parameter er for høj, kan det have en negativ indvirkning på ydeevnen for opgørelsesprocessen. |
| Maksimale antal transaktionslinjer, der er inkluderet i aggregering | Dette felt definerer antallet af posteringslinjer, som skal medtages i en enkelt aggregeret transaktion, før der oprettes en ny. Aggregerede posteringer oprettes på basis af forskellige aggregeringskriterier, f.eks. debitor, forretningsdato eller økonomiske dimensioner. Det er vigtigt at bemærke, at linjerne fra en enkelt transaktion ikke bliver opdelt på tværs af forskellige aggregerede transaktioner. Det betyder, at der er mulighed for, at antallet af linjer i en aggregeret transaktion er lidt højere eller lavere baseret på faktorer som antallet af specifikke produkter. |
| Maksimale antal tråde til at validere butikstransaktioner | Dette felt definerer det maksimale antal tråde, der kan bruges til validering af butikstransaktioner. Validering af transaktioner er et påkrævet trin, der skal udføres, før transaktionerne kan trækkes ind i opgørelserne. Desuden skal du også definere et gavekortprodukt på oversigtspanelet **Gavekort** under fanen **Bogføring** på siden **Commerce-parametre**, selvom organisationen ikke anvender gavekort. |

Følgende tabel indeholder de anbefalede værdier for parametrene den foregående tabel. Disse værdier skal testes og tilpasses konfigurationen af udrulning og den tilgængelige infrastruktur. Værdier, der overstiger de anbefalede værdier kan påvirke andre batchafviklinger negativt og bør valideres.

| Parameter | Anbefalet værdi | Detaljer |
|-----------|-------------------|---------|
| Det maksimale antal parallelle opgørelsesbogføringer | <p>Angiv denne parameter til det antal batchopgaver, der er tilgængelige for den batchgruppe, der kører jobbet **Opgørelse**.</p><p>**Generel regel:** Multiplicer antallet af virtuelle servere for applikationsobjektservere (AOS) med antallet af batchopgaver, der er tilgængelige pr. virtuel server til AOS.</p> | Denne parameter kan ikke anvendes, når funktionen **Detailopgørelser – Sivende feed** er aktiveret. |
| Maksimalt antal tråde til ordrebehandling pr. opgørelse | Start med at teste værdier ved **4**. Normalt bør værdien ikke overstige **8**. | Denne parameter definerer det antal tråde, der bruges til at oprette og bogføre salgsordrer. Den repræsenterer det antal tråde, der er tilgængelige for bogføring pr. opgørelse. |
| Maksimale antal transaktionslinjer, der er inkluderet i aggregering | Start med at teste værdier ved **1000**. Afhængigt af Commerce Headquarters-konfiguration kan det være mere fordelagtigt med mindre ordrer for ydeevnen. | Denne parameter bestemmer det antal linjer, der medtages i hver salgsordre i forbindelse med bogføring af opgørelsen. Når dette antal er nået, fordeles linjerne til en ny ordre. Selvom antallet af salgslinjer ikke er nøjagtigt det antal, du angiver, da opdelingen finder sted på salgsordreniveau. Antallet vil dog være tæt på det antal, der er angivet. Denne parameter bruges til at generere salgsordrer for detailtransaktioner, der ikke har en navngivet kunde. |
| Maksimale antal tråde til at validere butikstransaktioner | Det anbefales, at du angiver denne parameter til **4**, og at du kun øger den, hvis du ikke opnår acceptabel ydeevne. Det antal tråde, som denne proces bruger, må ikke overstige det antal processorer, der er tilgængelige for batchserveren. Hvis antallet af tråde er for højt, kan det påvirke en anden batchafvikling. | Denne parameter styrer antallet af transaktioner, der kan valideres på samme tid for en given butik. |

> [!NOTE]
> Alle indstillinger og parametre, der er relateret til bogføring af opgørelsen, og som er defineret i butikker og på siden **Commerce-parametre**, gælder for funktionen til forbedret bogføring af opgørelser.

## <a name="invoice-parameters"></a>Fakturaparametre

Følgende tabel viser de fakturaparametre, der gælder specifikt for bogføringen af økonomiske og fysiske posteringer.

| Parameter | Beskrivende tekst |
|-----------|-------------|
| Kladdenavn | Navnet på den betalingskladde, der bruges, når der oprettes debitorbetalingskladder for salgsordrebetalinger. Denne indstilling gælder for alle ordrebetalinger, der er bogført for POS, callcenter- og e-commerce-kanalordrer. |
| Kontonavn | Navnet på betalingskontoen. |
| Prioriter dimensioner fra betalingsmetode | Hvis flaget er aktiveret, har betalingskladden dimensioner, der prioriteres fra betalingsmetoden i stedet for butikken. |
| Funktionalitet for momsberegning | Denne parameter angiver funktionaliteten, når salgsordrer, der oprettes under bogføring af opgørelsen, faktureres:<ul><li>**Genberegn** – Beregn moms igen.</li><li> **Genberegn ikke** – Brug de momsbeløb, der er beregnet i POS.</li></ul> |
| Kladdenavn | Det kladdenavn, der bruges, når der oprettes en debitorbetalingskladde til refundering. Denne indstilling gælder for alle ordrebetalinger, der er bogført for POS, callcenter- og e-commerce-kanalordrer. |

## <a name="statement-parameters"></a>Opgørelsesparametre

Følgende tabel viser de opgørelsesparametre, der gælder specifikt for bogføringen af økonomiske og fysiske posteringer.

| Parameter | Beskrivende tekst |
|-----------|-------------|
| Reservér lager under beregning | Når denne parameter er aktiveret, reserverer opgørelsesberegningen midlertidigt lager, indtil opgørelsen er bogført. Denne parameter er som standard deaktiveret for at forbedre beregningen af opgørelser. Opdaterede lageroplysninger kan beregnes ved hjælp af lagerbatchjobbet **Bogfør**. Bemærk, at lagerbatchjobbet **Bogfør** ikke længere bruges, når [sivende feedbaseret](trickle-feed.md) ordreoprettelse for detailbutikstransaktioner er aktiveret. |
| Deaktivering af optælling er påkrævet | Dette flag deaktiverer optællingen under bogføring i Commerce Headquarters. |
| Genberegn økonomisk dimensioner ved fejl | Hvis denne parameter er aktiveret, genevalueres de økonomiske dimensioner på efterfølgende opgørelsesposteringer, når bogføring af opgørelsen mislykkes |
| Brug økonomiske dimensioner fra returneringsbutikken | Når denne parameter er aktiveret, kan der oprettes sammenkædede retursalgsordrer, der bruger butikkens økonomiske dimensioner i stedet for de økonomiske dimensioner fra den oprindelige transaktion. |
| Fjern sammenkædning af returneringer | Når denne parameter er aktiveret, kan opgørelsen oprette returneringer fra ikke-bogførte salg som skjulte returneringer. Denne parameter er som standard deaktiveret, og det anbefales, at du deaktiverer den. |
| Deaktiver bogføring af afrundingsdifference | Denne parameter deaktivere bogføring af afrundingsdifference mellem transaktionsbetaling og bruttobeløb under behandling af betalinger. |
| Udlign kundeindbetalinger automatisk | Når parameteren er aktiveret, skal debitorindbetalinger, der er bogført under behandling af detailopgørelse, udlignes mod åbne debitortransaktioner. |
| Aktivér og brug afstemning af kassestyring fra POS | Når denne parameter er aktiveret, udføres kontantstyringsafstemningen i POS, og værdierne overføres til bogføring af detailregnskaber for at oprette opgørelseslinjer. |
| Detaljeringsniveau for finansbilag | Denne parameter definerer detaljeringsniveauet i finansbilaget for udvalgte transaktioner, der stammer fra POS. Posteringstyper inkluderer indtægter, udgifter og rabatter. I forbindelse med rabatter tages der kun højde for denne parameter, når kontonummeret for en periodisk rabat og kontonummeret for en almindelig rabat ikke er det samme. Medmindre der kræves detaljer, er **Oversigt** den anbefalede værdi for disse posteringer. Når der er defineret bogføring på samleniveau, udfyldes **TransactionDiscountTrans.RecID** ikke. I versionen af Commerce 10.0.27 blev dette flag omdøbt og flyttet. Det har tidligere fået navnet **Detaljeniveau** og var i afsnittet **Lageropdatering**. |
