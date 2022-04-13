---
title: Brugerkonti til mobilenhed
description: Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere og administrere brugerkonti, der gør det muligt for arbejdere at logge på og bruge lagerstedsappen.
author: Mirzaab
ms.date: 09/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-09-15
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c4cb36160e692cc12140b57037d2c9739f7b2ebd
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462664"
---
# <a name="mobile-device-user-accounts"></a>Brugerkonti til mobilenhed

[!include [banner](../includes/banner.md)]

Hver gang en arbejder begynder at bruge lagerstedsappen, skal han eller hun logge på med et brugernavn og en adgangskode. Der kan knyttes et vilkårligt antal brugere af lagerstedsappen til hver enkelt arbejder i systemet, og lagersteder knyttes typisk til hver af disse brugere af lagerstedsappen. Der konfigureres også forskellige indstillinger for hver arbejder for at angive standardindstillinger og andre indstillinger, der er relevante for brugen af lagerstedsappen.

## <a name="set-up-the-required-worker-and-employee-records"></a>Konfigurere de nødvendige arbejder- og medarbejderposter

Før du kan konfigurere brugere af en lagerstedsapp, skal hver arbejder allerede eksistere som medarbejder eller arbejder i Supply Chain Management i modulet **Human Resources**.

## <a name="set-up-mobile-device-user-accounts"></a><a name="set-wma-users"></a>Konfigurere brugerkonti til mobilenhed

Når de nødvendige arbejdere og medarbejdere er konfigureret i Human Resources, kan du tildele brugere af lagerstedsappen til hver af dem og konfigurere andre indstillinger, der påvirker, hvordan de kan bruge appen.

1. Gå til **Lokationsstyring \> Konfiguration \> Arbejder**.
1. Hvis du vil redigere en eksisterende arbejder, skal du vælge arbejderen i listeruden. Vælg **Ny** i handlingsruden for at tilføje en ny post.
1. Hvis du konfigurerer en ny arbejder, skal du følge disse trin:

    1. I feltet **Arbejder** skal du vælge destinationsbrugeren på listen over medarbejdere.
    1. Vælg **Vælg**.
    1. Vælg **Gem** i handlingsruden.

1. En standardprofil kan bruges til at guide lagerarbejderen på pakkestationen gennem den proces, der kræves der. Standardprofilen kan også bruges til at gemme arbejderens foretrukne profilindstillinger. I oversigtspanelet **Profil** skal du indstille følgende felter:

    - **Politik for containerpakning** – Vælg en politik for containerpakning, der definerer, hvordan containere på pakkestationen skal behandles. Den politik for containerpakning, som vælges her, vælges på forhånd for arbejderen, når denne åbner pakkestationen. Yderligere oplysninger finder du i følgende blogindlæg: [Forbedret funktionalitet af følgeseddel](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611).
    - **Pakkeprofil-id** – Vælg et pakkeprofil-id, der definerer de indstillinger for pakkepolitik og container, der bruges. Hvis det valgte pakkeprofil-id er knyttet til en politik for containerpakning, kan du ikke ændre indstillingen **Politik for containerpakning** på denne side.

1. I oversigtspanelet **Standardpakkestation** skal du angive følgende felter for at definere den standardpakkestation, der gælder, når arbejderen logger på. Hvis det er nødvendigt, kan arbejderen vælge en anden pakkestation.

    - **Sted** – Vælg det sted, hvor standardpakkestationen er placeret.
    - **Lagersted** – Vælg det lagersted, hvor standardpakkestationen er placeret.
    - **Lokation** – Vælg lokationen for standardpakkestationen.

1. I oversigtspanelet **Brugere** kan du oprette et vilkårligt antal brugerkonti til lagerstedsappen for den valgte arbejder. Hver konto er tilknyttet et bestemt lagersted eller flere lagersteder. Brug værktøjslinjen til at tilføje eller fjerne brugerkonti, nulstille adgangskoden til en valgt konto eller tildele lagersteder til en valgt konto. For hver brugerkonto kan du angive følgende felter:

    - **Bruger-id** – Angiv et entydigt id.
    - **Brugernavn** – Angiv et navn til id'et.
    - **Standardlagersted** – Angiv det standardlagersted, hvor arbejderen normalt arbejder. Du kan bruge værktøjslinjen til at tildele flere lagersteder, og arbejderen kan skifte mellem lagersteder ved hjælp af den indirekte aktivitet for **Skift lagersted** i menupunktet på mobilenheden.
    - **Menunavn** – Vælg den rodmenu, der skal være startside for arbejderen. Muligheden for at konfigurere en rodmenu for hver arbejder er nyttig, da det giver dig mulighed for at styre menustrukturen, som hver arbejder kan bruge. Menuen for arbejdere, der kun er aktive i det udgående område, kan f.eks. være tilpasset opgaver, der vedrører udgående operationer for det pågældende område.
    - **Inaktiv** – Hvis afkrydsningsfeltet er markeret, er brugerkontoen inaktiv. Brugerkontoen deaktiveres automatisk, hvis en arbejder angiver den forkerte adgangskode fem gange i træk i lagerstedsappen. Du kan manuelt markere dette afkrydsningsfelt. Fjern markeringen i afkrydsningsfeltet for at aktivere brugeren igen.

