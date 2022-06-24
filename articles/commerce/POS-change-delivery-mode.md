---
title: Ændring af leveringsmetode i POS
description: Denne artikel indeholder en beskrivelse af, hvordan du kan konfigurere og bruge ændringsmåden for leveringshandlinger i POS.
author: hhainesms
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 583f568164d0de70e22998bf5ded5f4616b00bd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855815"
---
# <a name="change-mode-of-delivery-in-pos"></a>Ændring af leveringsmetode i POS

[!include [banner](includes/banner.md)]

Denne artikel indeholder en beskrivelse af, hvordan du kan konfigurere og bruge funktionen "Skift leveringsmåde" i dit POS-miljø. 

I Dynamics 365 Commerce version 10.0.10 og nyere kan handlingen **Ændring af leveringsmetode** (647) føjes til dine POS-skærmlayout.

Funktionen Ændring af leveringsmetode giver dig mulighed for at ændre leveringsmåden for en eller flere konfigurerede forsendelsessalgslinjer på POS-transaktionen. I tidligere versioner af Commerce skulle du gå gennem de fulde konfigurationsstrømme **Send alle** eller **Send valgte**, hvis du vil ændre leveringsmåden på en eksisterende linje, der er konfigureret til forsendelse. Denne proces var tidskrævende og kan resultere i utilsigtede ændringer af leveringsoprindelsen eller leveringsdatoerne for linjen. Den nye funktionalitet er en alternativ metode til effektiv opdatering af leveringsmåden på disse salgslinjer.

Du kan finde flere oplysninger om, hvordan du føjer en handling til en knap på din POS-knapmatrix, i [Skærmlayout for POS](pos-screen-layouts.md).

Når denne funktion er konfigureret i POS, og du vælger **Skift leveringsmåde**, vises en listeside, hvor du kan vælge de linjer i transaktionen, som du vil ændre leveringsmåden for. Du kan vælge nogle eller alle linjer eller afslutte uden at foretage nogen ændringer. De salgslinjer, der tidligere er konfigureret til forsendelse, er de eneste linjer på listen, som du kan ændre. Hvis du vil ændre en linje, der er angivet til afhentning eller til aflevering, skal du bruge handlingerne **Send alle** eller **Send valgte**. Hvis du derimod vil ændre en linje, der er angivet som en forsendelse til en afhentning eller afsendelse, skal du bruge handlingerne **Afhent alle**, **Afhent valgte**, **Udfør alle** eller **Udfør valgte**.

Når du har valgt de linjer, du vil ændre, skal klikke på **Skift leveringsmåde** for at vælge indstillinger for leveringsmåde. Hvis du har valgt flere linjer, der skal ændres, vil POS kun vise leveringsmåder, der er konfigureret som tilladte for alle de valgte produkter. Leveringsmåder kan konfigureres til at understøtte specifikke produkter og leveringsadresser. Hvis der er en leveringsmåde, der er acceptabel for ét produkt og én adressekombination, men ikke er acceptabel for en anden valgt produkt- og adressekombination, er leveringsmåden ikke tilgængelig. Du skal muligvis vælge én linje ad gangen og ændre leveringsmåden for hver linje separat, hvis du vil vælge en leveringsmåde for ét produkt, der ikke understøttes af et andet produkt.  

Når du har valgt den nye leveringsmåde, vises siden Transaktion. Hvis du vil have vist dine valg af nye leveringsmåder, skal du vælge fanen **Levering** på transaktionslisten.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette callcenter-ordrer](tasks/create-call-center-orders.md)

[Tilpasse transaktionsmails efter leveringsmåde](customize-email-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]