---
title: Importere ISO20022-filer
description: I dette emne beskrives, hvordan du importerer betalingsfiler med ISO 20022 camt.054- og pain.002-format i Microsoft Dynamics 365 Finance.
author: neserovleo
manager: AnnBe
ms.date: 07/27/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, CustBankAccounts, VendPaymMode, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Italy, Latvia, Lithuania, Norway, Poland, Spain, Sweden, Switzerland, United Kingdom
ms.author: v-lenest
ms.search.validFrom: 2017-06-01
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 48738f6af67bf40cac084d65aa4ff01935259c85
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209920"
---
# <a name="import-iso20022-files"></a>Importere ISO20022-filer

[!include [banner](../includes/banner.md)]

Du kan importere betalingsfiler, som har følgende formater:

 - **ISO20022 camt.054 kreditadvis** – Importere indgående betalinger fra en fil i dette format i debitorbetalingskladden.
 - **ISO20022 pain.002 returneringsstatus** og **ISO20022 camt.054 debetadvis** – Importere returfiler i disse formater i overførselskladden for kreditorbetaling.

## <a name="prerequisites-for-importing-the-camt054-credit-advice-file"></a>Forudsætninger for at importere filen camt.054 kreditadvis
Følgende forudsætninger skal være opfyldt, for at du kan importere meddelelser fra banken i formatet camt.054.001.002 i debitorbetalingskladden.

1. Importer **ISO20022 camt.054** med den elektroniske rapporteringskonfiguration (ER) fra Microsoft Dynamics Lifecycle Services (LCS). Vælg derefter denne konfiguration på siden **Debitorbetalingsmetode** i feltet **Importér formatkonfiguration**. Du kan finde flere oplysninger under [Filformater for betalingsmåder](emea-select-file-formats-for-the-method-of-payments.md).
2. På siden **Alle debitorer** skal du angive et navn og et organisationsnummer for hver debitor.
3. På siden **Debitors bankkonto** skal du oprette en debitorbankkontopost ved at angive følgende oplysninger: IBAN eller bankkontonummer, og SWIFT-kode eller registreringsnummer.
4. På siden **Bankkonti** skal du oprette bankkonti for juridiske enheder ved at angive følgende oplysninger: IBAN eller bankkontonummer, SWIFT-kode eller registreringsnummer, valuta og adresse.

   > [!NOTE]
   > Hvis du planlægger at bruge avanceret bankafstemning, skal du på i oversigtspanelet **Afstemning** indstille **Avanceret bankafstemning** til **Ja**. Hvis du planlægger at afstemme en ikke-bogførte importerede betalinger, kan du indstille **Brug bankkontoudtog som bekræftelse på elektroniske betalinger** til **Ja**.

5. Valgfrit: På siden **Tilknytning af transaktionskode** skal du oprette en tilknytning mellem bankposteringskoder i filen og bankposteringstyperne.
6. Hvis filen indeholder posteringsgebyrer, der skal bogføres sammen med den indgående betaling, kan du oprette et betalingsgebyr på siden **Debitorbetalingsgebyr**. Tilknyt derefter på siden **Betalingsmåder** betalingsgebyret med bankkontoen i opsætningen af betalingsgebyret.
7. Hvis ESR-betalinger skal importeres og indeholder ISR-referencer (gælder for juridiske enheder i Schweiz), skal du angive indstillinger for følgende opsætning:

    - I feltet **Debitorbetalinger, kontolængde** skal du angive længden på den debitorkode, der bruges i ISR-referencer eller til automatisk identifikation af kunden.
    - Sørg for, at kundenummer og fakturanummeret (nummerserier) kun indeholder cifre. De må ikke indeholde nogen andre tegn. Fakturanummeret må ikke have foranstillede nuller.
    - Angiv ESR, BESR og registreringsnumre for den juridiske enheds bankkonto. Yderligere oplysninger finder du i [import af kundebetalinger i ESR](emea-che-esr-customer-payments-import.md), fordi der kræves lignende indstillinger.
    
