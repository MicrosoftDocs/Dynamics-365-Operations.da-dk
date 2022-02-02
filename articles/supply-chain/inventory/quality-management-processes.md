---
title: Oversigt over styring af kvalitet og uoverensstemmelse
description: Dette emne introducerer funktioner til styring af kvalitet og uoverensstemmelse i Microsoft Dynamics 365 Supply Chain Management og forklarer, hvordan de kan hjælpe med at forbedre produktkvaliteten i din forsyningskæde.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling, InventNonConformanceHistory, InventNonConformanceTable, InventQualityOrderLineResults, InventQualityOrderTable, InventTestCorrection, InventTestDiagnosticType, InventTestInstrument, InventTestReportSetup, InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "11574"
- intro-internal
ms.assetid: 5ac8a059-5cb4-4cb5-ba14-b944bd08dae9
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1bb4bcb7f554c22b4e1ab1b41867bd2d3dcca4d4
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985503"
---
# <a name="quality-and-nonconformance-management-overview"></a>Oversigt over styring af kvalitet og uoverensstemmelse

[!include [banner](../includes/banner.md)]

Dette emne introducerer funktioner til styring af kvalitet og uoverensstemmelse i Microsoft Dynamics 365 Supply Chain Management og forklarer, hvordan de kan hjælpe med at forbedre produktkvaliteten i din forsyningskæde.

