---
title: "Oversigt over Hjælp"
description: "Denne artikel indeholder en oversigt over komponenterne i Microsoft Dynamics 365 for Operations-hjælpesystemet. Den forklarer også, hvordan du kan angive tilpasset brugerdokumentation og kurser til din organisation."
author: margoc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16381
ms.assetid: 018c148c-9cbd-41e0-8186-d75dbf66288f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 240060606c8a2955c3f0a0d47fb25b0cde64c187
ms.lasthandoff: 03/31/2017


---

# <a name="help-overview"></a>Oversigt over Hjælp

Denne artikel indeholder en oversigt over komponenterne i Microsoft Dynamics 365 for Operations-hjælpesystemet. Den forklarer også, hvordan du kan angive tilpasset brugerdokumentation og kurser til din organisation. 

Dynamics 365 for Operations indeholder et hjælpesystem, der er baseret på to hovedkomponenter:

-   Et dokumentationswebsted
-   Opgaveguider

Du kan få adgang til både artikler og opgaveguider fra ruden Hjælp i Dynamics 365 for Operations som vist på følgende skærmbillede. [![Ruden Hjælp](./media/help-pane-ops-task-guides-1024x741.png)](./media/help-pane-ops-task-guides.png) I denne artikel beskrives hjælpesystemet, og hvordan du kan oprette brugerdefineret dokumentation og undervisningsressourcer til din virksomhed.

