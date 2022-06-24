---
title: Anbefalet praksis for bogføringsprofiler
description: Denne artikel beskriver de anbefalede fremgangsmåder til konfiguration af posteringsprofiler.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, MainAccount, SysDatabaseLogSetup, CustGroup, VendGroup, InventItemGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb0e321f447b78b88c065e52bb7fad1c445e47b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849896"
---
# <a name="recommended-practices-for-posting-profiles"></a>Anbefalet praksis for posteringsprofiler

Der findes en række anbefalede fremgangsmåder, som du bør følge, når du konfigurerer posteringsprofiler i hele systemet. Denne artikel beskriver forskellige scenarier og de tilsvarende anbefalede fremgangsmåder.

## <a name="setting-the-do-not-allow-manual-entry-flag"></a>Angive flaget Tillad ikke manuel indtastning

På siden **Hovedkonti** skal du markere afkrydsningsfeltet **Tillad ikke manuel indtastning** for en hovedkonto, der bruges til en posteringsprofil. Denne indstilling forhindrer brugere i manuelt at bogføre en kladdepost på hovedkontoen. Den hjælper derfor med at sikre, at reskontroen forbliver i balance med finansmodulet, og hjælper med at gøre afstemningsprocessen lettere.

Hvis der kræves reguleringer på en konto, der styres af systemet og bogføres automatisk, kan du bruge en af disse metoder:

- Opret en sekundær hovedkonto, hvor reguleringerne kan bogføres. Brug derefter en totalkonto eller en særlig række i dine regnskabsrapporter til at gruppere og opsummere konti.
- Tilbageføre de oprindelige transaktioner i den relevante reskontro, foretage eventuelle nødvendige rettelser, og bogfør derefter transaktionen igen via den samme reskontro.

## <a name="changing-posting-profiles-after-transactions-exist"></a>Ændre posteringsprofiler, når der findes transaktioner

Hvis du ændrer en posteringsprofil, efter at der findes transaktioner, kan afstemningen mislykkes, og saldoen for reskontroen og finansmodulet kan komme ud af balance. Generelt anbefales det, at du **ikke** ændrer posteringsprofilen, når transaktionerne findes.

Hvis ændringer er nødvendige, skal du bruge følgende retningslinjer for at hjælpe med at sikre systemets integritet:

- Foretag ændringerne under en lukningsperiode.
- Foretag ændringerne, når der ikke forekommer andre transaktioner i systemet.
- Valider finansmodulet, og afstem det med reskontroen før og efter ændringerne.
- Bogførte transaktioner opdateres ikke, hvis du ændrer posteringsprofilen. Overvej nøje, om der kræves reguleringsposter for dine ændringer.
- Hvis du ændrer lagerposteringsprofilerne, skal du overveje, hvordan ændringerne påvirker den lagerbeholdning og de finanssaldi, du har. Nogle ændringer kan kræve, at du sætter lageret til 0 (nul), lukker lageret og derefter henter lageret tilbage, når ændringerne er foretaget.
- Test altid ændringerne i et ikke-produktionsmiljø, før du foretager dem i produktionen.

## <a name="using-database-logging-to-audit-changes-to-posting-profiles"></a>Bruge databaselog til at overvåge ændringer i posteringsprofiler

Overvej at konfigurere databaselog for hver posteringsprofil og de parametertabeller, der styrer bogføringen. Hvis en parameter eller profil ændres, vil du derefter have en komplet revisionspost over, hvilken værdi der er ændret, hvem der har ændret den, hvornår den er ændret, og hvad den foregående værdi var. Disse oplysninger kan være kritiske i løbet af afstemningsprocessen, og revisoren kan få brug for den understøttende dokumentation.

Du kan finde flere oplysninger under [Konfigurere databaselogning](../../fin-ops-core/dev-itpro/sysadmin/configure-manage-database-log.md).

Du kan bruge følgende tabel som reference for almindelige tabelnavne, der er relateret til posteringsprofiler og relaterede posteringsparametre.

