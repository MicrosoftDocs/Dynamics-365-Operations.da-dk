---
title: Vedligeholdelsesrunder
description: I dette emne beskrives vedligeholdelsesrunder i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRoundTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a3a64593a2155d35e78b0d854c7367fa65d1c5c8
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018540"
---
# <a name="maintenance-rounds"></a>Vedligeholdelsesrunder

[!include [banner](../../includes/banner.md)]

 

I **Styring af aktiver** kan du oprette vedligeholdelsesrunder for forskellige aktiver, hvor du skal udføre en lignende opgave med jævne mellemrum. Det kan f.eks. være smøreopgaver eller sikkerhedsinspektioner, der skal udføres på en række maskiner inden for de samme intervaller. Første trin er at oprette en vedligeholdelsesrunde, herunder aktiver, der kræver samme type vedligeholdelsesjob. Derefter skal du planlægge vedligeholdelsesrunderne. Når du har fuldført tidsplanen for vedligeholdelsesrunderne, kan du se alle de jobposter, der vedrører runden i **Alle vedligeholdelsestidsplaner** og **Åbne vedligeholdelsestidsplanslinjer**.

>[!NOTE]
>Vedligeholdelsesrunder kan også konfigureres på arbejdssteder og fuldføres på de aktiver, der er installeret på arbejdsstedet på tidspunktet for oprettelsen af den rundebaserede arbejdsordre. Se under [Oprette arbejdssteder](../functional-locations/create-functional-locations.md) for at få yderligere oplysninger om konfiguration af vedligeholdelsesrunder på arbejdssteder.

## <a name="set-up-a-maintenance-round"></a>Opsætning af vedligeholdelsesrunde

1. Klik på **Styring af aktiver** > **Opsætning** > **Forebyggende vedligeholdelse** > **Vedligeholdelsesrunder**.

2. Klik på **Ny** for at oprette en ny vedligeholdelsesrunde.

3. Indsæt et id i feltet **Vedligeholdelsesrunde** og et navn til vedligeholdelsesrunden i feltet **Navn**.

4. Vælg en startdato for runden i feltet **Startdato**.

5. I felterne **Afslut inden for dage** og **Afslut inden for timer** kan du indsætte den forventede slutdato i dage eller timer. Den forventede slutdato beregnes i forhold til den startdato, som beregnes, når der oprettes vedligeholdelsestidsplanlinjer. Du kan f.eks. indsætte "7" i feltet **Afslut inden for dage** for at angive, at det relaterede job skal fuldføres inden for en uge fra startdatoen.

6. Vælg "Ja" på til/fra-knappen **Automatisk oprettelse**, hvis der automatisk skal oprettes arbejdsordrer fra de vedligeholdelsestidsplanlinjer, der oprettes ud fra denne vedligeholdelsesrunde.

7. Vælg i feltet **Arbejdsordretype**, den arbejdsordretype, der skal bruges på arbejdsordrer, der er oprettes ud fra denne vedligeholdelsesrunde.

8. I feltet **Serviceniveau** skal du vælge det serviceniveau for arbejdsordren, der skal bruges på arbejdsordrer, der er oprettes ud fra denne vedligeholdelsesrunde.

9. I oversigtspanelet **Aktivlinjer** skal du klikke på **Tilføj** for at føje et aktiv til vedligeholdelsesrunden.

10. Et linjenummer indsættes automatisk i feltet **Linjenummer** for at angive rækkefølgen for aktiverne i vedligeholdelsesrunden.

11. Vælg aktivet i feltet **Aktiv**.

12. Vælg vedligeholdelsesjobtypen for aktivet i feltet **Vedligeholdelsesjobtype**.

13. Vælg om nødvendigt **Variant af vedligeholdelsesjobtype** og **Fag**, der har relation til typen af vedligeholdelsesjobbet.

14. Vælg gentagelse (dag, uge osv.) i feltet **Periodetype**.

15. Indsæt antallet af gentagelser for vedligeholdelsesrunden i feltet **Periodefrekvens**. Eksempel: Hvis du har valgt "Dag" i feltet **Periodetype**, og du indsætter tallet "7" i dette felt, oprettes der nye vedligeholdelsesrundelinjer under forebyggende vedligeholdelsesplanlægning en gang om ugen.

16. Vælg en startdato for det aktiv, der skal inkluderes i vedligeholdelsesrunden i feltet **Startdato**. Denne dato kan være en anden end den startdato, der er angivet i vedligeholdelsesrunden.

17. Gentag trin 9-16, hvis du vil føje flere aktiver til vedligeholdelsesrunden.

18. I oversigtspanelet **Arbejdsstedslinjer** skal du klikke på **Tilføj** for at føje et arbejdssted til vedligeholdelsesrunden. Se beskrivelsen af de relaterede felter ovenfor. De samme felter er tilgængelige som ved oprettelse af en aktivlinje, men du kan også vælge **Producent** og **Model** til et arbejdssted, hvis det er nødvendigt. Hvis du kun vælger et arbejdssted på en linje, men ikke vælger **Aktivtype**, **Producent** **Model** **Vedligeholdelsesjobtype**, **Variant af vedligeholdelsesjobtype** og **Fag**, bliver alle de aktiver, der er relateret til det pågældende arbejdssted på tidspunktet for vedligeholdelsesplanlægningen, medtaget i vedligeholdelsesrunden.

