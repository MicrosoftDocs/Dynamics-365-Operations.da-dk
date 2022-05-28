---
title: Bogføring af salgsordre
description: Dette emne indeholder oplysninger om fanen Salgsordre på siden til lagerbogføringsprofilen.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 5d84723b51d6977867fa162c4a47befa61bd9ef6
ms.sourcegitcommit: dc3053625dfe24aef64399dd1d002214e7f7619f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/13/2022
ms.locfileid: "8755922"
---
# <a name="sales-order-posting"></a>Bogføring af salgsordre

Fanen **Salgsordre på** siden **Lagerposteringsprofiler** bruges til at styre, hvordan salgsordrer bogføres i finansmodulet. To hovedaktiviteter bogføres i finansmodulet for en salgsordre: 

- Følgeseddel
- Faktura

Hvis en fysisk transaktion (følgeseddel) skal bogføres i finansmodulet for en salgsordre, skal følgende betingelser være opfyldt:

- På siden **Parametre til lager- og lokationsstyring** skal afkrydsningsfeltet **Bogfør følgeseddel i finans** være markeret.
- På siden **Varemodelgruppe** skal afkrydsningsfeltet **Bogfør fysisk lager i finans** være markeret for den vare, der er valgt på salgsordrelinjen.
- På siden **Lagerposteringsprofil** skal der angives hovedkonti for følgende posteringstyper:
  - Omkostninger ved leverede enheder
  - Vareforbrug for leverede varer

Hvis en økonomisk transaktion (faktira) skal bogføres i finansmodulet for en salgsordre, skal følgende betingelser være opfyldt:

- På siden **Varemodelgruppe** skal afkrydsningsfeltet **Bogfør økonomisk lager i finans** være markeret for den vare, der er valgt på salgsordrelinjen.
- På siden **Lagerposteringsprofil** skal der være angivet hovedkonti for følgende posteringstyper:
  - Omkostninger ved fakturerede enheder
  - Vareforbrug for fakturerede varer
  - Indtægter
  - Rabat\*

> [!NOTE]
> Rabatkontoen er valgfri. Mange regnskabsregler, f.eks. GAAP og IFRS, kræver, at rabatter reducerer salgsindtægten, og derfor bruges disse konti ikke i mange situationer. Hvis lokale regler tillader det, skal du bruge en separat hovedkonto til at bogføre den del af salgsprisen, der er fratrukket rabat.

Hvis du vil bogføre den udskudte (estimerede) omsætningsværdi i finansmodulet, når du genererer en følgeseddel til en salgsordre, skal følgende betingelser være opfyldt:

- På siden **Varemodelgruppe** skal afkrydsningsfeltet **Bogfør fysisk lager i finans** være markeret for den vare, der er valgt på salgsordrelinjen.
- På siden **Varemodelgruppe** skal afkrydsningsfeltet **Bogfør til udskudt omsætningskonto på salgslevering** være markeret.
- På siden **Parametre til lager- og lokationsstyring** skal afkrydsningsfeltet **Bogfør følgeseddel i finans** være markeret.
- På siden **Parametre til lager- og lokationsstyring** skal afkrydsningsfeltet **Bogfør fysisk moms** være markeret.
- På siden **Debitorparametre** skal afkrydsningsfeltet **Bogfør følgeseddel i finans** være markeret.
- På siden **Lagerposteringsprofil** skal der angives hovedkonti for følgende posteringstyper:
  - Udskudt indtægt ved levering
  - Modkonto til udskudt indtægt ved levering
  - Udskudt moms ved levering

> [!NOTE]
> Det anbefales generelt, at du aktiverer indstillingerne **Bogfør fysisk lager** og **Bogfør følgeseddel i Finans**. Aktivering af disse indstillinger kan hjælpe med at sætte fart i lukningsprocedurerne ved månedsafslutning, da det ikke er nødvendigt at beregne og bogføre dem manuelt. Derudover afspejler regnskaber automatisk de udskudte beløb uden manuel indgriben.

