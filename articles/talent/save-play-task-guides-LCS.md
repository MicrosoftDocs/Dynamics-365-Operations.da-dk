---
title: Gemme opgaveguider til LCS og afspille dem igen
description: I dette emne beskrives, hvordan du kan gemme opgaveguider til Microsoft Dynamics Lifecycle Services (LCS) og derefter afspille dem igen.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 40b4c3154a04a557b8a670e1f1ae3722c71122fe
ms.contentlocale: da-dk
ms.lasthandoff: 12/04/2018

---

# <a name="save-task-guides-to-lcs-and-replay-them"></a>Gemme opgaveguider til LCS og afspille dem igen

[!include [banner](includes/banner.md)]

**Miljøoplysninger** 

Microsoft Dynamics 365 for Talent, som blev installeret via Microsoft Dynamics Lifecycle Services (LCS)

**Afgang**

Kunden ønsker at gemme nye opgaveregistreringer til sit LCS-projekt og derefter afspille de gemte opgaveguider igen.

**Løsning**

Følg disse trin for at gemme en opgaveregistrering til LCS.

1. Log på LCS, og vælg projektet.
2. Vælg feltet **Forretningsmodeldesigner**.
3. Få vist siden i "Opdateret BPM-oplevelse".
4. Vælg et bibliotek, og vælg derefter **Kopier**.
5. Angiv et navn til forretningsmodeldesigneren (BPM).
6. Log på Talent fra LCS.
7. Skriv **hjælp** i feltet **Søg**. Hjælp til Lifecycle Services åbnes.
8. Vælg knappen **Opdater** til konfiguration af Lifecycle Services Hjælp.

    Dit nye BPM-bibliotek vises, og det skal være aktivt.

9. Luk siden.
10. Opret en opgaveregistrering.
11. Når du har gjort det, skal du vælge **Gem Lifecycle Services**.

    ![Gem i Lifecycle Services](media/task-guides.png)

12. Vælg det BPM-bibliotek og den node, som opgaveregistreringen skal gemmes til.

Følg disse trin for at afspille en opgaveguide fra LCS.

1. Start Arbejdsrutineoptager.
2. Vælg **Åbn fra LCS**.
3. Vælg biblioteket og den BPM-node, der har den gemte opgaveguide.
4. Åbn opgaveguiden.

