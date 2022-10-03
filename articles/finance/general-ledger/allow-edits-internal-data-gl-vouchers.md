---
title: Tillad redigering af interne data på finansbilag
description: Denne artikel indeholder oplysninger om, hvordan du redigerer interne data på finansbilag.
author: kweekley
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 6e346c6ff881d3a33743196b45247493fd19ed1d
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573245"
---
# <a name="allow-edits-to-internal-data-on-general-ledger-vouchers"></a>Tillad redigering af interne data på finansbilag

[!include[banner](../includes/banner.md)]


Når du bogfører regnskabsposter i Finans, bruges feltet **Beskrivelse** ofte til at gemme interne notater eller dokumentation. Hvis oplysningerne ikke er korrekte, kan det medføre forvirring og gøre lukningen af perioder mere besværlig. Denne funktion giver regnskabschefen eller den regnskabsansvarlige mulighed for at rette fejl ved at redigere feltet **Beskrivelse** på bogførte bilag i finansmodulet.

Ændringer af bogførte bilag i finansmodulet er begrænset til data, der er interne. Denne funktion giver dig aldrig mulighed for at redigere data som f.eks. beløb, bogføringsdatoer, finanskonti og transaktionsvalutaen. Ændringer i disse data påvirker den eksterne rapportering af regnskaber og skal kun ske via nye finansbilag.

> [!NOTE]
> For Dynamics 365 Finance version 10.0.29 er denne funktion begrænset til at redigere i feltet **Beskrivelse**.

## <a name="edit-internal-data-on-general-ledger-vouchers"></a>Redigere interne data på finansbilag

Før interne data på bilag i finansmodulet kan redigeres, skal du aktivere funktionen **Tillad redigering af interne data på finansbilag** i arbejdsområdet **Funktionsstyring**.
Når funktionen er aktiveret, skal den bruger, der skal redigere bogførte bilag, tildeles rollen Regnskabschef eller Regnskabsansvarlig. Du kan også føje rettigheder til andre roller ved at tilpasse sikkerhedsrollerne.

Redigeringsprocessen er kun tilladt fra siden Poster på bilag.

1. Gå til **Finans** > **Forespørgsler og rapporter** > **Poster på bilag**.
2. Angiv søgekriterier for at vælge bilag i dialogboksen **SysQuery**.
3. Marker linjerne for de bilag, du vil redigere, og vælg derefter **Rediger bilag** > **Rediger interne bilagsdata**.

    [![Siden Poster på bilag.](./media/voucher-transactions-page.png)](./media/voucher-transactions-page.png)
    
På siden **Rediger interne bilagsdata** vises følgende data for hver linje, du har valgt:
  
  - Finanskonto
  - Kontonavn
  - Bilag
  - Aktuel beskrivelse
  - Ny beskrivelse

    [![Kladdebilag.](./media/edit-internal-voucher-data.png)](./media/edit-internal-voucher-data.png)
    
> [!NOTE]
> Det er kun feltet **Ny beskrivelse**, der kan redigeres. Værdien svarer som standard til værdien i feltet **Aktuel beskrivelse**, så du hurtigt kan rette mindre fejl i beskrivelsen.

4. Rediger feltet **Ny beskrivelse** i hver række, eller slet beskrivelsen på hver række.

   Hvis der skal opdateres flere rækker med samme værdi, kan du også benytte følgende fremgangsmåde:

      1. Markér de rækker, der skal redigeres, og vælg derefter **Masseopdater valgte poster**.
      2. Vælg det felt, du vil redigere, i **Felt, der skal redigeres**. Aktuelt indeholder opslaget kun feltet **Ny beskrivelse**.
      3. Indtast en ny beskrivelse i feltet **Ny værdi**.
      4. Vælg **Opdater**. Alle de valgte poster opdateres med den nye værdi.

      [![Dialogboksen Masseopdater de valgte poster.](./media/bulk-update-selected-records.png)](./media/bulk-update-selected-records.png)
    
5. Angiv en note for at forklare, hvorfor redigeringen blev foretaget, i feltet **Årsag til redigering**. Denne note vises på siden **Revisionsspor for bilagsredigeringer**.

   Der kan foretages flere redigeringer af samme bilag, og hver enkelt redigering spores.

## <a name="audit-trail-of-voucher-edits"></a>Revisionsspor for bilagsredigeringer

Et revisionsspor vedligeholdes specifikt for at spore de ændringer, der foretages via denne funktion. Du kan få adgang til revisionssporet for bilagsredigeringer på to måder:

  - Gå til **Finans** > **Forespørgsler og rapporter** > **Poster på bilag**. På siden **Bilagsforespørgler** skal du vælge **Rediger bilag** > **Revisionsspor for bilagsredigeringer**. Revisionssporet vises kun for den valgte bilagspost. 
   
    Når du åbner en forespørgsel på denne måde, kan du fokusere på alle redigeringer, der er foretaget i en enkelt bilagspost.
  
  - Gå til **Finans** > **Periodiske opgaver** > **Revisionsspor for bilagsredigeringer**. Angiv kriterier for at angive de bilag, du vil have vist revisionssporet til redigeringer for, i dialogboksen. Hvis du vil have vist revisionssporet for alle bilag, skal du lade kriterierne stå tomme og vælge **OK**. 
    
    Ved at åbne forespørgsler på denne måde kan du filtrere efter redigeringer, der er foretaget på en bestemt dato eller af en bestemt bruger.

Siden **Revisionsspor for redigeringer** viser følgende oplysninger:

- **Dato og klokkeslæt for oprettelse** – Dato og klokkeslæt for redigeringen.
- **Årsag til redigering** – Årsagen, som brugeren har angivet for redigeringen.
- **Oprettet af** – Den bruger, der foretog redigeringen.

Hvis du vil have vist detaljerne i hvert revisionsspor, skal du rulle ned på værdien **Dato og klokkeslæt for oprettelse**. På siden **Få vist redigerede bilagsegenskaber** vises de samme oplysninger som den oprindelige redigeringsside, herunder den tidligere beskrivelse og den opdaterede beskrivelse.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
