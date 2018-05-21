--- 
title: Konfigurere validering af sammenholdelse af kreditorfakturaer
description: Denne registrering anvender demofirmaet USMF.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e9bf83269c34133509734691fd018ee703c40626
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Konfigurere validering af sammenholdelse af kreditorfakturaer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne registrering anvender demofirmaet USMF. Rollen kreditorchef eller rollen regnskabschef skal udføre disse trin. Inden du begynder, skal du kontrollere, at konfigurationsnøglen til fakturasammenholdelse er valgt. Hvis den juridiske enhed sporer udgifter, f.eks. fragt, med brug af tillæg, skal du sørge for, at konfigurationsnøglen Gebyrer er valgt.  Fakturasammenholdelse for kreditorer er den proces, hvor kreditorfakturaen, indkøbsordren og produktkvitteringen sammenholdes. Forskelle mellem disse dokumenter kaldes matchningafvigelser. Matchningsafvigelser sammenlignes med de angivne tolerancer. Hvis en matchningafvigelse overskrider toleranceprocenten eller -beløbet, vises ikoner for matchafvigelse i formularen Kreditorfaktura og formularen Detaljer om fakturasammenholdelse.

1. Gå til Kreditor > Opsætning > Kreditorparametre.
2. Klik på fanen Fakturavalidering.
3. Markér eller fjern markeringen i afkrydsningsfeltet Aktivér validering af fakturasammenholdelse.
    * Vælg, om der kræves godkendelse, før en faktura, der indeholder uoverensstemmelser ved fakturasammenholdelse, kan bogføres. Hvis der er angivet Tillad med en advarsel, vises en visuel indikation, når en uoverensstemmelse ved fakturasammenholdelse overstiger tolerancen. Du vil dog kunne bogføre fakturaen. Du kan bruge arbejdsgange sammen med validering af fakturasammenholdelse, Sørg for at bogføre fakturaen med feltet Uoverensstemmelser indstillet til Tillad med en advarsel for at undgå at skulle godkende flere gange.  
    * I Opdater status for sammenholdeles af fakturahoved automatisk skal du vælge, om sammenholdelse vil blive udført automatisk under dataindtastning af faktura af systemet. Den anbefalede indstilling er Ja, medmindre du oplever problemer med ydeevnen ved dataindtastning. Deaktivering af automatiske opdateringer kan give hurtigere systemydeevne, fordi validering af fakturasammenholdelse ignoreres under dataindtastning. Medarbejderen til indtastning af data skal opdatere status for fakturasammenholdelse manuelt for at få vist valideringsresultaterne for fakturasammenholdelse, når dette er angivet til Nej.  
4. Slå udvidelse af sektionen Sammenholdelse af fakturatotaler til/fra.
5. Markér eller fjern markeringen i afkrydsningsfeltet Afstem fakturatotaler for at sammenholde faktiske fakturatotaler med forventede totaler.
    * Vælg, om der skal vises et ikon, hvis en uoverensstemmelse ved fakturasammenholdelse overstiger tolerancen. Du kan vælge at få vist ikonet, når en positiv uoverensstemmelse overstiger tolerancen, eller når enten en positiv eller en negativ uoverensstemmelse overstiger tolerancen.  
    * Tolerancen er f.eks. 5 procent, og det samlede fakturabeløb på indkøbsordren er 100,00. Derfor vises der et ikon for prisafstemning, hvis det samlede fakturabeløb på fakturaen overstiger 105,00. Hvis du vælger Hvis større eller mindre end tolerance, vises ikonet også, hvis fakturabeløbet er mindre end 95,00.  
6. Indtast et tal i feltet Toleranceprocent for fakturatotaler.
7. Slå udvidelse af sektionen Sammenholdelse af pris og antal til/fra.
    * I feltet Sammenholdelsespolitik for linjer skal du vælge en værdi, der skal bruges som standardpolitik for den juridiske enhed, du arbejder med. "Kræves ikke" betyder, at der ikke kræves nogen kontrol af individuelle priser på fakturalinjer i forhold til indkøbsordrepris eller fakturaantal i forhold til antal på følgesedlen. "Tovejssammenholdelse" betyder, at kontrol af fakturalinjerne er påkrævet, men at kun indkøbsordren og leverandørens fakturadokumenter er inddraget i kontrollen. Produktkvitteringen medtages ikke i valideringerne af sammenholdelse. "Trevejsafstemning" betyder, at nettoenhedsprisen på fakturaen sammenlignes med nettoenhedsprisen på indkøbsordren, og det tilsvarende antal på produktkvitteringen sammenlignes med antallet på fakturaen.  
    * Hvis du bruger en sammenholdelsespolitik for linjer, som er tovejs-sammenholdelse eller trevejs-sammenholdelse, kan du konfigurere pristoleranceprocenter for din juridiske enhed, varer og kreditorer på siden med pristolerance for varer. Når kreditorfakturaer sammenholdes med oplysningerne på indkøbsordrer, søges der efter den relevante pristoleranceprocent.  
8. Vælg en indstilling i feltet Sammenholdelsespolitik for linjer.
    * Hvis der skal kunne anvendes et andet sammenholdelsesniveau for en vare, kreditor, kombination af kreditor og vare eller indkøbsordrelinje, skal du vælge en værdi i feltet Tillad overstyring af sammenholdelsespolitik. Sammenholdelsespolitikken for linjer for den juridiske enhed kan overstyres for en bestemt kreditor, vare og kombination af kreditor og vare på siden Sammenholdelsespolitik.  
    * Hvis du vil sammenligne pristotaler for linjeelementer på fakturaer, skal du vælge en værdi i feltet Afstem pristotaler. Denne type sammenholdelse er nyttig, når leverandøren sender flere fakturaer for samme indkøbsordrelinje. Du kan sammenligne prisoplysninger for nettobeløbet på hver linje på fakturaen og alle ventende og tidligere bogførte fakturalinjer med nettobeløbet på den tilsvarende indkøbsordrelinje.  
9. Vælg en indstilling i feltet Afstem pristotaler.
10. Indtast et tal i feltet Tolerance for indkøbspristotaler.
11. Slå udvidelsen af sektionen Sammenholdelse af gebyrer til/fra.
12. Hvis du vil sammenligne faktiske gebyrer med forventede gebyrer baseret på oplysninger på indkøbsordren, skal du markere afkrydsningsfeltet Sammenhold gebyrer.
13. Luk siden.


