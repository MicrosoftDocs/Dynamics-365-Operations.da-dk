---
title: Oprette mailskabeloner til transaktionshændelser
description: Dette emne beskriver, hvordan du opretter, overfører og konfigurerer mailskabeloner for transaktionshændelser i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ea484bfc1e9b293c53d7293c50630c4955000131
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983151"
---
# <a name="create-email-templates-for-transactional-events"></a>Oprette mailskabeloner til transaktionshændelser

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du opretter, overfører og konfigurerer mailskabeloner for transaktionshændelser i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Dynamics 365 Commerce indeholder en færdiglavet løsning til afsendelse af mails, der advarer kunderne om transaktionshændelser (f. eks. får en ordre er afgivet, er klar til afhentning, eller der er afsendt en ordre). I dette emne beskrives trinnene til oprettelse, upload og konfiguration af de mailskabeloner, der bruges til at sende transaktionsmails.

## <a name="create-an-email-template"></a>Opret en mailskabelon

Før du kan knytte en bestemt transaktionshændelse til en mailskabelon, skal du oprette skabelonen.

Benyt følgende fremgangsmåde for at oprette en mailskabelon.

1. I Commerce Headquarters skal du gå til **Skabelon til organisationsmail**, som du finder under **Detail og handel \> Konfiguration af hovedkontor \> Skabelon til organisationsmail** eller **Virksomhedsadministration \> Konfiguration \> Skabelon til organisationsmail**.
1. Vælg **Ny**.
1. Under **Generelt** skal du angive følgende felter:

    - **E-mail-id** – mail-id'et er det entydige id for en skabelon, og det er den værdi, der vises, når du vælger en skabelon, der skal knyttes til en hændelse.
    - **E-mail-beskrivelse** – du kan bruge dette valgfrie felt til at angive en beskrivelse af skabelonen. Den værdi, du angiver, vises kun i Commerce Headquarters.
    - **Navn på afsender** – det navn, du angiver, vises i feltet "fra" i de fleste e-mail-klienter.
    - **Afsenders-e-mailadresse** – angiv den e-mail-adresse, der skal bruges til e-mails, der sendes vha. denne skabelon.
    - **Standardsprogkode** – i dette felt angives den lokaliserede version af den e/mail, der sendes som standard, hvis der ikke er angivet et sprog i den kanal, der kalder denne skabelon.

1. Under **E-mailbeskedens indhold** skal du vælge **Ny**.
1. I feltet **Sprog** skal du angive sproget til e-mail-skabelonen. Du kan tilføje flere sprog og lokaliserede skabeloner på et senere tidspunkt.
1. I feltet **Emne** skal du angive det e-mail-emne, der skal vises i feltet Emne i e-mailen.
1. Vælg **Rediger** for at uploade e-mail-skabelonen.

## <a name="create-an-email-message-body-by-using-html"></a>Oprette en brødtekst i en e-mail ved hjælp af HTML

Meddelelsesbrødteksten i e-mail-meddelelsen oprettes i HTML. Du kan bruge ethvert layout, alle tilpasninger og mærkninger, som HTML og integrerede overlappende typografiark (CSS) tillader. Du kan også bruge billeder, hvis du hoster dem på et offentligt tilgængeligt websted. Hvis du vil tilføje et billede, skal du angive billedets URL-adresse i **src**-attributten for HTML-koden **&lt;img-&gt;**.

> [!NOTE]
> E-mail-klienter pålægger layout- og typografibegrænsninger, der kan kræver justeringer af HTML-koden, og CSS, som du bruger til meddelelsesbrødteksten. Det anbefales, at du orienterer dig om de bedste fremgangsmåder til oprettelse af HTML, der understøttes af de mest populære e-mail-klienter.

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

| Pladsholdernavn    | Pladsholderværdi                                                |
|---------------------|------------------------------------------------------------------|
| customername        | Navnet på den kunde, der har afgivet ordren.                   |
| salesid             | Salgsordrens id.                                       |
| deliveryaddress     | Leveringsadressen for afsendte ordrer.                         |
| customeraddress     | Kundens adresse.                                     |
| deliverydate        | Leveringsdatoen.                                               |
| shipdate            | Afsendelsesdatoen.                                                   |
| modeofdelivery      | Ordrens leveringsmåde.                                  |
| charges             | Det samlede gebyr for ordren.                                 |
| tax                 | Den samlede moms for ordren.                                     |
| total               | Det samlede beløb for ordren.                                  |
| ordrenettobeløb      | Det samlede beløb for ordren minus samlet moms.             |
| rabat            | Den samlede rabat for ordren.                                |
| storename           | Navnet på den butik, hvor ordren blev afgivet.                |
| storeaddress        | Adressen på den butik, der har afgivet ordren.                  |
| storeopenfrom       | Åbningstiden for den butik, der har afgivet ordren.             |
| storeopento         | Lukketiden for den butik, der har afgivet ordren.             |
| pickupstorename     | Navnet på den butik, hvor ordren afhentes.         |
| pickupstoreaddress  | Adressen på den butik, hvor ordren afhentes.      |
| pickupopenstorefrom | Åbningstidspunkt for den butik, hvor ordren afhentes. |
| pickupopenstoreto   | Lukketidspunkt for den butik, hvor ordren afhentes. |

### <a name="order-line-placeholders-sales-line-level"></a>Ordrelinjepladsholdere (på salgslinjeniveau)

Følgende pladsholdere henter og viser data for individuelle produkter (linjer) i salgsordren.

