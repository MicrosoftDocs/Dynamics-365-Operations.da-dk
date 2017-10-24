---
title: "Konfigurer anlægsaktiver"
description: "Dette emne indeholder en oversigt over opsætning af modulet Anlægsaktiver."
author: twheeloc
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d16c9ca5740c27528d74800957f9b47984c135cd
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-fixed-assets"></a>Konfigurer anlægsaktiver

[!include[banner](../includes/banner.md)]


Dette emne indeholder en oversigt over opsætning af modulet Anlægsaktiver.

<a name="overview"></a>Overblik
--------
Parametre styrer den generelle funktionsmåde i Anlægsaktiver.

Anlægsaktivgrupper kan gruppere anlægsaktiverne og angive standardattributter for hvert aktiv, der er knyttet til en gruppe. Bøger knyttes til anlægsaktivgrupper. Bøger sporer den økonomiske værdi af et anlægsaktiv over tid ved hjælp af konfigurationen af afskrivning, der er defineret i afskrivningsprofilen.

Anlægsaktiver tildeles en gruppe, når de oprettes. Som standard tildeles de bøger, der er tilknyttet anlægsaktivgruppen, derefter til anlægsaktivet. Bøger, der er konfigureret til at bogføre i finans, er knyttet til en posteringsprofil. Finanskonti definere pr. bog i posteringsprofilen og bruges, når anlægsaktivposter bogføres. 