> [!IMPORTANT]
> Indstillingen **Bogfør på udskudt omsætningskonto ved salgslevering** bruges ikke med indtægtsføring. Du kan finde flere oplysninger om indtægtsføring under [Oversigt over indtægtsføring](/accounts-receivable/revenue-recognition-overview.md)

## <a name="sample-posting-profile-configuration"></a>Eksempel på konfiguration af posteringsprofil 

I følgende tabel vises eksempler på standardbogføringstyper med eksempler på hovedkonti og beskrivelser:
 
- I kolonnen **Clearingkonto** angives, at bogføringstypen er en clearingkonto. Det beløb, der bogføres på denne konto, tilbageføres automatisk, når en senere transaktion bogføres. 
- I **P/F**-kolonnen angives **P** til fysisk bogføring og **F** til økonomisk bogføring. 
- I kolonnen **Følg** angives, om hovedkontoen for en bestemt bogføringstype typisk er den samme som en anden bogføringstype. Værdien i kolonnen angiver den bogføringstype, der typisk anvendes.

> [!NOTE]
> Disse hovedkonti og hovedkontonavne er kun forslag. Det anbefales, at du arbejder sammen med bogholderen for at finde den bedste konfiguration til virksomhedens behov.


| Bogføringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | P/F | Følg | Beskrivende tekst |
|------------|------------------------|-------------------------|--------------|---------|-------------------|------------|------|-------------------------|
| Omkostninger ved leverede enheder | 140100</br>140101 | Materialelager</br>Materialer, der er afsendt, ikke faktureret | Aktiv | Kredit | Ja | P | Omkostninger ved fakturerede enheder | Bruges, når følgesedlen for en salgsordre bogføres. Modkontoen er det leverede vareforbrug. Beløbet på denne konto tilbageføres, når der bogføres en salgsordrefaktura. Du kan bruge en konto til materialer, der er afsendt, ikke faktureret til at repræsentere det fysiske lager og reservere kontoen Materialelager til den økonomiske opdatering. |
| Vareforbrug for leverede varer | 500150 | Udskudt vareforbrug | Udgift | Debet | Ja | P  | Bruges, når følgesedlen for en salgsordre bogføres. Modkontoen er omkostninger ved leverede enheder. Beløbet på denne konto tilbageføres, når der bogføres en salgsordrefaktura. |
| Omkostninger ved fakturerede enheder | 140100 | Materialelager | Aktiv | Kredit | Nej | F | Omkostninger ved leverede enheder | Bruges, når fakturaen for en salgsordre bogføres. Denne modkonto er det fakturerede vareforbrug. Denne konto repræsenterer lageret i balancen. |
| Vareforbrug for fakturerede varer | 500100 | Materialer til vareforbrug | Udgift | Debet | Nej | F  | Bruges, når fakturaen for en salgsordre bogføres. Denne modkonto er omkostninger ved fakturerede enheder. Denne konto repræsenterer vareforbrug i din P&amp;L-opgørelse. |
| Indtægt (indtægt fra salgsordre*) | 400100 | Indtægtsmaterialer | Indtægter | Kredit | Nej | F   | Bruges, når fakturaen for en salgsordre bogføres. Modkontoen til denne konto er samlekontoen (Debitorsaldo*) i **debitorposteringsprofilen**. |
| Provision (Ordre, provision*) | 602150 | Provisionsudgift | Udgift | Debet | Nej | F  | Bruges, når provision er aktiveret og beregnet for salg og bogført under salgsordrefakturaprocessen. Modkontoen til denne konto er til skyldig provision. |
| Provisionsmodkonto (Ordre, provisionsmodkonto*) | 201110 | Skyldige provisioner | Passiv | Kredit | Ja | F | Bruges, når provision er aktiveret og beregnet for salg og bogført under salgsordrefakturaprocessen. Modkontoen til denne konto er til provisionsudgifter. |
| Udskudt indtægt ved levering (Ordre - følgeseddelsomsætning*) | 401400 | Periodiseret salg | Indtægter | Kredit | Ja | P  | Bruges, når Udskudt omsætning til levering er aktiveret og bogført, når du behandler en følgeseddel til en salgsordre. Modkontoen er udskudt omsætningskonto. Beløbene på denne konto tilbageføres automatisk, når du bogfører salgsordrefakturaen. |
| Modkonto til udskudt indtægt ved levering (Ordre - modkonto for følgeseddelsomsætning)* | 130400 | Debitor – ikke faktureret | Aktiv | Debet | Ja | P  | Bruges, når Udskudt omsætning til levering er aktiveret og bogføres, når du behandler en følgeseddel til en salgsordre. Modkontoen er Udskudt indtægt ved levering. Beløbene på denne konto tilbageføres automatisk, når du bogfører salgsordrefakturaen. |
| Udskudt moms ved levering (Salg, følgeseddelsmoms*) | 250500 | Udskudt moms | Passiv | Kredit | Ja | P  | Bruges, når Udskudt indtægt ved levering er aktiveret, og indstillingen Bogfør fysisk moms er aktiveret. Momsbeløbet bogføres, når du behandler en salgsordres følgeseddel. |

