---
title: Redigere og overvåge cash and carry-transaktioner og kassestyringstransaktioner
description: Dette emne beskriver, hvordan du redigerer og overvåger cash and carry-transaktioner og kassestyringstransaktioner i Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 15d23bfd591558e7330a273065429256c2e17d64
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/04/2020
ms.locfileid: "4458727"
---
# <a name="edit-and-audit-cash-and-carry-and-cash-management-transactions"></a>Redigere og overvåge cash and carry-transaktioner og kassestyringstransaktioner

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du redigerer og overvåger cash and carry-transaktioner og kassestyringstransaktioner i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Dynamics 365 Commerce-kunder bruger både en førsteparts-POS-applikation og tredjeparts-POS-applikationer. I forbindelse med førsteparts-POS-applikationen trækkes butikstransaktioner ind i hovedkontoret Commerce fra kanalerne via en batchproces. I forbindelse med tredjepartsapplikationer trækkes transaktionerne ind i hovedkontoret Commerce via integration. I begge tilfælde skal der udføres en konsistenskontrolproces, når der trækkes transaktioner ind i hovedkontoret Commerce. Denne proces kører flere valideringer af transaktionerne, og kun de transaktioner, der er valideret korrekt, trækkes ind i opgørelsen, så de kan bogføres i hovedkontoret Commerce.

Commerce-transaktioner valideres muligvis ikke korrekt af forskellige årsager. En fejl i integrationskoden eller i POS-applikationen kan medføre inkonsistente data. Alternativt kan en brugerfejl forårsage inkonsekvente data. F.eks. hvis en bruger sletter et produkt, når det er synkroniseret med kanalen, eller hvis en bruger lukker en regnskabsperiode uden at bogføre transaktioner for den pågældende periode. Selvom disse transaktioner markeres og udelukkes fra opgørelserne, kan de forstyrre en kundes daglige proces med at bogføre dagligt salg i finans. I Commerce kan du redigere de transaktioner, der ikke er valideret korrekt, samtidig med at du også bevarer overvågningen af alle ændringerne.

## <a name="edit-transactions"></a>Redigere transaktioner

I Commerce-version 10.0.5 er det kun cash and carry-transaktioner, der kan redigeres, f.eks. salg og returneringer. Kundeordrer og onlineordrer kan ikke redigeres. I Commerce-version 10.0.6 og senere kan kassestyringstransaktioner også redigeres.

Hvis du vil redigere transaktioner i hovedkontoret Commerce, skal du følge disse trin.

