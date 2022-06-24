---
title: Opdele genererede XML-filer ud fra filstørrelse og indholdsmængde
description: Denne artikel indeholder oplysninger om, hvordan du opdeler genererede filer baseret på filstørrelsen og antallet af indholdselementer.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 041bec441d2517a7b646c4a18a45863c541b2b7a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872995"
---
# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a>Opdele genererede XML-filer ud fra filstørrelse og indholdsmængde

[!include[banner](../includes/banner.md)]

Du kan designe ER-formater for at oprette udgående dokumenter i XML-format. Nogle gange kan disse dokumenterne kun accepteres, når de opfylder bestemte kriterier, f.eks. en maksimal filstørrelse eller et maksimalt antal af bestemte XML-noder. Du kan designe ER-formater for at generere elektroniske dokumenter, der opfylder de krav, som modtagerne af disse dokumenter angiver.

- For FILE-formatelementet kan du definere en grænse for filens størrelse som et ER-udtryk. Hvis den angivne grænse overskrides, når der oprettes en ER-rapport, afslutter ER oprettelsen af den aktuelle fil og fortsætter derefter med at oprette den næste fil.
- For XML ELEMENT-formater kan du definere en grænse for antal elementer som et ER-udtryk. Hvis antallet af XML-noder i den fil, der genereres, overskrider den angivne grænse, når der køres en ER-rapport, afslutter ER oprettelsen af den aktuelle fil og fortsætter derefter med at oprette den næste fil.
- For XML SEQUENCE-formatelementer kan du definere en grænse for antal underordnede elementer som et ER-udtryk. Hvis antallet af indlejrede XML-noder i formatelementet i den genererede fil overskrider den angivne grænse, når der køres en ER-rapport, afslutter ER oprettelsen af den aktuelle fil og fortsætter derefter med at oprette den næste fil.
- Du kan markere ethvert XML ELEMENT-format, som non-breakable. På denne måde kan du organisere de indlejrede elementer i XML-noder, der genereres under formatelementet, i en enkelt genereret fil.

Ud over at bruge XML ELEMENT- og XML SEQUENCE-formatelementer til at føje XML-noder til den oprettede fil, kan du bruge RAW XML-formatelementet. Noder, som du tilføjer ved hjælp af det RAW XML-formatelementet, tages ikke i betragtning, når antallet af noder, beregnes for at vurdere grænserne for antallet af elementer.

Hvis du har konfigureret fildestinationer for et FILE-formatelement, der er konfigureret til at opdele det genererede output, når bestemte grænseværdier overskrides, sendes hvert enkelt genererede output til den konfigurerede fildestination som en individuel fil. For entydigt at identificere de filer, der oprettes ved at opdele outputtet, skal du konfigurere et ER-udtryk for FILE-formatelementet. Hvis du medtager en ER-datakilde af typen NUMBER SEQUENCE, øges nummerserien trinvist for hver enkelt del af det opdelte output.

Hvis du vil vide mere om denne funktion, kan du afspille opgaveguiden **ER Opdele XML-filer baseret på filstørrelsen eller antallet af indholdselementer**, som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde komponenter til it-servicer og -løsninger (10677)**, og som kan hentes fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684). Denne opgaveguide gennemgår konfigurationen af et ER-format for at opdele genererede filer baseret på begrænsninger i filstørrelsen og antallet af indholdselementer. Du skal hente følgende filer for at fuldføre opgaveguiden:

- [ER-modelkonfiguration - XmlFilesSplittingModel.xml](https://download.microsoft.com/download/e/a/f/eaffe96a-22ec-4a32-898a-f4328c91c387/XmlFilesSplittingModel.xml)
- [ER-formatkonfiguration - XmlFilesSplittingFormat.xml](https://download.microsoft.com/download/e/9/c/e9c5849b-8254-4cdf-bb00-4c2ebc72ddec/XmlFilesSplittingFormat.xml)

## <a name="additional-resources"></a>Yderligere ressourcer
[Destinationer for elektronisk rapportering (ER)](electronic-reporting-destinations.md)

[Formeldesigner i elektronisk rapportering (ER)](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
