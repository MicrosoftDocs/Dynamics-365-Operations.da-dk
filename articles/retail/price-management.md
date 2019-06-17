<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="price-management.md" target-language="da-DK">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>price-management.9d0b0e.afa553fd0562b306f720f2a30c7f901db7ad1b3a.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>afa553fd0562b306f720f2a30c7f901db7ad1b3a</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>0fbfb9b0ab78c804f3931a083028d2ce313d6521</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/21/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\price-management.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail sales price management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Styring af detailsalgspriser</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the concepts for creating and managing sales prices in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I dette emne beskrives begreberne for oprettelse og styring af salgspriser i Microsoft Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Retail sales price management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail-salgsprisestyring</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides information about the process of creating and managing sales prices in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dette emne indeholder oplysninger om processen for oprettelse og styring af salgspriserne i Microsoft Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>It focuses on the concepts that are involved in this process, and on the effects of the various configuration options for sales prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der fokuseres på de begreber, der er involveret i processen, og om virkningerne af de forskellige konfigurationsindstillinger for salgspriser.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Terminology</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Terminologi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The following terms are used in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Følgende begreber anvendes i dette emne.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Term</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Periode</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Definition, usage, and notes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Definition, brug og noter</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pris</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The single unit amount that a product sells for in a point of sale (POS) client or on a sales order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Beløbet for én enhed, som et produkt sælges til, til en kunde gennem et salgssted (POS) eller en salgsordre.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In this topic, the term <bpt id="p1">*</bpt>price<ept id="p1">*</ept> always refers to the sales price, not the inventory price or cost price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I dette emne henviser begrebet <bpt id="p1">*</bpt>pris<ept id="p1">*</ept> altid til salgsprisen, ikke lagerprisen eller kostprisen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Base price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Basispris</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The price that is set in the <bpt id="p1">**</bpt>Price<ept id="p1">**</ept> field on a released product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Den pris, der er angivet i feltet <bpt id="p1">**</bpt>Pris<ept id="p1">**</ept> for et frigivet produkt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Trade agreement price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pris i samhandelsaftale</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The price that is set on a product or variant by using a trade agreement of the <bpt id="p1">**</bpt>Price (sales)<ept id="p1">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Den pris, der er angivet for et produkt eller en variant gennem en samhandelsaftale af typen <bpt id="p1">**</bpt>Pris (salg)<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Best price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bedste pris</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>When more than one price or discount can be applied to a product, the smallest price amount and/or the largest discount amount that produces the lowest possible net amount that the customer must pay.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når mere end én pris eller rabat kan gælde for et produkt, er prisen det mindste prisbeløb og/eller det største rabatbeløb, som giver det laveste mulige nettobeløb, som kunden skal betale.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>In this topic, the concept of best price is always referred to as "the best price."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I dette emne betegnes den bedste pris altid "den bedste pris".</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>This best price differs from and should not be confused with the <bpt id="p1">**</bpt>Best price<ept id="p1">**</ept> enumeration value for a discount's concurrency mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Den bedste pris adskiller sig fra og bør ikke forveksles med tællerværdien for <bpt id="p1">**</bpt>Bedste pris<ept id="p1">**</ept> for en samtidig rabattilstand.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Price groups</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prisgrupper</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Price groups are at the heart of price and discount management in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prisgrupper er omdrejningspunktet for styring af priser og rabatter i Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Price groups are used to assign prices and discounts to retail entities (that is, channels, catalogs, affiliations, and loyalty programs).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prisgrupper anvendes til at tildele priser og rabatter til detailenheder (dvs. kanaler, kataloger, tilknytninger og fordelskundeprogrammer).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Because price groups are used for all pricing and discounts, it's very important that you plan how you will use them before you start.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eftersom prisgrupper bruges til alle priser og rabatter, er det vigtigt, at du planlægger, hvordan du vil bruge dem, før du starter.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>By itself, a price group is just a name, a description, and, optionally, a pricing priority.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I sig selv er en prisgruppe blot et navn, en beskrivelse og eventuelt en prioritet for prissætning.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The main point to remember about price groups is that they are used to manage the many-to-many relationships that discounts and prices have with retail entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Det vigtigste at huske om prisgrupper er, at de bruges til at administrere de utallige relationer, rabatter og priser har med detailenheder.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The following illustration shows how price groups are used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I følgende illustration vises, hvordan prisgrupperne bruges.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In this illustration, notice that "Price group" is literally at the center of pricing and discount management.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I denne illustration skal du bemærke, at "Prisgruppe" bogstaveligt talt er placeret midt i administrationen af prissætning og rabat.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The retail entities that you can use to manage differential prices and discounts are on the left, and the actual price and discount records are on the right.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De detailenheder, du kan bruge til at administrere differentierede priser og rabatter, er placeret til venstre, og de faktiske pris- og rabatposter er placeret til højre.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">![</bpt>Price groups<ept id="p1">]</ept><bpt id="p2">(./media/PriceGroups.png "</bpt>Price groups<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>Prisgrupper<ept id="p1">]</ept><bpt id="p2">(./media/PriceGroups.png "</bpt>Prisgrupper<ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>When you create price groups, you should not use a single price group for multiple types of retail entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når du opretter prisgrupper, bør du ikke bruge samme prisgruppe til flere typer detailenheder.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Otherwise, it can be difficult to determine why a specific price or discount is being applied to a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I modsat fald kan det være vanskeligt at afgøre, hvorfor en bestemt pris eller rabat anvendes til en transaktion.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>As the red dashed line in the illustration shows, Retail does support the core Microsoft Dynamics 365 functionality of a price group that is set directly on a customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når den røde stiplede linje i illustrationen vises, understøtter Retail kernefunktionaliteten i Microsoft Dynamics 365 for en prisgruppe, som er indstillet direkte for en debitor.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>However, in this case, you get only sales price trade agreements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I så fald får du imidlertid kun samhandelsaftaler om salgspris.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If you want to apply customer-specific prices, we recommend that you not set price groups directly on the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du vil anvende kundespecifikke priser, anbefales det, at du ikke angiver prisgrupper direkte for debitoren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Instead, you should use affiliations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Du skal i stedet bruge tilknytninger.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The following sections provide more information about the retail entities that you can use to set distinct prices when the price groups are used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De følgende afsnit indeholder flere oplysninger om de detailenheder, du kan bruge til at angive specifikke priser, når der anvendes prisgrupper.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The configuration of prices and discounts for all these entities is a two-step process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konfigurationen af priser og rabatter for disse enheder er en proces i to trin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>These steps can be done in either order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Disse trin kan udføres i vilkårlig rækkefølge.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>However, the logical order is to set the price groups on the entities first, because this step is likely to be a one-time setup that is done during implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Den logiske rækkefølge er dog først at angive prisgrupperne for enhederne, fordi dette trin ofte kun skal udføres en enkelt gang under implementeringen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Then, as prices and discounts are created, you can set the price groups on those prices and discounts individually.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Derefter, når der oprettes priser og rabatter, kan du oprette prisgrupper for de enkelte priser og rabatter.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Channels</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kanaler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In the retail industry, it's very typical to have different prices in different channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Det er meget almindeligt at have forskellige priser i forskellige kanaler i detailbranchen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>The two primary factors that affect channel-specific prices are costs and local market conditions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De to primære faktorer, der påvirker kanalspecifikke priser, er omkostninger og lokale markedsforhold.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>Costs<ept id="p1">**</ept> – The farther away a channel is from the product source, the more it costs to stock a product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Omkostninger<ept id="p1">**</ept> – Jo længere væk en kanal er fra produktkilden, jo mere koster det at lagerføre et produkt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>For example, fresh produce has a limited shelf life and specific production requirements (for example, a growing season).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Friske produkter har f.eks. en begrænset hyldelevetid og specifikke produktionsbetingelser (f.eks. en enkelt vækstsæson).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>During the winter, fresh lettuce likely costs more in northern climates than in southern climates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Om vinteren koster frisk salat sandsynligvis mere i det nordlige klima end i det sydlige klima.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>If you're setting prices for channels over a large geographical area, you will probably want to set different prices in different channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du angiver priser for kanaler over et stort geografisk område, vil du sandsynligvis angive forskellige priser for forskellige kanaler.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source><bpt id="p1">**</bpt>Local market conditions<ept id="p1">**</ept> – A store that has a direct competitor across the street will be much more price-sensitive than a store that doesn't have a direct competitor nearby.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Lokale markedsbetingelser<ept id="p1">**</ept> – Et lager, som har en direkte konkurrent på den anden side af gaden, vil være meget mere prisfølsomt end en butik, som ikke har en direkte konkurrent i nærheden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Affiliations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tilhørsforhold</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The general definition of an affiliation is a link to or association with a group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Den generelle definition af en tilknytning er et hyperlink til eller en tilknytning til en gruppe.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>In Retail, affiliations are groups of customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I Retail er tilknytninger grupper af debitorer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Affiliations are a much more flexible tool for customer pricing and discounts than the core Microsoft Dynamics 365 concept of customer groups and discount groups.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tilknytninger er et meget fleksibelt værktøj for priser og rabatter for debitorer end den centrale opfattelse af debitorgrupper og rabatgrupper i Microsoft Dynamics 365.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>First, an affiliation can be used for both prices and discounts, whereas non-retail pricing has a different group for each type of discount and price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Først og fremmest kan en tilknytning bruges til både priser og rabatter, mens ikke-detailpriser har en ny gruppe for hver rabat- og pristype.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Next, a customer can belong to multiple affiliations but can belong to only one non-retail pricing group of each type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Derefter kan en debitor tilhøre flere tilknytninger, men de kan kun tilhøre én ikke-detailprisgruppe for hver type.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Finally, although affiliations can be set up so that they are linked to a customer, they don't have to be.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Endelig kan der konfigureres tilknytninger til en kunde, selvom det ikke er nødvendigt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>An ad-hoc affiliation can be used for anonymous customers at the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En ad hoc-tilknytning kan bruges til anonyme debitorer på salgsstedet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>A typical example of an anonymous affiliation discount is a senior or student discount, where a customer can receive a discount just by showing a group membership card.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Et typisk eksempel på rabat på en anonym tilknytning er rabat for ældre eller studerende, hvor en debitor kan modtage en rabat ved blot at fremvise et medlemskort for gruppen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Although affiliations are most often associated with discounts, you can also use them to set differential pricing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Selvom tilknytninger oftest omhandler rabatter, kan du også bruge dem til at angive differentieret prissætning</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>For example, when a retailer sells to an employee, it might want to change the selling price instead of applying a discount on top of the regular price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når en forhandler f.eks. sælger til en medarbejder, vil forhandleren muligvis ændre salgsprisen i stedet for at anvende en rabat på den almindelige pris.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>As another example, a retailer that sells to both consumer customers and business customers might offer business customers better prices, based on their purchasing volume.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Et andet eksempel er, når en forhandler, der sælger til både forbrugere og virksomheder, tilbyde virksomheder bedre priser, der er baseret på volumen af deres indkøb.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Affiliations enable both these scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tilknytninger muliggør begge disse scenarier.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Loyalty programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fordelskundeprogrammer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>In relation to prices and discounts, loyalty programs are basically just an affiliation that has a special name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I forbindelse med priser og rabatter er fordelskundeprogrammer grundlæggende blot en tilknytning med en særlig betegnelse.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Both prices and discounts can be set for a loyalty program, just as they can be set for an affiliation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Både priser og rabatter kan angives for et fordelskundeprogram, ligesom de kan angives for en tilknytning.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>However, the way that customers get loyalty pricing during a transaction or order differs from the way that they get affiliation pricing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Den måde, hvorpå debitorer får fordelskundepriser under en transaktion eller ordre, adskiller sig dog fra den måde, hvorpå de får tilknytningspriser.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Customers can get loyalty pricing only if a loyalty card is added to a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kunder kan kun få fordelskundepriser, hvis et fordelskundekort føjes til en transaktion.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>When a loyalty card is added to a transaction, the loyalty program is also added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når et fordelskundekort føjes til en transaktion, tilføjes fordelskundeprogrammet også.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>The loyalty program then enables special prices and discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fordelskundeprogrammet muliggør derefter særlige priser og rabatter.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Loyalty programs can have multiple tiers, and the discounts can differ for different tiers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fordelskundeprogrammer kan have flere niveauer, og rabatterne kan være forskellige for forskellige niveauer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>In this way, retailers can give frequent customers larger rewards without having to manually put those customers into a special group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På denne måde kan detailhandlere give hyppige debitorer større fordele uden at skulle placere dem manuelt i en specialgruppe.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Loyalty programs have additional functionality besides prices and discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kundefordelsprogrammer omfatter yderligere funktioner ud over priser og rabatter.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>However, from the perspective of pricing and discounts, they are the same as affiliations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I forhold til priser og rabatter er de dog det samme som tilknytninger.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Catalogs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kataloger</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Some retailers use physical or virtual catalogs to market products to, and price them for, focused groups of customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nogle detailhandlere bruger fysiske eller virtuelle kataloger til at markedsføre og prissætte produkter til målrettede grupper af debitorer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>As part of their business model to target marketing via a catalog, these retailers can set differential prices on their various catalogs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Som en del af deres forretningsmodel for at målrette markedsføringen gennem et katalog, kan disse detailhandlere angive differentierede priser i deres forskellige kataloger.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Microsoft Dynamics 365 supports this capability by letting you define catalog-specific discounts and prices, just as you can define channel-specific or affiliation-specific discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 understøtter denne funktion ved at lade dig definere katalogspecifikke rabatter og priser, ligesom du kan definere kanalspecifikke eller tilknytningsspecifikke rabatter.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>When you edit a catalog, you can associate price groups with the catalog, just as you can associate them with a channel, affiliation, or loyalty program.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når du redigerer et katalog, kan du kan knytte prisgrupper til kataloget, ligesom du kan knytte dem til en kanal, en tilknytning eller et fordelskundeprogram.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Best practices for price groups</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bedste praksis for prisgrupper</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Don't use a price group for multiple retail entity types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brug ikke en prisgruppe til flere detailenhedstyper.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Instead, use one set of price groups for channels, a different set of price groups for affiliations or loyalty programs, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I stedet anvendes et sæt prisgrupper for kanaler, et sæt prisgrupper for tilknytninger eller fordelskundeprogrammer osv.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>You can use a prefix or suffix in the name of the price group to visually group the various types of price groups that you're using.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Du kan bruge et præfiks eller suffiks i navnet på prisgruppen for at gruppere de forskellige prisgruppetyper visuelt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Avoid setting price groups directly on a customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Undlad at angive prisgrupper direkte for en debitor.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Instead, use an affiliation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Anvend i stedet en tilknytning.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>In this way, you can assign all types of prices and discounts to customers, not just sales price trade agreements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På denne måde kan du tildele alle typer priser og rabatter til debitorer, ikke blot samhandelsaftaler for salgspriser.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Pricing priority</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prioritet for prissætning</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>By itself, a pricing priority is just a number and a description.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I sig selv er en prioritet for prissætning blot et tal og en beskrivelse.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Pricing priorities can be applied to price groups, or they can be applied directly to discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prioriteter for prissætning kan anvendes til prisgrupper, eller de kan anvendes direkte til rabatter.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>When pricing priorities are used, they let a retailer override the principle of the best price by controlling the order in which prices and discounts are applied to products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når der anvendes prioriteter for prissætning, kan en detailhandler tilsidesætte princippet for bedste pris ved at styre rækkefølgen for tildeling af priser og rabatter til produkter.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>A larger pricing priority number is evaluated before a lower pricing priority number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Et højere prioritetsnummer for prissætning evalueres før et lavere prioritetsnummer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Additionally, if a price or discount is found at any priority number, all prices or discounts that have lower priority numbers are ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Derudover ignores alle priser og rabatter, der har lavere prioritetsnumre, hvis der er placeret en pris eller rabat ved et prioritetsnummer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>The price and a discount can come from two different pricing priorities, because pricing priorities apply to prices and discounts independently.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prisen og en rabat kan stamme fra to forskellige priser prioriteter for prissætning, fordi prioriteterne gælder uafhængigt af priser og rabatter.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>To use pricing priority for prices, you must assign a pricing priority to a price group and then create a sales price trade agreement for that price group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du vil bruge prioriteter for prissætning til priser, skal du tildele en prioritet til en prisgruppe og derefter oprette en samhandelsaftale for salgspris for den pågældende prisgruppe.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The pricing priority feature was introduced to support the scenario where a retailer wants to apply higher prices in a specific set of stores.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Funktionen til prioriteter for prissætning blev indført for at understøtte det scenarie, hvor en detailhandler ønsker at anvende højere priser i et bestemt række af butikker.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>For example, a retailer has defined regional prices for the east coast of the United States but wants higher prices for some products in New York City stores, because it costs more to sell some products in the city, and/or because the local market will bear a higher price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Et eksempel er, når en detailhandler har defineret regionale priser for den amerikanske østkyst i USA, men ønsker højere priser for visse produkter i butikkerne i New York City, fordi det koster mere at sælge visse produkter i byen, og/eller fordi en højere pris er gælder på det lokale marked.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>As was described in the "Best price" section of this topic, the retail pricing engine typically selects the lower of two prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Som beskrevet i afsnittet "Bedste pris" i dette emne, vælger programmet for detailprissætning typisk den mindste af to priser.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Therefore, the retailer is usually prevented from using the higher of two prices in a store that has both the East coast and New York price groups.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Derfor forhindres detailhandleren normalt i at bruge den højeste af to priser i en butik, der har både har prisgrupper for østkysten og i New York.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>To resolve this issue before the pricing priority feature was introduced, the retailer had to define prices for every product two times and not assign both price groups.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">For at løse problemet, inden funktionen for prioriteter for prissætning blev indført, måtte detailhandleren definere priser for hvert produkt to gange og ikke tildele prisen til begge prisgrupper.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Alternatively, the retailer had to create extra price groups to isolate the products that have higher prices from products that have the usual, lower prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Detailhandleren kunne også oprette ekstra prisgrupper for at isolere de produkter, der har højere priser, fra produkter med de normale, lavere priser.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>However, the pricing priority feature lets the retailer create a pricing priority for store prices that is higher than the pricing priority for regional prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Funktionen til prioriteter for prissætning lader imidlertid detailhandleren oprette en prioritet for butikkens priser, som er højere end prioriteten for de regionale priser.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Alternatively, the retailer can create a pricing priority just for store prices and leave regional prices at the default pricing priority, which is 0 (zero).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Forhandleren kan også oprette en prioritet for prissætning, der kun gælder for butikspriser, mens de regionale priser får standardprioriteten for prissætning, dvs. 0 (nul).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Both setups help guarantee that store prices will always be used before regional prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Begge opsætninger er med til at sikre, at butikspriser altid bruges før de regionale priser.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Pricing priority example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksempel på prioriteter for prissætning</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Let's look at an example where store prices override other prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lad os se et eksempel, hvor butikspriser tilsidesætter andre priser.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>A national retailer sets most prices per region, and it has four regions: North east, South east, Mid-west and West.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En national detailhandler angiver de fleste priser pr. område, hvilket omfatter fire områder: Nordøst, Sydøst, Midtvest og Vest.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>It has identified several high-cost markets that can support higher prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Den har identificeret flere markeder med høje omkostninger, som kan bære højere priser.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>These markets are in New York City, Chicago, and the San Francisco Bay area.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Disse markeder er i New York City, Chicago og området ved San Francisco Bay.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>For this example, we will drill into the North east region.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I dette eksempel vil vi dykke ned i den nordøstlige region.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Store 1 is in Boston, and store 2 is in Manhattan.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Butik 1 er i Boston, og butik 2 er i Manhattan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>For the Boston store, two price groups are linked to the channel: North East and Store 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">For butikken i Boston er der tilknyttet to prisgrupper til kanalen: Nordøst og Butik 1.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>For the Manhattan store, three price groups are linked to the channel: North East, NYC, and Store 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">For butikken i Manhatten er der tilknyttet tre prisgrupper til kanalen: Nordøst, NYC og Butik 2.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>The retailer sets up two pricing priorities: High cost has a priority number of 5, and Store prices has a priority number of 10.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Detailhandleren konfigurerer to prioriteter for prissætning: Høje omkostninger har prioritetsnummeret 5, og butikspriser for butikken har prioritetsnummeret 10.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>(Remember that, by default, the pricing priority is 0 <ph id="ph1">\[</ph>zero<ph id="ph2">\]</ph>, and a price or discount that has a higher priority number is used before a price or discount that has a lower priority number.) For the North East price group, the pricing priority is left at the default value of <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (zero).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(Husk, at som standard er prioriteten for prissætning 0 <ph id="ph1">\[</ph>nul<ph id="ph2">\]</ph>, og en pris eller rabat med et højere prioritetsnummer bruges før en pris eller rabat med et lavere prioritetsnummer.) For prisgruppen Nordøst beholder prioriteten for prissætning standardværdien på <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (nul).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>For the NYC price group, the pricing priority is set to <bpt id="p1">**</bpt>5<ept id="p1">**</ept>, because New York City is a high-cost market.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">For prisgruppen NYC er prioriteten for prissætning indstillet til <bpt id="p1">**</bpt>5<ept id="p1">**</ept>, da New York City er et marked med høje omkostninger.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>For the Store 1 and Store 2 price groups, the pricing priority is set to <bpt id="p1">**</bpt>10<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">For prisgrupperne Butik 1 og Butik 2 er prioriteten for prissætning indstillet til <bpt id="p1">**</bpt>10<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Two products that the retailer sells are product 1, a commodity T-shirt, and product 2, brand-specific fashion jeans.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">To produkter, der sælges af detailhandleren, er produkt 1, en T-shirt i basisudgave, og produkt 2, et par modejeans med varemærke.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Product</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Produkt</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>North East price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pris for Nordøst</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>NYC price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pris for NYC</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Store price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Butikspris</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>T-shirt</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">T-shirt</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>$15</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$15</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Not set</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ikke angivet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Not set</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ikke angivet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Fashion jeans</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Modejeans</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>$50</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$50</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>$70</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$70</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Not set</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ikke angivet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The T-shirt sells for the same price (that is, $15) at both the Boston and Manhattan stores, because only one price is set in the North East price group that is linked to both channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">T-shirten sælges for den samme pris (dvs. $15) i både Boston- og Manhattan-butikkerne, fordi kun én pris er angivet for prisgruppen Nordøst, der er tilknyttet begge kanaler.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The fashion jeans sell for $50 in the Boston store, because that price is the only price that is available in that store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">De måde cowboybukser sælger for $50 i butikken Boston, fordi denne pris er den eneste pris, der er tilgængelige i butikken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>However, in the Manhattan store, two prices are available: $50 and $70.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I Manhattan-butikken gælder imidlertid to priser: $50 og $70.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Because the pricing priority of 5 for the NYC price group is higher than the pricing priority of 0 (zero) for the North East price group, the price will be rung up as $70 in the POS system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Da prioriteten for prissætning på 5 for prisgruppen NYC er højere end prioriteten for prissætning på 0 (nul) for prisgruppen Nordøst, skal prisen angives som $70 i POS-systemet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>For each pricing priority, a full pass through the logic for the retail pricing engine is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">For hver prioritet for prissætning kræves en fuld gennemgang af logikken for programmet for detailprissætningen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Therefore, to help maintain the performance of the price and discount calculation, you should use pricing priorities sparingly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">For at forbedre performance for beregningen af pris og rabat, skal du derfor bruge prioriteter for prissætning med måde.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Types of prices</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pristyper</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>In Microsoft Dynamics 365, you can set the price of a product in three places:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I Microsoft Dynamics 365 kan du angive prisen på et produkt tre steder:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Directly on the product (base price)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Direkte for produktet (basisprisen)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>In a sales price trade agreement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I en samhandelsaftale for salgspriser</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>In a price adjustment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I en prisjustering</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>The base price and trade agreement price are part of core Microsoft Dynamics 365, and are available even if you don't use Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Basisprisen og samhandelsaftaleprisen er en central del af Microsoft Dynamics 365 og er tilgængelige, selvom du ikke bruger Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>The price adjustment functionality is available only in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Funktionen til prisjustering er kun tilgængelig i Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>The next section provides more information about each of these options for setting prices and explains how the options work together.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Næste afsnit indeholder flere oplysninger om hver af disse indstillinger for indstilling af priser og beskriver, hvordan indstillingerne arbejder sammen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Setting prices</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Indstilling af priser</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Base price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Basispris</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>The easiest place to set the price for a product is directly on the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Det sted, der er lettest at angive prisen for et produkt, er direkte for produktet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>The value that you set directly on a product is often referred to as the base price for the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Den værdi, du angiver direkte for et produkt, kaldes ofte basisprisen for produktet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>You set the base price in the <bpt id="p1">**</bpt>Price<ept id="p1">**</ept> field on the <bpt id="p2">**</bpt>Sell<ept id="p2">**</ept> tab of the <bpt id="p3">**</bpt>Released product details<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Du kan angive basisprisen i feltet <bpt id="p1">**</bpt>Pris<ept id="p1">**</ept> på fanen <bpt id="p2">**</bpt>Sælg<ept id="p2">**</ept> på siden <bpt id="p3">**</bpt>Frigivne produktdetaljer<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>The value that you enter is in the company currency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Værdier angives i virksomhedens valuta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>By default, the price is for a quantity of 1 of the unit of measure (UoM) that is set in the <bpt id="p1">**</bpt>Unit<ept id="p1">**</ept> field on the <bpt id="p2">**</bpt>Sell<ept id="p2">**</ept> tab. The actual price per unit of a product is based on the UoM, the price quantity, and the currency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prisen gælder som standard for et antal på 1 for måleenheden (UoM), der er angivet i feltet <bpt id="p1">**</bpt>Enhed<ept id="p1">**</ept> på fanen <bpt id="p2">**</bpt>Sælg<ept id="p2">**</ept>. Den faktiske pris pr. enhed af et produkt er baseret på måleenhed, prisantal og valuta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>If a product has one price for everyone, the base price offers the most efficient way to manage the price of that product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis et produkt har én pris for alle, udgør basisprisen den mest effektive metode til at administrere prisen på produktet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Even if you use trade agreements to set prices, you might also set the base price on a product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Selvom du bruger samhandelsaftaler til at angive priser, kan du også angive basisprisen for et produkt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Then, if you don't use an <bpt id="p1">**</bpt>All<ept id="p1">**</ept> trade agreement, you have a fallback price that is used when no trade agreement applies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du ikke bruger en samhandelsaftale af typen <bpt id="p1">**</bpt>Alle<ept id="p1">**</ept>, du har en reservepris, der bruges, når ingen samhandelsaftale er gældende.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>If a retail channel's currency differs from the company currency, the base price in that retail channel is determined by using currency conversion on the price that is set on the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis en detailkanals valuta afviger fra firmavalutaen, fastlægges basisprisen i den pågældende detailkanal ved hjælp af valutaomregning af den pris, der er angivet for produktet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Although the price unit isn't a common retail scenario, the retail pricing engine supports it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Selvom prisenheden ikke er et almindeligt scenarie for detailhandel, understøttes den af programmet for prissætning i detailhandlen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>If the price unit is set to a value other than <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (zero), the price per unit equals Price ÷ Price unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis prisenheden er indstillet til en anden værdi end <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (nul), er prisen pr. enhed lig med Pris ÷ Prisenhed.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>For example, if a product's price is $10.00, and the price unit is 50, the price for a quantity of 1 is $0.20 (= $10.00 ÷ 50).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis et produkts pris f.eks. er $10,00, og Prisenheden er 50, er prisen for et antal på 1 lig med $0,20 (= $10,00 ÷ 50).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Sales price trade agreement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Samhandelsaftale for salgspriser</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>By using the trade agreement journal, you can create sales price trade agreements for each product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ved hjælp af en samhandelsaftalekladde kan du oprette samhandelsaftaler om salgspriser for hvert produkt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>In Microsoft Dynamics 365, there are three customer scopes for sales price trade agreements: <bpt id="p1">**</bpt>Table<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Group<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>All<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I Microsoft Dynamics 365 findes der tre forskellige omfang af debitorer for samhandelsaftaler for salgspriser: <bpt id="p1">**</bpt>Tabel<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Gruppe<ept id="p2">**</ept> og <bpt id="p3">**</bpt>Alle<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>The customer scope determines the customers that a given sales price trade agreement applies to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Omfanget af debitorer bestemmer, hvilke debitorer en bestemt samhandelsaftale for salgspriser gælder for.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>A <bpt id="p1">**</bpt>Table<ept id="p1">**</ept> sales price trade agreement is for a single customer that is set directly on the trade agreement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En samhandelsaftale for salgspriser af typen <bpt id="p1">**</bpt>Tabel<ept id="p1">**</ept> gælder for en enkelt kunde, som er angivet direkte i samhandelsaftalen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>This scenario isn't a typical retail business-to-consumer (B2C) scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dette scenario er ikke et typisk detailscenarie for salg fra virksomheder til forbrugere (B2C).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>However, if it occurs, the retail pricing engine uses <bpt id="p1">**</bpt>Table<ept id="p1">**</ept> trade agreements when it determines price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis det forekommer, anvender programmet for detailprissætning samhandelsaftaler af typen <bpt id="p1">**</bpt>Tabel<ept id="p1">**</ept> til at fastlægge prisen..</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>A <bpt id="p1">**</bpt>Group<ept id="p1">**</ept> sales price trade agreement is the type that is most often used with retail functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En samhandelsaftale for salgspriser af typen <bpt id="p1">**</bpt>Gruppe<ept id="p1">**</ept> er den type, der bruges oftest til detailscenarier.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Outside Retail, <bpt id="p1">**</bpt>Group<ept id="p1">**</ept> sales price trade agreements are for a simple customer group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Uden for Retail gælder samhandelsaftaler for salgspriser af typen <bpt id="p1">**</bpt>Gruppe<ept id="p1">**</ept> en simpel debitorgruppe.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>However, in Retail, the concept of a customer group has been extended so that it's a more generic retail price group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I Retail er begrebet for en debitorgruppe udvidet til en mere generel detailprisgruppe.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>A price group can be linked to a retail channel, affiliation, loyalty program, or catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En prisgruppe kan knyttes til en detailkanal, en tilknytning, et fordelskundeprogram eller et katalog.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>For detailed information about price groups, see the "Price groups" section earlier in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Detaljerede oplysninger om prisgrupper finder du i afsnittet "Prisgrupper" tidligere i dette emne.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>A trade agreement price is always used before the base price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En samhandelsaftale for priser bruges altid før basisprisen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Price adjustment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prisjustering</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>As the name implies, a price adjustment is used to modify the price that was either set directly on the product or set by using a trade agreement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Som navnet antyder, anvendes en prisjustering til at ændre prisen, som enten er angivet direkte for produktet eller ved hjælp af en samhandelsaftale.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>A price adjustment can be used only to lower the price, not raise it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En prisjustering kan kun bruges til at sænke prisen, ikke til at hæve den.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>A price adjustment is the recommended way for retailers to create, track, and manage price markdowns for their products over time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En prisjustering er den anbefalede metode for detailhandlere til at oprette, spore og administrere prisreduktioner for produkterne over tid.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>There are three types of price adjustments: percentage off, amount off, and price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der findes tre typer prisjusteringer: rabatprocent, rabatbeløb og pris.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>A price adjustment of the percentage off or amount off type is always applied to a sale transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En prisjustering af typen rabatprocent eller rabatbeløb anvendes altid til en salgstransaktion.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>However, a price adjustment of the price type is applied only if the adjusted price is less than the price that was set by using the base price or trade agreement price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En prisjustering af pristypen anvendes dog kun, hvis den justerede pris er mindre end den pris, der blev angivet ved hjælp af basisprisen eller samhandelsaftalen for pris.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Therefore, if the price that is set in a price adjustment is more than the unadjusted price, the price adjustment isn't used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis den pris, der er angivet i en prisjustering er større end prisen inden justeringen, anvendes prisjusteringen således ikke.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Determining price for a product in a transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fastlæggelse af prisen for et produkt i en transaktion</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>The calculation of the price and discount on a transaction uses the principle of finding the best price for the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Beregningen af prisen og rabatten for en transaktion følger princippet for at finde den bedste pris for debitoren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>According to this principle, if more than one price is found, the lowest price is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I overensstemmelse med dette princip bruges den laveste pris, hvis der findes mere end en pris.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Additionally, the combination of discounts that produces the largest discount amount for the whole transaction is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Derudover anvendes den kombination af rabatter, der giver det største rabatbeløb for hele transaktionen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>In some cases, a smaller discount must be used on a single product, so that additional discounts can be applied to other products in the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I nogle tilfælde skal der anvendes en mindre rabat på et enkelt produkt, så yderligere rabatter kan anvendes til andre produkter i transaktionen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>The only exception to the principle of finding the best price for the customer is an option for mix-and-match least-expensive discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Den eneste undtagelse fra princippet om at finde den bedste pris for debitoren er muligheden for at blande og sammensætte rabatter til den laveste slutrabat.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>This option enables least-expensive discounts that favor the retailer when products are selected and grouped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Denne mulighed sikrer de billigste rabatter til fordel detailhandleren, når produkterne vælges og grupperes.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Therefore, when a transaction includes more products than are required to qualify for the least-expensive discount, the retail pricing engine selects the products that produce the smallest possible discount amount for the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når en transaktion inkluderer flere produkter, end der kræves for at opnå den billigste rabat, vælger programmet for detailprissætning de produkter, der resulterer i det mindste mulige rabatbeløb for debitoren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>The retail pricing engine returns three prices for every product: the base price, the trade agreement price, and the active price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Programmet for detailprissætning returnerer tre priser for hvert produkt: basisprisen, samhandelsaftalens pris og den aktive pris.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>The base price is just the property on the product and is the same for everyone everywhere.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Basisprisen er blot en fast egenskab for produktet og er den samme for alle overalt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>On the sales price trade agreement, if the <bpt id="p1">**</bpt>Find next<ept id="p1">**</ept> option is set to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>, the lowest price that is found for applicable sales price trade agreements is used as the trade agreement price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis indstillingen <bpt id="p1">**</bpt>Find næste<ept id="p1">**</ept> er angivet til <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>, bruges den laveste pris, der findes for de gældende samhandelsaftaler for salgspriser som samhandelsaftalens pris.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Trade agreements can be found by using price groups or the <bpt id="p1">**</bpt>ALL<ept id="p1">**</ept> account code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Samhandelsaftaler findes ved at bruge prisgrupper eller kontokoden <bpt id="p1">**</bpt>Alle<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>Alternatively, trade agreements can be assigned directly to a customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Samhandelsaftalerne kan også tildeles direkte til en debitor.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>If the <bpt id="p1">**</bpt>Find next<ept id="p1">**</ept> option is set to <bpt id="p2">**</bpt>No<ept id="p2">**</ept>, the first trade agreement price that is found is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis indstillingen <bpt id="p1">**</bpt>Find næste<ept id="p1">**</ept> er angivet til <bpt id="p2">**</bpt>Nej<ept id="p2">**</ept>, bruges den pris i samhandelsaftalen, som findes først.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>If no sales price trade agreements are found, then the trade agreement price is set equal to the base price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis der ingen samhandelsaftaler for salgspriser findes, angives samhandelsaftalens pris til basisprisen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>The active price is calculated by taking the trade agreement price and applying the largest price adjustment that applies to the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Den aktive pris beregnes ved at bruge samhandelsaftalens pris og anvende den største prisjustering, der gælder for produktet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>If no price adjustments are found, or if the calculated active price is more than the trade agreement price, the active price is set equal to the trade agreement price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis der ingen prisjusteringer findes, eller hvis den beregnede aktive pris er højere end samhandelsaftalens pris, indstilles den aktive pris til samhandelsaftalens pris.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Remember that you can't raise the price of a product by using a price adjustment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Husk, at du ikke kan hæve prisen på et produkt ved hjælp af en prisjustering.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>The applicable price adjustments can be found only by using price groups that are assigned to a channel, catalog, affiliation, or loyalty program.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gældende prisreguleringer finder du ved hjælp at bruge prisgrupper, der er knyttet til en kanal, et katalog, en tilknytning eller et fordelskundeprogram.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Category price rules</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Regler for kategoripriser</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>The category price rules feature in Retail gives you an easy way to create new trade agreements for all the products in a category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Funktionen for kategoriprisregler i Retail giver dig en nem metode til at oprette nye samhandelsaftaler for alle produkter i en kategori.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>This feature also lets you automatically find existing trade agreements for the products in the category and expire them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Denne funktion gør det også muligt automatisk at finde eksisterende samhandelsaftaler for produkterne i kategorien og ophæve dem.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>When you select the option to expire existing trade agreements, the system creates a new trade agreement journal for the products in the category that have an active trade agreement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når du vælger indstillingen for at ophæve eksisterende samhandelsaftaler, opretter systemet en ny samhandelsaftalekladde for produkterne i kategorien, der har en aktiv samhandelsaftale.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>However, the journal must be manually posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kladden skal dog bogføres manuelt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Additionally, the category price rules can find existing trade agreements only if you're using the same price rule (that is, if you create a new price rule that uses the same category that was before).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kategoriprisregler kan desuden finde eksisterende samhandelsaftaler, hvis du bruger den samme prisregel (dvs, hvis du opretter en ny prisregel, som anvender den samme kategori som før).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>If you aren't using the same price rule, the existing trade agreements won't be expired.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du ikke bruger den samme prisregel, ophæves de eksisterende samhandelsaftaler ikke.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>The prices can be increased or decreased by using the <bpt id="p1">**</bpt>Price rule<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Price basis<ept id="p2">**</ept> fields of the category price rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Priserne kan hæves eller sænkes ved hjælp af felterne <bpt id="p1">**</bpt>Prisregel<ept id="p1">**</ept> og <bpt id="p2">**</bpt>Prisbasis<ept id="p2">**</ept> kategoriprisreglerne.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>In the <bpt id="p1">**</bpt>Price rule<ept id="p1">**</ept> field, select the type of price change to use:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I feltet <bpt id="p1">**</bpt>Prisregel<ept id="p1">**</ept> skal du vælge den type prisændring, der skal bruges:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source><bpt id="p1">**</bpt>Markup<ept id="p1">**</ept> – A percentage of the price basis is used to calculate the sales price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Avance<ept id="p1">**</ept> – En procentdel af prisbasis anvendes til at beregne salgsprisen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>For example, a product that costs 10.00 and sells for 15.00 has a markup of 50 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Et produkt, der f.eks. koster 10,00 og sælges til 15,00, har en avance på 50 procent.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source><bpt id="p1">**</bpt>Margin<ept id="p1">**</ept> – A percentage of the sales price is used to calculate the amount of profit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dækningsbidrag<ept id="p1">**</ept> – En procentdel af salgsprisen bruges til at beregne overskuddet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>For example, a product that costs 10.00 and sells for 15.00 has a margin of 33.3 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Et produkt, der f.eks. koster 10,00 og sælges til 15,00, har en avance på 33,3 procent.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source><bpt id="p1">**</bpt>Fixed amount<ept id="p1">**</ept> – An amount that is added to the price basis is used to calculate the sales price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Fast beløb<ept id="p1">**</ept> – Et beløb, der lægges til prisbasis, bruges til at beregne salgsprisen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>For example, a product that costs 10.00 and sells for 15.00 has a fixed amount of 5.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Et produkt, der f.eks. koster 10,00 og sælges til 15,00, har et fast beløb på 5,00.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>In the <bpt id="p1">**</bpt>Price basis<ept id="p1">**</ept> field, select the type of price to modify:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vælg den pristype, der skal ændres, i feltet <bpt id="p1">**</bpt>Prisbasis<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source><bpt id="p1">**</bpt>Base cost<ept id="p1">**</ept> – The amount that the retailer paid to the supplier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Basisomkostninger<ept id="p1">**</ept> – Det beløb, som detailhandleren betalte til leverandøren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source><bpt id="p1">**</bpt>Base price<ept id="p1">**</ept> – The sales price before trade agreements and price adjustments are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Basispris<ept id="p1">**</ept> – Salgsprisen, før der er blevet anvendt samhandelsaftaler og prisjusteringer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source><bpt id="p1">**</bpt>Current price<ept id="p1">**</ept> – The sales price after trade agreements and price adjustments are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Aktuel pris<ept id="p1">**</ept> – Salgsprisen, efter der er blevet anvendt samhandelsaftaler og prisjusteringer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>To easily update the prices of various products from different product categories, you can use the supplemental product categories together with the category price rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">For nemt at opdatere priserne på forskellige produkter fra forskellige produktkategorier kan du bruge de supplerende produktkategorier sammen med kategoriprisregler.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Best practices</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bedste fremgangsmåder</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>Microsoft SQL Server Express is often used for channel databases because of the cost (free).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server Express bruges ofte til kanaldatabaser på grund af prisen (gratis).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>Keep in mind that SQL Server Express has hardware limitations and limits on data size.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Husk, at SQL Server Express har hardwarebegrænsninger og begrænsninger på datastørrelsen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>If you don't plan correctly, you can quickly reach the data size limits of SQL Server Express.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du ikke planlægger det nøje, kan du hurtigt nå datastørrelsesgrænserne for SQL Server Express.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>This consideration applies not only to pricing but also to other areas of the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dette hensyn gælder ikke kun for prissætning, men også andre områder for produktet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Here are a few best practices that can help you reduce the size of your data:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Her er nogle få retningslinjer for bedste praksis, som kan hjælpe dig med at reducere størrelsen på dine data:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>If you're using trade agreements, and your prices change, you should expire the old trade agreements by setting an end date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du bruger samhandelsaftaler og priserne ændrer sig, skal du ophæve de gamle samhandelsaftaler ved at angive en slutdato.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Over time, this approach helps reduce the number of trade agreements that are kept in channel databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Denne fremgangsmåde kan med tid reducere antallet af samhandelsaftaler, der opbevares i kanaldatabaserne.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>It also helps reduce the amount of data that the price calculation algorithm must work with.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dette er også med til at reducere den datamængde, som algoritmen for prisberegning skal bruge.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>If your prices vary by product variant, consider using the product base price as the price of the most common variant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis priserne varierer afhængigt af produktvariant, kan du overveje at bruge produktets basispris som prisen på den mest almindelige variant.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Then use trade agreements only for the variant prices that are exceptions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Du kan derefter kun bruge samhandelsaftaler for de variantpriser, som er undtagelser.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>This approach helps reduce the number of trade agreement records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Denne fremgangsmåde er med til at reducere antallet af poster i samhandelsaftalen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Because it's so easy to import data into Microsoft Dynamics 365, you might be tempted to import a trade agreement for every variant of every product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Da det er så nemt at importere data til Microsoft Dynamics 365, kan du være fristet til at importere en samhandelsaftale for hver variant af hvert enkelt produkt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>However, that approach can produce many trade agreements that have the same value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Denne fremgangsmåde kan imidlertid resultere i mange samhandelsaftaler med samme værdi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Therefore, it can needlessly increase the size of your data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dette kan øge størrelsen på dataene unødvendigt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Retail processes variant-specific prices in order from most specific to least specific.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail behandler variantspecifikke priser i rækkefølge, fra den mest specifikke til den mindst specifikke.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>If a product dimension doesn't affect the price, you don't have to define trade agreements for it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis en produktdimension ikke påvirker prisen, behøver du ikke at definere samhandelsaftaler for den.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>For example, a product is available in three colors and four sizes, but the price varies only by size.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Et produkt er f.eks. tilgængeligt i tre farver og fire størrelser, men prisen varierer kun efter størrelsen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>If you define a trade agreement for every variant, you create 12 records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du definerer en samhandelsaftale for alle varianter, vil du oprette 12 poster.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Instead, you can define a trade agreement just for each size and leave the Color dimension blank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I stedet kan du definere en samhandelsaftale kun for hver størrelse og lade farvedimensionen stå tom.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>In this case, you produce only four records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I så fald oprettes der kun fire poster.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>Alternatively, if not every value of a dimension produces a different price, you can define one trade agreement for the product master and leave all product dimensions blank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis ikke alle værdier i en dimension resulterer i en anden pris, kan du også definere en samhandelsaftale for produktmasteren og lade alle produktdimensioner stå tomme.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>Then define a separate trade agreement just for each dimension value that produces a different price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Definer derefter en særskilt samhandelsaftale kun for hver dimensionsværdi, der giver en anden pris.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>For example, if the XXL size has a higher price, but all other sizes have the same price, you require only two trade agreements: one for the product master and one for the XXL size.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis størrelsen XXL f.eks. har en højere pris, mens alle andre størrelser har den samme pris, kræves der kun to samhandelsaftaler: én for produktmasteren og én for XXL-størrelsen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Prices that include tax vs. prices that exclude tax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Priser inklusive moms, vs. priser eksklusive moms</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>When you set sales prices in Microsoft Dynamics 365, you don't specify whether the price value that you're setting includes or excludes tax.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når du angiver salgspriser i Microsoft Dynamics 365, skal du ikke angive, om den angivne prisværdi er med eller uden moms.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>The value is just the price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Værdien er kun prisen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>However, the <bpt id="p1">**</bpt>Price includes sales tax<ept id="p1">**</ept> setting on retail channels lets you configure retail channels so that they either include or exclude tax from prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Med indstillingen <bpt id="p1">**</bpt>Pris er inklusive moms<ept id="p1">**</ept> for detailkanaler kan du konfigurere detailkanaler, så de enten er inklusive eller eksklusive moms i priser.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>This setting is set on the channel and can change even in a single company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Denne indstilling er angivet for kanalen og kan ændres selv i en enkelt virksomhed.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>If you work with both inclusive and exclusive types of tax, it's very important that you set prices correctly, because the total amount that the customer pays will change if the <bpt id="p1">**</bpt>Price includes sales tax<ept id="p1">**</ept> setting on the channel is changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du arbejder både med inklusive og eksklusive moms, er det vigtigt, at du angiver priserne korrekt, da det samlede beløb, som kunden betaler, ændres, hvis indstillingen <bpt id="p1">**</bpt>Pris er inklusive moms<ept id="p1">**</ept> for kanalen ændres.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Differences between retail pricing and non-retail pricing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Forskelle mellem detailprissætning og ikke-detailprissætning</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>A single pricing engine is used to calculate retail prices across all channels: Call center, Retail store, and Online stores.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Et enkelt program til prissætning bruges til at beregne detailpriserne på tværs af alle kanaler: Callcenter, Detailbutik og Onlinebutikker.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>This helps in enabling the unified commerce scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dette hjælper med at muliggøre ensartede handelsscenarier.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>Retail pricing is designed to work with retail entities instead of non-retail entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Detailprissætning er designet til at fungere sammen med detailenheder i stedet for enheder uden for detailhandel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Specifically, it's designed to set prices by store, not by warehouse.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Den er specifikt designet til at angive butikspriser, ikke lagerpriser.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>The retail pricing engine doesn't support the following pricing features:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Programmet til prissætning i detailhandel understøtter ikke følgende prisfunktioner:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>Setting price by using the Site and Warehouse storage dimensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Angivelse af pris ved hjælp af lagerdimensionerne Lokation og Lagersted.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>Attribute-based pricing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Attributbaseret prissætning</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Vendor discount pass-through</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gennemgang af kreditorrabatter</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>In addition, <bpt id="p1">**</bpt>only<ept id="p1">**</ept> the retail pricing engine supports the following pricing features:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Programmet til prissætning i detailhandel understøtter desuden <bpt id="p1">**</bpt>kun<ept id="p1">**</ept> følgende prisfunktioner:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>The price is based on product dimensions, in order from the most-specific variant price to the least-specific variant price to the product master price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prisen baseres på produktdimensioner i rækkefølge fra den mest specifikke variantpris til den mindst specifikke variantpris til produktmasterprisen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>A price that is set by using two product dimensions (for example, Color and Size) is used before a price that is set by using only one product dimension (for example, Size).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En pris, der er angivet ved hjælp af to produktdimensioner (f.eks. Farve og Størrelse), bruges før en pris, der er angivet kun ved hjælp af en produktdimension (f.eks. Størrelse).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>The same price group can be used to control pricing and discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Den samme prisgruppe kan bruges til at styre priser og rabatter.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Pricing API enhancements</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Forbedringer af pris-API</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>Price is one of the most important factors that govern the buying decisions of many customers, and many customers compare prices on various sites before they make a purchase.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Prisen er en af de vigtigste faktorer, der gælder for mange kunders indkøbsbeslutninger, og mange kunder sammenligner priserne på forskellige websteder, før de foretager et køb.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>To help guarantee that they provide competitive prices, retailers keep a close eye on their competitors and often run promotions.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">For at hjælpe med at sikre, at de har konkurrencedygtige priser, holder detailhandlerne nøje øje med konkurrenterne og kører ofte kampagner.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>Therefore, to help these retailers attract customers, it's very important that product search, the browse feature, lists, and the product details page show the most accurate prices.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">For at hjælpe disse forhandlere med at tiltrække kunder er det derfor vigtigt at produktsøgning, gennemsynsfunktion, lister og siden med produktdetaljer viser de mest nøjagtige priser.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>In an upcoming release of Retail, the <bpt id="p1">**</bpt>GetActivePrices<ept id="p1">**</ept> application programming interface (API) will return prices that include simple discounts (for example, single-line discounts that don't depend on other items in the cart).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">I en kommende udgivelse af Retail returnerer <bpt id="p1">**</bpt>GetActivePrices<ept id="p1">**</ept>-API'en (Application Programming Interface) priser, der omfatter simple rabatter (f.eks. en enkeltlinjerabatter, der ikke er baseret på andre varer i indkøbsvognen).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>In this way, the prices that are shown are close to the actual amount that customers will pay for items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">På denne måde er de priser, der vises, tæt på det faktiske beløb, som kunderne skal betale for varerne.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>This API will include all the types of simple discounts: affiliation-based, loyalty-based, catalog-based, and channel-based discounts.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Denne API indeholder alle typer simple rabatter: tilknytningsbaserede, loyalitetsbaserede, katalogbaserede og kanalbaserede rabatter.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Additionally, the API will return the names and validity information for the applied discounts, so that retailers can provide a more detailed description of the price and create a sense of urgency if the discount's validity will expire soon.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Derudover returnerer API'en navnene og gyldighedsoplysningerne for de anvendte rabatter, så detailhandlerne kan give en mere detaljeret beskrivelse af prisen og skabe en oplevelse af, at det haster, hvis rabatten udløber snart.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>