---
title: Oversigt over bogføringsprofiler
description: Denne artikel forklarer, hvordan posteringsprofiler bruges i Microsoft Dynamics 365-apps.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7ef3be13e82ff3722fc81247b5cd581b0b571b0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876118"
---
# <a name="posting-profiles-overview"></a>Oversigt over posteringsprofiler

I Finans- og driftsapps bruges udtrykket *posteringsprofiler* til at beskrive de konfigurationer, der styrer, hvordan konto for reskontro konverteres til hovedkonti, så de kan bruges i transaktioner, der bogføres i finansmodulet. De styrer f.eks., hvordan kunden konverteres til en hovedkonto i Debitor, når en faktura bogføres.

Nogle moduler og funktioner har en side, der indeholder ordene "posteringsprofil" i navnet (f.eks. **Debitorposteringsprofil** og **Kreditorposteringsprofil**). Visse moduler indeholder desuden flere indstillinger til konfiguration af finanskontering for transaktioner, der genereres fra reskontroen. I modulet **Produktionsstyring** kan du f.eks. konfigurere posteringen efter produktionsgruppe, ressource eller ressourcegruppe.

Bemærk, at der findes et alternativ til posteringsprofiler i mange transaktionstyper: bogføringsdefinitioner. Til understøttede dokumenter kan du bruge bogføringsdefinitioner i stedet for posteringsprofiler til at klassificere hovedkonti og økonomiske dimensioner på regnskabsposter. Hvis du planlægger at bruge behæftelser eller forudgående behæftelser, skal der angives en bogføringsdefinition for at definere kontiene til regnskabsposterne.

Før du kan konfigurere posteringsprofiler, bogføringsdefinitioner eller siden **Konti til automatiske posteringer**, skal du konfigurere kontoplanen på siden **Finans** i den juridiske enhed, du vil konfigurere.

## <a name="posting-types"></a>Bogføringstyper

I Finans- og driftsapps bruges en bogføringstype til at definere en generel kategori for en debitering eller kreditering. Denne kategori er uafhængig af hovedkontoen i Finans. Der er bogføringstyper for de enkelte debiteringer eller krediteringer i Finans.

Et enkelt bilag kan have en eller flere bogføringstyper. En transaktion, der bogføres via en finanskladde, hvor kontoen og modkontoen angives til **Finans**, vil f.eks. have bogføringstypen **Finans** for både debet og kredit. Modsat vil en kreditorfaktura have flere bogføringstyper. Disse bogføringstyper omfatter én linje for kreditorsaldoen og yderligere linjer til modposteringen, f.eks. **Finanskladde**.

Du kan se bogføringstypen i feltet **Bogføringstype** under fanen **Generelt** på siden **Posteringer på bilag**.

> [!TIP]
> Du kan bruge værktøjslinjen **Tilpasning** til at føje feltet **Bogføringstype** til gitteret under fanen **Oversigt** eller flytte det. På den måde kan du gøre det nemmere at få adgang til eller se dette felt, når du får vist bilag.

## <a name="detail-settings-for-a-posting-profile"></a>Detailindstillinger for en posteringsprofil 

Når du konfigurerer posteringsprofiler, definerer feltet **Kontokode** niveauet for indstillingen. Der er følgende indstillinger: **Tabel**, **Gruppe** og **Alle**. Sammenholdelsen stopper efter den første match, og ordren går fra det mest specifikke niveau til det mindst specifikke niveau. Selvom feltet **Kontokode** kan have et lidt andet navn i nogle tilfælde, forbliver feltets funktionalitet og funktion den samme. Lagerposteringsprofilen indeholder f.eks. feltet **Varekode** og **Kontokode**. Begge felter har værdier som **Tabel**, **Gruppe** og **Alle**.

Hvis du lader feltet **Hovedkonto** være tomt for en posteringsprofil, og du ikke har konfigureret en hovedkonto på siden **Konti til automatisk postering** på en modulspecifik eller funktionsspecifik side, modtager du en fejlmeddelelse, når du bogfører en transaktion, der bruger bogføringstypen. Meddelelsen vil typisk være "Kontoen til \[Bogføringstype\] findes ikke".

