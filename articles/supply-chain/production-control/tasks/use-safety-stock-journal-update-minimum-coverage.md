---
title: Bruge sikkerhedslagerkladde for at opdatere minimumdisponering
description: Denne fremgangsmåde viser, hvordan du kan beregne minimumdækningsforslaget baseret på historiske transaktioner og derefter opdatere varedisponeringen med forslagene.
author: johanhoffmann
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ae2209fc2412a4a67b46d6eb82ecb70aafc0159
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573603"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a>Bruge sikkerhedslagerkladde for at opdatere minimumdisponering

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du kan beregne minimumdækningsforslaget baseret på historiske transaktioner og derefter opdatere varedisponeringen med forslagene. Dette kan du gøre ved hjælp af sikkerhedslagerkladden. Det demodatafirma, der bruges til at oprette denne opgave, er USMF. Denne opgave er beregnet til produktionsplanlæggeren og skal hjælpe med at vedligeholde minimumdækning.


## <a name="create-a-new-safety-stock-journal-name"></a>Opret et nyt sikkerhedslagerkladdenavn
1. Gå i **Navigationsrude** til **Varedisponering > Opsætning > Sikkerhedslagerkladdenavne**.
2. Klik på **Ny**.
3. Skriv 'Materiale' i feltet **Navn**.
4. Skriv 'Materiale' i feltet **Beskrivelse**.
5. Luk siden.

## <a name="create-a-safety-stock-journal"></a>Opret en sikkerhedslagerkladde
1. Gå i **Navigationsrude** til **Varedisponering > Varedisponering > Kørsel > Beregning af sikkerhedslager**.
2. Klik på **Ny**.
3. Indtast eller vælg en værdi i feltet **Navn**. Vælg den sikkerhedslagerkladde, du har oprettet, for eksempel Materiale.  
4. Klik på **Opret linjer**.
5. Indtast en dato i feltet **Fra dato**.  
6. Indtast en dato i feltet **Til dato**.
7. Klik på **OK**. Derved oprettes der linjer for de dimensioner, der har lagerposteringer.  

## <a name="calculate-proposal"></a>Beregn forslag
1. Klik på **Beregn forslag**.
2. Vælg indstillingen **Brug gns.afgang under gennemløbstiden**.
3. Indstil **Multiplikationsfaktor** til '10'. Miltipliceringsfaktoren bruges til at justere forslaget. Fordi demodata kun har få transaktioner, skal du angive faktoren for at få et realistisk forslag.  
4. Klik på **OK**. Rul ned for at finde M0002 og M0003. Vis kolonnen **Beregnet minimumantal**.   

## <a name="update-minimum-quantity"></a>Opdater minimummængde
1. Indtast et tal i feltet **Ny minimummængde**. Opdater den nye minimummængde, så den svarer til værdien i den beregnede minimummængde. Hvis det beregnede minimum er nul, kan du angive den ønskede fremtidige værdi. Du kan f.eks. angive den beregnede minimummængde i dette felt for M0002, der har lagersted 12.  
2. Find og vælg den ønskede post på listen. Du kan f.eks. vælge M0002, der har lagersted 12.  
3. Indtast et tal i feltet **Ny minimummængde**. Opdater den nye minimummængde, så den svarer til værdien i den beregnede minimummængde. Hvis det beregnede minimum er nul, kan du angive den ønskede fremtidige værdi.  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Bogfør det nye minimumantal, og valider resultatet
1. Klik på **Bogfør**.
2. Klik på **OK**.
3. Klik for at følge linket i feltet **Varenummer**.
4. Klik for at følge linket i feltet **Varenummer**.
5. Klik på Plan i **Handlingsrude**.
6. Klik på **Varedisponering**. Bemærk, at **Minimumantal** er blevet opdateret med det nye minimumsantal fra sikkerhedslagerkladden.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]