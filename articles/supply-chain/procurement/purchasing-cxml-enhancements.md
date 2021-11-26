---
title: Forbedringer af indkøbs-cXML
description: Funktionen Forbedringer af indkøbs-cXML bygger på den eksisterende eksterne katalogfunktionalitet, PunchOut, der bruges til indkøbsrekvisitioner.
author: Henrikan
ms.date: 08/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatCXMLParameters, CatCXMLPurchRequest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-08-03
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 210d92b9fd962708b141b79f3634f142cca9787a
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777761"
---
# <a name="purchasing-cxml-enhancements"></a>Forbedringer af indkøbs-cXML

[!include [banner](../includes/banner.md)]

Funktionen _Forbedringer af indkøbs-cXML_ bygger på den [eksisterende eksterne katalogfunktionalitet](set-up-external-catalog-for-punchout.md), der bruges til indkøbsrekvisitioner. Denne eksisterende funktionalitet kaldes _PunchOut_. Selvom en indkøbsordre ikke behøver at stamme fra en indkøbsrekvisition, skal der være en forbindelse mellem kreditoren på en indkøbsordre og de parametre, der bruges til at sende indkøbsordredokumentet.

## <a name="turn-on-the-purchasing-cxml-enhancements-feature"></a>Aktivere funktionen Forbedring af indkøbs-cXML

