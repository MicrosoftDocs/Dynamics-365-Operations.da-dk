---
title: Firmabegreb i Dataverse
description: Denne artikel beskriver integrationen af firmadata mellem finans og drift og Dataverse.
author: RamaKrishnamoorthy
ms.date: 08/04/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: ad0075e2b92ebeb9fba879bcae503100dc7adb47
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/28/2022
ms.locfileid: "9205930"
---
# <a name="company-concept-in-dataverse"></a>Firmabegreb i Dataverse

[!include [banner](../../includes/banner.md)]




I finans og drift er konceptet et *firma* både en juridisk konstruktion og en forretningskonstruktion. Det er også en sikkerheds- og synlighedsgrænse for data. Brugere arbejder altid i konteksten af et enkelt firma, og de fleste data stripes (spredes) af firmaet.

Dataverse har ikke et tilsvarende koncept. Det tætteste koncept er *virksomhedsenhed*, som primært er en sikkerheds- og synlighedsgrænse for brugerdata. Dette koncept har ikke samme juridiske eller forretningsmæssige implikationer som firmakonceptet.

Da virksomhedsenhed og firma ikke er tilsvarende koncepter, er det ikke muligt at gennemtvinge en en-til-en (1:1) tilknytning mellem dem med henblik på Dataverse-integration. Men da brugere som standard skal kunne se de samme rækker i programmet og Dataverse, har Microsoft introduceret en ny tabel i Dataverse, der hedder cdm\_Company. Denne tabel svarer til tabellen Firma i programmet. For at hjælpe med at sikre, at synlighed af rækker som standard er ens mellem programmet og Dataverse, anbefaler vi følgende opsætning af data i Dataverse:

+ For hver firmarække i finans og drift, der er aktiveret til dobbeltskrivning, oprettes der en tilknyttet cdm\_Company-række.

+ Når en cdm\_Company-række oprettes og aktiveres til dobbeltskrivning oprettes der en standardvirksomhedsenhed med samme navn. Selvom der automatisk oprettes en standardejer for denne virksomhedsenhed, bruges virksomhedsenheden ikke.
+ Der oprettes et separat ejerteam med samme navn med Dual Write-suffiks. Det er også tilknyttet virksomhedsenheden.

+ Som standard angives ejeren af enhver række, der oprettes og dobbeltskrives til Dataverse, til "DW-ejer"-teamet, der er knyttet til den tilknyttede virksomhedsenhed.

I følgende illustration vises et eksempel på denne dataopsætning i Dataverse.

![Dataopsætning i Dataverse.](media/dual-write-company-1.png)

På grund af denne konfiguration ejes alle rækker, der er relateret til USMF-firmaet, af et team, der er knyttet til USMF-virksomhedsenheden i Dataverse. Derfor kan alle brugere, der har adgang til den pågældende virksomhedsenhed via en sikkerhedsrolle, der er angivet til synlighed på virksomhedsenhedsniveau, nu se disse rækker. Følgende eksempel viser, hvordan teams kan bruges til at give den korrekte adgang til disse rækker.

+ Rollen "Sales Manager" er tildelt medlemmer af teamet "USMF Sales".
+ Brugere, der har rollen "Sales Manager", kan få adgang til alle firmarækker, der er medlem af den samme virksomhedsenhed, som de er medlem af.
+ Teamet "USMF Sales" er knyttet til den USMF-virksomhedsenhed, der er nævnt tidligere.
+ Derfor kan medlemmer af teamet "USMF Sales" se enhver konto, der ejes af brugeren "USMF DW", som ville være kommet fra USMF-firmaenheden i finans og drift.

![Sådan kan teams bruges.](media/dual-write-company-2.png)

Som den foregående illustration viser, er denne 1:1-tilknytning mellem virksomhedsenhed, firma og team blot et udgangspunkt. I dette eksempel oprettes der manuelt en ny "Europe"-virksomhedsenhed i Dataverse som overordnet til både DEMF og ESMF. Denne nye rodvirksomhedsenhed er ikke relateret til dobbeltskrivning. Den kan dog bruges til at give medlemmerne af "EUR Sales"-teamet adgang til kontodata i både DEMF og ESMF ved at indstille datasynlighed til **Parent/Child BU** i den tilknyttede sikkerhedsrolle.

