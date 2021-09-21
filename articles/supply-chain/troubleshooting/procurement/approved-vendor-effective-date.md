---
title: Kan ikke skifte ikrafttrædelsesdato for en godkendt kreditor
description: Listen over godkendte kreditorer efter produktenhed tillader ikke, at ikrafttrædelsesdatoen ændres
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: cb6dbd134d63daa163261cabdbd7eceb978877ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475860"
---
# <a name="cant-change-the-effective-date-for-an-approved-vendor"></a>Kan ikke skifte ikrafttrædelsesdato for en godkendt kreditor


## <a name="symptoms"></a>Symptomer

Et produkt har en godkendt kreditor, der f.eks. har ikrafttrædelsesdatoen 11. januar 2018 (*01/11/2018*) og udløbsdatoen *Aldrig*. Hvis du forsøger at ændre ikrafttrædelsesdatoen til 10. januar 2018 (*01/10/2018*) eller 12. januar 2018 (*01/12/2018*), får du vist følgende fejl:

> Der kan ikke oprettes en post på listen over godkendte kreditorer (PdsApproveVendorList). Værdien 'Udløb' skal være større end eller lig med værdien 'Gyldig fra'.

## <a name="resolution"></a>Løsning

Du kan kun udvide den periode, som kreditoren er godkendt til. Der gælder følgende regler:

- Hvis du vil ændre ikrafttrædelsesdatoen, så den er tidligere end nogen af de eksisterende poster (perioder) for varens leverandør, skal udløbsdatoen for den nye periode være før alle udløbsdatoerne i de eksisterende poster.
- Hvis du vil ændre udløbsdatoen, så den er senere end nogen af de eksisterende perioder, skal ikrafttrædelsesdatoen være efter den seneste udløbsdato i en eksisterende post.
- Hvis du vil reducere den overordnede periode, som kreditoren er godkendt for, skal du slette eller redigere eksisterende poster. Du kan også bruge **afkort**-parameteren under importen. Denne parameter sletter alle eksisterende poster i tabellen for godkendte kreditorer efter vare.

I eksempelscenariet, der er beskrevet i problembeskrivelsen, hvor en post har ikrafttrædelsesdatoen *01/11/2018* og en udløbsdato på *Aldrig*, kan du importere en ny post, der har ikrafttrædelsesdatoen *01/10/2018* og en udløbsdato på *Aldrig*. Du kan dog ikke reducere perioden, så ikrafttrædelsesdatoen opdateres til *01/12/2018* via Dataadministration. Du skal foretage denne ændring via brugergrænsefladen.
