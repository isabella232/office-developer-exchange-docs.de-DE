---
title: AppStatus
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f3ab8bf1-abc5-45cf-a2e1-d7602f2c24ec
description: Der Wert der AppStatus-Element gibt den Status der Mail-app.
ms.openlocfilehash: cf213fc3d7be02c411e9c2e83a4ff153dbefe098
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757369"
---
# <a name="appstatus"></a><span data-ttu-id="06804-103">AppStatus</span><span class="sxs-lookup"><span data-stu-id="06804-103">AppStatus</span></span>

<span data-ttu-id="06804-104">Der Wert der **AppStatus** -Element gibt den Status der Mail-app.</span><span class="sxs-lookup"><span data-stu-id="06804-104">The **AppStatus** element value indicates the status of the mail app.</span></span> 
  
```XML
<AppStatus/>
```

 <span data-ttu-id="06804-105">**string**</span><span class="sxs-lookup"><span data-stu-id="06804-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="06804-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="06804-106">Attributes and elements</span></span>

<span data-ttu-id="06804-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="06804-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06804-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="06804-108">Attributes</span></span>

<span data-ttu-id="06804-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="06804-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="06804-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="06804-110">Child elements</span></span>

<span data-ttu-id="06804-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="06804-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="06804-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="06804-112">Parent elements</span></span>

[<span data-ttu-id="06804-113">Metadaten</span><span class="sxs-lookup"><span data-stu-id="06804-113">Metadata</span></span>](metadata-ex15websvcsotherref.md)
  
## <a name="text-value"></a><span data-ttu-id="06804-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="06804-114">Text value</span></span>

<span data-ttu-id="06804-115">Der Textwert der **AppStatus** -Element gibt den Status der Mail-app.</span><span class="sxs-lookup"><span data-stu-id="06804-115">The text value of the **AppStatus** element indicates the status of the mail app.</span></span> <span data-ttu-id="06804-116">Wenn der Benutzer ein Problem im Zusammenhang mit den Status der Mail-app beheben kann, enthält das [ActionUrl](actionurl.md) -Element die URL, um das Update ausführen.</span><span class="sxs-lookup"><span data-stu-id="06804-116">If the user can fix an issue related to the status of the mail app, the [ActionUrl](actionurl.md) element provides the URL to perform the fix.</span></span> 
  
<span data-ttu-id="06804-117">**In Tabelle 1. AppStatus Werte**</span><span class="sxs-lookup"><span data-stu-id="06804-117">**Table 1. AppStatus values**</span></span>

