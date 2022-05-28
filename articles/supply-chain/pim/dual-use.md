---
title: Varer med dobbelt anvendelse
description: Dette emne forklarer, hvordan du kan holde styr på produkter, der er identificeret som varer med dobbelt anvendelse, gemme certifikatnumre for hvert af de relevante produkter og destinationslande og udskrive gyldige certifikatnumre på relevante fakturaer, følgesedler og/eller salgsordrer.
author: t-benebo
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COODualUseCerts, COORules, COODualUseCountries
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 787d0c4ebcf83d6bfec05943f2bb0ddc5961a93a
ms.sourcegitcommit: e18ea2458ae042b7d83f5102ed40140d1067301a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2022
ms.locfileid: "8736027"
---
# <a name="dual-use-goods"></a>Varer med dobbelt anvendelse

[!include [banner](../includes/banner.md)]

Varer med dobbelt anvendelse er typisk varer, der har både civile og militære anvendelsesformål. Et kemikalie kan f.eks. bruges som enten gødning eller et eksplosivt stof. Mange lande har særlige regler, der gælder for eksport, import og transport af varer med dobbelt anvendelse. Det er derfor vigtigt, at virksomheder, der er involveret i den internationale samhandel med varer med dobbelt anvendelse, holder styr på de forskellige politikker og certifikater.

Funktionen til dobbelt anvendelse holder styr på produkter, der er identificeret som varer med dobbelt anvendelse, gemmer certifikatnumre for hvert af de relevante produkter og destinationslande og udskrive gyldige certifikatnumre på relevante fakturaer, følgesedler og/eller salgsordrer. Den er med til at sikre, at dine produkter altid omfatter opdaterede certificeringer, når de leveres.

Overvej på følgende scenarie:

1. Siden **Landekonfiguration ved dobbelt anvendelse** i dit system angiver, at forsendelser til Frankrig kræver en certificering.
2. Siden **Oplysninger om frigivne produkter** til produkt X-100 angiver, at det er en vare med dobbelt anvendelse. Tilsammen angiver kode, kategori, gruppe og ordning den eksportkontrolklassifikation, som produktet tilhører.
3. Siden **Certifikater ved dobbelt anvendelse** indeholder et certifikat til produkt X-100, når det sendes til Frankrig. Dette certifikat udløber 1. januar 2020.
4. D. 17. juni 2020 opretter du en salgsordre for en kunde, der bor i Frankrig, og ordren omfatter produkt X-100.
5. Når du bekræfter salgsordren, bestemmer systemet følgende oplysninger:

    1. Indeholder ordren produkter, der er varer med dobbelt anvendelse?
    2. Hvis ordren omfatter varer med dobbelt anvendelse, kræver destinationslandet så certifikater for dobbelt anvendelse?
    3. Hvis det pågældende land/område kræver certifikater for dobbelt anvendelse, findes der så et gyldigt certifikat for hver vare med dobbelt anvendelse, der kan bruges til destinationslandet?

6. Ordren omfatter produkt X-100, produktet leveres til Frankrig, og der findes et fransk certifikat for produktet. Certifikatet er dog udløbet. Derfor får du vist følgende advarselsmeddelelse: "Certifikater for dobbelt anvendelser for en eller flere varer med dobbelt anvendelse i denne salgsordre er ikke gyldige. Vil du fortsætte med bekræftelsen? "

I dette emne forklares, hvordan du kan konfigurere alle de indstillinger, der skal bruges til opsætning af varer med dobbelt anvendelse, og dette scenarie understøttes ikke.

## <a name="define-dual-use-requirements-for-each-relevant-country"></a>Definere krav for dobbelt anvendelse for hvert af de relevante lande

Forskellige lande har forskellige krav til varer med dobbelt anvendelse. Du kan bruge **Landeopsætning for dobbelt anvendelse** til at holde styr på de lande, der kræver og ikke kræver et certifikat. De oplysninger, du angiver her, kontrolleres, når du opretter salgsordrer, og du bliver påmindet om at levere de nødvendige certificeringer.

Udfør følgende trin for at angive oplysninger om krav i forbindelse med dobbelt anvendelse for forskellige lande.

1. Gå til **Administration af produktoplysninger \> Konfiguration \> Produktoverholdelse \> Produkter med dobbelt anvendelse \> Konfigurer land for dobbelt anvendelse**.
2. Vælg en eksisterende landeopsætning for at redigere den, eller vælg **Ny** i handlingsruden for at oprette en ny landeopsætning.
3. Angiv følgende værdier for det valgte eller nye landeopsætning.

    | Felt | Beskrivende tekst |
    |---|---|
    | Land/område | Vælg det land/område, du sporer krav for. |
    | Krævet certifikat | Markér dette afkrydsningsfelt for lande/områder, der kræver certificering for varer med dobbelt anvendelse. Fjern markeringen for lande/områder, der ikke kræver denne certificering. |

