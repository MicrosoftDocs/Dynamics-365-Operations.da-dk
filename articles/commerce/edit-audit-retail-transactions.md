---
title: Redigere og overvåge transaktioner i detailbutik
description: I dette emne beskrives funktionerne til redigering og overvågning af butiksposteringer.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 97211ee36dbaa704d3a967e9b742ff1cae708707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004383"
---
# <a name="edit-and-audit-retail-store-transactions"></a>Redigere og overvåge transaktioner i detailbutik

[!include [banner](includes/banner.md)]



Dynamics 365 Commerce-kunder bruger både førsteparts- og tredjeparts-POS-programmer. Med førsteparts-POS-programmet trækkes butiksposteringer ind i Headquarters fra kanalerne via en batchproces. Med tredjepartsprogrammer trækkes transaktionerne ind i Headquarters via integration. I begge tilfælde skal der, efter at transaktionerne er trukket ind i Headquarters, udføres en konsistenskontrolproces, der kører flere valideringer på transaktionerne, så kun transaktioner, der er valideret korrekt, trækkes ind i den opgørelse, der bogføres i Headquarters. 

Commerce-transaktioner valideres ikke korrekt af forskellige årsager. For eksempel kan en fejl i integrationskoden eller en fejl i POS-programmet medføre inkonsistente data, eller en brugerfejl, f.eks. sletning af et produkt, efter at det er synkroniseret til kanalen, eller afslutning af en regnskabsperiode uden bogføring af transaktioner for den pågældende periode, kan medføre inkonsistente data.

Selvom disse transaktioner markeres og udelukkes fra opgørelserne, kan transaktionerne forstyrre en kundes daglige proces med at bogføre dagligt salg i finans.

I Commerce kan du redigere de specifikke transaktioner, der ikke er valideret korrekt, samtidig med at du bevarer overvågningen af alle ændringerne. 

## <a name="edit-and-audit-transactions"></a>Redigere og overvåge transaktioner

I Retail version 10.0.5 er cash and carry-transaktioner, f.eks. salg og returneringer, de eneste posteringer, der kan redigeres. Redigering af kundeordrer eller onlineordrer understøttes ikke. I Retail version 10.0.6 og nyere understøttes redigering af kassestyringstransaktioner også.

1. Installer tilføjelsesprogrammet Dynamics Excel.

2. Gå til arbejdsområdet **Butiksregnskab**. Feltet **Transaktionsvalideringsfejl** giver en forhåndsfiltreret visning af den transaktionsformular, hvor der opstod fejl ved én eller flere valideringsregler.
 
3. Åbn formularen. Klik på den post, hvor valideringen mislykkedes, klik på **Office-tilføjelsesprogram**, og klik derefter på **Rediger den valgte transaktion**. Der åbnes en Excel-fil med detaljerne om den valgte transaktion, med følgende regneark:

    - Linjer: Dette regneark indeholder hoved- og produktlinjerne og relaterede data for transaktionen.
    - Betalinger: Dette regneark indeholder oplysningerne om transaktionens betalingslinjer.
    - Rabatter: Dette regneark indeholder de rabatrelaterede detaljer for transaktionen.
    - Moms: Dette regneark indeholder de momsrelaterede detaljer for transaktionen.
    - Gebyrer: Dette regneark indeholder de gebyrrelaterede data for transaktionen.

4. I Excel-filen redigerer du de relevante felter og overfører derefter dataene tilbage til Headquarters ved hjælp af publiceringsfunktionen i Dynamics Excel-tilføjelsesprogrammet. Når de er publiceret, afspejles ændringerne i systemet. Under publiceringen sker der ingen validering af de ændringer, brugerne foretager.

