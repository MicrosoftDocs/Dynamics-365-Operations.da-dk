---
title: Rabatstyringsgrupper
description: Dette emne beskriver, hvordan du konfigurerer rabatstyringsgrupper. Rabatstyringsgrupper kan bruges under rabatberegninger og kan knyttes til en masterpost.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 10b5238f53f89dbd79e6a0fa4ef24ee92f0ae752f220c1f4d19ea629969a3049
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767382"
---
# <a name="rebate-management-groups"></a>Rabatstyringsgrupper

[!include [banner](../includes/banner.md)]

Beregninger af rabatstyring kan være baseret på grupper. Der kan oprettes rabatstyringsgrupper for debitorer, kreditorer og varer. De kan knyttes til en masterpost.

## <a name="rebate-management-customer-groups"></a>Debitorgrupper for rabatstyring

Beregningen for en debitorgruppe oprettes ofte for en kæde af firmaer som f.eks. en supermarkedskæde eller et franchisefirma. Denne type beregning vedrører normalt en rabat.

Der beregnes ofte et fradrag uden at tage højde for, hvem den relevante ordre er solgt til. Der er dog undtagelser. En licenstager kan f.eks. oprette et fradragsskema, hvor debitorgruppe A modtager 4 procent, mens debitorgruppe B kun får 3 procent.

### <a name="set-up-customer-groups"></a>Konfigurer kundegrupper

Du kan arbejde med debitorgrupper for rabatstyring ved at gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Debitorgrupper**. Brug knapperne i handlingsruden til at tilføje og fjerne grupper efter behov. For hver gruppe skal du angive følgende felter:

- **Rabatstyringsgruppe** – Angiv et entydigt navn til gruppen.
- **Beskrivelse** – Angiv en beskrivelse af gruppen for at give flere oplysninger om, hvordan den skal bruges.

### <a name="manage-customer-group-assignments"></a>Administrere tildelinger af debitorgrupper

Hver debitor kan tilhøre et vilkårligt antal rabatstyringsgrupper. Hvis du vil se og tildele gruppemedlemmer, kan du starte enten fra gruppelisten eller fra debitorlisten.

Hvis du vil se, tilføje eller fjerne debitorer for en valgt gruppe, skal du følge disse trin.

1. Gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Debitorgrupper**.
1. Vælg den gruppe, der skal administreres.
1. Vælg **Debitorer** i handlingsruden. Siden **Rabatstyringsgrupper** vises med en liste over debitorer, der allerede er medlem af den valgte gruppe.
1. Gå til handlingsruden, og vælg **Ny** for at føje en ny debitor til gruppen for at tilføje en række i gitteret. Angiv derefter følgende felt til den nye række:

    - **Debitorkonto** – Vælg debitorkonto-id.

1. Hvis du vil fjerne en debitor fra gruppen, skal du markere debitoren og derefter vælge **Slet** i handlingsruden.

Hvis du vil se, tilføje eller fjerne gruppetildelinger for en valgt debitor, skal du følge disse trin.

1. Gå til **Debitorer \> Kunder \> Alle kunder**.
1. Vælg den debitor, du vil arbejde med.
1. Vælg **Rabatstyringsgrupper** i gruppen **Rabatstyring** i handlingsruden under fanen **Debitor**. Siden **Rabatstyringsgrupper** vises med en liste over grupper, som den valgte debitor allerede er medlem af.
1. Gå til handlingsruden, og vælg **Ny** for at føje debitoren til en ny gruppe for at tilføje en række i gitteret. Angiv derefter følgende felt til den nye række:

    - **Rabatstyringsgruppe** – Vælg den gruppe, hvor debitoren skal tilføjes.

1. Hvis du vil fjerne en debitor fra en gruppe, skal du vælge gruppen og derefter vælge **Slet** i handlingsruden.

## <a name="rebate-management-vendor-groups"></a>Rabatstyringsgrupper for kreditor

Beregningen for en gruppe af kreditorer oprettes ofte for en gruppe leveringssteder. Denne type beregning vedrører normalt en rabat.

### <a name="set-up-vendor-groups"></a>Konfigurere kreditorgrupper

Du kan arbejde med kreditorgrupper for rabatstyring ved at gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Kreditorgrupper**. Brug knapperne i handlingsruden til at tilføje og fjerne grupper efter behov. For hver gruppe skal du angive følgende felter:

- **Rabatstyringsgruppe** – Angiv et entydigt navn til gruppen.
- **Beskrivelse** – Angiv en beskrivelse af gruppen for at give flere oplysninger om, hvordan den skal bruges.

### <a name="manage-vendor-group-assignments"></a>Administrere tildelinger af kreditorgrupper

Hver kreditor kan tilhøre et vilkårligt antal rabatstyringsgrupper. Hvis du vil se og tildele gruppemedlemmer, kan du starte enten fra gruppelisten eller fra kreditorlisten.

Hvis du vil se, tilføje eller fjerne kreditorer for en valgt gruppe, skal du følge disse trin.

1. Gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Kreditorgrupper**.
1. Vælg den gruppe, der skal administreres.
1. Vælg **Kreditorer** i handlingsruden. Siden **Rabatstyringsgrupper** vises med en liste over kreditorer, der allerede er medlem af den valgte gruppe.
1. Gå til handlingsruden, og vælg **Ny** for at føje en ny kreditor til gruppen ved at tilføje en række i gitteret. Angiv derefter følgende felt til den nye række:

    - **Kreditorkonto** – Vælg kreditorkonto-id.

1. Hvis du vil fjerne en kreditor fra gruppen, skal du markere kreditoren og derefter vælge **Slet** i handlingsruden.

Hvis du vil se, tilføje eller fjerne gruppetildelinger for en valgt kreditor, skal du følge disse trin.

1. Gå til **Kreditor \> Kreditorer \> Alle kreditorer**.
1. Vælg den kreditor, du vil arbejde med.
1. Vælg **Rabatstyringsgrupper** i gruppen **Rabatstyring** i handlingsruden under fanen **Kreditor**. Siden **Rabatstyringsgrupper** vises med en liste over grupper, som den valgte kreditor allerede er medlem af.
1. Gå til handlingsruden, og vælg **Ny** for at føje kreditoren til en ny gruppe ved at tilføje en række i gitteret. Angiv derefter følgende felt til den nye række:

    - **Rabatstyringsgruppe** – Vælg den gruppe, hvor kreditoren skal tilføjes.

1. Hvis du vil fjerne en kreditor fra en gruppe, skal du vælge gruppen og derefter vælge **Slet** i handlingsruden.

## <a name="item-rebate-groups"></a>Varerabatgrupper

Ved at gruppere varer har du større fleksibilitet, når der beregnes rabatter og fradrag. Denne metode er ofte en mere effektiv måde at konfigurere rabatter og fradrag for debitorer og kreditorer på.

### <a name="set-up-item-groups"></a>Konfigurer varegrupper

Du kan arbejde med varegrupper for rabatstyring ved at gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Varegrupper**. Brug knapperne i handlingsruden til at tilføje og fjerne grupper efter behov. For hver gruppe skal du angive følgende felter:

- **Rabatstyringsgruppe** – Angiv et entydigt navn til gruppen.
- **Beskrivelse** – Angiv en beskrivelse af gruppen for at give flere oplysninger om, hvordan den skal bruges.

### <a name="manage-item-group-assignments"></a>Administrere tildelinger af varegrupper

Hver vare kan tilhøre et vilkårligt antal rabatstyringsgrupper. Hvis du vil se og tildele gruppemedlemmer, kan du starte enten fra gruppelisten eller fra varelisten. Du kan også tilføje varer på baggrund af kategorihierarkiet.

Hvis du vil se, tilføje eller fjerne varer for en valgt gruppe, skal du følge disse trin.

1. Gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Varegrupper**.
1. Vælg den gruppe, der skal administreres.
1. Vælg **Varer** i handlingsruden. Siden **Rabatstyringsgrupper** vises med en liste over varer, der allerede er medlem af den valgte gruppe.
1. Gå til handlingsruden, og vælg **Ny** for at føje en ny vare til gruppen ved at tilføje en række i gitteret. Angiv derefter følgende felt til den nye række:

    - **Varekonto** – Vælg varekonto-id.

1. Hvis du vil fjerne en vare fra gruppen, skal du markere varen og derefter vælge **Slet** i handlingsruden.

Hvis du vil se, tilføje eller fjerne gruppetildelinger for en valgt vare, skal du følge disse trin.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg den vare, du vil arbejde med.
1. Vælg **Rabatstyringsgrupper** i gruppen **Rabatstyring** i handlingsruden under fanen **Produkt**. Siden **Rabatstyringsgrupper** vises med en liste over grupper, som den valgte vare allerede er medlem af.
1. Gå til handlingsruden, og vælg **Ny** for at føje varen til en ny gruppe ved at tilføje en række i gitteret. Angiv derefter følgende felt til den nye række:

    - **Rabatstyringsgruppe** – Vælg den gruppe, hvor varen skal tilføjes.

1. Hvis du vil fjerne en vare fra en gruppe, skal du markere gruppen og derefter vælge **Slet** i handlingsruden.

Hvis du vil føje varer til en gruppe på basis af kategorihierarkiet, skal du følge disse trin.

1. Gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Varegrupper**.
1. Vælg den gruppe, der skal administreres.
1. Vælg **Tilføj varer** i handlingsruden.
1. Vælg en kategori på øverste niveau i feltet **Kategorihierarki** i dialogboksen **Tilføj varer**.
1. Varehierarkiet åbnes i venstre rude. Vælg det hierarkiniveau, du leder efter. 
1. Varer fra det valgte hierarki og hierarkiniveau vises nu i højre rude. Benyt følgende fremgangsmåde, når du vil arbejde med ruden:

    - Markér afkrydsningsfeltet for hver vare, du vil tilføje.
    - Markér afkrydsningsfeltet i gitteroverskriften for at vælge alle de viste varer.
    - Vælg knappen **Vis valgte** for at filtrere gitteret, så det kun viser de varer, du har valgt indtil videre. Vælg knappen igen for at vende tilbage til hele listen.

1. Vælg **OK** for at anvende dit varevalg på den valgte gruppe.