| Pladsholdernavn               | Pladsholderværdi |
|--------------------------------|-------------------|
| productid                      | Produkt-id'et for linjen. |
| lineproductname                | Navnet på produktet. |
| lineproductdescription         | Beskrivelsen af produktet. |
| linequantity                   | Antallet af enheder, der er bestilt for linjen, plus måleenheden (f.eks. **ea** eller **par**). |
| lineunit                       | Måleenhed for linjen. |
| linequantity_withoutunit       | Antallet af enheder, der er bestilt for linjen, uden måleenheden. |
| linequantitypicked             | Når hændelsen **Pluk ordre** bruges, er det antallet af enheder, der blev plukket. Ellers **0** (nul). |
| linequantitypicked_withoutunit | Når hændelsen **Pluk ordre** bruges, er det antallet af enheder, der er plukket, uden måleenheden. Ellers **0** (nul). |
| linequantitypacked             | Når hændelserne **Pak ordre** og **Ordren er klar til afhentning** bruges, er det antallet af enheder, der blev pakket. Ellers **0** (nul). |
| linequantitypacked_withoutuom  | Når hændelserne **Pak ordre** og **Ordren er klar til afhentning** bruges, er det antallet af enheder, der blev pakket, uden måleenheden. Ellers **0** (nul). |
| linequantityshipped            | Altid **0**, undtagen når der bruges bestemte hændelser, som det er beskrevet i næste række. |
| linequantityshipped_withoutuom | Når hændelsen **Afsend ordre** bruges, er det antallet af enheder, der er plukket, uden måleenheden. Ellers **0** (nul). |
| lineprice                      | Prisen på en enkelt enhed. |
| linenetamount                  | Prisen på linjen, efter at antallet af enheder og rabat anvendes. |
| linediscount                   | Rabatten for en individuel enhed. |
| lineshipdate                   | Afsendelsesdatoen for linjen. |
| linedeliverydate               | Leveringsdatoen for linjen. |
| linedeliverymode               | Leveringstilstanden for linjen. |
| linedeliveryaddress            | Leveringsadressen for linjen. |
| giftcardnumber                 | Nummeret på gavekortet, for produkter af typen gavekort. |
| giftcardbalance                | Gavekortsaldoen, for produkter af typen gavekort. |
| giftcardmessage                | Gavekortmeddelelsen, for produkter af typen gavekort. |
| giftcardpin                    | Den personlige pinkode for gavekortet, for produkter af typen gavekort. (Denne pladsholder er specifik for eksterne gavekort). |
| giftcardexpiration             | Udløbsdatoen for gavekortet, for produkter af typen gavekort. (Denne pladsholder er specifik for eksterne gavekort). |
| giftcardrecipientname          | Navnet på gavekortmodtageren, for produkter af typen gavekort. |
| giftcardbuyername              | Navnet på gavekortkøberen, for produkter af typen gavekort. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Format for ordrelinjepladsholdere i e-mail-brødteksten

Når du opretter HTML'en til de enkelte ordrelinjer i e-mail-meddelelsens brødtekst, skal du omslutte gentagelsesblokken af HTML og pladsholdere for linjerne med følgende pladsholdere, der placeres i HTML-kommentarkoder.

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

- E-mail-id'et for e-mail-skabelonen skal være **emailRecpt**.
- Teksten til kvitteringen indsættes i e-mailen ved hjælp af pladsholderen **%message%**. For at sikre, at kvitteringsbrødteksten gengives korrekt, skal du omslutte pladsholderen **%message%** med HTML-koderne **&lt;pre&gt;** og **&lt;/pre&gt;**.
- Linjeskift i HTML-koden for sidehovedet og sidefoden i e-mailen konverteres til HTML-koder **&lt;br /&gt;**, så modtagelseskvitteringen gengives korrekt. Hvis du vil fjerne uønsket lodret plads i dine kvitterings-e-mails, skal du fjerne linjeskift fra et hvilket som helst sted i HTML-format, hvor der ikke kræves lodret plads.

Få flere oplysninger om, hvordan du kan konfigurere e-mail-kvitteringer, du i [Konfigurere e-mail-kvitteringer](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts).

## <a name="upload-the-email-html"></a>Uploade e-mail-HTML

Når du har oprettet og testet HTML-koden til meddelelsesbrødteksten, skal den overføres til Commerce Headquarters. I øjeblikket kan e-mail-HTML ikke eksporteres. Derfor skal du vedligeholde hovedkopien af din HTML uden for Commerce Headquarters.

Udfør følgende trin for at uploade en ny eller redigeret e-mail-skabelon i HTML.

1. I Commerce Headquarters skal du gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Skabelon til organisationsmail**.
1. Vælg rækken for det sprog, du vil tilføje eller erstatte HTML for. Du kan også vælge **Ny** for at oprette en række til et nyt sprog.
1. Vælg **Rediger**.
1. Vælg **Gennemse** i dialogboksen, der vises. Gå til det HTML-dokument, du vil overføre, marker det, og vælg derefter **Åbn**.
1. Vælg **Overfør**.
1. Når din e-mail-HTML-kode vises i eksempelvinduet, skal du klikke på **OK**.
1. Sørg for, at afkrydsningsfeltet **Har indhold** vælges for rækken.

Hvis du allerede har konfigureret Commerce Headquarters til at sende e-mail, vil den nye eller opdaterede e-mail blive sendt til alle kunder, der udfører en transaktioner, der udløser den hændelse, der er knyttet til skabelonen.

Få flere oplysninger om, hvordan du kan konfigurere e-mails i Dynamics 365 Commerce, i [Konfigurere og sende e-mail](../fin-ops-core/fin-ops/organization-administration/configure-email.md).

## <a name="additional-resources"></a>Yderligere ressourcer 

[Konfigurere en profil for mailbesked](email-notification-profiles.md)

[Konfigurere og sende mail](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[Konfigurere e-mail-kvitteringer](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[Sende e-mail-kvitteringer fra Modern POS ](email-receipts.md)
