---
title: Konfigurere og designe kvitteringsformater
description: I denne artikel beskrives det, hvordan du kan oprette og ændre formularlayout for at styre, hvordan kvitteringer, fakturaer og andre dokumenter udskrives. Dynamics 365 Commerce indeholder en formularlayoutdesigner, som du kan bruge til nemt at oprette og redigere forskellige typer formularlayout.
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFormLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a66590f18df04d2be0500b7fb1ab183cf64718e8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979747"
---
# <a name="set-up-and-design-receipt-formats"></a>Konfigurere og designe kvitteringsformater

[!include [banner](includes/banner.md)]

I denne artikel beskrives det, hvordan du kan oprette og ændre formularlayout for at styre, hvordan kvitteringer, fakturaer og andre dokumenter udskrives. Dynamics 365 Commerce indeholder en formularlayoutdesigner, som du kan bruge til nemt at oprette og redigere forskellige typer formularlayout.

> [!IMPORTANT]
> Du skal konfigurere formlayout og kvitteringsprofiler for at udskrive kvitteringer og andre dokumenter fra Retail Modern POS og Cloud POS. Du kan medtage flere formularlayout i en kvitteringsprofil. Du kan derefter tildele kvitteringsprofilen til en printer ved at redigere en hardwareprofil.

## <a name="set-up-a-receipt-format"></a>Konfigurere et kvitteringsformat

1. Klik på **Retail og Commerce** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS** &gt; **Kvitteringsformater**.
2. Klik på **Ny** på siden **Kvitteringsformat** for at oprette et nyt formularlayout eller vælge et eksisterende formularlayout.
3. Angiv et id til formularlayoutet i feltet **Kvitteringsformat**, og vælg derefter den type kvittering, dette layout bruges til. Du kan også angive en beskrivelse af og et kort navn til kvitteringen i feltet **Titel**.
4. Vælg en indstilling i oversigtspanelet **Generelt** for at definere udskriftsfunktionen:

    - **Udskriv altid** – kvitteringen udskrives automatisk efter behov.
    - **Udskriv ikke** – kvitteringen udskrives ikke.
    - **Spørg bruger** – brugeren bliver bedt om at udskrive kvitteringen.
    - **Som krævet** – denne indstilling bruges kun til gavekvitteringer. Når denne indstilling er valgt, kan brugeren udskrive en gavekvittering på siden **Skift**, hvis der kræves en gavekvittering.

## <a name="print-images"></a>Udskrive billeder

Kvitteringsdesigneren indeholder en **Logo**-variabel, der kan bruges til at angive billeder, der skal udskrives på kvitteringen. Billeder, der medtages i kvitteringer ved hjælp af variablen **Logo**, skal være monochrome bitmap (.bmp)-filtyper. Hvis der er angivet et .bmp-billede i kvitteringsdesigneren, men det udskrives ikke, når det sendes til printeren, kan filstørrelsen være for stor, eller pixeldimensionerne på billedet er ikke kompatible med printeren. Hvis det sker, skal du prøve at reducere billedopløsningen.   

## <a name="design-a-receipt-format"></a>Designe et kvitteringsformat

Brug formlayoutdesigneren til at oprette en grafisk illustration af layoutet for formdokumentet. Siden **Designer for kvitteringsformat** har tre sektioner: **Hoved**, **Linjer** og **Sidefod**. I visse typer af formlayout bruges elementer fra alle tre sektioner, mens der i andre typer kun bruges elementer fra en eller to sektioner. Hvis du vil have vist de elementer, der er tilgængelige for de enkelte sektioner, skal du klikke på den relevante knap i navigationsruden til venstre på siden.

1. Klik på **Retail og Commerce** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS** &gt; **Kvitteringsformater**.
2. Vælg et formularlayout på siden **Kvitteringsformat**, og klik derefter på **Designer**.
3. Klik på **Kør** for starte installationen af Commerce-designerværten.
4. Klik på **Åbn** på meddelelseslinjen nederst i vinduet Internet Explorer for at begynde at installere ét klik-designeren. (Meddelelseslinjen vises muligvis i et andet sted i andre browsere.) Statusindikatoren viser forløbet af installationen.
5. Når installationen er fuldført, skal du på angive dit brugernavn og din adgangskode til Commerce og derefter klikke på **Log på** for at starte designeren.
6. Når dine legitimationsoplysninger er valideret, og designeren starter, kan du begynde at designe kvitteringsformatet eller redigere et eksisterende format.
7. Hvis du vil oprette elementerne til formularen, skal du vælge sektionen **Hoved**, **Linjer** eller **Sidefod** og derefter trække et element fra sektionen til arbejdsområdet. De fleste elementer indeholder variabler, som automatisk udfyldes med data fra databasen. Du kan bruge andre elementer, f.eks. delen **Tekst**, til at udskrive brugerdefineret tekst på kvitteringen.

    > [!NOTE]
    > Du kan angive, hvor mange linjer hver sektion fylder, ved at justere antallet nederst til højre i den sektion. Hvis du vil gøre det lettere at redigere en sektion, kan du øge dens højde ved at trække i størrelsespanelet i bunden af sektionen. Sektionens højde på arbejdsområdet påvirker ikke antallet af linjer på den aktuelle kvittering.

8. Når du har trukket et element til arbejdsområdet, skal du angive egenskaberne for delen i ruden **Objektoplysninger** nederst på siden. Angiv en eller flere af følgende indstillinger:

    - **Juster** – Angiv justeringen for feltet til enten **Venstre** eller **Højre**.
    - **Udfyldningstegn** – Angiv blanktegnet. Der bruges som standard et mellemrumstegn, men du kan angive et andet tegn.
    - **Præfiks** – Angiv den værdi, der skal vises i begyndelsen af det valgte felt. Denne indstilling gælder kun for sektionen **Linjer** i layoutet.
    - **Tegn** – Angiv det maksimale antal tegn, som feltet kan indeholde, hvis elementet indeholder en variabel. Hvis teksten i feltet er længere end det antal tegn, du angiver, forkortes teksten, så den passer til feltet.
    - **Variabel** – Dette afkrydsningsfelt markeres automatisk, hvis elementet er en variabel, der ikke kan tilpasses.
    - **Skrifttype** – Angiv enten skrifttypen til **Almindelig** eller **Fed**. Bogstaver, der er formateret med fed, bruger dobbelt så meget plads som almindelige bogstaver. Derfor afkortes visse tegn måske.
    - **Skriftstørrelse** – Angiv enten skriftstørrelsen til **Almindelig** eller **Stor**. Store bogstaver er to gange højere end almindelige bogstaver. Derfor kan brug af store bogstaver føre til overlappende tekst på kvitteringen.
    - **Slet** – Klik på denne knap, hvis du vil fjerne den valgte del fra formularlayoutet.

## <a name="assign-receipt-profiles"></a>Tildele kvitteringsprofiler

Kvitteringsprofiler tildeles direkte til printere via hardwareprofilen.

1. Åbn hardwareprofilen ved at klikke på **Retail og Commerce** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler** &gt; **Hardwareprofil**.
2. Vælg printeren, og tildel derefter den kvitteringsprofil, der skal bruges på kasseapparatet, i feltet **Kvitteringsprofil**.

> [!NOTE]
> Hvis der anvendes to printere, kan en printer bruges til at udskrive standardkvitteringer med 40 kolonner (termisk). Den anden printer bruges typisk til at udskrive helsides kvitteringstyper, som kræver yderligere oplysninger. Disse kvitteringstyper omfatter ordrekvitteringer og debitorfakturaer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]