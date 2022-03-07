---
title: Overføre kundeemne til kontantdata fra dataintegrator til dobbeltskrivning
description: Dette emne beskriver, hvordan du overfører kundeemne til kontantdata fra dataintegrator til dobbeltskrivning.
author: RamaKrishnamoorthy
ms.date: 02/01/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-26
ms.openlocfilehash: 82bfb768b0ecac04184f4b806527346d39584d64
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087262"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Overføre kundeemne til kontantdata fra dataintegrator til dobbeltskrivning

[!include [banner](../../includes/banner.md)]

Den tilgængelige løsning Kundeemne til kontanter for Dataintegrator er ikke kompatibel med dobbeltskrivning. Årsagen til dette er indekset msdynce_AccountNumber i kontotabellen, der fulgte med løsningen Kundeemne til kontanter. Hvis dette indeks findes, kan du ikke oprette samme debitorkontonummer i to forskellige juridiske enheder. Du kan enten vælge at starte forfra med dobbeltskrivning ved at overføre Kundeemne til kontanter-data fra Dataintegrator til dobbeltskrivning, eller du kan installere den sidste "dorman"-version af løsningen Kundeemne til kontanter. Dette emne beskriver begge disse metoder.

## <a name="install-the-last-dorman-version-of-the-data-integrator-prospect-to-cash-solution"></a>Installer den sidste "dorman"-version af Dataintegrator-løsningen Kundeemne til kontanter

**P2C Version 15.0.0.2** regnes for den sidste "dorman"-version af Dataintegrator-løsningen Kundeemne til kontanter. Du kan hente den fra [FastTrack for Dynamics 365](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/P2C).

Du skal installere den manuelt. Efter installationen forbliver alt nøjagtigt det samme, med undtagelse af, at msdynce_AccountNumber-indekset fjernes.

## <a name="steps-to-migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Trin til at overføre kundeemne til kontantdata fra dataintegrator til dobbeltskrivning

Du kan overføre dit kundeemne til kontantdata fra dataintegrator til dobbeltskrivning ved at følge disse trin.

1. Kør jobsene for kundeemne til kontantdata fra dataintegrator for at udføre en sidste fuld synkronisering. På denne måde sikrer du, at begge systemer (Finans- og driftsapps og kundeengagementapps) har alle dataene.
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
5. Opret en dobbeltskrivningsforbindelse mellem Finans- og driftsappen og kundeengagementappen for én eller flere juridiske enheder.
6. Aktivér dobbeltskrivningstabeltilknytninger, og kør den første synkronisering for de påkrævede referencedata. (Du kan finde flere oplysninger i [Overvejelser ved første synkronisering](initial-sync-guidance.md)). Eksempler på påkrævede data omfatter debitorgrupper, betalingsbetingelser og betalingsplaner. Aktivér ikke dobbeltskrivningstilknytningerne for tabeller, der kræver initialisering, som f.eks. konto-, tilbuds-, tilbudslinje-, ordre- og ordrelinjetabellerne.
7. I kundeengagementappen skal du gå til **Avancerede indstillinger \> Systemindstillinger \> Dataadministration \> Regler for registrering af dubletter** og deaktivere alle reglerne.
8. Initialiser de tabeller, der vises i trin 2. Yderligere oplysninger finder du i de resterende afsnit i dette emne.
9. Åbn Finans- og driftsappen, og aktivér tabeltilknytningerne som f.eks. konto-, tilbuds-, tilbudslinje-, ordre- og ordrelinjetabeltilknytninger. Kør derefter den første synkronisering. (Du kan finde flere oplysninger i [Overvejelser ved første synkronisering](initial-sync-guidance.md)). Denne proces synkroniserer flere oplysninger fra Finans- og driftsappen, f.eks. behandlingsstatus, forsendelses- og faktureringsadresser, websteder og lagersteder.

## <a name="account-table"></a>Kontotabel

1. Angiv firmanavnet i kolonnen **Firma**, f.eks. **USMF**.
2. I kolonnen **Relationstype** skal du angive **Debitor** som en statisk værdi. Det kan være en god ide at klassificere hver enkelt kontopost som en debitor i din forretningslogik.
3. I kolonnen **Debitorgruppe-id** skal du angive debitorgruppenummeret fra Finans- og driftsappen. Standardværdien fra kundeemne til kontantløsningen er **10**.
4. Hvis du bruger kundeemne til kontantløsningen uden tilpasning af **Kontonummer**, skal du angive en værdi for **Kontonummer** i kolonnen **Partnummer**. Hvis der er tilpasninger, og du ikke kender partnummeret, skal du hente disse oplysninger fra Finans- og driftsappen.

## <a name="contact-table"></a>Tabellen Kontaktpersoner

1. Angiv firmanavnet i kolonnen **Firma**, f.eks. **USMF**.
2. Angiv følgende kolonner på baggrund af værdien **IsActiveCustomer** i CSV-filen:

    - Hvis **IsActiveCustomer** er angivet til **Ja** i CSV-filen, skal du angive kolonnen **Salgbar** til **Ja**. I kolonnen **Debitorgruppe-id** skal du angive debitorgruppenummeret fra Finans- og driftsappen. Standardværdien fra kundeemne til kontantløsningen er **10**.
    - Hvis **IsActiveCustomer** er angivet til **Nej** i CSV-filen, skal du angive kolonnen **Salgbar** til **Nej** og angive kolonnen **Kontaktperson for** til **Debitor**.

3. Hvis du bruger kundeemne til kontantløsningen uden tilpasning af **Kontaktnummer**, skal du angive følgende kolonner:

    - Overfør kontaktnummeret fra CSV-filen (**msdynce\_kontaktnummer**) til kontaktnummeret i tabellen **Kontaktperson** (**msdyn\_kontaktnummer**).
    - Brug værdier fra tabellen **Kontaktnummer** i kolonnen **Partnummer**.
    - Brug værdier fra tabellen **Kontaktnummer** i kolonnen **Kontonummer/kontaktperson-id**.

## <a name="invoice-table"></a>Tabellen Faktura

Da data fra tabellen **Faktura** er designet til at strømme én vej, fra Finans- og driftsappen til kundeengagementappen, er initialisering ikke nødvendig. Kør den første synkronisering for at overføre alle påkrævede data fra Finans- og driftsappen til kundeengagementappen. Du kan finde flere oplysninger i [Overvejelser ved første synkronisering](initial-sync-guidance.md).

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

Da data fra tabellen **Produkter** er designet til at strømme én vej, fra Finans- og driftsappen til kundeengagementappen, er initialisering ikke nødvendig. Kør den første synkronisering for at overføre alle påkrævede data fra Finans- og driftsappen til kundeengagementappen. Du kan finde flere oplysninger i [Overvejelser ved første synkronisering](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Tabellerne Tilbud og Tilbudsprodukter

For tabellen **Tilbud** skal du følge instruktionerne i afsnittet [Ordretabel](#order-table) tidligere i dette emne. For tabellen **Tilbudsprodukt** skal du følge instruktionerne i afsnittet [Tabellen Bestille produkter](#order-products-table).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
