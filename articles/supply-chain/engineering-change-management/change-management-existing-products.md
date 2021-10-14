---
title: Aktivér administration af ændringer på eksisterende produkter
description: Dette emne forklarer, hvordan du aktiverer ændringsstyring for eksisterende produkter. Det beskriver også tilfælde, hvor muligheden for at aktivere ændringsstyring er begrænset.
author: t-benebo
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-02
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f0fba0a9234e5b7cb055f7b97578bff72f1d06ac
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571971"
---
# <a name="enable-change-management-on-existing-products"></a>Aktivér administration af ændringer på eksisterende produkter

[!include [banner](../../includes/banner.md)]

Dette emne forklarer, hvordan du aktiverer ændringsstyring for eksisterende produkter. Det beskriver også tilfælde, hvor muligheden for at aktivere ændringsstyring er begrænset.

Når du aktiverer ændringsstyring for et eksisterende produkt, kan du oprette versioner af det pågældende produkt og spore de ændringer, der er foretaget af det, i hele dets levetid. Du kan derfor spore disse ændringer ved hjælp af ændringsordrer. Hvis du vil aktivere ændringsstyring, skal du konvertere de relevante produkter til *tekniske varer* (også kaldet tekniske produkter). Tekniske produkter er produkter, der er versionsstyret og administreret via ændringsstyring. Der findes en guide til konverteringsprocessen.

## <a name="turn-on-the-feature-in-your-system"></a>Aktivere funktionen i systemet

Når du skal bruge denne funktion, skal du udføre følgende opgaver:

