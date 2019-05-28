---
title: Formler og formelversioner
description: Dette emne indeholder oplysninger om formler og formelversioner. En formel definerer materialerne, ingredienserne og udfaldet for en bestemt proces i procesproduktion. Formler, der bruges til at planlægge og fremstille produkter i procesproduktion.
author: cvocph
manager: AnnBe
ms.date: 09/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbffc298ff5d2442092f8f0c987b7e79a7934a84
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564849"
---
# <a name="formulas-and-formula-versions"></a>Formler og formelversioner

[!include [banner](../includes/banner.md)]

En formel definerer materialerne, ingredienserne og udfaldet for en bestemt proces i procesproduktion. Sammen med den tilsvarende rute definerer formlen hele processen i procesproduktion. Formler, der bruges til at planlægge og fremstille produkter i procesproduktion.

En formel, der består af de ingredienser og mængder, der er nødvendige for at producere et bestemt antal af en formelvare. Afhængigt af den opgave du udfører, kan du åbne formelfunktionalitet fra lager- og lokationsstyring eller administration af produktoplysninger.

## <a name="formulas-and-formula-lines"></a>Formler og formellinjer
En formel består af en eller flere formellinjer, der er ingredienserne eller varerne, der udgør formlen. En formellinje kan indeholde styklistevarer, formelvarer, fangstvægtvarer, købte varer, samprodukter eller biprodukter. Da mange varer bruges til flere produkter, kan en vare bruges i mere end én formel.

Et eksempel på en formel er formlen for en cookie med chokoladestykker. Til ingredienserne til denne formel bruges flere linjer, f.eks. mel, sukker, æg, smør og chokoladestykker. Formlen for cookien med chokoladestykker indeholder ingredienser, der sandsynligvis bruges i andre formler. Når du fremstiller cookies med chokoladestykker, kan der være rester, f.eks. krummer, eller nogle af cookierne er bagt for meget eller for lidt. Disse elementer kan være oprettet som samprodukter eller biprodukter, afhængigt af produktionsoperationerne.

Når du opretter en formellinje, kan du bruge linjetypen til at angive, hvordan systemet skal håndtere linjen, når du kører varedisponering og producerer batchordrer. Hver linjetype giver et forskelligt resultat. I nedenstående tabel beskrives de linjetyper, du kan vælge. 

| Linjetype     | Betegnelse  |
|---------------|--------------|
| Post          | Vælg **Vare**, når varen er en råvare eller et halvfabrikata, der plukkes fra lager, eller når varen er en service. |
| Fantom       | Vælg **Fantom**, når du vil udfolde alle de lavere formelvareniveauer, der er indeholdt på formellinjer. Når du forkalkulerer batchordren, og formelvarerne nedbrydes, vises de indgående varer som formellinjer på batchordren. Desuden føjes de tilsvarende ruter til produktionsruten. Formelvarer udfoldes ved hjælp af den aktuelle konfiguration. Når du bruger linjetypen **Fantom**, kan du håndtere konfigurationer af produktion og måling, der opstår på forskellige formelniveauer. Hvis du vælger **Fantom** for et produkt på oversigtspanelet **Tekniker** på siden **Frigivne produktdetaljer** og derefter bruger dette produkt i en formel, ændres linjetypen for formellinjen til **Fantom**. Du kan ikke vælge **Fantom** for en fangstvægtvare eller for varer, hvor produktionstypen er **Samprodukt**, **Biprodukt** eller **Planlægningsvare**. |
| Sporet forsyning | Vælg **Sporet forsyning** for at oprette en batchordre, produktionsordre, kanban-ordre, flytteordre eller indkøbsordre for den ingrediens, som findes på formellinjen. Den relaterede ordre bestemmes ud fra standardordreindstillingerne og produktionstypen for ingrediensen, og den oprettes, når du forkalkulerer batchordren. De krævede ingrediensmængder reserveres automatisk til batchordren. |
| Leverandør        | Vælg **Leverandør**, hvis der i produktionsprocessen gøres brug af en underleverandør, og du vil oprette en underproduktion eller en indkøbsordre for underleverandøren. Den service eller det arbejde, der udføres af underleverandøren, skal være oprettet ved brug af en formel eller servicevare. Du kan knytte varen til den overordnede vare som en formellinje. Ruten skal indeholde en operation, der er tildelt underleverandørens operationsressource. Denne operation tilknyttes formellinjen ved hjælp af feltet **Opr.nr.** . |

