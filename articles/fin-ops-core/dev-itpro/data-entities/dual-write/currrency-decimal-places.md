---
title: Migrering af valutadatatype til dobbeltskrivning
description: Denne artikel indeholder en beskrivelse af, hvordan du kan ændre det antal decimaler, som dobbeltskrivning understøtter for valuta.
author: RamaKrishnamoorthy
ms.date: 12/08/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 327d6ced7fca4bdae1fd80928086dafed6b0f931
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289708"
---
# <a name="currency-data-type-migration-for-dual-write"></a>Migrering af valutadatatype til dobbeltskrivning

[!include [banner](../../includes/banner.md)]



Du kan øge antallet af decimaler, der understøttes for valutaværdier, til højst 10. Standardgrænsen er fire decimaler. Ved at øge antallet af decimaler undgår du datatab, når du bruger dobbeltskrivning til synkronisering af data. Stigningen i antallet af decimaler er et tilvalg. Hvis du vil implementere den, skal du bede Microsoft om hjælp.

Ændring af antallet af decimaler har to trin:

1. Anmod om migrering fra Microsoft.
2. Ret antallet af decimaler i Dataverse.

Programmer til finans og drift og Dataverse skal understøtte det samme antal decimaler i valutaværdier. Ellers kan der opstå datatab, når disse oplysninger synkroniseres mellem apps. Migreringsprocessen konfigurerer den måde, værdierne for valuta og valutakurs gemmes på, men den ændrer ikke nogen data. Når migreringen er fuldført, kan antallet af decimaler for valutakoder og prisfastsættelse øges, og de data, som brugerne indtaster og ser, kan have større decimalpræcision.

Migrering er valgfri. Hvis du kan få fordel ved understøttelse af flere decimaler, anbefales du at overveje migrering. Organisationer, der ikke har brug for værdier med mere end fire decimaler, behøver ikke at overføre data.

## <a name="requesting-migration-from-microsoft"></a>Anmodning om migrering fra Microsoft

Lager til eksisterende valutakolonner i Dataverse understøtter ikke mere end fire decimalpladser. Under migreringsprocessen kopieres valutaværdier derfor til nye interne kolonner i databasen. Denne proces foregår løbende, indtil alle data er overført. Internt i slutningen af migreringen erstatter de nye lagertyper de gamle lagertyper, men dataværdierne er uændrede. Valutakolonnerne kan derefter understøtte op til ti decimaler. Under migreringsprocessen kan Dataverse fortsat blive brugt uden afbrydelser.

På samme tid ændres valutakurserne, så de understøtter op til 12 decimaler i stedet for den aktuelle grænse på 10. Denne ændring er påkrævet, så antallet af decimaler er det samme i både program til finans og drift og Dataverse.

Migrering ændrer ikke nogen data. Når kolonnerne for valuta og valutakurs konverteres, kan administratorer konfigurere systemet til at bruge op til ti decimaler for valutakolonner ved at angive antallet af decimaler for hver transaktionsvaluta og for prisfastsættelse.

### <a name="request-a-migration"></a>Anmode om en migrering

Hvis du vil gøre denne funktion tilgængelig, skal du sende en email til **CDSExpandDecimal@microsoft.com** og medtage følgende oplysninger:

+ **Emne:** Anmodning om at aktivere udvidet decimalunderstøttelse for \<organizationID\>
+ **Brødtekst:** Jeg vil gerne aktivere udvidet decimalunderstøttelse for min organisation \<organizationID\>.

En Microsoft-repræsentant vil kontakte dig inden for to til tre arbejdsdage angående de næste trin.

Når du anmoder om en migrering, skal du være opmærksom på følgende oplysninger og planlægge i overensstemmelse hermed:

+ Den tid, der kræves til at overføre dataene, afhænger af mængden af data i systemet. Det kan tage flere dage at overføre store databaser.
+ Størrelsen på databasen øges midlertidigt, mens migreringen kører, fordi der skal bruges yderligere plads til indeks. Det meste af den ekstra plads frigøres, når migreringen er fuldført.
+ Hvis der opstår fejl under migreringsprocessen, og det forhindrer, at migreringen fuldføres, udløser systemet beskeder til Microsoft Support, så supportpersonalet kan gribe ind. Men selvom der opstår fejl under migreringen, forbliver Dataverse fuldt tilgængeligt for almindelig brug.
+ Migreringsprocessen kan ikke fortrydes.

