---
title: Oprette mailskabeloner til transaktionshændelser
description: Dette emne beskriver, hvordan du opretter, overfører og konfigurerer mailskabeloner for transaktionshændelser i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4fd46ea161fb4441d94a9e7c7f7ffbfb245eb873
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919495"
---
# <a name="create-email-templates-for-transactional-events"></a>Oprette e-mailskabeloner til transaktionshændelser

[!include [banner](includes/banner.md)]


Dette emne beskriver, hvordan du opretter, overfører og konfigurerer mailskabeloner for transaktionshændelser i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce indeholder en indbygget løsning til afsendelse af mails, der giver kunder besked om transaktionshændelser. Mails kan f.eks. sendes, når en ordre afgives, er klar til afhentning eller er afsendt. I dette emne beskrives trinnene til oprettelse, upload og konfiguration af de mailskabeloner, der bruges til at sende transaktionsmails.

## <a name="notification-types"></a>Beskedtyper

Beskeder kan konfigureres til at informere kunder via mail, når der opstår bestemte hændelser som en del af ordren og kundens livscyklus. Hvis du vil konfigurere beskeder, skal du knytte en mailskabelon til en beskedtype ved at oprette en Commerce-profil for mailbesked. Du kan finde oplysninger om, hvordan du konfigurerer beskedprofiler, i [Konfigurere en mailbeskedprofil](email-notification-profiles.md).

Dynamics 365 Commerce understøtter følgende beskedtyper.

### <a name="order-created"></a>Der er oprettet en ordre

Beskedtypen *ordre oprettet* udløses, når der oprettes en ny salgsordre i Commerce-hovedkontoret.

> [!NOTE]
> Beskedtypen for ordre oprettet udløses ikke for cash-and-carry-transaktioner, der finder sted på en POS-terminal. I dette tilfælde genereres der en mail og/eller udskrevet kvittering. Yderligere oplysninger finder du i [Sende mailkvitteringer fra Modern POS (MPOS)](email-receipts.md).

### <a name="order-confirmed"></a>Bekræftet ordre

Beskedtypen *ordre bekræftet* udløses, når der genereres et ordrebekræftelsesdokument for en salgsordre fra Commerce-hovedkontoret.

### <a name="picking-completed"></a>Fuldført pluk

Beskedtypen *pluk fuldført* udløses, når en plukliste for en ordre er markeret som fuldført i Commerce-hovedkontoret.

> [!NOTE]
> Den beskedtypen pluk fuldført udløses ikke, når en vare er markeret som plukket i en POS-klient.

### <a name="packing-completed"></a>Fuldført emballage

Beskedtypen *pakning fuldført* udløses, når et følgeseddeldokument oprettes for en ordre i Commerce-hovedkontoret på POS-klienten.

Beskedtypen for pakning fuldført understøtter følgende yderligere mailpladsholdere for at facilitere "ordre klar til afhentning" og ordreopslag fra transaktionsmails.

| Pladsholdernavn    | Formål |
| ------------------- | ------- |
| `pickupstorename`     | Navnet på den butik, hvor ordren kan afhentes. |
| `pickupstoreaddress`  | Adressen på den butik, hvor ordren kan afhentes. |
| `pickupstorehourfrom` | Åbningstiden i afhentningsbutikken. |
| `pickupstorehourto`   | Lukketiden i afhentningsbutikken. |
| `pickupchannelid`     | Id'et for butikskanalen for afhentningsbutikken. |
| `packingslipid`      | Id'et for følgesedlen til den ordre, der skal afhentes. |
| `confirmationid`      | Id'et for ordrebekræftelse af den ordre, der skal afhentes. (Dette id kaldes også kanalreference-id'et.) |

Du kan finde flere oplysninger om kunders indtjekning og ordreopslagsfunktioner i [Konfigurere registrering og omdirigeret registrering](geo-detection-redirection.md) og [Aktivere ordreopslag for gæsteudbetaling](order-lookup-guest.md).

### <a name="order-ready-for-pickup"></a>Ordre er klar til afhentning

Beskedtypen *ordre klar til afhentning*, udløses, når en ordre er markeret som pakket, og leveringsmåden er angivet til **Kundeafhentning** på en eller flere ordrelinjer.

> [!NOTE]
> Beskedtypen for ordre klar til afhentning er blevet udfaset til fordel for beskedtypen pakning fuldført. Denne beskedtype tilpasses efter leveringsmåde.

