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

-   Et websted til dokumentation
-   Opgaveguider

Du kan åbne både artikler og vejledninger til opgaven fra Hjælp-ruden i Dynamics 365 for operationer, som vist i nedenstående skærmbillede. [![Ruden Hjælp](./media/help-pane-ops-task-guides-1024x741.png)](./media/help-pane-ops-task-guides.png) denne artikel beskrives i Hjælp-systemet og forklarer, hvordan du kan oprette brugerdefinerede dokumentation og undervisningsressourcer til din virksomhed.

## <a name="help-on-docsmicrosoftcom"></a>Hjælp til docs.microsoft.com
Webstedet docs.microsoft.com ([docs.microsoft.com/dynamics365/operations](https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations) er den primære kilde til dokumentationen til Dynamics 365 for operationer. Webstedet tilbyder følgende funktioner:

-   **Adgang til det mest opdaterede indhold** – webstedet giver os en hurtigere og mere fleksibel måde at oprette, levere og opdatere produktdokumentationen. Derfor hjælper den med at sikre, at du har adgang til de seneste tekniske oplysninger.
-    **Indhold, der er skrevet af eksperter** – webstedet indeholder et mere omfattende sæt af produktdokumentation, der kan forbedres ved community-medlemmer både inden for og uden for Microsoft.
-   ** Adgang til forskellige typer indhold ** – webstedet kan du hurtigt adgang til forskellige typer indhold om Dynamics 365 for handlinger, som Microsoft Office Mix præsentationer, opgave vejledninger, videoer og wiki-artikler.
-    **Indhold, der understøtter dine forretningsprocesser** – webstedet indeholder business proces – fokuseret indhold, der drager fordel af Business Process model (BPM) i Microsoft Dynamics livscyklus Services (LCS).

Vi har flyttet alt indhold fra vores tidligere wiki hjælp til dokumenter. Vi er meget begejstret for vores nye websted og håb om, at der for.

### <a name="when-can-we-use-it"></a>Hvornår kan vi bruge den?

Du kan læse indholdet af dokumenter lige nu – det er helt offentlige og søgbare uden at logge på. Du kan bruge dine foretrukne søgemaskiner til at finde indhold. Du kan kommentere artikler på webstedet, hvis du vælger, ved at logge på med en konto på GitHub.


## <a name="task-guides"></a>Opgaveguider
Vejledning til en opgave er en kontrolleret, automatiseret, interaktiv oplevelse, der fører dig gennem trinene i en opgave eller forretningsproces. Du kan åbne vejledning (Afspil) for en opgave fra Hjælp-ruden. Når du først klikke på en opgave-vejledning, vises Hjælp-ruden de trinvise instruktioner til opgaven. Der er nu lokaliseret opgave vejledninger. [![Opgave guide læsevisning](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png) for at starte den automatiseret, interaktive oplevelse, skal du klikke på **opgave Introduktion** nederst i ruden hjælp. En sort markør åbnes og angiver den handling, du skal udføre. Følg vejledningen, der vises i brugergrænsefladen, og indtast data som anvist. [![Opgaven vejledning trin instruktion](./media/task-guide-step-1-ops.png)](./media/task-guide-step-1-ops.png)**vigtigt:** de data, du indtaster, når du afspiller en opgave vejledning er ægte. Hvis du er i et produktionsmiljø, indsættes dataene i det firma, du aktuelt bruger.

### <a name="it-all-begins-with-task-recorder"></a>Det hele begynder med Arbejdsrutineoptager

Opgaveguider oprettes ved hjælp af Arbejdsrutineoptager. Når du bruger Arbejdsrutineoptager, registreres alle dine handlinger i Dynamics 365 for Operations-brugergrænsefladen (f.eks. at klikke på menuer, ændre indstillinger og indtaste data). De trin, du optager, bliver samlet kaldes en opgaveregistrering. Som vi har forklaret i forrige afsnit, kan opgaveregistreringer vises i ruden Hjælp og afspilles som opgaveguider. Der er og andre måder, du kan bruge opgaveregistreringer på:

-   **Gemme opgaveregistreringer til BPM** – du kan gemme en registrering til en linje i et hierarki i et BPM-bibliotek i LCS. Når du gemmer en opgaveregistrering til BPM, oprettes der et rutediagram, der vises sammen med trin af registreringen. **Bemærk!** Hvis du vil have vist en opgaveregistrering i Dynamics 365 for Operations på ruden Hjælp, skal du gemme registreringen i et BPM-bibliotek.
-   **Gemme opgaveregistreringer som Word-dokumenter** – ved at gemme en opgaveregistrering som et Microsoft Word-dokument kan du nemt oprette kursusguider, der kan udskrives for organisationen.

Du kan finde flere oplysninger om Arbejdsrutineoptager, i [Arbejdsrutineoptager i Dynamics 365 i forbindelse med](../user-interface/task-recorder.md).

### <a name="creating-customized-task-recordings"></a>Oprette brugerdefinerede opgaveregistreringer

Du kan oprette dine egne opgaveregistreringer, eller du kan hente og tilpasse opgaveregistreringer, som Microsoft leverer. Du kan derfor oprette en tilpasset Hjælp for din organisation, der afspejler din implementering af Dynamics 365 for Operations. For at få vist en opgave, der optager i Dynamics-365 for operationer Hjælp-ruden og afspille det som en opgave, bliver du nødt til at gemme optagelsen på et BPM bibliotek i LCS. Hvis du er en partner, og fremme et bibliotek til et større bibliotek og medtage den i en løsning, bliver den tilgængelig for dine kunder. Yderligere oplysninger finder du i [ved hjælp af optagelser opgave til at oprette dokumentation eller uddannelse](../user-interface/task-recorder.md).

## <a name="in-product-help"></a>Hjælp i produkterne
For at få adgang til indhold i Hjælp i Dynamics 365 for operationer ved enten at klikke på **hjælpe** (**?**) ikon og vælge Hjælp eller trykke på Ctrl + Skift +?. I begge tilfælde åbnes ruden Hjælp. Du har adgang til artikler eller opgave hjælpelinjer fra Hjælp-ruden. [![](./media/help-pane-wiki-1024x684.png)](./media/help-pane-wiki.png)

### <a name="accessing-articles-from-the-help-pane"></a>Adgang til artikler fra Hjælp-ruden

Fra Hjælp-ruden kan du få adgang til artikler, der gælder for Dynamics-365 for operationer klient. Når du først åbner Hjælp-ruden og klikker på **Wiki** under fanen kan du se de artikler, der gælder for den side, du er i øjeblikket på i Dynamics 365 for operationer. Hvis der findes ingen artikler, kan du angive nøgleord til at indsnævre søgningen. Når du klikker på en artikel i Hjælp-ruden, en ny fane åbnes i browseren og viser artiklen. 

### <a name="accessing-task-guides-from-the-help-pane"></a>Adgang til opgaven hjælpelinjer fra Hjælp-ruden

Før du kan få adgang til opgaven hjælpelinjer fra ruden hjælp, en systemadministrator har at gå til den **systemparametre** side i Dynamics 365 for operationer og konfigurere nogle indstillinger. **Bemærkninger:**

-   Hvis du vil konfigurere hjælp, skal du være logget på med en konto i den samme lejer som den lejer, hvor Dynamics 365 for Operations er installeret.
-   Det er ikke muligt at oprette forbindelse til et LCS-bibliotek fra en forekomst af Dynamics 365 for Operations, der kører på en lokal virtuel harddisk (VHD).

[![Systemet parameterformen med indstillinger for Hjælp](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) på den **systemparametre** side, skal du følge disse trin:

1.  **Vigtigt: **Første gang du åbner fanen Hjælp, skal du oprette forbindelse til Lifecycle Services. Husk at klikke på hyperlinket i formularen, venter på forbindelsen, for at lukke dialogboksen og klik derefter på OK for at få adgang til parameterformen. [![Forbindelse til LCS](./media/connect-to-lcs-crop-1024x365.png)](./media/connect-to-lcs-crop.png)
2.  Vælg det Lifecycle Services-projekt, der skal oprettes forbindelse til.
3.  Vælg BPM-biblioteker (inden for det valgte projekt), hvor der skal hentes opgaveregistreringer fra.
4.  Angiv visningsrækkefølgen for BPM-bibliotekerne. Dette bestemmer den rækkefølge, som opgaveregistreringer fra bibliotekerne vises i på ruden Hjælp.

Når en systemadministrator har udført disse trin, kan du åbne ruden Hjælp og klikke på fanen **Opgaveguider**. Nu kan du se opgaven hjælpelinjer, der gælder for den side, du er i øjeblikket på i Dynamics 365 for operationer. Hvis der findes ingen opgave hjælpelinjer, kan du angive nøgleord til at indsnævre søgningen. Når du klikker på en opgave-vejledning i Hjælp-ruden Hjælp-ruden viser de trinvise instruktioner, og du kan afspille opgave-vejledning. [![Opgave guide læsevisning](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png)

### <a name="where-are-the-translated-task-guides"></a>Hvor er de oversatte opgave hjælpelinjer?

Oversat opgave hjælpelinjer er udgivet i biblioteker med "Alle sprog" i titlen. I Dynamics 365 for operationer, for at se lokaliserede opgave vejledning hjælpe, Sørg for, at du har forbindelse til et apppropriate bibliotek. Det sprog, der vises en vejledning til opgave i styres for hver bruger af sprogindstillinger under **indstillinger for**&gt;**indstillinger for**. 
-   Hvis en opgave vejledning er blevet oversat, når du åbner denne opgave guide teksten guide opgave vises i det valgte sprog.
-   Hvis en opgave vejledning ikke endnu er oversat, når du åbner den, vises kun noget af teksten (tekst kontrolelementer) i det valgte sprog.

## <a name="additional-resources"></a>Yderligere ressourcer
Følgende tabel viser en liste over websteder, der leverer indhold til Dynamics 365 for Operations. Vores indholdswebsteder er organiseret til at understøtte kundens livscyklus. Hver fase er understøttet af en række forskellige websteder. Websteder, der er markeret med en stjerne (\*) ved siden af navnet kræver, at du logger på med en konto, der er tilknyttet en serviceplan.

| Sted                                                                     | Betegnelse                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Docs.microsoft.com](https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations) | Er vært for eller indeholder hyperlinks til al produktdokumentation til Dynamics 365 for Operations.                                                                                                                                                               |
| [Lifecycle Services](http://lcs.dynamics.com/en/)\*                      | Indeholder et skybaseret arbejdsområde til samarbejde, som kunder og partnere kan bruge til at administrere Dynamics 365 for Operations-projekter, lige fra førsalg til implementering og drift. Dette websted er nyttigt i alle faserne i en installation. |
| [CustomerSource](http://www.customersource.com/)\*                       | Vært for omfattende undervisningsmateriale og er det primære supportwebsted til Dynamics 365 for Operations. Logon kan forlanges for at få adgang til bestemte ressourcer på webstedet.                                                                      |
| [Support blog](http://aka.ms/AXSupportBlog)                              | Indeholder tip og trick, der er oprettet af Dynamics 365 for Operations-supportteamet.                                                                                                                                                  |
| [MSDN](http://aka.ms/AXMSDN)                                             | Er vært for indhold fra tidligere versioner, der er skrevet til udviklere.                                                                                                                                                                       |
| [TechNet](http://aka.ms/TechNet)                                         | Er vært for indhold fra tidligere versioner, der er udviklet til it-medarbejdere og brugere af programmet.                                                                                                                                           |
| [Dynamics Community](http://community.dynamics.com/en/)                  | Er vært for blogs, fora og videoer.                                                                                                                                                                                                           |
| [Microsoft.com/Dynamics/](http://www.microsoft.com/dynamics/)                 | Indeholder oplysninger om evaluering og salg.                                                                                                                                                                                                 |



<a name="see-also"></a>Se også
--------

[Dynamics 365 for operationer Hjælp system (kan hentes fakta)](https://mbs.microsoft.com/files/public/CS/AX2012R3/DynamicsAXHelpSystemFactSheet.pdf)

[Arbejdsrutineoptager i Microsoft Dynamics 365 til operationer](../user-interface/task-recorder.md)

[Oprette dokumentation eller undervisning ved hjælp af opgaveregistreringer](../user-interface/task-recorder.md)

[Nye eller opdaterede opgave leder (November 2016)](new-task-guides-november-2016.md)<ph id="t1">
</ph>[nye eller opdaterede opgave leder (August 2016)](new-updated-task-guides-available-august-2016.md)<ph id="t2">
</ph>[nye eller opdaterede opgave leder (maj 2016)](new-updated-task-guides-available-may-2016.md)<ph id="t3">
</ph>[ny opgave leder (februar 2016)](new-task-guides-available-february-2016.md)






