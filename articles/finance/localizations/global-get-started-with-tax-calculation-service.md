---
title: Start her med tilføjelsesprogrammet til momsberegning
description: I dette emne beskrives, hvordan du konfigurerer tilføjelsesprogrammet til momsberegning.
author: wangchen
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 835ae33fba31d4bccb218969aa9aa61eaa7a3061
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832587"
---
# <a name="get-started-with-the-tax-calculation-add-in-preview"></a>Start her med tilføjelsesprogrammet til momsberegning (forhåndsversion)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dette emne indeholder oplysninger om, hvordan du kommer i gang med tilføjelsesprogrammet til momsberegning. Det fører dig først gennem konfigurationstrinnene i Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS) og Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Derefter gennemgås den almindelige proces for brug af tilføjelsesprogrammet Momsberegning i Finance- og Supply Chain Management-transaktioner.

Opsætningen består af fire hovedtrin:

1. Installer tilføjelsesprogrammet til momsberegning i LCS.
2. Konfigurer momsberegningsfunktionen i RCS. Denne opsætning er ikke specifik for de enkelte juridiske enheder. Den kan deles på tværs af juridiske enheder i Finance og Supply Chain Management.
3. I Finance og Supply Chain Management skal du konfigurere tilføjelsesprogrammets parametre for momsberegning efter juridisk enhed.
4. I Finance og Supply Chain Management skal du oprette posteringer som f.eks. salgsordrer og bruge tilføjelsesprogrammet til momsberegning til at fastlægge og beregne moms.

## <a name="prerequisites"></a>Forudsætninger

Før du kan fuldføre trinnene i dette emne, skal du kontrollere, at følgende forudsætninger er opfyldt:

- Du har adgang til din LCS-konto, og du har implementeret et LCS-projekt med et niveau 2-miljø (eller derover), der kører Dynamics 365 version 10.0.18 eller senere.
- Du har adgang til din RCS-konto.
- Du har kontaktet Microsoft for at aktivere flighting i dit implementerede Finance- eller Supply Chain Management-miljø.

## <a name="set-up-the-tax-calculation-add-in-in-lcs"></a>Konfigurere tilføjelsesprogrammet til momsberegning i LCS

