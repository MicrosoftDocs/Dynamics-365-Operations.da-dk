---
title: Angive en tilføjelse til et anlægsaktiv
description: Denne procedure viser, hvordan du føjer en tilføjelse til et eksisterende anlægsaktiv.
author: moaamer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d23f60963466249b332b759ee72ebc8387aee4b
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713016"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a>Angive en tilføjelse til et anlægsaktiv

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du føjer en tilføjelse til et eksisterende anlægsaktiv. Formålet med tilføjelser til anlægsaktiv er at spore varetilføjelser, vedligeholdelse eller forbedringer for et aktiv og er kun til orientering. Eventuelle ændringer af anlægsaktivværdien eller levetiden skal foretages separat.   

Proceduren bruger rollen Revisor og demodata for den juridiske enhed USMF.

1. I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Anlægsaktiver > Anlægsaktiver**.
2. På listen skal du finde og vælge anlægsaktivet for tilføjelsen.
3. Klik op linket i den valgte række på listen.
4. Klik på **Anlægsaktiv** i handlingsruden.
5. Klik på **Tilføjelser til anlægsaktiv**.
6. Klik på **Ny**.
7. Skriv en værdi i feltet **Navn**.
8. I feltet **Anskaffelsesdato** skal du angive datoen for tilføjelsen af køb eller tjeneste.
9. Angiv omkostningen for vare, vedligeholdelse eller anden forbedring for aktivet i feltet **Enhedskostpris**.
10. Angiv et tal i feltet **Antal**. De samlede omkostninger har ingen indflydelse på værdien af anlægsaktivet og bruges udelukkende til sporing og orientering. Hvis omkostningerne skal kapitaliseres, skal en opskrivningsregulering bogføres separat.  
11. Klik på fanen **Generelt**.

    * Indstil **Øger levetiden** til **Ja**, hvis tilføjelsen øger aktivets levetid.  
    * Feltet er kun til orientering. Hvis du vil forøge levetiden, skal du ændre levetiden i værdimodellerne og/eller afskrivningsmodellerne for aktivet.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
