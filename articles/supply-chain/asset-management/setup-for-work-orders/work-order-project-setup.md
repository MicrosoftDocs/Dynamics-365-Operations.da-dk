---
title: Opsætning af arbejdsordreprojekt
description: I dette emne beskrives projektopsætning for arbejdsordrer i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjectSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 031e61549474745360ac00f9a66bef7a9dbaaf96
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021548"
---
# <a name="work-order-project-setup"></a>Opsætning af arbejdsordreprojekt

[!include [banner](../../includes/banner.md)]

 

I modulet **Styring af aktiver** kræves der en projektrelation for hvert job i en arbejdsordre. I det projekt, der er knyttet til et arbejdsordrejob, har du mulighed for at spore omkostninger for forskellige projekter, der er relateret til Styring af aktiver, f.eks. interne vedligeholdelsesprojekter, servicestyringsprojekter og investeringsprojekter. 

## <a name="project-setup-for-a-work-order-job"></a>Projektopsætning for et arbejdsordrejob

Når du opretter et arbejdsordrejob på en arbejdsordre, bestemmer projektopsætningen i modulet **Projektstyring og regnskab**, og projektopsætningen for arbejdsordren i modulet **Aktivadministration** bestemmer, hvordan projekter kan bruges til omkostningsstyring i det aktiv, der er valgt i arbejdsordrejobbet. I dette afsnit beskrives følgende dele af projektopsætningen, der bruges til en arbejdsordre: det overordnede projekt (projekt-ID), projekttype, projektaktiviteter og økonomiske dimensioner:

- Når du opretter et arbejdsordrejob i en arbejdsordre, oprettes der automatisk et entydigt projekt-id og en relateret projektaktivitet for det. Men hvis flere job i en arbejdsordre indeholder det samme aktiv, bruges det samme projekt-id til dem. Det vil sige, at der oprettes ét projekt-ud for hvert aktiv i en arbejdsordre.

    - Det overordnede projekt (projekt-id) for et arbejdsordrejob findes i opsætningen af det overordnede projekt. (Yderligere oplysninger om opsætning af det overordnede projekt finder du i næste afsnit). Hvis du f.eks. knytter en kunde eller et arbejdssted til et bestemt overordnet projekt, bruges det overordnede projekt, hver gang du opretter arbejdsordrer for den pågældende kunde eller arbejdsstedet. Hvis du ikke kan tilknytte et bestemt projekt-id, f.eks. et arbejdssted, bruges det næste relevante overordnede projekt i opsætningen af arbejdsordreprojektet.
    - Der kræves en projekttype for hvert projekt-id. Projekttypen findes i projektgruppeopsætningen. (Yderligere oplysninger om opsætning af projektgrupper finder du i næste afsnit). Hvis der ikke findes et match i projektgruppeopsætningen, bruges projektgruppeopsætningen for det overordnede projekt.
    - Opsætningen af de krævede projektaktiviteter i budgetter og kladder, kopieres fra det overordnede projekt til arbejdsordreprojektet. Hvis der er valgt **ja** i indstillingerne **Time**, **Udgift** og **Vare** for det projekt, der bruges som et overordnet projekt, er det obligatorisk med en projektaktivitet i budgetter og kladder. (Du kan få adgang til disse indstillinger ved at vælge **Projektstyring og regnskab** \> **Projekter** \> **Alle projekter** og derefter vælge det projekt, der bruges som et overordnet projekt. Indstillingerne findes i sektionen **Gør aktivitet obligatorisk i kladder** i oversigtspanelet **Opsætning**).

- Økonomiske dimensioner kopieres fra aktivet og flettes sammen med det overordnede projekt.

I næste afsnit forklares, hvordan du kan konfigurere overordnede projekter og projektgrupper. Overordnede projekter og overordnede grupper bruges til at styre arbejdsordrer. De bruges også til rapportering af arbejdsordrer.

## <a name="set-up-work-order-projects"></a>Konfigurere arbejdsordreprojekter

Før du begynder at oprette arbejdsordrer, skal du konfigurere arbejdsordreprojekter. Siden **Opsætning af arbejdsordre projekt** (**Styring af aktiver** \> **Opsætning** \> **Arbejdsordrer** \> **Opsætning af projekt**) indeholder to faner: **Overordnet projekt** og **Projektgruppe**.

Under fanen **Overordnet projekt** kan du konfigurere projektrelationer, der kan bruges, hvis der ikke er konfigureret et projekt på det anlægsaktiv, der er valgt i arbejdsordrejobbet. Det er ikke nødvendigt at konfigurere en overordnet projektopsætning, hvis dit firma bruger aktivprojekter. Det er kun relevant, hvis du vil bruge arbejdsordreprojekter i stedet for aktivprojekter. Hvis du vil det, skal du oprette mindst ét overordnet projekt.

Under fanen **Projektgruppe** kan du konfigurere projektgrupper, der kan knyttes til typer af arbejdsordrer, aktivtyper og aktiver.

Projektgrupper kan bruges til at oprette specifikke kategorier (grupper), der bruges til omkostningsstyring. Hvis du f.eks. opretter projektgrupper for bestemte aktivtyper eller typer af arbejdsordrer, kan du foretage detaljeret sporing af vedligeholdelsesomkostninger efter type.

