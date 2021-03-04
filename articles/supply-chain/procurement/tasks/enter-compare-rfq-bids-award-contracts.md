---
title: Angive og sammenligne bud på tilbudsanmodninger og tildeler kontrakter
description: Dette emne viser, hvordan du indtaster svar på en tilbudsanmodning (RFQ), angiver score og sammenligner bud og derefter tildeler kontrakten en af leverandørerne.
author: mkirknel
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable, PurchTablePart, PurchRFQCompareLinePrices, PurchRFQCompareRFQ
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae7c43516fc90224439f6f7cfd5fd0a6058e8b39
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425057"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>Angive og sammenligne bud på tilbudsanmodninger og tildeler kontrakter

[!include [banner](../../includes/banner.md)]

Dette emne viser, hvordan du indtaster svar på en tilbudsanmodning (RFQ), angiver score og sammenligner bud og derefter tildeler kontrakten en af leverandørerne. Du kan bruge denne procedure i **USMF**-demodatafirmaet.

Før du starter proceduren, skal du have en tilbudsanmodning, der har to linjer og er blevet sendt til mindst to leverandører. Hvis du vil oprette denne tilbudsanmodning, skal du [Oprette en tilbudsanmodningsprocedure](create-request-quotation.md). Der skal også være oprettet scorekriterier, før du kan fuldføre denne procedure.

Du kan sende buddet som enten leverandør eller indkøber. Du kan finde flere oplysninger under [Konfigurere og vedligeholde kreditorsamarbejde](../set-up-maintain-vendor-collaboration.md).

## <a name="enter-a-reply-as-a-vendor"></a>Angive et svar som leverandør

1. Vælg **Kreditorbud** på dashboardet.
2. Find en tilbudsanmodning, der lige er blevet sendt, på listen **Invitationer til nyt bud**. Vælg tilbudsanmodningen for at gennemse, hvad der blev anmodet om.
3. Vælg **Tilbudsanmodning i vedhæftede filer** for at gennemse evt. vedhæftede filer, der er tilføjet.
4. Vælg **Bud** for at gøre felterne redigerbare. Bemærk, at **Status for bud** feltet er indstillet til **Leverandør opdaterer**.
5. Angiv værdierne fra budsvaret i hovedet og på linjerne.
6. Hvis der skal føjes vedhæftede filer til buddet, skal du vælge **Bud i vedhæftede filer**.
7. Vælg oversigtspanelet **Budvejledningselementer** for at få vist, om dokumenter er påkrævet.
8. Vælg oversigtspanelet **Ændringer** for at få vist, om tilbudsanmodningen er blevet ændret.
9. Vælg oversigtspanelet **Spørgeskema**. Eventuelle spørgeskemaer, der vises her, skal besvares.
10. Vælg oversigtspanelet **Linjedetaljer** for at få vist udvidede oplysninger om linjen.
11. Vælg kun **Nulstil fra tilbudsanmodning**, hvis du skal nulstille de værdier, der er angivet i de oprindelige tilbudsanmodningsværdier.
12. Du kan gemme tilbuddet når som helst og foretage yderligere behandling på et senere tidspunkt, hvis udløbsdatoen og -tidspunktet ikke er overskredet. I dette tilfælde kan du finde listen **Igangværende bud** i arbejdsområdet **Kreditorbud**.
13. Vælg **Send**, når buddet er klar til at blive afsendt. Vælg **Afvis**, hvis du ikke vil byde. Afsendte bud er tilgængelige på listen **Sendte bud** i arbejdsområdet **Kreditorbud**.  
14. Når tilbuddet er sendt, kan du altid tilbagekalde det før udløbsdatoen og -tidspunktet. Bemærk, at når et tilbud tilbagekaldes, behandles det ikke som sendt. Når buddet accepteres eller afvises af indkøbsafdelingen, vises det enten på listen **Tildelte tilbud** eller **Tabte bud** i arbejdsområdet **Kreditorbud**.  

## <a name="enter-a-reply-from-a-vendor-as-a-procurement-professional"></a>Angive et svar fra en leverandør som indkøber

1. Kontroller, at rettigheden til at redigere tilbud fra leverandører er konfigureret. Gå til **Indkøb og forsyning \> Opsætning \> Indkøbs- og forsyningsparametre**. Under fanen **Tilbudsanmodninger** kan du vælge **Ja** i indstillingen **Indkøber kan redigere kreditors bud**.
2. Gå til **Indkøb og forsyning \> Tilbudsanmodninger \> Alle tilbudsanmodninger**.
3. Vælg en tilbudsanmodning, der har statussen **Afsendt**, og vælg derefter linket i feltet **Tilbudsanmodningssag**.
4. Vælg **Administrer svar**. Den side, der åbnes, viser en tilbudsanmodning for hver leverandør, der er inviteret til at give et bud.
5. Vælg en tilbudsanmodning, der ikke er besvaret. (Feltet **Status for svar** skal være indstillet til **Ikke startet**).
6. Vælg **Rediger \> Rediger svar på tilbudsanmodning**. Følgende **Svar på tilbudsanmodning**-side vises. Som indkøber kan du nu angive svaret på vegne af leverandøren. Bemærk, at **Status for bud** feltet er indstillet til **Indkøber opdaterer**.  
7. Angiv buddataene. Vælg **Send**, når du er færdig.