En sidste artikel, der skal omtales, er, hvordan dobbeltskrivning afgør, hvilket ejerteam det skal tildeles rækker. Denne funktionsmåde styres af kolonnen **Standardejerteam** på cdm\_Company-rækken. Når en cdm\_Company-række er aktiveret til dobbeltskrivning, opretter en plug-in automatisk den tilknyttede virksomhedsenhed og ejerteamet (hvis den ikke allerede findes) og indstiller kolonnen **Standardejerteam**. Administratoren kan ændre denne kolonne til en anden værdi. Men administratoren kan ikke rydde kolonnen, så længe tabellen er aktiveret til dobbeltskrivning.

> [!div class="mx-imgBorder"]
![Kolonnen Standardejerteam.](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Firma-striping og bootstrapping

Dataverse-integration giver firmaparitet ved at bruge en firmaidentifikator til at stripe data. Som det fremgår af følgende illustration, udvides alle firmaspecifikke tabeller, så de har en mange-til-en-relation (N:1) med tabellen cdm\_Company.

> [!div class="mx-imgBorder"]
![N:1-relation mellem en firmaspecifik tabel og tabellen cdm_Company.](media/dual-write-bootstrapping.png)

+ Når et firma er tilføjet og gemt i rækker, bliver værdien skrivebeskyttet. Derfor skal brugerne sørge for, at de vælger det rigtige firma.
+ Kun rækker, der har firmadata, er kvalificerede til dobbeltskrivning mellem programmet og Dataverse.
+ For eksisterende Dataverse-data vil en administrativ bootstrapping-oplevelse snart være tilgængelig.


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Udfylde firmanavn automatisk i kundeengagementapps

Du kan automatisk udfylde firmanavnet i kundeengagementapps på flere måder.

+ Hvis du er systemadministrator, kan du angive standardfirmaet ved at navigere til **Avancerede indstillinger > System > Sikkerhed > Brugere**. Åbn formularen **Bruger**, og angiv i sektionen **Organisationsoplysninger** værdien **Firmastandard på formularer**.

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Angiv standardfirma i sektionen Organisationsoplysninger.":::

+ Hvis du har **Skrive**-adgang til tabellen **SystemUser** for **Afdeling**-niveauet, kan du ændre standardfirmaet i en hvilken som helst formular ved at vælge et firma i rullemenuen **Firma**.

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Ændre firmanavnet på en ny konto.":::

+ Hvis du har **skrive**-adgang til data i mere end ét firma, kan du ændre standardfirmaet ved at vælge en række, der tilhører et andet firma.

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Når du vælger en række, ændres standardfirmaet.":::

+ Hvis du er systemkonfigurator eller -administrator, og du vil udfylde firmadata automatisk i en brugerdefineret formular, kan du bruge [formularhændelser](/powerapps/developer/model-driven-apps/clientapi/events-forms-grids). Føj en JavaScript-reference til **msdyn_/DefaultCompany.js**, og brug følgende hændelser. Du kan bruge enhver standardformular, f.eks. formularen **Konto**.

    + Hændelsen **OnLoad** for formularen: Angiv kolonnen **defaultCompany**.
    + Hændelsen **OnChange** for kolonnen **Firma**: Angiv kolonnen **updateDefaultCompany**.

## <a name="apply-filtering-based-on-the-company-context"></a>Anvende filtrering baseret på firmakontekst

Hvis du vil anvende filtrering baseret på firmakonteksten i de brugerdefinerede formularer eller på brugerdefinerede opslagskolonner, der er føjet til standardformularer, skal du åbne formularen og bruge sektionen **Filtrering af relaterede poster** til at anvende firmafilteret. Du skal angive dette for hver opslagskolonne, der kræver filtrering, på baggrund af det underliggende firma på en bestemt række. Indstillingen vises for **Konto** i følgende illustration.

:::image type="content" source="media/apply-company-context.png" alt-text="Anvende firmakontekst.":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
