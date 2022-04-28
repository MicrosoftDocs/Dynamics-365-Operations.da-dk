---
title: Indgående og udgående aktiver
description: Dette emne forklarer, hvordan du registrerer indgående og udgående aktiver i "Styring af aktiver".
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ee3917725a95d47e37b9c914580e8ce521b52695
ms.sourcegitcommit: 4c8223c9540fbc1c1e554962938058d432e4c681
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/05/2022
ms.locfileid: "8548133"
---
# <a name="inbound-and-outbound-assets"></a>Indgående og udgående aktiver

[!include [banner](../../includes/banner.md)]

 

Hvis din virksomhed udfører reparationsarbejde eller vedligeholdelsesarbejde på aktiver, som er modtaget fra andre lokationer eller kunder, kan "Styring af aktiver" spore både indgående aktiver, der er på vej til din virksomhed, og udgående aktiver, der returneres.

> [!NOTE]
> Hvis du ønsker at bruge indgående og udgående livscyklustilstande til at administrere aktiver, der kommer ind og returneres, skal du konfigurere vedligeholdelsesanmodning for livscyklustilstande og livscyklusmodeller for at understøtte disse handlinger. Du kan finde flere oplysninger i [Vedligeholdelsesanmodninger](/d365F-O/supply-chain/asset-management/manage-maintenance-requests/../manage-maintenance-requests/maintenance-request-overview).

Opsætningen af "Styring af aktiver" afgør, om du kan arbejde med indgående og udgående aktiver.

## <a name="register-assets-as-inbound"></a>Registrer aktiver som indgående

1. Vælg **Styring af aktiver** \> **Almindelig** \> **Vedligeholdelsesanmodninger** \> **Aktive vedligeholdelsesanmodninger**.
2. Vælg vedligeholdelsesanmodningen.
3. Vælg **Opdater vedligeholdelsesanmodningens tilstand**.
4. Vælg **Indgående** (eller en anden livscyklustilstand, som du har oprettet for indgående aktiver), og vælg dernæst **OK**.

![Registrere aktiver som indgående.](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>Registrer indgående aktiver som modtaget

1. Vælg **Styring af aktiver** \> **Almindelig** \> **Indgående/udgående** \> **Indgående aktiver**.
2. Vælg aktivet eller vedligeholdelsesanmodningen.
3. Vælg **Modtag aktiver**.
4. Angiv datoen og tidspunktet i feltet **Modtaget**. Vælg derefter **OK**. Posten blev fjernet fra listesiden **Indgående aktiver**.

![Registrere indgående aktiver som modtaget.](media/08-manage-maintenance-requests.png)

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]