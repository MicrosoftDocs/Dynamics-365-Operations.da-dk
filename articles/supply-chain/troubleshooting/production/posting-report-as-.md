---
title: Fejl, når færdigmeldingskladden bogføres
description: Når du bogfører færdigmeldingskladden, modtager du en fejlmeddelelse om, at det bestilte antal ikke kan reduceres.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026360"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a>Fejl, når færdigmeldingskladden bogføres

KB-nummer: 4612891

## <a name="symptoms"></a>Symptomer

Når du bogfører kladden **Færdigmelding**, opstår der en fejl, og du modtager følgende fejlmeddelelse:

> Det bestilte antal kan ikke nedsættes, da der ikke er nok åbne lagertransaktioner med status 'bestilt'. Elementerne er Købt, Modtaget eller Registreret.

Denne fejl opstår kun, når feltet **Antal fejl** er indstillet på første linje i **Færdigmelding**-kladden, og feltet **Antal gode** er indstillet på sidste linje. Hvis feltet **Antal fejl** er indstillet på den sidste linje, opstår der ingen fejl.

## <a name="resolution"></a>Løsning

Du kan forhindre denne fejl ved at åbne siden **Produktionsstyringsparametre** og derefter vælge **Ja** i indstillingen **Stigning forbliver antal med antal fejl** under fanen *Generelt*.