### <a name="table-value"></a>Tabelværdi

**Tabel**-værdien refererer til den masterpost, der er knyttet til posteringsprofilen. Hver tabelpost er specifik for én værdi. Du angiver den værdi i det felt, der vises efter feltet **Kontokode**. Dette felt kaldes typisk **Konto** eller **Konto-/gruppenummer**. Det nøjagtige navn varierer, afhængigt af den side det vises på.

Hvis du f.eks. arbejder med en debitorposteringsprofil, repræsenterer **Tabel**-værdien en bestemt debitor. Hvis du vælger **Tabel** i feltet **Kontokode**, skal du derfor vælge kundenummeret i feltet **Konto/gruppenummer**.

**Tabel**-værdien repræsenterer den mest specifikke posttype. Systemet bruger altid denne værdi, også selvom du har konfigureret en anden post, hvor værdien **Gruppe** eller **Alle** er valgt. Denne værdi tilsidesætter også eventuelle værdier, du har oprettet som standardværdier på siden **Konti til automatiske posteringer**.

Du frarådes at bruge **Tabel**-værdien som den primære mekanisme til administration af posteringsprofiler, da datakvalitetsproblemer kan forekomme, hvis der vedligeholdes en separat posteringsprofil for hver masterdatapost. Det er også vanskeligt at vedligeholde og afstemme en separat posteringsprofil for hver masterdatapost. Denne værdi skal i stedet bruges til at administrere undtagelser i posteringsprofilerne.

### <a name="group-value"></a>Gruppeværdi

**Gruppe**-værdien henviser til den grupperingspost, der understøttes af den masterpost, der er tilknyttet posteringsprofilen. Hver gruppepost er specifik for én værdi. Du angiver den værdi i det felt, der vises efter feltet **Kontokode**. Dette felt kaldes typisk **Konto** eller **Konto-/gruppenummer**. Det nøjagtige navn varierer, afhængigt af den side det vises på.

**Gruppe**-værdien kræver, at du først konfigurerer en gruppe og sammenkæder den med en eller flere poster for kontoen. **Gruppe**-værdien er mindre specifik end **Tabel**-værdien, men mere specifik end værdien **Alle**. Hvis der ikke er konfigureret en post for en tabel, forsøger systemet at finde en post for den gruppe, som posten tilhører.

Hvis du f.eks. arbejder med en debitorposteringsprofil, og du vælger **Gruppe** i feltet **Kontokode**, skal du vælge en debitorgruppe i feltet **Konto-/gruppenummer**. Du skal foruddefinere debitorgrupperne på siden **Debitorgruppe**, og du skal angive en debitorgruppe, når du opretter en debitor.

Hvis du skal spore flere hovedkonti for en bestemt bogføringstype, anbefales det, at du bruger **Gruppe**-værdien. Du kan f.eks. have tre hovedkonti for debitorhandel: en til almindelige kunder, en til medarbejdere og en til internt salg. I dette tilfælde anbefales det, at du opretter tre debitorgrupper for at segmentere kunderne. Tilknyt derefter hver debitorgruppe til den korrekte hovedkonto i debitorens posteringsprofil. I følgende tabel vises de tre debitorgrupper for dette eksempel.

| Debitorgruppe | Navn | Beskrivelse |
|----------------|------|-------------|
| EXT | Ekstern kunde | Denne gruppe bruges til alle eksterne standardkunder. |
| EMP | Medarbejdere | Denne gruppe bruges til alle medarbejdere, der foretager køb fra din organisation. |
| INT | Internt salg | Denne gruppe bruges til alle interne debitorkonti, der bruges til integration af salgs- og indkøbsordrer. |

Du skal derefter oprette tre linjer i posteringsprofilen. På hver linje skal du vælge **Gruppe**-værdien og den relaterede hovedkonto.

### <a name="all-value"></a>Værdien Alle