## <a name="changing-the-number-of-decimal-places"></a>Ændring af antal decimaler

Når migreringen er fuldført, kan Dataverse gemme tal, der har flere decimaler. Administratorer kan vælge, hvor mange decimaler der skal bruges til bestemte valutakoder og til prisfastsættelse. Brugere af Microsoft Power Apps, Power BI og Power Automate kan derefter se og bruge tal, der har flere decimaler.

Hvis du vil foretage denne ændring, skal du opdatere følgende indstillinger i Power Apps:

+ **Systemindstillinger: valutapræcision for prisfastsættelse** – Kolonnen **Vælg den valutapræcision, der bruges til prissætning i hele systemet** definerer, hvordan valutaen fungerer for organisationen, når **Prissætningsnøjagtighed** er valgt.
+ **Forretningsstyring: valutaer** – I kolonnen **Valutapræcision** kan du angive et brugerdefineret antal decimaler for en bestemt valuta. Der er reserve i indstillingen for hele organisationen.

Der er nogle begrænsninger:

+ Du kan ikke konfigurere valutakolonnen i en tabel.
+ Du kan kun angive fire decimaler på niveauerne **Prisfastsættelse** og **Transaktionsvaluta**.

### <a name="system-settings-currency-precision-for-pricing"></a>Systemindstillinger: valutapræcision for prisfastsættelse

Når migreringen er fuldført, kan administratorer angive valutapræcisionen. Gå til **Indstillinger \> Administration**, og vælg **Systemindstillinger**. Under fanen **Generelt** skal du ændre værdien af kolonnen **Vælg den valutapræcision, der bruges til prissætning i hele systemet**, som vist i følgende illustration.

![Systemindstillinger for valuta.](media/currency-system-settings.png)

### <a name="business-management-currencies"></a>Forretningsstyring: valutaer

Hvis du kræver, at valutapræcisionen for en bestemt valuta er forskellig fra den valutapræcision, der bruges til prisfastsættelsen, kan du ændre den. Gå til **Indstillinger \> Forretningsstyring**, vælg **Valutaer**, og vælg den valuta, der skal ændres. Angiv derefter kolonnen **Valutapræcision** til det antal decimaler, du ønsker, som vist i følgende illustration.

![Valutaindstillinger for en bestemt landestandard.](media/specific-currency.png)

### <a name="tables-currency-column"></a>Tabeller: valutakolonne

Det antal decimaler, der kan konfigureres for bestemte valutakolonner, er begrænset til fire.

### <a name="default-currency-decimal-precision"></a>Decimalpræcision i standardvaluta
Se følgende tabel for den forventede funktionsmåde af standardvalutaens decimalpræcision i overflytnings- og ikke-overflytningsscenarier. 

| Oprettelsesdato  | Feltet valutadecimal    | Eksisterende organisation (feltet Valuta er ikke overflyttet) | Eksisterende organisation (feltet Valuta er overflyttet) | Ny organisation oprettet efter build 9.2.21062.00134 |
|---------------------------------------------------------|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|------------------------------------------------|
| Valutafelt oprettet før build 9.2.21111.00146  |     |  |       |
|    | Maksimal præcision synlig i brugergrænsefladen   | Fire cifre    | Ti cifre    | I/T    |
| | Maksimal præcision synlig i brugergrænsefladen til database og databaseforespørgsler         | Fire cifre   | Ti cifre   | I/T    |
| Valutafelt oprettet før efter 9.2.21111.00146 |    |  |     |   |
|   | Maksimal decimalpræcision synlig i brugergrænsefladen     | Fire cifre   | Ti cifre   | Ti cifre     |
|          | Maksimal decimalpræcision synlig i brugergrænsefladen til database og databaseforespørgsler | Ti cifre. Men det er kun fire, der er betydende med alle nuller ud over de fire decimaler. Dette giver en simplere og hurtigere overflytning af organisationen, hvis det er nødvendigt. | Ti cifre      | Ti cifre     |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

