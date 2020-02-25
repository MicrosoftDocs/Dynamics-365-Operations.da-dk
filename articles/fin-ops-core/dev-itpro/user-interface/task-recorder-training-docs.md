---
title: Oprette dokumentation eller kursusmateriale ved hjælp af Arbejdsrutineoptager
description: Dette emne forklarer, hvad Arbejdsrutineoptager og opgaveguider er, hvordan du opretter opgaveregistreringer, og hvordan du tilpasser Microsoft-opgaveguider og inkluderer dem i din Hjælp.
author: josaw1
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 268b95aad57c2e4863a3f58cd54828dbb0e09465
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006189"
---
# <a name="create-documentation-or-training-with-task-recorder"></a>Oprette dokumentation eller kursusmateriale ved hjælp af Arbejdsrutineoptager

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvad Arbejdsrutineoptager og opgaveguider er, hvordan du opretter opgaveregistreringer, og hvordan du tilpasser Microsoft-opgaveguider og inkluderer dem i din Hjælp.

> [!IMPORTANT]
> Du kan registrere dine egne opgaveguider til Dynamics 365 Human Resources, men du kan ikke gemme dem til et Forretningsmodeldesigner-bibliotek (BPM) eller åbne dem fra Hjælp-ruden på nuværende tidspunkt. Du kan gemme dem lokalt eller på en netværksplacering og derefter åbne og afspille dem igen ved hjælp af Arbejdsrutineoptager. 

<a name="learn-about-task-recorder"></a>Få mere at vide om Arbejdsrutineoptager
-------------------------

Arbejdsrutineoptager er et værktøj, du kan bruge til at registrere de handlinger, du udfører i produktets brugergrænseflade. Når du bruger Arbejdsrutineoptager – registreres alle de hændelser, du udfører i Brugergrænsefladen, på serveren, herunder tilføjelse af værdier, ændring af indstillinger og fjernelse af data. De trin, du optager, bliver samlet kaldes en *opgaveregistrering*. Opgaveregistreringer kan bruges på mange måder:

-   **Opgaveregistreringer kan afspilles som opgaveguide.** Opgaveguider er en integreret del af Hjælp-oplevelsen.En opgaveguide er en kontrolleret, automatiseret og interaktiv oplevelse, der fører dig gennem trinene i en forretningsproces. Brugeren bliver instrueret i at fuldføre hvert trin ved hjælp af en pop op-meddelelse (eller "boble"), som vil være animeret på tværs af brugergrænsefladen og pege på det element i brugergrænsefladen, som brugeren skal arbejde med. "Boblen" indeholder også oplysninger om, hvordan du arbejder med elementet, f.eks. "Klik her" eller "Angiv en værdi i dette felt".En opgaveguide kører i forhold til brugerens aktuelle datasæt, og de data, der er angivet, gemmes i brugerens miljø.
-   **Opgaveregistreringer kan vises som en trinvis fremgangsmåde i Hjælp-ruden.** Du kan bruge Hjælp-ruden til at søge efter og få vist opgaveregistreringer. Du kan få adgang til Hjælp-ruden ved at klikke på ikonet **?**. i den øverste navigationslinje, eller du kan bruge genvejstastekombinationen  **Ctrl + Skift +?**. Du kan læse trinene i en opgaveregistrering i Hjælp-ruden, eller du kan vælge at afspille optagelsen som en opgaveguide, så du bliver guidet gennem brugergrænsefladen.
-   **Opgaveregistreringer kan gemmes i BPM.** Du kan gemme din opgaveregistrering på en linje i et hierarki i et BPM-bibliotek i LCS (Lifecycle Services). En liste over trin og flowdiagram for en forretningsproces, der genereres fra optagelsen. Opgaveregistreringer, der er gemt i et BPM-bibliotek, kan vises i Hjælp.
-   **Opgaveregistreringer kan gemmes som Word-dokumenter.** På den måde kan du nemt oprette kursusguider, der kan udskrives.

Du kan oprette dine egne opgaveregistreringer, afspille opgaveregistreringer fra Microsoft eller ændre opgaveregistreringer fra Microsoft, så de afspejler din konfiguration.Du kan finde flere oplysninger om Arbejdsrutineoptager i [Arbejdsrutineoptager](task-recorder.md).

## <a name="plan-your-task-recording"></a>Planlægge din opgaveregistrering
Husk følgende oplysninger på, uanset om du skal oprette en ny opgave eller basere din registrering på en Microsoft-opgaveregistrering.

