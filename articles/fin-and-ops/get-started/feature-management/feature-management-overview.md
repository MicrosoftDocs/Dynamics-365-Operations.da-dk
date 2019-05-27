---
title: Oversigt over funktionsstyring
description: Dette emne beskriver funktionen Administration af funktioner, og hvordan du kan bruge den.
author: mikefalkner
manager: AnnBe
ms.date: 04/18/2019
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
ms.openlocfilehash: e75e42926db22d4fccda86c755b12d9d121a9c0e
ms.sourcegitcommit: be447fc81bc874982bc0185fcb4d87d99bd742c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538679"
---
# <a name="feature-management-overview"></a>Oversigt over funktionsstyring

[!include[banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Funktioner tilføjes og opdateres i alle versioner af Microsoft Dynamics 365 for Finance and Operations. Administration af funktioner indeholder et arbejdsområde, hvor du kan få vist en liste over de funktioner, der er leveret i hver version. Nye funktioner er som standard slået fra. Du kan bruge arbejdsområdet til at aktivere dem og få vist dokumentationen til dem.

## <a name="the-feature-management-workspace"></a>Arbejdsområdet Administration af funktioner

Du kan åbne arbejdsområdet **Administration af funktioner** ved at vælge det relevante felt i dashboardet. Der vises en side med en liste over funktioner for alle de versioner, der understøttes af Administration af funktioner. Med tiden vil Microsoft forbedre Administration af funktioner med yderligere funktionalitet, der kan hjælpe dig med at administrere funktioner.

Funktionslisten indeholder følgende oplysninger:

- **Funktionsnavn** – En beskrivelse af den funktion, der blev tilføjet.
- **Aktiveret status** – Et symbol angiver, om en funktion er aktiveret (markeret), ikke er aktiveret (ikke markeret), er planlagt til at blive aktiveret (ur) eller bliver aktiveret obligatorisk (lås). Den indstilling, der vises her, bruges til alle juridiske enheder. Bemærk, at selv når en funktion er slået til, styres den stadig af sikkerhed. Derfor er funktionen kun tilgængelig for brugere, der har adgang til den, baseret på brugernes sikkerhedsrolle. Den vil også kun være tilgængelig for juridiske enheder, som brugeren har adgang til.
- **Aktiveringsdato** – Den dato, hvor funktionen blev aktiveret eller bliver aktiveret, hvis det er en fremtidig dato.
- **Tilføjelse af funktion** – Den dato, hvor funktionen blev føjet til dit miljø. Denne dato angives automatisk, når du opdaterer dit miljø under de månedlige frigivelsescyklusser.
- **Modul** – Det modul, der påvirkes af den nye funktion.

Når du vælger en funktion, vises der flere oplysninger i detaljeruden til højre for funktionslisten. Øverst i ruden kan du se funktionsnavnet, den dato, hvor funktionen blev tilføjet, det modul, der påvirkes af funktionen, og linket **Få mere at vide**. Vælg dette link for at få vist dokumentationen til funktionen. Hvis dokumentationen ikke er tilgængelig, åbnes en midlertidig side. Detaljeruden indeholder også et **Bemærkninger** felt, hvor du kan tilføje dine egne kommentarer om funktionen.

Arbejdsområdet **Administration af funktioner** indeholder også adskillige faner med en liste over funktioner. 
- **Ny** - Viser alle de funktioner, der er blevet tilføjet siden den seneste månedlige opdatering. Hvis du har sprunget en månedlig opdatering over, vises alle de nye funktioner, siden du sidst opdaterede. De nyeste funktioner vises øverst på listen. Det samlede antal nye funktioner vises også i et felt øverst på siden.
- **Ikke aktiveret** - Viser alle de funktioner, der ikke er aktiveret. De nyeste funktioner vises øverst på listen. Det samlede antal nye funktioner vises også i et felt øverst på siden.
- **Planlagt** -Viser alle funktioner, der er planlagt til at blive aktiveret på en fremtidig dato. De funktioner, der har den tidligste planlagte dato, vises øverst på listen. Det samlede antal nye funktioner vises også i et felt øverst på siden.
- **Alle** - Viser alle funktioner. De nyeste funktioner vises øverst på listen.


## <a name="enable-a-feature"></a>Aktivere en funktion

Hvis en funktion ikke er aktiveret, vises knappen **Aktiver** i detaljeruden. Du kan bruge denne knap til at aktivere funktionen.

1. Vælg den funktion, du vil aktivere, og vælg derefter **Aktiver** i detaljeruden.
2. Der vises en skyder, hvor du kan angive den dato, hvor funktionen skal aktiveres. Denne dato er som standard indstillet til dags dato.
3. Vælg **Aktiver** for at aktivere funktionen.

Nogle funktioner kan ikke deaktiveres, når du har aktiveret dem. Hvis den funktion, du forsøger at aktivere, ikke kan deaktiveres, får du vist en advarsel. På dette tidspunkt kan du vælge **Annuller** for at annullere handlingen og lade funktionen være deaktiveret. Hvis du vælger **Aktiver** og aktiverer funktionen, kan du dog ikke deaktivere den senere.

Når funktionen er aktiveret, vises der en meddelelse under linket **Få mere at vide** i detaljeruden. Denne meddelelse angiver enten, at funktionen er aktiveret, eller angiver, hvornår funktionen bliver aktiveret fremover. Hvis du bruger en fremtidig dato, vises funktionen på listen **Planlagt**. Denne meddelelse vises, hver gang du vælger funktionen på funktionslisten. Funktioner, der er planlagt til en fremtidig dato, aktiveres ved midnat af en batchproces på basis af den tidszone, der er angivet ved hjælp af systemdatoen. 

## <a name="reschedule-a-feature"></a>Omplanlægge en funktion

Hvis en funktion er aktiveret til fremtiden, vises knappen **Omplanlæg** i detaljeruden. Du kan bruge denne knap til at ændre **Aktiveringsdato** til en anden dato.

1. Vælg en planlagt funktion, du vil omplanlægge, og vælg derefter **Omplanlæg** i detaljeruden.
2. Der vises en skyder, hvor du kan angive den dato, hvor funktionen skal aktiveres. 
3. Vælg **Aktiver** for at omplanlægge funktionen eller **Deaktiver** for at annullere planlægningen.

## <a name="disable-a-feature"></a>Deaktivere en funktion

Hvis en funktion allerede er aktiveret, vises knappen **Deaktiver** i detaljeruden. Du kan bruge denne knap til at deaktivere funktionen. Knappen **Deaktiver** er ikke tilgængelig, hvis funktionen ikke kan deaktiveres, når den først er aktiveret.

- Vælg den funktion, du vil deaktivere, og vælg derefter **Deaktiver** i detaljeruden.

- Funktionen er deaktiveret, og datoen er ryddet.

Når funktionen er deaktiveret, vises der en meddelelse under linket **Få mere at vide** i detaljeruden. Denne meddelelse angiver, at funktionen endnu ikke er aktiveret, og funktionen vises på listen **Ikke aktiveret**. Meddelelsen vises, hver gang du vælger funktionen på funktionslisten.

## <a name="features-that-must-be-enabled"></a>Funktioner, der skal aktiveres

Der kan blive leveret en vigtig funktion, som skal aktiveres automatisk, når du foretager en opdatering. Den bliver automatisk aktiveret på **Aktiveringsdato**. Der vises en meddelelse under linket **Få mere at vide** i detaljeruden. Denne meddelelse angiver, at funktionen er aktiveret eller automatisk bliver aktiveret på **Aktiveringsdato**. Meddelelsen vises, hver gang du vælger funktionen på funktionslisten.

## <a name="assigning-roles"></a>Tildeling af roller

Arbejdsområdet **Administration af funktioner** kan åbnes af systemadministratorer og af brugere, der er tildelt rollen som funktionsleder eller funktionsseer, der er oprettet for at understøtte oplevelsen Administration af funktioner. Brugere i rollen funktionsleder kan aktivere eller deaktivere enhver funktion. De kan også opdatere afsnittet med kommentarer for funktionen. Brugere i rollen funktionsseer kan kun se arbejdsområdet **Administration af funktioner**. De kan ikke slå funktioner til eller fra.

Rollerne som funktionsleder og funktionsseer tilsidesætter ikke den eksisterende sikkerhed, en bruger har. Rollerne styrer kun adgangen til aktivering af funktioner. Den giver ikke adgang til selve funktionerne.

## <a name="using-feature-management-to-enable-isv-features-or-custom-features"></a>Bruge Administration af funktioner til at aktivere ISV-funktioner eller brugerdefinerede funktioner

Processen til administration af funktioner er i øjeblikket ikke tilgængelig for ISV-funktioner eller brugerdefinerede funktioner. Vi tilføjer yderligere funktioner for at forbedre Administration af funktioner, og når disse forbedringer er fuldført, åbner vi Administration af funktioner for alle funktioner og angiver specifikke instruktioner om, hvordan du opdaterer en funktion, så den bruger den.

## <a name="feature-management-and-flighting"></a>Administration af funktioner og flighting

Med Administration af funktioner kan du styre de funktioner, der leveres i hver udgave. Flighting gør det muligt for Microsoft-team at frigive funktioner til et begrænset antal kunder, så funktionerne kan testes og valideres, uden at det påvirker alle kunder. Administration af funktioner styrer ikke flighting af nogen funktioner.
