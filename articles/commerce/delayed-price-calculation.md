---
title: Udskyde nøjagtig pris- og rabatberegning for at få bedre ydeevne
description: Denne artikel beskriver funktionen til udskudt beregning af priser, som er tilgængelig i Microsoft Dynamics 365 Commerce POS og callcenter.
author: boycezhu
ms.date: 09/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 66c7c5a61648ba0423b27b74a1c4e42bc1b22b8b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267584"
---
# <a name="delay-exact-price-and-discount-calculation-for-improved-performance"></a>Udskyde nøjagtig pris- og rabatberegning for at få bedre ydeevne

[!include [banner](includes/banner.md)]

Denne artikel beskriver funktionen til udskudt beregning af priser, som er tilgængelig i Microsoft Dynamics 365 Commerce POS og callcenter.

Dynamics 365 Commerce understøtter oprettelse af samkøbsrabatter, der anvendes, når flere salgslinjer i en salgsordre eller et salgstilbud kombineres. Disse rabatter omfatter mix og match, grænseværdi og mængderabatter.

Når der føjes en ny linje til en ordre, evaluerer Commerce-prissætningsprogrammet hele indkøbsvognen for at finde ud af, om nogen af disse samkøbsrabatter kan anvendes. På grund af denne genberegning kan tilføjelse af nye linjer påvirke ydeevnen, efterhånden som salgsordren vokser.

Business-to-business-firmaer (B2B) og visse B2C-firmaer (business-to-consumer) har dog ofte store ordrestørrelser. Derfor kan det være tidskrævende at vente på prissætningsprogrammets genberegning, efter at hver vare er føjet til indkøbsvognen. For store ordrer er det normalt ikke vigtigt, at den nøjagtige pris og rabat vises, hver gang der føjes en vare til indkøbsvognen. Det er vigtigere, at brugerne kan tilføje varer hurtigt. Muligheden for at udskyde den nøjagtige pris- og rabatberegning, indtil en bruger anmoder om den, eller en ordre færdiggøres, kan forbedre ydeevnen væsentligt. Det kan også reducere den tid, det tager at afslutte afgivelsen af en ordre.

Det har længe været muligt at udskyde den nøjagtige pris- og rabatberegning i POS. Fra og med Commerce version 10.0.22 frigivelsen er den også tilgængelig for callcenter.

## <a name="enable-delayed-price-and-discount-calculation-for-pos"></a>Aktivere udskudt pris- og rabatberegning for POS

Følg disse trin for at aktivere udskudt pris- og rabatberegning for POS.

1. I Commerce Headquarters skal du gå til den funktionalitetsprofil, der er tilknyttet den fysiske butik.
1. Aktivér konfigurationen **Beregn rabatter for flere varer manuelt** i oversigtspanelet **Beløb**.
1. Åbn skærmlayoutdesigneren for de kasseapparater, hvor den udskudte beregning skal aktiveres.
1. Tilføj en knap for handlingen **Beregn total** til det ønskede knapgitter.
1. Kør jobbene **1070** og **1090**.

Når der nu føjes varer til en transaktion, beregnes samkøbsrabatter ikke, medmindre kassereren vælger knappen **Beregn total**. Når der er valgt **Beregn total** for en transaktion, beregnes der altid samkøbsrabatter for den. Kassereren behøver ikke vælge knappen igen, heller ikke selvom der er føjet yderligere varer til indkøbsvognen. Systemet tillader ikke, at kassereren registrerer betalingen, før **Beregn total** er valgt.

## <a name="enable-delayed-price-and-discount-calculation-for-call-center"></a>Aktivere udskudt pris- og rabatberegning for callcenter

Følg disse trin for at aktivere udskudt pris- og rabatberegning for callcenter.

1. Gå til **Arbejdsområder \> Funktionsstyring** i Commerce Headquarters.
1. Aktivér funktionen **Undgå utilsigtet prisberegning for handelsordre**. Denne funktion er en forudsætning for funktionen til udskudt beregning af priser og rabatter.

    > [!NOTE]
    > I forbindelse med nye installationer er funktionen **Undgå utilsigtet prisberegning for handelsordre** aktiveret som standard.

1. Gå til **Parametre for handel \> Priser og rabatter**.
1. Aktivér **Beregn priser og rabatter på flere linjer manuelt** i sektionen **Diverse**.

Når en salgsordre eller et salgstilbud nu oprettes eller redigeres i callcenter, forsinkes den nøjagtige pris- og rabatberegning for den. Prissætningsprogrammet vil kun overveje den salgslinje, der tilføjes eller redigeres, og ignorerer alle andre salgslinjer. Nettobeløbet for en vare omfatter priskalkulation og simple rabatter (rabatprocent eller fratrukket beløb ud for en enkelt vare). Mix og match, grænseværdi og mængderabatter anvendes dog ikke. De callcenter-brugere, der ønsker at få vist den nøjagtige pris inkl. alle rabatter, kan vælge en af tre knapper: **Genberegn**, **Totaler** eller **Fuldført**.

> [!NOTE]
> I forbindelse med callcenterordrer vises der en advarsel for at minde brugeren om, at brugeren skal vælge knappen **Genberegn**, **Totaler** eller **Fuldfør** for at kunne udføre den nøjagtige pris- og rabatberegning. I forbindelse med ordrer, hvor knappen **Fuldført** er tilgængelig, kan callcenter-brugeren ikke udelade den nøjagtige pris- og rabatberegning, da de skal vælge **Fuldført** for at fuldføre ordreregistreringen. For ordrer, hvor knappen **Fuldfør** ikke er tilgængelig, er der ingen handling, der angiver fuldførelsen af ordreregistreringen. Callcenter-brugeren er derfor ansvarlig for at vælge enten **Genberegn** eller **Totaler**, før de fuldfører ordreregistreringen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
