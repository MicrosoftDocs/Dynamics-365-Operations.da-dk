---
title: Konfigurere fragtmænd
description: I dette emne beskrives, hvordan du kan konfigurere en fragtmand og definere detaljer som tjeneste, forsendelsestilstand, transporttilbud, transportbegrænsninger og forsendelsessats.
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e6a29dce877a53d125c5a151da6cfbb13d46b29
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201588"
---
# <a name="set-up-shipping-carriers"></a>Konfigurere fragtmænd

[!include [banner](../../includes/banner.md)]

I dette emne beskrives, hvordan du kan konfigurere en fragtmand og definere detaljer som tjeneste, forsendelsestilstand, transporttilbud, transportbegrænsninger og forsendelsessats. Derefter kan en transportkoordinator tildele en fragtmand til en indgående eller udgående last.


## <a name="create-a-new-shipping-carrier"></a>Opret en ny fragtmand
1. Gå til **Navigationsrude > Moduler > Transportstyring > Opsætning > Fragtmænd > Fragtmænd**.
2. Vælg **Ny** i handlingsruden.
3. Skriv en værdi i feltet **Fragtmand**.
4. Skriv en værdi i feltet **Navn**.
5. Vælg en indstilling på rullelisten i feltet **Måde**.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Udfyld generelle oplysninger om fragtmanden
1. Slå udvidelsen af sektionen **Oversigt** til/fra.
2. Markér eller fjern markeringen i afkrydsningsfeltet **Aktivér fragtmand**.
3. Vælg en indstilling på rullelisten i feltet **Kreditorkonto**. Vælg kreditorkontoen, som fragtmanden skal tildeles.  
4. Vælg en indstilling i feltet **Transporttilbudstype**. Vælg **Manuelt** for at bruge siden Transporttilbud, eller vælg **EDI** for opdatere tilbuddet ved hjælp af EDI (Electronic Data Interchange).  
5. Markér eller fjern markeringen i afkrydsningsfeltet **Aktivér fragtmandssatser**.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Opret de nødvendige tjenester for fragtmanden
1. Slå udvidelsen af sektionen afsnittet **Tjenester** til/fra.
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Fragttjeneste**.
4. Skriv en værdi i feltet **Navn**.
5. Vælg en indstilling på rullelisten i feltet **Transportmetode**.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Konfigurer adressen for fragtmanden (valgfrit)
1. Slå udvidelsen af sektionen **Adresser** til/fra.
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Navn eller beskrivelse**.
4. Vælg en indstilling på rullelisten i feltet **Land/område**.
5. Vælg en indstilling på rullelisten i feltet **Postnummer**.
6. Skriv en værdi i feltet **Gade**.
7. Vælg **OK**.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Konfigurer vurderingsprofil for fragtmanden
1. Slå udvidelsen af sektionen **Vurderingsprofiler** til/fra.
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Vurderingsprofil**.
4. Skriv en værdi i feltet **Navn**.
5. Vælg en indstilling på rullelisten i feltet **Sted**.
6. Vælg en indstilling på rullelisten i feltet **Lagersted**.
7. Vælg en indstilling på rullelisten i feltet **Satsprogram**. Vælg det Satsprogram, der er i overensstemmelse med den kontrakt, du har lavet med fragtmanden.  
8. Vælg en indstilling på rullelisten i feltet **Satsmaster**.
9. Vælg en indstilling på rullelisten i feltet **Program til transittid**.
10. Vælg **Gem**.

