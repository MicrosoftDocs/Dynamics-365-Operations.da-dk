---
title: Elektronisk rapportering (ER)
description: "Dette emne indeholder en oversigt over værktøjet Elektronisk rapportering (ER). Den indeholder oplysninger om centrale koncepter, de scenarier, som ER understøtter, samt en liste over formater, der er designet og udgivet som del af løsningen."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: a271887c4d2cfe4d0ee6518482dc4ebe407ebe56
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---

# <a name="electronic-reporting-er"></a>Elektronisk rapportering (ER)

[!include [banner](../includes/banner.md)]

Dette emne indeholder en oversigt over værktøjet Elektronisk rapportering (ER). Den indeholder oplysninger om centrale koncepter, de scenarier, som ER understøtter, samt en liste over formater, der er designet og udgivet som del af løsningen.

ER er et værktøj, du kan bruge til at konfigurere formater for både indgående og udgående elektroniske dokumenter i overensstemmelse med de lovgivningsmæssige krav i forskellige lande. Med ER du administrere disse formater i løbet af deres livscyklus. For eksempel kan du overholde nye lovgivningsmæssige krav og oprette forretningsdokumenter i det krævede format for at udveksle oplysninger elektronisk med offentlige myndigheder, banker og andre parter.

ER-programmet henvender sig til virksomhedsbrugere i stedet for udviklere. Da du konfigurerer formater frem for kode, udføres processer til oprettelse og tilpasning af formater for elektroniske dokumenter hurtigere og nemmere.

ER understøtter i øjeblikket regnearksformaterne TEXT, XML, OPENXML og Microsoft Word-dokument. Men der er mulighed for understøttelse af flere formater.

## <a name="capabilities"></a>Egenskaber
ER-programmet har følgende funktioner:

- Det repræsenterer et enkelt delt værktøj til elektronisk indberetning i forskellige domæner og erstatter mere end 20 forskellige programmer, der foretager en eller anden form for elektronisk rapportering i Microsoft Dynamics 365 for Finance and Operations.
- Det isolerer en rapports format fra den aktuelle Dynamics 365 for Finance and Operations-implementering. Med andre ord kan formatet anvendes i forskellige versioner af Microsoft Dynamics 365 for Finance and Operations.
- Det understøtter oprettelse af et brugerdefineret format, der er baseret på et oprindeligt format. Det indeholder også funktioner til automatisk at opgradere det tilpassede format, når det oprindelige format ændres pga. lokaliserings-/tilpasningskrav.
- Det bliver det primære standardværktøj til understøttelse af lokaliseringskrav i forbindelse med elektronisk rapportering, for både Microsoft og MS-partnere.
- Det understøtter muligheden for at distribuere formater til partnere og debitorer via Microsoft Dynamics Lifecycle Services (LCS).

## <a name="key-concepts"></a>Nøglebegreber
### <a name="components"></a>Komponenter

ER understøtter to komponenttyper: **Datamodel** og **Format**.

#### <a name="data-model-components"></a>Datamodelkomponenter

En datamodelkomponent er en abstrakt repræsentation af en datastruktur. Den bruges til at beskrive et bestemt forretningsdomæneområde, der er tilstrækkeligt detaljeret til at opfylde kravene til rapportering for det pågældende domæne. En data modelkomponent består af følgende dele:

- En datamodel som et sæt af domænespecifikke forretningsenheder samt en hierarkisk struktureret definition af relationerne mellem enhederne.
- En modeltilknytning, som sammenkæder valgte Dynamics 365 for Finance and Operations-datakilder med enkelte elementer i en datamodel, der under kørsel angiver dataflow og regler for forretningsdatapopulation til en datamodelkomponent.

En forretningsenhed af en datamodel er repræsenteret som en beholder (post). Egenskaber for forretningsenheden er repræsenteret som dataelementer (felter). Hvert dataelement har et entydigt navn, etiket, beskrivelse og værdi. Værdien af hvert dataelement kan være udformet, så den kan genkendes som en streng, heltal, reelt tal, dato, fasttekst, boolesk osv. Desuden kan det være en anden post eller postliste.

En enkelt modelkomponent kan indeholde flere hierarkier af domænespecifikke forretningsobjekter. Den kan også indeholde modeltilknytninger, der understøtter et rapportspecifikt dataflow på kørselstidspunktet. Hierarkierne afpasses efter en enkelt post, der er valgt som en rod for modeltilknytningen. Datamodellen for betalingsdomæneområdet kan f.eks. understøtte følgende tilknytninger:

