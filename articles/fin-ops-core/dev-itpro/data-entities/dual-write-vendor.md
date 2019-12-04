---
title: Integreret kreditormaster
description: I dette emne beskrives integrationen af kreditordata mellem Finance and Operations-apps og Common Data Service.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: da451c63c23444da564307505d38699faf9df19a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770973"
---
# <a name="integrated-vendor-master"></a>Integreret kreditormaster

[!include [banner](../includes/banner.md)]

Udtrykket *kreditor* refererer til en leverandørorganisation eller en eneindehaver, der er en del af forsyningskædens proces, og som leverer varer til virksomheden. Selvom *kreditor* er et etableret koncept i Finance and Operations-apps, findes der ikke et kreditorkoncept i andre Dynamics 365-apps. I stedet overbelaster nogle virksomheder kontoenheden for at gemme både debitoroplysninger og kreditoroplysninger. Andre virksomheder bruger et eget tilpasset kreditorkoncept. Common Data Service-integration understøtter begge disse design. Du kan derfor aktivere et af designene, afhængigt af dit forretningsscenarie.

Integration af leverandørdata mellem Finance and Operations-apps og andre Dynamics 365-apps giver dig mulighed for at håndtere flere data. Uanset hvor kreditordataene stammer fra, er de integreret i baggrunden på tværs af applikationsgrænser og infrastrukturforskelle. 

### <a name="vendor-data-flow"></a>Kreditordataflow

Hvis du vil bruge andre Dynamics 365-apps til leverandørhåndtering, og du vil adskille leverandøroplysninger fra kundeoplysninger, kan du bruge det nye leverandørdesign.

![Kreditordataflow](media/dual-write-vendor-data-flow.png)

Hvis du vil bruge andre Dynamics 365-apps til leverandørhåndtering, og du fortsat vil bruge kontoenheden til at gemme leverandøroplysninger, kan du bruge det nye udvidede leverandørdesign. I dette design gemmes udvidede kreditoroplysninger som f. eks kreditorgruppe og kreditorposteringsprofil i kreditordetaljerne.

![Udvidet kreditordataflow](media/dual-write-vendor-detail.jpg)

Kreditorkontaktoplysninger ligner leverandørkontaktoplysninger. Kontaktoplysningerne gemmes i baggrunden, og de hentes fra de samme enheder.

## <a name="templates"></a>Skabeloner

Kreditordata indeholder alle oplysninger om kreditoren, f.eks kreditorens gruppe, adresser, kontaktoplysninger, betalingsprofil og fakturaprofil. En samling af enhedstilknytninger arbejder sammen under interaktion med kreditordata, som vist i følgende tabel.

Finance and Operations-apps | Andre Dynamics 365-apps         | Beskrivelse
----------------------------|---------------------------------|------------
Kreditor V2               | Konto | Virksomheder, der bruger kontoenheden til at gemme kreditoroplysninger, kan fortsætte med at bruge den på samme måde. De kan også drage fordel af den eksplicitte leverandørfunktionalitet, der leveres med integrationen af Finance and Operations-apps.
Kreditor V2               | Msdyn\_vendors | Virksomheder, der bruger en tilpasset løsning til leverandører, kan drage fordel af det standardkoncept for leverandører, der introduceres i Common Data Service på grund af integrationen af Finance and Operations-apps. 
Kreditorgrupper | msdyn_vendorgroups | Denne skabelon synkroniserer oplysninger om leverandørgrupper.
Kreditorbetalingsmetode | msdyn_vendorpaymentmethods | Denne skabelon synkroniserer oplysninger om leverandørers betalingsmetoder.
CDS kontakter V2             | kontakter                        | Denne [skabelon for kontakter](dual-write-customer.md#cds-contacts-v2-to-contacts) synkroniserer alle primære, sekundære og tertiære kontaktoplysninger for både kunder og leverandører.
Betalingsplanlinjer      | msdyn_paymentschedulelines      | Denne [skabelon for betalingsskemalinjer](dual-write-customer.md#payment-schedule-lines-to-msdyn_paymentschedulelines) synkroniserer referencedata for betalingsskemaer for både kunder og leverandører.
Betalingsplan            | msdyn_paymentschedules          | Denne [skabelon for betalingsskemaer](dual-write-customer.md#payment-schedule-to-msdyn_paymentschedules) synkroniserer referencedata for betalingsskemaer for både kunder og leverandører.
Betalingsdagslinjer CDS V2    | msdyn_paymentdaylines           | Denne [skabelon for betalingsdagslinjer](dual-write-customer.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) synkroniserer referencedata for betalingsdagslinjer for både kunder og leverandører.
Betalingsdage CDS            | msdyn_paymentdays               | Denne [skabelon for betalingsdage](dual-write-customer.md#payment-days-cds-to-msdyn_paymentdays) synkroniserer referencedata for betalingsdage for både kunder og leverandører.
Betalingsbetingelse            | msdyn_paymentterms              | Denne [skabelon for betalingsbetingelser](dual-write-customer.md#terms-of-payment-to-msdyn_paymentterms) synkroniserer referencedata for betalingsbetingelser for både kunder og leverandører.
Foranstillede navne                | msdyn_nameaffixes               | Denne [skabelon for foranstillede navne](dual-write-customer.md#name-affixes-to-msdyn_nameaffixes) synkroniserer referencedata for foranstillede navne for både kunder og leverandører.

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [Vendors](dual-write/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](dual-write/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](dual-write/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
