---
title: Registrere varer aktiveret til lagerstyringsprocesser ved hjælp af en varemodtagelseskladde
description: Denne artikel præsenterer et scenario, der viser, hvordan du registrerer varer ved hjælp af varemodtagelseskladden, når du bruger lokationsstyringsprocesser (WMS).
author: Mirzaab
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66fc9e21b79d70ec14750440c74d354bb8ec0695
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219592"
---
# <a name="register-items-enabled-for-warehouse-management-processes-using-an-item-arrival-journal"></a>Registrere varer aktiveret til lagerstyringsprocesser ved hjælp af en varemodtagelseskladde

[!include [banner](../../includes/banner.md)]

Denne artikel præsenterer et scenario, der viser, hvordan du registrerer varer ved hjælp af varemodtagelseskladden, når du bruger lokationsstyringsprocesser (WMS). Dette vil normalt blive udført af en modtagende medarbejder.

## <a name="enable-sample-data"></a>Aktivér eksempeldata

Hvis du vil gennemgå dette scenario ved hjælp af de eksempelposter og værdier, der er angivet i denne artikel, skal du bruge et system, hvor [standarddemodataene](../../../fin-ops-core/fin-ops/get-started/demo-data.md) er installeret, og du skal vælge den juridiske enhed *USMF*, før du går i gang.

Du kan i stedet gennemgå dette scenario ved at erstatte værdier fra dine egne data, hvis du har følgende tilgængelige data:

- Du skal have en bekræftet indkøbsordre med en åben indkøbsordrelinje.
- Varen på linjen skal være på lager. Den må ikke bruge produktvarianter og må ikke have sporingsdimensioner.
- Varen skal være tilknyttet en lagringsdimensionsgruppe, hvor lagerstyringsproces er aktiveret.
- Det lagersted, der bruges, skal være aktiveret for WMS og den lokalitet, du bruger til modtagelse, skal være id-kontrolleret.

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a>Oprette en overskrift til varemodtagelseskladde, der bruger lokationsstyring

I følgende scenario vises, hvordan du kan oprette en overskrift til varemodtagelseskladden, der bruger lokationsstyring:

1. Kontrollér, at systemet indeholder en bekræftet indkøbsordre, der opfylder de krav, der er beskrevet i forrige afsnit. I dette scenario bruges en indkøbsordre for firmaet *USMF*, leverandørkonto *1001*, lagersted *51*, med en ordrelinje på *10 PL* (10 paller) af varenummer *M9200*.
1. Notér dig købsordrenummeret, du skal bruge.
1. Gå til **Lagerstyring \> Kladdeposteringer \> Varemodtagelse \> Varemodtagelse**.
1. Vælg **Ny** i handlingsrude.
1. Dialogboksen **Opret lokationsstyringskladde** åbnes. Vælg et kladdenavn i feltet **Navn**.
    - Hvis du bruger eksempeldataene *USMF*, skal du vælge *WHS*.
    - Hvis du bruger dine egne data, skal den kladde, du vælger, have **Undersøg plukplads** angivet til *Nej*, og **Karantænestyring** skal være angivet til *Nej*.
1. Indstil **Reference** til *Indkøbsordre*.
1. Angiv **Kontonummer** til *1001*.
1. Angiv **Nummer** til nummeret på den indkøbsordre, du har identificeret til denne øvelse.

    ![Varemodtagelseskladde.](../media/item-arrival-journal-header.png "Varemodtagelseskladde")

1. Vælg **OK** for at oprette kladdehovedet.
1. Vælg **Tilføj linje** i sektionen **Kladdelinjer**, og angiv følgende data:
    - **Varenummer** – Angiv til *M9200*. **Lokation**, **Lagersted** og **Antal** angives på basis af lagertransaktionsdataene for de 10 paller (1000 hver).
    - **Lokation** – Angiv til *001*. Denne specifikke lokation sporer ikke nummerplader.

    ![Linje på varemodtagelseskladde.](../media/item-arrival-journal-line.png "Varemodtagelseskladdelinje")

    > [!NOTE]
    > Feltet **Dato** angiver den dato, hvor det disponible antal af denne vare registreres på lageret.  
    >
    > **Parti-id** udfyldes af systemet, hvis det kan identificeres entydigt fra de givne oplysninger. Ellers skal du angive det manuelt. Dette er et påkrævet felt, der sammenkæder denne registrering med en bestemt kildedokumentlinje.  

1. Vælg **Valider** i handlingsruden. Dette kontrollerer, at kladden er klar til at blive bogført. Hvis valideringen mislykkes, skal du rette fejlene, før du kan bogføre kladden.  
1. Dialogboksen **Kontrollér kladde** åbnes. Vælg **OK**.
1. Gennemgå meddelelseslinjen. Der bør være en meddelelse om, at handlingen er fuldført.  
1. Vælg **Bogfør** i handlingsruden.
1. Dialogboksen **Bogfør kladde** åbnes. Vælg **OK**.
1. Gennemgå meddelelseslinjen. Der bør være en meddelelse om, at handlingen er fuldført.
1. Vælg **Funktioner > Produktkvittering** i handlingsruden for at opdatere indkøbsordrelinjen og bogføre en produktkvittering.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
