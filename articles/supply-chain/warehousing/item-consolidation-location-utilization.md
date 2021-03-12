---
title: Udnyttelse af varekonsolideringslokation
description: Dette emne indeholder oplysninger om funktioner, der gør det nemt for lagerchefer at få vist og filtrere volumetrisk anvendelse af lokationer på tværs af lagerstedet. Ledere kan vælge lokationer og oprette lagerbevægelse direkte fra siden siden Varekonsolidering for at konsolidere varer og dermed udnytte lagerstedets areal bedre.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6edabc51981d8935672b44e53b453cfbaca9031b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004646"
---
# <a name="item-consolidation---location-utilization"></a>Udnyttelse af varekonsolideringslokation

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om funktioner, der gør det nemt for lagerchefer at få vist og filtrere volumetrisk anvendelse af lokationer på tværs af lagerstedet. Ledere kan vælge lokationer og oprette lagerbevægelse direkte fra siden **Varekonsolidering** for at konsolidere varer og dermed udnytte lagerstedets areal bedre.

## <a name="turn-on-the-features"></a>Slå funktionerne til

Før du kan bruge de funktioner, der er beskrevet i dette emne, skal du aktivere dem i systemet. Administratorer kan bruge arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere statussen for funktionerne og aktivere dem, hvis de skal bruges. Slå begge af følgende funktioner til i den rækkefølge, de angives i. (Begge funktioner er til modulet **Lokationsstyring**).

1. Placeringsstatus for lagersted
2. Udnyttelse af varekonsolideringslokation

## <a name="warehouse-location-status"></a>Placeringsstatus for lagersted

Funktionen *Placeringsstatus for lagersted* føjer fire nye felter til siden **Lokationer** for at spore yderligere oplysninger om den aktuelle status for lokationen:

- **Varenummer** – den vare, der i øjeblikket findes på lokationen. Hvis lokationen indeholder flere varer, er feltet tomt.
- **Dato og klokkeslæt for seneste aktivitet** – tidsstemplet for den sidste lagertransaktion, der blev udført i forhold til lokationen.
- **Forældelsesdato** – den dato, hvor lagerbeholdingen på lokationen blev bragt ind på lagerstedet. Denne dato beregnes på basis af den aldersfordelte dato for nummerpladen. Selvom denne dato er nøjagtig for lokationer, hvor nummerpladen bruges til sporing, men er muligvis ikke nøjagtig for lokationer, hvor nummerpladen ikke bruges til sporing.
- **Lokationsstatus** – statussen for lokationen. Fire værdier er tilgængelige:

    - **Ikke fastlagt** – lokationsprofilen sporer ikke status. Derfor er den aktuelle status ukendt.
    - **Tom** – der er i øjeblikket ingen lagerbeholdning på lokationen.
    - **Pluk** – der er udført udgående transaktioner i forhold til lokationen, efter den sidst var tom.
    - **Lager** – der er kun udført indgående transaktioner, siden den sidst var tom.

Disse felter giver lagerchefer mulighed for at få et bedre overblik over statussen på lagerstedet. De giver også mulighed for mere avanceret rapportering og filtrering.

## <a name="set-up-item-consolidation-and-location-utilization"></a>Konfigurere varekonsolidering og lokationsudnyttelse

I dette afsnit beskrives, hvordan du forbereder dit system til at bruge varekonsolidering og lokationsudnyttelse. Procedurerne bruger eksempelværdier fra standarddemodataene. Hvis du planlægger at arbejde dig gennem det eksempelscenarie, der er angivet senere i dette emne, skal du vælge den juridiske enhed **USMF** (som indeholder standarddemodataene) og oprette de enkelte poster, der er beskrevet i dette afsnit. Hvis du ikke planlægger at arbejde dig gennem eksempelscenariet, kan de værdier, der angives her, betragtes som eksempler på de typer af opsætning, du skal udføre for at kunne bruge funktionerne.

### <a name="released-product"></a>Frigivet produkt

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Gå til feltet **Varenummer**, vælg *M9201*, og åbn detaljesiden.
1. I handlingsruden skal du under fanen **Styr lager** i gruppen **Lager** vælge **Fysiske dimensioner**.
1. Gå til siden **Fysiske dimensioner**, og vælg **Ny** i handlingsruden.

    Der føjes en ny linje til gitteret. Feltet **Varenummer** er foruddefineret.

