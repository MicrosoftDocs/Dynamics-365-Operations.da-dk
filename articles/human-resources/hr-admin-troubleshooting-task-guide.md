---
title: Gem opgaveguider for LCS, og afspil dem
description: I dette emne beskrives, hvordan du kan gemme opgaveguider til Microsoft Dynamics Lifecycle Services (LCS) og derefter afspille dem igen.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42fad014590abebf159b71227a44eb8df60bf05e
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416875"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>Gem opgaveguider for LCS, og afspil dem

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Miljøoplysninger** 

Microsoft Dynamics 365 Human Resources, som blev installeret via Microsoft Dynamics Lifecycle Services (LCS)

**Udsted**

Kunden ønsker at gemme nye opgaveregistreringer til sit LCS-projekt og derefter afspille de gemte opgaveguider igen.

**Løsning**

Følg disse trin for at gemme en opgaveregistrering til LCS.

1. Log på LCS, og vælg projektet.
2. Vælg feltet **Forretningsmodeldesigner**.
3. Få vist siden i "Opdateret BPM-oplevelse".
4. Vælg et bibliotek, og vælg derefter **Kopier**.
5. Angiv et navn til forretningsmodeldesigneren (BPM).
6. Log på Human Resources fra LCS.
7. Skriv **hjælp** i feltet **Søg**. Hjælp til Lifecycle Services åbnes.
8. Vælg knappen **Opdater** til konfiguration af Lifecycle Services Hjælp.

    Dit nye BPM-bibliotek vises, og det skal være aktivt.

9. Luk siden.
10. Opret en opgaveregistrering.
11. Når du har gjort det, skal du vælge **Gem Lifecycle Services**.

    ![Gem i Lifecycle Services.](media/task-guides.png)

12. Vælg det BPM-bibliotek og den node, som opgaveregistreringen skal gemmes til.

Følg disse trin for at afspille en opgaveguide fra LCS.

1. Start Arbejdsrutineoptager.
2. Vælg **Åbn fra LCS**.
3. Vælg biblioteket og den BPM-node, der har den gemte opgaveguide.
4. Åbn opgaveguiden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