## <a name="create-dual-use-categories"></a>Oprette kategorier for dobbelt anvendelse

Varer med dobbelt anvendelse kategoriseres ofte i henhold til deres klassifikationsnummer for eksportkontrol (ECCN). ECCN er en alfanumerisk kode, der kategoriserer varer baseret på faktorer som f.eks. vare og teknologi. Siden **Kategorier for dobbelt anvendelse** gør det muligt at oprette en liste over de kategorier, du kan bruge, til brug ved rapportering.

Benyt følgende fremgangsmåde for at konfigurere kategorier for dobbelt anvendelse.

1. Gå til **Administration af produktoplysninger \> Konfiguration \> Produktoverholdelse \> Produkter med dobbelt anvendelse \> Kategorier for dobbelt anvendelse**.
2. Vælg en eksisterende kategori for at redigere den, eller vælg **Ny** i handlingsruden for at oprette en ny kategori.
3. Angiv følgende værdier for den valgte eller nye kategori.

    | Felter | Beskrivende tekst |
    |---|---|
    | Kode for dobbelt anvendelse | Angiv den fulde ECCN-kode (f.eks. *3A001*).|
    | Kategori for dobbelt anvendelse | Angiv kategoridelen af CCL (Commerce Control List) i ECCN-koden. F.eks. er denne værdi *3* for ECCN-koden *3A001*. |
    | Gruppe for dobbelt anvendelse | Angiv produktgruppedelen af ECCN-koden. F.eks. er denne værdi *A* for ECCN-koden *3A001*. |
    | Ordning for dobbelt anvendelse | Angiv ordningskoden for varen. Denne kode angiver årsagen til, at varen er klassificeret som en dobbelt anvendelse. F.eks. er denne værdi *001* for ECCN-koden *3A001*. |

## <a name="apply-dual-use-categories-to-products"></a>Anvend kategorier for dobbelt anvendelse på produkter

Udfør følgende trin for at identificere et produkt som et med dobbelt anvendelse og anvende en kategori med dobbelt anvendelse.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg eller opret et produkt for at åbne dets side for **Frigivne produktdetaljer**.
1. Gå til oversigtspanelet **Udenrigshandel**, angiv indstillingen **Produkter med dobbelt anvendelse** til **Ja** for at identificere det aktuelle produkt som en vare med dobbelt anvendelse.
1. Indstil feltet **Kode for dobbelt anvendelse** til den kode, der gælder for det aktuelle produkt. (Du har defineret denne kode på siden **Kategorier for dobbelt anvendelse**).

Denne opsætning kontrolleres, når du opretter en salgsordre.

## <a name="set-up-dual-use-certificates"></a>Konfigurere certifikater for dobbelt anvendelse

Du kan bruge siden **Certifikater for dobbelt anvendelse** til til at konfigurere og administrere de påkrævede certifikater for dobbelt anvendelse for hvert produkt og land/område. Du kan spore hvert certifikats detaljer, f.eks. landet og gyldighedsdatoerne. Du kan også angive indstillinger for, hvor disse oplysninger skal udskrives. Oplysningerne kan f.eks. udskrives på fakturaen, følgesedlen og/eller salgsordren. Denne opsætning kontrolleres, når du opretter en salgsordre.

1. Gå til **Administration af produktoplysninger \> Konfiguration \> Produktoverholdelse \> Produkter med dobbelt anvendelse \> Certifikater for dobbelt anvendelse**.
2. Vælg en eksisterende certifikatopsætning for at redigere den, eller vælg **Ny** i handlingsruden for at oprette et nyt certifikat.
3. Angiv følgende værdier for det valgte eller nye certifikat.

    | Felt | Beskrivende tekst |
    |---|---|
    | varenummer | Vælg varenummeret for varen med dobbelte anvendelse, som dette certifikat gælder for. |
    | Land/område | Det destinationsland eller -område, hvor du skal bruge dette certifikat. |
    | Certifikatnummer | Det nummer, der vises på det certifikat, der er udstedt til kreditoren eller debitoren. |
    | Gyldig fra | Vælg den første dato, hvor det aktuelle certifikat er gyldigt.|
    | Udløb | Vælg den sidste dato, hvor det aktuelle certifikat er gyldigt. |
    | Udskriv på faktura | Markér dette afkrydsningsfelt for at udskrive certifikatnummeret på de fakturaer, der er adresseret til det angivne land/område i det angivne datointerval. |
    | Udskriv på følgeseddel | Markér dette afkrydsningsfelt for at udskrive certifikatnummeret på følgesedler, der er adresseret til det angivne land/område i det angivne datointerval. |
    | Udskriv på salgsordre | Markér dette afkrydsningsfelt for at udskrive certifikatnummeret på de salgsordrer, der er adresseret til det angivne land/område i det angivne datointerval. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
