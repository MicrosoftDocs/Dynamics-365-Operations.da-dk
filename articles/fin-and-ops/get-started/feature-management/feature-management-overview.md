---
title: Oversigt over funktionsstyring
description: Dette emne beskriver funktionen Administration af funktioner, og hvordan du kan bruge den.
author: mikefalkner
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: b200156a623c67a562cc1a5952899e3a77517528
ms.sourcegitcommit: bbc9aa0d6b94a942e1f4d5b038601509dcc87937
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/05/2019
ms.locfileid: "1619138"
---
# <a name="feature-management-overview"></a>Oversigt over funktionsstyring

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Funktioner tilføjes og opdateres i alle versioner af Microsoft Dynamics 365 for Finance and Operations. Administration af funktioner indeholder et arbejdsområde, hvor du kan få vist en liste over de funktioner, der er leveret i hver version. Nye funktioner er som standard slået fra. Du kan bruge arbejdsområdet til at aktivere dem og få vist dokumentationen til dem.

## <a name="the-feature-management-workspace"></a>Arbejdsområdet Administration af funktioner

Du kan åbne arbejdsområdet **Administration af funktioner** ved at vælge det relevante felt i dashboardet. Der vises en side med en liste over funktioner for alle de versioner, der understøttes af Administration af funktioner. Med tiden vil Microsoft forbedre Administration af funktioner med yderligere funktionalitet, der kan hjælpe dig med at administrere funktioner.

Funktionslisten indeholder følgende oplysninger:

- **Funktionsnavn** – En beskrivelse af den funktion, der blev tilføjet.
- **Aktiveret status** – Et symbol angiver, om en funktion er slået til (markeret), ikke er slået til (ikke markeret), er planlagt til at blive slået til (ur) eller bliver slået til obligatorisk (lås). Den indstilling, der vises her, bruges til alle juridiske enheder. Bemærk, at selv når en funktion er slået til, styres den stadig af sikkerhed. Derfor er funktionen kun tilgængelig for brugere, der har adgang til den, baseret på brugernes sikkerhedsrolle. Den vil også kun være tilgængelig i juridiske enheder, som brugeren har adgang til.
- **Aktiveringsdato** – Den dato, hvor funktionen blev slået til eller er planlagt til at blive slået til.
- **Tilføjelse af funktion** – Den dato, hvor funktionen blev føjet til dit miljø. Denne dato angives automatisk, når du opdaterer dit miljø under de månedlige frigivelsescyklusser.
- **Modul** – Det modul, der påvirkes af den nye funktion.

Når du vælger en funktion, vises der flere oplysninger i detaljeruden til højre for funktionslisten. Øverst i ruden kan du se funktionsnavnet, den dato, hvor funktionen blev tilføjet, det modul, der påvirkes af funktionen, og linket **Få mere at vide**. Vælg dette link for at få vist dokumentationen til funktionen. Hvis dokumentationen ikke er tilgængelig, åbnes en midlertidig side. Detaljeruden indeholder også et **Bemærkninger** felt, hvor du kan tilføje dine egne kommentarer om funktionen.

Arbejdsområdet **Administration af funktioner** indeholder også flere faner, som hver især har en liste over funktioner.

- **Ny** – Denne fane viser alle de funktioner, der er blevet tilføjet siden den seneste månedlige opdatering. Hvis du har sprunget en månedlig opdatering over, viser fanen alle de nye funktioner, der er blevet tilføjet, siden du sidst opdaterede. De nyeste funktioner vises øverst på listen. Det samlede antal nye funktioner vises også på et felt øverst på siden.
- **Ikke aktiveret** – Denne fane viser alle de funktioner, der ikke er slået til. De nyeste funktioner vises øverst på listen. Det samlede antal nye funktioner, der ikke er slået til, vises også på et felt øverst på siden.
- **Planlagt** – Denne fane viser alle funktioner, der er planlagt til at blive aktiveret i fremtiden. De funktioner, der har den tidligste planlagte dato, vises øverst på listen. Det samlede antal planlagte nye funktioner vises også på et felt øverst på siden.
- **Alle** – Denne fane viser alle funktioner. De nyeste funktioner vises øverst på listen.

