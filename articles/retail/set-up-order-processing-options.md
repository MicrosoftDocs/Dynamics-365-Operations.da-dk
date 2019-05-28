---
title: Konfigurere callcenterkanaler
description: Dette emne indeholder oplysninger om, hvordan du behandler ordrer til callcentre ved hjælp af Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 04/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCROrderParameters, MCRSalesTableOrderHistory, SalesOrderProcessingWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0bfbb763b8ded2a0ce90b66eb686379b1dc92a6d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549353"
---
# <a name="set-up-call-center-channels"></a>Konfigurere callcenter-kanaler

[!include [banner](includes/banner.md)]

Et firma kan definere flere callcenterkanaler i Microsoft Dynamics 365 for Retail. Callcenter-kanaler konfigureres under **Retail** \> **Kanaler** \> **Callcentre** \> **Alle callcentre**, og de er specifikke for en juridisk enhed.

Når der oprettes en ny callcenter-kanal, tildeles den systematisk et driftsenhedsnummer. Da callcentre oprettes som driftsenheder, kan brugere knytte callcenter-kanalen til forskellige Retail-funktioner, f.eks. sortimenter, kataloger og specifikke leveringsmåder.

Der kan konfigureres et standardlagersted for callcenter-kanalen. Derefter, når der oprettes salgsordrer i denne kanal, angives standardlagerstedet automatisk på salgsordrehovedet, medmindre et andet lagersted er defineret for den kunde, der er valgt til salgsordren. I så fald er kundens lagersted angivet som standard.

Brugere skal være knyttet til en callcenter-kanalen for at kunne bruge funktionerne i callcenteret. En salgsordre, som oprettes i Retail af bruger, knyttes automatisk til denne brugers callcenter-kanal. I øjeblikket kan en enkelt bruger ikke knyttes til flere callcenter-kanaler samtidigt.

En profil for e-mail-besked kan også konfigureres for callcenter-kanalen. Profilen definerer det sæt af e-mail-skabeloner, der bruges, når der sendes e-mail til kunder, der kan afgiver ordrer gennem callcenter-kanalen. E-mail-udløserne kan konfigureres i forhold til systemhændelser som f.eks. indgivelse eller forsendelse af ordrer.

Før salget kan behandles korrekt via en callcenter-kanal, skal du angive de rette [betalingsmetoder](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-payments) og leveringsmåder for kanalen.

På niveauet for callcenter-kanalen kan du definere andre standardværdier i relation til de økonomiske dimensioner, som knyttes til de ordrer, der oprettes i den pågældende kanal.

## <a name="options-for-order-processing-behavior"></a>Indstillinger for ordrebehandling

Tre indstillinger i konfigurationen af et callcenter har stor indvirkning på de funktioner, der er tilgængelige for salgsordrer, som oprettes i forhold til det pågældende callcenter: **Aktivér ordrefuldførelse**, **Aktivér direkte salg**, og **Aktivér ordrepriskontrol**.

### <a name="enable-order-completion"></a>Aktivér ordrefuldførelse

Indstillingen **Aktivér ordrefuldførelse** for callcenter-kanalen har en større effekt på ordrebehandlingens flow af de salgsordrer, som er angivet for den pågældende kanal. Når indstillingen er aktiveret, skal alle salgsordrer opfylde en række valideringsregler, før de kan bekræftes. Du kan køre disse regler ved at vælge knappen **Fuldført**, der er tilføjet i handlingsruden på siden for salgsordren. Alle salgsordrer, der oprettes, når indstillingen **Aktivér ordrefuldførelse** er aktiveret, skal gennemgå processen for ordrefuldførelse. Denne proces gennemtvinger indhentning af betaling og følger valideringslogikken for betalingen. Ud over indhentning af betaling kan ordreindgivelsesprocessen udløse [svindelkontroller](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts), som konfigureres i systemet. Ordrer, der ikke består betalings- eller svindelvalideringer, sættes i kø og kan ikke frigives til yderligere behandling (f.eks. pluk eller levering), indtil det problem, der forårsagede spærringen, er løst.

Når indstillingen **Aktivér ordrefuldførelse** er aktiveret for callcenter-kanalen, der er angivet linjeelementer på en salgsordre, og kanalens bruger forsøger at lukke eller forlade salgsordreformen uden først at markere **Fuldført**, håndhæver systemet ordrefuldførelsesprocessen ved at åbne siden for opsummering af salgsordrer og kræver, at brugeren indsender ordren korrekt. Hvis ordren ikke kan sendes korrekt sammen med betalingen, kan brugeren anvende funktionen for [ordrekø](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) for at sætte ordren i kø. Hvis brugeren forsøger at annullere ordren, skal han eller hun annullere den korrekt ved hjælp af funktionen Annuller eller Slet, afhængigt af den funktion brugerens sikkerhedsindstillinger tillader.

Hvis indstillingen **Aktivér ordrefuldførelse** er aktiveret for callcenter-kanalen, spores feltet **Betalingsstatus** på ordren. Systemet beregner **Betalingsstatus**, når salgsordren er afgivet. Kun ordrer, der har en godkendt betalingsstatus, får lov til at gå gennem systemet til de øvrige trin i ordrebehandlingen, f.eks. pluk og levering. Hvis betalinger bliver afvist, aktiveres flaget **Udfør ikke behandling** i den detaljerede ordrestatus, og ordren sættes i kø, indtil betalingsproblemet er løst.

