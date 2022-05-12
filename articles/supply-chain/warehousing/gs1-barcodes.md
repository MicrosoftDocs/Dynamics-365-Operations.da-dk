---
title: GS1-stregkoder
description: Dette emne beskriver, hvordan du opretter GS1-stregkoder og QR-koder, så etiketter kan scannes på et lagersted.
author: Mirzaab
ms.date: 03/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ea928bc8a020035adb36ae2e7873c656e8c3985d
ms.sourcegitcommit: 1050e58e621d9a0454895ed07c286936f8c03320
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2022
ms.locfileid: "8625272"
---
# <a name="gs1-bar-codes"></a>GS1-stregkoder

[!include [banner](../includes/banner.md)]

Arbejdere på lagersteder skal ofte udføre flere opgaver, når de bruger en mobilenhedsscanner til at registrere bevægelser for et element, et produkt eller en container. Disse opgaver kan omfatte både scanning af stregkoder og manuel angivelse af oplysninger på mobilenheden. Stregkoderne bruger et firmaspecifikt format, som du kan definere og administrere ved hjælp af Microsoft Dynamics 365 Supply Chain Management.

GS1-stregkoder til forsendelsesetiketter er udviklet til at være en global standard for udvekslingen af data mellem firmaer. De findes i både lineære symboler (1D) (stregkodeformater) som f.eks. GS1-128, og 2D-symboler, f.eks. GS1 DataMatrix og GS1 QR-koder. GS1-stregkoder indkoder ikke kun dataene, men gør det muligt at bruge en foruddefineret liste over *program-id'er* til at definere betydningen af dataene. GS1-standarden definerer dataformatet og de forskellige typer data, der kan bruges til kodning. I modsætning til ældre stregkodestandarder kan GS1-stregkoder have flere dataelementer. En enkelt stregkodescanning kan derfor registrere flere typer produktoplysninger, f.eks. batchet og udløbsdatoen.

Understøttelse af GS1 i Supply Chain Management forenkler i mærkbart omfang scanningsprocessen på lagersteder, hvor paller og containere mærkes ved hjælp af stregkoder i GS1-format. Lagerarbejdere kan udtrække alle de påkrævede oplysninger via en enkelt scanning af en GS1-stregkode. Hvis du ikke længere behøver at udføre flere scanninger og/eller indtaste oplysninger manuelt, kan GS1-stregkoder reducere den tid, der er forbundet med opgaverne. Samtidig kan de også forbedre præcisionen.

Logistikchefer skal oprette den krævede liste over program-id'er og knytte hver af dem til de relevante menupunkter på mobilenheder. Program-id'erne kan derefter bruges på tværs af lagersteder som en global indstilling til flytnings- og emballeringsformål. Derfor har alle forsendelsesetiketter samme form.

Medmindre andet er anført, henviser udtrykket *stregkode* i dette emne til både lineære (1D) stregkoder og 2D-stregkoder.

## <a name="the-gs1-bar-code-format"></a>GS1-stregkodeformatet

