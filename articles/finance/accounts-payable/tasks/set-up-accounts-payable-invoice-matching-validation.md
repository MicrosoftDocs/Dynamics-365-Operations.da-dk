---
title: Konfigurere validering af fakturasammenholdelse for kreditor
description: Dette emne indeholder oplysninger om, hvordan validering af fakturasammenholdelse for kreditorer defineres.
author: abruer
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a101edd9e25fba1aa2325cb2193c6ea56282c9d1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441501"
---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Konfigurere validering af fakturasammenholdelse for kreditor

[!include [banner](../../includes/banner.md)]

Inden du begynder, skal du kontrollere, at konfigurationsnøglen til fakturasammenholdelse er valgt. Hvis den juridiske enhed sporer udgifter, f.eks. fragt, med brug af tillæg, skal du sørge for, at konfigurationsnøglen Gebyrer er valgt.  Fakturasammenholdelse for kreditorer er den proces, hvor kreditorfakturaen, indkøbsordren og produktkvitteringen sammenholdes. Forskelle mellem disse dokumenter kaldes matchningafvigelser. Matchningsafvigelser sammenlignes med de angivne tolerancer. Hvis en sammenholdelsesafvigelse overskrider toleranceprocenten eller -beløbet, vises ikoner for matchafvigelse på siden **Kreditorfaktura** og på siden **Detaljer om fakturasammenholdelse**.

## <a name="determine-which-invoice-matching-validation-to-use"></a>Bestemme, hvilken validering af fakturasammenholdelse der skal bruges
Der findes fire forskellige typer sammenholdelsesvalideringer. 

- **Sammenholdelse på linjeniveau** – den mest almindelige type sammenholdelse er linjesammenholdelse. Sammenholdelse på linjeniveau kan være tovejs- eller trevejssammenholdelse. Standardsammenholdelse på linjeniveau kan angives for en juridisk enhed på siden **Kreditorparametre**. Tovejssammenholdelse sammenligner enhedsprisen på fakturaen med enhedsprisen på indkøbsordren. Trevejssammenholdelse sammenligner fakturamængden med den sammenholdte mængde på produktkvitteringen.
- **Sammenholdelse af fakturatotaler** – sammenlign de samlede beløb på fakturaen med de samlede beløb på indkøbsordren. Denne type fakturasammenholdelse involverer færrest detaljer, så du kan bruge denne indstilling til at definere kontrolelementer, der minimerer den tid, personalet skal bruge på at gennemgå oplysninger om fakturasammenholdelse. Der sammenlignes seks totaler, herunder Subtotal, Slutrabat, Tillæg, Moms, Afrund og Fakturabeløb. Systemet validerer, om nogen af disse værdier på fakturaen afviger fra de forventede beløb med mere end en acceptabel afvigelse.
- **Sammenholdelse af tillæg**  – sammenlign oplysninger om tillæg (beløb) på fakturaen med oplysningerne om tillæg (beløb) på indkøbsordren
- **Pristotaler for linjevaresammenholdelse** – denne type sammenholdelse er nyttig for firmaer, der typisk modtager flere fakturaer for en enkelt indkøbsordrelinje. Hvis du typisk kun modtager én faktura pr. indkøbsordrelinje, er denne type sammenholdelse ikke nødvendig. Denne sammenholdelse kræver, at tovejs- eller trevejs-sammenholdelse er aktiveret og fungerer som en validering af nettobeløb, der ikke må overskrides, baseret på en toleranceprocent og beløb.  Denne sammenholdelse sammenligner prisoplysninger for nettobeløbet på hver linje på fakturaen og alle ventende og tidligere bogførte fakturalinjer med nettobeløbet på den tilsvarende indkøbsordrelinje. Nettobeløbet bestemmes af følgende formel: (Enhedspris * linjeantal) + linjetillæg - linjerabatter. Når du sammenholder pristotaler med procentdel, sammenligner systemet værdier ved hjælp af transaktionsvalutaen. Når du sammenholder pristotaler med beløb, sammenligner systemet værdierne ved hjælp regnskabsvalutaen.

