---
title: Integreret kreditormaster
description: I dette emne beskrives integrationen af kreditordata mellem Finance and Operations-apps og Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 636bc57b5ef09d605744f4857fd5fbefceac4875
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685479"
---
# <a name="integrated-vendor-master"></a>Integreret kreditormaster

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Termen *Kreditor* henviser til en leverandørorganisation eller en solovirksomhed, der leverer varer eller ydelser til en virksomhed. Selvom *kreditor* er et etableret koncept i Microsoft Dynamics 365 Supply Chain Management, findes der ikke et kreditorkoncept i andre modelbaserede apps i Dynamics 365. Du kan dog også overbelaste **Konto/Kontaktperson**-enheden, når du vil gemme kreditoroplysninger. Den integrerede kreditormaster introducerer et eksplicit leverandørbegreb i modelbaserede apps i Dynamics 365. Du kan enten bruge det nye leverandørdesign eller gemme leverandørdata i enheden **Konto/Kontaktperson**. Dobbeltskrivning understøtter begge metoder.

I begge fremgangsmåder integreres leverandørdataene mellem Dynamics 365 Supply Chain Management-, Dynamics 365 Sales-, Dynamics 365 Field Service- og Power Apps-portaler. I Supply Chain Management er data tilgængelige i arbejdsgange, f.eks. indkøbsrekvisitioner og indkøbsordrer.

## <a name="vendor-data-flow"></a>Kreditordataflow

Hvis du ikke vil gemme leverandørdata i enheden **Konto/Kontaktperson** i Dataverse, kan du bruge det nye leverandørdesign.

![Kreditordataflow](media/dual-write-vendor-data-flow.png)

Hvis du fortsat vil gemme leverandørdata i enheden **Konto/Kontaktperson**, kan du bruge det udvidede leverandørdesign. Hvis du vil bruge det udvidede leverandørdesign, skal du konfigurere leverandørarbejdsgangene i Dobbeltskrivnings-løsningspakken. Du kan finde flere oplysninger i [Skifte mellem kreditordesign](vendor-switch.md).

![Udvidet kreditordataflow](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Hvis du bruger Power Apps-portaler til leverandørselvbetjening, kan kreditoroplysningerne flyde direkte til Finance and Operations-apps.

## <a name="templates"></a>Skabeloner

Kreditordata indeholder alle oplysninger om kreditoren, f.eks kreditorens gruppe, adresser, kontaktoplysninger, betalingsprofil og fakturaprofil. En samling af tabeltilknytninger arbejder sammen under interaktion med kreditordata, som vist i følgende tabel.

Finance and Operations-apps | Andre Dynamics 365-apps     | Beskrivelse
----------------------------|-----------------------------|------------
Kreditor V2                   | Konto                     | Virksomheder, der bruger kontoenheden til at gemme kreditoroplysninger, kan fortsætte med at bruge den på samme måde. De kan også drage fordel af den eksplicitte kreditorfunktionalitet, der leveres med integrationen af Finance and Operations-apps.
Kreditor V2                   | Msdyn\_vendors              | Virksomheder, der bruger en tilpasset løsning til kreditorer, kan drage fordel af det standardkoncept for kreditorer, der introduceres i Dataverse, på grund af integrationen af Finance and Operations-apps. 
Kreditorgrupper               | msdyn\_vendorgroups         | Denne skabelon synkroniserer oplysninger om leverandørgrupper.
Kreditorbetalingsmetode       | msdyn\_vendorpaymentmethods | Denne skabelon synkroniserer oplysninger om leverandørers betalingsmetoder.
CDS kontakter V2             | kontakter                    | Denne [skabelon for kontakter](customer-mapping.md#cds-contacts-v2-to-contacts) synkroniserer alle primære, sekundære og tertiære kontaktoplysninger for både kunder og leverandører.
Betalingsplanlinjer      | msdyn\_paymentschedulelines | Denne [skabelon for betalingsskemalinjer](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) synkroniserer referencedata for betalingsskemaer for både kunder og leverandører.
Betalingsplan            | msdyn\_paymentschedules     | Denne [skabelon for betalingsskemaer](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) synkroniserer referencedata for betalingsskemaer for både kunder og leverandører.
Betalingsdagslinjer CDS V2    | msdyn\_paymentdaylines      | Denne [skabelon for betalingsdagslinjer](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) synkroniserer referencedata for betalingsdagslinjer for både kunder og leverandører.
Betalingsdage CDS            | msdyn\_paymentdays          | Denne [skabelon for betalingsdage](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) synkroniserer referencedata for betalingsdage for både kunder og leverandører.
Betalingsbetingelse            | msdyn\_paymentterms         | Denne [skabelon for betalingsbetingelser](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) synkroniserer referencedata for betalingsbetingelser for både kunder og leverandører.
Foranstillede navne                | msdyn\_nameaffixes          | Denne [skabelon for foranstillede navne](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) synkroniserer referencedata for foranstillede navne for både kunder og leverandører.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
