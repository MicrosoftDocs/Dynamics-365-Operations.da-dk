---
title: Lastskabeloner
description: Dette emne beskriver, hvordan du kan konfigurere lastskabeloner, og hvordan du knytter en lastskabelon til en ny last.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 80004b5d22e1cf81c1ffa9f74c2c479e1561df72
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247208"
---
# <a name="load-templates"></a>Lastskabeloner

Når du opretter en ny last, kan du tildele en lastskabelon. Lastskabelonen indeholder oplysninger om udstyr og om måleenheder, f.eks. højde, bredde, dybde og volumen for lasten.

Dette emne beskriver, hvordan du kan konfigurere lastskabeloner, og hvordan du knytter en lastskabelon til en ny last.

## <a name="set-up-a-load-template"></a>Konfigurere en lastskabelon

1. Gå til **Transportstyring \> Konfiguration \> Lastopbygning \> Lastskabelon**.
1. Vælg **Ny** i handlingsruden for at tilføje en ny skabelon eller **Rediger** for at redigere en eksisterende skabelon.
1. Angiv følgende felter i rækken for den nye eller den eksisterende skabelon:

    - **Id for lastskabelon** – Angiv et entydigt id for lastskabelonen.
    - **Udstyr** – Vælg det udstyr, der skal bruges til levering af lasten.
    - **Lasthøjde**, **Lastbredde** og **Lastdybde** – Angiv dimensionerne af lasten.
    - **Maks. tilladt lastvolumen** og **Maks. tilladt lastvægt** – Angiv den maksimale tilladte volumen og vægt for lasten.
    - **Maksimalt tilladte bruttovægt** – Angiv den maksimalt tilladte bruttovægt for lasten. Lastens bruttovægt er inklusive både dens taravægt og dens lastvægt.
    - **Maksimalt antal tilladte fragtdele** – Angiv det maksimale antal fragtdele, som lasten kan indeholde.
    - **Udfør stabling af last på gulv** – Markér dette afkrydsningsfelt for at bruge gulvlast. I et scenarie med gulvlastning stables kasser fra gulv til loft og væg til væg inden i containeren for at maksimere den indvendige kapacitet.

1. Vælg **Gem** i handlingsruden.

## <a name="associate-a-load-template-with-a-new-load"></a>Knytte en lastskabelon til en ny last

1. Gå til **Transportstyring \> Planlægning \> Lastplanlægningspanel**.
1. I den øverste del af siden skal du vælge en af følgende faner afhængigt af, hvilken type kildedokument du opretter en last for: **Forsendelser**, **Salgslinjer**, **Overflytningslinjer** eller **Indkøbsordrelinjer**. 
1. Vælg det specifikke dokument, som du vil planlægge lasten for.
1. I handlingsruden skal du under fanen **Udbud og efterspørgsel** i gruppen **Tilføj** vælge **Til ny last**.
1. I dialogboksen **Lastskabelon** skal du i feltet **Lastskabelons-id** vælge den skabelon, der skal anvendes.
1. Vælg **OK** for at anvende skabelonen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]