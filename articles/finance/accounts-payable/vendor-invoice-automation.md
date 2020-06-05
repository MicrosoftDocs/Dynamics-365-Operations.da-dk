---
title: Automatisering af kreditorfaktura
description: Dette emne forklarer de funktioner, der er tilgængelige for start-til-slut-automatisering af kreditorfakturaer, tilmed fakturaer, der indeholder vedhæftede filer.
author: abruer
manager: AnnBe
ms.date: 05/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4560d7b61fa8f014f9a1185da087df8b1c8e61ba
ms.sourcegitcommit: b7af921189048d9f2eb4d3fd57c704c742bc96e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/23/2020
ms.locfileid: "3396003"
---
# <a name="vendor-invoice-automation"></a>Automatisering af kreditorfaktura

[!include [banner](../includes/banner.md)]

Dette emne forklarer de funktioner, der er tilgængelige for start-til-slut-automatisering af kreditorfakturaer, tilmed fakturaer, der indeholder vedhæftede filer.

Organisationer, der ønsker at strømline deres kreditorprocesser, identificerer ofte fakturabehandling som en af de vigtigste procesområder, der skal være mere effektive. I mange tilfælde overfører disse organisationer behandlingen af papirfakturaer til en tredjepartserviceudbyder af optisk tegngenkendelse (OCR). Derefter modtager de maskinlæsbare fakturametadata sammen med et scannet billede af hver faktura. Som hjælp til automatisering oprettes en sidste løsning derefter for at kunne forbruge disse artefakter i faktureringssystemet. Nu er denne sidste automatisering som standard aktiveret via en løsning til fakturaautomatisering.

## <a name="solution-context"></a>Løsningskontekst

Løsningen til fakturaautomatisering er en standardgrænseflade, der kan acceptere fakturametadata til fakturahovedet og fakturalinjer samt vedhæftede filer, der vedrører fakturaen. Alle eksterne systemer, der kan generere artefakter, som er i overensstemmelse med denne grænseflade, vil kunne sende feedet til automatisk behandling af fakturaer og vedhæftede filer.

I følgende illustration vises et eksempel på integrationsscenarie, hvor Contoso er gået sammen med en OCR-tjenesteudbyder til behandling af kreditorfakturaer. Contosos kreditorer sender fakturaer til tjenesteudbyderen via mail. Udbyderen genererer via OCR-behandling fakturametadata (hoved og/eller linjer) og et scannet billede af fakturaen. Et integrationslag transformerer derefter disse artefakter, så de kan forbruges.

![Eksempel på integrationsscenarie](media/vendor_invoice_automation_01.png)

Flere variationer af det foregående scenarie er mulige, hvis fakturaintegration er påkrævet. Overførsel af data er en anden metode, hvor denne grænseflade kan bruges til at oprette fakturaer og vedhæftede filer.

### <a name="solution-components"></a>Løsningskomponenter

Løsningens fodaftryk består af følgende komponenter:

+ Dataenheder for fakturahoved, fakturalinjer og fakturaens vedhæftede filer
+ Undtagelsesbehandling af fakturaer
+ En side om side-fremviser af vedhæftede filer i fakturaer

Resten af dette emne indeholder detaljerede beskrivelser af disse løsningskomponenter.

## <a name="data-entities"></a>Dataenheder

En datapakke er arbejdsenheden, der skal sendes til, så fakturahoveder, fakturalinjer og fakturaens vedhæftede filer kan oprettes. Følgende dataenheder anvendes for de artefakter, der udgør datapakken:

+ Kreditorfakturahoved
+ Kreditorfakturalinje
+ Vedhæftet dokument til kreditorfaktura

Kreditorfakturaens vedhæftede dokument er en ny dataenhed, der indføres i forbindelse med denne funktion. Kreditorfakturahovedets enhed er blevet ændret, så det understøtter vedhæftede filer. Kreditorfakturaens linjeenhed er ikke blevet ændret for denne funktion.

Få detaljerede oplysninger om datapakker i [Oversigt over datastyring](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md). Du kan finde oplysninger om, hvordan du opretter datapakker ved hjælp af arbejdsområdet Datastyring, i [Behandle og forbruge datapakker i Dynamics 365 Finance and Operations-app-løsning](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).

Du kan hurtigt generere testdata, der indeholder fakturaer og vedhæftede filer, ved at følge disse trin.

