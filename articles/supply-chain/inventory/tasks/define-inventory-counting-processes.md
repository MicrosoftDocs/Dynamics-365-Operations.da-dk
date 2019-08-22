---
title: Definere lageroptællingsprocesser
description: Denne procedure fører dig gennem konfigurationen af grundlæggende lageroptællingsprocesser ved at oprette en optællingsgruppe og en optællingskladde.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4128023ba9fded23b994579f0ab54a75f72fc15a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845421"
---
# <a name="define-inventory-counting-processes"></a>Definere lageroptællingsprocesser

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure fører dig gennem konfigurationen af grundlæggende lageroptællingsprocesser ved at oprette en optællingsgruppe og en optællingskladde. Den viser også, hvordan du aktiverer optællingspolitikker på et lagersted og vareniveau. Disse opgaver udføres normalt af en tilsynsførende på lagerstedet. Det er en forudsætning, at der er nogle eksisterende, frigivne produkter og lagersteder. Hvis du bruger et demodatafirma, kan du køre denne procedure i USMF-firmaet med en hvilken som helst lagervare.


## <a name="create-a-counting-group"></a>Oprette en optællingsgruppe.
1. Gå til Lagerstyring > Opsætning > Lageropdeling > Optællingsgrupper.
2. Klik på Ny.
3. Indtast en værdi i feltet Optællingsgruppe.
4. Skriv en værdi i feltet Navn.
5. Vælg en indstilling i feltet Optællingskode.
    * Manuel – Medtager linjer, hver gang du kører jobbet. Du bestemmer altså optællingsintervallet for optællingsgruppen.  Periode – Medtager linjer for perioden i optællingskladden, når periodeintervallet er udløbet.   Nul på lager – Hvis disponibel lagerbeholdning når nul (0), genereres der linjer i optællingskladden, når jobbet køres. Hvis disponibel lagerbeholdning når 0 efter en optælling, genereres der først linjer, næste gang du starter optællingen.   Minimum – Der indsættes linjer i optællingskladden, hvis den disponible lagerbeholdning er lig med eller mindre end det angivne minimum.  
    * Valgfri: Hvis du har angivet Periode i feltet Optællingskode, skal du skrive periodeintervallet i feltet Optællingsperiode. Intervalenheden er dage.  
    * Når du kører jobbet til oprettelse af nye linjer i optællingskladden, oprettes der nye linjer med det interval, der er angivet i dette felt, uanset hvor ofte du kører det samme job. F.eks. hvis optællingsperioden er indstillet til 7, og kladdelinjer blev sidst genereret for en optælling den 1. januar, er der ikke gået syv dage, hvis et andet job startes på den 5. januar, og derfor genereres der ingen linjer i kladden for dette tidsinterval. Hvis du starter jobbet igen den 8. januar, oprettes der linjer for perioden i optællingskladden, da der er gået 7 dage.  
6. Klik på Gem.

## <a name="create-a-counting-journal-name"></a>Oprette et navn på optællingskladde
1. Gå til Lagerstyring > Opsætning > Kladdenavne > Lager.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
4. Skriv en værdi i feltet Beskrivelse.
5. Vælg "Optælling" i feltet Kladdetype.
    * Valgfrit: Du kan vælge et andet id for bilagsserie, hvis du ønsker en bestemt nummerserie for bilags-id'er, der genereres, når du opretter optællingskladder. Bilagsserier oprettes på siden Nummerserier.  
6. Vælg en indstilling i feltet Detaljeringsniveau.
    * Dette er det detaljeniveau, der anvendes, når kladden bogføres.  
    * Valgfrit: Du kan ændre værdien i feltet Reservation. Dette er den metode, der bruges til at reservere varer under optælling.   
    * Manuel – Varerne reserveres manuelt i formen Reservation.   Automatisk – Ordreantallet reserveres fra en vares tilgængelige disponible lagerbeholdning.   Udfoldning – Reservationen er en del af varedisponeringen for transaktionen.  
7. Klik på Gem.

## <a name="set-standard-counting-journal-name"></a>Angive standardnavn for optællingskladde
1. Gå til lagerstyring > Opsætning > Parametre til lager- og lagerstedsstyring.
2. Klik på fanen Kladder.
3. Klik på rullelisten i feltet Optælling for at åbne opslaget.
4. Vælg kladde, som du oprettede tidligere.
    * Denne kladde vil så være standardkladdenavnet for lagerkladder af typen Tælling.  
5. Klik på fanen Generelt.
    * Valgfrit: Vælg denne indstilling for at låse en vare under optællingsprocessen for at forhindre opdateringer af følgesedler, pluklister eller pluklisteregistreringer.  

## <a name="set-the-counting-policy-for-an-item"></a>Konfigurere optællingspolitik for en vare
1. Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.
2. Klik i listen på linket for varenummeret for det produkt, du vil angive optællingspolitikker for.
    * Bemærk, at du skal vælge en vare, der spores på lageret. Et ikke-lagerført produkt kan ikke optælles. Hvis du bruger USMF-demodata, kan du vælge vare A0001.  
3. Klik på Rediger.
4. Slå udvidelsen af sektionen Styr lager til/fra.
5. Klik på rullelisten i feltet Optællingsgruppe for at åbne opslaget.
6. Klik på optællingsgruppen du tidligere har oprettet, på listen.
    * Dette produkt vil nu blive medtaget, når der oprettes kladdelinjer til lageroptælling ved hjælp af denne optællingsgruppe.  
7. Klik på Gem.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Angive optællingspolitikken for en vare på et bestemt lagersted
1. Klik på Styr lager i handlingsruden.
2. Klik på Varelagersteder.
3. Klik på Ny.
4. Klik på rullelisten i feltet Lagersted for at åbne opslaget.
5. Vælg på listen det lagersted, du vil konfigurere specifikke optællingspolitikker for.
6. Klik på rullelisten i feltet Optællingsgruppe for at åbne opslaget.
7. Vælg en optællingsgruppe på listen.
    * Her kan du vælge en bestemt optællingsgruppe, der skal gælde for varen på den bestemte lagersted, du har valgt. Når optællingen udføres på det pågældende lagersted, tilsidesætter denne optællingspolitik den generelle optællingspolitik for varen.  
8. Klik på Gem.

