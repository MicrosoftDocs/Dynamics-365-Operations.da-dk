---
title: Klientpåmindelsesbeskeder via e-mail
description: Dette emne indeholder oplysninger om, hvordan du opretter regler, der sender e-mailbeskeder om foruddefinerede hændelser, der indtræffer.
author: tjvass
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a1d520584e331631bb5a6a88ba6c9a8b50b3d29e
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798617"
---
# <a name="client-alert-notifications-by-email"></a>Klientpåmindelsesbeskeder via mail

[!include [banner](../includes/banner.md)]

Du kan definere brugerdefinerede regler for påmindelser, som overvåger filtrerede visninger af data og automatisk sender e-mailbeskeder, når foruddefinerede hændelser indtræffer. Muligheden for at sende mailbeskeder er tilgængelig for alle understøttede påmindelsestyper, og du kan også aktivere dem for eksisterende påmindelsesregler.

Du kan bruge indbyggede kontrolelementer til at oprette påmindelsesregler, der overvåger de filtrerede visninger af batchjob i systemet. Ved at overvåge værdien af feltet **Status** kan du også konfigurere regler for påmindelser, der sender e-mail, når der opstår fejl i et batchjob. Når disse påmindelsesregler er oprettet, behøver du ikke længere at kontrollere, om der er ændringer af forretningsdata i rapporter. Du kan i stedet lade den intelligente ændringsregistreringstjeneste foretage overvågning for dig.

Klientpåmindelser afhænger af det e-mailundersystem, der leveres via integration med Microsoft Office. Det anbefales, at du bruger SMTP-udbyderen (Simple Mail Transfer Protocol), så e-maildistribution ikke behøver at kræve en lokal mailklient.

Hvis du vil sende beskeder via e-mail, skal kunder konfigurere integrerede e-mailtjenester. E-mailbeskederne sendes til modtagerne på vegne af påmindelsesejere.

Yderligere oplysninger om, hvordan du kan konfigurere e-mail, finder du i [Konfigurere og sende e-mail](../organization-administration/configure-email.md).

Følgende billede viser **Opret påmindelsesregel** dialogboksen, som nu indeholder en **Send e-mail** indstilling.

[![Dialogboksen Opret påmindelsesregel, hvor indstillingen Send e-mail er sat til Ja](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Når **Send e-mail** er indstillet til **Ja**, bliver påmindelsesbeskeder fortsat leveret via Handlingscenter.

## <a name="alert-notification-email-templates"></a>E-mailskabeloner til påmindelsesbeskeder

Tjenesten sender e-mailbeskeder ved hjælp af foruddefinerede e-mailskabeloner, der leverer de grundlæggende oplysninger om påmindelsesbeskeden.

Følgende billede viser strukturen af påmindelsesbeskederne, når de modtages via mail.

[![Skabelonbaserede påmindelsesbeskeder til oprettelse af poster, ændringer af felter og sletning af skabelon](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]