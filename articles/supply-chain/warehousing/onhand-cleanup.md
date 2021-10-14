---
title: Job til oprydning i disponible poster til lokationsstyring
description: Dette emne beskriver jobbet til oprydning i disponible poster, som hjælper med at forbedre systemets ydeevne ved at identificere og slette relaterede, men unødvendige poster.
author: perlynne
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: d839ed861a24f6ef7267c85e942c275586b4a8c4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565090"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a>Job til oprydning i disponible poster til lokationsstyring

[!include [banner](../includes/banner.md)]

Ydeevnen af forespørgsler, der bruges til at beregne den disponible lagerbeholdning, påvirkes af antallet af poster i de tabeller, der er involveret. Én måde at forbedre ydeevnen på er at reducere antallet af poster, som databasen skal overveje.

Dette emne beskriver jobbet til oprydning i disponible poster, som sletter unødvendige poster i tabellerne InventSum og WHSInventReserve. Disse tabeller bruges til opbevaring af beholdningsoplysninger for varer, der er aktiveret til behandling i lokationstyring. (Disse varer kaldes WHS-varer). Sletning af disse poster kan forbedre ydeevnen for beregninger af den disponible lagerbeholdning betydeligt.

## <a name="what-the-cleanup-job-does"></a>Dette gør oprydningsjobbet

Jobbet til opryding i disponible poster sletter eventuelle poster i tabellen WHSInventReserve og InventSum, hvor alle feltværdier er *0* (nul). Disse poster kan slettes, fordi de ikke bidrager til oplysninger om den disponible lagerbeholdning. Jobbet sletter kun poster, der er under **Lokations**-niveauet.

Hvis negativt fysisk lager er tilladt, kan oprydningsjobbet måske ikke slette alle de relevante poster. Grunden til denne begrænsning er, at jobbet skal tillade et særligt scenarie, hvor en nummerplade har flere serienumre, og et af disse serienumre er blevet negative. For eksempel vil systemet blive sat til nul disponibel på nummerpladeniveau, når en nummerplade har +1 stk. af serienummer 1 og -1 stk. af serienummer 2. I dette særlige scenarie foretager jobbet en bredde-først-sletning, hvor det forsøger at slette fra lavere niveauer først.

## <a name="schedule-and-configure-the-cleanup-job"></a>Planlægge og konfigurere odprydningsjobbet

Oprydningsjobbet for disponible poster finder du i **Lagerstyring \> Periodiske opgaver \> Oprydning \> Oprydning i disponible poster til lokationsstyring**. Brug standardindstillingerne for jobbet til at styre omfanget af og planen for kørsel af jobbet. Desuden findes der følgende indstillinger:

- **Slet, hvis der ikke er opdateret i så mange dage** – Angiv det mindste antal dage, jobbet skal vente, før det sletter en disponibel post, der er faldet til nul antal. Brug denne indstilling til at reducere risikoen for at slette de disponible poster, der stadig bruges. Hvis oprydningen skal finde sted så hurtigt som muligt, skal du enten indtaste *0* (nul) eller lade feltet være tomt.
- **Maksimal kørselstid (timer)** – Angiv den maksimale kørselstid for oprydningsjobbet i timer. Hvis jobbet ikke fuldføres indenfor dette tidsrum, gemmes det arbejde, det har fuldført indtil nu, og lukkes derefter. Denne funktion er især relevant for implementeringer, der krævet stort lager. I disse tilfælde bør du planlægge, at jobbet skal køres på tidspunkter, hvor systembelastningen er så lille som muligt. Hvis du vil have, at batchjobbet skal fortsætte med at køre, indtil det er fuldført, skal du enten indtaste *0* (nul) eller lade feltet være tomt. Denne indstilling er kun tilgængelig, hvis den relaterede funktion er [aktiveret i systemet](#max-execution-time).

Selvom du kan køre jobbet inden for normal arbejdstid, anbefales det, at du kører det uden for arbejdstiden. På denne måde er du med til at forhindre konflikter, der kan opstå, hvis en bruger arbejder med en post, der også ryddes op i.

Hvis jobbet forsøger at slette en post for en vare, mens den pågældende post bruges af en anden bruger, opstår der en deadlock-fejl for enten oprydningsjobbet eller brugeren.

Når jobbet kører, har det en commit size (mængde af reserveret virtuel hukommelse) på 100. Det vil med andre ord forsøge at "committe" én gang for hver 100-sletning. Men da visse sletninger er sætbaserede, kan der være situationer, hvor der kan slettes mere end 100 poster i samme transaktion. Derfor kan låseeskaleringer undertiden stadigvæk forekomme.

## <a name="possible-user-impact"></a>Mulig brugereffekt

Brugere kan blive påvirket, hvis jobbet til oprydning af disponible poster sletter alle poster for et givet niveau (f.eks. nummerpladeniveauet). I dette tilfælde kan det ske, at funktionaliteten til visning af dette lager, som tidligere var direkte tilgængelig på nummerpladen, ikke fungerer som forventet, da de relevante disponible poster ikke længere er tilgængelige. Dette kan f.eks. opleves i følgende situationer:

- Når brugeren på **Beholdningsliste** fravælger betingelsen **Antal \<\> 0** eller vælger betingelsen **Lukkede posteringer** i indstillingerne for **Dimensionsvisning**.
- I en **Fysisk lager pr. lagerdimension**-rapport for tidligere perioder, hvor brugeren angiver parameteren **Pr. dato**.

Den forbedring af ydeevnen, som oprydningsjobbet skal give, skulle dog kompensere for dette mindre funktionalitetstab.

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a>Gøre indstillingen for den maksimale kørselstid tilgængelig

Som standard er indstillingen for **Maksimal kørselstid** ikke tilgængelig. Hvis du vil anvende den, skal du bruge [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) for at aktivere den relaterede funktion i systemet. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Den maksimale kørselstid for job til oprydning i disponible poster til lokationsstyring*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]