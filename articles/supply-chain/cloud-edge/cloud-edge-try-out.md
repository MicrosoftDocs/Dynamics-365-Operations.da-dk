---
title: Afprøve skalaenheder i en distribueret hybridtopologi
description: Denne artikel indeholder oplysninger om afprøvning af sky- og edge-skalaenheder til styring af arbejdsbyrder i produktion og lagersted.
author: perlynne
ms.date: 05/02/2022
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-03-03
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 5645955109e7a942e617b3b90a27065c2a8fe4a3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893578"
---
# <a name="try-out-scale-units-in-a-distributed-hybrid-topology"></a>Afprøve skalaenheder i en distribueret hybridtopologi

[!include [banner](../includes/banner.md)]

Processen for afprøvning af distribueret hybridtopologi er simpel. I første stadie skal du validere tilpasninger for at sikre, at de fungerer i den distribuerede topologi. Du har to muligheder.

## <a name="option-1-evaluate-customizations-in-development-environments"></a>Mulighed 1: Evaluere tilpasninger i udviklingsmiljøer

Før du starter onboarding af dine sandkassemiljøer, anbefales du at undersøge skalaenheder i en udviklingsopsætning, f.eks. et miljø med én boks (også kaldet niveau-1-miljø), så du kan validere processer, tilpasninger og løsninger. I dette stadie anvendes data og tilpasninger på miljøer med én boks. Du kan køre i et enkelt miljø, der både kan være virksomhedshubben og skalaenheden. Alternativt kan du have to udviklingsmiljøer, hvoraf det ene har rollen som hub, og det andet har rollen som skalaenhed. Denne konfiguration giver dig den bedste måde at identificere og løse problemer på. Den seneste [forhåndsversion-build](../../fin-ops-core/fin-ops/get-started/one-version.md#how-can-i-get-early-access-to-non-released-platform-updates) kan også bruges til at fuldføre dette stadie.

Du skal du bruge [implementeringsværktøjerne til skalaenheden for udviklingsmiljøer med én boks](https://github.com/microsoft/SCMScaleUnitDevTools) til at installere og vedligeholde miljøer. Disse værktøjer giver dig mulighed for at konfigurere hub og skalaenheder i et eller to miljøer med én boks. Værktøjerne leveres som både binær frigivelse og i kildekode på GitHub. Undersøg projektets wiki, som inkluderer en [trinvis brugsvejledning](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide), der beskriver, hvordan værktøjerne bruges. Hvis du [udruller edge-skalaenheder på tilpasset hardware ved hjælp af LBD (lokale forretningsdata),](cloud-edge-edge-scale-units-lbd.md) skal du følge en anden proces.

## <a name="option-2-acquire-add-ins-and-deploy-in-your-sandbox-environments"></a>Mulighed 2: Anskaffe tilføjelsesprogrammer og udrulle dem i dine sandkassemiljøer

Hvis du vil afprøve den distribuerede hybridtopologi, skal du have to sandkassemiljøer (niveau 2), hvoraf det ene indeholder data (virksomhedshub), og det andet er til skalaenheden og har "tomme data".

Du skal anskaffe tilføjelsesprogrammer til mindst én sky- eller edge-skalaenhed. Tilsvarende projekt- og miljøpladser tildeles i [Microsoft Dynamics Lifecycle Services (LCS),](https://lcs.dynamics.com/), så skalaenhedsmiljøerne kan implementeres ved hjælp af [portalen til styring af skalaenhed](https://aka.ms/SCMSUM).

Kontakt Microsoft Support for at anmode om, at sandkassemiljøerne aktiveres.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