1. Vælg **hver** i feltet *Enhed*. De resterende felter på linjen angives automatisk.
1. Vælg **Gem**, og luk siden.

### <a name="location-profile"></a>Lokationsprofil

1. Gå til **Lagerstedsstyring \> Konfiguration \> Lagersted \> Lokationsprofiler**.
1. Vælg **PRODUKTION-05** på listen over lokationsprofiler.
1. Vælg **Rediger** i handlingsruden.
1. Gå til oversigtspaneletI **Generelt**, og sørg for, at følgende indstillinger er angivet til *Ja*:

    - Aktivér vare på placering
    - Aktivér placeringsstatus

1. Vælg **Gem**.

    > [!IMPORTANT]
    > Hvis indstillingen **Aktivér vare på lokation** og **Indstillinger for lokationsstatus** allerede er angivet til *Ja*, skal du gå videre til instruktionerne for opsætning af oversigtspanelet **Dimensioner** i trin 10. Hvis indstillingerne ikke allerede er angivet til *Ja*, skal du udføre en konsistenskontrol for modulet **Lokationsstyring**, når du har angivet dem manuelt. I dette tilfælde skal du fortsætte til næste trin.

1. Hvis du vil køre konsistenskontrollen, skal du gå til **Systemadministration \> Periodiske opgaver \> Database \> Konsistenskontrol**.
1. Angiv følgende værdier i dialogboksen **Konsistenskontrol**:

    - **Modul:** *Lokationsstyring*
    - **Kontrollér/ret:** *Kontrol*
    - **Fra dato** – Lad dette felt stå tomt.
    - **Konsistenskontrol af placeringsstatus for lagersted:** Markér dette afkrydsningsfelt.

1. Vælg **OK**.

    > [!TIP]
    > Når konsistenskontrollen er udført, modtager du en besked. Åbn [Handlingscenter](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) for at få vist meddelelsen. Vælg **Meddelelsesdetaljer** for at få vist detaljerne.
    >
    > Hvis meddelelsen for konsistenskontrollen angive, at der er "fundet forkerte statusoplysninger for lokationen for lokation XXXX i lager XX", skal du køre konsistenskontrollen igen. Denne gang skal du angive feltet **Kontrollér/ret** til *Ret fejl*. Få vist meddelelserne for at sikre dig, at der ikke blev fundet fejl.

1. Du skal nu afslutte konfigurationen af lokationsprofilen. Gå tilbage til **Lokationsstyring \> Konfiguration \> Lagersted \> Lokationsprofiler**, vælg lokationsprofilen **PRODUKTION-05**, og vælg derefter **Rediger** i handlingsruden.
1. I oversigtspanelet **Dimensioner** kan du angive følgende værdier:

    - **Volumenudnyttelse i procent:** *100*
    - **Volumetrisk metode, der anvendes til lagerlokation:** *Brug lokationsvolumen*
    - **Lokationens faktiske højde:** *10*
    - **Lokationens faktiske bredde:** *10*
    - **Lokationens faktiske dybde:** *10*
    - **Maks. vægt:** *100*

1. Vælg **Gem**.

### <a name="mobile-device-menu-items"></a>Menupunkter i mobilenhed

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Vælg **Ny** i handlingsruden for at oprette et menupunkt til sortering.
1. Angiv følgende værdier i overskriften:

    - **Navn på menupunkt:** *Regulering i*
    - **Titel:** *Reguler i*
    - **Tilstand:** *Arbejde*
    - **Brug eksisterende arbejde:** *Nej*

1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Arbejdsgang for oprettelse:** *Regulering ind*
    - **Typer af lagerreguleringer:** *Reguler ind*

1. Vælg **Gem**.

### <a name="mobile-device-menu"></a>Menu i mobilenhed

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.
1. Vælg **Lager** på listen over menuer.
1. Vælg **Rediger** i handlingsruden.
1. På listen **Tilgængelig menuer og menupunkter** skal du finde og vælge menupunktet **Reguler ind**.
1. Vælg den højre piletast for at flytte **Reguler ind** til listen **Menustruktur**. På denne måde føjer du det nye menupunkt til den valgte menu.
1. Vælg **Gem**.

### <a name="movement-types"></a>Bevægelsestyper

