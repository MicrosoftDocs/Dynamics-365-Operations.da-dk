---
title: Arbejde med funktionsopsætninger
description: Denne artikel beskriver, hvordan du konfigurerer funktioner til elektronisk fakturering.
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 23466a53bb8ba597503aaa12d41395fc82b9f14e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904319"
---
# <a name="work-with-feature-setups"></a>Arbejde med funktionsopsætninger

[!include [banner](../includes/banner.md)]

Hvis du vil oprette generering af elektroniske filer og andre behandlingstrin (f.eks. digital signering af filer, afsendelse af dem til den offentlige myndigheds webtjeneste og modtagelse af et svar eller lagring af dem), skal du konfigurere behandlingspipelinen, anvendelighedsregler og variabler for funktioner til elektronisk fakturering.

Opsætningsoplysningerne kombineres i begrebet *funktionsopsætning* og kan oprettes, slettes, ændres. Oplysningerne kan også ses for de fuldførte versioner af funktioner til elektronisk fakturering.

Du kan oprette lige så mange elementer til opsætning af funktioner, som du har brug for, for at definere forskellige scenarier for generering, behandling og modtagelse af elektroniske filer. Selvom disse elementer til opsætning af funktioner har uafhængige behandlingshandlinger og betingelser for udførelse, oprettes de som en del af en enkelt funktion til elektronisk fakturering og nedarver dens livscyklus og installationsproces.

## <a name="add-a-feature-setup"></a>Tilføje en funktionsopsætning

1. Logge på din RCS-konto (Regulatory Configuration Service).
2. I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **Elektronisk fakturering**.
3. På siden **Funktioner til elektronisk fakturering** skal du vælge en elektronisk fakturafunktionsversion med status af **Kladde**.
4. Vælg **Tilføj** på fanen **Opsætninger**.
5. Vælg en af følgende muligheder i feltgruppen **Ny** i dialogboksen **Opret funktionsopsætning**.
 
    - **Brugerdefineret opsætning** – Opret en ny funktionsopsætning med tomme kanaler, en tom behandlingspipelineliste, en tom sektion til anvendelsesregler og et standardsæt af variabler, afhængigt af opsætningstypen.
    - **Fra funktionsopsætning** – Opret en kopi af en anden funktionsopsætning inden for området af den aktuelle funktion til elektronisk fakturering.

6. Hvis du valgte indstillingen **Brugerdefineret opsætning** i det sidste trin, skal du angive et navn til og en beskrivelse af funktionens opsætningselement og derefter vælge en af følgende indstillinger i feltgruppen **Opsætningstype**:

    - **Behandlingspipeline** – Vælg denne indstilling for at generere og behandle udgående elektroniske dokumenter. For denne opsætningstype opretter systemet en tom pipelineliste til behandling, en tom sektion til anvendelsesregler og et standardsæt af variabler. Du kan ikke arbejde med kanalerne til indgående elektroniske dokumenter.
    - **Datakanal** – Vælg denne indstilling for at konfigurere processen til modtagelse af indgående elektroniske dokumenter fra en af de definerede kanaler og overføre dem direkte til Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management uden yderligere handlinger. For denne opsætningstype opretter systemet en foruddefineret liste over parametre for datakanalerne, en tom sektion til anvendelsesregler og et standardsæt af variabler. Du kan ikke tilføje nogen handlinger i behandlingspipelinen.
    - **Datakanal og behandlingspipeline** – Denne opsætningstype ligner opsætningstypen **Datakanal**. Før et indgående elektronisk dokument sendes til Finans eller Supply Chain Management, kan du dog oprette yderligere handlinger i behandlingspipelinen.

7. Hvis du valgte indstillingen **Datakanal** eller **Datakanal og behandlingspipeline** i det sidste trin, skal du vælge den kanal, du vil integrere med, i feltet **Vælg datakanal**.
8. Vælg **Opret**.

Når du har oprettet en funktionsopsætning, kan du vælge **Rediger** for at konfigurere den.

## <a name="edit-a-feature-setup"></a>Redigere en funktionsopsætning

Afhængigt af funktionsopsætningstypen kan du konfigurere processen for generering af udgående elektroniske filer og afsendelse af dem til eksterne kanaler eller modtagelse af indgående dokumenter og overføre dem til dit Finans- eller Supply Chain Management-programmet.

### <a name="data-channel"></a>Datakanal

En *datakanal* tager den elektroniske fil og behandler den eller sender den direkte til Finans eller Supply Chain Management. Denne mulighed er ikke tilgængelig for funktionsopsætninger af typen **Behandlingspipeline**.

Hvis du vil konfigurere en datakanal, skal du angive navnet på kanalen. Definer derefter parametrene på basis af den valgte kanaltype. Datakanal-id'et skal referere til den variabel, der oprettes specifikt for at identificere datakanalen. Det vil blive brugt som reference i Finans eller Supply Chain Management.

