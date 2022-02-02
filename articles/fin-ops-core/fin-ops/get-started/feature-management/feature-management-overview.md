---
title: Oversigt over funktionsstyring
description: Dette emne beskriver funktionsstyring, og hvordan du kan bruge den.
author: Peakerbl
ms.date: 01/10/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 6605fe68576ce80726438b60c1f1fbf3782d0934
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984453"
---
# <a name="feature-management-overview"></a>Oversigt over funktionsstyring

[!include [banner](../../includes/banner.md)]

Funktioner tilføjes og opdateres i alle versioner. Administration af funktioner indeholder et arbejdsområde, hvor du kan få vist en liste over de funktioner, der er leveret i hver version. Du kan derefter bruge arbejdsområdet til at få vist funktionsdokumentation og aktivere eller deaktivere funktioner.

## <a name="the-feature-management-workspace"></a>Arbejdsområdet Administration af funktioner

Du kan åbne arbejdsområdet **Administration af funktioner** ved at vælge det relevante felt i dashboardet. Der vises en side med en liste over funktioner for alle de versioner, der understøttes af Administration af funktioner. 

Funktionslisten indeholder følgende oplysninger:

- **Funktionsnavn** – En beskrivelse af den funktion, der blev tilføjet.
- **Status** – Et symbol angiver, om en funktion er slået til (markeret), er slået fra (tom), er planlagt til at blive slået til (ur), er obligatorisk (lås), kræver handling, før du slår den til (advarselssymbol) eller ikke kan aktiveres (X). Den indstilling, der vises, bruges til alle juridiske enheder. Bemærk, at selv når en funktion er slået til, styres den stadig af sikkerhed. Derfor er funktionen kun tilgængelig for brugere, der har adgang til den, baseret på brugernes sikkerhedsrolle. Den vil også kun være tilgængelig i juridiske enheder, som brugeren har adgang til.
- **Aktiveringsdato** – Den dato, hvor funktionen blev slået til eller er planlagt til at blive slået til.
- **Tilføjelse af funktion** – Den dato, hvor funktionen blev føjet til dit miljø. Denne dato angives automatisk, når du opdaterer dit miljø under de månedlige frigivelsescyklusser.
- **Funktionstilstand** – Den aktuelle livscyklustilstand for funktionen: **Forhåndsversion**, **Frigivet** (vist som tom), **Som standard slået til** og **Obligatorisk**. Der er flere detaljer om tilstande senere i dette emne. 
- **Modul** – Det modul, der påvirkes af den nye funktion.

> [!NOTE]
> Kolonnen **Funktionstilstand** er medtaget fra og med version 10.0.21.

Når du vælger en funktion, vises der flere oplysninger i detaljeruden til højre for funktionslisten. Øverst i ruden kan du se funktionsnavnet, den dato, hvor funktionen blev tilføjet, det modul, der påvirkes af funktionen, og linket **Få mere at vide**. Vælg dette link for at få vist dokumentationen til funktionen. Hvis dokumentationen ikke er tilgængelig, åbnes en midlertidig side. Detaljeruden indeholder også et **Bemærkninger** felt, hvor du kan tilføje dine egne kommentarer om funktionen.

Arbejdsområdet **Administration af funktioner** indeholder også flere faner, som hver især har en liste over funktioner.

- **Ny** – Denne fane viser alle de funktioner, der er blevet tilføjet siden den seneste månedlige opdatering. Hvis du har sprunget en månedlig opdatering over, viser fanen alle de nye funktioner, der er blevet tilføjet, siden du sidst opdaterede. De nyeste funktioner vises øverst på listen. Det samlede antal nye funktioner vises også på et felt øverst på siden.
- **Ikke aktiveret** – Denne fane viser alle de funktioner, der ikke er slået til. De nyeste funktioner vises øverst på listen. Derudover viser et felt øverst på siden det samlede antal nye funktioner, der aktuelt er deaktiveret.
- **Planlagt** – Denne fane viser alle funktioner, der er planlagt til at blive aktiveret i fremtiden. De funktioner, der har den tidligste planlagte dato, vises øverst på listen. Desuden viser et felt øverst på siden det samlede antal planlagte funktioner.
- **Alle** – Denne fane viser alle funktioner. De nyeste funktioner vises øverst på listen.

