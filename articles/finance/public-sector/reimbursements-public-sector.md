---
title: Refusioner i den offentlige sektor
description: Denne artikel besvarer almindelige spørgsmål i forbindelse med refusioner i den offentlige sektor.
author: JodiChristiansen
ms.date: 11/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 27311
ms.assetid: 9d61d1d8-1672-4bd0-ae0d-605b09240890
ms.search.industry: Public sector
ms.search.form: CustBillingClassification
ms.openlocfilehash: 4155d2a0ceb4e9b55bb1c9b2f04d15f43add8cc3
ms.sourcegitcommit: e25fe4228add88dd37f4f38ece86979e1c621f6a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2022
ms.locfileid: "9734310"
---
# <a name="reimbursements-in-the-public-sector"></a>Refusioner i den offentlige sektor

[!include [banner](../includes/banner.md)]

Denne artikel besvarer almindelige spørgsmål i forbindelse med refusioner i den offentlige sektor. 

## <a name="how-do-billing-classifications-affect-reimbursements-for-overpayments"></a>Hvordan påvirker faktureringsklassifikationer refusioner for overbetalinger?
Det gør de ikke. Faktureringsklassifikationer anvendes aldrig til debitorbetalinger, så de bruges ikke ved behandling af refusioner for overbetalinger.

## <a name="can-i-process-a-reimbursement-for-a-customer-who-has-outstanding-debit-transactions"></a>Er det muligt at behandle en refusion til en kunde, der har udestående debiteringer?
Ja. Hvis du vil behandle en refusion for en kunde med udestående debiteringer, skal du bruge filtre på siden refusion til at vælge debitoren og vælge indstillingen for at medtage debitorer med udestående debiteringer. Når du gør dette, oprettes refusionsposteringer for det fulde beløb af alle kundens kreditposteringer. De udestående debetbeløb er ikke trukket fra kreditbeløbene.

## <a name="can-i-process-reimbursements-for-customers-who-have-pending-settlements"></a>Kan jeg ikke behandle refusioner for kunder, der har ventende udligninger?
Nej. Refusioner behandles ikke for en kunde, der har ventende udligninger, der ikke er blevet bogført til journalen.

## <a name="can-i-reverse-reimbursement-settlements"></a>Kan jeg fortryde refusionsudligninger?
Nej, ikke direkte. Du kan dog bruge finanskladdeposter til at oprette posteringer, der ville medføre tilbageførsel af finansposterne.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
