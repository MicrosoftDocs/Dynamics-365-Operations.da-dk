<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="emea-ISO20022-file-formats.md" target-language="da-DK">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>emea-ISO20022-file-formats.35e138.d91e937c62d4d498e67d753e39676514835f4161.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>d91e937c62d4d498e67d753e39676514835f4161</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\financials\localizations\emea-ISO20022-file-formats.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>ISO20022 files import</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Import af ISO20022-filer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to import payment files of the ISO 20022 camt.054 and pain.002 formats into Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I dette emne beskrives, hvordan du importerer betalingsfiler med ISO 20022 camt.054- og pain.002-format i Microsoft Dynamics 365 for Finance and Operations.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Import ISO20022 files</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Importere ISO20022-filer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>You can import payment files that have the following formats:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Du kan importere betalingsfiler, som har følgende formater:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source><bpt id="p1">**</bpt>ISO20022 camt.054 credit advice<ept id="p1">**</ept> – Import incoming payments from a file in this format into the Customer payment journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ISO20022 camt.054 kreditadvis<ept id="p1">**</ept> – Importere indgående betalinger fra en fil i dette format i debitorbetalingskladden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source><bpt id="p1">**</bpt>ISO20022 pain.002 status return<ept id="p1">**</ept> and <bpt id="p2">**</bpt>ISO20022 camt.054 debit advice<ept id="p2">**</ept> – Import return files in these formats into the AP Payment transfer journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ISO20022 pain.002 returneringsstatus<ept id="p1">**</ept> og <bpt id="p2">**</bpt>ISO20022 camt.054 debetadvis<ept id="p2">**</ept> – Importere returfiler i disse formater i overførselskladden for kreditorbetaling.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prerequisites for importing the camt.054 credit advice file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Forudsætninger for at importere filen camt.054 kreditadvis</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>You must complete the following prerequisites to import bank notification messages in the camt.054.001.002 format into the Customer payment journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Følgende forudsætninger skal være opfyldt, for at du kan importere meddelelser fra banken i formatet camt.054.001.002 i debitorbetalingskladden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Import the <bpt id="p1">**</bpt>ISO20022 camt.054<ept id="p1">**</ept> Electronic reporting (ER) configuration from Microsoft Dynamics Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Importer <bpt id="p1">**</bpt>ISO20022 camt.054<ept id="p1">**</ept> med den elektroniske rapporteringskonfiguration (ER) fra Microsoft Dynamics Lifecycle Services (LCS).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Then, on the <bpt id="p1">**</bpt>Customer method of payment<ept id="p1">**</ept> page, in the <bpt id="p2">**</bpt>Import format configuration<ept id="p2">**</ept> field, select that configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vælg derefter denne konfiguration på siden <bpt id="p1">**</bpt>Debitorbetalingsmetode<ept id="p1">**</ept> i feltet <bpt id="p2">**</bpt>Importér formatkonfiguration<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For more information, see <bpt id="p1">[</bpt>File formats for methods of payment<ept id="p1">](emea-select-file-formats-for-the-method-of-payments.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Du kan finde flere oplysninger under <bpt id="p1">[</bpt>Filformater for betalingsmåder<ept id="p1">](emea-select-file-formats-for-the-method-of-payments.md)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>On the <bpt id="p1">**</bpt>All customers<ept id="p1">**</ept> page, enter a name and organization number for each customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På siden <bpt id="p1">**</bpt>Alle debitorer<ept id="p1">**</ept> skal du angive et navn og et organisationsnummer for hver debitor.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>On the <bpt id="p1">**</bpt>Customer bank account<ept id="p1">**</ept> page, set up a customer bank account record by entering the following information: IBAN or bank account number, and SWIFT code or routing number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På siden <bpt id="p1">**</bpt>Debitors bankkonto<ept id="p1">**</ept> skal du oprette en debitorbankkontopost ved at angive følgende oplysninger: IBAN eller bankkontonummer, og SWIFT-kode eller registreringsnummer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>On the <bpt id="p1">**</bpt>Bank accounts<ept id="p1">**</ept> page, set up legal entity bank accounts by entering the following information: IBAN or bank account number, SWIFT code or routing number, currency, and address.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På siden <bpt id="p1">**</bpt>Bankkonti<ept id="p1">**</ept> skal du oprette bankkonti for juridiske enheder ved at angive følgende oplysninger: IBAN eller bankkontonummer, SWIFT-kode eller registreringsnummer, valuta og adresse.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>If you plan to use Advanced bank reconciliation, on the <bpt id="p1">**</bpt>Reconciliation<ept id="p1">**</ept> FastTab, set the <bpt id="p2">**</bpt>Advanced bank reconciliation<ept id="p2">**</ept> option to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du planlægger at bruge avanceret bankafstemning, skal du på i oversigtspanelet <bpt id="p1">**</bpt>Afstemning<ept id="p1">**</ept> indstille <bpt id="p2">**</bpt>Avanceret bankafstemning<ept id="p2">**</ept> til <bpt id="p3">**</bpt>Ja<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>If you plan to reconcile unposted imported payments, set the <bpt id="p1">**</bpt>Use bank statements as confirmation of electronic payments<ept id="p1">**</ept> option to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du planlægger at afstemme en ikke-bogførte importerede betalinger, kan du indstille <bpt id="p1">**</bpt>Brug bankkontoudtog som bekræftelse på elektroniske betalinger<ept id="p1">**</ept> til <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Optional: On the <bpt id="p1">**</bpt>Transaction code mapping<ept id="p1">**</ept> page, set up the mapping between bank transaction codes in the file and bank transaction types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Valgfrit: På siden <bpt id="p1">**</bpt>Tilknytning af transaktionskode<ept id="p1">**</ept> skal du oprette en tilknytning mellem bankposteringskoder i filen og bankposteringstyperne.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>If the file contains transaction charges that you want to post together with the incoming payment, create a payment fee on the <bpt id="p1">**</bpt>Customer payment fee<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis filen indeholder posteringsgebyrer, der skal bogføres sammen med den indgående betaling, kan du oprette et betalingsgebyr på siden <bpt id="p1">**</bpt>Debitorbetalingsgebyr<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Then, on the <bpt id="p1">**</bpt>Methods of payment<ept id="p1">**</ept> page, associate the payment fee with the bank account in the payment fee setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tilknyt derefter på siden <bpt id="p1">**</bpt>Betalingsmåder<ept id="p1">**</ept> betalingsgebyret med bankkontoen i opsætningen af betalingsgebyret.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>If ESR payments will be imported and will contain ISR references (applicable for legal entities in Switzerland), complete the following setup:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis ESR-betalinger skal importeres og indeholder ISR-referencer (gælder for juridiske enheder i Schweiz), skal du angive indstillinger for følgende opsætning:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>In the <bpt id="p1">**</bpt>Customer payments, account lengths<ept id="p1">**</ept> field, enter the length of the customer code that is used in ISR references or for automatic identification of the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I feltet <bpt id="p1">**</bpt>Debitorbetalinger, kontolængde<ept id="p1">**</ept> skal du angive længden på den debitorkode, der bruges i ISR-referencer eller til automatisk identifikation af kunden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Make sure that the customer number and invoice number (number sequences) contain only digits.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sørg for, at kundenummer og fakturanummeret (nummerserier) kun indeholder cifre.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>They must contain no other characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De må ikke indeholde nogen andre tegn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The invoice number must not have leading zeros.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fakturanummeret må ikke have foranstillede nuller.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Enter the ESR, BESR, and routing number for the legal entity bank account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Angiv ESR, BESR og registreringsnumre for den juridiske enheds bankkonto.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>For more information, see <bpt id="p1">[</bpt>legacy ESR feature<ept id="p1">](emea-che-esr-customer-payments-import.md)</ept>, because similar settings are required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yderligere oplysninger finder du i <bpt id="p1">[</bpt>ældre ESR-funktion<ept id="p1">](emea-che-esr-customer-payments-import.md)</ept>, fordi der kræves lignende indstillinger.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Import the camt.054 credit advice file into the Customer payment journal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Importere filen camt.054 kreditadvis til debitorbetalingskladden</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>On the <bpt id="p1">**</bpt>Customer payment journal lines<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Functions<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>Import payments<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På siden <bpt id="p1">**</bpt>Kladdelinjer for debitorindbetalinger<ept id="p1">**</ept> skal du klikke på <bpt id="p2">**</bpt>Funktioner<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>Importer betalinger<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Select the method of payment that has the required settings for the ISO20022 camt.054 format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vælg den betalingsmåde, der har de nødvendige indstillinger for formatet ISO20022 camt.054.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Specify the required parameters and the path of the file, and then click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Angiv de krævede parametre og filstien, og klik derefter på <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The file is imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Filen importeres.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Prerequisites for importing files in the pain.002 status return and camt.054 debit advice formats into the AP Payment transfer journal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Forudsætninger for at importere filer i pain.002 returneringsstatus- og camt.054 debetadvis-format i overførselskladden for kreditorbetaling.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>You must complete the following prerequisites to import bank messages in the following ISO20022 formats to the <bpt id="p1">**</bpt>Vendor payment transfer<ept id="p1">**</ept> page: pain.002.001.003 status return messages and camt.054.001.002 debit advice.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Følgende forudsætninger skal være opfyldt, for at du kan importere bankmeddelelser i følgende ISO20022 formater til siden <bpt id="p1">**</bpt>Overførsel af kreditorbetaling<ept id="p1">**</ept>: pain.002.001.003 returneringsstatusmeddelelser og camt.054.001.002 debetadvis.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Import the <bpt id="p1">**</bpt>ISO20022 camt.054<ept id="p1">**</ept> and <bpt id="p2">**</bpt>ISO20022 pain.002<ept id="p2">**</ept> ER configurations from LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Import af <bpt id="p1">**</bpt>ISO20022 camt.054<ept id="p1">**</ept> og <bpt id="p2">**</bpt>ISO20022 pain.002<ept id="p2">**</ept> ER-konfigurationer fra LCS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>On the <bpt id="p1">**</bpt>Vendor method of payment<ept id="p1">**</ept> page, in the <bpt id="p2">**</bpt>Return format configuration<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Return format secondary configuration<ept id="p3">**</ept> fields, select the ER configurations that you imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På siden <bpt id="p1">**</bpt>Kreditors betalingsmetode<ept id="p1">**</ept> i felterne <bpt id="p2">**</bpt>Konfiguration af returformat<ept id="p2">**</ept> og <bpt id="p3">**</bpt>Sekundær konfiguration af returformat<ept id="p3">**</ept> skal du vælge de ER-konfigurationer, du har importeret.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>You will have to activate the generic electronic return format for the selected method of payment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Du vil skulle aktivere det generiske elektroniske returneringsformat for den valgte betalingsmåde.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>On the <bpt id="p1">**</bpt>Return format status mapping<ept id="p1">**</ept> page, set up the mapping of status codes between pain.002 statuses and Vendor payment journal statuses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På siden <bpt id="p1">**</bpt>Tilknytning af returformatstatus<ept id="p1">**</ept> skal du konfigurer tilknytningen af statuskoder mellem statusser for pain.002 og Kreditorbetalingskladde.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Here is an example of a status setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Her er et eksempel på et statusopsætning.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Return status</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Returstatus</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Payment status</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Betalingsstatus</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>RJCT</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RJCT</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Rejected</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Afvist</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>ACCP</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ACCP</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Accepted</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Accepteret</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>ACSP</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ACSP</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Received</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Modtaget</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>On the <bpt id="p1">**</bpt>Return format error codes<ept id="p1">**</ept> page, set up pain.002 error codes and descriptions in accordance with external ISO20022 status reason codes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På siden <bpt id="p1">**</bpt>Fejlkoder for returformat<ept id="p1">**</ept> skal du angive pain.002 fejlkoder og beskrivelser i overensstemmelse med eksterne ISO20022-statusårsagskoder.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Here is an example of part of an error code setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Her er et eksempel på en del af opsætningen af en fejlkode.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kode</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Navn</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>AC01</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AC01</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>IncorrectAccountNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IncorrectAccountNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>AC02</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AC02</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>InvalidDebtorAccountNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InvalidDebtorAccountNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>AC03</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AC03</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>InvalidCreditorAccountNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InvalidCreditorAccountNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>AC04</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AC04</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>ClosedAccountNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ClosedAccountNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>AC05</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AC05</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>ClosedDebtorAccountNumber</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ClosedDebtorAccountNumber</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>AC06</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AC06</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>BlockedAccount</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BlockedAccount</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>If the camt.054 file contains transaction charges that you want to post together with the incoming payment, create a payment fee on the <bpt id="p1">**</bpt>Vendor payment fee<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis camt.054-filen indeholder posteringsgebyrer, der skal bogføres sammen med den indgående betaling, kan du oprette et betalingsgebyr på siden <bpt id="p1">**</bpt>Kreditorbetalingsgebyr<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Then, on the <bpt id="p1">**</bpt>Methods of payment<ept id="p1">**</ept> page, associate the payment fee with the bank account in the payment fee setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tilknyt derefter på siden <bpt id="p1">**</bpt>Betalingsmåder<ept id="p1">**</ept> betalingsgebyret med bankkontoen i opsætningen af betalingsgebyret.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Import the pain.002 status return or camt.054 debit advice files into the Vendor payment journal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Importere pain.002 returneringsstatus- eller camt.054 debetadvis-filer til kreditorbetalingskladden</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Open the <bpt id="p1">**</bpt>Payment transfers<ept id="p1">**</ept> page in Accounts Payable menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Åbn siden <bpt id="p1">**</bpt>Betalingsoverførsler<ept id="p1">**</ept> i menuen i Kreditor.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>On the <bpt id="p1">**</bpt>Payment transfers<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Return file - vendor<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På siden <bpt id="p1">**</bpt>Betalingsoverførsler<ept id="p1">**</ept> skal du klikke på <bpt id="p2">**</bpt>Returfil - kreditor<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Select the method of payment that has the required settings for ISO20022 files, and then click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vælg den betalingsmåde, der har de nødvendige indstillinger for ISO20022-filer, og klik derefter på <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Select the file format that you plan to import, and then click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vælg det filformat, du vil importere, og klik derefter på <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Specify the required parameters and the path of the file, and then click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Angiv de krævede parametre og filstien, og klik derefter på <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>If you're importing the pain.002 file, the status of vendor payment lines is updated, based the information in the imported file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du importerer filen pain.002, opdateres status for kreditorbetalingslinjer baseret på oplysningerne i den importerede fil.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>If you're importing the camt.054 file, you should specify the following additional parameters:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du importerer filen camt.054, skal du angive følgende yderligere parametre:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source><bpt id="p1">**</bpt>Fee ID<ept id="p1">**</ept> – Enter the Fee ID which will define new payment fee lines, which will be created on the Vendor payment journal line if a charge amount is present in the camt.054 file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Gebyr-ID<ept id="p1">**</ept> – Angiv det gebyr-ID, der definerer nye betalingsgebyrlinjer, som oprettes på kreditorbetalingskladdelinjen, hvis der findes et gebyrbeløb i filen camt.054.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source><bpt id="p1">**</bpt>New journal name<ept id="p1">**</ept> and <bpt id="p2">**</bpt>New journal description<ept id="p2">**</ept> – Enter the name and description of the journal that processed transactions will be transferred to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Nyt kladdenavn<ept id="p1">**</ept> og <bpt id="p2">**</bpt>Beskrivelse af ny kladde<ept id="p2">**</ept> – Angiv navnet og beskrivelsen af kladden, som behandlede transaktioner skal overføres til.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>After the transfer, new voucher numbers should be assigned in the new journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Efter overførslen skal nye bilagsnumre tildeles i den nye kladde.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source><bpt id="p1">**</bpt>Import direct debit transactions<ept id="p1">**</ept> – Set this option to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept> if outgoing direct debits must be imported into the Vendor payment journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Importér Direct Debit-transaktioner<ept id="p1">**</ept> – Vælg <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept> for denne indstilling, hvis udgående direkte debiteringer skal importeres til kreditorbetalingskladden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source><bpt id="p1">**</bpt>Journal name<ept id="p1">**</ept> – Define a new journal name for the imported direct debit transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Kladdenavn<ept id="p1">**</ept> – Definer et nyt kladdenavn for de importerede direct debit-transaktioner.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source><bpt id="p1">**</bpt>Settle transactions<ept id="p1">**</ept> – Set this option to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept> if imported vendor payments must be settled with invoices that are found in the system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Udlign posteringer<ept id="p1">**</ept> – Vælg <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept> for denne indstilling, hvis importerede kreditorbetalinger skal udlignes med fakturaer, der findes i systemet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>You can view the imported information on the <bpt id="p1">**</bpt>Payment transfers<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Du kan få vist de importerede oplysninger på siden <bpt id="p1">**</bpt>Betalingsoverførsler<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Additional details</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Flere oplysninger</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>When you import a format configuration from LCS, you import the whole configuration tree which means that the Model and Model mapping configurations are included.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når du importerer en formatkonfiguration fra LCS, kan du importere hele konfigurationstræet, hvilket betyder, at Model- og Model tilknytning-konfigurationerne er medtaget.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>In the Payment model starting from version 8, the mappings are located in separate ER configurations in the solution tree (Payment model mapping 1611, Payment model mapping to destination ISO20022, etc).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I Betalingsmodel fra og med version 8 findes tilknytningerne i separate ER-konfigurationer i løsningstræet (Betalingsmodel-tilknytning 1611, Betalingsmodel-tilknytning til destination ISO20022 osv).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>There are many different payment formats under one model (Payment model), thus separate mapping handling is a key for easy solution maintenance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der er mange forskellige betalingsformater i én model (Betalingsmodel), og derfor er separat tilknytningshåndtering nøglen til nem løsningsvedligeholdelse.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>For example, consider this scenario: you use ISO20022 payments to generate credit transfer files and then you import the return messages from the bank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Overvej f.eks. følgende scenarie: Du bruger ISO20022 betalinger til at generere kreditoverførselsfiler og derefter importerer du returmeldingerne fra banken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>In this scenario, you should use the following configurations:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I denne situation skal du bruge følgende konfigurationer:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source><bpt id="p1">**</bpt>Payment model<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Betalingsmodel<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source><bpt id="p1">**</bpt>Payment model mapping 1611<ept id="p1">**</ept> – this mapping will be used to generate the export file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Betalingsmodel-tilknytning 1611<ept id="p1">**</ept> – denne tilknytning bruges til at generere eksportfilen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source><bpt id="p1">**</bpt>Payment model mapping to destination ISO20022<ept id="p1">**</ept> – this configuration includes all mappings which will be used to import the data (“to destination” mapping direction)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Betalingsmodel-tilknytning til destination ISO20022<ept id="p1">**</ept> – denne konfiguration omfatter alle de tilknytninger, der skal bruges til at importere dataene ("til destination"-tilknytningsretning)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">**</bpt>ISO20022 Credit transfer<ept id="p1">**</ept> – this configuration includes a format component that is responsible for export file generation (pain.001) based on the Payment model mapping 1611, as well as a format to model mapping component which will be used together with Payment model mapping to destination ISO20022 to register exported payments in the system for further import purposes (import in CustVendProcessedPayments technical table)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ISO20022 kreditoverførsel<ept id="p1">**</ept> – denne konfiguration omfatter en format-komponent, der er ansvarlig for at eksportere filoprettelse (pain.001) baseret på betalingsmodel-tilknytning 1611, samt et format til modeltilknytningskomponenten, der skal bruges sammen med betalingsmodel-tilknytning til destination ISO20022 til at registrere eksporterede betalinger i systemet med henblik på yderligere import (importere i den tekniske CustVendProcessedPayments-tabel)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>ISO20022 Credit transfer (CE)<ept id="p1">**</ept>, where CE correspond to country extension – derived format to the ISO20022 Credit transfer with the same structure and with certain country-specific differences</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ISO20022 pengeoverførsel (CE)<ept id="p1">**</ept>, hvor CE svarer til landeangivelsen – afledte format til ISO20022 pengeoverførsel med samme struktur og visse landespecifikke forskelle</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Pain.002<ept id="p1">**</ept> – this format will be used together with the Payment model mapping to destination ISO20022 in order to import the pain.002 file into vendor payments transfers journal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Pain.002<ept id="p1">**</ept> – dette format skal bruges sammen med betalingsmodel-tilknytningen til destination ISO20022 for at importere filen pain.002 til overførselskladder for kreditorbetaling</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source><bpt id="p1">**</bpt>Camt.054<ept id="p1">**</ept> – this format will be used together with the Payment model mapping to destination ISO20022 to import the camt.054 file into vendor payments transfers journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Camt.054<ept id="p1">**</ept> – dette format skal bruges sammen med betalingsmodel-tilknytningen til destination ISO20022 for at importere filen camt.054 til overførselskladder for kreditorbetaling.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The same format configuration will be used in customer payments import functionality, but the different mapping will be used in the Payment model mapping to destination ISO20022 configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der skal bruges samme formatkonfigurationen i funktionen til import af debitorbetalinger, men den anden tilknytning skal bruges i betalingsmodel-tilknytningen til destinationen ISO20022-konfiguration.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>For more information about Electronic reporting, refer to <bpt id="p1">[</bpt>Electronic reporting overview<ept id="p1">](../../dev-itpro/analytics/general-electronic-reporting.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yderligere oplysninger om elektronisk indberetning kan du finde i <bpt id="p1">[</bpt>Oversigt over elektronisk rapportering<ept id="p1">](../../dev-itpro/analytics/general-electronic-reporting.md)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yderligere ressourcer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source><bpt id="p1">[</bpt>Create and export vendor payments using ISO20022 payment format<ept id="p1">](./tasks/create-export-vendor-payments-iso20022-payment-format.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Oprette og eksportere kreditorbetalinger ved hjælp af ISO20022-betalingsformat<ept id="p1">](./tasks/create-export-vendor-payments-iso20022-payment-format.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">[</bpt>Import ISO20022 credit transfer configuration<ept id="p1">](./tasks/import-iso20022-credit-transfer-configuration.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Importere konfiguration for ISO20022-kreditoverførsel<ept id="p1">](./tasks/import-iso20022-credit-transfer-configuration.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source><bpt id="p1">[</bpt>Import ISO20022 direct debit configuration<ept id="p1">](./tasks/import-iso20022-direct-debit-configuration.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Importere ISO20022 Direct Debit-konfiguration<ept id="p1">](./tasks/import-iso20022-direct-debit-configuration.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><bpt id="p1">[</bpt>Set up company bank accounts for ISO20022 credit transfers<ept id="p1">](./tasks/set-up-company-bank-accounts-iso20022-credit-transfers.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Konfigurere firmas bankkonti for ISO20022-kreditoverførsler<ept id="p1">](./tasks/set-up-company-bank-accounts-iso20022-credit-transfers.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">[</bpt>Set up company bank accounts for ISO20022 direct debits<ept id="p1">](./tasks/set-up-company-bank-accounts-iso20022-direct-debits.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Konfigurere firmas bankkonti for direkte ISO20022-debiteringer<ept id="p1">](./tasks/set-up-company-bank-accounts-iso20022-direct-debits.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">[</bpt>Set up customers and customer bank accounts for ISO20022 direct debits<ept id="p1">](./tasks/set-up-bank-accounts-iso20022-direct-debits.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Konfigurere debitorer og debitorbankkonti for direkte ISO20022-debiteringer<ept id="p1">](./tasks/set-up-bank-accounts-iso20022-direct-debits.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source><bpt id="p1">[</bpt>Set up method of payment for ISO20022 credit transfer<ept id="p1">](./tasks/set-up-method-payment-iso20022-credit-transfer.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Konfigurere en betalingsmetode for ISO20022-kreditoverførsler<ept id="p1">](./tasks/set-up-method-payment-iso20022-credit-transfer.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">[</bpt>Set up method of payment for ISO20022 direct debit<ept id="p1">](./tasks/setup-method-payment-iso20022-direct-debit.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Konfigurere en betalingsmetode for ISO20022 Direct Debit<ept id="p1">](./tasks/setup-method-payment-iso20022-direct-debit.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source><bpt id="p1">[</bpt>Set up vendors and vendor bank accounts for ISO20022 credit transfers<ept id="p1">](./tasks/set-up-vendor-iso20022-credit-transfers.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Konfigurere kreditorer og kreditorbankkonti for ISO20022-kreditoverførsler<ept id="p1">](./tasks/set-up-vendor-iso20022-credit-transfers.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>