1. Log på din forekomst.
1. Gå til **Kreditor** > **Fakturaer** > **Ventende kreditorfakturaer**.
1. Opret fakturaer, der har linjer og vedhæftede filer.

    > [!NOTE]
    > De vedhæftede filer skal være i hovedet. Enheden Vedhæftet dokument til kreditorfaktura understøtter i øjeblikket ikke vedhæftede filer i en linje.

1. Åbn arbejdsområdet **Datastyring**.
1. Opret et eksportjob, der omfatter enhederne Kreditorfakturahovedet, Kreditorfakturalinje og Vedhæftet dokument til kreditorfaktura.
1. Eksportér dataene.
1. Hent de eksporterede data som en pakke. Du kan nu bruge pakken til at importere data til målforekomster til testformål.

### <a name="determining-the-legal-entity-for-an-invoice"></a>Bestemmelse af den juridiske enhed for en faktura

Fakturaer, der importeres via datapakker, kan knyttes til den juridiske enhed, de tilhører, på to måder:

+ Importjobbet, der behandler fakturaen, importerer den til det samme regnskab, hvor jobbet er planlagt i **Datastyring**-arbejdsområdet. Med andre ord fastsætter jobbets regnskab det regnskab, som fakturaen tilhører.
+ Når der sendes en datapakke, der indeholder fakturaer, til Finance, kan kalderen (dvs. det integrationsprogram, der kører uden for Finance) udtrykkeligt nævne regnskabs-id i HTTP-anmodningen. I dette tilfælde tilsidesættes den regnskabskontekst, hvor behandlingsjobbet kører i Finance, og fakturaerne importeres til det regnskab, der blev sendt via HTTP-anmodningen.

> [!NOTE]
> Denne funktionsmåde er standardfunktionsmåde for datastyring. Den er forklaret her i forbindelse med fakturaer for at give en komplet beskrivelse.

## <a name="exception-processing"></a>Behandling af undtagelser

I scenarier, hvor kommer kreditorfakturaer kommer ind i Finance and Operations via integration, skal det være nemt for et kreditorteammedlem at behandle undtagelser eller mislykkede fakturaer og at oprette ventende fakturaer ud fra mislykkedes fakturaer. Denne undtagelsesbehandling for kreditorfakturaer er nu en del af Finance and Operations.

### <a name="exceptions-list-page"></a>Listesiden Undtagelser

Den nye listeside for fakturaundtagelser findes under **Kreditor** > **Fakturaer** > **Importfejl** > **Kreditorfakturaer, der blev ikke importeret**. Denne side viser alle kreditorfakturahoveders poster fra den midlertidige tabel i dataenheden Kreditorfakturahoved. Bemærk, at du kan få vist de samme poster fra **Datastyring**-arbejdsområdet, hvor du også kan udføre de samme handlinger, der findes i funktionen for undtagelseshåndtering. Dog er funktionen for undtagelseshåndtering i brugergrænsefladen optimeret til en funktionel bruger.

![Listesiden Undtagelser](media/vendor_invoice_automation_02.png)

Denne listeside indeholder følgende felter, der leveres via feedet:

+ **Regnskab** – Det regnskab, som fakturaen tilhører
+ **Fejlmeddelelse** – Den fejlmeddelelse, der vises i datastyringen for at forklare, hvorfor fakturaen kunne ikke oprettes
+ **Nummer** – Fakturanummeret
+ **Fakturakonto**
+ **Navn** – Leverandørens navn
+ **Kreditorkonto**
+ **Indkøbsordre** – Indkøbsordrenummeret for fakturaen
+ **Bogføringsdato**
+ **Fakturadato**
+ **Fakturabeskrivelse**
+ **Valuta**
+ **Logfil**
+ **Linjereference** – Den identifikator, der kommer fra det eksterne system

    > [!NOTE]
    > Linjereferencen er ikke faktura-id.

Denne listeside har også en indholdsrude, som du kan bruge på følgende måder:

+ Få vist hele fejlmeddelelsen, så du ikke behøver at udvide kolonnen **Fejlmeddelelse** i gitteret.
+ Få vist hele listen over vedhæftede filer for fakturaen, hvis vedhæftede filer blev leveret med fakturaen.

Listesiden understøtter følgende handlinger:

