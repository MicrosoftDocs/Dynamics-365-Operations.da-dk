---
title: Konfigurere rentefordeling for kontantkonti
description: I dette emne beskrives, hvordan du kan oprette dine bankkonti på siden for rentefordelingsregler. Du skal fuldføre denne opsætning, før du fordeler renten.
author: velofog
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNLedgerInterestDistributionRules, PSNLedgerInterestDistributionResults
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: public sector
ms.author: roschlom
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: d6ab44b7ddcbb3b7d3c394695e54398029654f78
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982032"
---
# <a name="set-up-interest-distribution-for-cash-accounts"></a>Konfigurere rentefordeling for kontantkonti

[!include[banner](../includes/banner.md)]

Din institution kan tildele (fordele) renten på en bankkonto til bestemte finanskonti baseret på den gennemsnitlige daglige saldo for kontantkonti. Du kan bruge denne proces til at oprette en avanceret finanspost for rentebeløbene. Du kan også generere rentebeløbene til gennemsyn uden at bogføre dem.

Før du fordeler renten, skal du oprette dine bankkonti på siden **Rentefordelingsregler**. Hver kombination af en kontantkonto og en bonus kan bruges til at beregne renter for en anden rentekonto.

## <a name="add-a-cash-account-for-interest-distribution"></a>Tilføje en kontantkonto til rentefordeling

1. Gå til **Finans \> Opsætning \> Bogføring \> Rentefordelingsregler**.
2. Vælg **Ny** for at tilføje en række.
3. I feltet **Kontantkonto** skal du angive den kontantkonto, der indeholder en del af de samlede kontanter.
4. Valgfrit: I feltet **Bonus** skal du angive bonusbeløbet for bonusrelaterede posteringsbeløb, der skal medtages i beregningen af kontantsaldoen for den tilknyttede kontantkonto. Hvis alle bonusser for kontantkontoen bogfører renter på den samme konto, kan du lade dette felt være tomt. Men hvis du angiver en rentekonto for en bestemt bonus, skal du angive en rentekonto for hver bonus til kontantkontoen.
5. Markér afkrydsningsfeltet **Deltag** for at medtage kontantkontiene i rentefordeling. Hvis markeringen i afkrydsningsfeltet fjernes, kan du ikke redigere andre felter i rækken. Kontantkonti, der ikke indgår, medtages på forespørgselssiden, så du kan gennemse den gennemsnitlige daglige saldo. Du kan dog ikke fordele renter på disse kontantkonti.
6. Angiv enten en bestemt rentekonto eller et projekt. Den værdi, du angiver, bestemmer, hvilken finanskonto renten bogføres på for den tilknyttede kontantkonto.

    - Angiv en specifik konto i feltet **Rentekonto**.
    - I feltet **Projekt-id** skal du angive et projekt, der skal bruges som grundlag for bogføring af renter. Denne konto bruges sammen med andre kontofaktorer til at bestemme hele den konto, der bogføres til.

7. Marker afkrydsningsfeltet **Negativ rente** for at beregne et negativt rentebeløb, når kontantkontoen har en negativ saldo. Hvis markeringen i dette afkrydsningsfelt fjernes, rapporterer kontantkontoen renten som 0 (nul) i stedet for et negativt beløb.
8. Rentekontoen for én kontantkonto kan modtage eventuelle øredifferencebeløb, når der beregnes rentefordeling. Markér afkrydsningsfeltet **Afrunding** for den pågældende kontantkonto. Du kan kun markere én kontantkonto som afrundingskontoen.

## <a name="distributing-interest"></a>Fordele renter

1. Gå til **Finans \> Periodisk \> Fordeling \> Rentefordeling**.
2. Vælg **Parametre**, og vælg derefter indstillinger i følgende felter:

    - I feltet **Total rente** skal du angive det samlede rentebeløb, der skal udbetales.
    - I felterne **Fra dato** og **Til dato** skal du vælge det datointerval, der skal beregnes gennemsnitlige daglige saldi for, baseret på posteringer i datointervallet.

3. Vælg **Fordel**.
4. Gennemse de beregnede rentebeløb, der er fordelt til kontiene. Du kan opdatere beløbene i feltet **Fordelt rente**.

    Hvis du ændrer rentebeløbene, skal feltet **Totalt fordelt** svare til feltet **Total rente**, før du kan fortsætte. Det beregnede rentebeløb kan medføre, at det samlede fordelte beløb ikke svarer til det samlede rentebeløb. Forskellen er som regel én procent. Denne difference anvendes på rentekontoen for den kontantkonto, der er markeret som afrundingskonto.

    > [!NOTE]
    > Hvis du ændrer rentebeløbene, men derefter vil nulstille dem til de beregnede rentebeløb, skal du vælge **Parametre** og derefter vælge **Fordel** for at generere renten ved hjælp af de oprindelige data.

5. Hvis du vil bogføre den fordelte rente, skal du vælge **Bogfør rente** og derefter vælge indstillinger i følgende felter:

    - Angiv regnskabsdatoen for den avancerede finanspost i feltet **Regnskabsdato**.
    - Vælg den projektkategori, der skal bruges til varerne i den avancerede finanspost, i feltet **Projektkategori**. Projektkategorien bestemmer også, hvilken hovedkonto den avancerede finanspost bogføres til.
    - Vælg den bogføringsdefinition, der skal bruges til den avancerede finanspost, i feltet **Bogføringsdefinition**.

6. Vælg **OK**. En meddelelse viser nummeret på den avancerede finanspost, der automatisk oprettes.

## <a name="calculated-amounts"></a>Beregnede beløb

Rentefordelingsprocessen omfatter nogle beregnede beløb.

| Beløb                | Udregning |
|-----------------------|-------------|
| Gennemsnitlig daglig saldo | Summen af de daglige saldi for hver dag i datointervallet divideret med antallet af dage i intervallet for hver kombination af en kontantkonto og en bonus. Kombinationerne defineres på siden **Rentefordelingsregler**. |
| Samlet daglig gennemsnit   | Summen af alle daglige saldi i gennemsnit, undtagen negative beløb for kontantkonti, der ikke tillader negative rente- og kontantkonti, som ikke er en del af en rentefordeling. |
| Procent af total      | Det gennemsnitlige daglige saldobeløb divideret med det samlede daglige gennemsnitlige beløb for hver kombination af en kontantkonto og en bonus. |
| Fordelt rente    | Den samlede rente på siden **Rentefordelingsparametre** ganget med procentdelen af det samlede beløb for kontantkontoen. Renter overføres ikke til kontantkonti, der har negative beløb, og som ikke tillader negativ rente. Renter distribueres heller ikke til kontantkonti, der ikke indgår i rentefordeling. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]