## <a name="score-the-bids"></a>Give score til buddene

1. På siden **Alle tilbudsanmodninger** skal du vælge den tilbudsanmodningssag, som du vil angive scorer for svar på.
2. Vælg **Administrer svar**.
3. Vælg det svar, du vil tildele score.
4. Vælg **Hoved**, så du kan få vist scoren for buddet.
5. I oversigtspanelet **Budscore** skal du skrive et tal i feltet **Resultat** for et af scorekriterierne. Hvis du placerer markøren over et scorekriterie, viser et værktøjstip det interval, som scoren skal være inden for. Du kan angive et tal mellem 1 og 5 for et af scorekriterierne i denne demo.  
6. Gentag trin 5 for et andet scorekriterium.
7. Hvis tilbudsanmodningssagen har et spørgeskema, der blev sendt til kreditorerne, kan du angive kreditorsvar i oversigtspanelet **Spørgeskemaer**.
8. Luk siden.
9. Gentag trin 1 til 8 for alle andre bud.

## <a name="compare-the-replies"></a>Sammenligne svarene

1. I handlingsruden skal du under fanen **Generelt** vælge **Sammenlign svar**.
2. Angiv et tal i feltet **Rang**.  
    - Denne side viser buddene sammen med hoved- og linjeoplysninger og også den samlede score på hovedniveau. Du kan sammenligne linjerne ved at sortere i gitteret, så sammenlignelige linjer er placeret ved siden af hinanden. Der er også medtaget følgende oplysninger:
    - **Antal** – Det antal, leverandøren har tilbudt. Dette antal er muligvis ikke det samme som det antal, der er angivet i tilbudsanmodningen.
    - **Nettobeløb** – Den pris, som kreditoren har tilbudt for varerne på linjen minus eventuelle rabatter.
    - **Afvigelse** – Det antal dage, hvormed leveringsdatoen i tilbudshovedet eller -linjen adskiller sig fra den ønskede leveringsdato i tilbudsanmodningshovedet eller -linjen. Du kan angive en rangering for hvert bud.  
3. Vælg overskriftslinjen for det andet bud, du vil rangere.
4. Angiv et tal i feltet **Rang**.
5. Vælg **Gem**.

## <a name="reject-a-bid"></a>Afvise et bud

1. Vælg overskriftslinjen for det bud, du vil afvise. Du kan kun acceptere, afvise eller returnere ét bud eller linjerne i ét bud ad gangen.
2. Marker afkrydsningsfeltet **Marker**.  
    - Hvis du markerer afkrydsningsfeltet **Marker** i hovedet på et bud, markeres alle linjer også. Hvis du kun vil afvise eller acceptere nogle af linjerne i buddet, kan du markere netop disse linjer. Du kan desuden acceptere én kreditors tilbud på nogle linjer i en tilbudsanmodning, og derefter tildele andre linjer i en tilbudsanmodning til en anden kreditor. Du skal dog fuldføre ét tilbud ad gangen.  
    - Hvis der findes alternative linjer, kan du acceptere den oprindelige budlinje eller dens alternativ, men ikke begge.  
3. Vælg **Afvis**.
4. Vælg **Parametre**, og angiv eller vælg derefter i feltet **Årsag til afvisning** din grund til at afvise buddet. Årsagen gemmes i svaret.  
5. Vælg **OK**.
6. Vælg **OK**.

## <a name="accept-a-bid"></a>Acceptere et bud

1. Vælg det bud, du vil acceptere, og vælg derefter linket i feltet **Tilbudsanmodning**. Hvis du arbejder på siden **Sammenlign tilbudsanmodningssvar**, er det fremhævede bud, der er i fokus, være det bud, som systemet tager i betragtning under accepten. Du kan kun acceptere linjer fra ét tilbud ad gangen.  
2. Vælg **Svar** i handlingsruden.
3. Vælg **Accepter**. Hvis du kun har markeret bestemte linjer, omfatter accepthandlingen kun disse linjer. Hvis du vil acceptere alle linjerne i et bud, behøver du ikke at markere linjerne.  
4. Vælg **Parametre**, og angiv eller vælg derefter i feltet **Årsag til godkendelse** din grund til at acceptere buddet. Årsagen gemmes i buddet.  
5. Vælg **OK**.
6. Vælg **OK**. Når du vælger **OK**, genereres en indkøbsordre ud fra de linjer, der er inkluderet i accepten af tilbudsanmodningen. Hvis der er andre bud, der ikke er blevet behandlet (accepteret, afvist eller returneret), bliver du bedt om at afvise dem.  

## <a name="view-the-purchase-order-that-is-generated"></a>Få vist den indkøbsordre, der blev genereret

I handlingsruden skal du under fanen **Generelt** vælge **Indkøbsordre**. På den side, der åbnes, vises den indkøbsordre, der blev genereret, da du accepterede buddet.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]