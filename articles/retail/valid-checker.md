<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="valid-checker.md" target-language="da-DK">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>valid-checker.125a66.1fc894206f9d90fce1e2eab292ac241e9d943e23.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>1fc894206f9d90fce1e2eab292ac241e9d943e23</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>aec1dcd44274e9b8d0770836598fde5533b7b569</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/03/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\valid-checker.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail transaction consistency checker</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konsistenskontrol af detailtransaktion</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the retail transaction consistency checker functionality in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dette emne beskriver funktionen konsistenskontrol af detailtransaktion i Microsoft Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Retail transaction consistency checker</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konsistenskontrol af detailtransaktion</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dette emne beskriver funktionen konsistenskontrol af detailtransaktion, der blev introduceret i Microsoft Dynamics 365 for Finance and Operations, version 8.1.3.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Konsistenskontrollen identificerer og isolerer inkonsistente transaktioner, før de hentes af processen til bogføring af opgørelsen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When a statement is posted in Microsoft Dynamics 365 for Retail, posting can fail due to inconsistent data in the retail transaction tables.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Når en opgørelse bogføres i Microsoft Dynamics 365 for Retail, kan bogføringen mislykkes på grund af inkonsistente data i detailtransaktionstabellerne.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The data issue may be caused by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Dataproblemet kan skyldes uforudsete problemer i POS-programmet, eller at transaktioner blev importeret forkert fra tredjeparts-POS-systemer.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Examples of how these inconsistencies may appear include:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksempler på, hvordan denne inkonsistens kan vise sig, omfatter:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The transaction total on the header table does not match the transaction total on the lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Totalen for transaktionen i hovedtabellen stemmer ikke overens med transaktionstotalen på linjerne.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The line count on the header table does not match with the number of lines in the transaction table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Linjeantallet i hovedtabellen stemmer ikke overens med antallet af linjer i transaktionstabellen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Taxes on the header table do not match the tax amount on the lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Moms i hovedtabellen stemmer ikke overens med momsbeløb på linjerne.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når inkonsistente transaktioner hentes af processen til bogføring af opgørelsen, oprettes der inkonsekvente salgsfakturaer og betalingskladder, og hele bogføringsprocessen for opgørelsen mislykkes derfor.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gendannelsen af opgørelserne fra en sådan tilstand omfatter komplekse rettelser af data på tværs af flere transaktionstabeller.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The retail transaction consistency checker prevents such issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konsistenskontrollen af detailtransaktioner forhindrer sådanne problemer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The following chart illustrates the posting process with the transaction consistency checker.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I følgende diagram illustreres bogføringsprocessen med konsistenskontrollen af transaktioner.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">![</bpt>Statement posting process with retail transaction consistency checker<ept id="p1">]</ept><bpt id="p2">(./media/validchecker.png "</bpt>Statement posting process with retail transaction consistency checker<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>Processen til bogføring af opgørelse med konsistenskontrol af detailtransaktioner<ept id="p1">]</ept><bpt id="p2">(./media/validchecker.png "</bpt>Processen til bogføring af opgørelse med konsistenskontrol af detailtransaktioner<ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The <bpt id="p1">**</bpt>Validate store transactions<ept id="p1">**</ept> batch process checks the consistency of the retail transaction tables for the following scenarios.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Batchprocessen <bpt id="p1">**</bpt>Valider butiksposteringer<ept id="p1">**</ept> kontrollerer konsistensen af detailtransaktionstabellerne i følgende scenarier.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Customer account<ept id="p1">**</ept> – Validates that the customer account in the retail transaction tables exists in the HQ customer master.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Debitorkonto<ept id="p1">**</ept> – validerer, at debitorkontoen i detailtransaktionstabellerne findes i debitormasteren i hovedkontoret.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Line count<ept id="p1">**</ept> – Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Linjetæller<ept id="p1">**</ept> – validerer, at antallet af linjer, som er angivet i transaktionshovedtabellen, svarer til antallet af linjer i salgstransaktionstabellerne.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Price includes tax<ept id="p1">**</ept> – Validates that the <bpt id="p2">**</bpt>Price includes tax<ept id="p2">**</ept> parameter is consistent across transaction lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Pris inkl. moms<ept id="p1">**</ept> – validerer, at parameteren <bpt id="p2">**</bpt>Pris inkl. moms<ept id="p2">**</ept> er konsistent på tværs af transaktionslinjer.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">**</bpt>Gross amount<ept id="p1">**</ept> – Validates that the gross amount on the header is the sum of the net amounts on the lines plus the tax amount.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Bruttobeløb<ept id="p1">**</ept> – validerer, at bruttobeløbet i hovedet er summen af nettobeløbene på linjerne plus momsbeløbet.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Net amount<ept id="p1">**</ept> – Validates that the net amount on the header is the sum of the net amounts on the lines.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Nettobeløb<ept id="p1">**</ept> – validerer, at nettobeløbet i hovedet er summen af nettobeløbene på linjerne.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Under / Over payment<ept id="p1">**</ept> – Validates that the difference between the gross amount on the header and the payment amount doesn't exceed the maximum underpayment/overpayment configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Under-/overbetaling<ept id="p1">**</ept> – validerer, at differencen mellem bruttobeløbet i hovedet og betalingsbeløbet ikke overskrider konfigurationen af den maksimalt tilladte underbetaling/overbetaling.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Discount amount<ept id="p1">**</ept> – Validates that the discount amount on the discount tables and the discount amount on the retail transaction line tables are consistent, and that the discount amount on the header is the sum of the discount amounts on the lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Rabatbeløb<ept id="p1">**</ept> – validerer, at rabatbeløbet på rabattabellerne og rabatbeløbet i tabellerne for detailtransaktionslinjer er konsistente, og at rabatbeløbet i hovedet er summen af rabatbeløbene på linjerne.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Line discount<ept id="p1">**</ept> – Validates that the line discount on the transaction line is the sum of all the lines in the discount table that corresponds to the transaction line.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Linjerabat<ept id="p1">**</ept> – validerer, at linjerabatten på transaktionslinjen er summen af alle linjer i rabattabellen, der svarer til transaktionslinjen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Gift card item<ept id="p1">**</ept> – Retail doesn't support the return of gift card items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Gavekortvare<ept id="p1">**</ept> – Retail understøtter ikke returnering af gavekortvarer.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>However, the balance on a gift card can be cashed out. Any gift card item that is processed as a return line instead of a cash-out line fails the statement posting process.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Saldoen på et gavekort kan dog udbetales kontant. Alle gavekortvarer, der behandles som en returlinje i stedet for en udbetalingslinje, mislykkes i bogføringsprocessen for opgørelsen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The validation process for gift card items helps guarantee that the only return gift card line items on the retail transaction tables are gift card cash-out lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Valideringsprocessen for gavekortvarer er garanti for, at de eneste returneringslinjer for gavekortvarer i detailtransaktionstabellerne er udbetalingslinjer for gavekort.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>Negative price<ept id="p1">**</ept> – Validates that there are no negative price transaction lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Negativ pris<ept id="p1">**</ept> – validerer, at der ikke er nogen negative pristransaktionslinjer.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Item &amp; Variant<ept id="p1">**</ept> – Validates that items and variants on the transaction lines exist in the item and variant master file.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Vare og variant<ept id="p1">**</ept> – validerer, at varer og varianter på transaktionslinjerne findes i masterfilen for vare og variant.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Set up the consistency checker</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Konfigurere konsistenskontrollen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Configure the "Validate store transactions" batch process, at <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Retail IT <ph id="ph2">\&gt;</ph> POS posting<ept id="p1">**</ept>, for periodic runs.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Konfigurer batchprocessen "Valider butiksposteringer" på <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Retail IT <ph id="ph2">\&gt;</ph> POS-bogføring<ept id="p1">**</ept> til periodiske kørsler.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Batchjobbet kan planlægges ud fra butikkens organisationshierarki på samme måde som processerne "Beregn opgørelser i batch" og "Bogfør opgørelse i batch" er konfigureret.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Det anbefales, at du konfigurerer denne batchproces til at køre flere gange i løbet af dagen og planlægger den, så den køres ved afslutningen af hver kørsel af P-job.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Results of validation process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Resultater af valideringsprocessen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The results of the validation check by the batch process are tagged on the appropriate retail transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Resultaterne af valideringskontrollen af batchprocessen markeres på den relevante detailtransaktion.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The <bpt id="p1">**</bpt>Validation status<ept id="p1">**</ept> field on the retail transaction record is either set to <bpt id="p2">**</bpt>Successful<ept id="p2">**</ept> or <bpt id="p3">**</bpt>Error<ept id="p3">**</ept>, and the date of the last validation run appears on the <bpt id="p4">**</bpt>Last validation time<ept id="p4">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Feltet <bpt id="p1">**</bpt>Valideringsstatus<ept id="p1">**</ept> på detailtransaktionsposten er enten angivet til <bpt id="p2">**</bpt>Fuldført<ept id="p2">**</ept> eller <bpt id="p3">**</bpt>Fejl<ept id="p3">**</ept>, og datoen for den seneste valideringskørsel vises i feltet <bpt id="p4">**</bpt>Sidste valideringstidspunkt<ept id="p4">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the <bpt id="p1">**</bpt>Validation errors<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">For at få vist mere beskrivende fejltekst, der vedrører en valideringsfejl, skal du vælge den relevante detailbutikstransaktionspost og klikke på knappen <bpt id="p1">**</bpt>Valideringsfejl<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Transaktioner, der ikke består valideringskontrollen, og transaktioner, der endnu ikke blevet valideret, trækkes ikke ind i opgørelser.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Under processen "Beregn opgørelse" får brugere besked, hvis der findes posteringer, der kunne have været medtaget i opgørelsen, men ikke blev det.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>If a validation error is found, the only way to fix the error is to contact Microsoft Support.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis der findes en valideringsfejl, er den eneste måde at rette fejlen på, at kontakte Microsoft Support.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In a future release, capability will be added so that users can fix the records that failed through the user interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I en senere version vil der blive tilføjet en funktion, så brugerne kan rette de poster, hvor der opstod fejl, via brugergrænsefladen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Logging and auditing capabilities will also be made available to trace the history of the modifications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Logførings- og overvågningsfunktioner vil også blive tilgængelige, så historikken over ændringerne kan spores.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Additional validation rules to support more scenarios will be added in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der tilføjes yderligere valideringsregler for at understøtte flere scenarier i en senere version.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>