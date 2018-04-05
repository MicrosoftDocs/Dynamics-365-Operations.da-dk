---
title: "Økonomiske dimensioner og bogføring"
description: "Når du planlægger at oprette din kontoplan, skal du overveje, hvordan de forskellige komponenter kan arbejde sammen, når du bogfører et dokument eller kladde. Disse komponenter omfatter kontostrukturer, avancerede regler og udligningsdimensioner og faste dimensioner. Dette emne forklarer, hvad hver enkelt komponent er, og hvordan komponenterne arbejder sammen."
author: aprilolson
manager: AnnBe
ms.date: 08/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerChartofAccounts,DimensionDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: a0530a569978bafffcdcc63c8d502b9bfa645bc5
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---

# <a name="financial-dimensions-and-posting"></a>Økonomiske dimensioner og bogføring 

[!include[banner](../includes/banner.md)]

Når du planlægger at oprette din kontoplan, skal du overveje, hvordan de forskellige komponenter kan arbejde sammen, når du bogfører et dokument eller kladde. Disse komponenter omfatter kontostrukturer, avancerede regler og udligningsdimensioner og faste dimensioner. Dette emne forklarer, hvad hver enkelt komponent er, og hvordan komponenterne arbejder sammen.

## <a name="chart-of-accounts-and-financial-dimension-components"></a>Komponenter i kontoplan og økonomisk dimension

Microsoft Dynamics 365 for Finance and Operations har et omfattende, regelbaseret system til at definere gyldige kombinationer af værdier for hovedkonti og økonomiske dimensioner. Dette afsnit giver en kort oversigt over funktionaliteten af hver komponent og forklarer, hvor du kan finde komponenten.

### <a name="account-structures"></a>Kontostrukturer

Der kræves en kontostruktur, når du konfigurerer Finans. Du skal definere og aktivere mindst én kontostruktur, og du skal tildele den til Finans. Kontostrukturen skal omfatte hovedkontoen. Du kan definere rækkefølgen af de segmenter, der passer bedst til virksomheden. Når hovedkontoen er defineret, kan systemet bestemme, hvilken kontostruktur der bruges. Når du placerer hovedkontoen først eller tæt på forsiden af en struktur, kan du begrænse værdierne og også hjælpe systemet med at anvende de sidste kendte gyldige værdier som standardværdi. Du kan have op til 10 yderligere økonomiske dimensioner i kontostrukturen. Kontostrukturen definerer, hvilke dimensionsværdier der er gyldige sammen med andre værdier. Den definerer også, om der skal angives dimensionsværdier.

### <a name="advanced-rules"></a>Avancerede regler

Avancerede regler er en valgfri komponent, når du konfigurerer kontoplanen. Du kan tilføje så mange avancerede regler, som du vil, i en kontostruktur. Avancerede regler bruges ofte til at håndtere situationer, hvor yderligere økonomiske dimensioner skal spores, når bestemte kriterier er opfyldt. Hvis du f.eks. bruger en rejseudgiftskonto, kan du spore yderligere oplysninger, f.eks. den hændelse, medarbejderen er på vej til. Hvis der er flere avancerede regler, anvendes de i alfabetisk rækkefølge baseret på navnene på reglerne. De segmenter, som en regel tilføjer, kan først anvendes efter segmenterne i kontostrukturen.

### <a name="balancing-dimension"></a>Udligningsdimension

Du kan vælge at angive en økonomisk udligningsdimension. På siden **Finans** kan du definere den økonomiske dimension, der skal udlignes. Hver gang der bogføres posteringer til den pågældende økonomiske dimension, opretter og bogfører systemet derefter automatisk poster for at udligne den økonomiske dimension.

### <a name="defaultfixed-financial-dimensions-on-the-main-account"></a>Standard/faste økonomiske dimensioner på hovedkontoen.

Standarddimensioner kommer fra forskellige steder som f.eks. masterposter (f.eks. debitor- eller kreditorposter), dokumenthoveder og hovedkontoen. I dette emne beskrives standarddimensioner på hovedkontoen efter juridisk enhed. Du kan angive, om en hovedkonto har en **Ikke fast** eller **Fast** værdi for hver økonomisk dimension, der bruges i alle kontostrukturer til Finans. Hvis en økonomisk dimension er **Ikke fast**, bruger den en standardværdi, men denne værdi kan overskrives. Denne funktionsmåde gælder for alle standardværdier i systemet, selv standardværdier, der stammer fra masterposter. Hvis en økonomisk dimension, der er indstillet til en **Fast** værdi, anvendes denne værdi altid, uanset om den stammer fra et sted som standardværdi, eller brugeren har angivet den.

## <a name="order-in-which-default-dimensions-are-applied-during-posting"></a>Rækkefølge, som standarddimensioner anvendes i under bogføring

Brugere har ofte spørgsmål om den rækkefølge, de forskellige komponenter køres i. Det er meget vigtigt, at du forstår den rækkefølge, som standarddimensioner anvendes i, da denne funktionsmåde påvirker den tilgang, du vælger i forhold til konfigurationen.

> [!NOTE]
> Disse oplysninger gælder kun for anvendelsen af standarddimensioner i programmet. Hvis du importerer data ved hjælp af Microsoft Excel eller Data Management Framework, afviger funktionsmåden.

### <a name="example-1"></a>Eksempel 1

**Kontostruktur**

| Hovedkonto            | Virksomhedsenhed           | Afdeling              | Bærer             |
|-------------------------|-------------------------|-------------------------|-------------------------|
| Alle værdier er tilladt. | Alle værdier er tilladt. | Alle værdier er tilladt. | Alle værdier er tilladt. |