## <a name="import-the-camt054-credit-advice-file-into-the-customer-payment-journal"></a>Importere filen camt.054 kreditadvis til debitorbetalingskladden
1. På siden **Kladdelinjer for debitorindbetalinger** skal du klikke på **Funktioner** > **Importer betalinger**.
2. Vælg den betalingsmåde, der har de nødvendige indstillinger for formatet ISO20022 camt.054.
3. Angiv de krævede parametre og filstien, og klik derefter på **OK**. Filen importeres.

## <a name="prerequisites-for-importing-files-in-the-pain002-status-return-and-camt054-debit-advice-formats-into-the-ap-payment-transfer-journal"></a>Forudsætninger for at importere filer i pain.002 returneringsstatus- og camt.054 debetadvis-format i overførselskladden for kreditorbetaling.
Følgende forudsætninger skal være opfyldt, for at du kan importere bankmeddelelser i følgende ISO20022 formater til siden **Overførsel af kreditorbetaling**: pain.002.001.003 returneringsstatusmeddelelser og camt.054.001.002 debetadvis.

1. Import af **ISO20022 camt.054** og **ISO20022 pain.002** ER-konfigurationer fra LCS.
2. På siden **Kreditors betalingsmetode** i felterne **Konfiguration af returformat** og **Sekundær konfiguration af returformat** skal du vælge de ER-konfigurationer, du har importeret. Du vil skulle aktivere det generiske elektroniske returneringsformat for den valgte betalingsmåde.
3. På siden **Tilknytning af returformatstatus** skal du konfigurer tilknytningen af statuskoder mellem statusser for pain.002 og Kreditorbetalingskladde.

    Her er et eksempel på et statusopsætning.

    Returstatus | Betalingsstatus
    --------------|---------------
    RJCT          | Afvist
    ACCP          | Accepteret
    ACSP          | Modtaget

4. På siden **Fejlkoder for returformat** skal du angive pain.002 fejlkoder og beskrivelser i overensstemmelse med eksterne ISO20022-statusårsagskoder.

    Her er et eksempel på en del af opsætningen af en fejlkode.

    Kode | Navn
    -----|-----
    AC01 | IncorrectAccountNumber
    AC02 | InvalidDebtorAccountNumber
    AC03 | InvalidCreditorAccountNumber
    AC04 | ClosedAccountNumber
    AC05 | ClosedDebtorAccountNumber
    AC06 | BlockedAccount

5. Hvis camt.054-filen indeholder posteringsgebyrer, der skal bogføres sammen med den indgående betaling, kan du oprette et betalingsgebyr på siden **Kreditorbetalingsgebyr**. Tilknyt derefter på siden **Betalingsmåder** betalingsgebyret med bankkontoen i opsætningen af betalingsgebyret.

## <a name="import-the-pain002-status-return-or-camt054-debit-advice-files-into-the-vendor-payment-journal"></a>Importere pain.002 returneringsstatus- eller camt.054 debetadvis-filer til kreditorbetalingskladden
1. Åbn siden **Betalingsoverførsler** i menuen i Kreditor.
2. På siden **Betalingsoverførsler** skal du klikke på **Returfil - kreditor**.
3. Vælg den betalingsmåde, der har de nødvendige indstillinger for ISO20022-filer, og klik derefter på **OK**.
4. Vælg det filformat, du vil importere, og klik derefter på **OK**.
5. Angiv de krævede parametre og filstien, og klik derefter på **OK**.

Hvis du importerer filen pain.002, opdateres status for kreditorbetalingslinjer baseret på oplysningerne i den importerede fil.

Hvis du importerer filen camt.054, skal du angive følgende yderligere parametre:

- **Gebyr-ID** – Angiv det gebyr-ID, der definerer nye betalingsgebyrlinjer, som oprettes på kreditorbetalingskladdelinjen, hvis der findes et gebyrbeløb i filen camt.054.
- **Nyt kladdenavn** og **Beskrivelse af ny kladde** – Angiv navnet og beskrivelsen af kladden, som behandlede transaktioner skal overføres til. Efter overførslen skal nye bilagsnumre tildeles i den nye kladde.
- **Importér Direct Debit-transaktioner** – Vælg **Ja** for denne indstilling, hvis udgående direkte debiteringer skal importeres til kreditorbetalingskladden.
- **Kladdenavn** – Definer et nyt kladdenavn for de importerede direct debit-transaktioner.
- **Udlign posteringer** – Vælg **Ja** for denne indstilling, hvis importerede kreditorbetalinger skal udlignes med fakturaer, der findes i systemet.

