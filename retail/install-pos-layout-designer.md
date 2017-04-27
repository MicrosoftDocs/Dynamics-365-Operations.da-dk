---
title: Installere layoutdesigneren til Retail POS
description: "Du kan bruge ét-klik-designer til at designe forskellige Retail Modern POS (MPOS) og Cloud POS-layout, i enten liggende eller stående tilstand, til butikker, kasseapparater, kasserer og ledere."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: b33cbf67c00b6baea4393e82d19300085781af29
ms.lasthandoff: 03/31/2017


---

# <a name="install-the-retail-pos-layout-designer"></a>Installere layoutdesigneren til Retail POS

Du kan bruge ét-klik-designer til at designe forskellige Retail Modern POS (MPOS) og Cloud POS-layout, i enten liggende eller stående tilstand, til butikker, kasseapparater, kasserer og ledere.

Det grafiske design af brugergrænsefladen for MPOS og Cloud POS styres af pengeskuffelayoutet. Et layout styrer placeringen af forskellige objekter. Af eksempler kan nævnes det samlede layout, layout for varegitter, kundelayout og betalingslayout samt layoutet for forskellige menuknapper. Layout omfatter også det overordnede udseende af den salgsgrænseflade, som arbejderne kan se.

## <a name="install-the-oneclick-designer"></a>Installere ét klik-designer
1.  Brug menuen øverst til venstre i Microsoft Dynamics 365 for Operations til at navigere til **Detail** **og handel** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS** &gt; **Skærmlayout**.
2.  Vælg et layout, der har programtypen **Modern POS til Windows** eller **Cloud POS**, og klik derefter på **Layoutdesigner**.
3.  Klik på **Åbn** på meddelelseslinjen nederst i vinduet Internet Explorer for at starte ét klik-designeren. (Meddelelseslinjen vises muligvis et andet sted i andre browsere).
4.  I **Programkørsel - Sikkerhedsadvarsel**-meddelelsen, der vises, skal du klikke på **Kør **for at installere Retail designerværten. Statusindikatoren viser forløbet af installationen.
5.  Når installationen er fuldført, skal du angive dit brugernavn og din adgangskode til Microsoft Dynamics 365 for Operations på siden **Log på** og derefter klikke på **Log på** for at starte designeren.
6.  Når dine legitimationsoplysninger er valideret, og designeren starter, kan du designe dit eget layout eller redigere det eksisterende layout. [![Layout i ét klik-designeren](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Fejlfinding i forbindelse med installationen af layoutdesigneren
-   Når du klikker på **Designer**, bliver du ikke bedt om at downloade (eller køre) installationsprogrammet, eller dine aktuelle sikkerhedsindstillinger tillader ikke download af filen. **Løsninger:**
    -   Sørg for, at blokering af pop-up-vinduer er deaktiveret for dette websted i Internet Explorer. Klik på **Indstillinger** &gt; **Indstillinger** &gt; **Beskyttelse af personlige oplysninger** &gt; **Blokering af pop op-vinduer**, og skift indstillingen, hvis der kræves en ændring.
    -   Tilføj Dynamics-365 for Operations-URL-adresse på listen over websteder, du har tillid til, i Internet Explorer. Klik på **Indstillinger** &gt; **Indstillinger** &gt; **Sikkerhed** &gt; **Websteder, du har tillid til** &gt; **Websteder** &gt; **Tilføj**.
-   Programmet starter ikke, og du bliver bedt om at kontakte leverandøren. **Løsning:** Tilføj Dynamics-365 for Operations-URL-adresse på listen over websteder, du har tillid til, i Internet Explorer. Klik på **Indstillinger** &gt; **Indstillinger** &gt; **Sikkerhed** &gt; **Websteder, du har tillid til** &gt; **Websteder** &gt; **Tilføj**.

**Kendt problem:** Designeren virker ikke korrekt i Google Chrome- og Mozilla Firefox-browsere. Vi arbejder på at løse dette problem.

<a name="see-also"></a>Se også
--------

[Konfigurere, downloade, installere og aktivere Retail Modern POS](retail-modern-pos-device-activation.md)


