---
title: Oversigt over elektronisk rapportering (ER)
description: Dette emne indeholder en oversigt over værktøjet Elektronisk rapportering. Det indeholder en beskrivelse af nøglebegreber, understøttede scenarier og formater, der er en del af løsningen.
author: NickSelin
ms.date: 09/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "58941"
- intro-internal
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0fd83c787be4d9de151d2727384d07bc209e33f
ms.sourcegitcommit: 86f0574363fb869482ef73ff294f345f81d17c5b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7562170"
---
# <a name="electronic-reporting-er-overview"></a>Oversigt over elektronisk rapportering (ER)

[!include [banner](../includes/banner.md)]

Dette emne indeholder en oversigt over værktøjet Elektronisk rapportering (ER). Den indeholder oplysninger om centrale koncepter, de scenarier, som ER understøtter, samt en liste over formater, der er designet og udgivet som del af løsningen.

ER er et værktøj, du kan bruge til at konfigurere formater for både indgående og udgående elektroniske dokumenter i overensstemmelse med de lovgivningsmæssige krav i forskellige lande/områder. Med ER du administrere disse formater i løbet af deres livscyklus. For eksempel kan du overholde nye lovgivningsmæssige krav og oprette forretningsdokumenter i det krævede format for at udveksle oplysninger elektronisk med offentlige myndigheder, banker og andre parter.

ER-programmet henvender sig til virksomhedsbrugere i stedet for udviklere. Da du konfigurerer formater frem for kode, udføres processer til oprettelse og tilpasning af formater for elektroniske dokumenter hurtigere og nemmere.

ER understøtter i øjeblikket TEXT, XML, Microsoft Word-dokument og OPENXML-regnearksformater. Men der er mulighed for understøttelse af flere formater.

## <a name="capabilities"></a>Egenskaber

ER-programmet har følgende funktioner:

- Det repræsenterer et enkelt delt værktøj til elektronisk indberetning i forskellige domæner og erstatter mere end 20 forskellige programmer, der foretager en eller anden form for elektronisk rapportering i Finance and Operations.
- Det isolerer en rapports format fra den aktuelle implementering. Med andre ord kan formatet anvendes i forskellige versioner.
- Det understøtter oprettelse af et brugerdefineret format, der er baseret på et oprindeligt format. Det indeholder også funktioner til automatisk at opgradere det tilpassede format, når det oprindelige format ændres pga. lokaliserings-/tilpasningskrav.
- Det bliver det primære standardværktøj til understøttelse af lokaliseringskrav i forbindelse med elektronisk rapportering, for både Microsoft og MS-partnere.
- Det understøtter muligheden for at distribuere formater til partnere og debitorer via Microsoft Dynamics Lifecycle Services (LCS).

## <a name="key-concepts"></a>Nøglebegreber

### <a name="components"></a>Komponenter

Elektronisk rapportering (ER) understøtter følgende komponenttyper:

- Datamodel
- Modeltilknytning
- Formater
- Metadata

Du kan finde flere oplysninger under [Elektronisk rapporteringskomponenter](er-overview-components.md).

#### <a name="data-model-and-model-mapping-components"></a>Komponenter til datamodel og modeltilknytning

En datamodelkomponent er en abstrakt repræsentation af en datastruktur. Den bruges til at beskrive et bestemt forretningsdomæneområde, der er tilstrækkeligt detaljeret til at opfylde kravene til rapportering for det pågældende domæne. En data modelkomponent består af følgende dele:

- <a name="DataModelComponent"></a>En datamodel som et sæt af domænespecifikke forretningsenheder samt en hierarkisk struktureret definition af relationerne mellem enhederne.
- <a name="ModelMappingComponent"></a>En modeltilknytning, som sammenkæder valgte programdatakilder med enkelte elementer i en datamodel, der under kørsel angiver dataflow og regler for forretningsdatapopulation til en datamodelkomponent.

En forretningsenhed af en datamodel er repræsenteret som en beholder (post). Egenskaber for forretningsenheden er repræsenteret som dataelementer (felter). Hvert dataelement har et entydigt navn, etiket, beskrivelse og værdi. Værdien af hvert dataelement kan være udformet, så den kan genkendes som en streng, heltal, reelt tal, dato, fasttekst, boolesk osv. Desuden kan det være en anden post eller postliste.