Projektgrupper er ikke obligatoriske. Hvis du ikke konfigurerer projektgrupper, bruges det overordnede projekt til at bestemme projektgruppen, og der oprettes et underordnet projekt ud fra det overordnede projekts projektgruppe.

Opsætningen giver fuldstændig integration med modulet **Projektstyring og regnskab**. Du kan derfor spore de omkostninger, der er relateret til arbejdsordrer i de relaterede projekter. Følgende procedure beskriver opsætningen af arbejdsordreprojekter.

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Arbejdsordrer** \> **Opsætning af projekt**.
2. Vælg **Tilføj** under fanen **Overordnet projekt**.
3. Vælg de ønskede værdier i felterne **Arbejdsordretype**, **Arbejdssted**, **Aktivtype** og **Aktiv**. For hver linje, du tilføjer, kan du angive ét eller flere felter. Det antal felter, du angiver, bestemmer den kombination, der bruges, når der vælges et projekt-id i Styring af aktiver. 

    Hvis du vælger et arbejdssted, medtages de tilhørende underordnede placeringer automatisk. Hvis du vælger et aktiv, kan du oprette flere linjer til projektopsætning af arbejdsordrer for det samme aktiv, men du kan vælge forskellige projekter for det pågældende aktiv.

4. I feltet **Projekt-id** skal du vælge det projekt, der skal relateres til den opsætning, du oprettede i trin 3.
5. Hvis projektopsætningen kun skal være gyldig i en begrænset periode, skal du vælge en slutdato i feltet **Slutdato**. Ellers skal du vælge **Ingen**.

    Startdatoen er som standard den dato, hvor du føjer arbejdsordreprojektet til siden. Den styres af feltet **Gyldig fra**, der som standard er skjult. Hvis du vil have vist feltet **Gyldig fra**, skal du vælge **Vis** \> **Alle**. Du kan derefter bruge feltet **Gyldig fra** sammen med feltet **Slutdato** til at angive en begrænset gyldighedsperiode for arbejdsordreprojektet.

    ![Siden Opsætning af arbejdsordreprojekt](media/17-setup-for-work-orders.png)

6. Vælg **Tilføj** under fanen **Projektgruppe**.
7. I feltet **Arbejdsordretype** skal du vælge en arbejdsordretype.
8. Hvis du ønsker, at tilknytningen til projektgruppen skal være mere specifik, skal du vælge en aktivtype i feltet **Aktivtype** eller et aktiv i feltet **Aktiv**.
9. Vælg den projektgruppe, der skal knyttes til arbejdsordretypen, i feltet **Projektgruppe**. En arbejdsordretype med navnet **Forebyggende vedligeholdelse** kan f.eks. knyttes til en projektgruppe med navnet **Foreb. vedl.** eller **Intern**. Alternativt kan der knyttes en **Investering**-arbejdsordretype, der bruges til arbejdsordrer, som er relateret til investeringer og anlægsaktiver, til en projektgruppe med navnet **Invester** eller **Investering**.
10. Vælg **Gem**.

![Siden Opsætning af arbejdsordreprojekt, Tilføj arbejdsordre](media/18-setup-for-work-orders.png)

> [!NOTE]
> Hver gang der oprettes en linje i en arbejdsordre, søger Styring af aktiver efter en projektgruppe, der skal relateres til arbejdsordrejobprojektet. Søgningen er baseret på den opsætning, der er beskrevet i dette emne. Hver projektgruppe har en relateret projekttype. Projektgrupper, der har projekttypen **Tid og materiale** eller **Fastpris**, er kun gyldige for aktiver, der er relateret til en debitorkonto.
>
> For overordnede projekter og projektgrupper, når systemet vælger det projekt eller den projektgruppe, der er tilgængeligt for arbejdsordren, baseres valget på de poster, du oprettede ved hjælp af den foregående procedure. Styring af aktiver gennemgår poster, der er relateret til arbejdsordreprojektet, for at finde et muligt match. Den kontrollerer altid den mest specifikke kombination først. Med andre ord for arbejdsordrens overordnede projekt kontrollerer Styring af aktiver først, om der er et muligt match for feltet **Arbejdsordretype**. Hvis der ikke findes et match, kontrolleres det, om der er et match for feltet **Aktivtype**. Hvis der ikke findes et match, kontrolleres det, om der er et match for feltet **Arbejdssted** osv. Som du kan se i layoutet for siden **Opsætning af arbejdsordreprojekt**, betyder denne adfærd, at Styring af aktiver kontrollerer hver enkelt post fra højre mod venstre for et match for at finde den mest specifikke kombination. Hvis der ikke findes et match, bruges standardposten, hvor der kun er valgt et projekt-id. Den relaterede projektgruppe findes på tilsvarende måde. Styring af aktiver kontrollerer først, om der er et muligt match i feltet **Aktiv**, derefter i feltet **Aktivtype** og derefter i feltet **Arbejdsordretype**. Hvis der ikke findes et match, bruges standardposten, hvor der kun er valgt projektgruppe.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]