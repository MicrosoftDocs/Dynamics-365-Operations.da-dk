---
title: Start her med momsberegning
description: Dette emne beskriver, hvordan du konfigurerer momsberegning.
author: wangchen
ms.date: 03/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0ab9c0cf974114c4fa9b673e5601e138acef534d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685905"
---
# <a name="get-started-with-tax-calculation"></a>Start her med momsberegning

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om, hvordan du kommer i gang med momsberegning. Sektionerne i dette emne fører dig gennem de overordnede design- og konfigurationstrin i Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS), Dynamics 365 Finance og Dynamics 365 Supply Chain Management. 

Opsætningen består af tre hovedtrin.

1. Installer tilføjelsesprogrammet Momsberegning i LCS.
2. Konfigurer momsberegningsfunktionen i RCS. Denne opsætning er ikke specifik for de enkelte juridiske enheder. Den kan deles på tværs af juridiske enheder i Finance og Supply Chain Management.
3. I Finance og Supply Chain Management skal du konfigurere parametre for momsberegning efter juridisk enhed.

## <a name="high-level-design"></a>Overordnet design

### <a name="runtime-design"></a><a name="runtime"></a> Kørselsdesign

I følgende illustration vises det overordnede kørselsdesign af momsberegning. Da momsberegning kan integreres med flere Dynamics 365-apps, bruger illustrationen integrationen med Finance som et eksempel.

1. Der oprettes en transaktion i Finance, f.eks. en salgsordre eller indkøbsordre.
2. Finance anvender automatisk standardværdierne i momsgruppen og varemomsgruppen.
3. Når knappen **Moms** vælges i transaktionen, udløses momsberegningen. Finance sender derefter nyttedataene til tjenesten Momsberegning.
4. Tjenesten Momsberegning matcher nyttedataene med foruddefinerede regler i momsfunktionen for at finde en mere præcis momsgruppe og varemomsgruppe på samme tid.

    - Hvis nyttelasten kan matches med matrixen **Anvendelse af momsgruppe**, tilsidesætter den momsgruppeværdien med værdien for matchet momsgruppe i anvendelighedsreglen. Ellers fortsætter den med at bruge momsgruppeværdien fra Finance.
    - Hvis nyttelasten kan matches med matrixen **Anvendelse af varemomsgruppe**, tilsidesætter den varemomsgruppeværdien med værdien for matchet varemomsgruppe i anvendelighedsreglen. Ellers fortsætter den med at bruge varemomsgruppeværdien fra Finance.

5. Tjenesten Momsberegning fastlægger de endelige momskoder ved at bruge skæringspunktet for momsgruppen og varemomsgruppen.
6. Tjenesten Momsberegning beregner moms på basis af de endelige momskoder, som den har fastlagt.
7. Tjenesten Momsberegning returnerer momsberegningsresultatet til Finance.

![Design til kørsel af momsberegning.](media/tax-calculation-runtime-logic.png)

### <a name="high-level-configuration"></a>Overordnet konfiguration

Følgende trin giver en overordnet oversigt over konfigurationsprocessen for momsberegningstjenesten.

1. Installer tilføjelsesprogrammet **Momsberegning** i dit LCS-projekt.
2. Opret funktionen **Momsberegning** i RCS.
3. Konfigurer funktionen **Momsberegning** i RCS:

    1. Vælg momskonfigurationsversionen.
    2. Opret momskoder.
    3. Opret en momsgruppe.
    4. Opret en varemomsgruppe.
    5. Valgfrit: Opret anvendelse af momsgruppe, hvis du vil tilsidesætte den standardmomsgruppe, der angives fra masterdata for debitorer eller kreditorer.
    6. Valgfrit: Opret anvendelse af varemomsgruppe, hvis du vil tilsidesætte den standardvaremomsgruppe, der angives fra varemasterdata.

4. Fuldfør og publicer funktionen **Momsberegning** i RCS.
5. Vælg den publicerede **Momsberegning**-funktion i Finance.

