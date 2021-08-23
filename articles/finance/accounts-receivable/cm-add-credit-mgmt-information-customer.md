---
title: Tilføje kreditstyringsoplysninger for debitorer
description: I dette emne beskrives, hvordan du kan tilføje oplysninger om kreditstyring for en debitor.
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 080b1c4a3887aa5f354743315dc11ffd9f089e73350429d5e08710927f6b2454
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724057"
---
# <a name="add-credit-management-information-for-customers"></a>Tilføje kreditstyringsoplysninger for debitorer

[!include [banner](../includes/banner.md)]

Når du har konfigureret de parametre, der styrer kreditstyring, kan du tilføje flere oplysninger for hver debitor. Disse oplysninger styrer kreditstyringsprocesserne, og de indeholder også yderligere detaljer, der hjælper medlemmer af inkassatorteamet med at administrere debitorer.

## <a name="customer-information"></a>Debitoroplysninger

Du kan tilføje debitoroplysningerne i oversigtspanelet **Kredit** på siden **Alle kunder** (**Debitor \> Kunder \> Alle kunder**).

1. Vælg **Ja** i indstillingen **Ubegrænset kreditgrænse**, hvis kunden ikke skal være begrænset af nogen kreditmaksimumtest.
2. Vælg **Ja** i indstillingen **Udeluk fra kreditstyring** for at udelukke debitoren fra handlinger, der sædvanligvis forekommer under kreditstyring.
3. Vælg kreditstyringsgruppe for debitoren.
4. Hvis du vil beregne kreditmaksimum i debitorens valuta, skal du angive debitorens kreditmaksimum i feltet **Kreditmaksimum i kundens valuta**. Kreditmaksimum i firmavalutaen omregnes ved hjælp af de valutakurser, der er defineret af den valutakurstype for kreditmaksimum, som er valgt i parametrene for kreditstyring.
5. Angiv den dato, hvor debitorens kreditmaksimum sidst blev gennemset af en kreditchef, i feltet **Dato for sidste gennemsyn**.
6. I feltet **Næste planlagte dato for gennemsyn** skal du angive den dato, hvor der er planlagt kreditgennemsyn og -opdatering for debitoren.
7. I feltet **Berettiget kreditmaksimum** skal du angive det højeste kreditmaksimum, der kan tildeles debitorens, baseret på din gennemgang af debitorens kredithistorik. Det berettigede kreditmaksimum kan afvige fra det kreditmaksimum, der vises i oversigtspanelet **Kredit**.
8. Angiv valutaen for det berettigede kreditmaksimum i feltet **Valuta for berettiget kreditmaksimum**.
9. Angiv den dato, hvor kreditmaksimum blev oprettet, i feltet **Dato for berettiget kreditmaksimum**.
10. Angiv status for debitorens kreditkonto i feltet **Status for kreditkonto**.
11. Angiv den årsag, der er knyttet til kontoens status, i feltet **Statusårsag**.
12. Vælg **Ja** i indstillingen **Med agentur** for at angive, at kunden aktuelt er tildelt et kreditagentur. Denne værdi er udelukkende til orientering. Den bruges ikke i nogen kreditstyringsprocesser.
13. Vælg **Ja** i indstillingen **Adkomsthaver** for at angive firmaets adkomst. Denne værdi er udelukkende til orientering. Den bruges ikke i nogen kreditstyringsprocesser.
14. Angiv den dato, hvor kunden første gang startede en forretning, i feltet **Dato for start af virksomhed**. Disse oplysninger bruges, når der oprettes risikovurderinger.
15. Angiv den dato, hvor de første posteringer blev afviklet for debitoren, i feltet **Kunde siden**. Disse oplysninger bruges, når der oprettes risikovurderinger.
16. Angiv noter, som kreditteamet kan bruge til yderligere at evaluere kundens kreditværdighed.

Bemærk, at nogle af de oplysninger, der vises på siden **Kunder**, oprettes af en anden proces:

- Feltet **Udløbsdato for kreditmaksimum** viser den dato, hvor kreditmaksimum udløber. Hvis du ikke indstiller dette felt, udløber kundens kreditmaksimum ikke.
- Feltet **Dato for kreditmaksimum** viser den dato, hvor kreditmaksimum blev oprettet. Dette felt opdateres, når kreditmaksimum reguleres.
- Midlertidige kreditgrænser tilsidesætter kundens kreditmaksimum i en periode. De bruges i stedet for kreditmaksimum til at beregne den samlede kreditgrænse. Disse oplysninger vises kun, hvis der er et aktivt kreditmaksimum. Du kan tilføje midlertidige kreditgrænser gennem reguleringer af kreditmaksimum.
- I feltet **Forsikring og garantier** vises den samlede værdi af forsikring og garantier, der kan øge kundens kreditmaksimum.
- I feltet **Samlet kreditgrænse** vises kundens endelige kreditgrænse. Den samlede kreditgrænse omfatter forsikring og garantier og midlertidige kreditgrænser.

