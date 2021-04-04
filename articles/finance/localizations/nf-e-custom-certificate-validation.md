---
title: NF-e-brugerdefineret certifikatvalidering
description: Dette emne giver oplysninger om aktivering og brug af det brugerdefinerede NF-e-certifikat.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3efa05f49748f6bbff680f322a77cec24da46c0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240573"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e-brugerdefineret certifikatvalidering

[!include [banner](../includes/banner.md)]

Når du aktiverer NF-e-brugerdefineret certifikatkontrolfunktionen, giver brugerdefineret validering en forbindelse til webtjenesterne. Denne forbindelse er påkrævet for at overføre NF-e og modtage autorisation fra SEFAZ.

Egenskaben **Formål for servergodkendelse** fra certifikatet V5 udstedes af det brasilianske rodnøglecenter. Denne egenskab er deaktiveret som standard og skal aktiveres manuelt. I nogle tilfælde kan den automatiske certifikatopdatering ændre denne egenskab, så den ikke længere er aktiveret. Hvis dette sker, påvirkes TLS-forbindelsen og er ikke længere pålidelig. Muligheden for at udstede NF-e i produktionsmiljøer for tilstande af Minas Gerais (MG) og Paraná (PR) påvirkes også.

Denne opdatering giver mulighed for en alternativ løsning til certifikatvalidering, hvilket betyder, at det er muligt at oprette en sikker kommunikation.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]