---
title: Oprette kreditorer, debitorer og varer for samhandel internt i firmaet
description: Denne artikel beskriver oprettelse af kreditorer, debitorer og varer for samhandel internt i firmaet
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4c928435a4e66832b09dbc805664934cfb1236be
ms.sourcegitcommit: b666289f5113d0a3fa2220fe337d5aacf07cbd92
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/08/2022
ms.locfileid: "8945749"
---
# <a name="set-up-vendors-customers-and-items-for-intercompany-trade"></a>Oprette kreditorer, debitorer og varer for samhandel internt i firmaet

[!include [banner](../../includes/banner.md)]

Når du skal forberede din organisation til intern handel, skal du definere leverandører og kunder, som du vil handel internt med. Derefter skal du knytte disse leverandører og kunder sammen med de varer, du vil købe eller sælge.

1. Gå til **Indkøb og forsyning \> Kreditorer \> Alle kreditorer**.
1. Vælg leverandøren, der skal defineres som en intern leverandør.
1. I handlingsruden skal du under fanen **Generelt** vælge **Intern**.
1. Angiv parametre for intern opsætning for leverandørkontoen. Disse parametre omfatter kundens juridiske enhed og konto, politikker for salgsordre, politikker for indkøbsordre, værditilknytning og politikker for købs-og salgsaftaler. Du også angive, om der skal bruges stamdataværdier fra leverandørkontoen eller fra kundekontoen i den anden juridiske enhed.
1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. På listesiden **Frigivne produkter** skal du markere de varer, der skal tildeles leverandøren, så varerne er tilgængelige til internhandel. På siden **Frigivne produktdetaljer** for en vare. Gå til formen , og angiv kreditornummeret i feltet **Kreditor** på fanen **Køb**.
1. Gå til **Debitorer \> Kunder \> Alle kunder**.
1. Vælg den kunden, der skal defineres som intern kunde.
1. I handlingsruden skal du under fanen **Generelt** vælge **Intern**.
1. Angiv parametre for intern opsætning for kundekontoen. Disse parametre omfatter leverandørens juridiske enhed og konto, politikker for indkøbsordre, politikker for salgsordre, værditilknytning og politikker for salgs- og købsaftaler. Du også angive, om der skal bruges stamdataværdier fra kundekontoen eller fra leverandørkontoen i den anden juridiske enhed.
1. Når du er færdig med at konfigurere de interne parametre, skal du lukke siden **Intern handel** for at vende tilbage til de valgte kundeoplysninger.
1. Udvid oversigtspanelet **Diverse**, og angiv **Opret interne ordrer** til *Ja*. Hvis ordrerne også skal leveres direkte til kunderne, skal du markere afkrydsningsfeltet **Direkte levering** til *Ja*.

    > [!NOTE]
    > Hvis organisationen lagerfører og leverer nogle af varerne til kunder, kan det være en god idé med automatisk oprettelse af interne ordrer, også selvom varen er på lager. Hvis du vil deaktivere den automatiske generering af ordrer for de varer, der somme tider lagerføres, skal du indstille **Opret interne ordre** til *Nej*.

1. Hvis du vil tillade, at ekstra linjer oprettes indirekte på en salgsordre, skal du indstille **Opret interne ordrelinjer** til *Ja*. En bruger kan så føje linjer til den oprindelige salgsordre fra den interne salgsordre.

> [!WARNING]
> Hvis du tillader, at ordrelinjer oprettes indirekte, giver du tilladelse til alle tilføjelser til den oprindelige salgsordre fra den interne salgsordre. Hver tilføjelse behandles derefter videre til kunden og føjes til ordren og fakturaen. Hvert dokument, der er involveret i salget, udskrives desuden og bogføres automatisk. Brugerne bliver ikke advaret om tilføjelsen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
