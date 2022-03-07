---
title: Systemadministratorer kan ikke fjerne ordrehold, fordi de ikke er godkendt
description: Systemadministratorer kan ikke fjerne ordrehold, fordi de ikke er godkendt.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026388"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a>Systemadministratorer kan ikke fjerne ordrehold, fordi de ikke er godkendt

KB-nummer: 4614642

## <a name="symptoms"></a>Symptomer

Systemadministratorer kan ikke fjerne salgsordrehold, medmindre de har den specifikke rolle, der er tildelt i koden for ordreholdet.

## <a name="resolution"></a>Løsning

Adgangen til visse handlinger, f.eks. fjernelse af salgsordrehold, er baseret på konfigurationen af en forretningspolitik. Systemadministratorer har typisk ikke tilladelse til at udføre handlinger af denne type. 

Adgangen til at udføre en bestemt opgave styres oftere af forretningspolitikker, og kun bestemte personer i en organisation er godkendt til at udføre den pågældende opgave. Eksempler omfatter godkendelser, der er resultatet af godkendelser af arbejdsgange, og specifikke opgaver, der er resultatet af en arbejdsgangskonfiguration.

Selvom der ikke er knyttet nogen arbejdsgang til ordrehold, er princippet det samme. En relevant rolle tildeler den specifikke gruppe personer i en organisation, som har ret til at fjerne ordrehold. Denne rettighed skal ikke nødvendigvis tildeles til alle administratorer, da denne fremgangsmåde overtræder den definerede forretningspolitik.