Værdien **Alle** angiver, at indstillingerne gælder for alle poster. Hvis du vælger værdien **Alle** i feltet **Kontokode**, er feltet **Konto-/gruppenummer** ikke tilgængeligt, og du kan ikke vælge en bestemt post, som konfigurationen skal anvendes på.

Værdien **Alle** er den mindst specifikke værdi. Den bruges kun, hvis systemet ikke kan finde et match for **Tabel-** eller **Gruppe**-værdien. Du skal vælge værdien **Alle**, når du kun har én hovedkonto til en bestemt bogføringstype.

Når du f.eks. arbejder med en debitorposteringsprofil, gælder de hovedkonti, du angiver for alle andre debitorer og debitorgrupper, der ikke har en post for en bestemt tabel (kunde) eller gruppe (kundegruppe).

### <a name="category"></a>Kategori

Lagerposteringsprofiler har en ekstra værdi, der er specifik for salgskategorien eller indkøbskategorien. Denne værdi svarer til **Tabel**-værdien, da den kun gælder for en bestemt salgs- eller indkøbskategori.

### <a name="default-value"></a>Standardværdi

Hvis du ikke opretter en post for en bogføringstype i en posteringsprofil, hvor feltet **Kontokode** er angivet til **Alle**, og systemet ikke kan finde en tilsvarende posteringsprofilpost for værdien **Gruppe** eller **Tabel**, går systemet tilbage til den standardværdi, der kan angives på siden **Konti til automatiske posteringer**. Yderligere oplysninger finder du under [Konti til automatiske posteringer](accounts-for-auto-transactions.md).

## <a name="clearing-accounts"></a>Clearingkonto

Udtrykket *clearingkonto* bruges ofte i regnskaber. Nogle bogføringstyper i Microsoft Dynamics 365-apps er clearingkonti. Det vil sige, at saldoen på kontoen cleares eller tilbageføres, når der bogføres en anden transaktion. Når du f.eks. bogfører en produktkvittering for en indkøbsordre, bogføres summen af forkalkulerede omkostninger for produkterne plus moms og eventuelle gebyrer på indkøbsordrelinjerne til bogføringstypen for købsperiodisering som et passiv. Senere, når du fakturerer indkøbsordren, tilbageføres saldoen fra bogføringstypen for købsperiodisering og flyttes til samhandelskontoen Kreditor.

## <a name="additional-resources"></a>Yderligere ressourcer

Mange moduler i Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Project Operations har en posteringsprofil eller yderligere konfigurationer, der styrer, hvordan bogføringen til finansmodulet fungerer. Du kan bruge følgende emner til at få mere at vide om posteringsprofiler og bogføringsopsætninger i de enkelte moduler:

- [Konti til automatisk posteringer](accounts-for-auto-transactions.md)
- [Kreditorbogføring](accts-payble-posting.md)
- [Debitorbogføring](accts-recvble-posting.md)
- [Bogføring af Aktivleasing](../asset-leasing/set-up-lease-posting-accts.md)
- Bogføring af aktivstyring (kommer snart)
- Kontant- og bankstyring (kommer snart)
- Bogføringskonti til værdiregulering af valuta (kommer snart)
- Bogføring af udgiftsstyring (kommer snart)
- [Posteringsprofil for anlægsaktiver](../fixed-assets/tasks/set-up-fixed-asset-posting-profiles.md)
- Bogføring af mellemregninger (kommer snart)
- Lagerposteringsprofil (kommer snart)
- [Bogføring af landingsomkostninger](../../supply-chain/landed-cost/costing-parameters-setup.md)
- [Oversigt over bogføringsdefinitioner](posting-definitions.md)
- Bogføring af produktionsstyring (kommer snart)
- Bogføring af projektstyring og regnskab (kommer snart)
- Bogføring af servicestyring (kommer snart)
- Momsbogføring (kommer snart)
- Bogføring af tid og fremmøde (kommer snart)
- Bogføring af transportstyring (kommer snart)
- Posteringsprofiler for rabatstyring (kommer snart)
