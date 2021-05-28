---
title: Registrere certifikatnumre for skattekoncession
description: Dette emne forklarer, hvordan du registrerer koncessionscertifikatnumre for kildeskat (TDS – Tax Deducted at Source), der er udstedt til kreditorer.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023106"
---
# <a name="record-tds-concession-certificate-numbers"></a>Registrere certifikatnumre for skattekoncession

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du registrerer koncessionscertifikatnumre for kildeskat (TDS – Tax Deducted at Source), der er udstedt til kreditorer.

1. Gå til **Skat \> Indirekte skatter \> A-skat \> Koncessioner for A-skat**.
2. Vælg **Kildeskat** i feltet **Skattetype** for at registrere koncessionscertifikater for skattetypen Kildeskat.
3. Vælg **Alt+N** under fanen **Oversigt** for at oprette en linje.

    [![Overskriften på den nye linje](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)

4. Vælg den kildeskattekode, som kreditorens koncessionscertifikater udstedes for, i feltet **Kode for A-skat**. Feltet **Kodenavn for A-skat** viser navnet på kildeskattekoden.
5. I felterne **Fra dato** og **Til dato** skal du definere gyldighedsperioden for koncessionscertifikater, der bruger kildeskattekoden til at beregne kildeskat for kreditoren på koncessionelt grundlag.
6. Angiv eventuelle bemærkninger i feltet **Bemærkninger**.
7. Angiv koden for det juridiske område, som skattekoncessionscertifikatet aktiveres under, i feltet **Afsnit**.

    Hvis afsnitskoden er 197, vises værdien "A" i kolonnen "Årsag til ikke-fradrag/lavere fradrag" i Formular 26Q og kolonnen "Årsag til ikke-fradrag/lavere fradrag/bruttoberegning (eventuelt)" i Formular 27Q. Hvis afsnitskoden er 197A, vises værdien "B" begge steder.

8. Vælg oversigtspanelet **Certifikat** for at registrere certifikatnumre for skattekoncession til kreditorer.
9. Vælg den kreditorkonto, som skattekoncessionscertifikatet er udstedt for, i feltet **Kreditorkonto**.
10. Definer gyldighedsperioden for skattekoncessionscertifikatet i felterne **Fra dato** og **Til dato**.

    Beregningen af kildeskat på koncessionelt grundlag er baseret på den periode, hvor certifikatet oprettes for kreditoren.

11. Angiv skattekoncessionens certifikatnummer i feltet **Certifikat**.

    [![Oversigtspanelet Certifikat](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)

12. Luk siden.