## <a name="feature-states"></a>Funktionstilstande
Funktioner kan skifte mellem flere stater, fra de introduceres i Funktionsstyring til det tidspunkt, hvor de bliver obligatoriske i produktet. I dette afsnit beskrives de gyldige funktionstilstande.

### <a name="preview-features-optional"></a>Prøveversionsfunktioner (valgfri)

Produktteams kan beslutte, at en ny funktion skal starte som en prøveversionsfunktion. Prøveversionsfunktioner er ikke aktiverede som standard, og de er valgfrie. Ejerproduktteamet opdaterer funktioner til frigivet, efter at de har fuldført en vellykket forhåndsversionsperiode.

> [!NOTE]
> Prøveversionsfunktioner er underlagt specifikke [vilkår og betingelser](https://go.microsoft.com/fwlink/?linkid=2105274) for forhåndsversioner. 

### <a name="released-features-optional"></a>Frigivne funktioner (valgfrie)

Kolonnen **Funktionstilstand** er tom for disse funktioner. Funktioner, der i første omgang tilføjes som frigivne, er som standard ikke aktiverede, og aktivering af dem er valgfri. Funktioner, der opdateres fra forhåndsversion, vil bevare aktiveringsstatussen.

### <a name="on-by-default-features-optional"></a>Slået til som standard-funktioner (valgfrit)

Funktioner, der opdateres til **Som standard slået til**, er aktiveret som standard, men de kan deaktiveres. Når funktioner, der kan deaktiveres, har været i **Frigivet** tilstand i mindst seks måneder, forventes de at flytte til denne tilstand i næste større version. Funktioner, som skifter til **Som standard slået til**, forventes at blive omtalt i emnet [Nyheder](../whats-new-changed.md) i frigivelsen. Opdateringen startes af ejerproduktteamet.

> [!NOTE]
> Da disse funktioner aktiveres automatisk, er det vigtigt, at du afgør, om din organisation er klar til at aktivere disse funktioner igen, eller om der kræves mere tid. Hvis der kræves mere tid, kan det være nødvendigt midlertidigt at deaktivere disse funktioner. Bemærk, at en funktions skifte til **Som standard slået til** typisk sker i den større version, før funktionen skal være **Obligatorisk**. På dette tidspunkt har du ikke mulighed for at deaktivere funktionen. 

### <a name="mandatory"></a>Obligatorisk

**Obligatorisk** er den forventede sidste tilstand for funktioner. Den angiver, at funktionerne er aktiveret, og at du ikke kan deaktivere dem uden at kontakte Microsoft. Det forventes, at valgfrie funktioner bliver obligatoriske efter to større versioner. Kritiske funktioner kan som en undtagelse introduceres som obligatoriske.

## <a name="example-of-expected-feature-lifecycles"></a>Eksempel på forventede funktionslivscyklusser

Funktioner, der kan deaktiveres, og som er tilføjet som frigivet og valgfri før eller som en del af aprilversionen, forventes som standard at blive **Som standard slået til** i den følgende version til oktober. De forventes derefter at være **Obligatoriske** i april det følgende år.

Funktioner, der ikke kan deaktiveres, og som er tilføjet som frigivet og valgfri før eller som en del af aprilversionen, forventes som standard at blive **Obligatorisk** i april det efterfølgende år.

## <a name="enable-a-feature"></a>Aktivere en funktion

Hvis en funktion ikke er slået til, vises knappen **Aktivér nu** i detaljeruden. Du kan bruge denne knap til at aktivere funktionen.

Nogle funktioner kan ikke deaktiveres, når du har aktiveret dem. Hvis den funktion, du forsøger at slå til, ikke kan aktiveres, får du vist en advarsel. På dette tidspunkt kan du vælge **Annuller** for at annullere handlingen og lade funktionen være deaktiveret. Hvis du vælger **Aktiver** for at aktivere funktionen, kan du dog ikke deaktivere den senere.

Nogle funktioner viser en meddelelse, der indeholder yderligere oplysninger, før du aktiverer dem. Disse funktioner er angivet med et gult advarselssymbol. Du bør læse de yderligere oplysninger omhyggeligt for bedre at forstå, hvad der vil ske, når funktionen er aktiveret. Du kan dog stadig vælge **Aktivér** for at aktivere funktionen.

Nogle funktioner viser en meddelelse om, at funktionen ikke kan aktiveres, før der er foretaget en handling. Disse funktioner er angivet med et rødt X-symbol. Du skal foretage de handlinger, der er anført i beskrivelsen, før funktionen aktiveres. Hvis du for eksempel ikke kan bruge en funktion, før en konfigurationsnøgle er deaktiveret, skal du først deaktivere konfigurationsnøglen og derefter vende tilbage til funktionsstyring for at aktivere funktionen.

Når en funktion er aktiveret, vises der en meddelelse under linket **Få mere at vide** i detaljeruden. Denne meddelelse angiver enten, at funktionen er aktiveret, eller angiver den fremtidige dato, hvor funktionen er planlagt til at blive aktiveret. Meddelelsen vises, hver gang du vælger funktionen på funktionslisten.

Funktioner, der er planlagt til at blive aktiveret i fremtiden, vises under fanen **Planlagt**. En batchproces aktiverer dem ved midnat den angivne dato på baggrund af den tidszone, der er repræsenteret af systemdatoen.

## <a name="reschedule-a-feature"></a>Omplanlægge en funktion

Hvis det er planlagt, at en funktion skal aktiveres i fremtiden, vises knappen **Tidsplan** i detaljeruden. Du kan bruge denne knap til at ændre værdien i **Aktiveringsdato** til en anden dato.

1. Vælg den planlagte funktion, og vælg derefter **Planlæg** i detaljeruden.
2. Angiv den nye dato, hvor funktionen skal aktiveres, i feltet **Aktiveringsdato** i den dialogboks, der vises.
3. Vælg **Aktiver** for at omplanlægge funktionen eller **Deaktiver** for at annullere planlægningen.

## <a name="disable-a-feature"></a>Deaktivere en funktion

Hvis en funktion er aktiveret, vises knappen **Deaktiver** i detaljeruden. Du kan bruge denne knap til at deaktivere funktionen. Knappen **Deaktiver** er ikke tilgængelig, hvis funktionen ikke kan deaktiveres. 

Når en funktion er deaktiveret, vises der en meddelelse under linket **Få mere at vide** i detaljeruden. Denne meddelelse angiver, at funktionen ikke er aktiveret. Meddelelsen vises, hver gang du vælger funktionen på funktionslisten. Funktioner, der ikke er aktiveret, vises under fanen **Ikke aktiveret**.

## <a name="features-that-must-be-enabled"></a>Funktioner, der skal aktiveres

Sommetider findes der en vigtig funktion, som skal aktiveres automatisk, når du foretager en opdatering. Disse funktioner aktiveres automatisk på den dato, der er angivet i feltet **Aktiveringsdato**. For disse funktioner vises der en meddelelse under linket **Få mere at vide** i detaljeruden. Denne meddelelse angiver enten, at funktionen er aktiveret, eller angiver den dato, hvor funktionen bliver aktiveret. Meddelelsen vises, hver gang du vælger funktionen på funktionslisten.

## <a name="enable-all-features"></a>Aktivér alle funktioner

Du kan aktivere alle funktioner ved at vælge knappen **Aktivér alle**. 

Når du vælger **Aktivér alle**, vises en indstilling, hvor du skal angive følgende oplysninger:

- En liste over alle funktioner, der kræver bekræftelse, før de kan aktiveres. Hvis du vil aktivere funktionerne på listen, skal du vælge **Ja** for knappen **Aktivér funktioner, der kræver bekræftelse**.
- Der vises en liste over alle funktioner, der ikke kan aktiveres. Disse funktioner vil ikke blive aktiveret.

Alle funktioner, der kan aktiveres, vil blive aktiveret. Hvis en funktion allerede er planlagt til at blive aktiveret i fremtiden, vil tidsplanen ikke blive ændret. 

## <a name="enable-all-features-automatically"></a>Aktivere alle funktioner automatisk

Hvis du automatisk vil aktivere alle nye funktioner, kan du bruge rullelisten under titlen på arbejdsområdet til at ændre, hvad der sker, når der tilføjes nye funktioner.

- Vælg **Aktivér nye funktioner automatisk**, så alle nye funktioner automatisk aktiveres, når de føjes til miljøet.
- Vælg **Aktivér ikke nye funktioner automatisk**, så alle nye funktioner som standard er slået fra, når de føjes til miljøet.

Når du aktiverer alle funktionerne automatisk, aktiveres alle de funktioner, der vil blive aktiveret, når du klikker på knappen **Aktivér alle**. Det vil ikke aktivere de funktioner, der kræver bekræftelse, eller de funktioner, der ikke kan aktiveres, før en handling er udført.

## <a name="check-for-updates"></a>Søg efter opdateringer

Funktioner føjes til dit miljø efter hver opdatering. Du kan dog manuelt søge efter opdateringer ved at klikke på knappen **Søg efter opdateringer**. Enhver funktion, der blev føjet til systemet efter opdateringen, vil blive føjet til listen over funktioner. Hvis en tilgængelig funktion er aktiveret efter en udgivelse, kan du søge efter opdateringer, så funktionen vil blive føjet til din liste.

## <a name="assigning-roles"></a>Tildeling af roller

Arbejdsområdet **Administration af funktioner** kan åbnes af systemadministratorer og også af brugere, der er tildelt rollen som funktionsleder eller funktionsseer. Disse to roller er oprettet for at understøtte funktionsstyringsoplevelsen. Brugere i rollen funktionsleder kan aktivere eller deaktivere enhver funktion. De kan også opdatere feltet **Kommentarer** for funktionen. Brugere i rollen funktionsseer kan kun se arbejdsområdet **Administration af funktioner**. De kan ikke slå funktioner til eller fra.

Rollerne som funktionsleder og funktionsseer tilsidesætter ikke den eksisterende sikkerhed, en bruger har. De styrer blot, om brugeren kan slå funktioner til og fra. De giver ikke adgang til selve funktionerne.

## <a name="features-that-use-configuration-keys"></a>Funktioner, der bruger konfigurationsnøgler

Hvis en funktion bruger en konfigurationsnøgle, men konfigurationsnøglen ikke er slået til, viser arbejdsområdet **Administration af funktioner** ikke funktionen på listen over tilgængelige funktioner. Når du har slået konfigurationsnøglen til, skal du opdatere funktionslisten ved hjælp af menupunktet **Kontrollér, om der er opdateringer**. Funktionen vises derefter på listen over funktioner.

Hvis du slår konfigurationsnøglen fra, fjernes den pågældende funktion ikke fra funktionslisten.

## <a name="data-entities"></a>Dataenheder

Med dataenheden **Administration af funktioner** får du mulighed for at eksportere indstillingerne for administration af funktioner fra ét miljø og derefter importere dem til et andet miljø. Denne enhed opdaterer kun eksisterende funktioner. Forretningslogikken i enheden bidrager også til at garantere, at de samme regler, der bruges i arbejdsområdet til **Administration af funktioner**, anvendes, når importen udføres. Du kan f.eks. ikke tilsidesætte en obligatorisk funktionsindstilling ved at fjerne datoen under importen.

Følgende eksempler beskriver, hvad der sker, når du bruger enheden **Administration af funktioner** til at importere data.

- Hvis du ændrer værdien i feltet **Aktiveret** til **Ja**, aktiveres funktionen, og feltet **Aktiveringsdato** indstilles til dags dato.
- Hvis du ændrer værdien i feltet **Aktiveret** til **Nej** eller lader feltet **EnableDate** være tomt, deaktiveres funktionen, og feltet **Aktiveringsdato** ryddes. Du kan ikke deaktivere en obligatorisk funktion eller en funktion, der ikke kan deaktiveres, efter at den er aktiveret.
- Hvis du ændrer værdien i feltet **EnableDate** til en fremtidig dato, bliver funktionen planlagt til den pågældende dato.
- Hvis du ændrer værdien i feltet **Aktiveret** til **Ja** og ændrer værdien i feltet **EnableDate** til en fremtidig dato, planlægges funktionen til denne dato. 
- Hvis du ændrer værdien i feltet **Aktiveret** til **Nej** og samtidig ændrer værdien i feltet **EnableDate** til en fremtidig dato, planlægges funktionen til denne dato.
- Hvis en funktion er aktiveret, og du tilføjer et **EnableDate**-felt, der er angivet til en fremtidig dato, forbliver funktionen aktiveret. Hvis du vil planlægge denne funktion på ny, skal du ændre værdien af feltet **Aktiveret** til **Nej**.

## <a name="feature-management-and-flighting"></a>Administration af funktioner og flighting

Med Administration af funktioner kan du styre de funktioner, der leveres i hver frigivelse. Flighting gør det muligt for Microsoft Teams at frigive funktioner til et begrænset antal kunder, så disse funktioner kan testes og valideres, uden at det påvirker alle kunder. Administration af funktioner styrer ikke flighting af nogen funktioner.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>Bruge Administration af funktioner til at slå ISV-funktioner eller brugerdefinerede funktioner til

Funktionsstyring er i øjeblikket ikke tilgængelig for funktioner fra uafhængige softwareleverandører (ISV'er) og brugerdefinerede funktioner. Microsoft tilføjer dog flere funktioner til forbedring af funktionsstyring. Når disse forbedringer er gennemført, vil Microsoft gøre Administration af funktioner tilgængelig for alle funktioner og give vejledning i opdatering af funktionerne, så de kan bruge det.

## <a name="frequently-asked-questions-faq"></a>Ofte stillede spørgsmål

### <a name="when-are-features-added-removed-or-changed"></a>Hvornår bliver funktioner tilføjet, fjernet eller ændret? 
Funktioner tilføjes, fjernes og ændres ved hjælp af kodeændringer fra ejerproduktteams. Miljøer skal opdateres for at kunne modtage disse ændringer.

### <a name="does-a-feature-become-mandatory-automatically"></a>Bliver en funktion automatisk obligatorisk? 
Nej, en funktion bliver ikke automatisk obligatorisk. Ejerproduktteams skal foretage en kodeændring.

### <a name="why-isnt-there-a-specific-mandatory-enabled-date"></a>Hvorfor er der ikke en specifik 'obligatorisk aktiveringsdato'? 
Timing af opdateringsfrigivelse er variabel, timing af miljøopdateringer er variabel, og kunder kan vælge at springe visse opdateringer over. Derfor er det vanskeligt at fastlægge bestemte datoer. 

### <a name="wheres-the-documentation-for-features-that-are-mandatory"></a>Hvor er dokumentationen til de funktioner, der er obligatoriske? 
Denne dokumentation kommer fra de enkelte Dynamics 365-programteams. Disse funktioner nævnes ofte i [Opdateringer til klientfunktiontilstande](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/updates-client-feature-states) eller [Fjernede eller udfasede funktioner](../../../dev-itpro/migration-upgrade/deprecated-features.md). 

### <a name="is-there-an-in-product-notification-or-signal-that-a-feature-is-going-to-be-mandatory-enabled"></a>Er der en besked i produktet eller et signal om, at en funktion skal være obligatorisk? 
I dag findes der ikke en beskedmekanisme, der vedrører, at funktionen er obligatorisk.

### <a name="do-features-ever-get-enabled-without-the-customer-knowing-about-it"></a>Kan funktioner blive aktiveret, uden at kunden kender til det? 
Ja, funktioner kan aktiveres uden kundens viden i følgende situationer:
- En funktion skifter til **Som standard slået til**. I denne tilstand kan funktionen stadig deaktiveres. 
- En funktion opdateres til **Obligatorisk**. Denne ændring vil kun ske i kombination med en større version. Kritiske funktioner kan som en undtagelse blive flyttet til **Obligatorisk** ved enhver opdatering.

### <a name="what-is-feature-flighting-and-how-does-it-relate-to-feature-management"></a>Hvad er funktions-flighting, og hvordan er den relateret til funktionsstyring? 
Funktions-flights er til/fra-parametre i realtid, som Microsoft kontrollerer. De er adskilt fra den kundestyring, der leveres af Funktionsstyring. 
- Funktioner i private prøveversioner vises ikke i Funktionsstyring, før de er flighted på. I produktionen skal kunden aftale at være en del af et særligt program, før dette kan ske.
- Offentlig prøveversion og frigivne funktioner (generelt tilgængelige) vises i Funktionsstyring, medmindre de er flighted off. Flighting off af en funktion anses for at være en sidste mulighed for produktteams, hvis der findes et vigtigt problem, og det normalt vil være en pr. kunde-operation.

### <a name="do-features-ever-get-flighted-off-without-the-customer-knowing-about-it"></a>Kan funktioner blive flighted off, uden at kunden kender til det? 
Ja, hvis en funktion har indflydelse på funktionaliteten af et miljø, som ikke har en funktionel effekt, kan de som standard aktiveres.

### <a name="how-can-feature-enablement-be-checked-in-code"></a>Hvordan kan funktionsaktivering kontrolleres i kode?
Brug metoden **isFeatureEnabled** på klassen **FeatureStateProvider**, og giv den en forekomst af funktionsklassen. Eksempel: 

```xpp
if (FeatureStateProvider::isFeatureEnabled(BatchContentionPreventionFeature::instance()))
```

### <a name="how-can-feature-enablement-be-checked-in-metadata"></a>Hvordan kan funktionsaktivering kontrolleres i metadata?
Egenskaben **FeatureClass** kan bruges til at angive, at visse metadata er knyttet til en funktion. Det klassenavn, der bruges til funktionen, skal bruges, f.eks. **BatchContentionPreventionFeature**. Disse metadata er kun synlige i denne funktion. Egenskaben **FeatureClass** er tilgængelig i menuer, menupunkter, fasttekstværdier og tabel-/visningsfelter.

### <a name="what-is-a-feature-class"></a>Hvad er en funktionsklasse?
Funktioner i funktionsstyring er defineret som *funktionsklasser*. En funktionsklasse **implementerer IFeatureMetadata** og bruger funktionsklasseattributten til at identificere sig selv i arbejdsområdet Funktionsstyring. Der findes mange eksempler på tilgængelige funktionsklasser, som kan kontrolleres for aktivering i kode ved hjælp af **FeatureStateProvider**-API og i metadata ved hjælp af egenskaben **FeatureClass**. Eksempel: 

```xpp
[ExportAttribute(identifierStr(Microsoft.Dynamics.ApplicationPlatform.FeatureExposure.IFeatureMetadata))]
internal final class BankCurrencyRevalGlobalEnableFeature implements IFeatureMetadata
```

### <a name="what-is-the-ifeaturelifecycle-implemented-by-some-feature-classes"></a>Hvad er IFeatureLifecycle, der er implementeret af nogle funktionsklasser?
IFeatureLifecycle er en Microsoft-intern mekanisme til angivelse af fasen for funktionslivscyklussen. Funktioner kan være:
- `PrivatePreview` - skal have flight for at være synlig.
- `PublicPreview` – vises som standard, men med en advarsel om, at det er en prøveversionsfunktion.
- `Released` – fuldt frigivet.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