| Sidens navn | Navigationssti | Tabel-label |
|-----------|-----------------|------------|
| Kreditorparametre | Kreditor &gt; Opsætning &gt; Kreditorparametre | VendParm |
| Kreditorbogføringsprofil | Kreditor &gt; Opsætning &gt; Kreditorposteringsprofil | VendPosting |
| Gebyrkode | Kreditor &gt; Konfiguration af gebyrer &gt; Gebyrkode eller Debitor &gt; Konfiguration af gebyrer &gt; Gebyrkode | MarkupTable |
| Betalingsmåder | Kreditor &gt; Opsætning af betaling &gt; Betalingsmåder | VendPaymMode |
| Kasserabatter | Kreditor &gt; Betalingsopsætning &gt; Kasserabatter eller Debitor &gt; Betalingsopsætning &gt; Kasserabatter | CashDisc |
| Betalingsgebyr (kreditor) | Kreditor &gt; Betalingsopsætning &gt; Betalingsgebyr | VendPaymFee |
| Debitorparametre | Debitor &gt; Opsætning &gt; Debitorparametre | CustParm |
| Debitor, posteringsprofiler | Debitor &gt; Opsætning &gt; Debitorposteringsprofil | CustPosting |
| Betalingsmåder | Debitor &gt; Betalingsopsætning &gt; Betalingsmetoder | CustPaymMode |
| Betalingsgebyr (debitor) | Debitor &gt; Betalingsopsætning &gt; Betalingsmåder | CustPaymFee |
| Parametre for aktivleasing | Aktivleasing &gt; Opsætning &gt; Parametre til aktivleasing | AssetLeasePostingAccounts<br>AssetLeaseJournalParameters<br>AssetLeaseExecutoryCostPostingAccounts |
| Bankkonti | Kontant- og bankstyring &gt; Bankkonti &gt; Bankkonti | BankAccountsTable |
| Bankposteringstyper | Kontant- og bankstyring &gt; Opsætning &gt; Bankposteringstyper | BankTransType |
| Elimineringsregler | Konsolideringer &gt; Opsætning &gt; Elimineringsregel | LedgerEliminationRule<br>LedgerEliminationRuleLines |
| Udgiftskategorier | Udgiftsstyring &gt; Opsætning &gt; Generelt &gt; Udgiftskategorier | ProjCategories |
| Anlægsaktivernes parametre | Anlægsaktiver &gt; Opsætning &gt; Anlægsaktivparametre | AssetParameters |
| Posteringsprofiler for anlægsaktiver | Anlægsaktiver &gt; Opsætning &gt; Posteringsprofiler for anlægsaktiver | AssetLedgerAccounts<br>AssetDisposalParameters |
| Værdireguleringskonti for valuta | Finans &gt; Valutaer &gt; Værdireguleringskonti for valuta | CurrencyLedgerGainLossAccount |
| Konti til automatisk posteringer | Finans &gt; Opsætning af bogføring &gt; Konti til automatiske posteringer | LedgerSystemAccounts |
| Mellemregning | Finans &gt; Opsætning af bogføring &gt; Mellemkonti | LedgerIntercompany |
| Definitioner af posteringsbogføring | Finans &gt; Opsætning af bogføring &gt; Definitioner af posteringsbogføring | JournalizingDefinitionTrans |
| Bogføringsdefinitioner | Finans &gt; Opsætning af bogføring &gt; Bogføringsdefinitioner | JournalizingDefintion |
| Bogføring (lager) | Lagerstyring &gt; Konfiguration &gt; Bogføring &gt; Bogføring | InventPosting |
| Omkostningstypekoder | Landingsomkostninger &gt; Opsætning af efterkalkulation &gt; Omkostningstypekoder | ITMCostTypeTable |
| Ressourcer | Produktionsstyring &gt; Opsætning &gt; Ressourcer &gt; Ressourcer | WrkCtrTable |
| Ressourcegrupper | Produktionsstyring &gt; Opsætning &gt; Ressourcer &gt; Ressourcegrupper | WrkCtrResourceGroup |
| Produktionsgrupper | Produktionsstyring &gt; Opsætning &gt; Produktion &gt; Produktionsgruppe | ProdGroup |
| Omkostningskategorier | Produktionsstyring &gt; Konfiguration &gt; Ruter &gt; Omkostningskategorier | ProjCategory |
| Projektgrupper | Projektstyring og regnskab &gt; Opsætning &gt; Bogføring &gt; Projektgrupper | ProjGroup |
| Opsætning af finanskontering (projekter) | Projektstyring og regnskab &gt; Opsætning &gt; Bogføring &gt; Opsætning af finanskontering | ProjPosting |
| Standardmodkonti for udgifter | Projektstyring og regnskab &gt; Konfiguration &gt; Bogføring &gt; Standardmodkonti for udgifter | ProjDefaultOffsetSetup |
| Posteringsprofiler for rabatstyring | Rabatstyring &gt; Opsætning af bogføring af rabatstyring &gt; Posteringsprofiler til rabatstyring | TAMRebatePosting |
| Finanskonteringsgruppe (moms) | Moms &gt; Opsætning &gt; Moms &gt; Finanskonteringsgruppe | TaxAccountGroup |