## <a name="formula-versions"></a>Formelversioner
Når du opretter en nye formel , skal du først oprette en formelversion, før du tilføjer formellinjevarerne med deres specifikke karakteristika. Enhver formel skal findes i mindst en version. Knappen **Godkendt** på en formelversion bliver kun tilgængelig, når en versionspost er blevet gemt. Hver formelversionspost er knyttet til et eller flere samprodukter og biprodukter, der kan produceres, som du fremstiller det færdige produkt. Mange produkter kan fremstilles af de samme ingredienser i forskellige batchstørrelser, i multipla eller ved at bruge forskellige udbytter. Du kan oprette lige så mange versioner af en formel, som du har brug for.

Hvis du vil holde styr på flere aktive formelversioner, kan du bruge gyldighedsdatointervaller eller "fra" antalsfelter. Der kan være flere aktive formelversioner på én gang, men kun hvis datointervallet og "fra"-antallet overlapper.

I modsætning til styklister, hvor én stykliste ofte er knyttet til mange styklisteversioner, findes der typisk kun én formelversion pr. formel. Husk, at kun én formelversion kan aktiveres for disponeringsdimensionerne og antallet for et bestemt produkt. Der kan dog være mange formelversioner af andre årsager, og du kan manuelt vælge dem, når du opretter en batchordre.

## <a name="approve-and-activate-formulas-and-formula-versions"></a>Godkende og aktivere formler og formelversioner
Formler og formelversioner skal godkendes, før de kan bruges til planlægning og produktion. Formler aktiveres normalt, før de kan bruges. Under produktionen kan du dog vælge en formelversion, der er godkendt, men ikke er aktiveret.

For at sikre en formel eller formelversion kan du angive parametrene **Spær redigering** og **Spær fjernelse af godkendelse** på siden **Produktionsstyringsparametre**.

Hvis du vælger **Spær redigering**, og formlen er godkendt, kan ingen felter på formellinjerne slettes eller redigeres. Men hvis du fjerner godkendelsen af formlen, kan du slette og redigere formellinjerne. Du kan også oprette nye formler og nye formelversioner.

Hvis du vælger **Spær fjernelse af godkendelse**, kan du ikke fjerne godkendelsen af en godkendt formel eller formelversion. Men du kan oprette nye formler og nye formelversioner, og du kan fjerne aktivering af formelversionen.

Du kan tilføje flere kontrolniveauer ved hjælp af elektronisk signatur. Når en bruger er konfigureret, så der kræves en elektronisk signatur på tidspunktet for godkendelsen af formlen, vises siden **Signatur**, når formlen aktiveres. Brugeren skal have tilladelse til at signere elektronisk, og certifikatet skal være valideret, før ændringen kan træde i kraft. Hvis signaturen ikke kan godkendes, bliver godkendelsen eller annulleringen af godkendelse afslået, og den ændring, der forårsagede godkendelsen eller annulleringen af godkendelse, returneres til sin oprindelige tilstand.

## <a name="use-the-scalable-feature"></a>Brug funktionen Skalerbar
Funktionen Skalerbar er kun tilgængelig, hvis alle varekomponenter i formlen er angivet til **Variabelt forbrug**. Funktionen er ikke tilgængelig, hvis varekomponenterne angives som **Fast forbrug** eller **Trinforbrug**. Når funktionen Skalerbar bruges, og du ændrer en ingrediens i en formel, justeres mængden af de andre ingredienser, der er valgt, også. Størrelsen af formlen justeres også. Hvis du ændrer formelstørrelsen, ændres mængden af alle skalerbare ingredienser på samme måde. Denne funktion er beregnet specifikt til formeloprettelse og -vedligeholdelse. Den angive ikke, om mængden af en ingrediens skaleres op eller ned på en batchordre.

## <a name="use-step-consumption"></a>Brug af trinforbrug
Trinforbrug fjerner kravet om, at du skal angive en mængde under fanen **Formellinje** for en ingrediens. I stedet er trinforbrug konfigureret, så det har en **Fra serie**-værdi og en **Mængde**-værdi. Oplysningerne fra trinforbruget pr. seriepost, der opfylder mængden på batchordren vælges. Trinforbrug er nyttigt, når forbrugsraten ikke er lineær i forhold til batchordrestørrelsen og kun øger behovet, når en bestemt mængdetærskel er opfyldt. For at aktivere denne funktion for en ny formel under gruppen **Forbrugsberegning** skal du ændre formelindstillingen for den relevante ingrediens fra **Standard** til **Trin**. Du kan angive denne forbrugsmetode under fanen **Konfiguration** på siden **Formellinje**.
