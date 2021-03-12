---
title: NF-e-brugerdefineret certifikatvalidering
description: Dette emne giver oplysninger om aktivering og brug af det brugerdefinerede NF-e-certifikat.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f13e8b8229bbd9e174e5bde7858a468048ba309b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990080"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="85d31-103">NF-e-brugerdefineret certifikatvalidering</span><span class="sxs-lookup"><span data-stu-id="85d31-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85d31-104">Når du aktiverer NF-e-brugerdefineret certifikatkontrolfunktionen, giver brugerdefineret validering en forbindelse til webtjenesterne.</span><span class="sxs-lookup"><span data-stu-id="85d31-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="85d31-105">Denne forbindelse er påkrævet for at overføre NF-e og modtage autorisation fra SEFAZ.</span><span class="sxs-lookup"><span data-stu-id="85d31-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="85d31-106">Egenskaben **Formål for servergodkendelse** fra certifikatet V5 udstedes af det brasilianske rodnøglecenter.</span><span class="sxs-lookup"><span data-stu-id="85d31-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="85d31-107">Denne egenskab er deaktiveret som standard og skal aktiveres manuelt.</span><span class="sxs-lookup"><span data-stu-id="85d31-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="85d31-108">I nogle tilfælde kan den automatiske certifikatopdatering ændre denne egenskab, så den ikke længere er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="85d31-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="85d31-109">Hvis dette sker, påvirkes TLS-forbindelsen og er ikke længere pålidelig.</span><span class="sxs-lookup"><span data-stu-id="85d31-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="85d31-110">Muligheden for at udstede NF-e i produktionsmiljøer for tilstande af Minas Gerais (MG) og Paraná (PR) påvirkes også.</span><span class="sxs-lookup"><span data-stu-id="85d31-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="85d31-111">Denne opdatering giver mulighed for en alternativ løsning til certifikatvalidering, hvilket betyder, at det er muligt at oprette en sikker kommunikation.</span><span class="sxs-lookup"><span data-stu-id="85d31-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>


