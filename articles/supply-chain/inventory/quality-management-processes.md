---
title: Processer for kvalitetsstyring
description: Denne artikel indeholder oplysninger om kvalitetsstyringsprocessen for ikke-standardiserede produkter. Det beskriver, hvordan du kan bruge funktioner til kvalitetskontrol, definere og vedligeholde uoverensstemmelser og håndtere rettelser.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling, InventNonConformanceHistory, InventNonConformanceTable, InventQualityOrderLineResults, InventQualityOrderTable, InventTestCorrection, InventTestDiagnosticType, InventTestInstrument, InventTestReportSetup, InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 11574
ms.assetid: 5ac8a059-5cb4-4cb5-ba14-b944bd08dae9
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2ab3b886b9d5237e96e193d7369c6060f19516e5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424903"
---
# <a name="quality-management-processes"></a>Processer for kvalitetsstyring

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om kvalitetsstyringsprocessen for ikke-standardiserede produkter. Det beskriver, hvordan du kan bruge funktioner til kvalitetskontrol, definere og vedligeholde uoverensstemmelser og håndtere rettelser.

Kvalitetssikring omfatter test af produkter og håndteringen af uoverensstemmende materiale. Processer for kvalitetsstyring hjælper med at sikre et højt niveau af produkternes kvalitet i forsyningskæden. Disse processer kan også hjælpe med at optimere processer for forsyningskæden og øge kundetilfredsheden. Kvalitetsstyring kan hjælpe dig med at administrere behandlingstid, når du har med ikke-standardiserede produkter at gøre, uanset oprindelsessted for de pågældende produkter. Du kan sammenkæde diagnosticeringsresultater til korrektion af opgaver. Systemet kan planlægge opgaver til at løse problemer og derfor hjælpe med til at forhindre gentagelser af disse problemer i fremtiden. Kvalitetsstyring giver dig også mulighed for at spore problemer (herunder interne problemer) efter problemtype, og giver dig mulighed for at identificere løsninger som enten kortsigtede eller langsigtede. Statistik over nøgletal (KPI'er) giver indsigt i problemer med uoverensstemmelse, der er sket tidligere, og de løsninger, der anvendes til at rette dem. Du kan bruge historiske data til at gennemgå effektiviteten af kvalitetsmål, der tidligere er truffet, og fastlægge passende foranstaltninger i fremtiden.

## <a name="controlling-the-quality-management-process"></a>Styring af processen for kvalitetsstyring
Her er nogle af de måder, du kan styre processen til kvalitetsstyring på:

-   Opret kvalitetsordrer, der er baseret på udløsningspunkter som "på produktkvitteringen" for indgående transaktioner eller "ved afhentning af produktet" for udgående transaktioner.
-   Dokumentér testresultaterne, og bestem, om resultaterne opfylder de fastlagte testkriterier og acceptable kvalitetsniveauer.
-   Du kan bruge dokumentstyring til detaljerede produktspecifikationer og brugerspecifikke noter som en del af rapportering under inspektionsprocessen.
-   Vedligehold produkter, der ikke opfylder kravene, og koordiner disse produkter med ekstra oplysninger om uoverensstemmelse for at spore den oprindelige årsag til et problem.
-   Dokumentér omkostninger ved administration af en uoverensstemmelse. Denne omkostning kan omfatte de varer (som f.eks. reservedele), diverse tillæg og timer på timeseddel, som er påkrævet for at kunne rette uoverensstemmelsen.
-   Planlæg processer for fejlkorrektion ved hjælp af korrektionshåndtering, der er knyttet til kvalitetsordrer.

[![Proces for kvalitetsstyring](./media/quality-management-process-diagram.png)](./media/quality-management-process-diagram.png)  

## <a name="product-testing-and-quality-orders"></a>Produkttest og kvalitetsordrer
Produkttest kaldes som regel kvalitetskontrol og bruger kvalitetsordrer. Når du bruger kvalitetskontrolfunktionen, kan du gøre følgende:

-   Definer de test, der skal udføres for materialet. Disse tests omfatter kvalitetsspecifikationerne, det gældende testinstrument, de dokumenter, der beskriver testen, en vareprøveplan og det acceptable kvalitetsniveau.
-   Opret en kvalitetsordre, der identificerer de test, som skal udføres for en bestemt ordre (f.eks. en købs- eller produktionsordre) eller for et bestemt lagerantal. Du kan oprette en kvalitetsordre manuelt eller oprette en kvalitetsordre automatisk på baggrund af retningslinjer for kvalitet.
-   Definer retningslinjerne for kvalitet, der vedrører indkøb, karantæne, produktions- eller salgsordrer i hver forretningsproces, så en kvalitetsordre kan oprettes automatisk, og som identificerer testkravene for indgående eller udgående materiale.
-   Registrer testresultaterne i en kvalitetsordre, valider testresultaterne i forhold til det acceptable kvalitetsniveau, og udskriv et analysecertifikat, der viser testresultaterne.

## <a name="nonconformance"></a>Uoverensstemmelse
En uoverensstemmelse beskriver en vare med et kvalitetsproblem. Med processen for uoverensstemmelse kan du oprette en uoverensstemmende ordre, der beskriver en mængde uoverensstemmende materiale med hensyn til problemkilde, problemtype og posteringsnoter. Du kan definere en klassificering af problemtyper for at gøre analyse af uoverensstemmende materiale nemmere. Du kan også udskrive et uoverensstemmelsesmærkat og en uoverensstemmelsesrapport, der skal vejlede i dispositionen af uoverensstemmende materiale. Mærket og rapporten kan f.eks. angive en betingelse for **Ubrugelig** eller **Begrænset brug**.

Følgende tabel viser seks standard uoverensstemmelsestyper og beskriver de oplysninger, der skal registreres for hver type.

| Uoverensstemmelsestype   | Kildeoplysninger                                                                                                                                                                                                                          |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Debitor              | Debitorkontonummeret, salgsordrenummeret eller et partinummer for en salgsordrepostering. Uoverensstemmelsen kan f.eks. vedrøre en bestemt salgsordreforsendelse eller kundetilbagemeldinger vedrørende et produkts kvalitet.       |
| Serviceanmodning       | Debitorkontonummeret, salgsordrenummeret eller et partinummer for en salgsordrepostering. Uoverensstemmesen kan f.eks. vedrøre en bestemt salgsordreforsendelse eller kundeklager over varens kvalitet.     |
| Kreditor                | Leverandørkontonummeret, indkøbsordrenummeret eller et partinummer for en indkøbsordrepostering. Uoverensstemmelsen kan f.eks. vedrøre en indkøbsordretilgang eller en leverandørs bekymring for en vare, som denne leverer. |
| Produktion            | Produktionsordrenummeret eller et partinummer for en produktionsordrepostering. Uoverensstemmelsen kan f.eks. vedrøre et bestemt batch, der er fremstillet.                                                                      |
| Intern              | Kvalitetsordrenummeret eller et partinummer for en kvalitetsordrepostering. Uoverensstemmelsen kan f.eks. vedrøre test, der er blevet udført som del af en kvalitetsordre, eller foranlediget af en medarbejders bekymring for produktkvaliteten.     |
| Produktion af samprodukter | En uoverensstemmelse i samprodukt i forbindelse med produktionsordren, der er relateret til batchproduktionsordrer.                                                                                                                                                    |

Uoverensstemmelser er knyttet til en problemtype. Problemtyper, der er defineret på siden **Problemtyper**, hvor du angiver, hvilke problemtyper der kan knyttes til hver enkelt uoverensstemmelsestype. Problemtyperne for uoverensstemmelse for typen **Serviceanmodning** kan f.eks. afspejle en klassifikation af kundeklager, mens problemtyperne for uoverensstemmelse af typen **Intern** kan repræsentere en klassifikation af defektkoder.

Når du opretter en ny uoverensstemmelse, vælger du overensstemmelsestypen og problemtypen. Status for første godkendelse er **Ny**, der repræsenterer en anmodning om handling. Det næste trin er at ændre godkendelsesstatussen til **Godkendt** eller **Afvist** for at angive, at du vil eller ikke vil udføre en handling for uoverensstemmelsen. Du kan også lukke uoverensstemmelsen (ved at vælge et særskilt afkrydsningsfelt) for at angive, at du er færdig med den, eller du kan genåbne en uoverensstemmelse for at angive, at der kræves yderligere handlinger.

Du kan skrive bemærkninger til en uoverensstemmelse ved at vedhæfte et dokument. Det er en god idé at definere en entydig dokumenttype for uoverensstemmelser ved hjælp af siden **Dokumenttype**. Du kan derefter bruge siden **Rapportopsætning** til at definere, om der skal udskrives kommentarer til denne dokumenttype på uoverensstemmelsesrapporten og uoverensstemmelsesmærkatet. Uoverensstemmelsesrapporten og uoverensstemmelsesmærkatet kan hjælpe med materialedisponering. Du kan generere rapporter og mærkater selektivt på basis af udvælgelseskriterier, der er knyttet til en uoverensstemmelse. Disse kriterier omfatter uoverensstemmelsesnummer, vare, debitor, kreditor og status.

Rapportopsætning viser tallet for uoverensstemmelsen, vare og problemtype. Afhængigt af politikken for rapportens opsætning kan rapporten vise relaterede noter om uoverensstemmelsen. Mærkatet for uoverensstemmelsen viser også lignende oplysninger og indeholder også karantænezone og type (som f.eks. **Begrænset brug** eller **Ubrugelig**), som du har tildelt til uoverensstemmelsen som en vejledning til dispositionen af de defekte materialer.

## <a name="approved-nonconformance"></a>Godkendt uoverensstemmelse
Du kan vælge at angive en eller flere relaterede handlinger for en godkendt uoverensstemmelse. En relateret operation er det arbejde, der skal udføres, og indeholder en liste over kvalitetsoperationer, som du har defineret og beskrivende tekst om årsagen til, at arbejdet skal udføres. Når du definerer en operation, kan du vælge at angive de tillæg, varer og timeseddelbaserede arbejdstimer, der kræves for at udføre arbejdet. De beregnede omkostninger vises for den relaterede operation, og de samlede beregnede omkostninger vises for uoverensstemmelsen. De beregnede omkostninger og de underliggende detaljer (om varer, arbejdsløn og tillæg) udgør referenceoplysninger, som kun skal bruges i funktionen til kvalitetsstyring.

Du kan vælge at oprette en kvalitetsordre på basis af en uoverensstemmelse ved først at foretage en forespørgsel på kvalitetsordrer og derefter oprette den nye kvalitetsordre. En kvalitetsordre kan f.eks. identificere behovet for et teste eller (genteste) det defekte materiale. Den nyoprettede kvalitetsordre viser tilknytningen til den oprindelige uoverensstemmelse.

Du kan vælge at knytte en uoverensstemmelse til en anden og oprette en ny uoverensstemmelse på grundlag af en eksisterende. Tilknytningen kan f.eks. afspejle forbindelsen mellem kvalitetsproblemer.

## <a name="correction-handling"></a>Korrektionshåndtering
Med siden **Rettelser** kan du oprette en liste over uoverensstemmelser, der skal rettes. Hver korrektionsvare er knyttet til den diagnosticeringstype, der forårsagede problemet til at blive opdaget. Siden **Rettelser** indeholder også oplysninger om, hvem der skal udføre en korrigerende handling, og hvornår. Du kan beskrive detaljer om problemet og de afhjælpende foranstaltninger, der kræves, ved at vedhæfte et dokument til korrektionen. Når uoverensstemmelsen er løst eller rettet, skal du "lukke" korrektionsvaren ved at vælge indstillingen **Fuldført**. Du kan også angive, at løsningen er en kortsigtet løsning.

Det er en god idé at definere en entydig dokumenttype for rettelser ved hjælp af siden **Dokumenttype**. Du kan derefter bruge siden **Rapportopsætning** til at definere, om der skal udskrives kommentarer til denne dokumenttype på rettelsesrapporten. En udskrevet rettelsesrapport viser oplysninger om uoverensstemmelsen og de relaterede uoverensstemmelsesbemærkninger. Rapporten indeholder også oplysninger om rettelser, som f.eks. diagnosticeringstypen og de relaterede rettelsesbemærkninger.

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Oversigt over kvalitetsstyring](enable-quality-management.md)

[Håndtering af uoverensstemmelse](enable-nonconformance-management.md)

[Lagerblokering](inventory-blocking.md)

[Karantæneordrer](quarantine-orders.md)

[Konfigurere kvalitetsordrer](tasks/set-up-quality-orders.md)

[Kontrollere kvaliteten af varer](tasks/inspect-quality-goods.md)
