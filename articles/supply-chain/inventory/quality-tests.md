---
title: Test for kvalitetsstyring
description: I dette emne beskrives, hvordan du opretter test, som kan bruges til kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62e5aca8c41aa324802e83e53f52ea39b623a65882962413e743e6dd2671a901
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781032"
---
# <a name="quality-management-tests"></a>Test for kvalitetsstyring

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du opretter test, som kan bruges til kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.

Du kan bruge siden **Test** til at definere og få vist de individuelle test, der bestemmer, om produkterne opfylder kvalitetsspecifikationerne. Du kan tildele en eller flere individuelle test til en testgruppe. Når du gør det, skal du også angive testspecifikke oplysninger, f.eks. de acceptable måleværdier. Måleværdier bruges til kvantitative test. Til kvalitative test bruges testvariabler.

- For kvantitativ test er feltet **Type** angivet til *Heltal* eller *Del*. Der er også angivet en måleenhed. Kvalitetsspecifikationer og testresultater er udtrykt som tal.
- For kvalitative test er feltet **Type** angivet til *Indstilling*. Kvalitative test forudsætter flere oplysninger om den testvariabel, der måles, og de faste indstillinger. Kvalitetsspecifikationer og testresultater er udtrykt i overensstemmelse med et udfald.

Du kan også vælge at tildele et testinstrument til en test. Testinstrumenter er dog ikke påkrævede for at oprette og bruge test sammen med kvalitetsordrer. Du kan finde flere oplysninger under [Testinstrumenter for kvalitetsstyring](quality-test-instruments.md).

Du kan også vælge at angive en enhed for en test for at angive den måleenhed, som testresultaterne skal registreres i. En test for temperatur kan f.eks. omfatte en enhed på grader Fahrenheit eller grader Celsius.

## <a name="example-of-a-test"></a>Eksempel på en test

Et produktionsfirma udfører to test af købt materiale: en kvantitativ test for materialets kvalitet og en kvalitativ test for skader på emballagen. Virksomheden angiver yderligere oplysninger om den kvalitative test for at definere testvariablen (f.eks. beskadiget emballage) og udfaldet. Firmaet bruger siden **Testgrupper** til at tildele de to test til en testgruppe og til at angive de testspecifikke oplysninger. Testgruppen tildeles en kvalitetsordre, så virksomheden kan rapportere testresultater for de to test.

## <a name="create-a-test"></a>Oprette en test

Benyt denne fremgangsmåde for at oprette en test.

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Test**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Test** – Angiv et entydigt id eller navn til testen.
    - **Beskrivelse** – Indtast en detaljeret beskrivelse af testen.
    - **Type** – Vælg den resultattype, som testen giver. For kvantitative test skal du vælge *Del* eller *Heltal*. Vælg *Indstilling* for kvalitative test.
    - **Testinstrument** – Vælg et [testinstrument](quality-test-instruments.md), der skal bruges til testen.
    - **Enhed** – Hvis du har valgt *Del* eller *Heltal* i feltet **Type** (dvs. hvis testen er en kvantitativ test), skal du vælge den måleenhed, som testresultaterne skal registreres i.

1. Luk siden.

> [!NOTE]
> Når du har gemt en test, kan du ikke længere redigere feltet **Type** i gitteret. Hvis du skal ændre typen af de testresultater, der registreres for en test, skal du vælge **Skift kvalitetstesttype** i handlingsruden. I dialogboksen **Skift kvalitetstesttype** skal du angive feltet **Ny type** til den ønskede type og derefter vælge **OK** for at lukke dialogboksen.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Testinstrumenter for kvalitetsstyring](quality-test-instruments.md)
- [Testgrupper for kvalitetsstyring](quality-test-groups.md)
- [Testvariabler for kvalitetsstyring](quality-test-variables.md)
- [Kvalitetstilknytninger](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