1. Gå til **Lokationsstyring \> Opsætning \> Lager \> Bevægelsestyper**.
1. I handlingsruden skal du vælge **Ny** og derefter indstille følgende værdier:

    - **Kode for bevægelsestype:** *KONSOLIDER*
    - **Beskrivelse:** *Konsolider lokationer*
    - **Arbejdsklasse-id:** *LagBev*

1. Vælg **Gem**.

## <a name="example-scenario"></a>Eksempelscenario

I følgende scenarie bruges lagerstedsappen på en mobilenhed, når der foretages en *regulering ind* for lager på to lokationer på lagerstedet.

### <a name="add-inventory-to-locations"></a>Føj lager til lagerlokationer

1. Log på mobilenheden som en bruger, der er konfigureret til lagersted *51*.
1. Gå til **Lager \> Reguler ind**.

    Du skal nu angive den første lokationsregulering.

1. I opgaven **Regulering ind** skal du vælge den lokation, som lagerreguleringen skal foretages for. I feltet **LOK** skal du vælge *NP-001*.
1. Bekræft lokationen.
1. Opret et nummerplade-id for den vare, der skal føjes til lokationen. I feltet **NP** skal du angive *NP00101*.
1. Bekræft nummerpladen.
1. Angiv den vare, der skal føjes til nummerpladen. I feltet **ITEM** skal du angive *M9201*.
1. Bekræft varen.
1. Angiv det antal af varen, der bliver tilføjet. I feltet **Antal** skal du angive *10*.
1. Bekræft antallet.

    Du modtager en meddelelse om arbejde fuldført. Du skal nu angive den anden lokationsregulering.

1. I opgaven **Regulering ind** skal du vælge den lokation, som lagerreguleringen skal foretages for. I feltet **LOK** skal du vælge *NP-002*.
1. Bekræft lokationen.
1. Opret et nummerplade-id for den vare, der skal føjes til lokationen. I feltet **NP** skal du angive *NP00201*.
1. Bekræft nummerpladen.
1. Angiv den vare, der skal føjes til nummerpladen. I feltet **ITEM** skal du angive *M9201*.
1. Bekræft varen.
1. Angiv det antal af varen, der bliver tilføjet. I feltet **Antal** skal du angive *15*.
1. Bekræft antallet.

    Du modtager en meddelelse om arbejde fuldført.

1. Vælg menuknappen (kaldes også hamburger eller hamburgerknappen), og vælg derefter **Annuller** for at afslutte opgaven **Regulering i**.

### <a name="consolidate-locations"></a>Konsolidere lokationer

1. Gå til **Lagerstyring \> Periodiske opgaver for \> Varekonsolidering**.
1. Vælg et lagersted, som konsolideringen skal udføres for, i overskriften. Angiv *51* i feltet **Lagersted**.

    Der vises en post for hver lokation, hvor varen *M9201* blev reguleret. Kolonnen **Udnyttelsesgrad** viser den enkelte lokations volumetriske udnyttelse.

1. Hvis du vil konsolidere lagerbeholdning, skal du vælge alle de lokationer, der skal konsolideres, og derefter skal du vælge **Konsolider lager** i handlingsruden.
1. I dialogboksen **Konsolider lager** skal du angive lokationen og bevægelsestypen, der skal bruges til at oprette arbejdet for lagerbevægelsen. Angiv følgende værdier:

    - **Lokation:** *NP-001*
    - **Kode for bevægelsestype:** *KONSOLIDER*

1. Vælg **OK**.
1. Du modtager en meddelelse med oplysninger, der viser det udførte bevægelsesarbejde. Notér dig bevægelsesarbejds-id'et.

### <a name="view-movement-work"></a>Få vist bevægelsesarbejde

1. Gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer**.
1. Få vist det arbejde, der blev oprettet. Brug bevægelsesarbejds-id'et fra lagerkonsolideringen til at filtrere eller søge i arbejdsgitteret.

    I dette scenarie blev der brugt en eksisterende lokation, som har haft en lagerbeholdning, der blev brugt som lagerkonsolideringslokation. Derfor er der kun oprettet ét arbejds-id.

    > [!NOTE]
   > Systemet opretter et arbejds-id for hver flytning, der skal fuldføres. Hvis du angiver en lokation, der allerede indeholder lager, oprettes der kun ét arbejds-id. Hvis du angiver en ny lokation, oprettes der to arbejds-id'er.
