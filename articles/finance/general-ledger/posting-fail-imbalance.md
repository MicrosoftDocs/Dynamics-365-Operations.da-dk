---
title: Kladdebogføringsfejl på grund af ubalance
description: Denne artikel forklarer, hvorfor debiteringer og krediteringer muligvis ikke afstemmes i bilagsposteringer, så posteringerne ikke kan bogføres. Artiklen indeholder også fremgangsmåder for rettelse af fejlen.
author: kweekley
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f5afded3d5c42f8dab465b668e4c1fcdaed8c215
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861323"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Kladdebogføringsfejl på grund af ubalance

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvorfor debiteringer og krediteringer muligvis ikke afstemmes i bilagsposteringer, så posteringerne ikke kan bogføres. Artiklen indeholder også fremgangsmåder for rettelse af fejlen.

## <a name="symptom"></a>Symptom

I nogle tilfælde kan en kladde ikke bogføres, og følgende meddelelse vises: "Posteringerne for et bestemt bilag afstemmes ikke pr. en bestemt dato (regnskabsvaluta: 0,01 - rapporteringsvaluta: 0,06)." Hvorfor kan kladden ikke bogføres?

## <a name="resolution"></a>Løsning

Ved bogføring til Finans skal alle bilag afstemmes i transaktionsvalutaen, regnskabsvalutaen og rapporteringsvalutaen, hvis disse valutaer er defineret på siden **Finans**. (Bilag afstemmes, når de samlede debiteringer svarer til de samlede krediteringer).

Nederst på kladdelinjesiden vises totalerne i regnskabsvalutaen og rapporteringsvalutaen. De vises **ikke** i transaktionsvalutaen for posteringer i udenlandsk valuta. Den fejlmeddelelse, som brugerne modtager under simuleringen eller bogføringen, viser desuden kun forskellene i regnskabsvalutaen og rapporteringsvalutaen. Den viser dem ikke i transaktionsvalutaen, da et enkelt bilag kan have mere end én transaktionsvaluta, og kladden kan indeholde bilag i forskellige transaktionsvalutaer. Det er derfor vigtigt at kontrollere manuelt, at beløbene i transaktionsvalutaen for hvert bilag, der kun har én posteringsvaluta, afbalanceres.

### <a name="transaction-currency"></a>Transaktionsvaluta

Ved simulering og bogføring kontrollerer systemet, at alle bilag, der kun har én transaktionsvaluta, er afstemt i transaktionsvalutaen. For hvert bilag, der er angivet, kan der være en eller flere valutaer for transaktionsvalutaen. Et bilag, der angives i finanskladden, kan f.eks. have to transaktionsvalutaer, når der overføres kontanter fra en bankkonto, som bruger euro (EUR), til en bankkonto, der bruger canadiske dollar (CAD).

Hvis et bilag kun indeholder én transaktionsvaluta, skal de samlede debiteringer være lig med de samlede krediteringer i transaktionsvalutaen for det pågældende bilag. Der er opstået følgende scenarier for debitorer, hvor bogføringen mislykkedes, da beløbene for transaktionsvalutaen ikke er blevet afstemt:

- De samlede debiteringer og krediteringer blev **ikke** afstemt i transaktionsvalutaen, men er blevet afstemt regnskabsvalutaen og rapporteringsvalutaen. En debitor antog, at bilaget stadig vil blive bogført. Denne antagelse er imidlertid ikke korrekt. **Beløbene i transaktionsvalutaen på et bilag skal altid afstemmes, når alle linjer på bilaget har samme transaktionsvaluta.**
- Bilaget blev importeret med en dataenhed via DMF (Data Management Framework), og brugeren har tænkt, at beløbene i transaktionsvalutaen er afbalancerede. I importfilen havde nogle af beløbene mere end to decimaler, og der blev medtaget mere end to decimaler, da beløbene blev importeret. Debiteringerne svarer derfor ikke til krediteringerne, da de var forskellige med en brøkdel af en øre. Kladden afspejler ikke denne forskel på linjerne på bilaget, da de viste beløb kun har to decimaler.
- Bilaget blev importeret med en dataenhed via DMF, og brugeren troede, at beløbene i transaktionsvalutaen blev afstemt. Selvom **bilaget** er blevet afstemt, har visse linjer på bilaget forskellige transaktionsdatoer. Hvis du har tilføjet de samlede debiteringer og krediteringer i transaktionsvalutaen pr. **bilag og transaktionsdato**, er de ikke blevet afstemt. Dette krav gennemtvinges, når du angiver et bilag via finanskladden i systemet. Den gennemtvinges dog ikke, når et bilag importeres med en dataenhed via DMF.

