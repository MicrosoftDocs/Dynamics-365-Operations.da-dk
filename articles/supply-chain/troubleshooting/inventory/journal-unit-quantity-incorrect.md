---
title: Enheden og enhedsantallet fungerer ikke korrekt i lagerkladden
description: Enheden og enhedsantallet fungerer ikke korrekt i lagerkladden
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 074be71d7b6ec1acab6307a79e397c2a2a045c39
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778419"
---
# <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Enheden og enhedsantallet fungerer ikke korrekt i lagerkladden

## <a name="symptoms"></a>Symptomer

Der kan opstå en eller begge af følgende fejl, når du arbejder med enheder og antal i en lagerkladde:

- Du kan ikke se enheder eller enhedsantal i lagerkladden, når der er konfigureret en enhedskonvertering for det frigivne produkt, og du kan ikke ændre enheden i lagerkladden.
- Du kan se felterne **Antal** og **Enhed** i lagerkladden, men du kan ikke se feltet **Enhedsantal**. Hvis du ændrer enheden, angiver et antal og bogfører kladden, vises den oprindelige måleenhed for dette antal stadig i kladden.

## <a name="resolution"></a>Løsning

Følg disse trin for at løse dette problem.

1. I arbejdsområdet **Funktionsstyring** skal du sørge for, at funktionen *Brug af måleenhed og enhedsantal i lagerkladder* er aktiveret. Denne funktion føjer felterne **Enhed** og **Enhedsantal** til kladden. (Fra og med Supply Chain Management version 10.0.21 er denne funktion som standard aktiveret.)
1. Når funktionen er aktiveret, skal du benytte felterne **Antal**, **Enhedsantal** og **Enhed** på følgende måde:

    - **Antal** – Angiv antallet ved hjælp af den standardenhed, der er defineret for det frigivne produkt. Selve standardenheden vises dog ikke her. Hvis der er konfigureret en konvertering mellem standardenheden og den valgte enhed i feltet **Enhed**, opdateres feltet **Antal** automatisk baseret på valgene i felterne **Enhedantal** og **Enhed**.
    - **Enhedsantal** – Angiv antallet ved at bruge den enhed, der er valgt i feltet **Enhed**.
    - **Enhed** – Vælg den enhed, der skal anvendes på værdien i feltet **Enhedsantal**.
