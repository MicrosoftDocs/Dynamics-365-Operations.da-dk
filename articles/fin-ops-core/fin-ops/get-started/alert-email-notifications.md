---
title: Klientpåmindelsesbeskeder via mail
description: Denne artikel indeholder oplysninger om, hvordan du opretter regler, der sender e-mailbeskeder om foruddefinerede hændelser, der indtræffer.
author: RichdiMSFT
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 469c7fdda40780d6e559819103d73d7a4e7132a1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878272"
---
# <a name="client-alert-notifications-by-email"></a>Klientpåmindelsesbeskeder via mail

[!include [banner](../includes/banner.md)]

Du kan definere brugerdefinerede regler for påmindelser, som overvåger filtrerede visninger af data og automatisk sender e-mailbeskeder, når foruddefinerede hændelser indtræffer. Muligheden for at sende mailbeskeder er tilgængelig for alle understøttede påmindelsestyper, og du kan også aktivere dem for eksisterende påmindelsesregler.

Du kan bruge indbyggede kontrolelementer til at oprette påmindelsesregler, der overvåger de filtrerede visninger af batchjob i systemet. Ved at overvåge værdien af feltet **Status** kan du også konfigurere regler for påmindelser, der sender e-mail, når der opstår fejl i et batchjob. Når disse påmindelsesregler er oprettet, behøver du ikke længere at kontrollere, om der er ændringer af forretningsdata i rapporter. Du kan i stedet lade den intelligente ændringsregistreringstjeneste foretage overvågning for dig.

Klientpåmindelser afhænger af det e-mailundersystem, der leveres via integration med Microsoft Office. Det anbefales, at du bruger SMTP-udbyderen (Simple Mail Transfer Protocol), så e-maildistribution ikke behøver at kræve en lokal mailklient.

Hvis du vil sende beskeder via e-mail, skal kunder konfigurere integrerede e-mailtjenester. E-mailbeskederne sendes til modtagerne på vegne af påmindelsesejere.

Yderligere oplysninger om, hvordan du kan konfigurere e-mail, finder du i [Konfigurere og sende e-mail](../organization-administration/configure-email.md).

Følgende billede viser **Opret påmindelsesregel** dialogboksen, som nu indeholder en **Send e-mail** indstilling.

[![Dialogboksen Opret påmindelsesregel, hvor indstillingen Send e-mail er sat til Ja.](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Når **Send e-mail** er indstillet til **Ja**, bliver påmindelsesbeskeder fortsat leveret via Handlingscenter.

## <a name="alert-notification-email-templates"></a>E-mailskabeloner til påmindelsesbeskeder

Tjenesten sender e-mailbeskeder ved hjælp af foruddefinerede e-mailskabeloner, der leverer de grundlæggende oplysninger om påmindelsesbeskeden.

Følgende billede viser strukturen af påmindelsesbeskederne, når de modtages via mail.

[![Skabelonbaserede påmindelsesbeskeder til oprettelse af poster, ændringer af felter og sletning af skabelon.](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]