En enkelt modelkomponent kan indeholde flere hierarkier af domænespecifikke forretningsobjekter. Den kan også indeholde modeltilknytninger, der understøtter et rapportspecifikt dataflow på kørselstidspunktet. Hierarkierne afpasses efter en enkelt post, der er valgt som en rod for modeltilknytningen. Datamodellen for betalingsdomæneområdet kan f.eks. understøtte følgende tilknytninger:

- Virksomhed \> Kreditor \> Betalingstransaktioner for AP-domænet
- Debitor \> Virksomhed \> Betalingstransaktioner for AR-domænet

Bemærk forretningsenheder som f.eks firma- og betalingsposteringer angives én gang. Forskellige tilknytninger genbruger dem.

En modeltilknytning, der understøtter udgående elektroniske dokumenter, har følgende muligheder:

- Den kan bruge forskellige datatyper som datakilder til en datamodel. Den kan for eksempel bruge tabeller, dataenheder, metoder eller fasttekster.
- Den understøtter brugerinputparametre, der kan defineres som datakilder for en datamodel, når data skal angives på kørselstidspunktet.
- Den understøtter transformationen af data til de grupper, der kræves. Den gør det også muligt at filtrere, sortere og summere data og tilføje logisk beregnede felter, der er designet via formler, der ligner Microsoft Excel-formler. Du kan finde flere oplysninger under [Formeldesigner i elektronisk rapportering (ER)](general-electronic-reporting-formula-designer.md).

En modeltilknytning, der understøtter indgående elektroniske dokumenter, har følgende muligheder:

- Det kan bruge forskellige opdaterbare dataelementer som mål. Disse dataelementer omfatter tabeller, dataenheder og visninger. Dataene kan opdateres ved hjælp af dataene fra de indgående elektroniske dokumenter. Der kan bruges flere destinationer i en enkelt modeltilknytning.
- Den understøtter brugerinputparametre, der kan defineres som datakilder for en datamodel, når data skal angives på kørselstidspunktet.

Der udvikles en datamodelkomponent til hvert forretningsdomæne, der skal bruges som en samlet datakilde til rapportering, der isolerer rapportering fra den fysiske implementering af datakilder. Den repræsenterer domænespecifikke forretningsbegreber og -funktioner i en formular, der gør et rapporteringsformats oprindelige design og yderligere vedligeholdelse mere effektivt.

#### <a name="format-components-for-outgoing-electronic-documents"></a><a name="FormatComponentOutbound"></a>Formatkomponenter for udgående elektroniske dokumenter

En formatkomponent er skemaet for rapporteringsoutput, der skal oprettes på kørselstidspunktet. Et skema består af følgende elementer:

- Et format, der definerer strukturen og indholdet af det udgående elektroniske dokument, der oprettes på kørselstidspunktet.
- Datakilder som et sæt brugerinputparametre og en domænespecifik datamodel, der bruger en valgt modeltilknytning.
- En formattilknytning som et sæt bindinger af formatdatakilder, der har enkelte elementer af et format, der angiver dataflow og regler for formatoutputgenerering på kørselstidspunktet.
- En formatvalidering som et sæt konfigurerbare regler, der styrer oprettelsen af rapporten på kørselstidspunktet afhængigt af kørselskonteksten. Eksempelvis kan der være en regel, der standser outputgenerering af en kreditors betalinger og medfører en undtagelse, når bestemte attributter for den valgte kreditor mangler, f.eks. bankkontonummeret.

En formatkomponent understøtter følgende funktioner:

- Oprettelse af rapporteringsoutput som separate filer i forskellige formater, f.eks. tekst, XML, Microsoft Word-dokument eller regneark.
- Separat oprettelse af flere filer og indkapsling af disse filer i zip-filer.

En formatkomponent gør det muligt at vedhæfte bestemte filer, der kan bruges i rapporteringsoutputtet:

- Excel-projektmapper, der indeholder et regneark, der kan bruges som skabelon for output i regnearksformat OPENXML:
- Word-filer, der indeholder et dokument, der kan bruges som skabelon for output i Microsoft Word-dokumentformatet
- Andre filer kan indgå i formatets output som foruddefinerede filer.

