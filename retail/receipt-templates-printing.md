---
title: Kvitteringsskabeloner og udskrivning
description: "I denne artikel beskrives det, hvordan du kan oprette og ændre formularlayout for at styre, hvordan kvitteringer, fakturaer og andre dokumenter udskrives. Microsoft Dynamics 365 for Retail indeholder en formularlayoutdesigner, som du kan bruge til nemt at oprette og redigere forskellige typer formularlayout."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 6f1ec982522c6fe677b1921b69d5d04c4e783725
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017



---

# <a name="receipt-templates-and-printing"></a>Kvitteringsskabeloner og udskrivning

[!include[banner](includes/banner.md)]


I denne artikel beskrives det, hvordan du kan oprette og ændre formularlayout for at styre, hvordan kvitteringer, fakturaer og andre dokumenter udskrives. Microsoft Dynamics 365 for Retail indeholder en formularlayoutdesigner, som du kan bruge til nemt at oprette og redigere forskellige typer formularlayout.

**Vigtigt!** Du skal konfigurere formlayout og kvitteringsprofiler for at udskrive kvitteringer og andre dokumenter fra Retail Modern POS og Cloud POS. Du kan medtage flere formularlayout i en kvitteringsprofil. Du kan derefter tildele kvitteringsprofilen til en printer ved at redigere en hardwareprofil.

## <a name="set-up-a-receipt-format"></a>Konfigurere et kvitteringsformat
1.  Klik på **Detail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS** &gt; **Kvitteringsformater**.
2.  Klik på **Ny** på siden **Kvitteringsformat** for at oprette et nyt formularlayout eller vælge et eksisterende formularlayout.
3.  Angiv et id til formularlayoutet i feltet **Kvitteringsformat**, og vælg derefter den type kvittering, dette layout bruges til. Du kan også angive en beskrivelse af og et kort navn til kvitteringen i feltet **Titel**.
4.  Vælg en indstilling i oversigtspanelet **Generelt** for at definere udskriftsfunktionen:
    -   **Udskriv altid** – kvitteringen udskrives automatisk efter behov.
    -   **Udskriv ikke** – kvitteringen udskrives ikke.
    -   **Spørg bruger** – brugeren bliver bedt om at udskrive kvitteringen.
    -   **Som krævet** – denne indstilling bruges kun til gavekvitteringer. Når denne indstilling er valgt, kan brugeren udskrive en gavekvittering på siden **Skift**, hvis der kræves en gavekvittering.

## <a name="design-a-receipt-format"></a>Designe et kvitteringsformat
Brug formlayoutdesigneren til at oprette en grafisk illustration af layoutet for formdokumentet. Siden **Designer for kvitteringsformat** har tre sektioner: **Hoved**, **Linjer** og **Sidefod**. I visse typer af formlayout bruges elementer fra alle tre sektioner, mens der i andre typer kun bruges elementer fra en eller to sektioner. Hvis du vil have vist de elementer, der er tilgængelige for de enkelte sektioner, skal du klikke på den relevante knap i navigationsruden til venstre på siden.

1.  Klik på **Detail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS** &gt; **Kvitteringsformater**.
2.  Vælg et formularlayout på siden **Kvitteringsformat**, og klik derefter på **Designer**.
3.  Klik på **Kør** for starte installationen af Retail-designerværten.
4.  Klik på **Åbn** på meddelelseslinjen nederst i vinduet Internet Explorer for at starte ét klik-designeren. (Meddelelseslinjen vises muligvis i et andet sted i andre browsere.) Statusindikatoren viser forløbet af installationen.
5.  Når installationen er fuldført, skal du angive dit brugernavn og din adgangskode til Dynamics 365 for Retail og derefter klikke på **Log på** for at starte designeren.
6.  Når dine legitimationsoplysninger er valideret, og designeren starter, kan du begynde at designe kvitteringsformatet eller redigere et eksisterende format.
7.  Hvis du vil oprette elementerne til formularen, skal du vælge sektionen **Hoved**, **Linjer** eller **Sidefod** og derefter trække et element fra sektionen til arbejdsområdet. De fleste elementer indeholder variabler, som automatisk udfyldes med data fra databasen. Du kan bruge andre elementer, f.eks. delen **Tekst**, til at udskrive brugerdefineret tekst på kvitteringen. **Bemærk!** Du kan angive, hvor mange linjer hver sektion fylder, ved at justere antallet nederst til højre i den sektion. Hvis du vil gøre det lettere at redigere en sektion, kan du øge dens højde ved at trække i størrelsespanelet i bunden af sektionen. Sektionens højde på arbejdsområdet påvirker ikke antallet af linjer på den aktuelle kvittering.
8.  Når du har trukket et element til arbejdsområdet, skal du angive egenskaberne for delen i ruden **Objektoplysninger** nederst på siden. Angiv en eller flere af følgende indstillinger:
    -   **Juster** – Angiv justeringen for feltet til enten **Venstre** eller **Højre**.
    -   **Udfyldningstegn** – Angiv blanktegnet. Der bruges som standard et mellemrumstegn, men du kan angive et andet tegn.
    -   **Præfiks** – Angiv den værdi, der skal vises i begyndelsen af det valgte felt. Denne indstilling gælder kun for sektionen **Linjer** i layoutet.
    -   **Tegn** – Angiv det maksimale antal tegn, som feltet kan indeholde, hvis elementet indeholder en variabel. Hvis teksten i feltet er længere end det antal tegn, du angiver, forkortes teksten, så den passer til feltet.
    -   **Variabel** – Dette afkrydsningsfelt markeres automatisk, hvis elementet er en variabel, der ikke kan tilpasses.
    -   **Skrifttype** – Angiv enten skrifttypen til **Almindelig** eller **Fed**. Bogstaver, der er formateret med fed, bruger dobbelt så meget plads som almindelige bogstaver. Derfor afkortes visse tegn måske.
    -   **Skriftstørrelse** – Angiv enten skriftstørrelsen til **Almindelig** eller **Stor**. Store bogstaver er to gange højere end almindelige bogstaver. Derfor kan brug af store bogstaver føre til overlappende tekst på kvitteringen.
    -   **Slet** – Klik på denne knap, hvis du vil fjerne den valgte del fra formularlayoutet.

## <a name="assign-receipt-profiles"></a>Tildele kvitteringsprofiler
Kvitteringsprofiler tildeles direkte til printere via hardwareprofilen.

1.  Åbn hardwareprofilen ved at klikke på **Detail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler** &gt; **Hardwareprofil**.
2.  Vælg printeren, og tildel derefter den kvitteringsprofil, der skal bruges på kasseapparatet, i feltet **Kvitteringsprofil**.

**Bemærk!** Hvis der anvendes to printere, kan en printer bruges til at udskrive standardkvitteringer med 40 kolonner (termisk). Den anden printer bruges typisk til at udskrive helsides kvitteringstyper, som kræver yderligere oplysninger. Disse kvitteringstyper omfatter ordrekvitteringer og debitorfakturaer.




