---
title: Oversigt over fletning af Dynamics 365 Human Resources-infrastruktur
description: I denne artikel beskrives fletningen af Microsoft Dynamics 365 Human Resources-infrastrukturen.
author: twheeloc
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e68b28bfde35b51605aa0b653265da6261b69a90
ms.sourcegitcommit: 68efa7b89273d04484566cbe14d3533a8fd4ee53
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/02/2022
ms.locfileid: "9819236"
---
# <a name="dynamics-365-human-resources-infrastructure-merge"></a>Fletning af Dynamics 365 Human Resources-infrastruktur 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="dynamics-human-resources-365"></a>Dynamics Human Resources 365

Microsoft Dynamics 365 Human Resources leverer værktøjer, der kan hjælpe personaleteam med at øge organisationens fleksibilitet, transformere medarbejdernes erfaring og optimere personaleprogrammer for at oprette en arbejdsplads, hvor medarbejdere og virksomheden kan blive ansat. Du kan finde flere oplysninger om Dynamics 365 Human Resources i [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Transformer medarbejdererfaringen.** Fastholdelse af de bedste medarbejdere ved at styrker ledere og medarbejdere via connectede selvbetjeningserfaringer, der er med til at skabe ansættelse og vækst.
- **Optimer HR-programmer.** Reducer driftsomkostningerne, og opret medarbejderfokuseret orlov og fravær, tid, frynsegode og kompensationsstyringsprogrammer.
- **Øg organisationsuligheden.** Gør HR i stand til at arbejde med den færdighed, som virksomheden har brug for, ved at bruge Dataverse og Microsoft Power Platform til at centralisere persondata, så de nemt kan udvide Dynamics 365 Human Resources.
- **Få indsigt i arbejdsstyrken.** Foretag databaserede beslutninger ved hjælp af muligheden for at analysere og visualisere persondata på detaljerede dashboards, der er tilgængelige på alle enheder.

## <a name="human-resources-infrastructure-merge"></a>Fletning af Human Resources-infrastruktur

Dynamics 365 Human Resources er et selvstændigt program, der aktuelt bruger en anden infrastruktur end andre programmer til finans og drift, f.eks. Dynamics 365 Finance eller Dynamics 365 Supply Chain Management. Fletningen af infrastrukturen placerer Dynamics 365 Human Resources i samme infrastruktur som andre programmer til finans og drift.

Du kan få mere at vide om fletningen af Human Resources-infrastruktur i [Fletning af HR-tilbud](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers/). Du kan finde svar på ofte stillede spørgsmål i [Ofte stillede spørgsmål om fletning af Human Resources-infrastruktur](./hr-infrastructure-merge-faq.md).

## <a name="customer-migration-vs-customer-merge"></a>Kundeoverførsel vs. kundefletning

Som et led i infrastrukturfletningen er alle funktioner i Human Resources-programmet blevet tilgængelige i finans- og driftsmiljøer. Kunder kan overføre deres Human Resources-miljøer ved hjælp af det overførselsværktøj, der findes i Microsoft Dynamics Lifecycle Services. De kan også vælge at flette dataene med deres eksisterende økonomi- og driftsmiljø. 

Overførsel af kunder og fletning af kunder er forskellige på følgende måde:

- **Kundeoverførsel** – Værktøjet til automatisk overførsel bruges til at udføre en "flytning" (bevægelse) af kundedatabasen fra Human Resources-infrastrukturen til finans- og driftsinfrastrukturen. Resultatet er et nyt finans- og driftsmiljø, hvor kundens Human Resources-database bruges. 
- **Kundefletning** – Dette ekstra trin er ikke et krav fra Microsoft. Det sker efter kundens egen vurdering og efter kundens egen tidsplan. I dette trin flyttes kundedata til et eksisterende miljø, f.eks. et Finance- eller Project Operations-miljø. Den er oftest manuel og kan udføres ved hjælp af dataenhederne i strukturen Dataadministration. 

## <a name="planning-a-human-resources-environment-migration"></a>Planlægge en overførsel af et Human Resources-miljø

Som en del af infrastrukturfletningen vil alle kunder skulle overføre deres eksisterende Human Resources-miljøer fra den enkeltstående infrastruktur. Som en hjælp til denne proces anbefaler vi, at du bruger værktøjet til automatisk overførsel i Lifecycle Services til at flytte de aktuelle miljøer til den nye infrastruktur. 

Følgende afsnit indeholder flere detaljer om, hvordan Lifecycle Services-værktøjerne bruges til at overføre et enkeltstående Human Resources-miljø. 

Kunder, der planlægger overførsel, kan have følgende forventninger:

- Alle kunder skal overflyttes til et sandkassemiljø, før de overfører produktionsmiljøet. 
- Værktøjet til overførsel giver kun mulighed for overførsel fra sandkasse til sandkasse og produktion til produktion. Derfor bestemmer miljøtypen, hvilket miljø der kan overføres korrekt. 
- Kunder kan overføre alle de sandkasser, der er brug for, før de overfører produktionsmiljøet, forudsat at der findes en ledig plads til målsandkassen. Kunder kan også slette en overført sandkasse og genoverføre flere gange. 
- Hvis overførsel af en sandkasse mislykkes, eller hvis du vil starte forfra, kan du slette et miljø i finans- og driftsinfrastrukturen og genoverføre det samme miljø.
- URL-adressen for Human Resources-miljøet er forskellig efter overførslen.
- Planlæg en passende mængde nedetid for overførslen af dit produktionsmiljø. Den forventede tidsramme for fuldførelse af den automatiserede overførselsproces er tre til fire timer. Tidsrammen varierer, afhængigt af organisationens data. Du skal validere den tid, der kræves under overførslen af dine sandkassemiljøer, og afsætte tid til andre manuelle opgaver, der skal udføres.

> [!IMPORTANT] 
> Når et produktionsmiljø er blevet overført til den økonomiske og driftsmæssige infrastruktur, slettes det enkeltstående produktionsmiljø for kilden automatisk. Du bør ikke slette det overførte produktionsmiljø. 

Overførselsprocessen sker oftest automatisk. Virksomhedens brugere skal dog udføre nogle manuelle trin og validering efter overførslen.

Følgende manuelle opgaver skal fuldføres:

- Opret et nyt Lifecycle Services-projekt til overførslen.
- Revider eventuelle integrationer i det gamle miljø med det nye miljø ved at rette integrationen mod de nye URL-adresser/slutpunkter baseret på de enkelte integrationskonfigurationer.
- Opdater datalageret til integrerede Power BI-rapporter.
- Opdater listen over dataenheder fra DMF-arbejdsområdet.
- Opret hjælpelink til Lifecycle Services.
- Opret regnskabskalendere.

Under den automatiske proces fuldføres følgende handlinger, og de skal valideres:

- Data:

    - Varianter
    - Sikkerhedsroller (herunder brugerdefinerede roller)
    - Arbejdsgange (herunder beskeder)
    - Personlige tilpasninger og gemte visninger
    - Transaktioner
    - Brugerdefinerede felter
    - Vedhæftede filer
    - Påmindelser

- Datastyring – Brug din egen database (BYOD).
- Funktionsstyring - Aktiverede/deaktiverede funktioner.
- Integrer Power Apps.
- Power Platform Administration-tilknyttet miljø (kun produktion).
- Batchjob.
- Der oprettes et tomt finansmodul for hver juridiske enhed. Standardregnskabsvalutaen og -valutakurstypen for hver finanskonto er angivet.
- I hver juridiske enhed oprettes automatisk en ny kontoplan, som knyttes til siden **Finans**. De økonomiske dimensioner, der konfigureres i Human Resources-miljøet, føjes automatisk til en ny kontostruktur, der knyttes til finansmodulet. 

> [!NOTE]
> Der skal bruges en finanskonto på finans- og driftsinfrastrukturen som en del af Dynamics 365 Finance-produktet. Den brugerdefinerede dimensionscontroller, der fandtes i det enkeltstående Dynamics 365 Human Resources-program, er ikke tilgængeligt. Den flettede infrastruktur for Human Resources bruger den økonomiske logik til at vise økonomiske dimensioner i modulet **Human Resources**. Du kan få mere at vide om kontoplanen og de økonomiske dimensioner [her](../finance/general-ledger/plan-chart-of-accounts.md). 

## <a name="considerations"></a>Overvejelser

- Overførsel til miljøer sker altid i den seneste generelt tilgængelige version. Afhængigt af overførsels- og testplanen anbefales det, at du validerer en sandkasseoverførsel i samme version som produktionsmiljøet, hvis overførselsvalidering af sandkassemiljøer var i en anden version. 
- Under overførsel placeres de overførte miljøer i samme område som de enkeltstående Human Resources-kildemiljøer.

## <a name="licensing"></a>Licensering

Der er ingen ændringer i licenser til Dynamics 365 Human Resources på følgende områder: 

- **Minimumskrav til licenskøb**
- **Licenser til et produktionsmiljø og et sandkassemiljø** – Hvis du har eksisterende enkeltstående Human Resources-licenser, der giver ret til ét produktionsmiljø og ét sandkassemiljø, vil det samme antal licenser være tilgængelige på finans- og driftsinfrastrukturen uden ekstraomkostninger.
- **Yderligere sandkasselicenser** – Hvis du har købt yderligere sandkasselicenser til det enkeltstående Human Resources-program, vil det samme antal sandkasselicenser være tilgængelige for et standardgodkendelsestestmiljø (sandkasse) i finans- og driftsinfrastrukturen uden ekstraomkostninger. 