**Hovedkonto**

| Hovedkonto | Navn          | Juridisk enhed | Afdeling                                 |
|--------------|---------------|--------------|--------------------------------------------|
| 401100       | Produktsalg | USMF         | Fast – 022 Salgs- og marketingafdeling |

I følgende illustration vises den faste standarddimension, der er angivet for hovedkontoen 401100.

[![Økonomiske standarddimensioner](./media/default-dimensions.png)](./media/default-dimensions.png)

I dette meget grundlæggende eksempel vil vi angive en finanskladde, hvor afdelingsdimensionen er indstillet til at bruge standardværdien **023** (Operations). Vi vil angive og bogføre en finanskonto. I følgende illustration vises den økonomiske standarddimension i finansbogholderihovedet.

[![Finanskladder](./media/general-journal.png)](./media/general-journal.png)

Standarddimensionen i kladdehovedet medfører, at afdeling 023 skal anvendes som standard i salgskontolinjen. I følgende illustration vises den finanskladdelinje, hvor standarddimensionsværdien **023** fra hovedet anvendes.

[![Kladdebilag](./media/journal-voucher.png)](./media/journal-voucher.png)

Når linjen bogføres, anvendes den faste dimension dog, og linjen bogføres til afdeling 022. I følgende illustration vises det bogførte bilag, hvor den faste dimension anvendes for salgskontoen.

[![Poster på bilag](./media/voucher-transactions.png)](./media/voucher-transactions.png)

### <a name="example-2"></a>Eksempel 2

I dette eksempel bruges samme opsætning som i det første eksempel. Vi vil dog tilføje endnu en komponent og bruge afdelingsdimensionen som en udligningsdimension. I følgende illustration er **Afdeling** angivet som den økonomiske udligningsdimension for USMF-finans.

[![Finans](./media/ledger.png)](./media/ledger.png)

Når der bruges samme kladdehovedopsætning, og den samme postering bogføres, anvendes den faste dimension først. Derefter anvendes udligningslogikken for at hjælpe med at sikre, at hver afdeling har en udlignet post. I følgende illustration vises bilagsposteringer, der omfatter modposten, når den faste dimension anvendes.

[![Poster på bilag](./media/voucher-transactions2.png)](./media/voucher-transactions2.png)

### <a name="example-3"></a>Eksempel 3

I dette eksempel vil vi tilføje en avanceret regel. Den avancerede regel angiver, at hvis salgskontoen 401100 og afdeling 022 (Salg og marketing) anvendes, skal systemet spore et ekstra segment, Debitor.

Dette eksempel er vigtigt på grund af rækkefølgen. Kontostrukturen bestemmes, når hovedkontoen er angivet. Hvis du refererer til kontostrukturopsætningen, kan systemet bestemme, at hovedkontoen, afdelingen og bæreren er relevante. På dette tidspunkt er den avancerede regel ikke blevet udløst, fordi faste dimensioner ikke anvendes, før der er anvendt standarddimensioner for kladdebilaget under bogføringen. I følgende illustration er debitorsegmentet ikke angivet, fordi kriterierne for den avancerede regel ikke er opfyldt.

[![Finanskonto](./media/drop-down.png)](./media/drop-down.png)

Bogføringen kan ikke udføres, fordi den faste dimension blev anvendt sidst i processen. Validering af dimension bestemmer, at debitorsegmentet kræves, hvis hovedkontoen er 401100 og afdelingen er 022. Bogføring kan ikke udføres på grund af valideringsfejlen. I følgende illustration kan du se den meddelelse, der vises, når dimensionsvalideringen bestemmer, at debitoren er et påkrævet segment.

[![Meddelelsesdetaljer](./media/message.png)](./media/message.png)

I dette eksempel skal du overskrive standardværdien, så den avancerede regel udløses, og du kan angive debitorsegmentet. Men denne løsning er ikke altid mulig, og nogle brugere er desuden ikke opmærksomme på reglerne for bogføring. Det er derfor vigtigt, at du forstår den rækkefølge standarddimensioner anvendes i, når du konfigurerer din kontoplan.

For at opnå det ønskede resultat i dette eksempel kan du ændre konfigurationen på flere måder. Du kan f.eks. oprette en ny kontostruktur til salgskonti og lade debitorsegmentet indgå i strukturen. Du kan også tilføje flere rækker i en eksisterende kontostruktur og angive hovedkontoen og gyldige afdelingsværdier. Og derefter, i den yderligere debitorstruktur, kan det være nyttigt at have en separat kontostruktur for salgskonti, hvor debitorsegmentet indgår.

## <a name="additional-resources"></a>Yderligere ressourcer 

Nogle af følgende ressourcer refererer til en tidligere version af Finance and Operations. Men mange af oplysningerne om anvendelsen af standarddimensioner og mange af begreberne er de samme i den tidligere version, og referencerne er stadig gyldige.

[Afstemte kladder for regnskab mellem enheder](example-balanced-journals-interunit-accounting.md)

[Planlægge din kontoplan](plan-chart-of-accounts.md) 

[Planlægning af kontoplanen i AX 2012 blog](https://blogs.msdn.microsoft.com/axsa/2014/06/12/planning-your-chart-of-accounts-in-ax-2012-part-1-of-7/) – Dette link fører til del 1 i en serie på syv dele.

[Dimension, der benyttes som standard i regnskabsfordelinger](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2013/12/16/dimension-defaulting-in-accounting-distributions-part-1-introduction/)

[Dimension, der benyttes som standard i dimensionsstruktur](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2014/09/)

