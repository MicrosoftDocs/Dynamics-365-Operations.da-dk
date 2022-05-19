---
title: Økonomiske standarddimensioner på finanskladder
description: Dette emne indeholder en beskrivelse af de regler, der definerer, hvordan økonomiske dimensionsværdier konfigureres på posteringer, der indtastes via finanskladder. Det indeholder også oplysninger om scenarier, hvor der bruges faste dimensioner.
author: kweekley
ms.date: 09/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransDaily, LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 51235b8a5dac50aad5031456760c970e50506d66
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713100"
---
# <a name="default-financial-dimensions-on-financial-journals"></a>Økonomiske standarddimensioner på finanskladder

[!include [banner](../includes/banner.md)]

Dette emne indeholder en beskrivelse af de regler, der definerer, hvordan økonomiske dimensionsværdier konfigureres på posteringer, der indtastes via finanskladder (men ikke via lagerkladder eller projektkladder). Det indeholder også oplysninger om scenarier, hvor der bruges faste dimensioner.

## <a name="symptom"></a>Symptom

De økonomiske dimensionsværdier er ikke angivet som forventet på kontoen eller modkontoen i en finanskladde. Følgende scenarier er to eksempler:

Der angives et bilag i en kladde i en finanskladde. Kontoen er en kreditorkonto, og modkontoen er en bankkonto. Leverandørens økonomiske dimensioner angives som standard på kontoen, men bankens økonomiske dimensioner angives ikke som standard på modkontoen. Dimensionsværdierne fra kontoen angives i stedet som standard på modkontoen.

En kunde har tildelt økonomiske standarddimensionsværdier, og en hovedkonto for indtægt har en fast dimensionsværdi tilknyttet den afdelingens økonomiske dimension. Der angives et bilag i en finanskladde.  Kontoen er debitor, og modkontoen er en finanskonto, specifikt omsætningskontoen med den faste dimensionsværdi. Den faste dimensionskonto er ikke angivet på modkontoen for hovedkontoen for indtægt. Den er i stedet angivet til afdelingen for dimensionen fra kontoen, som kommer fra debitoren.  Når bilaget er bogført, bruges den faste dimensionsværdi på den bogførte regnskabspost, men bilaget viser stadig debitorens afdelingsværdi på omsætningskontoen. 

Hvilke regler følges for økonomiske dimensionsværdier, der er angivet på bilag i en kladde?

## <a name="resolution"></a>Løsning

Følgende regler følges, når du som standard angiver økonomiske dimensionsværdier på linjerne i et bilag i finanskladder, f.eks. finanskladden eller kreditorfakturakladden. 

1. **Kladdehoved**

   - Dimensioner for kladdehoved angives som standard fra dimensioner for kladdenavne.

2. **Kladdelinjekonto**

   - Dimensioner for kladdelinjekonto angives som standard fra dimensioner for kladdehoved.
   - Hvis økonomiske dimensioner er tomme, angives deres værdier som standard fra debitor-, kreditor-, bank-, anlægsaktiv-, projekt- eller finansdimensioner.

     - Hvis kontotypen er **Finans**, behandles en fast dimension på en finanskonto som en standarddimension ved indtastning af posteringer.
     - Hvis kontotypen er **Debitor**, **Kreditor**, **Bank**, **Anlægsaktiver** eller **Projekt**, kan hovedkontoen endnu ikke bestemmes. Derfor angives der aldrig en fast dimension som standard for kontoen.

3. **Kladdelinje-modkonto**

 - Dimensioner for kladdelinje-modkonto angives først som standard fra dimensioner for kladdelinjekonto.

 - Hvis økonomiske dimensioner er tomme, angives den næste standardpost fra standarddimensionerne fra debitor-, kreditor-, bank-, anlægsaktiv-, projekt- eller finansdimensioner.
   1. Hvis modkontotypen er **Finans**, behandles en fast dimension på en finanskonto som en standarddimension ved indtastning af posteringer. Hvis der allerede er angivet en dimensionsværdi fra kontoen, tilsidesætter hovedkontoens standard- eller faste dimensionsværdi ikke den eksisterende værdi.
   2. Hvis modkontotypen er **Debitor**, **Kreditor**, **Bank**, **Anlægsaktiver** eller **Projekt**, kendes hovedkontoen endnu ikke, så en fast dimension vil aldrig blive standard for modkontoen.

4. **Postering**

    1. Under bogføringen evalueres hovedkontoen for hver linje i regnskabsposten (for både kontoen og modkontoen) for at bestemme, om der er en fast dimensionsværdi. Hvis der er defineret en fast dimension, erstattes alle eksisterende eller tomme værdier med den faste dimensionsværdi.

        Den faste dimensionsværdi vises **ikke** på kladdelinjerne efter bogføringen. Den vises i stedet på regnskabsposten, når du får vist bilaget, efter det er bogført.

    2. Der angives ingen andre dimensionsværdier som standard under bogføringen, herunder yderligere finanskonti, der tilføjes under bogføringen, f.eks. ørerundingskonti og interne på grund af eller forfalden fra konti. Standarddimensionsposterne for andre finanskonti tages fra kontoen eller modkontiene.

