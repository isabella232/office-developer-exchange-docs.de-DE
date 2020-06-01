---
title: CreateFolderPathResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f7b3507-713d-4ccf-8518-75fa6f967d6d
description: Das CreateFolderPathResponseMessage-Element gibt die Antwortnachricht für eine CreateFolderPath-Anforderung an.
ms.openlocfilehash: 3c0c4e98b568a6398dcd0e71a6e6931a3f47e3da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458887"
---
# <a name="createfolderpathresponsemessage"></a><span data-ttu-id="0d611-103">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0d611-103">CreateFolderPathResponseMessage</span></span>

<span data-ttu-id="0d611-104">Das **CreateFolderPathResponseMessage** -Element gibt die Antwortnachricht für eine **CreateFolderPath** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="0d611-104">The **CreateFolderPathResponseMessage** element specifies the response message for a **CreateFolderPath** request.</span></span> 
  
```XML
<CreateFolderPathResponseMessage ResponseClass="">
    <Folders></Folders>
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</CreateFolderPathResponseMessage>
```

 <span data-ttu-id="0d611-105">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0d611-105">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0d611-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0d611-106">Attributes and elements</span></span>

<span data-ttu-id="0d611-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0d611-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d611-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0d611-108">Attributes</span></span>

|<span data-ttu-id="0d611-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0d611-109">**Attribute**</span></span>|<span data-ttu-id="0d611-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d611-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0d611-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="0d611-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="0d611-112">Gibt die Klasse der Antwort an.</span><span class="sxs-lookup"><span data-stu-id="0d611-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="0d611-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="0d611-113">ResponseClass</span></span>

|<span data-ttu-id="0d611-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0d611-114">**Value**</span></span>|<span data-ttu-id="0d611-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d611-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0d611-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="0d611-116">Success</span></span>  <br/> |<span data-ttu-id="0d611-117">Gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="0d611-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="0d611-118">Warnung</span><span class="sxs-lookup"><span data-stu-id="0d611-118">Warning</span></span>  <br/> |<span data-ttu-id="0d611-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="0d611-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="0d611-120">Fehler (ungefährer Wortlaut)</span><span class="sxs-lookup"><span data-stu-id="0d611-120">Error</span></span>  <br/> |<span data-ttu-id="0d611-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="0d611-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0d611-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d611-122">Child elements</span></span>

|<span data-ttu-id="0d611-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d611-123">**Element**</span></span>|<span data-ttu-id="0d611-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d611-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d611-125">Ordner</span><span class="sxs-lookup"><span data-stu-id="0d611-125">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0d611-126">Enthält ein Array von Ordnern, die in Ordnervorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d611-126">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
|[<span data-ttu-id="0d611-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0d611-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0d611-128">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="0d611-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="0d611-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="0d611-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0d611-130">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="0d611-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0d611-131">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="0d611-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0d611-132">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="0d611-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="0d611-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0d611-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0d611-134">Stellt Statusinformationen zur Anforderung bereit.</span><span class="sxs-lookup"><span data-stu-id="0d611-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0d611-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d611-135">Parent elements</span></span>

|<span data-ttu-id="0d611-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d611-136">**Element**</span></span>|<span data-ttu-id="0d611-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d611-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d611-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0d611-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="0d611-139">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="0d611-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d611-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d611-140">Remarks</span></span>

<span data-ttu-id="0d611-141">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0d611-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0d611-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0d611-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d611-143">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0d611-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d611-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d611-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0d611-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0d611-145">Schema Name</span></span>  <br/> |<span data-ttu-id="0d611-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="0d611-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="0d611-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0d611-147">Validation File</span></span>  <br/> |<span data-ttu-id="0d611-148">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0d611-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0d611-149">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="0d611-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0d611-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d611-150">See also</span></span>

- [<span data-ttu-id="0d611-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0d611-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