## <a name="turn-on-a-feature"></a>Aktivere en funktion

Hvis en funktion ikke er slået til, vises knappen **Aktiver nu** i detaljeruden. Du kan bruge denne knap til at slå funktionen til.

- Vælg den funktion, du vil slå til, og vælg derefter **Aktiver nu** i detaljeruden. Funktionen slås til.

Nogle funktioner kan ikke slås fra, når du har slået dem til. Hvis den funktion, du forsøger at slå til, ikke kan slås fra, får du vist en advarsel. På dette tidspunkt kan du vælge **Annuller** for at annullere handlingen og lade funktionen være slået fra. Hvis du vælger **Aktiver** for at slå funktionen til, kan du dog ikke slå den fra senere.

Når en funktion er slået til, vises der en meddelelse under linket **Få mere at vide** i detaljeruden. Denne meddelelse angiver enten, at funktionen er slået til, eller angiver den fremtidige dato, hvor funktionen er planlagt til at blive slået til. Meddelelsen vises, hver gang du vælger funktionen på funktionslisten.

Funktioner, der er planlagt til at blive aktiveret i fremtiden, vises under fanen **Planlagt**. En batchproces slår dem til ved midnat den angivne dato på baggrund af den tidszone, der er repræsenteret af systemdatoen.

## <a name="reschedule-a-feature"></a>Omplanlægge en funktion

Hvis det er planlagt, at en funktion skal aktiveres i fremtiden, vises knappen **Planlæg** i detaljeruden. Du kan bruge denne knap til at ændre værdien i **Aktiveringsdato** til en anden dato.

1. Vælg den planlagte funktion, og vælg derefter **Planlæg** i detaljeruden.
2. Angiv den nye dato, hvor funktionen skal aktiveres, i feltet **Aktiveringsdato** i den dialogboks, der vises.
3. Vælg **Aktiver** for at omplanlægge funktionen eller **Deaktiver** for at annullere planlægningen.

## <a name="turn-off-a-feature"></a>Deaktivere en funktion

Hvis en funktion allerede er slået til, vises knappen **Deaktiver** i detaljeruden. Du kan bruge denne knap til at slå funktionen fra. Knappen **Deaktiver** er ikke tilgængelig, hvis funktionen ikke kan slås fra, når den først er slået til.

- Vælg den funktion, du vil slå fra, og vælg derefter **Deaktiver** i detaljeruden. Funktionen deaktiveres, og feltet **Aktiveringsdato** ryddes.

Når en funktion er slået fra, vises der en meddelelse under linket **Få mere at vide** i detaljeruden. Denne meddelelse angiver, at funktionen endnu ikke er slået til. Meddelelsen vises, hver gang du vælger funktionen på funktionslisten. Funktioner, der ikke er slået til, vises under fanen **Ikke aktiveret**.

## <a name="features-that-must-be-turned-on"></a>Funktioner, der skal slås til

Sommetider findes der en vigtig funktion, som skal slås til automatisk, når du foretager en opdatering. Disse funktioner aktiveres automatisk på den dato, der er angivet i feltet **Aktiveringsdato**. For disse funktioner vises der en meddelelse under linket **Få mere at vide** i detaljeruden. Denne meddelelse angiver enten, at funktionen er slået til, eller angiver den fremtidige dato, hvor funktionen bliver slået til. Meddelelsen vises, hver gang du vælger funktionen på funktionslisten.

## <a name="turn-on-all-features-automatically"></a>Aktivere alle funktioner automatisk

Alle de funktioner, der føjes til dit miljø, er som standard slået fra, medmindre de er obligatoriske funktioner. Men hvis du automatisk vil aktivere alle nye funktioner, kan du bruge rullelisten under titlen på arbejdsområdet til at ændre, hvad der sker, når der tilføjes nye funktioner.

- Vælg **Alle nye funktioner aktiveres som standard**, så alle nye funktioner automatisk aktiveres, når de føjes til miljøet.
- Vælg **Alle nye funktioner deaktiveres som standard**, så alle nye funktioner automatisk deaktiveres, når de føjes til miljøet.

## <a name="assigning-roles"></a>Tildeling af roller

