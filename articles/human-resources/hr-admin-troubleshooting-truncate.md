---
title: Undgå tekstafkortning i stillingshierarkiet, og eksportér til Visio
description: Denne artikel beskriver, hvordan du kan løse problemet med afkortede navne på personer og stillinger i stillingshierarkiet i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3663f5689fc0109caad01a285185f9f4ffa6fcca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865376"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>Undgå tekstafkortning i stillingshierarkiet, og eksportér til Visio


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Afgang**

Når en kunde får vist stillingshierarkiet i Microsoft Dynamics 365 Human Resources, afkortes navnene på personer og stillinger. Derfor kan det være svært at tage et skærmbillede eller udskrive og distribuere hierarkiet.

![Stillingshierarki.](media/position-h.png)

**Årsag**

Denne funktionsmåde er tilsigtet.

**Løsning**

Desværre kan brugere ikke nemt ændre størrelsen af teksten. Du kan dog eksportere stillingshierarkiet fra Human Resources og derefter importere det til Microsoft Visio. Selvom følgende artikel er skrevet til Microsoft Dynamics AX 2012, gælder processen stadig for Human Resources: [Eksportere et stillingshierarki til Microsoft Visio](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).

Følg disse trin for at eksportere til Visio.

1. Åbn listesiden **Stillinger** i Human Resources.

    Hvis du vil medtage flere oplysninger i organisationsstrukturdiagrammet, skal du tilføje felter på listen **Stillinger**, så de er tilgængelige, når du bruger **Guiden Organisationsdiagram** senere i denne procedure.

2. I handlingsruden skal du vælge knappen **Åbn i Microsoft Office**, og derefter skal du under **Eksportér til Excel** vælge **Stillinger**. Du kan også trykke på Ctrl + T.

    ![Eksportere listesiden Stillinger til Excel.](media/org-admin.png)

3. Gem Excel-filen, der eksporteres.

    ![Dialogboksen Eksportér til Excel.](media/export-excel.png)

4. I Visio skal du vælge **Visio - Opret ny** og vælge skabelonkategorien **Forretning**.

    ![Nyt diagram.](media/new.png)

5. Vælg **Guiden Organisationsdiagram**, og vælg derefter **Opret**.

    ![Dialogboksen Guiden Organisationsdiagram.](media/orgchart-wizard.png)

6. Vælg **Oplysninger, der allerede er gemt i en fil eller database**, og vælg derefter **Næste**.

    ![Guiden Organisationsdiagram 1.](media/orgchart-wizard7.png)

7. Vælg **En tekstfil, Org Plus (\*.txt) eller en Excel-fil**, og vælg derefter **Næste**.

    ![Guiden Organisationsdiagram 2.](media/orgchart-wizard3.png)

8. Gennemse for at vælge den eksporterede Excel-fil, der indeholder stillingshierarkiet, og vælg derefter **Næste**.

    ![Guiden Organisationsdiagram 3.](media/orgchart-wizard2.png)

9. Indstil feltet **Navn** til **Stilling**, indstil feltet **Rapportér til** til **Rapporterer til stilling**, og vælg derefter **Næste**.

    ![Guiden Organisationsdiagram 4.](media/orgchart-wizard1.png)

10. Vælg de felter, der skal vises på hver node, og vælg derefter **Næste**.

    ![Guiden Organisationsdiagram 5.](media/orgchart-wizard5.png)

11. Føj kolonnen **Stilling** til listen **Figurdatafelter**, og vælg derefter **Næste**.

    ![Guiden Organisationsdiagram 6.](media/orgchart-wizard6.png)

12. Der er ingen tilgængelige billeder i øjeblikket. Vælg derfor **Næste** på den næste side.
13. Vælg **Guiden skal automatisk opdele organisationsdiagrammet på tværs af sider**.

    ![Guiden Organisationsdiagram 7.](media/orgchart-wizard4.png)

14. Vælg **Udfør**.

    Hvis der eventuelt er stillinger, der ikke findes i strukturen, bliver du bedt om at medtage dem i diagrammet.

Det diagram, der er oprettet i Visio, viser hver enkelt leder i et separat regneark.

Baseret på de felter, du har valgt at medtage i diagrammet, viser hver node de relevante oplysninger, når Visio-filen genereres.

![Hierarkidiagram.](media/hierarchy.png)

**Flere indstillinger**

I Human Resources kan du muligvis også bruge arbejdsområdet **Personer** til at få vist visse oplysninger i forbindelse med hierarkiet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
