---
title: CreateFolderPathResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f7b3507-713d-4ccf-8518-75fa6f967d6d
description: Das CreateFolderPathResponseMessage-Element gibt die Antwortnachricht für eine Anforderung CreateFolderPath.
ms.openlocfilehash: f8f85cc246bb5d5ecd5cb745267d9d373286cf7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757762"
---
# <a name="createfolderpathresponsemessage"></a><span data-ttu-id="8b8c0-103">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8b8c0-103">CreateFolderPathResponseMessage</span></span>

<span data-ttu-id="8b8c0-104">Das **CreateFolderPathResponseMessage** -Element gibt die Antwortnachricht für eine Anforderung **CreateFolderPath** .</span><span class="sxs-lookup"><span data-stu-id="8b8c0-104">The **CreateFolderPathResponseMessage** element specifies the response message for a **CreateFolderPath** request.</span></span> 
  
```XML
<CreateFolderPathResponseMessage ResponseClass="">
    <Folders></Folders>
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</CreateFolderPathResponseMessage>
```

 <span data-ttu-id="8b8c0-105">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="8b8c0-105">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8b8c0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8b8c0-106">Attributes and elements</span></span>

<span data-ttu-id="8b8c0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8b8c0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8b8c0-108">Attributes</span></span>

|<span data-ttu-id="8b8c0-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8b8c0-109">**Attribute**</span></span>|<span data-ttu-id="8b8c0-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8b8c0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b8c0-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="8b8c0-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="8b8c0-112">Gibt die Klasse der Antwort.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="8b8c0-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="8b8c0-113">ResponseClass</span></span>

|<span data-ttu-id="8b8c0-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8b8c0-114">**Value**</span></span>|<span data-ttu-id="8b8c0-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8b8c0-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b8c0-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="8b8c0-116">Success</span></span>  <br/> |<span data-ttu-id="8b8c0-117">Gibt Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="8b8c0-118">Warning</span><span class="sxs-lookup"><span data-stu-id="8b8c0-118">Warning</span></span>  <br/> |<span data-ttu-id="8b8c0-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="8b8c0-120">Fehler</span><span class="sxs-lookup"><span data-stu-id="8b8c0-120">Error</span></span>  <br/> |<span data-ttu-id="8b8c0-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8b8c0-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8b8c0-122">Child elements</span></span>

|<span data-ttu-id="8b8c0-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="8b8c0-123">**Element**</span></span>|<span data-ttu-id="8b8c0-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8b8c0-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8b8c0-125">Ordner</span><span class="sxs-lookup"><span data-stu-id="8b8c0-125">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8b8c0-126">Enthält ein Array von Ordnern, die im Ordner Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-126">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
|[<span data-ttu-id="8b8c0-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8b8c0-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="8b8c0-128">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="8b8c0-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="8b8c0-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="8b8c0-130">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="8b8c0-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="8b8c0-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="8b8c0-132">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="8b8c0-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8b8c0-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="8b8c0-134">Enthält Statusinformationen über die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8b8c0-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8b8c0-135">Parent elements</span></span>

|<span data-ttu-id="8b8c0-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="8b8c0-136">**Element**</span></span>|<span data-ttu-id="8b8c0-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8b8c0-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8b8c0-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8b8c0-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="8b8c0-139">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b8c0-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8b8c0-140">Remarks</span></span>

<span data-ttu-id="8b8c0-141">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8b8c0-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8b8c0-143">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8b8c0-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8b8c0-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b8c0-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8b8c0-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8b8c0-145">Schema Name</span></span>  <br/> |<span data-ttu-id="8b8c0-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8b8c0-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="8b8c0-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8b8c0-147">Validation File</span></span>  <br/> |<span data-ttu-id="8b8c0-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8b8c0-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8b8c0-149">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8b8c0-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="8b8c0-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b8c0-150">See also</span></span>

- [<span data-ttu-id="8b8c0-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8b8c0-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

