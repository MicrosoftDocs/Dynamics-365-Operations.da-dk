---
title: Deaktivere regler, der bruges i valideringsprocessen for transaktioner
description: Denne artikel beskriver funktionen til deaktivering af valideringsregler for transaktioner i Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 12/11/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7d566aa3b829dad281528925a341382f9637fdba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884870"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>Deaktivere regler, der bruges i valideringsprocessen for transaktioner

[!include [banner](../includes/banner.md)]

Detailhandlere kan have forretningsscenarier og -processer, der er specifikke for dem. Derfor er det ikke alle de regler, der er inkluderet i valideringsprocessen til handelstransaktioner, der gælder for alle detailhandlere. For at sørge for tilpasning til forskellige situationer indeholder Microsoft Dynamics 365 Commerce funktionalitet, der kan bruges til at deaktivere de regler, der ikke er relevante.

Hvis du vil have vist listen over regler, der er tilgængelige i valideringsprocessen til transaktioner i dit miljø og få vist status for hver regel, skal du gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Commerce-parametre** og vælge fanen **Transaktionsvalidering**. Alle aktiverede regler bruges til at validere transaktioner under processen **Valider butiksposteringer** og skal overholdes, før transaktioner kan indsamles og bogføres i en transaktionsopgørelse.

Status for alle regler angives som standard til **Aktiveret**. Derfor bruges alle reglerne til at validere transaktioner, før de trækkes ind i handelstransaktionsopgørelserne. Hvis du vil deaktivere en regel, skal du ændre dens status til **Deaktiveret**. Deaktiverede regler tages ikke i betragtning, når transaktioner valideres under processen **Valider butiksposteringer**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