Hvis du vil aktivere funktionen, skal du åbne siden **[Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og søge efter den funktion, der hedder *Forbedringer af indkøbs-cXML*. Vælg funktionen, og vælg derefter **Aktivér nu** for at aktivere den. (Fra og med Supply Chain Management version 10.0.21 er denne funktion som standard aktiveret.)

Når du har aktiveret funktionen, skal du konfigurere indstillingerne på følgende tre områder:

- **[cXML-parametre](#cxml-parameters)** – Brug disse indstillinger til at konfigurere globale parametre for funktionen til afsendelse af indkøbsordrer.
- **[Kreditoropsætning](#vendor-setup)** – Hvis cXML (commerce eXtensible Markup Language) skal bruges som standard til alle nye indkøbsordrer, der oprettes for en kreditor, skal du angive indstillingen **Send indkøbsordre via cXML** til _Ja_ for den pågældende kreditor.
- **[Eksterne kataloger](#external-catalog-setup)** – Brug de nye indstillinger for **Ordreegenskaber** til at definere formatet for indkøbsordredokumentet, og hvordan det skal sendes.

Denne konfiguration er opsummeret i følgende illustration.

![Områder til konfiguration af cXML-funktioner.](media/cxml-settings-areas.png "Områder til konfiguration af cXML-funktioner")

Derudover skal du konfigurere [batchjobbet for indkøbsordreanmodningen](#po-batch). Dette batchjob bruges til at sende de bekræftede indkøbsordrer.

## <a name="set-up-global-cxml-parameters"></a><a name="cxml-parameters"></a>Konfigurere globale cXML-parametre

Brug siden **cXML-parametre** til at foretage enkelte globale indstillinger, der gælder for funktionaliteten i forbindelse med afsendelse af indkøbsordrer.

![Siden cXML-parametre.](media/cxml-parameters.png "Siden cXML-parametre")

Gå til **Indkøb og forsyning \> Opsætning \> cXML-administration \> cXML-parametre**, og angiv følgende parametre:

- **cXML-testtilstand** – Denne globale parameter påvirker den måde, indkøbsordrer afsendes fysisk fra batchjobbet. Vælg en af følgende værdier:

    - **Test** – I denne tilstand kan batchjobbet køre, og XML-dokumentet for meddelelsen oprettes, men det sendes ikke. Det gemmes i stedet på indkøbsordreanmodningen til gennemsyn. Denne tilstand er nyttig under den første implementering, og du vil se, hvordan data er angivet i cXML-meddelelsen. Du kan også oprette eksempelmeddelelser, som du kan sende til den første validering hos kreditorer.
    - **Direkte** – I denne tilstand bruger funktionen de [eksterne katalogindstillinger](#external-catalog-setup) til fysisk at sende hvert dokument til kreditoren.

- **Send opdateringer for indkøbsanmodning** – Angiv denne indstilling til *Ja* for at sende en opdateringsmeddelelse for indkøbsordrer. Angiv *Nej* for at forhindre, at meddelelsen sendes. De fleste kreditorer foretrækker ikke at modtage opdateringsmeddelelser. De kræver i stedet, at kunderne kontakter dem via telefon eller e-mail, hvis en indkøbsordre skal ændres. Denne parameter er en global parameter, og der kan ikke angives nogen tilsidesætning i det eksterne katalog for hver kreditor. En indkøbsordre vil blive markeret som opdateret, hvis du bogfører endnu en bekræftelse på en indkøbsordre, men den første bekræftelse er allerede blevet sendt og bekræftet af kreditoren. Hvis der er en anden bekræftelse, men den første bekræftelse ikke er blevet sendt, vil den anden bekræftelse blive behandlet som et nyt dokument. Du kan bekræfte en indkøbsordre, så mange gange du vil have afsendt en bekræftelse. Den næste bekræftelse vil derefter blive behandlet som en opdateringsmeddelelse.
- **Send sletning for indkøbsanmodning** – Angiv denne indstilling til *Ja* for at sende en meddelelse om sletning for indkøbsordrer. Angiv *Nej* for at forhindre, at meddelelsen sendes. De fleste kreditorer foretrækker ikke at modtage meddelelser om sletning. De kræver i stedet, at debitorer kontakter dem via telefon eller e-mail, hvis en indkøbsordre blev sendt ved en fejl. Denne parameter er en global parameter, og der kan ikke angives nogen tilsidesætning i det eksterne katalog for hver kreditor. En indkøbsordre markeres som slettet, hvis du annullerer indkøbsordren i Supply Chain Management.
- **Arkivfil** – Angiv den filsti, hvor du vil eksportere og gemme arkiverede cXML-dokumenter. Stien bruges, når du kører fjernelsesfunktionen fra siden **Indkøbsordreanmodning**.
- **Maksimalt antal tegn for linje med vejnavn** – Angiv det maksimale antal tegn, der kan bruges i feltet med vejnavn for adresser i cXML-dokumentet. Denne globale parameter påvirker alle kreditorer, medmindre der er angivet en tilsidesættelse i egenskaberne for det eksterne katalog.

## <a name="set-up-vendor-purchase-orders-to-use-cxml"></a><a name="vendor-setup"></a>Konfigurere indkøbsordrer for kreditorer til at bruge cXML

Hver gang du bekræfter en indkøbsordre, hvor indstillingen **Send indkøbsordre via cXML** er angivet til _Ja_, opretter systemet automatisk cXML-meddelelsen og sender den til den kreditor, der er knyttet til den pågældende indkøbsordre. Du kan styre denne indstilling for indkøbsordrer på to måder:

- Hvis du vil konfigurere en kreditor, så der automatisk bruger cXML til alle nye indkøbsordrer, der er oprettet fra en rekvisition, skal du gå til **Indkøb og forsyning \> Kreditorer \> Alle kreditorer** og vælge eller oprette en kreditor for at åbne siden med detaljer. Derefter skal du i oversigtspanelet **Standardindstillinger for indkøbsordrer** angive indstillingen **Send indkøbsordre via cXML** til _Ja_. Hvis cXML også automatisk skal bruges til nye indkøbsordrer, der **ikke** oprettes ud fra en rekvisition, skal du også angive ordreegenskaben **ENABLEMANUALPO** til _Sand_ for det relaterede eksterne katalog, som det er beskrevet i sektionen [Angive ordreegenskaberne](#set-order-properties) senere i dette emne.
- For individuelle indkøbsordrer skal du gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer** og vælge eller oprette en indkøbsordre for at åbne siden med detaljer i den. Skift til visningen **Overskrift**, og angiv derefter indstillingen **Send indkøbsordre via cXML** efter behov i oversigtspanelet **Opsætning**.

![Standardindstillinger for indkøbsordrer for kreditorer.](media/cxml-order-defaults.png "Standardindstillinger for indkøbsordrer for kreditorer")

## <a name="set-up-an-external-catalog-to-use-cxml"></a><a name="external-catalog-setup"></a>Konfigurere et eksternt katalog til at bruge cXML

På siden **Eksterne kataloger** kan du for hver af dine kataloger konfigurere PunchOut-funktionaliteten og funktionaliteten til afsendelse af indkøbsordrer. Du kan finde de relevante indstillinger ved gå til **Indkøb og forsyning \> Kataloger \> Eksterne kataloger**. Start med at [konfigurere hvert katalog som normalt](set-up-external-catalog-for-punchout.md). Denne proces omfatter tildeling af en kreditor, valg af de kategorier, som kreditoren har tilladelse til at levere, og aktivering af kataloget. Konfigurer derefter de yderligere indstillinger, der er beskrevet i dette afsnit.

> [!NOTE]
> Når du bekræfter en indkøbsordre, der kan sendes via cXML, søger systemet efter den kreditor, der er knyttet til indkøbsordren, og finder derefter det første aktive eksterne katalog, der er knyttet til den pågældende kreditor. Systemet bruger derefter indstillingerne fra det eksterne katalog til at sende indkøbsordren. Hvis der er oprettet flere eksterne kataloger, bruger systemet kun det første eksterne katalog, som det finder, baseret på kreditoren på indkøbsordren. Det anbefales derfor, at du kun opretter ét eksternt katalog for hver kreditor.

![Indstillinger for eksternt katalog.](media/cxml-supplier-catalog.png "Indstillinger for eksternt katalog")

### <a name="set-the-punchout-protocol-type"></a>Angive PunchOut-protokoltypen

I oversigtspanelet **Generelt** på siden **Eksterne kataloger** skal du angive feltet **PunchOut-protokoltype** til _cXML_. Denne indstilling er den eneste tilgængelige indstilling, medmindre en partner har udvidet funktionaliteten og giver en ekstra mulighed i udvidelsen.

Hvis du også bruger kataloget til PunchOut, skal du også [oprette meddelelsesformatet](set-up-external-catalog-for-punchout.md). Meddelelsesformatet bruges til at oprette forbindelsen til kreditor i PunchOut-transaktionen fra rekvisitionen. Når en indkøbsordre sendes, bruges ordreegenskaberne til at oprette forbindelsen til en kreditor.

### <a name="set-the-order-properties"></a><a name="set-order-properties"></a>Angive ordreegenskaberne

Funktionen _Forbedring af indkøbs-cXML_ føjer et nyt oversigtspanel for **Ordreegenskaber** til eksterne kataloger. Dette oversigtspanel viser et gitter, hvor du kan definere ordreegenskaberne. Det viser også en værktøjslinje. Denne værktøjslinje indeholder følgende tre knapper, som du kan bruge til at administrere ordreegenskaberne:

- **Standardegenskaber** – Når du konfigurerer et nyt katalog, skal du vælge denne knap for at føje en foruddefineret samling af almindeligt anvendte egenskaber til gitteret.
- **Ny** – Føj en ny egenskab til gitteret.
- **Slet** – Slet den aktuelt valgte egenskab fra gitteret. Hvis du ved et uheld kommer til at slette en standardegenskab, skal du vælge **Standardegenskaber** for at gendanne alle de manglende egenskaber.

Hver gang du føjer en eller flere egenskaber til gitteret, skal du bruge højre kolonne til at angive en værdi for hver enkelt.

Brug standardegenskaberne på følgende måde:

- **BUYER\_COOKIE** – dette sporings felt kan bruges til at angive specifikke oplysninger for din virksomhed. Medmindre du har en aftale med kreditoren om, hvordan denne egenskab anvendes, har den ikke den store betydning, når der sendes en indkøbsordre. Derfor skal du angive den til en simpel værdi.
- **DELIVERTO** – Når forsendelsesadressen angives i dokumentet fra indkøbsordren, bruges feltet **Attentionoplysninger** til at angive feltet **DeliverTo** i XML-meddelelsen. Hvis du kræver, at denne værdi skal være navnet på en anmoder, og du vil angive anmoderfeltet i indkøbsordrehovedet, skal du angive værdien _REQUESTER_ for denne egenskab, så navnet på anmoderen angives i feltet **DeliverTo** i XML-koden. I dette tilfælde kommer den primære e-mailadresse og det telefonnummer, der bruges, fra anmoderen i stedet for ordregiveren.
- **DEPLOYMENTMODE** – Angiv denne egenskab som påkrævet af kreditoren. Værdierne er normalt _PRODUCTION_ eller _TEST_. Angiv værdien baseret på din kommunikation med kreditoren. Normalt skal den stemme overens med det tilsigtede system bag **ORDERCHECKURL**-værdien, som kreditoren angiver som et test- eller produktionssystem.
- **FIXEDBILLADDRESSID** – Når feltet **addressID** i XML-meddelelsen er angivet, vælger det den placering, der er angivet på adressen. Hvis den id-værdi, du har kommunikeret til kreditoren, afviger fra værdien på adresseplaceringen af en eller anden grund, kan du gennemtvinge en tilsidesættelse ved at angive værdien her. Det forudsættes, at du kun skal bruge én adresse med kreditoren, og at adressen er konfigureret i kreditorsystemet. Faktureringsadressen er den primære fakturaadresse, der er angivet for den juridiske enhed i Supply Chain Management.
- **FIXEDSHIPADDRESSID** – Når feltet **addressID** i XML-meddelelsen er angivet, vælger det den placering, der er angivet på adressen. Hvis den id-værdi, du har kommunikeret til kreditoren, afviger fra værdien på adresseplaceringen af en eller anden grund, kan du gennemtvinge en tilsidesættelse ved at angive værdien her. Det forudsættes, at du kun skal bruge én adresse med kreditoren, og at adressen er konfigureret i kreditorsystemet. Forsendelsesadressen er den adresse, der er angivet i indkøbsordrehovedet. De fleste kreditorer accepterer kun adresser i ordrehovedet, ikke linjeadresser. Selvom der er felter til linjeadresser i XML-koden, vil de blive angivet til adressen i ordrehovedet.
- **FROM\_DOMAIN** – Angiv den værdi, der bruges til at sende indkøbsordredokumenter. Denne værdi leveres af din kreditor.
- **FROM\_IDENTITY** – Angiv den værdi, der bruges til at sende indkøbsordredokumenter. Denne værdi leveres af din kreditor.
- **ORDERCHECKURL** – Angiv den URL-adresse, som indkøbsordredokumenterne skal overføres til. Denne URL-adresse starter med `https://` og oplyses af din kreditor.
- **PAYLOAD\_ID** – Angiv en præfiksværdi for det nyttedata-id, der kræves til de forretningsprocesser, der gør sig gældende for den aktuelle kreditor.
- **SENDER\_DOMAIN** – Angiv den værdi, der bruges til at sende indkøbsordredokumenter. Denne værdi leveres af din kreditor.
- **SENDER\_IDENTITY** – Angiv den værdi, der bruges til at sende indkøbsordredokumenter. Denne værdi leveres af din kreditor.
- **SHARED\_SECRET** – Angiv den værdi, der bruges til at sende indkøbsordredokumenter. Denne værdi leveres af din kreditor.
- **STREETLENGTH** – Angiv et tal, der angiver det maksimale antal tegn, som kreditoren accepterer som vejnavn. Hvis der angives en værdi her, tilsidesættes den værdi, der er angivet på siden **cXML-parametre**. Systemet fjerner linjeskift og mellemrum i forsøget på at tilpasse standardadressen i Supply Chain Management til det antal tegn, der er angivet her. Alle andre tegn vil blive afkortet.
- **>TO\_DOMAIN** – Angiv den værdi, der bruges til at sende indkøbsordredokumenter. Denne værdi leveres af din kreditor.
- **TO\_IDENTITY** – Angiv den værdi, der bruges til at sende indkøbsordredokumenter. Denne værdi leveres af din kreditor.
- **USERAGENT** – Angiv en værdi, der identificerer det system, du bruger. Angiv for eksempel _Dynamics 365 Supply Chain Management_.
- **VERSION** – Angiv et cXML-versionsnummer, hvis kreditoren anmoder om disse oplysninger. Standardværdien er *1.2.008*. Denne version er stabil og accepteret af de fleste kreditorer.
- **RESPONSETEXT** – Angiv en brugerdefineret tekst, du forventer, at kreditoren returnerer, i cXML-svarmeddelelsen, når ordren er sendt. På denne måde kan systemet markere meddelelsen som _Bekræftet_. Hvis svaret ikke svarer til standardteksten eller den debitortekst, du angiver her, vil anmodningen blive markeret som _Fejl_.
- **RESPONSETEXTSUB** – Angiv denne egenskab til _TRUE_, hvis du vil søge efter de værdier i kreditorens svartekst, der er angivet i feltet **RESPONSETEXT**. Kreditoren kan f.eks. returnere en lang streng, der indeholder "OK" i svaret. I dette tilfælde kan du angive _OK_ i feltet **RESPONSETEXT** og angive **RESPONSETESTSUB** til _TRUE_ for at søge efter "OK" hvor som helst i svaret. Ordren kan derefter angives til _Bekræftet_.
- **CONTENTTYPE** – I en typisk katalogopsætning skal du ikke angive denne egenskab. Hvis du modtager en server 500-fejl fra en kreditors system, når du sender en indkøbsordre, kan du udføre en test ved at angive denne egenskab til _FALSE_. Denne værdi ændrer en indstilling i webanmodningen og kan tillade, at meddelelsen sendes til visse platforme.
- **ENABLEHEADERS** – Angiv denne egenskab til _TRUE_ for at sende ordrehoveder sammen med indkøbsordren. Du skal kun angive denne egenskab, hvis kreditoren kræver det. Hvis du angiver denne egenskab til _TRUE_, kan du tilføje ekstra brugerdefinerede egenskaber, der er baseret på de navne, som kreditoren oplyser, og angive dem med præfikset _H\__. Typiske eksempler omfatter **H\_USERID**, **H\_PASSWORD**, **H\_RECEIVERID** og **H\_ACTIONREQUEST**. Følgende brugerdefinerede egenskaber er medtaget i standardegenskaberne:

    - **H\_USERID** – Hvis handelspartneren kræver, at du sender et bruger-id som en del af URL-adressen for at sende en indkøbsordre, skal du angive værdien her.
    - **H\_PASSWORD** – Hvis handelspartneren kræver, at du sender en adgangskode som en del af URL-adressen for at sende en indkøbsordre, skal du angive værdien her.

- **ENABLEMANUALPO** – Hvis denne egenskab er angivet til _TRUE_, når brugere opretter indkøbsordrer manuelt (dvs. når de ikke starter fra en rekvisition), arver disse indkøbsordrer indstillingen fra indstillingen **Send indkøbsordre via cXML** fra kreditoren. Hvis denne egenskab ikke er angivet, eller hvis den er angivet til _FALSE_, angives indstillingen **Send indkøbsordre via cXML** ikke på indkøbsordrehovedet for manuelt oprettede indkøbsordrer. I forbindelse med indkøbsordrer, der oprettes ud fra en rekvisition, nedarves indstillingen fra indstillingen **Send indkøbsordre via cXML** altid fra kreditoren, uafhængigt af indstillingen for denne egenskab. Du kan finde flere oplysninger i sektionen [Konfigurere indkøbsordrer for kreditorer til at bruge cXML](#vendor-setup) tidligere i dette emne.
- **PUNCHOUTPOONLY** – Hvis denne egenskab er angivet til _TRUE_, er det kun indkøbsrekvisitionslinjer, der er oprettet via PunchOut-processen, som angiver indstillingen **Send indkøbsordre via cXML** på indkøbsordrehovedet. Derudover skal indkøbsrekvisitionslinjetypen for alle linjer i indkøbsordren være _Ekstern katalogvare_. Ellers kan cXML-indkøbsordre ikke oprettes.
- **PUNCHOUTSHIPTO** – Hvis denne egenskab er angivet til _TRUE_, vil standardadressen for den juridiske enhed blive føjet til admodningsmeddelelsen om PunchOut-opsætning, når brugeren åbner et eksternt katalog. Denne adresse tilføjes som **ShipTo**-adressen. Kreditorer bruger **ShipTo**-adressen til at vise prisfastsættelse ud fra virksomhedens placering.
- **TRACEPUNCHOUT** – Angiv denne egenskab til _TRUE_, hvis du får vist en fejlmeddelelse, når du forsøger at gå til et eksternt katalog fra rekvisitionen. Sporingsoplysninger udfyldes derefter for **PunchOutSetupRequest**- og **PunchOutResponse**-meddelelser, der sendes mellem Supply Chain Management og kreditorens lokalitet. Du kan få vist disse oplysninger på siden **Meddelelseslog for cXML-indkøbsvogn**, som du kan åbne fra siden **Opsætning af eksternt katalog** for det kreditorkatalog, du har problemer med. Du bør kun angive denne egenskab til _TRUE_, hvis du foretager fejlfinding, da den skaber en stor ydeevnebelastning på databasen for hvert PunchOut. Du kan finde flere oplysninger i sektionen [Få vist meddelelsesloggen for cXML-indkøbsvogn for eksternt katalog, PunchOut](#message-log) senere i dette emne.
- **REPLACENEWLINE** – Angiv denne egenskab til _TRUE_, hvis du oplever et problem, fordi en kreditors system sender en **PunchOutResponse**-meddelelse, der indeholder tegn på nyoprettede linjer (\\n). Dette problem kan opstå, hvis kreditorens meddelelser fortolkes via middleware eller en indkøbshub. Hvis du har problemer med en ny kreditoropsætning, skal du angive egenskaben **TRACEPUNCHOUT** til _TRUE_ for at få vist **PunchOutResponse**-meddelelsen og afgøre, om XML-koderne skal opdeles med tegn på nyoprettede linjer.
- **POCOMMENTS** – Angiv denne egenskab til _TRUE_, hvis cXML-dokumentet skal indeholde notater, der er knyttet til indkøbsordren i Supply Chain Management. Den vedhæftede tekst er medtaget i kommentarerne i ordrehovedet i indkøbsordremeddelelsen. Du kan finde flere oplysninger om, hvordan systemet vælger og behandler disse vedhæftede filer, i sektionen [Vedhæfte noter til en indkøbsordre](#attach-po-notes) senere i dette emne.
- **VENDCOMMENTS** – Angiv denne egenskab til _TRUE_, hvis cXML-dokumentet skal indeholde notater, der er knyttet til indkøbsordren i Supply Chain Management. Den vedhæftede tekst er medtaget i kommentarerne i ordrehovedet i indkøbsordremeddelelsen. Du kan finde flere oplysninger om, hvordan systemet vælger og behandler disse vedhæftede filer, i sektionen [Vedhæfte noter til en indkøbsordre](#attach-po-notes).
- **CLEANAMP** – Angiv denne egenskab til _TRUE_, hvis du modtager en fejlmeddelelse, når du forsøger at udføre en PunchOut til en kreditor, og kreditorens returnerings-URL-adresse indeholder forkert kodede tegn (\&).
- **PUNCHOUTTZ** – Angiv denne egenskab til _TRUE_, hvis den kreditor, du arbejder med, bruger ISO 8601-standarden (International Organization for Standardization) til at foretage en bestemt validering af dato/klokkeslæt for PunchOut-anmodningsmeddelelsen. Supply Chain Management bruger UTC-datoen i **PunchOutSetupRequest**-meddelelsen. Når du angiver denne egenskab til _TRUE_, føjes *+00:00* derfor til dato-/klokkeslætsformatet.
- **WMSADDRESSID** – Angiv denne egenskab til _TRUE_ for at bruge lagerstedsnummeret på indkøbsordrehovedet som **addressID**-værdien i den **ShipTo**-adresse for den indkøbsordreanmodning, der sendes til kreditoren. Hvis du angiver en værdi for egenskaben **FIXEDSHIPADDRESSID**, tilsidesætter denne værdi den anden værdi. Derfor skal du bruge én egenskab eller den anden til at angive **addressID**-værdien i **ShipTo**-adressen for dokumentet.
- **PUNCHOUTSHIPTOUSER** – Denne egenskab fungerer sammen med egenskaben **PUNCHOUTSHIPTO**. Hvis **PUNCHOUTSHIPTO** er angivet til _TRUE_, hentes adressen for den juridiske enhed. Hvis **PUNCHOUTSHIPTOUSER** er angivet til _TRUE_, bruges den primære adresse fra PunchOut-brugeren i stedet for adressen på den juridiske enhed.

### <a name="activate-the-external-catalog"></a>Aktivere det eksterne katalog

Når du er færdig med at definere egenskaberne og konfigurere andre indstillinger for det eksterne katalog, skal du gå tilbage til oversigtspanelet **Generelt** på siden **Eksternt kataloger** og angive indstillingen **Aktiv** til *Ja*.

### <a name="attach-notes-to-a-purchase-order"></a><a name="attach-po-notes"></a>Vedhæfte noter til en indkøbsordre

Som beskrevet i sektionen [Angive ordreegenskaber](#set-order-properties) – hvis den leverede cXML skal medtage tekst fra noter, der er vedhæftet de relevante indkøbsordrer og/eller kreditorposter, kan du angive egenskaben **POCOMMENTS** og/eller **VENDCOMMENTS** til _TRUE_ i opsætningen af det eksterne katalog. Denne sektion giver flere oplysninger om, hvordan systemet vælger og behandler disse vedhæftede filer, hvis du bruger dem.

Du kan angive de notattyper, som systemet skal søge efter, ved at gå til **Indkøb og forsyning \> Opsætning \> Formularer \> Fra opsætning**. På fanen **Indkøbsordre** skal du derefter angive feltet **Medtag dokumenter af typen** den notattype, som skal medtages. Det er kun tekstnoter, der medtages, ikke vedhæftede dokumenter.

![Siden Formularopsætning.](media/cxml-form-setup.png "Siden Formularopsætning")

Vedhæftede filer vil kun blive medtaget i en indkøbsordre, hvis deres felt **Type** er angivet til den værdi, du vælger i feltet **Medtag dokumenter af typen**, og hvis deres felt **Begrænsning** er angivet til _Ekstern_. Hvis du vil oprette, få vist eller redigere de vedhæftede filer for en indkøbsordre, skal du gå til **Indkøb og forsyning \> Alle indkøbsordrer**, vælge eller oprette en indkøbsordre og derefter vælge knappen **Vedhæftede filer** (symbolet med papirklip) i øverste højre hjørne.

![Vedhæftet note, der er konfigureret til at blive sendt til en kreditor.](media/cxml-note-to-vendor.png "Vedhæftet note, der er konfigureret til at blive sendt til en kreditor")

## <a name="view-the-cxml-cart-message-log-for-external-catalog-punchout"></a><a name="message-log"></a>Få vist meddelelsesloggen for cXML-indkøbsvogn for eksternt katalog, PunchOut

Når du angiver feltet **PunchOut-protokoltype** til _cXML_ for et eksternt katalog, vil systemet registrere en meddelelseslog for de indkøbsvogne, der returneres fra kreditorer. Denne log kan bruges til fejlfinding og andre dataformål.

Hvis du vil åbne loggen for et eksternt katalog, skal du vælge det relevante katalog og derefter vælge **Meddelelseslog for cXML-indkøbsvogn**. På siden **Meddelelseslog for cXML-indkøbsvogn** vises en liste over de indkøbsvogne, der er returneret, den XML, der er knyttet til disse indkøbsvogne, og de linjer, der blev oprettet på den relaterede indkøbsrekvisition.

![Siden Meddelelseslog for cXML-indkøbsvogn.](media/cxml-cart-message-log.png "Siden Meddelelseslog for cXML-indkøbsvogn")

## <a name="set-the-extrinsic-elements-for-external-catalog-punchout"></a>Angive ydre elementer for eksternt katalog, PunchOut

Når du angiver feltet **PunchOut-protokoltype** til *cXML* for et eksternt katalog, kan du tilføje brugerdefinerede ydre elementer, der indsættes på det korrekte sted i XML-anmodningsmeddelelsen.

Du kan føje ydre elementer til et eksternt katalog ved at følge nedenstående trin.

1. Gå til **Indkøb og forsyning \> Kataloger \> Eksterne kataloger**.
1. Vælg det relevante katalog.
1. I oversigtspanelet **Meddelelsesformat** skal du i sektionen **Ydre** vælge **Tilføj** for at føje en række til gitteret for hvert ydre element, du vil medtage. På hver række skal du angive følgende felter:

    - **Navn** – Angiv et navn på elementet. Denne værdi bliver værdien for attributten **Navn** for det **Ydre** XML-element, der oprettes af hver række. Normalt vil du sammen med kreditoren aftale navnet på hvert ydre element.
    - **Værdi** – Vælg en værdi for elementet. Denne værdi bliver værdien for det XML-element, der oprettes af hver række. Følgende værdier er tilgængelige:

        - **Brugernavn** – Brug navnet på den bruger, der foretager PunchOut. Dette navn er logonnavnet til Supply Chain Management.
        - **Brugermail** – Brug mailadressen på den bruger, der foretager PunchOut. Denne adresse er den adresse, som brugeren har oprettet på fanen **Konto** på siden **Brugerindstillinger**.
        - **Tilfældig værdi** – Brug en entydig, tilfældig værdi.
        - **Brugerens fulde navn** – Brug det fulde navn på den kontaktperson, der er knyttet til den bruger, der skal have adgang til det eksterne katalog.
        - **Fornavn** – Brug fornavnet på den kontaktperson, der er knyttet til den bruger, der skal have adgang til det eksterne katalog.
        - **Efternavn** – Brug efternavnet på den kontaktperson, der er knyttet til den bruger, der skal have adgang til det eksterne katalog.
        - **Telefonnummer** – Brug det primære telefonnummer på den kontaktperson, der er knyttet til den bruger, der skal have adgang til det eksterne katalog.

![Indstillinger for ydre element.](media/cxml-extrinsics.png "Indstillinger for ydre element")

Brugeren eller administratoren kan ikke se de ydre elementer, fordi de ikke tilføjes, før brugeren foretager en PunchOut. De indsættes automatisk mellem elementerne **BuyerCookie** og **BrowserFromPost** i cXML-meddelelsen om opsætningsanmodning. Derfor behøver du ikke at angive dem manuelt i XML, når du konfigurerer det eksterne katalog.

![Ydre elementer føjet til XML.](media/cxml-extrinsics-xml.png "Ydre elementer føjet til XML")

## <a name="create-and-process-a-purchase-order"></a><a name="create-po"></a>Oprette og behandle en indkøbsordre

Når du opretter en indkøbsordre for en kreditor, vil den nedarve indstillingen fra indstillingen **Send indkøbsordre via cXML** fra denne kreditor. Indstillingen forbliver dog tilgængelig i oversigtspanelet **Opsætning** i **overskriftsvisningen** for indkøbsordren, så du kan ændre den senere efter behov.

![Indkøbsordre angivet til at bruge cXML.](media/cxml-purchase-order.png "Indkøbsordre angivet til at bruge cXML")

Når du opretter en indkøbsordre fra en indkøbsrekvisition, der stammer fra et PunchOut-flow, udfyldes alle de nødvendige linjedetaljer. Derefter kan du manuelt tilføje indkøbsordrelinjer eller kopiere dem fra andre indkøbsordrer. Sørg for at angive alle obligatoriske felter. De obligatoriske felter omfatter det eksterne referencenummer, som er det kreditornummer, der skal bruges i cXML-meddelelsen.

![Eksempel på et eksternt referencenummer.](media/cxml-line-details.png "Eksempel på et eksternt referencenummer")

Når du er færdig med at udfylde alle detaljer for indkøbsordren, skal du huske at bekræfte den. Der sendes ingen meddelelse, medmindre indkøbsordren er bekræftet. Du kan bekræfte en indkøbsordre ved at gå til handlingsruden på fanen **Indkøb** og vælge **Bekræft** i gruppen **Handlinger**. 

Når indkøbsordren er bekræftet, kan du få vist statussen for bekræftelsen via kladderne **Bekræftelser på indkøbsordrer**. Vælg **Bekræftelser på indkøbsordrer** i gruppen **Kladder** på fanen **Indkøb** i handlingsruden.

Alle indkøbsordrer kan have mange bekræftelser. Hver bekræftelse er markeret med et trinvist tal. I følgende illustration er indkøbsordren *00000275*, og bekræftelsen er *00000275-1*. Denne nummerering afspejler Supply Chain Management-standardfunktionen, hvor ændringer i en indkøbsordre, og derfor den type cXML-meddelelse, der skal sendes til kreditoren, identificeres på grundlag af bekræftelsen. Som illustrationen viser, indeholder siden **Bekræftelser på indkøbsordrer** også felterne **Status på ordreafsendelse** og **Status på ordreanmodning for kreditor**. Du kan finde flere oplysninger om de forskellige statusværdier, du kan se på denne side, i sektionen [Overvåge indkøbsordreanmodninger](#monitor-po-requests) senere i dette emne.

![Siden Bekræftelser på indkøbsordrer.](media/cxml-po-confirmations.png "Siden Bekræftelser på indkøbsordrer")

Hvis du vil have vist flere oplysninger om dokumentet, skal du vælge **Indkøbsordreanmodning** over gitteret.

Siden **Indkøbsordreanmodning** indeholder to gitre. Gitteret på den øverste del af siden har én post for hver indkøbsordre, der er markeret til afsendelse. Gitteret på fanen **Historik for indkøbsordreanmodning** på den nederste del af siden kan have flere poster for den valgte indkøbsordre for at angive status for hver bekræftelse. I følgende illustration vises indkøbsordre 00000275 i det øverste gitter og dokument 00000275-1 i gitteret på fanen **Historik for indkøbsordreanmodning**.

![Siden Indkøbsordreanmodning.](media/cxml-po-request.png "Siden Indkøbsordreanmodning")

Hvis batchjobbet er konfigureret og kører, vil dokumentet blive sendt. Du kan få vist statusændringen, efter at dokumentet er afsendt. I følgende illustration er feltet **Status på ordreafsendelse** angivet til _Sent_. Feltet **Status på ordreanmodning for kreditor** er angivet til _Bekræftet_ for at angive, at kreditoren har modtaget dokumentet, og at denne var i stand til at læse og gemme det i sit system. Gitteret på fanen **Historik for indkøbsordreanmodning** viser det tidspunkt, hvor dokumentet blev sendt. Du kan finde flere oplysninger om de forskellige statusværdier, du kan se på denne side, i sektionen [Overvåge indkøbsordreanmodninger](#monitor-po-requests).

![Statusmeddelelser på siden Indkøbsordreanmodning.](media/cxml-po-request-2.png "Statusmeddelelser på siden Indkøbsordreanmodning")

## <a name="schedule-the-purchase-order-request-batch-job"></a><a name="po-batch"></a>Planlægge batchjob for Indkøbsordreanmodning

Hvis du vil aktivere batchjobbet til afsendelse af indkøbsordreanmodninger, skal du gå til **Indkøb og forsyning \> Opsætning \> cXML-administration \> Indkøbsordreanmodning** og i oversigtspanelet på fanen **Indkøbsordreanmodning** i gruppen **Batch** vælge **Send job** for at åbne dialogboksen **Forbered og send indkøbsanmodning** Du kan bruge denne dialogboks til at konfigurere gentagelsen på samme måde som for batchjob i Supply Chain Management. Vælg et interval, der er baseret på ordrens volumen. Selvom du kan køre batchjobbet hvert minut, er det nok bedst at sende batchjob i løbet af arbejdsdagen på baggrund af de tidsvinduer for ordrekvitteringer, der svarer til dine kreditorers tidsplaner.

Din kreditor kan f.eks. have en politik, der angiver, at alle ordrer, der modtages senest kl. 13.00, skal afsendes samme dag. I dette tilfælde skal du muligvis kun køre batchjobbet nogle få gange om morgenen for at kommunikere de ordrer, du har. De resterende ordrer vil derefter blive sendt næste dag. Denne beslutning er udelukkende en virksomhedsbeslutning. Du kan gennemse den og angive parametrene i overensstemmelse hermed.

Processen vil søge efter indkøbsordredokumenter, der har statussen *Afventer*. Hvis du har en ordre, som du skal sende til en kreditor med det samme, kan du vælge **Send job** og angive indstillingen **Batchbehandling** til *Nej*.

## <a name="monitor-purchase-order-requests"></a><a name="monitor-po-requests"></a>Overvåge indkøbsordreanmodninger

### <a name="view-the-status-of-a-purchase-order"></a>Få vist statussen for en indkøbsordre

Når ordrer, der kan sendes via cXML, bekræftes, går de i statussen _Afventer_. Som det er beskrevet i [Oprette og behandle en indkøbsordre](#create-po), kan du få vist statussen for indkøbsordren på siden **Indkøbsordreanmodning**. Hver indkøbsordreanmodning kan have én af flere statusser, afhængigt af parametrene og dataene. I denne sektion beskrives de forskellige statustyper og de værdier, de kan have. Disse oplysninger kan hjælpe dig med at administrere problemer og forstå statussen for indkøbsordrer.

![Status for indkøbsordrer på siden Indkøbsordreanmodning.](media/cxml-monitor-po-request.png "Status for indkøbsordrer på siden Indkøbsordreanmodning")

I gitteret i den øverste del af siden **Indkøbsordreanmodning** kan du få vist følgende statusværdier:

- **Status på ordreafsendelse** – Dette felt kan have en af følgende værdier:

    - **Afventer** – Dokumentet venter på at blive sendt.
    - **Sendt** – Dokumentet er sendt.
    - **Stoppet** – Dokumentet blev markeret som _Stoppet_, før det blev sendt. (Du kan markere et dokument som _Stoppet_ ved at vælge **Stop** i handlingsruden på siden **Indkøbsanmodning**).
    - **Arkiv** – Dokumentet er slettet. (Du kan fjerne et dokument ved at vælge **Fjern** i handlingsruden på siden **Indkøbsanmodning**).

- **Status på ordreanmodning for kreditor** – Dette felt kan have en af følgende værdier:

    - **Afventer** – Dokumentet venter på at blive sendt.
    - **Bekræftet** – Dokumentet er bekræftet som modtaget af kreditoren. Du kan gennemse den detaljerede XML-meddelelse, der returneres fra leverandøren, ved at vælge fanen **Svar-XML** på den nederste del af siden.
    - **Fejl** – Dokumentet blev sendt til kreditoren, men der opstod en fejl. Du kan gennemse fejlmeddelelsen ved at vælge fanen **Svar-XML** på den nederste del af siden.

Gitteret på fanen **Historik for indkøbsordreanmodning** på den nederste del af siden **Indkøbsordreanmodning** kan vise følgende værdier:

- **Ordreanmodnignstype** – Dette felt kan have en af følgende værdier:

    - **Ny** – Linjen er markeret som ny, straks efter at indkøbsordren er bekræftet.
    - **Opdatering** – Hvis en bekræftelse allerede er blevet sendt og bekræftet af kreditoren, vil den næste bekræftelse blive markeret som _Opdatering_. Opdateringer sendes kun, hvis indstillingen **Send opdateringer for indkøbsanmodning** er angivet til *Ja* i de [globale cXML-parametre](#cxml-parameters).
    - **Slet** – Hvis en bekræftelse allerede er blevet sendt og bekræftet af kreditoren, men indkøbsordren annulleres, vil den bekræftelse, der venter, blive markeret som _Slet_. Sletninger sendes kun, hvis indstillingen **Send sletning for indkøbsanmodning** er angivet til *Ja* i de [globale cXML-parametre](#cxml-parameters).

- **Anmodningstidspunkt** – Det tidspunkt, hvor ordrebekræftelsen blev oprettet. Du kan sammenligne anmodningstidspunktet med ordrestatustidspunktet for at fastlægge tiden mellem bekræftelse og kreditorens bekræftelse.
- **Status på ordreafsendelse** – Dette felt er det samme som feltet **Status på ordreafsendelse** på den øverste del af siden. Det gentages her for at gøre det lettere at få vist statussen på bekræftelsesniveau. Hvis feltet **Ordreanmodningstype** er angivet til *Ny*, og indkøbsordren er bekræftet igen, før der sendes en bekræftelse, er feltet **Status på ordreafsendelse** angivet til *Arkiv*.
- **Ordrestatustidspunkt** – Det tidspunkt, hvor historikposten for indkøbsordreanmodningen sidst blev opdateret. (Opdateringerne omfatter statusændringer).
- **Status på ordreanmodning for kreditor** – Dette felt er det samme som feltet **Status på ordreanmodning for kreditor** på den øverste del af siden. Det gentages her for at gøre det lettere at få vist statussen på bekræftelsesniveau.
- **Tidspunkt for ny afsendelse** – Tidspunktet, hvor posten blev sendt igen.
- **Antal nye afsendelser** – Det antal gange, posten blev sendt igen. Et højt antal angiver flere fejl og kan derfor angive et problem med enten din dataopsætning eller kreditorens dataopsætning.

### <a name="view-the-xml-for-a-purchase-order-request-message"></a>Få vist XML for en meddelelse om indkøbsordreanmodning

Hvis du vil have vist XML for meddelelsen om indkøbsordreanmodningen, skal du vælge **Anmod om XML-tekst** nederst på siden **Indkøbsordreanmodning**. Oplysningerne på denne fane kan være nyttige ved test eller fejlvalidering. Du kan gøre oplysningerne lettere at læse ved at få vist dem som en formateret meddelelse. Kopiér indholdet fra fanen til en tekstfil, og få det vist i en XML-editor.

![Fanen Anmod om XML-tekst.](media/cxml-request-xml-text.png "Fanen Anmod om XML-tekst")

### <a name="view-the-details-of-the-vendor-response"></a>Få vist detaljerne for kreditorens svar

Hvis du vil have vist indholdet af en kreditors bekræftelse eller fejlsvar, skal du vælge fanen **Svar-XML** nederst på siden **Indkøbsordreanmodning**.

![Fanen Svar-XML.](media/cxml-response-xml.png "Fanen Svar-XML")

## <a name="additional-resources"></a>Yderligere ressourcer

- [Konfigurere et eksternt katalog til PunchOut e-indkøb](set-up-external-catalog-for-punchout.md)
- [Bruge eksterne kataloger til PunchOut e-indkøb](use-external-catalogs-for-punchout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]