![FixedAssetsComponentsImage](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Afskrivningsprofiler
Afskrivningsprofiler skal oprettes først. I afskrivningsprofilen kan du konfigurere, hvordan værdien af et aktiv afskrives over tid. Du skal angive metoden for afskrivning, afskrivningsår (kalenderår eller regnskabsår) og hyppigheden af afskrivning. Du kan finde flere oplysninger i [Konfigurere og oprette afskrivningsprofiler](tasks/set-up-depreciation-profiles.md).

## <a name="books"></a>Bøger
Når du har konfigureret afskrivningsprofiler, skal du oprette de krævede bøger for dine aktiver. Hver bog sporer en uafhængig økonomisk livscyklus for et aktiv. Bøger kan konfigureres til at bogføre tilknyttede transaktioner i finans. Denne konfiguration er standardindstillingen, fordi den typisk bruges til virksomhedens regnskabsaflæggelse. Bøger, der ikke bogføres i finans, bogføres kun til anlægsaktivers reskontro og bruges typisk til momsrapporteringen.

En primære afskrivningsprofil er tilknyttet hver bog. Bøger har også en alternativ eller skifteafskrivningsprofil, hvis denne profiltype er relevant. For at medtage anlægskartoteket automatisk i afskrivningskørsel skal du aktivere Beregn afskrivning-indstillingen. Hvis denne indstilling ikke er markeret for et aktiv, springer afskrivningsforslaget aktivet over.

Du kan også oprette afledte bøger. De angivne afledte transaktioner bogføres som en nøjagtig kopi af den primære transaktion mod de afledte bøger. Derfor er afledte transaktioner normalt angivet til anskaffelser og kassation, ikke til afskrivningstransaktioner.
Du kan finde flere oplysninger under [Opsætning af bøger](tasks/set-up-value-models.md).

## <a name="fixed-asset-posting-profiles"></a>Posteringsprofiler for anlægsaktiver
Når du har konfigureret bøger, kan du oprette posteringsprofilen. Posteringsprofilen skal være defineret i bogen, men den kan også defineres på et mere detaljeret niveau. For eksempel kan du definere posteringsprofilen for kombinationen af en bog og en anlægsaktivgruppe eller endda for et enkelt anlægskartotek. Som standard bruges de finanskonti, der er defineret, til posteringer for anlægsaktiver.

Du skal definere de finanskonti, der bruges under kassationsprocessen, både kassationssalg og kassation af spild. De anlægsaktivposteringer, der tidligere er bogført, tilbageføres fra de oprindelige konti på tidspunktet for kassation, og nettobeløbene flyttes til den relevante konto for gevinst og tab ved kassation af aktiver. For at sikre, at transaktionerne er tilbageført korrekt, skal du oprette konti for hver type transaktion, som du bruger i din virksomhed. Hovedkontoen bør være den oprindelige konto, som du angiver i posteringsprofilen for den pågældende transaktionstype, mens modkontoen bør være gevinst eller tab for kassationskontoen. Undtagelsen er den bogførte nettoværdi. I dette tilfælde skal både hovedkontoen og modkontoen være angivet til gevinst og tab for kassationskontoen. Du kan finde flere oplysninger under [Oprette posteringsprofiler for anlægsaktiver](tasks/set-up-fixed-asset-posting-profiles.md).

## <a name="fixed-asset-groups"></a>Anlægsaktivgrupper
Anlægsaktivgruppe er det eneste obligatoriske felt, når du opretter et anlægsaktiv. Værdien af dette felt bestemmer standardværdien for flere oplysningsfelter for aktivet. Bøger er konfigureret, så en standardbog er knyttet til hvert aktiv i en gruppe. Du kan derefter angive attributter for de bøger, der er specifikke for en gruppe af aktiver, såsom Levetid og Afskrivningsprincip.

Du kan også definere særlige afskrivninger eller straksafskrivning for en bestemt kombination af en anlægsaktivgruppe og en bog. Du skal tildele en prioritet til særlig afskrivning for at angive den rækkefølge, som fradrag beregnes i, når flere fradrag er tildelt en bog. Du kan finde flere oplysninger under [Konfigurere anlægsaktivgrupper](tasks/set-up-fixed-asset-groups.md).

## <a name="fixed-asset-parameters"></a>Anlægsaktivernes parametre
Det sidste trin er at opdatere parametrene for anlægsaktiver.

Feltet **Grænse for kapitalisering** bestemmer de aktiver, der afskrives. Hvis en indkøbslinje er valgt som et anlægsaktiv, men det ikke længere opfylder den angivne grænse for kapitalisering, bliver et anlægsaktiv stadig oprettet eller opdateret, men Beregn afskrivning-indstillingen er angivet til Nej. Derfor afskrives aktivet ikke automatisk som en del af afskrivningsforslagene.

Indstillingen **Opret automatisk afskrivningsreguleringsbeløb med afhændelse** er vigtig. Når du angiver denne indstilling til **Ja**, bliver afskrivning af anlægsaktivet automatisk reguleret, baseret på indstillingerne for afskrivning ved aktivkassation. Med en anden indstilling kan du fratrække kasserabatter fra dit anskaffelsesbeløb, når du anskaffer anlægsaktiver ved hjælp af en kreditorfaktura.

I oversigtspanelet Indkøbsordrer kan du konfigurere, hvordan aktiver skal oprettes som en del af indkøbsprocessen. Den første mulighed er Tillad aktivanskaffelse fra Indkøb. Hvis du angiver denne indstilling til Ja, foregår aktivanskaffelse, når fakturaen bogføres. Hvis du angiver denne indstilling til Nej, kan du stadig placere et anlægsaktiv på en indkøbsordre (IO) og en faktura, men anskaffelsen bogføres ikke. Bogføring skal foretages i et separat trin fra anlægsaktivkladden. Med indstillingen Opret aktiv under bogføring af produktkvittering eller faktura kan du oprette et nyt aktiv "i en fart" under bogføring, så det ikke behøver at være sat op som et anlægsaktiv før transaktionen. Den sidste indstilling, Kontrollér, om der oprettes anlægsaktiver under indtastning på linjen, gælder kun for indkøbsrekvisitioner.

Du kan konfigurere årsagskoder, så de er nødvendige for ændringer af et anlægsaktiv eller specifikke anlægsaktivtransaktioner.

Endelig kan du under fanen Nummerserier definere nummerserier for anlægsaktiver. Nummerserien for anlægsaktiver kan tilsidesættes af nummerserien for anlægsaktivgruppen, hvis den er angivet.

Du kan finde flere oplysninger under [Oprette et anlægsaktiv](tasks/create-fixed-asset.md).