## <a name="temporary-credit-limits"></a>Midlertidige kreditgrænser

Midlertidige kreditgrænser tilsidesætter kundens kreditgrænser i en angivet periode. Du kan tilføje midlertidige kreditgrænser ved hjælp af reguleringer af kreditgrænsen. Med reguleringer af kreditmaksimum kan kreditchefer opdatere kreditmaksimum og udløbsdatoer for en enkelt debitor, en gruppe debitorer eller alle debitorer via en bogføringsproces.

Du kan oprette reguleringsposter for kreditmaksimum på siden **Reguleringer af kreditmaksimum** (**Kreditstyring \> Reguleringer af kreditmaksimum \> Reguleringer af kreditmaksimum**).

## <a name="create-insurance-policies-and-guarantees"></a>Oprette forsikringspolicer og garantier

Du kan oprette en eller flere forsikringspolicer og garantier for hver enkelt debitor. Du kan derefter bruge dem til at beregne den eksponering, dit firma har, når det giver kredit til en kunde. Forsikringspolicer og garantier kan også inkluderes i kreditmaksimum for en kunde.

Du kan oprette forsikringspolicer og garantier på siden **Alle kunder** (**Debitor \> Kunder \> Alle kunder**). Vælg en kunde, og brug derefter handlingsruden under fanen **Kreditstyring** til at vælge **Forsikring og garantier**.

> [!NOTE]
> I følgende procedure skal du vælge en forsikringsgiver eller kautionist i det globale adressekartotek. Derfor skal du sikre dig, at forsikringsgiverne og kautionisterne er føjet til det globale adressekartotek, før du går i gang med denne procedure.

1. Angiv **Garanti** eller **Forsikring** i feltet **Identifikator**.
2. I feltet **Garanti-/forsikringstyper** skal du vælge en af de garanti- eller forsikringstyper, som du tidligere har konfigureret.
3. I feltet **Forsikringsgiver/kautionist** skal du vælge forsikringsgiveren eller kautionisten i det globale adressekartotek. 
4. Hvis du valgte **Forsikring** i feltet **Identifikator**, skal du vælge en af de disponeringstyper, du tidligere har konfigureret, i feltet **Polices dækningstype**. Du kan ikke vælge en policedækningstype for en garanti.
5. Angiv id'et for policen i feltet **Identifikation**. Dette id er normalt et policenummer.
6. Angiv startdatoen for forsikringspolicen eller garantien i feltet **Gælder fra**.
7. Angiv forfaldsdatoen for forsikringspolicen eller garantien i feltet **Udløb**. .
8. Angiv værdien af forsikringspolicen eller garantien i feltet **Værdi**. Denne værdi er policens fulde værdi.
9. Vælg valutaen for policeværdien i feltet **Valuta**. 
10. Angiv en procent mellem **0** og **100** i feltet **Opdater kreditgrænse**. Denne procentsats bliver anvendt på policeværdien, og resultatet bliver brugt til at øge det kreditmaksimum, der bruges i beregningen af kreditmaksimum. Den beregnede værdi vises under **Samlet kreditgrænse, forsikring og garantier** i oversigtspanelet **Kredit** på siden **Kunder**.

    Her er et eksempel:

    - Kreditmaksimum (A) er 100.000.
    - Policeværdien (B) er 50.000.
    - Procentdelen for **Opdater kreditgrænse** (C) er 50,00.
    
    I dette tilfælde er den gældende kreditgrænse 125.000 (= A + \[B × C\]).

11. Marker afkrydsningsfeltet **Medtaget i eksponering** for at reducere den kreditgrænse, der bruges i beregningen af kreditmaksimum, med fulde værdi i policen. Hvis dette afkrydsningsfelt er markeret, vil den værdi, der beregnes, når procenten i **Opdater kreditgrænse** er angivet, ikke blive brugt i beregninger af kreditmaksimum.

    Her er et eksempel:

    - Kreditmaksimum (A) er 100.000.
    - Policeværdien (B) er 50.000.
    - Procentdelen for **Opdater kreditgrænse** (C) er 50,00.

    I dette tilfælde er den gældende kreditgrænse 125.000 (= A + \[B × C\]).
    
    Men hvis du markerer afkrydsningsfeltet **Medtaget i eksponering**, fjernes **Opdater kreditgrænse**-værdien på 50.000 (= 50,00 procent af 100.000), og eksponeringsværdien er 75.000 (= A + \[B × C\] – B).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]