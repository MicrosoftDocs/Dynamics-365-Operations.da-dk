---
title: GS1-stregkoder og QR-koder
description: Dette emne beskriver, hvordan du opretter GS1-stregkoder og QR-koder, så etiketter kan scannes på et lagersted.
author: Mirzaab
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 702985ef9726690829e35e43d270477be318fc41
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075208"
---
# <a name="gs1-bar-codes-and-qr-codes"></a>GS1-stregkoder og QR-koder

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- Preview until 10.0.25 GA -->

Arbejdere på lagersteder skal ofte udføre flere opgaver, når de bruger en mobilenhedsscanner til at registrere bevægelser for et element, et produkt eller en container. Disse opgaver kan omfatte både scanning af stregkoder og manuel angivelse af oplysninger på mobilenheden. Stregkoderne bruger et firmaspecifikt format, som du kan definere og administrere ved hjælp af Microsoft Dynamics 365 Supply Chain Management.

GS1-stregkode- og QR-kodeformater for forsendelsesetiketter er udviklet til at være en global standard for udvekslingen af data mellem firmaer. GS1-formater indkoder ikke kun dataene, men gør det muligt at bruge en foruddefineret liste over *program-id'er* til at definere betydningen af dataene. GS1-standarden definerer dataformatet og de forskellige typer data, der kan bruges til kodning. I modsætning til ældre stregkoder kan GS1-stregkoder have flere dataelementer. En enkelt stregkodescanning kan derfor registrere flere typer produktoplysninger, f.eks. batchet og udløbsdatoen.

Understøttelse af GS1 i Supply Chain Management forenkler i mærkbart omfang scanningsprocessen på lagersteder, hvor paller og containere mærkes ved hjælp af koder i GS1-format. Lagerarbejdere kan udtrække alle de påkrævede oplysninger via en enkelt scanning af en GS1-stregkode. Hvis du ikke længere behøver at udføre flere scanninger og/eller indtaste oplysninger manuelt, kan GS1-stregkoder reducere den tid, der er forbundet med opgaverne. Samtidig kan de også forbedre præcisionen.

Logistikchefer skal oprette den krævede liste over program-id'er og knytte hver af dem til de relevante menupunkter på mobilenheder. Program-id'erne kan derefter bruges på tværs af lagersteder som en global indstilling til flytnings- og emballeringsformål. Derfor har alle forsendelsesetiketter samme form.

Medmindre andet er anført, henviser udtrykket *stregkode* i dette emne til både stregkoder og QR-koder.

## <a name="turn-on-the-gs1-feature"></a>Slå GS1-funktionen til

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Warehouse Management*
- **Funktionsnavn:** *Scan GS1-stregkoder*

## <a name="set-up-global-gs1-options"></a>Konfigurere globale GS1-indstillinger

Siden **Parametre for lagerstedsstyring** indeholder nogle få indstillinger, der fastlægger globale GS1-indstillinger.

Benyt følgende fremgangsmåde for at angive globale GS1-indstillinger.

1. Gå til **Warehouse Management \> Opsætning \> Parametre til lagerstedsstyring**.
1. Udfyld følgende ekstra felter i oversigtspanelet **Stregkoder**:

    - **FNC1-tegn** – Angiv tegn, der skal fortolkes som et præfiks, når en stregkode fortolkes.
    - **Datamatrix-tegn** – Angiv tegn, der skal fortolkes som et præfiks, når en datamatrix fortolkes.
    - **QR-kodetegn** – Angiv tegn, der skal fortolkes som et præfiks, når en QR-kode fortolkes.
    - **Gruppeseparator** – Angiv det tegn, der identificerer separate dele af en stregkode eller QR-kode.
    - **Maks. længde på id** – Angiv det maksimale antal tegn, der er tilladt for program-id'et.

> [!NOTE]
> Præfikser fortæller systemet, at en stregkode er krypteret ifølge GS1-standarden. Der kan bruges op til tre præfikser (**FNC1-tegn**, **Datamatrix-tegn** og **QR-kodetegn**) samtidigt og til forskellige formål.

## <a name="gs1-application-identifiers"></a>GS1-programidentifikatorer

GS1-formater koder ikke kun dataene, men gør det muligt at bruge en foruddefineret liste over program-id'er til at definere betydningen af dataene. Logistikchefer skal oprette den krævede liste over program-id'er og knytte hver af dem til de relevante menupunkter på mobilenheder. Id'erne kan derefter bruges på tværs af lagersteder som en global indstilling til flytnings- og emballeringsformål. Derfor har alle forsendelsesetiketter samme form.

Systemet bruger dataene, især de foruddefinerede program-id'er, til at fastlægge de regler, der skal anvendes for de relevante oplysninger, der er scannet.

Hvert program-id signalerer til systemet, at efterfølgende tegn i den scannede stregkode skal betragtes som en blok af krypterede oplysninger. Konfigurationen af program-id'erne definerer, hvordan systemet skal tolke en stregkode og gemme den som en værdi i systemet.

Logistikadministratorer kan bruge standard-id'er til internationale programmer og/eller oprette deres egne.

