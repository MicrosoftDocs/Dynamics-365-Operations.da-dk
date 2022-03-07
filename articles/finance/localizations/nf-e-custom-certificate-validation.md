---
title: NF-e-brugerdefineret certifikatvalidering
description: Dette emne giver oplysninger om aktivering og brug af det brugerdefinerede NF-e-certifikat.
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8144e16b127bdbe954ef44f52c5ac71689a2036e6085e9a4ccc8bb17f91ae9b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755585"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e-tilpasset certifikatvalidering

[!include [banner](../includes/banner.md)]

Egenskaben **Servergodkendelsesformål** fra de certifikater, der er udstedt af det brasilianske rodnøglecenter, er som standard deaktiveret og skal aktiveres manuelt. I nogle tilfælde kan den automatiske certifikatopdatering ændre denne egenskab, så den ikke længere er aktiveret. Hvis dette sker, påvirkes TLS-forbindelsen og er ikke længere pålidelig. Muligheden for at udstede det brasilianske elektroniske regnskabsdokument model 55 (NF-e) i produktionsmiljøer for tilstande af Minas Gerais (MG) og Paraná (PR) påvirkes også.

Du kan aktivere rettelsen til **brugerdefineret validering af NF-e-certifikater** ved at gå til **Funktionsstyring**. Denne funktion giver mulighed for en alternativ løsning til validering af V5- og V10-certifikatet og tillader en sikker forbindelse til webtjenesterne, hvilket er påkrævet for sikker overførsel af NF-e og modtagelse af godkendelsen fra SEFAZ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
