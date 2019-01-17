---
title: Sortimentsstyring
description: "I dette emne beskrives de grundlæggende begreber for sortimentsstyring i Microsoft Dynamics 365 for Retail og overvejelser i forbindelse med implementering af projekter."
author: jblucher
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: jeffbl
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Application update 5
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 033968667048faf475b13f8fb95e693dc26935ca
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---

# <a name="assortment-management"></a>Sortimentsstyring

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Overblik

Microsoft Dynamics 365 for Retail indeholder *sortimenter*, så du kan administrere produkttilgængeligheden på tværs af kanaler. Sortimenter bestemmer, hvilke produkter der er tilgængelige i bestemte butikker og i en bestemt periode.

I Retail er et sortiment en tilknytning af en eller flere kanaler (eller grupper af kanaler, når der bruges organisationshierarkier) til et eller flere produkter (eller grupper af produkter, når der bruges kategorihierarkier).

Den overordnede blanding af produkter på en kanal afhænger af de publicerede sortimenter, der er tildelt til kanalen. Derfor kan du konfigurere flere aktive sortimenter pr. kanal.

### <a name="basic-assortment-setup"></a>Konfiguration af basissortiment

I følgende eksempel er der konfigureret et entydigt sortiment for hver butik. I eksemplet er kun produkt 1 tilgængeligt på lager 1, og kun produkt 2 er tilgængeligt i butik 2.

![Hvert produkt er tilgængeligt i én butik](./media/Managing-assortments-figure1.png)

Hvis du vil gøre produkt 2 tilgængeligt i butik 1, kan du føje produktet til sortiment 1.

![Produkt 2 blev føjet til sortiment 1](./media/Managing-assortments-figure2.png)

Du kan også føje butik 1 til sortiment 2.

![Butik 1 blev føjet til sortiment 2](./media/Managing-assortments-figure3.png)

### <a name="organization-hierarchies"></a>Organisationshierarkier

I situationer, hvor flere kanaler deler de samme produktsortimenter, kan du konfigurere sortimenterne ved hjælp af sortimentsorganisationshierarkiet i Retail. Når der tilføjes noder fra dette hierarki, medtages alle kanaler i den pågældende node og dens underordnede noder.

![Organisationshierarki](./media/Managing-assortments-figure4.png)

### <a name="product-categories"></a>Produktkategorier

På samme måde kan du på produktsiden medtage grupper af produkter ved hjælp af produktkategorihierarkier. Du kan konfigurere sortimenter ved at medtage en eller flere kategorihierarkinoder. I dette tilfælde omfatter sortimentet alle produkter i kategorinoden og dens underordnede noder.

![Produktkategorier](./media/Managing-assortments-figure5.png)

### <a name="excluded-products-or-categories"></a>Udeladte produkter eller kategorier

Ud over at medtage produkter og kategorier i sortimenter kan du bruge indstillingen Udelad til at definere bestemte produkter eller kategorier, der skal udelades fra sortimenter. I følgende eksempel skal du medtage alle produkter i en bestemt kategori, med undtagelse af produkt 2. I dette tilfælde behøver du ikke at definere sortimentet produkt for produkt eller oprette flere kategorinoder. I stedet kan du nøjes med at medtage kategorien, men udelade produktet.

> [!NOTE]
> Hvis et produkt er både medtaget og udeladt i et eller flere sortimenter pr. definition, bliver produktet altid betragtet som udeladt.

![Udeladt produkt](./media/Managing-assortments-figure6.png)

### <a name="global-and-released-products"></a>Globale og frigivne produkter

Sortimenter defineres på globalt niveau og kan indeholde kanaler fra flere juridiske enheder. De produkter og kategorier, der er inkluderet i sortimenter, deles også på tværs af juridiske enheder. Et produkt skal dog frigives, før det faktisk kan sælges, bestilles, tælles eller modtages i kanalen (f.eks. på \[POS\]). Selvom to butikker i forskellige juridiske enheder kan dele et sortiment, der indeholder de samme produkter, er produkterne derfor kun tilgængelige, hvis de er frigivet til disse juridiske enheder.

### <a name="dynamic-and-static-assortments"></a>Dynamiske og statiske sortimenter

Sortimenter kan defineres med bestemte kanaler og produkter eller ved at medtage organisationsenheder og -kategorier. Sortimenter, herunder referencer til disse grupper, betragtes som dynamiske sortimenter. Hvis definition eller indholdet af disse grupper ændres, mens sortimentet er aktivt, ændres definitionen af sortimentet også.

