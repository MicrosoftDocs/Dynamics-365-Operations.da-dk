---
title: Oprette en indkøbsordre
description: Dette emne viser, hvordan du opretter en indkøbsordre manuelt.
author: mkirknel
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventDimParmFixed, InventItemIdLookupPurchase, InventProductDimensionLookup, PurchTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec91174f291bcfa7027a93ca344823561cc29e3f
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018142"
---
# <a name="create-a-purchase-order"></a>Oprette en indkøbsordre

[!include [banner](../../includes/banner.md)]

Dette emne viser, hvordan du opretter en indkøbsordre manuelt. Det er mere almindeligt for indkøbsordrer, at de oprettes automatisk som resultat af varedisponering, direkte levering og andre processer. Indkøbsordrer oprettes typisk af en indkøbsagent. Det viste eksempel kan bruges i USMF-demodatafirmaet ved hjælp af de værdier, der foreslås i noterne til de forskellige trin.


## <a name="create-the-purchase-order-header"></a>Oprette indkøbsordrehovedet
1. Gå til **Navigationsruden > Moduler > Indkøb og forsyning > Indkøbsordrer > Alle indkøbsordrer**.
2. Vælg **Ny**.
3. Vælg kreditorkonto **US-101**. Når du vælger en kreditor, kopieres oplysninger fra kreditorposten, f.eks. adresse, fakturakonto, leveringsbetingelser og leveringsmåde, som standardværdier til ordrehovedet. Du kan ændre disse værdier når som helst.  
4. Udvid sektionen **Generelt**.

    - Feltet **Lokation** og feltet **Lagersted** angiver, hvor de indkøbte varer eller tjenesteydelser skal leveres. Standardleveringsadressen er lokationen. Begge felter kan udfyldes med værdier, der er konfigureret for den valgte kreditor, eller du kan angive dem manuelt.  
    - Feltet **Leveringsdato** bruges til at angive, hvornår indkøbte varer og tjenester skal leveres. Du kan angive en enkelt leveringsdato for ordren, eller de enkelte ordrelinjer kan gives entydige leveringsdatoer. Hvis den leveringsdato, der er angivet her, ikke kan opfyldes for bestemte produkter eller tjenester, fordi de har længere leveringstider, oprettes linjerne med en senere leveringsdato for at tage højde for dette.  

5. Udvid sektionen **Administration**. Feltet **Bestiller** kan bruges til at angive, hvem der afgiver ordren. Dette kan være praktisk at dele med kreditoren, i tilfælde af at de har brug at kontakte den pågældende person. Feltet kan tildeles en værdi automatisk, hvis den aktuelle brugerkonto er tilknyttet et navn på siden **Brugere**.  
6. Vælg **OK**. Ordrehovedet er nu blevet oprettet. Når du arbejder med indkøbsordrelinjer, vises kun en oversigt over oplysningerne i hovedet. Hvis du vil se resten af oplysningerne, skal du vælge **Hoved**.  

## <a name="add-a-purchase-order-line"></a>Tilføje en indkøbsordrelinje
1. Vælg **Indkøbsordrelinje**.
2. Vælg **Dimensioner**. Produkter kan forekomme i varianter, der differentieres efter dimensioner som f.eks. farve, størrelse eller typografi. Produkter kan også konfigureres til at bruge lagringsdimensioner som f.eks. lokation og lagersted. Der er også valgfrie sporingsdimensioner som f.eks. batch- og serienumre. Du kan tilføje de dimensionsfelter, du bruger oftest, direkte til ordregitteret for at forbedre effektiviteten af ordreindtastningen.  
3. Markér afkrydsningsfeltet **Farve**. Valgfrit: Hvis du vælger feltet **Gem opsætning** , vil de dimensioner, du har valgt, også blive vist på ordrelinjegitteret, næste gang du åbner siden Indkøbsordre.  
4. Vælg **OK**.
5. Vælg **T0004** i feltet **Varenummer**.

    - Der oprettes ordrelinjer for produkter og tjenester ved at angive et varenummer eller udgifter ved at angive en indkøbskategori. 
    - Feltet **Indkøbskategori** bruges til at tilføje linjer, hvor indkøbte varer udgiftsføres direkte og ikke går ind på lageret. Det betyder, at hvis du skal udgiftsføre et indkøb, kan du oprette en indkøbsordrelinje, der angiver en indkøbskategori, i stedet for at oprette en linje med et varenummer. Varer kan også være knyttet til en indkøbskategori, og i så fald vises indkøbskategorien kun som vejledende oplysning.  

6. Indtast eller vælg en værdi i feltet **Farve**. Felterne **Lokation** og **Lagersted** udfyldes typisk med værdier fra ordrehovedet, men det er muligt at tilsidesætte felterne, hvis nogle linjer skal leveres til andre lokationer.  
7. Angiv et tal i feltet **Antal**.

    - Vælg det antal, du vil indkøbe. Feltet **Antal** udfyldes automatisk med det mindste tilladte ordreantal for produktet, hvis dette er konfigureret, eller med værdien 1.  
    - Feltet **Enhed** angiver måleenheden for det bestilte antal. Typisk hentes enheden automatisk fra købsmåleenheden i produktmasterdataene, men du kan ændre den.  
    - Feltet **Enhedspris** indeholder typisk en værdi fra en købsaftale eller en samhandelsaftale. Det er muligt at ændre enhedsprisen på de enkelte ordrelinjer, f.eks. hvis der er forhandlet en særlig pris med kreditoren.  
    - Feltet **Rabat** repræsenterer et rabatbeløb pr. enhed. Denne rabat nedsætter derfor enhedsprisen med rabatten. Denne rabat gives normalt automatisk ud fra købsaftaler eller samhandelsaftaler, men det er muligt at tilsidesætte den på enkelte linjer, hvis der er forhandlet særlige rabatter med kreditoren.  
    - Der kan angives en rabatprocent, der reducerer nettobeløbet for linjen. Rabatprocenten gives ofte automatisk ud fra købsaftaler eller samhandelsaftaler, men det er muligt at tilsidesætte den på enkelte linjer, hvis der er forhandlet en særlig rabatprocent med kreditoren.  
    - Værdien i feltet **Nettobeløb** beregnes ud fra de andre felter på linjen, herunder antal, enhedspris, rabat og rabatprocent. Det er muligt at ændre nettobeløbet, men felterne **Enhedspris** , **Rabat** og **Rabatprocent** vil være tomme, og når du bogfører linjen, vil det bogførte beløb være proportionalt med nettobeløbet. Feltet **Nettobeløb** bruges normalt kun til at få vist nettobeløbet for linjen.  

8. Vis eller skjul sektionen **Linjedetaljer**.
9. Vælg fanen **Levering**. Der kan tildeles en entydig leveringsdato for hver ordrelinje. Datoen arves fra feltet i indkøbsordrehovedet, men du kan ændre den.  

## <a name="review-order-totals"></a>Gennemse ordretotaler
1. Vælg **Totaler**.

    - Hvis du ikke kan se handlingen **Totaler** , skal du vælge fanen **Indkøbsordre** på handlingsruden.  
    - Denne dialogboks viser totaler for hele ordren.  
    - Med feltet **Valg** kan du ændre grundlaget for beregningen af totaler. For eksempel kan du vælge **Antal produktkvitteringer** for at få vist totaler, der relaterer til beløbet af produkt(er), der er modtaget, eller **Bestilt antal** for at få vist det produktantal, der er bestilt.  

2. Vælg **OK**.

