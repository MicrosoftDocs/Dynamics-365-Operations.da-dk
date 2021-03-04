---
title: Styklisteskabeloner
description: En styklisteskabelon indeholder en standardiseret liste over komponenter for serviceobjekter, der serviceres regelmæssigt.
author: ShylaThompson
manager: tfehr
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88e732f64b389acafee23427594225dfacda71cc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424581"
---
# <a name="template-boms"></a>Styklisteskabeloner    

[!include [banner](../includes/banner.md)]


En styklisteskabelon giver dig en standardiseret liste over komponenter for serviceobjekter, der serviceres regelmæssigt. Komponenterne i styklisteskabelonen repræsenterer de enkelte underkomponenter i serviceobjektet. Ved at anvende en styklisteskabelon på et serviceobjekt kan du registrere de underkomponenter, der er erstattet på serviceobjektet.

Hvis du vil anvende en styklisteskabelon på en serviceaftale eller en serviceordre, skal du knytte den til en serviceobjektrelation.


> [!NOTE]
> <P>Du kan kun anvende én styklisteskabelon på et serviceobjekt.</P>

## <a name="create-a-template-bom"></a>Oprette en styklisteskabelon

Følgende tabel indeholder oplysninger om de forskellige metoder, du kan bruge til at oprette en styklisteskabelon.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Metode</p></th>
<th><p>Beskrivelse</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Produktion</p></td>
<td><p>Styklisteskabelonen er baseret på en produktionsordre. Denne indstilling kan kun anvendes, hvis du arbejder i et produktionsmiljø. Fordelen er, at du har en aktuel og detaljeret liste over de komponenter, der udgør en vare.</p></td>
</tr>
<tr class="even">
<td><p>Vare BOM</p></td>
<td><p>Styklisteskabelonen er baseret på en varestykliste. I modsætning til produktionsstyklisten er varestyklisten en statisk liste over de komponenter, en vare består af.</p></td>
</tr>
<tr class="odd">
<td><p>Eksisterende skabelon</p></td>
<td><p>Skabelonen er baseret på en eksisterende styklisteskabelon.</p></td>
</tr>
<tr class="even">
<td><p>Manuel</p></td>
<td><p>Hvis du ved, hvilke reservedele der typisk udskiftes i et serviceobjekt, kan du oprette din styklisteskabelon manuelt. Med denne metode kan du sikre, at komponenterne i skabelonen afspejler de faktiske krav på arbejdspladsen.</p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a>Anvende en styklisteskabelon på en serviceaftale eller en serviceordre

Du kan anvende en styklisteskabelon på en serviceaftale, en serviceordre eller begge. Serviceaftalen omfatter normalt det langvarige forhold til en kunde. Historikken over udskiftninger, der registreres i servicestyklisten, kan med fordel registreres i serviceaftalen.

Du kan også anvende en styklisteskabelon på en serviceordre for at registrere historikken for den service, der er udført på et serviceobjekt.

## <a name="copy-the-history-of-a-service-bom"></a>Kopiere historikken i en servicestykliste

Du kan kopiere historikken for en servicestykliste fra én serviceaftale til en anden. Ved at kopiere servicehistorikken mellem serviceaftaler kan du registrere udskiftninger for en vare.

**Eksempel**

Du har oprettet en treårig serviceaftale for en kundes bil. I denne periode bliver kunden vant til den gode service, som virksomheden yder. Så når aftalen udløber, ønsker kunden at indgå en ny. Du kan nu forhandle en mere fordelagtig aftale for firmaet. Da du kan få brug for registreringen af udskiftede komponenter i fremtiden, kopierer du historikken for servicestyklisten til den nye aftale.

## <a name="modify-the-template-bom"></a>Redigere styklisteskabelonen

Hvis der ikke er knyttet en styklisteskabelon til et serviceobjekt, kan du redigere eller slette linjerne i den. Når styklisteskabelonen er knyttet til et serviceobjekt, kan du kun redigere den lokale version af styklisten. Hvis du vil kopiere opsætningen af en lokal version af styklisteskabelonen, kan du oprette en ny styklisteskabelon baseret på den lokale version. Du kan finde flere oplysninger under [Redigere en servicestykliste](modify-service-bom.md).

Hvis du erstatter en vare på styklisten, kan du registrere erstatningen på styklistelinjen i styklistedesigneren. Du kan eventuelt oprette en serviceordrelinje for erstatningsobjektet. Hvis du opretter en serviceordrelinje, kan du fakturere erstatningsvaren. Hvis du ikke opretter en serviceordrelinje for en erstatning, bevares registreringen af erstatningen, så du kan spore serviceobjektets historik.

## <a name="change-how-information-on-the-bom-line-is-displayed"></a>Ændre visningen af oplysninger på styklistelinjen

Du kan ændre visningen af oplysninger for en styklistelinje for alle styklisteskabeloner og servicestyklister. Ændringerne anvendes på alle styklisteskabeloner og servicestyklister. Dette omfatter de styklister, der er knyttet til serviceobjekter.

## <a name="set-up-number-sequences-for-template-boms"></a>Oprette nummerserier for styklisteskabelonerne

Hvis du vil bruge styklisteskabeloner, skal du oprette to nummerserier. Opret én nummerserie for styklisteskabelonen og én for linjenummeret for styklistehistorikken.


> [!NOTE]
> <P>Nummerserier bruges til at tildele identifikatorer til poster, der kræver dem. Før du kan tildele en nummerserie til en styklisteskabelon eller et linjenummer for styklistehistorikken, skal du angive nummerseriekoderne.</P>


## <a name="set-up-number-sequences"></a>Oprette nummerserier

1.  Opret nummerserier for styklisteskabeloner og linjenummeret for styklistehistorikken på listesiden **Nummerserier**. 

2.  Klik på **Servicestyring** \> **Opsætning** \> **Parametre for servicestyring**.

3.  Klik på **Nummerserier**, og vælg derefter en nummerseriekode for de nummerseriereferencer, du oprettede i formularen **Nummerserier**.

4.  Luk formen for at gemme ændringerne.


> [!NOTE]
> <P>Linjenummeret for styklistehistorikken bruges til at knytte posteringer i styklisteoversigten til en serviceaftale eller serviceordre. Nummeret vises ikke i brugergrænsefladen.</P>



## <a name="see-also"></a>Se også

[Oprette en styklisteskabelon](create-template-bom.md)

[Administrere styklisteskabeloner på objektrelationer](manage-template-boms-on-object-relations.md)

[Redigere en servicestykliste](modify-service-bom.md)

 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]