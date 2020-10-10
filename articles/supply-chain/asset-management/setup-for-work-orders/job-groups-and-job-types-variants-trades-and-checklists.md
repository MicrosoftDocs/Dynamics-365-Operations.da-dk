---
title: Kategorier af vedligeholdelsesjobtyper og vedligeholdelsesjobtyper, varianter af vedligeholdelsesjobtyper, vedligeholdelsesjobfag og vedligeholdelsestjeklister
description: Dette emne beskriver kategorier af vedligeholdelsesjobtyper og vedligeholdelsesjobtyper, varianter af vedligeholdelsesjobtyper, vedligeholdelsesjobfag og vedligeholdelsestjeklister i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetJobTypeDefaultForecast, EntAssetJobTrade, EntAssetJobTypeDefaultCopy, EntAssetChecklistVariableValueLookup, EntAssetChecklistTemplateCreate, EntAssetJobVariant, EntAssetJobTypeDefaultReference, EntAssetJobTypeDefaultChecklist, EntAssetJobTypeDefault, EntAssetJobType, EntAssetJobTypeDefaultChecklistCopy, EntAssetChecklistTemplate, EntAssetJobTypeDefaultDescription, EntAssetJobTypeLookup, EntAssetJobTypeDefaultToolCopy, EntAssetJobTypePreviewPart, EntAssetJobTypeDefaultTool, EntAssetJobTypeDefaultForecastCopy, EntAssetChecklistTemplateLookup, EntAssetJobGroup, EntAssetChecklistVariable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8bf7c53a6150a2beeca5c6e9b5ab4ea98584158d
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889069"
---
# <a name="maintenance-job-type-categories-and-maintenance-job-types-maintenance-job-type-variants-maintenance-job-trades-and-maintenance-checklists"></a>Kategorier af vedligeholdelsesjobtyper og vedligeholdelsesjobtyper, varianter af vedligeholdelsesjobtyper, vedligeholdelsesjobfag og vedligeholdelsestjeklister

[!include [banner](../../includes/banner.md)]

 

Der er knyttet en aktivtype til hvert aktiv. Aktivtyper definerer de vedligeholdelsesjobtyper (og dermed vedligeholdelsesjob), der kan udføres på aktiver. Du skal vælge en vedligeholdelsesjobtype, når du opretter en arbejdsordre. Du kan kun vælge de vedligeholdelsesjobtyper, der er relateret til opsætningen af den aktivtype, der bruges for aktivet.

Der findes en grafisk oversigt over aktiver og vedligeholdelsesjobtyper og deres forbindelse til arbejdsordrer i [Arbejdssteder og aktiver](../overview/functional-locations-and-objects.md).

Varianter af vedligeholdelsesjobtyper kan konfigureres for en vedligeholdelsesjobtype. Varianter af vedligeholdelsesjobtype definerer varianter af en jobtype, f.eks. størrelser (lille, mellem eller stor), perioder (hver uge, hver anden uge, en måned eller tre måneder) og konfigurationer (lav standard, fleksibel eller høj ydeevne).

Vedligeholdelsesjobfag indeholder oplysninger om professionelle fag, f.eks. mekaniske, elektriske og hydrauliske fag. Kompetencekravene kan konfigureres for et vedligeholdelsesjobfag. Alle vedligeholdelsesjobfag kan bruges i forhold til alle typer af vedligeholdelsesjob. Valg af en vedligeholdelsesjobtypevariant og/eller vedligeholdelsesjobfag på en arbejdsordre er valgfrit.

For hver vedligeholdelsesjobtype kan der oprettes variationer af vedligeholdelsesjobtypens opsætning. Hvis du f.eks. har en vedligeholdelsesjobtype, der hedder **Service**, kan du oprette følgende variationer for den pågældende vedligeholdelsesjobtype **Lastbiler 30.000 km**, **Personbiler 30.000 km** og **Varevogne 30.000 km**.

Kategorier af vedligeholdelsesjobtyper bruges til at indsamle en gruppe vedligeholdelsesjobtyper til oversigtsformål. Eksempler på vedligeholdelsesjobtypers kategorier kan omfatte **Kalibrering**, **Inspektion**, **Eftersyn**og **Instrumentering.**

