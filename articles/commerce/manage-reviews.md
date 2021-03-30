---
title: Administrere vurderinger og anmeldelser
description: I dette emne beskrives, hvordan du kan håndtere vurderinger og anmeldelser i Microsoft Dynamics 365 Commerce-webstedsgenerator.
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f8ab85605bce11934f71237ad1ef7cd24804319b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250798"
---
# <a name="manage-ratings-and-reviews"></a>Administrere vurderinger og anmeldelser

[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du kan håndtere vurderinger og anmeldelser i Microsoft Dynamics 365 Commerce-webstedsgenerator.

## <a name="overview"></a>Overblik

Dynamics 365 Commerce bruger Microsoft Azure Cognitive Services til automatisk at moderere tekst i anmeldelser ved at bortredigere krænkende ord og udtryk. Derudover kan redaktører bruge Dynamics 365 Commerce-webstedsgenerator til at implementere følgende manuelle opgaver:

- Moderere anmeldelser ved at reagere på dem eller fjerne dem.
- Slette en kundes anmeldelser på kundens anmodning.
- Masseimportere vurderings- og anmeldelsesdata for alle produkter i en Microsoft Power BI-skabelon, så tendenser for vurderinger og anmeldelser kan analyseres.

## <a name="read-a-review"></a>Læse en anmeldelse 

Følg disse trin for at læse en anmeldelse i Commerce-webstedsgenerator.

1. Gå til **Startside \> Anmeldelser \> Redigering**.
1. Brug søgefeltet øverst til højre på siden til at filtrere de anmeldelser, der vises efter produkt-id, produktnavn eller anmeldelsestekst.

Yderligere filtre giver dig mulighed for at begrænse anmeldelserne efter status periode, vurdering, kanal eller problem (fjernet, besvaret eller rapporteret).

![Startside for redigering](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a>Besvare en anmeldelse 

Kunder, der har købt et produkt, giver jævnligt udtryk for deres tilfredshed eller utilfredshed, eller angiver i nogle tilfælde, at de ikke forstår, hvordan produktet skal bruges. Som redaktør kan du sende et svar på en anmeldelse. Dette svar vises sammen med anmeldelsen på webstedet. 

Følg disse trin for at reagere på en anmeldelse i Commerce-webstedsgenerator.

1. Gå til **Startside \> Anmeldelser \> Redigering**.
1. Find og vælg den anmeldelse, der kræver et svar.
1. Vælg **Tilføj et svar** i egenskabsruden til højre.
1. Angiv svarteksten og det navn, der skal vises for respondenten. Respondentens navn er som standard **Redaktør**.
1. Vælg **Send svar**, når du er færdig.

![Besvare en anmeldelse](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a>Fjerne en anmeldelse 

Nogle gange kan redaktører være berettigede til at fjerne kunders anmeldelser af forretningsmæssige årsager. 

Følg disse trin for at fjerne en anmeldelse i Commerce-webstedsgenerator.

1. Gå til **Startside \> Anmeldelser \> Redigering**.
1. Find og vælg den anmeldelse, der skal fjernes.
1. Vælg en årsag til fjernelsen under **Fjern anmeldelse** i egenskabsruden til højre, og vælg derefter **Fjern**.
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a>Slette en kundes anmeldelser på kundens anmodning 

Nogle gange ønsker kunderne, at deres vurderings- og anmeldelsesdata slettes permanent fra et e-handelswebsted. En redaktør, der modtager en anmodning om fjernelse fra en kunde, kan fjerne kundens data ved hjælp af funktionen sletning af anmeldelser. Hvis du vil søge efter og slette en kundes data, skal redaktøren bruge den e-mailadresse, som kunden har brugt til at logge på og skrive anmeldelser. 

Hvis du vil finde og slette kundedata i Commerce-webstedsgenerator, skal du følge disse trin.

1. Gå til **Startside \> Anmeldelser \> Slet**.
1. Angiv kundens mailadresse i feltet **Søg efter brugere vha. mailadresse**, og vælg derefter **Søg**.
1. Hvis kunden har anmeldelsesaktivitet (f.eks. indsendelse af anmeldelser, tilkendegivelser om nytten af andre kunders anmeldelser eller kommentarer til en anden kundes anmeldelse), vises resultaterne. Knappen **Slet** vises for hvert element.
1. Vælg **Slet** for hvert element, der skal slettes. Når du bliver bedt om at bekræfte, skal du vælge **Ja**. 
    
![Slette kundedata](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - Det kan tage op til syv dage, før data er fjernet fuldstændigt fra systemet. Redaktører skal give kunderne besked om denne forsinkelse.
> - Hvis kunderne har ændret deres navn i deres kontoindstillinger, kan der blive vist flere elementer i søgeresultaterne. Hvis redaktøren i sådanne tilfælde vil slette kundens data fuldstændigt, skal han eller hun vælge **Slet** for hvert element. 

## <a name="download-ratings-and-reviews-data"></a>Hente vurderings- og anmeldelsesdata

Med Commerce-webstedsgenerator kan redaktører importere vurderings- og anmeldelsesdata samlet, så de kan analysere tendenser. En Power BI-skabelon, der indeholder grundlæggende metrikværdier, er tilgængelig. Redaktører kan bruge denne skabelon til at forbinde masseimporterede data med hinanden og få vist et dashboard. Det er ikke nødvendigt at oprette et brugerdefineret dashboard. Redaktører kan også tilpasse Power BI-skabelonen, så den opfylder deres specifikke behov. 

Hvis du vil downloade vurderings- og anmeldelsesdata i Commerce-webstedsgenerator, skal du følge disse trin.

1. Gå til **Startside \> Anmeldelser \> Rapportering**.
1. Vælg **Hent anmeldelsesdata** for at hente vurderings- og anmeldelsesdata samlet i CSV-format (semikolonseparerede værdier).

## <a name="view-ratings-and-reviews-trends"></a>Se vurderings- og anmeldelsestendenser

Redaktører kan hente Power BI-skabelonen, så de kan få vist tendenser i et dashboard.

Hvis du vil se vurderings- og anmeldelsestendenser i Commerce-webstedsgenerator, skal du følge disse trin.

1. Gå til **Startside \> Anmeldelser \> Rapportering**.
1. Vælg **Power BI-skabelon** for at hente skabelonen.

    ![Hent Power BI-skabelonen](media/rnr-moderation-reports.png) 

1. Åbn den hentede skabelon ved hjælp af Power BI-appen. Luk dialogboksen **Adgang til webindhold**, der vises, og luk derefter fejlmeddelelsen "Opdater", der vises.
1. Gå til **Startside**, vælg **Rediger forespørgsler**, og vælg derefter **indstillinger for datakilde**.
1. Vælg **Skift kilde** i dialogboksen **Indstillinger for datakilde**.
1. I feltet **URL-adresse** skal du angive stien til de anmeldelsesdata, du hentede i den forrige procedure (f.eks **C:\\Anmeldelser\\Anmeldelsesdata.csv**).

    ![Felt med URL-adresse i dialogboksen Kommaseparerede værdier](media/rnr-powerbi-datasource-settings.png) 

1. Vælg **OK**, og vælg derefter **Anvende ændringer**. Det tager ét til to minutter at anvende ændringerne på datakilden.
1. Vælg **Tendensark** for at få vist tendenser for vurderinger og anmeldelser.

    ![Tendenser i vurderinger og anmeldelser](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Tilvælge brug af vurderinger og anmeldelser](opt-in-ratings-reviews.md)

[Konfigurere vurderinger og anmeldelser](configure-ratings-reviews.md)

[Synkronisere produktvurderinger i Dynamics 365 Retail](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]