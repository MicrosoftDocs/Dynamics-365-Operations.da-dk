---
title: "Oprette dokumentation eller undervisning ved hjælp af opgaveregistreringer"
description: "Dette emne forklarer, hvilke Arbejdsrutineoptager og hjælpelinjer opgave er, hvordan du opretter opgaven optagelser, og hvordan du tilpasser Microsoft opgave leder og inkludere dem i din hjælp."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: 38bce4a843f0db575c8d1ba08b7dc2ece8366663
ms.lasthandoff: 03/31/2017


---

# <a name="create-documentation-or-training-using-task-recordings"></a>Oprette dokumentation eller undervisning ved hjælp af opgaveregistreringer
Dette emne forklarer, hvilke Arbejdsrutineoptager og hjælpelinjer opgave er, hvordan du opretter opgaven optagelser, og hvordan du tilpasser Microsoft opgave leder og inkludere dem i din hjælp.

<a name="learn-about-task-recorder"></a>Få mere at vide om Arbejdsrutineoptager
-------------------------

Arbejdsrutineoptager er en Microsoft Dynamics-365 for Operations-værktøjet, som du kan bruge til at registrere de handlinger, du tager i produktets brugergrænseflade (UI). Når du bruger Arbejdsrutineoptager – registreres alle de hændelser, du udfører i Brugergrænsefladen, på serveren, herunder tilføjelse af værdier, ændring af indstillinger og fjernelse af data. De trin, du optager, bliver samlet kaldes en *opgaveregistrering*. Opgaveregistreringer kan bruges på mange måder:

-   **Opgaveregistreringer kan afspilles som opgaveguide.** Der er en integrerende del af Dynamics-365 for at hjælpe operationer oplevelse opgave vejledninger. Vejledning til en opgave er en kontrolleret, automatiseret, interaktiv oplevelse gennem trinnene til en forretningsproces. Brugeren bliver instrueret i at fuldføre hvert trin ved hjælp af en pop op-meddelelse (eller "boble"), som vil være animeret på tværs af brugergrænsefladen og pege på det element i brugergrænsefladen, som brugeren skal arbejde med. "bubble" indeholder også oplysninger om, hvordan du arbejder med elementet, som "Klik her" eller "Angiv en værdi i dette felt". Vejledning til en opgave kører mod brugerens aktuelle datasæt, og de data, der er angivet, gemmes i brugerens miljø.
-   **Opgave optagelser kan vises som en trinvis fremgangsmåde i Hjælp-ruden.** Du kan bruge Hjælp-ruden for at søge efter og få vist opgaven optagelser. Du kan få adgang til Hjælp-ruden ved at klikke på den **?** Ikonet i den øverste navigationslinje, eller du kan bruge den genvejstastekombination, **Ctrl + Skift +?**. Du kan læse trinene i en opgave, der optager i Hjælp-ruden, eller du kan vælge for at afspille optagelsen som en opgave, så den tager dig gennem Brugergrænsefladen.
-   **Opgaveregistreringer kan gemmes i BPM.** Du kan gemme din opgaveregistrering på en linje i et hierarki i et BPM-bibliotek (Business Process Modeler) i LCS (Lifecycle Services). En liste over trin og flowdiagram for en forretningsproces, der genereres fra optagelsen. Opgave-optagelser, der er gemt i et bibliotek med BPM kan vises i Dynamics 365 til handlinger som hjælp.
-   **Opgaveregistreringer kan gemmes som Word-dokumenter.** På den måde kan du nemt oprette kursusguider, der kan udskrives.

Du kan oprette dine egne optagelser af opgaven, spille opgave optagelser fra Microsoft eller ændre Microsoft opgave optagelser for at afspejle din konfiguration. Du kan finde flere oplysninger om Arbejdsrutineoptager, i [Arbejdsrutineoptager i Dynamics 365 i forbindelse med](task-recorder.md).

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
-   For hvert trin i en opgaveregistrering kan du oprette anmærkninger. Anmærkninger vises under afspilning af en opgaveguide i "boblen" som noter over eller under teksten i trinnet. Når den vises som tekst i ruden hjælp, vises anmærkninger som tekst indbygget i trin. Som med beskrivelsen er det en god ide at skrive og gemme dine anmærkninger i et separat dokument. Når du optager opgaveregistreringen, kan du klippe og indsætte anmærkningerne fra dette dokument.