### <a name="order-shipped"></a>Afsendt ordre

Beskedtypen *ordre afsendt* udløses, når en ordre, hvis leveringsmåde ikke er afhentning i butikken, er faktureret.

> [!NOTE]
> Beskedtypen for ordre afsendt er blevet udfaset til fordel for beskedtypen ordre faktureret. Denne beskedtype tilpasses efter leveringsmåde.

### <a name="order-invoiced"></a>Ordre faktureret

Beskedtypen *ordre faktureret* udløses, når der faktureres en ordre i POS eller Commerce-hovedkontoret.

### <a name="issue-gift-card"></a>Udsted gavekort

Beskedtypen *udsted gavekort* udløses, når en salgsordre, der indeholder et produkt af typen gavekort, faktureres.

> [!NOTE]
> Beskedmailen for udsted gavekort sendes til modtageren af gavekortet. Modtageren af gavekortet angives i Commerce-hovedkontoret på en individuel salgsordrelinje under fanen **Emballage** under **Linjedetaljer**. Den kan angives manuelt eller via programmering.

Beskedtypen udstedelse af gavekort understøtter følgende yderligere pladsholdere.

| Pladsholdernavn      | Formål |
| --------------------- | ------- |
| `giftcardnumber`        | Nummeret på gavekortet, for produkter af typen gavekort. |
| `giftcardbalance`       | Gavekortsaldoen, for produkter af typen gavekort. |
| `giftcardmessage`       | Gavekortmeddelelsen, for produkter af typen gavekort. |
| `giftcardpin`         | Den personlige pinkode for gavekortet, for produkter af typen gavekort. (Denne pladsholder er specifik for eksterne gavekort). |
| `giftcardexpiration`    | Udløbsdatoen for gavekortet, for produkter af typen gavekort. (Denne pladsholder er specifik for eksterne gavekort). |
| `giftcardrecipientname` | Navnet på gavekortmodtageren, for produkter af typen gavekort. |
| `giftcardbuyername`     | Navnet på gavekortkøberen, for produkter af typen gavekort. |

Du kan finde flere oplysninger om gavekort i [Digitale e-handelsgavekort](digital-gift-cards.md) og [Understøttelse af eksterne gavekort](dev-itpro/gift-card.md).

### <a name="order-cancellation"></a>Ordreannullering

Beskedtypen *ordreannullering* udløses, når der annulleres en ordre i POS eller Commerce-hovedkontoret.

### <a name="customer-created"></a>Kunden er oprettet

Beskedtypen *kunde oprettet* udløses, når der oprettes en ny kundeenhed i Commerce-hovedkontoret.

### <a name="b2b-prospect-approved"></a>B2B-kundeemne er godkendt