I følgende illustration vises, hvordan dataene flyder for disse formater.

[![Dataflow for udgående formatkomponenter.](./media/ER-overview-02.png)](./media/ER-overview-02.png)

For at køre en enkelt ER-formatkonfiguration og generere et udgående elektronisk dokument skal du identificere tilknytningen af formatkonfigurationen.

#### <a name="format-components-for-incoming-electronic-documents"></a><a name="FormatComponentInbound"></a>Formatkomponenter for indgående elektroniske dokumenter

En formatkomponent er skemaet for det indgående dokument, der importeres på kørselstidspunktet. Et skema består af følgende elementer:

- Et format, der definerer strukturen og indholdet af det indgående elektroniske dokument, som indeholder data, der importeres på kørselstidspunktet. En formatkomponent bruges til at fortolke et indgående dokument i forskellige formater, f.eks. tekst og XML.
- En formattilknytning, som binder individuelle formateringselementer til elementer i en domænespecifik datamodel. På kørselstidspunktet angiver elementerne i datamodellen dataflowet og reglerne for import af data fra et indgående dokument og gemmer derefter dataene i en datamodel.
- En formatvalidering som et sæt konfigurerbare regler, der styrer import af data på kørselstidspunktet afhængigt af kørselskonteksten. Eksempelvis kan der være en regel, der standser import af data fra et bankkontoudtog, der har en kreditors betalinger og medfører en undtagelse, når en bestemt kreditors attributter mangler, f.eks. kreditor-id-koden.

I følgende illustration vises, hvordan dataene flyder for disse formater.