Du kan få vist de importerede oplysninger på siden **Betalingsoverførsler**. 

## <a name="additional-details"></a>Flere oplysninger

Når du importerer en formatkonfiguration fra LCS, kan du importere hele konfigurationstræet, hvilket betyder, at Model- og Model tilknytning-konfigurationerne er medtaget. I Betalingsmodel fra og med version 8 findes tilknytningerne i separate ER-konfigurationer i løsningstræet (Betalingsmodel-tilknytning 1611, Betalingsmodel-tilknytning til destination ISO20022 osv). Der er mange forskellige betalingsformater i én model (Betalingsmodel), og derfor er separat tilknytningshåndtering nøglen til nem løsningsvedligeholdelse. Overvej f.eks. følgende scenarie: Du bruger ISO20022 betalinger til at generere kreditoverførselsfiler og derefter importerer du returmeldingerne fra banken. I denne situation skal du bruge følgende konfigurationer:

 - **Betalingsmodel**
 - **Betalingsmodel-tilknytning 1611** – denne tilknytning bruges til at generere eksportfilen.
 - **Betalingsmodel-tilknytning til destination ISO20022** – denne konfiguration omfatter alle de tilknytninger, der skal bruges til at importere dataene ("til destination"-tilknytningsretning)
 - **ISO20022 kreditoverførsel** – denne konfiguration omfatter en format-komponent, der er ansvarlig for at eksportere filoprettelse (pain.001) baseret på betalingsmodel-tilknytning 1611, samt et format til modeltilknytningskomponenten, der skal bruges sammen med betalingsmodel-tilknytning til destination ISO20022 til at registrere eksporterede betalinger i systemet med henblik på yderligere import (importere i den tekniske CustVendProcessedPayments-tabel)
 - **ISO20022 pengeoverførsel (CE)**, hvor CE svarer til landeangivelsen – afledte format til ISO20022 pengeoverførsel med samme struktur og visse landespecifikke forskelle
 - **Pain.002** – dette format skal bruges sammen med betalingsmodel-tilknytningen til destination ISO20022 for at importere filen pain.002 til overførselskladder for kreditorbetaling
 - **Camt.054** – dette format skal bruges sammen med betalingsmodel-tilknytningen til destination ISO20022 for at importere filen camt.054 til overførselskladder for kreditorbetaling. Der skal bruges samme formatkonfigurationen i funktionen til import af debitorbetalinger, men den anden tilknytning skal bruges i betalingsmodel-tilknytningen til destinationen ISO20022-konfiguration.

Yderligere oplysninger om elektronisk indberetning kan du finde i [Oversigt over elektronisk rapportering](../../dev-itpro/analytics/general-electronic-reporting.md).

## <a name="additional-resources"></a>Yderligere ressourcer
- [Oprette og eksportere kreditorbetalinger ved hjælp af ISO20022-betalingsformat](./tasks/create-export-vendor-payments-iso20022-payment-format.md)
- [Importere konfiguration for ISO20022-kreditoverførsel](./tasks/import-iso20022-credit-transfer-configuration.md)
- [Importere ISO20022 Direct Debit-konfiguration](./tasks/import-iso20022-direct-debit-configuration.md)
- [Konfigurere firmas bankkonti for ISO20022-kreditoverførsler](./tasks/set-up-company-bank-accounts-iso20022-credit-transfers.md)
- [Konfigurere firmas bankkonti for direkte ISO20022-debiteringer](./tasks/set-up-company-bank-accounts-iso20022-direct-debits.md)
- [Konfigurere debitorer og debitorbankkonti for direkte ISO20022-debiteringer](./tasks/set-up-bank-accounts-iso20022-direct-debits.md)
- [Konfigurere en betalingsmetode for ISO20022-kreditoverførsler](./tasks/set-up-method-payment-iso20022-credit-transfer.md)
- [Opret betalingsmåde til ISO20022 direkte debet](./tasks/setup-method-payment-iso20022-direct-debit.md)
- [Konfigurere kreditorer og kreditorbankkonti for ISO20022-kreditoverførsler](./tasks/set-up-vendor-iso20022-credit-transfers.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]