Når du har fuldført disse trin, synkroniseres følgende konfigurationer automatisk fra RCS til Finance.

- Momskoder
- Momsgrupper
- Varemomsgrupper

De resterende afsnit i dette emne indeholder flere detaljerede konfigurationstrin.

## <a name="prerequisites"></a>Forudsætninger

Før du kan fuldføre trinnene de resterende procedurer i dette emne, skal følgende forudsætninger være opfyldt:<!--TO HERE-->

- Du skal have adgang til din LCS-konto, og du skal have et aktivt LCS-projekt med et niveau 2-miljø eller derover, som kører Dynamics 365 version 10.0.21 eller senere.
- Du skal oprette et RCS-miljø for din organisation, og du skal have adgang til din konto. Du kan finde flere oplysninger om, hvordan du opretter et RCS-miljø, i [Oversigt over Regulatory Configuration Service](rcs-overview.md).
- Følgende funktioner skal være aktiveret i arbejdsområdet **Funktionsstyring** i det installerede Supply Chain Management-miljø baseret på virksomhedens forretningsbehov:

    - Momsberegningstjeneste
    - Understøt flere momsregistreringsnumre
    - Moms i flytteordre

- Følgende funktioner skal være aktiveret i arbejdsområdet **Funktionsstyring** i dit installerede RCS-miljø.

    - Globaliseringsfunktioner

- Følgende roller skal tildeles brugerne i RCS-miljøet efter behov:

    - Udvikler til elektronisk rapportering
    - Udvikler af funktion til globalisering
    - Udvikler af momsprogram
    - Funktionel konsulent for momsprogram
    - Tjenesteudvikler for moms

## <a name="set-up-tax-calculation-in-lcs"></a>Konfigurere momsberegning i LCS

