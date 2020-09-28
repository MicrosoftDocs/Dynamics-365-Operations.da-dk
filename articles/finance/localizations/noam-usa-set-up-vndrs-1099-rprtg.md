---
title: Konfigurere kreditorer til 1099-rapportering
description: Dette emne forklarer, hvordan du konfigurerer kreditorposter, så der knyttes en 1099-rubrik til en hovedkonto.
author: v-kiarnd
manager: Ann Beebe
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNCanadianHSTTaxFeature
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: v-kiarnd
ms.search.validFrom: 2020-8-03
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: fff04a8259165cdfb1bd6c56932f103a34881a68
ms.sourcegitcommit: d6b17b9bafa84b574a597a560a80e6b7b1852b14
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/12/2020
ms.locfileid: "3799992"
---
# <a name="set-up-vendors-for-1099-reporting"></a>Konfigurere kreditorer til 1099-rapportering

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du konfigurerer kreditorposter, så der knyttes en 1099-rubrik til en hovedkonto. Det anbefales, at du fuldfører disse opsætningstrin, før du bogfører kreditorposteringer. Du kan finde flere oplysninger under [1099-rapportering ved årsafslutning](noam-usa-year-end-1099-reporting.md).

> [!NOTE]
> Det anbefales, at du gennemgår det amerikanske skattevæsens (IRS) regelændringer for det pågældende skatteår, før du opretter og behandler 1099-opgørelser.

Benyt følgende fremgangsmåde for at konfigurere kreditorer til 1099-rapportering.

1. Gå til **Kreditor \> Kreditorer \> Alle kreditorer** eller **Indkøb og forsyning \> Generelt \> Kreditorer \> Alle kreditorer**.
2. Vælg en kreditorkonto.
3. I oversigtspanelet **1099-skat** skal du vælge indstillingen **Rapport 1099** for at medtage posterings- og 1099-oplysninger for kreditoren i 1099-rapporten. Hvis denne indstilling ikke er valgt, indgår 1099-oplysningerne for kreditoren ikke i 1099-opgørelsen, og de elektroniske eller magnetiske filer indeholder ikke beløb for kreditoren.
4. Indtast skatteyder-id'et for kreditoren i feltet **Federal Tax ID (USA)**. Vælg derefter den type moms-id, du lige har angivet, i feltet **1099-nummertype**.

    > [!NOTE]
    > Sikkerhedsrettighederne **Undgå dubletter af momsregistreringsnummeret** bestemmer, om du kan angive en skatteyders identifikationsnummer, der allerede bruges i en anden kreditorpost.

5. I feltet **Rubrik i 1099** skal du angive den standardværdi, der vises på hver posteringslinje, der oprettes for kreditoren. Denne indstilling er påkrævet, så posteringer for kreditoren kan medtages i 1099-opgørelsen og i de elektroniske eller magnetiske mediefiler.
6. Vælg indstillingen **Indikator for udenlandsk enhed**, hvis kreditororganisationen ejes af en enhed uden for USA.
7. Markér afkrydsningsfeltet **Andet TIN (Taxpayer Identification Number - US)**, hvis din organisation to gange i løbet af tre kalenderår har fået besked om, at kreditoren har angivet et forkert navn.
8. I feltet **Det navn, der skal angives på 1099-blanketten** skal du vælge **Kreditornavn**. Hvis kreditoren bruger et alternativt navn, kan du vælge **DBA (Doing Business As)**. Hvis dette er tilfældet, skal du angive det alternative navn i **DBA**-feltet.
9. Angiv i feltet **Navnekontrol** det alfanumeriske navnekontrol-id, som IRS kræver skal være udskrevet på mail-etiketten til validering af kreditorens EIN (Employer Identification Number).
10. Vælg indstillingen **CUSIP** for at angive, at CUSIP-identifikationsnummeret (Committee on Uniform Security Identification Procedures) gælder for gældsinstrumentet.
11. I feltet **CUSIP-id** skal du angive det alfanumeriske CUSIP-nummer på ni tegn for at identificere gældsinstrumentet.
12. I feltet **CUSIP-detaljer** skal du angive forkortelsen for børs og udsteder, obligationsrente og indløsningsår.

    > [!NOTE]
    > Du kan kun angive CUSIP-oplysningerne, hvis afkrydsningsfeltet **CUSIP** ikke er markeret.

13. Skriv navnene på den nominelle ejer og udstederen i feltet **Oplysninger om nominel ejer**.
14. Vælg typen af investor i feltet **Investortype**:

    - **None**
    - **Ejer** – Investoren er ejeren af gældsinstrumentet.
    - **Nominel ejer/mægler** – Investoren er en mægler, der repræsenterer ejeren af gældsinstrumentet.

15. I handlingsruden under fanen **Kreditor** skal du i gruppen **Konfiguration** vælge **Kreditors 1099-numre på statsniveau**.
16. Opret en ny post for hver stat, hvor kreditoren modtager betalinger fra din organisation. Angiv forbundsskat-id. Vælg også 1099-nummertypen, hvis der findes oplysninger om skatte-id'et.
17. Hvis der tilbageholdes lokal indkomstskat i årets løb, skal du markere afkrydsningsfeltet **Tilbageholdt indkomstskat på lokalt niveau**.
18. Luk de forskellige sider for at gemme ændringerne.

