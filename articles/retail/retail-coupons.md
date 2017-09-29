---
title: Oprette kuponer for detailsalg
description: Dette emne indeholder en oversigt over detailkuponer og en beskrivelse af, hvordan de konfigureres.
author: scott-tucker
manager: AnnBe
ms.date: 05/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: cebd1b6f041e18c2e016142aba7447bf813f570b
ms.openlocfilehash: fb013d3695870cb3b69ac41ff488f0865a648be4
ms.contentlocale: da-dk
ms.lasthandoff: 06/19/2017


---

# <a name="create-coupons-for-retail-sales"></a>Oprette kuponer for detailsalg

[!include[banner](includes/banner.md)]


## <a name="overview-of-coupons"></a>Oversigt over kuponer

Kuponer er koder og stregkoder, der bruges til at føje detailrabatter til posteringer. Hver kupon kan have flere koder, og hver kode kan have sine egne ikrafttrædelsesdatoer. 

Hver kupon er knyttet til én detailrabat. De prisgrupper, der er tilknyttet rabatten, definerer de kunder, der kan bruge en kupon, eller de kanaler, hvor en kupon er gyldig. 

I praksis er kuponer ekstra validering ud over detailrabatter. Kuponen indeholder de kuponkoder og stregkoder, der skal bruges, sammen med datointervaller til koderne. Kuponen indeholder desuden valgfrie brugerbegrænsninger og Debitor påkrævet-egenskaber. Rabatten angiver det sæt af produkter, som kuponen gælder for. Prisgrupperne for rabatten angiver det sæt af kunder, kanaler eller kataloger, kuponen gælder for.

Hvis du vil oprette en kupon, skal du oprette rabatten og kuponen særskilt. Derefter kan du tilknytte dem ved at vælge rabatten på kuponsiden i Microsoft Dynamics 365 for Retail. 

> [!NOTE]
> Når en kupon er tilknyttet en rabat, bliver flere af felterne på rabatsiden i Microsoft Dynamics 365 for Retail skrivebeskyttet, fordi de styres af indstillingerne for kuponen. Disse felter omfatter felterne for status og standarddatointervaller.

### <a name="limited-use-coupons"></a>Kuponer med begrænset anvendelse

Kuponer kan konfigureres som kuponer med begrænset anvendelse. Anvendelsesgrænsen kan defineres pr. kunde eller kanal eller som en global begrænsning. Denne begrænsning gennemtvinges, når koden eller stregkode angives eller indscannes i POS eller under indtastning af salgsordrer. En kupon registreres som anvendt, når en ordre, der har en kupon tilknyttet, er fuldført.

Grænsen gennemtvinges pr. kuponkode på en kupon. F.eks. kan en engangskupon, der har to kuponkoder, bruges to gange: én gang for hver kuponkode. Hver kode på en kupon kan indstilles uafhængigt til aktiv.

## <a name="managing-coupons"></a>Administration af kuponer

Du skal oprette rabatten og kuponen særskilt. Derefter tilknytter du dem ved at vælge rabatten på kuponsiden. Når du har knyttet en kupon til en rabat, bliver flere af felterne for rabatten skrivebeskyttet, fordi de styres af indstillingerne for kuponen. Disse felter omfatter felterne for status og standarddatointervaller.  

I praksis er kuponer nu ekstra validering ud over detailrabatter. Kuponen indeholder de kuponkoder og stregkoder sammen med datointervaller, som anvendelsen begrænser, og egenskaben Debitor påkrævet. Rabatten angiver det sæt af produkter, som kuponen gælder for. Prisgrupperne for rabatten angiver det sæt af kunder, kanaler eller kataloger, kuponen gælder for.

## <a name="system-setup-for-coupons"></a>Systemopsætning for kuponer 

Når du vil konfigurere en kupon, skal du først angive kuponens stregkode og to kuponnummerserier. 

1.  På siden **Masketegn** skal du oprette et nyt masketegn for kuponkoden. Du kan vælge alle ikke-anvendte tegn.
2.  På siden **Opsætning af stregkodemaske** skal du oprette en ny stregkodemaske. Indstil feltet **Type** til **Kupon**.
3.  På siden **Stregkodeopsætning** skal du oprette en ny stregkode, der bruger den stregkodemaske, du lige har oprettet.
4.  På siden **Nummerserier** skal du oprette to nye nummerserier. Én serie er til kuponkode-id'et, og den anden serie er til kuponnummeret. Kuponkode-id'et er det entydige id for hver kuponkode for en kupon. Kuponnummeret er et entydigt id for en kupon. Hver kupon kan have flere koder og stregkoder, der udløser kuponen.

    > [!NOTE]
    > For begge nummerserier skal du indstille feltet **Interval** til **Firma**. I de fleste tilfælde bør du generere begge serienumre automatisk.

5.  På siden **Delte parametre for detail** under fanen **Stregkoder** skal du vælge den stregkode, du oprettede tidligere.
6.  På siden **Detailparametre** under fanen **Nummerserier** skal du vælge de nummerserier, du oprettede for Kuponnummer og Kuponkode-id.
7.  Du kan nu åbne siden **Kuponer** og oprette nye rabatkuponer.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Virkningen af delvise opdateringer på kuponer

Kuponfunktioner indeholder flere specifikke funktioner i Dynamics 365 for Retail. Microsoft Dynamics 365 for Retail Headquarters (HQ) og kanalen kan opdateres delvist på tværs af komponenter. Det er derfor vigtigt, at du forstår, hvordan delvise opdaterer påvirker kuponfunktioner som helhed.

- **HQ opdateres delvist, men Retail Server og POS opdateres ikke.** Under en opdatering af HQ opdateres kupon- og rabatsiderne, og detailprisprogrammet opdateres også. Hvis der kun en af disse to komponenter opdateres, vil nogle sider i Retail ikke svare til prisberegningsdataene. Derfor kan der forekomme uventede rabatberegninger eller fejl under rabatberegninger.
- **HQ opdateres, men Retail Server og POS opdateres ikke (N-1).** Da ikke alle detailbutikker kan opdateres på samme tid, anbefales det, at du opdaterer HQ, før du opdaterer detailbutikker. I eksemplet N-1 er nye funktioner, der er relateret til kuponer, ikke tilgængelige i butikker, der endnu ikke er blevet opdateret. For eksempel introducerer kuponfunktionen "udelad"-linjer. Hvis du bruger udelad-linjer på en rabat, bliver de ikke anvendt i en detailbutik, der kører en tidligere version.
- **HQ opdateres ikke, men Retail Server og POS opdateres (N+1).** Da det opdaterede prisprogram i Retail Server kan håndtere ældre rabatkoder under prisberegninger, bør opdateringen ikke have nogen indflydelse på funktioner i dette eksempel.
