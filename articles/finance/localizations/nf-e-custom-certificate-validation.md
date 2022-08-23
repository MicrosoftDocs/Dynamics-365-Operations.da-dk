---
title: NF-e-tilpasset certifikatvalidering
description: Denne artikel giver oplysninger om aktivering og brug af det brugerdefinerede NF-e-certifikat.
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f78fdbd133aecaf9dbf8abe0006abd6deb1b1b15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288538"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e-tilpasset certifikatvalidering

[!include [banner](../includes/banner.md)]

Egenskaben **Servergodkendelsesformål** fra de certifikater, der er udstedt af det brasilianske rodnøglecenter, er som standard deaktiveret og skal aktiveres manuelt. I nogle tilfælde kan den automatiske certifikatopdatering ændre denne egenskab, så den ikke længere er aktiveret. Hvis dette sker, påvirkes TLS-forbindelsen og er ikke længere pålidelig. Muligheden for at udstede det brasilianske elektroniske regnskabsdokument model 55 (NF-e) i produktionsmiljøer for tilstande af Minas Gerais (MG) og Paraná (PR) påvirkes også.

Du kan aktivere rettelsen til **brugerdefineret validering af NF-e-certifikater** ved at gå til **Funktionsstyring**. Denne funktion giver mulighed for en alternativ løsning til validering af V5- og V10-certifikatet og tillader en sikker forbindelse til webtjenesterne, hvilket er påkrævet for sikker overførsel af NF-e og modtagelse af godkendelsen fra SEFAZ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
