---
title: Notaintegration
description: Denne artikel beskriver integrationen af notadata i dobbeltskrivning.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f09d455181b7929e25d5238949a0236ac60d457b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289010"
---
# <a name="note-integration"></a>Notaintegration

[!include [banner](../../includes/banner.md)]



I løbet af Microsoft Dynamics 365-forretningsprocesserne indsamler brugere ofte oplysninger om deres kunder. Oplysningerne registreres som aktiviteter og notater. Denne artikel beskriver integrationen af notadata i dobbeltskrivning.

Kundeoplysninger kan klassificeres på følgende måder:

+ **Handlingsbare oplysninger, som en Dynamics 365-bruger håndterer på vegne af en kunde** - f.eks. udfører Contoso (en Dynamics 365-bruger) et spil show. En af Contosos kunder (en kunde) ønsker at deltage i dette show. Kunden beder en medarbejder hos Contoso om at booke en plads i spilopvisning for dem. Reservationen sker i Contosos hændelseskalender.
+ **Oplysninger, der kan ageres på, for en Dynamics 365-bruger** - En kunde, der køber en Surface-enhed, angiver f.eks., at enheden skal være pakket ind som gave før levering. Disse instruktioner er oplysninger, der kan anvendes, og som håndteres af den medarbejder hos Contoso, der er ansvarlig for emballagen.
+ **Oplysninger, der ikke kan ageres på** - En kunde besøger f.eks. Contoso-butikken, og under samtalen med en butiksmedarbejder udtrykkes interessen for *Halo*-spil og spiltilbehør. Butikspartneren noterer sig disse oplysninger. Programmet til produktanbefalinger bruger det derefter til at komme med anbefalinger til kunden.

Generelt registreres handlingsbare oplysninger som *aktiviteter* i programmer til finans og drift og kundeaftale-apps. Oplysninger, der ikke kan ageres på, registreres som *noter* i programmer til finans og drift, and som *anmærkninger* i kundeaftale-apps.

> [!TIP]
> Notater er beregnet til oplysninger, der ikke kan handlings, men appsene forhindrer dig ikke i at bruge dem til at gemme og håndtere oplysninger, der kan handlings, hvis du vil bruge dem på den måde.

Microsoft frigiver i øjeblikket funktioner til noteintegration. Funktioner til aktivitetsintegration frigives senere. Notatintegration er tilgængelig for debitorer, kreditorer, salgsordrer og indkøbsordrer.

## <a name="create-a-note-in-a-customer-engagement-app"></a>Oprette et notat i en kunde aftale-app

Hvis du vil oprette et notat i en kunde aftale-app og derefter synkronisere den med program til finans og drift, skal du udføre følgende trin.

1. Åbn kontoposten for en kunde i kundetilfredsheds-appen.
2. Vælg i ruden **Tidslinje** plustegnet (**+**), og vælg derefter **Notat** for at oprette et notat.

    ![Oprette et notat i en kundeaftale-app.](media/notes-ce-1.png)

3. Vælg **Tilføj note**, og angiv derefter titel og en beskrivelse.

    ![Angiv en titel og en beskrivelse.](media/notes-ce-2.png)

    Det nye notat føjes til debitortidslinjen.

    ![Nyt notat på debitortidslinjen.](media/notes-ce-3.png)

4. Log på program til finans og drift, og åbn den samme kundepost. Bemærk, at knappen **Vedhæftede filer** (papirklipssymbolet) øverst til højre angiver, at posten er vedhæftet.

    ![Besked om en vedhæftet fil.](media/notes-ce-4.png)

5. Vælg knappen **Vedhæftede filer** for at åbne siden **Vedhæftede filer**. Du skal finde det notat, du har oprettet i kundens aftale-app.

    ![Notat fra kundeaftale-appen.](media/notes-ce-5.png)

Eventuelle opdateringer af notatet synkroniseres frem og tilbage mellem program til finans og drift og kundeaftale-appen.

## <a name="create-a-note-in-a-finance-and-operations-app"></a>Opret en note i program til finans og drift

Du kan også oprette en note i en program til finans og drift og derefter synkronisere den med en kundeaftale-app.

Hvis du vil oprette et notat i et program til finans og drift og derefter synkronisere den med kundeaftale-appen, skal du udføre følgende trin.

1. I program til finans og drift skal du på siden **Vedhæftede filer** vælge **Ny** \> **Note**.

    ![Oprettelse af en note i program til finans og drift.](media/notes-fo-1.png)

2. Angiv en titel og et kort sæt instruktioner, og vælg derefter **Gem**.

    ![Angiv en titel og beskrivelse.](media/notes-fo-2.png)

3. Opdater posten i kundeengagementsappen. Du skal finde det nye notat på tidslinjen.

    ![Nyt notat på tidslinjen i kundeaftale-appen.](media/notes-fo-3.png)

Du kan klassificere en note som enten intern eller ekstern.

- I program til finans og drift skal du på siden **Vedhæftede filer** åbne noten og derefter i feltet **Begrænsning** vælge **Intern** eller **Ekstern**.

    ![Begrænsningsfelt.](media/notes-fo-4.png)

Du kan også oprette en URL-adresse.

1. I program til finans og drift skal du på siden **Vedhæftede filer** vælge **Ny** \> **URL-adresse**.
2. Angiv en titel og en URL-adresse.
3. I feltet **Begrænsning** vælges **Intern** eller **Ekstern**.

    ![Oprettelse af en URL i program til finans og drift.](media/notes-fo-5.png)

4. Vælg **Gem**.

    Da apps til kundeengagement ikke har en URL-type, er URL-adressen integreret med skriv som et notat.

    ![URL-adressen vises som et notat i en kundeaftale-app.](media/notes-ce-6.png)

> [!NOTE]
> Filer, der er vedhæftede filer, understøttes ikke.

## <a name="templates"></a>Skabeloner

Noteintegration omfatter en samling af tabeltilknytninger, der arbejder sammen i forbindelse med datainteraktion, som vist i følgende tabel.

| Program til finans og drift | Customer Engagement-app | Beskrivende tekst |
|----------------------------|-------------------------|-------------|
| [Vedhæftede filer for debitorer](mapping-reference.md#230) | Anmærkning | Virksomheder, der bruger almindelig tekst og URL-adresser til at hente kundespecifikke oplysninger (for både organisationer og personer). |
| [Vedhæftede kreditordokumenter](mapping-reference.md#231) | Anmærkning | Virksomheder, der bruger almindelig tekst og URL-adresser til at hente leverandørspecifikke oplysninger (for både organisationer og personer). |
| [Vedhæftede dokumenter til salgsordrehoved](mapping-reference.md#229) | Anmærkning | Virksomheder, der bruger almindelig tekst og URL-adresser til at registrere salgsordrespecifikke oplysninger. |
| [Vedhæftede dokumenter til indkøbsordrehoved](mapping-reference.md#232) | Anmærkning | Virksomheder, der bruger almindelig tekst og URL-adresser til at registrere købsordrespecifikke oplysninger. |

## <a name="limitations"></a>Begrænsninger

Når du har installeret noteløsningen, kan du ikke afinstallere den. 

Du kan finde flere oplysninger i [referencen til tilknytning af dobbeltskrivning](mapping-reference.md).

