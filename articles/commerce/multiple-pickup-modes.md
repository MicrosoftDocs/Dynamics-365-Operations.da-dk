---
title: Aktivere flere leveringsmåder for afhentning af kundeordrer
description: Denne artikel forklarer den funktionalitet i Microsoft Dynamics 365 Commerce, der giver dig mulighed for at oprette kundeordrer til afhentning i en butik.
author: hhainesms
ms.date: 12/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: e4d8883b3dc1c4a0e12bcb00b6441f76d73da92e
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831578"
---
# <a name="enable-multiple-pickup-delivery-modes-for-customer-orders"></a>Aktivere flere leveringsmåder for afhentning af kundeordrer

[!include [banner](includes/banner.md)]


I Microsoft Dynamics 365 Commerce kan organisationer definere flere leveringsmåder, som kunder eller salgsforbindelser kan vælge imellem, når de opretter en ordre, der skal afhentes i en butik. På denne måde kan organisationer stille flere afhentningsmuligheder til rådighed for deres kunder. Mange forhandlere tilbyder nu kunder at vælge mellem afhentning af ordrer i butikken eller ved fortovskanten. Commerce understøtter konfigurationen af disse forskellige leveringsmåder for afhentning. Brugerne kan derefter benytte dem, når de opretter kundeordrer i en hvilken som helst understøttet Commerce-kanal (e-handel, callcenter eller butik).

## <a name="enable-and-configure-pickup-delivery-modes"></a>Aktivere og konfigurere leveringsmåder for afhentning

Funktionen **Understøttelse af flere leveringsmåder for afhentning** til i arbejdsområdet **Funktionsstyring** i Commerce Headquarters er obligatorisk og bør være aktiveret i miljøet.

Hvis du tidligere har defineret en leveringsmåde for afhentning på siden **Handelsparametre** , vises denne tilstand i den aktuelle konfiguration for leveringsmåder til afhentning.

![Leveringsmåder ved afhentning på siden Commerce-parametre.](media/multiplepickupparameter.png)

Du kan definere flere **leveringsmåder til afhentningsgitteret** i **Handelsparametre** > **Kundeordrer**-fanen i oversigtspanelet **Moderne for levering**.  

Felterne **Leveringsmåde ved afhentning** og **Elektronisk leveringsmåde**, og indstillingen **Vis kun fragtmandstilstande for indstillingen forsendelsesordrer** er flyttet til dette oversigtspanel.

Før du kan konfigurere flere leveringsmåder for afhentning, skal du definere leveringsmåderne. På siden **Leveringsmåder** i Commerce Headquarters kan du tilføje de leveringsmåder, der skal betragtes som afhentningsmåder. Sørg for, at al konfiguration er fuldført. Hvis du f.eks. tilbyder afhentning ved fortovskant som leveringsmulighed for dine onlinekunder i bestemte butikker, skal du oprette en ny leveringsmåde til dette formål. Du kan oprette denne leveringsmåde ved hjælp af "afhentning ved fortovskant" som beskrevet. Du vil derefter sikre, at leveringsmåden "afhentning ved fortovskant" knyttes til alle de handelskanaler, der kan tilbyde den, herunder onlinebutikker, der kan tilbyde denne mulighed, og de individuelle butikskanaler, der vil tilbyde denne opfyldelsesmetode. Leveringsmåder skal også knyttes til produkterne. Hvis der i dette eksempel er bestemte produkter, der ikke kan opfyldes ved hjælp af "afhentning ved fortovskant", skal du sikre dig, at disse varer udelades. Når du er færdig med at tilføje nye leveringsmåder, kan du køre jobbet **Behandling af leveringsmåder** for at oprette relationerne mellem leveringsmåde, kanaler og varer. Når jobbet er fuldført, kan du åbne siden **Distributionsplan** i Commerce Headquarters og køre distributionsjobbet **1120** for at sikre, at de relevante Commerce-kanaldatabaser opdateres med den nye konfiguration af leveringsmåden.

![Eksempel på en leveringskonfiguration for afhentning ved fortovskanten.](media/pickupmodes.png)

Når du har defineret flere leveringsmåder for afhentning, skal du føje dem til **Levering gennem afhentning** på siden **Commerce-parametre**. Kør derefter de relevante distributionsjob for at opdatere de relevante Commerce-kanaldatabaser med konfigurationsændringen.

