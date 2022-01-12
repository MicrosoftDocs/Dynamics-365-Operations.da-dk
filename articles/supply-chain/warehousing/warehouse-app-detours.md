---
title: Konfigurere omveje til trin i menupunkter på mobilenheder
description: Dette emne indeholder en beskrivelse af, hvordan du konfigurerer omveje til menupunkter, så arbejdere kan tilbageholde den aktuelle opgave, udføre en anden opgave og derefter vende tilbage til den oprindelige opgave uden at miste oplysninger.
author: Mirzaab
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 874abbdf7c0938a7ad4cc66e23dd01d901a1f0d3
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920342"
---
# <a name="configure-detours-for-steps-in-mobile-device-menu-items"></a>Konfigurere omveje til trin i menupunkter på mobilenheder

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> De funktioner, der er beskrevet i dette emne, gælder kun for den nye Warehouse Management-mobilapp. De påvirker ikke den gamle lagerstedsapp, der nu er udgået og frarådes.

Dette emne indeholder en beskrivelse af, hvordan du konfigurerer omveje til menupunkter, så arbejdere kan "tilbageholde" den aktuelle opgave, udføre en anden opgave og derefter vende tilbage til den oprindelige opgave uden at miste oplysninger.

En omvej er et separat menupunkt, der kan åbnes fra et trin i en hovedopgave. I slutningen af omvejen vender arbejderen tilbage til det sted, hvor han eller hun forlod hovedopgaven. Under konfigurationen skal du angive det menupunkt, der skal fungere som omvej. Du vælger også, hvilke feltværdier fra hovedopgaven, der automatisk skal videresendes (kopieres) til omvejen og angives der. Du skal derfor forstå, hvor i opgaveflowet du ønsker, at omvejen skal være tilgængelig for arbejdere. Du skal også sikre dig, at de oplysninger, der skal kopieres til omvejen, er tilgængelige for det pågældende trin i opgaveflowet.

## <a name="enable-detours-in-your-system"></a>Aktivere omveje i systemet

Før du kan konfigurere omveje for trin i menupunkterne på mobilenheden, skal du gennemføre følgende procedure for at aktivere de påkrævede funktioner og generere de nødvendige feltnavne i mobilappen Warehouse Management.

1. Gå til **Systemadministration \> Arbejdsområder \> Funktionsstyring**.
1. I [arbejdsområdet **Funktionsstyring**](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) skal du aktivere funktionen, der vises, på følgende måde:

    - **Modul:** *Warehouse Management*
    - **Funktionsnavn:** *Trininstruktioner for lagerstedsappen*

    Du kan finde flere oplysninger om trinnet *Vejledninger til trin i lagerstedsapp* i [Tilpasse trintitler og instruktioner til Warehouse Management-mobilappen](mobile-app-titles-instructions.md). Denne funktion er en forudsætning for funktionen *Omveje i Warehouse Management-app*.

1. Aktivér funktionen, der vises, på følgende måde:

    - **Modul:** *Warehouse Management*
    - **Funktionsnavn:** *Omveje i Warehouse Management-app*

    Denne funktion er den funktion, der er beskrevet i dette emne.

1. Opdater feltnavnene i Warehouse Management-mobilappen ved at gå til **Warehouse Management \> Opsætning \> Mobilenhed \> Feltnavne for lagerstedsapp** og vælge **Opret standardkonfiguration**. Du kan finde flere oplysninger i [Konfigurere felter til mobilappen Lokationsstyring](configure-app-field-names-priorities-warehouse.md).
1. Gentag det forrige trin for hver juridisk enhed (firma), hvor du bruger mobilappen Warehouse Management.

## <a name="configure-a-detour-from-a-menu-specific-override"></a>Konfigurere en omvej fra en menuspecifik tilsidesættelse

Benyt følgende fremgangsmåde, hvis du vil konfigurere en omvej fra en menuspecifik tilsidesættelse.

1. Opret en menuspecifik tilsidesættelse for den relevante menu og det relevante trin som beskrevet i [Tilpasse trintitler og instruktioner til Warehouse Management-mobilappen](mobile-app-titles-instructions.md).
1. Find kombinationen af værdier for **Trin-id** og **Menupunktnavn**, som du vil redigere, og vælg derefter værdien i kolonnen **Trin-id**.
1. På den side, der vises, kan du angive det menupunkt, der skal fungere som omvej, i oversigtspanelet **Tilgængelige omveje (menupunkter)**. Du kan også vælge, hvilke feltværdier fra hovedopgaven, der automatisk skal kopieres til og fra omvejen. Du kan finde eksempler, der viser, hvordan du bruger disse indstillinger, i scenarierne senere i dette emne.

## <a name="sample-scenario-1-sales-picking-where-a-location-inquiry-acts-as-a-detour"></a>Eksempelscenarie 1: Salgspluk, hvor en forespørgsel om en lokation fungerer som en omvej