## <a name="help-on-docsmicrosoftcom"></a>Hjælp til docs.microsoft.com
Webstedet docs.microsoft.com ([docs.microsoft.com/dynamics365/operations](https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations) er den primære kilde til produktdokumentation til Dynamics 365 for Operations. Webstedet indeholder følgende funktioner:

-   **Adgang til det mest opdaterede indhold** – Webstedet giver os en hurtigere og mere fleksibel måde at oprette, levere og opdatere produktdokumentationen på. Derfor hjælper den med at sikre, at du har adgang til de seneste tekniske oplysninger.
-    **Indhold, der er skrevet af eksperter** – Webstedet giver et mere omfattende sæt af produktdokumentation, der kan forbedres af community-medlemmer både inden for og uden for Microsoft.
-   **Adgang til forskellige typer indhold** – På webstedet kan du hurtigt få adgang til forskellige typer indhold om Dynamics 365 for Operations som Microsoft Office Mix-præsentationer, opgaveguider, videoer og wiki-artikler.
-    **Indhold, der understøtter dine forretningsprocesser** – Webstedet omfatter indhold, der er fokuseret på forretningsprocesser, og som drager fordel af Business Process Modeler (BPM) i Microsoft Dynamics Lifecycle Services (LCS).

Vi har flyttet alt indhold fra vores tidligere Hjælp-wiki til dokumenter. Vi er meget begejstrede for vores nye websted og håber, at du også bliver glad for det.

### <a name="when-can-we-use-it"></a>Hvornår kan vi bruge den?

Du kan læse indhold på webstedet lige nu – det er helt offentligt og søgbart og kræver ikke logon. Du kan bruge dine foretrukne søgemaskiner til at finde indhold. Du kan kommentere artikler på webstedet, hvis du vil, ved at logge på med en GitHub-konto.


## <a name="task-guides"></a>Opgaveguider
En opgaveguide er en kontrolleret, automatiseret, interaktiv oplevelse, der fører dig gennem trinene i en opgave eller forretningsproces. Du kan åbne (afspille) en opgaveguide fra ruden Hjælp. Når du først klikker på en opgaveguide, viser ruden Hjælp de trinvise instruktioner til opgaven. Der er nu lokaliserede opgaveguider. [![Opgaveguides læsevisning](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png) For at starte den automatiserede, interaktive oplevelse skal du klikke på **Start opgaveguiden** i bunden af ruden Hjælp. En sort markør åbnes og angiver den handling, du skal udføre. Følg vejledningen, der vises i brugergrænsefladen, og indtast data som anvist. [![Opgaveguidens trinvise instruktion](./media/task-guide-step-1-ops.png)](./media/task-guide-step-1-ops.png) **Vigtigt!** De data, du indtaster, når du afspiller en opgaveguide, er ægte. Hvis du er i et produktionsmiljø, indsættes dataene i det firma, du aktuelt bruger.

### <a name="it-all-begins-with-task-recorder"></a>Det hele begynder med Arbejdsrutineoptager

Opgaveguider oprettes ved hjælp af Arbejdsrutineoptager. Når du bruger Arbejdsrutineoptager, registreres alle dine handlinger i Dynamics 365 for Operations-brugergrænsefladen (f.eks. at klikke på menuer, ændre indstillinger og indtaste data). De trin, du optager, bliver samlet kaldes en opgaveregistrering. Som vi har forklaret i forrige afsnit, kan opgaveregistreringer vises i ruden Hjælp og afspilles som opgaveguider. Der er og andre måder, du kan bruge opgaveregistreringer på:

-   **Gemme opgaveregistreringer til BPM** – du kan gemme en registrering til en linje i et hierarki i et BPM-bibliotek i LCS. Når du gemmer en opgaveregistrering til BPM, oprettes der et rutediagram, der vises sammen med trin af registreringen. **Bemærk!** Hvis du vil have vist en opgaveregistrering i Dynamics 365 for Operations på ruden Hjælp, skal du gemme registreringen i et BPM-bibliotek.
-   **Gemme opgaveregistreringer som Word-dokumenter** – ved at gemme en opgaveregistrering som et Microsoft Word-dokument kan du nemt oprette kursusguider, der kan udskrives for organisationen.

Du kan finde flere oplysninger om Arbejdsrutineoptager i [Arbejdsrutineoptager i Dynamics 365 for Operations](../user-interface/task-recorder.md).

### <a name="creating-customized-task-recordings"></a>Oprette brugerdefinerede opgaveregistreringer

Du kan oprette dine egne opgaveregistreringer, eller du kan hente og tilpasse opgaveregistreringer, som Microsoft leverer. Du kan derfor oprette en tilpasset Hjælp for din organisation, der afspejler din implementering af Dynamics 365 for Operations. Hvis du vil have vist en opgaveregistrering i ruden Hjælp i Dynamics 365 for Operations og afspille den som en opgaveguide, skal du gemme registreringen i et BPM-bibliotek i LCS. Hvis du som partner fremmer et bibliotek til at være virksomhedens bibliotek og medtager det i en løsning, bliver det tilgængeligt for dine kunder. Du kan finde flere oplysninger under [Brug af opgaveregistreringer til at oprette dokumentation eller uddannelse](../user-interface/task-recorder.md).

## <a name="in-product-help"></a>Hjælp i produkterne
For at få adgang til indhold i Hjælp i Dynamics 365 for Operations skal du enten klikke på ikonet **Hjælp** (**?**) og derefter vælge Hjælp eller trykke på Ctrl + Skift +?. I begge tilfælde åbnes ruden Hjælp. Fra ruden Hjælp kan du få adgang til artikler eller opgaveguider. [![](./media/help-pane-wiki-1024x684.png)](./media/help-pane-wiki.png)

### <a name="accessing-articles-from-the-help-pane"></a>Adgang til artikler fra ruden Hjælp

Fra ruden Hjælp kan du få adgang til artikler, der gælder for Dynamics 365 for Operations-klienten. Når du først åbner Hjælp-ruden og klikker på fanen **Wiki**, kan du se de artikler, der gælder for den aktuelle side i Dynamics 365 for Operations. Hvis der ikke findes artikler, kan du angive nøgleord for at indsnævre søgningen. Når du klikker på en artikel i ruden Hjælp, åbnes en ny fane i browseren og viser artiklen. 

### <a name="accessing-task-guides-from-the-help-pane"></a>Adgang til opgaveguider fra ruden Hjælp

Før du kan få adgang til opgaveguider fra ruden **Hjælp**, skal en systemadministrator gå til siden Systemparametre i Dynamics 365 for Operations og konfigurere nogle indstillinger. **Bemærkninger:**

-   Hvis du vil konfigurere hjælp, skal du være logget på med en konto i den samme lejer som den lejer, hvor Dynamics 365 for Operations er installeret.
-   Det er ikke muligt at oprette forbindelse til et LCS-bibliotek fra en forekomst af Dynamics 365 for Operations, der kører på en lokal virtuel harddisk (VHD).

[![Systemparametre med hjælpeindstillinger](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) På siden **Systemparametre** skal du følge disse trin:

1.  **Vigtigt: **Første gang du åbner fanen Hjælp, skal du oprette forbindelse til Lifecycle Services. Husk at klikke på linket i midten af formularen, vente på forbindelsen, lukke dialogboksen og derefter klikke på OK for at få adgang til parameterformen.[![Opret forbindelse til LCS](./media/connect-to-lcs-crop-1024x365.png)](./media/connect-to-lcs-crop.png)
2.  Vælg det Lifecycle Services-projekt, der skal oprettes forbindelse til.
3.  Vælg BPM-biblioteker (inden for det valgte projekt), hvor der skal hentes opgaveregistreringer fra.
4.  Angiv visningsrækkefølgen for BPM-bibliotekerne. Dette bestemmer den rækkefølge, som opgaveregistreringer fra bibliotekerne vises i på ruden Hjælp.

Når en systemadministrator har udført disse trin, kan du åbne ruden Hjælp og klikke på fanen **Opgaveguider**. Nu kan du se opgaveguiderne, der gælder for den aktuelle side i Dynamics 365 for Operations. Hvis der ikke findes opgaveguider, kan du angive nøgleord for at indsnævre søgningen. Når du klikker på en opgaveguide i ruden Hjælp, viser ruden Hjælp de trinvise instruktioner, og du kan afspille opgaveguiden. [![Opgaveguidens læsevisning](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png)

### <a name="where-are-the-translated-task-guides"></a>Hvor er de oversatte opgaveguider?

Oversatte opgaveguider udgives i biblioteker med "Alle sprog" i titlen. Når du vil se den lokaliserede hjælp til opgaveguider i Dynamics 365 for Operations, skal du sørge for, at der er forbindelse til et relevant bibliotek. Det sprog, en opgaveguide vises på, styres for hver bruger af sprogindstillingerne under **Indstillinger** &gt; **Indstillinger**. 
-   Hvis en opgaveguide er blevet oversat, vises teksten i opgaveguiden på det valgte sprog, når du åbner denne opgaveguide.
-   Hvis en opgaveguide ikke er blevet oversat, er det kun noget af teksten (tekst i kontrolelementerne), der vises på det valgte sprog, når du åbner guiden.

## <a name="additional-resources"></a>Yderligere ressourcer
Følgende tabel viser en liste over websteder, der leverer indhold til Dynamics 365 for Operations. Vores indholdswebsteder er organiseret til at understøtte kundens livscyklus. Hver fase er understøttet af en række forskellige websteder. Websteder, der har en stjerne (\*) ud for navnet, kræver, at du logger på med en konto, der er tilknyttet en serviceplan.

| Sted                                                                     | Betegnelse                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Docs.microsoft.com](https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations) | Er vært for eller indeholder hyperlinks til al produktdokumentation til Dynamics 365 for Operations.                                                                                                                                                               |
| [Lifecycle Services](http://lcs.dynamics.com/en/)\*                      | Indeholder et skybaseret arbejdsområde til samarbejde, som kunder og partnere kan bruge til at administrere Dynamics 365 for Operations-projekter, lige fra førsalg til implementering og drift. Dette websted er nyttigt i alle faserne i en installation. |
| [CustomerSource](http://www.customersource.com/)\*                       | Vært for omfattende undervisningsmateriale og er det primære supportwebsted til Dynamics 365 for Operations. Logon kan forlanges for at få adgang til bestemte ressourcer på webstedet.                                                                      |
| [Supportblog](http://aka.ms/AXSupportBlog)                              | Indeholder tip og trick, der er oprettet af Dynamics 365 for Operations-supportteamet.                                                                                                                                                  |
| [MSDN](http://aka.ms/AXMSDN)                                             | Er vært for indhold fra tidligere versioner, der er skrevet til udviklere.                                                                                                                                                                       |
| [TechNet](http://aka.ms/TechNet)                                         | Er vært for indhold fra tidligere versioner, der er udviklet til it-medarbejdere og brugere af programmet.                                                                                                                                           |
| [Dynamics Community](http://community.dynamics.com/en/)                  | Er vært for blogs, fora og videoer.                                                                                                                                                                                                           |
| [Microsoft.com/Dynamics/](http://www.microsoft.com/dynamics/)                 | Indeholder oplysninger om evaluering og salg.                                                                                                                                                                                                 |



<a name="see-also"></a>Se også
--------

[Dynamics 365 for Operations-hjælpesystemet (dataark kan hentes)](https://mbs.microsoft.com/files/public/CS/AX2012R3/DynamicsAXHelpSystemFactSheet.pdf)

[Arbejdsrutineoptager i Microsoft Dynamics 365 for Operations](../user-interface/task-recorder.md)

[Oprette dokumentation eller undervisning ved hjælp af opgaveregistreringer](../user-interface/task-recorder.md)

[Nye eller opdaterede opgaveguider (november 2016)](new-task-guides-november-2016.md)
[Nye eller opdaterede opgaveguider (august 2016)](new-updated-task-guides-available-august-2016.md)
[Nye eller opdaterede opgaveguider (maj 2016)](new-updated-task-guides-available-may-2016.md)
[Nye opgaveguider (februar 2016)](new-task-guides-available-february-2016.md)






