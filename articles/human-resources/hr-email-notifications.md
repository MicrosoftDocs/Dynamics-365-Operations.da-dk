---
title: Mailbesked om frynsegoder
description: Denne artikel indeholder en oversigt over mailbesked i frynsegodeadministration i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d550cbb2f639535dbb43765c9fb0632a514fbe8c
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229894"
---
# <a name="benefits-email-notification"></a>Mailbesked om frynsegoder

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [banner](../includes/preview-banner.md)]

Mailbeskedfunktionen gør det muligt at sende mailbeskeder og påmindelser til medarbejdere i følgende situationer:

- Tilmelding af nyansat
- Åben tilmelding
- Kvalificerende livshændelser

Du kan oprette og angive flere mailskabeloner og sende beskederne ved hjælp af arbejdsområdet **Frynsegodeadministration** og siden **Arbejderpersonalegoder**. Du kan også spore historikken for beskeder/påmindelser.

## <a name="set-up-human-resources-shared-parameters"></a>Konfigurere delte parametre for Personale

På siden **Delte parametre for personale** kan du oprette mailskabeloner for frynsegoder til forskellige typer kommunikation, der sendes til medarbejdere eller medarbejdergrupper.

## <a name="create-a-new-email-id-template"></a>Oprette en ny skabelon for mail-id

Benyt følgende fremgangsmåde for at oprette en ny skabelon for mail-id.

1. Gå til **Skabelon til systemmail**.
2. Vælg **Ny**.
3. Angiv et navn i feltet **Mail-id**.
4. Angiv de andre felter efter behov.
5. Vælg **E-mailbesked** for at uploade skabelonen.
6. På siden **Delte parametre i personale** skal du vælge den nye skabelon under **Systemskabeloner** og flytte den under **Skabeloner til frynsegoder**.

## <a name="send-email-to-employees"></a>Sende mail til medarbejdere

Hvis du vil sende en mail til en nyansat, der endnu ikke er startet, skal du følge disse trin.

1. Åbn arbejdsområdet **Personalegodeadministration**.
2. Vælg feltet for den gruppe medarbejdere, du vil sende mailen til.
3. Vælg **Send mail**.
4. Vælg de medarbejdere, du vil sende mailen til.
5. Vælg **Send mail**.
6. Vælg den skabelon, du vil bruge.
7. Vælg **OK** for at sende mailen.

    Du kan gennemse mailmeddelelsen og status fra medarbejderens side **Frynsegodeplaner for arbejder** eller ved at vælge **Mailhistorik for frynsegoder** i afsnittet **Links** i arbejdsområdet **Personalegodeadministration**. Du kan også sende mailen fra siden **Personalegodeplaner for arbejder**.

8. Du kan få vist mailhistorikken for frynsegoder i arbejdsområdet **Personalegodeadministration** i sektionen **Links** ved at vælge **Mailhistorik for frynsegoder**.
9. Se hele mailhistorikken for mailmeddelelser om frynsegoder, der er sendt. Hvis du vil gennemse mailens indhold, skal du vælge **Vis meddelelse**.
10. Vælg **Arbejder**.
11. På siden **Personalegodeplaner for arbejder** kan du sende mail og se mailhistorikken for frynsegoder.

Arbejdsområdet **Personalegodeadministration** indeholder forskellige felter. Du kan sende mails ved at vælge den relaterede skabelon. Hvis mailmeddelelser om nyansættelser er sendt, skal du vælge feltet **Nyansat er ikke startet** og derefter vælge linket **Send påmindelse**. Du kan vælge en påmindelsesskabelon og angive titlen på beskeden som en første, anden eller tredje påmindelse.