|<span data-ttu-id="06804-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="06804-118">**Value**</span></span>|<span data-ttu-id="06804-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="06804-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="06804-120">NULL oder 0</span><span class="sxs-lookup"><span data-stu-id="06804-120">Null or 0</span></span>  <br/> |<span data-ttu-id="06804-121">Die Mail-app hat einen fehlerfreien Status.</span><span class="sxs-lookup"><span data-stu-id="06804-121">The mail app has a healthy status.</span></span>  <br/> |
|<span data-ttu-id="06804-122">1,0</span><span class="sxs-lookup"><span data-stu-id="06804-122">1.0</span></span>  <br/> |<span data-ttu-id="06804-123">Die Mail-app konnte nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="06804-123">The mail app could not be automatically updated.</span></span> <span data-ttu-id="06804-124">Die Mail-app muss aus dem Office Store neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="06804-124">The mail app needs to be re-installed from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="06804-125">1.1</span><span class="sxs-lookup"><span data-stu-id="06804-125">1.1</span></span>  <br/> |<span data-ttu-id="06804-126">Die Mail-app konnte nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="06804-126">The mail app could not be automatically updated.</span></span> <span data-ttu-id="06804-127">Die Mail-app erhöhte Berechtigungen benötigt, und dies erfordert die Überprüfung und Bestätigung zum Installieren.</span><span class="sxs-lookup"><span data-stu-id="06804-127">The mail app requires increased permissions, and this requires your review and confirmation to install.</span></span>  <br/> |
|<span data-ttu-id="06804-128">1.2</span><span class="sxs-lookup"><span data-stu-id="06804-128">1.2</span></span>  <br/> |<span data-ttu-id="06804-129">Die Mail-app konnte nicht automatisch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="06804-129">The mail app couldn't be updated automatically.</span></span> <span data-ttu-id="06804-130">Die aktuelle Lizenz ist abgelaufen oder ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="06804-130">The current license has expired or is invalid.</span></span> <span data-ttu-id="06804-131">Aktualisieren Sie die Mail-app aus dem Office Store.</span><span class="sxs-lookup"><span data-stu-id="06804-131">Please update the mail app from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="06804-132">2.0</span><span class="sxs-lookup"><span data-stu-id="06804-132">2.0</span></span>  <br/> |<span data-ttu-id="06804-133">Die Mail-app-Lizenz konnte nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="06804-133">The mail app license could not be automatically updated.</span></span> <span data-ttu-id="06804-134">Die Lizenz für die Mail-app muss aus dem Office Store wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="06804-134">The license for the mail app needs to be recovered from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="06804-135">2.1</span><span class="sxs-lookup"><span data-stu-id="06804-135">2.1</span></span>  <br/> |<span data-ttu-id="06804-136">Die Mail-app-Lizenz konnte nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="06804-136">The mail app license could not be automatically updated.</span></span> <span data-ttu-id="06804-137">Die aktuelle Lizenz ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="06804-137">The current license has expired.</span></span> <span data-ttu-id="06804-138">Eine neue Lizenz für diese app muss aus dem Office Store installiert werden.</span><span class="sxs-lookup"><span data-stu-id="06804-138">A new license for this app needs to be installed from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="06804-139">3.0</span><span class="sxs-lookup"><span data-stu-id="06804-139">3.0</span></span>  <br/> |<span data-ttu-id="06804-140">Der Office Store Status für die Mail-app wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="06804-140">The Office Store status for the mail app has changed.</span></span> <span data-ttu-id="06804-141">Dies kann bedeuten, dass ein mit der Mail-app Problem.</span><span class="sxs-lookup"><span data-stu-id="06804-141">This may indicate that there is a problem with the mail app.</span></span> <span data-ttu-id="06804-142">Wechseln Sie auf der Seite e-Mail-app im Office Store für Weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="06804-142">Go to the mail app page in the Office Store for more information.</span></span>  <br/> |
|<span data-ttu-id="06804-143">3.1</span><span class="sxs-lookup"><span data-stu-id="06804-143">3.1</span></span>  <br/> |<span data-ttu-id="06804-144">Die Mail-app wurde aus dem Office Store entfernt.</span><span class="sxs-lookup"><span data-stu-id="06804-144">The mail app has been removed from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="06804-145">3.2</span><span class="sxs-lookup"><span data-stu-id="06804-145">3.2</span></span>  <br/> |<span data-ttu-id="06804-146">Ein Problem mit der Mail-app ermittelt wurden und wurde aus dem Office Store vorübergehend wurde zurückgezogen.</span><span class="sxs-lookup"><span data-stu-id="06804-146">A problem has been discovered with the mail app and it has temporarily been withdrawn from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="06804-147">3.3</span><span class="sxs-lookup"><span data-stu-id="06804-147">3.3</span></span>  <br/> |<span data-ttu-id="06804-148">Innerhalb von 30 Tagen werden die Mail-app aus dem Office Store entfernt.</span><span class="sxs-lookup"><span data-stu-id="06804-148">The mail app will be removed from the Office Store within 30 days.</span></span>  <br/> |
|<span data-ttu-id="06804-149">4.0</span><span class="sxs-lookup"><span data-stu-id="06804-149">4.0</span></span>  <br/> |<span data-ttu-id="06804-150">Die Mail-app wurde automatisch durch Ihren e-Mail-Client deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="06804-150">The mail app has been automatically disabled by your mail client.</span></span>  <br/> |
|<span data-ttu-id="06804-151">4.1</span><span class="sxs-lookup"><span data-stu-id="06804-151">4.1</span></span>  <br/> |<span data-ttu-id="06804-152">Die Mail-app wurde von Outlook aus Leistungsgründen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="06804-152">The mail app has been disabled by Outlook for performance reasons.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06804-153">Hinweise</span><span class="sxs-lookup"><span data-stu-id="06804-153">Remarks</span></span>

<span data-ttu-id="06804-154">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="06804-154">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="06804-155">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="06804-155">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="06804-156">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="06804-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06804-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="06804-157">Namespace</span></span>  <br/> | http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="06804-158">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="06804-158">Schema Name</span></span>  <br/> |<span data-ttu-id="06804-159">Schematypen</span><span class="sxs-lookup"><span data-stu-id="06804-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="06804-160">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="06804-160">Validation File</span></span>  <br/> |<span data-ttu-id="06804-161">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="06804-161">Not applicable</span></span>  <br/> |
|<span data-ttu-id="06804-162">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="06804-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="06804-163">False</span><span class="sxs-lookup"><span data-stu-id="06804-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="06804-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06804-164">See also</span></span>

- [<span data-ttu-id="06804-165">Metadaten</span><span class="sxs-lookup"><span data-stu-id="06804-165">Metadata</span></span>](metadata-ex15websvcsotherref.md)
- [<span data-ttu-id="06804-166">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="06804-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

