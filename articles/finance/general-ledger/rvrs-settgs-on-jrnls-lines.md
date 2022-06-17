---
title: Tilbageføre indstillinger på kladder og linjer
description: Denne artikel omhandler, hvorfor en tilbageførselspost, der er angivet i en økonomikladde, muligvis ikke inkluderes i den bogførte transaktion.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e36a3ea1736e4d7f60a5a6ce588ad3e66c950c14
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899836"
---
# <a name="reverse-settings-on-journals-and-lines"></a>Tilbageføre indstillinger på kladder og linjer

[!include [banner](../includes/banner.md)]

Denne artikel omhandler, hvorfor en tilbageførselspost, der er angivet i en økonomikladde, muligvis ikke inkluderes i den bogførte transaktion.  

## <a name="symptom"></a>Symptom

En finanskladde omfatter en tilbageførselspost og tilbageførselsdato i kladden. Når du bogfører kladden, tilbageføres ingen af bilagene. Hvorfor sker det?

## <a name="resolution"></a>Løsning

Når kladden bogføres, behandles tilbageførslen kun med indstillingerne for **Tilbageførselspost** og **Tilbageførselsdato** i sektionen **Linjer** på bilaget. Denne metode giver en kladde mulighed for at medtage visse bilag, der er markeret til tilbageførsel, mens andre ikke er.

Værdierne fra kladden bruges kun som standard, når der tilføjes *nye* linjer. Ændring af værdierne i kladden påvirker ikke eksisterende linjer. I dette eksempel er bilagslinjerne blevet angivet først. Når du angiver linjedetaljerne, inden du angiver kladden som tilbageførsel, anvendes angivelsen som en tilbageførsel og dato ikke på eksisterende linjer.

Ændring af tilbageførselsposten eller tilbageførselsdatoen på en eksisterende linjekvittering, der ændres til andre linjer i samme bilag. Hvis ydeevnen skal optimeres, opdateres gitteret ikke, når der er foretaget ændringer af linjen til andre linjer. Du kan få vist de opdaterede værdier ved at opdatere gitteret.


