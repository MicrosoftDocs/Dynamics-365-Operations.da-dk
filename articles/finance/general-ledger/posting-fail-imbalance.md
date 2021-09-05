---
title: Kladdebogføringsfejl på grund af ubalance
description: Dette emne forklarer, hvorfor debiteringer og krediteringer muligvis ikke afstemmes i bilagsposteringer, så posteringerne ikke kan bogføres. Emnet indeholder også fremgangsmåder for rettelse af fejlen.
author: kweekley
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a59724ff698b6ad0e84b0642240da5f8953ab3d1
ms.sourcegitcommit: 9642494da87c0d237f9fcbe15df14315d9e88fa2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/15/2021
ms.locfileid: "7385717"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Kladdebogføringsfejl på grund af ubalance

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvorfor debiteringer og krediteringer muligvis ikke afstemmes i bilagsposteringer, så posteringerne ikke kan bogføres. Emnet indeholder også fremgangsmåder for rettelse af fejlen.

## <a name="symptom"></a>Symptom

I nogle tilfælde kan en kladde ikke bogføres, og følgende meddelelse vises: "Posteringerne for et bestemt bilag afstemmes ikke pr. en bestemt dato (regnskabsvaluta: 0,01 - rapporteringsvaluta: 0,06)." Hvorfor kan kladden ikke bogføres?

## <a name="resolution"></a>Løsning

Ved bogføring til Finans skal alle bilag afstemmes i transaktionsvalutaen, regnskabsvalutaen og rapporteringsvalutaen, hvis disse valutaer er defineret på siden **Finans**. (Bilag afstemmes, når de samlede debiteringer svarer til de samlede krediteringer).

Nederst på kladdelinjesiden vises totalerne i regnskabsvalutaen og rapporteringsvalutaen. De vises **ikke** i transaktionsvalutaen for posteringer i udenlandsk valuta. Den fejlmeddelelse, som brugerne modtager under simuleringen eller bogføringen, viser desuden kun forskellene i regnskabsvalutaen og rapporteringsvalutaen. Den viser dem ikke i transaktionsvalutaen, da et enkelt bilag kan have mere end én transaktionsvaluta, og kladden kan indeholde bilag i forskellige transaktionsvalutaer. Det er derfor vigtigt at kontrollere, at beløbene i transaktionsvalutaen for hvert bilag er blevet afstemt.

### <a name="transaction-currency"></a>Transaktionsvaluta

Ved simulering og bogføring kontrollerer systemet, at alle bilag er afstemt i transaktionsvalutaen. For hvert bilag, der er angivet, kan der være en eller flere valutaer for transaktionsvalutaen. Et bilag, der angives i finanskladden, kan f.eks. have to transaktionsvalutaer, når der overføres kontanter fra en bankkonto, som bruger euro (EUR), til en bankkonto, der bruger canadiske dollar (CAD).

Hvis et bilag kun indeholder én transaktionsvaluta, skal de samlede debiteringer være lig med de samlede krediteringer for det pågældende bilag. Der er opstået følgende scenarier for debitorer, hvor bogføringen mislykkedes, da beløbene for transaktionsvalutaen ikke er blevet afstemt:

