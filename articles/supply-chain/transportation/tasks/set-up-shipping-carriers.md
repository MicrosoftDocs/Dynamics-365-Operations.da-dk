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
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1ec19288f01ceb0bb3021cf549af1c38746785c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233577"
---
# <a name="set-up-shipping-carriers"></a>Konfigurere fragtmænd

[!include [banner](../../includes/banner.md)]

I dette emne beskrives, hvordan du kan konfigurere en fragtmand og definere detaljer som tjeneste, forsendelsestilstand, transporttilbud, transportbegrænsninger og forsendelsessats. Derefter kan en transportkoordinator tildele en fragtmand til en indgående eller udgående last.


## <a name="create-a-new-shipping-carrier"></a>Opret en ny fragtmand
1. Gå til **Navigationsrude > Moduler > Transportstyring > Opsætning > Fragtmænd > Fragtmænd**.
2. Vælg **Ny** i handlingsrude.
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]