---
title: Opret salgsordrer
description: Denne procedure viser, hvordan du opretter en salgsordre.
author: omulvad
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User, SalesTableDelete, SalesTableListPagePreviewPage, SalesUpdateRemain
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a52c512d630e560afac998e1a35e71204d98f5d1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841353"
---
# <a name="create-sales-orders"></a>Opret salgsordrer

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du opretter en salgsordre. Du kan bruge denne procedure i demodatafirmaet USMF. Salgsordrer oprettes typisk af en salgsordreprocessor. 

## <a name="enter-sales-order-header-details"></a>Angiv oplysninger om salgsordrehovedet
1. Gå til **Navigationsrude > Moduler > Salg og marketing > Salgsordrer > Alle salgsordrer**.
2. Vælg **Ny**.
3. Vælg rullelisten i feltet **Kundekonto** for at åbne opslaget.
4. Find og vælg kundeposten på listen.
    - I dette eksempel skal du vælge kundenummer "US 004"  
5. Vælg **OK**.

## <a name="enter-sales-order-line-details"></a>Angiv oplysninger om salgsordrelinjen
    
De produkter, der sælges af organisationen, kan findes i varianter, der er differentieret efter dimensioner, f.eks. konfiguration, farve, størrelse og type. Produkter kan også konfigureres til at bruge lagringsdimensioner som sted, lagersted, og palle og sporingsdimensioner som batch- og serienumre. Når disse dimensioner er tildelt, skal du vælge værdier for dimensionerne på ordrelinjen. For at forbedre effektiviteten af ordreindtastning kan du føje de respektive dimensionsfelter til ordregitteret.
    
1. I afsnittet **Salgsordrelinjer** skal du vælge **Salgsordrelinjen**.
2. Vælg **Dimensioner**.
    
    I dette eksempel skal du vælge dimensionerne farve, lokation og lagersted. De dimensioner, du vælger her, vises i salgsordregitteret. Hvis dine valg skal bevares, skal du angive indstillingen **Gem opsætningen** til Ja.
    
3. Vælg **OK**.
4. Klik på rullelisten i feltet **Varenummer** for at åbne opslaget.
5. I dette eksempel skal du vælge varenummer T0004.
    - Hvis varen er en del af en salgskategori, vises varenavnet automatisk i feltet Salgskategori.  
    - Hvis produktdimensionsfelterne allerede indeholder en værdi, er det fordi, værdien blev kopieret fra produktposten, hvor den er defineret som standardproduktdimension. Du kan når som helst ændre standardværdien.   
6. Klik på rullelisten i feltet **Farve** for at åbne opslaget.
7. Find og vælg den ønskede post på listen.
8. Angiv et tal i feltet **Antal**.
    - Hvis varen sælges i andre enheder end dem, de er købt, produceret og gemt i, og der er angivet en måleenhed for salg i produktposten, vises denne værdi i feltet **Enhed**. Du kan til enhver tid ændre værdien.   
    - Hvis feltet **Sted** allerede indeholder en værdi, kopieres værdien fra ordrehovedet eller fra ordreindstillinger, der er knyttet til produktet. Du kan til enhver tid ændre værdien. Vælg en værdi, hvis feltet er tomt.   
    - Hvis feltet **Enhedspris** allerede indeholder en værdi, kopieres værdien fra en gyldig samhandelsaftale eller fra produktposten. (Enhedsprisen kan også stamme fra en salgsaftale, men processen til oprettelse af salgsordrer fra salgsaftaler afviger fra den, der vises her). Angiv en værdi, hvis feltet er tomt.   
    - Feltet **Rabat** indeholder et rabatbeløb pr. produktenhed. For at beregne det samlede linjerabatbeløbet ganges rabatværdien med linjeantallet. Hvis feltet **Rabat** allerede indeholder en værdi, kopieres værdien fra en gyldig samhandelsaftale. Hvis feltet er tomt, og du vil give kunden en linjerabat, kan du angive en værdi.  
    - Feltet **Rabatprocent** indeholder en værdi i procent, som det samlede bruttobeløb på linjen skal reduceres med.  Hvis feltet **Rabatprocent** allerede indeholder en værdi, er den kopieret fra en gyldig samhandelsaftale. Hvis feltet er tomt, og du vil give kunden en linjerabat, kan du angive en værdi. 
    - Feltet **Nettobeløb** indeholder en værdi, der beregnes ud fra linjens antal og enhedspris reguleret af rabatter.  Du kan tilsidesætte den beregnede værdi for en anden.  

## <a name="review-the-order-totals"></a>Gennemse ordretotalerne
1. Vælg **Salgsordre** i **handlingsruden**.
2. Vælg **Totaler**.
    
    Siden **Totaler** viser oplysninger om hele ordren. Dette omfatter subtotalbeløb, som er summen af alle linjenettobeløb justeret for eventuelle linjerabatter, det samlede fakturabeløb, som er et subtotalbeløb justeret for eventuel rabat på ordreniveau, afgifter og moms, kundens kreditmaksimum og andet. Fakturabeløbet er det beløb, der skal vises på kundens fakturadokument.  
    
3. Vælg **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]