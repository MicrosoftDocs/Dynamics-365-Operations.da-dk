---
title: Testinstrumenter for kvalitetsstyring
description: Denne artikel beskriver, hvordan du opretter testinstrumenter, som kan bruges til test for kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36b712e6a99a0625af28ef121d0c9c39c1e32603
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857657"
---
# <a name="quality-management-test-instruments"></a>Testinstrumenter for kvalitetsstyring

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du opretter testinstrumenter, som kan bruges til test for kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.

Du kan bruge siden **Testinstrumenter** til at definere og få vist detaljer om de enheder, der bruges til at udføre test for kvalitetsordrer. Testinstrumenter er valgfrie. De kan dog hjælpe kvalitetsmedarbejdere med at finde ud af, hvilken enhed eller hvilket værktøj de skal bruge til at udføre en bestemt test.

## <a name="test-instrument-example"></a>Eksempel på testinstrument

Du udfører forskellige test af elektroniske komponenter. Nogle test angår strømspændingen for komponenter, én test angår deres temperatur, og én test angår deres vægt. Der bruges forskellige værktøjer, enheder eller udstyr til at udføre hver test. En strømspændingsmåler kan f.eks. bruges til at måle spændingen, et termometer kan bruges til at måle temperaturen, og en vægt kan bruges til at måle vægt. Du kan konfigurere hver af disse enheder som et testinstrument og angive den måleenhed, som testresultaterne skal registreres i. Resultaterne fra strømspændingsmåleren registreres f.eks. i volt, resultaterne fra termometeret registreres i grader såsom Fahrenheit eller Celsius, og resultaterne fra vægten registreres i pund eller kilo.

## <a name="create-a-test-instrument"></a>Oprette et testinstrument

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Testinstrumenter**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Testinstrument** – Angiv et entydigt id eller navn til testinstrumentet.
    - **Beskrivelse** – Indtast en detaljeret beskrivelse af testinstrumentet.
    - **Enhed** – Vælg den enhed, som instrumentet måler resultater i. Feltet **Præcision** angives automatisk ud fra den enhed, du vælger.

1. Luk siden.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Test for kvalitetsstyring](quality-tests.md)
- [Testgrupper for kvalitetsstyring](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