Kvalitetssikring omfatter test af produkter og håndteringen af uoverensstemmende materiale. Processer for kvalitetsstyring hjælper med at sikre et højt niveau af produkternes kvalitet i forsyningskæden. Disse processer kan også hjælpe med at optimere processer for forsyningskæden og øge kundetilfredsheden. Kvalitetsstyring kan hjælpe dig med at administrere behandlingstid, når du har med ikke-standardiserede produkter at gøre, uanset oprindelsessted for de pågældende produkter. Du kan sammenkæde diagnosticeringsresultater til korrektion af opgaver. Systemet kan planlægge opgaver til at løse problemer og derfor hjælpe med til at forhindre gentagelser af disse problemer i fremtiden. Kvalitetsstyring giver dig også mulighed for at spore problemer (herunder interne problemer) efter problemtype, og giver dig mulighed for at identificere løsninger som enten kortsigtede eller langsigtede. Statistik over nøgletal (KPI'er) giver indsigt i problemer med uoverensstemmelse, der er sket tidligere, og de løsninger, der anvendes til at rette dem. Du kan bruge historiske data til at gennemgå effektiviteten af kvalitetsmål, der tidligere er truffet, og fastlægge passende foranstaltninger i fremtiden.

Kvalitetsstyring kan hjælpe dig med at administrere behandlingstid, når du håndterer ikke-standardiserede produkter, uanset deres oprindelsessted. Fordi diagnosticeringstyper er knyttet til rapportering af korrektion, kan Supply Chain Management planlægge opgaver for at løse problemer og forhindre dem i fremtiden.

Ud over funktionen til styring af uoverensstemmelser omfatter kvalitetsstyring funktioner til sporing af problemer efter problemtype (også når problemet er internt) og til identifikation af løsninger på kort og lang sigt. Statistik over nøgletal (KPI'er) giver indsigt i historikken for tidligere problemer med uoverensstemmelse, og de løsninger, der blev anvendt til at rette dem. Du kan bruge historikdata til at gennemgå effektiviteten af tidligere kvalitetsmål og fastlægge passende foranstaltninger, der skal bruges i fremtiden.

Når du opretter en kvalitetstilknytning, kan Supply Chain Management oprette kvalitetsordrer for forskellige forretningsprocesser, hændelser og betingelser. Kvalitetstilknytningen kan dække en bestemt vare, en bestemt gruppe varer eller alle varer.

## <a name="examples-of-the-use-of-quality-management"></a>Eksempler på brug af kvalitetsstyring

Kvalitetsstyring er fleksibel og kan gennemføres på forskellige måder for at opfylde kravene på bestemte niveauer i forsyningskædeoperationer. Eksemplerne nedenfor viser mulige anvendelser af disse funktioner:

- Automatisk start af en proces for kvalitetskontrol baseret på foruddefinerede kriterier (f.eks. ved lagerregistreringen af en indkøbsordre fra en bestemt leverandør).
- Spærre lageret under kontrol for at forhindre, at ikke-godkendt lagerbeholdning bliver brugt (fuld spærring af indkøbsordreantal).
- Bruge vareprøve som en del af en kvalitetstilknytning til at definere beløbet af det aktuelle fysiske lager, der skal undersøges. Varestikprøver kan baseres på faste antal, en procentdel eller hele varenummeret.
- Opret kvalitetsordrer for delleverancer. For at oprette en kvalitetsordre, der er baseret på det antal, der fysisk er modtaget med en ordre, skal du markere afkrydsningsfeltet **Pr. opdateret antal** på siden **Varestikprøve**.
- Oprette testtyper, der omfatter minimum, maksimum og måltestværdier og udføre kvalitative kontra kvantitative test, der har foruddefinerede valideringsresultater.
- Angive et acceptabelt kvalitetsniveau (AQL) for at styre tolerancer for kvalitetsmål.
- Angive de ressourcer, som en inspektionshandling kræver, f.eks. et testområde og testinstrumenter.

> [!NOTE]
> Funktionen _Kvalitetsstyring for lagerstedsprocesser_ udvider funktionerne for kvalitetsstyring. Hvis du bruger denne funktion, skal du se [Kvalitetsstyring for lagerstedsprocesser](quality-management-for-warehouses-processes.md) for at få vist eksempler på, hvordan kvalitetsstyring fungerer, når den er aktiveret.

## <a name="controlling-the-quality-management-process"></a>Styring af processen for kvalitetsstyring

Her er nogle af de måder, du kan styre processen til kvalitetsstyring på:

- Opret kvalitetsordrer, der er baseret på udløsningspunkter som f.eks. "ved produktmodtagelse" for indgående operationer eller "ved produktafhentning" for udgående operationer.
- Dokumentér testresultaterne, og bestem, om resultaterne opfylder de fastlagte testkriterier og AQL'er.
- Du kan bruge dokumentstyring til detaljerede produktspecifikationer og brugerspecifikke noter som en del af rapportering under inspektionsprocessen.
- Vedligehold produkter, der ikke opfylder kravene, og koordiner produkter med ekstra oplysninger om uoverensstemmelse for at spore den oprindelige årsag til et problem.
- Dokumentér omkostninger ved administration af en uoverensstemmelse. Denne omkostning kan omfatte de varer (som f.eks. reservedele), diverse tillæg og timer på timeseddel, som kræves for at kunne håndtere uoverensstemmelsen.
- Planlæg processer for fejlkorrektion ved hjælp af korrektionshåndtering, der er knyttet til kvalitetsordrer.

[![Proces for kvalitetsstyring.](media/quality-management-process-diagram.png)](media/quality-management-process-diagram.png)

## <a name="product-testing-and-quality-orders"></a>Produkttest og kvalitetsordrer

Produkttest kaldes som regel kvalitetskontrol og bruger kvalitetsordrer. Når du bruger kvalitetskontrolfunktionen, kan du gøre følgende:

- Definer de test, der skal udføres for materialet. Disse test omfatter kvalitetsspecifikationerne, det relevante testinstrument og de dokumenter, der beskriver testen, en varestikprøveplan og AQL'er.
- Opret en kvalitetsordre, der identificerer de test, som skal udføres for en bestemt ordre (f.eks. en købs- eller produktionsordre) eller for et bestemt lagerantal. Du kan oprette en kvalitetsordre manuelt, eller der kan genereres en kvalitetsordre automatisk på baggrund af retningslinjer for kvalitet.
- Definer retningslinjerne for kvalitet angående indkøb, karantæne, produktion eller salgsordrer i hver virksomhedsproces, så der automatisk kan genereres en kvalitetsordre, der identificerer testkravene for indgående eller udgående materiale.
- Registrer testresultaterne i en kvalitetsordre, valider testresultaterne i forhold til AQL'et, og udskriv et analysecertifikat, der viser testresultaterne.

## <a name="nonconformance"></a>Uoverensstemmelse

En uoverensstemmelse beskriver en vare med et kvalitetsproblem. Med processen for uoverensstemmelse kan du oprette en uoverensstemmende ordre, der beskriver en mængde uoverensstemmende materiale med hensyn til problemkilde, problemtype og posteringsnoter. Du kan definere en klassificering af problemtyper for at gøre analyse af uoverensstemmende materiale nemmere. Du kan også udskrive et uoverensstemmelsesmærkat og en uoverensstemmelsesrapport, der skal vejlede i dispositionen af uoverensstemmende materiale. Mærket og rapporten kan f.eks. angive en betingelse for **Ubrugelig** eller **Begrænset brug**.

Følgende tabel viser seks standard uoverensstemmelsestyper og beskriver de oplysninger, der skal registreres for hver type.

| Uoverensstemmelsestype | Kildeoplysninger |
|---|---|
| Debitor | Debitorkontonummeret, salgsordrenummeret eller et partinummer for en salgsordrepostering. Uoverensstemmelsen kan f.eks. vedrøre en bestemt salgsordreforsendelse eller kundetilbagemeldinger vedrørende et produkts kvalitet. |
| Serviceanmodning | Debitorkontonummeret, salgsordrenummeret eller et partinummer for en salgsordrepostering. Uoverensstemmesen kan f.eks. vedrøre en bestemt salgsordreforsendelse eller kundeklager over varens kvalitet. |
| Kreditor | Leverandørkontonummeret, indkøbsordrenummeret eller et partinummer for en indkøbsordrepostering. Uoverensstemmelsen kan f.eks. vedrøre en indkøbsordretilgang eller en leverandørs bekymring for en vare, som denne leverer. |
| Produktion | Produktionsordrenummeret eller et partinummer for en produktionsordrepostering. Uoverensstemmelsen kan f.eks. vedrøre et bestemt batch, der er fremstillet. |
| Intern | Kvalitetsordrenummeret eller et partinummer for en kvalitetsordrepostering. Uoverensstemmelsen kan f.eks. vedrøre test, der er blevet udført som del af en kvalitetsordre, eller foranlediget af en medarbejders bekymring for produktkvaliteten. |
| Produktion af samprodukter | En uoverensstemmelse i samprodukt i forbindelse med produktionsordren, der er relateret til batchproduktionsordrer. |

Uoverensstemmelser er knyttet til en problemtype. Problemtyper, der er defineret på siden **Problemtyper**, hvor du angiver, hvilke problemtyper der kan knyttes til hver enkelt uoverensstemmelsestype. Problemtyperne for uoverensstemmelser af typen **Serviceanmodning** kan f.eks. afspejle en klassifikation af kundeklager, mens problemtyperne for uoverensstemmelser af typen **Intern** kan repræsentere en klassifikation af defektkoder.

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

## <a name="additional-resources"></a>Yderligere ressourcer

- [Aktivere styring af kvalitet og uoverensstemmelse](enable-quality-management.md)
- [Lagerspærring](inventory-blocking.md)
- [Karantæneordrer](quarantine-orders.md)
- [Inspicere varers kvalitet](tasks/inspect-quality-goods.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