Dette scenarie viser, hvordan du kan konfigurere en forespørgsel om en lokation som en omvej i et arbejderstyret opgaveflow for salgspluk. Denne omvej giver arbejdere mulighed for at søge efter alle id'er på den lokation, de plukker fra, og plukke det id, de vil bruge til at udføre plukket. Denne type omvej kan være nyttig, hvis stregkoden er beskadiget og derfor ikke kan læses af scannerenheden. Alternativt kan det være nyttigt, hvis en arbejder skal finde ud af, hvad lagerbeholdningen rent faktisk er i systemet. Bemærk, at dette scenario kun fungerer, hvis du plukker fra id-styrede lokationer.

### <a name="enable-sample-data"></a>Aktivér eksempeldata

Hvis du vil bruge de angivne eksempelposter og -værdier, når du arbejder i dette scenarie, skal du bruge et system, hvor standarddemodataene er installeret. Du skal også vælge den juridiske enhed **USMF**, før du starter.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-1"></a>Oprette en menuspecifik tilsidesættelse og konfigurere omvejen til scenarie 1

I denne procedure konfigurerer du en omvej til menupunktet **Salgspluk** i id-trinnet.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Trin for mobilenhed**.
1. Find det trin-id, der hedder *LicensePlateId*, og vælg det.
1. Vælg **Tilføj trinkonfiguration** i handlingsruden.
1. Brug feltet **Menupunkt** i dialogboksen med rullelisten til at finde og vælge *Salgspluk*.
1. Vælg **OK**.
1. Detaljesiden for den tilsidesættelse, du netop har oprettet, vises. Vælg **Tilføj** på værktøjslinjen i oversigtspanelet **Tilgængelige omveje (menupunkter)**.
1. Vælg **Lokationsforespørgsel** som den omvej, der skal gøres tilgængelig i mobilappen Warehouse Management, i dialogboksen **Tilføj omvej**.
1. Vælg **OK**.
1. Vælg den omvej, du netop har tilføjet, i oversigtspanelet **Tilgængelige omveje (menupunkter)**, og vælg derefter **Vælg felter, der skal sendes** på værktøjslinjen.
1. Angiv de oplysninger, der skal sendes til og fra omvejen, i dialogboksen **Vælg felter, der skal sendes**. I dette scenario giver du arbejdere mulighed for at bruge den lokation, de skal plukke fra, som input for omvejen til lokationsforespørgslen. Derfor skal du vælge **Tilføj** på værktøjslinjen i sektionen **Send fra salgspluk** for at føje en række til gitteret. Angiv følgende værdier for den nye række:

    - **Kopiér fra salgspluk:** *Lokation*
    - **Indsæt i lokationsforespørgsel:** *Lokation*

1. Da omvejen i dette scenario er konfigureret i id-trinnet, vil det være nyttigt, hvis arbejderne kan føre id'et fra forespørgslen tilbage til hovedflowet. Derfor skal du vælge **Tilføj** på værktøjslinjen i sektionen **Før tilbage fra lokationsforespørgsel** for at føje en række til gitteret. Angiv følgende værdier for den nye række:

    - **Kopiér fra lokationsforespørgsel:** *Id*
    - **Indsæt i salgspluk:** *Id*

1. Vælg **OK**.

Omvejen er nu fuldt konfigureret. Der vises nu en knap, du kan bruge til at starte omvejen **Lokationsforespørgsel** på id-trinnet for menupunktet **Salgspluk**.

### <a name="complete-a-sales-pick-on-a-mobile-device-and-use-the-detour"></a>Fuldføre et salgspluk på en mobilenhed og bruge omvejen

I denne procedure skal du fuldføre et salgspluk ved hjælp af mobilappen Warehouse Management. Du skal bruge den omvej, du netop har konfigureret, til at finde det id, du vil bruge til at udføre pluktrinnet.

1. I Microsoft Dynamics 365 Supply Chain Management kan du oprette en salgsordre, der skal bruge et pluktrin til at plukke fra en placering, som id'et har sporet. Frigiv derefter salgsordren til lagerstedet. Notér det arbejds-id, der genereres.
1. Åbn mobilappen Warehouse Management, og log på lagersted 24. (I standarddemodataene skal du logge på ved at bruge *24* som bruger-id og *1* som adgangskode.)
1. Vælg menuen **Udgående**, og vælg derefter menupunktet **Salgspluk**.
1. Følg instruktionerne til dataindtastning på skærmen for at angive det arbejds-id, der blev genereret i trin 1.
1. Åbn handlingsmenuen i det trin, der indeholder teksten **Scan et id**. Du bør få vist en ny knap med navnet **Lokationsforespørgsel**. En pil i øverste venstre hjørne angiver, at knappen starter en omvej. Vælg **Lokationsforespørgsel**.
1. Omvejen er startet. På den næste side skal du bekræfte den lokation, der blev kopieret fra hovedflowet.
1. På listen over tilgængelige id'er på lokationen skal du trykke på det id, du vil kopiere tilbage til hovedflowet. Vælg derefter knappen **Tilbage**.
1. Du er tilbage til hovedflowet for salgspluk, og id'et er kopieret tilbage til det fra omvejen. Bekræft værdien, så du kan fortsætte til næste trin.
1. Du kan nu fuldføre resten af standardflowet ved at angive instruktionerne til den ønskede dataindtastning.