\*Værdier, der står i parentes i denne tabel, repræsenterer den værdi, der bruges i feltet **Bogføringstype** på siden **Poster på bilag**. Du kan se **Bogføringstype** på siden **Poster på bilag** under fanen **Generelt**.

## <a name="sales-category-posting"></a>Bogføring af salgskategori

Som et alternativ til at konfigurere lagerbogføring for alle varer, en gruppe varer eller en enkelt vare kan du oprette kategorier og styre finansbogføringen efter salgskategorier. Du kan få flere oplysninger om, hvordan du konfigurerer et kategorihierarki og tildeler kategorier til produkter, ved at gå til [Oprette et hierarki for produktklassifikation](/supply-chain/pim/tasks/create-hierarchy-product-classification.md) og [Klassificere et produkt ved hjælp af kategorihierarkier](/supply-chain/pim/tasks/classify-product-category-hierarchies.md).

Når du har oprettet et kategorihierarki, skal du tildele hierarkiet til en eller flere typer. Hvis du vil bruge et kategorihierarki i salgsordrer, skal du tildele kategorien til hierarkitypen Salgskategori. Du kan finde flere oplysninger under [Om kategorihierarkityper](/dynamicsax-2012/appuser-itpro/about-category-hierarchies.md).

## <a name="create-revenue-posting-by-sales-category"></a>Oprette indtægtsføring efter salgskategori

Hvis du vil tildele finanskonteringer for en salgsordre baseret på en salgskategori, skal du benytte følgende fremgangsmåde:

1. Gå til **Lagerstyring** > **Konfiguration** > **Bogføring** > **Bogføring**.
2. Vælg fanen **Salg**.
3. Vælg alternativknappen til den bogføringstype, du vil konfigurere (f.eks. **Indtægter**).
4. Vælg **Ny**.
5. Vælg **Kategori** i feltet **Varekode**.
6. Vælg kategorien til posteringsprofilen i feltet **Kategorirelation**.
7. Vælg en indstilling for **Tabel**, **Gruppe** eller **Alle** i feltet **Kontokode**. Hvis du f.eks. vil anvende posteringsprofilen på alle debitorer, skal du vælge **Alle**.
   - Hvis du valgte **Tabel** i trin 6, skal du vælge det specifikke **Kreditornummer** for posteringsprofilen i feltet **Kontorelation**.
   - Hvis du valgte **Gruppe** i trin 6, skal du vælge **Kreditorgruppe** for posteringsprofilen i feltet **Kontorelation**.
   - Hvis du valgte **Alle** i trin 6, vil feltet **Kontorelation** være tomt.

8. Hvis du vil tilknytte en bestemt momsgruppe, der har den valgte bogføringstype, skal du vælge **Momsgruppe**. Hvis der ikke angives noget i feltet, gælder bogføringstypen for alle eksisterende momsgrupper. Bogføring, der angives for momsgrupper, gælder kun for transaktioner, der foretages ved salg og indkøb.

9. Vælg det kontonummer, som kontotypen skal bogføres til, i feltet **Hovedkonto**. Vælg et af de eksisterende kontonumre i kontoplanen.