I et understøttet scenarie kan et bilag have mere end én transaktionsvaluta. I dette tilfælde kontrollerer systemet **ikke**, om debetbeløbene svarer til krediteringerne i transaktionsvalutaen, fordi valutaerne ikke stemmer overens. Systemet kontrollerer i stedet, at beløb i regnskabsvalutaen og rapporteringsvalutaen er blevet afstemt.

### <a name="accounting-currency"></a>Regnskabsvaluta

Hvis alle linjer på et bilag har samme transaktionsvaluta, og hvis beløbene i transaktionsvalutaen er afstemt, kontrollerer systemet, at beløbene i regnskabsvalutaen er afstemt. Hvis bilaget er angivet i en fremmed valuta, bruges valutakursen på bilagslinjerne til at omregne beløb i transaktionsvalutaen til regnskabsvalutaen. For det første oversættes hver linje i bilaget og afrundes til to decimaler. Derefter lægges linjerne sammen for at bestemme de samlede debiteringer og krediteringer. Da hver linje omregnes, vil de samlede debiteringer og krediteringer muligvis ikke blive afstemt. Hvis den absolutte værdi af differencen ligger inden for den værdi for **Maksimal øredifference**, der er defineret på siden **Finansparametre**, bogføres bilaget, og differencen bogføres automatisk på øredifferencekontoen.

Hvis bilaget har mere end én transaktionsvaluta, omregnes hver linje på bilaget til regnskabsvalutaen, rundes op til to decimalpladser, og derefter summeres linjerne for at bestemme de samlede debiteringer og krediteringer. Debiteringer og krediteriner skal afstemmes i regnskabsvalutaen, for at beløbet kan betragtes som afstemt.  Der føjes aldrig en øredifferencekonto til bilaget i regnskabsvalutaen for at afstemme debet- og kreditbeløbene. 

### <a name="reporting-currency"></a>Rapporteringsvaluta

Hvis alle linjer på et bilag har samme transaktionsvaluta, og hvis beløbene i transaktionsvalutaen er afstemt, kontrollerer systemet, at beløbene i rapporteringsvalutaen er afstemt. Hvis bilaget er angivet i en fremmed valuta, bruges valutakursen på bilagslinjerne til at omregne beløb i transaktionsvalutaen til rapporteringsvalutaen. For det første oversættes hver linje i bilaget og afrundes til to decimaler. Derefter lægges linjerne sammen for at bestemme de samlede debiteringer og krediteringer. Da hver linje omregnes, vil de samlede debiteringer og krediteringer muligvis ikke blive afstemt. Hvis differencen ligger inden for den værdi for **Maksimal øreafrunding i rapporteringsvaluta**, der er defineret på siden **Finansparametre**, bogføres bilaget, og differencen bogføres automatisk på øredifferencekontoen.

Hvis bilaget har mere end én transaktionsvaluta, omregnes hver linje på bilaget til rapporteringsvalutaen, rundes op til to decimalpladser, og derefter summeres linjerne for at bestemme de samlede debiteringer og krediteringer. Debiteringer og krediteriner skal afstemmes i rapporteringsvalutaen, for at beløbet kan betragtes som afstemt.  Der føjes aldrig en øredifferencekonto til bilaget i rapporteringsvalutaen for at afstemme debet- og kreditbeløbene.

### <a name="example-for-an-accounting-currency-imbalance"></a>Eksempel på en ubalance i regnskabsvaluta

> [!NOTE]
> Rapporteringsvalutabeløbet beregnes ud fra transaktionsvalutabeløbet på samme måde som regnskabsvalutabeløbet.

Valutakurs: 1,5

| Linje | Bilag | Konto | Valuta | Debet (transaktion) | Kredit (transaktion) | Debet (regnskab) | Kredit (regnskab) |
|---|---|---|---|---|---|---|---|
| 1 | 001 | 1101-01 | EUR | 3.33 | | 5,00 (4.995) | |
| 2 | 001 | 1101-02 | EUR | 3.33 | | 5,00 (4.995) | |
| 3 | 001 | 1101-03 | EUR | 3.34 | | 5.01 | |
| 4 | 001 | 4101- | EUR | | 10.00 | | 15.00 |
| **Sum** | | | | **10.00** | **10.00** | **15.01** | **15.00** |

Regnskabsvalutaen har en saldo på 0,01. Hvis den maksimale øre afrunding i regnskabsvalutaen er mindst 0,01, bogføres differencen dog automatisk på øredifferencekontoen, og bilaget bogføres korrekt.
