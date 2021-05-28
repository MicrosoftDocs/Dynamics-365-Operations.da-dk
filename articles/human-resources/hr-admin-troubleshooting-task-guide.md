---
title: Gem opgaveguider for LCS, og afspil dem
description: I denne artikel beskrives det, hvordan du kan gemme opgaveguider til Microsoft Dynamics Lifecycle Services (LCS) og derefter afspille dem igen.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 40377ece3685c50a448bf48e1d001fb1ecbbff3e
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6028053"
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

    ![Gem i Lifecycle Services](media/task-guides.png)

12. Vælg det BPM-bibliotek og den node, som opgaveregistreringen skal gemmes til.

Følg disse trin for at afspille en opgaveguide fra LCS.

1. Start Arbejdsrutineoptager.
2. Vælg **Åbn fra LCS**.
3. Vælg biblioteket og den BPM-node, der har den gemte opgaveguide.
4. Åbn opgaveguiden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]