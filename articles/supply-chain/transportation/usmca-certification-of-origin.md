---
title: USMCA-certificering af oprindelse
description: Denne funktion giver dig mulighed for at udskrive certificeringen af oprindelsesdokumenter, der kræves af USA-Mexico-Canada-aftalen (USMCA).
author: Henrikan
manager: tfehr
ms.date: 10/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-23
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: a0395f74065cf656e286186d619824d88836c45a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233289"
---
# <a name="usmca-certification-of-origin"></a>USMCA-certificering af oprindelse

[!include [banner](../includes/banner.md)]

Denne funktion giver dig mulighed for at udskrive certificeringen af oprindelsesdokumenter, der kræves af USA-Mexico-Canada-aftalen (USMCA).

*USMCA-certificeringen for oprindelsesdokument* indeholder de dataelementer, der som minimum kræves til erklæringen. Nogle dataelementer kan være udfyldt før udskrivningen, mens andre skal udfyldes manuelt efter udskrivningen. For at erhverve en præferencetarifbehandling skal dokumentet være udfyldt og i importørens besiddelse på det tidspunkt, hvor erklæringen udfærdiges. Dokumentet kan udfyldes af importøren, eksportøren eller producenten.

Du kan udskrive dokumentet for en enkelt forsendelse fra **Alle forsendelser**-listesiden eller fra siden **Forsendelsesoplysninger**.

Dokumentet er kun tilgængeligt, når landet på den juridiske enheds primære adresse er USA.

Afhængigt af dokumentets udskriftsvalg kan dokumentet være forhåndsudfyldt med data fra systemet. Det er muligt at ændre eller tilføje data i det udskrevne dokument ved at eksportere det udskrevne dokument til et format, der kan redigeres, f.eks. Microsoft Word. Når du har eksporteret, kan du anvende eventuelle nødvendige ændringer, før du opretter en erklæring.

## <a name="turn-on-the-usmca-feature"></a>Slå USMCA-funktionen til

Før du kan bruge USMCA-funktionen, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Module** *Transportstyring*
- **Funktionsnavn:** *USMCA-certificering af oprindelsesdokument*

## <a name="document-content"></a>Indhold af dokument

USMCA-certificeringen af oprindelsesdokumentet indeholder følgende dataelementer:

- Adresseelementer
- Den certificerende parts rolle
- Enkelt forsendelse
- Fakturaer
- Rammeperiode
- Vareoplysninger
- Certificerendes signatur
- Antal sider

Yderligere oplysninger om hvert af disse elementer og om, hvordan deres værdier findes, finder du i de resterende afsnit i dette emne.

## <a name="print-a-usmca-certification-of-origin-document"></a>Udskrive en USMCA-certificering af oprindelsesdokument

Benyt følgende fremgangsmåde for at udskrive en USMCA certificering af oprindelsesdokument for en forsendelse:

1. Benyt en af følgende fremgangsmåder:
    - Gå til **Transportstyring > Forsendelser > Alle forsendelser**, og vælg den forsendelse, du vil udskrive dokumentet for.
    - Åbn siden **Forsendelsesdetaljer** for den forsendelse, du vil udskrive dokumentet for (der er flere måder at nå hertil, herunder på siden **Alle forsendelser**).
1. Åbn fanen **Forsendelser** i handlingsruden, og vælg **USMCA-oprindelsescertifikat** i gruppen **Udskriv**.
1. Dialogboksen **Certifikat eller oprindelse** åbnes. Foretag de indstillinger, der beskrives i følgende underafsnit, og vælg derefter **OK** for at generere dokumentet.
1. Der åbnes en forhåndsvisning af dokumentet. Brug de kommandoer, der er tilgængelige i handlingsruden, til at udskrive eller eksportere dokumentet efter behov.

### <a name="certifying-party"></a>Certificeringspart

Brug rullelisten **Certificeringspart** til at identificere den type part, dokumentet udskrives af. Angiv, om certificeringsparten er *Eksportør*, *Eksportøren og producenten*, *Producent* eller *Importør*, eller lad feltet være tomt, hvis certificeringsparten ikke er nogen af disse. Den indstilling, du vælger, bestemmer, hvad der udskrives i adressesektionen af dokumentet.

