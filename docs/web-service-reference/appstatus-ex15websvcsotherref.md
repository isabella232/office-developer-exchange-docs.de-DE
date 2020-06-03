---
title: AppStatus
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f3ab8bf1-abc5-45cf-a2e1-d7602f2c24ec
description: Der Wert des AppStatus-Elements gibt den Status der Mail-APP an.
ms.openlocfilehash: d833947fd62d500418f257829d241a2e0b3bca9c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464777"
---
# <a name="appstatus"></a><span data-ttu-id="b12d8-103">AppStatus</span><span class="sxs-lookup"><span data-stu-id="b12d8-103">AppStatus</span></span>

<span data-ttu-id="b12d8-104">Der Wert des **AppStatus** -Elements gibt den Status der Mail-APP an.</span><span class="sxs-lookup"><span data-stu-id="b12d8-104">The **AppStatus** element value indicates the status of the mail app.</span></span> 
  
```XML
<AppStatus/>
```

 <span data-ttu-id="b12d8-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b12d8-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b12d8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b12d8-106">Attributes and elements</span></span>

<span data-ttu-id="b12d8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b12d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b12d8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b12d8-108">Attributes</span></span>

<span data-ttu-id="b12d8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b12d8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b12d8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b12d8-110">Child elements</span></span>

<span data-ttu-id="b12d8-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b12d8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b12d8-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b12d8-112">Parent elements</span></span>

[<span data-ttu-id="b12d8-113">Metadaten</span><span class="sxs-lookup"><span data-stu-id="b12d8-113">Metadata</span></span>](metadata-ex15websvcsotherref.md)
  
## <a name="text-value"></a><span data-ttu-id="b12d8-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="b12d8-114">Text value</span></span>

<span data-ttu-id="b12d8-115">Der Textwert des **AppStatus** -Elements gibt den Status der Mail-APP an.</span><span class="sxs-lookup"><span data-stu-id="b12d8-115">The text value of the **AppStatus** element indicates the status of the mail app.</span></span> <span data-ttu-id="b12d8-116">Wenn der Benutzer ein Problem im Zusammenhang mit dem Status der Mail-App beheben kann, stellt das [ActionUrl](actionurl.md) -Element die URL zum Durchführen des Updates bereit.</span><span class="sxs-lookup"><span data-stu-id="b12d8-116">If the user can fix an issue related to the status of the mail app, the [ActionUrl](actionurl.md) element provides the URL to perform the fix.</span></span> 
  
<span data-ttu-id="b12d8-117">**Tabelle 1. AppStatus-Werte**</span><span class="sxs-lookup"><span data-stu-id="b12d8-117">**Table 1. AppStatus values**</span></span>

