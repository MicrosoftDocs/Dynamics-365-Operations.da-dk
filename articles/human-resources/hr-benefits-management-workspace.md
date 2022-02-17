---
title: Arbejdsområde for personalegodeadministration
description: Dette emne beskriver arbejdsområdet Frynsegodeadministration i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 01/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 424f4a2098e05b4f7dc6fa84df133dda81cc59f0
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071418"
---
# <a name="benefits-management-workspace"></a>Arbejdsområde for personalegodeadministration


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [applies to](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

Dette emne beskriver arbejdsområdet **Frynsegodeadministration** i Dynamics 365 Human Resources.

> [!NOTE]
> Hvis du vil have vist arbejdsområdet **Frynsegodeadministration**, skal du først aktivere funktionen **(Forhåndsversion) arbejdsområdet Frynsegodeadministration** i funktionsstyring. Du kan finde flere oplysninger om aktivering af prøveversionsfunktioner i [Administrere funktioner](hr-admin-manage-features.md).<br><br>![Aktivere arbejdsområdet Frynsegodeadministration.](./media/hr-benefits-management-workspace-enable.png)

Arbejdsområdet **Frynsegodeadministration** giver dig et hurtigt overblik over elementer til frynsegoder, der kræver din opmærksomhed. På denne side kan du se:

- Totaler for elementer, der afventer handling
- Arbejdere med ikke-bekræftede valg
- Arbejdere, der for nylig har tilmeldt sig frynsegoder
- Arbejdere med fremtidige livshændelser
- Nyansatte, der ikke er tilmeldt
- Arbejdere med aktive livshændelser
- Arbejdere med åbne tilmeldinger, som ikke har valgt nogen planer

![Arbejdsområdet Frynsegodeadministration.](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a>Se handlingselementer

Du kan få vist dine handlingselementer ved enten at vælge et felt eller en fane. Hvis du vælger en fane, kan du se og vælge arbejdere direkte på arbejdsområdesiden.

![Handlingselementer.](./media/hr-benefits-management-workspace-action-items.png)

Hvis du vælger et felt, går du til siden for det pågældende område. Hvis du f.eks. vælger et af disse felter, vises siden **Frynsegodeplaner for medarbejdere** filtreret efter medarbejdere, du skal udføre handling på:

- **Ikke-bekræftede valg**
- **Åbn tilmeldinger med ingen udtjekkede planer**
- **Tilmeldt i frynsegoder**
- **Nyansat, der ikke er tilmeldt**

![Frynsegodeplaner for arbejder.](./media/hr-benefits-management-workspace-plans.png)

Når du vælger feltet **Aktive livshændelser** eller **Fremtidige livshændelser**, får du en liste over aktive eller fremtidige livshændelser.

![Livshændelser.](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a>Behandler

Hvis du vil behandle tilmeldingsberettigelse, livshændelser eller ændringer af frynsegodesatsen, skal du vælge det relevante element på navigationslinjen.

![Afvikling.](./media/hr-benefits-management-workspace-processing.png)

For at få vist resultaterne af processen skal du vælge **Procesresultater** på siden.

![Procesresultater.](./media/hr-benefits-management-workspace-process-results.png)

Du kan finde flere oplysninger om behandling af frynsegoder under:

- [Behandle berettigelse til tilmelding](hr-benefits-process-enrollment-eligibility.md)
- [Behandle ændringer af livsbegivenheder](hr-benefits-process-life-event-changes.md)
- [Behandle berettigelse til livsbegivenheder](hr-benefits-process-life-event-eligibility.md)
- [Behandle livsbegivenheder](hr-benefits-process-life-events.md)
- [Behandle satsændringer](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a>Ændre periode

Hvis du vil have vist en anden frynsegodeperiode, skal du vælge den på rullelisten **Periode**.

![Ændre periode.](./media/hr-benefits-management-workspace-period.png)


## <a name="open-enrollment-tab"></a>Åben fanen Tilmelding

Du kan få vist dine handlingselementer ved enten at vælge et felt eller en fane. Hvis du vælger en fane, kan du se og vælge arbejdere direkte på arbejdsområdesiden.
Fanen **Åben tilmelding** indeholder nøgleværdier for processen til åben tilmelding. 

Oplysninger om åbne tilmeldinger vises 30 dage før **startdatoen for tilmelding**. Dette er defineret i opsætningen af **Perioder** i **Frynsegodestyring** > **Link** > **Perioder** i feltet **Startdato for tilmelding**.  Du kan ændre denne indstilling ved at gå til **Delte Human Resources-parametre** > **Frynsegodeadministration** > **Åbne indstillinger for tilmelding** og opdatere feltet **Antal**.  

Følgende oplysninger er tilgængelige under fanen **Åben tilmelding**:
 - Medarbejdere, der ikke har startet den åbne tilmeldingsproces
 - Medarbejdere, som har medarbejdere i arbejde
 - Medarbejdere, som har fuldført valgprocessen
 - Ikke-bekræftede valg

**Oversigt over felter**

- **Ikke startet** – Feltet **Ikke startet** viser en optælling af medarbejdere, der ikke har startet tilmeldingsprocessen. Feltet **Ikke startet** er en filtreret liste, som kun viser de medarbejdere, der ikke har valgt, frafaldet eller checket ud for den åbne tilmeldingsplanperiode. Obligatoriske planer ignoreres og medtages ikke, da de er valgt som standard for medarbejderen.  Du kan foretage en detailudgang på denne side for at få vist en liste over medarbejdere, der ikke har startet den åbne tilmeldingsproces på siden **Medarbejderfrynsegoder**.

  > [!NOTE]
  > Hvis du ikke vil spore status for åben tilmelding for en **plantype**, kan du udelade den ved at gå til **Frynsegodsstyring** > **Links** > **Medarbejder-selvbetjeningsparametre** > **Konfigurer felt til frynsegodeplaner** og opdatere feltet **Spor status for åben tilmelding**.  Der kan f.eks. være oprettet planer, hvor **plantype** = **Andet**. Disse planer kan være valgfrie planer, som du ikke ønsker at spore status for tilmeldinger for. Hvis du ikke vælger denne plantype, ignoreres planerne af disse typer, når status for tilmelding spores eller fuldføres under fanen **Åben tilmelding**. Denne indstilling gælder for den plantype, der er valgt for alle perioder og juridiske enheder.

- **I gang** – Feltet **I gang** giver en optælling af medarbejdere, der er igangværende. Feltet **I gang** er en filtreret liste, der kun viser medarbejdere, der har mindst én plan, som er frafaldet eller valgt. Obligatoriske planer ignoreres og medtages ikke, da de er valgt som standard for medarbejderen. Du kan foretage en tilbagerulning fra dette felt for at få vist de valgte og fravalgte planer på siden **Masseopdatering af medarbejderes frynsegoder**.

- **Tilmeldte frynsegoder** – Feltet **Tilmeldte frynsegoder** indeholder en tælling af medarbejdere, der er fuldt tilmeldt frynsegoder. Feltet **Tilmeldte frynsegoder** er en filtreret liste, der viser medarbejdere, som har valgt eller frafaldet alle planer. Forespørgslen vil udelukke planer, der ikke spores for åben tilmelding på siden **Parametre for medarbejderselvbetjening**. Du kan foretage en tilbagerulning fra dette felt for at få vist en liste over medarbejdere på siden **Frynsegodeplaner for medarbejder**.

- **Ikke-bekræftede valg** – Feltet til **ikke-bekræftede valg** viser et antal medarbejdere, der har valgte eller fravalgte planer, som skal bekræftes. Du kan foretage en tilbagerulning fra dette felt for at få vist siden **Masseopdatering af medarbejderes frynsegoder**.

**Aktivitet**

- **Ikke startet** – Feltet **Ikke startet** viser en optælling af medarbejdere, der ikke har startet tilmeldingsprocessen. Feltet **Ikke startet** er en filtreret liste, som kun viser de medarbejdere, der ikke har valgt, frafaldet eller checket ud for den åbne tilmeldingsplanperiode. Obligatoriske planer ignoreres og medtages ikke, da de er valgt som standard for medarbejderen. Du kan foretage en tilbagerulning for arbejderen for at få vist siden **Detaljeret frynsegodeplan for lønmedarbejder**.

- **Optælling i gang** – Feltet **Optællinger i gang** giver en optælling af medarbejdere, der er igangværende. Feltet **Optællinger i gang** er en filtreret liste, der kun viser medarbejdere, der har mindst én plan, som er frafaldet eller valgt. Obligatoriske planer ignoreres og medtages ikke, da de er valgt som standard for medarbejderen. Du kan foretage en tilbagerulning for arbejderen for at få vist siden **Detaljeret frynsegodeplan for lønmedarbejder**.

## <a name="view-more-options"></a>Se flere indstillinger

Vælg **Links**, hvis du vil have vist flere oplysninger og handlinger, du kan udføre.

![Links.](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a>Se også

[Oversigt over administration af frynsegoder](hr-benefits-management-overview.md)
