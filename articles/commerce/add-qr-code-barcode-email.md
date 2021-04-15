---
title: Føje en QR-kode eller stregkode til transaktions- og kvitterings-mails
description: Dette emne forklarer, hvordan du indsætter QR-koder og stregkoder, der repræsenterer ordre-d'er, i transaktions- og kvitteringsmails i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: f8d9408090846799c1bb421c4b6e5e248d37fa07
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797497"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a><span data-ttu-id="3272a-103">Føje en QR-kode eller stregkode til transaktions- og kvitterings-mails</span><span class="sxs-lookup"><span data-stu-id="3272a-103">Add a QR code or bar code to transactional and receipt emails</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="3272a-104">Dette emne forklarer, hvordan du indsætter QR-koder og stregkoder, der repræsenterer ordre-d'er, i transaktions- og kvitteringsmails i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3272a-104">This topic explains how to insert QR codes and bar codes that represent order IDs into transactional and receipt emails in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3272a-105">Du kan nemt medtage QR-koder og stregkoder i transaktionsmails for at gøre ordreopslagsprocessen hurtigere i et detailmiljø.</span><span class="sxs-lookup"><span data-stu-id="3272a-105">You can easily include QR codes and bar codes in transactional emails to help speed up the order lookup process in a retail environment.</span></span> <span data-ttu-id="3272a-106">Hvis du vil indsætte QR-koder og stregkoder i mails, kan du bruge et HTML **\<img\>**-tag, der anmoder om en QR-kode eller et stregkodebillede fra en tjeneste til generering og gengivelse.</span><span class="sxs-lookup"><span data-stu-id="3272a-106">To insert QR codes and bar codes into emails, you use an HTML **\<img\>** tag that requests a QR code or bar code image from a generation and rendering service.</span></span> <span data-ttu-id="3272a-107">Microsoft leverer ikke denne tjeneste.</span><span class="sxs-lookup"><span data-stu-id="3272a-107">Microsoft doesn't provide this service.</span></span> <span data-ttu-id="3272a-108">Der findes dog mange gratis tjenester eller tjenester, der fungerer som tjenester, der fungerer som tjenester, der kan fungere som koder for QR, eller stregkoder, som genereres dynamisk på grundlag af en værdi, som overføres i en forespørgselsstreng.</span><span class="sxs-lookup"><span data-stu-id="3272a-108">However, there are many free or inexpensive services that can serve QR codes or bar codes that are dynamically generated based on a value that is passed in a query string.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a><span data-ttu-id="3272a-109">Føje en QR-kode eller stregkode til transaktions-mail</span><span class="sxs-lookup"><span data-stu-id="3272a-109">Add a QR code or bar code to a transactional email</span></span>

<span data-ttu-id="3272a-110">Hvis du vil indsætte en QR-kode eller stregkode i en transaktionsmail, der sendes som en del af et e-handelskøb, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="3272a-110">To insert a QR code or bar code into a transactional email that is sent as part of an e-commerce purchase, follow these steps.</span></span>

1. <span data-ttu-id="3272a-111">Åbn kilde-HTML-kilde-skabelonen til mailskabelonen til transaktionen, og tilføj et HTML **\<img\>**-tag, der peger på QR-koden eller stregkodetjenesten.</span><span class="sxs-lookup"><span data-stu-id="3272a-111">Open the source HTML for the transactional email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="3272a-112">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="3272a-112">Here is an example.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    <span data-ttu-id="3272a-113">Her er en forklaring på tidligere eksempler:</span><span class="sxs-lookup"><span data-stu-id="3272a-113">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="3272a-114">**DIN\_QR\_KODE\_STREG\_KODE\_TJENESTE** repræsenterer domænet for din QR-kode eller stregkodetjeneste.</span><span class="sxs-lookup"><span data-stu-id="3272a-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="3272a-115">**data** repræsenterer den parameter, som QR-koden eller stregkodetjenesten bruger til at modtage det indhold, der skal gengives som en QR-kode eller stregkode.</span><span class="sxs-lookup"><span data-stu-id="3272a-115">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="3272a-116">Værdien **%salesid%** skal tilknyttes denne parameter.</span><span class="sxs-lookup"><span data-stu-id="3272a-116">The value **%salesid%** must be assigned to this parameter.</span></span> <span data-ttu-id="3272a-117">Bemærk i dette eksempel, at værdien også bruges som alt. tekst til billedet.</span><span class="sxs-lookup"><span data-stu-id="3272a-117">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="3272a-118">**param1** og **param2** repræsenterer yderligere valgfrie parametre.</span><span class="sxs-lookup"><span data-stu-id="3272a-118">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="3272a-119">Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Skabelon til organisationsmail**, og overfør den opdaterede HTML til den relevante mailskabelon til transaktioner.</span><span class="sxs-lookup"><span data-stu-id="3272a-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the appropriate transactional email template.</span></span>

