---
title: Oversigt over optimeringsrådgiver
description: Dette emne beskriver, hvordan du kan bruge Optimeringsrådgiver til at sikre optimal konfiguration af Finance and Operations.
author: roxanadiaconu
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: sericks
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 1e53dbae2d139af554b1918102937f8c3579f64a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682531"
---
# <a name="optimization-advisor-overview"></a>Oversigt over optimeringsrådgiver

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du kan bruge Optimeringsrådgiver til at sikre optimal konfiguration af Finance and Operations.

## <a name="overview"></a>Overblik

Forkert konfiguration og opsætning af et modul kan påvirke tilgængeligheden af programfunktioner, systemets ydeevne og den glidende afvikling af forretningsprocesser. Kvaliteten af virksomhedens data (f.eks. korrekte, komplette og rene data) påvirker også systemets ydeevne, og en organisations muligheder for at tage beslutninger, produktivitet og så videre.

Arbejdsområdet **Optimeringsrådgiver** er et værktøj, der giver superbrugere, virksomhedsanalytikere, funktionelle konsulenter og it-supportfunktioner mulighed for at identificere problemer i modulkonfiguration og forretningsdata. Optimeringsrådgiver foreslår bedste fremgangsmåder til konfiguration af modulet og identificerer forretningsdata, der er forældede eller fejlagtige.

