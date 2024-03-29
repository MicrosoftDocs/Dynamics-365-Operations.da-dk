---
title: Oprette en købsaftale
description: Denne artikel fører dig gennem oprettelsen af en købsaftale.
author: GalynaFedorova
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 108c3a47132b262ebe2e15f00d26191b75469959
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877560"
---
# <a name="create-a-purchase-agreement"></a>Oprette en købsaftale

[!include [banner](../../includes/banner.md)]

Denne artikel fører dig gennem oprettelsen af en købsaftale. Dette vil normalt ske ved en indkøbschef. Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data. Du skal have oprettet købsaftaleklassifikationer, før du starter. Når du har oprettet en aftale, du kan bruge den, når du opretter en Indkøbsordre, og denne handling kopierer køb aftale betingelserne til hovedet og linjer i ordren, der berøres af aftalen.


## <a name="create-a-new-purchase-agreement"></a>Opret en ny købsaftale
1. Gå til **Navigationsruden > Moduler > Indkøb og forsyning > Købsaftaler > Købsaftaler**.
2. Klik på **Ny**.
3. Vælg rækken med den ønskede post fra rullemenuen i feltet **Kreditorkonto**.
4. Vælg rækken med den ønskede post fra rullemenuen i feltet **Købsaftaleklassifikation**.
5. Udvid oversigtspanelet **Generelt**.
6. Indtast en dato i feltet **Udløbsdato**.

    - Denne udløbsdato er standard for alle tilsagnslinjer og bestemmer, hvor længe hvert specifikt tilsagn er gyldigt.  

7. Indtast et navn for købsaftalen i feltet **Dokumenttitel**.

    - Lad feltet **Standardtilsagn** være angivet til **Bundet produktantal** (eller ret det, hvis det ikke er angivet til dette).  
    - Værdien for standardtilsagnet angiver dine indstillinger på aftalelinjerne. Hvis du har brug for en ny tilsagnstype, når du opretter aftalelinjer, skal du ændre standardtilsagnet i overskriften. Der er 4 typer tilsagn: **Bundet produktantal** – for en bestemt mængde af et produkt, **Værditilsagn om produkt** – for et bestemt valutabeløb af et produkt, **Værditilsagn om produktkategori** – for et bestemt valutabeløb i en indkøbskategori, hvor beløbet kan være for en katalogvare eller en vare uden for kataloget, **Værditilsagn** – for et bestemt valutabeløb, som kan opfyldes af et produkt eller en indkøbskategori.  

8. Vælg **OK**.

## <a name="add-a-commitment"></a>Tilføj et tilsagn
1. Vælg **Tilføj linje**.
2. Vælg den ønskede post på rullemenuen i feltet **Varenummer**.
3. Angiv et tal i feltet **Antal**. Dette er den samlede mængde, som du har aftalt at købe fra din kreditor.  
4. Angiv et tal i feltet **Enhedspris**.
5. Vis eller skjul sektionen **Linjedetaljer**.
6. Sæt indstillingen **Maks. gennemtvinges** til **Ja**. Indstillingen **Maks. gennemtvinges** begrænser brugen af forpligtelsen. Du kan kun købe op til det antal, der er angivet i feltet **Antal** for linjen.  

## <a name="add-header-conditions"></a>Tilføj hovedbetingelser
1. Vælg **Indstillinger** i handlingsruden.
2. Vælg **Skift visning**.
3. Vælg **Overskriftsvisning**.
4. Udvid afsnittet **Betingelser**.
5. I feltet **Betalingsmåde** skal du vælge den ønskede post i rullemenuen. Betalingsbetingelserne fra kreditorkontoen vises her som standard.  
6. I feltet **Leveringsmåde** skal du vælge den ønskede post i rullemenuen.
7. Vælg rullelisten i feltet **Leveringsbetingelse** for at åbne opslaget.

## <a name="confirm-and-activate-the-agreement"></a>Bekræft og aktivér aftalen
1. Klik på **Købsaftale** i handlingsruden.
2. Vælg **Bekræftelse**. Angiv indstillingen **Markér aftale som gældende** til **Ja**.  
3. Vælg **OK**.
4. Klik på **Købsaftale** i handlingsruden.
5. Vælg **Bekræftelser af købsaftaler**. Med indstillingen **Vis/udskriv** kan du oprette et dokument for købsaftalen, som du kan udskrive eller sende til kreditoren. Hvis du opdaterer aftalen senere og bekræfter den igen, vises begge versioner her.  
6. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]