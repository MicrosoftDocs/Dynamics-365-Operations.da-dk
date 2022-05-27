---
title: Forslag til leasingophør
description: Dette emne forklarer, hvordan du foreslår en leasingtransaktion til opsigelse.
author: moaamer
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseTerminateLeaseListPage
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 2f6990177251418bece8c99a0f9befa333d6549f
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/06/2022
ms.locfileid: "8720496"
---
# <a name="propose-a-lease-for-termination"></a>Foreslå en leasingaftale til opsigelse

[!include [banner](../includes/banner.md)]

Hvis en leasingaftale ophører før tid, kan aktivleasing registrere en fratrædelseskladdepost, der afskrives for det leasingforpligtelsen, ROU-forbrugsaktivet og akkumuleret afskrivning samt registrere vinding eller tab. I processen til tidlig fratrædelse afsluttes en leasingaftale, og dens tilknyttede leasingbøger. Det betyder ikke, at individuelle leasingbøger opsiges. Dette emne indeholder en beskrivelse af den funktionalitet, der giver dig mulighed for at foreslå en leasingaftale til fratrædelse og behandle kladdeposten til fratrædelsesposten.

Hvis en leasingaftale ikke er klassificeret som en udskudt rettighed til lejebehandling af leasingaftale og ikke er tilknyttet et anlægsaktiv, medfører leasing af anlægsaktivet følgende fratrædelseskladdepostering.

| Postering                           | Debet (D.) | Kredit (K.) |
|---------------------------------------|-------------|--------------|
| Dr. Leasingforpligtelse                   | X           |              |
| D. Akkumuleret afskrivning          | X           |              |
| Dr. Gevinst (tab) ved leasingændring | X           |              |
| Cr. Leasingaktiv                       |             | X            |
| Cr. Gevinst (tab) ved leasingændring |             | X            |

Hvis leasingbogen klassificeres som en udskudt lejebog, afskrives saldoen på den udskudte leje før fratrædelseskontoen som vist her.

| Postering                           | Debet (D.) | Kredit (K.) | 
|---------------------------------------|-------------|--------------|
| Dr. Udskudt leje                     | X           |              |
| Cr. Gevinst (tab) ved leasingændring |             | X            |
| Cr. Udskudt leje                     |             | X            |
| Dr. Gevinst (tab) ved leasingændring | X           |              |

Hvis leasingbogen er knyttet til et anlægsaktiv, vises ROU-aktivet i Anlægsaktiver. Dette regnskab omfatter regnskabet for tidlige fratrædelse. Leasing af et anlægsaktiv medfører, at følgende kladdeposter afskrives.

| Postering                           | Debet (D.) | Kredit (K.) |
|---------------------------------------|-------------|--------------|
| Dr. Leasingforpligtelse                   | X           |              |
| Cr. Gevinst (tab) ved leasingændring |             | X            |

Du kan finde oplysninger om den korrekte måde at kassere et ROU-aktiv på, under [Afvis et anlægsaktiv som spild](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md).

## <a name="propose-a-lease-for-termination"></a>Foreslå en leasingaftale til opsigelse

1. Gå til den leasingaftale, der skal afsluttes, og vælg derefter **Fratrædelsesforslag** i handlingsruden.

    > [!NOTE]
    > Knappen **Fratrædelsesforslag** er ikke tilgængelig, hvis der er ikke-bogførte kladdeposteringer i forhold til en bog. Før du kan afslutte leasingaftalen, skal du bogføre eller slette eventuelle kladdeposteringer, der er oprettet i forhold til leasingaftalen.

2. Angiv felterne **Ikrafttrædelsesdato** og **Bogføringsdato** for fratrædelseskladdeposteringen i den dialogboks, der vises.
3. Vælg **Fratrædelsesforslag** for at foreslå leasingaftalen til fratrædelse.
4. Vælg **Bogfør leasingfratrædelse** for automatisk at bogføre kladdeposten til fratrædelsesposten for leasingaftalen.
5. På siden **Fratrædelsesleasing** skal du vælge leasing-id for den leasing, du har foreslået til fratrædelse for at få vist fratrædelseslinjerne. Fratrædelseslinjerne viser regnskabsmæssige værdier for det ROU-aktivet, leasingforpligtelse, den akkumulerede afskrivning, eventuelt udskudt leje og den vinding eller tab, der skal registreres ved fratrædelse af leasingaftalen.

Leasingaftalen er nu klar til fratrædelse. Værdien i feltet **Fratrædelsesstatus** for leasingbogen ændres til **Klar til fratrædelse**. På dette tidspunkt kan du ikke længere bogføre kladdeposteringer mod leasingaftalen eller justere eller ændre den. 

## <a name="process-leases-that-are-ready-for-termination"></a>Behandle leasingaftaler, der er klar til fratrædelse

Hvis du vil behandle leasingaftaler, der er klar til fratrædelse og bogføre fratrædelseskladdeposten, skal du følge disse trin.

1. Vælg den leasingaftale, der skal justeres, og vælg **Fratrædelsesleasing** på siden **Afslut**.
2. Vælg **OK** i dialogboksen, der vises.

Systemet bogfører kladdeposten for fratrædelse. Feltet **Leasingstatus** for leasingbogen er angivet til **Afsluttet**, og **Status for fratrædelsesforslag** angives til **Afsluttet**.

## <a name="reverse-a-lease-termination"></a>Tilbageføre en afslutning af en leasingaftale

Hvis du vil tilbageføre en kladdepost for en leasingaftale og åbne en fratrådt leasingaftale, skal du følge dette trin.

