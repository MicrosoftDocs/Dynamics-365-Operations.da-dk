---
title: Registrere modtagelsen af returnerede varer
description: Du kan registrere modtagelsen af returnerede varer ved hjælp af formularen Modtagelsesoversigt eller formularen Registrering.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42ca1d4d2d9b45d79cf479833f83e498e3b73540
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424371"
---
# <a name="register-the-receipt-of-returned-items"></a>Registrere modtagelsen af returnerede varer 

[!include [banner](../includes/banner.md)]


Der findes to metoder til at registrere modtagelsen af returnerede varer. Den første metode er en lagertilgangsproces, der bruger formularen **Modtagelsesoversigt**. Den anden bruger formularen **Registrering**.

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a>Registrere modtagelsen af returnerede varer i formen Modtagelsesoversigt

Du kan bruge formularen **Modtagelsesoversigt** til at identificere en returforsendelse ved dens RMA-nummer (Return Material Authorization). Hvis der er defineret et kladdenavn under fanen **Opsætning**, og der findes kladdelinjer, som svarer til de linjer, der er valgt i formularen **Modtagelsesoversigt** , oprettes der et nyt kladdehoved, når du klikker på **Start modtagelse**.

1.  Klik på **Lagerstyring** \> **Periodisk** \> **Modtagelsesoversigt**.

2.  I feltet **Opsætningsnavn** skal du vælge **Returordre** og derefter klikke på **Opdater**.
    

    > [!TIP]
    > <P>Du kan bruge <STRONG>Afgrænsning</STRONG>-felterne til at indsnævre søgeresultaterne. Du kan skrive eller vælge RMA-nummeret i feltet <STRONG>RMA-nummer</STRONG> for at få et præcist resultat. Hvis du vil definere og gemme et sæt filtre, der begrænser, hvilke indgående modtagelser der skal vises, skal du klikke på fanen <STRONG>Opsætning</STRONG>. De tilgængelige filtre omfatter typer, lagersteder og modtagelsesområder.</P>

    

    > [!WARNING]
    > <P>Returordrer kan ikke blandes med andre modtagelsestyper i formularen <STRONG>Modtagelsesoversigt</STRONG>. Derfor er referencen altid en salgsordre, men der angives ikke et salgsordre-id angives på kladdehovedet.</P>



3.  Find den linje, der svarer til den vare, der returneres, i gitteret **Tilgange**, og markér derefter afkrydsningsfeltet i kolonnen **Vælg til modtagelse**.

4.  Hvis du vil udelukke bestemte linjer fra returmodtagelse, f.eks. varer fra den oprindelige ordre, der ikke var medtaget i returforsendelsen, skal du fjerne markeringen i de tilknyttede **Vælg til modtagelse**-felter i tabellen **Linjer** i den nederste del af formularen.

5.  Klik på knappen **Start modtagelse** for at oprette en modtagelseskladde.
    

    > [!NOTE]
    > <P>Du kan markere flere returordrer og medtage dem alle i en enkelt modtagelsesproces. Hver returordrelinje kopieres til en tilsvarende linje i varemodtagelseskladden.</P>

    

    > [!NOTE]
    > <P>Du kan også oprette en modtagelseskladde manuelt ved hjælp af formularen <STRONG>Varemodtagelse</STRONG>. 



6.  Klik på **Lagerstyring** \> **Kladder** \> **Varemodtagelse** \> **Varemodtagelse**.

7.  Vælg den modtagelseskladde, du lige har oprettet, og klik derefter på **Linjer** for at åbne formularen **Kladdelinjer, lokationer**.

8.  Juster evt. antallet i feltet **Antal** under fanen **Generelt**, og tildel derefter en dispositionskode i feltet **Dispositionskode**.
    
    Du kan også markere afkrydsningsfeltet **Karantænestyring** for at få de returnerede varer sendt via en inspektionsproces i forbindelse med en karantæneordre.
    

    > [!NOTE]
    > <P>Hvis du sender de returnerede varer via karantæne, kan du ikke angive en dispositionskode.</P>



9.  Klik på knappen **Valider**.

10. Hvis der ikke forekommer fejl under valideringen, skal du klikke på **Bogfør**.

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a>Registrere modtagelsen af returnerede varer i formen Registrering

I stedet for at bruge formularen **Modtagelsesoversigt** kan du bruge formularen **Registrering** til at registrere modtagelsen af returnerede varer.

1.  Klik på **Salg og marketing** \> **Generelt** \> **Returordrer** \> **Alle returordrer**. Opret en ny returordre, eller åbn returordren på listen. Vælg returordrelinjen i oversigtspanelet **Linjer**. Klik på **Opdater linje**, og klik derefter på **Registrering**.

2.  Tildel en dispositionskode i feltet **Dispositionskode**, og klik derefter på **OK**.
    

    > [!NOTE]
    > <P>Du kan ikke sende varen til inspektion som en karantæneordre ved hjælp af formularen <STRONG>Registrering</STRONG>.</P>



3.  I gitteret **Transaktioner** skal du vælge den transaktion, der skal registreres.

4.  I gitteret **Registrer nu** skal du klikke på **Tilføj**. Gentag de forrige to trin, indtil alle de returnerede varer vises i gitteret **Registrer nu**.

5.  Klik på **Bogfør alle**.

## <a name="see-also"></a>Se også

[Modtagelsesoversigt (form)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))

  