1. Installér [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Åbn arbejdsområdet **Butiksregnskab** i hovedkontoret Commerce. Feltet **Transaktionsvalideringsfejl** giver en forhåndsfiltreret visning af den transaktionsside, hvor der opstod fejl ved én eller flere valideringsregler.
1. Åbn transaktionssiden, vælg den post, der ikke blev valideret korrekt, vælg **Office-tilføjelsesprogram**, og vælg derefter **Rediger den valgte transaktion**. En Excel-fil, der viser oplysningerne om den valgte transaktion, åbnes. Denne fil indeholder følgende regneark:

    - **Linjer** – dette regneark indeholder hoved- og produktlinjerne for transaktionen og relaterede data for transaktionen.
    - **Betalinger** – dette regneark indeholder oplysningerne om transaktionens betalingslinjer.
    - **Rabatter** – dette regneark indeholder de rabatrelaterede detaljer for transaktionen.
    - **Moms** – dette regneark indeholder de momsrelaterede detaljer for transaktionen.
    - **Gebyrer** – dette regneark indeholder de gebyrrelaterede data for transaktionen.

1. I Excel-filen redigerer du de relevante felter og overfører derefter dataene tilbage til hovedkontoret Commerce ved hjælp af publiceringsfunktionen i Dynamics Excel-tilføjelsesprogrammet. Når dataene er publiceret, afspejles ændringerne i systemet. Under publiceringen sker der ingen validering for de ændringer, brugerne foretager.
1. Du kan få vist et komplet revisionsspor for ændringerne ved at vælge **Vis revisionsspor** i hovedet på **detailtransaktionen** for ændringerne på hovedniveau og i den relevante sektion og post på den relevante transaktionsside. Alle ændringer, der f.eks. er relateret til salgslinjer, vises på siden **Salgstransaktioner**, og alle ændringer, der er relateret til betalinger, vises på siden **Betalingstransaktioner**. Følgende revisionsoplysninger bevares for ændringerne:

    - Dato og klokkeslæt for ændring
    - Felt
    - Gammel værdi
    - Ny værdi
    - Ændret af

1. Når du har foretaget og publiceret dine ændringer, skal du køre **Valider butikstransaktioner** for at validere, at disse ændringer er konsistente og gyldige.

> [!NOTE]
> Du kan kun redigere transaktioner, hvor valideringen mislykkedes. Hvis du vil redigere en transaktion, der har bestået valideringen, skal du ændre valideringsstatus for transaktionen til **Fejl** eller **Ingen** og derefter publicere ændringen. Du kan derefter redigere dataene i overskriften eller i andre underordnede poster for transaktionen og publicere overskriften eller posterne.

## <a name="bulk-edit-transactions-that-are-linked-to-a-statement"></a>Masseredigering af transaktioner, der er knyttet til en opgørelse

Commerce-version 10.0.6 og nyere understøtter muligheden for at masseredigere transaktioner på opgørelsesniveau.

Hvis du vil masseredigere transaktioner, der er knyttet til en opgørelse i hovedkontoret Commerce, skal du følge disse trin.

1. Åbn siden **Opgørelser**, og vælg den opgørelse, der indeholder de transaktioner, der skal redigeres.
1. Vælg knappen **Åbn i Microsoft Office**.
1. Vælg en af følgende indstillinger, alt efter hvad der skal redigeres:

    - **Rediger cash and carry-transaktioner** – med denne indstilling kan du redigere alle de cash and carry-transaktioner, der er medtaget i opgørelsen. Følgende Excel-regneark er tilgængelige:

        - **Transaktion** – dette regneark indeholder alle oplysningerne på hovedniveau for salgstransaktionerne.
        - **Salgstransaktion** – dette regneark indeholder alle oplysningerne på linjeniveau for salgstransaktionerne.
        - **Betalingstransaktioner** – dette regneark indeholder alle betalingslinjeoplysningerne for salgstransaktionerne.
        - **Rabattransaktioner** – dette regneark indeholder alle rabatlinjeoplysningerne for salgstransaktionerne.
        - **Momstransaktioner** – dette regneark indeholder alle momsoplysningerne for salgstransaktionerne.
        - **Gebyrtransaktioner** – dette regneark indeholder alle rabatlinjeoplysningerne for salgstransaktionerne.

    - **Rediger kassestyringstransaktioner** – med denne indstilling kan du redigere alle de kassestyringstransaktioner, der er medtaget i opgørelsen. Følgende Excel-regneark er tilgængelige:

        - **Transaktion** – dette regneark indeholder alle oplysningerne på hovedniveau for kassestyringstransaktionerne.
        - **Transaktioner med bankbetalingsmiddel** – dette regneark indeholder alle oplysninger om transaktioner med indsættelse i bank.
        - **Betalingsmiddeltransaktioner lagt i pengeskab** – dette regneark indeholder alle oplysninger om transaktioner med betalingsmidler lagt i pengeskab.
        - **Kasseoptælling** – dette regneark indeholder alle oplysninger om transaktioner med kasseoptælling.
        - **Indtægts-/udgiftstransaktion** – dette regneark indeholder alle oplysninger om indtægts-/udgiftstransaktionslinjer.
        - **Betalingstransaktioner** – dette regneark indeholder alle betalingsrelaterede oplysninger for handlingen **Betal faktura** og indtægts-/udgiftstransaktionen.

1. Rediger de nødvendige transaktioner.

    > [!NOTE]
    > Valideringer udføres ikke, når du publicerer masseredigerede transaktioner. Du skal sikre dig, at alle dine redigeringer er nøjagtige, og at pålideligheden af dataene bevares på tværs af alle regneark. Hvis du f.eks. vil ændre transaktionsdatoen, så du kan administrere de scenarier, hvor regnskabs-eller lagerperioden for de åbne transaktioner er lukket, skal du ændre datoen på alle de Excel-regneark, der indeholder kolonnen **Forretningsdato**. Hvis du vil validere transaktioner, når de er blevet redigeret, kan du vælge **Valider transaktioner igen** på siden **Opgørelser**. Vent, indtil valideringsjobbet er kørt, før du bogfører opgørelsen.

1. Hvis der allerede er oprettet en aggregering, skal du åbne siden **Aggregerede transaktioner** og vælge **Gendan en salgsordre-XML igen**.

## <a name="bulk-edit-transactions-that-arent-linked-to-a-statement"></a>Masseredigering af transaktioner, der ikke er knyttet til en opgørelse

Commerce-version 10.0.10 og nyere understøtter muligheden for masseredigering af transaktioner, der ikke blev valideret korrekt, men ikke er knyttet til en opgørelse.

Hvis du vil masseredigere transaktioner, der ikke er knyttet til en opgørelse i hovedkontoret Commerce, skal du følge disse trin.

1. Åbn siden **Alle butikker**, og vælg den butik, som transaktionerne skal redigeres for.
1. Vælg knappen **Åbn i Microsoft Office**, og vælg derefter **Rediger cash and carry-transaktioner**.
1. Rediger de nødvendige transaktioner, og publicer dem derefter.

## <a name="additional-resources"></a>Yderligere ressourcer

[Redigere og overvåge onlineordre- og asynkrone kundeordretransaktioner](edit-order-trans.md)

[Redigere økonomiske dimensioner for detailtransaktioner](edit-financial-dim.md)

[Oprette en Excel-projektmappe for at redigere detailtransaktioner](create-excel-edit.md)

[Føje felter til en Excel-projektmappe for at redigere detailtransaktioner](add-fields-excel.md)