Arbejdet på lagerstedet er nu fuldført. Arbejderen har åbnet en omvej for at udføre en sekundær opgave (lokationsforespørgsel) uden at miste sin plads i hovedopgaven og har hentet de oplysninger, der skulle bruges til at udføre hovedopgaven, tilbage.

## <a name="sample-scenario-2-item-inquiry-with-movement-and-adjustment-detours"></a>Eksempelscenario 2: Vareforespørgslen med bevægelses- og reguleringsomveje

I dette scenarie vises, hvordan du kan konfigurere bevægelser og reguleringer som flere omveje i opgaveflowet for lokationsforespørgsler. Denne egenskab kan være nyttig i situationer, hvor en arbejder ankommer til en lokalitet, finder ud af, at lageret på lokationen afviger fra det, der er registreret i systemet, og derfor skal regulere eller flytte varer.

Du kan erstatte lokationsforespørgslen med en id-forespørgsel eller en vareforespørgslen efter behov.

### <a name="enable-sample-data"></a>Aktivér eksempeldata

Hvis du vil bruge de angivne eksempelposter og -værdier, når du arbejder i dette scenarie, skal du bruge et system, hvor standarddemodataene er installeret. Du skal også vælge den juridiske enhed **USMF**, før du starter.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-2"></a>Oprette en menuspecifik tilsidesættelse og konfigurere omvejen til scenarie 2

I denne procedure konfigurerer du en omvej til menupunktet **Salgspluk** i id-trinnet.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Trin for mobilenhed**.
1. Find og vælg det trin-id, der hedder *LocationInquiryList*.

    > [!NOTE]
    > Hvis du vil bruge en vareforespørgsel i stedet for en lokationsforespørgsel, skal du vælge en række, hvor trin-id'et hedder *ItemInquiryList*. Hvis du vil bruge en id-forespørgsel, skal du vælge en række, hvor trin-id'et hedder *LPInquiryList*.

1. Vælg **Tilføj trinkonfiguration** i handlingsruden.
1. Brug feltet **Menupunkt** i dialogboksen med rullelisten til at finde og vælge *Lokationsforespørgsel*.
1. Vælg **OK**.
1. Detaljesiden for den tilsidesættelse, du netop har oprettet, vises. Vælg **Tilføj** på værktøjslinjen i oversigtspanelet **Tilgængelige omveje (menupunkter)**.
1. Vælg **Bevægelse** som den omvej, der skal gøres tilgængelig i mobilappen Warehouse Management, i dialogboksen **Tilføj omvej**.
1. Vælg **OK**.
1. Vælg den omvej, du netop har tilføjet, i oversigtspanelet **Tilgængelige omveje (menupunkter)**, og vælg derefter **Vælg felter, der skal sendes** på værktøjslinjen.
1. Angiv de oplysninger, der skal sendes til og fra omvejen, i dialogboksen **Vælg felter, der skal sendes**. I dette scenario forventer du, at arbejdere søger efter id-styrede lokationer. Derfor vil det være en god ide at kopiere id'et fra forespørgslen til omvejen **Bevægelse**. Vælg **Tilføj** på værktøjslinjen i sektionen **Send fra salgspluk** for at føje en række til gitteret. Angiv følgende værdier for den nye række:

    - **Kopiér fra lokationsforespørgsel:** *Lokation*
    - **Indsæt i Bevægelse:** *Loc/LP*

    I denne omvej forventer du ikke, at oplysninger kopieres tilbage, fordi hovedflowet var en forespørgsel, hvor der ikke kræves yderligere trin.

1. Vælg **OK**.

Omvejen er nu fuldt konfigureret. Der vises nu en knap, du kan bruge til at starte omvejen **Bevægelse** på id-trinnet for menupunktet **Lokationsforespørgsel**.

### <a name="do-a-location-inquiry-on-a-mobile-device-and-use-the-detour"></a>Udføre en lokationsforespørgsel på en mobilenhed og bruge omvejen

I denne procedure skal du udføre en lokationsforespørgsel ved hjælp af mobilappen Warehouse Management. Du skal derefter bruge omvejen til at fuldføre en varebevægelse.

1. Åbn mobilappen Warehouse Management, og log på lagersted 24. (I standarddemodataene skal du logge på ved at bruge *24* som bruger-id og *1* som adgangskode.)
1. Vælg menuen **Lager**, og vælg derefter menupunktet **Lokationsforespørgsel**.
1. Angiv en lokation, du vil forespørge om, for eksempel *FL-001*.
1. Når listen vises, skal du trykke og holde nede på et af kortene i den for at få vist de tilgængelige omveje.
1. Vælg **Bevægelse**.
1. Bemærk, at id'et er blevet kopieret fra det valgte kort. Bekræft værdien.
1. Du kan nu følge standardopgaveflowet for at fuldføre bevægelsen. Når arbejdet er fuldført, skal du åbne handlingsmenuen og vælge **Annuller**.
1. Du returneres til siden **Lokalitetsforespørgsel**. Bemærk, at værdierne ikke opdateres automatisk. Du skal derfor opdatere siden manuelt for at se ændringerne fra bevægelsesomvejen.