- Virksomhed > Kreditor > Betalingstransaktioner for AP-domænet
- Debitor > Virksomhed > Betalingstransaktioner for AR-domænet

Bemærk forretningsenheder som f.eks firma- og betalingsposteringer angives én gang. Forskellige tilknytninger genbruger dem.

En modeltilknytning, der understøtter udgående elektroniske dokumenter, har følgende muligheder:

- Den kan bruge forskellige Dynamics 365 for Finance and Operations-datatyper som datakilder til en datamodel. Den kan for eksempel bruge tabeller, dataenheder, metoder eller fasttekster.
- Den understøtter brugerinputparametre, der kan defineres som datakilder for en datamodel, når data skal angives på kørselstidspunktet.
- Den understøtter transformationen af Dynamics 365 for Finance and Operations-data til de grupper, der kræves. Den gør det også muligt at filtrere, sortere og summere data og tilføje logisk beregnede felter, der er designet via formler, der ligner Microsoft Excel-formler, som vist i følgende illustration. Du kan finde flere oplysninger under [Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md).

[![Formeldesigner](./media/ER-overview-01.png)](./media/ER-overview-01.png) 

En modeltilknytning, der understøtter indgående elektroniske dokumenter, har følgende muligheder:

- Det kan bruge forskellige opdaterbare dataelementer som mål. Disse dataelementer omfatter tabeller, dataenheder og visninger. Dataene kan opdateres ved hjælp af dataene fra de indgående elektroniske dokumenter. Der kan bruges flere destinationer i en enkelt modeltilknytning.
- Den understøtter brugerinputparametre, der kan defineres som datakilder for en datamodel, når data skal angives på kørselstidspunktet.

Der udvikles en datamodelkomponent til hvert forretningsdomæne, der skal bruges som en samlet datakilde til rapportering, der isolerer rapportering fra den fysiske implementering af datakilder. Den repræsenterer domænespecifikke forretningsbegreber og -funktioner i en formular, der gør et rapporteringsformats oprindelige design og yderligere vedligeholdelse mere effektivt.

#### <a name="format-components-for-outgoing-electronic-documents"></a>Formatkomponenter for udgående elektroniske dokumenter

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
- Word-filer, der indeholder et dokument, der kan bruges som skabelon for output i Microsoft Word-dokument-formatet
- Andre filer kan indgå i formatets output som foruddefinerede filer.

I følgende illustration vises, hvordan dataene flyder for disse formater.

[![Dataflow for udgående formatkomponenter](./media/ER-overview-02.png)](./media/ER-overview-02.png)

For at køre en enkelt ER-formatkonfiguration og generere et udgående elektronisk dokument skal du identificere tilknytningen af formatkonfigurationen.

#### <a name="format-components-for-incoming-electronic-documents"></a>Formatkomponenter for indgående elektroniske dokumenter
En formatkomponent er skemaet for det indgående dokument, der importeres på kørselstidspunktet. Et skema består af følgende elementer:

- Et format, der definerer strukturen og indholdet af det indgående elektroniske dokument, som indeholder data, der importeres på kørselstidspunktet. En formatkomponent bruges til at fortolke et indgående dokument i forskellige formater, f.eks. tekst og XML.
- En formattilknytning, som binder individuelle formateringselementer til elementer i en domænespecifik datamodel. På kørselstidspunktet angiver elementerne i datamodellen dataflowet og reglerne for import af data fra et indgående dokument og gemmer derefter dataene i en datamodel.
- En formatvalidering som et sæt konfigurerbare regler, der styrer import af data på kørselstidspunktet afhængigt af kørselskonteksten. Eksempelvis kan der være en regel, der standser import af data fra et bankkontoudtog, der har en kreditors betalinger og medfører en undtagelse, når en bestemt kreditors attributter mangler, f.eks. kreditor-id-koden.

I følgende illustration vises, hvordan dataene flyder for disse formater.

