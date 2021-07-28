---
title: Tildeling af opgavelister til butikker eller medarbejdere
description: Dette emne beskriver, hvordan du tildeler opgavelister til butikker eller medarbejdere i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 85b021f99a1260e4ed640764e4a3e96a80197768
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354583"
---
# <a name="assign-task-lists-to-stores-or-employees"></a>Tildele opgavelister til butikker eller medarbejdere

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du tildeler opgavelister til butikker eller medarbejdere i Microsoft Dynamics 365 Commerce.

Opgavestyring i Dynamics 365 Commerce giver dig mulighed for at tildele en opgaveliste til flere butikker eller medarbejdere eller til en kombination af butikker og medarbejdere. En regional chef for 20 butikker kan f.eks. vælge at tildele opgavelisten **Forberedelser til juleferien** til alle 20 butikker.

## <a name="start-the-task-list-assignment-process"></a>Start tildelingsprocessen for opgavelisten

Benyt følgende fremgangsmåde for at starte tildelingen af en opgaveliste.

1. Gå til **Retail og Commerce \> Opgavestyring \> Administration af opgavestyring**.
1. Vælg den opgaveliste, der skal tildeles.
1. Vælg **Start proces**.
1. Angiv et navn (f.eks. **Butikker i den østlige region**) i feltnavnet **Procesnavn** i dialogboksen **Start proces** på fanen **Generelt**.
1. Angiv en dato i feltet **Måldato**.
1. Hvis du vil tildele opgavelisten til butikker, skal du finde og vælge butikker på fanen **Butikker** vha. filteret **Organisationshierarki**.

    Hvis du vil tildele opgavelisten til medarbejdere, skal du finde og vælge medarbejderne under fanen **Arbejdere**.

1. Vælg **OK** for at starte processen. Opgavelisten tildeles til de valgte butikker eller medarbejdere.

I følgende illustration vises et eksempel på, hvordan du finder og vælger butikker i dialogboksen **Start proces**.

![Finde og vælge butikker i dialogboksen Start proces.](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a>Tildele tilbagevendende opgavelister

Detailhandleren har nogle gange tilbagevendende opgaver, f.eks. "Tjekliste til torsdagslukning" eller "Tjekliste til første dag i måneden". Det kan derfor være en god ide at tildele en tilbagevendende opgaveliste.

1. Gå til **Retail og Commerce \> Opgavestyring \> Administration af opgavestyring**.
1. Vælg den opgaveliste, der skal tildeles.
1. Vælg **Start proces**.
1. Angiv et navn i feltet **Procesnavn** i dialogboksen **Start proces** på fanen **Generelt**.
1. Indstil indstillingen **Gentagelse** til **Ja**.
1. Angiv antallet af dage i feltet **Forskydning af gentagelse af måldage i dage**. Hvis du f.eks. angiver **4**, vil måldatoen være gentagelsesdatoen plus fire dage.
1. Vælg **Gentagelse** på fanen **Kør i baggrunden**.
1. Angiv frekvenskriterierne i dialogboksen **Definer gentagelse**, og vælg derefter **OK**.

I følgende illustration vises et eksempel på, hvordan du kan angive hyppighedskriterier i dialogboksen **Definer gentagelse**.

![Angive frekvenskriterierne i dialogboksen Definer gentagelse.](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a>Spor status for opgaveliste

Hvis du er regional chef eller butikschef, kan det være en god ide at spore status for opgavelister, der er tildelt til flere butikker eller medarbejdere. Du kan derefter følge op med butikker eller arbejdere, der ikke har fuldført deres tildelte opgaver til tiden. Med funktionen Commerce-bagkontor kan du få vist status for opgavelister, tildele opgaver igen eller ændre status for en opgave.

Hvis du vil følge op på opgavelistestatus for alle opgaver, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Opgavestyring \> Opgavestyringsprocesser**.
1. Vælg fanen **Alle opgavelister** for at få vist status for alle opgavelister, der er knyttet til forskellige butikker.

Hvis du vil følge spore status for opgavelister for alle opgaver, som er tildelt dig, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Opgavestyring \> Opgavestyringsprocesser**.
1. Vælg fanen **Mine opgaver** eller **Alle opgaver** for at få vist eller opdatere status for de opgaver, der er tildelt til dig.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over opgavestyring](task-mgmt-overview.md)

[Konfigurer opgavestyring](task-mgmt-configure.md)

[Oprette opgavelister og tilføje opgaver](task-mgmt-create-lists.md)

[Opgavestyring i POS](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
