---
title: Oprindelsesland
description: Mange organisationer udsteder certifikater til deres leverandører for at sikre, at produkterne opfylder bestemte certificeringsstandarder. Disse certifikater afhænger ofte af oprindelseslandet. Dette emne indeholder oplysninger om oprindelseslandsfunktionen, som giver dig mulighed for at sammenkæde et produkt med oprindelseslandet og holde styr på dets produktcertificeringer.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0471785991a307de11147e9773d9abe1e02941d6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424292"
---
# <a name="country-of-origin"></a>Oprindelsesland

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Mange organisationer udsteder certifikater til deres leverandører for at sikre, at produkterne opfylder bestemte certificeringsstandarder. Disse certifikater afhænger ofte af oprindelseslandet. Oprindelseslandet giver dig mulighed for at sammenkæde et produkt med dets oprindelsesland og holde styr på dets produktcertificeringer.

## <a name="turn-on-the-country-of-origin-feature"></a>Aktivere funktionen for oprindelsesland

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Administration af produktoplysninger*
- **Funktionsnavn:** *Administrationsfunktion for oprindelsesland*

## <a name="configure-source-and-destination-countries"></a>Konfigurere kilde- og destinationslande

Før du udsteder et certifikat for et produkt, skal du knytte produktet til destinationslandet og oprindelseslandet.

1. Gå til **Administration af produktoplysninger \> Konfiguration \> Produktoverholdelse \> Oprindelsesland \> Regler for oprindelsesland**.
2. Vælg en eksisterende landeopsætning, du vil redigere, eller vælg **Ny** i handlingsruden for at oprette en ny landeopsætning.
3. Angiv følgende værdier for det valgte eller nye land/område.

    | Felt | Beskrivende tekst |
    |---|---|
    | varenummer | Vælg varenummeret for produktet. |
    | Destinationsland | Vælg det land/område, du sender produktet til. |
    | Oprindelsesland | Vælg det land/område, du sender produktet fra. |

Formålet med denne konfiguration er at hjælpe dig med at generere en styklisterapport, hvor du kan medtage oprindelsesland for hver del, som kilde- og destinationslandene er angivet for. Denne rapport kan hjælpe dig med at få et holistisk billede af, hvor dine dele kommer fra, og hvor de befinder sig.

## <a name="keep-track-of-vendor-certificates"></a>Holde styr på kreditorcertifikater

Du kan bruge siden **Oprindelsesland for keditorcertifikater** til at holde styr på certifikater, som du udsteder til kreditorer.

Du skal beslutte, hvilke certifikatdokumenter du er ved at udstede, og hvordan du vil rapportere dem til kunderne. Denne funktion hjælper dig med at holde styr på dine certifikater. Du kan også vælge, om de relevante certifikatnumre skal vises på fakturaer, følgesedler og/eller ordrebekræftelser.

Benyt følgende fremgangsmåde for at konfigurere dine certifikatoplysninger.

1. Gå til **Administration af produktoplysninger \> Konfiguration \> Produktoverholdelse \> Oprindelsesland \> Regler for oprindelsesland for kreditorcertifikater**.
2. Vælg en eksisterende certifikatopsætning, du vil redigere, eller vælg **Ny** i handlingsruden for at oprette en ny certifikatopsætning.
3. Angiv følgende indstillinger for det valgte eller nye certifikat.

    | Felt | Beskrivende tekst |
    |---|---|
    | Kreditorkonto | Vælg den kreditor, du har udstedt certifikatet til. |
    | varenummer | Vælg den vare, du har udstedt certifikatet for. |
    | Land/område | Det destinationsland eller -område, hvor du skal bruge dette certifikat. |
    | Certifikatnummer | Angiv id-nummeret på det certifikat, du har udstedt. |
    | Gyldig fra | Vælg den første dato, hvor det aktuelle certifikat er gyldigt.|
    | Udløb | Vælg den sidste dato, hvor det aktuelle certifikat er gyldigt. |
    | Udskriv på faktura | Markér dette afkrydsningsfelt for at udskrive certifikatnummeret på de fakturaer, der er adresseret til det angivne land/område i det angivne datointerval. |
    | Udskriv på følgeseddel | Markér dette afkrydsningsfelt for at udskrive certifikatnummeret på følgesedler, der er adresseret til det angivne land/område i det angivne datointerval. |
    | Udskriv på salgsordre | Markér dette afkrydsningsfelt for at udskrive certifikatnummeret på de salgsordrer, der er adresseret til det angivne land/område i det angivne datointerval. |

## <a name="include-the-country-of-origin-on-bom-reports"></a>Medtag oprindelseslandet på styklisterapporter

Når du genererer en styklisterapport, kan du medtage oprindelseslandet for hver del, som du har angivet kilde- og destinationslande for, på siden **Regler for oprindelsesland**.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg eller opret et produkt for at åbne dets side for **Frigivne produktdetaljer**.
1. Gå til handlingsruden, og vælg **Designer** i gruppen **Stykliste** under fanen **Tekniker**.
1. På den side, der vises, skal du i handlingsruden vælge **Stykliste \> Udskriv**.
1. I dialogboksen **Styklistelinjer** skal du angive feltet **Destinationsland** til det destinationsland, du vil have vist i rapporten.
1. Vælg **OK**.

En rapport, der viser oplysninger om de enkelte deles oprindelsesland, genereres og vises. Her er et eksempel på rapporten.

![Rapport om oprindelsesland](media/country-of-origin-report.png "Rapport om oprindelsesland")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]