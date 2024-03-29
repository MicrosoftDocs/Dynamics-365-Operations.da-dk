---
title: Fordelt ordrestyring (DOM)
description: Denne artikel beskriver funktionaliteten til fordelt ordrestyring (DOM) i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/16/2022
ms.topic: index-page
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.openlocfilehash: cfb89544580141ed397d27886f51fd0f1ac138d2
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785174"
---
# <a name="distributed-order-management-dom"></a>Fordelt ordrestyring (DOM)

[!include [banner](includes/banner.md)]

Denne artikel beskriver funktionaliteten til fordelt ordrestyring (DOM) i Microsoft Dynamics 365 Commerce.

DOM er en optimeringsløsning til omnikanal-ordreopfyldning, der hjælper med at maksimere ordreopfyldning i et forsyningskædenetværk. DOM hjælper dig med at sikre, at produkterne leveres til kunderne i de rette mængder, fra de korrekte kilder, på de rigtige tidspunkter. DOM kan også hjælpe dig med at få det maksimale udbytte ud af overskuddet, minimere omkostningerne og opfylde kravene på serviceniveau.

DOM bruger blandet heltalsplanlægning (MIP) og fremtidsanalysemodeller til at udføre optimeringer på både batchniveau og niveauet for individuelle ordrer. Denne egenskab giver detailhandlere mulighed for at bruge detaljerede regler til at afbalancere mange modstridende ordreopfyldningsbehov. I et moderne leveringsnetværk, hvor produktopfyldelse kan komme fra flere kanaler, skal organisationer hurtigt tilpasse sig ordreændringer, problemer med forsyninger og høj efterspørgsel. DOM hjælper dig med at maksimere ordreopfyldelse og finde de korrekte kilder til produktlevering baseret på forretningsbegrænsninger og målsætninger, som f.eks. at minimere omkostningerne ved at opfylde ordrer fra de nærmeste kilder. DOM bruger afstand mellem kilder til produktopfyldning og forsendelsesdestinationer, omkostningsfaktorer, der er defineret som optimeringsmålsætninger, og regler, der er defineret som begrænsninger, som f.eks. lager ved opfyldningsnoder, for at optimere ordreopfyldelse. DOM giver mulighed for at definere flere profiler, der gør det muligt for firmaer at køre forskellige optimeringsstrategier, afhængigt af typen af forretnings- eller forbrugersegment. 

Følgende illustration viser livscyklussen for en salgsordre i et DOM-system.

![Salgsordrelivscyklus i DOM-sammenhæng.](./media/flow.png "Salgsordrelivscyklus i DOM (fordelt ordrestyring)")

Følgende video indeholder en oversigt og DOM-funktioner i Dynamics 365 Commerce.


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5bRYl]

## <a name="set-up-dom"></a>Konfigurer DOM