|<span data-ttu-id="b12d8-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b12d8-118">**Value**</span></span>|<span data-ttu-id="b12d8-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b12d8-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b12d8-120">NULL oder 0</span><span class="sxs-lookup"><span data-stu-id="b12d8-120">Null or 0</span></span>  <br/> |<span data-ttu-id="b12d8-121">Die Mail-APP hat einen fehlerfreien Status.</span><span class="sxs-lookup"><span data-stu-id="b12d8-121">The mail app has a healthy status.</span></span>  <br/> |
|<span data-ttu-id="b12d8-122">1.0</span><span class="sxs-lookup"><span data-stu-id="b12d8-122">1.0</span></span>  <br/> |<span data-ttu-id="b12d8-123">Die Mail-App konnte nicht automatisch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b12d8-123">The mail app could not be automatically updated.</span></span> <span data-ttu-id="b12d8-124">Die Mail-app muss aus dem Office Store erneut installiert werden.</span><span class="sxs-lookup"><span data-stu-id="b12d8-124">The mail app needs to be re-installed from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="b12d8-125">1.1</span><span class="sxs-lookup"><span data-stu-id="b12d8-125">1.1</span></span>  <br/> |<span data-ttu-id="b12d8-126">Die Mail-App konnte nicht automatisch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b12d8-126">The mail app could not be automatically updated.</span></span> <span data-ttu-id="b12d8-127">Die Mail-App erfordert erhöhte Berechtigungen, und dies erfordert eine Überprüfung und Bestätigung für die Installation.</span><span class="sxs-lookup"><span data-stu-id="b12d8-127">The mail app requires increased permissions, and this requires your review and confirmation to install.</span></span>  <br/> |
|<span data-ttu-id="b12d8-128">1.2</span><span class="sxs-lookup"><span data-stu-id="b12d8-128">1.2</span></span>  <br/> |<span data-ttu-id="b12d8-129">Die Mail-App konnte nicht automatisch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b12d8-129">The mail app couldn't be updated automatically.</span></span> <span data-ttu-id="b12d8-130">Die aktuelle Lizenz ist abgelaufen oder ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b12d8-130">The current license has expired or is invalid.</span></span> <span data-ttu-id="b12d8-131">Aktualisieren Sie die Mail-App aus dem Office Store.</span><span class="sxs-lookup"><span data-stu-id="b12d8-131">Please update the mail app from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="b12d8-132">2.0</span><span class="sxs-lookup"><span data-stu-id="b12d8-132">2.0</span></span>  <br/> |<span data-ttu-id="b12d8-133">Die Mail-App-Lizenz konnte nicht automatisch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b12d8-133">The mail app license could not be automatically updated.</span></span> <span data-ttu-id="b12d8-134">Die Lizenz für die Mail-app muss aus dem Office Store wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b12d8-134">The license for the mail app needs to be recovered from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="b12d8-135">2.1</span><span class="sxs-lookup"><span data-stu-id="b12d8-135">2.1</span></span>  <br/> |<span data-ttu-id="b12d8-136">Die Mail-App-Lizenz konnte nicht automatisch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b12d8-136">The mail app license could not be automatically updated.</span></span> <span data-ttu-id="b12d8-137">Die aktuelle Lizenz ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="b12d8-137">The current license has expired.</span></span> <span data-ttu-id="b12d8-138">Eine neue Lizenz für diese APP muss aus dem Office Store installiert werden.</span><span class="sxs-lookup"><span data-stu-id="b12d8-138">A new license for this app needs to be installed from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="b12d8-139">3,0</span><span class="sxs-lookup"><span data-stu-id="b12d8-139">3.0</span></span>  <br/> |<span data-ttu-id="b12d8-140">Der Office Store Status für die Mail-App wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="b12d8-140">The Office Store status for the mail app has changed.</span></span> <span data-ttu-id="b12d8-141">Dies deutet möglicherweise darauf hin, dass ein Problem mit der Mail-App vorliegt.</span><span class="sxs-lookup"><span data-stu-id="b12d8-141">This may indicate that there is a problem with the mail app.</span></span> <span data-ttu-id="b12d8-142">Wechseln Sie zur Seite Mail-App im Office Store, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b12d8-142">Go to the mail app page in the Office Store for more information.</span></span>  <br/> |
|<span data-ttu-id="b12d8-143">3.1</span><span class="sxs-lookup"><span data-stu-id="b12d8-143">3.1</span></span>  <br/> |<span data-ttu-id="b12d8-144">Die Mail-App wurde aus dem Office Store entfernt.</span><span class="sxs-lookup"><span data-stu-id="b12d8-144">The mail app has been removed from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="b12d8-145">3.2</span><span class="sxs-lookup"><span data-stu-id="b12d8-145">3.2</span></span>  <br/> |<span data-ttu-id="b12d8-146">Es wurde ein Problem mit der Mail-App entdeckt, und es wurde vorübergehend aus dem Office Store zurückgezogen.</span><span class="sxs-lookup"><span data-stu-id="b12d8-146">A problem has been discovered with the mail app and it has temporarily been withdrawn from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="b12d8-147">3.3</span><span class="sxs-lookup"><span data-stu-id="b12d8-147">3.3</span></span>  <br/> |<span data-ttu-id="b12d8-148">Die Mail-APP wird innerhalb von 30 Tagen aus dem Office Store entfernt.</span><span class="sxs-lookup"><span data-stu-id="b12d8-148">The mail app will be removed from the Office Store within 30 days.</span></span>  <br/> |
|<span data-ttu-id="b12d8-149">4,0</span><span class="sxs-lookup"><span data-stu-id="b12d8-149">4.0</span></span>  <br/> |<span data-ttu-id="b12d8-150">Die Mail-App wurde von Ihrem e-Mail-Client automatisch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b12d8-150">The mail app has been automatically disabled by your mail client.</span></span>  <br/> |
|<span data-ttu-id="b12d8-151">4.1</span><span class="sxs-lookup"><span data-stu-id="b12d8-151">4.1</span></span>  <br/> |<span data-ttu-id="b12d8-152">Die Mail-App wurde aus Leistungsgründen von Outlook deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b12d8-152">The mail app has been disabled by Outlook for performance reasons.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b12d8-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b12d8-153">Remarks</span></span>

<span data-ttu-id="b12d8-154">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b12d8-154">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="b12d8-155">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b12d8-155">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b12d8-156">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b12d8-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b12d8-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="b12d8-157">Namespace</span></span>  <br/> | https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b12d8-158">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b12d8-158">Schema Name</span></span>  <br/> |<span data-ttu-id="b12d8-159">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b12d8-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="b12d8-160">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b12d8-160">Validation File</span></span>  <br/> |<span data-ttu-id="b12d8-161">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="b12d8-161">Not applicable</span></span>  <br/> |
|<span data-ttu-id="b12d8-162">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b12d8-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="b12d8-163">False</span><span class="sxs-lookup"><span data-stu-id="b12d8-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b12d8-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b12d8-164">See also</span></span>

- [<span data-ttu-id="b12d8-165">Metadaten</span><span class="sxs-lookup"><span data-stu-id="b12d8-165">Metadata</span></span>](metadata-ex15websvcsotherref.md)
- [<span data-ttu-id="b12d8-166">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b12d8-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