+ **Rediger** – Åbn undtagelsesposten i redigeringstilstand, så du kan løse problemerne.
+ **Indstillinger** – Få adgang til de standardindstillinger, der er tilgængelige på listesider. Du kan bruge **Føj til arbejdsområde**-indstillingen til at fastgøre listesiden med undtagelser til arbejdsområdet som en liste eller et felt.

### <a name="exception-details-page"></a>Siden Undtagelsesoplysninger

Når du starter redigeringstilstand, vises siden Undtagelsesoplysninger for den faktura, der er problemer med. Hvis der er vedhæftede filer, vises fakturaen og den vedhæftede fil som standard ved siden af hinanden på siden Undtagelsesoplysninger.

![Siden Undtagelsesoplysninger](media/vendor_invoice_automation_03.png)

I foregående illustration er der ikke nogen linjer for kreditorfakturahoved, der fulgte med. Linjeafsnittet er derfor tomt.

Siden Undtagelsesoplysninger understøtter følgende handling:

+ **Opret ventende faktura** – Når du har løst problemerne på fakturaen som en del af undtagelsesbehandlingen, kan du klikke på denne knap for at oprette den ventende faktura. Oprettelse af ventende fakturaer foregår i baggrunden (som en asynkron handling).

### <a name="shared-service-vs-organization-based-exception-processing"></a>Behandling af delt tjeneste vs. organisationsbaseret undtagelse

Listesiden med undtagelser understøtter standardsikkerhedskonstruktioner, som **Datastyring**-arbejdsområdet understøtter til behandling af midlertidige poster. Importjobbet for fakturaer kan sikres på følgende måder:

+ Af brugerrolle
+ Pr. bruger
+ af juridisk enhed

![Importjob, der er sikret af brugerrolle og juridisk enhed](media/vendor_invoice_automation_04.png)

Hvis sikkerhed er konfigureret for importjobbet til fakturaer, bruger listesiden med undtagelser disse indstillinger. Brugere vil kun kunne se fakturaundtagelsesposter, som denne konfiguration giver mulighed for at se.

For eksempel har Contoso besluttet at behandle fakturaundtagelser efter juridisk enhed. Derfor er sikkerheden konfigureret på importjobbet for fakturaer på en sådan måde, at en bruger i juridisk enhed A kun kan se fakturaundtagelser i juridisk enhed A, mens en bruger i juridisk enhed B kun kan se fakturaundtagelser i juridisk enhed B. Denne konfiguration giver mulighed for opdeling af opgaver til administration af fakturaundtagelser.

Contoso kan også beslutte ikke at indføre en sikkerhed, så de samme brugere kan behandle fakturaundtagelser for alle juridiske enheder. Denne konfiguration giver mulighed for et delt tjenestescenarie til styring af fakturaundtagelser.

## <a name="side-by-side-attachment-viewer"></a>Side om side-fremviser af vedhæftede filer

Så du nemt kan få vist vedhæftede filer for kreditorfakturaer, indeholder følgende sider, der bruges i faktureringsprocessen, nu en vedhæftet fil-fremviser:

+ **Undtagelseshåndtering**
+ **Ventende kreditorfakturaer**-siden (findes også i evalueringsprocessen for fakturaer)
+ **Fakturajournal**-forespørgselsside (for bogførte fakturaer)

Her er den vigtigste funktion i fremviseren af vedhæftede filer:

+ Få vist alle vedhæftede filtyper, som dokumentstyring understøtter (filer, billeder, URL-adresser og noter).
+ Få vist flere sider i TIFF-filer.
+ Du kan udføre følgende handlinger på billedfiler:
  + Fremhæve dele af billedet.
  + Blokere dele af billedet.
  + Tilføje anmærkninger på billedet.
  + Zoome ind og ud på billedet.
  + Panorere billedet.
  + Fortryde og annullere Fortryd af handlinger.
  + Tilpasse billedets størrelse.

> [!NOTE]
> Disse handlinger er kun tilgængelige for billedfiler (JPEG, TIFF, PNG osv.). Eventuelle ændringer, du foretager af et billede ved hjælp af disse handlinger, gemmes i billedfilen. Fremviseren omfatter ikke i øjeblikket versionsstyring og overvågning.

### <a name="default-attachment"></a>Standardvedhæftning

