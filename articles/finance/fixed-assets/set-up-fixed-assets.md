---
title: Konfigurere anlægsaktiver
description: Dette emne indeholder en oversigt over opsætning af modulet Anlægsaktiver.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8196ddc879df1f398aabef0c1c4064bf0d4fff2c
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771912"
---
# <a name="set-up-fixed-assets"></a>Konfigurere anlægsaktiver

[!include [banner](../includes/banner.md)]

Dette emne indeholder en oversigt over opsætning af modulet **Anlægsaktiver**.

## <a name="overview"></a>Overblik

Parametre styrer den generelle funktionsmåde i Anlægsaktiver.

Anlægsaktivgrupper kan gruppere anlægsaktiverne og angive standardattributter for hvert aktiv, der er knyttet til en gruppe. Bøger knyttes til anlægsaktivgrupper. Bøger sporer den økonomiske værdi af et anlægsaktiv over tid ved hjælp af konfigurationen af afskrivning, der er defineret i afskrivningsprofilen.

Anlægsaktiver tildeles en gruppe, når de oprettes. Som standard tildeles de bøger, der er tilknyttet anlægsaktivgruppen, derefter til anlægsaktivet. Bøger, der er konfigureret til at bogføre i finans, er knyttet til en posteringsprofil. Finanskonti defineres for hver bog i posteringsprofilen og bruges, når anlægsaktivposter bogføres.