- Vælg den leasingaftale, der skal justeres, og vælg **Tilbagefør afslutning** på siden **Fratrædelsesleasing**.

Systemet tilbagefører kladdeposten for fratrædelse. Feltet **Leasingstatus** for leasingbogen angives til **Åben**. Leasingaftalen vises ikke længere på siden **Fratrædelsesleasing** og kan foreslås igen i forbindelse med fratrædelse.

## <a name="example-of-a-lease-termination"></a>Eksempel på en fratrædelsesleasing

I dette eksempel er leasingaftalen tilknyttet et ikke-specialiseret aktiv, der ikke overfører ejerskab, eller giver leasingtageren mulighed for at købe.

### <a name="setup"></a>Konfiguration

Følgende tabeller viser de værdier, der er angivet under fanerne **Generelt** og **Betalingsplanlinjer** for den leasingaftale, der bruges i dette eksempel.

Fanen **Generelt**

| Felt                      | Værdi            |
|----------------------------|------------------|
| Aktivets handelsværdi    | 600,000          |
| Valuta                   | USD              |
| Oprindelige direkte omkostninger       | 1.000            |
| Trinvis lånesats | 7 %               |
| Sammensætningsinterval       | Årligt         |
| Brugstid for aktiv (måneder) | 600              |
| Annuitetstype               | Almindelig annuitet |
| Dato for påbegyndelse          | 1/1/2019         |

**Betalingsplanlinjer-fane**

| Felt             | Værdi      |
|-------------------|------------|
| Igangsæt dato        | 1/1/2019   |
| Periodeinterval   | Månedligt    |
| Perioder           | 120        |
| Slutdato          | 31/12/2028 |
| Betalingshyppighed | Årligt   |
| Betalingsbeløb    | 10,000     |

### <a name="steps-for-terminating-the-lease"></a>Trin til afslutning af leasingaftale

1. Når du har oprettet leasingaftalen som beskrevet tidligere i dette emne, skal du gå til leasingkartoteket og bekræfte betalingsplanen. Bogfør derefter kladdeposten for den oprindelige genkendelse. Det oprindelige ROU-aktiv er $71.235,81, og leasingforpligtelse skal være $70.235,81. I dette eksempel blev leasingaftalen klassificeret som en driftsleasingaftale i henhold til Accounting Standards Codification Topic 842 (ASC 842).
2. Kør batchkladdeprocessen tre gange for at simulere passagen af tre år for leasingbetalingerne, renteudgifterne og afskrivningsudgifterne.
3. Når du er færdig med at køre alle tre kørsler, skal du gå tilbage til leasingkartoteket og åbne tabellerne Passiv- og Aktivposteringer for at få vist den aktuelle værdi af ROU-aktivet og leasingforpligtelsen. Efter tre år bør ansvarsværdien være cirka $-53.893,00, og aktivets værdi skal være ca. $54.593,00.

    Når de tre år er overskredet, aftaler virksomheden og leasinggiveren gensidigt at opsige leasingaftalen. Du skal derfor afslutte leasingaftalen nu.

4. Gå til den leasingaftale, der skal afsluttes, og vælg derefter **Fratrædelsesforslag** i handlingsruden. 
5. I den dialogboks, der vises, skal du skrive **1/1/2021** i feltet **Ikrafttrædelsesdato** og **Bogføringsdato**.
6. Vælg **Fratrædelsesforslag** for at foreslå leasingaftalen til fratrædelse.

    Siden **Fratrædelsesleasing** vises og viser den leasingaftale, der afsluttes.

7. Hvis du vil vise fratrædelseslinjerne skal du vælge leasing-id for den leasing, du har foreslået til fratrædelse. Fratrædelseslinjerne viser værdien af leasingaftalen. Følgende tabel viser, hvad disse værdier skal bruges til i dette eksempel. 

    | Felt                                                 | Værdi      |
    |-------------------------------------------------------|------------|
    | Overføre passivsaldo i transaktionsvaluta | $53.892,89 |
    | Brugsaktiv i transaktionsvaluta            | $71.235,81 |
    | Akkumuleret afskrivning i transaktionsvaluta      | $16.642,92 |
    | Gevinst (tab) i transaktionsvaluta                   | $-700,00   |

8. Vælg den leasingaftale, der skal posteres, og vælg **Afslut** på siden **Fratrædelsesleasing**.
9. Vælg **OK** i dialogboksen, der vises.
10. Du kan få vist kladdeposten for fratrædelse, der er oprettet og bogført, ved at gå til aktivets leasingkladde i leasingbogen. Følgende tabel viser, hvad disse posteringer skal bruges til i dette eksempel.

    | Postering                           | Debet (D.) | Kredit (K.) |
    |---------------------------------------|-------------|--------------|
    | Dr. Leasingforpligtelse                   | 53,892.89   |              |
    | D. Akkumuleret afskrivning          | 16,642.92   |              |
    | Dr. Gevinst (tab) ved leasingændring | 700.00      |              |
    | Cr. Leasingaktiv                       |             | 71,235.81    |

11. Hvis du vil have vist nettovirkningen af fratrædelsen, hvor ROU-aktivet og leasingforpligtelsen er 0 (nul), skal du åbne tabellerne Passiv- og Aktivposteringer.

Status for leasingaftalen skal nu være **Afsluttet**. Der bogføres ingen yderligere kladdeposteringer mod denne leasingaftale, medmindre fratrædelsen tilbageføres.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
