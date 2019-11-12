---
title: Garantier for aktiver og aktivtyper
description: I dette emne beskrives, hvordan du konfigurerer garantier for aktiver og aktivtyper i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6e69b471af0853159ba807af5f39db64dbbb04f8
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569702"
---
# <a name="warranties-on-assets-and-asset-types"></a>Garantier for aktiver og aktivtyper

[!include [banner](../../includes/banner.md)]

 


I dette emne beskrives, hvordan du konfigurerer garantier for aktiver og aktivtyper i Styring af aktiver.

## <a name="set-up-a-warranty-on-an-asset-type"></a>Konfigurere en garanti for en aktivtype

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Aktivtype** \> **Aktivtyper**.
2. I ruden til venstre skal du vælge den aktivtype, som en leverandørgarantiaftale skal knyttes til, og derefter skal du vælge **Standarder for aktivtype**.
3. Vælg aftalen i feltet **Leverandørgaranti** i oversigtspanelet **Generelt**.

## <a name="set-up-a-warranty-on-an-asset"></a>Konfigurere en garanti for et aktiv

1. Vælg **Styring af aktiver** \> **Almindelig** \> **Aktiver** \> **Alle aktiver**.
2. Vælg aktivet, og vælg derefter **Rediger**.
3. I oversigtspanelet **Leverandør** i sektionen **Leverandørgaranti** skal du vælge garantiaftalen i feltet **Garanti**.
4. Vælg start- og slutdatoerne i felterne **Garantistart** og **Garantiafslutning**.

    > [!IMPORTANT]
    > Hvis der er valgt en dato i feltet **Garantistart** på en arbejdsordre, bliver garantien gyldig for arbejdsordren på den pågældende dato. Når du opretter en arbejdsordre, indstilles feltet **Garantistart** automatisk til oprettelsesdatoen. Du kan dog ændre datoen, så den svarer til f.eks. startdatoen for en garantiaftale.
    >
    > ![Siden Arbejdsordre](media/02-warranty.png)

> [!NOTE]
> Når du opretter en arbejdsordre for et aktiv, der er dækket af en leverandørgaranti, modtager du en besked om garantiaftalen, hvis arbejdsordren har en forventet startdato i løbet af garantiperioden. Du kan derefter annullere arbejdsordren efter behov.