Med det formål at angive dimensionsværdier som standard, kan kladdestandardprocessen ikke bestemme, om en tom dimensionsværdi er blevet udfyldt med vilje, eller om den ikke er angivet som standard. Hvis en dimensionsværdi med vilje ikke udfyldes, kan der som standard stadig angives en værdi ved hjælp af den standardrækkefølge, der er beskrevet tidligere. Hvis du kræver, at en dimension har en tom værdi, skal du muligvis oprette en dimension, der har en værdi på **0** (nul) eller **Tom**, så den kan bruges i stedet for en tom dimension.

Gennemse følgende scenarier for eksempler på standardrækkefølgen for den økonomiske dimension.

### <a name="scenario-1"></a>Scenario 1

Gå til **Finans \> Kladdeopsætning \> Kladdenavne**, og vælg **GenJrn** kladdenavn. Definer derefter følgende værdier for de økonomiske standarddimensioner i oversigtspanelet **Økonomiske dimensioner**:

- **BUSINESSUNIT:** 001
- **DEPARTMENT:** 024

[![Siden Kladdenavne](./media/financial-dimension-defaulting-jrnl-names-01.png)](./media/financial-dimension-defaulting-jrnl-names-01.png)

Gå til **Finans \> Kladdeposteringer \> Finanskladde**, og opret en ny finanskladde, der bruger kladdenavnet **GenJrn**. Dimensionerne angives som standard fra kladdenavnet (LedgerJournalName-tabellen) til kladdehovedet (tabellen LedgerJournalTable), som vist under fanen **Økonomiske dimensioner**.

[![Fanen Økonomiske dimensioner på siden Finans](./media/financial-dimension-defaulting-genrl-jrnl-02.png)](./media/financial-dimension-defaulting-genrl-jrnl-02.png)

Gå til **Linjer**. Vælg **Finans** i feltet **Kontotype**, og skriv derefter **170150** i feltet **Kontotype**. Vælg derefter tasten **Tab** for at flytte ud af feltet. Dimensionerne angives som standard fra kladdehovedet. **Kontoværdien** vises derfor som **170150-001-024**.

[![Kladdelinjer til en finanskladde på siden Kladdebilag](./media/financial-dimension-defaulting-jrnl-vchr-03.png)](./media/financial-dimension-defaulting-jrnl-vchr-03.png)

Skift **Konto**-værdi til **170150-001-023**. Angiv enten et debet- eller kreditbeløb. Vælg **Finans** i feltet **Modkontotype**, og skriv derefter **600150** i feltet **Modkontotype**. Dimensionsværdierne angives som standard fra kontoen. **Modkontoværdien** vises derfor som **600150-001-023**.

### <a name="scenario-2"></a>Scenario 2

Brug de samme økonomiske dimensioner, som du har defineret for kladdenavnet i eksempel 1. Gå derefter til **Debitorer \> Debitorer \> Alle debitorer**, definer økonomiske standarddimensionsværdier for debitor US-001. Vælg debitoren for at åbne kundeoplysningerne. Under fanen **Økonomiske dimensioner** skal du beholde standardværdien for **BUSINESSUNIT**-dimensionen (**001**). Tilføj **COSTCENTER**-dimensionen, og angiv **007** som værdi.

Opret en ny finanskladde, der bruger kladdenavnet **GenJrn**. Under fanen **Økonomiske dimensioner** skal du ændre standardværdien for **BUSINESSUNIT** fra **001** til **002**.

Gå til **Linjer**. Vælg **Debitor** i feltet **Kontotype**, og skriv derefter **US-001** i feltet **Konto**. Hvis du vil have vist de økonomiske dimensioner for kontotyper, der ikke er finanskontotyper, skal du vælge **Finansdimensioner \> Konto**. Følgende standardposter for de økonomiske dimensionsværdier angives:

- **BUSINESSUNIT:** 002 – Standardposten tages fra kladdehovedet. Værdien **001** er ikke angivet som standard fra debitor US-001, da der allerede er angivet en standardværdi.
- **COSTCENTER:** 007 – Standardposten tages fra opsætningen af debitor US-001.
- **DEPARTMENT:** 024 – Standardposten tages fra kladdehovedet.

Vælg **Finans** tilbage på linjen i **Modkontotype**, og skriv derefter **600150** i feltet **Modkontotype**. Følgende standardposter for de økonomiske dimensionsværdier angives på linjen:

