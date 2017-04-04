---
title: Kvitteringsskabeloner og udskrivning
description: "I denne artikel beskrives det, hvordan du kan oprette og ændre formularlayout for at styre, hvordan kvitteringer, fakturaer og andre dokumenter udskrives. Microsoft Dynamics 365 for operationer – Retail indeholder en formularlayoutdesigner, du kan bruge til nemt at oprette og redigere forskellige typer formularlayout."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fabaacbc7187b38a1745c2139a9eb7760f2be987
ms.lasthandoff: 03/31/2017


---

# <a name="receipt-templates-and-printing"></a>Kvitteringsskabeloner og udskrivning

I denne artikel beskrives det, hvordan du kan oprette og ændre formularlayout for at styre, hvordan kvitteringer, fakturaer og andre dokumenter udskrives. Microsoft Dynamics 365 for operationer – Retail indeholder en formularlayoutdesigner, du kan bruge til nemt at oprette og redigere forskellige typer formularlayout.

**Vigtigt:** du skal konfigurere formularlayout og kvitteringsprofiler for at udskrive kvitteringer og andre dokumenter fra Retail moderne POS og sky POS. Du kan medtage flere formularlayout i en kvitteringsprofil. Du kan derefter tildele kvitteringsprofilen til en printer ved at redigere en hardwareprofil.

## <a name="set-up-a-receipt-format"></a>Konfigurere et kvitteringsformat
1.  Klik på **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**POS**&gt;**modtagelse formater**.
2.  Klik på **Ny** på siden **Kvitteringsformat** for at oprette et nyt formularlayout eller vælge et eksisterende formularlayout.
3.  Angiv et id til formularlayoutet i feltet **Kvitteringsformat**, og vælg derefter den type kvittering, dette layout bruges til. Du kan også angive en beskrivelse af og et kort navn til kvitteringen i feltet **Titel**.
4.  Vælg en indstilling i oversigtspanelet **Generelt** for at definere udskriftsfunktionen:
    -   **Udskriv altid** – kvitteringen udskrives automatisk efter behov.
    -   **Udskriv ikke** – kvitteringen udskrives ikke.
    -   **Spørg bruger** – brugeren bliver bedt om at udskrive kvitteringen.
    -   **Som krævet** – denne indstilling bruges kun til gavekvitteringer. Når denne indstilling er valgt, kan brugeren udskrive en gavekvittering på siden **Skift**, hvis der kræves en gavekvittering.

## <a name="design-a-receipt-format"></a>Designe et kvitteringsformat
Brug formlayoutdesigneren til at oprette en grafisk illustration af layoutet for formdokumentet. Siden **Designer for kvitteringsformat** har tre sektioner: **Hoved**, **Linjer** og **Sidefod**. I visse typer af formlayout bruges elementer fra alle tre sektioner, mens der i andre typer kun bruges elementer fra en eller to sektioner. Hvis du vil have vist de elementer, der er tilgængelige for de enkelte sektioner, skal du klikke på den relevante knap i navigationsruden til venstre på siden.

1.  Klik på **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**POS**&gt;**modtagelse formater**.
2.  Vælg et formularlayout på siden **Kvitteringsformat**, og klik derefter på **Designer**.
3.  Klik på **Kør** for starte installationen af Retail-designerværten.
4.  Klik på **Åbn** på meddelelseslinjen nederst i vinduet Internet Explorer for at starte ét klik-designeren. (Meddelelseslinjen vises muligvis i et andet sted i andre browsere.) Statusindikatoren viser forløbet af installationen.
5.  Når installationen er fuldført, indtast din Dynamics 365 for operationer brugernavn og adgangskode, og klik derefter på **logge på** at starte designeren.
6.  Når dine legitimationsoplysninger er valideret, og designeren starter, kan du begynde at designe kvitteringsformatet eller redigere et eksisterende format.
7.  Hvis du vil oprette elementerne til formularen, skal du vælge sektionen **Hoved**, **Linjer** eller **Sidefod** og derefter trække et element fra sektionen til arbejdsområdet. De fleste elementer indeholder variabler, som automatisk udfyldes med data fra databasen. Du kan bruge andre elementer, f.eks. delen **Tekst**, til at udskrive brugerdefineret tekst på kvitteringen. **Bemærk!** Du kan angive, hvor mange linjer hver sektion fylder, ved at justere antallet nederst til højre i den sektion. Hvis du vil gøre det lettere at redigere en sektion, kan du øge dens højde ved at trække i størrelsespanelet i bunden af sektionen. Sektionens højde på arbejdsområdet påvirker ikke antallet af linjer på den aktuelle kvittering.
8.  Når du har trukket et element til arbejdsområdet, skal du angive egenskaberne for delen i ruden **Objektoplysninger** nederst på siden. Angiv en eller flere af følgende indstillinger:
    -   **Juster** – Angiv justeringen for feltet til enten **Venstre** eller **Højre**.
    -   **Udfyldningstegn** – Angiv blanktegnet. Der bruges som standard et mellemrumstegn, men du kan angive et andet tegn.
    -   **Præfiks** – Angiv den værdi, der skal vises i begyndelsen af det valgte felt. Denne indstilling gælder kun for sektionen **Linjer** i layoutet.
    -   **Tegn** – Angiv det maksimale antal tegn, som feltet kan indeholde, hvis elementet indeholder en variabel. Hvis teksten i feltet er længere end det antal tegn, du angiver, forkortes teksten, så den passer til feltet.
    -   **Variabel** – Dette afkrydsningsfelt markeres automatisk, hvis elementet er en variabel, der ikke kan tilpasses.
    -   **Skrifttype** – Angiv enten skrifttypen til **Normal** eller **Fed**. Bogstaver, der er formateret med fed, bruger dobbelt så meget plads som normale bogstaver. Derfor afkortes visse tegn måske.
    -   **Slet** – Klik på denne knap, hvis du vil fjerne den valgte del fra formularlayoutet.

## <a name="assign-receipt-profiles"></a>Tildele kvitteringsprofiler
Kvitteringsprofiler tildeles direkte til printere via hardwareprofilen.

1.  Åbn hardwareprofilen ved at klikke på **detail- og commerce**&gt;**kanal setup**&gt;**POS installation**&gt;**profiler for POS**&gt;**hardwareprofil**.
2.  Vælg printeren, og tildel derefter den kvitteringsprofil, der skal bruges på kasseapparatet, i feltet **Kvitteringsprofil **.

**Bemærk!** Hvis der anvendes to printere, kan en printer bruges til at udskrive standardkvitteringer med 40 kolonner (termisk). Den anden printer bruges typisk til at udskrive helsides kvitteringstyper, som kræver yderligere oplysninger. Disse kvitteringstyper omfatter ordrekvitteringer og debitorfakturaer.


