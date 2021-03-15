---
title: Definere lageroptællingsprocesser
description: Dette emne beskriver konfigurationen af grundlæggende lageroptællingsprocesser ved at oprette en optællingsgruppe og en optællingskladde.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c8550e539a1b3299d89ec2b13550a13e284d807
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961365"
---
# <a name="define-inventory-counting-processes"></a>Definere lageroptællingsprocesser

[!include [banner](../../includes/banner.md)]

Dette emne beskriver konfigurationen af grundlæggende lageroptællingsprocesser ved at oprette en optællingsgruppe og en optællingskladde. Den viser også, hvordan du aktiverer optællingspolitikker på et lagersted og vareniveau. Disse opgaver udføres normalt af en tilsynsførende på lagerstedet. Det er en forudsætning, at der er nogle eksisterende, frigivne produkter og lagersteder. Hvis du bruger et demodatafirma, kan du køre denne procedure i USMF-firmaet med en hvilken som helst lagervare.


## <a name="create-a-counting-group"></a>Oprette en optællingsgruppe.
1. I navigationsruden skal du gå til **Moduler > Lagerstyring > Opsætning > Lager > Optællingsgrupper**.
2. Vælg **Ny**.
3. Indtast en værdi i feltet **Optællingsgruppe** for den nye række.
4. Skriv en værdi i feltet **Navn**.
5. Vælg en indstilling i feltet **Optællingskode**.

    - **Manuel** – Medtager linjer, hver gang du kører jobbet. Du bestemmer altså optællingsintervallet for optællingsgruppen.  
    - **Periode** – Medtager linjer for perioden i optællingskladden, når periodeintervallet er udløbet.  
    - **Nul på lager** – Hvis disponibel lagerbeholdning når nul (0), genereres der linjer i optællingskladden, når jobbet køres. Hvis disponibel lagerbeholdning når 0 efter en optælling, genereres der først linjer, næste gang du starter optællingen.  
    - **Minimum** – Der indsættes linjer i optællingskladden, hvis den disponible lagerbeholdning er lig med eller mindre end det angivne minimum.  
    - Valgfri: Hvis du har angivet **Periode** i feltet **Optællingskode**, skal du skrive periodeintervallet i feltet **Optællingsperiode**. Intervalenheden er dage.  
    - Når du kører jobbet til oprettelse af nye linjer i optællingskladden, oprettes der nye linjer med det interval, der er angivet i dette felt, uanset hvor ofte du kører det samme job. F.eks. hvis **Optællingsperiode** er indstillet til 7, og kladdelinjer sidst blev genereret for en optælling den 1. januar, er der ikke gået syv dage, hvis et andet job startes den 5. januar, og derfor genereres der ingen linjer i kladden for dette tidsinterval. Hvis du starter jobbet igen den 8. januar, oprettes der linjer for perioden i optællingskladden, da der er gået 7 dage.  

6. Vælg **Gem**.

## <a name="create-a-counting-journal-name"></a>Oprette et navn på optællingskladde
1. I navigationsruden skal du gå til **Moduler > Lagerstyring > Opsætning > Kladdenavne > Lager**.
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Navn**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Vælg **Optælling** i feltet **Kladdetype**. Valgfrit: Du kan vælge et andet id for bilagsserie, hvis du ønsker en bestemt nummerserie for bilags-id'er, der genereres, når du opretter optællingskladder. Bilagsserier oprettes på siden **Nummerserier**.  
6. Vælg en indstilling i feltet **Detaljeringsniveau**.  

    - Dette er det detaljeniveau, der anvendes, når kladden bogføres.  
    - Valgfrit: Du kan ændre værdien i feltet Reservation. Dette er den metode, der bruges til at reservere varer under optælling.   
    - **Manuel** – Varerne reserveres manuelt i formen Reservation.  
    - **Automatisk** – Ordreantallet reserveres fra en vares tilgængelige disponible lagerbeholdning.   
    - **Udfoldning** – Reservationen er en del af varedisponeringen for transaktionen.  

7. Vælg **Gem**.

## <a name="set-standard-counting-journal-name"></a>Angive standardnavn for optællingskladde
1. Gå i navigationsruden til **Moduler > Lagerstyring > Opsætning > Parametre til lager- og lokationsstyring**.
2. Vælg fanen **Kladder**.
3. Vælg den kladde, du tidligere har oprettet, i rullemenuen til feltet **Optælling**. Denne kladde vil så være standardkladdenavnet for lagerkladder af typen **Optælling**.  
4. Vælg fanen **Generelt**. Valgfrit: Vælg denne indstilling for at låse en vare under optællingsprocessen for at forhindre opdateringer af følgesedler, pluklister eller pluklisteregistreringer.  

## <a name="set-the-counting-policy-for-an-item"></a>Konfigurere optællingspolitik for en vare
1. I navigationsruden skal du gå til **Moduler > Administration af produktoplysninger > Produkter > Frigivne produkter**.
2. Vælg på listen linket for varenummeret for det produkt, du vil angive optællingspolitikker for. Du skal vælge en vare, der spores på lageret. Et ikke-lagerført produkt kan ikke optælles. Hvis du bruger USMF-demodata, kan du vælge vare A0001.  
3. Vælg **Rediger**.
4. Slå udvidelsen af sektionen **Styr lager** til/fra.
5. Vælg den optællingsgruppe, du tidligere har oprettet, i rullemenuen til feltet **Optællingsgruppe**. Dette produkt vil nu blive medtaget, når der oprettes kladdelinjer til lageroptælling ved hjælp af denne optællingsgruppe.  
6. Vælg **Gem**.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Angive optællingspolitikken for en vare på et bestemt lagersted
1. Vælg **Styr lager** i handlingsruden.
2. Vælg **Varelagersteder**.
3. Vælg **Ny**.
4. Vælg det lagersted, som du vil definere specifikke optællingspolitikker for, i rullemenuen til feltet **Lagersted**.
5. Vælg en optællingsgruppe i rullemenuen til feltet **Optællingsgruppe**. Du kan vælge en bestemt optællingsgruppe, der skal gælde for varen på det bestemte lagersted, du har valgt. Når optællingen udføres på det pågældende lagersted, tilsidesætter denne optællingspolitik den generelle optællingspolitik for varen.  
6. Vælg **Gem**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]