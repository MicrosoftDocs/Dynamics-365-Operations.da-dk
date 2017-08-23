--- 
title: Opret salgsordrer
description: Denne procedure viser, hvordan du opretter en salgsordre.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 62276765e1cc76b2328a7b5b57bd18593d93e4ab
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-sales-orders"></a>Opret salgsordrer

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter en salgsordre. Du kan bruge denne procedure i demodatafirmaet USMF. Salgsordrer oprettes typisk af en salgsordreprocessor. 




## <a name="enter-sales-order-header-details"></a>Angiv oplysninger om salgsordrehovedet
1. Gå til Salg og marketing > Salgsordrer > Alle salgsordrer.
2. Klik på Ny.
3. Klik på rullelisten i feltet Kundekonto for at åbne opslaget.
4. Find og vælg kundeposten på listen.
    * I dette eksempel skal du vælge kundenummer "US 004"  
5. Klik op linket i den valgte række på listen.
6. Klik på OK.

## <a name="enter-sales-order-line-details"></a>Angiv oplysninger om salgsordrelinjen
    * De produkter, der sælges af organisationen, kan findes i varianter, der er differentieret efter dimensioner, f.eks. konfiguration, farve, størrelse og type. Produkter kan også konfigureres til at bruge lagringsdimensioner som sted, lagersted, og palle og sporingsdimensioner som batch- og serienumre. Når disse dimensioner er tildelt, skal du vælge værdier for dimensionerne på ordrelinjen. For at forbedre effektiviteten af ordreindtastning kan du føje de respektive dimensionsfelter til ordregitteret.  
1. Klik på Salgsordrelinje.
2. Klik på Dimensioner.
    * I dette eksempel skal du vælge dimensionerne farve, lokation og lagersted. De dimensioner, du vælger her, vises i salgsordregitteret. Hvis dine valg skal bevares, skal du angive indstillingen Gem opsætningen til Ja.   
3. Klik på OK.
4. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
5. I dette eksempel skal du vælge varenummer T0004.
6. Klik op linket i den valgte række på listen.
    * Hvis varen er en del af en salgskategori, vises varenavnet automatisk i feltet Salgskategori.  
    * Hvis produktdimensionsfelterne allerede indeholder en værdi, er det fordi, værdien blev kopieret fra produktposten, hvor den er defineret som standardproduktdimension. Du kan når som helst ændre standardværdien.   
7. Klik på rullelisten i feltet Farve for at åbne opslaget.
8. Find og vælg den ønskede post på listen.
9. Klik op linket i den valgte række på listen.
10. Angiv et tal i feltet Antal.
    * Hvis varen sælges i andre enheder end dem, de er købt, produceret og gemt i, og der er angivet en måleenhed for salgsenheden i produktposten, vises denne værdi i feltet Enhed. Du kan til enhver tid ændre værdien.   
    * Hvis dette felt allerede indeholder en værdi, kopieres værdien fra ordrehovedet eller fra ordreindstillinger, der er knyttet til produktet. Du kan til enhver tid ændre værdien. Vælg en værdi, hvis feltet er tomt.   
    * Hvis feltet Enhedspris allerede indeholder en værdi, kopieres værdien fra en gyldig samhandelsaftale eller fra produktposten. (Enhedsprisen kan også stamme fra en salgsaftale, men processen til oprettelse af salgsordrer fra salgsaftaler afviger fra den, der vises her). Angiv en værdi, hvis feltet er tomt.   
    * Feltet Rabat indeholder et rabatbeløb pr. produktenhed. For at beregne det samlede linjerabatbeløbet ganges rabatværdien med linjeantallet.    Hvis feltet Rabat allerede indeholder en værdi, kopieres værdien fra en gyldig samhandelsaftale. Hvis feltet er tomt, og du vil give kunden en linjerabat, kan du angive en værdi.  
    * Feltet Rabatprocent indeholder en værdi i procent, som det samlede bruttobeløb på linjen skal reduceres med.  Hvis feltet Rabatprocent allerede indeholder en værdi, er den kopieret fra en gyldig samhandelsaftale. Hvis feltet er tomt, og du vil give kunden en linjerabat, kan du angive en værdi.  
    * Feltet Nettobeløb indeholder en værdi, der beregnes ud fra linjes antal og enhedspris reguleret af rabatter.  Du kan tilsidesætte den beregnede værdi for en anden.  

## <a name="review-the-order-totals"></a>Gennemse ordretotalerne
1. Klik på Salgsordre i handlingsruden.
2. Klik på Totaler.
    * Siden Totaler vise oplysninger om hele ordren. Dette omfatter subtotalbeløb, som er summen af alle linjenettobeløb justeret for eventuelle linjerabatter, det samlede fakturabeløb, som er et subtotalbeløb justeret for eventuel rabat på ordreniveau, afgifter og moms, kundens kreditmaksimum og andet.  Fakturabeløbet er det beløb, der skal vises på kundens fakturadokument.  
3. Klik på OK.