## <a name="set-up-parameters-to-enable-invoice-matching-validation"></a>Konfigurer parametre for at aktivere validering af sammenholdelse af fakturaer
1. Gå til **Kreditor > Opsætning > Kreditorparametre**.
2. Vælg fanen **Fakturavalidering**.
3. Markér eller fjern markeringen i afkrydsningsfeltet **Aktivér validering af fakturasammenholdelse**.
    * Vælg, om der kræves godkendelse, før en faktura, der indeholder uoverensstemmelser ved fakturasammenholdelse, kan bogføres. Hvis der er angivet **Tillad med en advarsel**, vises en visuel indikation, når en uoverensstemmelse ved fakturasammenholdelse overstiger tolerancen. Du vil dog kunne bogføre fakturaen. Du kan bruge arbejdsgange sammen med validering af fakturasammenholdelse. Sørg for at bogføre fakturaen med feltet **Bogfør faktura med uoverensstemmelser** er indstillet til **Tillad med en advarsel** for at undgå at skulle godkende flere gange.  
    * I feltet **Opdater status for sammenholdelse af fakturahoved automatisk** skal du vælge, om sammenholdelse vil blive udført automatisk under dataindtastning af faktura af systemet. Den anbefalede indstilling er **Ja**, medmindre du oplever problemer med ydeevnen ved dataindtastning. Deaktivering af automatiske opdateringer kan give hurtigere systemydeevne, fordi validering af fakturasammenholdelse ignoreres under dataindtastning. Medarbejderen til indtastning af data skal opdatere status for fakturasammenholdelse manuelt for at få vist valideringsresultaterne for fakturasammenholdelse, når dette er angivet til **Nej**.  
4. Indstil **Sammenholdelse af fakturatotaler**.
5. Markér eller fjern markeringen i afkrydsningsfeltet **Afstem fakturatotaler** for at sammenholde faktiske fakturatotaler med forventede totaler.
    * Vælg, om der skal vises et ikon, hvis en uoverensstemmelse ved fakturasammenholdelse overstiger tolerancen. Du kan vælge at få vist ikonet, når en positiv uoverensstemmelse overstiger tolerancen, eller når enten en positiv eller en negativ uoverensstemmelse overstiger tolerancen.  
    * Tolerancen er f.eks. 5 procent, og det samlede fakturabeløb på indkøbsordren er 100,00. Derfor vises der et ikon for prisafstemning, hvis det samlede fakturabeløb på fakturaen overstiger 105,00. Hvis du vælger **Hvis større eller mindre end tolerance**, vises ikonet også, hvis fakturabeløbet er mindre end 95,00.  
