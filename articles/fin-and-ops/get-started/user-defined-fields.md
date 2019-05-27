---
title: Oprette og arbejde med brugerdefinerede felter
description: Dette emne viser, hvordan Microsoft Dynamics 365 for Finance and Operations tillader nogle brugere at oprette brugerdefinerede felter for at skræddersy programmet, så det passer til virksomheden.
author: jasongre
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 18402579789c17de7b46dd7a013b3b6327ea5d4f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561754"
---
# <a name="create-and-work-with-custom-fields"></a>Oprette og arbejde med brugerdefinerede felter

[!include [banner](../includes/banner.md)]

Selvom Microsoft Dynamics 365 for Finance and Operations indeholder et omfattende sæt af felter klar til brug til administration af en lang række forretningsprocesser, er der nogle gange et behov for, at et firma vil spore flere oplysninger i systemet. For at imødekomme dette behov,giver Finance and Operations dig mulighed for at oprette brugerdefinerede felter for at skræddersy programmet til virksomhedens behov, forudsat at du har rettigheder til funktionen.

Muligheden for at tilføje brugerdefinerede felter findes i platformsopdatering 13 og nyere.

Denne video viser, hvor let det er at føje et brugerdefineret felt til en side: [Tilføje brugerdefinerede felter i Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=gWSGZI9Vtnc).

## <a name="creating-custom-fields"></a>Oprettelse af brugerdefinerede felter

Når du har identificeret yderligere oplysninger, du vil spore i programmet, kan du oprette det brugerdefinerede felt i den relevante tabel og vise det nye felt på en side.

Følgende trin beskriver processen til oprettelse af et brugerdefineret felt og placeringen af det på en formular.

1. Gå til formularen, hvor der er behov for det nye felt.
2. Da slutmålet er at vise det brugerdefinerede felt i en formular, befinder startpunktet for oprettelse af brugerdefinerede felter i sig i området til brugertilpasning. Åbn værktøjslinjen til brugertilpasning ved at vælge **Indstillinger** og derefter **Tilpas denne formular**.
3. Klik på **Indsæt** og derefter på **Felt**.
4. Vælg området af formularen, hvor du vil vise det nye felt. Efter markeringen viser dialogboksen **Indsæt felter** en liste over eksisterende felter, der kan indsættes i det valgte område i formularen.
5. Kontrollér, at feltet, du er interesseret i, ikke allerede findes på listen. Hvis det er tilfældet, kan du blot markere feltet på listen og klikke på **Indsæt**.
6. Klik på den **Opret nyt felt** oven over listen for at starte processen med at oprette et brugerdefineret felt. Derved åbnes dialogboksen **Opret nyt felt**.

    Hvis du ikke kan se knappen **Opret nyt felt**, har du ikke de nødvendige tilladelser til at bruge denne funktion.

7. I dialogboksen **Opret nyt felt** skal du angive følgende oplysninger.

    1. Vælg den databasetabel, hvor feltet skal tilføjes. Bemærk, at kun de tabeller, der understøtter brugerdefinerede felter, vises på rullelisten. Se afsnittet nedenfor, for at få tekniske oplysninger om understøttede tabeller.
    2. Vælg datatypen for det nye felt. De tilgængelige datatyper er afkrydsningsfelt, dato, dato/klokkeslæt, decimal, tal, valgliste og tekst.

        - Hvis du vælger datatypen tekst, kan du også angive den maksimale længde for den tekst, der kan angives i dette felt.
        - Hvis du vælger datatypen valglisten, kan du også vælge sættet af gyldige værdier for feltet.

    3. Angiv et navn, en etiket og en hjælpetekst for feltet. Navnet svarer til det fysiske feltnavn i databasen, mens etiket og hjælpeteksten er den tekst, der bruges til at repræsentere feltet i brugergrænsefladen.