1. I oversigtspanelet **Arbejde** skal du indstille følgende felter:

    - **Tillad tilsidesættelse af pluklokation** – Angiv denne indstilling til *Ja*, hvis arbejderen skal kunne tilsidesætte lokationen for pluktrin. Denne egenskab kan være nyttig, hvis det fysiske lager ikke svarer til den systemforeslåede lokation.
    - **Tillad tilsidesættelse af læg på lager-lokation** – Angiv denne indstilling til *Ja*, hvis arbejderen skal kunne tilsidesætte lokationen for læg på lager-trin. Denne egenskab kan være nyttig, hvis den foreslåede læg på lager-lokation er fuld eller ikke tilgængelig, eller hvis den midlertidige lagringslokation er ændret.
    - **Tillad salg over pluk** – Angiv denne indstilling til *Ja* for at tillade arbejderen at overplukke, når salgsordrer plukkes. Du kan finde flere oplysninger under [Overpluk af salgsordrer og flytteordrer](over-picking-for-sales-and-transfer-orders.md).
    - **Tillad flytteordre over pluk** – Angiv denne indstilling til *Ja* for at tillade arbejderen at overplukke, når flytteordrer plukkes. Du kan finde flere oplysninger under [Overpluk af salgsordrer og flytteordrer](over-picking-for-sales-and-transfer-orders.md).
    - **Tillad lagerbevægelser med tilknyttet arbejde** – Angiv denne indstilling til *Ja*, hvis arbejderen skal kunne flytte lager, der allerede er reserveret eller allerede er tilknyttet andet arbejde. Du kan finde flere oplysninger under [Flytning af lager med tilknyttet arbejde i lagerstedsstyring](move-inventory-associated-work.md).
    - **Tillad manuel vareomfordeling** – Angiv denne indstilling til *Ja* for at aktivere manuel omfordeling for arbejderen under kort pluk. Vareomfordeling får arbejderne til at plukke lager fra en anden lokation. Selvom automatisk omfordeling er tilgængelig for alle arbejdere, kræver manuel omfordeling eksplicit opsætning for en arbejder. Muligheden for at styre manuel omfordeling for hver arbejder kan være nyttig, fordi det giver dig mulighed for at styre den synlighed, hver arbejder har, når varepluk fra karantæne- eller masseområdet f.eks. er begrænset til betroede arbejdere. Yderligere oplysninger finder du i følgende blogindlæg: [Automatisk og manuel vareomfordeling under kort plukning](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/11/07/automatic-and-manual-item-reallocation-during-the-short-picking-dynamics-365-for-operations-1611/).
    - **Er en cyklusoptællingssupervisor** – Angiv denne indstilling til *Ja* for at gøre arbejderen til en cyklusoptællingssupervisor. I dette tilfælde godkendes alle cyklusoptællinger, som arbejderen udfører på lagerstedsappen, med det samme. Der tages ikke højde for felterne **Grænse for maks. procent**, **Grænse for maks. antal** og **Grænse for maks. værdi** for arbejdere, som denne indstilling er angivet til *Ja* for.
    - **Grænse for maks. procent** – Angiv den højeste procentvise grænse, som en cyklusoptælling kan afvige fra det forventede antal, uden at det kræver godkendelse fra en cyklusoptællingssupervisor.
    - **Grænse for maks. antal** – Angiv det samlede antal, som det angivne antal kan være forskelligt fra det forventede antal (i enheder), uden at det kræver godkendelse fra en cyklusoptællingssupervisor.
    - **Grænse for maks. værdi** – Angiv det maksimale beløb, som omkostningen på lageret kan afvige fra den forventede omkostning, uden at det kræver godkendelse fra en cyklusoptællingssupervisor.