1. Gå til **Systemadministration \> Opsætning \> Licenskonfiguration**.
2. På fanen **Konfigurationsnøgler** kan du udvide noden **Commerce** og derefter markere afkrydsningsfeltet **Fordelt ordrestyring**.
3. Gå til **Retail og Commerce \> Fordelt ordrestyring \> Opsætning \> DOM-parametre**.
4. På fanen **Generelt** kan du angive følgende værdier:

    - **Aktivér fordelt ordrestyring** – Angiv denne indstilling til **Ja**.
    - **Bekræft brug af Bing Kort til DOM** – Angiv denne indstilling til **Ja**.

        > [!NOTE]
        > Du kan kun angive denne indstilling til **Ja**, hvis indstillingen **Aktivér Bing Kort** på fanen **Bing Kort** på siden **Delte Commerce-parametre** (**Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Delte Commerce-parametre**) også er angivet til **Ja**, og hvis en gyldig nøgle er angivet i feltet **Bing Kort-nøgle**.
        >
        > Portalen [Bing Kort Dev Center](https://www.bingmapsportal.com/) giver mulighed for at begrænse adgangen på Bing Kort API-nøgler til et sæt domæner, som du angiver. Med denne funktion kan kunder definere et strengt sæt med henviste værdier eller IP-adresseintervaller, som nøglen kan valideres op imod. De anmodninger, der stammer fra din liste over tilladte, behandles normalt, mens anmodninger, der ikke stammer fra listen, returnerer et svar med adgang nægtet. Tilføjelse af domænesikkerhed til din API-nøgle er valgfri, og nøgler, der efterlades, som de er, kan fortsat anvendes. Listen over tilladte nøgler er uafhængig af alle dine øvrige nøgler, hvilket gør det muligt at angive særskilte regler for de individuelle nøgler. Fordelt ordrestyring understøtter ikke konfiguration af domænehenviste egenskaber.

    - **Tilbageholdelsesperiode i dage** – Angiv, hvor længe de opfyldningsplaner, som DOM kører, beholdes i systemet. Batchjobbet **Opsætning af job til sletning af DOM-opfyldningsdata** sletter opfyldningsplanen, der er ældre end det antal dage, du angiver her.
    - **Afvisningsperiode (i dage)** – Angiv, hvor lang tid der skal gå, før en afvist ordrelinje kan tildeles til det samme sted.

5. På fanen **Problemløser** kan du angive følgende værdier:

    - **Maksimalt antal forsøg på automatisk opfyldelse** – Angiv, hvor mange gange DOM-programmet skal forsøge at formidle en ordrelinje til et sted. Hvis DOM-programmet ikke kan formidle en ordrelinje til en lokation i det angivne antal forsøg, markeres ordrelinjen som en undtagelse. Derefter springes den linje over i fremtidige kørsler, indtil status nulstilles manuelt.
    - **Radius på lokalt butiksområde** – Angiv en værdi. Dette felt er med til at bestemme, hvordan lokationer er grupperet, og betragtes som værende lige med hensyn til afstanden. Hvis du f.eks. angiver **100**, betragtes hver butik eller distributionscenter inden for en radius på 100 mil som ens med hensyn til afstanden.
    - **Type af problemløser** – Vælg en værdi. To typer problemløsere frigives med Commerce: **Problemløser for produktion** og **Forenklet problemløser**. For alle computere, der skal køre DOM (dvs. alle servere, der tilhører gruppen DOMBatch), skal **Problemløser for produktion** være valgt. Problemløser for produktion kræver den særlige licensnøgle, der som standard er givet i licens og installeret i produktionsmiljøer. I nyere niveau 2+-miljøer er problemløseren for produktion allerede aktiveret. For ikke-produktionsmiljøer skal denne licensnøgle installeres manuelt. Du kan installere licensnøglen manuelt ved at gøre følgende:

        1. I Microsoft Dynamics Lifecycle Services skal du åbne det delte aktivbibliotek, vælge **Model** som aktivtype og downloade filen **DOM-licens**.
        1. Start Microsoft Internet Information Services (IIS) Manager, højreklik på **AOS Service website**, og vælg derefter **Undersøg**. Et Windows Stifinder-vindue åbnes på **\<AOS service root\>\\-webrod**. Notér stien til \<AOS Service root\>, da du skal bruge den i næste trin.
        1. Kopiér konfigurationsfilen i mappen **\<AOS Service root\>\\PackagesLocalDirectory\\DOM\\bin**.
        1. Gå til Headquarters-klienten, og åbn siden **DOM-parametre**. På fanen **Problemløser** i feltet **Type af problemløser** skal du vælge **Problemløser for produktion** og bekræfte, at der ikke vises nogen fejlmeddelelser.

        > [!NOTE]
        > Forenklet problemløser leveres, så detailhandlere kan afprøve DOM-funktionen uden at skulle installere den særlige licens. Organisationer bør ikke anvende Forenklet problemløser i produktionsmiljøer.
        >
        > Problemløser for produktion øger ydeevnen (f.eks. det antal ordrer og ordrelinjer, der kan håndteres i en kørsel) og konvergens af resultater (eftersom et batch af ordrer giver muligvis ikke de bedste resultat i visse scenarier). Reglen **Delordrer** kræver, at der oprettes en Problemløser for produktion.

6. Gå tilbage til **Retail og Commerce \> Fordelt ordrestyring \> Opsætning \> DOM-parametre**.
7. På fanen **Nummerserier** kan du tildele de nødvendige nummerserier til forskellige DOM-enheder.

    > [!NOTE]
    > Før nummerserierne der kan tildeles til enhederne, skal de defineres på siden **Nummerserier** (**Organisationsadministration \> Nummerserier \> Nummerserier**).

8. DOM-funktionen understøtter definitionen af forskellige typer DOM-regler, og organisationer kan konfigurere flere regler afhængigt af deres forretningsbehov. DOM-regler kan defineres for en gruppe af lokationer eller individuelle lokationer og for en bestemt produktkategori, et produkt eller en variant. For at oprette den gruppering af lokationer, der skal anvendes for DOM-reglerne, skal du følge disse trin:

    1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Opfyldelsesgrupper**.
    2. Vælg **Ny**, og angiv et navn og en beskrivelse for den nye gruppe.
    3. Vælg **Gem**.
    4. Vælg **Tilføj linje** for at tilføje et enkelt sted til gruppen. Du kan også vælge **Tilføj linjer** for at tilføje flere steder.

    > [!NOTE]
    > I Commerce version 10.0.12 og derover skal **Evnen til at angive steder som 'Forsendelse' eller 'Afhentning' aktiveret i gruppen Opfyldelse** være aktiveret i arbejdsområdet **Funktionsstyring**.
    >
    > Denne funktion tilføjer nye konfigurationer på siden **Opfyldelsesgruppe**, så du kan definere, om lagerstedet kan bruges til forsendelse, eller om kombinationen af lager/butik kan bruges til forsendelse, afhentning eller begge dele. 
    >
    > Hvis du aktiverer funktionen, opdateres indstillingerne, der er tilgængelige for valg af lokation, når du opretter afhentnings- eller forsendelsesordrer i POS.
    >
    > Aktivering af funktionen resulterer også i opdaterede sider i POS, når operationerne "afsend alle" eller "forsendelse angivet" er valgt.

9. For at angive regler skal du gå til **Retail og Commerce \> Fordelt ordrestyring \> Opsætning \> Administrer regler**. Følgende DOM-regler understøttes i øjeblikket:

    - **Regel for minimumslager** – Denne regeltype giver organisationer mulighed for at "ring fence" en bestemt mængde af et produkt til andre formål end ordreopfyldning. For eksempel ønsker organisationer måske ikke, at DOM skal medtage alt det lager, der findes i en butik til ordreopfyldning. I stedet ønsker de muligvis at reservere noget af lageret til kunder, der kommer ind fra gaden. Når denne regeltype anvendes, kan du definere det minimumslager, der skal beholdes for en kategori af produkter, et enkelt produkt eller en produktvariant pr. sted eller gruppe af steder. Du kan også definere minimumslager ved hjælp af et hierarki for supplerende kategorier. Hvis et produkt falder inden for flere kategorier, tildeles en supplerende kategori højeste prioritet for alle regler, hvor du kan bruge kategorier.
    - **Opfyldelse af lokations prioriteringsregel** – Denne regeltype giver organisationer mulighed for at definere et hierarki af lokationer for at bestemme den prioritet, som DOM-programmet tager i betragtning, når det forsøger at identificere ordreopfyldelseslokationer for bestemte produkter. Det gyldige interval af prioriteter er 1 til 10, hvor 1 er den højeste prioritet og 10 er den laveste prioritet. Lokationer, der har højere prioritet, tages i betragtning før lokationer, der har lavere prioritet. Hvis reglen er defineret som en fast betingelse, formidles ordrer udelukkende for steder, der er angivet prioriteter for. DOM giver fuldstændig præference for forsendelsesordrer fra én lokalitet. Hvis en hel ordre og dens linjer derfor ikke er tilgængelige fra en lokation med prioritet 1, vil DOM forsøge at opfylde den fra en lokation, der har prioritet 2.
    - **Regel for delordrer** – I Retail version 10.0.5 blev parameteren **Opfyld ordren fra kun én lokation** ændret til **Maksimalt antal lokationer til opfyldelse**. De gamle parameteraktiverede brugere til at konfigurere, om ordrer kun kan opfyldes fra én lokation eller fra så mange lokaliteter som muligt. Den nye parameter giver brugerne mulighed for at angive, om opfyldningen kan være fra et bestemt sæt lokationer (op til fem) eller fra så mange lokaliteter som muligt. For alle indstillinger undtagen opfyldning fra én lokation opdeler DOM linjen, fordi ordrebehandlingen foretages på linje. Denne regel fungerer kun med Problemløser for produktion.
    - **Offline opfyldelse af lokationsregel** – Denne regel giver organisationer mulighed for at angive en lokation eller en gruppe af lokationer som offline eller ikke er tilgængelige for DOM, så ordrer ikke kan tildeles til disse lokationer til opfyldelse.
    - **Regel for maksimalt antal afvisninger** – Denne regel giver organisationer mulighed for at definere en tærskel for antal afvisninger. Når grænsen nås, skal DOM-processoren markere en ordre eller en ordrelinje, som en undtagelse, og udelade den fra videre behandling. Ved sikring af ydeevnen kigger DOM ikke i alle afvisningers historik. 

        Når ordrelinjer tildeles til en lokation, kan lokationen afvise den tildelte ordrelinje, da den muligvis ikke kan opfylde linjen af en eller anden grund. Afviste linjer markeret som en undtagelse og placeret tilbage i puljen til behandling i den næste kørsel. Under næste kørsel forsøger DOM at tildele den afviste linje til en anden lokation. Den nye lokation kan også afvise den tildelte ordrelinje. Denne cyklus af tildeling og afvisning kan forekomme flere gange. Når antallet af afvisninger når den angivne grænse, markerer DOM ordrelinjen som en permanent undtagelse, og vælger ikke linjen til tildeling igen. DOM medtager ordrelinjen igen til gentildeling, hvis en bruger manuelt nulstiller status for ordrelinjen.

    - **Regel for maksimal afstand** – Denne regel giver organisationer mulighed for at angive den maksimale afstand, der kan være til en lokation eller en gruppe af lokationer for at opfylde ordren. Hvis der er angivet overlappende regler for maksimal afstand for en lokation, anvender DOM den laveste maksimale afstand, der er defineret for den pågældende lokation.
    - **Regel for maks. antal ordrer** – Denne regel giver organisationer mulighed for at definere det maksimale antal ordrer, som en lokation eller en gruppe af lokationer kan behandle. Under optimeringsprocessen vil systemet tage højde for ordrer, der ikke er afsendt fra disse lokationer. Denne kontrol udføres på tværs af profiler. Hvis det maksimale antal ordrer, der overlapper, derfor defineres på tværs af profiler for den samme lokation, vil systemet overveje det maksimale antal ordrer, der er defineret på tværs af alle profiler. 

    Her er nogle af de fælles attributter, der kan defineres for alle de foregående regeltyper:

    - **Startdato for** og **Slutdato** – Brug disse felter til at aktivere hver regel efter dato.
    - **Deaktiveret** – Kun regler, der har værdien **Nej** for dette felt tages i betragtning i en DOM-kørsel.
    - **Fast betingelse** – En regel kan angives som enten en fast betingelse eller ikke en fast betingelse. Hver DOM-kørsel gennemgår to gentagelser. I den første gentagelse behandles hver regel som en fast betingelse, uanset indstillingen i dette felt. Med andre ord anvendes hver regel. Den eneste undtagelse er reglen **Lokations prioritet**. I den anden gentagelse fjernes de regler, der ikke er angivet som faste betingelser, og de ordrer eller ordrelinjer, der ikke blev tilknyttet til lokationer, da alle reglerne blev anvendt, tildeles til lokationer.

10. Opfyldningsprofiler bruges til at gruppere en samling regler, juridiske enheder, salgsordreoprindelser og leveringsmåder. Hver DOM-kørsel er for en bestemt opfyldelsesprofil. På denne måde kan organisationer definere og køre et sæt regler for et sæt juridiske enheder på ordrer, der har en bestemt salgsordreoprindelse og leveringsmåde. Hvis der skal køres forskellige sæt regler for forskellige sæt salgsordreoprindelser eller leveringsmåder, kan opfyldningsprofilerne derfor defineres i overensstemmelse hermed. Benyt følgende fremgangsmåde for at konfigurere opfyldelsesprofiler:  

    1. Gå til **Retail og Commerce \> Fordelt ordrestyring \> Opsætning \> Opfyldningsprofiler**.
    2. Vælg **Ny**.
    3. Angiv værdier i felterne **Profil** og **Beskrivelse**.
    4. Angiv indstillingen **Anvend automatisk resultat**. Hvis du angiver denne indstilling til **Ja**, anvendes resultaterne af DOM-kørslen for profilen automatisk på salgsordrelinjerne. Hvis du angiver indstillingen til **Nej**, kan resultaterne kun vises i opfyldningsplanen. De anvendes ikke for salgsordrelinjerne.
    5. Hvis du ønsker, at DOM (fordelt ordrestyring)-profilen skal køres for ordrer, der har enhver salgsordreoprindelse, herunder ordrer, hvor salgsordreoprindelsen ikke er defineret, skal du angive indstillingen **Behandl ordrer med tomme ordreoprindelser** til **Ja**. Hvis du kun vil køre profilen for et par salgsordreoprindelser, kan du definere dem på siden **Salgsoprindelser** som beskrevet senere.

        > [!NOTE]
        > I Commerce version 10.0.12 og nyere skal **Evnen til at tildele Opfyldelsesgruppe til en Opfyldelsesprofil** være aktiveret i arbejdsområdet **Funktionsstyring**. Med denne funktion kan du angive en liste over lagersteder, som DOM skal overveje, når optimering køres med en opfyldningsprofil. Hvis listen over lagersteder ikke er angivet, vil DOM kigge på alle lagersteder på juridiske enheder, der er defineret i profilen.
        >
        > Denne funktion tilføjer en ny konfiguration på siden **Opfyldelsesprofil**, der kan knyttes til en enkelt opfyldelsesgruppe. 
        >
        > Hvis du vælger opfyldelsesgruppe, udføres DOM (fordelt ordrestyring)-reglerne for den pågældende opfyldelsesprofil effektivt i forhold til de "forsendelseslagersteder", der er inkluderet i opfyldelsesgruppen. 
        > 
        > Hvis du vil bruge denne funktion effektivt, skal du sikre dig, at der er én opfyldelsesgruppe, der indeholder alle forsendelseslagersteder, og derefter tilknytte denne opfyldelsesgruppe til opfyldelsesprofilen.

    6. På oversigtspanelet **Juridiske enheder** skal du vælge **Tilføj** og derefter vælge en juridisk enhed.
    7. På oversigtspanelet **Regler** skal du vælge **Tilføj** og derefter vælge den regel, der skal tilknyttes til profilen.
    8. Gentag de to forrige trin, indtil alle de nødvendige regler er tilknyttet til profilen.
    9. Vælg **Gem**.
    10. I handlingsruden skal du på fanen **Opsætning** vælge **Leveringsmåder**.
    11. På siden **Leveringsmåder** skal du vælge **Ny**.
    12. I feltet **Virksomhed** skal du vælge den juridiske enhed. Listen med virksomheder er begrænset til de juridiske enheder, du tidligere har tilføjet.
    13. I feltet **Leveringsmåde** skal du vælge den leveringsmåde, der skal tilknyttes til denne profil. En leveringsmåde kan ikke tilknyttes til flere aktive profiler.
    14. Gentag de to forrige trin, indtil alle de nødvendige leveringsmåder er tilknyttet til profilen.
    15. Luk siden **Leveringsmåder**.
    16. I handlingsruden skal du på fanen **Opsætning** vælge **Salgsordreoprindelser**.
    17. På siden **Ordreoprindelser** skal du vælge **Ny**.
    18. I feltet **Virksomhed** skal du vælge den juridiske enhed. Listen med virksomheder er begrænset til de juridiske enheder, du tidligere har tilføjet.
    19. I feltet **Ordreoprindelser** skal du vælge den ordreoprindelse, der skal tilknyttes til denne profil. En ordreoprindelse kan ikke tilknyttes til flere aktive profiler.
    20. Gentag de to forrige trin, indtil alle de nødvendige ordreoprindelser er tilknyttet til profilen.
    21. Luk siden **Ordreoprindelser**.
    22. Angiv indstillingen **Aktivér profil** til **Ja**. Hvis der er fejl i opsætningen, modtager du en advarselsmeddelelse.

## <a name="dom-processing"></a>DOM (fordelt ordrestyring)-behandling

DOM (fordelt ordrestyring) kører kun i et batchjob. Du kan konfigurere batchjobbet til DOM (fordelt ordrestyring)-kørsler ved at følge disse trin.

1. Gå til **Retail og Commerce \> Fordelt ordrestyring \> Batchbehandling \> Opsætning af DOM (fordelt ordrestyring)-processorjob**.
1. På oversigtspanelet **Parametre** i feltet **Opfyldelsesprofil** skal du vælge en profil, der skal køres DOM (fordelt ordrestyring) for.
1. På oversigtspanelet **Kør i baggrunden** i feltet **Batchgruppe** skal du vælge en batchgruppe, der er konfigureret.
1. I feltet **Opgavebeskrivelse** skal du angive et navn til batchjobbet.
1. Vælg **Gentagelse**, og definer gentagelsen af batchjobbet.
1. Vælg **OK**.

På behandlingstidspunktet medtager DOM ordren og ordrelinjerne som beskrevet her:

- Ordrelinjer, der opfylder kriterierne for salgsordreoprindelser, leveringsmåder og juridisk enhed som defineret i DOM (fordelt ordrestyring)-profilen, og som også opfylder nogen af disse kriterier:

    - De oprettes fra Commerce-kanaler.
    - De er aldrig blevet formidlet af DOM (fordelt ordrestyring).
    - De er blevet formidlet af DOM (fordelt ordrestyring) før, men de er markeret som undtagelser og ligger under tærsklen for maksimalt antal forsøg.
    - Leveringsmåden er ikke afhentning eller elektronisk levering.
    - De ikke er markeret til levering.
    - De er ikke udelukket manuelt.

- Ordrer, der ikke er på hold

Efter anvendelse af regler, lagerbegrænsninger og optimering vælger DOM (fordelt ordrestyring) den placering, der er tættest på kundens leveringsadresse. DOM konverterer adresser af **leveringstypen** til værdier for leveringstid og længde. Derefter konverterer den leveringsadressen på salgsordren til værdier for leveringstid og længde, og opdaterer værdierne for placering og længde for adressen til fremtidig brug. DOM afhænger af Bing Maps til at angive nøjagtige værdier for adresse, by og postnummer.

DOM bruger Bing Maps-API'en til at beregnevej og vejlængde, afhængigt af indstillingerne. Derefter bruges disse oplysninger til at fastlægge forsendelsesomkostningerne. Optimeringsmodellen prioriterer opfyldelsen af en komplet ordre fra én lokation. Selvom en del af en ordre er tilgængelig i samme by eller postnummer, er modellen optimeret for at reducere antallet af forsendelser. 

DOM søger i den tilgængelige lagerbeholdning ved at få vist den disponible lagerbeholdning i lagerstedS V2-enheder. Under hver batchkørsel opdeler DOM ordrer i batches, afhængigt af parameterværdien for **DOM-processor** for de opgaver, der er defineret i profilen. Standardværdien for denne parameter er **2000**. Hvis f.eks. 10.000 ordrelinjer optimeres i en kørsel, og parameteren **DOM Processor** er angivet til standardværdien **2000**, opretter DOM fem batches, der behandles samtidigt. Opfyldningsplaner hentes derefter fra optimeringen og anvendes på linjen. Hvis ordrelinjen skal opdeles mellem to lokationer, sikrer DOM, at priser og moms fordeles korrekt på alle linjer.

![Salgsordrekriterier.](./media/ordercriteria.png "Salgsordrekriterier")

## <a name="results-of-dom-runs"></a>Resultater af DOM-kørsler

Hvis opfyldelsesprofilen er indstillet til **Anvend automatisk** anvendes resultaterne af kørslen automatisk for salgsordrelinjerne, og ordreopfyldningsplanen kan vises separat. Men hvis opfyldelsesprofilen ikke er angivet til **Anvend automatisk** kan du kun se resultaterne af kørslen fra visningen af opfyldningsplanen. 

Følg disse trin for at få vist alle de opfyldningsplaner, der genereres.

1. Gå til **Retail og Commerce \> Fordelt ordrestyring \> Fordelt ordrestyring**.
2. I arbejdsområdet **Fordelt ordrestyring** skal du vælge feltet **Opfyldningsplaner**.
3. Vælg ID'et for den relevante ordreopfyldningsplan for at få vist opfyldningsplanen.

    Sektionen med ordreoplysninger i opfyldningsplanen viser de oprindelige salgsordrelinjer, der var en del af kørslen. Ud over standardfelterne for salgsordrelinjer indeholder sektionen med ordreoplysninger også følgende tre DOM (fordelt ordrestyring)-relaterede felter:

    - **Opfyldelsestype** – Dette felt angiver, om salgsordrelinjen er fuldt formidlet, delvist formidlet eller slet ikke formidlet til en lokation.
    - **Opdel** – Dette felt angiver, om en salgsordrelinje er blevet opdelt og formidlet til forskellige placeringer.
    - **Antal opfyldelseslokationer** – Dette felt angiver, hvor mange opfyldningslinjer, der er oprettet for en salgsordrelinje (baseret på det antal lokationer, som den oprindelige salgsordrelinje er formidlet til).

    Sektionen med oplysninger om ordreopfyldelse viser tildelingen af de oprindelige salgsordrelinjer til forskellige lokationer sammen med deres mængder.

## <a name="order-line-actions-and-statuses"></a>Handlinger og statusser for ordrelinjer

I det følgende beskrives indstillingerne på ordrelinjen. For at åbne ordrelinjen skal du gå til **Retail og Commerce \> Debitorer \> Alle salgsordrer**.

- Hvis du angiver indstillingen **Udeluk fra DOM-behandling** på fanen **Generelt** i salgsordrelinjen til **Ja**, udelukkes ordren eller ordrelinjen fra DOM-behandling.
- Feltet **DOM-status** på fanen **Generelt** i salgsordrelinjen kan angives til en af følgende værdier:

    - **Ingen** – Ordrelinjen er aldrig blevet formidlet.
    - **Fuldført** – Ordrelinjen er blevet formidlet og tildelt til en lokation.
    - **Undtagelse** – Ordrelinjen er blevet formidlet, men kan ikke tildeles til en lokation. Undtagelser har flere undertyper, der kan ses fra DOM-arbejdsområdet:

        - **Intet disponibelt antal** – Der er intet tilgængeligt lager at tildele ordren til på lokationerne.
        - **Maksimalt antal afvisninger** – Ordrelinjen har nået den maksimale grænse for afvisninger.
        - **Dataændringskonflikt** – Salgsordrelinjen er blevet ændret, siden ordren blev formidlet. Opfyldningsplanen kan derfor ikke anvendes for ordren.
        - **Specifik undtagelse for ordrelinje** – Der er flere undtagelser på ordrelinjen.

- Under salgsordreindtastning kan DOM (fordelt ordrestyring) køres i en interaktiv tilstand. Mens du indtaster en ordrelinje, når du har angivet produktet og antallet, kan du vælge **Opdater linje** og derefter klikke på **DOM** (fordelt ordrestyring) og vælge **Foreslå opfyldelseslokation**. Du ser derefter en liste over lokationer, der er baseret på DOM (fordelt ordrestyring)-regler, som kan opfylde antallet på ordrelinjen. Denne listen er sorteret efter afstand. Vælg en lokation for at angive den relevante websted og lagersted på salgsordrelinjen. For at denne funktion kan fungere, skal der være en eksisterende, aktivt opfyldningsprofil, der svarer til salgsoprindelsen og leveringsmåden på salgslinjen.
- For at få vist DOM-kørselslogfiler for en salgsordrelinje skal du vælge **Salgsordrelinje** og derefter under **DOM** vælge **Vis DOM-logfiler**. DOM-logfilerne viser alle hændelser og logfiler, der blev oprettet af DOM (fordelt ordrestyring)-kørslen. Logfilerne kan hjælpe dig med at forstå, hvorfor en bestemt lokation er tildelt til ordrelinjen, og hvilke regler og begrænsninger der blev taget i betragtning som en del af tildelingen. På fanen **Administrer** er DOM-logfilerne også tilgængelige på salgsordrehovedniveau.

## <a name="run-a-clean-up-job-for-dom-fulfillment-plans"></a>Kør et oprydningsjob for DOM (fordelt ordrestyring)-opfyldningsplaner

Når DOM (fordelt ordrestyring)-behandlingen køres, oprettes der opfyldningsplaner. Med tiden beholder systemet adskillige opfyldningsplaner. For at administrere det antal opfyldningsplaner, som systemet opbevarer, kan du konfigurere et batchjob, der sletter ældre opfyldningsplaner baseret på værdien **Tilbageholdelsesperiode i dage**.

1. Gå til **Retail og Commerce \> Fordelt ordrestyring \> Batchbehandling \> Opsætning af job til sletning af DOM-opfyldelsesdata**. 
1. Vælg en konfigureret batchgruppe i feltet **Batchgruppe**.
1. Vælg **Gentagelse**, og definer gentagelsen af batchjobbet.
1. Vælg **OK**.

## <a name="more-information"></a>Flere oplysninger

Her er nogle ting, du bør være opmærksom på, når du bruger DOM (fordelt ordrestyring)-funktionen:

- DOM (fordelt ordrestyring) ser i øjeblikket kun på ordrer, der er oprettet ud fra Commerce-kanaler. Salgsordrer identificeres som detailsalgsordrer, når indstillingen **Commerce-salg** er angivet til **Ja**.
- Microsoft har ikke testet DOM med funktioner til avanceret lagerstedsstyring. Derfor skal kunder og partnere være omhyggelige med at afgøre, om DOM (fordelt ordrestyring) er kompatibel med de funktioner og processer for avanceret lagerstedsstyring, der er relevante for dem. Avanceret lagerstyring giver mulighed for konfigurerbare dimensioner, f.eks. lagerstatus, der ikke giver en præcis forståelse af den disponible lagerbeholdning. DOM indeholder en skalerbar metode til angivelse af tilgængelig lagerbeholdning til implementeringer, hvor der bruges avanceret lager. Den kan bruges til at arbejde med tilpassede værdier for lagerstatus og andre dimensioner.

    Extensibility i DOM er begrænset, fordi optimering finder sted i den forudindstillede MIP-model, der tager hensyn til optimeringen og begrænsningerne her. Der er allerede adskillige extensible punkter tilgængelige til angivelse af lager- og efterbehandlingsoptimering. DOM-profiler kan være forskellige efter salgsoprindelses- og leveringstilstand. Salgsordreoprindelse kan angives under ordreinddrivelse, og der kan bruges forskellige optimeringsstrategier baseret på disse værdier. DOM understøtter også oprettelsen af brugerdefinerede batchjob, der kan tage opgaven DOM-processor som input og aktivere profilen til at blive overført som en parameter. Derfor kan der køres én optimering efter den anden for at understøtte forskellige forretningsscenarier.

- DOM (fordelt ordrestyring) er kun tilgængelig i sky-versionen af Commerce. Funktionen understøttes ikke i lokale installationer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
