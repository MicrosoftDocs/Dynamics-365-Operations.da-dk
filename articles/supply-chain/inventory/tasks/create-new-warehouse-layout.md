---
title: Oprette en ny lageropbygning
description: Dette emne beskriver, hvordan du konfigurerer oplysninger om lokationer på et lagersted.
author: perlynne
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a329df85c339c90e4bdc620c8a63837ebc19a7c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833971"
---
# <a name="create-a-new-warehouse-layout"></a>Oprette en ny lageropbygning

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du konfigurerer oplysninger om lokationer på et lagersted. Dette gælder for kun for lagersteder, der er oprettet ved hjælp af "grundlæggende lagerfunktioner" i modulet Lagerstyring, ikke for lagersteder, der er oprettet i modulet Lagerstedsstyring. Du kan bruge denne procedure på demofirmaet USMF eller dine egne data.


## <a name="set-the-default-location-capacity"></a>Angiv lokalitetens standardkapacitet
1. Gå i navigationsruden til **Moduler > Lagerstyring > Opsætning > Parametre til lager- og lokationsstyring**.
2. Vælg fanen **Lokationer**.
3. Angiv et tal i feltet **Standardbredde**.
4. Angiv et tal i feltet **Standarddybde**.
5. Angiv et tal i feltet **Standardhøjde**.
6. Vælg **Gem**.
7. Luk siden.

## <a name="define-the-location-name-format"></a>Definer formatet for navnet på lokaliteten
1. I navigationsruden skal du gå til **Moduler > Lagerstyring > Opsætning > Lageropdeling > Lagersteder**.
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Lagersted**.
4. Skriv en værdi i feltet **Navn**.
5. Vælg den ønskede post i opslaget til feltet **Sted**.
6. Slå udvidelsen af sektionen **Lokationsnavne** til/fra. Indstillingerne i denne sektion definerer standardformatet for navne på lokaliteter. I vores eksempel medtager vi gangnummer, reolnummer og hyldenummer.  
7. Angiv indstillingen **Medtag gang** til **Ja**.
8. Angiv indstillingen **Medtag reol** til **Ja**. 
9. Angiv en værdi for reolen i feltet **Format**.
10. Angiv indstillingen **Medtag hylde** til **Ja**.
11. Angiv en værdi for hylden i feltet **Format**.

## <a name="define-warehouse-locations"></a>Definer lagerstedslokationer
1. Vælg **Lagersted** i handlingsruden.
2. Vælg **Guiden Lokation**.
3. Vælg **Næste**.
4. Fjern markeringen af indstillingen **Forsendelsesområder**.
5. Fjern markeringen af indstillingen **Bulkvarelokationer**.
6. Vælg **Næste**, indtil du kan vælge **Udfør**.
7. Luk siden.
8. Opdater siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]