### <a name="load-the-standard-application-identifiers"></a>Indlæse standardprogram-id'erne

Du kan hurtigt komme i gang med at indlæse en liste over almindelige internationale program-id'er. Du kan derefter udvide eller redigere listen senere efter behov.

Benyt følgende fremgangsmåde for at indlæse standardprogram-id'erne.

1. Gå til **Lagerstedsstyring \> Opsætning \> GS1 \> GS1-program-id'er**.
1. Vælg **Opret standardkonfiguration** i handlingsruden.

> [!WARNING]
> Kommandoen **Opret standardopsætning** sletter alle aktuelt definerede program-id'er og erstatter dem med standardlisten. Når du har indlæst standardopsætningen, kan du dog tilpasse listen efter behov.

### <a name="set-up-custom-application-identifiers"></a>Oprette brugerdefinerede program-id'er

Hvis nogle eller alle program-id'er, som din virksomhed bruger, adskiller sig fra standardsættet, kan du oprette dine egne koder fra bunden eller tilpasse standardsættet, som du ønsker.

Benyt følgende fremgangsmåde for at konfigurere og tilpasse dine egne GS1-program-id'er.

1. Gå til **Lagerstedsstyring \> Opsætning \> GS1 \> GS1-program-id'er**.
1. Udfør ét af følgende trin:

    - Vælg **Ny** i handlingsruden for at oprette et nyt id.
    - Hvis du vil redigere et eksisterende id: Vælg id'et, og vælg derefter **Rediger** i handlingsruden.

1. Angiv følgende felter for det nye eller valgte id:

    - **Program-id** – Angiv identifikationskoden for program-id'et. Normalt er denne kode et tocifret heltal, men den kan være længere. Ved decimalværdier angiver det sidste ciffer antallet af decimaler. Du kan finde flere oplysninger under beskrivelsen af afkrydsningsfeltet **Decimal** senere på listen.
    - **Beskrivelse** – Angiv en kort beskrivelse af id'et.
    - **Fast længde** – Markér dette afkrydsningsfelt, hvis værdier, der scannes med dette program-id, har et fast antal tegn. Fjern markeringen i afkrydsningsfeltet, hvis længden på værdier er variabel. I dette tilfælde skal du angive afslutningen på værdien ved at bruge det gruppeseparatortegn, du angav på siden **Parametre for lagerstedsstyring**.
    - **Længde** – Angiv det maksimale antal tegn, der kan vises i de værdier, der scannes ved hjælp af dette program-id. Hvis afkrydsningsfeltet **Fast længde** er markeret, forventes præcist dette antal tegn.
    - **Type** – Vælg den type værdi, der scannes ved hjælp af dette program-id (*Numerisk*, *Alfanumerisk* eller *Dato*). For datoer er det forventede format ÅÅMMDD (uden mellemrum eller bindestreger).
    - **Decimal** – Marker dette afkrydsningsfelt, hvis værdien indeholder et stiltiende decimaltegn. Hvis dette afkrydsningsfelt er markeret, vil systemet bruge det sidste ciffer i program-id'et til at bestemme antallet af decimaler. Hvis program-id'et f.eks. er *3205*, fortolkes værdiens fem cifre yderst til højre efter decimaltegnet.

