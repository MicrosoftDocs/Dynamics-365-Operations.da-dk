---
title: Lokalisere fejl i indkøbsordrer
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med indkøbsordrer.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 964f31c21faae6a947174f637624aca917881297
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841449"
---
# <a name="troubleshoot-purchase-orders"></a>Lokalisere fejl i indkøbsordrer

Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med indkøbsordrer.

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a>En handling kan først fuldføres, når linjenummeret er fuldt fordelt.

Dette problem kan opstå på grund af inkonsistens i indkøbsordrefordeling.

Hvis du vil løse dette problem og nulstille indkøbsordren til en *Kladde*-tilstand, skal du gå til **Indkøb og forsyning \> Periodiske opgaver \> Oprydning \> Nulstil indkøbsordrefordeling**. Du kan finde flere oplysninger i følgende blogindlæg: [Løse fejl i indkøbsordrefordeling i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a>Når indkøbsordrer importeres via datastyring, følger numrene på indkøbsordrelinjer ikke den forøgelse, der er defineret i systemparametrene.

### <a name="issue-description"></a>Problembeskrivelse

Automatisk genererede linjenumre for indkøbsordrelinjer, der er importeret via *Indkøbsordrelinjer V2*-dataenhed, bruger som standard ikke det stigende systemlinjenummer, der er angivet i systemparametrene. Hvis du opretter en indkøbsordre manuelt og tilføjer linjer via brugergrænsefladen, stiger linjenumrene korrekt. Men hvis du bruger datastyringsstrukturen (DMF - Data Management Framework), stiger de ikke korrekt.

Dette problem opstår, fordi systemet bruger DMF-metoden til at tildele dem, når du importerer linjer via DMF, hvis de ikke allerede er tildelt i den importerede enhed. Metoden øger altid linjenumrene med én.

### <a name="issue-workaround"></a>Problemløsning

Sørg for, at de ønskede linjenumre allerede er angivet i felterne for linjenummer i dataenheden, når du importerer indkøbsordrelinjerne. I dette tilfælde overskriver DMF ikke linjenumrene.

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a>Der udfyldes ikke en standardmomsgruppe og en standardkasserabat fra fakturakontoen.

Hvis du bruger en fakturakonto, der er forskellig fra debitorkontoen, udfyldes der ikke en standardmomsgruppe og en standardkasserabat fra fakturakontoen, når der oprettes en indkøbsordre.

Denne funktionsmåde er tilsigtet. Standardværdierne for momsgruppen, kasserabatter og andre prisoplysninger er baseret på debitorkontoen – ikke fakturakontoen.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Jeg får vist fejlmeddelelsen "Objektreferencen er ikke angivet" under bekræftelse af indkøbsordren, eller der er opstået "Destinationen for en aktivering udløste en undtagelse" under bogføring af kreditorfakturaen.

Dette problem kan opstå på grund af inkonsistens i indkøbsordrefordeling.

Hvis du vil løse dette problem og nulstille indkøbsordren til en *Kladde*-tilstand, skal du gå til **Indkøb og forsyning \> Periodiske opgaver \> Oprydning \> Nulstil indkøbsordrefordeling**. Du kan finde flere oplysninger i følgende blogindlæg: [Løse fejl i indkøbsordrefordeling i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>En eller flere regnskabsfordelinger er enten overfordelt eller underfordelt.

### <a name="issue-description"></a>Problembeskrivelse

Du får følgende fejl: "En eller flere regnskabsfordelinger er enten overfordelt eller underfordelt".

### <a name="issue-resolution"></a>Problemløsning

Dette problem kan opstå på grund af inkonsistens i indkøbsordrefordeling.

Hvis du vil løse dette problem og nulstille indkøbsordren til en *Kladde*-tilstand, skal du gå til **Indkøb og forsyning \> Periodiske opgaver \> Oprydning \> Nulstil indkøbsordrefordeling**. Du kan finde flere oplysninger i følgende blogindlæg: [Løse fejl i indkøbsordrefordeling i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Kan jeg nøjes med at få vist de indkøbsordrer, jeg har oprettet?

Denne funktionalitet er ikke tilgængelig i øjeblikket.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Kan jeg reservere en lagerbeholdning og oprette transaktioner mod registreret lager på en indkøbsordre?

### <a name="issue-description"></a>Problembeskrivelse

Selv når varer er i en *Registreret* tilstand på en indkøbsordre, kan du stadig reservere lageret. Du kan med andre ord oprette transaktioner mod det registrerede lager.

### <a name="reproduce-the-issue"></a>Genskabe problemet

Følgende procedurer viser en måde at genskabe problemet på.

1. Oprette en indkøbsordre.
2. Registrér indkøbsordrelinjen.
3. Bemærk, at du kan generere reservationer eller transaktioner mod det registrerede lager.

### <a name="issue-resolution"></a>Problemløsning

Denne funktionsmåde er tilsigtet. Det forventes, at de registrerede varer er modtaget fysisk på lagerstedet eller lageret, og at de derfor er tilgængelige for reservation.

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Indkøbsordrer afspejler ikke den juridiske enheds sprogindstillinger.

### <a name="issue-description"></a>Problembeskrivelse

Produktnavnet på en indkøbsordre vises på systemsproget i stedet for det sprog, der er angivet for den juridiske enhed, hvor indkøbsordren er oprettet.

### <a name="reproduce-the-issue"></a>Genskabe problemet

Følgende procedurer viser en måde at genskabe problemet på.

1. Indstil systemsproget til *EN-US* (amerikansk engelsk).
1. Sørg for, at der findes et produkt, hvor sprogene *EN-US* og *DK* (dansk) bruges til oversættelser af produktnavnet.
1. Skift sproget for en juridisk enhed til *DK*.
1. Opret en indkøbsordre, der indeholder produktet, i den juridiske enhed, hvor *DK* er angivet som sprog.
1. Bemærk, at produktnavnet stadig vises på amerikansk engelsk (systemsproget).

### <a name="issue-resolution"></a>Problemløsning

Denne funktionsmåde er tilsigtet. På indkøbsordrer vises produktet altid på systemsproget. Indkøbsordresproget bruges, når der oprettes en bekræftelsesjournal.

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a>Listen over godkendte kreditorer efter produktenhed tillader ikke, at ikrafttrædelsesdatoen ændres.

### <a name="issue-description"></a>Problembeskrivelse

Et produkt har en godkendt kreditor, der f.eks. har ikrafttrædelsesdatoen 11. januar 2018 (*01/11/2018*) og udløbsdatoen *Aldrig*. Hvis du forsøger at ændre ikrafttrædelsesdatoen til 10. januar 2018 (*01/10/2018*) eller 12. januar 2018 (*01/12/2018*), får du vist følgende fejl:

> Der kan ikke oprettes en post på listen over godkendte kreditorer (PdsApproveVendorList). Værdien 'Udløb' skal være større end eller lig med værdien 'Gyldig fra'.

### <a name="issue-resolution"></a>Problemløsning

Du kan kun udvide den periode, som kreditoren er godkendt til. Der gælder følgende regler:

- Hvis du vil ændre ikrafttrædelsesdatoen, så den er tidligere end nogen af de eksisterende poster (perioder) for varens leverandør, skal udløbsdatoen for den nye periode være før alle udløbsdatoerne i de eksisterende poster.
- Hvis du vil ændre udløbsdatoen, så den er senere end nogen af de eksisterende perioder, skal ikrafttrædelsesdatoen være efter den seneste udløbsdato i en eksisterende post.
- Hvis du vil reducere den overordnede periode, som kreditoren er godkendt for, skal du slette eller redigere eksisterende poster. Du kan også bruge **afkort**-parameteren under importen. Denne parameter sletter alle eksisterende poster i tabellen for godkendte kreditorer efter vare.

I eksempelscenariet, der er beskrevet i problembeskrivelsen, hvor en post har ikrafttrædelsesdatoen *01/11/2018* og en udløbsdato på *Aldrig*, kan du importere en ny post, der har ikrafttrædelsesdatoen *01/10/2018* og en udløbsdato på *Aldrig*. Du kan dog ikke reducere perioden, så ikrafttrædelsesdatoen opdateres til *01/12/2018* via Dataadministration. Du skal foretage denne ændring via brugergrænsefladen.

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-name-isnt-synced"></a>Efter at jeg har ændret leveringsadressen på et indkøbsordrehoved, synkroniseres leveringsnavnet ikke.

### <a name="issue-description"></a>Problembeskrivelse

Adressen på hovedet i en indkøbsordre opdateres til en adresse, der ikke er en leveringsadresse. Selvom adressen opdateres på indkøbsordren, opdateres leveringsnavnet ikke på basis af den opdaterede adresse.

### <a name="issue-resolution"></a>Problemløsning

Denne funktionsmåde er tilsigtet. Den valgte adresse skal klassificeres som en leveringsadresse. Ellers opdateres leveringsnavnet ikke på basis af den valgte adresse.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Kan jeg finde den bruger, der har annulleret en indkøbsordre?

Disse oplysninger spores kun, hvis ændringsstyring er aktiveret for indkøbsordren. Hvis du bruger ændringsstyring, kan du se, hvem der har afsendt ændringen (annulleringen), og hvem der har godkendt den.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]