![Anlægsaktivkomponenter](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Afskrivningsprofiler

Du skal først oprette afskrivningsprofiler. I afskrivningsprofilen kan du konfigurere, hvordan værdien af et aktiv afskrives over tid. Du skal angive metoden for afskrivning, afskrivningsår (kalenderår eller regnskabsår) og hyppigheden af afskrivning. Du kan finde flere oplysninger i [Konfigurer og opret afskrivningsprofiler](tasks/set-up-depreciation-profiles.md).

## <a name="books"></a>Bøger

Når du har konfigureret afskrivningsprofiler, skal du oprette de krævede bøger for dine aktiver. Hver bog sporer en uafhængig økonomisk livscyklus for et aktiv. Bøger kan konfigureres til at bogføre tilknyttede transaktioner i finans. Denne konfiguration er standardindstillingen, fordi den bruges typisk til virksomhedens regnskabsaflæggelse. Bøger, der ikke bogføres i finans, bogføres kun til anlægaktivers reskontro og bruges typisk til momsrapporteringen.

En primære afskrivningsprofil er tilknyttet hver bog. Bøger har også en alternativ eller skifteafskrivningsprofil, hvis denne profiltype er relevant. For at medtage anlægskartoteket automatisk i afskrivningskørsel skal du aktivere **Beregn afskrivning**-indstillingen. Hvis denne indstilling ikke er aktiveret for et aktiv, springer afskrivningsforslaget aktivet over.

Du kan også oprette afledte bøger. De angivne afledte transaktioner bogføres mod de afledte bøger som en nøjagtig kopi af den primære transaktion. Derfor er afledte transaktioner normalt angivet til anskaffelser og kassation, ikke til afskrivningstransaktioner. Du kan finde flere oplysninger i [Opsætning af værdimodeller](tasks/set-up-value-models.md).

## <a name="fixed-asset-posting-profiles"></a>Posteringsprofiler for anlægsaktiver

Når du har konfigureret bøger, kan du oprette posteringsprofilen. Posteringsprofilen skal være defineret i bogen, men den kan også defineres på et mere detaljeret niveau. For eksempel kan du definere posteringsprofilen for kombinationen af en bog og en anlægsaktivgruppe eller endda for et enkelt anlægskartotek. Som standard bruges de finanskonti, der er defineret, til posteringer for anlægsaktiver.

Du skal definere de finanskonti, der bruges under kassationsprocessen, både kassationssalg og kassation af spild. På tidspunktet for salg tilbageføres de anlægsaktivposteringer, der tidligere er bogført fra det oprindelige regnskab. Nettobeløbene flyttes derefter til den relevante konto for gevinst eller tab for kassation af aktiver. For at sikre, at transaktionerne er tilbageført korrekt, skal du oprette konti for hver type transaktion, som du bruger i din virksomhed. Hovedkontoen bør være den oprindelige konto, som du angiver i posteringsprofilen for den pågældende transaktionstype, mens modkontoen bør være gevinst eller tab for kassationskontoen. Undtagelsen er den bogførte nettoværdi. I dette tilfælde skal både hovedkontoen og modkontoen være angivet til gevinst og tab for kassationskontoen. Du kan finde flere oplysninger under [Oprette posteringsprofiler for anlægsaktiver](tasks/set-up-fixed-asset-posting-profiles.md).

## <a name="fixed-asset-groups"></a>Anlægsaktivgrupper

Feltet **Anlægsaktivgruppe** er det eneste obligatoriske felt, når du opretter et anlægsaktiv. Værdien af dette felt bestemmer standardværdien for flere oplysningsfelter for aktivet. Bøger er konfigureret, så en standardbog er knyttet til hvert aktiv i en gruppe. På denne måde kan attributter, du angiver for bøgerne, være specifikke for en gruppe af anlægsaktiver. Disse attributter omfatter levetid og afskrivningsprincip.

Du kan også definere særlige afskrivninger eller straksafskrivning for en bestemt kombination af en anlægsaktivgruppe og en bog. Du skal tildele en prioritet til særlig afskrivning for at angive den rækkefølge, som fradrag beregnes i, når flere fradrag er tildelt en bog. Du kan finde flere oplysninger under [Konfigurere anlægsaktivgrupper](tasks/set-up-fixed-asset-groups.md).

## <a name="journal-names"></a>Kladdenavne

På siden **Kladdenavne** skal du oprette de kladdenavne, der skal bruges til anlægsaktiverne. Du skal angive feltet **Kladdetype** til **Bogføring af anlægsaktiver**. Angiv feltet **Bilagsserier**, så kladdenavnene bruges til anlægsaktivkladden. Anlægsaktivkladder må ikke bruge indstillingen **Kun ét bilagsnummer**, fordi ser kræves et entydigt bilagsnummer til flere automatiserede processer, f.eks. ved overførsler og opdelinger.

## <a name="fixed-asset-parameters"></a>Anlægsaktivernes parametre

Det sidste trin er at opdatere parametrene for anlægsaktiver.

Feltet **Grænse for kapitalisering** bestemmer de aktiver, der afskrives. Hvis en indkøbslinje er valgt som et anlægsaktiv, men det ikke længere opfylder den angivne grænse for kapitalisering, bliver et anlægsaktiv stadig oprettet eller opdateret, men **Beregn afskrivning**-indstillingen er angivet til **Nej**. Derfor afskrives aktivet ikke automatisk som en del af afskrivningsforslagene.

Indstillingen **Opret automatisk afskrivningsreguleringsbeløb med afhændelse** er vigtig. Når du angiver denne indstilling til **Ja**, bliver afskrivningen af anlægsaktivet automatisk reguleret, baseret på indstillingerne for afskrivning ved aktivkassation. Med en anden indstilling kan du fratrække kasserabatter fra anskaffelsesbeløbet, når du anskaffer anlægsaktiver ved hjælp af en kreditorfaktura.

I oversigtspanelet **Indkøbsordrer** kan du konfigurere, hvordan aktiver skal oprettes som en del af indkøbsprocessen. Den første mulighed hedder **Tillad aktivanskaffelse fra Indkøb**. Hvis du angiver denne indstilling til **Ja**, foregår aktivanskaffelse, når fakturaen bogføres. Hvis du angiver denne indstilling til **Nej**, kan du stadig placere et anlægsaktiv på en indkøbsordre (IO) og en faktura, men anskaffelsen bogføres ikke. Bogføring skal foretages i et separat trin fra anlægsaktivkladden. Med indstillingen **Opret aktiv under bogføring af produktkvittering eller faktura** kan du oprette et nyt aktiv "med det samme" under bogføringen. Derfor behøver aktivet ikke sættes op som et anlægsaktiv før posteringen. Den sidste indstilling, **Kontrollér, om der oprettes anlægsaktiver under indtastning på linjen**, gælder kun for indkøbsrekvisitioner.

Du kan konfigurere årsagskoder, så de er nødvendige for ændringer af et anlægsaktiv eller specifikke anlægsaktivtransaktioner.

Endelig kan du under fanen **Nummerserier** definere nummerserier for anlægsaktiver. Nummerserien for **anlægsaktiver** kan tilsidesættes af nummerserien for **anlægsaktivgruppen**, hvis den er angivet.

Du kan finde flere oplysninger under [Oprette et anlægsaktiv](tasks/create-fixed-asset.md).