## <a name="associate-a-1099-default-value-with-a-main-account"></a>Knytte en 1099-standardværdi til en hovedkonto

Nogle af de fakturalinjer, der er identificeret for de føderale myndigheders 1099-rapportering, kan rapporteres for en anden 1099-rubrik end leverandørens standardrubrik. Da leverandører kan modtage betalinger, der korreleres med flere rubrikker i 1099, er det bedst at bruge en hovedkonto på en linje til en finansieringsfordeling. Denne fremgangsmåde sikrer ensartet rapportering af betalinger til en bestemt 1099-rubrik. Du kan nu genberegne værdierne for 1099-rubrikken for kreditorerne, så de akkumulerede saldi rapporteres metre præcist til det amerikanske skattevæsen (IRS).

> [!NOTE]
> 1099-rubrikken og beløbet kan kun udfyldes på fakturaen, hvis afkrydsningsfeltet **Rapport 1099** er markeret i oversigtspanelet **1099-skat** på siden kreditordetaljer.

1. Gå til **Kreditor \> Periodiske opgaver \> 1099-skat \> Tilknytning af 1099-hovedkonto**.
2. Vælg den hovedkonto, der skal relateres til en 1099-rubrik, i feltet **Hovedkontonummer**. Du kan kun vælge en hovedkonto af **Udgift**-typen.
3. I feltet **1099-rubrik** skal du vælge den rubrikkode i 1099-formularen, som beløb, der bogføres på den valgte hovedkonto, skal tilknyttes.
4. Gentag de foregående trin for at tilføje eventuelle andre hovedkonti, der skal bruges.

## <a name="update-1099-boxes-and-amounts"></a>Opdatere 1099-rubrikker og -beløb

Du kan opdatere 1099-rapporteringers rubrikker og beløb for alle betalte fakturaer for et kalenderår på baggrund af den aktuelle tildeling af hovedkonti til 1099-rubrikker.

1. Gå til **Kreditor \> Periodiske opgaver \> 1099-skat \> Opdater 1099-oplysninger efter hovedkonto**.
2. Vælg et datointerval og en kreditor, og vælg derefter **OK**.
3. Vælg **OK** for at opdatere 1099-saldiene baseret på hovedkontoen, som bruges til kreditorens bogførte og betalte fakturaer.

Systemet evaluerer alle kreditorer, hvor indstillingen **Rapport 1099** er valgt. Derefter evalueres alle kreditorfakturaerne. Beløbet for 1099 genberegnes på basis af hovedkontiene på hver linje, herunder alle linjer, der har opdelte fordelinger. Hvis linjens fuldt betalte beløb ikke er knyttet til 1099-rubrikken, er linjen ikke medtaget i 1099-beløbet, som vist i følgende eksempler:

- Leverandørens standardværdi for 1099-rubrikken er forskellig fra den værdi, der er angivet på fakturalinjen.

    Hvis én linje på en kreditorfaktura bruger en hovedkonto, der er tilknyttet 1099-rubrik 7, og 1099-standardrubrikken for kreditoren er et andet nummer, vil standardangivelsen for kreditoren og det beløb, der skal rapporteres for den, blive genberegnet for 1099-rubrik 7.

- Ikke alle fakturalinjer har 1099-rubrikværdier.

   Hvis én linje på en kreditorfaktura bruger en hovedkonto, der er tilknyttet 1099-rubrik 7, og en anden linje bruger en hovedkonto, der ikke er tilknyttet en 1099-rubrik, vil standardangivelsen for kreditoren og det beløb, der skal rapporteres for den, blive genberegnet for 1099-rubrik 7.

- Fakturalinjer har forskellige 1099-rubrikværdier.

     Hvis én linje på en kreditorfaktura bruger en hovedkonto, der er tilknyttet 1099-rubrik 7, og en anden linje bruger en hovedkonto, der er tilknyttet 1099-rubrik 1, vil systemet ignorere standardangivelsen for kreditoren, og 1099-beløbet vil blive genberegnet for de tilknyttede hovedkonti.

- Fakturaen har opdelte fordelinger.

    Hvis en kreditorfaktura indeholder en linje med opdelt fordeling, genberegnes standardangivelsen for kreditoren for den 1099-rubrik, der er tilknyttet den hovedkonto, der bruges i fordelingerne.

> [!NOTE]
> Der er føjet en ny kolonne med navnet **Oprettet af 1099-opdateringsprocessen** til siden **1099-skat transaktioner**. Afkrydsningsfelterne i denne kolonne er markeret for at vise, at den nye opdateringsproces har opdateret 1099-saldoen. Hvis afkrydsningsfeltet for en række ikke er markeret, blev standardfunktionaliteten brugt til at oprette posteringen. Hvis du vil åbne siden **1099-skat transaktioner**, skal du gå til **Kreditor \> Periodiske opgaver \> Kreditorudligning for 1099 \> 1099-kreditor transaktioner**. Du kan også gå til **Kreditor \> Kreditorer \> Alle kreditorer**. Vælg en kreditor, og brug derefter fanen **Kreditor** i handlingsruden til i gruppen **Skatteoplysninger** at vælge **Kreditorudligning for 1099 \> 1099-kreditor transaktioner**.
