---
title: Svar på leverandørspørgsmål i forbindelse med tilbudsanmodninger
description: Leverandører, der har spørgsmål til en RFP, kan sende deres spørgsmål og læse svarene på siden til **Kreditorsamarbejde**.
author: velofog
manager: AnnBe
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.search.industry: public sector
ms.author: v-alpavk
ms.search.validFrom: 2020-1-22
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 75bf839fbda034609eb2a9e36520ae113f4701ec
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015436"
---
# <a name="responding-to-vendor-questions-on-request-for-quotations"></a>Svar på leverandørspørgsmål i forbindelse med tilbudsanmodninger

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Når dit kontor har sendt en tilbudsanmodning, har leverandørerne nogle gange spørgsmål, der vedrører anmodningen. Leverandører, der har spørgsmål til en RFP, kan sende deres spørgsmål og læse svarene på siden til **Kreditorsamarbejde**, når du gør siden tilgængelig for dem. Når leverandørspørgsmål er accepteret, er **Spørgsmål og svar** tilgængelige på siden **Bud på tilbudsanmodning** i **Kreditorsamarbejde** og for dit kontor via siden **Tilbudsanmodning** i **Spørgsmål og svar**. 

Brugerne kan udgive svar på leverandørspørgsmål mere end én gang. Kreditorer kan ikke længere postere spørgsmål, når en leverandør er valgt, og tilbudsanmodningen er tildelt, eller når skæringsdatoen for spørgsmål er nået.

## <a name="setting-up-for-vendor-questions"></a>Opsætning af leverandørspørgsmål
Når du opretter en tilbudsanmodning, bestemmer du, om leverandører kan stille spørgsmål til tilbudsanmodningen.
1. Gå til **Indkøb og forsyning > Tilbudsanmodninger**, og klik på **Ny > Tilbudsanmodning**. 
2. På siden **Ny tilbudsanmodning** skal **Hoved** angives til **Indstillinger for leverandørspørgsmål** for at tillade spørgsmål før en bestemt dato.
- Angiv indstillingen **Tillad leverandørspørgsmål** til **Ja**, så leverandørerne kan skrive spørgsmål. Brugerne kan angive og besvare spørgsmål og udpege ofte stillede spørgsmål til udgivelse for leverandører, når tilbudsanmodningen er sendt til leverandørerne.
3. Valgfrit: Definer feltet **Skæringsdato**, hvor spørgsmål senest skal indsendes. Hvis der ikke angives en skæringsdato, accepteres spørgsmålene, så længe tilbudsanmodningen er åben og accepterer bud.
4. Klik på **Gem** for at gemme tilbudsanmodningen.
5. Klik på **Send** for at sende tilbudsanmodningen til leverandører.

## <a name="entering-and-replying-to-vendor-questions"></a>Angive og besvare leverandørspørgsmål
Leverandører skriver spørgsmål i **Kreditorsamarbejde > Bud på tilbudsanmodning**, oversigtspanelet **Leverandørspørgsmål**. Spørgsmålet er kun synligt for leverandøren og brugerne.

## <a name="entering-a-vendor-question"></a>Angive et leverandørspørgsmål
1. I Kreditorsamarbejde skal du på siden **Bud på tilbudsanmodning** klikke på **Spørgsmål og svar** og derefter klikke på **+ Stil et spørgsmål**.

[Bemærk!] Alternativt kan en bruger skrive spørgsmål til en leverandør på siden **Tilbudsanmodning** ved at klikke **Administrer svar**, **Rediger svar på tilbudsanmodning** og derefter klikke på **Spørgsmål og svar**.

2. Skriv teksten til spørgsmålet i feltet **Spørgsmål**.
3. Klik på **Send**. Gentag trin 1-3 for at tilføje et spørgsmål.
4. Når du er færdig, skal du klikke på **Gem** for at gemme dine spørgsmål.

## <a name="replying-to-a-single-vendor"></a>Besvare en enkelt leverandør
Spørgsmål og svar er kun synlige for leverandøren og brugerne.
1. På siden **Tilbudsanmodning** skal du klikke på **Spørgsmål og svar** for at åbne siden **Spørgsmål og svar**.
2. Klik på **Rediger**.
1. Indtast tekst i **Svar**-feltet for at svare på leverandørspørgsmålet.
2. Markér feltet **Direkte svar**.
3. Klik på **Gem** for at gemme svarene.
4. Klik på **Send svar** for at sende svarene til leverandøren.

## <a name="replying-to-all-vendors"></a>Besvare alle leverandører
Hvis du modtager samme spørgsmål fra flere leverandører, kan du gruppere spørgsmålene og reagere med det samme svar. Alle leverandører modtager en besked, når de ofte stillede spørgsmål og svar udgives. Leverandørerne og alle, der har adgang til tilbudsanmodningen, kan få vist oversigten over spørgsmål og svar.

1. På siden **Tilbudsanmodning** skal du klikke på **Spørgsmål og svar** for at åbne siden **Spørgsmål og svar**.
2. Klik på **Rediger**.
3. Vælg en kode for det almindelige spørgsmål, f.eks. bogstavet 'a'.
4. For hver linje, der stiller et lignende spørgsmål, skal du angive koden i feltet **Gruppekode**. For hver linje, der spørger til varens farve, skal du f.eks. angive 'a'.
5. Vælg en af linjerne med kodeværdien, og angiv det spørgsmål og svar, som de skal læse i oversigten, og som skal være tilgængeligt, når spørgsmålene og svarene publiceres (**Gruppespørgsmål, Gruppesvar** som felter).
6. Valgfrit: Du kan markere afkrydsningsfeltet **Direkte svar** for kun at sende svarene til de valgte leverandører.
7. Klik på **Gem** for at gemme svarene.
8. Valgfrit: Du kan ændre spørgsmålene og svarene til de tidligere udgivne værdier, hvis du vil fortryde dine ændringer.
9. Klik på **Send svar** for at sende svarene til leverandørerne.

## <a name="changing-rfq-to-allow-or-disallow-questions"></a>Ændre tilbudsanmodning for at tillade eller forbyde spørgsmål
Du kan foretage ændringer for at tillade eller ikke tillade spørgsmål til tilbudsanmodninger, indtil tilbudsanmodningen er belønnet. Du kan også udvide eller forkorte den tidsramme, som leverandørerne kan indsende spørgsmål i.
I forbindelse med publicerede tilbudsanmodninger skal du redigere en tilbudsanmodning for at tillade eller ikke tillade leverandørspørgsmål eller justere tidsrammen for spørgsmål. 