Arbejdsområdet **Administration af funktioner** kan åbnes af systemadministratorer og også af brugere, der er tildelt rollen som funktionsleder eller funktionsseer. Disse to roller er oprettet for at understøtte funktionsstyringsoplevelsen. Brugere i rollen funktionsleder kan aktivere eller deaktivere enhver funktion. De kan også opdatere feltet **Kommentarer** for funktionen. Brugere i rollen funktionsseer kan kun se arbejdsområdet **Administration af funktioner**. De kan ikke slå funktioner til eller fra.

Rollerne som funktionsleder og funktionsseer tilsidesætter ikke den eksisterende sikkerhed, en bruger har. De styrer blot, om brugeren kan slå funktioner til og fra. De giver ikke adgang til selve funktionerne.

## <a name="features-that-use-configuration-keys"></a>Funktioner, der bruger konfigurationsnøgler

Hvis en funktion bruger en konfigurationsnøgle, men konfigurationsnøglen ikke er slået til, viser arbejdsområdet **Administration af funktioner** ikke funktionen på listen over tilgængelige funktioner. Når du har slået konfigurationsnøglen til, skal du opdatere funktionslisten ved hjælp af menupunktet **Kontrollér, om der er opdateringer**. Funktionen vises derefter på listen over funktioner.

Hvis du slår konfigurationsnøglen fra, fjernes den pågældende funktion ikke fra funktionslisten.

## <a name="data-entities"></a>Dataenheder

Med dataenheden **Administration af funktioner** får du mulighed for at eksportere indstillingerne for administration af funktioner fra ét miljø og derefter importere dem til et andet miljø. Denne enhed opdaterer kun eksisterende funktioner. Forretningslogikken i enheden bidrager også til at garantere, at de samme regler, der bruges i arbejdsområdet til **Administration af funktioner**, anvendes, når importen udføres. Du kan f.eks. ikke tilsidesætte en obligatorisk funktionsindstilling ved at fjerne datoen under importen.

Følgende eksempler beskriver, hvad der sker, når du bruger enheden **Administration af funktioner** til at importere data.

- Hvis du ændrer værdien i feltet **Aktiveret** til **Ja**, slås funktionen til, og feltet **Aktiveringsdato** indstilles til dags dato.
- Hvis du ændrer værdien i feltet **Aktiveret** til **Nej** eller lader feltet **EnableDate** være tomt, slås funktionen fra, og feltet **Aktiveringsdato** ryddes. Du kan ikke deaktivere en funktion eller en funktion, der ikke kan slås fra, efter at den er slået til.
- Hvis du ændrer værdien i feltet **EnableDate** til en fremtidig dato, bliver funktionen planlagt til den pågældende dato.
- Hvis du ændrer værdien i feltet **Aktiveret** til **Ja** og ændrer værdien i feltet **EnableDate** til en fremtidig dato, planlægges funktionen til denne dato. 
- Hvis du ændrer værdien i feltet **Aktiveret** til **Nej** og samtidig ændrer værdien i feltet **EnableDate** til en fremtidig dato, planlægges funktionen til denne dato.
- Hvis en funktion er slået til, og du tilføjer et **EnableDate**-felt, der er angivet til en fremtidig dato, forbliver funktionen aktiveret. Hvis du vil planlægge denne funktion på ny, skal du ændre feltet **Aktiveret** til **Nej**.

## <a name="feature-management-and-flighting"></a>Administration af funktioner og flighting

Med Administration af funktioner kan du styre de funktioner, der leveres i hver udgave. Flighting gør det muligt for Microsoft Teams at frigive funktioner til et begrænset antal kunder, så disse funktioner kan testes og valideres, uden at det påvirker alle kunder. Administration af funktioner styrer ikke flighting af nogen funktioner.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>Bruge Administration af funktioner til at slå ISV-funktioner eller brugerdefinerede funktioner til

Funktionsstyring er i øjeblikket ikke tilgængelig for funktioner fra uafhængige softwareleverandører (ISV'er) og brugerdefinerede funktioner. Microsoft tilføjer dog flere funktioner til forbedring af funktionsstyring. Når disse forbedringer er gennemført, vil Microsoft gøre Administration af funktioner tilgængelig for alle funktioner og give vejledning i opdatering af funktionerne, så de kan bruge det.