1. Log på [LCS](https://lcs.dynamics.com)
2. Fuldfør Microsoft Power Platform-integrationsopsætningen. Du kan finde flere oplysninger under fanen [Oversigt over tilføjelsesprogrammer](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Vælg et af de installerede miljøer, og vælg derefter **Installer et nyt tilføjelsesprogram**.
4. Vælg **Momsberegning**.
5. Læs og acceptér vilkår og betingelser, og vælg derefter **Installer**.

## <a name="set-up-tax-calculation-in-rcs"></a>Konfigurere momsberegning i RCS

Trinnene i dette afsnit er ikke relateret til en bestemt juridisk enhed. Du skal kun gennemføre denne procedure én gang, så du kan fuldføre den i enhver juridisk enhed i RCS.

1. Log på [RCS](https://marketing.configure.global.dynamics.com/).
2. I arbejdsområdet **Elektronisk rapportering** skal du tilføje en ny konfigurationsudbyder. Brug dit firmanavn som navnet på udbyderen. Få flere oplysninger i [Oprette konfigurationsudbydere og markere dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Vælg den konfigurationsudbyder, du lige har oprettet, og vælg derefter **Angiv som aktiv**.
4. Vælg **Microsoft**-konfigurationsudbyderen, og vælg derefter **Lagre**.
5. I feltet **Type** skal du vælge **Global**.
6. Vælg **Åbn**.
7. Gå til **Datamodel for moms**, udvid filtræet, og vælg derefter **Momskonfiguration**.
8. Vælg den korrekte [momskonfigurationsversion](global-tax-calcuation-service-overview.md#versions) på baggrund af din Finance-version, og vælg derefter **Importér**.
9. I arbejdsområdet **Globaliseringsfunktioner** skal du vælge **Funktioner**, markere feltet **Momsberegning** og derefter vælge **Tilføj**.
10. Vælg en af følgende funktionstyper:

    - **Ny funktion** – Opret en funktionsopsætning, der har tomt indhold.
    - **Baseret på eksisterende funktion** – Opret en funktion ud fra en eksisterende funktion, og kopiér indholdet fra den eksisterende funktionsopsætning.

11. Angiv et navn og en beskrivelse for funktionen, og vælg derefter **Opret funktion**.

    Når funktionen er oprettet, oprettes der automatisk en kladdeversion af den. Du kan vælge **Hent denne version**, hvis du vil rebasere kladdeversionen på enhver fuldført version.

12. Vælg kladdeversionen af funktionen, og vælg derefter **Rediger**. Siden **Opsætning af momsberegning** er udfyldt.
13. Vælg **Konfigurationsversion**. Du bør kunne se den konfigurationsversion, du importerede i trin 8.

    Microsoft leverer en standardmomskonfiguration for momsberegningen. Denne konfiguration opfylder de fleste krav til momsberegningsmåder. Den opdateres på baggrund af markedsfeedback. Hvis du skal udvide konfigurationen, så den opfylder bestemte krav, kan du se [Sådan bygger du udvidelse i momstjeneste](./tax-service-add-data-fields-tax-integration-by-extension.md) med oplysninger om, hvordan du genererer og vælger din egen momskonfiguration.

14. Når du har valgt **Konfigurationsversion**, vises flere ekstra faner. Følg den rækkefølge, der er vist her, for at fuldføre opsætningen af den obligatoriske fane.

    **Obligatorisk opsætning**

    - **Momskoder** – Bevar masterdata for momskoder. Alle momskoder, der oprettes under denne fane, synkroniseres automatisk med Finance, når du aktiverer den aktuelle version.
    - **Momsgruppe** – Definer masterdata for momsgruppen og momskoderne under gruppen.
    - **Varemomsgruppe** – Definer masterdata for momsgruppen for varesalg og momskoderne under gruppen.

    **Valgfri konfiguration**

    - **Anvendelse af momsgruppe** – Definer en matrix, der fastlægger momsgruppen. Hvis ingen anvendelsesregler i denne matrix stemmer overens med det momspligtige dokument fra Dynamics 365, bruger Momsberegning standardværdien på den momspligtige dokumentlinje.
    - **Anvendelse af varemomsgruppe** – Definer en matrix, der fastlægger momsgruppen for varesalg. Hvis ingen anvendelsesregler i denne matrix stemmer overens med det momspligtige dokument fra Dynamics 365, bruger Momsberegning standardværdien på den momspligtige dokumentlinje.
    - **Anvendelse af debitors momsregistreringsnummer** – Hvis der er flere momsregistreringsnumre for samme debitor, kan Momsberegning automatisk bestemme det korrekte momsregistreringsnummer. I matrixen under denne fane kan du definere de regler, som skal bruges til at fastlægge det. Ellers vil Finance og Supply Chain Management fortsætte med at bruge standardmomsregistreringsnummeret på momspligtige dokumenter til salgstransaktioner.
    - **Anvendelse af kreditors momsregistreringsnummer** – Hvis der er flere momsregistreringsnumre for samme kreditor, kan Momsberegning automatisk bestemme det korrekte momsregistreringsnummer. I matrixen under denne fane kan du definere de regler, som skal bruges til at fastlægge det. Ellers vil Finance og Supply Chain Management fortsætte med at bruge standardmomsregistreringsnummeret på momspligtige dokumenter til købstransaktioner.
    - **Anvendelse af listekode** – Bestem automatisk værdien i feltet **Listekode** ved hjælp af mere fleksible og konfigurerbare regler. I matrixen under denne fane kan du definere de regler, som skal bruges til at fastlægge det. Ellers vil Finance og Supply Chain Management fortsætte med at bruge standardkoden på momspligtige dokumenter.

14. Under fanen **Momskoder** skal du vælge **Tilføj** og angive momskoden samt en beskrivelse.
15. Vælg **Momskomponent**. Momskomponenten er en gruppe af metoder, der blev defineret i den forrige version af den valgte momskonfiguration. Følgende momskomponenter er tilgængelige:

    - Efter nettobeløb
    - Efter bruttobeløb
    - Efter antal
    - Efter margen
    - Moms på moms

16. Vælg **Gem**. Flere felter bliver tilgængelige baseret på den momskomponent, du har valgt.
17. Benyt følgende indstillinger til at identificere momskodens art:

    - Er momsfri
    - Er importmoms
    - Er modtagermoms
    - Udelad i beregning af grundbeløb

    I et scenarie med importmoms skal du konfigurere en enkelt momskode med en positiv momssats og markere den som **Er importmoms**.

    Du kan f.eks. konfigurere to momskoder til modtagermoms, hvoraf den ene har en positiv momssats, og den anden har en negativ momssats, men samme satsværdi. Markér den negative momskode som **Er modtagermoms**. Du kan finde flere oplysninger om løsningen med modtagermoms i Finance i [Modtagermomsmekanisme for momsskema](emea-reverse-charge.md).

    For nogle momstyper, der skal udelades fra beregningen af momsgrundbeløbet for pris inklusive transaktioner (f.eks. toldafgift i visse lande/områder), skal du markere afkrydsningsfeltet **Udelad i beregning af grundbeløb**. Du kan finde flere oplysninger om denne parameter under [Beregning af moms oven på prisen, når Priser er inklusive moms aktiveret](global-exclude-from-tax-base-amount-calculation.md).

    Vedligehold momssatser og momsbeløbsgrænser for denne momskode.

18. Gentag trin 14 til og med 17 for at tilføje alle andre momskoder, du har brug for.
19. Under fanen **Momsgruppe** skal du vælge kolonnen **Momsgruppe**, tilføje den i matrixen som inputbetingelse og derefter tilføje linjer for at bevare masterdata for momsgruppen.

    Her er et eksempel.

    | Skattegruppe    | Momskoder           |
    | ------------ | ------------------- |
    | DEU_Indland | DEU_VAT19; DEU_VAT7 |
    | DEU_EU       | DEU_Momsfri          |
    | BEL_Indland | BEL_VAT21; BEL_VAT6 |
    | BEL_EU       | BEL_Momsfri          |

20. Under fanen **Varemomsgruppe** skal du vælge kolonnen **Varemomsgruppe**, tilføje den i matrixen som inputbetingelse og derefter tilføje linjer for at bevare masterdata for momsgruppen for varesalg.

    Her er et eksempel.

    | Varemomsgruppe | Momskoder                                    |
    | -------------- | -------------------------------------------- |
    | Fuld           | DEU_VAT19; BEL_VAT21; DEU_Momsfri; BEL_Momsfri |
    | Reduceret        | DEU_VAT7; BEL_VAT6; DEU_Momsfri; BEL_Momsfri   |

21. Under fanen **Anvendelse af momsgruppe** skal du vælge de kolonner, der skal bruges til at bestemme den korrekte momsgruppe, og derefter vælge **Tilføj**. Angiv eller vælg værdier for hver kolonne. Feltet **Momsgruppe** vil være outputtet for denne matrix. Hvis denne fane ikke er konfigureret, anvendes momsgruppen på transaktionslinjen.

    Her er et eksempel.

    | Forretningsproces | Afsender | Modtager | Skattegruppe    |
    | ---------------- | --------- | ------- | ------------ |
    | Sales            | DEU       | DEU     | DEU_Indland |
    | Sales            | DEU       | FRA     | DEU_EU       |
    | Sales            | BEL       | BEL     | BEL_Indland |
    | Sales            | BEL       | FRA     | BEL_EU       |
    
    > [!NOTE]
    > Hvis standardmomsgruppen på de momspligtige dokumentlinjer er korrekt, skal du lade denne matrix være tom. Du kan finde flere oplysninger i afsnittet [Kørselsdesign](#runtime) i dette emne.

22. Under fanen **Anvendelse af varemomsgruppe** skal du vælge de kolonner, der skal bruges til at bestemme den korrekte momskode, og derefter vælge **Tilføj**. Angiv eller vælg værdier for hver kolonne. Feltet **Varemomsgruppe** vil være outputtet for denne matrix. Hvis denne fane ikke er konfigureret, anvendes momsgruppen for varesalg på transaktionslinjen.

    Her er et eksempel.

    | Varekode | Varemomsgruppe |
    | --------- | -------------- |
    | D0001     | Fuld           |
    | D0003     | Reduceret        |

    > [!NOTE]
    > Hvis standardvaremomsgruppen på de momspligtige dokumentlinjer er korrekt, skal du lade denne matrix være tom. Du kan finde flere oplysninger i afsnittet [Kørselsdesign](#runtime) i dette emne.

    Yderligere oplysninger om, hvordan momskoder fastsættes i Momsberegning, finder du i [Logik for fastlæggelse af momsgruppe og varemomsgruppe](global-sales-tax-group-determination.md).

23. Konfigurer anvendelsen af debitorers momsregistreringsnumre, kreditorers momsregistreringsnumre og listekoder baseret på forretningsbehovet.
24. Vælg **Gem**, og luk derefter siden.
25. Vælg **Skift status** \> **Fuldfør**. Når status er ændret til **Fuldført**, kan versionen ikke længere redigeres.
26. Vælg **Skift status** \> **Publicer**. Denne version af konfigurationen af momsfunktionen skubbes til det globale lager og vil være synlig for hver juridiske enhed i Finance.

## <a name="set-up-tax-calculation-in-dynamics-365"></a>Konfigurere Momsberegning i Dynamics 365

Når du har fuldført opsætningen i RCS, har du en udgivet version af momsfunktionen. Udfør følgende trin for at konfigurere momsberegning i Finance.

Opsætningen i dette afsnit udføres efter juridisk enhed. Du skal konfigurere den for hver juridiske enhed, du vil aktivere momsberegning for i Finance.

1. I Finance skal du gå til **Moms** \> **Konfiguration** \> **Momskonfiguration** \> **Parametre for momsberegning**.
2. Under fanen **Generelt** skal du angive følgende felter:

    - **Aktivér momsberegningstjeneste** – Markér dette afkrydsningsfelt for at aktivere Momsberegning for den juridiske enhed. Hvis momsberegning ikke er aktiveret for den aktuelle juridiske enhed, fortsætter den juridiske enhed med at bruge det eksisterende momsprogram til at fastlægge og beregne momsen.
    - **Funktionsopsætning** – Vælg en publiceret momsfunktionsopsætning og -version for den juridiske enhed. Du kan finde flere oplysninger om, hvordan du konfigurerer og fuldfører en publiceret momsfunktion, i forrige afsnit i dette emne.
    - **Forretningsproces** – Vælg de forretningsprocesser, der skal aktiveres.

3. Definer den forventede afrundingsregel for den juridiske enhed under fanen **Beregning**. Yderligere oplysninger om afrundingslogikken finder du i [Regler for afrunding i momsberegning](https://go.microsoft.com/fwlink/?linkid=2166988).
4. Definer den forventede metode til håndtering af fejl for den juridiske enhed under fanen **Fejlhåndtering**. Følgende tre indstillinger er tilgængelige:

    - Nej
    - Advarsel
    - Fejl

    Du kan konfigurere en metode til håndtering af fejl for hver resultatkode i sektionen **Detaljer**. Hvis nogle resultatkoder ikke synkroniseres fra momsberegningstjenesten, kan du også definere en standardmetode i sektionen **Generelt**.

5. Under fanen **Flere momsregistreringer** kan du aktivere momsopgørelse, EU-listesystem og Intrastat separat for at arbejde med et scenarie med flere momsregistreringer. Du kan finde flere oplysninger om momsrapportering for flere momsregistreringer i [Rapportering for flere momsregistreringer](emea-reporting-for-multiple-vat-registrations.md).
6. Gem opsætningen, og gentag de forrige trin for hver ekstra juridisk enhed. Når en ny version udgives, og du vil anvende den, skal du angive feltet **Funktionsopsætning** under fanen **Generelt** på siden **Parametre for momsberegning** (se trin 2).
