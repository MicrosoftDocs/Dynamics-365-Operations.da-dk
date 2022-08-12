---
title: Scenarier for kreditgrænse
description: I denne artikel beskrives, hvordan debitors kreditmaksimum kontrolleres, når debitoren tilhører en debitorkreditmaksimumgruppe.
author: JodiChristiansen
ms.date: 06/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-06-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 60b17a6b7f57b468610974ae9bd05b7db3584cc1
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130252"
---
# <a name="credit-limit-scenarios"></a>Scenarier for kreditgrænse

I Kreditstyring kan der tildeles et kreditmaksimum til kunder på kundeniveau. Hver debitor kan tildeles til en debitors *kreditmaksimumsgruppe*, og hver gruppe har et kreditmaksimum. Derfor kan der i Kreditstyring også tildeles et kreditmaksimum til kunder på gruppeniveau. Alle kunder, der er knyttet til samme debitorkreditgruppe, har samme kreditmaksimum.

Generelt kontrolleres gruppekreditmaksimal før de enkelte kreditmaks. Det enkelte kreditmaksimum tilsidesætter ikke altid gruppens kreditmaksimum.

I denne artikel beskrives fem scenarier, der vedrører debitorkreditgrupper og individuelle kreditmaks.

## <a name="the-customer-group-credit-limit-is-more-than-the-individual-credit-limit"></a>Kreditgrænsen for kundegruppen er større en den individuelle kreditmaksimum

Debitoren har f.eks. et individuelt kreditmaksimum på $10.000. Debitoren er tildelt en debitorkreditgruppe, og gruppens kreditmaksimum er $15.000. I dette tilfælde er debitorens "gældende kreditmaksimum" $10.000, fordi dette beløb er mindre end gruppegrænsen. Blokeringsregler kontrollerer først gruppegrænsen. Derefter kontrollerer de den individuelle grænse. Alle salgsordrer, der er $10.000, blokeres.

## <a name="the-individual-credit-limit-is-more-than-the-customer-group-credit-limit"></a>Kreditgrænsen for kundegruppen er større en den individuelle kreditmaksimum

Debitoren har f.eks. et individuelt kreditmaksimum på $20.000. Debitoren er tildelt en debitorkreditgruppe, og gruppens kreditmaksimum er $15.000. I dette tilfælde er debitorens gældende kreditmaksimum $15.000, fordi blokeringsregler altid kontrollerer gruppegrænsen først. Alle salgsordrer, der er $15.000, blokeres.

## <a name="the-individual-credit-limit-is-set-to-000-and-mandatory-credit-limit-is-set-to-yes"></a>Den enkelte kreditmaksimum angives til 0,00, og det obligatoriske kreditmaksimum angives til Ja

Hvis debitoren har et individuelt kreditmaksimum, der er angivet til **0,00**, og indstillingen **Tvungen kreditmaksimum** er angivet til **Ja**, angives debitorens gældende kreditmaksimum til $0.00, også selvom debitoren er tildelt en debitorkreditgruppe. På den måde kan kunden være en del af en gruppe, men alle ordrer går til Kreditstyring.

## <a name="the-individual-credit-limit-is-set-to-000-and-unlimited-credit-limit-is-set-to-yes"></a>Den enkelte kreditmaksimum angives til 0,00, og det ubegrænsede kreditmaksimum angives til Ja

Hvis debitoren har et individuelt kreditmaksimum, der er angivet til **0,00**, men indstillingen **Ubegrænset kreditmaksimum** er angivet til **Ja**, har kunden ubegrænset kredit, selvom de er tildelt en kundekreditgruppe.

## <a name="the-individual-credit-limit-is-set-to-000-and-the-customer-is-part-of-a-customer-credit-group"></a>Den individuelle kreditgrænse er angivet til 0,00, og kunden er en del af en kundekreditgruppe

Kunden har f.eks. et individuelt kreditmaksimum, der er angivet til **0,00**, indstillingen **Ubegrænset kredit** angives til **Nej**, og indstillingen **Tvungen kreditmaksimum** angives til **Nej**. Debitoren er tildelt en debitorkreditgruppe, og gruppens kreditmaksimum er $15.000. I dette tilfælde er debitorens gældende kreditmaksimum gruppens grænse, dvs. $15.000. Derfor blokeres eventuelle salgsordrer, der ligger over det pågældende beløb. Denne funktionalitet gør det muligt at administrere kreditmaksimum på debitorkreditgruppeniveau i stedet for på de enkelte debitorniveau. Alle kunder, der er knyttet til samme gruppe, har samme kreditmaksimum.