19. I oversigtspanelet **Puljer** skal du klikke på **Tilføj** for at vælge en arbejdsordrepulje, der skal inkluderes i vedligeholdelsesrunden. Der kan knyttes flere ordrepuljer til en vedligeholdelsesrunde.

20. Gem din opsætning.

>[!NOTE]
>Felterne **Aktiver** og **Linjer**, der findes i gruppen **Detaljer** i oversigtspanelet **Hoved**, viser det samlede antal aktiver og linjer, der er relateret til den valgte vedligeholdelsesrunde.

Illustrationen nedenfor viser et eksempel på en vedligeholdelsesrunde, der indeholder tre aktiver.

![Figur 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a>Planlæg vedligeholdelsesrunder

Når du har konfigureret en vedligeholdelsesrunde, skal du køre et tidsplanlægningsjob for at planlægge alle job, der er relateret til vedligeholdelsesrunden.

1. Klik på **Styring af aktiver** > **Periodisk** > **Forebyggende vedligeholdelse** > **Planlæg vedligeholdelsesrunder** eller **Styring af aktiver** > **Almindeligt** > **Vedligeholdelsestidsplan** > **Alle vedligeholdelsestidsplaner** eller på **Åbne vedligeholdelsestidsplanslinjer** eller **Åbne vedligeholdelsestidsplanspuljer** > vælg vedligeholdelsestidsplanslinje på listen > knappen **Vedligeholdelsesrunder**.

2. Vælg den periodetype, der skal bruges til planlægningsjobbet, i feltet **Periode**.

3. Indsæt det antal perioder, der skal medtages i Planlægningsjobbet, i feltet **Periodefrekvens**. Startdatoen for planlægningen er dags dato.

4. Vælg "ja" på knappen **Automatisk oprettelse**, hvis der automatisk skal oprettes en arbejdsordre ud fra en vedligeholdelsesrunde.

>[!NOTE]
>Hvis denne til/fra-knap er indstillet til "ja", og til/fra-knappen **Automatisk oprettelse** også er indstillet til "ja" i vedligeholdelsesrunden i formularen **Vedligeholdelsesrunder**, oprettes arbejdsordrer baseret på vedligeholdelsesrundelinjerne, og der oprettes også vedligeholdelsestidsplanslinjer med status "Oprettet af arbejdsordre ". Hvis kun en af de til/fra-knapper til **Automatisk oprettelse** er indstillet til "ja" i denne rulleliste eller i **Vedligeholdelsesrunder**, oprettes kun vedligeholdelsestidsplanslinjer med status "Oprettet". Hvis det er tilfældet, oprettes der ingen arbejdsordrer.

5. Hvis det er nødvendigt, kan du vælge bestemte runder eller en anden startdato for planlægningsjobbet. Klik på **Filter**, og tilføj de runder, der skal medtages.

6. Klik på **OK**.

7. Du kan nu se vedligeholdelsesrundejob i **Styring af aktiver** > **Almindeligt** > **Vedligeholdelsestidsplan** > **Alle vedligeholdelsestidsplaner** eller **Åbne vedligeholdelsestidsplanslinjer**. Hvis de planlagte runder er forbundet til en arbejdsordrepulje, kan du også se vedligeholdelsestidsplanslinjer i **Åbne vedligeholdelsestidsplanspuljer**. Vedligeholdelsestidsplanslinjer, der er oprettet ud fra en runde, har referencetypen "Vedligeholdelsesrunder".

De to illustrationer nedenfor viser et planlægningsjob i dialogboksen **Planlæg vedligeholdelsesrunder** og vedligeholdelsestidsplanslinjer, der er oprettet i **Hele vedligeholdelsestidsplanen** baseret på det pågældende planlægningsjob.

![Figur 2](media/14-preventive-maintenance.png)

![Figur 3](media/15-preventive-maintenance.png)

- Når der oprettes arbejdsordrer manuelt for aktiver, der er dækket af en leverandørgaranti, vises der en dialogboks for at gøre brugeren opmærksom på garantien. Oprettelsen af arbejdsordren kan derefter annulleres. Kontrollen af en garantirelation udelades for arbejdsordrer, der oprettes automatisk.  
- Du kan oprette et batchjob i oversigtspanelet **Kør i baggrunden** for at planlægge runder med jævne mellemrum.  
- Hvis en runde er medtaget i flere arbejdsordrepuljer (referer til [Arbejdsordrepuljer](../work-orders/work-order-pools.md)), vises der én post for hver pulje i **Åbne vedligeholdelsestidsplanspuljer**. Dette gøres for at optimere filtreringsindstillingerne for arbejdsordrepuljer.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]