8. Hvis dette er det eneste felt, du skal oprette til denne formular, skal du klikke på **Gem**. Hvis du vil oprette flere felter, skal du klikke på **Gem og ny**, og gå tilbage til trin 7. Bemærk, at der i øjeblikket er en grænse på **20 brugerdefinerede felter pr. tabel**.
9. Når du forlader dialogboksen **Opret nyt felt**, kommer du tilbage til dialogboksen **Indsæt felter**. Alle brugerdefinerede felter, der lige er tilføjet, bliver automatisk markeret på listen til at blive indsat i formularen.
10. Klik på **Indsæt** for at indsætte de markerede felter i det valgte område i formularen.
11. **Valgfrit:** Aktivér tilstanden **Flyt** fra værktøjslinjen til personlige indstillinger for at flytte de nye felter til den ønskede placering i det valgte område. Se [Tilpasse brugeroplevelsen](personalize-user-experience.md) for at få yderligere oplysninger om, hvordan du bruger de forskellige funktioner for tilpasning til at optimere en formular til din personlige brug.

## <a name="sharing-custom-fields-with-other-users"></a>Dele brugerdefinerede felter med andre brugere

Når du har oprettet et brugerdefineret felt og vist det i en formular, ønsker du muligvis at give denne opdaterede sidevisning, der indeholder det nye felt, til andre brugere i systemet. Dette kan gøres på to forskellige måder ved hjælp af funktionerne til brugertilpasning af produktet:

- Den anbefalede rute er via systemadministratoren, der kan overføre en tilpasning til alle brugere eller en undergruppe af brugere. Du kan finde flere oplysninger i [Tilpasse brugeroplevelsen](personalize-user-experience.md).
- Du kan også eksportere dine ændringer (kaldet *tilpasninger*), og du sende dem til en eller flere brugere og få hver af disse brugere til at importere dine ændringer. Indstillingen **Administrer** på værktøjslinjen for personlige indstillinger giver dig mulighed for at eksportere og importere tilpasninger.

## <a name="managing-custom-fields"></a>Administration af brugerdefinerede felter

Styring af de brugerdefinerede felter i systemet kan udføres ved hjælp af siden **Brugerdefinerede felter** i moudlet til systemadministration. Denne side giver brugere adgang til mange egenskaber, herunder:

- Få vist en liste over alle de brugerdefinerede felter i systemet.
- Begrænset redigering af eksisterende brugerdefinerede felter.
- Sletning af brugerdefinerede felter.
- Visning af brugerdefinerede felter på dataenheder.
- Angivelse af oversættelser af etiketter til brugerdefineret felt og hjælpetekst.

### <a name="viewing-all-custom-fields"></a>Visning af alle brugerdefinerede felter

Siden **Brugerdefinerede felter** giver oversigt over alle de brugerdefinerede felter, der er defineret i systemet. Du skal blot markere den tabel, du er interesseret i, og siden opdateres for at vise en liste over de brugerdefinerede felter, der er knyttet til den pågældende tabel. Når du vælger et brugerdefineret felt på listen, kan du få vist alle detaljer om feltet.

### <a name="editing-custom-fields"></a>Redigering af brugerdefinerede felter.

Når der er oprettet et brugerdefineret felt, er det kun visse dele af oplysningerne om det brugerdefinerede felt, der kan ændres på siden **Brugerdefinerede felter**.

Du *kan* ændre disse attributter:

- Label
- Hjælpetekst
- Længde, for tekstfelter

Du *kan ikke* redigere følgende attributter:

- Feltnavn
- Datatype

For felter på valglister kan sættet af gyldige værdier for det brugerdefinerede felt derudover omarrangeres, og der kan tilføjes nye værdier, men eksisterende værdier for feltet på valglisten kan ikke fjernes. Husk at klikke på **Anvend ændringer**, når du er færdig med at redigere felter for en bestemt tabel, så ændringerne gemmes.

### <a name="exposing-custom-fields-on-data-entities"></a>Visning af brugerdefinerede felter på dataenheder