Under fanen **Filtre for vedhæftede filer** skal du definere et sæt filtre for at hente specifikke filer fra kanalen. Du kan oprette flere linjer, hvis du forventer, at filerne har forskellige filtypenavne, eller hvis filerne skal behandles forskelligt afhængigt af filnavnet. Her er hovedparametrene:

- **Navn** – Angiv navnet på den fil, som systemet skal referere til under behandlingen. I Finans- og Supply Chain Management-programmer kan du se filerne i overførselsloggen.
- **Filter** – Definer det filter, der skal udvælge filer.
- **Valgfrit** – Hvis markeringen i dette afkrydsningsfelt er fjernet, er filen påkrævet. I dette tilfælde vil systemet vise en fejlmeddelelse, hvis kanalerne ikke indeholder filer, der svarer til filteret. Denne parameter gælder for mails.

Hvis kanalen er en postkasse, og en indgående mail indeholder flere vedhæftede filer, kan du konfigurere regler for at definere, hvordan tjenesten skal håndtere vedhæftede filer. Tjenesten kan behandle hver enkelt vedhæftede fil som en separat elektronisk faktura, eller den kan behandle den ene vedhæftede fil som en hovedfaktura og alle andre vedhæftede filer som tilføjelser.

### <a name="processing-pipeline"></a>Behandling af pipeline

En *behandlingspipeline* er et sæt *handlinger*, der køres i sekvens, indtil de er fuldført korrekt. Du kan bruge en behandlingspipeline til at konfigurere processen til generering af elektroniske filer og udførelse af andre trin (f.eks. digital signering af filer, afsendelse af dem til eksterne webtjenester, fortolkning af svaret og modtagelse og behandling af indgående dokumenter).

Listen over handlinger er foruddefineret. Du kan bruge knapperne **Ny** og **Slet** til at angive den kombination af aktioner, der logisk definerer den nødvendige proces for afsendelse eller modtagelse af dokumenter.

Rækkefølgen af handlingerne er vigtig. Du kan ændre rækkefølgen med knapperne **Op** og **Ned**.

Hver handling har et sæt parametre, du kan konfigurere eller justere. Det specifikke parametersæt afhænger af handlingstypen.

- **Handling** – Vælg handlingstypen.
- **Handlingsnavn** – Angiv navnet på handlingen. Dette navn vises i overførselslogfiler og i meddelelser i Finans- og Supply Chain Management-applikationer.
- **Beskrivelse** – Angiv flere detaljer om formålet med handlingen i processen.
- **Aktivér forsøg igen** – Hvis du markerer dette afkrydsningsfelt, kan du vælge en handling i feltet **Handling for gentagelse** og konfigurere flere parametre under fanen **Gentagelsesparametre**.

    Gentagelsesfunktionen giver dig mulighed for at konfigurere tjenestens funktionsmåde, hvis en bestemt handling ikke kan køres. Hvis den eksterne webtjeneste, du forsøger at oprette forbindelse til, f.eks. ikke svarer, kan du angive, hvor mange gange systemet skal forsøge at få forbindelse, hvilket interval og hvilken handling i behandlingspipelinen der skal bruges.

- **Eksportér resultater** – Du kan markere dette afkrydsningsfelt for *én* handling i behandlingspipelinen. Den elektroniske fil, som handlingen opretter i programmet Finans eller Supply Chain Management, kan derefter eksporteres fra siden **Overførselslog for elektroniske dokumenter**.

### <a name="applicability-rules"></a>Anvendelighedsregler

*Anvendelighedsregler* er konfigurerbare sætninger, der giver kontekst til kørsel af funktioner for elektronisk fakturering via egenskabssættet for elektronisk fakturering.
Når et forretningsdokument fra Finance eller Supply Chain Management sendes til elektronisk fakturering, indeholder det ikke en eksplicit reference, der giver mulighed for, at funktionen Elektronisk fakturering er indstillet til at kalde en bestemt version af elektronisk faktureringsfunktion for at behandle afsendelsen. Når forretningsdokumentet er konfigureret korrekt, indeholder det dog de elementer, der er nødvendige for, at elektronisk fakturering kan bestemme, hvilken funktionsversion til elektronisk fakturering og behandlingspipeline, der skal vælges og køres.

Anvendelsesregler giver mulighed for, at den elektroniske faktureringsservice kan finde de nøjagtige funktioner for elektronisk fakturering, der skal bruges til behandling af indsendelsen. Hvis du vil finde de rigtige funktioner, skal felterne **Kontekst** i det sendte forretningsdokument sammenholdes med delsætninger fra anvendelighedsreglerne.

Du kan arbejde med anvendelighedsregler på følgende måder:

