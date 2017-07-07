---
title: "Pluk det ældste batch på en mobilenhed"
description: "I dette emne beskrives, hvordan du kan konfigurere og anvende indstillingerne for at plukke det ældste batch fra en mobilenhed."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: ee45fed40b10dbe913c73e1186b726a39831816d
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017


---

# <a name="pick-oldest-batch-on-a-mobile-device"></a>Pluk det ældste batch på en mobilenhed

[!include[banner](../includes/banner.md)]

Du kan få adgang til konfigurationen af **Pluk den ældste batch** via en menu på mobilenhed, og det giver dig mulighed at tvinge lagermedarbejdere til eller advare dem mod at plukke det ældste batch på deres aktuelle placering.  

## <a name="where-it-applies"></a>Hvor det er relevant
Vælg den ældste batch konfigureres i menupunkter på en mobilenhed og påvirker pluk for-batchet under varer.

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a>Sådan indstilles konfigurationen for Pluk den ældste batch 
For varer, der er indstillet til at bruge eksisterende arbejde, kan **Pluk den ældste batch** indstilles til **Ingen**, **Advar** eller **Gennemtving** fra en menu på en mobilenhed.

**Ingen**: Arbejdere modtager ingen meddelelser, og de kan plukke ethvert batch på deres placering.

**Advar** og **Gennemtving**: Der vises en liste over batches med den ældste udløbsdato over batchkontrolelementet, når arbejderen vælger et batch. Hvis placeringen er id-kontrolleret, vises en liste over id'er, der har det ældste batch, over id-kontrolelementet. 
-   **Advar**: Hvis en arbejder vælger et id eller et batch, der ikke findes på listen, er kontrolelement tomt, og der vises en advarsel om, at et ældre batch kan vælges. Hvis arbejderen vil have mulighed for at fortsætte arbejdet, kan vedkommende vælge det samme id eller batch igen.  
-   **Gennemtving**: Arbejdere kan fortsat modtage meddelelsen om, at et ældre batch skal plukkes.