[![Dataflow for indgående formatkomponenter](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Hvis du vil køre en enkelt ER-formatkonfigurationen for at importere data fra et indgående elektronisk dokument, skal du identificere den ønskede tilknytning af en formatkonfiguration samt integrationspunktet for en modeltilknytning. Du kan bruge den samme modeltilknytning og de samme destinationer sammen med forskellige formater for forskellige typer indgående dokumenter.

#### <a name="component-versioning"></a>Komponentversioner

Versionering understøttes for ER-komponenter. Der findes følgende arbejdsgang til håndtering af ændringer i ER-komponenter:

1. Den oprindelige version, der blev oprettet, er markeret som en **Kladde**-version. Denne version kan redigeres og er tilgængelig for testkørsler.
2. **Kladde** versionen kan konverteres til en **Fuldført** version. Denne version kan bruges i lokale rapporteringsprocesser.
3. Versionen **Fuldført** kan konverteres til en **Delt** version. Denne version udgives på LCS og kan bruges i globale rapportingsprocesser.
4. Versionen **Delt** kan konverteres til en **Annulleret** version. Denne version kan derefter slettes.

Versioner, der har status som enten **Fuldført** eller **Delt** er tilgængelige for anden dataudveksling. Følgende handlinger kan udføres på en komponent, der har disse statusser:

- Komponenten kan serialiseres i XML-format og eksporteres som en fil i XML-format.
- Komponenten kan reserialiseres fra en XML-fil og importeres til Dynamics 365 for Finance and Operations som en ny version af en ER-komponent.

#### <a name="component-date-effectivity"></a>Komponentens datogyldighed

ER-komponentversioner har en ikrafttrædelsesdato. Du kan indstille datoen **Gyldig fra** for en ER-komponent for at angive startdatoen, hvor komponenten træder i kraft for rapporteringsprocesser. Finance and Operations-sessionsdatoen bruges til at definere, om en komponent er gyldig til udførelse. Hvis mere end én version er gyldig for en bestemt dato, bruges den nyeste version til rapporteringsprocesser.

#### <a name="component-access"></a>Komponentadgang

Adgang til ER-formatkomponenter afhænger af indstilling af ISO-lande/områdekoden. Når denne indstilling er tom for en valgt version af en formatkonfiguration, kan en formatkomponent åbnes fra ethvert firma på kørselstidspunktet. Når denne indstilling indeholder ISO-lande/områdekoder, er en formatkomponent kun tilgængelig fra firmaer, der har en primær adresse, som er defineret for en af en formatkomponents ISO-lande/områdekoder.

Forskellige versioner af en dataformatkomponent kan have forskellige indstillinger for ISO-lande/områdekoder.

#### <a name="configuration"></a>Konfiguration

En ER-konfiguration er wrapperen for en bestemt ER-komponent. Denne komponent kan enten være en datamodelkomponent eller en formatkomponent. En konfiguration kan omfatte forskellige versioner af en ER-komponent. Hver konfiguration er markeret som ejet af en bestemt konfigurationsudbyder. Versionen **Kladde** af en komponent i en konfiguration kan redigeres, når ejeren af konfigurationen er valgt som aktiv udbyder i ER-indstillingerne i Finance and Operations.

Hver modelkonfiguration indeholder en datamodelkomponent. En ny formatkonfiguration kan stamme fra en bestemt datamodelkonfiguration. I konfigurationstræet vises den formatkonfiguration, der oprettes, som underordnet til den oprindelige modeldatakonfiguration.

Den formatkonfiguration, der oprettes, indeholder en formatkomponent. Datamodelkomponenten for den oprindelige modelkonfiguration indsættes automatisk i formatkomponenten i den underordnede formatkonfiguration som en standarddatakilde.

En ER-konfiguration deles for Finance and Operations-firmaer.

#### <a name="provider"></a>Udbyder

ER-udbyderen er den partsidentifikator, der bruges til at angive forfatteren (ejeren) af hver ER-konfiguration. Med ER kan du administrere listen over udbydere af konfigurationen. Formatkonfigurationer, der frigives for elektroniske dokumenter som del af Finance and Operations-løsningen, markeres som ejet af **Microsoft**-konfigurationsudbyderen.

Du kan få oplysninger om, hvordan du registrerer en ny ER-udbyder, ved at afspille opgaveguiden **Oprette en ER-konfigurationsudbyder og markere den som aktiv** (en del af forretningsprocessen **7.5.4.3 Anskaf/udarbejd komponenter til it-ydelser og -løsninger (10677)**).

#### <a name="repository"></a>Lager

Et ER-lager indeholder ER-konfigurationer. To typer ER lagre understøttes i øjeblikket: **Operations-ressourcer** og **LCS-projekt**.

Et **Operations-ressourcer**-lager giver adgang til listen over de konfigurationer, som Microsoft som ER-konfigurationsudbyder frigiver som en del af Finance and Operations-løsningen. Disse konfigurationer kan importeres til den aktuelle forekomst af Finance and Operations og bruges til elektronisk indberetning. De kan også bruges til flere sprogversioner og tilpasninger.

Et **LCS-projektlager** giver adgang til listen over konfigurationer af et LCS-projekt (LCS-projektets aktivbibliotek), der blev valgt på stadiet for lagerregistrering. Med ER kan du overføre delte konfigurationer fra den aktuelle Finance and Operations-forekomst til et bestemt **LCS-projekt**-lager. Du kan også importere konfigurationer fra et **LCS-projekt**-lager til den aktuelle Finance and Operations-forekomst.

Påkrævede **LCS-projektlagre** kan registreres individuelt for hver konfigurationsudbyder for den aktuelle forekomst af Finance and Operations. Hvert lager kan dedikeres til en bestemt konfigurationsudbyder.

## <a name="supported-scenarios"></a>Understøttede scenarier
### <a name="building-a-data-model"></a>Opbygning af en datamodel

ER leverer en modeldesigner, som du kan bruge til at bygge en datamodel for et bestemt virksomhedsdomæne. Alle domænespecifikke forretningsenheder og relationerne mellem dem kan præsenteres i en datamodel som en hierarkisk struktur. I følgende illustration vises et eksempel på denne type datamodel (betalingsdomæne-datamodellen). 

[![Datamodel for betalingsdomæne](./media/ER-overview-04.png)](./media/ER-overview-04.png)

For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden **Design ER-domænespecifik datamodel** (som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**).

### <a name="translating-data-model-content"></a>Oversættelse af datamodelindhold

Datamodelindhold (etiketter og beskrivelser) kan oversættes til andre sprog, som Dynamics 365 for Finance and Operations understøtter. Du kan oversætte datamodelindhold af følgende årsager:

-   På designtidspunktet for at gøre indholdet mere forståeligt for formatdesignere, der taler andre sprog og som bruger datamodellen til datatilknytning af formatkomponenter.
-   På kørselstidspunktet for at gøre indholdet mere brugervenligt ved at vise beskeder og hjælp til kørselsparametre samt konfigurerede valideringsmeddelelser (fejl og advarsler) på det sprog, som er det foretrukne for den bruger, der aktuelt er logget på.

I følgende illustration vises et eksempel på, hvor datamodelindhold oversættes fra engelsk til japansk. 

[![Datamodelindhold på engelsk](./media/ER-overview-05.png)](./media/ER-overview-05.png)

[![Datamodelindhold oversat til japansk](./media/ER-overview-06.png)](./media/ER-overview-06.png)


### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Konfiguration af datamodeltilknytninger for udgående dokumenter

ER indeholder en modeltilknytningsdesigner, så brugerne kan knytte datamodeller, de har designet, til bestemte datakilder i Dynamics 365 for Finance and Operations. På baggrund af tilknytningen importeres dataene på kørselstidspunktet fra valgte datakilder til datamodellen. Datamodellen bruges derefter som en abstrakt datakilde til ER-formater, der genererer udgående elektroniske dokumenter. I følgende illustration vises et eksempel på denne type datamodeltilknytning vises i nedenstående billede (**SEPA-overførsel**-modeltilknytningen i datamodellen for betalingsdomæne). 

[![Eksempel på en datamodeltilknytning](./media/ER-overview-07.png)](./media/ER-overview-07.png)

For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiderne **Definere ER-modeltilknytning, og vælg datakilder** og **ER Tilknyt datamodel til valgte datakilder** (del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**).

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Konfiguration af datamodeltilknytninger for indgående dokumenter
ER indeholder en modeltilknytningsdesigner, så brugerne kan knytte datamodeller, de har designet, til bestemte destinationer. For eksempel kan datamodeller knyttes til datakomponenter i Finance and Operations, der kan opdateres (tabeller, dataenheder og visninger). På baggrund af tilknytningen opdateres Finance and Operations-data på kørselstidspunktet ved hjælp af data fra datamodellen. Som abstrakt lagring af ER-formatet udfyldes datamodellen med data, der er importeret fra et indgående elektronisk dokument. I følgende illustration vises et eksempel på denne type datamodeltilknytning. I dette eksempel bruges **Importér tilknytning for NETS**-modeltilknytningen af datamodellen for betalingsdomænet til at understøtte import af bankkontoudtog i NETS-bankformatet for Norge.

[![Importere tilknytning for NETS-datamodeleksempel](./media/ER-overview-08.png)](./media/ER-overview-08.png)

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Lagring af en designet modelkomponent som en modelkonfiguration

ER kan gemme en designet datamodel med sammen tilknyttede datatilknytninger som en modelkonfiguration for den aktuelle forekomst af Finance and Operations. I følgende illustration vises et eksempel på denne type datamodelkonfiguration (betalingsdomæne-datakonfigurationen). 

For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden **Tilknyt ER-datamodel til markerede datakilder** (som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Opbygning af et format, der bruger en datamodel som udgangspunkt

ER understøtter en formatdesigner, som du kan bruge til at bygge formatet for et elektronisk dokument for et valgt forretningsdomæne ved at vælge modelkomponenten som udgangspunkt. Med samme ER-formatdesigner kan du knytte et format, som du opretter, til et markeret domænes datamodeltilknytning som en datakilde. I følgende illustration vises et eksempel på denne type format (den formatkonfiguration, der understøtter **BACS**-betalingsformatet for Storbritannien). 

[![Eksempel på et format, der har en datamodel som udgangspunkt](./media/ER-overview-09.png)](./media/ER-overview-09.png)

For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden **Design ER-domænespecifikt format** (som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Oprettelse af en konfiguration for at generere elektroniske dokumenter i OPENXML-regnearksformat

ER-formatdesigneren kan bruges til at oprette en elektronisk dokument i OPENXML-regnearksformat. I følgende illustration vises et eksempel på denne type format (en formatkonfiguration til at generere OPENXML-regneark med oplysninger om en valgt betalingskladde).

[![Pic-ER-format-Excel](./media/ER-overview-10.png)](./media/ER-overview-10.png)

For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden **ER Opret en konfiguration for rapporter i OPENXML-format** (som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**). Som en del af trinnet i opgaveguiden til import af en skabelon skal du bruge [Skabelon for betalingsrapport (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202) Excel-filen som skabelon.

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Oprettelse af en konfiguration for at generere elektroniske dokumenter i et Word-dokumentformat
ER-formatdesigneren kan bruges til at oprette en elektronisk dokument i et Word-dokumentformat. I følgende illustration vises et eksempel på denne type format. Bemærk, at dette format genbruger den eksisterende ER-konfiguration, der oprindeligt blev udviklet til at generere rapporten i OPENXML-formatet.

[![Pic-ER-format-Word](./media/ER-overview-11.png)](./media/ER-overview-11.png)

For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden ER Design en konfiguration til oprettelse af rapporter i Microsoft WORD-format (som er en del af forretningsprocessen 7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)). Som en del af trinnet i opgaveguiden til import af en skabelon skal du bruge følgende Word-filer som skabeloner for ER-formatet:

- [Skabelon for betalingsrapport (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Bundet skabelon for betalingsrapport (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Oprettelse af en konfiguration til import af data fra indgående elektroniske dokumenter  
ER-formatdesigneren kan bruges til at beskrive et elektronisk dokument, der er planlagt til import af data i enten XML- eller tekstformat. Designerformatet bruges til at fortolke et indgående dokument. ER-designeren for formattilknytning kan bruges til at definere bindingen af elementerne i det designede format til datamodellen. I følgende illustration vises et eksempel på denne type format og formattilknytning. I dette eksempel importeres NETS-bankkontoudtog, som indeholder oplysninger om kreditorbetalinger i tekstformat.

[![ER-format-designer](./media/ER-overview-12.png)](./media/ER-overview-12.png)

[![ER-model-mapping-designer](./media/ER-overview-13.png)](./media/ER-overview-13.png)

For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden ER-konfigurationer for at importere data fra en ekstern fil (som er en del af forretningsprocessen 7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)). Du kan bruge følgende filer til at afspille denne guide:

- [Konfiguration af ER-datamodel (1099model.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [ER-formatkonfiguration (1099format.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Eksempel på det indgående dokument i XML-format (1099entries.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Eksempel på projektmappen til håndtering af data til indgående dokument (1099entries.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Lagring af en designet formatkomponent i en formatkonfiguration

ER kan gemme en designet format sammen med de konfigurerede datatilknytninger som en formatkonfiguration for den aktuelle forekomst af Dynamics 365 for Finance and Operations. Ovenstående illustration viser et eksempel på denne type formatkonfiguration (**BACS (UK)**, som er underordnet i forhold til **Betalingsmodel**-konfigurationen). For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden **Design ER-domænespecifikt format** (som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**).

### <a name="configuring-finance-and-operations-to-start-to-use-a-created-format-internally"></a>Konfiguration af Finance and Operations for at begynde at bruge et oprettet format internt

Finance and Operations kan konfigureres til at begynde at bruge et oprettet format til generering af elektroniske rapporter. Referencen til den oprettede formatkonfigurationen bør fastlægges i indstillingerne for et bestemt domæne. For eksempel for at begynde at bruge en ER-formatkonfiguration for elektroniske kreditorbetalinger i BACS format, skal der refereres til formatkonfigurationen i bestemte betalingsmåder, som vist i følgende illustrationer: 

[![BACS (UK) formatkonfiguration](./media/ER-overview-14.png)](./media/ER-overview-14.png)

[![Referencer til formatet BACS (UK) i en betalingsmetode](./media/ER-overview-15.png)](./media/ER-overview-15.png)

For at blive fortrolig med detaljerne i dette scenarie skal du afspille **ER Brug format til at generere elektronisk dokument til betalinger** (del af forretningsprocessen **7.5.4.3 Anskaffe/udvikle IT-tjeneste/løsningskomponenter (10677)**).

## <a name="handling-er-components"></a>Håndtering af ER-komponenter
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Udgive en ER-komponent i LCS for at tilbyde den eksternt (lokalisering)

Ejeren af en komponent (model eller format), der er oprettet, kan bruge ER til udgivelse af den færdige version af en ER-komponenten til LCS. Et lager af typen **LCS-projekt** for den aktuelle ER-konfigurationsudbyder er nødvendigt. Når statussen for den færdige version af en komponent er ændret fra **FULDFØRT** til **DELT**, udgives denne version LCS. Når en komponent er udgivet til LCS, bliver ejeren af denne komponent en udbyder af tjenesten til at understøtte komponenten. Hvis formatkomponenten f.eks. er designet til at generere et elektronisk dokument, der er juridisk påkrævet (f.eks. i henhold til et lokaliseringsscenarie), antages det, at formatet fortsat er kompatibelt med lovgivningsmæssige ændringer, og at udbyderen vil udsende nye versioner af komponenten, hver gang der kommer nye lovgivningsmæssige krav. For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden **Overføre ER-konfiguration til Lifecycle Services** (som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**).

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Importere ER-komponent fra LCS for at bruge det internt

Med ER kan du importere ER komponenter fra LCS til den aktuelle forekomst af Finance and Operations. Et lager af typen **LCS-projekt** er påkrævet. Når en ER-komponent er blevet importeret fra LCS til den aktuelle forekomst af Finance and Operations, bliver ejeren af forekomsten forbrugeren af tjenesten, som leveres af ejeren (forfatteren) af den importerede komponent. Hvis en formatkomponent f.eks. er designet til at generere et bestemt elektronisk dokument fra Finance and Operations i et land/områdespecifikt format (lokaliseringsscenarie), antages det, at forbrugeren af tjenesten kan få de opdateringer, der udføres af dette format, for at holde det kompatibelt med lovmæssige krav. For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgaveguiden **ER-import af en konfiguration fra Lifecycle Services** (som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**).

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Opbygge et format ved at vælge et andet format som udgangspunkt (tilpasning)

Med ER kan du oprette (aflede) en ny komponent fra den aktuelle version af en komponent (basis), der er importeret fra LCS. For eksempel ønsker en bruger at aflede et nyt format for at implementere nogle særlige krav til et elektronisk dokument (f.eks. et ekstra felt eller en omfattende beskrivelse) til understøttelse af et tilpasningsscenario. For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgavevejledningen **ER Opgrader format ved at implementere en ny basisversion af det** (del af **7.5.4.3 Anskaffe/udvikle IT-tjeneste/løsningskomponenter (10677)** for forretningsproces).

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Opgradering af et format ved at vælge en ny version af basisformat (rebasere)

Med ER kan du automatisk implementere ændringer af den nyeste version af basiskomponenten i den aktuelle kladdeversion af den afledte komponent. Denne proces kaldes *rebasering*. F.eks. kan en ny lovmæssig ændring, der er indført i den nyeste version af formatet, der blev importeret fra LCS, automatisk flettes med den tilpassede version af dette format af det elektroniske dokument. Ændringerne, der ikke kan flettes automatisk, anses for konflikter. Disse konflikter præsenteres for manuel løsning i designerværktøjet for den pågældende komponent. For at blive fortrolig med detaljerne i dette scenarie skal du afspille opgavevejledningen **ER Opgrader format ved at implementere en ny basisversion af formatet** (del af forretningsprocessen **7.5.5.3 Anskaffe/udvikle ændret IT-tjeneste/løsningskomponent (10683)**).

## <a name="list-of-er-configurations-that-are-delivered-in-the-finance-and-operations-solution"></a>Oversigt over ER-konfigurationer, der leveres i Finance and Operations-løsningen

| Domænespecifikke datamodelkonfigurationer: titel | Domæne                | Datamodel-afhængige formatkonfigurationer: titel | Beskrivelse                                                        |
|--------------------------------------------------|-----------------------|---------------------------------------------------|--------------------------------------------------------------------|
| Revisionsfilmodel                                 | Finansiel revision       |                                                   |                                                                    |
|                                                  |                       | Revisionsfil (NL)                                   | Revisionsfilformat for Nederlandene                                  |
| BAS-model                                        | Momsrapportering         |                                                   |                                                                    |
|                                                  |                       | BAS (AU)                                          | BAS-format for Australien                                           |
| Skemamodel til konstruktionsbranchen               | Momsrapportering         |                                                   |                                                                    |
|                                                  |                       | CIS månedlig returnering (UK)                           | CIS månedligt returformat for Storbritannien                   |
| Rykkermodel                          | Elektronisk fakturering  |                                                   |                                                                    |
|                                                  |                       | OIOUBL-rykker (DK)                     | OIOUBL-rykkerformat for Danmark                        |
| Elektronisk finansregnskabsmodel (MX)          | Momsrapportering         |                                                   |                                                                    |
|                                                  |                       | Supplerende finans-XML (MX)                         | Supplerende finanstransaktioner pr. kontorapportformat for Mexico |
|                                                  |                       | Kontoplan XML (MX)                         | Diagram over kontorapportformat for Mexico                          |
|                                                  |                       | Kladder XML (MX)                                 | Kladdeposteringsrapportformat for Mexico                      |
|                                                  |                       | Råbalance XML (MX)                            | Råbalance-rapportformat for Mexico                             |
| Elster-model                                     | Momsrapportering         |                                                   |                                                                    |
|                                                  |                       | Elster (DE)                                       | Elster-format for Tyskland                                          |
| EU-listesystemmodel                              | Handelsrapportering       |                                                   |                                                                    |
|                                                  |                       | EU-listesystem (DE)                                | EU-listesystem, TXT-format for Tyskland                               |
|                                                  |                       | EU-listesystem (DK)                                | EU-listesystem, TXT-format for Danmark                               |
|                                                  |                       | EU-listesystem (FR)                                | EU-listesystem, XML-format for Frankrig                                |
|                                                  |                       | EU-listesystem (NL)                                | EU-listesystem, XML-format for Nederlandene                           |
|                                                  |                       | EU-listesystem TXT (UK)                            | EU-listesystemet, TXT-format for Storbritannien                    |
|                                                  |                       | EU-listesystem XML (UK)                            | EU-listesystemet, XML-format for Storbritannien                    |
|                                                  |                       | Rapport for EU-listesystem efter kolonne                   | Rapport for EU-listesystem efter kolonne                                    |
|                                                  |                       | Rapport over EU-listesystem efter rækker                      | Rapport over EU-listesystem efter rækker                                       |
| FEC regnskabsmodel (FR)                        | Momsrapportering         |                                                   |                                                                    |
|                                                  |                       | FEC-regnskabsdata XML (FR)                      | XML-format for eksport af FEC regnskabsdata for Frankrig                   |
| Tysk revisionsfil                                | Finansiel revision       |                                                   |                                                                    |
|                                                  |                       | Output af tysk revisionsfil                          | Output af revisionsfil for Tyskland og Østrig                          |
| Intrastat-modul                                  | Handelsrapportering       |                                                   |                                                                    |
|                                                  |                       | Intrastat (DE)                                    | Intrastat-format for Tyskland                                       |
|                                                  |                       | Intrastat (DK)                                    | Intrastat-format for Danmark                                       |
|                                                  |                       | Intrastat INTRACOM (FR)                           | Intrastat INTRACOM-format for Frankrig                               |
|                                                  |                       | Intrastat SAISUNIC (FR)                           | Intrastat SAISUNIC-format for Frankrig                               |
|                                                  |                       | Intrastat (NL)                                    | Intrastat-format for Nederlandene                               |
|                                                  |                       | Intrastat (UK)                                    | Intrastat-format for Storbritannien                            |
|                                                  |                       | Intrastat-rapport                                  | Intrastat Excel-kontrolrapport                                     |
| Debitorfakturamodel                           | Elektronisk fakturering  |                                                   |                                                                    |
|                                                  |                       | OIOUBL projektkreditnota (DK)                   | OIOUBL format for projektkreditnota for Danmark                      |
|                                                  |                       | OIOUBL projektfaktura (DK)                       | OIOUBL format for projektfaktura for Danmark                          |
|                                                  |                       | OIOUBL salgskreditnota (DK)                     | OIOUBL format for salgskreditnota for Danmark                        |
|                                                  |                       | OIOUBL salgsfaktura (DK)                         | OIOUBL format for salgsfaktura for Danmark                            |
| OB-opgørelsesmodel                             | Momsrapportering         |                                                   |                                                                    |
|                                                  |                       | OB-opgørelse (NL)                               | OB-opgørelsesformat for Nederlandene                          |
| Betalingsmodel                                    | Betalinger              |                                                   |                                                                    |
|                                                  |                       | Betalingsservice (DK)                             | Betalingsservice-betalingsformat for Danmark                        |
|                                                  |                       | Vekselremittering (FR)                  | Vekselremitteringsformat for Frankrig                      |
|                                                  |                       | BTL91 (NL)                                        | BTL91-kreditorbetalingsformat for Nederlandene                    |
|                                                  |                       | CFONB Prelevements (FR)                           | CFONB format for direkte debetbetalinger for Frankrig                       |
|                                                  |                       | CFONB Virements (FR)                              | CFONB format for indenlandsk kreditorbetaling for Frankrig                    |
|                                                  |                       | Nordea kreditor (DK)                                | Kreditorbetalingsformatet Nordea Corporate Netbank for Danmark         |
|                                                  |                       | ANZ direkte kreditydelsesformat (AU)                    | Formatet for ANZ kreditydelsesformat for Australien                 |
|                                                  |                       | CBA direkte kreditydelsesformat (AU)                    | Format for CBA direkte kreditydelse for Australien                 |
|                                                  |                       | NAB direkte kreditydelsesformat (AU)                    | Format for NAB direkte kreditydelse for Australien                 |
|                                                  |                       | STG direkte kreditydelsesformat (AU)                    | Format for STG direkte kreditydelse for Australien                 |
|                                                  |                       | WBC direkte indtastningssystemformat (AU)                      | Format for WBC direkte indtastningssystem for Australien                   |
|                                                  |                       | DirectLink (NZ)                                   | Formatet for DirectLink for New Zealand                              |
|                                                  |                       | JBA-betalingsfil (JP)                             | JBA betalingsformat for Japan                                       |
|                                                  |                       | ISO20022 overførsel                          | SEPA kreditoverførselsformat for Europa                             |
|                                                  |                       | ISO20022-overførsel (FR)                     | SEPA kreditoverførselsformat for Frankrig                             |
|                                                  |                       | ISO20022-overførsel (DE)                     | SEPA kreditoverførselsformat for Tyskland                            |
|                                                  |                       | ISO20022-overførsel (NL)                     | SEPA kreditoverførselsformat for Nederlandene                    |
|                                                  |                       | ISO20022 direkte debet                             | SEPA direkte debetformat for Europa                                |
|                                                  |                       | ISO20022 direkte debet (FR)                        | SEPA direkte debetformat for Frankrig                                |
|                                                  |                       | ISO20022 direkte debet (DE)                        | SEPA direkte debetformat for Tyskland                               |
|                                                  |                       | ISO20022 direkte debet (NL)                        | SEPA direkte debetformat for Nederlandene                       |
|                                                  |                       | BACS (UK)                                         | BACS kreditorbetalingsformat for Storbritannien                  |
| Modtagermoms                                   | Momsrapportering         |                                                   |                                                                    |
|                                                  |                       | Salgsliste med modtagermoms                         | Salgsliste med modtagermomsformat                                   |
| Nederlandsk XBRL-integrationsmodel                     | XBRL-rapportering        |                                                   |                                                                    |
|                                                  |                       | Semansys XBRL (NL)                                | Semansys XBRL eksportformat for Nederlandene                    |
| GAF-model (MY)                                   | Finansiel revision       |                                                   |                                                                    |
|                                                  |                       | GAF-fil (MY)                                     | Format for GAF for Malaysia                                         |
| Aldersfordelt saldoliste for kreditor (CN)                         | Kreditordataanalyse |                                                   |                                                                    |
|                                                  |                       | Aldersfordelt saldoliste for kreditor (CN)                   | Aldersfordelt saldoliste for kreditorer for Kina                               |
| Opgørelsesmodel for kreditorfaktura                 | Kreditordataanalyse |                                                   |                                                                    |
|                                                  |                       | Kreditorfakturadeklaration (IS)                   | Opgørelse for kreditorfaktura, format for Island                      |
|                                                  |                       | Kreditorfakturadeklaration, rapport (IS)            | Opgørelse for kreditorfaktura, rapport for Island                      |



<a name="additional-resources"></a>Yderligere ressourcer
--------

[Lokaliseringskrav – oprette en elektronisk rapporteringskonfiguration](electronic-reporting-configuration.md)

[Administrere livscyklus for elektroniske indberetningskonfigurationer](general-electronic-reporting-manage-configuration-lifecycle.md)