- Vælg **Ny** for at føje en ny delsætning til et sæt af anvendelighedsregler.
- Vælg **Slet** for at slette en delsætning.
- Vælg flere poster, og brug knappen **Gruppér** eller **Opdel gruppe** til at oprette en kombination af elementer eller logiske sætninger. Vælg f.eks. de linjer, du vil gruppere, og vælg derefter **Gruppér delsætning**. Når delsætningerne er grupperet, føjes der en ny kolonne til gitteret. Denne kolonne angiver den logiske operator for den grupperede delsætning. Følgende typer af operatorer understøttes:

    - Lig med
    - Ikke lig med
    - Større end/mindre end
    - Større end eller lig med/mindre end eller lig med
    - Indeholder
    - Begynd med

    > [!NOTE]
    > Når du opdeler en grupperet delsætning, skal du altid starte fra det inderste grupperingsniveau.

### <a name="variables"></a>Variabler

*Variabler* giver dig større fleksibilitet, når du konfigurerer en behandlingspipeline og dataflowet mellem handlinger. Du kan referere til en variabel i nogle handlingsparametre for midlertidigt at gemme data eller elektroniske filer. Nogle variabler bruges til at overføre data mellem applikationerne Finans eller Supply Chain Management og tjenesten til elektronisk fakturering.

Systemet opretter som standard nogle variabler. Variablen **BusinessDocumentDataModel** indeholder f.eks. forretningsdata i en JSON-struktur (JavaScript Object Notation), der kommer i kaldet fra det tilknyttede program under afsendelsesprocessen.

Følgende variabeltyper er tilgængelige:

- **Konstant** – En container til lagring af midlertidige data, der bruges til handlinger i behandling af pipelines.
- **Fra klient** – indholdet af variablen hentes fra Dynamics 365-klienten under udførelsen af indsendelsesprocessen.
- **Til klient** – indholdet af variablen er gjort tilgængelig til import af Dynamics 365-klienten under udførelsen af indsendelsesprocessen.
- **Datatype** – Vælg datatypen for de oplysninger, der er gemt i variablen.

### <a name="parameters"></a>Parametre

Indstillingen **Deaktiver reduktion af forretningsdata** bruges til at optimere strukturen i den nyttelast for forretningsdata, der kommer fra programmet Finans eller Supply Chain Management under afsendelse af elektronisk dokument. Optimering er med til at reducere de data, der bruges i tjenesten Elektronisk fakturering, så de kan blive transformeret til den nødvendige elektroniske fil. Standardværdien er **Nej**.

- **Ja** – Finans eller Supply Chain Management sender en JSON-fil af strukturen **Fakturamodel** eller **Regnskabsmodelstruktur** (for Brasilien), der er defineret i modulet **Elektronisk rapportering**. Alle elementer i modellen er udfyldt med forretningsdata på programsiden, uanset den endelige struktur i den elektroniske fil. Modeller indeholder normalt flere forretningsdata, end målfilstrukturen kræver, og der kan kræves mere tid til at generere disse data i programmet. Værdien **Ja** for denne indstilling er påkrævet i det sjældne tilfælde, hvor du vil generere forskellige outputfiler i én elektronisk faktureringsfunktion og funktionsopsætning. Værdien **Ja** er nyttig, når du foretager fejlfinding i scenarier, strukturen i de elektroniske filer og fuldstændigheden af forretningsdataene.
- **Nej** – Finans eller Supply Chain Management foretager det første kald til tjenesten uden firmadata. Formålet med dette kald er at få oplysninger om ER-konfiguration (Elektronisk Rapportering), der vil blive brugt til elektronisk filtransformation i behandlingspipelinen. Disse oplysninger returneres til programmet, som bruges til at bestemme undersættet af forretningsdata, der skal medtages i JSON-filen i strukturen **Fakturamodel** eller **Regnskabsmodel** (for Brasilien). Værdien **Nej** for denne indstilling hjælper med at reducere mængden af forretningsdata, som programmet sender til tjenesten, da programmet kun kan sende de forretningsdata, der kræves for at generere en elektronisk fil korrekt.

### <a name="validate-a-feature-setup"></a>Validere en funktionsopsætning

Du kan køre validering for at kontrollere konsistensen af hele konfigurationen. Hvis en obligatorisk parameter til en handling f.eks. er tom, registrerer valideringen denne inkonsistens, og du modtager en advarselsmeddelelse.

- På siden **Opsætning af funktionsversion** skal du i handlingsruden vælge **Valider**.

## <a name="delete-a-feature-setup"></a>Slette en funktionsopsætning

1. På siden **Funktioner til elektronisk fakturering** skal du vælge en elektronisk fakturafunktionsversion med status af **Kladde**.
2. Vælg **Slet** under fanen **Konfigurationer**.
3. Vælg **Ja** i det meddelelsesfelt, der vises, for at bekræfte, at du vil slette funktionsopsætningen.