## <a name="changing-groups-after-transactions-exist"></a>Ændre grupper, når der findes transaktioner

Vær forsigtig, når du ændrer grupper i masterdata. Hvis du bruger grupper til at definere posteringsprofiler, kan enhver ændring af en gruppe i en masterpost have en negativ indflydelse på muligheden for at afstemme Finans med reskontroen. Du kan f.eks. konfigurere lagerkonteringsprofilen for salgsordreomsætning, så der bruges en anden omsætningskonto til hver varegruppe. Hvis du ændrer den varegruppe, der er knyttet til en vare, når der findes transaktioner, bogføres omsætningen for de nye posteringer på den opdaterede konto. Den omsætning, der blev bogført før ændringen, vil dog forblive på den oprindelige konto.

## <a name="testing-posting-profiles"></a>Test af posteringsprofiler

Før du går live, og når du har foretaget ændringer eller tilføjelser til posteringsprofilerne eller de relaterede parametre, skal du teste hvert scenario. Du skal som minimum teste hver enkelt bogføringstype for at validere, at bogføringen fungerer korrekt. Den anbefalede fremgangsmåde er dog at teste hver enkelt posteringsprofiltransaktion og -kombination.

Du har f.eks. to debitorposteringsprofiler, som hver har tre poster, der er specifikke for debitorgrupper. I dette tilfælde skal du teste hver enkelt transaktionstype.

**Posteringsprofiler:**

- **GEN** – Den generelle posteringsprofil, der har én gruppe for medarbejdere, en for debitorer og én for intern handel. Hver gruppe peger på en anden debitorhandelskonto.
- **PRE** – Posteringsprofilen for forudbetaling, der har én post for alle forudbetalinger, der peger på debitorforudbetalingskontiene.

### <a name="testing-scenarios"></a>Testscenarier

- Fritekstfaktura for en debitor i gruppen **Medarbejder**, der bruger posteringsprofilen **GEN**
- Fritekstfaktura for en debitor i gruppen **Medarbejder**, der bruger posteringsprofilen **PRE**
- Salgsordrefaktura for en debitor i gruppen **Medarbejder**, der bruger posteringsprofilen **GEN**
- Salgsordrefaktura for en debitor i gruppen **Medarbejder**, der bruger posteringsprofilen **PRE**
- Debitorbetalingskladde for en debitor i gruppen **Medarbejder**, der bruger posteringsprofilen **GEN**
- Debitorbetalingskladde for en debitor i gruppen **Medarbejder**, der bruger posteringsprofilen **PRE**

Gentag et testscenario med det foregående eksempel for hver debitorgruppe, og gentag hver gruppe af testscenarier for hver ekstra transaktionstype (f.eks. projektfakturaer og servicestyring).

## <a name="reconciling-the-ledger-to-the-subledger"></a>Afstemning af finans med reskontro

Finans skal afstemmes med reskontroen i hver periode. Mange moduler indeholder standardrapporter, der kan bruges til at udføre denne afstemning. Afhængigt af dine lokale krav kan du dog være nødt til at udvikle brugerdefinerede rapporter eller udvide de eksisterende rapporter, så de opfylder kravene til rapportering.

Det anbefales, at du foretager en simuleret lukning af en periode og afstemmer hver enkelt af dine reskontroposter med finans, før du går live. Det anbefales også, at du laver en afsluttende test af alle åbne saldi og åbne transaktioner, før du går live første gang. Som en del af denne proces skal du køre en komplet afstemning for at sikre, at overflytningen af saldi og åbne transaktioner er i balance med de tidligere systemer, og at alle reskontroer stemmer med finansmodulet, før der oprettes nye transaktioner.