1. Vælg **Gem** i handlingsruden.
1. Hvis du har tilføjet en ny brugerkonto, vises dialogboksen **Angiv adgangskode**, hvor du kan oprette en simpel adgangskode, som brugeren kan bruge til at logge på mobilappen. Angiv den simple adgangskode to gange, og vælg derefter **Gem adgangskode** for at fortsætte.

## <a name="set-the-language-number-formats-and-time-zone-for-each-warehouse-app-user"></a>Angive sprog, nummerformater og tidszone for hver bruger af lagerstedsappen

Når en arbejder logger på en Warehouse Management-mobilapp, ændres sproget, nummerformater og tidszone, så de stemmer overens med arbejderens indstillinger. Kontoindstillingerne for den arbejder, der vælges i trin 3 i afsnittet [Konfigurere brugerkonti for mobilenhed](#set-wma-users), bestemmer, hvilke indstillinger der bruges. Hvis du kræver separate indstillinger for hver bruger, skal du bruge forskellige arbejderkonti. Følgende procedure viser, hvordan du kan ændre sprog, nummerformater og tidszone for hver bruger af lagerstedsappen.

1. Gå til **Lokationsstyring \> Konfiguration \> Arbejder**.
1. Find navnet på den arbejder, du vil konfigurere. Kontrollér, at arbejderen har alle de nødvendige brugerkonti til lagerstedsappen, der er vist i oversigtspanelet **Brugere**. Opret en ny arbejder, og/eller tilføj brugerkonti til lagerstedsappen efter behov ved at følge trinnene i afsnittet [Konfigurere brugerkonti til mobilenhed](#set-wma-users).
1. Gå til **Systemadministration \> Brugere \> Brugere**.
1. Vælg den brugerkonto, hvor kolonnen **Person** viser navnet på den arbejder, du fandt i trin 2.

    > [!IMPORTANT]
    > De værdier for **Bruger-id**, der vises på siden **Brugere**, er *ikke* relateret til den værdi, der vises i oversigtspanelet **Brugere** på den **Arbejder**-side, du åbnede i trin 1.

1. Vælg **Brugerindstillinger** i handlingsruden.
1. Under fanen **Præferencer** skal du angive følgende felter:

    - **Sprog** – Vælg det sprog, som arbejderen foretrækker. Dette felt styrer også det talformat, der vises i lagerstedsappen.
    - **Dato-, klokkeslæts- og talformat** – Vælg det dato- og klokkeslætsformat, som arbejderen foretrækker. I lagerstedsappen bruges det talformat, der er tilknyttet det sprog, der er valgt i feltet **Sprog**, i stedet for denne indstilling.
    - **Tidszone** – Vælg den tidszone, hvor arbejderen arbejder. Dette felt påvirker tidsstemplet for alle registreringer, som arbejderen foretager ved hjælp af appen.

> [!NOTE]
> I nogle tilfælde kan lagerstedsappen ikke finde bestemte arbejderindstillinger, der fastlægger sprog, nummerformater og tidszone. Der gælder følgende regler:
>
> - Hvis appen ikke er tilknyttet et Supply Chain Management-miljø (f.eks. første gang appen startes, efter at den er installeret), bruges sproget for den lokale enhed. Når enhedssproget ændres, ændres appsproget også. Yderligere oplysninger om, hvordan du konfigurerer sproget for den lokale enhed, finder du i dokumentationen til enheden og/eller operativsystemet.
> - Hvis appen er forbundet med et Supply Chain Management-miljø, men der ikke er angivet præferencer for den arbejder, der er logget på, er sprog, nummerformater og tidszone valgt baseret på den konto, der er knyttet til det klient-id, som enheden bruger til at oprette forbindelse til Supply Chain Management. Du kan finde flere oplysninger under [Opret og konfigurer en brugerkonto i Supply Chain Management](install-configure-warehouse-management-app.md#user-azure-ad).

> [!TIP]
> Hvis du bemærker, at der vises forkerte tidsstempler for registreringer, der foretages via lagerstedsappen, skal du måske justere den tidszone, der er angivet for den brugerkonto, som arbejdere bruger til at logge på og/eller blive godkendt af Supply Chain Management. Som tidligere nævnt, kan tidszoneindstillingen komme fra den brugerkonto, der bruges til at logge på lagerstedsappen, som er konfigureret på siden **Arbejder**. Hvis brugerkontoen ikke er angivet på siden **Arbejder**, kommer tidszonen fra den brugerkonto, der er tilknyttet det klient-id, der bruges til godkendelse, som det er angivet på siden **[Azure Active Directory-programmer](install-configure-warehouse-management-app.md)**.