6. Angiv den procentvise afvigelse, der er acceptabel, i feltet **Toleranceprocent for fakturatotaler**. Denne værdi er standardværdien for firmaet. Denne værdi kan tilsidesættes for bestemte kreditorer ved hjælp af **Tolerancer for fakturatotaler**. Du kan finde flere oplysninger om, hvordan du tilsidesætter toleranceprocenten for fakturatotaler for en bestemt leverandør, i afsnittet "Konfigurer tolerance for sammenholdelse af fakturatotaler for kreditorer" senere i dette emne.
7. Indstil **Sammenholdelse af pris og antal**.
8. I feltet **Sammenholdelsespolitik for linjer** skal du vælge en værdi, der skal bruges som standardpolitik for den juridiske enhed, du arbejder med. **Kræves ikke** betyder, at der ikke kræves nogen kontrol af individuelle priser på fakturalinjer i forhold til indkøbsordrepris eller fakturaantal i forhold til antal på følgesedlen. **Tovejssammenholdelse** betyder, at kontrol af fakturalinjerne er påkrævet, men at kun indkøbsordren og leverandørens fakturadokumenter er inddraget i kontrollen. Produktkvitteringen medtages ikke i valideringerne af sammenholdelse. **Trevejsafstemning** betyder, at nettoenhedsprisen på fakturaen sammenlignes med nettoenhedsprisen på indkøbsordren, og det tilsvarende antal på produktkvitteringen sammenlignes med antallet på fakturaen.
9. Hvis der skal kunne anvendes et andet sammenholdelsesniveau for en vare, kreditor, kombination af kreditor og vare eller indkøbsordrelinje, skal du vælge en værdi i feltet **Tillad overstyring af sammenholdelsespolitik**. Sammenholdelsespolitikken for linjer for den juridiske enhed kan overstyres for en bestemt kreditor, vare og kombination af kreditor og vare på siden **Sammenholdelsespolitik**.
    * Hvis du bruger en sammenholdelsespolitik for linjer, som er tovejs-sammenholdelse eller trevejs-sammenholdelse, kan du konfigurere pristoleranceprocenter for din juridiske enhed, varer og kreditorer på siden med **pristolerance for varer**. Standardpristolerancen for den juridiske enhed angives til nul procent for tovejs- og trevejssammenholdelse. Når kreditorfakturaer sammenholdes med oplysningerne på indkøbsordrer, søges der efter den relevante pristoleranceprocent.   
10. Hvis du vil sammenligne pristotaler for linjeelementer på fakturaer, skal du vælge en værdi i feltet **Afstem pristotaler**. Denne type sammenholdelse er nyttig, når leverandøren sender flere fakturaer for samme indkøbsordrelinje. Du kan sammenligne prisoplysninger for nettobeløbet på hver linje på fakturaen og alle ventende og tidligere bogførte fakturalinjer med nettobeløbet på den tilsvarende indkøbsordrelinje.  Indstillinger omfatter **Ingen**, **Procent**, **Beløb** eller **Procent og beløb**.
11. I feltet **Toleranceprocent for indkøbspristotaler** skal du angive en procentdel af den varians, du vil acceptere. Dette felt er tilgængeligt, når **Afstem pristotaler** er indstillet til **Procent** eller **Procent og beløb**.
12. I feltet **Tolerance for indkøbspristotaler** skal du angive et beløb i regnskabsvalutaen. Dette felt er tilgængeligt, når **Afstem pristotaler** er indstillet til **Beløb** eller **Procent og beløb**.
13. I feltet **Vis ikon for afstemning af pristotal** skal du vælge, hvornår der skal vises et ikon, hvis en uoverensstemmelse for fakturasammenholdelse overstiger tolerancen for nettoenhedsprisen. Ikonet kan blive vist, når en positiv uoverensstemmelse overstiger tolerancen, eller når enten en positiv eller en negativ uoverensstemmelse overstiger tolerancen.
Tolerancen er f.eks. 5 procent, og den samlede linjepris på indkøbsordren er 10,00. Derfor vises der et ikon for prisafstemning, hvis den samlede linjepris på fakturaen overstiger 10,50. Hvis du vælger **Hvis større eller mindre end tolerance**, vises ikonet også, hvis samlede linjepris på fakturaen er mindre end 9,50.
13. Indstil sammenholdelsen af gebyrer.
14. Hvis du vil sammenligne faktiske gebyrer med forventede gebyrer baseret på oplysninger på indkøbsordren, skal du markere afkrydsningsfeltet **Sammenhold gebyrer**.

## <a name="set-up-unit-price-tolerance-percentages"></a>Konfigurer pristoleranceprocenter for enhed
Gå til **Kreditor > Opsætning > Konfiguration af fakturasammenholdelse > Pristolerancer** for at definerede de tilladte pristoleranceprocenter. Hvis du bruger en sammenholdelsespolitik for linjer, som er tovejs-sammenholdelse eller trevejs-sammenholdelse, kan du konfigurere pristoleranceprocenter for din juridiske enhed, varer og kreditorer. Når kreditorfakturaer sammenholdes med oplysningerne på indkøbsordrer, søges der efter den relevante pristoleranceprocent. Følgende er i standardsøgerækkefølge:
* Tabel/Tabel
* Tabel/Gruppe
* Tabel/Alt
* Gruppe/Tabel
* Gruppe/Gruppe
* Grupper/Alle
* Alle/Tabel
* Alle/Gruppe
* Alle/Alle

