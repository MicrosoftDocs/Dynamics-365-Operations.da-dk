---
title: Indgående og udgående aktiver
description: Dette emne forklarer, hvordan du registrerer indgående og udgående aktiver i "Styring af aktiver".
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 62998da7f541379296d5ac325ae29f24a42f9b7c
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847545"
---
# <a name="inbound-and-outbound-assets"></a>Indgående og udgående aktiver

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Hvis din virksomhed udfører reparationsarbejde eller vedligeholdelsesarbejde på aktiver, som er modtaget fra andre lokationer eller kunder, kan "Styring af aktiver" spore både indgående aktiver, der er på vej til din virksomhed, og udgående aktiver, der returneres.

> [!NOTE]
> Hvis du ønsker at bruge indgående og udgående livscyklustilstande til at administrere aktiver, der kommer ind og returneres, skal du konfigurere vedligeholdelsesanmodning for livscyklustilstande og livscyklusmodeller for at understøtte disse handlinger. Du kan finde flere oplysninger i [Opsætning af vedligeholdelsesanmodninger](../setup-for-maintenance-requests/requests.md).

Opsætningen af "Styring af aktiver" afgør, om du kan arbejde med indgående og udgående aktiver.

## <a name="register-assets-as-inbound"></a>Registrer aktiver som indgående

1. Vælg **Styring af aktiver** \> **Almindelig** \> **Vedligeholdelsesanmodninger** \> **Aktive vedligeholdelsesanmodninger**.
2. Vælg vedligeholdelsesanmodningen.
3. Vælg **Opdater vedligeholdelsesanmodningens tilstand**.
4. Vælg **Indgående** (eller en anden livscyklustilstand, som du har oprettet for indgående aktiver), og vælg dernæst **OK**.

![Figur 1](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>Registrer indgående aktiver som modtaget

1. Vælg **Styring af aktiver** \> **Almindelig** \> **Indgående/udgående** \> **Indgående aktiver**.
2. Vælg aktivet eller vedligeholdelsesanmodningen.
3. Vælg **Modtag aktiver**.
4. Angiv datoen og tidspunktet i feltet **Modtaget**. Vælg derefter **OK**. Posten blev fjernet fra listesiden **Indgående aktiver**.

![Figur 2](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>Registrer aktiver som udgående

Når du har fuldført vedligeholdelses-eller reparationsopgaven, kan du registrere aktivet som returneret.

1. Vælg **Styring af aktiver** \> **Almindelig** \> **Vedligeholdelsesanmodninger** \> **Aktive vedligeholdelsesanmodninger**.
2. Vælg vedligeholdelsesanmodningen.
3. Vælg **Opdater vedligeholdelsesanmodningens tilstand**.
4. Vælg **Udgående** (eller en anden livscyklustilstand, som du har oprettet for udgående aktiver), og vælg dernæst **OK**.

## <a name="register-outbound-assets-as-delivered"></a>Registrer udgående aktiver som leveret

1. Vælg **Styring af aktiver** \> **Almindelig** \> **Indgående/udgående** \> **Udgående aktiver**.
2. Vælg aktivet eller vedligeholdelsesanmodningen.
3. Vælg **Levér aktiver**.
4. Angiv datoen og tidspunktet i feltet **Leveret**. Vælg derefter **OK**. Posten blev fjernet fra listesiden **Udgående aktiver**.