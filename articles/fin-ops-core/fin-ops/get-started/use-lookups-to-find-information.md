---
title: Finde oplysninger ved hjælp af opslag
description: Mange felter har opslag, der kan hjælpe dig med nemt at finde den korrekte eller ønskede værdi. Der er føjet flere forbedringer til opslag, der gør disse kontrolelementer mere brugbare og gør brugerne mere produktive. I dette emne får du mere at vide om disse nye opslagsfunktioner og får nogle nyttige tip til at få en optimal udnyttelse af opslag i systemet.
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d75e66e8fb9f1a227c9dd15f92ca5db433c0db4a
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798136"
---
# <a name="find-information-by-using-lookups"></a>Finde oplysninger ved hjælp af opslag

[!include [banner](../includes/banner.md)]

Mange felter har opslag, der kan hjælpe dig med nemt at finde den korrekte eller ønskede værdi. Der er føjet flere forbedringer til opslag, der gør disse kontrolelementer mere brugbare og gør brugerne mere produktive. I dette emne får du mere at vide om disse nye opslagsfunktioner og får nogle nyttige tip til at få en optimal udnyttelse af opslag i systemet.

## <a name="responsive-lookups"></a>Responsive opslag

I tidligere versioner skulle en bruger foretage en eksplicit handling for at åbne rullemenuen, når der blev kommunikeret med et opslagskontrolelement. Dette skete måske ved at skrive en stjerne (\*) i kontrolelementet for at filtrere opslaget baseret på den aktuelle værdi af kontrolelementet, ved at klikke på rullelisten eller ved hjælp af genvejstasten **Alt**+**pil ned**. Opslagskontrolelementer er blevet ændret på følgende måder for bedre at passe med webpraksis:

- Opslagsrullemenuer åbnes nu automatisk efter en lille pause i indtastningen, og rullelisteindholdet filtreres på basis af værdien af opslagskontrolelementet.

    Bemærk, at den gamle funktionsmåde med automatisk åbning af rullemenuen, når du har skrevet en stjerne (\*), er blevet frarådet.

- Når opslagsrullemenuen er åbnet, sker følgende:

    - Markøren forbliver i opslagskontrolelementet (i stedet for at fokus flytter ind i rullemenuen), så du kan fortsætte med at foretage ændringer i værdien af kontrolelementet. Brugeren kan dog stadig bruge **pil op** og **pil ned** til at ændre rækker i rullemenuen, og Enter til at markere den aktuelle række i rullemenuen.
    - Indholdet i rullemenuen justeres, når der foretages ændringer i opslagskontrolelementets værdi.

Se f.eks. på et opslagsfelt kaldet **By**.

Når fokus er på feltet **By**, kan du starte med at søge efter den ønskede by ved at skrive et par bogstaver, f.eks. "kol." Når du holder op med at skrive, åbnes opslaget automatisk og er filtreret efter de byer, der begynder med "kol".

[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)

På dette tidspunkt er markøren stadig placeret i opslagsfeltet. Hvis du fortsætter med at skrive, så værdien er "kolonne", justeres opslag indholdet automatisk for at afspejle den seneste værdi i kontrolelementet.

![updateFilterLookupExample](./media/updatefilterlookupexample.png)

Selvom fokus er stadig i opslagskontrolelementet, kan du også bruge tasterne **pil op** eller **pil ned** til at markere den række, du vil vælge. Hvis du trykker på **Enter**, vælges den fremhævede række fra opslaget, og kontrolelementets værdi vil blive opdateret.

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Indtastning af mere end id'er

Når de indtaster data, er det naturligt for brugerne at forsøge at identificere et objekt, som en debitor eller kreditor, ved hjælp navnet i stedet for en identifikator, der repræsenterer objektet. Mange (men ikke alle) opslag giver nu mulighed for kontekstbetinget dataindtastning. Denne effektive funktion tillader brugeren at skrive id'et eller det tilsvarende navn i opslagskontrolelementet.

Tænk f.eks. på feltet **Debitorkonto**, når du opretter en salgsordre. Dette felt viser **konto-id'et** for kunden, men brugerne foretrækker normalt at angive et **kontonavn** i stedet for et **konto-id** for dette felt, når de opretter en salgsordre, f.eks. "Forest Wholesales" i stedet for "US-003".

Hvis brugeren er begyndt at indtaste et **konto-ID** i opslagskontrolelementet, åbnes rullemenuen automatisk som beskrevet i forrige afsnit, og brugeren kan se opslaget, som vist nedenfor.

[![Kontekstafhængigt opslag, når der angives et konto-id](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Brugeren kan dog også nu angive begyndelsen af et **kontonavn**. Hvis det registreres, ser brugeren følgende opslag. Bemærk hvordan kolonnen **Navn** flyttes til den første kolonne i opslaget, og hvordan opslaget er sorteret og filtreret på basis af kolonnen **Navn**.

[![Kontekstafhængigt opslag, når der angives et kundenavn](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Brug af gitterets kolonneoverskrifter til mere avanceret filtrering og sortering

De opslagsforbedringer, der er beskrevet i de foregående to afsnit giver en væsentligt forbedring af en brugers mulighed for at navigere mellem rækkerne i et opslag, der er baseret på en "starter med"-søgning i felterne **Id** eller **Navn** i opslaget. Der er dog situationer, hvor der er behov for mere avanceret filtrering (eller sortering) for at finde den rigtige række. I disse situationer skal brugeren bruge indstillinger for filtrering og sortering i gitterets kolonneoverskrifter i opslaget. F.eks. angiver en medarbejder en salgsordrelinje og har behov for at finde det rigtige "kabel". Det hjælper ikke at skrive "kabel" i kontrolelementet **Varenummer**, da der ikke er nogen produktnavne, der begynder med "kabel".

![emptyitemlookup](./media/emptyitemlookup.png)

Brugeren skal i stedet at rydde værdien i opslagskontrolelementet, åbne opslagsrullemenuen og filtrere rullemenuen ved hjælp af gitterets kolonneoverskrift, som vist nedenfor. En bruger, der anvender mus (eller tryk), kan blot klikke (eller trykke) på en kolonneoverskrift for at få adgang til filtrerings- og sorteringsindstillingerne for den pågældende kolonne. Når der bruges tastatur, skal brugeren blot at trykke på **Alt**+**Pil** **ned** endnu en gang for at flytte fokus ind i rullemenuen, hvorefter brugeren kan tabulere til den korrekte kolonne og derefter trykke på **Ctrl**+**G** for at åbne rullemenuen for gitterets kolonnehoved.

[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)

Når filteret er anvendt (se billedet nedenfor), kan brugeren som normalt finde og markere rækken.

![filtereditemlookup](./media/filtereditemlookup.png)