Der bruges skabeloner for vedligeholdelsestjekliste og variabler for vedligeholdelsestjekliste til at oprette vedligeholdelsestjeklister. Vedligeholdelsestjeklister defineres for vedligeholdelsesjobtyper og bruges på arbejdsordrer.

Du skal først konfigurere de påkrævede kategorier af vedligeholdelsesjobtyper, varianter af vedligeholdelsesjobtyper og vedligeholdelsesjobfag. Du skal derefter oprette vedligeholdelsesjobtyper. Endelig skal du på siden **Standarder for vedligeholdelsesjobtype** oprette alle de varianter af vedligeholdelsesjobtyper, der kræves til dit udstyr. På denne side kan du også oprette budgetter, vedligeholdelsestjeklister og værktøjer til en kombination af vedligeholdelsesjobtyper.

> [!NOTE]
> En vedligeholdelsesjobtype kan kun være relateret til én kategori af vedligeholdelsesjobtype.

## <a name="create-a-maintenance-job-type-category"></a>Oprette en kategori for vedligeholdelsesjobtype

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Job** \> **Kategorier af vedligeholdelsesjobtype**.
2. Vælg **Ny**.
3. I feltet **Kategorier af vedligeholdelsesjobtype** skal du angive et id for kategorien af vedligeholdelsesjobtype.
4. Indtast et navn i feltet **Navn**.

    Når du har relateret kategorier af vedligeholdelsesjobtyper til vedligeholdelsesjobtyper, viser feltet **Jobtyper** antallet af vedligeholdelses jobtyper, der er relateret til denne kategori af vedligeholdelsesjobtype.