Et sortiment er f.eks. oprindeligt defineret og frigivet, så det refererer til en kategori af produkter. Hvis der senere føjes flere produkter til kategorien, medtages disse produkter automatisk i definitionen af det eksisterende sortiment. Du behøver ikke at føje produkterne til sortimentet manuelt. På samme måde, hvis en organisationsenhed føjes til en anden node, reguleres organisationsenhedens sortiment automatisk ud fra denne definition.

### <a name="stopped-products"></a>Stoppede produkter

Du kan "stoppe" frigivne produkter for salgsprocessen ved at slå en indstilling til i **Standardordre**-indstillingerne. Denne indstilling bruges oftest, når et produkt er i slutningen af sin levetid og derfor ikke bør sælges på nogen kanal. Sortimenter respekterer denne indstilling, og stoppede produkter bliver ikke udvalgt, uanset sortimentskonfigurationen.

### <a name="blocked-products"></a>Spærrede produkter

Ud over at stoppe salget af et produkt kan du midlertidigt spærre et produktsalg. Du kan konfigurere denne indstilling under fanen **Retail** for et frigivet produkt. Spærrede produkter udvælges stadig, men du får en meddelelse i POS, der angiver, at produktet ikke kan sælges.

### <a name="date-effectivity"></a>Gyldig fra

Sortimenter er datorelaterede. Detailhandlere kan derfor vælge, hvornår produkter skal være tilgængelige eller ikke være tilgængelige pr. kanal. Du kan definere og publicere sortimenter på forhånd og angive start- og slutdatoer. Produkterne bliver automatisk tilgængelig eller ikke tilgængelig på de angivne datoer.

### <a name="process-assortments-batch-job"></a>Behandle sortimentsbatchjob

Sortimenter, der defineres i Retail, skal behandles, før de kan træde i kraft. Denne behandling udføres af følgende årsager:

- Sortimentsdefinitioner skal være denormaliserede, så kanaler lettere kan forbruge dem. Du kan definere en produktsammensætning for en kanal gennem flere sortimenter, der spænder over forskellige datointervaller. Når nogle af disse oplysninger beregnes forhånd på serveren, forbedres ydeevnen på kanalen.
- Produkterne og kanalerne i sortimentet kan ændres uden for selve sortimentet. Dynamiske sortimenter, der indeholder referencer til kategorier eller organisationsenheder, skal behandles med jævne mellemrum, så de medtager eller udelukker poster baseret på deres aktuelle tildeling.

## <a name="implementation-considerations"></a>Overvejelser i forbindelse med implementering

Overvej følgende implementeringskrav, når du planlægger og administrerer sortimenter til din Retail-installation:

- **Datareplikering og databasestørrelse** – Selvom sortimenter hjælper med forretningsbehovet for at administrere produkttilgængeligheden, er de også et vigtigt værktøj til administration af størrelsen på kanal og offlinedatabaserne. Godt administrerede sortimenter er med til at reducere den mængde data, der skal behandles og replikeres til kanal- og offlinedatabaserne. De hjælper også med reducere antallet af poster, der skal gøres permanente. Færre poster i disse databaser øger ydeevnen, når du føjer varer til en transaktion og søger efter produkter.
- **Datorelaterede/udløbende sortimenter** – Et af de mest effektive værktøjer til administration af antallet af produkter i kanal- og offlinedatabaser er sortimenters datogyldighed. Hvis du overlader åbne (ikke-udløbende) sortimenter til sæsonprodukter eller produkter, der er i slutningen af deres levetid, vokser disse databaser uendeligt. Du kan bruge forskellige metoder til at styre denne situation. For eksempel kan du opretholde separate sortimenter til sæsonbetonede produkter og produkter, der altid er tilgængelige.
- **Salg og returneringer uden for et sortiment** – Denne funktion hjælper detailhandlere med effektivt at styre deres sortimenter ved at lade dem med at begrænse antallet af tilgængelige produkter til produkter, der hører til den centrale produktsammensætning for butikken. Denne funktion hjælper også detailhandlere med at håndtere situationer, hvor et produkt ved en fejltagelse er udeladt fra et sortiment, eller hvor der blev returneret et produkt uden for ikrafttrædelsesdatoerne for sortimentet.

Hvis produktdataene ikke findes i kanaldatabasen, foretager POS kald i realtid til hovedkontoret for at få de nødvendige oplysninger, så produktet kan blive solgt, returneret eller sættes på en debitorordre. Produktoplysninger, der hentes på denne måde, er kun tilgængelige for den pågældende transaktion. Produktet føjes ikke til sortimentsdefinitionen. Derfor vil efterfølgende kald i realtids blive foretaget efter behov.

