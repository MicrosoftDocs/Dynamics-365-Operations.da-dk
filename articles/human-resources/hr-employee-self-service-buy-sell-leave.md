---
title: Køb og sælg orlov
description: I Dynamics 365 Human Resources kan du sende anmodninger om køb og salg af orlov på grundlag af de politikker for køb og salg af orlov, der er konfigureret af din virksomhed.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d32abacc1539cb930ad6f1ebcfe6fa9af4befcf
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271473"
---
# <a name="buy-and-sell-leave"></a>Køb og sælg orlov

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I Dynamics 365 Human Resources kan du sende anmodninger om køb og salg af orlov på grundlag af de politikker for køb og salg af orlov, der er konfigureret af din virksomhed.  

## <a name="request-to-buy-leave"></a>Anmod om at købe orlov

1. I arbejdsområdet **Medarbejderselvbetjening** skal du vælge **Anmodning om at købe orlov** i feltet **Fritidssaldi**. 

2. Tilføj en **Orlovstype**, og angiv et **Antal** for det antal orlovsdage, du vil købe. 

3. Vælg **Send**, når du er klar til at sende din anmodning. 

Dine saldi opdateres enten automatisk eller gennem en godkendelsesproces, inden de opdateres. Dette afhænger af, hvordan købspolitikken er konfigureret.

## <a name="request-to-sell-leave"></a>Anmode om at sælge orlov

1. I arbejdsområdet **Medarbejderselvbetjening** skal du vælge **Anmodning om at sælge orlov** i feltet **Fritidssaldi**. 

2. Tilføj en **Orlovstype**, og angiv et **Antal** for det antal orlovsdage, du vil sælge. 

3. Vælg **Send**, når du er klar til at sende din anmodning.

Dine saldi opdateres enten automatisk eller gennem en godkendelsesproces, inden de opdateres. Dette afhænger af, hvordan købspolitikken er konfigureret.


## <a name="troubleshooting"></a>Fejlfinding 

Hvis en arbejdsgang for anmodning om køb eller salg af orlov mislykkes, kan brugere med rettigheden **EssLeaveBuySellRequestApprover** gennemse meddelelsesloggen for alle anmodninger om køb og salg af orlov. Hvis du vil gøre det, skal du gå til **Orlov og fravær > Link > Anmodninger om køb og salg af orlov > Meddelelseslog** (øverst til venstre). **Meddelelsesloggen** viser brugerne, hvordan transaktionerne blev behandlet, og den tilknyttede arbejdsgangshistorik.


## <a name="see-also"></a>Se også

[Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)</br>
[Administrere politikker for køb og salg af orlov](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
