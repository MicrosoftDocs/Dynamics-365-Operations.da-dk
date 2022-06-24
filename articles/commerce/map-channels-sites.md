---
title: Knytte kanaler til e-handelswebsteder
description: Denne artikel beskriver nogle af de mest almindelige kanaltilknytningsscenarier i Microsoft Dynamics 365 Commerce, hvor de fleste andre forretningsbehov kan ekstrapoleres.
author: samjarawan
ms.date: 05/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 94c43df26e8d6e55a5b6d459b65066d5873e1063
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902757"
---
# <a name="map-channels-to-e-commerce-sites"></a>Knytte kanaler til e-handelswebsteder

Denne artikel beskriver nogle af de mest almindelige kanaltilknytningsscenarier i Microsoft Dynamics 365 Commerce, hvor de fleste andre forretningsbehov kan ekstrapoleres.

Dynamics 365 Commerce understøtter mange forretningsscenarier for tilknytning af [onlinekanaler](#channels), der har et konfigureret sæt produkter, priser og rabatter, til kunders erfaringer med [e-handelswebsteder](#e-commerce-sites).

Denne artikel omhandler følgende scenarier:

- **En kanal med ét sprog, der har en enkelt e-handelswebstedsoplevelse.** Dette scenario kan f.eks. omfatte en enkelt mærkevarewebsted, der er konfigureret til det amerikanske marked.
- **En kanal med flere sprog, der har en enkelt lokaliseret webstedsoplevelse.** Dette scenario kan f.eks. omfatte en enkelt mærkevarewebsted, der er konfigureret til Canada med fransk og engelsk sprogunderstøttelse. I dette scenario har brugere, der vælger forskellige sprog, samme webstedsoplevelse, men som er oversat til hver brugers valgte sprog.
- **En kanal med flere sprog, der har en separat webstedsoplevelse pr. sprog.** Dette scenario kan f.eks. omfatte en enkelt mærkevarewebsted, der er konfigureret til Canada med fransk og engelsk sprogunderstøttelse. I dette scenario er der en entydig webstedserfaring for hvert sprog.
- **Flere kanaler (enkelt sprog og/eller flere sprog), der har en enkelt lokaliseret webstedsoplevelse.** Dette scenario kan f.eks. omfatte en enkelt mærkevarewebsted, der er konfigureret til Australien og New Zealand. I dette scenario har begge lande samme webstedserfaring på engelsk, men hvert land er konfigureret med forskellige produkter, valuta, priser, rabatter og forsendelsesmåder.
- **Flere kanaler (enkelt sprog og/eller flere sprog), der har separat webstedsoplevelse pr. kanal.** Dette scenario kan f.eks. omfatte en enkelt mærkevarewebsted, der er konfigureret til Australien, Canada og Tyskland på flere sprog. I dette scenario har hvert land en separat webstedserfaring, der er konfigureret med forskellige produkter, valuta, priser, rabatter og forsendelsesmåder.

## <a name="channels"></a>Kanaler

En kanal (også kendt som en onlinebutik eller onlinekanal) repræsenterer en online-e-handelsbutiksfacade, der bruges til at tilknytte produkter, priser, rabatter, sprog, betalingsmåder, leveringsmåder, opfyldelsescentre og andre aspekter af den onlineoplevelse, der vil være tilgængelig for dine e-handelskunder. Kanaler oprettes og administreres i Commerce headquarters og knyttes til en enkelt [juridisk enhed](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json#legal-entities). Den juridiske enhed er normalt baseret på et enkelt land/område, der kræver momsrapportering for kanalen, og den kan kun konfigureres med en enkelt valuta.

Du kan finde flere oplysninger om kanaler i [Oversigt over kanaler](channels-overview.md). Du kan finde flere oplysninger om, hvordan du opretter en onlinekanal, i [Konfigurere en onlinekanal](channel-setup-online.md).

I følgende eksempelillustration fra Commerce headquarters vises de standardonlinekanaler, der implementeres med Dynamics 365 Commerce, hvis indstillingen for demodata er valgt.

![Standarddemodatakanaler i Commerce headquarters.](media/channel-mapping-1.png)

## <a name="e-commerce-sites"></a>E-handelswebsteder

Et e-handelswebsted indeholder et sæt websider, som kunderne bruger til at søge og købe. E-handelswebsteder administreres i Commerce-webstedsgenerator.

Du kan finde flere oplysninger om, hvordan du opretter og administrerer websteder i webstedsgeneratoren, i [Oversigt over e-handelswebsteder](online-store-overview.md).

## <a name="common-channel-mapping-scenarios"></a>Almindelige kanaltilknytningsscenarier

Dynamics 365 Commerce understøtter en lang række kanaltilknytningsscenarier. Følgende scenarier for kanaltilknytning er blot et undersæt af alle mulige kanaltilknytningsscenarier. De er udarbejdet som en vejledning, der kan hjælpe dig med at planlægge eventuelle unikke forretningsscenarier, du har. Den fiktive Adventure Works-sportsbutik, der er inkluderet i Dynamics 365 Commerce-demodataene, bruges som eksempel for hvert scenario.

### <a name="single-language-channel-that-has-a-single-e-commerce-site-experience"></a>Kanal med ét sprog, der har en enkelt e-handelswebstedsoplevelse

I det mest grundlæggende scenario har en enkelt kanal ét sprog til salg på et enkelt marked. Dette scenario er f.eks. en onlinebutikken Adventure Works, der kun er konfigureret til det amerikanske marked.

I følgende illustration vises et eksempel på en kanalkonfiguration i Commerce headquarters. I denne konfiguration understøtter onlinekanalen kun et enkelt sprog (**en-us**), en enkelt valuta (**USD**) og en enkelt forretningsenhed (**usrt**), der bruges til momsrapportering.

![Værdier for juridisk enhed, valuta og sprog til Adventure Works-onlinebutikken fremhævet i Commerce headquarters.](media/channel-mapping-3.png)

Den ene onlinekanal kan knyttes til et enkelt e-handelswebsted i webstedsgenerator. Du kan finde oplysninger om, hvordan du opretter et nyt websted og knytter det til en kanal, under [Knytte en kanal til et websted i webstedsgeneratoren](#map-a-channel-to-a-site-in-site-builder) i denne artikel.

### <a name="multi-language-channel-that-has-a-single-localized-site-experience"></a>Kanal med flere sprog, der har en enkelt lokaliseret webstedsoplevelse

I dette scenario understøtter en enkelt kanal mere end ét sprog. Produktnavne, beskrivelser og attributter kan derfor lokaliseres i Commerce headquarters. For at give en komplet lokaliseret webstedsoplevelse kan marketingindhold på webstedet også lokaliseres i Commerce-webstedsgeneratoren.

Begrænsningen i dette scenario er, at en enkelt kanal kun kan konfigureres med én valuta, én juridisk enhed og ét sæt produkter og priser. Denne konfiguration fungerer bedst for lande/områder, der har en enkelt valuta og flere sprog (f.eks. Canada, som har engelsk og fransk som sprog), en enkelt juridisk enhed og et enkelt sæt produkter og priser.

Hvert sprog i en kanal kan konfigureres med sit eget domænenavn. Domænet `www.adventure-works.ca` kan f.eks. konfigureres til den engelske version i Canada, og `www.adventure-works-fr.ca`-domænet kan konfigureres til den franske version i Canada. Alternativt kan forskellige sprog i en kanal konfigureres i et enkelt domæne, og derefter kan der bruges en separat sti til hvert sprog. Domænet `www.adventure-works.ca` kan f.eks. konfigureres til den engelske version i Canada, og derefter kan stien til `www.adventure-works.ca/fr` bruges til den franske version i Canada. [Geografisk registrering](geo-detection-redirection.md) kan også aktiveres, så en bruger automatisk bliver omdirigeret til det rette websted baseret på brugerens opholdssted.

Du kan finde flere oplysninger om, hvordan kunder kan skifte mellem sprog manuelt, i afsnittet [Tilføje og konfigurere webstedsvælgermodulet](#add-and-configure-the-site-picker-module) i denne artikel. Du kan finde oplysninger om tilpasning af lokalisere sider og fragmenter i afsnittet [Administrere webstedsindhold , der har flere kanaler og sprog](#manage-site-content-that-has-multiple-channels-and-languages).

### <a name="multi-language-channel-that-has-a-different-site-experience-per-language"></a>Kanal med flere sprog, der har en separat webstedsoplevelse pr. sprog

Du vil muligvis foretrække et scenario, hvor en enkelt kanal understøtter mere end ét sprog, men hvor der gengives en helt anden webstedsoplevelse for hvert sprog. Den anbefalede metode til implementering af dette scenario er at bruge [sidevarianter](#implement-page-variants-for-each-language) på ét enkelt websted.

En anden metode er at oprette et nyt e-handelswebsted for hvert sprog i webstedsgeneratoren og derefter knytte hvert enkelt websted til en enkelt onlinekanal og sprog. Resultatet bliver en enkelt onlinekanal, der er knyttet til flere e-handelswebsteder, én for hvert sprog. Denne metode for flere websteder kræver ekstra administrationsressourcer, da der vil være mere end ét websted, der skal administreres i webstedsgeneratoren.

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-single-localized-site-experience"></a>Flere kanaler (enkelt sprog og/eller flere sprog), der har en enkelt lokaliseret webstedsoplevelse

Et brandet websted kan kræve flere onlinekanaler pr. websted for at understøtte en anden valuta, andre produkter og andre priser for hver kanal på et enkelt websted. Webstedet Adventure Works kan f.eks. have en onlinekanal til det canadiske marked, der har flere sprog, en kanal til det amerikanske marked, der har ét sprog, og en kanal til det tyske marked, der har ét sprog. I dette scenario konfigureres hver enkelt onlinekanal for en områdespecifik juridisk enhed, og den kan have samme sæt produkter, som andre kanaler har, et undersæt af disse produkter eller et andet sæt produkter. Hver kanal har også egne priser i den lokale valuta, moms, rabatter og forsendelsesmåder.

I dette scenarie kan hvert sprog konfigureres med egne domænenavne. Domænet `www.adventure-works.com` kan f.eks. konfigureres til det amerikanske marked, og `www.adventure-works.de`-domænet kan konfigureres til det tyske marked. Alternativt kan hvert enkelt marked konfigureres til at bruge en separat sti. Domænet `www.adventure-works.com` kan f.eks. konfigureres til det amerikanske marked, og stien `www.adventure-works.com/de` kan bruges til det tyske marked. [Geografisk registrering](geo-detection-redirection.md) kan også aktiveres, så brugerne automatisk bliver omdirigeret til det rette websted baseret på deres geografiske område.

Du vil måske også have, at dit websted indeholder en rulleliste, der giver brugerne mulighed for manuelt at skifte til et bestemt marked. Du kan finde flere oplysninger i afsnittet [Tilføje og konfigurere webstedsvælgermodulet](#add-and-configure-the-site-picker-module) i denne artikel.

Oplysninger om, hvordan du konfigurerer flere kanaler på et enkelt websted, finder du i afsnittet [Konfigurere flere kanaler på et e-handelswebsted](#configure-multiple-channels-on-an-e-commerce-site).

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-different-site-experience-per-channel"></a>Flere kanaler (enkelt sprog og/eller flere sprog), der har separat webstedsoplevelse pr. kanal

Du vil måske have flere kanaler til et enkelt brand i forskellige geografiske områder, og du vil have, at hvert websted skal have egen webstedsoplevelse. Der findes to metoder til implementering af dette scenario:

- Brug [sidevarianter](#implement-page-variants-for-each-language).
- Konfigurer et separat websted til hver onlinekanal i webstedsgeneratoren, og knyt derefter hvert websted til separat onlinekanal og sprog. Denne metode kræver ekstra administrationsressourcer, da der vil være mere end ét websted, der skal administreres i webstedsgeneratoren.

## <a name="cross-channel-sharing"></a>Dele kanal tværs af kanaler

Deling på tværs af kanaler er nyttig, når flere kanaler på et enkelt websted kan dele indhold. En forhandler, der har flere mærker og udstillingsvinduer, der er grupperet under et enkelt websted, kan f.eks. dele noget indhold på nogle eller alle udstillingsvinduer. Delte indhold kan være sider til vilkår og betingelser, betalingsbetingelser, leveringsmetoder og ofte stillede spørgsmål. Du kan finde flere oplysninger under [Aktivere og bruge deling på tværs af kanaler](cross-channel-sharing.md).

## <a name="map-a-channel-to-a-site-in-site-builder"></a>Knytte en kanal til et websted i webstedsgenerator

Der findes flere metoder til oprettelse og konfiguration af websteder til brug af forskellige onlinekanaler.

### <a name="create-a-new-site"></a>Oprette et nyt websted

Du kan oprette et helt nyt websted i webstedsgeneratoren ved at gå til listesiden **Websteder** og vælge **Nyt websted**. I dialogboksen **Nyt websted**, der vises, kan du derefter vælge standardonlinekanalen og -sproget for webstedet som vist i følgende illustration nedenfor.

![Opret en ny kanal i webstedsgeneratoren.](media/channel-mapping-4.png)

Det websted, du opretter på denne måde, er tomt og inkluderer ikke nogen webstedssider (f.eks. en startside, kategorisider og produktsider).

Du kan finde flere oplysninger under [Oprette et websted for e-handel](create-ecommerce-site.md).

### <a name="create-a-new-site-by-using-the-site-copy-operation"></a>Oprette et nyt websted ved hjælp af kopieringshandlingen for websted

I stedet for at oprette et helt nyt, tomt websted, som det er beskrevet i forrige afsnit, er det bedre praksis at starte med en kopi af et af de startwebsteder, der findes i Commerce-modelbiblioteket, f.eks. Fabrikam- eller Adventure Works-webstedet.

Hvis du vil kopiere et eksisterende websted, skal du gå til listesiden **Websteder** i webstedsgeneratoren og vælge **Kopiér websted**. I dialogboksen **Kopiér websted**, der vises, kan du derefter vælge kildewebstedet og angive navnet på destinationswebstedet.

På dette tidspunkt kan du endnu ikke vælge standardonlinekanalen og -sproget for webstedet. Du kan dog konfigurere disse egenskaber, når kopieringshandlingen for webstedet er fuldført. Første gang du vælger webstedet på listesiden **Websteder** i webstedsgeneratoren, vises dialogboksen **Konfigurer dit websted**, hvor du kan vælge standardkanalen og -sproget.

Du kan finde oplysninger om, hvordan du kopierer et websted, under [Kopiere et websted for e-handel](copy-ecommerce-site.md).

### <a name="manage-an-existing-site-channel"></a>Administrere en eksisterende webstedskanal

Når et websted er konfigureret med en kanal, kan du administrere og opdatere kanalen fra det valgte websted i webstedsgeneratoren i **Indstillinger for websted \> Kanaler** som vist i følgende illustration.

![Administrere kanaltilknytningen i webstedsgenerator.](media/channel-mapping-7.png)

## <a name="support-multiple-sites-in-a-single-tenant"></a>Understøtte flere websteder i en enkelt lejer

Mange brandede websteder kan sameksistere i en enkelt lejer. I følgende eksempelsillustration vises tre forskellige brandede websteder (Adventure Works, Adventure Works Business og Fabrikam), som hver især er tilknyttet en enkelt separat onlinekanal.

![Liste over websteder i webstedsgenerator.](media/channel-mapping-8.png)

## <a name="configure-a-single-domain-name-with-paths-for-multiple-sites"></a>Konfigurere et enkelt domænenavn med stier til flere websteder

Et enkelt domænenavn kan bruges til flere websteder, og stier kan derefter bruges til at adskille websteder eller sprog. Domænet `www.mycompany.com` er f.eks. konfigureret til to forskellige e-handelswebsteder: det ene til Fabrikam og det andet til Adventure Works. I dette tilfælde kan standardstien (`www.mycompany.com`), som også kaldes den tomme sti, bruges til Fabrikam-webstedet, og en anden sti (f.eks. `www.mycompany.com/adventureworks`) kan bruges til webstedet Adventure Works. En anden mulighed er at bruge en tilpasset sti (f.eks. `www.mycompany.com/fabrikam`) i stedet for standardstien til Fabrikam-webstedet.

Alternativt kan der bruges et andet domænenavn til hvert enkelt websted (f.eks. `www.adventure-works.com` og `www.fabrikam.com`). Stier kan derefter bruges til forskellige sprog eller geografiske områder (f.eks. `www.adventure-works.com/fr-ca` for fransk Canada).

## <a name="configure-multiple-languages-on-a-site"></a>Konfigurere flere sprog på et websted

Sprog kan konfigureres til e-handelswebstedet i webstedsgeneratoren på **Indstillinger for websted \> Kanaler**. I illustrationen i følgende eksempel er hvert sprog konfigureret ved hjælp af landestandarden for stien, så hvert sprog har en entydig URL-adresse.

![Flere konfigurerede sprog på et websted.](media/channel-mapping-10.png)

Hvis du vil tilføje et nyt kanalsprog, skal du gå til **Indstillinger for websted \> Kanaler** og vælge kanallinket. I den rude, der vises til højre, skal du vælge **Tilføj en landestandard** for at vælge den kanal og landestandard, du vil tilføje. Angiv derefter stien, der skal bruges til den valgte kanal.

### <a name="add-and-configure-the-site-picker-module"></a>Tilføje og konfigurere webstedsvælgermodulet

Når du har konfigureret et websted med flere sprog og eller kanaler, kan du føje en sprogvælger til sidehovedet på webstedet, så brugerne manuelt kan vælge deres sprog eller land/område. Modulbibliotekets [hovedmodul](author-header-module.md) har indbygget understøttelse af, at brugerne kan vælge et sprog ved hjælp af [webstedsvælgermodulet](site-selector.md). Webstedsvælgermodulet kan føjes til hovedmodulet i sidehovedfragmentet.

Du kan finde flere oplysninger om at tilføje og konfigurere webstedsvælgermodulet i [Webstedsvælgermodul](site-selector.md).

### <a name="implement-page-variants-for-each-language"></a>Implementere sidevarianter for hvert sprog

I dette scenario er der kun én kanal, men der er flere sprog. Du kan ændre en sides udseende på baggrund af det valgte sprog ved at oprette en sidevariant for den. Derefter kan du føje lokaliseret indhold til varianten.

Når der er en side åben i webstedsgeneratoren, og du vælger linket øverst til højre, som viser den aktuelle kanal og det aktuelle sprog, vises der en kanal- og sprogvælger som vist i følgende eksempelillustration. Hvis du vil tilsidesætte siden for det aktuelle sprog, skal du vælge en anden landestandard og derefter vælge **Rediger**. Du kan også ændre kanalen, hvis du [administrerer et websted, der har flere kanaler og sprog](#manage-site-content-that has-multiple-channels-and-languages).

![Ændring af sproget for en side i webstedsgeneratoren.](media/channel-mapping-14.png)

Hvis varianten for den valgte side eller det valgte element endnu ikke er oprettet, får du vist en advarselsmeddelelse som i følgende eksempelillustration. I dette tilfælde skal du vælge linket **Opret sidevariant** i meddelelsesteksten. Den dialogboks, der vises, indeholder indstillinger, som giver dig mulighed for enten at starte med en kopi af en eksisterende variant eller oprette en helt ny side ud fra en skabelon.

![Prompt til at oprette en sidevariant i webstedsgeneratoren](media/channel-mapping-16.png)

Hvis du ikke opretter en variant, gengives den oprindelige side, som viser det relevante sprog for modulstrenge og produktoplysninger fra Commerce headquarters. Men hvis tekst, f.eks. en sidetitel eller andet marketingindhold, er angivet direkte i standardsidemodulerne, forbliver strengene for den pågældende tekst på det oprindelige sprog.

I stedet for at oprette hver side og hvert fragment manuelt kan du eksportere hver side og fragmentet til en XLIFF-fil (XML Localization Interchange File Format), der derefter kan sendes til lokalisering. Når hver XLIFF er blevet lokaliseret, kan den importeres som en lokaliseret sidevariant. Hvis du vil eksportere en XLIFF-fil fra en side eller et fragment i webstedsgeneratoren eller importere en XLIFF-fil til en side eller et fragment, skal du vælge **Lokalisering** på kommandolinjen. Vælg derefter enten **Eksportér XLIFF** eller **Importér XLIFF** som vist i følgende eksempelillustration.

![Import eller eksport af en side eller et fragment i XLIFF-format.](media/channel-mapping-18.png)

## <a name="manage-site-content-that-has-multiple-channels-and-languages"></a>Administrere webstedsindhold, der har flere kanaler og sprog

Et websted, der har flere kanaler og/eller sprog, gemmer en entydig variant af hver side og et fragment for hver kombination af en kanal og et sprog. Denne funktionalitet gør det muligt for at sidevarianter at indeholde lokaliserede data, men giver dig også fleksibilitet til at ændre udseende og funktionsmåde for en side til en bestemt variant.

Du kan finde oplysninger om, hvordan du kan arbejde med sidevarianter, under [Implementere sidevarianter for hvert sprog](#implement-page-variants-for-each-language) i denne artikel.

## <a name="configure-multiple-channels-on-an-e-commerce-site"></a>Konfigurere flere kanaler på et e-handelswebsted

Du kan føje kanaler til et e-handelswebsted i webstedsgeneratoren ved at gå til **Indstillinger for websted \> Kanaler** og vælge **Tilføj en kanal**. Du kan derefter vælge onlinekanalen og landestandarden i den viste dialogboks **Tilføj en kanal**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over kanaler](channels-overview.md)

[Konfigurere en onlinekanal](channel-setup-online.md)

[Oversigt over organisationer og organisationshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md)

[Konfigurere registrering og omdirigeret registrering](geo-detection-redirection.md)

[Aktivere og bruge deling på tværs af kanaler](cross-channel-sharing.md)

[Oprette et e-handelswebsted](create-ecommerce-site.md)

[Kopiere et e-handelswebsted](copy-ecommerce-site.md)

[Webstedsvælgermodul](site-selector.md)
