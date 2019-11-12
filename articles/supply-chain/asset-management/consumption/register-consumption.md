---
title: Registrere forbrug
description: Dette emne forklarer, hvordan du registrerer forbrug i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 43f14a1cbd016335b857fdff1147740b27d5c765
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653317"
---
# <a name="register-consumption"></a>Registrere forbrug

[!include [banner](../../includes/banner.md)]

 

Når et vedligeholdelsesjob er fuldført i en arbejdsordre, er det næste trin at foretage registrering af forbrug og bogføre kladderne. Du kan foretage registreringer på følgende forbrugstyper: timer, varer og udgifter. De forskellige typer af forbrug registreres og bogføres på siden **Arbejdsordrekladder**. Kladdeopsætningen i **Styring af aktiver** bruges til at oprette og bogføre separate kladder for timer, varer og udgifter i modulet **Projektstyring og regnskab**.

Du kan muligvis tilføje eller slette prognoselinjer på en arbejdsordre i visse tilfælde. Opsætningen af en livscyklustilstand for en arbejdsordre, den relaterede projekttype og stadiereglerne for projekttypen bestemmer, om du kan tilføje eller redigere kladdelinjer. Læs mere om livscyklustilstande for produktionsordrer og relaterede projektstadier i [Integration med projektstyring og regnskab](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

>[!NOTE]
>Det er muligt at konfigurere automatisk bogføring af kladder på en livscyklustilstand for en arbejdsordre. Du kan finde flere oplysninger i [Livscyklustilstande for arbejdsordrer](../setup-for-work-orders/work-order-lifecycle-states.md).

1. Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg arbejdsordren, og klik på **Kladder**.

3. Klik på **Kopiér fra prognose** for at overføre eventuelle prognoselinjer, der er knyttet til arbejdsordren. Du kan vælge, hvilke forbrugstyper du vil overføre.

4. Hvis det er nødvendigt, kan du tilføje flere forbrugslinjer i det relevante oversigtspanel ved at klikke på **Tilføj linje** og angive data på linjen.

5. Klik på **Valider kladder** for at validere kladdelinjerne inden bogføringen.

6. Klik på **Bogfør kladder** for at bogføre kladdelinjerne.

7. Når du har bogført forbrugskladderne, kan du opdatere livscyklustilstanden for arbejdsordren. Hvis du f.eks. vil angive, at arbejdsordren er fuldført, kan du opdatere livscyklustilstanden til "Afsluttet".

    - I feltet **Vis** øverst på siden **Arbejdsordrekladder** skal du vælge, hvilke kladdelinjer du vil have vist: **Alle**, **Ikke bogført** eller **Bogført**. Bogførte kladder er markeret i afkrydsningsfeltet **Bogført**.  
    - Når der oprettes varelinjer i arbejdsordrekladden, overføres produktdimensioner og sporingsdimensioner, der er knyttet til varen, automatisk til kladdelinjen.  

Skærmbilledet nedenfor viser et eksempel på time- og vareregistreringer på en arbejdsordre i **Arbejdsordrekladder**.

![Figur 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a>Opdele timer i arbejdsordrer med flere arbejdsordrejob

Hvis en arbejdsordre indeholder flere arbejdsordrejob, kan du registrere arbejdstimer ved hjælp af funktionen **Opdel timer**. Det betyder, at én timeregistreringslinje kan fordeles jævnt på hvert arbejdsordrejob.

1. Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg arbejdsordren, og klik på **Kladder**.

3. Vælg den timeregistreringslinje, du vil opdele, og klik på **Opdel timer**.

4. Navnet på den arbejder, der er logget på automatisk, vises i feltet **Arbejder** i dialogboksen med **Opdel timer på vedligeholdelsesjob for arbejdsordrer**. Hvis du har brug for det, kan du vælge en anden arbejder.

5. Vælg en kategori til timeregistreringen i feltet **Kategori**.

6. Indsæt det antal arbejdstimer, der skal opdeles, i feltet **Timer**.

    ![Figur 2](media/02-consumption.png)

7. Klik på **OK**.

*Eksempel:* I skærmbilledet nedenfor vises kladdelinjer for en arbejdsordre, der indeholder tre arbejdsordrejob. Den første linje, der indeholder tre arbejdstimer, er opdelt, og der er registreret én arbejdstime for hvert job i en arbejdsordre. Når registreringslinjerne på tre timer er oprettet, bestemmer du, hvad du vil gøre med den oprindelige timeregistreringslinje (den første linje i eksemplet). Du kan beholde den, som den er, eller slette den. 

![Figur 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a>Økonomiske dimensioner for registrering af forbrug

Når du foretager registreringer af forbrug, føjes økonomiske dimensioner, der er relateret til de forskellige registreringstyper, til registreringerne i en bestemt rækkefølge. 

- *Time- og udgiftsregistreringer:* Først tilføjes økonomiske dimensioner fra kladdehovedet, hvis det er relevant. Derefter tilføjes økonomiske dimensioner fra det relaterede arbejdsordreprojekt. Til sidst tilføjes økonomiske dimensioner fra ressourcen (arbejderen).

- *Vareregistreringer:* Først tilføjes økonomiske dimensioner fra kladdehovedet, hvis det er relevant. Derefter tilføjes økonomiske dimensioner fra det relaterede arbejdsordreprojekt. Så tilføjes økonomiske dimensioner fra stedet. Til sidst tilføjes økonomiske dimensioner fra varen.

>[!NOTE]
>For alle tre registreringstyper valideres den økonomiske dimensionskombination, og ugyldige kombinationer står tomme. Dette er standardopsætning i andre Finance and Operations-apps.