- **BUSINESSUNIT:** 002 – Standardposten tages fra kontoens økonomiske dimensioner. (Var oprindeligt angivet som standard fra kladdehovedet.)
- **DEPARTMENT:** 024 – Standardposten tages fra kontoens økonomiske dimensioner. (Var oprindeligt angivet som standard fra kladdehovedet.)
- **COSTCENTER:** 007 – Standardposten tages fra kontoens økonomiske dimensioner. (Var oprindeligt angivet som standard fra debitor.)

### <a name="scenario-3"></a>Scenario 3

Tilføj en ny linje i den kladde, du har brugt til eksempel 2. Vælg **Finans** i feltet **Kontotype**, og skriv derefter **170150** i feltet **Kontotype**. Ryd standarddimensionsværdierne, så det kun er 170150 der er tilbage. Vælg **Kunde** i feltet **Modkontotype**, og skriv derefter **US-001** i feltet **Modkontotype**. Følgende standardposter for de økonomiske dimensionsværdier angives:

- **BUSINESSUNIT:** 002 – Standardposten tages fra kladdehovedet, fordi kontodimensionsværdien er tom. Værdien **001** er ikke angivet som standard fra debitor US-001, da der allerede er angivet en standardværdi fra kladdehovedet. Hvis værdien **BUSINESSUNIT** med vilje ikke er udfyldt, skal du også fjerne den økonomiske dimension på modkontoen.
- **COSTCENTER:** 007 – Standardposten tages fra debitor US-001, da dimensionsværdien for kontodimensionen og kladdehovedet er tomme. Hvis værdien **COSTCENTER** med vilje ikke er udfyldt, skal du også fjerne den økonomiske dimension på modkontoen.
- **DEPARTMENT:** 024 – Standardposten tages fra kladdehovedet, fordi kontodimensionsværdien er tom. Hvis værdien **DEPARTMENT** med vilje ikke er udfyldt, skal du også fjerne den økonomiske dimension på modkontoen.

### <a name="scenario-4"></a>Scenario 4

Brug de samme økonomiske standarddimensionsværdier, som du har defineret for kladdenavnet og debitoren i eksempel 1 og 2. Definer derefter en fast dimensionsværdi for **BUSINESSUNIT**-dimensionen på hovedkontoen 170150. Gå til **Finans \> Kontoplan \> Konti \> Hovedkonti**. Vælg **170150** i feltet **Hovedkonto**, og vælg derefter **Tilføj** under fanen **Tilsidesættelse af juridisk enhed**. Vælg **USMF** som juridisk enhed, og vælg derefter **Tilføj**. Vælg den pågældende post, og vælg derefter **Standarddimensioner**. Skift **BUSINESSUNIT**-dimensionen til **Fast værdi**, og angiv **003** som værdi.

Opret en ny finanskladde, der bruger kladdenavnet **GenJrn**. Fjern alle standarddimensionsværdier under fanen **Økonomiske dimensioner**.

Gå til **Linjer**. Vælg **Finans** i feltet **Kontotype**, og skriv derefter **170150** i feltet **Kontotype**. Vælg derefter tasten **Tab** for at flytte ud af feltet. Dimensionsværdierne fra kontoen angives som standard fra hovedkontoens opsætning for konto 170150. **Kontoværdien** vises derfor som **170150-003**.

Skift **Konto**-værdi til **170150-004**. **Kladdefunktionen forhindrer ikke, at en fast dimensionsværdi ændres.** Angiv enten et debet- eller kreditbeløb. Vælg **Finans** i feltet **Modkontotype**, og skriv derefter **170250** i feltet **Modkontotype**. Den økonomiske dimensionsværdi 004 angives som standard fra kontoen. Bogfør derefter dokumentet. Vælg i kladden **Bilagskladde**. Bemærk, at **BUSINESSUNIT**-værdien er vendt tilbage til den faste dimensionsværdi **003** under bogføringen.

Når du vender tilbage til bilaget i kladden, afspejler **BUSINESSUNIT**-dimensionen **ikke** den faste dimensionsværdi. Den har altid den værdi, der blev vist på skærmen, før den bogføres. Bogføringsprocessen ændrer ikke noget, der er angivet på bilaget. Det er kun regnskabsposten, der ændres under bogføringen.

## <a name="developer-notes"></a>Udviklernotater

Hvis du er udvikler og vil se på koden for standardprocessen, skal du gennemgå følgende metoder:

- **LedgerJournalEngine.accountModified()** – Denne metode er hovedpunktet for standardprocessen for den primære kontodimension, som er standard for alle kladder (og tilsidesættes af nogle kladdetyper).
- **LedgerJournalEngine.offsetAccountModified()** – Denne metode er hovedpunktet for standardprocessen for modkontodimensioner.
