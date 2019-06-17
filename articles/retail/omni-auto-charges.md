<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="omni-auto-charges.md" target-language="da-DK">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>omni-auto-charges.2f6e37.47829a6fcae37e03510929dc46b942455016df0b.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>47829a6fcae37e03510929dc46b942455016df0b</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>ffc37f7c2a63bada3055f37856a30424040bc9a3</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/16/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\omni-auto-charges.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Omni-channel advanced auto charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Avancerede automatiske gebyrer for omni-kanal</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes capabilities for managing additional order charges for Retail channel orders using advanced auto charges features.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I dette emne beskrives funktioner til styring af ekstra ordregebyrer for detailkanalordrer ved hjælp af funktioner til avancerede automatiske gebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Omni-channel advanced auto charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Avancerede automatiske gebyrer for omni-kanal</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides information on configuration and deployment of the advanced auto-charges feature which are available in Dynamics 365 for Retail version 10.0.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dette emne indeholder oplysninger om konfiguration og implementering af den avancerede automatiske gebyrfunktion, der er tilgængelig i Dynamics 365 for Retail version 10.0.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When the advanced auto-charges features are enabled, orders created in any supported Retail channel (point of sale (POS), call center, and online), can take advantage of the <bpt id="p1">[</bpt>auto-charges<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> configurations defined in the ERP application for both header and line-level related charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når de avancerede automatiske gebyrfunktioner er aktiveret, kan ordrer, der oprettes i en understøttet detailkanal (POS, callcenter og online), udnytte de konfigurationer for <bpt id="p1">[</bpt>automatiske gebyrer<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept>, der er defineret i ERP-programmet for gebyrer på både for ordrehoved- og -linjeniveau.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In releases prior to Dynamics 365 for Retail version 10.0, <bpt id="p1">[</bpt>auto-charge<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> configurations are only accessible by orders created in e-Commerce and call center channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I versioner før Dynamics 365 for Retail version 10.0 er konfigurationer af <bpt id="p1">[</bpt>automatiske gebyrer<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> kun tilgængelige for ordrer, der er oprettet i e-handels- og callcenterkanaler.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In versions 10.0 and later, POS-created orders can leverage the auto-charges configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I 10.0 og senere versioner kan POS-oprettede ordrer udnytte de automatiske gebyrkonfigurationer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>That way, additional miscellaneous charges can systematically be added to sales transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På denne måde kan flere gebyrer systematisk føjes til salgstransaktioner.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>When using releases prior to version 10.0, a POS user is prompted to manually enter a shipping fee during the creation of a "ship all" or "ship selected" POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I versioner før version 10.0 bliver POS-brugere bedt om at angive et forsendelsesgebyr manuelt under oprettelse af en "send alle" eller "send valgte" POS transaktion.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>While the miscellaneous charges capabilities of the application are utilized in respect to how the charges are written to the order, no systematic calculation is provided – the calculation relies on the user's input to determine the value of the charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">Når gebyrfunktionerne i programmet bruges i forhold til, hvordan gebyrerne skrives til ordren, foretages der ingen systematisk beregning – beregningen til bestemmelse af værdien af gebyrerne er baseret på input fra brugeren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The charges can only be added as a single "shipping" related charges code and cannot easily be edited or changed in the POS after they are created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gebyrerne kan kun tilføjes som en enkelt "forsendelse"-relaterede gebyrkode og kan kun dårligt redigeres eller ændres i POS, når de først er oprettet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The use of manual prompts to add shipping charges is still available in versions 10.0 and later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der bruges stadig manuelle prompts ved tilføjelse af forsendelsesgebyrer i version 10.0 og nyere.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>If an organization does not enable the <bpt id="p1">**</bpt>Advanced Auto-charges<ept id="p1">**</ept> parameter, the POS prompts for manual entry of charges will remain the same.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis en organisation ikke aktiverer parameteren <bpt id="p1">**</bpt>Avancerede automatiske gebyrer<ept id="p1">**</ept>, forbliver POS-prompts om manuel angivelse af gebyrer uændret.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>With the advanced auto-charges feature, POS users can have systematic calculations for any defined miscellaneous charges based on auto-charges setup tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Med den avancerede automatiske gebyrfunktion kan POS-brugere få systematiske beregninger for ethvert defineret gebyr baseret på tabeller til opsætning af automatiske gebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In addition, users will have the ability to add or edit an unlimited amount of additional charges and fees to any POS sales transaction at the header or line-level (for a cash and carry or customer order).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Desuden får brugere mulighed for at tilføje eller redigere et ubegrænset antal ekstra gebyrer og gebyrer for enhver POS-salgstransaktion på hoved- eller linjeniveau (for en cash and carry- eller kundeordre).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Enabling advanced auto-charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aktivering af avancerede automatiske gebyrer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>On the <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Headquarters setup <ph id="ph2">\&gt;</ph> Parameters <ph id="ph3">\&gt;</ph> Retail parameters<ept id="p1">**</ept> page, go to the <bpt id="p2">**</bpt>Customer orders<ept id="p2">**</ept> tab. On the <bpt id="p3">**</bpt>Charges<ept id="p3">**</ept> FastTab, set <bpt id="p4">**</bpt>Use advanced auto-charges<ept id="p4">**</ept> to <bpt id="p5">**</bpt>Yes<ept id="p5">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">På siden <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Opsætning af Headquarters <ph id="ph2">\&gt;</ph> Parametre <ph id="ph3">\&gt;</ph> Detailparametre<ept id="p1">**</ept> skal du gå til fanen <bpt id="p2">**</bpt>Kundeordrer<ept id="p2">**</ept>. I oversigtspanelet <bpt id="p3">**</bpt>Gebyrer<ept id="p3">**</ept> skal du indstille <bpt id="p4">**</bpt>Brug avancerede automatiske gebyrer<ept id="p4">**</ept> til <bpt id="p5">**</bpt>Ja<ept id="p5">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Advanced Auto-Charges Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Parametre for avancerede automatiske gebyrer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>When advanced auto-charges are enabled, users are no longer prompted to manually enter a shipping charge at the POS terminal when creating a ship-all or ship-selected customer order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når avancerede autogebyrer er aktiveret, bliver brugerne ikke længere bedt om manuelt at indtaste et forsendelsesgebyr i POS-klienten, når de opretter en kundeordre af typen send alle eller send valgte.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>POS order charges are systematically calculated and added to the POS transaction (if a corresponding auto-charges table that matches the criterion of the order being created are found).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS-gebyrer beregnes systematisk og føjes til POS-transaktionen (hvis der findes en tilsvarende tabel for automatiske gebyrer, der svarer til kriteriet for den ordre, der oprettes).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Users can also add or maintain header or line-level charges manually through newly added POS operations that can be added to the POS screen layouts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brugere kan også tilføje eller vedligeholde gebyrer på hoved- eller linjeniveau manuelt via nye, tilføjede POS-handlinger, der kan føjes til POS-skærmlayoutet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>When advanced auto-charges are enabled, the existing <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> for <bpt id="p2">**</bpt>Shipping charges code<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Refund shipping charges<ept id="p3">**</ept> are no longer utilized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når avancerede automatiske gebyrer er aktiveret, bruges de eksisterende <bpt id="p1">**</bpt>Detailparametre<ept id="p1">**</ept> for <bpt id="p2">**</bpt>Kode for forsendelsesgebyrer<ept id="p2">**</ept> og <bpt id="p3">**</bpt>Refunder forsendelsesgebyrer<ept id="p3">**</ept> ikke længere.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>These parameters are only applicable if the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is set to <bpt id="p2">**</bpt>No<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Disse parametre gælder kun hvis parameteren <bpt id="p1">**</bpt>Brug avancerede automatiske gebyrer<ept id="p1">**</ept> er indstillet til <bpt id="p2">**</bpt>Nej<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Before you enable this feature, ensure that you have tested and trained your employees, as this will change the business process flow of how shipping or other charges are calculated and added to POS sales orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Inden du aktiverer denne funktion, skal du teste og uddanne dine medarbejdere, fordi dette ændrer forretningsprocessen for, hvordan forsendelsesgebyrer eller andre gebyrer beregnes og føjes til salgsordrer i POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Make sure that you understand the impact of the process flow to the creation of transactions from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Du skal kunne forstå, hvilken virkning procesforløbet har på oprettelsen af transaktioner fra POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>For call center and e-Commerce orders, the impact of enabling advanced auto-charges is minimal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Virkningen af at aktivere avancerede automatiske gebyrer er minimal for callcenter- og e-handelsordrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Call center and e-Commerce applications will continue to have the same behavior they have had historically related to the auto-charges tables to calculate additional order fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Callcenter- og e-handels-programmer vil fortsat fungere på samme måde, som de har gjort historisk i forbindelse med tabeller for automatiske gebyrer til beregning af yderligere gebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Call center channel users will continue to have the ability to manually edit any system calculated auto-charges at the header or line level, or manually add additional miscellaneous charges at the header or line level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Callcenterkanalbrugere har fortsat mulighed for manuelt at redigere eventuelle systemberegnede automatiske gebyrer på hoved- eller linjeniveau eller manuelt tilføje ekstra gebyrer på hoved- eller linjeniveau.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Additional POS operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yderligere POS-handlinger</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>For advanced auto-charges to work properly in your POS application environment, new POS operations have been added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der er tilføjet nye operationer i POS, der sikrer, at avancerede automatiske gebyrer kan fungere korrekt i dit POS-programmiljø.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>These operations must be added to your <bpt id="p1">[</bpt>POS screen layouts<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> and deployed to the POS devices as you deploy advanced auto-charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Disse handlinger skal føjes til dine <bpt id="p1">[</bpt>POS-skærmlayout<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> og installeres på POS-enhederne, når du implementerer avancerede automatiske gebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>If these operations are not added, users will not be able to manage or maintain miscellaneous charges on the POS transactions and will have no way of adjusting or changing the charges values that are systematically calculated based on auto-charges configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis disse handlinger ikke tilføjes, kan brugerne ikke administrere eller vedligeholde gebyrer på POS-transaktioner og har ingen mulighed for at justere eller ændre værdierne for gebyrer, der systematisk er beregnet ud fra konfigurationer af automatiske gebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>At minimum, it is suggested that you deploy the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation to your POS layout.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Det anbefales, at du som minimum anvender handlingen <bpt id="p1">**</bpt>Administrer gebyrer<ept id="p1">**</ept> på dit POS-layout.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The new operations are as follows.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Der findes følgende nye handlinger.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><bpt id="p1">**</bpt>142 - Manage charges<ept id="p1">**</ept> – Use this operation to allow POS users to view and edit miscellaneous charges for the POS transaction that were either added manually or systematically through auto-charges calculations.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>142 - Administrer gebyrer<ept id="p1">**</ept> – Brug denne handling til at give POS-brugere tilladelse til at se og redigere gebyrer for den POS-transaktion, der enten blev tilføjet manuelt eller systematisk via beregninger af automatiske gebyrer.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>141 - Add header charges<ept id="p1">**</ept> – Use this operation to give the user the ability to manually add a header-level miscellaneous charge to any POS sales transaction (and select the charges code to be used).</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>141 – Tilføj gebyrer i hoved<ept id="p1">**</ept> – Brug denne handling for at give brugeren mulighed for manuelt at føje et gebyr på hovedniveau til eventuelle POS-salgstransaktioner (og vælge den gebyrkode, der skal bruges).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>140 - Add line charges<ept id="p1">**</ept> – Use this operation to give the user the ability to manually add a line level miscellaneous charge to any POS sales transaction line (and select the charges code to be used).</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>140 – Tilføj linjegebyrer<ept id="p1">**</ept> – Brug denne handling for at give brugeren mulighed for manuelt at føje et gebyr på linjeniveau til en eventuel POS-salgstransaktionslinje (og vælge den gebyrkode, der skal bruges).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>143 - Recalculate charges<ept id="p1">**</ept> – Use this operation to perform a full re-calculation of the charges for the sales transaction.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>143 - Genberegn gebyrer<ept id="p1">**</ept> – Brug denne handling til at udføre en komplet genberegning af gebyrerne for salgstransaktionen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Any previously user-overwritten auto-charges will be recalculated based on the current cart configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eventuelle tidligere automatiske gebyrer, der er tilsidesat af en bruger, genberegnes baseret på den aktuelle konfiguration af indkøbsvognen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>As with all POS operations, security configurations can be made to require manager approval in order to execute the operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Som med alle POS-handlinger kan sikkerhedskonfigurationer udføres, så det kræver godkendelse fra lederen at udføre handlingen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>It is important to note that the above listed POS operations can also be added to the POS layout even if the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Det er vigtigt at bemærke, at de ovenfor angivne POS operationer også kan føjes til POS layout, selvom <bpt id="p1">**</bpt>Brug avancerede automatiske gebyrer<ept id="p1">**</ept>-parameteren er deaktiveret.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In this scenario, organizations will still get added benefits of being able to view manually added charges and edit them using the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I dette scenario får organisationer stadig fordelene ved at kunne få vist gebyrer, der er tilføjet manuelt, og redigere dem ved hjælp af handlingen <bpt id="p1">**</bpt>Administrer gebyrer<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Users may also use the <bpt id="p1">**</bpt>Add header charges<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Add line charges<ept id="p2">**</ept> operations for POS transactions even when <bpt id="p3">**</bpt>Use advanced auto-charges<ept id="p3">**</ept> parameter is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brugere kan også bruge handlingerne <bpt id="p1">**</bpt>Tilføj hovedgebyrer<ept id="p1">**</ept> og <bpt id="p2">**</bpt>Tilføj linjegebyrer<ept id="p2">**</ept> for POS-transaktioner, selv når <bpt id="p3">**</bpt>Brug avancerede automatiske gebyrer<ept id="p3">**</ept>-parameteren er deaktiveret.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>The <bpt id="p1">**</bpt>Recalculate charges<ept id="p1">**</ept> operation has less functionality if used when <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Handlingen <bpt id="p1">**</bpt>Genberegn gebyrer<ept id="p1">**</ept> har mindre funktionalitet, hvis den bruges, når <bpt id="p2">**</bpt>Brug avancerede automatiske gebyrer<ept id="p2">**</ept> er deaktiveret.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In this sceanrio, nothing would be recalculated and any charges manually added to the transaction would just reset to $0.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I dette scenario skal intet genberegnes, og eventuelle gebyrer, der er føjet til transaktionen manuelt, ville blot nulstille til $0,00.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Use case examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksempler på brugsmønstre</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>In this section, sample use cases are presented to help you understand the configuration and usage of auto-charges and miscellaneous charges within the context of Retail channel orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I dette afsnit beskrives brugsmønstre, som kan hjælpe dig med at forstå konfiguration og brug af automatiske gebyrer og andre gebyrer inden for rammerne af detailkanalordrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>These examples illustrate the behavior of the application when the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter has been enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Disse eksempler illustrerer funktionsmåden af programmet, når parameteren <bpt id="p1">**</bpt>Brug avancerede automatiske gebyrer<ept id="p1">**</ept> er aktiveret.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Auto-charges header charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksempel på automatiske gebyrer af typen hovedgebyrer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brugsmønsterscenario</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>A retailer wants to automatically add charges for freight when transactions are created in any Retail channel that require a shipment of products to the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En forhandler ønsker automatisk at tilføje gebyrer for fragt, når der oprettes transaktioner i en detailkanal, der kræver en forsendelse af produkter til kunden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The retailer offers 2 methods of delivery: Ground and Air.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Detailhandleren tilbyder 2 leveringsmåder: Fragt og Luft.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>If a customer chooses Ground delivery and the order value is less than $100, the retailer wants to charge the customer a freight charge of $10.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis en kunde vælger Fragt-levering, og ordreværdien er mindre end 100 USD, vil detailhandleren kræve et fragtgebyr af kunden på 10,00 USD.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>If the order is over $100 in value and the customer chooses ground shipping, the customer will not be charged any additional freight fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis ordreværdien er over 100 USD, og kunden vælger Fragt-levering, opkræves kunden ikke yderligere fragtgebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If the customer chooses the Air method of delivery for all orders, regardless of their total value, will be charged a freight fee of $20.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis kunden vælger leveringsmetoden Luft for alle ordrer, uanset deres samlede værdi, opkræves et fragtgebyr på 20,00 USD.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Installation og konfiguration</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This scenario requires the configuration of two auto-charges tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dette scenario kræver konfiguration af to tabeller for automatiske gebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Go to <bpt id="p1">**</bpt>Accounts receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Auto charges<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gå til <bpt id="p1">**</bpt>Debitor <ph id="ph1">\&gt;</ph> Konfiguration af gebyrer <ph id="ph2">\&gt;</ph> Automatiske gebyrer<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Configure two different header-level auto charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konfigurer to forskellige automatiske gebyrer på overskriftsniveau.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Configure one for the "Ground mode" of delivery and one for the "Air mode" of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konfigurer ét for "Fragt-leveringsmåde" og ét for "Luft-leveringsmåde".</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>For this scenario, configure them to be used for "All customers".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I dette scenarie skal du konfigurere dem, så de kan bruges til "Alle kunder".</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>For the ground delivery charges, in the lines section of the <bpt id="p1">**</bpt>Auto-charges<ept id="p1">**</ept> page, define a charge that will be applied for orders between $.01 and $100 as $10.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">For Fragt-leveringsgebyrerne skal du i området Linjer på siden <bpt id="p1">**</bpt>Automatiske gebyrer<ept id="p1">**</ept> definere et gebyr, der gælder for ordrer mellem 0,01 USD og 100 USD som 10,00 USD.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Create another charges line to indicate orders over $100.01 will have no charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Opret en anden gebyrlinje for at angive, at ordrer over 100,01 USD er gebyrfri.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Auto charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksempel på automatiske gebyrer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>For the air delivery charges, in the lines section of the auto-charges form, define a charge of $20.00 that will be applied to all orders (between a value of $.01 to $9,999,999).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">For Luft-leveringsgebyrerne skal du i området Linjer i formularen Automatiske gebyrer definere et gebyr på 20,00 USD, der skal anvendes på alle ordrer (mellem en værdi på 0,01 og 9.999.999 USD).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Send the changes to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Send gebyrerne til Retail Server/Kanaldatabase, så POS kan udnytte dem, ved at køre jobbet <bpt id="p1">**</bpt>Distributionsplan 1040<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Sales processing for this scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Salgsbehandling i dette scenarie</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>After the configuration steps above are complete and the changes have been applied to the channel database, any customer order or sales transaction created in the POS, call center, or e-Commerce channels that have the ground or air delivery methods set at the header level will utilize these charges and automatically apply them to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når konfigurationen ovenfor er fuldført, og ændringerne er anvendt på kanaldatabasen, udnytter enhver kundeordre eller salgstransaktion, der er oprettet i POS, callcenter eller e-handels-kanaler, og har leveringsmetoden Fragt eller Luft angivet på hovedniveau, disse gebyrer og anvender dem automatisk på salget.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>At this time the charges will apply to all sales transactions created within the legal entity that utilize these delivery modes, as there is no functionality to designate that an auto-charge configuration will only apply to a specific selling channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På nuværende tidspunkt anvendes gebyrerne på alle salgstransaktioner, der er oprettet inden for den juridiske enhed, og bruger disse leveringsmåder, fordi der ikke findes nogen funktionalitet, som angiver, at en konfiguration af automatiske gebyrer kun gælder for en bestemt salgskanal.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For POS and e-Commerce scenarios, because there is no clearly defined "header" on these orders, header-level charges will only apply if all sales lines on the transaction are set to ship with the exact same mode of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvad angår POS- og e-handelsscenarier – fordi der ikke er noget klart defineret "hoved" på disse ordrer, anvendes gebyrer på hovedniveau kun, hvis alle salgslinjer i transaktionen er indstillet til levering med nøjagtig samme leveringsmåde.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>If there are "mixed-modes" of fulfillment on the transactions created by POS or e-Commerce, only line-level auto-charges will be considered and applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis der er "blandede måder" for ordreopfyldning på de transaktioner, der er oprettet af POS- eller e-handel, er det kun automatiske gebyrer på linjeniveau, der tages i betragtning og anvendes.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>In call center scenarios, the user has control over the setting of the delivery mode at the order header, therefore header-level charges will apply for these orders even if some of the sales lines have been configured to use a different mode of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brugeren har kontrol over indstillingen af leveringsmåden på ordrehovedet i callcenterscenarier, og derfor anvendes gebyrer på hovedniveau for disse ordrer, selvom nogle af salgslinjerne er konfigureret til at bruge en anden leveringsmåde.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Header-level charges for call center orders will always be based on the mode of delivery that is defined at the order header level of the sales order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gebyrer på hovedniveau for callcenterordrer baseres altid på den leveringsmåde, der er defineret på ordrehovedniveau i salgsordren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Auto-charges line charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksempel på automatiske gebyrer af typen linjegebyrer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brugsmønsterscenario</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>A retailer wants to add an additional charge to the customer for setup fees when the customer purchases a particular model of computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En forhandler ønsker at tilføje et ekstra gebyr til kunden som et opsætningsgebyr, når kunden køber en bestemt computermodel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>This computer requires additional non-optional setup actions that the retailer will perform for the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Denne computer kræver yderligere ikke-obligatoriske opsætningshandlinger, som forhandleren skal udføre for kunden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The retailer has informed customers that there will be an additional fee for this setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Forhandleren har underrettet kunderne om, at der vil være et ekstra gebyr for denne opsætning.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The retailer prefers to manage the charges related to this fee separately from the product sales price for financial reporting purposes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Forhandleren foretrækker at administrere de gebyrer, der er relateret til dette gebyr separat fra salgsprisen for produktet af økonomiske rapporteringshensyn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>A setup fee of $19.99 will be charged to the customer when this specific computer is purchased in any retail channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Et gebyr for opsætning på 19,99 USD vil blive faktureret kunden, når denne computer købes via en detailkanal.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Installation og konfiguration</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This scenario requires the configuration of one line-level auto charges table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dette scenario kræver konfiguration af én tabel for automatiske gebyrer på linjeniveau.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Go to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Auto charges<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gå til <bpt id="p1">**</bpt>Debitor <ph id="ph1">\&gt;</ph> Konfiguration af gebyrer <ph id="ph2">\&gt;</ph> Automatiske gebyrer<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Set the <bpt id="p1">**</bpt>Level<ept id="p1">**</ept> drop-down menu to <bpt id="p2">**</bpt>Line<ept id="p2">**</ept>, and create a new auto-charges record for all customers and for the specific product or product group where the setup fees will be charged.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Indstil <bpt id="p1">**</bpt>Niveau<ept id="p1">**</ept> rullemenuen til <bpt id="p2">**</bpt>Linje<ept id="p2">**</ept>, og opret en ny post til automatiske gebyrer for alle kunder og for det specifikke produkt eller produktgruppe, hvor opsætningsgebyrerne bliver opkrævet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Auto charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksempel på automatiske gebyrer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Send gebyrerne til Retail Server/Kanaldatabase, så POS kan udnytte dem, ved at køre jobbet <bpt id="p1">**</bpt>Distributionsplan 1040<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Sales processing for this scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Salgsbehandling i dette scenarie</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>After the configurations steps above are complete and the changes have been applied to the channel database, any customer order or sales transaction created in the POS, call center, or e-Commerce channels that have this item on the order will trigger a line-level charge to be systematically added to the order total.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når konfigurationen ovenfor er fuldført, og ændringerne er anvendt på kanaldatabasen, udløser enhver kundeordre eller salgstransaktion, der er oprettet i POS, callcenter eller e-handels-kanaler, der har denne vare på ordren, et gebyr på linjeniveau, der systematisk føjes til ordretotalen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>At this time the charges will apply to any sales line that matches the configuration of the line-level auto charges within the legal entity, as there is no functionality to configure a line-level auto-charge to apply only to a specific selling channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På nuværende tidspunkt anvendes gebyrerne på enhver salgslinje, der matcher konfigurationen af automatiske gebyrer på linjeniveau inden for den juridiske enhed, fordi der ikke findes nogen funktioner til konfiguration af automatiske gebyrer på linjeniveau, så de kun gælder for en bestemt salgskanal.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Manual header charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksempel på manuelle hovedgebyrer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Use case scenario description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Beskrivelse af brugsmønsterscenario</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>A retailer is making an exception to typical processes by offering to provide a special home delivery of products to a customers who order products in the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En forhandler gør en undtagelse fra typiske processer ved at tilbyde at levere en særlig privat levering af produkter til en kunde, der bestiller produkter i butikken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The retailer and the customer have agreed that the customer will pay an additional $25 handling fee for this service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Forhandleren og kunden har aftalt, at kunden skal betale et gebyr på 25 USD ekstra for håndtering af denne service.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The order-taker needs to add this additional fee to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Medarbejderen hos forhandleren skal føje dette ekstra gebyr til transaktionen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Because the fee is a blanket fee and not related to any single product on the order, a header charge will be utilized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Da gebyret er et rammeordregebyr og ikke er relateret til et enkelt produkt i ordren, bruges et hovedgebyr.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Installation og konfiguration</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Ensure the charges code that will be used in this scenario has been properly configured by going to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Charges<ept id="p1">**</ept> to define an appropriate charges code for the scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sørg for, at den gebyrkode, der skal bruges i dette scenario, er konfigureret korrekt, ved at gå til <bpt id="p1">**</bpt>Debitor <ph id="ph1">\&gt;</ph> Konfiguration af gebyrer <ph id="ph2">\&gt;</ph> Tillæg<ept id="p1">**</ept> for at definere en tillægskode, der er relevant for scenariet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksempel på gebyrer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>If the charge should be considered a "shipping" related charge for the purpose of shipping related discounts or promotions, set <bpt id="p1">**</bpt>Shipping charge<ept id="p1">**</ept> on the charges code to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">Hvis gebyret skal betragtes som et gebyr, der er relateret til "forsendelse" med henblik på forsendelsesrelaterede rabatter eller kampagnetilbud, skal du indstille <bpt id="p1">**</bpt>Forsendelsesgebyr<ept id="p1">**</ept> i gebyrkoden til <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>If this charge is also allowed to be systematically refunded during the processing of a return transaction in the POS application, set <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis dette gebyr også må refunderes systematisk under behandlingen af en returtransaktion i POS-programmet, kan du indstille <bpt id="p1">**</bpt>Kan refunderes<ept id="p1">**</ept> til <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>The <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag is only applicable when the <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> parameter is set to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Flaget <bpt id="p1">**</bpt>Kan refunderes<ept id="p1">**</ept> kan kun anvendes, når <bpt id="p2">**</bpt>Brug avancerede automatiske gebyrer<ept id="p2">**</ept> parameter er indstillet til <bpt id="p3">**</bpt>Ja<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Send gebyrerne til Retail Server/Kanaldatabase, så POS kan udnytte dem, ved at køre jobbet <bpt id="p1">**</bpt>Distributionsplan 1040<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>The <bpt id="p1">**</bpt>Add header charge<ept id="p1">**</ept> operation must be configured in your <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a button that is accessible to the user from POS can call this operation (operation 141).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Handlingen <bpt id="p1">**</bpt>Tilføj gebyrer i hoved<ept id="p1">**</ept> skal være konfigureret i dit <bpt id="p2">[</bpt>POS-skærmlayout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept>, så en knap, der er tilgængelig for brugeren fra POS, kan kalde denne handling (handling 141).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The screen layout changes must be distributed to the retail channel as well through the distribution schedule function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skærmlayout-ændringer skal fordeles til detailkanalen samt via distributionstidsplansfunktionen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Sales processing of manual header charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Salgsprocessen for manuelle hovedgebyrer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>To execute the scenario in the POS application, the POS user will create the sales transaction as usual, adding the products and any other configurations to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Du kan udføre scenariet i POS-programmet. POS-brugeren opretter salgstransaktionen som sædvanlig og tilføjer produkterne og eventuelle andre konfigurationer til salget.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Prior to collecting payment, the user should execute the <bpt id="p1">**</bpt>Add header charge<ept id="p1">**</ept> operation, which will prompt the user to select a charges code and enter the charges value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Før opkrævning af betaling skal brugeren udføre <bpt id="p1">**</bpt>Tilføj gebyrer i hoved<ept id="p1">**</ept> handlingen, hvor brugeren bliver bedt om at vælge en gebyrkode og angive værdien for gebyret.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Once the user completes the process, the charge will be added to the sales order as a header-level charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når brugeren har fuldført processen, føjes gebyret til salgsordren som et gebyr på overskriftsniveau.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>This process can be applied in the call center by using the existing <bpt id="p1">**</bpt>Charges<ept id="p1">**</ept> feature found on the <bpt id="p2">**</bpt>Sell<ept id="p2">**</ept> tab on the toolbar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Denne proces kan anvendes i callcenter ved hjælp af den eksisterende <bpt id="p1">**</bpt>Tillæg<ept id="p1">**</ept> funktion, der findes under fanen <bpt id="p2">**</bpt>Sælg<ept id="p2">**</ept> på værktøjslinjen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Maintain charges<ept id="p1">**</ept> page, the user can add a new charges line to the order header.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På siden <bpt id="p1">**</bpt>Vedligehold gebyrer<ept id="p1">**</ept> kan brugeren tilføje en ny gebyrlinje i ordrehovedet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Manual line charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksempel på manuelt linjegebyr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brugsmønsterscenario</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>A customer has requested that 2 of the 5 items on their sales order be gift-wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En kunde har anmodet om, at 2 af 5 varer på salgsordren bliver pakket som gave.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>The retailer offers this optional service for a fee of $2.00 per item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Detailhandleren tilbyder denne valgfrie tjeneste for et gebyr på 2,00 USD pr. vare.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The order-taker will need to add these fees to the specific items that need to be gift-wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Medarbejderen hos detailhandleren skal tilføje disse gebyrer til de forskellige varer, som skal pakkes som gave.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Installation og konfiguration</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Ensure the charges code that will be used in this scenario has been properly configured by going to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Charges<ept id="p1">**</ept> to define an appropriate charges code for the scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sørg for, at den gebyrkode, der skal bruges i dette scenario, er konfigureret korrekt, ved at gå til <bpt id="p1">**</bpt>Debitor <ph id="ph1">\&gt;</ph> Konfiguration af gebyrer <ph id="ph2">\&gt;</ph> Tillæg<ept id="p1">**</ept> for at definere en tillægskode, der er relevant for scenariet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>If the charge should be considered a "shipping" related charge for the purpose of shipping related discounts or promotions, set the <bpt id="p1">**</bpt>Shipping charge<ept id="p1">**</ept> on the charges code to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis gebyret skal betragtes som et gebyr, der er relateret til "forsendelse" med henblik på forsendelsesrelaterede rabatter eller kampagnetilbud, skal du indstille <bpt id="p1">**</bpt>Forsendelsesgebyr<ept id="p1">**</ept> i gebyrkoden til <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>If the charge is also allowed to be systematically refunded during the processing of a return transaction in the POS application, set <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis gebyret også må refunderes systematisk under behandlingen af en returtransaktion i POS-programmet, kan du indstille <bpt id="p1">**</bpt>Kan refunderes<ept id="p1">**</ept> til <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>The <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag is only applicable when the <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> parameter is set to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Flaget <bpt id="p1">**</bpt>Kan refunderes<ept id="p1">**</ept> kan kun anvendes, når <bpt id="p2">**</bpt>Brug avancerede automatiske gebyrer<ept id="p2">**</ept> parameter er indstillet til <bpt id="p3">**</bpt>Ja<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Send gebyrerne til Retail Server/Kanaldatabase, så POS kan udnytte dem, ved at køre jobbet <bpt id="p1">**</bpt>Distributionsplan 1040<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>The <bpt id="p1">**</bpt>Add line charge<ept id="p1">**</ept> operation must be configured in your <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a button that is accessible to the user from POS can call this operation (operation 140).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Handlingen <bpt id="p1">**</bpt>Tilføj linjegebyrer<ept id="p1">**</ept> skal være konfigureret i dit <bpt id="p2">[</bpt>POS-skærmlayout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept>, så en knap, der er tilgængelig for brugeren fra POS, kan kalde denne handling (handling 140).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>The screen layout changes must be distributed to the retail channel as well through the distribution schedule function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skærmlayout-ændringer skal fordeles til detailkanalen samt via distributionstidsplansfunktionen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Sales processing of the manual line charge</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Salgsprocessen for det manuelle linjegebyr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>To execute the scenario in the POS application, the POS user will create the sales transaction as usual, adding the products and any other configurations to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Du kan udføre scenariet i POS-programmet. POS-brugeren opretter salgstransaktionen som sædvanlig og tilføjer produkterne og eventuelle andre konfigurationer til salget.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Prior to collecting payment, the user should select the specific line where the charge will apply from the POS item list display and execute the <bpt id="p1">**</bpt>Add line charge<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Før opkrævning af betaling, skal brugeren vælge den specifikke linje, hvor gebyret anvendes, fra visningen med POS-varelisten og udføre <bpt id="p1">**</bpt>Tilføj linjegebyr<ept id="p1">**</ept>-handlingen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>The user will be prompted to select a charges code and enter the charges value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brugeren bliver bedt om at vælge en gebyrkode og angiv værdien af gebyret.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Once the user completes the process, the charge will be linked to the line and added to the order total as a line level charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når brugeren har fuldført processen, knyttes gebyret til linjen og føjes til ordretotalen som et gebyr på linjeniveau.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The user can repeat the process to add additional line charges to other items lines on the transaction if needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brugeren kan gentage processen for at føje yderligere linjegebyrer til andre varelinjer i posteringen, hvis det er nødvendigt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The same process can be applied in the call center by using the "maintain charges" feature found under the <bpt id="p1">**</bpt>Financials<ept id="p1">**</ept> drop-down menu in the <bpt id="p2">**</bpt>Sales order lines<ept id="p2">**</ept> section on the <bpt id="p3">**</bpt>Sales order<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Den samme proces kan anvendes i callcenteret ved hjælp af funktionen "Vedligehold gebyrer", som du finder under <bpt id="p1">**</bpt>Regnskaber<ept id="p1">**</ept>-rullemenuen i <bpt id="p2">**</bpt>Salgsordrelinjer<ept id="p2">**</ept> sektionen på siden <bpt id="p3">**</bpt>Salgsordre<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>This will open the <bpt id="p1">**</bpt>Maintain charges<ept id="p1">**</ept> page where the user can add a new line specific charge to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Siden <bpt id="p1">**</bpt>Vedligehold gebyrer<ept id="p1">**</ept>, hvor brugeren kan tilføje et nyt linjespecifikt gebyr til transaktionen, åbnes.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Additional features</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yderligere funktioner</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Editing charges on a POS sales transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Redigering af gebyrer på en POS-salgstransaktion</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>The <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation (142) should be added to the <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a user can view and edit or override any system-calculated or manually-created header or line-level charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Handlingen <bpt id="p1">**</bpt>Administrer gebyrer<ept id="p1">**</ept> (142) skal føjes til <bpt id="p2">[</bpt>POS-skærmlayoutet<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept>, så en bruger kan få vist og redigere eller tilsidesætte eventuelle gebyrer på linje- eller overskriftsniveau, der er beregnet af systemet eller oprettet manuelt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>If the operation is not added, users will not be able to adjust the value of the charges on the POS transaction, nor will they be able to view the details of the charges such as the type of charges code tied to the charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis handlingen ikke tilføjes, kan brugerne ikke justere værdien gebyret på POS-transaktionen, og de kan heller ikke se detaljerne for gebyrerne, f.eks. typen gebyrkode, der er knyttet til gebyret.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>On the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> page in POS, the user can view both header and line-level charges details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På siden <bpt id="p1">**</bpt>Administrer gebyrer<ept id="p1">**</ept> i POS kan brugeren kan få vist detaljer om gebyrer på både hoved- og linjeniveau.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The user can use the <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> function available on this page to make changes to the amount charged to a specific charges line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brugeren kan anvende <bpt id="p1">**</bpt>Rediger<ept id="p1">**</ept> funktionen, der er tilgængelig på denne side, til at foretage ændringer af det beløb, der lægges til en linje for specifikke gebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Once a charges line is overwritten manually, it will not be systematically recalculated unless the user initiates the <bpt id="p1">**</bpt>Recalculate charges<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når en linje for gebyrer overskrives manuelt, genberegnes den ikke systematisk, medmindre brugeren starter handlingen <bpt id="p1">**</bpt>Genberegn gebyrer<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>If the <bpt id="p1">**</bpt>Charge override reason code<ept id="p1">**</ept> has been configured on the <bpt id="p2">**</bpt>Retail parameters<ept id="p2">**</ept> setup page, the user will be prompted to provide a reason code when charges have been modified in the POS application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis <bpt id="p1">**</bpt>Årsagskode for tilsidesættelse af gebyr<ept id="p1">**</ept> er konfigureret på opsætningssiden <bpt id="p2">**</bpt>Detailparametre<ept id="p2">**</ept>, bliver brugeren bedt om at angive en årsagskode, når gebyrer er blevet ændret i POS-programmet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>If reason codes have been captured for overwritten charges, a new report is also available to review and audit these overrides.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis der er hentet årsagskoder for tilsidesatte gebyrer, findes der også en ny rapport til gennemsyn og overvågning af disse tilsidesættelser.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>The report can be found in <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Inquiries and reports <ph id="ph2">\&gt;</ph> Charge override history<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rapporten findes i <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Forespørgsler og rapporter <ph id="ph2">\&gt;</ph> Tilsidesættelseshistorik for gebyr<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Refunding charges on a POS return transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tilbagebetaling af gebyrer på en POS-returtransaktion</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>If the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is set to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>, the existing retail parameter for <bpt id="p3">**</bpt>Refund shipping charges<ept id="p3">**</ept> is no longer applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis parameteren <bpt id="p1">**</bpt>Brug avancerede automatiske gebyrer<ept id="p1">**</ept> er indstillet til <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>, gælder den eksisterende detailparameter for <bpt id="p3">**</bpt>Refunder forsendelsesgebyrer<ept id="p3">**</ept> ikke længere.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>To indicate which charges should be systematically refunded to a customer when using advanced auto-charges, ensure the related charges code has been configured as <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> setup page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Du kan angive, hvilke gebyrer der systematisk skal refunderes til en kunde, når der bruges avancerede automatiske gebyrer, skal du sikre, at koden for relaterede gebyrer er konfigureret som <bpt id="p1">**</bpt>Kan refunderes<ept id="p1">**</ept> på opsætningssiden <bpt id="p2">**</bpt>Gebyrkode<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Make sure that the settings have been synchronized to your Retail channel databases through distribution schedule processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sørg for, at indstillingerne er synkroniseret med detailkanalens databaser via behandling af distributionstidsplan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Refunding charges on a return order transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tilbagebetaling af gebyrer på en returordretransaktion</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Charges are not systematically refunded to <bpt id="p1">**</bpt>Return orders<ept id="p1">**</ept> created in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gebyrer refunderes ikke systematisk til <bpt id="p1">**</bpt>Returordrer<ept id="p1">**</ept>, der er oprettet i Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Users are required to select the <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> option when creating the <bpt id="p2">**</bpt>Return order<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brugerne skal vælge indstillingen <bpt id="p1">**</bpt>Kopiér gebyrer<ept id="p1">**</ept>, når de opretter deres <bpt id="p2">**</bpt>Returordre<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>If <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> is not selected, charges from the original sales transaction will not be automatically refunded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis <bpt id="p1">**</bpt>Kopiér gebyrer<ept id="p1">**</ept> er ikke markeret, refunderes gebyrer fra den oprindelige salgstransaktion ikke automatisk.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>If <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> is selected, all charges will be copied to the return order and the user can manually edit or remove any charges they do not want to have refunded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis <bpt id="p1">**</bpt>Kopiér gebyrer<ept id="p1">**</ept> er markeret, kopieres alle gebyrer til returordren, og brugeren kan manuelt redigere eller fjerne eventuelle gebyrer, som de ikke vil have refunderet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The call center return order process currently does not acknowledge the <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Callcenterets returordreproces kan i øjeblikket ikke bekræfte flaget <bpt id="p1">**</bpt>Kan refunderes<ept id="p1">**</ept> i <bpt id="p2">**</bpt>Gebyrkode<ept id="p2">**</ept>-opsætningen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Configuring POS receipts to show charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konfiguration af POS-kvitteringer til visning af gebyrer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>The following receipt elements have been added to the receipt line and footer to support the advanced auto-charges functionality.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Der er tilføjet følgende kvitteringselementer til kvitteringslinjen og -sidefoden til understøttelse af den avancerede automatiske gebyrfunktion.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source><bpt id="p1">**</bpt>Line Shipping Charges<ept id="p1">**</ept> – This line-level element can be used to recap specific charges codes that have been applied to the sales line.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Forsendelsesgebyrer for linje<ept id="p1">**</ept> – Dette element på linjeniveau kan bruges til at opsummere bestemt gebyrkoder, der er anvendt til salgslinjen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Only charges codes that have been flagged as <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> charges on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> page will be displayed here.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kun gebyrkoder, der er blevet afmærket som <bpt id="p1">**</bpt>Forsendelse<ept id="p1">**</ept>-gebyrer på siden <bpt id="p2">**</bpt>Gebyrkode<ept id="p2">**</ept>, vises her.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source><bpt id="p1">**</bpt>Line Other Charges<ept id="p1">**</ept> – This line-level element can be used to recap any non-shipping specific charge codes that have been applied to the sales line.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Andre gebyrer for linje<ept id="p1">**</ept> – Dette element på linjeniveau kan bruges til at opsummere ikke-forsendelsesgebyrkoder, der er anvendt på salgslinjen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>These are charges codes where the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> flag on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> page has not been enabled.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Disse er gebyrkoder, hvor flaget <bpt id="p1">**</bpt>Forsendelse<ept id="p1">**</ept> på siden <bpt id="p2">**</bpt>Gebyrkode<ept id="p2">**</ept> er ikke aktiveret.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source><bpt id="p1">**</bpt>Order Shipping Charges Details<ept id="p1">**</ept> – This footer-level element displays the descriptions of the charge codes applied to the order that have been flagged as <bpt id="p2">**</bpt>Shipping<ept id="p2">**</ept> charges on the <bpt id="p3">**</bpt>Charges code<ept id="p3">**</ept> setup page.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Oplysninger om forsendelsesgebyrer for ordre<ept id="p1">**</ept> – Dette element sidefodsniveau vises beskrivelserne af de gebyrkoder, der er anvendt på ordren, der er afmærket som <bpt id="p2">**</bpt>Forsendelse<ept id="p2">**</ept>-gebyr på opsætningssiden <bpt id="p3">**</bpt>Gebyrkode<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source><bpt id="p1">**</bpt>Order Shipping Charges<ept id="p1">**</ept> – This footer-level element shows the dollar value of the shipping-related charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Forsendelsesgebyrer for ordre<ept id="p1">**</ept> – Dette element på sidefodsniveau vises værdien i dollar af de forsendelsesrelaterede gebyrer.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source><bpt id="p1">**</bpt>Order Other Charges Details<ept id="p1">**</ept> – This footer-level element displays the description of the charges codes applied to the order that have not been flagged as shipping-related charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Oplysninger om andre gebyrer for ordre<ept id="p1">**</ept> – Dette element sidefodsniveau vises beskrivelsen af de gebyrkoder, der er anvendt på ordren, der ikke er mærket som forsendelsesrelaterede gebyrer.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source><bpt id="p1">**</bpt>Order Other Charges<ept id="p1">**</ept> – This footer-level element displays the dollar value of the other charges that are not shipping-related.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Andre gebyrer for ordre<ept id="p1">**</ept> – Dette element på sidefodsniveau vises værdien i dollar af de andre gebyrer, der ikke er forsendelsesrelaterede.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>It is recommended that the organization also add free text fields to the receipt footer, in order to define the areas where charges will be recapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Det anbefales, at organisationen også føjer fritekstfelter i kvitteringens sidefod for at definere de områder, hvor gebyrerne opsummeres.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Preventing charges from being calculated until the POS order is completed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Forhindre, at gebyrer beregnes, før POS-ordren er fuldført</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Some organizations may prefer to wait until the user has finished adding all of the sales lines to the POS transaction before calculating charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visse organisationer kan foretrække at vente på, at brugeren er færdig med at tilføje alle salgslinjerne til POS transaktionen før beregning af gebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>To prevent calculation of charges as items are added to the POS transaction, turn on the <bpt id="p1">**</bpt>Manual charge calculation<ept id="p1">**</ept> parameter in the <bpt id="p2">**</bpt>Functionality profile<ept id="p2">**</ept> used by the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">For at forhindre beregning af gebyrer i takt med at varer føjes til POS-transaktionen, skal du slå parameteren <bpt id="p1">**</bpt>Beregning af manuelt gebyr<ept id="p1">**</ept> i den <bpt id="p2">**</bpt>Funktionalitetsprofil<ept id="p2">**</ept>, der bruges i butikken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Enabling this parameter will require the POS user to use the <bpt id="p1">**</bpt>Calculate totals<ept id="p1">**</ept> operation when they have completed adding the products to the POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aktivering af denne parameter forudsætter, at POS-brugeren bruger handlingen <bpt id="p1">**</bpt>Beregn totaler<ept id="p1">**</ept> efter at have føjet produkterne til POS-transaktionen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>The <bpt id="p1">**</bpt>Calculate totals<ept id="p1">**</ept> operation will then trigger the calculation of any auto charges for the order header or lines as applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Handlingen <bpt id="p1">**</bpt>Beregn totaler<ept id="p1">**</ept> udløser derefter beregningen af de automatiske gebyrer for det/de relevante ordrehoved eller -linjer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Charges override reports</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rapporter over gebyrtilsidesættelser</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>If users manually override the calculated charges or add a manual charge to the transaction, this data will available for auditing in the <bpt id="p1">**</bpt>Charge Override History<ept id="p1">**</ept> report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis brugere tilsidesætter de beregnede gebyrer manuelt eller føjer et manuelle gebyr til transaktionen, er disse data tilgængelige til revidering i rapporten <bpt id="p1">**</bpt>Tilsidesættelseshistorik for gebyr<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>The report can be accessed from <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Inquiries and reports <ph id="ph2">\&gt;</ph> Charge Override History<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der er adgang til rapporten fra <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Forespørgsler og rapporter <ph id="ph2">\&gt;</ph> Tilsidesættelseshistorik for gebyr<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>It is important to note that the data needed for this report is imported from the channel database into HQ through the "P" distribution schedule jobs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Det er vigtigt at bemærke, at de data, der skal bruges til denne rapport, importeres fra kanaldatabasen til Headquarters via "P"-distributionsplanlægningsopgaver.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Therefore, information about overrides just performed in the POS may not be immediately available on this report until this job has uploaded the store transaction data into HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Derfor er oplysninger om tilsidesættelser, der netop er udført i POS, muligvis ikke umiddelbart tilgængelige i denne rapport, før dette job har overført butikkens transaktionsdata til Headquarters.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>