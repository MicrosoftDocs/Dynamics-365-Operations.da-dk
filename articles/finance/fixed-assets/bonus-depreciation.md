---
title: Straksafskrivning
description: Denne artikel indeholder en oversigt over funktionerne til bonusafskrivning.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: roschlom
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41a59b9dfe0482c995cfefc7a70f63550794428d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969172"
---
# <a name="bonus-depreciation"></a>Straksafskrivning

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over funktionerne til bonusafskrivning.

Du kan bruge straksafskrivning til ekstra- eller straksafskrivning det første år, et anlægsaktiv er taget i anvendelse og afskrives. Straksafskrivning skal foretages før eventuelle andre afskrivningsberegninger. Det er derfor bedst at bruge straksafskrivning med bøger, hvor bogføring til Finans-funktionalitet er deaktiveret. Du kan bruge indstillingen **Slet transaktioner, der ikke er bogført i Finans** til at slette historiske transaktioner for bøger, der ikke bogføres i finansmodulet. Du kan derefter tilpasse straksafskrivning senere i aktivets levetid ved at slette afskrivningstransaktioner, der tidligere er bogført. 

Du kan beregne straksafskrivningen ved hjælp af forslagsprocessen, eller du kan oprette manuelle transaktioner til straksafskrivning. Du kan ikke oprette transaktioner til straksafskrivning, hvis der findes afskrivningstransaktioner eller transaktioner til afskrivningsregulering for den pågældende afskrivningsmodel.

Når du bruger forslagsprocessen til beregning af straksafskrivning, inkluderes alle eksisterende transaktioner i beregningen af grundlaget. Beregningen inkluderer også eventuelle tidligere straksafskrivninger, som du har angivet manuelt for aktivet. 

Når der skal foretages mere end én straksafskrivning for et aktiv, tages prioriteten i betragtning. Hver straksafskrivning reducerer anlægsaktivgrundlaget for den efterfølgende straksafskrivning. Restværdien medtages ikke i anlægsaktivgrundlaget ved beregninger af straksafskrivning, og afskrivningsprincippet gælder ikke for straksafskrivningen. 

I USA er det i øjeblikket sådan, at visse anlægsaktiver gælder som Section 179-anlægsaktiver. En Section 179-afskrivning giver mulighed for at afskrive alle eller nogle af omkostningerne for et bestemt anlægsaktiv, op til en vis grænse. Du kan få dækning for omkostningen ved at afskrive den i det år, hvor anlægsaktivet tages i anvendelse.

## <a name="example"></a>Eksempel
Følgende straksafskrivninger er tilknyttet en aktivbog:

-   **Section 179:** 1.000,00, Prioritet 1
-   **Fritagelseszone:** 30 procent, Prioritet 2

Omkostningerne ved anskaffelsen af anlægsaktivet er 5.000,00. Når straksafskrivningen beregnes, vil beløbet for den første straksafskrivning være 1.000,00 for Section 179-afskrivningen. 

Det næste straksafskrivningsbeløb i afskrivningen for Liberty Zone beregnes som følger: 

Anskaffelsesomkostninger – 1.000 (Section 179-afskrivning) x 30 % = 1.200 

Hvis beløbet i straksafskrivningen er større end det resterende beløb for anskaffelsesomkostningen, vil beløbet for straksafskrivningen enten være resultatet af den beregnede straksafskrivning eller den resterende anskaffelsesomkostning afhængigt af, hvilket beløb der er mindst. 

Hvis den tilbageværende anskaffelsesomkostning er 0 (nul) eller mindre end nul, genereres der ikke afskrivningstransaktioner. 

Når straksafskrivningen beregnes ved hjælp af forslagsprocessen, oprettes der en transaktion for straksafskrivningen for alle de relevante straksafskrivningsposter, der er tilknyttet aktivbogen. 

Du kan oprette et ubegrænset antal straksafskrivningsposter. Når du har tildelt aktivgruppebogen disse poster, anvendes de i aktivbogen. 

Straksafskrivningen angives som enten en procentsats eller et fast beløb. Når du bogfører afskrivningsforslag, bogføres transaktionerne for straksafskrivningen i bogen som andre transaktioner end afskrivningstransaktionerne.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]