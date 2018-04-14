---
title: Udvide funktionaliteten i Microsoft Dynamics 365 for Talent
description: Hvis du har oprettet Microsoft PowerApps, kan du starte disse programmer fra hyperlinks i Microsoft Dynamics 365 for Talent.
author: rschloma
manager: AnnBe
ms.date: 11/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c606ea957c5d6347d275cb9f29a6ac12c00a0137
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="06e0a-103">Udvide funktionaliteten i Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="06e0a-103">Extend the functionality of Microsoft Dynamics 365 for Talent</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="06e0a-104">Hvis du har oprettet Microsoft PowerApps, kan du starte disse programmer fra hyperlinks i Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="06e0a-104">If you’ve created any Microsoft PowerApps, you can start those applications from links within Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="06e0a-105">Når du vil oprette adgang til dine programmer, skal du angive nogle oplysninger i Talent på en konfigurationsside, som du kan åbne fra arbejdsområdet **Systemadministration**.</span><span class="sxs-lookup"><span data-stu-id="06e0a-105">To set up access to your applications, you’ll need to set up some information in Talent on a configuration page that you can open from the **System administration** workspace.</span></span>

## <a name="configuring-embedded-powerapps-within-talent"></a><span data-ttu-id="06e0a-106">Konfiguration af integrerede PowerApps i Talent</span><span class="sxs-lookup"><span data-stu-id="06e0a-106">Configuring embedded PowerApps within Talent</span></span>
<span data-ttu-id="06e0a-107">Brug siden **Indstil integrerede Microsoft PowerApps** til at konfigurere Talent-sider for at starte PowerApps-programmer.</span><span class="sxs-lookup"><span data-stu-id="06e0a-107">Use the **Set embedded Microsoft PowerApps** page to configure Talent pages to start PowerApps applications.</span></span> <span data-ttu-id="06e0a-108">Du kan åbne siden **Indstil integrerede Microsoft PowerApps** ved at åbne arbejdsområdet **Systemadministration** og derefter åbne fanen **Links**. Vælg **Microsoft PowerApps** i gruppen **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="06e0a-108">To open the **Set embedded Microsoft PowerApps** page, open the **System administration** workspace and then open the **Links** tab. Select **Microsoft PowerApps** from the **Setup** group.</span></span> 

<span data-ttu-id="06e0a-109">Følgende oplysninger angives eller indstilles på denne side:</span><span class="sxs-lookup"><span data-stu-id="06e0a-109">The following information is entered or set on this page:</span></span> 