**Forstå de forskellige typer af anmærkninger** Alle anmærkninger er valgfrie. Tilføj dem kun, når de giver brugeren nyttige oplysninger.

-   **Afsnit**: en titel anmærkning vises før teksten trin, der optager en opgave automatisk genererer. Anmærkningen titel vises i programguiden opgave over automatisk genererede teksten. Brug denne type anmærkning til at forklare, hvorfor brugeren udfører trinnet eller til at give ekstra kontekst.

Dette er redigeringsruden, som du ser, når du tilføjer en anmærkning, mens du opretter din registrering. Angiv en titelanmærkning i feltet **Titel**. 

[![screen1](./media/screen1.png)](./media/screen1.png) 

Sådan ser titelanmærkningen ud i "boble"-opgaveguiden. 

[![screen2](./media/screen2.png)](./media/screen2.png)

-   **Bemærk!** Der vises en anmærkning til noter efter den trintekst, som opgaveregistreringen genererer automatisk. I opgavevejledningen er den kun synlig, hvis brugeren klikker på linket **Vis flere** i opgaveguidens boble. Brug denne anmærkning til at beskrive noget, som en bruger skal kende for at fuldføre trinnet.

Dette er redigeringsruden, som du ser, når du tilføjer en anmærkning, mens du opretter din registrering. Angiv en notatanmærkning i feltet **Notater**. 

[![screen3](./media/screen3.png)](./media/screen3.png) 

Dette er, hvordan noter anmærkningen ser ud i "boble" i opgave-vejledning.

[![screen4](./media/screen4.png)](./media/screen4.png)

-   **Oplysninger om trin**: disse anmærkninger, der oprettes ved at højreklikke på et kontrolelement eller et vilkårligt sted på en formular &lt;**Arbejdsrutineoptager**&lt; ** Tilføj info trin. ** Info trin vises som en nummererede trin på sted, du indsætter, selvom intet blev registreret i Brugergrænsefladen. Du kan tilføje et infotrin på formularniveau eller et infotrin, der er knyttet til et kontrolelement. Når et infotrin er knyttet til en formular, vises opgaveguidens "boble" et sted i formularen uden markør, når opgaveguiden afspilles. Når en info-trin er knyttet til et kontrolelement, bliver opgaven guide "boble" peger på kontrolelementet, når opgave-vejledning, der afspilles. I Hjælp-ruden vises en info trin anmærkning som et nummererede trin med teksten, du har angivet. Brug info trin til at forberede brugeren til de næste trin til at beskrive de skridt, der skal udføres uden for Dynamics 365 for operationer eller til at henvise til andre optagelser (selvom du kan oprette hyperinks i anmærkningerne.).

**Fastlægge, hvor lang registreringen skal være**

-   Brugeren vil normalt enten læse eller afspille registreringen fra start til slut, så undlad at kombinere trin eller opgaver, som det er bedre at have separat.
-   Prøv ikke at optage et scenario, der er så langt, at det strækker sig over flere underordnede processer. For eksempel er "Opgaver for butikkens kundeservicedesk" for omfattende. Opdel det i kortere opgaver som "Acceptér returneringer" og "Føj til gavekort".
-   Hvis en opgave kan udføres som en del af flere forskellige forretningsprocesser, kan du oprette en separat registrering til den, og du kan henvise til den i de andre registreringer.
-   Hvis processen omfatter flere opgaver, som personen sandsynligvis udfører på én gang, kan du holde opgaverne i én registrering, for eksempel "Konfigurer og tildel funktionalitetsprofiler".
-   Hvis det er noget, som en person gør én gang (f.eks. konfiguration) og derefter en anden opgave, som vedkommende kan udføre umiddelbart efter, men som også kan udføres flere gange, kan du bryde dem op i to opgaveregistreringer.