- De samlede debiteeringer og krediteringer blev **ikke** afstemt i transaktionsvalutaen, men er blevet afstemt regnskabsvalutaen og rapporteringsvalutaen. En debitor antog, at bilaget stadig vil blive bogført. Denne antagelse er imidlertid ikke korrekt. **Beløbene i transaktionsvalutaen på et bilag skal altid afstemmes, når alle linjer på bilaget har samme valuta.**
- Bilaget blev importeret via Microsoft Excel, og brugeren troede, at beløbene i transaktionsvalutaen blev afstemt. I Excel-projektmappen blev de beløb, der blev importeret, angivet som værdier af typen **Numerisk**, ikke **Valuta**. I dette scenarie havde de numeriske beløb i projektmappen mere end to decimaler, og der blev medtaget mere end to decimaler, da beløbene blev importeret. Debiteringerne svarer derfor ikke til krediteringerne, da de var forskellige med en brøkdel af en øre. Kladden afspejler ikke denne forskel på linjerne på bilaget, da de viste beløb kun har to decimaler.
- Bilaget blev importeret via Excel, og brugeren troede, at beløbene i transaktionsvalutaen blev afstemt. Selvom bilaget er blevet afstemt, har visse linjer på bilaget forskellige transaktionsdatoer. Hvis du har tilføjet de samlede debiteringer og krediteringer pr. bilag og transaktionsdato, er de ikke blevet afstemt. Systemet forhindrer nu dette scenarie. Et bilag kan kun have én transaktionsdato. Dette krav gennemtvinges, når du angiver et bilag via finanskladden i systemet. Det blev oprindeligt ikke gennemtvunget ved import af et bilag via Excel.

I et understøttet scenarie kan et bilag have mere end én transaktionsvaluta. I dette tilfælde kontrollerer systemet **ikke**, om debetbeløbene svarer til krediteringerne i transaktionsvalutaen, fordi valutaerne ikke stemmer overens. Systemet kontrollerer i stedet, at beløb i regnskabsvalutaen er blevet afstemt.

### <a name="accounting-currency"></a>Regnskabsvaluta

Hvis alle linjer på et bilag har samme transaktionsvaluta, og hvis beløbene i transaktionsvalutaen er afstemt, kontrollerer systemet, at beløbene i regnskabsvalutaen er afstemt. Hvis bilaget er angivet i en fremmed valuta, bruges valutakursen på bilagslinjerne til at omregne beløb i transaktionsvalutaen til regnskabsvalutaen. For det første omregnes hver linje på bilaget. Derefter lægges linjerne sammen for at bestemme de samlede debiteringer og krediteringer. Da hver linje omregnes, vil de samlede debiteringer og krediteringer muligvis ikke blive afstemt. Hvis differencen ligger inden for den værdi for **Maksimal øredifference**, der er defineret på siden **Finansparametre**, bogføres bilaget, og differencen bogføres automatisk på øredifferencekontoen.

Hvis bilaget har mere end én transaktionsvaluta, omregnees hver linje på bilaget til regnskabsvalutaen, og derefter summeres linjerne for at bestemme de samlede debiteringer og krediteringer. Debiteringer og krediteriner skal afstemmes, og der må ikke være differencer på grund af øreafrunding, for at beløbet kan betragtes som afstemte.

### <a name="reporting-currency"></a>Rapporteringsvaluta

Hvis alle linjer på et bilag har samme transaktionsvaluta, og hvis beløbene i transaktionsvalutaen er afstemt, kontrollerer systemet, at beløbene i rapporteringsvalutaen er afstemt. Hvis bilaget er angivet i en fremmed valuta, bruges valutakursen på bilagslinjerne til at omregne beløb i transaktionsvalutaen til rapporteringsvalutaen. For det første omregnes hver linje på bilaget. Derefter lægges linjerne sammen for at bestemme de samlede debiteringer og krediteringer. Da hver linje omregnes, vil de samlede debiteringer og krediteringer muligvis ikke blive afstemt. Hvis differencen ligger inden for den værdi for **Maksimal øreafrunding i rapporteringsvaluta**, der er defineret på siden **Finansparametre**, bogføres bilaget, og differencen bogføres automatisk på øredifferencekontoen.

Hvis bilaget har mere end én transaktionsvaluta, omregnees hver linje på bilaget til rapporteringsvalutaen, og derefter summeres linjerne for at bestemme de samlede debiteringer og krediteringer. Debiteringer og krediteriner skal afstemmes, og der må ikke være differencer på grund af øreafrunding, for at beløbet kan betragtes som afstemte.