Det kan også være vigtigt at tillade brugerdefinerede felter at være synlige på dataenheder. Dataenheder bruges i funktionen [Åbn i Office](../../dev-itpro/office-integration/office-integration.md), samt hvad angår scenarier til import og eksport af data.

Følg disse trin for at få vist et brugerdefineret felt i en dataenhed:

1. Vælg det brugerdefinerede felt på formularen **Brugerdefinerede felter**.
2. Udvid afsnittet **Enheder** afsnit for at få vist sættet af relevante enheder.
3. Klik på knappen **Rediger**.
4. Rediger feltet **Aktiveret** til at være markeret for hver enhed, der skal vise dette felt.
5. Klik på **Anvend ændringer** for at gemme dine valg.

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a>Tillad, at brugerdefinerede felter vises på andre sprog

Det der kan være behov for adgang til brugerdefinerede felter på forskellige sprog, indeholder siden **Brugerdefinerede felter** en mekanisme, så etiketten og hjælpeteksten til et brugerdefineret felt kan oversættes til andre sprog.

De følgende trin beskriver processen til oversættelse af brugerdefinerede felter til andre sprog:

1. Vælg det brugerdefinerede felt på siden **Brugerdefinerede felter**.
2. Vælg knappen **Oversættelser** i bunden af handlingsruden. Der åbnes en rullemenu med eksisterende oversættelser til dette felt.
3. Rullemenuen **Sprog** viser det sæt af sprog, hvor der allerede er angivet oversættelser.

    Hvis du vil redigere en eksisterende oversættelse, skal du vælge det ønskede sprog i menuen og ændre værdierne for etiketten og hjælpeteksten.

    Ellers skal du klikke på knappen **Tilføj sprog**, vælge det ønskede sprog i menuen og derefter angive oversatte værdier for etiketten og hjælpeteksten.

4. Klik på **OK**, når du er færdig.

### <a name="deleting-custom-fields"></a>Sletning af brugerdefinerede felter

I sjældne tilfælde kan du beslutte, at et brugerdefineret felt ikke længere er nødvendigt. Når dette sker kan en systemadministrator vælge at slette feltet fra siden **Brugerdefinerede felter**. Det gør du ved at sikre, at det rette felt er markeret, klikke på **Slet**, klikke på **Ja** for at bekræfte sletningen og derefter klikke på **Anvend ændringer**.

> [!NOTE]
> Denne handling kan ikke fortrydes, og det vil resultere i, at de data, der er knyttet til feltet, slettes permanent fra databasen.

## <a name="appendix"></a>Appendiks

### <a name="who-can-create-custom-fields"></a>Hvem kan oprette brugerdefinerede felter?

Som en sikring af systemet er det kun systemadministratorer, der som standard kan oprette brugerdefinerede felter. Men de superbrugere, som organisationen finder det nødvendigt, kan gives rettigheder af en systemadministrator til at oprette brugerdefinerede felter ved hjælp af sikkerhedsrollen **Superbruger for tilpasning på kørselstidpunkt**. Brugere uden denne sikkerhedsrolle vil ikke kunne oprette brugerdefinerede felter, men de vil stadig kunne se og anvende brugerdefinerede felter, der er tilføjet af andre brugere i systemet.

### <a name="what-tables-support-custom-fields"></a>Hvilke tabeller understøtte brugerdefinerede felter?

Af ydelsesmæssige og tekniske årsager tillader kun tabeller, der opfylder følgende betingelser, i øjeblikket, at brugerdefinerede felter tilføjes.

- Tabellen skal mærkes som en af disse grupper:

    - Multi
    - WorksheetHeader
    - Hoved
    - Diverse
    - Parameter
    - Reference
    - TransactionHeader

- Tabellen kan ikke udvide en anden tabel.
- Tabellen kan ikke markeres som en systemtabel.
- Tabellen må ikke være en midlertidig tabel.