> [!NOTE]
> Bortset fra den eksisterende leveringsmåde for afhentning, der kopieres til **Levering gennem afhentning**, når du aktiverer funktionen **Understøttelse af flere leveringsmåder for afhentning**, skal du konfigurere nye leveringsmåder for alle de øvrige konfigurationer af afhentningsleveringsmåder, som du opretter. Når du føjer leveringsmåder til gitteret **Levering gennem afhentning**, validerer Commerce, om de allerede bruges af aktive åbne salgslinjer. Hvis der findes åbne salgslinjer, vises en fejlmeddelelse. Leveringsmåderne betragtes ikke som leveringsmåder for afhentning, før alle åbne salgslinjer, der bruger dem, er blevet lukket (enten faktureret eller annulleret).


### <a name="e-commerce-site-configurations"></a>Konfigurationer af e-handelswebsted

Når funktionen **Understøttelse af flere leveringsmåder for afhentning** er aktiveret, viser følgende moduler på e-handelssider de nye afhentningsmåder, der er konfigureret:

- Købefelt
- Butiksvælger
- Indkøbskurv
- Afhentningsoplysninger
- Ordrebekræftelse
- Ordredetaljer

Der kræves ikke yderligere trin på e-handelssider for at gøre leveringsmåderne tilgængelige.

## <a name="work-with-multiple-pickup-delivery-modes"></a>Arbejde med flere leveringsmåder for afhentning

Når der er flere tilgængelige leveringsmåder for en kanal, giver det en forbedret oplevelse for kunderne, når de køber produkter, der skal afhentes. 

- I e-handelskanaler kan kunderne vælge en tilgængelig og gyldig leveringsmåde for afhentning. En detailhandler definerer f.eks. to leveringsmåder for afhentning (afhentning i butik og afhentning ved fortovskant), som begge konfigureres i **Levering gennem afhentning**, og som begge er gyldige for ordreopfyldningskanalen og det produkt, som en kunde aktuelt køber. I dette tilfælde kan kunden vælge sin foretrukne afhentningsmåde. Den valgte afhentningsleveringsmåde bliver derefter den leveringsmåde, der er knyttet til salgsordrelinjen, når ordren oprettes i Commerce Headquarters.

    ![Valg af en afhentningsindstilling i e-handel.](media/pickupecommerce.png)

- Hvis der er oprettet en kundeordre for afhentning via POS-programmet i butikskanaler, bliver salgsmedarbejderen bedt om at vælge mellem de tilgængelige afhentningsmåder, der måtte være konfigureret. Hvis der kun findes én gyldig leveringsmåde for kanalen og varen, bliver medarbejderen ikke bedt om at vælge den. I stedet anvendes den tilgængelige leveringsmåde for afhentning automatisk på ordrelinjerne.

    ![Valg af en afhentningsindstilling i POS-programmet.](media/pickuppos.png)

- Når brugere opretter afhentningsordrer i callcenter-kanaler, kan de manuelt vælge en eventuel angivet leveringsmåde for afhentning, der er knyttet til callcenter-kanalen. Systemet validerer derefter, at den valgte afhentningsmåde kan bruges, når den vare, der knyttes til den, bestilles. Når der vælges en leveringsmåde for afhentning i callcenter-kanaler, skal salgsordrelinjerne knyttes til et gyldigt butikslagersted. Hvis der defineres et ikke-butikslagersted på en salgslinje i et callcenter, kan der ikke angives en leveringsmåde for afhentning på den pågældende salgslinje.
- Salgsmedarbejderne kan bruge handlingen **Ordretilbagekaldelse** eller **Ordreopfyldelse** i POS-programmet til at hente en liste over ordrer eller ordrelinjer til afhentning. Hvis en salgsmedarbejder bruger et foruddefineret søgefilter til at vise alle ordrer, der vil blive afhentet i den aktuelle butik, ændres forespørgslerne for at sikre, at søgeresultaterne omfatter alle de berettigede ordrer, der bruger en leveringsmåde for afhentning. POS-brugerne kan også bruge eksisterende filtre til at indsnævre listen over ordrer til en bestemt leveringsmåde for afhentning. De kan f.eks. kun vise ordrer for afhentning ved fortovskant.

    ![Filter til leveringsmåder for afhentning anvendt på en oversigt over tilbagekaldsordrer.](media/pickuprecallorder.png)

## <a name="considerations-for-distributed-order-management"></a>Overvejelser vedrørende fordelt ordrestyring

Funktionerne for [fordelt ordrestyring (DOM)](./dom.md) i Commerce ignorerer alle salgslinjer, der er markeret til afhentning i butikken. Disse funktioner er blevet opdateret for at sikre, at salgslinjer, der er knyttet til konfigurerede leveringsmåder, springer DOM-logikken over, og de omfordeles ikke til et nyt opfyldningslagersted.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
