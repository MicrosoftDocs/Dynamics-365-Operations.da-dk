---
title: Pluk det ældste batch på en mobilenhed
description: Denne artikel beskriver, hvordan du kan konfigurere og anvende indstillingerne for at plukke det ældste batch fra en mobilenhed.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad1f2cfd029d71784d5efcc169178a791f0ae077
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885632"
---
# <a name="pick-oldest-batch-on-a-mobile-device"></a>Pluk det ældste batch på en mobilenhed

[!include [banner](../includes/banner.md)]

Du kan få adgang til konfigurationen af **Pluk den ældste batch** via en menu på mobilenhed, og det giver dig mulighed at tvinge lagermedarbejdere til eller advare dem mod at plukke det ældste batch på deres aktuelle placering.  

## <a name="where-it-applies"></a>Hvor det er relevant
Vælg den ældste batch konfigureres i menupunkter på en mobilenhed og påvirker pluk for-batchet under varer.

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a>Sådan indstilles konfigurationen for Pluk den ældste batch 
For varer, der er indstillet til at bruge eksisterende arbejde, kan **Pluk den ældste batch** indstilles til **Ingen**, **Advar** eller **Gennemtving** fra en menu på en mobilenhed.

**Ingen**: Arbejdere modtager ingen meddelelser, og de kan plukke ethvert batch på deres placering.

**Advar** og **Gennemtving**: Der vises en liste over batches med den ældste udløbsdato over batchkontrolelementet, når arbejderen vælger et batch. Hvis placeringen er id-kontrolleret, vises en liste over id'er, der har det ældste batch, over id-kontrolelementet. 
-   **Advar**: Hvis en arbejder vælger et id eller et batch, der ikke findes på listen, er kontrolelement tomt, og der vises en advarsel om, at et ældre batch kan vælges. Hvis arbejderen vil have mulighed for at fortsætte arbejdet, kan vedkommende vælge det samme id eller batch igen.  
-   **Gennemtving**: Arbejdere kan fortsat modtage meddelelsen om, at et ældre batch skal plukkes.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]