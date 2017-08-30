---
title: "Registrere materialeforbrug ved hjælp af en mobilenhed"
description: "I dette emne beskrives en arbejdsgang, der gør det muligt at registrere forbrug af råmaterialer i produktionen ved hjælp af en håndholdt enhed."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b4c0d14340e96b2e7916ea73e25e62ae5c33ce49
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---

# <a name="register-material-consumption-using-a-mobile-device"></a>Registrere materialeforbrug ved hjælp af en mobilenhed
I dette emne beskrives en arbejdsgang, der gør det muligt at registrere forbrug af råmaterialer i produktionen ved hjælp af en håndholdt enhed.

<a name="introduction"></a>Introduktion
------------

Denne arbejdsproces er relevant, hvis der er strenge krav til sporbarhed af materialer. I så fald skal den nøjagtige tid og det nøjagtige antal rapporteres for forbruget for at opretholde materialernes sporbarhed. Denne proces kan ses som modsætning til forlæns- eller baglænstrækoperationer, hvor der er en forskydning mellem tidspunktet for registreringen og tidspunktet, hvornår det faktiske forbrug finder sted. Det forklarer, hvorfor en strategi for automatisk forbrug ikke kan bruges til visse materialer med krav til sporbarhed. Lad os se på et enkelt scenario, der forklarer, hvordan du konfigurerer en arbejdsgang for at aktivere registrering af forbrug af råmaterialer i produktionen ved hjælp af en håndholdt enhed. [![](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a>Scenariedetaljer

I en fortløbende produktionsproces (5) bruges det batchstyrede råmateriale RM-100. Materialet er disponibelt på lokationen Bulk-001 (1) i id'et PL-1 med to batches, B1 og B2, begge med et antal på 100 kg. Lagerstedsarbejde (2) frigives og behandles for RM-100, og materialet plukkes fra Bulk-001 til produktionsindlagringslokationen PIL-01 (3), der er defineret som ikke-id-styret. Maskinoperatøren afvejer materiale fra produktionsindlagringslokationen (3) og registrerer vægten og batchnummeret som forbrugt (4). Fra produktionsindlagringslokationen føjes en del af materialet manuelt til produktionsprocessen i fastlagte tidsintervaller. Når maskinoperatøren tilføjer materiale, vejes det på en vægt, og batchnummeret registreres.

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a>Konfigurere arbejdsgangen for at registrere forbrug ved hjælp af en håndholdt enhed
Opret et færdigvareprodukt, FG-100, med en stykliste, der har det batchstyrede råmateriale RM-100. Tilføj to batches, B1 og B2, af RM-100 i et antal på 100 til lokation: Bulk-001 på id: PL 1. Den varetrækprincippet på styklistelinjen for RM-100 er indstillet til **Manuel**. Indstil produktionsindlagringslokationen til PIL-01. Du kan gøre det ved at vælge denne lokation som standardproduktionsindlagringslokationen for lagersted til 51.

1.  Oprette et nyt menupunkt på en mobilenhed: 

-    **Menupunktnavn** - Registrer materialeforbrug. 
-    **Titel** - Registrer materialeforbrug. 
-    **Tilstand** - Indirekte. 
-    **Aktivitetskode** – Registrer materialeforbrug.

2.  Føj menupunktet til en menuen for **produktionsmobilenheden**.
3.  Opret en produktionsordre for et færdige projekt. 

-    **Varenummer**- FG-100 
-    **Lokation** - 5 
-    **Lagersted** - 51 
-    **Antal** - 150

Produktionsordren er **Estimeret** og **Frigivet** og lagerstedsarbejde er oprettet.

4.  Afslut arbejdet ved hjælp af arbejdsgangen for råmaterialepluk for den håndholdte enhed.

Derved føres materialet fra bulkvarelokationen til produktionsindlagringslokation PIL-01. Når arbejdet er fuldført, har materialet status **Plukket på produktionsindlagringslokationen**. Status efter at arbejdet er blevet behandlet kan være enten **Plukket** eller **Reserveret fysisk**. Dette konfigureres med parameteren **Afgangsstatus efter læg på lager i lagerstedsformularen**.

5.  Igangsæt produktionsordren fra klienten eller fra den håndholdte enhed ved hjælp af menupunktet **Produktionsstart**.

Når produktionsordren er startet, kan du registrere materialeforbruget med arbejdsgangen for den håndholdte enhed. Lad os starte med at registrere forbruget på 25 kg af batch B1.

6.  Vælg menupunktet **Registrer materiale****forbrug** i menuen for den håndholdte enhed, og angiv følgende oplysninger: 

-    Produktionsordrenummeret. 
-    Det sted, hvor materialet skal forbruges, i dette tilfælde PIL-01. 
-    Varenummer RM-100. 
-    Batchnummer B1. 
-    Et antal på 25.

7.  Vælg **OK**.

Bemærk, at meddelelsen "Journallinje er oprettet" vises på skærmen. I produktionsordren er der en åben kladde af typen **Produktionsplukliste** for varenummer RM-100 og batchnummer B1. 

Du kan nu vælge at fortsætte registreringen, for eksempel på batchnummer B2, og hver gang du vælger **OK**, føjes der en ny kladdelinje til den åbne kladde. 

Når du har gennemført registreringen, kan du vælge **Udført** for at bogføre kladden og afslutte arbejdsgangen.

### <a name="additional-comments"></a>Yderligere kommentarer 

-   Hvis en bruger annullerer arbejdsgangen, når der oprettes en kladdelinje, er kladden i en ikke-bogført tilstand, men hvis brugeren på et senere tidspunkt bruger arbejdsgangen til den samme produktionsordre, føjes linjerne til den åbne kladde i stedet for en ny kladde.
-   Den nye arbejdsgang understøtter også registrering af serienumre.
-   Det er kun muligt at registrere et varenummer, der er defineret i styklisten eller formlen for den valgte produktionsordre eller batchordre.
-   Materiale kan overforbruges. Hvis der f.eks. er forkalkuleret et materialeforbrug på 100 kg, kan det være et overforbrug på f.eks. 105 kg.