1. Log på [LCS](https://lcs.dynamics.com)
2. Fuldfør Microsoft Power Platform-integrationsopsætningen. Du kan finde flere oplysninger under fanen [Oversigt over tilføjelsesprogrammer](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Vælg et af de implementerede miljøer uden for produktion, og vælg derefter **Installer et nyt tilføjelsesprogram**.
4. Vælg **Momsberegning (forhåndsversion)**.
5. Læs og acceptér vilkår og betingelser, og vælg derefter **Installer**.

## <a name="set-up-the-tax-calculation-add-in-in-rcs"></a>Konfigurere tilføjelsesprogrammet til momsberegning i RCS

Trinnene i dette afsnit er ikke relateret til en bestemt juridisk enhed. Du skal kun gennemføre denne procedure én gang, så du kan fuldføre den i enhver juridisk enhed i RCS.

1. Log på [RCS](https://marketing.configure.global.dynamics.com/).
2. I Finance-arbejdsområdet **Elektronisk rapportering** skal du tilføje en ny konfigurationsudbyder. Brug dit firmanavn som navnet på udbyderen. Få flere oplysninger i [Oprette konfigurationsudbydere og markere dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Vælg den konfigurationsudbyder, du lige har oprettet, og vælg derefter **Angiv som aktiv**.
4. Vælg **Microsoft**-konfigurationsudbyderen, og vælg derefter **Lagre**.
5. I feltet **Type** skal du vælge **Global**.
6. Vælg **Åbn**.
7. Gå til **Datamodel for moms**, udvid filtræet, og vælg derefter **Momskonfiguration – Europa**.
8. Vælg den seneste version, og vælg derefter **Import**.
9. Vend tilbage til arbejdsområdet **Globaliseringsfunktioner (forhåndsversion)**, vælg **Funktioner**, vælg **Momsberegning**-feltet, og vælg derefter **Tilføj**.
10. Vælg en af følgende funktionstyper:

    - **Ny funktion** – Opret en funktionsopsætning, der har tomt indhold.
    - **Baseret på eksisterende funktion** – Opret en funktion ud fra en eksisterende funktion, og kopiér indholdet fra den eksisterende funktionsopsætning.

11. Angiv et navn og en beskrivelse for funktionen, og vælg derefter **Opret funktion**.

    Når funktionen er oprettet, oprettes der automatisk en kladdeversion af den.

12. Vælg kladdeversionen af funktionen, og vælg derefter **Rediger**. Siden **Opsætning af momsberegning** er udfyldt.
13. Vælg **Konfigurationsversion**. Du bør kunne se den konfigurationsversion, du importerede i trin 8.

    Microsoft leverer en standardmomskonfiguration til tilføjelsesprogrammet til momsberegningen. Denne konfiguration opfylder de fleste krav til momsberegningsmåder. Den opdateres på baggrund af markedsfeedback. Hvis du skal udvide konfigurationen, så den opfylder bestemte krav, kan du se [Sådan bygger du udvidelse i momstjeneste](https://go.microsoft.com/fwlink/?linkid=2138483) med oplysninger om, hvordan du genererer og vælger din egen momskonfiguration.

    Når du har valgt **Konfigurationsversion**, vises der flere ekstra faner:

    - **Momskoder** – Denne fane er obligatorisk for tjenesten til momsberegning. Den bruges til at vedligeholde masterdata til momskoder. Alle momskoder, der oprettes under denne fane, synkroniseres automatisk med Finance, når du aktiverer den aktuelle version af momsfunktionsopsætningen i den juridiske enhed.
    - **Gyldighed af momskoder** – Denne fane er obligatorisk for tilføjelsesprogrammet til momsberegning. Den bruges til at definere en matrix, der bestemmer momskoden, momsgruppen og varemomsgruppen. Den momskode, der fastlægges, bruges til beregning af momsbeløbet. Værdierne i felterne **Momskode**, **Momsgruppe** og **Varemomsgruppe** returneres til Finance.
    - **Gyldighed af kundens momsregistreringsnummer** – Denne fane er valgfri for tilføjelsesprogrammet til momsberegning. Hvis der er flere momsregistreringsnumre for samme kunde, kan tilføjelsesprogrammet til momsberegning automatisk bestemme det korrekte momsregistreringsnummer. I matrixen under denne fane kan du definere de regler, som tilføjelsesprogrammet bruger til at fastlægge det. Ellers vil Finance og Supply Chain Management fortsætte med at bruge standardmomsregistreringsnummeret på momspligtige dokumenter til salgstransaktioner.
    - **Gyldighed af leverandørens momsregistreringsnummer** – Denne fane er valgfri for tilføjelsesprogrammet til momsberegning. Hvis der er flere momsregistreringsnumre for samme leverandør, kan tilføjelsesprogrammet til momsberegning automatisk bestemme det korrekte momsregistreringsnummer. I matrixen under denne fane kan du definere de regler, som tilføjelsesprogrammet bruger til at fastlægge det. Ellers vil Finance og Supply Chain Management fortsætte med at bruge standardmomsregistreringsnummeret på momspligtige dokumenter til købstransaktioner.
    - **Gyldighed af listekode** – Denne fane er valgfri for tilføjelsesprogrammet til momsberegning. Den kan hjælpe med automatisk at bestemme værdien i feltet **Listekode** ved hjælp af mere fleksible og konfigurerbare regler. I matrixen under denne fane kan du definere de regler, som tilføjelsesprogrammet bruger til at fastlægge det. Ellers vil Finance og Supply Chain Management fortsætte med at bruge standardkoden på momspligtige dokumenter.

14. Under fanen **Momskoder** skal du vælge **Tilføj** og angive momskoden samt en beskrivelse.
15. Vælg **Momskomponent**. Momskomponenten er en gruppe af momsberegningsmetoder, der blev defineret i den forrige version af den valgte momskonfiguration. Følgende momskomponenter er tilgængelige:

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

    I et scenario med importmoms skal du konfigurere en enkelt momskode med en positiv momssats og markere den som **Er importmoms**.

    Du kan f.eks. konfigurere to momskoder til modtagermoms, hvoraf den ene har en positiv momssats, og den anden har en negativ momssats, men samme satsværdi. Markér den negative momskode som **Er modtagermoms**. Du kan finde flere oplysninger om løsningen med modtagermoms i Finance i [Modtagermomsmekanisme for momsskema](emea-reverse-charge.md).
    
    For nogle momstyper, der skal udelades i beregningen af momsgrundlagsbeløb for pris inklusive transaktioner, f.eks. toldafgift i visse lande/områder, skal du markere afkrydsningsfeltet **Udelad beregning af grundbeløb**.

    Vedligehold momssatser og momsbeløbsgrænser for denne momskode.

18. Gentag trin 14 til og med 17 for at tilføje alle andre momskoder, du har brug for.
19. Under fanen **Gyldighed af momskoder** skal du vælge de kolonner, der skal bruges til at bestemme den korrekte momskode, og derefter vælge **Tilføj**.
20. Angiv eller vælg værdier for hver kolonne. Felterne **Momskode**, **Momsgruppe** og **Varemomsgruppe** returneres af denne matrix.
21. Gentag trin 19 til 20 for at konfigurere gyldigheden af kunders momsregistreringsnumre, leverandørers momsregistreringsnumre og listekoder.
22. Vælg **Gem**, og luk derefter siden.
23. Vælg **Skift status** \> **Fuldfør**. Når status er ændret til **Fuldført**, kan versionen ikke længere redigeres.
24. Vælg **Skift status** \> **Publicer**. Denne version af konfigurationen af momsfunktionen skubbes til det globale lager og vil være synlig for hver juridiske enhed i Finance.

## <a name="dynamics-365-setup"></a>Dynamics 365-opsætning

Når du har fuldført konfigurationen i RCS, som det beskrives i forrige afsnit, har du en publiceret version af momsfunktionen. Udfør følgende trin for at konfigurere tilføjelsesprogrammet til momsberegning i Finance.

Opsætningen i dette afsnit udføres efter juridisk enhed. Du skal konfigurere den for hver juridiske enhed, du vil aktivere tilføjelsesprogrammet til momsberegning for i Finance.

1. I Finance skal du gå til **Moms** \> **Konfiguration** \> **Momskonfiguration** \> **Tilføjelsesprogrammet til momsberegning (forhåndsversion)**.
2. Under fanen **Generelt** skal du angive følgende felter:

    - **Aktivér tilføjelsesprogrammet til momsberegning** – Markér dette afkrydsningsfelt for at aktivere tilføjelsesprogrammet til momsberegning for den juridiske enhed. Hvis tilføjelsesprogrammet til momsberegning ikke er aktiveret for den aktuelle juridiske enhed, fortsætter den juridiske enhed med at bruge det eksisterende momsprogram til at fastlægge og beregne momsen.
    - **Funktionsopsætning** – Vælg en publiceret momsfunktionsopsætning og -version for den juridiske enhed. Du kan finde flere oplysninger om, hvordan du konfigurerer og fuldfører en publiceret momsfunktion, i forrige afsnit i dette emne.
    - **Forretningsproces** – Vælg de forretningsprocesser, der skal aktiveres i tilføjelsesprogrammet til momsberegning.
    - **Aktivér momskoderegulering** – Angiv denne indstilling til **Ja** for at aktivere momskodereguleringer på momssiden.

3. Definer den forventede afrundingsregel for den juridiske enhed under fanen **Beregning**.
4. Definer den forventede metode til håndtering af fejl for den juridiske enhed under fanen **Fejlhåndtering**. Der er tre tilgængelige indstillinger til hver resultatkode fra tilføjelsesprogrammet til momsberegning:

    - Ingen
    - Advarsel
    - Fejl

5. Gem konfigurationen af tilføjelsesprogrammet til momsberegning.
6. Gentag trin 1 til 5 for hver ekstra juridiske enhed.

## <a name="transaction-processing"></a>Behandle transaktioner

Når du har fuldført alle opsætningsprocedurerne, kan du bruge tilføjelsesprogrammet til momsberegning til at fastlægge og beregne moms i Finance. De trin, der skal til for at behandle transaktioner, forbliver de samme. Følgende transaktioner understøttes i Finance version 10.0.18:

- Salgsproces

    - Salgstilbud
    - Salgsordre
    - Bekræftelse
    - Plukliste
    - Følgeseddel
    - Salgsfaktura
    - Kreditnota
    - Returordre
    - Gebyr i overskrift
    - Linjegebyr

- Indkøbsproces

    - Indkøbsordre
    - Bekræftelse
    - Tilgangsliste
    - Produktkvittering
    - Indkøbsfaktura
    - Gebyr i overskrift
    - Linjegebyr
    - Kreditnota
    - Returordre
    - Indkøbsrekvisition
    - Gebyrer til indkøbsrekvisitionslinje
    - Tilbudsanmodning
    - Gebyrer i overskrift til tilbudsanmodning
    - Gebyrer på linje til tilbudsanmodning

- Lagerproces

    - Flytteordre – send
    - Flytteordre – modtag
