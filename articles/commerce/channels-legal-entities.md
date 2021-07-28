---
title: Opret juridiske enheder
description: Dette emne beskriver, hvordan du opretter juridiske enheder i Microsoft Dynamics 365 Commerce, som skal være oprettet og konfigureret, før du opretter kanaler.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 698c556b8839ae1d657ef02796fe08ab9cd3621e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346028"
---
# <a name="create-legal-entities"></a>Opret juridiske enheder

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du opretter juridiske enheder i Microsoft Dynamics 365 Commerce, som skal være oprettet og konfigureret, før du opretter kanaler.

En juridisk enhed er en organisation, der består af en registreret eller lovgivningsbaseret juridisk struktur. Juridiske enheder kan indgå juridisk bindende kontrakter og skal udarbejde opgørelser med afrapportering af deres præstation.

Et firma er en type juridisk enhed. I øjeblikket er firmaer den eneste slags juridiske enhed, som du kan oprette, og hver juridiske enhed får tilknyttet et firma-id. Denne tilknytning findes, da nogle funktionsområder i programmet bruger et firma-id, eller *DataAreaId* i deres datamodeller. Firmaer bruges som en afgrænsning for datasikkerhed i disse funktionsområder. Brugere har kun adgang til data for det firma, som de er logget på. 

Når du opretter en kanal, skal du angive den juridiske enhed, som kanalen tilhører.

## <a name="create-a-new-legal-entity"></a>Opret en ny juridisk enhed

Gør følgende for at oprette en ny juridisk enhed i Dynamics 365 Commerce.

1. Gå til **Moduler \> Konfiguration af hovedkontor \> Juridiske enheder** i navigationsruden.
1. Gå til handlingsruden, og vælg **Ny**. Ruden **Ny juridisk enhed** vises til højre.
1. Angiv en værdi i feltet **Navn**.
1. Angiv en værdi i feltet **Virksomhed**.
1. Indtast eller vælg en værdi i feltet **Land/område**.
1. Vælg **OK**. 

   ![Oprettelse af en juridisk enhed.](media/legal-entities.png)

1. Angiv følgende generelle oplysninger om den juridiske enhed i sektionen **Generelt**: 
   1. Angiv et søgenavn, hvis et søgenavn er påkrævet. Et søgenavn er et alternativt navn, der kan bruges til at søge efter den pågældende juridiske enhed. 
   1. Angiv, om den pågældende juridiske enhed skal bruges til et konsolideret regnskab.
   1. Angiv, om den pågældende juridiske enhed skal bruges til et elimineringsregnskab. 
   1. Vælg **standardsproget** for enheden. 
   1. Vælg **tidszonen** for enheden.
1. Vælg **Rediger** for at angive adresseoplysninger, som f.eks. gadenavn, husnummer, postnummer og by, i sektionen **Adresser**.
1. Angiv oplysninger om kommunikationsmåder som f.eks. mailadresser, URL-adresser og telefonnumre, i sektionen **Kontaktoplysninger**.
1. Angiv de registreringsnumre, der bruges til lovpligtig rapportering, i sektionen **Lovpligtig rapportering**.
1. Angiv de oplysninger, der kræves af den juridiske enhed, i sektionen **Registreringsnumre**.
1. Angiv bankkonti og registreringsnumre for den juridiske enhed, i sektionen **Bankkontooplysninger**.
1. Angiv forsendelsesoplysninger for den juridiske enhed, i sektionen **Udenrigshandel og logistik**.
1. Du kan se de nummerserier, der er tilknyttet den juridiske enhed, i sektionen **Nummerserier**. Dette er tomt fra starten.
1. Vis eller skift det logo og/eller dashboardbillede, der er tilknyttet den juridiske enhed, i sektionen **Dashboardbillede**.
1. Angiv de registreringsnumre, der bruges til rapportering til skattemyndigheder, i sektionen **Momsregistrering**.
1. Angiv 1099-oplysninger for den juridiske enhed i sektionen **1099-skat**.
1. Angiv momosoplysningerne for den juridisk enhed i sektionen **Momsoplysninger**.
1. Vælg **Gem**.

Følgende billede viser et eksempel på en juridisk enhed.

![Sektion for generel juridisk enhed.](media/legal-entities-general.png)
   
## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over organisationer og organisationshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Planlægge dit organisationshierarki](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Organisationshierarkier](channels-org-hierarchies.md)

[Oversigt over kanaler](channels-overview.md)

[Forudsætninger for konfiguration af kanal](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