> [!NOTE]
> <span data-ttu-id="3272a-120">Parametrene kan variere mellem leverandører af QR-kode og stregkoder.</span><span class="sxs-lookup"><span data-stu-id="3272a-120">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="3272a-121">Kontakt derfor din leverandør for at bekræfte de parametre, du skal angive værdier til.</span><span class="sxs-lookup"><span data-stu-id="3272a-121">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a><span data-ttu-id="3272a-122">Føje en QR-kode eller stregkode til kvitterings-mail</span><span class="sxs-lookup"><span data-stu-id="3272a-122">Add a QR code or bar code to a receipt email</span></span> 

<span data-ttu-id="3272a-123">Hvis du vil indsætte en QR-kode eller stregkode i en kvitteringsmail, der kan sendes, efter at et køb er foretaget på POS, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="3272a-123">To insert a QR code or bar code into a receipt email that can be sent after a purchase is made at the point of sale (POS), follow these steps.</span></span>

1. <span data-ttu-id="3272a-124">Åbn kilde-HTML-kilde-skabelonen til mailskabelonen til kvitteringen, og tilføj et HTML **\<img\>**-tag, der peger på QR-koden eller stregkodetjenesten.</span><span class="sxs-lookup"><span data-stu-id="3272a-124">Open the source HTML for the receipt email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="3272a-125">Herunder følger et eksempel.</span><span class="sxs-lookup"><span data-stu-id="3272a-125">Here is an example below.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    <span data-ttu-id="3272a-126">Her er en forklaring på tidligere eksempler:</span><span class="sxs-lookup"><span data-stu-id="3272a-126">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="3272a-127">**DIN\_QR\_KODE\_STREG\_KODE\_TJENESTE** repræsenterer domænet for din QR-kode eller stregkodetjeneste.</span><span class="sxs-lookup"><span data-stu-id="3272a-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="3272a-128">**data** repræsenterer den parameter, som QR-koden eller stregkodetjenesten bruger til at modtage det indhold, der skal gengives som en QR-kode eller stregkode.</span><span class="sxs-lookup"><span data-stu-id="3272a-128">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="3272a-129">Værdien **%receiptid%** skal tilknyttes denne parameter.</span><span class="sxs-lookup"><span data-stu-id="3272a-129">The value **%receiptid%** must be assigned to this parameter.</span></span> <span data-ttu-id="3272a-130">Bemærk i dette eksempel, at værdien også bruges som alt. tekst til billedet.</span><span class="sxs-lookup"><span data-stu-id="3272a-130">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="3272a-131">**param1** og **param2** repræsenterer yderligere valgfrie parametre.</span><span class="sxs-lookup"><span data-stu-id="3272a-131">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="3272a-132">Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Skabelon til organisationsmail**, og overfør den opdaterede HTML til den mailskabelon, der indeholder mail-id **emailrecpt**.</span><span class="sxs-lookup"><span data-stu-id="3272a-132">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the email template that has the email ID **emailrecpt**.</span></span>

> [!NOTE]
> <span data-ttu-id="3272a-133">Parametrene kan variere mellem leverandører af QR-kode og stregkoder.</span><span class="sxs-lookup"><span data-stu-id="3272a-133">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="3272a-134">Kontakt derfor din leverandør for at bekræfte de parametre, du skal angive værdier til.</span><span class="sxs-lookup"><span data-stu-id="3272a-134">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3272a-135">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3272a-135">Additional resources</span></span>

[<span data-ttu-id="3272a-136">Sende mailkvitteringer fra Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="3272a-136">Send email receipts from Modern POS (MPOS)</span></span>](email-receipts.md)

[<span data-ttu-id="3272a-137">Oprette e-mailskabeloner til transaktionshændelser</span><span class="sxs-lookup"><span data-stu-id="3272a-137">Create email templates for transactional events</span></span>](email-templates-transactions.md)
