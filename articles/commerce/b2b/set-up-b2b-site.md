---
title: Konfigurere et B2B-e-handelswebsted
description: Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere et business-to-business (B2B)-e-handelswebsted i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 171e518258e9600bd7526cf52e3e456d272e6bce
ms.sourcegitcommit: 5f5a8b1790076904f5fda567925089472868cc5a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891379"
---
# <a name="set-up-a-b2b-e-commerce-site"></a>Oprette et B2B-e-handelswebsted

[!include [banner](../../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Business-to-business-e-handelswebsteder indeholder nogle af de vigtigste funktioner, der optimerer arbejdsgangen for en B2B-bruger. Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere et business-to-business (B2B)-e-handelswebsted i Microsoft Dynamics 365 Commerce. Den gennemgår de moduler og lokationsindstillinger, der skal konfigureres for at aktivere B2B-specifikke scenarier.

## <a name="prerequisites"></a>Forudsætninger

- Hvis du vil konfigurere et B2B-e-handelswebsted, skal du aktivere og konfigurere specifikke funktioner i Commerce Headquarters som beskrevet i dette emne.
- Kerneerfaringer, f.eks. registrering af produkter, sider med produktoplysninger, indkøbsvognen og betaling ved kassen, drives af de samme moduler, der bruges til B2C-e-handelswebsteder (business-to-consumer). Webstedets forfattere skal kende til alle de moduler, der understøtter Dynamics 365 Commerce. Yderligere oplysninger finder du i [Modulbiblioteksoversigt](../starter-kit-overview.md).
- I dette emne antages det, at forfattere af websteder forstår de grundlæggende funktioner i Commerce Site Builder, skabeloner, fragmenter og sider, så de kan aktivere B2B-funktionerne for e-handelswebsteder.

## <a name="site-level-settings"></a>Indstillinger på lokationsniveau

Du kan få adgang til indstillinger på webstedsniveau i Site Builder på **Websted-indstillinger \> Udvidelser**. Følgende to indstillinger på lokationsniveau gælder for B2B-scenarier:

- **Aktiver debitorkontobetalinger** – Denne egenskab giver brugerne mulighed for at betale for ordrer ved hjælp af debitorkonti. De tilgængelige værdier er **Aktiveret for B2B-kunder**, **Aktiveret for B2C-kunder**, **Aktiveret for alle debitorer** og **Deaktiveret for alle debitorer**. Hvis dit B2B-websted understøtter debitorkonti, skal du vælge **Aktiveret for B2B-kunder**.
- **Aktiver grænser for ordreantal** – Denne egenskab giver dig mulighed for at angive grænser for det antal varer, der kan bestilles for hvert produkt eller hver kategori. De tilgængelige værdier er **Aktiveret for B2B-kunder**, **Aktiveret for B2C-kunder**, **Aktiveret for alle debitorer** og **Deaktiveret for alle debitorer**.

> [!NOTE]
> Når du opgraderer til den seneste version af modulbiblioteket, skal du følge en ekstra fremgangsmåde for at sikre, at de tidligere beskrevne indstillinger for webstedet er tilgængelige i dit miljø. Du kan finde flere oplysninger under [Opdatere app.settings.json-filen](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="create-business-partner-sign-up-pages"></a>Oprette tilmeldingssider til forretningspartner

For at blive forretningspartner skal brugerne først sende en anmodning om forretningspartner. Et link til siden til anmodning om forretningspartner vil være tilgængeligt på B2B-startsiden, så brugerne kan starte processen. Når brugerne sender en anmodning om en forretningspartner, modtager de en bekræftelse på, at anmodningen er sendt. 

### <a name="create-a-business-partner-request-page"></a>Oprette en anmodningsside for forretningspartner

Modulet **Tilmelding for partner** på en side med en anmodning om forretningspartner bruges til at starte brugeranmodninger om at blive forretningspartnere. I dette modul kan du indsamle de brugeroplysninger, der kræves til tilmeldingsprocessen. Modulet til **Forretningskontoadresse** bruges desuden til at hente brugerens adresse.

Hvis du vil konfigurere siden til anmodning om forretningspartner i Site Builder, skal du følge disse trin.

1. Opret en skabelon med navnet **Tilmelding**. Denne skabelon skal indeholde følgende moduler:

    - Partner-logon
    - Brødkrumme
    - Overordnet
    - Sidefod
    - Indholdsblok
    - Tekstblok
    - Produktsamling

1. Brug skabelonen **Tilmelding** til at oprette en side med navnet **Forretningspartneranmodning**.
1. På pladsen **Overskrift** tilføjes overskriftsfragmentet, der er forudkonfigureret med webstedets overskrift.
1. På pladsen **Sidefor** tilføjes sidefodsfragmentet, der er forudkonfigureret med webstedets sidefod.
1. Tilføj modulet **Container** på pladsen **Hoved**. Angiv **Bredde**-værdien til **Udfyld container** i egenskabsruden for modulet.
1. På pladsen **Container** skal du tilføje et **Brødkrumme**-modul. Konfigurer et link til startsiden under **Links** i ruden Modulegenskaber, og angiv **Startside** som hyperlinktekst.
1. på pladsen **Container** skal du tilføje et modul til **Partnertilmelding** under modulet **Brødkrumme**. I ruden Modulegenskaber under **Overskrift** skal du angive **Blive forretningspartner**.
1. På pladsen **Partnertilmelding** skal du tilføje modulet **Forretningskontoadresse**.
1. på pladsen **Container** skal du tilføje et modul til **Tekstblok** under modulet **Partnertilmelding**. Her kan du definere vilkår og betingelser for tilmeldingsprocessen.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.
1. Udgiv URL-adressen for siden.

### <a name="create-a-business-partner-request-confirmation-page"></a>Oprette en anmodningsbekræftelsesside for forretningspartner

Når en anmodning om forretningspartner er sendt, skal brugeren have vist en bekræftelsesside for at bekræfte afsendelsen. 

Hvis du vil konfigurere siden til anmodningsbekræftelse om forretningspartner i Site Builder, skal du følge disse trin.

1. Brug skabelonen **Tilmelding**, du tidligere har oprettet til at oprette en side med navnet **Partneranmodningsbekræftelse**.
1. På pladsen **Overskrift** tilføjes overskriftsfragmentet, der er forudkonfigureret med webstedets overskrift.
1. På pladsen **Sidefor** tilføjes sidefodsfragmentet, der er forudkonfigureret med webstedets sidefod.
1. Tilføj modulet **Container** på pladsen **Hoved**. Angiv **Bredde**-værdien til **Udfyld container** i egenskabsruden for modulet.
1. Tilføj modulet **Indholdsblok** til pladsen **Container**. Angiv **Anmodning overført** i ruden modulegenskaber under **Overskrift**. Angiv **Din anmodning er overført** i feltet **Tekst**. Konfigurer et link til startsiden under **Links**, og angiv **Tilbage til indkøb** som hyperlinktekst.
1. Tilføj et andet **Container**-modul, og tilføj modulet **Produktsamling**.
1. Konfigurer modulet **Produktsamling** med den anbefaling eller kategoriliste, som du vil vise på siden.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.
1. Udgiv URL-adressen for siden.

Hvis du vil tilføje et link til anmodningsbekræftelse om forretningspartner i Site Builder, skal du følge disse trin.

1. Gå til siden **Forretningspartneranmodning**, som du oprettede tidligere, og vælg **Rediger**. 
1. Vælg modulet **partnertilmelding**. Konfigurer linket til den anmodningsside for forretningspartner, du oprettede tidligere, under **Link til siden Bekræftelse af tilmelding** i egenskabsruden. 
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

### <a name="add-a-business-partner-request-link-to-the-home-page"></a>Tilføje et link til en anmodning om forretningspartner til startsiden

Når tilmeldingssiderne til anmodning om forretningspartner er oprettet, skal du gøre tilmeldingssiden tilgængelig via et link på startsiden. Du kan udføre denne opgave ved at føje linket til ethvert modul **Indholdsblok** på startsiden.

Hvis du vil tilføje et link til forretningspartneranmodning til startsiden i Site Builder, skal du følge disse trin.

1. Gå til startsiden for dit websted, og vælg **Rediger**.
1. Tilføj modulet **Indholdsblok**. I ruden Modulegenskaber under **Links** kan du konfigurere et link til den side med forretningspartneranmodning, du oprettede tidligere, og angive, at du vil angive **Tilmelding til forretningspartner** eller lignende som linktekst. Tilføj et billede efter behov.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="account-management-landing-page"></a>Landingsside for kontostyring

På kontostyringssiden vises alle de oplysninger, der skal bruges til både B2B- og B2C-e-handelswebsteder. Det er kun brugere, der er logget på, som kan få vist denne side.

Hvis du vil oprette og konfigurere en landingsside til B2B-kontostyring i Site Builder, skal du følge disse trin.

1. Opret en skabelon med navnet **Kontostyring**. Denne skabelon skal indeholde følgende moduler:

    - Overordnet
    - Sidefod
    - Brødkrumme
    - Felt til kontovelkomst
    - Generisk felt til konto
    - Kontoadressefelt
    - Felt til kontoønskeliste
    - Kontoadressefelt
    - Felt til kontofordelskunde
    - Kontokundesaldofelt
    - Skabelonfelt til kontoordre
    - Organisationsbrugere
    - Forretningsorganisationsliste
    - Kundens kontosaldo
    - Linjer i ordreskabelon
    - Liste i ordreskabelon
    - Kontofakturafelt
    - Fakturaliste
    - Fakturadetaljer

1. Du kan bruge skabelonen **Konto** til at oprette en side med navnet **Min konto**.
1. På pladsen **Overskrift** tilføjes overskriftsfragmentet, der er forudkonfigureret med webstedets overskrift.
1. På pladsen **Sidefor** tilføjes sidefodsfragmentet, der er forudkonfigureret med webstedets sidefod.
1. Tilføj modulet **Container** på pladsen **Hoved**. Angiv **Bredde**-værdien til **Udfyld container** i egenskabsruden for modulet. 
1. På pladsen **Container** skal du tilføje et **Brødkrumme**-modul. Konfigurer et link til startsiden under **Links** i ruden Modulegenskaber, og angiv **Startside** som hyperlinktekst.
1. Tilføj modulet **Velkomstfelt** på pladsen **Container**. Angiv **Velkommen** i ruden modulegenskaber under **Overskrift**.
1. Tilføj et nyt modul **Container** (**Container 2**) på pladsen **Hoved**. Angiv **Bredde**-værdien til **Udfyld container** i egenskabsruden for modulet. Angiv værdien for **Underordnet** til **To**. 
1. På pladsen **Container 2** skal du tilføje et **Kontogenerisk felt**-modul. Angiv **Min profil** i ruden modulegenskaber under **Overskrift**. Konfigurer et link til siden **Min profil** under **Links**. 
1. På pladsen **Container 2** skal du tilføje endnu et **Kontogenerisk felt**-modul. Angiv **Ordrehistorik** i ruden modulegenskaber under **Overskrift**. Konfigurer et link til ordrehistorik under **Links**.
1. Tilføj et nyt modul **Container** (**Container 3**) på pladsen **Hoved**. Angiv **Bredde**-værdien til **Udfyld container** i egenskabsruden for modulet. Angiv værdien for **Underordnet** til **To**. 
1. På pladsen **Container 3** skal du tilføje et **Kontoadressefelt**-modul. Angiv **Min adresse** i ruden modulegenskaber under **Overskrift**. Konfigurer et link til siden **Min adresse** under **Links**. 
1. På pladsen **Container 3** skal du tilføje et **Kontoønskelistefelt**-modul. Angiv **Min ønskeliste** i ruden modulegenskaber under **Overskrift**. Konfigurer et link til siden **Min ønskeliste** under **Links**.
1. Tilføj et nyt modul **Container** (**Container 4**) på pladsen **Hoved**. Angiv **Bredde**-værdien til **Udfyld container** i egenskabsruden for modulet. Angiv værdien for **Underordnet** til **To**. 
1. På pladsen **Container 4** skal du tilføje et **Organisationsbrugere**-modul. Angiv **Organisationsbrugere** i ruden modulegenskaber under **Overskrift**. 
1. På pladsen **Container 4** skal du tilføje et **Kontokundesaldofelt**-modul. Angiv **Kontokredit** i ruden modulegenskaber under **Overskrift**. 
1. Tilføj et nyt modul **Container** (**Container 5**) på pladsen **Hoved**. Angiv **Bredde**-værdien til **Udfyld container** i egenskabsruden for modulet. Angiv værdien for **Underordnet** til **To**. 
1. På pladsen **Container 5** skal du tilføje et **Kontoordreskabelonfelt**-modul. Angiv **Ordreskabelon** i ruden modulegenskaber under **Overskrift**. 
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

> [!NOTE] 
> Nogle af de afsnit, som du har tilføjet i trin 13 til og med 18, vises ikke på lærredet "hvad du kan se, hvad du får" (WYSIWIG) i Site Builder, da de kræver en signeret B2B-konto.

## <a name="create-and-configure-customer-balance-pages-and-modules"></a>Oprette og konfigurere debitorsaldosider og -moduler 

Debitorkonti kan bruges til at betale for ordrer. Den tilgængelige saldo på en debitorkonto kan ses fra en brugers kontostyringsside.

### <a name="create-a-customer-balance-page"></a>Oprette en debitorsaldoside 

Før du er logget på B2B-brugere, kan se deres debitorsaldo, skal du oprette en debitorsaldoside. 

Hvis du vil oprette en kundesaldoside i webstedgeneratoren, skal du følge disse trin.

1. Brug skabelonen **Kontostyring**, som du oprettede tidligere, til at oprette en side med navnet **Kundesaldo**.
1. På pladsen **Overskrift** tilføjes overskriftsfragmentet, der er forudkonfigureret med webstedets overskrift.
1. På pladsen **Sidefor** tilføjes sidefodsfragmentet, der er forudkonfigureret med webstedets sidefod.
1. Tilføj et nyt modul **Container** (**Container 3**) på pladsen **Hoved**. Angiv **Bredde**-værdien til **Udfyld container** i egenskabsruden for modulet. Angiv værdien for **Underordnet** til **To**.
1. På pladsen **Container** skal du tilføje et **Brødkrumme**-modul. Konfigurer et link til kontostyringslandingssiden under **Links** i ruden Modulegenskaber, og angiv **Min konto** som hyperlinktekst.
1. På pladsen **Container 4** skal du tilføje modulet **Kundekontosaldo**. Angiv **Kontosaldo** i ruden modulegenskaber under **Overskrift**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.
1. Udgiv URL-adressen for siden.
1. Gå til den landingsside for kontostyring (**Min konto**), som du oprettede tidligere.
1. Tilføj et link til kundesaldosiden i egenskabsruden **Kontokundesaldofelt**. 
1. Gem og publicer siden.

Siden kundesaldo er nu oprettet, og brugerne kan åbne den fra kontostyringssiden.

### <a name="configure-a-checkout-page-so-that-the-customer-balance-can-be-used-as-a-form-of-payment"></a>Konfigurere en side til betaling ved kassen, så debitorsaldoen kan bruges som betalingsmåde

Modulet **Kundekontobetaling** er påkrævet for at aktivere, at kundesaldoen kan bruges som en betalingsform. Dette modul skal føjes til siden til betaling ved kassen som en betalingsmåde. Oplysninger om, hvordan du konfigurerer en side til betaling ved kassen og de moduler, der kræves til betaling ved kassen, inklusive alle betalingsoplysninger, finder du i [Til betaling ved kassen-modul](../add-checkout-module.md).

Når du har konfigureret en side til betaling ved kassen, skal du føje modulet **Debitorkontobetaling** til betalingssektionen og derefter gemme og publicere siden. B2B-brugere kan derefter logge på e-handelswebstedet og anvende deres tilgængelige debitorsaldo på ordrer under betaling ved kassen.

Derudover skal du ved **Webstedsgenerator \> Udvidelser** sikre dig, at egenskaben **Aktiver debitorkontobetalinger** er angivet til **Aktiveret for B2B-debitorer**.

## <a name="create-order-template-pages"></a>Oprette sider med ordreskabeloner

Der kan oprettes to sider med ordreskabeloner til et B2B-e-handelswebsted: en listeside med ordreskabeloner og en side med ordreskabelonlinjer.

På en listeside med ordreskabeloner vises en liste over alle tilgængelige ordreskabeloner. Det konfigureres ved hjælp af **Ordreskabelonliste**-modulet. På listesiden med ordreskabeloner kan du oprette eller slette en skabelon og føje varerne i en skabelon til indkøbsvognen.

På en side med ordreskabelonlinjer vises detaljerne om den ordreskabelon, der er valgt på en listeside med ordreskabeloner. Det konfigureres ved hjælp af **Ordreskabelonlinjer**-modulet. Når en bruger vælger navnet på en skabelon på listesiden med ordreskabeloner, vises siden med ordreskabelonlinjer, som viser detaljerne i skabelonen. Brugeren kan derefter få vist og redigere varerne i skabelonen.

### <a name="create-an-order-templates-list-page"></a>Oprette en listeside med ordreskabeloner

Hvis du vil oprette en side med ordreskabelonliste i webstedgeneratoren, skal du følge disse trin.

1. Brug skabelonen **Kontostyring**, som du oprettede tidligere, til at oprette en side med navnet **Ordreskabeloner**.
1. På pladsen **Overskrift** tilføjes overskriftsfragmentet, der er forudkonfigureret med webstedets overskrift.
1. På pladsen **Sidefor** tilføjes sidefodsfragmentet, der er forudkonfigureret med webstedets sidefod.
1. Tilføj modulet **Container** på pladsen **Hoved**. Angiv **Bredde**-værdien til **Udfyld container** i egenskabsruden for modulet.
1. På pladsen **Container** skal du tilføje et **Brødkrumme**-modul. Konfigurer et link til kontostyringslandingssiden under **Links** i ruden Modulegenskaber, og angiv **Min konto** som hyperlinktekst.
1. På pladsen **Container** skal du tilføje et **Ordreskabelonliste**-modul.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.
1. Udgiv URL-adressen for siden.
1. Gå til den landingsside for kontostyring (**Min konto**), som du oprettede tidligere.
1. Konfigurer et link til den listeside med ordreskabeloner, du netop har oprettet, under **Links** i egenskabsruden for modulet **Kontoordreskabeloner**.
1. Gem og publicer siden.

Siden ordreskabelonliste er nu oprettet, og brugerne kan åbne den fra kontostyringssiden.

### <a name="create-an-order-template-lines-page"></a>Oprette en side med ordreskabelonlinjer

Hvis du vil oprette en side med skabelonlinjer i webstedgeneratoren, skal du følge disse trin.

1. Brug skabelonen **Kontostyring**, som du oprettede tidligere, til at oprette en side med navnet **Ordreskabelonlinjer**.
1. På pladsen **Overskrift** tilføjes overskriftsfragmentet, der er forudkonfigureret med webstedets overskrift.
1. På pladsen **Sidefor** tilføjes sidefodsfragmentet, der er forudkonfigureret med webstedets sidefod.
1. Tilføj modulet **Container** på pladsen **Hoved**. Angiv **Bredde**-værdien til **Udfyld container** i egenskabsruden for modulet.
1. På pladsen **Container** skal du tilføje et **Brødkrumme**-modul. Konfigurer et link til kontostyringslandingssiden under **Links** i ruden Modulegenskaber, og angiv **Min konto** som hyperlinktekst.
1. På pladsen **Container** skal du tilføje et **Ordreskabelonlinjer**-modul.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.
1. Udgiv URL-adressen for siden.

## <a name="onboard-business-partner-users"></a>Få forretningspartnerbrugere med i start

På siden Med organisationsbrugere kan administratoren af en forretningspartnerorganisation modtage yderligere brugere fra den pågældende organisation til webstedet for B2B-e-handel. Det konfigureres ved hjælp af **Forretningsorganisationsliste**-modulet. Fra organisationsbrugersiden kan en administrator tilføje eller fjerne brugere, definere kontosaldi og anmode om kontoudtog for en bruger.

Hvis du vil oprette en side med organisationsbrugere i webstedgeneratoren, skal du følge disse trin.

1. Brug skabelonen **Kontostyring**, som du oprettede tidligere, til at oprette en side med navnet **Organisationsbrugere**.
1. På pladsen **Overskrift** tilføjes overskriftsfragmentet, der er forudkonfigureret med webstedets overskrift.
1. På pladsen **Sidefor** tilføjes sidefodsfragmentet, der er forudkonfigureret med webstedets sidefod.
1. Tilføj modulet **Container** på pladsen **Hoved**. Angiv **Bredde**-værdien til **Udfyld container** i egenskabsruden for modulet.
1. På pladsen **Container** skal du tilføje et **Brødkrumme**-modul. Konfigurer et link til kontostyringslandingssiden under **Links** i ruden Modulegenskaber, og angiv **Min konto** som hyperlinktekst.
1. På pladsen **Container** skal du tilføje et **Forretningsorganisationsliste**-modul. Angiv **Organisationsbrugere** i ruden modulegenskaber under **Overskrift**.
1. Aktiver egenskaberne **tabelsortering** og **tabelinddeling** i ruden med modulegenskaberne **Forretningsorganisationsliste**. Angiv sideoptællingen til **5**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.
1. Udgiv URL-adressen for siden.
1. Gå til den landingsside for kontostyring (**Min konto**), som du oprettede tidligere.
1. Konfigurer et link til den side med organisationsbrugere, du netop har oprettet, under **Links** i egenskabsruden for modulet **Organisationsbrugere**. 
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="create-invoice-pages"></a>Oprette fakturasider

En listeside med fakturaer vises en liste over alle tilgængelige fakturaer. Den konfigureres ved hjælp af modulet **Fakturaliste**. På fakturalistesiden kan brugere betale eller anmode om fakturaer. 

En side med fakturadetaljer viser oplysningerne om den faktura, der er valgt på en listeside med fakturaer. Den konfigureres ved hjælp af modulet **Fakturadetaljer**. Når en bruger vælger et faktura-id på en fakturalisteside, vises siden med fakturadetaljer, og oplysningerne om fakturaen vises.

### <a name="create-an-invoices-list-page"></a>Oprette en listeside med fakturaer

Hvis du vil oprette en side med fakturaliste i webstedgeneratoren, skal du følge disse trin.

1. Brug skabelonen **Kontostyring**, som du oprettede tidligere, til at oprette en side med navnet **Fakturaliste**.
1. På pladsen **Overskrift** tilføjes overskriftsfragmentet, der er forudkonfigureret med webstedets overskrift.
1. På pladsen **Sidefor** tilføjes sidefodsfragmentet, der er forudkonfigureret med webstedets sidefod.
1. Tilføj modulet **Container** på pladsen **Hoved**. Angiv **Bredde**-værdien til **Udfyld container** i egenskabsruden for modulet.
1. På pladsen **Container** skal du tilføje et **Brødkrumme**-modul. Konfigurer et link til kontostyringslandingssiden under **Links** i ruden Modulegenskaber, og angiv **Min konto** som hyperlinktekst.
1. Tilføj modulet **fakturaliste** til pladsen **Container**. Angiv **fakturaer** i ruden modulegenskaber under **Overskrift**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.
1. Udgiv URL-adressen for siden.
1. Gå til den landingsside for kontostyring (**Min konto**), som du oprettede tidligere.
1. Konfigurer et link til den fakturalisteside, du netop har oprettet, under **Links** i egenskabsruden for modulet **Kontofakturafelt**. 
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

### <a name="create-an-invoice-details-page"></a>Oprette en side med fakturadetaljer

Hvis du vil oprette en side med fakturadetaljer i webstedgeneratoren, skal du følge disse trin.

1. Brug skabelonen **Kontostyring**, som du oprettede tidligere, til at oprette en side med navnet **Fakturadetaljer**.
1. På pladsen **Overskrift** tilføjes overskriftsfragmentet, der er forudkonfigureret med webstedets overskrift.
1. På pladsen **Sidefor** tilføjes sidefodsfragmentet, der er forudkonfigureret med webstedets sidefod.
1. Tilføj modulet **Container** på pladsen **Hoved**. Angiv **Bredde**-værdien til **Udfyld container** i egenskabsruden for modulet.
1. På pladsen **Container** skal du tilføje et **Brødkrumme**-modul. Konfigurer et link til kontostyringslandingssiden under **Links** i ruden Modulegenskaber, og angiv **Min konto** som hyperlinktekst. Konfigurer derefter et link til fakturalistesiden, og indtast **Fakturalister** som hyperlinktekst.
1. Tilføj modulet **Fakturadetaljer** til pladsen **Container**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.
1. Udgiv URL-adressen for siden.

## <a name="add-a-quick-add-module-to-the-cart-page"></a>Føje et modul til hurtig tilføjelse til indkøbsvognssiden

Du kan bruge modulet Hurtig tilføjelse til hurtigt at føje flere varer til indkøbsvognen ved hjælp af vare-id'er (også kaldet \[SKU\]-id'er for lagerenhed). Modulet Hurtig tilføjelse er føjet til et websteds indkøbsvogn.

Hvis du vil tilføje modulet Hurtig tilføjelse til en indkøbsvognsside i Commerce Site Builder, skal du benytte følgende fremgangsmåde.

1. Gå til **Skabeloner**, og vælg skabelonen for webstedets indkøbsvognsside.
1. Vælg **Rediger**.
1. På pladsen **Hoved** i modulet **Standardside** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Hurtig tilføjelse** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til **Sider**, og vælg webstedets indkøbsvognsside.
1. På pladsen **Hoved** i modulet **Standardside** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.
1. I egenskabsruden for modulet **Container** skal du vælge **Fyld container** under **Bredde**.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Hurtig tilføjelse** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

> [!NOTE] 
> Modulet Hurtig tilføjelse er tilgængeligt fra frigivelsen af Commerce version 10.0.17. Hvis du opdaterer fra en ældre version af Commerce, skal du opdatere filen appsettings.json manuelt. Du kan finde instruktioner i [Opdateringer af SDK og modulbibliotek](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="add-a-bulk-purchase-module-to-a-product-details-page"></a>Føje et massekøbsmodul til en side med produktoplysninger

Massekøbsmodulet på en side med produktoplysninger (PDP) giver en matrixbaseret oplevelse, hvor en køber hurtigt kan føje flere varianter af et produkt til indkøbsvognen. Når en webstedsbruger skal bestille flere varianter af samme produkt, fjerner denne oplevelse behovet for at vælge kombinationen af produktdimensioner, definere antallet, føje varianten til indkøbsvognen og derefter gentage processen for andre kombinationer af produktdimensioner.

Udfør følgende trin for at føje et massekøbsmodul til en PDP i Commerce-webstedsgeneratoren.

1. Gå til **Skabeloner**, og vælg PDP-skabelonen for webstedet.
1. Vælg **Rediger**.
1. På pladsen **Hoved** i modulet **Standardside** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Massekøb** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til **Sider**, og vælg webstedets PDP.
1. På pladsen **Hoved** i modulet **Standardside** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.
1. I egenskabsruden for modulet **Container** skal du vælge **Fyld container** under **Bredde**.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Massekøb** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

> [!NOTE] 
> Modulet Massekøb er tilgængeligt efter Commerce-version 10.0.24-udgaven. Hvis du opdaterer fra en ældre version af Commerce, skal du opdatere filen appsettings.json manuelt. Du kan finde instruktioner i [Opdateringer af SDK og modulbibliotek](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](../starter-kit-overview.md)

[Opdateringer til SDK og modulbibliotek](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)

[Oprette oversigt over side](../authoring-home-overview.md)

[Oversigt over skabeloner og layout](../templates-layouts-overview.md)

[Arbejde med fragmenter](../work-with-fragments.md)

[Tilføje en ny webstedsside](../add-new-page.md)

[Betalingsmodul](../add-checkout-module.md)

[Indholdsblokmodul](../add-hero-module.md)

[Produktsamlingsmodul](../product-collection-module-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