GS1-generelle specifikationer angiver, hvilke symboler der kan bruges til GS1-stregkoder, og hvordan dataene skal kodes i stregkoden. Dette afsnit indeholder en kort introduktion til emnet. Du kan finde alle oplysninger i [Generelle GS1-specifikationer](https://www.gs1.org/docs/barcodes/GS1_General_Specifications.pdf), der er udgivet af GS1. GS1-specifikationsdokumentet opdateres jævnligt, og dets oplysninger er opdaterede med GS1-generelle specifikationer frigivelse 22.0.

GS1-stregkoder bruger følgende symbolik:

- **Lineære stregkoder eller 1D-stregkoder** – GS1-128 og GS1 DataBar
- **2D-stregkoder** – GS1 DataMatrix, GS1 QR-kode og GS1 Dotcode

Bemærk, at der er særlige oplysninger om GS1 i GS1-128, som er en særlig sag med den almindelige kode-128 lineære stregkode, GS1 DataMatrix og GS1 QR-koden. Forskellen mellem GS1-versionen og ikke-GS1-versionen er, at der findes et særligt tegn (FNC1) som det første tegn i stregkodedataene. Forekomsten af et FNC1-tegn angiver, at dataene i stregkoden skal fortolkes i overensstemmelse med GS1-specifikationen.

Dataene i selve stregkoden består af flere dataelementer, som hver især er identificeret af et program-id i starten af feltet. Normalt vises dataene også under stregkoden i menneskeligt læsbart format, hvor applikations-id'et vises i parentes. Her er et eksempel: `(01) 09521101530001 (17) 210119 (10) AB-123`. Denne stregkode indeholder tre elementer:

- **Programidentifikator 01** – GS1-varenummer til global handel (GTIN) for varen.
- **Programidentifikator 17** – Udløbsdatoen.
- **Programidentifikator 10** – Batchnummeret.

Dataene kan for hvert element have enten en foruddefineret længde eller en variabel længde. Der findes en fast liste over programidentifikatorer, der har foruddefinerede længder. Alle andre programidentifikatorer har variabel længde, og på GS1-programidentifikatorlisten angives den maksimale længde og formatet af data. Programidentifikator 01 har f.eks. en foruddefineret længde på 16 tegn (to til selve programidentifikatoren og derefter 14 til GTIN), og programidentifikator 17 har en foruddefineret længde på otte tegn (to til selve programidentifikatoren og derefter seks for datoen). Programidentifikator 10 har dog to numre til selve programidentifikatoren og derefter op til 20 alfanumeriske tegn.

Når elementer sættes sammen, og et element efterfølger et element med variabel længde, skal der bruges et separatortegn. Denne separator kan enten være det særlige FNC1-tegn eller gruppeseparatortegnet (et tegn, der ikke kan udskrives, og som har ASCII-kode 29 og hexadecimal kode 1D). Separatoren må ikke bruges efter det sidste element. Selvom separatoren ikke bør bruges efter elementer, der har en foruddefineret længde, er det ikke en kritisk fejl at medtage den.

I stregkodedataene fra forrige eksempel på en stregkode, der indeholder programidentifikatorerne 01, 17 og 10, data i Kode-128, QR-kode eller DataMatrix-symbol, indkodes som `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` (applikationsidentifikatorer vises med fed skrift). Det er en bedste fremgangsmåde at placere alle elementer med variabel længde i slutningen for at fjerne behovet for endnu et gruppeseparatortegn. Stregkoden kan dog også have en anden rækkefølge af elementer, hvor separatoren er obligatorisk. Her er et eksempel: `<FNC1>`**`01`**`09521101530001`**`10`**`AB-123<GS>`**`17`**`210119`.

### <a name="dates-and-decimal-numbers"></a>Datoer og decimaltal

Datoer vises altid i *ÅÅMMDD*-format, hvor århundredet i året bestemmes af GS1-specifikationer. Det er kun datoer fra 49 år i fortiden til 50 år i fremtiden (i forhold til det indeværende år), der kan repræsenteres.

Nogle dataelementer indeholder decimaltal. Ansøgningsidentifikatorer 3100, 3101, ... 3105 repræsenterer f.eks. en nettovægt i kilo. Da disse applikationsidentifikatorer har en foruddefineret længde på 10, er der seks cifre tilgængelige for antallet. Placeringen af decimaltegnet angives af det sidste ciffer i programidentifikatoren. Derfor kan denne gruppe af programidentifikatorer også være gengivet som *310n*. Da GS1-standarden angiver, at der altid skal være mindst ét ciffer til venstre for decimaltegnet, er et maksimum på fem decimalpladser tilladt.

Her er nogle eksempler, der viser, hvordan nummeret *123456* fortolkes af forskellige programidentifikatorer (vises med fed skrift):

- **`3100`**`123456` &rarr; 123456 (heltal)
- **`3101`**`123456` &rarr; 12345,6 (én decimal)
- **`3102`**`123456` &rarr; 1234,56 (to decimaler)
- **`3103`**`123456` &rarr; 123,456 (tre decimaler)
- **`3104`**`123456` &rarr; 12,3456 (fire decimaler)
- **`3105`**`123456` &rarr; 1,23456 (fem decimaler)

## <a name="scanning-gs1-bar-codes-in-supply-chain-management"></a>Scanne GS1-stregkoder i Supply Chain Management

Lagerarbejdere bruger en scanner, der er indbygget eller forbundet med en mobilenhed, til at scanne GS1-stregkoder. Scanneren sender derefter den scannede stregkode til Warehouse Management-mobilappen som en række tastaturhændelser. Denne operationsmåde kaldes også *kreditkortlæser* eller *læser*. Mobilappen sender derefter den modtagne tekst som den er til Supply Chain Management. Når systemet modtager inputdata, bestemmer det først, om dataene begynder med et af de konfigurerede præfikser, der angiver, at dataene faktisk er en GS1-stregkode (se afsnittet [Konfigurere globale GS1-indstillinger](#set-gs1-options)). Hvis de scannede data begynder med et af disse præfikser, bruger systemet en GS1-parser til at fortolke dataene og udtrække individuelle dataelementer i henhold til deres programidentifikatorer. Når dataene er blevet fortolket, udfyldes enten det aktuelle inputfelt eller flere felter med de scannede data.

### <a name="configuration-of-bar-code-scanner-hardware-and-software"></a>Konfiguration af stregkodescannerhardware og -software

For at Supply Chain Management kan genkende og afkode GS1-stregkoder korrekt skal hardwarescanneren eller den understøttende software være konfigureret til at udføre følgende handlinger:

- Føj et præfiks til de scannede stregkoder, så systemet kan genkende en GS1-stregkode.
- Konverter det ASCII-gruppeseparatortegn, der ikke kan udskrives (ASCII-kode 29 eller hexadecimalkode 1D), til et tegn, der kan udskrives, f.eks. en tilde (~).

Selvom du kan føje et vilkårligt præfiks til den scannede stregkode, kan du tilføje en ISO/IEC 15424-symbolidentifikator, der også kaldes en *AIM-identifikator*. Denne identifikator på tre tegn starter med `]`. Det indeholder derefter ét tegn, der identificerer det symbol, der bruges, og har et nummer, der bruges som yderligere modifikator. AIM-identifikatoren `]C1` angiver f.eks. en Kode 128-stregkode (på grund af tegnet `C`), og modifikatoren `1` angiver, at der er et FNC1-tegn på dataenes første position. Derimod er en `]C0` en Kode 128-stregkode med et hvilket som helst andet tegn som dataenes første tegn.

Følgende fem symbolikidentifikatorer svarer til GS1-stregkoder med programidentifikatorelementer:

- `]C1` – Kode 128 (`C`) med FNC1-tegn på første position (`1`), også kaldet GS1-128.
- `]e0` – GS1 DataBar.
- `]d2` – DataMatrix (`d`) med ECC 200 og FNC1 i første position (`2`), også kaldet GS1 DataMatrix.
- `]Q3` – QR-kode (`Q`) Model 2-symbol med FNC1 i første position (`3`), også kaldet GS1 QR-kode.
- `]J1` – GS1 DotCode.

Hvis du bruger disse identifikatorer, kræver kompatibilitet med ikke-GS1-stregkoder, at scannerne eller scanningssoftwaren er konfigureret til at fjerne eventuelle identifikatorer, der ikke svarer til GS1-identifikatorerne. Hvis du f.eks. scanner en "normal" Code 39-stregkode, tilføjes præfikset `]A0`. Da systemet ikke kan forstå dette præfiks som et af GS1-præfikserne, vil det tolke det som data og give uventede resultater.

> [!NOTE]
> For at gøre det nemmere vil version 2.0.17.0 og senere af Warehouse Management-mobilappen fjerne eventuelle AIM-præfikser, der ikke findes på den forrige liste. Denne funktionalitet understøtter tilfælde, hvor du kan konfigurere scanneren til at tilføje AIM-præfikset, men ikke for at fjerne de uønskede præfikser.

### <a name="single-and-multiple-field-scanning"></a>Scanning af et enkelt og flere felter

Når dataene er blevet registreret fra stregkoden, bliver de indkodet i flowstyringen for mobilenheden. Der er to metoder, der vil blive behandlet på skift:

- **Scanning af enkelt felt** – Denne metode udfylder kun det felt, som stregkoden er scannet ind i. Hvis du f.eks. scanner stregkoden `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123`, mens markøren er i feltet **Vare**, indsættes GTIN `09521101530001` fra stregkoden i det pågældende felt. Hvis du scanner den samme stregkode, mens markøren er i feltet **Batch-id** indsættes batchnummer `AB-123` fra stregkoden. Denne tilstand fungerer for alle felter i alle flow og kræver kun, at den generiske GS1-opsætning er konfigureret. Hvis en stregkode indeholder flere elementer, skal den stadig scannes flere gange, da der kun indsættes ét stykke af stregkoden ad gangen i flowet for mobilenheden. Denne funktionsmåde styres af en generisk GS1-opsætning som beskrevet i afsnittet [Oprette den generiske GS1-opsætning](#generic-gs1-setup).
- **Scanning af flere felter** – Denne metode udfylder flere felter, når en stregkode scannes, ved at overføre yderligere data ind i flowtilstanden for mobilenheden. Politikken er f.eks. konfigureret til at indsætte programidentifikator 01 i `ItemId`-kontrolelementet og programidentifikator 10 i feltet `InventBatchId`. Hvis du scanner stregkoden `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123`, vil data for begge variabler blive overført på samme tid. Derfor vil systemet ikke bede dig om varen og/eller batchnummeret i flowet. Denne funktionalitet styres af GS1-politikker, der er kædet sammen med menupunkter, som det er beskrevet i afsnittet [Konfigurere GS1-politikker for menupunkter til mobilenheder](#policies-for-menus).

> [!WARNING]
> Standardpolitikkerne for GS1 er testet til at fungere uden uventet funktionalitet. Tilpasningen af GS1-politikker, der er kædet sammen med menupunkter, kan dog forårsage uventede funktionsmåder, da flowet muligvis ikke forventer, at visse data er tilgængelige på et bestemt tidspunkt.

## <a name="turn-on-the-gs1-feature"></a>Slå GS1-funktionen til

Før du kan bruge denne funktion, skal den være aktiveret i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Warehouse Management*
- **Funktionsnavn:** *Scan GS1-stregkoder*

### <a name="turn-on-the-enhanced-parser-for-gs1-barcodes-feature"></a>Aktivere funktionen Udvidet parser til GS1-stregkoder

Hvis du bruger GS1-stregkoder, anbefales det, at du også aktiverer funktionen *Udvidet parser til GS1-stregkoder*. Denne funktion giver en forbedret implementering af GS1-stregkode-parser. Den tilføjer følgende forbedringer:

- Den følger den GS1-generelle specifikationsalgoritme for symboldatafortolkning og validerer, at dataene i symbolet er gyldige i henhold til specifikationen.
- Det kræver ikke, at du konfigurerer en værdi af **Maksimal længde på identifikator** og bruger den længste præfikssammenholdelse fra konfigurerede programidentifikatorer.
- Det giver dig mulighed for nemmere at konfigurere decimalprogramidentifikatorer ved at bruge bogstavet *n* til at matche et vilkårligt tal. Du kan f.eks. nøjes med at konfigurere én programidentifikator (*310n*) i stedet for separate programidentifikatorer (*3101*, *3102*, *3103* osv.).
- Det løser et problem, hvor forkert kodede data fortolkes som feltdata.
- Den findes som en separat klasse, der kan genbruges i andre sammenhænge, og som gør det muligt at bruge et udvidelsespunkt til at manipulere med scannede data, før flowfelterne udfyldes.

## <a name="set-up-global-gs1-options"></a><a name="set-gs1-options"></a>Konfigurere globale GS1-indstillinger

Siden **Parametre for lagerstedsstyring** indeholder nogle få indstillinger, der fastlægger globale GS1-indstillinger.

Benyt følgende fremgangsmåde for at angive globale GS1-indstillinger.

1. Gå til **Warehouse Management \> Opsætning \> Parametre til Warehouse management**.
1. Udfyld følgende ekstra felter i oversigtspanelet **Stregkoder**:

    - **FNC1-tegn**, **Datamatrix-tegn** og **QR-kodetegn** – Angiv tegn, der skal fortolkes som præfiks for hver type GS1-stregkode.
    - **Gruppeseparator** – Angiv det tegn, der erstatter ASCII-gruppeseparatortegnet.
    - **Maks. længde på id** – Angiv det maksimale antal tegn, der er tilladt for program-id'et. Dette felt er ikke obligatorisk, hvis funktionen *Udvidet parser til GS1* er aktiveret i systemet.

> [!NOTE]
> Præfikser fortæller systemet, at en stregkode er kodet ifølge GS1-standarden. Der kan bruges op til tre præfikser (**FNC1-tegn**, **Datamatrix-tegn** og **QR-kodetegn**) samtidigt og til forskellige formål.

## <a name="gs1-application-identifiers"></a>GS1-programidentifikatorer

GS1-formater koder ikke kun dataene, men gør det muligt at bruge en foruddefineret liste over program-id'er til at definere betydningen af dataene. Logistikchefer skal oprette den krævede liste over program-id'er og knytte hver af dem til de relevante menupunkter på mobilenheder. Id'erne kan derefter bruges på tværs af lagersteder som en global indstilling til flytnings- og emballeringsformål. Derfor har alle forsendelsesetiketter samme form.

Systemet bruger dataene, især de foruddefinerede program-id'er, til at fastlægge de regler, der skal anvendes for de relevante oplysninger, der er scannet.

Hvert program-id signalerer til systemet, at efterfølgende tegn i den scannede stregkode skal betragtes som en blok af krypterede oplysninger. Konfigurationen af program-id'erne definerer, hvordan systemet skal tolke en stregkode og gemme den som en værdi i systemet.

Logistikadministratorer kan bruge standard-id'er til internationale programmer og/eller oprette deres egne.

### <a name="load-the-standard-application-identifiers"></a>Indlæse standardprogram-id'erne

Du kan hurtigt komme i gang med at indlæse en liste over almindelige internationale program-id'er. Du kan derefter udvide eller redigere listen senere efter behov.

Benyt følgende fremgangsmåde for at indlæse standardprogram-id'erne.

1. Gå til **Warehouse management \> Opsætning \> GS1 \> GS1-program-id'er**.
1. Vælg **Opret standardkonfiguration** i handlingsruden.

> [!WARNING]
> Kommandoen **Opret standardopsætning** sletter alle aktuelt definerede program-id'er og erstatter dem med standardlisten. Når du har indlæst standardopsætningen, kan du dog tilpasse listen efter behov.

### <a name="set-up-custom-application-identifiers"></a>Oprette brugerdefinerede program-id'er

Hvis nogle eller alle program-id'er, som din virksomhed bruger, adskiller sig fra standardsættet, kan du oprette dine egne koder fra bunden eller tilpasse standardsættet, som du ønsker.

Benyt følgende fremgangsmåde for at konfigurere og tilpasse dine egne GS1-program-id'er.

1. Gå til **Warehouse management \> Opsætning \> GS1 \> GS1-program-id'er**.
1. Udfør ét af følgende trin:

    - Vælg **Ny** i handlingsruden for at oprette et nyt id.
    - Hvis du vil redigere et eksisterende id: Vælg id'et, og vælg derefter **Rediger** i handlingsruden.

1. Angiv følgende felter for det nye eller valgte id:

    - **Program-id** – Angiv identifikationskoden for program-id'et. Normalt er denne kode et tocifret heltal, men den kan være længere. Ved decimalværdier angiver det sidste ciffer antallet af decimaler. Du kan finde flere oplysninger under beskrivelsen af afkrydsningsfeltet **Decimal** senere på listen. Hvis funktionen *Udvidet parser til GS1-stregkoder* er aktiveret, kan du oprette en enkelt programidentifikator for alle varianter af decimaler ved at bruge bogstavet *n* som det sidste tegn i programidentifikatoren. Du kan f.eks. nøjes med at konfigurere én programidentifikator (*310n*) i stedet for en separat programidentifikator for hvert antal decimaler (*3101*, *3102*, *3103* osv.).
    - **Beskrivelse** – Angiv en kort beskrivelse af id'et.
    - **Fast længde** – Markér dette afkrydsningsfelt, hvis værdier, der scannes med dette program-id, har et fast antal tegn. Fjern markeringen i afkrydsningsfeltet, hvis længden på værdier er variabel. I dette tilfælde skal du angive afslutningen på værdien ved at bruge det gruppeseparatortegn, du angav på siden **Parametre for Warehouse management**.
    - **Længde** – Angiv det maksimale antal tegn, der kan vises i de værdier, der scannes ved hjælp af dette program-id. Hvis afkrydsningsfeltet **Fast længde** er markeret, forventes præcist dette antal tegn.
    - **Type** – Vælg den type værdi, der scannes ved hjælp af dette program-id (*Numerisk*, *Alfanumerisk* eller *Dato*). Yderligere oplysninger om, hvordan datoer og tal vises i stregkodedata, finder du i afsnittet [Datoer og decimaltal](#dates-and-decimal-numbers).
    - **Decimal** – Marker dette afkrydsningsfelt, hvis værdien indeholder et stiltiende decimaltegn. Hvis dette afkrydsningsfelt er markeret, vil systemet bruge det sidste ciffer i program-id'et til at bestemme antallet af decimaler. Yderligere oplysninger om, hvordan datoer og tal vises i stregkodedata, finder du i afsnittet [Datoer og decimaltal](#dates-and-decimal-numbers).

> [!WARNING]
> Selvom systemet giver dig mulighed for at angive afkrydsningsfeltet **Fast længde** for en programidentifikator, bør det kun bruges til undersættet af programidentifikatorer, der har en foruddefineret længde pr. GS1-generelle specifikationer. Den udvidede GS1-parser indeholder allerede listen over alle programidentifikatorer, der har foruddefinerede længder.

> [!NOTE]
> Den værdi af **Gruppeseparator**, der er angivet på siden **Parametre til Warehouse management**, er valgfri, hvis en værdi, der efterfølges af en programidentifikator, har en fast længde.

## <a name="establish-the-generic-gs1-setup"></a><a name="generic-gs1-setup"></a>Oprette den generiske GS1-opsætning

Den generiske GS1-opsætning opretter en samling af fælles tilknytninger. Disse tilknytninger stemmer overens med hvert relevant inputfelt i mobilappen for program-id'et, som bestemmer, hvordan værdier fra scannede stregkoder skal fortolkes og lagres i det pågældende felt. Disse indstillinger anvendes som standard til alle scanninger for alle menupunkter for mobilenheder. De kan dog overskrives for et eller flere specifikke felter af en GS1-politik, der er tildelt et bestemt menupunkt.

Den generiske GS1-opsætning giver kun mulighed for at scanne én værdi ad gangen. Hvis du vil indlæse flere feltværdier fra en enkelt scanning, skal du derfor definere en GS1-politik for de relevante menupunkter.

Du kan finde flere oplysninger om GS1-politikker i næste afsnit.

### <a name="load-the-standard-generic-gs1-setup"></a>Indlæse den generiske GS1-standardopsætning

På siden **Generisk GS1-opsætning** kan du indlæse et standardsæt af tilknytninger mellem felter for mobilenheder og standardprogram-id'er, der er oprettet med standardopsætningen.

Hvis du vil oprette den generiske GS1-opsætning, skal du gå til **Warehouse management \> Opsætning \> GS1 \> Generisk GS1-opsætning**. Vælg derefter **Opret standardopsætning** for automatisk at tildele et egnet program-id til hvert af de felter, der normalt bruges af menupunkter for mobilenheder.

> [!WARNING]
> Hvis der allerede findes en generisk GS1-opsætning, sletter kommandoen **Opret standardopsætning** fuldstændigt og indlæser standardopsætningen.

### <a name="customize-the-standard-generic-gs1-setup"></a>Tilpasse den generiske GS1-standardopsætning

Benyt denne fremgangsmåde for at tilpasse den generiske GS1-opsætning.

1. Gå til **Warehouse management \> Opsætning \> GS1 \> Generisk GS1-opsætning**.
1. Udfør ét af følgende trin:

    - Hvis du vil oprette en ny tilknytning; Vælg **Ny** i handlingsruden.
    - Hvis du vil redigere en eksisterende tilknytning: Vælg tilknytningen, og vælg derefter **Rediger** i handlingsruden.

1. Angiv følgende felter for den nye eller valgte tilknytning:

    - **Felt** – Vælg eller angiv det inputfelt for mobilappen, som den indgående værdi skal tildeles. Værdien af det viste navn, som arbejdere kan se. Det er i stedet det nøglenavn, der tildeles feltet i den underliggende kode. Standardopsætningen indeholder en samling felter, der sandsynligvis vil være nyttige, og indeholder nøglenavne for hvert felt og tilsvarende programmerede funktionalitet. Du skal måske ændre indstillinger til dine udviklingspartnere for at finde de rette indstillinger for implementeringen.
    - **Program-id** – Vælg det relevante program-id som defineret på siden **GS1-program-id'er**. Id'et fastlægger, hvordan stregkoden fortolkes og gemmes som en værdi for det navngivne felt. Når du har valgt et program-id, viser feltet **Beskrivelse** beskrivelsen af det.

## <a name="set-up-gs1-policies-to-be-to-mobile-device-menu-items"></a><a name="policies-for-menus"></a>Konfigurere GS1-politikker til menupunkter for mobilenheder

Formålet med GS1-standarden er at give arbejdere mulighed for at indlæse flere værdier, når de scanner en enkelt stregkode én gang. Til dette formål skal logistikchefer oprette GS1-politikker, der fortæller systemet, hvordan stregkoder med flere værdier skal fortolkes. Du kan senere tildele politikker til menupunkter for mobilenheder for at styre, hvordan en stregkode fortolkes, når arbejdere scanner den, mens de bruger et bestemt menupunkt.

Hvis der ikke er tildelt en GS1-politik til et menupunkt, kan systemet kun hente en enkelt værdi. Denne værdi anvendes til det mobilappinput, der vælges, når arbejderen foretager scanningen, sådan som det er angivet i den generiske GS1-opsætning. Hvis en GS1-politik er tildelt menupunktet, bruger systemet stadig den generiske GS1-opsætning til at knytte den første stregkodeværdi til det valgte felt. Den kan derefter hente yderligere feltværdier som angivet i den gældende politik.

### <a name="load-the-standard-specific-gs1-policies"></a>Indlæse specifikke GS1-standardpolitikker

Du kan hurtigt indlæse et sæt af GS1-politikker. Du kan derefter udvide eller redigere politikkerne senere efter behov.

Benyt følgende fremgangsmåde for at indlæse standardprogram-id'erne.

1. Gå til **Warehouse management \> Opsætning \> GS1 \> GS1-poltik**.
1. Vælg **Opret standardkonfiguration** i handlingsruden.

> [!WARNING]
> Kommandoen **Opret standardopsætning** sletter alle aktuelt definerede politikker og erstatter dem med standardsættet af politikker. Når du har indlæst standardopsætningen, kan du dog tilpasse politikkerne efter behov.

### <a name="set-up-custom-specific-gs1-policies"></a>Konfigurere brugerdefinerede specifikke GS1-politikker

> [!WARNING]
> Nogle GS1-politikker fungerer muligvis ikke med alle de mobilflow, du bruger. Når du konfigurerer tilpassede GS1-politikker, skal du teste flowet for mobilenheden ved at bruge forskellige oplysninger, der scannes på forskellige steder i flowet. På denne måde kan du afgøre, om flowet fungerer som forventet.

Benyt følgende fremgangsmåde for at konfigurere og tilpasse GS1-politikkerne.

1. Gå til **Warehouse management \> Opsætning \> GS1 \> GS1-poltik**.
1. Udfør ét af følgende trin:

    - Hvis du vil oprette en ny politik; Vælg **Ny** i handlingsruden.
    - Hvis du vil redigere en eksisterende politik: Vælg politikken i listeruden.

1. Udfyld følgende felter i hovedet for den nye eller valgte politik:

    - **Politiknavn** – Angiv et navn til politikken.
    - **Beskrivelse** – Angiv en kort beskrivelse af politikken.

1. Knyt feltnavne til program-id'er ifølge den aktuelle politik under hovedet i oversigtspanelet. Brug knapperner på værktøjslinjen til at tilføje og fjerne rækker efter behov. På hver række skal du angive følgende felter:

    - **Felt** – Vælg eller angiv det inputfelt for mobilappen, som den indgående værdi skal tildeles. Værdien af det viste navn, som arbejdere kan se. Det er i stedet det nøglenavn, der tildeles feltet i den underliggende kode. Standardopsætningen indeholder en samling felter, der sandsynligvis vil være nyttige, og indeholder nøglenavne for hvert felt og tilsvarende programmerede funktionalitet. Du skal måske ændre indstillinger til dine udviklingspartnere for at finde de rette indstillinger for implementeringen.
    - **Program-id** – Vælg det relevante program-id som defineret på siden **GS1-program-id'er**. Id'et fastlægger, hvordan stregkoden fortolkes og gemmes som en værdi for det navngivne felt. Når du har valgt et program-id, viser feltet **Beskrivelse** beskrivelsen af det.
    - **Sortering** – De enkelte stregkode med flere værdier indeholder en række af program-id'er, som hver efterfølges af en værdi. Den gældende GS1-politik identificerer, hvilket program-id der er knyttet til hvert enkelt databasefelt. Hvis en stregkode bruger samme program-id mere end én gang, bruger systemet den rækkefølge, som program-id'er vises i i koden, til at knytte dem til felter. For rækker, der deler et program-id med en eller flere andre rækker, kan du bruge dette felt til at fastsætte den rækkefølge, som de tilsvarende rækker behandles i. Den række, der har den laveste sorteringsværdi, behandles først.

> [!NOTE]
> For stregkoder, der indeholder mere end ét identisk program-id, *skal* du bruge feltet **Sortering** til at fastlægge rækkefølgen af felterne.

## <a name="assign-gs1-policies-to-mobile-device-menu-items"></a>Tildele GS1-politikker til menupunkter for mobilenheder

Alle menupunkter for mobilenheder indeholder som standard inputfelter, hvor arbejderne kan scanne en enkelt værdi ifølge den generiske GS1-opsætning. Hvis arbejdere skal kunne scanne mere end én feltværdi i én enkelt scanning for ethvert menupunkt for mobilenheder, skal du tildele en GS1-politik ved at følge disse trin.

1. Gå til **Warehouse Management \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Opret eller åbn et menupunkt.
1. Angiv feltet **GS1-politik** til den politik, der gælder for menupunktet, i oversigtspanelet **Generelt**.

## <a name="gs1-setup-example"></a>Eksempel på GS1-opsætning

Dette eksempel gælder for et system, hvor GS1-indstillingerne er angivet på følgende måde:

- På siden **Parametre for Warehouse management** angives følgende globale indstillinger:

    - **FNC1-tegn:** *\]C1*
    - **Gruppeseparator:** *\~*

- På siden **GS1-program-id'er** er følgende program-id'er relevante for dette eksempel.

    | Programidentifikator | Betegnelse | Fast længde | Længde | Type | Decimal |
    |---|---|---|---|---|---|
    | 01 | GTIN (Global Trade Identification Number) | Udvalgt | 14 | Numerisk | Afstemt |
    | 10 | Batchnummer | Afstemt | 20 | Alfanumerisk | Afstemt |
    | 17 | Udløbsdato | Udvalgt | 6 | Dato | Afstemt |
    | 30 | Modtaget antal | Afstemt | 8 | Numerisk | Afstemt |

- På siden **Generisk GS1-opsætning** er følgende indstillinger for den generiske GS1-politik relevante for dette eksempel.

    | Felt | Programidentifikator | Betegnelse |
    |---|---|---|
    | ItemId | 01 | GTIN (Global Trade Identification Number) |

- På siden **GS1-politik** er der en politik, når feltet **Politiknavn** er angivet til *Modtagelse af indkøb*. Denne politik inkluderer følgende linjer.

    | Felt | Programidentifikator | Betegnelse | Sortering |
    |---|---|---|---|
    | ExpDate | 17 | Udløbsdato | 0 |
    | InventBatchId | 10 | Batchnummer | 0 |
    | Antal | 30 | Modtaget antal | 0 |

- På siden **Menupunkter for mobilenhed** er der et menupunkt med navnet *Modtagelse af indkøb*. Feltet **GS1-politik** er angivet til *Modtagelse af indkøb*.

Når varerne for en indkøbsordre ankommer til lagerstedet, følger arbejderen disse trin.

1. Vælg menupunktet **Modtagelse af indkøb** på mobilenheden.
1. Angiv indkøbsordrens nummer.
1. Vælg feltet **Vare**, og scan følgende stregkode: `]C10100000012345678~3030~10b1~17220215`.

På grund af de indstillinger, der er oprettet for dette eksempel, fortolker systemet den scannede stregkode på følgende måde.

| Feltnøgle | Applikations-id | Værdi | Bemærk! |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Da arbejderen har scannet til feltet **Vare**, knyttes den første værdi i stregkoden til dette felt. Tilknytningen er taget fra den generiske GS1-opsætning. |
| Antal | 30 | 30 | Da flere feltværdier registreres i en enkelt scanning, hentes denne tilknytning og alle resterende tilknytninger fra den GS1-politik, der er knyttet til menupunktet **Modtagelse af indkøb**. Denne værdi er det antal, der er modtaget. |
| InventBatchId | 10 | b1 | Denne værdi er batch-id'et. |
| ExpDate | 17 | 220215 | Datoformatet er ÅÅMMDD. Udløbsdatoen er derfor 15. februar 2022. |

Modtagelsen registreres derefter, og de relevante databaseværdier angives efter den enkelte scanning.
