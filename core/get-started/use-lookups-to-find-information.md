---
title: Bruge Opslag til at finde oplysninger
description: "I Microsoft Dynamics 365 for operationer har mange felter opslag, der kan hjælpe dig med nemt at finde den korrekte eller ønskede værdi. Flere forbedringer, der er føjet til opslag, der foretager kontrollen mere brugbare og gøre brugerne mere produktive. I dette emne, du vil lære om disse nye funktioner til opslag og får nogle nyttige tip til at få en optimal udnyttelse af opslag i systemet."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 6a25593632575dcd71fa4a3c9cf5b83c9f8ecd39
ms.lasthandoff: 03/31/2017


---

# <a name="use-lookups-to-find-information"></a>Bruge Opslag til at finde oplysninger

I Microsoft Dynamics 365 for operationer har mange felter opslag, der kan hjælpe dig med nemt at finde den korrekte eller ønskede værdi. Flere forbedringer, der er føjet til opslag, der foretager kontrollen mere brugbare og gøre brugerne mere produktive. I dette emne, du vil lære om disse nye funktioner til opslag og får nogle nyttige tip til at få en optimal udnyttelse af opslag i systemet.  

<a name="responsive-lookups"></a>Svartider opslag
------------------

I tidligere versioner af Dynamics 365 for operationer, når du kommunikerer med en opslagsindstilling, ville en bruger har en eksplicit handling til at åbne den i rullemenuen. Dette er måske ved at skrive en stjerne (\*) i kontrolelementet til at filtrere de opslag, der er baseret på den aktuelle værdi af kontrolelementet, klikke på knappen ned eller ved hjælp af den **Alt**+**pil ned** genvejstast. Opslag-objekter er blevet ændret på følgende måder for bedre at afpasse med web praksis:

-   Opslag rullemenuer åbnes nu automatisk efter en lille pause i at skrive med rullelisten indholdet af menuen filtreres baseret på værdien af kontrolelementet opslag.
    -   Bemærk, at gamle funktionsmåden for automatisk åbning af rullemenuen, når du har skrevet en stjerne (\*) er blevet frarådet.
-   Når rullemenuen opslag er åbnet, sker følgende:
    -   Markøren forbliver i kontrolelementet opslag (i stedet for fokus flytter ind i rullemenuen) så du kan fortsætte med at foretage ændringer i værdien af kontrolelementet. Brugeren kan dog stadig bruge den **pil op** og **pil ned** ændre rækker i den rullemenu, og enter for at markere den aktuelle række i den rullemenu.
    -   Oplysningerne i den rullemenu justeres, når der foretages ændringer i opslag kontrolelementets værdi.

For eksempel overveje et opslagsfelt, der kaldes **by**. 

Når fokus er på de **by**, kan du starte på udkig efter den by, som du ønsker, ved at skrive et par bogstaver, som "col."  Når du holder op med at skrive, åbnes opslaget automatisk, filtreret, så de pågældende byer, der begynder med "kolonne". 

[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png) 

Markøren er placeret på dette tidspunkt stadig i opslagsfeltet. Hvis du fortsætter med at skrive, så værdien er "kolonne", justeres opslag indholdet automatisk for at afspejle den seneste værdi i kontrolelementet. 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

Selvom fokus er stadig i kontrolelementet opslag, kan du også bruge den **pil op** eller **pil ned** til at markere den række, du vil markere. Hvis du trykker på **Enter** den fremhævede række bliver valgt fra opslaget, og kontrolelementets værdi vil blive opdateret. 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>At skrive i mere end id'er
Når du indtaster data, er det kun naturligt for brugere, der forsøger at identificere et objekt, som en debitor eller kreditor, som navnet i stedet for et id, der repræsenterer objektet. I den aktuelle version af Dynamics 365 for operationer tillader mange (men ikke alle) opslag nu kontekstafhængige dataindtastning. Denne effektive funktion tillader brugeren at skrive ID'ET eller tilsvarende navn i kontrolelementet opslag. 

Eksempel på **debitorkonto** når du opretter en salgsordre. Dette felt viser den **konto-ID** for kunden, men brugeren foretrækker normalt at angive en **kontonavn** i stedet for en **konto-ID** for dette felt, når du opretter en salgsordre, som "Skov Wholesales" i stedet for "US-003."

Hvis brugeren er begyndt at indtaste en **konto-ID** i kontrolelementet opslag i rullemenuen åbner automatisk som beskrevet i forrige afsnit, og brugeren kan se opslaget, som vist nedenfor.

[![Kontekstafhængige opslag, når der angives en kunde-ID-konto](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Brugeren kan dog også nu angive begyndelsen af en **navn** også. Hvis det opdages, vil brugeren se følgende opslag. Bemærk hvordan **navn** kolonne flyttes til den første kolonne i opslaget, og hvordan opslaget er sorteret og filtreret, der er baseret på den **navn** kolonne.

[![Kontekstafhængige opslag, når der angives et kundenavn](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Ved hjælp af gitteret kolonneoverskrifter for mere avanceret filtrering og sortering
De opslag forbedringer, der er beskrevet i de foregående to afsnit væsentligt forbedre en brugers mulighed for at navigere mellem rækkerne i et opslag, der er baseret på søgning "starter med" i den **ID** eller **navn** i opslaget. Der er dog situationer, hvor mere avanceret filtrering (eller sortering) bruges til at finde den rigtige række. I disse situationer skal brugeren bruge indstillinger for filtrering og sortering i gitteret kolonneoverskrifterne i opslaget. For eksempel overveje en medarbejder, der angiver en salgsordrelinje, og som skal finde højre "kabel" som produktet. At skrive "kabel" i den **varenummer** kontrol ikke er nyttige, da der ikke er nogen produktnavne, der begynder med "kabel". 

![emptyitemlookup](./media/emptyitemlookup.png) 

Brugeren skal i stedet at rydde værdien i kontrolelementet opslag, åbne rullemenuen opslag og filtrere den rullemenu med gitter i kolonneoverskriften, som vist nedenfor. En mus (eller tryk) bruger kan blot klikke (eller røre) en kolonneoverskrift for at få adgang til de filtrerings- og sorteringsindstillinger for den pågældende kolonne. Bruger et tastatur, skal brugeren blot at trykke på **Alt**+**ned****pil** endnu en gang til at flytte fokus i rullemenuen, hvorefter brugeren kan fanen til den korrekte kolonne, og tryk derefter på **Ctrl**+**G** at åbne menuen gitter kolonne hovedet ned. 

[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png) 

Når filteret er anvendt (se billedet nedenfor), kan brugeren finde og markere den række, som du plejer. 

![filtereditemlookup](./media/filtereditemlookup.png)


