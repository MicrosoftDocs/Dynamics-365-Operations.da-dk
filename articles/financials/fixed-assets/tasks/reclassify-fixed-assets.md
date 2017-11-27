--- 
title: "Genklassificer anlægsaktiver"
description: "Hvis du vil genklassificere et anlægsaktiv, skal du overføre det til en ny anlægsaktivgruppe eller tildele det et nyt anlægsaktivnummer i samme gruppe."
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cafd499e849570cae7b7f58bf2d487a7ac0093e6
ms.openlocfilehash: 6bce294329c7ec6dc436c3d3baf6597e0283c9bd
ms.contentlocale: da-dk
ms.lasthandoff: 10/30/2017

---
# <a name="reclassify-fixed-assets"></a>Genklassificer anlægsaktiver

[!include[task guide banner](../../includes/task-guide-banner.md)]

Hvis du vil genklassificere et anlægsaktiv, skal du overføre det til en ny anlægsaktivgruppe eller tildele det et nyt anlægsaktivnummer i samme gruppe. 

Når et anlægsaktiv genklassificeres:

• Alle værdimodeller for det eksisterende anlægsaktiv oprettes for det nye anlægsaktiv. Oplysninger, der var oprettet for det oprindelige anlægsaktiv, kopieres til det nye anlægsaktiv. Status for det oprindelige anlægsaktivs værdimodeller er Lukket. 

• Det nye anlægsaktivs nye værdimodeller indeholder datoen for genklassificeringen i feltet Anskaffelsesdato. Datoen i feltet Afskrivning kopieres fra de oprindelige aktivoplysninger. Hvis afskrivningen allerede er startet, vises datoen for genklassificeringen i feltet Dato, hvor afskrivning sidst blev udført. 

• De eksisterende anlægsaktivposteringer for det oprindelige anlægsaktiv annulleres og oprettes for det nye anlægsaktiv igen.

1. Gå til Anlægsaktiver > Periodiske opgaver > Genklassificering.
2. I feltet Anlægsaktivgruppe skal du vælge den gruppe, som skal genklassificeres.
3. Vælg det anlægsaktiv, der skal genklassificeres, i feltet Nummer på anlægsaktiv.
4. Vælg en gruppe, som det nye anlægsaktiv skal overføre til, i feltet Ny anlægsaktivgruppe.
    * Hvis den nye anlægsaktivgruppe er knyttet til en nummerserie, opdateres feltet Nyt nummer på anlægsaktivet med nummeret fra nummerserien for den nye anlægsaktivgruppe. Ellers opdateres feltet Nyt nummer på anlægsaktivet med nummeret fra nummerserien, der er konfigureret på siden Parametre for anlægsaktiver. Hvis der ikke er konfigureret en nummerserie på siden Parametre for anlægsaktiver, skal du angive et tal i feltet Nyt nummer på anlægsaktivet.  
5. Indtast en dato i feltet Dato for genklassificering.
6. Indtast eller vælg en værdi i feltet Bilagsserie.
7. Klik på OK.


