---
title: Installere layoutdesigneren til POS
description: Du kan bruge ét-klik-designeren til at designe forskellige Modern POS- (MPOS) og Cloud POS-layout, i enten liggende eller stående tilstand, til butikker, kasseapparater, kasserer og ledere.
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f9882ae895de926e0da3579ab65a988f2b97f7be
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022067"
---
# <a name="install-the-pos-layout-designer"></a>Installere layoutdesigneren til POS

[!include [banner](includes/banner.md)]

Du kan bruge ét-klik-designeren til at designe forskellige Modern POS- (MPOS) og Cloud POS-layout, i enten liggende eller stående tilstand, til butikker, kasseapparater, kasserer og ledere.

Det grafiske design af brugergrænsefladen for MPOS og Cloud POS styres af pengeskuffelayoutet. Et layout styrer placeringen af forskellige objekter. Af eksempler kan nævnes det samlede layout, layout for varegitter, kundelayout og betalingslayout samt layoutet for forskellige menuknapper. Layout omfatter også det overordnede udseende af den salgsgrænseflade, som arbejderne kan se.

## <a name="install-the-one-click-designer"></a>Installere enkelt klik-designer

1. I Commerce skal du bruge menuen øverst til venstre til at navigere til **Retail og Commerce** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS** &gt; **Skærmlayout**.
2. Vælg et layout, der har programtypen **Modern POS til Windows** eller **Cloud POS**, og klik derefter på **Layoutdesigner**.
3. Klik på **Åbn** på meddelelseslinjen nederst i vinduet Internet Explorer for at starte ét klik-designeren. (Meddelelseslinjen vises muligvis et andet sted i andre browsere).
4. I **Programkørsel - Sikkerhedsadvarsel**-meddelelsen, der vises, skal du klikke på **Kør** for at installere Retail designerværten. Statusindikatoren viser forløbet af installationen.
5. Når installationen er fuldført, skal du på siden **Log på** angive dit Commerce-brugernavn og din adgangskode og derefter klikke på **Log på** for at starte designeren.
6. Når dine legitimationsoplysninger er valideret, og designeren starter, kan du designe dit eget layout eller redigere det eksisterende layout.

    [![Layout i ét klik-designeren](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Fejlfinding i forbindelse med installationen af layoutdesigneren

- Når du klikker på **Designer**, bliver du ikke bedt om at downloade (eller køre) installationsprogrammet, eller dine aktuelle sikkerhedsindstillinger tillader ikke download af filen. 

    **Løsninger:**

    - Sørg for, at blokering af pop-up-vinduer er deaktiveret for dette websted i Internet Explorer. Klik på **Indstillinger** &gt; **Indstillinger** &gt; **Beskyttelse af personlige oplysninger** &gt; **Blokering af pop op-vinduer**, og skift indstillingen, hvis der kræves en ændring.
    - I Internet Explorer skal du føje Commerce-URL-adressen til listen over websteder, der er tillid til. Klik på **Indstillinger** &gt; **Indstillinger** &gt; **Sikkerhed** &gt; **Websteder, du har tillid til** &gt; **Websteder** &gt; **Tilføj**.

- Programmet starter ikke, og du bliver bedt om at kontakte leverandøren.

    **Løsning:** I Internet Explorer skal du føje Commerce-URL-adressen til listen over websteder, der er tillid til. Klik på **Indstillinger** &gt; **Indstillinger** &gt; **Sikkerhed** &gt; **Websteder, du har tillid til** &gt; **Websteder** &gt; **Tilføj**.

**Kendt problem:** Designeren virker ikke korrekt i Google Chrome- og Mozilla Firefox-browsere. Vi arbejder på at løse dette problem.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere, installere og aktivere Retail Modern POS (MPOS)](retail-modern-pos-device-activation.md)
