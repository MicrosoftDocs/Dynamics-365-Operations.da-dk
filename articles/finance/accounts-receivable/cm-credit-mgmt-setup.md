---
title: Konfiguration af kreditstyringsparametre
description: Denne artikel beskriver de indstillinger, du kan bruge til at konfigurere kreditstyring, så det opfylder virksomhedens behov.
author: JodiChristiansen
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2ac5e0ba8c9279fc5f04a80d4444b11850e72d3c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876348"
---
# <a name="credit-management-parameters-setup"></a>Konfiguration af kreditstyringsparametre

[!include [banner](../includes/banner.md)]

Denne artikel beskriver de indstillinger, du kan bruge til at konfigurere kreditstyring, så det opfylder virksomhedens behov. Når du vil begynde at bruge kreditstyringsfunktioner, skal du konfigurere parametrene på siden **Parametre for Kredit og inkasso** (**Kredit \> Konfiguration \> Parametre for Kredit og inkasso**).

## <a name="credit-parameters"></a>Kreditparametre

Der er fire oversigtspaneler i sektionen **Kredit**, hvor du kan ændre parametrene for Kreditstyring: **Kreditter på hold**, **Kontrolpunkt for kreditstyring**, **Kreditstyringsstatistik** og **Kreditgrænser**. I følgende afsnit beskrives de indstillinger, der er tilgængelige i hvert oversigtspanel.

### <a name="credit-holds"></a>Kreditter på hold

- Vælg **Nej** i indstillingen **Tillad redigering af salgsordrer, når spærringen af ordren er ophævet** for at angive, at bogføringsreglerne skal kontrolleres igen, hvis salgsordrens værdi (udvidet pris) er blevet øget, efter at salgsordren blev frigivet fra spærringslisten.
- I feltet **Årsager til annullerede ordrer** skal du vælge den frigivelsesårsag, der skal bruges som standard, når en salgsordre, hvor der er spærret for kreditstyring, annulleres.
- Vælg **Ja** i indstillingen **Kontroller kreditmaksimum for kundekreditgrupper** for at kontrollere kreditgrænsen for en kundekreditgruppe, når kunden på en salgsordre tilhører en kundekreditgruppe. Gruppens kreditmaksimum kontrolleres, og hvis det er tilstrækkeligt, kontrolleres kreditmaksimum for kunden.
- Vælg **Ja** i indstillingen **Kontroller kreditmaksimum, når betalingsbetingelserne er forlænget**, hvis du vil kontrollere, om rangeringen i betalingsbetingelserne er forskellig fra standardbetalingsbetingelserne for kunden. Hvis de nye betalingsbetingelser har en højere rangering end de oprindelige betalingsbetingelser, sættes ordren på hold i kreditstyringen.
- Vælg **Ja** i indstillingen **Kontroller kreditmaksimum, når en udligningsrabat er forøget**, hvis du vil kontrollere rangeringerne i udligningsrabatten for at afgøre, om kasserabatten er forskellig standardkasserabatten for kunden. Hvis den nye kasserabat har en højere rangering end den oprindelige kasserabat, sættes ordren på hold i kreditstyringen.
- I feltet **Årsag til frigivelse af ændrede ordrer** skal du vælge den årsag til frigivelse, der skal bruges som standard, når spærringen af ændrede ordrer automatisk fjernes i kreditstyringen.
- Vælg **Ja** i indstillingen **Ignorer spærringsreglen for udløbet kreditmaks., når udløbsdatoen ikke er angivet** for at styre funktionsmåden for **Kreditmaksimum udløbet**. Vælg **Nej** i indstillingen for at spærre en ordre, når udløbsdatoen ikke er angivet.
- I Lokationsstyring kan der oprettes belastninger på tidspunktet for ordreindtastning. Vælg **Nej** i indstillingen **Fjern blokerede lastlinjer** for at lade salgsordrelinjer forblive i belastningen, når en salgsordre er på kredithold. Belastningen kan ikke behandles, mens salgsordren er på hold. Vælg **Ja** for at fjerne salgsordrelinjer fra belastningen, når en salgsordre er på kredithold. Belastningen kan derefter behandles.
- Salgsordrer kan automatisk frigives fra kreditstyringsgennemsyn. I feltet **Årsag til automatisk frigivelse** skal du vælge den årsag til frigivelse, der skal bruges som standard, når salgsordrer frigives automatisk.
- Salgsordrer kan automatisk frigives fra kreditstyringsgennemsyn. I feltet **Frigiv automatisk** skal du vælge **Uden bogføring** for at frigive et ordrehold. Du skal køre den proces, der har sat ordren på hold, manuelt. Vælg **Med bogføring** for at bogføre ordren ved at bruge samme bogføringsproces, der blev kørt, da salgsordren blev sat på hold.

### <a name="credit-management-checkpoint"></a>Kontrolpunkt for kreditstyring

Du kan angive den tidsindstilling, der bruges til at kontrollere salgsordrer for kreditudstedelser. Oversigtspanelet **Kontrolpunkt for kreditstyring** identificerer de dokumentbogføringsprocesser, der omfatter behandling af regler for kreditstyring. Du kan også kontrollere kreditreglerne, mens du enten udfører en proformabogføring eller en fuld bogføring af salgsordren. Markér afkrydsningsfelterne for at definere de posteringsprocesser, der skal sætte en ordre på hold, hvis der findes et problem, efter at reglerne for blokering af kreditstyring er behandlet.

