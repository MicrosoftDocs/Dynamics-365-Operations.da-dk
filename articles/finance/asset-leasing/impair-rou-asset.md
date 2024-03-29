---
title: Forringe et brugsretsaktiver
description: Denne artikel beskriver de funktioner, der registrerer en forringelse og justerer aktivafskrivningsplanen for et regnskabsstandarder Codification Emne 842 (ASC 842) operationel leasing.
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f953b3a351859c6becba10a129bbb17b49be6290
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894107"
---
# <a name="impair-right-of-use-assets"></a>Forringe brugsretsaktiver

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Hvis det ikke er muligt at genoprette et ROU aktivbeløb, skal du muligvis teste, om aktivet er forringet. Hvis du mener, at aktivet forringes, kan aktivleasing registrere forbrydelsen og justere afskrivningsplanen tilsvarende. Denne artikel beskriver de funktioner, der registrerer forringelse og justerer aktivafskrivningsplanen for et regnskabsstandarder Codification Emne 842 (ASC 842) operationel leasing. Den samme metode gælder også for International Financial Reporting Standard 16 (IFRS 16) leasinger.

Den resterende saldo på ROU-aktivet vil blive amortiseret på et lineært grundlag for det antal perioder, der er tilbage, uanset om rettigheden er klassificeret som en finansieringsleasing i henhold til IFRS 16 eller en driftsleasing under ASC 842.

## <a name="impair-an-rou-asset"></a>Forringe et ROU-aktiv

1. Gå til den forringede leasingaftale, og vælg **Kartotek**.
2. Vælg **Forringelse** i handlingsruden.
3. Angiv beløbet for aktivets forringet i feltet **Nedskrivningsbeløb** i den dialogboks, der vises. Hvis du vil reducere ROU-aktivet, skal du angive en positiv værdi.
4. Angiv den dato, hvor nedslags posten skal bogføres, i feltet **Posteringsdato**.
5. Angiv det resterende antal måneder, der skal amortiseres, i feltet **Resterende perioder**.
6. Angiv indstillingen **Forhåndsvisning** til at vise den foreslåede aktivsaldo og økonomiske post, før de oprettes eller bogføres.
7. Angiv indstillingen **Luk kartotek** til **Ja** for at lukke leasingkartoteket. Du kan fortryde denne handling ved at bruge statussen **Åbn leasing igen**. Der kan ikke bogføres poster mod lukkede leasingaftaler, og lukkede leasingaftaler kan ikke reguleres. 
8. Vælg **Bogfør** for at oprette eller bogføre værdiforringelsesposten.

    > [!NOTE]
    > Når posteringen for en værdiforringelse er bogført, oprettes der en ny kartoteksversion.

    > Hvis leasingen er klassificeret som en operationel leasing, beregnes den månedlige afskrivning efter værdiforringelse med en lineær afskrivning.

9. Hvis du vil se den afskrivningsplan for værdiforringelse fo anlægsaktiver, skal du åbne siden med afskrivningsplanen for leasingkartoteket. Aktivet afskrives nu på et lineært grundlag i det antal måneder, du har angivet i feltet **Resterende perioder**.
10. Hvis du vil have vist kladdeposter for værdiforringelse, skal du vælge **Aaktivleasingkladde** i handlingsruden i kartoteket Forringet leasing. Systemet opretter en kladdepost, der debiterer bogføringskontoen for forringede udgifter og krediterer bogføringskontoen for anlægsaktivet. 
11. Hvis du vil have vist den nye værdi for ROU-aktivet, skal du vælge **Aaktivposteringer** i handlingsruden i kartoteket Leasingaftale.

## <a name="example-of-rou-asset-impairment"></a>Eksempel på ROU-aktivforringelse

I dette eksempel er leasingaftalen et ikke-specialiseret aktiv, der ikke overfører ejerskab, eller giver leasingtageren mulighed for at købe.

### <a name="setup"></a>Konfiguration

Følgende tabeller viser de værdier, der er angivet under fanerne **Generelt** og **Betalingsplanlinjer** for den leasingaftale, der bruges i dette eksempel.

Fanen **Generelt**

| Felt                      | Værdi            |
|----------------------------|------------------|
| Aktivets handelsværdi    | 600,000          |
| Trinvis lånesats | 7 %               |
| Sammensætningsinterval       | Årligt         |
| Brugstid for aktiv (måneder) | 600              |
| Annuitetstype               | Almindelig annuitet |
| Dato for påbegyndelse          | 01/01/2019       |

**Betalingsplanlinjer-fane**

| Felt             | Værdi      |
|-------------------|------------|
| Igangsæt dato        | 1/1/2019   |
| Periodeinterval   | Månedligt    |
| Perioder           | 120        |
| Slutdato          | 31/12/2028 |
| Betalingshyppighed | Årligt   |
| Betalingsbeløb    | 10,000     |

### <a name="steps"></a>Trin

1. Når du har oprettet leasingaftalen som beskrevet tidligere i denne artikel, skal du gå til leasingkartoteket og bekræfte betalingsplanen. Bogfør derefter kladdeposten for den oprindelige genkendelse. Det oprindelige ROU-aktiv og leasingansvar skal være $70.235,81. I dette eksempel blev rettigheden klassificeret som en driftsleasingaftale i henhold til ASC 842.
2. Kør batchkladdeprocessen tre gange for at simulere passagen af tre år for leasingbetalingerne, renteudgifterne og afskrivningsudgifterne.
3. Når du er færdig med at køre alle tre kørsler, skal du gå tilbage til leasingkartoteket og åbne tabellerne passiv- og aktivposteringer for at få vist den aktuelle værdi af ROU-aktivet og leasingforpligtelsen. Efter tre år bør ansvarsværdien være cirka $-53.893,00, og aktivets værdi skal være ca. $53.893,00. 

    Efter tre år kan virksomheden udføre værdiforringelsestest, og det bestemmes, at ROU-aktivet har en forringelse på $35.000. Du skal nu angive denne værdiforringelse.
    
4. Gå til leasingkartoteket, og vælg derefter **Værdiforringelse** i handlingsruden.
5. Angiv følgende oplysninger på siden **Værdiforringelsesparameter**.

    | Felt                  | Værdi    |
    |------------------------|----------|
    | Værdiforringelsesbeløb      | 35,000   |
    | Transaktionsdato       | 1/1/2022 |
    | Resterende perioder      | 84       |
    | Bogfør                   | Ja      |
    | Forhåndsvisning før bogføring | Nej       |
    | Luk bog             | Nej       |

6. Der er oprettet og bogført en kladdepostering for værdiforringelsen. Hvis du vil se den, skal du gå til aktivets leasingkladde i leasingkartoteket. Bemærk, at beløbet for forringelsen blev debiteret på bogføringskontoen for værdiforringelsen, og at bogføringskontoen for ROU er krediteret.

7. Hvis du vil have vist nettoeffekten af værdiforringelsen, skal du gå til tabellerne for passiver og aktiver. Bemærk, at udgiften til værdiforringelsen har formindsket ROU-aktivet, men at der ikke er ændret et overførselsbeløb for leasingforpligtelsen.

Værdiforringelsen har én anden effekt, du skal overveje. Da ROU-aktivbeløbet nu er meget mindre end leasingforpligtelsen, skal beløbet afskrives anderledes end før. Specielt afskrives aktivet nu i en lineær måde i løbet af de resterende 84 måneder af leasingaftalen med start på transaktionsdatoen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