> [!NOTE]
> Den gruppeseparator, der er angivet på siden **Parametre for lagerstedsstyring**, er valgfri, hvis en værdi, der efterfølges af et program-id, har en fast længde, eller hvis dets længde er maksimeret (dvs. længden er lig med værdien for **Længde**, der er angivet for program-id'et).

## <a name="establish-the-generic-gs1-setup"></a>Oprette den generiske GS1-opsætning

Den generiske GS1-opsætning opretter en samling af fælles tilknytninger. Disse tilknytninger stemmer overens med hvert relevant inputfelt i mobilappen for program-id'et, som bestemmer, hvordan værdier fra scannede stregkoder skal fortolkes og lagres i det pågældende felt. Disse indstillinger anvendes som standard til alle scanninger for alle menupunkter for mobilenheder. De kan dog overskrives for et eller flere specifikke felter af en GS1-politik, der er tildelt et bestemt menupunkt.

Den generiske GS1-opsætning giver kun mulighed for at scanne én værdi ad gangen. Hvis du vil indlæse flere feltværdier fra en enkelt scanning, skal du derfor definere en GS1-politik for de relevante menupunkter.

Du kan finde flere oplysninger om GS1-politikker i næste afsnit.

### <a name="load-the-standard-generic-gs1-setup"></a>Indlæse den generiske GS1-standardopsætning

På siden **Generisk GS1-opsætning** kan du indlæse et standardsæt af tilknytninger mellem felter for mobilenheder og standardprogram-id'er, der er oprettet med standardopsætningen.

Hvis du vil oprette den generiske GS1-opsætning, skal du gå til **Lagerstedsstyring \> Opsætning \> GS1 \> Generisk GS1-opsætning**. Vælg derefter **Opret standardopsætning** for automatisk at tildele et egnet program-id til hvert af de felter, der normalt bruges af menupunkter for mobilenheder.

> [!WARNING]
> Hvis der allerede findes en generisk GS1-opsætning, sletter kommandoen **Opret standardopsætning** fuldstændigt og indlæser standardopsætningen.

### <a name="customize-the-standard-generic-gs1-setup"></a>Tilpasse den generiske GS1-standardopsætning

Benyt denne fremgangsmåde for at tilpasse den generiske GS1-opsætning.

1. Gå til **Lagerstedsstyring \> Opsætning \> GS1 \> Generisk GS1-opsætning**.
1. Udfør ét af følgende trin:

    - Hvis du vil oprette en ny tilknytning; Vælg **Ny** i handlingsruden.
    - Hvis du vil redigere en eksisterende tilknytning: Vælg tilknytningen, og vælg derefter **Rediger** i handlingsruden.

1. Angiv følgende felter for den nye eller valgte tilknytning:

    - **Felt** – Vælg eller angiv det inputfelt for mobilappen, som den indgående værdi skal tildeles. Værdien af det viste navn, som arbejdere kan se. Det er i stedet det nøglenavn, der tildeles feltet i den underliggende kode. Standardopsætningen indeholder en samling felter, der sandsynligvis vil være nyttige, og indeholder nøglenavne for hvert felt og tilsvarende programmerede funktionalitet. Du skal måske ændre indstillinger til dine udviklingspartnere for at finde de rette indstillinger for implementeringen.
    - **Program-id** – Vælg det relevante program-id som defineret på siden **GS1-program-id'er**. Id'et fastlægger, hvordan stregkoden fortolkes og gemmes som en værdi for det navngivne felt. Når du har valgt et program-id, viser feltet **Beskrivelse** beskrivelsen af det.

## <a name="set-up-gs1-policies-that-you-can-assign-to-mobile-device-menu-items"></a>Konfigurere GS1-politikker, som du kan tildele til menupunkter for mobilenheder

Formålet med GS1-standarden er at give arbejdere mulighed for at indlæse flere værdier, når de scanner en enkelt stregkode én gang. Til dette formål skal logistikchefer oprette GS1-politikker, der fortæller systemet, hvordan stregkoder med flere værdier skal fortolkes. Du kan senere tildele politikker til menupunkter for mobilenheder for at styre, hvordan en stregkode fortolkes, når arbejdere scanner den, mens de bruger et bestemt menupunkt.

Hvis der ikke er tildelt en GS1-politik til et menupunkt, kan systemet kun hente en enkelt værdi. Denne værdi anvendes til det mobilappinput, der vælges, når arbejderen foretager scanningen, sådan som det er angivet i den generiske GS1-opsætning. Hvis en GS1-politik er tildelt menupunktet, bruger systemet stadig den generiske GS1-opsætning til at knytte den første stregkodeværdi til det valgte felt. Den kan derefter hente yderligere feltværdier som angivet i den gældende politik.

### <a name="load-the-standard-specific-gs1-policies"></a>Indlæse specifikke GS1-standardpolitikker

Du kan hurtigt indlæse et sæt af GS1-politikker. Du kan derefter udvide eller redigere politikkerne senere efter behov.

Benyt følgende fremgangsmåde for at indlæse standardprogram-id'erne.

1. Gå til **Lagerstedsstyring \> Opsætning \> GS1 \> GS1-poltik**.
1. Vælg **Opret standardkonfiguration** i handlingsruden.

> [!WARNING]
> Kommandoen **Opret standardopsætning** sletter alle aktuelt definerede politikker og erstatter dem med standardsættet af politikker. Når du har indlæst standardopsætningen, kan du dog tilpasse politikkerne efter behov.

### <a name="set-up-custom-specific-gs1-policies"></a>Konfigurere brugerdefinerede specifikke GS1-politikker

Benyt følgende fremgangsmåde for at konfigurere og tilpasse GS1-politikkerne.

1. Gå til **Lagerstedsstyring \> Opsætning \> GS1 \> GS1-poltik**.
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

- På siden **Parametre for lagerstedsstyring** angives følgende globale indstillinger:

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
1. Marker feltet **Vare**, og scan følgende stregkode: *\]C10100000012345678\~3030\~10b1\~17220215*.

På grund af de indstillinger, der er oprettet for dette eksempel, fortolker systemet den scannede stregkode på følgende måde.

| Feltnøgle | Applikations-id | Værdi | Bemærk! |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Da arbejderen har scannet til feltet **Vare**, knyttes den første værdi i stregkoden til dette felt. Tilknytningen er taget fra den generiske GS1-opsætning. |
| Antal | 30 | 30 | Da flere feltværdier registreres i en enkelt scanning, hentes denne tilknytning og alle resterende tilknytninger fra den GS1-politik, der er knyttet til menupunktet **Modtagelse af indkøb**. Denne værdi er det antal, der er modtaget. |
| InventBatchId | 10 | b1 | Denne værdi er batch-id'et. |
| ExpDate | 17 | 220215 | Datoformatet er ÅÅMMDD. Udløbsdatoen er derfor 15. februar 2022. |

Modtagelsen registreres derefter, og de relevante databaseværdier angives efter den enkelte scanning.