> - <span data-ttu-id="06e0a-110">Et beskrivende navn eller id til hvert PowerApps-program.</span><span class="sxs-lookup"><span data-stu-id="06e0a-110">A descriptive name or identifier for each PowerApps application.</span></span>
> - <span data-ttu-id="06e0a-111">Et entydigt id (GUID) for hvert program, du føjer til en Talent-side.</span><span class="sxs-lookup"><span data-stu-id="06e0a-111">A unique identifier (GUID) for each application that you add to a Talent page.</span></span> <span data-ttu-id="06e0a-112">Program-id'et findes på webstedet PowerApps-webstedet [powerapps.com](http://powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="06e0a-112">The app ID is available on the PowerApps site, [powerapps.com](http://powerapps.com/).</span></span> 
> - <span data-ttu-id="06e0a-113">Den side, hvorfra brugere kan åbne et program eller en rapport.</span><span class="sxs-lookup"><span data-stu-id="06e0a-113">The page from which users can open an application or report.</span></span> <span data-ttu-id="06e0a-114">Ikke alle Talent-sider understøtter integrerede PowerApps og Power BI-rapporter.</span><span class="sxs-lookup"><span data-stu-id="06e0a-114">Not all Talent pages support embedded PowerApps and Power BI reports.</span></span> 
> 
> [!NOTE]
>  <span data-ttu-id="06e0a-115">Angiv det interne navn på siden i stedet for det viste navn, der vises øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="06e0a-115">Enter the internal name of the page, rather than the display name that appears at the top of the page.</span></span> <span data-ttu-id="06e0a-116">Du kan finde det interne navn ved at åbne den side, du skal bruge interne navn på, og højreklikke på et vilkårligt sted på siden.</span><span class="sxs-lookup"><span data-stu-id="06e0a-116">To find the internal name, open the page that you need the internal name of, and right-click anywhere on the page.</span></span> <span data-ttu-id="06e0a-117">Når menuen åbnes, skal du pege på elementet **Oplysninger om formular**.</span><span class="sxs-lookup"><span data-stu-id="06e0a-117">When the menu opens, hover over the **Form information** item.</span></span> <span data-ttu-id="06e0a-118">Det interne formularnavn, der vises ud for elementet **Oplysninger om formular** i menuen.</span><span class="sxs-lookup"><span data-stu-id="06e0a-118">The internal form name is displayed next to the **Form information** item in the menu.</span></span>
> 
> - <span data-ttu-id="06e0a-119">Angiv det kontrolelement i formularen, som programmet kan hente kontekstdata fra.</span><span class="sxs-lookup"><span data-stu-id="06e0a-119">Specify the form control from which the application can retrieve context data.</span></span> <span data-ttu-id="06e0a-120">Et program kan for eksempel bruge data om en arbejder.</span><span class="sxs-lookup"><span data-stu-id="06e0a-120">For example, an application might use data about a worker.</span></span> <span data-ttu-id="06e0a-121">Hvis du angiver siden **Arbejder** i feltet **Kontekst**, åbnes siden **Arbejder**, når du starter programmet.</span><span class="sxs-lookup"><span data-stu-id="06e0a-121">If you enter the **Worker** page in the **Context** field, the **Worker** page will open when you start the application.</span></span> <span data-ttu-id="06e0a-122">En post i **Kontekstfelt** er valgfri.</span><span class="sxs-lookup"><span data-stu-id="06e0a-122">An entry in the **Context field** is optional.</span></span> 
> - <span data-ttu-id="06e0a-123">Angiv størrelsen på den dialogboks, hvor PowerApps-programmet skal køre.</span><span class="sxs-lookup"><span data-stu-id="06e0a-123">Set the size of the dialog box on which the PowerApps application will run.</span></span> <span data-ttu-id="06e0a-124">Dialogboksene er angivet som "små" eller "store" for at optimere brugergrænsefladen, når programmet kører på henholdsvis en telefon eller en større enhed.</span><span class="sxs-lookup"><span data-stu-id="06e0a-124">The dialog boxes are designated as “small” or “large” to optimize the user interface when your application for running on a phone or a larger device, respectively.</span></span> 

<span data-ttu-id="06e0a-125">Du kan også angive, hvilke juridiske enheder et program er tilgængeligt til, eller du kan gøre det tilgængeligt for alle juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="06e0a-125">You can also specify which legal entities an application will be available for, or you can make it available to all your legal entities.</span></span> <span data-ttu-id="06e0a-126">PowerApps-programmerne er som standard tilgængelige for alle juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="06e0a-126">By default, your PowerApps applications are available to all legal entities.</span></span>

## <a name="opening-an-application"></a><span data-ttu-id="06e0a-127">Åbning af et program</span><span class="sxs-lookup"><span data-stu-id="06e0a-127">Opening an application</span></span>
<span data-ttu-id="06e0a-128">Når du har konfigureret integrerede PowerApps-programmer, føjes links til de programmer, du har angivet, til siderne i Talent.</span><span class="sxs-lookup"><span data-stu-id="06e0a-128">When you’ve configured embedded PowerApps applications, links to the applications that you specified will be added to the pages within Talent.</span></span> <span data-ttu-id="06e0a-129">Klik på et link for at åbne et program.</span><span class="sxs-lookup"><span data-stu-id="06e0a-129">Click a link to open an application.</span></span> 



