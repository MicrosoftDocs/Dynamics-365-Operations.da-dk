---
title: Lånte aktiver
description: Denne artikel beskriver, hvordan du kan registrere lånte aktiver i Styring af aktiver.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f70b29ef69b80160f108e6f53edda12b86c2c9db
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015748"
---
# <a name="asset-loans"></a>Lånte aktiver

[!include [banner](../../includes/banner.md)]

 

Hvis din virksomhed modtager aktiver til reparations- eller vedligeholdelsesopgaver fra enten interne lokationer eller kunder, og hvis du midlertidigt låner aktiver ud til disse lokationer eller kunder, kan Styring af aktiver registrere de lånte aktiver.

## <a name="register-asset-loans-on-a-maintenance-request"></a>Registrere lånte aktiver på en vedligeholdelsesanmodning

1. Vælg **Styring af aktiver** \> **Vedligeholdelsesanmodninger** \> **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger**.
2. Vælg den vedligeholdelsesanmodning, du vil registrere et lånt aktiv på, og vælg derefter **Rediger**.
3. Vælg **Send lånt aktiv** på siden **Anmodning**.
4. Vælg aktivet, og angiv den forventede tilbageleveringsdato.
5. Vælg **OK**.

> [!NOTE]
> - Du kan kun sende et lånt aktiv, hvis et aktiv af samme aktivtype er tilgængeligt.
> - Det aktiv, du låner ud, skal have en livscyklustilstand, der gør det muligt at bruge det som et lånt aktiv, f.eks. **InStorage**. Når det lånte aktiv er registreret, opdateres aktivets livscyklustilstand automatisk til eksempelvis **OnLoan**.

Hvis du vil have vist en liste over alle de aktiver, du har udlånt til andre lokationer eller kunder, skal du vælge **Styring af aktiver** \> **Lånt aktiv** \> **Alle lånte aktiver**. Hvis afkrydsningsfeltet **Afsluttet** er markeret for et aktiv, er aktivet registreret som returneret til dit firma.

![Administrere vedligeholdelsesanmodninger.](media/06-manage-maintenance-requests.png)

På siden **Aktive lånte aktiver** kan du få vist en liste over alle de lånte aktiver, der endnu ikke er returneret til din virksomhed.

## <a name="register-loan-assets-as-returned"></a>Registrere lånte aktiver som returneret

1. Vælg **Styring af aktiver** \> **Lånt aktiv** \> **Aktive lånte aktiver**.
2. Vælg det lånte aktiv, du vil registrere som returneret, og vælg derefter **Returner lånt aktiv**.
3. Angiv datoen og tidspunktet i feltet **Returneret**.
4. Vælg **OK**.
5. Opdater listesiden **Aktive lånte aktiver**, og bemærk, at det lånte aktiv ikke længere vises på listen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]