Den **Certificeringspart**, som du vælger, vil blive medtaget i det udskrevne dokument.

Dokumentet kan udskrives for både indgående og udgående forsendelser. Vælg *Importør* som **Certificeringspart** for indgående forsendelser.

I følgende tabel beskrives de typer oplysninger, der findes i dokumentet baseret på den **Certificeringspart**, du vælger.

| Certificeringspart | Beskrivelse |
|---|---|
| *\[Tom\]* | Føjer følgende detaljer til dokumentet:<ul><li>**Oplysninger om certificerende**: Brug adresseoplysningerne for forsendelseslagerstedet, hvis de er tilgængeligt. Ellers bruges adressen til forsendelsesstedet, hvis det er tilgængeligt. Ellers bruges adressen på den juridiske enhed (firma), der er valgt i Supply Chain Management.</li><li>**Oplysninger om eksportør**: Tom</li><li>**Oplysninger om producent**: Tom</li><li>**Oplysninger om importør**: Tom</li><ul>|
| *Eksportør* | Føjer følgende detaljer til dokumentet:<ul><li>**Oplysninger om certificerende**: Brug adresseoplysningerne for forsendelseslagerstedet, hvis de er tilgængeligt. Ellers bruges adressen til forsendelsesstedet, hvis det er tilgængeligt. Ellers bruges adressen på den juridiske enhed (firma), der er valgt i Supply Chain Management.</li><li>**Oplysninger om eksportør**: Bruger adresseoplysningerne for den juridiske enhed.</li><li>**Oplysninger om producent**: Tom</li><li>**Oplysninger om importør**: Bruger fakturakontoen til den relaterede salgsordre.</li><ul>|
| *Eksportør og producent* | Føjer følgende detaljer til dokumentet:<ul><li>**Oplysninger om certificerende**: Brug adresseoplysningerne for forsendelseslagerstedet, hvis de er tilgængeligt. Ellers bruges adressen til forsendelsesstedet, hvis det er tilgængeligt. Ellers bruges adressen på den juridiske enhed (firma), der er valgt i Supply Chain Management.</li><li>**Oplysninger om eksportør**: Bruger adresseoplysningerne for den juridiske enhed.</li><li>**Oplysninger om producent**: Bruger adresseoplysningerne for den juridiske enhed.</li><li>**Oplysninger om importør**: Bruger fakturakontoen til den relaterede salgsordre.</li><ul>|
| *Importør* | Føjer følgende detaljer til dokumentet:<ul><li>**Oplysninger om certificerende**: Brug adresseoplysningerne for forsendelseslagerstedet, hvis de er tilgængeligt. Ellers bruges adressen til forsendelsesstedet, hvis det er tilgængeligt. Ellers bruges adressen på den juridiske enhed (firma), der er valgt i Supply Chain Management.</li><li>**Oplysninger om eksportør**: Tom</li><li>**Oplysninger om producent**: Tom</li><li>**Oplysninger om importør**: Bruger adresseoplysningerne for den juridiske enhed.</li><ul>|
| *Producent* | Føjer følgende detaljer til dokumentet:<ul><li>**Oplysninger om certificerende**: Brug adresseoplysningerne for forsendelseslagerstedet, hvis de er tilgængeligt. Ellers bruges adressen til forsendelsesstedet, hvis det er tilgængeligt. Ellers bruges adressen på den juridiske enhed, der er valgt i Supply Chain Management.</li><li>**Oplysninger om eksportør**: Tom</li><li>**Oplysninger om producent**: Bruger adresseoplysningerne for den juridiske enhed.</li><li>**Oplysninger om importør**: Tom</li><ul>|

### <a name="has-various-producers"></a>Har forskellige producenter

Rullelisten **Certificeringspart** kontrollerer den tekst, der skal bruges til producentoplysningerne i dokumentet. Vælg en af følgende muligheder:

