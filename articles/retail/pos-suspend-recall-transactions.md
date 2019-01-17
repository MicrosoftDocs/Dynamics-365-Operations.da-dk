---
title: Afbryde og genoptage en transaktion i POS
description: "Dette emne forklarer, hvordan brugere kan afbryde igangværende transaktioner og derefter genoptage dem senere eller på et andet kasseapparat ved hjælp af Microsoft Dynamics 365 for Retail."
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: ffb04609318c7de4b9ef729a8e03a7f9395806b8
ms.contentlocale: da-dk
ms.lasthandoff: 01/04/2019

---

# <a name="suspend-and-resume-transactions-in-the-point-of-sale-pos"></a>Afbryde og genoptage transaktioner i POS

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

POS-brugere kan afbryde igangværende transaktioner og derefter genoptage dem senere eller på et andet kasseapparat. Transaktioner afbrydes ofte for hurtigt at frigøre et kasseapparat til en anden opgave uden at tage tid fra den aktuelle transaktion. En butiksansat begynder f.eks. at behandle en debitorpostering på en mobilenhed, men skal afslutte den på et kasseapparat, der har en pengeskuffe. Den butiksansatte kan afbryde transaktionen på mobilenheden og derefter hente den frem og genoptage den på et kasseapparat.

## <a name="configure-suspend-and-resume-functionality"></a>Konfigurere afbryde- og genoptage-funktionalitet

### <a name="pos-operations"></a>POS-handlinger

Afbrydelse og genoptagelse understøttes af to [POS-handlinger](pos-operations.md). Du kan tildele disse handlinger til [knapmatrixer](pos-screen-layouts.md) på transaktionssiden eller velkomstsiden.

- 503: Udsæt transaktion
- 504: Hent transaktion igen

### <a name="receipt-template"></a>Skabelon for modtagelse

POS kan konfigureres til at generere en udskrevet følgeseddel, når en transaktion afbrydes. Dette bilag kan derefter bruges til hurtigt at identificere og genkalde transaktionen senere.

Hvis du vil indstille POS til at udskrive en følgeseddel, skal du tilføje kvitteringsformatet **Udsat transaktion** i butikkens kvitteringsprofil. Du kan designe kvitteringsformatet, så bestemte oplysninger om posteringen medtages eller udelukkes. Formatet kan f.eks. omfatte en stregkode for at understøtte scanning.

### <a name="receipt-numbering"></a>Kvitteringsnummerering

Hvad angår andre POS-transaktionstyper, der genererer en udskrevet kvittering, kan du definere en nummerserie for udsatte transaktioner i sektionen **Kvitteringsnummerering** af butikkens funktionalitetsprofilen.

### <a name="void-when-closing-shift"></a>Erklær som ugyldig, når skiftet lukkes

Du kan bruge indstillingen **Erklær som ugyldig, når skiftet lukkes** til at kræve, at brugerne enten fuldfører eller annullerer en afbrudt transaktion, før de afslutter deres skift. Når der udføres et **Luk skift**, beder POS brugerne om enten at vise eller annullere alle udestående, afbrudte transaktioner.

## <a name="suspend-and-resume-a-transaction"></a>Afbryde og genoptage en transaktion

### <a name="suspend-a-transaction"></a>Afbryde en transaktion

Brugere, der har de nødvendige rettigheder, og som har et skærmlayout, der omfatter handlingen **Udsæt transaktion**, kan afbryde en transaktion, så den kan hentes frem senere eller på et andet kasseapparat.

Transaktioner kan kun afbrydes, hvis de **ikke** indeholde følgende typer linjer:

- Aktive betalingslinjer
- Gavekortlinjer (enten til udstedelse af et gavekort eller til tilføjelse af saldoen for gavekortet)

En afbrudt transaktion påvirker ikke salgsoplysninger eller oplysninger om disponibel lagerbeholdning for butikken.

### <a name="resume-a-suspended-transaction"></a>Genoptage en afbrudt transaktion

Afbrudte transaktioner kan hentes frem og genoptages i den samme butik af alle brugere, der har de fornødne rettigheder, og som også har et layout, der omfatter handlingen **Hent transaktion igen**.

Du kan hurtigt og nemt kalde en afbrudt transaktion frem igen ved at scanne stregkoden på udskrevne følgeseddel, mens du ser på listen over transaktioner fra handlingen **Hent transaktion igen**.

### <a name="considerations-for-offline-mode"></a>Overvejelser om offlinetilstand

- Ingen transaktioner, der afbrydes, mens POS i onlinetilstand, kan fortsætte i offlinetilstand, fordi dataene ikke er synkroniseret med offlinedatabasen.
- Hvis du afbryder en transaktion, mens POS er offline, kan du genkalde den i offlinetilstand, forudsat at POS ikke på noget tidspunkt, siden du afbrød transaktionen, er blevet skiftet tilbage til onlinetilstand. Når POS skiftes tilbage til onlinetilstand, flyttes data om afbrudte transaktioner til onlinedatabasen og fjernes fra offlinedatabasen. Derfor kan transaktionerne kun genoptages i onlinetilstand. Hvis du skifter POS tilbage til offlinetilstand, kan du ikke genoptage de afbrudte transaktioner, fordi de allerede er blevet fjernet fra offlinedatabasen.

### <a name="void-a-suspended-transaction"></a>Annullere en afbrudt transaktion

Du kan annullere afbrudte transaktioner enten ved at genkalde transaktionen og derefter udføre handlingen **Afvis transaktion** eller ved at markere transaktionen på listen **Hent transaktion igen** og vælge **Afvist** på applinjen. Butikken kan også konfigureres til at bede brugerne om at annullere afbrudte transaktioner, når de afslutter deres skift.

