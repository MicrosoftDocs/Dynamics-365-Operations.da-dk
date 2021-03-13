---
title: Overvåge konsignationslager ved hjælp af kreditorsamarbejde
description: Denne fremgangsmåde viser, hvordan du kan bruge leverandørsamarbejde til at få vist oplysninger om lagerbeholdning for det produkt, som du har i konsignation hos en kunde.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f2e782bed4cd9f2f13e2ee45afffaef277279131
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020123"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>Overvåge konsignationslager ved hjælp af kreditorsamarbejde

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du kan bruge leverandørsamarbejde til at få vist oplysninger om lagerbeholdning for det produkt, som du har i konsignation hos en kunde. Du kan også overvåge forbruget af lager, når kunden overtager ejerskabet af lageret. Du kan bruge denne procedure i USMF-demodatafirmaet. Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="view-consumed-inventory"></a>Vis forbrugt lager
1. Gå til Kreditorsamarbejde > Konsignationslager > Produkter, der er modtaget fra konsignationslager.
    * Listen viser de produktkvitteringslinjer, der blev genereret, da ejerskabet af konsignationslageret blev ændret fra leverandøren til kunden. Du skal muligvis rulle til højre for at se mængder og andre oplysninger. Du kan bruge oplysningerne på denne liste til at generere fakturaer for kunden. Du kan også eksportere dataene til Microsoft Excel.   
2. Klik på Vis indkøbsordre.
3. Vis eller skjul sektionen Linjedetaljer.
    * Linjen er markeret som Konsignation, og sektionsoverskriften viser, at købsordren har statussen Modtaget.  
4. Luk siden.

## <a name="view-on-hand-inventory"></a>Få vist disponibel lagerbeholdning
1. Gå til Kreditorsamarbejde > Konsignationslager > Disponibelt konsignationslager.
    * Siden Disponibelt konsignationslager viser det lager, du ejer på kundens lagersted. Du kan se yderligere dimensioner, såsom lokation og lagersted, ved at klikke på fanen Vis dimensioner.   

