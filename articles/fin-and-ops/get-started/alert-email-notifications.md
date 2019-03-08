---
title: Klientpåmindelsesbeskeder via e-mail
description: Dette emne indeholder oplysninger om, hvordan du opretter regler, der sender e-mailbeskeder om foruddefinerede hændelser, der indtræffer.
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 314f04eec04a75aed058c9c38066738e8758f653
ms.sourcegitcommit: 440ebe14ad26574ba227d23ee8370f6b6110645b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2019
ms.locfileid: "373749"
---
# <a name="client-alert-notifications-by-email"></a>Klientpåmindelsesbeskeder via e-mail

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

I Microsoft Dynamics 365 for Finance and Operations kan du definere brugerdefinerede regler for påmindelser, som overvåger filtrerede visninger af data og automatisk sender e-mailbeskeder, når foruddefinerede hændelser indtræffer. Muligheden for at sende e-mailbeskeder er tilgængelig for alle understøttede typer af påmindelser og kan også aktiveres for eksisterende påmindelsesregler.

Du kan bruge indbyggede kontrolelementer til at oprette påmindelsesregler, der overvåger de filtrerede visninger af batchjob i systemet. Ved at overvåge værdien af feltet **Status** kan du også konfigurere regler for påmindelser, der sender e-mail, når der opstår fejl i et batchjob. Når disse påmindelsesregler oprettes, behøver du ikke længere at kontrollere, om der er ændringer af forretningsdata i rapporter. Du kan i stedet lade den intelligente ændringsregistreringstjeneste i Finance and Operations foretage overvågning for dig.

Klientpåmindelser afhænger af det e-mailundersystem, der leveres via integration med Microsoft Office. Det anbefales, at du bruger SMTP-udbyderen (Simple Mail Transfer Protocol), så e-maildistribution ikke behøver at kræve en lokal mailklient.

Hvis du vil sende beskeder via e-mail, skal kunder konfigurere integrerede e-mailtjenester. E-mailbeskederne sendes til modtagerne på vegne af påmindelsesejere.

Yderligere oplysninger om, hvordan du kan konfigurere e-mail i Finance and Operations, finder du i [Konfigurere og sende e-mail](../organization-administration/configure-email.md).

Følgende billede viser **Opret påmindelsesregel** dialogboksen, som nu indeholder en **Send e-mail** indstilling.

[![Dialogboksen Opret påmindelsesregel, hvor indstillingen Send e-mail er sat til Ja](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Når **Send e-mail** er indstillet til **Ja**, bliver påmindelsesbeskeder fortsat leveret via Handlingscenter.

## <a name="alert-notification-email-templates"></a>E-mailskabeloner til påmindelsesbeskeder

Tjenesten sender e-mailbeskeder ved hjælp af foruddefinerede e-mailskabeloner, der leverer de grundlæggende oplysninger om påmindelsesbeskeden. Disse oplysninger omfatter et direkte link til den side, hvor påmindelsesreglen blev defineret.

Følgende billede viser strukturen af påmindelsesbeskederne, når de modtages via e-mail.

[![Skabelonbaserede påmindelsesbeskeder til oprettelse af poster, ændringer af felter og sletning af skabelon](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)