Optimeringsrådgiver kører regelmæssigt et sæt regler for bedste fremgangsmåde. Der findes et standardsæt af regler, men brugerne kan også oprette regler, der er specifikke for deres tilpasninger, løsninger fra uafhængige softwareleverandører (ISV'er) og forretningsdata. Du kan finde flere oplysninger om, hvordan du opretter regler, under [Opret nye regler for Optimeringsrådgiver](./create-rules-optimization-advisor.md).

Når der registreres en overtrædelse af en regel, genereres der en optimeringsmulighed, og den vises i arbejdsområdet **Optimeringsrådgiver**. En bruger kan foretage korrigerende handlinger direkte fra arbejdsområdet **Optimeringsrådgiver**.

Mulighederne kan være firmaspecifikke eller gælde på tværs af firmaer, afhængigt af typen af konfiguration og de data, der skal valideres. Muligheder på tværs af firmaer kan ses fra alle firmaer. Hvis du vil have vist muligheder for et specifikt firma, skal du først vælge firmaet.

Der gælder standardsikkerhedspolitikker for optimeringsmuligheder. Optimeringsmuligheder, der er relateret til konfigurationen af modulet **Lokationsstyring** er f.eks. kun synlige for brugere, der har adgang til Lokationsstyring og kan ændre dets opsætning.

Når du udfører en handling i forbindelse med visse optimeringsmuligheder, beregner systemet virkningen af muligheden med hensyn til reduktionen i kørselstiden for forretningsprocesser. Desværre er denne funktion ikke tilgængelig for alle optimeringsmuligheder.

Hvis du vil vide mere om optimeringsrådgiver, kan du se den korte video om [Optimeringsrådgiver i Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ).

## <a name="optimization-rules"></a>Optimeringsregler

Hvis du vil have vist den komplette liste over Optimeringsrådgiver-regler og se, hvor ofte reglerne evalueres, skal du gå til **Systemadministration** &gt; **Periodiske opgaver** &gt; **Vedligehold valideringsregel i diagnosticering**. Kun de regler, der har status som **Aktiv** evalueres. Evalueringsfrekvensen kan angives til **Daglig**, **Ugentlig**, **Månedlig** eller **Ikke-planlagt**.

For at udløse evalueringen af ikke-planlagte regler eller for at evaluere periodiske regler igen uden for deres foruddefinerede interval, skal du gå til **Systemadministration** &gt; **Periodiske opgaver** &gt; **Planlæg valideringsregel i diagnosticering**. Vælg en frekvens for evaluering i dialogboksen **Validering af diagnosticeringsregel**. Alle regler, der har den angivne frekvens, evalueres igen.

Det aktuelle sæt af optimeringsregler kan opdeles i følgende kategorier.

### <a name="module-configuration-and-setup"></a>Modulkonfiguration og opsætning

Opsætning af Lokationsstyring er en kompliceret proces. For at gøre processen nemmere er der indført nogle regler, der hjælper med til at validere rigtigheden af opsætningen. F.eks. validerer én regel opsætningen af direktiver for lokationsstyring for faste produktvariantlokationer for salgsordrer og flytteordrer.

Nogle regler kontrollerer også, om de funktioner, der er blevet aktiveret, faktisk bruges. F.eks. afgør en regel, om du bruger modulet **Varedisponering**. Hvis reglen afgør, at du ikke bruger modulet, genereres der en optimeringsmulighed for at foreslå, at du kan deaktivere planlægningsprocesserne.

### <a name="system-configuration"></a>Systemkonfiguration

Hvis bestemte funktioner, der styres af en konfigurationsnøgle, ikke bruges, genereres en optimeringsmulighed for at foreslå, at du deaktiverer konfigurationsnøglen. Eksempler på konfigurationsnøgler omfatter **fastvægt**, **budgetplanlægning**, **projekt** og **godkendt kreditorliste**.

### <a name="business-data-consistency-and-cleanup"></a>Konsistens og oprydning i forretningsdata

Hvis masterdata ikke er korrekte (f.eks., hvis du har omregninger af måleenhed for enheder, der ikke er defineret, eller hvis du har omregninger af måleenhed, der har en division med 0 \[nul\]), genereres en optimeringsmulighed for at foreslå, at kan du rette data. 

Hvis du har for mange poster i batchjobhistorikken, forældede varer, lukkede disponible poster til lagerstedsaktiverede varer osv, eller hvis disse poster og varer er forældede, genereres der optimeringsmuligheder, der foreslår, at renser dataene. Ved at holde dataene rene kan du hjælpe med til at forbedre systemets samlede ydeevne.

### <a name="best-practices"></a>Bedste fremgangsmåder

Hvis du ikke kører nogle af forretningsprocesserne i overensstemmelse med de bedste fremgangsmåder (hvis du f.eks. kører forudgående lagerlukning, før lageret er lukket, eller hvis du bruger planlagt batch til batchoverførsel af reskontrokladde), informerer optimeringsmulighederne dig om den bedste fremgangsmåde og beder dig om at følge den.

## <a name="optimization-opportunities"></a>Optimeringsmuligheder

For at få vist de optimeringsmuligheder, der genereres under evalueringen af optimeringsreglerne, skal du åbne arbejdsområdet **Optimeringsrådgiver**.

I dette arbejdsområde kan du få vist yderligere oplysninger om en mulighed ved at vælge **Flere oplysninger**. Hvis systemet skal udføre en handling og rette opsætningen, rense dataene og så fremdeles, så du ikke behøver selv åbne de relevante sider, skal du markere **Udfør handling**.

Der er ingen arbejdsgang for optimeringsmuligheder. Når du har valgt **Udfør handling** eller brugt en navigationssti, der er angivet i dialogboksen **Flere oplysninger** forsvinder optimeringsmuligheden fra listen. Hvis korrigerende handling ikke helt løser et problem, genereres muligheden igen, næste gang reglen evalueres.

Hvis en mulighed ikke gælder for din rolle, kan du vælge **Skjul på min liste**. Selvom reglen bag denne mulighed udløses igen senere, kan du ikke se muligheden på din liste.

Hvis du vil deaktivere evalueringen af bestemte regler, skal du vælge den mulighed, der blev genereret af reglen og derefter vælge **Deaktiver analyse**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette regler for optimeringsrådgiver](./create-rules-optimization-advisor.md)

[Optimeringsrådgiver i Dynamics 365 for Finance and Operations (video)](https://www.youtube.com/watch?v=MRsAzgFCUSQ)