1. Aktivér funktionen Styring af tekniske ændringer og dens konfigurationsnøgle, som beskrevet i [Oversigt over styring af tekniske ændringer](product-engineering-overview.md).
1. Slå funktionen *Aktivér administration af ændringer på eksisterende produkter* i funktionsstyring. Få flere oplysninger i [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="restrictions-and-limitations"></a>Restriktioner og begrænsninger

Ikke alle produkttyper kan konverteres til alle andre typer. Der gælder følgende restriktioner og begrænsninger:

- Når du konverterer et produkt til et teknisk produkt, forbliver det et *produkt*. Den bliver ikke en *produktmaster*.
- Når du konverterer en produktmaster, der har et bestemt sæt dimensioner, vedligeholdes disse dimensioner efter ændringen. Hvis du f.eks. konverterer en produktmaster, der har størrelsesdimensionen, bevares størrelsesdimensionen.

Hvis du har et specifikt produkt, kan du derfor kun ændre det til et teknisk produkt, der ikke sporer produktdimensionen i transaktioner (det vil sige, at versionsdimensionen ikke bruges). Du kan finde flere oplysninger om disse problemer i de resterende afsnit i dette emne.

## <a name="prepare-for-conversion-by-creating-all-required-engineering-product-categories"></a>Forberede konverteringen ved at oprette alle nødvendige tekniske produktkategorier

Der skal tildeles en *kategori af teknisk produkt* til alle tekniske produkter. Du skal udføre denne tildeling, når du kører guiden **Konvertér til teknisk produkt**. Der skal findes tekniske produktkategorier for alle relevante standardprodukter, *før* du kan konvertere disse produkter.

Den tekniske produktkategori udgør grundlaget for oprettelsen af et teknisk produkt, og den fastlægger et sæt standardværdier og -politikker. Tekniske attributter og deres standardværdier (som defineret for den tekniske kategori) anvendes også på det resulterende tekniske produkt. Du kan redigere attributværdierne og/eller føje flere tekniske attributter til det resulterende produkt efter behov.

Den tekniske produktkategori skal matche det produkt, som du tildeler den. Produkttypen og dimensionsgruppen skal f.eks. svare til både produktet og dets tekniske produktkategori. Du kan finde flere oplysninger under [Tekniske versioner og tekniske produktkategorier](engineering-versions-product-category.md).

> [!IMPORTANT]
> Guiden **Konvertér til teknisk produkt** kan kun konvertere produktet til tekniske produkter, hvor versionen ikke spores i transaktioner. Derfor skal indstillingen **Spor version i transaktioner** indstilles til *Nej* for tekniske produktkategorier, som du opretter for at konvertere eksisterende produkter.

Du kan finde oplysninger om oprettelse af tekniske produktkategorier i [Tekniske versioner og tekniske produktkategorier](engineering-versions-product-category.md).

## <a name="run-the-convert-to-engineering-product-wizard"></a>Køre guiden Konverter til teknisk produkt

Guiden **Konverter til teknisk produkt** hjælper dig med at konvertere et eller flere eksisterende produkter til tekniske produkter. Den konverterer produkterne til tekniske produkter (versionerede produkter), hvor versionen ikke spores i transaktioner (så versionsdimensionen ikke bruges). Når konverteringen er fuldført, kan du administrere produkterne ved hjælp af Styring af tekniske ændringer.

Konverteringen er permanent. Du kan derfor ikke tilbageføre den senere. 

Hvert konverterede tekniske produkt vil fortsat blive frigivet i de samme firmaer, som det oprindelige produkt blev frigivet i. Styklisten og ruterne til teknikere frigives dog ikke automatisk til disse firmaer.

Benyt følgende fremgangsmåde for at køre guiden **Konvertér til teknisk produkt** og konvertere et produkt til et teknisk produkt.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Markér afkrydsningsfeltet for hvert produkt, der skal konverteres, i gitteret.
1. Vælg **Konverter til teknisk produkt** i gruppen **Teknisk ændringsstyring** i handlingsruden under fanen **Tekniker** for at åbne guiden.
1. Den første side i guiden er **velkomstsiden**. Hvis du ikke allerede kender konverteringsprocessen, skal du omhyggeligt læse oplysningerne på denne side. Når du er klar til at fortsætte, skal du vælge **Næste**.
1. På siden **Vælg detaljer for de produkter, der skal konverteres** vises hvert af de produkter, du valgte før åbning af guiden. Inspicer listen. Brug knapperne **Ny** og **Slet** på værktøjslinjen til at tilføje og fjerne produkter efter behov.
1. Brug følgende felter øverst i gitteret til at tildele standardværdier til hvert produkt på listen. (Du kan ændre disse værdier for individuelle produkter, når konverteringen er fuldført). Standardværdier tildeles ikke produkter, hvor en relevant værdi allerede er tildelt.

    - **Teknisk standardkategori** – Vælg en indledende teknisk produktkategori, der skal tildeles hvert enkelt produkt på listen. Den kategori, du vælger, anvendes kun på produkter, der er kompatible med den.
    - **Standardversion** – Angiv den første produktversion, der skal tildeles hvert enkelt produkt på listen. Hvert tekniske produkt har mindst én teknisk version.
    - **Standardlivscyklustilstand** – Vælg den første produktlivscyklustilstand, der skal tildeles hvert produkt på listen.
    - **Aktuel stykliste vil være en del af det tekniske produkt** – Markér dette afkrydsningsfelt, hvis den aktuelle stykliste for hvert viste produkt skal bruges som stykliste for det pågældende tekniske produkt.

    Du kan finde flere oplysninger om produktindstillinger i næste trin.

1. Gennemgå hvert produkt, der vises i gitteret, og evaluer, hvor godt de standardværdier, du har tildelt, gælder for det. Gennemgå følgende oplysninger for hver række, og angiv eventuelle relevante felter:

    - **Produktnummer** – Produktnummeret.
    - **Produktnavn** – Navnet på produktet.
    - **Teknisk kategori** – Vælg den tekniske produktkategori, som produktet skal tilhøre, når det er konverteret. Der skal allerede findes en relevant kategori for hvert produkt, som det blev forklaret i forrige afsnit i dette emne. Du skal tildele en kategori til alle produkter.
    - **Version** – Angiv den produktversion, der skal tildeles produktet efter konvertering. Du kan f.eks. vælge et nummer, der passer til den nummerserie, som din kategori allerede bruger. Hver enkelt tekniske version gemmer de teknisk relevante data, der er specifikke for den pågældende version. Du kan finde flere oplysninger under [Tekniske versioner og tekniske produktkategorier](engineering-versions-product-category.md).
    - **Produktlivscyklustilstand** – Vælg den produktlivscyklustilstand, som produktet skal være i, når det er konverteret. Produktlivscyklustilstanden giver dig mulighed for at styre, hvilke transaktioner der er tilladt for en bestemt teknisk version. Du kan finde flere oplysninger i [Produktlivscyklustilstand og transaktioner](product-lifecycle-state-transactions.md).
    - **Har stykliste** – Hvis afkrydsningsfeltet er markeret, angiver det, at produktet har en stykliste. Indstillingen af dette afkrydsningsfelt kan hjælpe dig med at bestemme, hvordan afkrydsningsfeltet **Aktuel stykliste vil være en del af det tekniske produkt** skal indstilles.
    - **Aktuel stykliste vil være en del af det tekniske produkt** – Markér dette afkrydsningsfelt, hvis den aktuelle stykliste for produktet skal bruges som stykliste for det tekniske produkt. Denne stykliste administreres derefter af Styring af tekniske ændringer. Hvis produktet ikke har en stykliste, eller hvis du foretrækker at oprette en stykliste manuelt for det konverterede produkt senere, skal du fjerne markeringen i dette afkrydsningsfelt.
    - **Har fejl** – Et markeret afkrydsningsfelt angiver, at produktopsætningen har en eller flere fejl. Produkttypen eller dimensionsgruppen er f.eks. ikke ens i kategorien. Produkter med fejl springes over og konverteres ikke.

1. Når du er færdig, skal du vælge **Valider** på værktøjslinjen for at validere produktopsætningen. For hver række opdateres afkrydsningsfeltet **Har fejl** for at angive produktets status. Juster værdierne, indtil det enkelte produkts opsætning er fejlfri.
1. Når alle produkter er konfigureret korrekt, skal du vælge **Næste** for at fortsætte.
1. Siden **Bekræft valg** viser antallet af produkter, der ikke har fejl i opsætningen, og som derfor er klar til konvertering. Den viser også det antal produkter, der springes over på grund af fejl. Hvis du vil køre konverteringen som et batchjob, skal du angive indstillingen **Kør i batch** til *Ja*.
1. Vælg **Udfør** for at anvende dine indstillinger og starte med at konvertere produkterne til tekniske produkter.

> [!NOTE]
> Hvis systemet er konfigureret til manuelt at acceptere produkter, før de frigives, skal du acceptere hvert konverterede produkt ved at bruge siden **Åbn produktfrigivelser** i de relevante firmaer. Du kan finde flere oplysninger under [Gennemse og acceptere produktet, før du frigiver det i det lokale firma](engineering-scenarios.md#accept).
