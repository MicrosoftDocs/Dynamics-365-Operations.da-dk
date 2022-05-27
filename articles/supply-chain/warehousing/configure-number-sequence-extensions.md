---
title: Konfigurere nummerserier til lagerstrømme
description: Dette emne giver en oversigt over de funktioner, der omfatter nummerserieudvidelser til id-numre, bølgeetiket-id'er, container-id'er og fragtseddel-id'er.
author: Mirzaab
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSNumberSequenceExt
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 20438ed3e34775a6312508595bcd32b16a37a81d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669549"
---
# <a name="configure-number-sequences-for-warehouse-flows"></a>Konfigurere nummerserier til lagerstrømme

[!include [banner](../includes/banner.md)]

Funktionen *Nummerserieudvidelser* tilføjer en ny konfigurationsside til opsætning af nummerserier. Den giver mulighed for en fleksibel konfiguration af GS1-regulerede id'er, herunder GS1-præfikser og kontrolcifre (modulo 10), og gennemtvinger en længdebegrænsning i eksisterende nummerserier.

Standardnummerseriesegmenter er ikke egnede til GS1-implementering, da der ikke beregnes et kontrolciffer, og firmaets GS1-præfiks skal opdateres manuelt.

Denne funktion inkluderer følgende funktioner:

- Stykliste-id'er kan genereres på forhånd.
- En entydig nummerserie kan genereres for SSCC-numre (Serial Report Container Code).
- GS1-kompatible nummerserier kan oprettes for stykliste- og SSCC-numre. Funktionen tilføjer færdiglavet understøttelse af id-numre, container-id'er, bølgeetiket-id'er og stykliste-id'er.
- Konfiguration af id-numre er fleksibel. Du kan f.eks. medtage eller udelukke programidentifikatorer, f.eks. foranstillede nuller (00).

Denne funktionalitet gør det mere effektivt at understøtte etikettering af kartoner og justere nye numre, der genereres af systemet.

## <a name="turn-on-the-number-sequence-extensions-feature"></a>Slå funktionen Nummerserieudvidelser til

Før du kan bruge funktionen, skal den være slået til i dit system. Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Nummerserieudvidelser*

## <a name="set-up-the-feature"></a>Konfigurere funktionen

Hvis du vil konfigurere nummerserieudvidelser i systemet, skal du følge disse trin.

1. Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**.
1. Gå til fanen **Generelt** i feltet **GS1-firmapræfiks**, og indtast dit firmas GS1-præfiks. Denne værdi vil påvirke alle de nummerserier, hvor GS1-præfikset medtages som segment.
1. Hvis du vil generere styklistenumre til bølgeetiketter, skal du på fanen **Rapporter** markere afkrydsningsfeltet **Generer styklistenummer ved udskrivning af bølgeetiketter**.

    > [!NOTE]
    > Dette afkrydsningsfelt er kun tilgængeligt, hvis funktionen til [udskrivning af bølgeetiketter](configure-wave-label-printing.md) er slået til.

1. Gå til **Lokationsstyring** \> **Konfiguration** \> **Nummerserieudvidelser**
1. Vælg **Opret standardkonfiguration** i handlingsruden. Der oprettes en GS1-kompatibel styklistenummerserie og tre typer SSCC-nummerserier. Alle disse nummerserier tager højde for længden af dit firmas GS1-præfiks.

    Du kan finde flere oplysninger om, hvordan du tilpasser disse standardnummerserier og/eller tilføjer nye serier, i næste afsnit. Du kan også fjerne disse sekvenser, hvis du ikke har brug for dem.

1. Gå tilbage **Lokationsstyring \> Konfiguration \> Parametre til lokationsstyring**.
1. Gå til fanen **Nummerserier**, og vælg en relevant nummerserieudvidelse, der skal bruges til at generere numre til dine id-numre, bølgeetiket-id'er, container-id'er (i dette tilfælde skal du vælge det relevante **SSCC-18-nummerserie**) og/eller stykliste-id'er (i dette tilfælde skal du vælge **styklisteserien**). Som standard understøttes kun nummerserieudvidelser for disse fire typer id'er.

