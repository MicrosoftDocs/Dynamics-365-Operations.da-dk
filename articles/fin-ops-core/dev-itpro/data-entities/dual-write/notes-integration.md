---
title: Notaintegration
description: I dette emne beskrives integrationen af notadata i dobbeltskrivning.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d52ff69cfd7a81eb9f19a0ef498c6ceeea77b360
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782350"
---
# <a name="note-integration"></a>Notaintegration

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I løbet af Microsoft Dynamics 365-forretningsprocesserne indsamler brugere ofte oplysninger om deres kunder. Oplysningerne registreres som aktiviteter og notater. I dette emne beskrives integrationen af notadata i dobbeltskrivning.

Kundeoplysninger kan klassificeres på følgende måder:

+ **Handlingsbare oplysninger, som en Dynamics 365-bruger håndterer på vegne af en kunde** - f.eks. udfører Contoso (en Dynamics 365-bruger) et spil show. En af Contosos kunder (en kunde) ønsker at deltage i dette show. Kunden beder en medarbejder hos Contoso om at booke en plads i spilopvisning for dem. Reservationen sker i Contosos hændelseskalender.
+ **Oplysninger, der kan ageres på, for en Dynamics 365-bruger** - En kunde, der køber en Surface-enhed, angiver f.eks., at enheden skal være pakket ind som gave før levering. Disse instruktioner er oplysninger, der kan anvendes, og som håndteres af den medarbejder hos Contoso, der er ansvarlig for emballagen.
+ **Oplysninger, der ikke kan ageres på** - En kunde besøger f.eks. Contoso-butikken, og under samtalen med en butiksmedarbejder udtrykkes interessen for *Halo*-spil og spiltilbehør. Butikspartneren noterer sig disse oplysninger. Programmet til produktanbefalinger bruger det derefter til at komme med anbefalinger til kunden.

Generelt registreres handlingsbare oplysninger som *aktiviteter* i Finance and Operations-apps og kundetilfredshedsapps. Oplysninger, der ikke kan ageres på, registreres som *noter* i Finance and Operations-apps, and som *bemærkninger* i kundetilfredshedsapps.

> [!TIP]
> Notater er beregnet til oplysninger, der ikke kan handlings, men appsene forhindrer dig ikke i at bruge dem til at gemme og håndtere oplysninger, der kan handlings, hvis du vil bruge dem på den måde.

Microsoft frigiver i øjeblikket funktioner til noteintegration. Funktioner til aktivitetsintegration frigives senere. Notatintegration er tilgængelig for debitorer, kreditorer, salgsordrer og indkøbsordrer.

## <a name="create-a-note-in-a-customer-engagement-app"></a>Oprette et notat i en kunde aftale-app

Hvis du vil oprette et notat i en kunde aftale-app og derefter synkronisere den med en Finance and Operations-app, skal du udføre følgende trin.

1. Åbn kontoposten for en kunde i kundetilfredsheds-appen.
2. Vælg i ruden **Tidslinje** plustegnet (**+**), og vælg derefter **Notat** for at oprette et notat.

    ![Oprette et notat i en kundeaftale-app.](media/notes-ce-1.png)

3. Vælg **Tilføj note**, og angiv derefter titel og en beskrivelse.

    ![Angiv en titel og en beskrivelse.](media/notes-ce-2.png)

    Det nye notat føjes til debitortidslinjen.

    ![Nyt notat på debitortidslinjen.](media/notes-ce-3.png)

4. Logge på appen Finance and Operations, og åbn den samme kundepost. Bemærk, at knappen **Vedhæftede filer** (papirklipssymbolet) øverst til højre angiver, at posten er vedhæftet.

    ![Besked om en vedhæftet fil.](media/notes-ce-4.png)

5. Vælg knappen **Vedhæftede filer** for at åbne siden **Vedhæftede filer**. Du skal finde det notat, du har oprettet i kundens aftale-app.

    ![Notat fra kundeaftale-appen.](media/notes-ce-5.png)

Eventuelle opdateringer af notatet synkroniseres frem og tilbage mellem Finance and Operations-appen og kundens aftale-app.

## <a name="create-a-note-in-a-finance-and-operations-app"></a>Oprette et notat i en Finance and Operations-app

Du kan også oprette et notat i en Finance and Operations-app og derefter synkronisere den med en kundeaftale-app.

Hvis du vil oprette et notat i en Finance and Operations-app og derefter synkronisere den med en kundeaftale-app, skal du udføre følgende trin.

1. I appen Finance and Operations på siden **Vedhæftede filer** skal du vælge **Ny** \> **Note**.

    ![Oprette et notat i en Finance and Operations-app.](media/notes-fo-1.png)

2. Angiv en titel og et kort sæt instruktioner, og vælg derefter **Gem**.

    ![Angiv en titel og beskrivelse.](media/notes-fo-2.png)

3. Opdater posten i kundeengagementsappen. Du skal finde det nye notat på tidslinjen.

    ![Nyt notat på tidslinjen i kundeaftale-appen.](media/notes-fo-3.png)

Du kan klassificere en note som enten intern eller ekstern.

- I Finance and Operations-appen på siden **Vedhæftede filer** skal du åbne noten og derefter i feltet **Begrænsning** vælge **Intern** eller **Ekstern**.

    ![Begrænsningsfelt.](media/notes-fo-4.png)

Du kan også oprette en URL-adresse.

1. I appen Finance and Operations på siden **Vedhæftede filer** skal du vælge **Ny** \> **URL-adresse**.
2. Angiv en titel og en URL-adresse.
3. I feltet **Begrænsning** vælges **Intern** eller **Ekstern**.

    ![Opret en URL-adresse i Finance and Operations-appen.](media/notes-fo-5.png)

4. Vælg **Gem**.

    Da apps til kundeengagement ikke har en URL-type, er URL-adressen integreret med skriv som et notat.

    ![URL-adressen vises som et notat i en kundeaftale-app.](media/notes-ce-6.png)

> [!NOTE]
> Filer, der er vedhæftede filer, understøttes ikke.

## <a name="templates"></a>Skabeloner

Noteintegration omfatter en samling af tabeltilknytninger, der arbejder sammen i forbindelse med datainteraktion, som vist i følgende tabel.

| Finance and Operations-app | Customer Engagement-app | Betegnelse |
|----------------------------|-------------------------|-------------|
| [Vedhæftede filer for debitorer](mapping-reference.md#230) | Anmærkning | Virksomheder, der bruger almindelig tekst og URL-adresser til at hente kundespecifikke oplysninger (for både organisationer og personer). |
| [Vedhæftede kreditordokumenter](mapping-reference.md#231) | Anmærkning | Virksomheder, der bruger almindelig tekst og URL-adresser til at hente leverandørspecifikke oplysninger (for både organisationer og personer). |
| [Vedhæftede dokumenter til salgsordrehoved](mapping-reference.md#229) | Anmærkning | Virksomheder, der bruger almindelig tekst og URL-adresser til at registrere salgsordrespecifikke oplysninger. |
| [Vedhæftede dokumenter til indkøbsordrehoved](mapping-reference.md#232) | Anmærkning | Virksomheder, der bruger almindelig tekst og URL-adresser til at registrere købsordrespecifikke oplysninger. |

## <a name="limitations"></a>Begrænsninger

Når du har installeret noteløsningen, kan du ikke afinstallere den. 

Du kan finde flere oplysninger i [referencen til tilknytning af dobbeltskrivning](mapping-reference.md).
