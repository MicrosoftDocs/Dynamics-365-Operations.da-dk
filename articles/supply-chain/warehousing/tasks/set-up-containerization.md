---
title: Konfigurere containerisering
description: Dette emne beskriver, hvordan du automatiserer containeriseringen af laster i Lokationsstyring.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/19
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0f042e6ffe5ecf01b9e5044fc83d081528fbc56
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383291"
---
# <a name="set-up-containerization"></a>Konfigurere containerisering

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du automatiserer containeriseringen af laster i Lokationsstyring. Automatiseret containerisering opretter containere og plukker arbejde for leverancer, når en bølge behandles og arbejdslinjer kan opdeles i mængder, der passer til containerne. Det gør det lettere for lagermedarbejdere at plukke varer direkte i den valgte container. Sammenlignet med den manuelle pakningsproces, udføres opgaver såsom oprettelse af containere, tildeleling af varer og lukning af containere automatisk af systemet. Denne procedure bruger USMF-demofirmaet og udføres af en lagerchef.


## <a name="set-up-a-wave-template"></a>Konfigurere en bølgeskabelon
1. I navigationsruden skal du gå til **Moduler > Lokationsstyring > Opsætning > Bølger > Bølgeskabeloner**.
2. Vælg **Ny**.
3. Indtast en værdi i feltet **Bølgeskabelonnavn**.
4. Indtast en værdi i feltet **Beskrivelse af bølgeskabelon**.
5. Indtast eller vælg en værdi i feltet **Sted**.
6. Indtast eller vælg en værdi i feltet **Lokation**.
7. Udvid sektionen **Metoder**. I vinduet **Valgte metoder** vises metoderne for den valgte bølgeskabelontype. Bølgeskabelonen skal indeholde containeriseringsmetoden.  
8. Skriv en værdi i feltet **Kode for bølgetrin**. Angiv en bølgetrinkode for den tilføjede metode, som kan være en hvilken som helst kode. Det er muligt at tilføje metoden mere end én gang og tildele forskellige bølgetrinkoder. Til dette formål skal du vælge **Kan gentages for denne metode** på siden **Metoder til bølgeproces**.  
9. Vælg **Gem**.
10. Luk siden.

## <a name="set-up-a-container-type"></a>Konfigurere en containertype
1. I navigationsruden skal du gå til **Moduler > Lokationsstyring > Opsætning > Bølger > Container > Containertyper**. Du kan definere dine containere på siden **Containertyper**. Du kan konfiguree containeres fysiske dimensioner, herunder taravægt, maksimal vægt, maksimal volumen, længde, bredde, vægt og højde. I dette eksempel har vi tre forskellige størrelser af bokse.  
2. Vælg **Ny**.
3. Indtast en værdi i feltet **Containertypekode**.
4. Angiv et tal i feltet **Taravægt**.
5. Angiv et tal i feltet **Maksimal vægt**.
6. Angiv et tal i feltet **Volumen**.
7. Angiv et tal i feltet **Længde**.
8. Indtast et tal i feltet **Bredde**.
9. Indtast et tal i feltet **Højde**.
10. Indtast en værdi i feltet **Beskrivelse**.
11. Vælg **Gem**.
13. Gentag trin 2-11 to gange mere for at oprette tre containertyper i alt.
14. Luk siden.

## <a name="set-up-a-container-group"></a>Konfigurere en containergruppe
1. I navigationsruden skal du gå til **Moduler > Lokationsstyring > Opsætning > Bølger > Container > Containergrupper**.
2. Gå til handlingsruden, og vælg **Ny**. Du kan konfigurere logiske grupper af containertyper. For hver gruppe kan du angive den rækkefølge, i hvilken du skal pakke containerne, og hvor meget containerne skal fyldes op i procent. Varens størrelsesdimensioner bruges til at bestemme, om den kan være i en container. Den container, der er tættest på varens størrelsesdimension, bruges. Hvis du har flere containertyper i en gruppe, anbefaler vi, at du arrangerer rækkefølgen efter størrelse, så den største container er først, nummer 1 i rækkefølgen, og den mindste container er sidst.    
3. Skriv en værdi, du tidligere har oprettet, i feltet **Containergruppe-ID**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Gentag trin 2-4 for alle tre containertyper, du oprettede tidligere.
6. Vælg **Gem**.
7. Luk siden.

## <a name="set-up-a-container-build-template"></a>Konfigurere en containerbuildskabelon
1. I navigationsruden skal du gå til **Moduler > Lokationsstyring > Opsætning > Bølger > Container > Skabeloner til containerbygning**.
2. Vælg **Ny**. Skabelonen til container-build er baseret på, hvilke af containeriseringsprocesserne der udføres. Hver skabelon til container-build definerer en containeriseringsproces, der vil blive brugt af en bølgeskabelon. Indstillingen **Rediger forespørgsel** giver dig mulighed at definere de betingelser, som den valgte skabelon vil blive behandlet under. For eksempel kan du kun køre containerisering for bestemte kunder, produkter eller lagersteder, eller du kan tilføje de tilsvarende forespørgselsområder til skabelonen. Feltet **Bølgetrinkode** viser, hvordan en skabelon til containerbygning er knyttet til trinnene i en bølgeskabelon. Når der udføres en bølge, bestemmer den, hvilke skabeloner til container-build der bruges til at starte containeriseringen. Feltet Basisforespørgselstype bestemmer, hvad der skal pakkes, og hvad filterforespørgslen skal baseres på. 
3. Skriv en værdi i feltet **Containerskabelon-ID**.
4. Indtast eller vælg en værdi i feltet **Containergruppe-ID**.
5. Skriv en værdi i feltet **Kode for bølgetrin**.
6. Markér afkrydsningsfeltet **Tillad opdeling af plukninger**.
7. Vælg **Gem**.
8. Klik på **Begrænsninger i containerblanding**. Med pauser i blandingsregler kan du angive regler for fordelingslinjer for pakning i containere. Hvis du for eksempel tilføjer **Varenummerfelt**, når varer tildeles containerne, oprettes der en ny container, når der er et nyt varenummer. Dette er vil forhindre, at arbejdere pakker fordelingslinjer for to forskellige kunder i samme container.  
9. Vælg **Ny**.
10. Vælg en indstilling i feltet **Tabel**.
11. Indtast eller vælg en værdi i feltet **Valg af felt**.
12. Vælg **OK**.