**Beslutte, hvor i Brugergrænsefladen til at starte en optagelse** siden, du arbejder på, når du begynder at optage en optagelse opgave påvirker hvilken side, vises guiden opgave for. Hvis du vil registrere din opgave skal vises i ruden hjælp, når en bruger klikker på Hjælp på siden Finans parametre, skal du starte optagelsen på siden Finans parametre. **Gemme optagelser som .axtr-filer** Når du er færdig med at oprette eller redigere en opgaveregistrering, får du vist flere muligheder for, hvordan du vil downloade eller gemme registreringen. Du kan hente filen som en opgaveregistreringspakke (.axtr), hente den som en råfil med registreringer (.xml), hente den som et Word-dokument eller gemme filen i et LCS-bibliotek. Det er en god ide altid at gemme din opgaveregistrering som en pakkefil med opgaveregistrering (.axtr). Dette vil gøre det nemmere at vedligeholde filen, hvis procedurer eller anmærkninger skal ændres senere. Hvis du vil hente filen som et Word-dokument, kan du også gemme den som en pakkefile med opgaveregistrering.

## <a name="create-your-task-recording"></a>Oprette din opgaveregistrering
Se detaljerede gennemgå trinnene i [hvordan du opretter en opgave optagelse](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Kopiere og tilpasse Microsofts opgaveregistreringer
Du kan hente og redigere Microsofts opgave optagelser for at bruge dem til dine egne Hjælp-dokumentationen eller undervisningsmaterialer. Følg nedenstående trin, når du vil hente en Microsoft-opgaveregistrering:

1.  Dynamics 365 for operationer, Åbn Arbejdsrutineoptager. Arbejdsrutineoptager findes i menuen **Indstillinger**.
2.  Klik i ruden Arbejdsrutineoptager på **Vedligehold en registrering.**
3.  Under **Hvor er registreringen?** skal du klikke på **Det er et LCS-bibliotek**.
4.  Klik på **Vælg LCS-biblioteket**.
5.  Vælg det globale Microsoft-bibliotek.
6.  I træet skal du vælge den biblioteksnode for forretningsproces, som opgaveregistreringen er tilknyttet.
7.  Klik på **OK**.
8.  Klik på **Start**.
9.  På dette tidspunkt trin til optagelse, ændre eventuelle trin, efterhånden til at indspille den igen. **Bemærk**: Hvis du kun vil ændre teksten i en optagelse, kan du åbne registrering i **Rediger en optagelse anmærkninger** tilstand, og derefter gemme den.
10. Når registreringen er afspillet helt, skal du klikke på **Stop** på værktøjslinjen Arbejdsrutineoptager øverst på skærmen.
11. Vælg, hvordan du vil gemme Arbejdsrutineoptager.

## <a name="include-your-task-recordings-in-the-help-pane"></a>Medtage optagelserne opgave i Hjælp-ruden
For at få vist din egen brugerdefinerede opgave-optagelser i ruden hjælp, så de kan afspilles som opgave hjælpelinjer eller vises som tekst, skal du gemme optagelserne opgaven til din egen BPM-bibliotek og derefter opdatere din Hjælp-systemparametre til at pege på biblioteket BPM. Yderligere oplysninger finder du [forbinder Hjælp-systemet.](../get-started/help-connect.md)

<a name="see-also"></a>Se også
--------

[I forbindelse med Dynamics 365 hjælp](..\get-started\help-overview.md)

[Tilslut hjælp](..\get-started\help-connect.md)

[Arbejdsrutineoptager i Dynamics 365 til operationer](task-recorder.md)

[Tilføjet for nylig opgave optager funktioner](\core\get-started\recently-added-editing-features-in-task-recorder)

[Oprette nye biblioteker til uddannelse til Dynamics AX i levetidsservices ved hjælp af Arbejdsrutineoptager (eksternt link)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)

[Oprette avancerede emner i Hjælp med Arbejdsrutineoptager (eksternt link)](https://mbspartner.microsoft.com/AX/Videos/970)


