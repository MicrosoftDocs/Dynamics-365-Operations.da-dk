---
title: Registrere varer for en vare med aktiveret avanceret lagerstyring ved hjælp af en varemodtagelseskladde
description: Denne procedure viser, hvordan du registrerer varer ved hjælp af varemodtagelseskladden, når du bruger avancerede lagerstyringsprocesser.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 392884d2a87c10a5f38bf6f51967f879c68c1ca6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "355489"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>Registrere varer for en vare med aktiveret avanceret lagerstyring ved hjælp af en varemodtagelseskladde

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du registrerer varer ved hjælp af varemodtagelseskladden, når du bruger avancerede lagerstyringsprocesser. Dette vil normalt blive udført af en modtagende medarbejder. 

Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data. Du skal have en bekræftet indkøbsordre med en åben indkøbsordrelinje, før du starter denne guide. Varen på linjen skal på lager, og den skal ikke bruge produktvarianter og ikke have sporingsdimensioner. Og varen skal tilknyttes en lagerstyringsprocesaktiveret lagringsdimensionsgruppe. Det lagersted, der bruges, skal være aktiveret for lagerstyringsprocesser og den lokalitet, du bruger til modtagelse, skal være id-kontrolleret. Hvis du bruger USMF, kan du bruge regnskab 1001, lagersted 51 og vare M9200 til at oprette din IO. 

Noter nummeret på den indkøbsordre, du opretter, og bemærk også varenummeret og det sted, du har brugt til din indkøbsordrelinje.


## <a name="create-an-item-arrival-journal-header"></a>Oprette en varemodtagelseskladde
1. Gå til Varemodtagelse.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
    * Hvis du bruger USMF, kan du skrive WHS. Hvis du bruger andre data, skal kladden, hvis navn du vælger, have følgende egenskaber: Undersøg plukplads skal angives til Nej, og Karantænestyring skal angives til Nej.  
4. Skriv en værdi i feltet Nummer.
5. Skriv en værdi i feltet Sted.
    * Vælg det sted, du brugte til din indkøbsordrelinje. Dette vil fungere som en standardværdi, der som standard bruges til alle linjer i kladden. Hvis du brugte lagersted 51 i USMF, skal du vælge sted 5.  
6. Skriv en værdi i feltet Lagersted.
    * Vælg et lagersted, der er gyldigt for det sted, du har valgt. Dette vil fungere som en standardværdi, der som standard bruges til alle linjer i kladden. Hvis du bruger eksempelværdierne i USMF, skal du vælge 51.  
7. Skriv en værdi i feltet Lokalitet.
    * Vælg en gyldig lokalitet på det lagersted, du har valgt. Lokaliteten skal knyttet til en lokalitetsprofil, som er nummerpladekontrolleret. Dette vil fungere som en standardværdi, der som standard bruges til alle linjer i kladden. Hvis du bruger eksempelværdierne i USMF, skal du vælge Bulk-008.  
8. Højreklik på rullepilen i feltet Nummerplade, og vælg derefter Vis detaljer.
9. Klik på Ny.
10. Skriv en værdi i feltet Nummerplade.
    * Noter værdien.  
11. Klik på Gem.
12. Luk siden.
13. Skriv en værdi i feltet Nummerplade.
    * Angiv værdien af den nummerplade, du netop har oprettet. Dette vil fungere som en standardværdi, der som standard bruges til alle linjer i kladden.  
14. Klik på OK.

## <a name="add-a-line"></a>Tilføj en linje
1. Klik på Tilføj linje.
2. Indtast en værdi i feltet Varenummer.
    * Angiv det varenummer, som du brugte på indkøbsordrelinjen.  
3. Angiv et tal i feltet Antal.
    * Angiv den mængde, du vil registrere.  
    * Feltet Dato angiver den dato, hvor den disponible mængde af denne vare registreres på lageret.  
    * Parti-id udfyldes af systemet, hvis det kan identificeres entydigt fra de givne oplysninger. Ellers skal du tilføje dem manuelt. Dette er et obligatorisk felt, der sammenkæder denne registrering med en bestemt kildedokumentlinje.  

## <a name="complete-the-registration"></a>Fuldføre registreringen
1. Klik på Valider.
    * Dette kontrollerer, at kladden er klar til at blive bogført. Hvis valideringen mislykkes, skal du rette fejlene, før du kan bogføre kladden.  
2. Klik på OK.
    * Når du har klikket på OK, kan du se meddelelsen. Der bør være en meddelelse om, at kladden er OK.  
3. Klik på Bogfør.
4. Klik på OK.
    * Når du har klikket på OK, skal du tjekke meddelelseslinjen. Der bør være en meddelelse om, at handlingen er fuldført.  
5. Luk siden.

