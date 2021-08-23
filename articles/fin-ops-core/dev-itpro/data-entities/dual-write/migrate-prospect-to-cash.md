---
title: Overføre kundeemne til kontantdata fra dataintegrator til dobbeltskrivning
description: Dette emne beskriver, hvordan du overfører kundeemne til kontantdata fra dataintegrator til dobbeltskrivning.
author: RamaKrishnamoorthy
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-01-04
ms.openlocfilehash: 46f869265e589ad8e0c94a839df70e54fe781c5a4e7f992e6534e883b21801ae
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733117"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Overføre kundeemne til kontantdata fra dataintegrator til dobbeltskrivning

[!include [banner](../../includes/banner.md)]

Du kan overføre dit kundeemne til kontantdata fra dataintegrator til dobbeltskrivning ved at følge disse trin.

1. Kør jobsene for kundeemne til kontantdata fra dataintegrator for at udføre en sidste fuld synkronisering. På denne måde sikrer du, at begge systemer (Finance and Operations-apps og kundeengagementapps.) har alle dataene.
2. Du kan hjælpe med at forhindre tab af potentielle data ved at eksportere kundeemne til kontantdata fra Microsoft Dynamics 365 Sales til en Excel-fil eller en kommasepareret fil (CSV). Eksportér data fra følgende enheder:

    - [Konto](#account-table)
    - [Kontaktperson](#contact-table)
    - [Fakturaer](#invoice-table)
    - Fakturaprodukter
    - [Bestilling](#order-table)
    - [Produktbestilling](#order-products-table)
    - [Produkter](#products-table)
    - [Tilbud](#quote-and-quote-product-tables)
    - [Tilbudsprodukter](#quote-and-quote-product-tables)

3. Fjern kundeemne til kontantløsningen fra salgsmiljøet. Dette trin fjerner kolonnerne og de tilsvarende data, som kundeemne til kontantløsningen introducerede.
4. Installér dobbeltskrivningsløsningen.
5. Opret en dobbeltskrivningsforbindelse mellem Finance and Operations-appen og kundeengagementapps for én eller flere juridiske enheder.
6. Aktivér dobbeltskrivningstabeltilknytninger, og kør den første synkronisering for de påkrævede referencedata. (Du kan finde flere oplysninger i [Overvejelser ved første synkronisering](initial-sync-guidance.md)). Eksempler på påkrævede data omfatter debitorgrupper, betalingsbetingelser og betalingsplaner. Aktivér ikke dobbeltskrivningstilknytningerne for tabeller, der kræver initialisering, som f.eks. konto-, tilbuds-, tilbudslinje-, ordre- og ordrelinjetabellerne.
7. I kundeengagementappen skal du gå til **Avancerede indstillinger \> Systemindstillinger \> Dataadministration \> Regler for registrering af dubletter** og deaktivere alle reglerne.
8. Initialiser de tabeller, der vises i trin 2. Yderligere oplysninger finder du i de resterende afsnit i dette emne.
9. Åbn Finance and Operations-appen, og aktiver tabeltilknytningerne, som f.eks. konto-, tilbuds-, tilbudslinje-, ordre- og ordrelinjetabeltilknytninger. Kør derefter den første synkronisering. (Du kan finde flere oplysninger i [Overvejelser ved første synkronisering](initial-sync-guidance.md)). Denne proces synkroniserer flere oplysninger fra Finance and Operations-appen, f.eks. behandlingsstatus, forsendelses- og faktureringsadresser, websteder og lagersteder.

## <a name="account-table"></a>Kontotabel

1. Angiv firmanavnet i kolonnen **Firma**, f.eks. **USMF**.
2. I kolonnen **Relationstype** skal du angive **Debitor** som en statisk værdi. Det kan være en god ide at klassificere hver enkelt kontopost som en debitor i din forretningslogik.
3. I kolonnen **Debitorgruppe-id** skal du angive debitorgruppenummeret fra Finance and Operations-appen. Standardværdien fra kundeemne til kontantløsningen er **10**.
4. Hvis du bruger kundeemne til kontantløsningen uden tilpasning af **Kontonummer**, skal du angive en værdi for **Kontonummer** i kolonnen **Partnummer**. Hvis der er tilpasninger, og du ikke kender partnummeret, skal du hente disse oplysninger fra Finance and Operations-appen.

## <a name="contact-table"></a>Tabellen Kontaktpersoner

1. Angiv firmanavnet i kolonnen **Firma**, f.eks. **USMF**.
2. Angiv følgende kolonner på baggrund af værdien **IsActiveCustomer** i CSV-filen:

    - Hvis **IsActiveCustomer** er angivet til **Ja** i CSV-filen, skal du angive kolonnen **Salgbar** til **Ja**. I kolonnen **Debitorgruppe-id** skal du angive debitorgruppenummeret fra Finance and Operations-appen. Standardværdien fra kundeemne til kontantløsningen er **10**.
    - Hvis **IsActiveCustomer** er angivet til **Nej** i CSV-filen, skal du angive kolonnen **Salgbar** til **Nej** og angive kolonnen **Kontaktperson for** til **Debitor**.

3. Hvis du bruger kundeemne til kontantløsningen uden tilpasning af **Kontaktnummer**, skal du angive følgende kolonner:

    - Overfør kontaktnummeret fra CSV-filen (**msdynce\_kontaktnummer**) til kontaktnummeret i tabellen **Kontaktperson** (**msdyn\_kontaktnummer**).
    - Brug værdier fra tabellen **Kontaktnummer** i kolonnen **Partnummer**.
    - Brug værdier fra tabellen **Kontaktnummer** i kolonnen **Kontonummer/kontaktperson-id**.

## <a name="invoice-table"></a>Tabellen Faktura

Da data fra tabellen **Faktura** er designet til at strømme én vej, fra Finance and Operations-appen til kundeengagementappen, er initialisering ikke nødvendig. Kør den første synkronisering for at overføre alle påkrævede data fra Finance and Operations-appen til kundeengagementappen. Du kan finde flere oplysninger i [Overvejelser ved første synkronisering](initial-sync-guidance.md).

## <a name="order-table"></a>Ordretabel

1. Angiv firmanavnet i kolonnen **Firma**, f.eks. **USMF**.
2. Kopiér værdien fra kolonnen **Ordre-id** i CSV-filen til kolonnen **Salgsordrenummer**.
3. Kopiér værdien fra kolonnen **Debitor** i CSV-filen til kolonnen **Fakturadebitornummer**.
4. Kopiér værdien fra kolonnen **Levér til land/område** i CSV-filen til kolonnen **Levér til land/område**. Eksempler på denne værdi omfatter **US** og **United States**.
5. Angiv kolonnen **Ønsket modtagelsesdato**. Hvis du ikke bruger en modtagelsesdato, skal du bruge kolonnerne **Ønsket leveringsdato**, **Dato opfyldt** og **Dato sendt** i CSV-filen. Et eksempel på denne værdi er **2020-03-27T00:00:00Z**.
6. Angiv kolonnen **Sprog**. Et eksempel på denne værdi er **da-dk**.
7. Angiv kolonnen **Ordretype** ved hjælp af kolonnen **Varebaseret**.

## <a name="order-products-table"></a>Tabellen Bestille produkter

- Angiv firmanavnet i kolonnen **Firma**, f.eks. **USMF**.

## <a name="products-table"></a>Tabellen Produkter

Da data fra tabellen **Produkter** er designet til at strømme én vej, fra Finance and Operations-appen til kundeengagementappen, er initialisering ikke nødvendig. Kør den første synkronisering for at overføre alle påkrævede data fra Finance and Operations-appen til kundeengagementappen. Du kan finde flere oplysninger i [Overvejelser ved første synkronisering](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Tabellerne Tilbud og Tilbudsprodukter

For tabellen **Tilbud** skal du følge instruktionerne i afsnittet [Ordretabel](#order-table) tidligere i dette emne. For tabellen **Tilbudsprodukt** skal du følge instruktionerne i afsnittet [Tabellen Bestille produkter](#order-products-table).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]