Du kan også definere antallet af respitdage, før kreditreglerne kontrolleres igen. Selvom du kan angive, at reglerne for kreditstyring skal kontrolleres ved bogføring, kontrolleres reglerne ikke i det angivne antal respitdage. Du bekræfter f.eks. en salgsordre på dag 1, og du angiver to respitdage i bekræftelsestrinnet. I dette tilfælde kontrolleres kreditreglerne ikke ved det næste trin i bogføringen (f.eks. oprettelse af en følgeseddel eller fakturering af ordren) før dag 4. Efter den 4. dag kontrolleres reglerne igen, når der foretages bogføring, og antallet af respitdage ændres til den værdi, der er angivet for det næste bogføringskontrolpunkt.

Hvis du ikke angiver antallet af respitdage, kontrolleres kreditreglerne for alle de posteringstrin, der er konfigureret til kørslen af regler for kreditstyring. Hvis du frigiver salgsordren uden at bogføre den og derefter kører det samme ordrebehandlingstrin igen, kontrolleres kreditreglerne igen. En ordre sættes f.eks. på hold efter en bekræftelse, og du frigiver den enten med eller uden bogføring. I dette tilfælde vil ordren blive sat på hold igen, hvis du bekræfter den igen. Brug respitdage, hvis ordren skal gå videre til næste behandlingstrin uden at blive sat på hold igen.

> [!Note]
> Hvis der er angivet en respitdag for et bogføringskontrolpunkt, skal alle kontrolpunkter, der er markeret til bogføring, have respitdage.

- Markér afkrydsningsfeltet **Bogføring** for at køre reglerne for kreditstyring, når det bogføringskontrolpunkt, der vises på linjen, køres. Hvis du ikke markerer afkrydsningsfeltet, bliver reglerne kun kontrolleret én gang i hele bogføringsprocessen.
- Hvis du markerer afkrydsningsfeltet **Bogføring**, skal du angive det antal respitdage, der skal gå, før blokeringsreglerne skal kontrolleres igen. Du kan ikke tilføje respitdage, hvis afkrydsningsfeltet **Bogføring** ikke er markeret.
- Markér afkrydsningsfeltet **Proforma** for at køre reglerne for kreditstyring, når det proforma bogføringskontrolpunkt, der vises på linjen, køres. I de fleste tilfælde er **Bogføring**- feltet indstillet til **Nej** i den dialogboks, der vises, når en salgsordre bogføres.
- Hvis du markerer afkrydsningsfeltet **Bogføring**, skal du angive det antal respitdage, der skal gå, før blokeringsreglerne skal kontrolleres igen. Du kan ikke tilføje respitdage, hvis afkrydsningsfeltet **Bogføring** ikke er markeret.

### <a name="credit-management-statistics"></a>Kreditstyringsstatistik

Der findes flere kreditstyringsstatistikker i faktaboksen **Statistik for kundekreditstyring** på siden **Kunde**. Du skal angive flere værdier, der skal bruges til beregning af statistikken. Angiv det antal måneder, der skal bruges til at beregne følgende værdier i faktaboksen **Statistik for kundekreditstyring**:

1. Udestående dages salg 1
2. Udestående dages salg 2
3. Gennemsnitlig saldo 1
4. Gennemsnitlig saldo 2
5. Gennemsnitlig kreditmaks. i %
6. Gennemsnitlig eksponering i %

### <a name="credit-limits"></a>Kreditgrænser

- I forbindelse med kreditstyring vises kundens kreditmaksimum i kundens valuta. Du skal angive valutakurstypen for kreditmaksimum i kundens valuta. I feltet **Valutakurstype for kreditmaksimum** skal du vælge den type valutakurs, der skal bruges til omregning af den primære kreditmaksimum til debitorens kreditmaksimum.
- Vælg **Nej** i indstillingen **Tillad manuel redigering af kreditmaks.** for at forhindre brugere i at redigere kreditmaksimum på siden **Debitor**. Hvis du vælger **Nej** i denne indstilling, kan ændringer af en debitors kreditmaksimum kun foretages ved bogføring af reguleringsposteringer for kreditmaksimum.
- Angiv indstillingen **Undgå lagerreservationer** til **Ja**, hvis du vil ignorere lagerreservationer, når blokeringsregler for kreditstyring kontrolleres. I dette tilfælde kontrollerer systemet hele linjeantal og aktiverer fristerne for kontrolpunktet, uanset antallet på lagerreservationen.
- Når Kreditstyring er aktiveret, bruges indstillingen af feltet **Meddelelse ved overskridelse af kreditmaksimum** kun til behandling af fritekstfakturaer. Selvom meddelelser stadig føjes til salgsordrer, når kunderne har overskredet deres kreditmaksimum, spærres der ikke for bekræftelse, udskrivning af pluklister og følgesedler eller bogføring af fakturaer.

    Kreditstyring er som standard aktiveret, men du kan deaktivere den. Hvis den er aktiveret, kan du bruge blokeringsreglerne for kreditstyring og kontrolpunkter til at identificere, hvornår kunder har overskredet deres kreditmaksimum. Hvis den deaktiveres, kan de meddelelser, der føjes til salgsordrer baseret på indstillingen af feltet **Meddelelse ved overskridelse af kreditmaksimum**, hjælpe dig med at identificere, hvornår kunder har overskredet deres kreditmaksimum.

### <a name="number-sequences-and-shared-number-sequence-parameters"></a>Nummerserier og parametre for delte nummerserier

Der kræves et kladde-ID for at behandle reguleringer af kreditmaksimum. Du skal tilføje det reguleringsnummer for kreditmaksimum, der skal bruges til generering af kladde-id'et.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
