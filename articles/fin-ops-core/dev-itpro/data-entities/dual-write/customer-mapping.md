---
title: Integreret debitormaster
description: I dette emne beskrives integrationen af debitordata mellem Finance and Operations og Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 0b78b6071a354fef91573455f03b908d8b09a525299daef62d9a4f49752e6c03
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725154"
---
# <a name="integrated-customer-master"></a>Integreret kundemaster

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Debitordata kan styres i mere end ét Dynamics 365-program. En debitorrække kan f.eks. stamme fra en salgsaktivitet i Dynamics 365 Sales (en Customer Engagement-app), eller en række kan stamme fra detailaktivitet i Dynamics 365 Commerce (en Finance and Operations-app). Uanset hvor debitordataene stammer fra, integreres de i baggrunden. Integreret kundemaster giver dig fleksibiliteten til at administrere debitordata i ethvert Dynamics 365-program og giver en omfattende oversigt over kunden på tværs af Dynamics 365-programpakken.

## <a name="customer-data-flow"></a>Debitordataflow

*Debitor* er et veldefineret begreb i programmer. Derfor involverer integrationen af debitordata blot en harmonisering af debitorkonceptet mellem de to programmer. Følgende illustration viser debitordataflowet.

![Debitordataflow.](media/dual-write-customer-data-flow.png)

Debitorer kan groft inddeles i to typer: kommercielle/organisatoriske debitorer og forbrugere/slutbrugere. Disse to typer af debitorer lagres og håndteres forskelligt i Finance and Operations og Dataverse.

I Finance and Operations  styres både kommercielle/organisatoriske debitorer og forbrugere/slutbrugere i en enkelt tabel med navnet **CustTable** (CustCustomerV3Entity), og de klassificeres ud fra attributten **Type**. (Hvis **Type** er angivet til **Organisation**, er debitoren en kommerciel/organisatorisk kunde, og hvis **Type** er angivet til **Person**, er debitoren en forbruger/slutbruger). Oplysningerne om den primære kontaktperson håndteres via tabellen SMMContactPersonEntity.

I Dataverse bliver kommercielle/organisatoriske kunder styret i kontotabellen og identificeres som debitorer, når attributten **RelationshipType** er angivet til **Debitor.** Både forbrugere/slutbrugere og kontaktpersonen repræsenteres af kontakttabellen. Hvis du vil have en klar adskillelse mellem en forbruger/slutbruger og en kontaktperson, har tabellen **Kontakt** et boolesk flag med navnet **Salgbar**. Når **Salgbar** er **Sand**, er kontakten en forbruger/slutbruger, og der kan oprettes tilbud og ordrer for den pågældende kontakt. Når **Salgbar** er **Falsk**, er kontakten kun en primær kontaktperson for en kunde.

Når en kontakt, der ikke er salgbar, deltager i et tilbud eller en ordreproces, angives **Salgbar** til **Sand** for at markere kontakten som en salgbar kontakt. En kontakt, der er blevet en salgbar kontakt, forbliver en salgbar kontakt.

## <a name="templates"></a>Skabeloner

Debitordata indeholder alle oplysninger om debitoren, f.eks debitorens gruppe, adresser, kontaktoplysninger, betalingsprofil, fakturaprofil og fordelskundestatus. En samling af tabeltilknytninger fungerer sammen under interaktion med debitordata, som vist i følgende tabel.

Finance and Operations-apps | Kundeengagementapps         | Betegnelse
----------------------------|---------------------------------|------------
[CDS kontakter V2](mapping-reference.md#115) | kontakter | Denne skabelon synkroniserer alle primære, sekundære og tertiære kontaktoplysninger for både kunder og leverandører.
[Debitorgrupper](mapping-reference.md#126) | msdyn_customergroups | Denne skabelon synkroniserer kundegruppeoplysninger.
[Debitorbetalingsmetode](mapping-reference.md#127) | msdyn_customerpaymentmethods | Denne skabelon synkroniserer kundebetalingsoplysninger.
[Debitorer V3](mapping-reference.md#101) | konti | Denne skabelon synkroniserer kundemasteroplysninger for kommercielle og organisatoriske kunder.
[Debitorer V3](mapping-reference.md#116) | kontakter | Denne skabelon synkroniserer kundemasterdata for forbrugere og slutbrugere.
[Foranstillede navne](mapping-reference.md#155) | msdyn_nameaffixes | Denne skabelon synkroniserer referencedata for foranstillede navne for både kunder og leverandører.
[Betalingsdagslinjer CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Denne skabelon synkroniserer betalingsdagslinjers referencedata for både kunder og leverandører.
[Betalingsdage CDS](mapping-reference.md#158) | msdyn_paymentdays | Denne skabelon synkroniserer referencedata for linjer for betalingsdage for både kunder og leverandører.
[Betalingsplanlinjer](mapping-reference.md#159) | msdyn_paymentschedulelines | Synkroniserer betalingsdagsskemalinjers referencedata for både kunder og leverandører.
[Betalingsplan](mapping-reference.md#160) | msdyn_paymentschedules | Denne skabelon synkroniserer referencedata for betalingsskemaer for både kunder og leverandører.
[Betalingsbetingelse](mapping-reference.md#161) | msdyn_paymentterms | Denne skabelon synkroniserer referencedata for betalingsbetingelser (betalingsvilkår) for både kunder og leverandører.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