Hvis en kreditorfaktura har mere end én vedhæftet fil, kan du angive et af dokumenterne som den standardvedhæftede fil på siden **Vedhæftede filer**. **Er standardvedhæftning**-indstillingen er en ny indstilling, der er tilføjet som en del af denne funktion. Denne indstilling vises også i dataenheden Vedhæftet dokument til kreditorfaktura. Derfor kan standardvedhæftningen angives via integrationer.

Kun ét dokument kan angives som standardvedhæftning. Når du har oprettet et dokument som standardvedhæftning, vises det automatisk i fremviseren, når fakturaen åbnes. Hvis du ikke angiver noget dokument som standardvedhæftning, viser fremviseren ikke automatisk nogen vedhæftet fil, når fakturaen åbnes.

### <a name="showhide-invoice-attachments"></a>Vise/skjule fakturavedhæftninger

Med en ny knap, der findes på forespørgselssiderne **Behandling af undtagelsen**, **Ventende faktura** og **Fakturajournal**, kan du vise eller skjule fremviseren af vedhæftede filer.

### <a name="security"></a>Sikkerhed

Følgende handlinger i fremviseren styres via rollebaseret sikkerhed:

+ Fremhævning
+ Blokering
+ Anmærkning

### <a name="pending-vendor-invoices-page"></a>Siden Ventende kreditorfakturaer

Følgende rettigheder giver skrivebeskyttet adgang eller læse- og skriveadgang til fremviseren for at fremhævnings-, blokerings- og anmærkningshandlinger:

+ **Vedligehold billede af kreditorfaktura** – Denne rettighed giver læse-/skriveadgang.
+ **Vis billede af kreditorfaktura** – Denne rettighed giver skrivebeskyttet adgang.

Følgende opgaver giver skrivebeskyttet adgang eller læse- og skriveadgang til fremviseren for disse handlinger:

+ **Vedligehold kreditorfakturaer** – Rettigheden Vedligehold billede af kreditorfaktura er tildelt denne opgave.
+ **Forespørg status for kreditorfaktura** – Rettigheden Vis billede af kreditorfaktura er tildelt denne opgave.

Følgende roller giver skrivebeskyttet adgang eller læse- og skriveadgang til fremviseren for disse handlinger:

+ **Kreditorassistent** og **Kreditorchef** – Opgaven Vedligehold kreditorfakturaer er tildelt disse roller.
+ **Kreditorassistent**, **Kreditorchef**, **Medarbejder for centraliserede kreditorbetalinger** og **Ansvarlig for kreditorbetalinger** – Opgaven Forespørg status for kreditorfaktura er tildelt til disse roller.

### <a name="invoice-exception-details-page"></a>Siden med undtagelsesoplysninger om fakturaer

Følgende rettigheder giver skrivebeskyttet adgang eller læse- og skriveadgang til fremviseren for fremhævnings-, blokerings- og anmærkningshandlinger.

> [!NOTE]
> De roller, der er nævnt i dette afsnit, giver fra starten skrivebeskyttet adgang til fakturabillederne i fremviseren af vedhæftede filer. Hvis en rolle også skal have skriveadgang til billederne, kan du tildele denne rolle skriveadgang ved hjælp af den rettighed eller opgave, der er beskrevet her.

+ **Vedligehold billede af enhed for overskrift til kreditorfaktura** – Denne rettighed giver læse-/skriveadgang til fakturabillederne i fremviseren.
+ **Vis billede af enhed for overskrift til kreditorfaktura** – Denne rettighed giver skrivebeskyttet adgang til fakturabilledet i fremviseren.

Følgende opgaver giver skrivebeskyttet adgang til fremviseren for disse handlinger:

+ **Vedligehold kreditorfakturaer** – Rettigheden Vedligehold billede af enhed for overskrift til kreditorfaktura er tildelt denne opgave.

Følgende roller giver skrivebeskyttet adgang til fremviseren for disse handlinger:

+ **Kreditorassistent** og **Kreditorchef** – Opgaven Vedligehold kreditorfakturaer er tildelt disse roller.

Som standard, hvis brugerrollen giver redigeringsrettigheder på enhver side, skal brugeren også have redigeringsrettigheder til fremviseren af vedhæftede filer for fremhævnings-, blokerings- og anmærkningshandlinger. Hvis der er situationer, hvor en bestemt rolle skal have redigeringsrettigheder på siden, men ikke i fremviseren, kan der dog bruges de nødvendige rettigheder fra den foregående liste for at opfylde behovet.
