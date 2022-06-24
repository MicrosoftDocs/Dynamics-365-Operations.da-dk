---
title: Komponenter til globaliseringsfunktion
description: Denne artikel giver en oversigt over komponenterne til globaliseringsfunktioner.
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5525332fe3f1a3ea96da630dc34bab82e4117f99
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891482"
---
# <a name="globalization-feature-components"></a>Komponenter til globaliseringsfunktion

[!include [banner](../includes/banner.md)]

En globaliseringsfunktion er et sæt komponenter, der definerer reglerne for datatransformation i konfigurationer af elektronisk rapportering (ER). Disse komponenter inkluderer instruktioner til behandling af elektroniske dokumenter og sender dem derefter til eller modtager dem fra eksterne kanaler. De omfatter også betingelser, der definerer, hvornår en funktion skal køres for indgående forretningsdata.

Alle komponenter er afhængige af hinanden. Globaliseringsfunktioner gør det let at oprette og vedligeholde denne afhængighed og understøtte administration af livscyklus og versioner i sættet af komponenter.

## <a name="access-electronic-invoicing-feature-components"></a>Få adgang til komponenter for funktioner til elektronisk fakturering 

1. Logge på din RCS-konto (Regulatory Configuration Service).
2. I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **Elektronisk fakturering**.

    Globaliseringsfunktioner har flere komponenter. Siden **Funktioner for elektronisk fakturering** indeholder en separat fane for hver komponent.

    - **Version** – Denne komponent understøtter administration af livscyklus i funktionen. Du kan bruge den til at administrere status for forskellige versioner af funktionen.
    - **Konfigurationer** – Denne komponent giver dig mulighed for at administrere, se og redigere relateret ER-format og formattilknytningskonfigurationer, der bruges i behandlingspipelinen.
    - **Opsætninger** – Denne komponent giver brugerne af globaliseringstjenester, f.eks. en e-faktureringstjeneste, mulighed for at administrere opsætningen af den relaterede funktionsversion. Den understøtter derfor den fleksible konstruktion af kommunikations- og svarregler.
    - **Miljøer** – Denne komponent giver brugerne af globaliseringstjenester, f.eks. en e-faktureringstjeneste, mulighed for at administrere det miljø, hvor opsætningen af funktionsversionen bruges. Den kan også tildele godkendelse til de brugere, der skal have adgang til opsætningen af funktionsversionen.
    - **Organisationer** – Denne komponent giver brugerne mulighed for at dele funktionen med eksterne organisationer.
    - **Mærker** – Denne komponent giver dig mulighed for at mærke funktioner, der kan bruges i globaliseringsplanen for referencen.