-   Planlæg din registrering på samme måde, som du ville registrere en video. Træf alle dine beslutninger på forhånd.
-   Gennemgå forretningsprocessen en eller to gange uden at registrere den for at forstå trinnene.
-   Når du gennemgår processen, før du laver din registrering, skal du lægge mærke til, hvor du bruger genvejstaster eller tasten **Enter**, så du kan undgå at bruge dem under den faktiske registrering.
-   Identificer følgende:
    -   Vil du gruppere trinnene til underordnede opgaver? Underopgaver afgrænser visuelt sektioner i en proces. Hvis du for eksempel opretter en optagelse til "Oprette og frigive et produkt", vil du måske gruppere de trin, der er nødvendige for at oprette et produkt, og derefter gruppere de trin, der er nødvendige for at frigive produktet. Underopgaver gør det også nemmere at læse længere processer.
    -   Vil du tilføje anmærkninger og i så fald hvor? Se "Forstå de forskellige typer af anmærkninger" nedenfor for at få yderligere oplysninger.
    -   Hvilke værdier vil du tilføje i de forskellige felter, efterhånden som du fuldfører trinnene i forretningsprocessen? Det er en god ide at vide, hvad du vil vælge eller angive, når du fortsætter, så du ikke må gå tilbage eller rette fejl, mens du registrerer.

**Skriv din beskrivelse og anmærkninger i forvejen**

-   I begyndelsen af hver opgaveregistrering er der et beskrivelsesfelt, hvor du kan angive en introduktion til registreringen. Det er en god ide at skrive og gemme beskrivelsen på forhånd i et separat dokument, så du kan kopiere og indsætte den i opgaveregistreringen, mens du optager. På den måde kan du bruge tid på at finpudse teksten, når du ikke er i gang med at registrere. Klipning og indsætning af tekst betyder, at registreringsprocessen går hurtigere og problemfrit.
-   For hvert trin i en opgaveregistrering kan du oprette anmærkninger. Anmærkninger vises under afspilning af en opgaveguide i "boblen" som noter over eller under teksten i trinnet. Når anmærkninger vises som tekst i ruden Hjælp, vises de som tekst, der er integreret i trinnet. Som med beskrivelsen er det en god ide at skrive og gemme dine anmærkninger i et separat dokument. Når du optager opgaveregistreringen, kan du klippe og indsætte anmærkningerne fra dette dokument.

**Forstå de forskellige typer af anmærkninger** Alle anmærkninger er valgfrie. Tilføj dem kun, når de giver brugeren nyttige oplysninger.

-   **Bemærk!** Der vises en anmærkning til titlen før den trintekst, som Arbejdsrutineoptager genererer automatisk.Anmærkningen til titlen vises i opgaveguiden over den automatisk genererede tekst. Brug denne type anmærkning til at forklare, hvorfor brugeren udfører trinnet eller til at give ekstra kontekst.

Dette er redigeringsruden, som du ser, når du tilføjer en anmærkning, mens du opretter din registrering. Angiv en titelanmærkning i feltet **Titel**. 

[![Redigeringsrude med titelanmærkning](./media/screen1.png)](./media/screen1.png) 

Sådan ser titelanmærkningen ud i "boble"-opgaveguiden. 

[![Visning af titelanmærkning i opgaveguide](./media/screen2.png)](./media/screen2.png)

-   **Bemærk!** Der vises en anmærkning til noter efter den trintekst, som opgaveregistreringen genererer automatisk. I opgavevejledningen er den kun synlig, hvis brugeren klikker på linket **Vis flere** i opgaveguidens boble. Brug denne anmærkning til at beskrive noget, som en bruger skal kende for at fuldføre trinnet.

Dette er redigeringsruden, som du ser, når du tilføjer en anmærkning, mens du opretter din registrering. Angiv en notatanmærkning i feltet **Notater**. 

[![Redigeringsrude med anmærkning i noteboks](./media/screen3.png)](./media/screen3.png) 

Sådan ser noteanmærkningen ud i "boblen" i opgaveguiden.

[![Visning af noteanmærkning i opgaveguide](./media/screen4.png)](./media/screen4.png)

-   **Infotrin**: Disse anmærkninger oprettes ved at højreklikke på et kontrolelement eller et vilkårligt sted i en formular &lt; **Arbejdsrutineoptager** &lt; **Tilføj infotrin**. Infotrin vises som et nummereret trin på sted, hvor du indsætter det, selvom intet blev registreret i brugergrænsefladen. Du kan tilføje et infotrin på formularniveau eller et infotrin, der er knyttet til et kontrolelement. Når et infotrin er knyttet til en formular, vises opgaveguidens "boble" et sted i formularen uden markør, når opgaveguiden afspilles. Når et infotrin er knyttet til et kontrolelement, peger opgaveguidens "boble" på kontrolelementet, når opgaveguiden afspilles.I Hjælp-ruden vises en infotrinanmærkning som et nummererede trin med den tekst, du har angivet. Brug infotrin til at forberede brugeren til de næste trin, til at beskrive de skridt, der skal udføres uden for programmet, eller at henvise til andre optagelser (selvom du ikke kan oprette links i anmærkningerne).

