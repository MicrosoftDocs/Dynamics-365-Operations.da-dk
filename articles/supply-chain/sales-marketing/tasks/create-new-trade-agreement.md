---
title: Oprette en ny samhandelsaftale
description: Denne fremgangsmåde viser, hvordan du kan oprette en samhandelsaftale, hvor du registrerer en ny produktsalgspris, som du har aftalt med en bestemt debitor.
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e49793fc7f6b3f37bafae05770d4b23d24171329
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974879"
---
# <a name="create-a-new-trade-agreement"></a>Oprette en ny samhandelsaftale

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du kan oprette en samhandelsaftale, hvor du registrerer en ny produktsalgspris, som du har aftalt med en bestemt debitor. Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data. Hvis du bruger dine egne data, før du starter denne vejledning, skal du sikre, at der findes et navn på en Samhandelskladde, hvor standardrelationen er indstillet til "Pris (salg)".


## <a name="create-and-post-a-new-trade-agreement-journal"></a>Opret og bogfør en ny samhandelsaftalekladde
1. Gå til **Navigationsrude > Moduler > Salg og marketing > Priser og rabatter > Samhandelskladder**.
2. Klik på **Ny**.
3. Klik på rullelisten i feltet **Navn** for at åbne opslaget.
4. Find og vælg den ønskede post på listen.
5. Klik på **Linjer** i **handlingsruden**.
6. Vælg 'Tabel' i feltet **Kontokode**.
    
    I dette eksempel skal du opdatere prisen for en bestemt debitor, hvilket betyder, at du skal vælge Tabel. Hvis du har opdateret produktets listepris, skal du markere 'Alle', så den nye pris gælder for alle kunder. Hvis du differentierer priser mellem forskellige debitorsegmenter, skal du vælge Gruppe. Hvis du vil vælge Gruppe, skal du have indstillet Debitorprisgrupper.  

7. Klik på rullelisten i feltet **Kontovalg** for at åbne opslaget.
8. Find og vælg den ønskede post på listen.
9. Vælg 'Tabel' i feltet **Varekode**.
    
    Når du indtaster en samhandelsaftale af typen 'Pris (salg)', skal du kun vælge 'Tabel' i feltet **Varekode**. Det skyldes, at en pris er en absolut værdi og ikke kan være ens for alle produkter eller gruppe af produkter.
    
10. Klik på rullelisten i feltet **Varerelation** for at åbne opslaget.
11. Vælg det produkt, der inkluderes i dokumentet, på listen. Noter hvilket produkt, du har valgt.  
12. Indtast et minimumantal i feltet **Fra**.
    - Hvis debitoren skal bestille et minimumsantal, før de kan blive kvalificeret til den nye pris, skal du angive antallet her.  
    - Angiv en værdi i feltet **Til** for at angive det maksimale antal, hvorover aftalens pris ikke er gyldig. Hvis du tilbyder priser og rabatter, der er baseret på flere mængdereduktioner, skal du angive hver mængdekategori som et par med min. og maks. mængde i felterne **Fra** og **Til**.
13. Indtast en pris i feltet **Beløb i valuta**.
14. Indtast en dato, hvorfra denne aftale vil være gyldig, i feltet **Fra dato** i sektionen **Oplysninger**.
15. Klik på **Gem**.
16. Klik på **Valider**.
17. Klik på **Valider valgte linjer**.
18. Klik på **OK**.
19. Klik på **Bogfør**.
20. Klik på **OK**.

## <a name="view-trade-agreements-for-a-product"></a>Få vist samhandelsaftaler for et produkt
1. Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Produkter > Frigivne produkter**.
2. På listen skal du finde og vælge produktet, hvis pris du netop har opdateret.
3. Klik på **Sælg** i **handlingsruden**.
4. Klik på **Vis samhandelsaftaler**.
    
    Gennemse oplysningerne om samhandelsaftalens pris, som du lige har oprettet.    

5. Luk siden.

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="whitepaper"></a>Hvidbog
Yderligere oplysninger finder du ved at downloade følgende hvidbog (skrevet som support til AX2012, men gælder stadig for Dynamics 365 Supply Chain Management)
- [Samhandelsaftale](https://mbs.microsoft.com/files/public/CS/AX2012R3/TradeagreementsinAX.pdf)

### <a name="community-blogs"></a>Fællesskabsblogge
- [Salgspriser i Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