5. Du kan få vist et komplet revisionsspor for ændringerne ved at klikke på **Vis revisionsspor** i hovedet på **detailtransaktionen** for ændringerne på hovedniveau og i den relevante sektion og post på den relevante transaktionsside. Alle ændringer i forbindelse med salgslinjer vil f.eks. være synlige på siden **Salgstransaktioner**, ændringer vedrørende betalinger vil være synlige på siden **Betalingstransaktioner** osv. De revisionsoplysninger, der vedligeholdes for ændringerne, er følgende.

   - Dato og klokkeslæt for ændring
   - Felt 
   - Gammel værdi
   - Ny værdi
   - Ændret af

6. Når dine ændringer er foretaget og publiceret, skal du køre indstillingen **Valider butiksposteringer** igen for at validere, at de ændringer, du har foretaget, er konsistente og gyldige.

> [!NOTE]
> Du kan kun redigere transaktioner, hvor valideringen mislykkedes. Hvis du vil redigere transaktioner, der har bestået valideringen, skal du ændre valideringsstatus for den transaktion, du vil ændre, til **Fejl** eller **Ingen**, og derefter kan du redigere den. 


## <a name="bulk-edit-transactions"></a>Masseredigere transaktioner

I Retail version 10.0.6 og nyere understøttes muligheden for at masseredigere transaktioner på opgørelsesniveau. 

1. Brug Excel-tilføjelsesprogrammet til at åbne en opgørelse, der har transaktioner, du vil redigere ved brug af trin 1-3 ovenfor.

2. Vælg en af indstillingerne nedenfor.

    - **Rediger cash and carry-transaktioner**. Denne indstilling giver dig mulighed for at redigere alle de cash and carry-transaktioner, der indgår i opgørelsen. Følgende Excel-regneark er tilgængelige.
    
       - **Transaktion**: Dette regneark indeholder alle oplysningerne på hovedniveau for salgstransaktionerne.
       - **Salgstransaktion**: Dette regneark indeholder alle oplysningerne på linjeniveau for salgstransaktionerne.
       - **Betalingstransaktioner**: Dette regneark indeholder alle betalingslinjeoplysningerne for salgstransaktionerne.
       - **Rabattransaktioner**: Dette regneark indeholder alle rabatlinjeoplysningerne for salgstransaktionerne.
       - **Momstransaktioner**: Dette regneark indeholder alle momsoplysningerne for salgstransaktionerne.
       - **Gebyrtransaktioner**: Dette regneark indeholder alle rabatlinjeoplysningerne for salgstransaktionerne.

    - **Rediger kassestyringstransaktioner**. Denne indstilling giver dig mulighed for at redigere alle de kassestyringstransaktioner, der indgår i opgørelsen. Følgende Excel-regneark er tilgængelige.
     
       - **Transaktion**: Dette regneark indeholder alle oplysningerne på hovedniveau for kassestyringstransaktionerne.
       - **Transaktioner med bankbetalingsmiddel**: Dette regneark indeholder alle oplysninger om transaktioner med indsættelse i bank.
       - **Betalingsmiddeltransaktioner lagt i pengeskab**: Dette regneark indeholder alle oplysninger om transaktioner med betalingsmidler lagt i pengeskab.
       - **Kasseoptælling**: Dette regneark indeholder alle oplysninger om transaktioner med kasseoptælling.
       - **Indtægts-/udgiftstransaktion**: Dette regneark indeholder alle oplysninger om indtægts-/udgiftstransaktionslinjer.
       - **Betalingstransaktioner**: Dette regneark indeholder alle betalingsrelaterede oplysninger for handlingen **Betal faktura** samt indtægts-/udgiftstransaktionen.

3.  Valideringer udføres ikke, når du publicerer masseredigerede transaktioner. Du skal sikre dig, at alle dine redigeringer er nøjagtige, og at pålideligheden af dataene bevares på tværs af alle regneark. Hvis du f.eks. vil ændre posteringsdatoen for at administrere de scenarier, hvor regnskabs-eller lagerperioden for de åbne transaktioner er lukket, skal du ændre datoen på alle de Excel-regneark, der indeholder kolonnen **Forretningsdato**. Hvis du vil validere transaktioner, når de er blevet redigeret, kan du bruge **Valider transaktioner igen** på siden **Opgørelser**.