- *Diverse producenter* - Udskriver teksten "Diverse" i oplysningerne om producenten.
- *Tilgængelig på anmodning* - Udskriver teksten "Tilgængelig efter anmodning fra importmyndighederne" i oplysningerne om producenten.

Når **Certificeringspart** er angivet til *Eksportør og producent* eller *Producent*, overstyres **Har forskellige producenter**-indstillingen, og producentens adressedetaljer vil være de samme som certificeringsparten.

### <a name="blanket-period"></a>Rammeperiode

Du kan bruge indstillingerne **Rammeperiode fra** og **Rammeperiode til** til at oprette en rammeperiode, hvor dokumentet skal dække flere forsendelser af identiske varer, selvom dokumentet kun udskrives til én forsendelse. Du kan angive rammeperiodens datoer uden begrænsninger, og den vil blive føjet til dokumentet. Du kan også lade disse indstillinger være tomme eller angive dem i fortiden.

### <a name="is-single-shipment"></a>Er enkelt forsendelse

I dialogboksen **Oprindelsescertifikat** skal du angive **Er enkelt forsendelse** til en af følgende:

- *Ja* - Tilføjer "Enkelt forsendelse: Ja" ved siden af fakturanummeret.
- *Nej* - Tilføjer intet.

## <a name="other-information-included-in-the-document"></a>Andre oplysninger, der findes i dokumentet

Ud over de valgfrie elementer, som du vælger i dialogboksen **Certifikat eller oprindelse**, indeholder USMCA-certificeringen af oprindelsesdokumentet oplysningerne og de brugerdefinerede felter, der er opsummeret i følgende underafsnit. Nogle af disse oplysninger skal angives manuelt, når du har oprettet dokumentet.

### <a name="invoice-number"></a>Fakturanummer

Id'erne for salgsfakturaer, der er relateret til forsendelser, udskrives på dokumentet uanset rammeperioden. Fakturanumre udskrives, uanset om der vælges **Er enkelt forsendelse**.

### <a name="item-details"></a>Vareoplysninger

Dokumentet indeholder flere sektioner med liste over specifikke varedetaljer:

- **SKU-nummer** : Udskriver varenummeret for det frigivne produkt.

- **Beskrivelse**: Udskriver enten beskrivelsen af eller navnet på det frigivne produkt. Hvis der findes en beskrivelse på brugerens sprog, udskrives den. Hvis der ikke findes en sådan beskrivelse, udskrives navnet på brugerens sprog. Hvis dette navn ikke findes, udskrives varenavnet.

- **Harmoniseret systems (HS) tarifklassifikation**: Udskriver den harmoniserede tarifplan, der er knyttet til produktet. Du kan oprette disse planer ved at gå til **Transportstyring \> Konfiguration \> Transportstandard \> Harmoniserede tarifplaner**.

- **Oprindelseskriterium:** Du skal angive data i dette afsnit manuelt, første gang du frigiver dokumentet.

- **Oprindelsesland:** Udskriver oprindelseslandet, som du anvender ved at gå til **Administration af produktoplysninger \> Konfiguration \> Produktoverholdelse \> Oprindelsesland** (se også [Oprindelsesland](../pim/country-of-origin.md)). ISO-koden for oprindelseslandet udskrives på basis af destinationens land/område i forsendelsens leveringsadresse og varen. Hvis der ikke er oprettet nogen oprindelseslandsdata, vender denne værdi tilbage til den indstilling, der blev fundet i **Frigivet produkt \> Udenrigshandel \> Oprindelse**. Hvis der stadig ikke findes noget data om oprindelsesland, skal du angive oprindelseslandet manuelt efter genereringen af dokumentet.

### <a name="certifier-signature-and-date"></a>Bekræfter signatur og dato

Du skal angive dette manuelt, når du har genereret dokumenterne.

### <a name="consists-of-number-of-pages"></a>Består af antal sider

Den bruger, der signerer certificeringen, skal manuelt angive antallet af sider (til bekræftelse), efter at dokumentet er blevet genereret.

### <a name="page-numbers"></a>Sidenumre

Aktuel side og antal sider udskrives nederst i dokumentet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]