**Fastlægge, hvor lang registreringen skal være**

-   Brugeren vil normalt enten læse eller afspille registreringen fra start til slut, så undlad at kombinere trin eller opgaver, som det er bedre at have separat.
-   Prøv ikke at optage et scenario, der er så langt, at det strækker sig over flere underordnede processer. For eksempel er "Opgaver for butikkens kundeservicedesk" for omfattende. Opdel det i kortere opgaver som "Acceptér returneringer" og "Føj til gavekort".
-   Hvis en opgave kan udføres som en del af flere forskellige forretningsprocesser, kan du oprette en separat registrering til den, og du kan henvise til den i de andre registreringer.
-   Hvis processen omfatter flere opgaver, som personen sandsynligvis udfører på én gang, kan du holde opgaverne i én registrering, for eksempel "Konfigurer og tildel funktionalitetsprofiler".
-   Hvis det er noget, som en person gør én gang (f.eks. konfiguration) og derefter en anden opgave, som vedkommende kan udføre umiddelbart efter, men som også kan udføres flere gange, kan du bryde dem op i to opgaveregistreringer.

**Beslut, hvor i brugergrænsefladen en registrering starter** Siden, du arbejder på, når du begynder at registrere en opgaveregistrering påvirker, hvilken side opgaveguiden vises for.Hvis du f.eks. ønsker, at din opgaveregistrering skal vises i Hjælp-ruden, når en bruger klikker på Hjælp på siden Finansparametre, skal du starte registreringen på siden Finansparametre. **Gemme optagelser som .axtr-filer** Når du er færdig med at oprette eller redigere en opgaveregistrering, får du vist flere muligheder for, hvordan du vil downloade eller gemme registreringen. Du kan hente filen som en opgaveregistreringspakke (.axtr), hente den som en råfil med registreringer (.xml), hente den som et Word-dokument eller gemme filen i et LCS-bibliotek. Det er en god ide altid at gemme din opgaveregistrering som en pakkefil med opgaveregistrering (.axtr). Dette vil gøre det nemmere at vedligeholde filen, hvis procedurer eller anmærkninger skal ændres senere. Hvis du vil hente filen som et Word-dokument, kan du også gemme den som en pakkefile med opgaveregistrering.

## <a name="create-your-task-recording"></a>Oprette din opgaveregistrering
Du kan finde en detaljeret gennemgang i [Ressourcer til arbejdsrutineoptager](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Kopiere og tilpasse Microsofts opgaveregistreringer
Du kan hente og redigere Microsofts opgaveregistreringer for at bruge dem til din egen Hjælp-dokumentation eller dit eget undervisningsmateriale. Følg nedenstående trin, når du vil hente en Microsoft-opgaveregistrering:

1.  Åbn Arbejdsrutineoptager. Arbejdsrutineoptager findes i menuen **Indstillinger**.
2.  Klik i ruden Arbejdsrutineoptager på **Vedligehold en registrering.**
3.  Under **Hvor er registreringen?** skal du klikke på **Det er et LCS-bibliotek**.
4.  Klik på **Vælg LCS-biblioteket**.
5.  Vælg det globale Microsoft-bibliotek.
6.  I træet skal du vælge den biblioteksnode for forretningsproces, som opgaveregistreringen er tilknyttet.
7.  Klik på **OK**.
8.  Klik på **Start**.
9.  På dette punkt skal du gå gennem registreringen og ændre eventuelle trin, når du vil registrere den igen. **Bemærk!** Hvis du kun vil ændre teksten i en registrering, kan du åbne registreringen i tilstanden **Rediger en registrerings anmærkninger** og derefter gemme den.
10. Når registreringen er afspillet helt, skal du klikke på **Stop** på værktøjslinjen Arbejdsrutineoptager øverst på skærmen.
11. Vælg, hvordan du vil gemme Arbejdsrutineoptager.

## <a name="include-your-task-recordings-in-the-help-pane"></a>Medtag dine opgaveregistreringer i Hjælp-ruden
For at få vist dine egne brugerdefinerede opgaveregistreringer i ruden Hjælp, så de kan afspilles som opgaveguider eller vises som tekst, skal du gemme opgaveregistreringerne i dit eget BPM-bibliotek og derefter opdatere dine systemparametre til Hjælp til at pege på BPM-biblioteket. Du kan finde flere oplysninger i [Tilslut Hjælp-systemet](../../fin-ops/get-started/help-connect.md).

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Hjælp-system](../../fin-ops/get-started/help-overview.md)

[Oprette forbindelse til Hjælp-systemet](../../fin-ops/get-started/help-connect.md)

[Arbejdsrutineoptager](task-recorder.md)

[Opret avancerede emner i Hjælp med Arbejdsrutineoptager (eksternt link)](https://mbspartner.microsoft.com/AX/Videos/970)