[![Dataflow for indgående formatkomponenter.](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Hvis du vil køre en enkelt ER-formatkonfigurationen for at importere data fra et indgående elektronisk dokument, skal du identificere den ønskede tilknytning af en formatkonfiguration samt integrationspunktet for en modeltilknytning. Du kan bruge den samme modeltilknytning og de samme destinationer sammen med forskellige formater for forskellige typer indgående dokumenter.

#### <a name="component-versioning"></a>Komponentversioner

Versionering understøttes for ER-komponenter. Der findes følgende arbejdsgang til håndtering af ændringer i ER-komponenter:

1. Den oprindelige version, der blev oprettet, er markeret som en **Kladde**-version. Denne version kan redigeres og er tilgængelig for testkørsler.
2. **Kladde** versionen kan konverteres til en **Fuldført** version. Denne version kan bruges i lokale rapporteringsprocesser.
3. Versionen **Fuldført** kan konverteres til en **Delt** version. Denne version udgives på LCS og kan bruges i globale rapportingsprocesser.
4. Versionen **Delt** kan konverteres til en **Annulleret** version. Denne version kan derefter slettes.

Versioner, der har status som enten **Fuldført** eller **Delt** er tilgængelige for anden dataudveksling. Følgende handlinger kan udføres på en komponent, der har disse statusser:

- Komponenten kan serialiseres i XML-format og eksporteres som en fil i XML-format.
- Komponenten kan reserialiseres fra en XML-fil og importeres til programmet som en ny version af en ER-komponent.

#### <a name="component-date-effectivity"></a>Komponentens datogyldighed

ER-komponentversioner har en ikrafttrædelsesdato. Du kan indstille datoen **Gyldig fra** for en ER-komponent for at angive startdatoen, hvor komponenten træder i kraft for rapporteringsprocesser. Programsessionsdatoen bruges til at definere, om en komponent er gyldig til udførelse. Hvis mere end én version er gyldig for en bestemt dato, bruges den nyeste version til rapporteringsprocesser.

#### <a name="component-access"></a>Komponentadgang

Adgang til ER-formatkomponenter afhænger af indstilling af ISO-land/område-koden. Når denne indstilling er tom for en valgt version af en formatkonfiguration, kan en formatkomponent åbnes fra ethvert firma på kørselstidspunktet. Når denne indstilling indeholder ISO-land/område-koder, er en formatkomponent kun tilgængelig fra firmaer, der har en primær adresse, som er defineret for en af en formatkomponents ISO-land/område-koder.

Forskellige versioner af en dataformatkomponent kan have forskellige indstillinger for ISO-land/område-koder.

#### <a name="configuration"></a><a name="Configuration"></a>Konfiguration

En ER-konfiguration er wrapperen for en bestemt ER-komponent. Denne komponent kan enten være en datamodelkomponent eller en formatkomponent. En konfiguration kan omfatte forskellige versioner af en ER-komponent. Hver konfiguration er markeret som ejet af en bestemt konfigurationsudbyder. **Kladde**-versionen af en komponent i en konfiguration kan redigeres, når ejeren af konfigurationen er valgt som aktiv udbyder i ER-indstillingerne i programmet.

Hver modelkonfiguration indeholder en datamodelkomponent. En ny formatkonfiguration kan stamme fra en bestemt datamodelkonfiguration. I konfigurationstræet vises den formatkonfiguration, der oprettes, som underordnet til den oprindelige modeldatakonfiguration.

Den formatkonfiguration, der oprettes, indeholder en formatkomponent. Datamodelkomponenten for den oprindelige modelkonfiguration indsættes automatisk i formatkomponenten i den underordnede formatkonfiguration som en standarddatakilde.

En ER-konfiguration deles for firmaer i programmet.

#### <a name="provider"></a><a name="Provider"></a>Udbyder

ER-udbyderen er den partsidentifikator, der bruges til at angive forfatteren (ejeren) af hver ER-konfiguration. Med ER kan du administrere listen over udbydere af konfigurationen. Formatkonfigurationer, der frigives for elektroniske dokumenter som del af Finance and Operations-løsningen, markeres som ejet af **Microsoft**-konfigurationsudbyderen.

Du kan få oplysninger om, hvordan du registrerer en ny ER-udbyder, ved at afspille opgaveguiden **Oprette en ER-konfigurationsudbyder og markere den som aktiv** (en del af forretningsprocessen **7.5.4.3 Anskaf/udarbejd komponenter til it-ydelser og -løsninger (10677)**).

#### <a name="repository"></a><a name="Repository"></a>Lager

Et ER-lager indeholder ER-konfigurationer. Følgende typer af ER-lagre understøttes i øjeblikket: 

- Delt LCS-bibliotek
- LCS-projekt
- Filsystem
- RCS
- Operations-ressourcer
- Global lagermappe

Et **Delt LCS-bibliotek**-lager giver adgang til listen med konfigurationer i biblioteket for delte aktiver i Lifecycle Services (LCS). Denne type ER-lager kan alene registreres for Microsoft-udbydere. Fra LCS-biblioteket for delte aktiver kan du importere de seneste versioner af ER-konfigurationer til den aktuelle forekomst.

Et **LCS-projektlager** giver adgang til listen over konfigurationer af et bestemt LCS-projekt (LCS-projektets aktivbibliotek), der blev valgt, da lageret blev registreret. Med ER kan du overføre delte konfigurationer fra den aktuelle forekomst til et bestemt **LCS-projekt**-lager. Du kan også importere konfigurationer fra et **LCS-projekt**-lager til den aktuelle forekomst af dine Finance and Operations-apps.

Et **Filsystem**-lager giver adgang til listen over konfigurationer, der findes som XML-filer i den pågældende mappen på det lokale filsystem på den computer, der er vært for AOS-tjenesten. Den påkrævede mappe vælges på lagerregistreringsstadiet. Du kan importere konfigurationer fra et **Filsystem**-lager til den aktuelle forekomst. 

Bemærk, at denne lagertype er tilgængelig i følgende miljøer:

- Skybaserede miljøer, der er installeret til udviklingsformål (og som indeholder testmodeller af lukkede pakker)
- Lokalt installerede miljøer (på lokaliteten)

Du kan finde flere oplysninger under [Importer konfigurationer for elektronisk rapportering (ER)](./electronic-reporting-import-ger-configurations.md).

Et **RCS**-lager giver adgang til listen over konfigurationer af en bestemt forekomst af [Konfigurationstjeneste (RCS)](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration), der blev valgt på stadiet for lagerregistrering. Med ER kan du importere fuldførte eller delte konfigurationer fra den valgte RCS-forekomst til den aktuelle forekomst, hvor du kan anvende dem til elektronisk rapportering.

Du kan finde flere oplysninger under [Importere konfigurationer for elektronisk rapportering (ER) fra RCS](./rcs-download-configurations.md).

Et **Globalt lager** giver adgang til listen over konfigurationer i det globale lager i [Konfigurationstjenesten](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration). Denne type ER-lager kan alene registreres for Microsoft-udbydere. Fra det globale lager kan du importere de seneste versioner af ER-konfigurationer til den aktuelle forekomst.

Du kan finde flere oplysninger under [Importere konfigurationer af elektronisk rapportering (ER) fra det globale lager i konfigurationstjenesten](./er-download-configurations-global-repo.md).

Et lager med **Operationsressourcer** giver adgang til listen over de konfigurationer, som Microsoft, i kraft af sin rolle som ER-konfigurationsudbyder, indledningsvist frigiver som en del af programløsningen. Disse konfigurationer kan importeres til den aktuelle forekomst og anvendes til elektronisk rapportering eller afspilning af opgaveguider for stikprøver. De kan også bruges til flere sprogversioner og tilpasninger. Bemærk, at de nyeste versioner fra Microsoft ER-konfigurationer skal importeres fra LCS-biblioteket med delte aktiver ved hjælp af det tilsvarende ER-lager.

Påkrævede **LCS-projekt**-, **Filsystem**- og **Regulatory Configuration Services (RCS)**-lagre kan registreres individuelt for hver konfigurationsudbyder for den aktuelle forekomst. Hvert lager kan dedikeres til en bestemt konfigurationsudbyder.

## <a name="supported-scenarios"></a>Understøttede scenarier

### <a name="building-a-data-model"></a>Opbygning af en datamodel

ER leverer en modeldesigner, som du kan bruge til at bygge en datamodel for et bestemt virksomhedsdomæne. Alle domænespecifikke forretningsenheder og relationerne mellem dem kan præsenteres i en datamodel som en hierarkisk struktur. 

For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden **Design ER-domænespecifik datamodel** (som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**).

### <a name="translating-data-model-content"></a>Oversættelse af datamodelindhold

Datamodelindhold (navne og beskrivelser) kan oversættes til andre sprog, som programmet understøtter. Du kan oversætte datamodelindhold af følgende årsager:

- På designtidspunktet for at gøre indholdet mere forståeligt for formatdesignere, der taler andre sprog og som bruger datamodellen til datatilknytning af formatkomponenter.
- På kørselstidspunktet for at gøre indholdet mere brugervenligt ved at vise beskeder og hjælp til kørselsparametre samt konfigurerede valideringsmeddelelser (fejl og advarsler) på det sprog, som er det foretrukne for den bruger, der aktuelt er logget på.

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Konfiguration af datamodeltilknytninger for udgående dokumenter

ER indeholder en modeltilknytningsdesigner, så brugerne kan knytte datamodeller, de har designet, til bestemte programdatakilder. På baggrund af tilknytningen importeres dataene på kørselstidspunktet fra valgte datakilder til datamodellen. Datamodellen bruges derefter som en abstrakt datakilde til ER-formater, der genererer udgående elektroniske dokumenter. 

For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiderne **Definere ER-modeltilknytning, og vælg datakilder** og **ER Tilknyt datamodel til valgte datakilder** (del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**).

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Konfiguration af datamodeltilknytninger for indgående dokumenter

ER indeholder en modeltilknytningsdesigner, så brugerne kan knytte datamodeller, de har designet, til bestemte destinationer. For eksempel kan datamodeller knyttes til datakomponenter, der kan opdateres (tabeller, dataenheder og visninger). På baggrund af tilknytningen opdateres data på kørselstidspunktet ved hjælp af data fra datamodellen. Som abstrakt lagring af ER-formatet udfyldes datamodellen med data, der er importeret fra et indgående elektronisk dokument. 

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Lagring af en designet modelkomponent som en modelkonfiguration

ER kan gemme en designet datamodel sammen med tilknyttede datatilknytninger som en modelkonfiguration for den aktuelle forekomst. I følgende illustration vises et eksempel på denne type datamodelkonfiguration (betalingsdomæne-datakonfigurationen).

For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden **Tilknyt ER-datamodel til markerede datakilder** (som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Opbygning af et format, der bruger en datamodel som udgangspunkt

ER understøtter en formatdesigner, som du kan bruge til at bygge formatet for et elektronisk dokument for et valgt forretningsdomæne ved at vælge modelkomponenten som udgangspunkt. Med samme ER-formatdesigner kan du knytte et format, som du opretter, til et markeret domænes datamodeltilknytning som en datakilde. 

For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden **Design ER-domænespecifikt format** (som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Oprettelse af en konfiguration for at generere elektroniske dokumenter i OPENXML-regnearksformat

ER-formatdesigneren kan bruges til at oprette en elektronisk dokument i OPENXML-regnearksformat. 

For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden **ER Opret en konfiguration for rapporter i OPENXML-format** (som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**). Som en del af trinnet i opgaveguiden til import af en skabelon skal du bruge [Skabelon for betalingsrapport (SampleVendPaymWsReport.xlsx)](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx) Excel-filen som skabelon.

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Oprettelse af en konfiguration for at generere elektroniske dokumenter i et Word-dokumentformat

ER-formatdesigneren kan bruges til at oprette en elektronisk dokument i et Word-dokumentformat. I følgende illustration vises et eksempel på denne type format. Bemærk, at dette format genbruger den eksisterende ER-konfiguration, der oprindeligt blev udviklet til at generere rapporten i OPENXML-formatet.

For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden ER Design en konfiguration til oprettelse af rapporter i Microsoft WORD-format (som er en del af forretningsprocessen 7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)). Som en del af trinnet i opgaveguiden til import af en skabelon skal du bruge følgende Word-filer som skabeloner for ER-formatet:

- [Skabelon for betalingsrapport (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [Bundet skabelon for betalingsrapport (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Oprettelse af en konfiguration til import af data fra indgående elektroniske dokumenter

ER-formatdesigneren kan bruges til at beskrive et elektronisk dokument, der er planlagt til import af data i enten XML- eller tekstformat. Designerformatet bruges til at fortolke et indgående dokument. ER-designeren for formattilknytning kan bruges til at definere bindingen af elementerne i det designede format til datamodellen. 

For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden ER-konfigurationer for at importere data fra en ekstern fil (som er en del af forretningsprocessen 7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)). Du kan bruge følgende filer til at afspille denne guide:

- [Konfiguration af ER-datamodel (1099model.xml)](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)
- [ER-formatkonfiguration (1099format.xml)](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)
- [Eksempel på det indgående dokument i XML-format (1099entries.xml)](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)
- [Eksempel på projektmappen til håndtering af data til indgående dokument (1099entries.xlsx)](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Lagring af en designet formatkomponent i en formatkonfiguration

ER kan gemme et designet format sammen med de konfigurerede datatilknytninger som en formatkonfiguration for den aktuelle forekomst. Ovenstående illustration viser et eksempel på denne type formatkonfiguration (**BACS (UK)**, som er underordnet i forhold til **Betalingsmodel**-konfigurationen). For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden **Design ER-domænespecifikt format** (som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**).

### <a name="configuring-finance-to-start-to-use-a-created-format-internally"></a>Konfiguration af Finans for at begynde at bruge et oprettet format internt

Programmet kan konfigureres til at begynde at bruge et oprettet format til generering af elektroniske rapporter. Referencen til den oprettede formatkonfigurationen bør fastlægges i indstillingerne for et bestemt domæne. For eksempel for at begynde at bruge en ER-formatkonfiguration for elektroniske kreditorbetalinger i BACS format, skal der refereres til formatkonfigurationen i bestemte betalingsmåder.

For at blive fortrolig med detaljerne i dette scenarie skal du afspille **ER Brug format til at generere elektronisk dokument til betalinger** (del af forretningsprocessen **7.5.4.3 Anskaffe/udvikle IT-tjeneste/løsningskomponenter (10677)**).

## <a name="handling-er-components"></a>Håndtering af ER-komponenter

### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Udgive en ER-komponent i LCS for at tilbyde den eksternt (lokalisering)

Ejeren af en komponent (model eller format), der er oprettet, kan bruge ER til udgivelse af den færdige version af en ER-komponenten til LCS. Et lager af typen **LCS-projekt** for den aktuelle ER-konfigurationsudbyder er nødvendigt. Når statussen for den færdige version af en komponent er ændret fra **FULDFØRT** til **DELT**, udgives denne version LCS. Når en komponent er udgivet til LCS, bliver ejeren af denne komponent en udbyder af tjenesten til at understøtte komponenten. Hvis formatkomponenten f.eks. er designet til at generere et elektronisk dokument, der er juridisk påkrævet (f.eks. i henhold til et lokaliseringsscenarie), antages det, at formatet fortsat er kompatibelt med lovgivningsmæssige ændringer, og at udbyderen vil udsende nye versioner af komponenten, hver gang der kommer nye lovgivningsmæssige krav. For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden **Overføre ER-konfiguration til Lifecycle Services** (som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**).

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Importere ER-komponent fra LCS for at bruge det internt

Med ER kan du importere ER-komponenter fra LCS til den aktuelle forekomst. Et lager af typen **LCS-projekt** er påkrævet. Når en ER-komponent er blevet importeret fra LCS til den aktuelle forekomst, bliver ejeren af forekomsten forbrugeren af tjenesten, som angives af ejeren (forfatteren) af den importerede komponent. Hvis en formatkomponent f.eks. er designet til at generere et bestemt elektronisk dokument fra programmet i et land/område-specifikt format (lokaliseringsscenarie), antages det, at forbrugeren af tjenesten kan få de opdateringer, der udføres af dette format, for at holde det kompatibelt med lovmæssige krav. For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden **ER-import af en konfiguration fra Lifecycle Services** (som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**).

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Opbygge et format ved at vælge et andet format som udgangspunkt (tilpasning)

Med ER kan du oprette (aflede) en ny komponent fra den aktuelle version af en komponent (basis), der er importeret fra LCS. For eksempel ønsker en bruger at aflede et nyt format for at implementere nogle særlige krav til et elektronisk dokument (f.eks. et ekstra felt eller en omfattende beskrivelse) til understøttelse af et tilpasningsscenario. For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgavevejledningen **ER Opgrader format ved at implementere en ny basisversion af det** (del af **7.5.4.3 Anskaffe/udvikle IT-tjeneste/løsningskomponenter (10677)** for forretningsproces).

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Opgradering af et format ved at vælge en ny version af basisformat (rebasere)

Med ER kan du automatisk implementere ændringer af den nyeste version af basiskomponenten i den aktuelle kladdeversion af den afledte komponent. Denne proces kaldes *rebasering*. F.eks. kan en ny lovmæssig ændring, der er indført i den nyeste version af formatet, der blev importeret fra LCS, automatisk flettes med den tilpassede version af dette format af det elektroniske dokument. Ændringerne, der ikke kan flettes automatisk, anses for konflikter. Disse konflikter præsenteres for manuel løsning i designerværktøjet for den pågældende komponent. For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgavevejledningen **ER Opgrader format ved at implementere en ny basisversion af formatet** (del af forretningsprocessen **7.5.5.3 Anskaffe/udvikle ændret IT-tjeneste/løsningskomponent (10683)**).

## <a name="list-of-er-configurations-that-have-been-released-in-finance"></a><a name="list-of-configurations"></a>Liste over ER-konfigurationer, der er frigivet i Finans

Listen over ER-konfigurationer for Finans opdateres konstant. Åbn det [globale lager](er-download-configurations-global-repo.md) for at gennemgå listen over ER-konfigurationer, der understøttes i øjeblikket. I oversigtspanelet **Oplysninger om ophør** kan du gennemse oplysninger om konfigurationer, der er ophørt, eller som ikke længere vedligeholdes. 

![Indhold af globalt lager på siden Konfigurationslager.](./media/er-overview-03.gif)

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oprette en konfiguration af elektronisk rapportering (ER)](electronic-reporting-configuration.md)
- [Administrere livscyklus for konfigurationen af elektronisk rapportering (ER)](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