Hvis indstillingen **Aktivér ordrefuldførelse** er aktiveret, når brugere opretter salgsordrer, og tilstanden for indtastning af linjeelementer er aktiveret, vil feltet **Kilde** være tilgængeligt i det overordnede salgsordrehoved. Feltet **Kilde** bruges til at registrere en [katalogkildekode](https://docs.microsoft.com/dynamics365/unified-operations/retail/call-center-catalogs) i forbindelse med et salgscenarie med direkte marketing. Denne kode kan derefter udløse specialpriser og kampagner.

Selvom indstillingen **Aktivér ordrefuldførelse** er deaktiveret, kan brugerne stadig anvende en kildekode til en salgsordre. De skal dog først åbne salgsordrehovedets detaljer for at få adgang til feltet **Kilde**. Med andre ord kræves der nogle ekstra klik. Samme funktionsmåde gælder for funktioner som f.eks. Forsendelse fuldført og Fremskyndede ordrer. Disse funktioner er tilgængelige for alle ordrer, der er oprettet i callcenteret. Når indstillingen **Aktivér ordrefuldførelse** er slået til, kan brugere dog se konfigurationen af disse funktioner på salgshovedet, mens de er i linjepostvisning. De behøver ikke dykke ned i salgsordrehovedets detaljer for at finde de relevante indstillinger og felter.

### <a name="enable-direct-selling"></a>Aktivere direkte salg

Hvis indstillingen **Aktivér direkte salg** er aktiveret for callcenter-kanalen, kan brugerne udnytte fordelene ved funktionerne for mersalg og tillægssalg i Retail. I så fald vises pop op-vinduer under ordreindtastningen med forslag til andre produkter, som callcenter-brugeren kan tilbyde sin kunde. De produkter, der foreslås, er baseret på det produkt, der netop er blevet bestilt på salgsordrelinjen. Forslag til mersalg og tillægsslag konfigureres i øjeblikket på vareniveauet for produkter eller kataloger. Hvis indstillingen **Aktivér direkte salg** er deaktiveret for callcenter-kanalen, vises der ikke pop op-vinduer under ordreindtastningen, selvom der er defineret et gyldigt mersalg eller tillægssalg for den vare, der bestilles.

Når indstillingen **Aktivér direkte salg** er aktiveret, er funktionerne for scripts og billeder på siden for salgsordreindtastningen også aktiveret. I så fald findes der et informationspanel til højre på siden under ordreindtastningen. Dette panel kan vise scripts, der er relateret til den generiske ordreindtastningsproces, den anvendte kildekode for kataloget eller scripts i relation til de varer, som bliver bestilt. Derudover kan billedpanelet vise et produktbillede for de varer, som bliver bestilt, hvis der er defineret et billede for varen i produktopsætningen.

### <a name="enable-order-price-control"></a>Aktivér ordrepriskontrol

Når indstillingen **Aktivér ordrepriskontrol** er aktiveret, kan kun autoriserede brugere ændre salgsprisen for en vare under ordreindtastningen. Ændringerne skal ligge inden for de angivne tolerancer. Brugere, der ikke har den rette godkendelse, skal i stedet indsende en anmodning om en prisændring. Anmodningen behandles derefter via systemets arbejdsgange for gennemsyn og godkendelse.

## <a name="channel-users"></a>Kanalbrugere

Når du definerer callcenter-kanalen, skal du knytte kanalens brugere til callcenteret. Ellers kan callcenteret ikke bruges i systemet. Når brugere logger på Retail og indtaster salgsordrer eller returordrer på en side, der er relateret til ordreindtastning, valideres deres bruger-id'er ud fra konfigurationen af callcenter-kanalen. Hvis en bruger er knyttet til en bestemt callcenter-kanal, arver de ordrer, som brugeren opretter, egenskaberne og standardværdierne for den pågældende kanal.

Som standard er flaget **Detailsalg** aktiveret på salgsordrehovedet for alle ordrer, som callcenterets brugere opretter. Ordrerne kan derefter udnytte systemets detailspecifikke pris- og kampagnefunktioner.

Brugere, som ikke er sammenkædet med en callcenterkanal, bruger standardordreindtastningsfunktionerne i Microsoft Dynamics 365 for Finance and Operations. De ordrer, som disse brugere indtaster via salgsordreformularen, registreres ikke systematisk som ordrer i Retail. Derudover vil disse ordrer, der er indgivet af disse brugere, ikke være omfattet af behandlingsreglerne for ordrefuldførelse, logikken for detailpriser eller andre valideringer, som kan defineres i konfigurationen af callcenter-kanalen eller callcenterets systemparametre.

Når du er færdig med at konfigurere callcenter-kanalen og definere kanalens brugere, og når du vil sikre den ønskede systemadfærd, skal du kontrollere, at alle nødvendige parametre for callcenteret er defineret under **Retail** \> **Konfiguration af kanal** \> **Callcenter-konfiguration** \> **Callcenter-parametre**. Sørg for, at der også er defineret relaterede nummerserier.
