---
title: Tildele opgavelister til butikker eller medarbejdere
description: Denne artikel beskriver, hvordan du tildeler opgavelister til butikker eller medarbejdere i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.search.industry: ''
ms.openlocfilehash: faff772051738f624b86fd23fb6bf29173e909ea
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746188"
---
# <a name="assign-task-lists-to-stores-or-employees"></a>Tildele opgavelister til butikker eller medarbejdere

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du tildeler opgavelister til butikker eller medarbejdere i Microsoft Dynamics 365 Commerce.

Opgavestyring i Dynamics 365 Commerce giver dig mulighed for at tildele en opgaveliste til flere butikker eller medarbejdere eller til en kombination af butikker og medarbejdere. En regional chef for 20 butikker kan f.eks. vælge at tildele opgavelisten **Forberedelser til juleferien** til alle 20 butikker.

## <a name="start-the-task-list-assignment-process"></a>Start tildelingsprocessen for opgavelisten

Før du går i gang med at tildele opgaver, skal du sørge for at oprette en opgaveliste ved at følge trinnene i artiklen [Oprette opgavelister og tilføje opgaver](task-mgmt-create-lists.md). Benyt følgende fremgangsmåde for at starte tildelingen af en opgaveliste.

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