Beskedtypen *B2B-kundeemne godkendt* udløses, når en anmodning om onboarding af et kundeemne godkendes i Commerce-hovedkontoret. Du kan finde flere oplysninger om godkendelse eller afvisning af B2B-kundeemner i [Konfigurere administratorbrugeren til en ny forretningspartner](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

Beskedtypen B2B-kundeemne godkendt understøtter følgende yderligere pladsholdere.

| Pladsholdernavn | Formål                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`       | Fornavnet på B2B-kundeemnet, som det er angivet i programmet. |
| `lastname`         | Efternavnet på B2B-kundeemnet, som det er angivet i programmet. |
| `company`          | Navnet på ansøgerens firma, som det er angivet i programmet. |
| `email`            | Kundeemnets mailadresse, som det er angivet i programmet.   |
| `zipcode`          | Postnr. til kundeemnets primære adresse. |
| `comments`         | Kommentaren, som kundeemnet har angivet i programmet. |
| `storename`        | Navnet på den kanal, hvor kundeemnet blev oprettet. |
| `storeurl`         | Tom som standard. Der skal oprettes en brugerdefineret udvidelse til brug af denne pladsholder. |

### <a name="b2b-prospect-rejected"></a>B2B-kundeemne blev afvist

Beskedtypen *B2B-kundeemne afvist* udløses, når en anmodning om onboarding af et kundeemne afvises i Commerce-hovedkontoret. Du kan finde flere oplysninger om godkendelse eller afvisning af B2B-kundeemner i [Konfigurere administratorbrugeren til en ny forretningspartner](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

Beskedtypen B2B-kundeemne afvist understøtter følgende yderligere pladsholdere.

| Pladsholdernavn | Formål                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`        | Fornavnet på B2B-kundeemnet, som det er angivet i programmet. |
| `lastname`         | Efternavnet på B2B-kundeemnet, som det er angivet i programmet. |
| `company`          | Navnet på ansøgerens firma, som det er angivet i programmet. |

## <a name="create-an-email-template"></a>Opret en mailskabelon

Før du kan knytte en bestemt transaktionshændelse til en mailskabelon, skal du oprette skabelonen.

Benyt følgende fremgangsmåde for at oprette en mailskabelon.

1. I Commerce Headquarters skal du gå til **Detail og handel \> Konfiguration af hovedkontor \> Skabeloner til organisationsmail** eller **Organisationsadministration \> Konfiguration \> Skabeloner til organisationsmail**.
1. Vælg **Ny**.
1. Under **Generelt** skal du angive følgende felter:

    - **Mail-id** – Mail-id'et er det entydige id for en skabelon. Det er den værdi, der vises, når du vælger en skabelon, som skal knyttes til en hændelse.
    - **E-mail-beskrivelse** – du kan bruge dette valgfrie felt til at angive en beskrivelse af skabelonen. Den værdi, du angiver, vises kun i Commerce Headquarters.
    - **Navn på afsender** – det navn, du angiver, vises i feltet "fra" i de fleste e-mail-klienter.
    - **Afsenders-e-mailadresse** – angiv den e-mail-adresse, der skal bruges til e-mails, der sendes vha. denne skabelon.
    - **Standardsprogkode** – i dette felt angives den lokaliserede version af den mail, der sendes som standard, hvis der ikke er angivet et sprog i den kanal, der kalder denne skabelon.

1. Under **E-mailbeskedens indhold** skal du vælge **Ny**.
1. I feltet **Sprog** skal du angive sproget til e-mail-skabelonen. Du kan tilføje flere sprog og lokaliserede skabeloner på et senere tidspunkt.
1. I feltet **Emne** skal du angive det e-mail-emne, der skal vises i feltet Emne i e-mailen.
1. Vælg **Rediger** for at uploade e-mail-skabelonen.

## <a name="create-an-email-message-body-by-using-html"></a>Oprette en brødtekst i en e-mail ved hjælp af HTML

Meddelelsesbrødteksten i e-mail-meddelelsen oprettes i HTML. Du kan bruge ethvert layout, alle tilpasninger og mærkninger, som HTML og integrerede overlappende typografiark (CSS) tillader. Du kan også bruge billeder, hvis du hoster dem på et offentligt tilgængeligt websted. Hvis du vil tilføje et billede, skal du angive billedets URL-adresse i **src**-attributten for HTML-koden **&lt;img-&gt;**.

> [!NOTE]
> E-mail-klienter pålægger layout- og typografibegrænsninger, der kan kræver justeringer af HTML-koden, og CSS, som du bruger til meddelelsesbrødteksten. Det anbefales, at du sætter dig ind i de bedste metoder til at oprette HTML-tekst, der understøttes af de mest populære emailklienter.

## <a name="add-placeholders-to-the-email-message-body"></a>Føje pladsholdere til e-mail-meddelelsens brødtekst

Din e-mail kan indeholde pladsholdere, der erstattes af kundespecifikke og transaktionsspecifikke værdier, når e-mailen genereres. Pladsholdere er altid omgivet af procenttegn (%) og indsættes direkte i HTML-dokumentet.

Her er et eksempel.

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a>Ordrepladsholdere (på salgsordreniveau)

Følgende pladsholdere henter og viser data, der er defineret på salgsordreniveau (i modsætning til salgslinjeniveau).

| Pladsholdernavn     | Formål                                                      |
| -------------------- | ------------------------------------------------------------ |
| `customername`         | Navnet på den kunde, der har afgivet ordren.               |
| `customeraddress`      | Kundens adresse.                                 |
| `customeremailaddress` | Den mailadresse, som kunden angav ved kassen.     |
| `salesid`              | Salgsordrens id.                                   |
| `orderconfirmationid`  | Det krydskanal-id, der blev genereret ved ordreoprettelse.   |
| `channelid`            | Id'et for den detail- eller onlinekanal, som ordren er afgivet via. |
| `deliveryname`         | Det navn, der er angivet for leveringsadressen.         |
| `deliveryaddress`      | Leveringsadressen for afsendte ordrer.                     |
| `deliverydate`         | Leveringsdatoen.                                           |
| `shipdate`             | Afsendelsesdatoen.                                               |
| `modeofdelivery`       | Ordrens leveringsmåde.                              |
| `ordernetamount`       | Det samlede beløb for ordren minus samlet moms.         |
| `discount`            | Den samlede rabat for ordren.                            |
| `charges`              | Det samlede gebyr for ordren.                             |
| `tax`                  | Den samlede moms for ordren.                                 |
| `total`                | Det samlede beløb for ordren.                              |
| `storename`            | Navnet på den butik, hvor ordren blev afgivet.            |
| `storeaddress`         | Adressen på den butik, der har afgivet ordren.              |
| `storeopenfrom`        | Åbningstiden for den butik, der har afgivet ordren.         |
| `storeopento`          | Lukketiden for den butik, der har afgivet ordren.         |
| `pickupstorename`      | Navnet på den butik, hvor ordren afhentes.\*   |
| `pickupstoreaddress`   | Adressen på den butik, hvor ordren afhentes.\* |
| `pickupopenstorefrom`  | Åbningstidspunkt for den butik, hvor ordren afhentes.\* |
| `pickupopenstoreto`    | Lukketidspunkt for den butik, hvor ordren afhentes.\* |
| `pickupchannelid`     | Kanal-id'et for den butik, der er angivet for levering som afhentningsmåde.\* |
| `packingslipid`        | Id'et for den følgeseddel, der blev genereret, da linjerne i en ordre blev pakket.\* |

\*Disse pladsholdere returnerer kun data, når de bruges til **Ordre klar til afhentning** som beskedtype. 

### <a name="order-line-placeholders-sales-line-level"></a>Ordrelinjepladsholdere (på salgslinjeniveau)

Følgende pladsholdere henter og viser data for individuelle produkter (linjer) i salgsordren.

| Pladsholdernavn               | Formål |
|--------------------------------|-------------------|
| `productid`                      | <p>Id'et for produktet. Dette id medtager varianter.</p><p><strong>Bemærk:</strong> Denne pladsholder er blevet udfaset til fordel for `lineproductrecid`.</p> |
| `lineproductrecid`               | Id'et for produktet. Dette id medtager varianter. Den identificerer en vare entydigt på variantniveau. |
| `lineitemid`                     | Id for produkt på produktniveauet. (Dette id medtager ikke varianter). |
| `lineproductvariantid`           | Id'et for produktvarianten. |
| `lineproductname`                | Navnet på produktet. |
| `lineproductdescription`         | Beskrivelsen af produktet. |
| `linequantity`                   | Antallet af enheder, der er bestilt for linjen, plus måleenheden (f.eks. **ea** eller **par**). |
| `lineunit`                       | Måleenhed for linjen. |
| `linequantity_withoutunit`       | Antallet af enheder, der er bestilt for linjen, uden måleenheden. |
| `linequantitypicked`             | Når hændelsen **Pluk ordre** bruges, er det antallet af enheder, der blev plukket. Ellers **0** (nul). |
| `linequantitypicked_withoutunit` | Når hændelsen **Pluk ordre** bruges, er det antallet af enheder, der er plukket, uden måleenheden. Ellers **0** (nul). |
| `linequantitypacked`             | Når hændelserne **Pak ordre** og **Ordren er klar til afhentning** bruges, er det antallet af enheder, der blev pakket. Ellers **0** (nul). |
| `linequantitypacked_withoutuom`  | Når hændelserne **Pak ordre** og **Ordren er klar til afhentning** bruges, er det antallet af enheder, der blev pakket, uden måleenheden. Ellers **0** (nul). |
| `linequantityshipped`            | Altid **0**, undtagen når der bruges bestemte hændelser, som det er beskrevet i næste række. |
| `linequantityshipped_withoutuom` | Når hændelsen **Afsend ordre** bruges, er det antallet af enheder, der er plukket, uden måleenheden. Ellers **0** (nul). |
| `lineprice`                      | Prisen på en enkelt enhed. |
| `linenetamount`                  | Prisen på linjen, efter at antallet af enheder og rabat anvendes. |
| `linediscount`                   | Rabatten for en individuel enhed. |
| `lineshipdate`                   | Afsendelsesdatoen for linjen. |
| `linedeliverydate`               | Leveringsdatoen for linjen. |
| `linedeliverymode`               | Leveringstilstanden for linjen. |
| `linedeliveryaddress`            | Leveringsadressen for linjen. |
| `linepickupdate`                 | Den afhentningsdato, som kunden har angivet for ordrer, der anvender levering som afhentningsmetode. |
| `linepickuptimeslot`             | Det tidsinterval for afhentning, som kunden har angivet for ordrer, der anvender levering som afhentningsmetode. |
| `giftcardnumber`                 | Nummeret på gavekortet, for produkter af typen gavekort. |
| `giftcardbalance`                | Gavekortsaldoen, for produkter af typen gavekort. |
| `giftcardmessage`                | Gavekortmeddelelsen, for produkter af typen gavekort. |
| `giftcardpin`                    | Pinkoden til gavekortet, for produkter af typen gavekort. (Denne pladsholder er specifik for eksterne gavekort). |
| `giftcardexpiration`             | Udløbsdatoen for gavekortet, for produkter af typen gavekort. (Denne pladsholder er specifik for eksterne gavekort). |
| `giftcardrecipientname`          | Navnet på gavekortmodtageren, for produkter af typen gavekort. |
| `giftcardbuyername`              | Navnet på gavekortkøberen, for produkter af typen gavekort. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Format for ordrelinjepladsholdere i e-mail-brødteksten

Når du opretter HTML'en til de enkelte ordrelinjer i indholdet af en mailmeddelelse, skal du omslutte gentagelsesblokken af HTML og pladsholdere for linjerne med følgende pladsholdere. Bemærk, at pladsholderne er inde i HTML-kommentarmærker.

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

Her er et eksempel.

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a>Oprette en skabelon til e-mail-kvitteringer

Kvitteringer kan sendes via e-mail til kunder, der foretager indkøb i en detailbutik (POS). Trinnene til oprettelse af skabelonen til e-mail-modtagelse er som regel de samme som de trin, du skal bruges til at oprette skabeloner til andre transaktionshændelser. Følgende ændringer er dog nødvendige:

- Pladsholderen **%message%** bruges til at indsætte kvitteringens tekst i mailen. For at sikre, at kvitteringsbrødteksten gengives korrekt, skal du omslutte pladsholderen **%message%** med HTML-tags **&lt;pre&gt;** og **&lt;/pre&gt;**.
- Pladsholderen **%receiptid%** kan bruges til at vise en QR-kode eller stregkode, der repræsenterer kvitterings-id. (QR-koder og stregkoder genereres dynamisk og serviceres af en tredjepartstjeneste). Yderligere oplysninger om, hvordan du viser en QR-kode eller stregkode i en e-mail-kvittering, finder du i [Tilføje en QR-kode eller stregkode til transaktions- og kvitterings-e-mails](add-qr-code-barcode-email.md).

## <a name="upload-the-email-html"></a>Uploade e-mail-HTML

Når du har oprettet og testet HTML-koden til meddelelsesbrødteksten, skal den overføres til Commerce Headquarters. I øjeblikket kan e-mail-HTML ikke eksporteres. Derfor skal du vedligeholde hovedkopien af din HTML uden for Commerce Headquarters.

Udfør følgende trin for at uploade en ny eller redigeret e-mail-skabelon i HTML.

1. I Commerce Headquarters skal du gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Skabelon til organisationsmail**.
1. Vælg rækken for det sprog, du vil tilføje eller erstatte HTML for. Du kan også vælge **Ny** for at oprette en række til et nyt sprog.
1. Vælg **Rediger**.
1. Vælg **Gennemse** i dialogboksen, der vises. Gå til det HTML-dokument, du vil overføre, marker det, og vælg derefter **Åbn**.
1. Vælg **Overfør**.
1. Når din e-mail-HTML-kode vises i eksempelvinduet, skal du klikke på **OK**.
1. Sørg for, at afkrydsningsfeltet **Har indhold** er valgt for rækken.

Hvis du allerede har konfigureret Commerce Headquarters til at sende e-mail, vil den nye eller opdaterede e-mail blive sendt til alle kunder, der udfører en transaktioner, der udløser den hændelse, der er knyttet til skabelonen.

Få flere oplysninger om, hvordan du kan konfigurere e-mails i Dynamics 365 Commerce, i [Konfigurere og sende e-mail](../fin-ops-core/fin-ops/organization-administration/configure-email.md).

## <a name="additional-resources"></a>Yderligere ressourcer 

[Konfigurere en profil for mailbesked](email-notification-profiles.md)

[Konfigurere og sende mail](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[Konfigurere e-mail-kvitteringer](/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[Sende e-mail-kvitteringer fra Modern POS ](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
