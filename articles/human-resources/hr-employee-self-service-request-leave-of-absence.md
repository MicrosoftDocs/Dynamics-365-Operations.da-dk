---
title: Anmode om orlov
description: Send anmodning om orlov.
author: twheeloc
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveofAbsenceRequestEntry, EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6c98246e94670dd5f882fcbbd1f269e57f66faf
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805281"
---
# <a name="request-a-leave-of-absence"></a>Anmode om orlov

>[!Important]
>De funktioner, der nævnes i denne artikel, er i øjeblikket tilgængelige for kunder med enkeltstående Dynamics 365 Human Resources. Nogle eller alle funktionerne vil være tilgængelige som en del af en fremtidig version af Finance-infrastrukturen efter Finance-frigivelse 10.0.26.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan sende en anmodning om orlov og se status for dine orlovsanmodninger i Dynamics 365 Human Resources.

## <a name="request-a-leave-of-absence"></a>Anmode om orlov

1. I arbejdsområdet **Selvbetjeningsservice** skal du vælge **Mere** (...) i feltet **Fritidssaldi**.

2. Hvis du vil sende en orlovsanmodning, skal du vælge **Orlovsanmodning**.

3. Indtast oplysninger om **Orlovstype**, **Startdato** og **Slutdato**.

4. Hvis du skal sende understøttende dokumentation, skal du vælge **Overfør** under **Vedhæftede filer**.

5. Angiv eventuelle oplysninger i **Kommentar**.

6. Vælg **Send**, når du er klar til at sende din anmodning. Ellers skal du vælge **Gem kladde**.


## <a name="view-leave-of-absence-request-status"></a>Få vist status for orlovsanmodning

1. I arbejdsområdet **Selvbetjeningsservice** skal du vælge **Mere** (...) i feltet **Fritidssaldi**.

2. Hvis du vil se dine orlovsanmodninger, skal du vælge **Vis orlovsanmodning**.

## <a name="update-a-leave-of-absence-request"></a>Opdatere en anmodning om orlov

1. I arbejdsområdet **Selvbetjeningsservice** skal du vælge **Mere (...)** i feltet **Orlov**.
2. Vælg den orlovsanmodning, der skal opdateres, og vælg derefter **Opdater orlov**.
3. Opdater værdien i feltet **Slutdato** for at forlænge eller forkorte orlovstiden.
4. Hvis slutdatoen er bekræftet, skal du angive indstillingen **Bekræft slutdato** til **Ja**.
5. Når indstillingen **Bekræft slutdato** er angivet til **Ja**, kan du uploade en meddelelse om returnering til arbejde. Markér derefter afkrydsningsfeltet for at bekræfte, at en meddelelse om returnering til arbejde er blevet uploadet.
6. Vælg **Send** for at opdatere orlovsanmodningen.

## <a name="cancel-a-leave-of-absence-request"></a>Annullere en anmodning om orlov

1. I arbejdsområdet **Selvbetjeningsservice** skal du vælge **Mere (...)** i feltet **Orlov**.
2. Vælg den orlovsanmodning, der skal annulleres, og vælg derefter **Opdater orlov**.
3. Angiv indstillingen **Annuller orlov** til **Ja**.
4. Vælg **Send** for at annullere orlovsanmodningen.

## <a name="importing-leave-requests-from-other-systems-or-older-systems"></a>Importere orlovsanmodninger fra andre systemer eller ældre systemer

Hvis du vil importere orlovsanmodninger fra et andet system, skal du gennemgå den almindelige arbejdsgang for at oprette de relevante orlovstransaktioner. Du kan også importere orlovsbanktransaktionerne og orlovsanmodningerne i afsluttet tilstand. Bemærk, at orlovsbanktransaktionerne ikke oprettes automatisk, hvis du kun importerer orlovsanmodningerne.

## <a name="see-also"></a>Se også

[Stop orlov midlertidigt](hr-leave-and-absence-suspend-leave.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
