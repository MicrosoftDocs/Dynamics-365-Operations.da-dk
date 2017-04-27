---
title: Oversigt over positive betalinger
description: "Denne artikel indeholder oplysninger om positiv betaling, som bruges til at generere en elektronisk liste over checks, der kan indløses i en bank."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 1fd606817b06a05b9abaaedf20ea9872bd7edd5d
ms.openlocfilehash: cb4806a1f023c1e60311ff9d8facb4ef5717ad94
ms.lasthandoff: 03/31/2017


---

# <a name="positive-pay-overview"></a>Oversigt over positive betalinger

[!include[banner](../includes/banner.md)]


Denne artikel indeholder oplysninger om positiv betaling, som bruges til at generere en elektronisk liste over checks, der kan indløses i en bank. 

Positiv betaling bruges til at generere en elektronisk liste over checks, der kan indløses i en bank. Positive betalingsfiler kan hjælpe banker med at forebygge checkbedrageri. Du konfigurerer en positiv betaling til at generere en elektronisk liste over checks, hver gang checks udskrives. Når checken derefter skal indløses hos banken, sammenligner banken checken med den liste over checks, du tidligere har fremsendt. Hvis checken svarer til en check på listen, indløser banken den. Hvis checken ikke stemmer overens med en check på listen, beholder banken den til gennemsyn.

Positiv betaling er også kendt som SafePay. 

Filer til positiv betaling kan indeholde følsomme oplysninger om beløbsmodtagere og checkbeløb. Sørg derfor for, at du bruger passende de sikringsforanstaltninger fra det tidspunkt, hvor filerne genereres, indtil de modtages af banken. Filer til positive betalinger overføres i henhold til overførselsinstruktionerne for webbrowseren. 

Filer til positiv betaling oprettes ved hjælp af dataenheder. Før du genererer en fil til positiv betaling, skal du angive transformationsformaterne for den XML-filer, der oversætter dataene til et format, som banken kan anvende. 

For hver bankkonto, du vil generere oplysninger om positiv betaling for, skal du tildele formatet for positiv betaling. Når du har genereret betalinger, kan du oprette en fil til positiv betaling for en enkelt juridisk enhed og en enkelt bankkonto. Du kan også samtidig generere filer til positiv betaling for flere juridiske enheder og bankkonti. 

Når de checks, der er angivet i en fil til positiv betaling, er betalt, modtager du et bekræftelsesnummer fra din bank. Du kan derefter bekræfte filen til positiv betaling i Microsoft Dynamics 365 for Operations. 

Hvis du vil ændre en fil til positiv betaling, kan du tilbagekalde den. For hver check i filen til positiv betaling, nulstilles derefter det felt, der angiver, om checken er inkluderet i en fil til positiv betaling.

Yderligere oplysninger finder du i afsnittet [Konfigurer og generer filer til positive betalinger](set-up-generate-positive-pay-files.md).




