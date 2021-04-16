---
title: Opret en standardstatus for produktlivscyklus
description: Denne fremgangsmåde viser, hvordan du opretter en standardstatus for produktlivscyklus, samt hvordan standardstatussen tilknyttes frigivne produkter.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b62d47f52da7f9e18bce401578a5e2a629ac5eb8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818127"
---
# <a name="create-a-default-product-lifecycle-state"></a>Opret en standardstatus for produktlivscyklus

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du opretter en standardstatus for produktlivscyklus, samt hvordan standardstatussen tilknyttes frigivne produkter.


## <a name="create-a-default-lifecycle-state"></a>Opret en standardstatus for livscyklus
1. Gå til Administration af produktoplysninger > Konfiguration > Status for produktlivscyklus.
2. Klik på Ny.
3. Skriv en værdi i feltet Status.
4. Vælg Ja i feltet Standard ved frigivelse til juridisk enhed.
5. Skriv en værdi i feltet Beskrivelse.
6. Vælg Nej i feltet Er aktiv for planlægning.

> [!NOTE]
> Hvis et nyt frigivet produkt ikke skal medtages i varedisponering, skal du vælge Nej. Hvis det skal medtages i varedisponering, skal kontrolelementet beholde standardværdien Ja.  

## <a name="create-a-new-released-product"></a>Opret et nyt frigivet produkt
1. Luk siden.
2. Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.
3. Klik på Ny.
4. Skriv en værdi i feltet Produktnummer.
5. Angiv en værdi i feltet Produktnavn.
6. Angiv en værdi i feltet Søgenavn.
7. Indtast eller vælg en værdi i feltet Varemodelgruppe.
8. Indtast eller vælg en værdi i feltet Varegruppe.
9. Indtast eller vælg en værdi i feltet Lagringsdimensionsgruppe.
10. Indtast eller vælg en værdi i feltet Sporingsdimensionsgruppe.
11. Klik på OK.

> [!NOTE]
> Standardstatussen for produktlivscyklus er en global definition.  

## <a name="change-the-product-to-an-active-state"></a>Skift produktet til en aktiv tilstand
1. Indtast eller vælg en værdi i feltet Status for produktlivscyklus.

> [!NOTE]
> Forudsat at du har oprettet en aktiv tilstand, kan du nu vælge den aktive tilstand for at tillade, at produktet bruges i varedisponering og styklisteniveauberegning. Selvfølgelig giver dette kun mening, hvis alle produktoplysningerne, der skal bruges til ensartet planlægning er angivet.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]