Standardpristolerance for den juridiske enhed er 0 procent, og denne pristolerance anvendes til alle varer og alle konti (Alle, Alle). Du kan ikke slette posten for standardpristolerancen for den juridiske enhed.

Som standard tillades negative prisuoverensstemmelser. Du kan imidlertid ikke angive et negativt tal som pristoleranceprocent. For at spore negative pristoleranceprocenter skal du vælge **Hvis større eller mindre end tolerance** i feltet **Vis ikon for sammenholdelse af enhedspriser** på siden **Kreditorparametre**. Angiv derefter pristoleranceprocenter på siden **Pristolerancer**.

## <a name="set-up-matching-policy-override"></a>Konfigurer overstyring af sammenholdelsespolitik

Gå til **Kreditor > Konfiguration > Konfiguration af fakturasammenholdelse > Sammenholdelsespolitik** for at definere standardposten for feltet Sammenholdelsespolitik for linjer i indkøbsordreformularen. Denne konfiguration er valgfri. Du kan bruge denne form til at konfigurere tovejs-sammenholdelse eller trevejs-sammenholdelse, der skal bruges til varer og leverandører eller kombinationer af varer og leverandører. Disse poster giver dig mulighed for at definere flere detaljerede sammenholdelsespolitikker end den sammenholdelsespolitik for den juridiske enhed, som du har defineret på siden **Kreditorparametre**. Standardlinjesammenholdelsespolitikken for den juridiske enhed gælder for alle linjevarer og -leverandører med undtagelse af elementer, som har en anden sammenholdelsespolitik for linjer angivet på denne side.

Vælg **Niveau for sammenholdelsespolitik** på denne side. Vælg det niveau i hierarkiet for sammenholdelsespolitikker, der skal angives sammenholdelsespolitikker for linjer for.

- **Vare og leverandør** – Angiv sammenholdelsespolitikken for bestemte varer, der er købt hos bestemte leverandører.
- **Vare** – Angiv sammenholdelsespolitikken for bestemte varer, der er købt fra en kreditor, undtagen dem, der er angivet på vare- og kreditorniveau.
- **Kreditor** – Angiv sammenholdelsespolitikken for alle varer, der er købt fra bestemte kreditorer, undtagen dem der er angivet på vare- samt kreditor- og vareniveauer.
  
Følgende hierarki bruges til at bestemme den sammenholdelse, der bruges:
  *  Vare og leverandør
  *  Element
  *  Leverandør
  *  Juridisk enhed
  
## <a name="set-up-invoice-totals-matching-tolerance-for-vendors"></a>Konfigurer fakturatolerancer, der svarer til tolerancer for kreditorer

Gå til **Kreditorer > Konfiguration > Konfiguration af fakturasammenholdelse > Tolerancer for fakturatotaler** for at angive kreditorspecifikke tolerancer for sammenholdelse af fakturatotaler. Beregningen af sammenholdelsen bruger toleranceprocenten for fakturatotaler fra den kreditorkonto, der er angivet som ordrekontoen på kreditorfakturaen. Hvis kreditorkontoen ikke har en angivet toleranceprocent for fakturatotaler, bruges den toleranceprocent for fakturatotaler, der er angivet for den juridiske enhed på siden **Kreditorparametre**.

1. Hvis du vil angive tolerancer for individuelle kreditorer, der tilsidesætter standardtolerancen, skal du vælge en **Kreditorkonto**.
2. Angiv den afvigelsesprocent, som du kan acceptere for denne kreditor.
