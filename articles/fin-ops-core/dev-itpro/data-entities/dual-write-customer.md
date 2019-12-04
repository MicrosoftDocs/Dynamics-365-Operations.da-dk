---
title: Integreret debitormaster
description: I dette emne beskrives integrationen af debitordata mellem Finance and Operations og Common Data Service.
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
ms.openlocfilehash: 09d985e5c6816ec0c718aaf418f4e85fb828f1c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769677"
---
# <a name="integrated-customer-master"></a>Integreret debitormaster

[!include [banner](../includes/banner.md)]

Det er typisk, at debitorposter styres i mere end ét program. F.eks. kan salgsaktivitet indlæse kommercielle debitorposter via et Sales-program, og e-handel eller detailsalg kan indlæse debitorposter via et Finance and Operations-program. Uanset hvor debitorposten stammer fra, er den integreret i baggrunden på tværs af applikationsgrænser og infrastrukturforskelle. Integreret debitor-mastering hjælper med at håndtere multi-mastering-scenarier og giver en omfattende visning af debitoren i Dynamics 365-programpakken.

## <a name="customer-data-flow"></a>Debitordataflow

*Debitor* er et veldefineret begreb i programmer. Derfor involverer integrationen af debitordata blot en harmonisering af debitorkonceptet mellem de to programmer. Følgende illustration viser debitordataflowet.

![Debitordataflow](media/dual-write-customer-data-flow.png)

Debitorer kan groft inddeles i to typer: kommercielle/organisatoriske debitorer og forbrugere/slutbrugere. Disse to typer af debitorer lagres og håndteres forskelligt i Finance and Operations og Common Data Service.

I Finance and Operations styres både kommercielle/organisatoriske debitorer og forbrugere/slutbrugere i en enkelt tabel med navnet **CustTable** (CustomerCustomerV3Entity), og de klassificeres ud fra attributten **Type**. (Hvis **Type** er angivet til **Organisation**, er debitoren en kommerciel/organisatorisk kunde, og hvis **Type** er angivet til **Person**, er debitoren en forbruger/slutbruger). Oplysningerne om den primære kontaktperson håndteres via enheden SMMContactPersonEntity.

I Common Data Service bliver kommercielle/organisatoriske kunder styret i kontoenheden og identificeres som debitorer, når attributten **RelationshipType** er angivet til **Debitor.** Både forbrugere/slutbrugere og kontaktpersonen repræsenteres af kontaktenheden. Hvis du vil have en klar adskillelse mellem en forbruger/slutbruger og en kontaktperson, har enheden **Kontakt** et boolesk flag med navnet **Salgbar**. Når **Salgbar** er **Sand**, er kontakten en forbruger/slutbruger, og der kan oprettes tilbud og ordrer for den pågældende kontakt. Når **Salgbar** er **Falsk**, er kontakten kun en primær kontaktperson for en kunde.

Når en kontakt, der ikke er salgbar, deltager i et tilbud eller en ordreproces, angives **Salgbar** til **Sand** for at markere kontakten som en salgbar kontakt. En kontakt, der er blevet en salgbar kontakt, forbliver en salgbar kontakt.

## <a name="templates"></a>Skabeloner

Debitordata indeholder alle oplysninger om debitoren, f.eks debitorens gruppe, adresser, kontaktoplysninger, betalingsprofil, fakturaprofil og fordelskundestatus. En samling af enhedstilknytninger fungerer sammen under interaktion med debitordata, som vist i følgende tabel.

Finance and Operations-apps | Andre Dynamics 365-apps         | Beskrivelse
----------------------------|---------------------------------|------------
CDS kontakter V2             | kontakter                        | Denne skabelon synkroniserer alle primære, sekundære og tertiære kontaktoplysninger for både kunder og leverandører.
Debitorgrupper             | msdyn_customergroups            | Denne skabelon synkroniserer kundegruppeoplysninger.
Debitorbetalingsmetode     | msdyn_customerpaymentmethods    | Denne skabelon synkroniserer kundebetalingsoplysninger.
Debitorer V3                | konti                        | Denne skabelon synkroniserer kundemasteroplysninger for kommercielle og organisatoriske kunder.
Debitorer V3                | kontakter                        | Denne skabelon synkroniserer kundemasterdata for forbrugere og slutbrugere.
Fordelskundekort                | msdyn_loyaltycards              | Denne skabelon synkroniserer oplysninger om fordelskundekort.
Foranstillede navne                | msdyn_nameaffixes               | Denne skabelon synkroniserer referencedata for foranstillede navne for både kunder og leverandører.
Betalingsdagslinjer CDS V2    | msdyn_paymentdaylines           | Denne skabelon synkroniserer betalingsdagslinjers referencedata for både kunder og leverandører.
Betalingsdage CDS            | msdyn_paymentdays               | Denne skabelon synkroniserer referencedata for linjer for betalingsdage for både kunder og leverandører.
Betalingsplanlinjer      | msdyn_paymentschedulelines      | Synkroniserer betalingsdagsskemalinjers referencedata for både kunder og leverandører.
Betalingsplan            | msdyn_paymentschedules          | Denne skabelon synkroniserer referencedata for betalingsskemaer for både kunder og leverandører.
Betalingsbetingelse            | msdyn_paymentterms              | Denne skabelon synkroniserer referencedata for betalingsbetingelser (betalingsvilkår) for både kunder og leverandører.

[!include [banner](../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](dual-write/CDSContactsV2-contacts.md)]

[!include [mapping customer group](dual-write/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](dual-write/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](dual-write/CustomersV3-accounts.md)]

[!include [mapping customer contacts](dual-write/CustomersV3-contacts.md)]

[!include [mapping loyalty card](dual-write/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](dual-write/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](dual-write/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](dual-write/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](dual-write/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](dual-write/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](dual-write/TermsofPayment-msdyn-paymentterms.md)]