Næste gang der genereres et nyt nummer for en af disse nummerserier, bruges den nye logik.

> [!NOTE]
> Hvis du ikke vælger en nummerserieudvidelse til id-numre, bruges de aktuelle regler for generering af id-numre. Ellers vil den valgte nummerserie blive brugt. De andre id'er bruger en almindelig nummerserie, indtil du anvender en nummerserieudvidelse for dem.

## <a name="create-and-edit-number-sequences"></a>Oprette og redigere nummerserier

I det forrige afsnit blev der genereret der et standardsæt med nummerserier. Dette afsnit forklarer, hvordan hver nummerserie defineres. Det forklarer også, hvordan du opretter brugerdefinerede rækkefølger, og hvordan du kan redigere standardserier eller de brugerdefinerede serier.

Benyt følgende fremgangsmåde for at oprette og redigere nummerserier.

1. Gå til **Lokationsstyring** \> **Konfiguration** \> **Nummerserieudvidelser**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Gå til feltet **Nummerserieudvidelse**, og angiv et navn til den nye serie. Indtast en beskrivelse i feltet **Beskrivelse**.
1. Gå til oversigtspanelet **Segmenter**, og brug knapperne på værktøjslinjen til at samle nummereringsformatet ved at tilføje, slette og arrangere segmenter. I feltet **Segment** skal du for hver række tildele en segmenttype for at definere formålet med og indholdet af det pågældende segment. I følgende tabel forklares de typer af segmenter, der er tilgængelige.

    | Segmenttype | Beskrivende tekst |
    |---|---|
    | Konstant | Denne segmenttype tilføjer den samme konstanttekst for hvert genereret nummer i serien. Angiv den krævede tekst i feltet **Værdi**. Feltet **Længde** opdateres automatisk til længden af den tekst, du har angivet i feltet **Værdi**. |
    | Nummerserie | I feltet **Værdi** skal du angive et nummertegn (*\#*) for hvert tegn, der skal vises i den oprettede serie. Selve nummerserien kan f.eks. generere længere numre, men kun de tegnene længst til højre vil blive vist. Feltet **Længde** opdateres automatisk til antallet af nummertegn, som du har angivet i feltet **Værdi**.<p>Hvis du vil overholde GS1-kravene for SSCC-18-numre, skal du kontrollere, at længden på dette segment er 16 minus længden på GS1-præfikset.</p> |
    | GS1-præfiks | Denne segmenttype tilføjer den værdi, der er angivet i feltet **GS1-firmapræfiks** på siden **Parametre for lokationsstyring**. Feltet **Værdi** viser den værdi, der er angivet på siden **Parametre for lokationsstyring**, og feltet **Længde** viser antallet af tegn i værdien. Både feltet **Værdi** og feltet **Længde** er skrivebeskyttet. |
    | Programidentifikator | I feltet **Værdi** skal du angive et ansøgnings-id, som angivet i den relevante GS1-politik for denne type nummerserie. Skriv f.eks. *00* for SSCC eller *420* for stykliste. Feltet **Længde** opdateres automatisk til længden af det id, du har angivet i feltet **Værdi**. |
    | Pakketype | For varer, der klart kan identificeres, tilføjer denne segmenttype en feltværdi fra den relevante enheds seriegruppe (fra siden **Enhedsseriegrupper**). (Denne funktionsmåde svarer til den eksisterende logik for id-numre). For nummerplader, der omfatter flere lagerenheder, tilføjer denne segmenttype *0* (nul) som standard. For denne segmenttype indstilles feltet **Værdi** altid til *P*, og feltet **Længde** indstilles altid til *1*.|
    | Kontroltal | Denne segmenttype tilføjer et kontrolciffer, som er en modulo 10-beregning. (Denne funktionsmåde svarer til den eksisterende logik for id-numre). For denne segmenttype angives feltet **Værdi** til et cirkumflekstegn (*^*), og feltet **Længde** indstilles altid til *1*. |

1. Hvis du vil have vist et eksempel på dit endelige talformat, skal du kontrollere feltet **Format** nederst i oversigtspanelet **Segmenter**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]