![Siden Kategorier af vedligeholdelsesjobtype](media/01-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type-variant"></a>Oprette en variant af en vedligeholdelsesjobtype

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Job** \> **Varianter af vedligeholdelsesjobtype**.
2. Vælg **Ny**.
3. I feltet **Variant af vedligeholdelsesjobtype** skal du angive et id for varianten af vedligeholdelsesjobtype.
4. Indtast en beskrivelse i feltet **Beskrivelse**.
5. Vælg **Tilføj** i oversigtspanelet **Vedligeholdelsesjobtyper** for at tilføje en vedligeholdelsesjobtype.
6. Vælg vedligeholdelsesjobtypen for i feltet **Vedligeholdelsesjobtype**.
7. Gentag trin 5 til 6 for at føje flere vedligeholdelsesjobtyper til varianten af vedligeholdelsesjobtype.

    I oversigtspanelet **Detaljer** viser feltet **Jobtyper** antallet af vedligeholdelsesjobtyper, der er føjet til denne variant af vedligeholdelsesjobtypen.

![Siden Varianter af vedligeholdelsesjobtype](media/02-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-trade"></a>Oprette et vedligeholdelsesjobfag

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Job** \> **Vedligeholdelsesjobfag**.
2. Vælg **Ny**.
3. Angiv et id for vedligeholdelsesjobfaget i feltet **Fag**.
4. Indtast en beskrivelse i feltet **Beskrivelse**.
5. I oversigts panelet **Færdigheder** skal du vælge **Tilføj** for at tilføje en ny færdighed, der skal relateres til vedligeholdelsesjobfaget.
6. Vælg færdigheden i feltet **Færdighed**.
7. Vælg færdighedsniveauet i feltet **Niveau**.
8. Gentag trin 5 til 7 for at føje flere færdigheder til vedligeholdelsesjobfaget.

    I oversigtspanelet **Detaljer** viser feltet **Færdigheder** antallet af færdigheder, der er føjet til dette vedligeholdelsesjobfag.

9. I oversigts panelet **Certifikater** skal du vælge **Tilføj** for at føje et certifikat til vedligeholdelsesjobfaget.
10. I feltet **Certifikattype** skal du vælge certifikatet.
11. Gentag trin 9 til 10 for at føje flere certifikater til vedligeholdelsesjobfaget.

    I oversigtspanelet **Detaljer** viser feltet **Certifikater** antallet af certifikater, der er føjet til dette vedligeholdelsesjobfag.

![Siden Vedligeholdelsesjobfag](media/03-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-variable"></a>Oprette en variabel til vedligeholdelsestjekliste

Når du opretter linjer til vedligeholdelsestjeklisten i standarden for vedligeholdelsesjobtypen, skal du vælge en type af vedligeholdelsestjekliste. **Variabel** er en type af vedligeholdelsestjekliste. Den bruges til at definere et muligt resultat i et interval på en vedligeholdelsestjeklistelinje, der er relateret til en arbejdsordrelinje. En variabel giver dig mulighed for at oprette et sæt foruddefinerede resultater uden at skulle foretage en præcis måling.

**Eksempel 1:** Du kan måle olieniveauet ved at definere tre værdier: **Niveauet er for højt**, **Niveauet er for lavt** og **Niveauet er inden for intervallet**. For hver værdi kan du definere, om værdiens resultat er **Bestået**, **Mislykket** eller **Ingen**.

**Eksempel 2:** Du foretager en visuel inspektion af et stykke udstyr for at vurdere slitage.

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Vedligeholdelsestjeklister** \> **Variabler til vedligeholdelsestjeklister**.
2. Vælg **Ny**.
3. Angiv et id for vedligeholdelsestjeklistens variabel i feltet **Variabel**.
4. Indtast et navn i feltet **Navn**.
5. Vælg **Tilføj** i oversigtspanelet **Generelt** for at tilføje en variabellinje.

    Der indsættes automatisk et fortløbende linjenummer i feltet **Linjenummer**. Når du har tilføjet alle linjerne, kan du ændre linjenumrene efter behov. Når du vælger linje og derefter trykker på tasten **Pil ned**, indsættes det næste nummer i rækkefølgen automatisk på næste linje.

6. Indtast en beskrivelse i feltet **Værdi**.
7. Vælg et resultat for linjen i feltet **Resultat**.

![Siden Variabler til vedligeholdelsestjeklister](media/04-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-template"></a>Oprette en skabelon for en vedligeholdelsestjekliste

Skabeloner til vedligeholdelsestjeklister kan bruges som et almindeligt sæt opgaver, som en arbejder skal udføre for at fuldføre en arbejdsordre korrekt. Der refereres til skabeloner fra vedligeholdelsestjeklistelinjer i standardtypen for vedligeholdelsesjob. Der kan refereres til skabeloner på tværs af flere standardlinjer for vedligeholdelsesjobtype. Derfor kan du let genbruge et sæt almindelige opgaver på vedligeholdelsestjeklisten. Eksempler på skabeloner til vedligeholdelsestjeklister omfatter generelle sikkerhedsinstruktioner og en liste over elementer og betingelser, der skal kontrolleres på en bestemt pumpe eller lignende modeller af et transportbånd.

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Vedligeholdelsestjeklister** \> **Skabeloner til vedligeholdelsestjekliste**.
2. Vælg **Ny**.

    Der indsættes automatisk et skabelon-id i feltet **Skabelon til vedligeholdelsestjekliste**.

3. Indtast et navn til vedligeholdelsestjeklisteskabelonen i feltet **Navn**.
4. Vælg **Tilføj** i oversigtspanelet **Vedligeholdelsestjeklistelinjer** for at tilføje en skabelonlinje.

    Der indsættes automatisk et fortløbende linjenummer i feltet **Linjenummer**. Når du har tilføjet alle linjerne, kan du ændre linjenumrene efter behov. Når du vælger linje og derefter trykker på tasten **Pil ned**, indsættes det næste nummer i rækkefølgen automatisk på næste linje.

5. Angiv en type for vedligeholdelsestjeklistelinjen i feltet **Type**. For hver vedligeholdelsestjeklistetype vises de relaterede felter i oversigtspanelet **Linjedetaljer**. Følgende værdier er tilgængelige:

    - **Tekst** – Linjen indeholder tekst, der beskriver, hvad der skal gøres. Brug denne type af vedligeholdelsestjekliste, hvis du vil have, at en arbejder skal kontrollere eller inspicere noget, uden at du forventer et specifikt (målbart) resultat. Når du har valgt denne type, skal du angive et navn eller en overskrift i feltet **Navn**. Indtast en beskrivelse af, hvad der skal gøres, i feltet **Instruktioner**. Hvis trinnet er obligatorisk for vedligeholdelsestjeklisten, skal du angive indstillingen **Obligatorisk** til **Ja**.
    - **Hoved** – Linjen bruges som en overskrift til at gruppere vedligeholdelsestjeklinjer, der vises under den. Denne type er nyttig, hvis du har flere vedligeholdelsestjeklistelinjer, der kan inddeles i bestemte områder. Hoveder giver en oversigt for den arbejder, der skal udføre en vedligeholdelsestjekliste med mange vedligeholdelsestjeklistelinjer. Når du har valgt denne type, skal du indtaste et navn i feltet **Navn**.
    - **Skabelon** – Linjen bruges til at oprette en reference til en eksisterende skabelon. Når du har valgt denne type, skal du indtaste et navn til skabelonen i feltet **Navn**. I feltet **Skabelon** skal du vælge skabelonen.
    - **Variabel** – Linjen bruges til at definere et muligt resultat i et interval. Du kan finde oplysninger om, hvordan du konfigurerer variabler for vedligeholdelsestjeklister, afsnittet [Oprette en variabel til vedligeholdelsestjekliste](#create-a-maintenance-checklist-variable). Når du har valgt denne type, skal du indtaste et sigende navn til variablen i feltet **Navn**. Vælg variablen i feltet **Variabel**. Indtast en beskrivelse af, hvad der skal gøres, i feltet **Instruktioner**. Hvis trinnet er obligatorisk for vedligeholdelsestjeklisten, skal du angive indstillingen **Obligatorisk** til **Ja**.
    - **Mål** – Linjen bruges til at registrere et bestemt mål. Du kan konfigurere et mål, der skal relateres til en foruddefineret tæller. Når du har valgt denne type, skal du indtaste et navn til skabelonen i feltet **Navn**. Hvis trinnet er obligatorisk for vedligeholdelsestjeklisten, skal du angive indstillingen **Obligatorisk** til **Ja**. Hvis du vil bruge målelinjen som en tællerregistrering, skal du vælge tælleren i feltet **Tæller**. Det relaterede felt **Enhed** opdateres derefter automatisk. Hvis du har valgt en tæller, skal du vælge opdateringsmetoden i feltet **Værdi**. I felterne **Min. værdi** og **Maks. værdi** skal du angive det tilladte værdiinterval. Indtast en beskrivelse af, hvad der skal gøres, i feltet **Instruktioner**.

        > [!NOTE]
        > En linje af **Mål**-typen, der ikke har en tælleropsætning, behandles som en uafhængig måleregistrering, som der ikke er nogen automatisk opfølgning til i aktivstyring. Ligeledes, hvis den valgte tællertype ikke findes på det aktiv, der er knyttet til arbejdsordren, behandles vedligeholdelsestjeklisteopgaven som et uafhængigt mål. Tællerværdien kan ændres flere gange. Den bogføres først, når [livscyklustilstanden for arbejdsordren](work-order-lifecycle-states.md) ændres til en tilstand, hvor indstillingen **Behandling af vedligeholdelsestjekliste** er angivet til **Ja**.

    I oversigtspanelet **Detaljer** indeholder feltet **Tjek** det samlede antal tjeklistelinjer i skabelonen. Dette antal omfatter de indlejrede linjer i enhver eksisterende skabelon, som du har refereret til i din skabelon.

![Siden Skabeloner til vedligeholdelsestjekliste](media/05-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type"></a>Oprette et vedligeholdelsesjobtype

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Job** \> **Vedligeholdelsesjobtyper**.
2. Vælg **Ny**.
3. I feltet **Vedligeholdelsesjobtype** skal du angive et id for vedligeholdelsesjobtypen.
4. Indtast et navn i feltet **Navn**.

    Oversigtspanelet **Detaljer** indeholder en oversigt over antallet af varianter af vedligeholdelsesjobtyper, færdigheder, certifikater, efterfølgende job og aktivtyper, der er oprettet for denne type vedligeholdelsesjob. Feltet **Opsætningslinjer** viser antallet af standardlinjer for vedligeholdelsesjobtypen, der er defineret for denne vedligeholdelsesjobtype. I feltet **Aktiver** vises antallet af aktive aktiver, der aktuelt bruger denne vedligeholdelsesjobtype.

5. I feltet **Kategori af vedligeholdelsesjobtype** i oversigtspanelet **Generelt** skal du vælge en kategori af vedligeholdelsesjobtype.
6. Angiv indstillingen **Aktiviteter med vedligeholdelsesnedetid** til **Ja**, hvis typen af vedligeholdelsesjob kræver et vedligeholdelsesstop for udstyret, før jobbet kan udføres.
7. Angiv en beskrivelse af vedligeholdelsesjobtypen i oversigtspanelet **Beskrivelse**.
8. I oversigtspanelet **Varianter af vedligeholdelsesjobtype** kan du føje varianter til vedligeholdelsesjobtypen.
9. I oversigtspanelerne **Påkrævede færdigheder** og **Påkrævede certifikater** kan du føje færdigheds- og certifikatkrav til typen af vedligeholdelsesjob.
10. Hvis der derefter skal udføres en bestemt type vedligeholdelsesjob, skal du tilføje den i oversigtspanelet **Efterfølgende job**. Du kan også oprette en variant og et fag for vedligeholdelsesjobtypen, der er relateret til vedligeholdelsesjobtypen. Hvis det efterfølgende job skal starte et bestemt antal dage før eller efter starten af det job, der bruger denne vedligeholdelsesjobtype, skal du angive antallet af dage i feltet **Dages forsinkelse**. Positive tal angiver dage efter startdatoen for det relaterede job, og negative tal angiver dage før den planlagte start af det relaterede job. Hvis du f.eks. angiver **5**, vil det efterfølgende job starte fem dage efter startdatoen for det job, der er relateret til vedligeholdelsesjobtypen. Hvis du f.eks. angiver **-3**, vil det efterfølgende job starte tre dage før den planlagte start for det job, der er relateret til vedligeholdelsesjobtypen.

    > [!NOTE]
    > Hvis du tilføjer mere end én linje i vedligeholdelsesjobtypen, angiver sekvensen af linjerne den rækkefølge, de skal udføres i. Rækkefølgen starter øverst på listen.

11. I oversigtspanelet **Aktivtyper** kan du føje aktivtyper til vedligeholdelsesjobtypen.

![Siden Vedligeholdelsesjobtyper](media/06-setup-for-work-orders.png)

## <a name="create-maintenance-job-type-default-lines-and-related-forecasts-maintenance-checklists-tools-description-and-attachments"></a>Oprette standardlinjer for vedligeholdelsesjobtyper og relaterede budgetter, vedligeholdelsestjeklister, værktøjer, beskrivelse og tilknytninger

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Job** \> **Standarder for vedligeholdelsesjobtype**.

    eller

    Vælg **Styring af aktiver** \> **Opsætning** \> **Job** \> **Vedligeholdelsesjobtyper**, vælge en vedligeholdelsesjobtype, og vælg derefter **Standarder for vedligeholdelsesjobtype**.

2. Vælg **Ny**.
3. I felterne **Arbejdssted**, **Aktivtype**, **Producent**, **Model** og **Aktiv** skal du vælge de relevante værdier, afhængigt af hvor specifik vedligeholdelsesjobtypens standard skal være.
4. Vælg en vedligeholdelsesjobtype i feltet **Vedligeholdelsesjobtype**, hvis den ikke automatisk er valgt.
5. I felterne **Vedligeholdelsesjobtypevariant** og **Fag** skal du vælge en variant for vedligeholdelsesjobtypen og et fag for vedligeholdelsesjobbet efter behov.
6. Vælg **Budget**.
7. På siden **Standardbudget for vedligeholdelsesjobtype** kan du oprette budgetter på timer, varer og udgifter. Vælg **Tilføj**under de relevante faner, og foretag valg for at oprette de nødvendige budgetter for typen af vedligeholdelsesjob.
8. Under fanen **Varebudget** kan du vælge de lagerdimensioner, der skal vises på varelinjen. Vælg **Lager** \> **Dimensioner**, vælg de dimensioner, der skal vises, angiv indstillingen **Gem opsætning** til **Ja**, og vælg derefter **OK**.
9. Vælg **Hvor er varen brugt?** under fanen **Varebudget** for at se en oversigt over, hvor i Styring af aktiver varen på den valgte linje bruges i relation til aktiver, typestandard for vedligeholdelsesjob, reservedele og arbejdsordrer. 

    Oversigtspanelet **Vedligeholdelsesprognosetotaler** indeholder en oversigt over budgettotaler. Denne oversigt indeholder det samlede antal timer og budgetlinjer, der er oprettet.

    > [!NOTE]
    > Hvis du vil kopiere budgetopsætningen fra en anden type vedligeholdelsesjob, skal du vælge **Kopiér budget** og derefter vælge den type vedligeholdelsesjob, som opsætningen skal kopieres fra.

11. Vælg **Gem** for at gemme ændringerne.
12. Luk siden **Standardbudget for vedligeholdelsesjobtype** for at gå tilbage til siden **Standarder for vedligeholdelsesjobtype**.
13. Vælg **Vedligeholdelsestjekliste**.
14. På siden **Standardtjekliste for vedligeholdelsesjobtype** kan du føje vedligeholdelsestjeklistelinjer til den valgte standardtype for vedligeholdelsesjob. Vælg **Ny** i oversigtspanelet **Vedligeholdelsestjeklinjer** for at tilføje en ny vedligeholdelsestjeklistelinje.

    Linjenumre indsættes automatisk i feltet **Linjenummer** for at angive rækkefølgen af linjerne på vedligeholdelsestjeklisten. Du kan redigere linjenumre efter behov. Når du har oprettet den første vedligeholdelsestjeklistelinje, skal du markere linjen og derefter trykke på **Pil ned**-tasten for at tilføje en linje nedenunder. Du kan også vælge en vedligeholdelsestjeklistelinje og derefter vælge **Ny**. I dette tilfælde tilføjes en ny linje oven over den valgte vedligeholdelsestjeklistelinje.

15. Vælg linje typen i feltet **Type**, og tilføj derefter oplysninger vedrørende vedligeholdelsestjeklistens type. Du kan finde en beskrivelse af de tilgængelige typer og relaterede felter i afsnittet [Oprette en skabelon for en vedligeholdelsestjekliste](#create-a-maintenance-checklist-template).

    > [!NOTE]
    > Hvis du vil kopiere opsætningen af vedligeholdelsestjeklisten fra en anden type vedligeholdelsesjob, skal du vælge **Kopiér vedligeholdelsestjekliste** og derefter vælge den type vedligeholdelsesjob, som opsætningen skal kopieres fra.
    >
    > Du kan nemt oprette en skabelon ud fra en eksisterende vedligeholdelsestjekliste. Du kan derefter genbruge skabelonen på tværs af flere vedligeholdelsestjeklister. Den nye skabelon er en nøjagtig kopi af den aktive vedligeholdelsestjekliste. Vælg **Opret skabelon**, og angiv derefter et navn til skabelonen. Hvis du vil erstatte den eksisterende vedligeholdelsestjekliste med en enkelt linje, der henviser til den nye skabelon, skal du angive indstillingen **Erstat** til **Ja**. Du kan få vist indholdet af skabelonen på detaljesiden for **Skabeloner til vedligeholdelsestjekliste**.

16. Vælg **Gem** for at gemme ændringerne.
17. Vend tilbage til siden **Standarder for vedligeholdelsesjobtype**.
18. Vælg **Værktøjer**.
19. På siden **Standardværktøjer for vedligeholdelsesjobtype** kan du tilføje de værktøjer (ressourcer), der skal bruges til vedligeholdelsesjobtypen. Vælg **Ny**, og vælg derefter værktøjet i feltet **Ressource**.

    > [!NOTE]
    > Hvis du vil kopiere værkstøjsopsætningen fra en anden type vedligeholdelsesjob, skal du vælge **Kopiér værkstøj** og derefter vælge den type vedligeholdelsesjob, som opsætningen skal kopieres fra.

20. Vælg **Gem** for at gemme ændringerne.
21. Vend tilbage til siden **Standarder for vedligeholdelsesjobtype**.
22. Vælg **Arbejdsbeskrivelse**.
23. Vælg **Rediger** på siden **Arbejdsbeskrivelse**, og tilføj derefter en beskrivelse, der er relateret til den valgte standardtype for vedligeholdelsesjob.
24. Vælg **Gem** for at gemme beskrivelsen.

    Hvis du tilføjer en arbejdsbeskrivelse her, tilsidesætter den eventuelle beskrivelser, der er konfigureret for vedligeholdelsesjobtypen på siden **Vedligeholdelsesjobtyper**. Hvis du ikke tilføjer en arbejdsbeskrivelse her, bruges enhver beskrivelse, der er konfigureret for den brugte vedligeholdelsesjobtype. Beskrivelser overføres automatisk til de arbejdsordrer, der bruger vedligeholdelsesjobtypen eller standarden for vedligeholdelsesjobtype.

25. Vend tilbage til siden **Standarder for vedligeholdelsesjobtype**.
26. Hvis du vil oprette vedhæftede filer på en valgt standardlinje i en vedligeholdelsesjobtype, skal du vælge **Vedhæft dokumenter**. Vedhæftede filer, der er konfigureret på en standardlinje for en vedligeholdelsesjobtype, medtages automatisk på arbejdsordrelinjer, der bruger standardlinjen for vedligeholdelsesjobtypen.
27. Vælg **Ny**, og vælg derefter en dokumenttype.
28. Upload dokumentet eller filen.
29. Angiv felterne på siden **Vedhæftede filer**. I opsætningen af vedhæftninger bruges opsætningsfunktionen for standarddokument.
30. Vælg **Gem** for at gemme vedhæftningen.

    > [!NOTE]
    > Vedhæftede filer på en standardlinje for vedligeholdelsesjobtypen udskrives kun sammen med en arbejdsordrerapport, hvis dokumenttyperne for de vedhæftede filer er valgt under fanen **Dokumenttyper** på siden **Parametre til aktivstyring** (**Styring af aktiver** \> **Opsætning** \> **Parametre til aktivstyring**). Eksempler på vedhæftede filer er retningslinjer, der forklarer, hvordan et bestemt job skal fuldføres, eller en foruddefineret vedligeholdelsestjekliste (hvis du ikke bruger funktionalitet af vedligeholdelsestjekliste til vedligeholdelsesjobtypens standardlinjer).

    På siden **Standarder for vedligeholdelsesjobtype** viser hver linje antallet af budgetterede timer og også antallet af linjer, der er oprettet for varer, udgifter, vedligeholdelsestjeklister og værktøjer. I feltet **Aktiver** vises antallet af aktive aktiver, der er relateret til vedligeholdelsesjobtypens standardlinje.

31. Hvis du vil kopiere en vedligeholdelsesjobtypestandard til en anden vedligeholdelsesjobtypestandard, skal du vælge standardlinjen for vedligeholdelsesjobtypen for at kopiere en anden opsætning, vælge **Kopiér opsætning** og derefter vælge den vedligeholdelsesjobtypestandard, der skal kopieres.
32. Hvis du vil se en liste over aktiver, vedligeholdelsesplaner eller vedligeholdelsesrunder, der aktuelt bruger en standardlinje for en vedligeholdelsesjobtype, skal du vælge linjen og derefter vælge **Bruges af**.

![Siden Standarder for vedligeholdelsesjobtype](media/07-setup-for-work-orders.png)

Når systemet vælger den tilgængelige vedligeholdelsesjobtypestandard, der skal bruges på en arbejdsordrelinje, baseres valget på aktivet og den relaterede aktivtypeopsætning. Styring af aktiver gennemgår alle standardposter for vedligeholdelsesjobtypen, der er relateret til den vedligeholdelsesjobtype, der er relateret til aktivtypen, for at kontrollere, om der findes et muligt match. Den kontrollerer altid den mest specifikke kombination først. Med andre ord kontrolleres det først, for at finde den mest specifikke kombination, om der findes et muligt match til feltet **Fag**. Hvis der ikke findes et match, kontrolleres det, om der er et match for feltet **Vedligeholdelsesjobtypevariant**. Hvis der ikke findes et match, kontrolleres der for et match med feltet **Vedligeholdelsesjobtype** osv. (**Fag**, derefter **Variant af vedligeholdelsesjobtype**, derefter **Vedligeholdelsesjobtype**, derefter **Aktiv**, derefter **Model**, derefter **Producent** og derefter **Aktivtype**). Hvis der ikke findes et match, bruges standardposten, hvor der kun er valgt en vedligeholdelsesjobtype.

Et projektaktivitets-id knyttes automatisk til hver standardlinje for vedligeholdelsesjobtypen, som du opretter. Projektaktiviteten oprettes på det budgetprojekt, der er valgt i feltet **Vedligeholdelsesprognoseprojekt** under fanen **Aktiver** på siden **Parametre til aktivstyring**. Formålet med projektaktiviteten er at administrere prognoser for timer, varer og udgifter i relation til arbejdsordrer. Budgetter for vedligeholdelsesjobtyper overføres automatisk til arbejdsordrelinjen, og de kopieres fra budgetprojektet til det arbejdsordreprojekt, der oprettes for arbejdsordrelinjen. Formålet med projektaktiviteten er at administrere prognoser i relation til arbejdsordrer.

Du kan konfigurere et batchjob til at opdatere standardreferencer for vedligeholdelsesjobtyper med jævne mellemrum, eller du kan køre jobbet manuelt. Hvis du vil oprette et batchjob eller køre en manuel opdatering, skal du vælge **Styring af aktiver** \> **Periodisk** \> **Præventiv vedligeholdelse** \> **Opdater standardreferencer for vedligeholdelsesjobtyper**.

## <a name="overview-of-maintenance-job-types-that-are-related-to-assets"></a>Oversigt over vedligeholdelsesjobtyper, der er relateret til aktiver

Når du har oprettet de nødvendige standardkombinationer af vedligeholdelsesjobtypen, kan du bruge siden **Alle aktiver** til at se en oversigt over den aktuelle standard for vedligeholdelsesjobtype, der er knyttet til et bestemt aktiv. Oversigten viser alle de standardkombinationer af vedligeholdelsesjobtype, der kan bruges på den aktivtype, som er valgt for aktivet. Disse kombinationer omfatter kombinationer, der har variationer af vedligeholdelsesjobtypevarianter af vedligeholdelsesjobfag.

1. Vælg **Styring af aktiver** \> **Almindelig** \> **Aktiver** \> **Alle aktiver** eller **Aktive aktiver**.
2. På listen skal du vælge aktivet for at få vist en oversigt over dets kombinationer af vedligeholdelsesjobtyper.
3. Vælg **Vedligeholdelsesjobtyper** i gruppen **Relaterede oplysninger** under fanen **Generelt** i handlingsruden.

    I venstre rude på siden **Vedligeholdelsesjobtyper for aktiv** vises en liste over alle de kombinationer af vedligeholdelsesjobtyper, der er relateret til det valgte aktiv.

4. Vælg en kombination af vedligeholdelsesjobtyper for at se den relaterede opsætning af vedligeholdelsestjeklister, budgetter og værktøjer. Afsnittet **Detaljer** i oversigtspanelet **Standarder for vedligeholdelsesjobtype** viser antallet af relaterede vedligeholdelsestjeklister, budgetterede timer, varer osv., der er relateret til den valgte kombination af vedligeholdelsesjobtype.
5. Vælg **Vedligeholdelsesjobtyper** for at få vist oplysninger om den valgte vedligeholdelsesjobtype.

![Siden Vedligeholdelsesjobtyper for aktiv](media/08-setup-for-work-orders.png)

## <a name="automatic-update-of-maintenance-job-type-forecasts"></a>Automatisk opdatering af budgetter for vedligeholdelsesjobtyper

I Styring af aktiver kan du automatisk opdatere eventuelle ændringer i budgetter til vedligeholdelsesjobtypen for timeomkostninger, vareomkostninger og udgifter, der er opdateret i andre moduler. På denne måde er du med til at sikre, at dine budgetter for vedligeholdelsesjobtyper altid bruger de seneste kostpriser.

1. Vælg **Styring af aktiver** \> **Periodisk** \> **Budget** \> **Opdater budget for vedligeholdelsesjobtype**.
2. I dialogboksen **Opdater budget for vedligeholdelsesjobtype** kan du i oversigtspanelet **Poster, der skal indgå** tilføje valg for bestemte typer af vedligeholdelsesjob efter behov. Vælg **Filter**, og vælg derefter **Vælg** for at foretage valgene.
3. I oversigtspanelet **Kør i baggrunden** kan du konfigurere automatisk opdatering som et batchjob efter behov.
4. Vælg **OK** for at starte budgetopdateringen.
