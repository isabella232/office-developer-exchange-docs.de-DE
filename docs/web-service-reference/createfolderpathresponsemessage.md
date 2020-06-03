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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458887"
---
# <a name="createfolderpathresponsemessage"></a><span data-ttu-id="665a2-103">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="665a2-103">CreateFolderPathResponseMessage</span></span>

<span data-ttu-id="665a2-104">Das **CreateFolderPathResponseMessage** -Element gibt die Antwortnachricht für eine **CreateFolderPath** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="665a2-104">The **CreateFolderPathResponseMessage** element specifies the response message for a **CreateFolderPath** request.</span></span> 
  
```XML
<CreateFolderPathResponseMessage ResponseClass="">
    <Folders></Folders>
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</CreateFolderPathResponseMessage>
```

 <span data-ttu-id="665a2-105">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="665a2-105">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="665a2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="665a2-106">Attributes and elements</span></span>

<span data-ttu-id="665a2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="665a2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="665a2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="665a2-108">Attributes</span></span>

|<span data-ttu-id="665a2-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="665a2-109">**Attribute**</span></span>|<span data-ttu-id="665a2-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="665a2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="665a2-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="665a2-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="665a2-112">Gibt die Klasse der Antwort an.</span><span class="sxs-lookup"><span data-stu-id="665a2-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="665a2-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="665a2-113">ResponseClass</span></span>

|<span data-ttu-id="665a2-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="665a2-114">**Value**</span></span>|<span data-ttu-id="665a2-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="665a2-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="665a2-116">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="665a2-116">Success</span></span>  <br/> |<span data-ttu-id="665a2-117">Gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="665a2-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="665a2-118">Warnung</span><span class="sxs-lookup"><span data-stu-id="665a2-118">Warning</span></span>  <br/> |<span data-ttu-id="665a2-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="665a2-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="665a2-120">Fehler (ungefährer Wortlaut)</span><span class="sxs-lookup"><span data-stu-id="665a2-120">Error</span></span>  <br/> |<span data-ttu-id="665a2-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="665a2-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="665a2-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="665a2-122">Child elements</span></span>

|<span data-ttu-id="665a2-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="665a2-123">**Element**</span></span>|<span data-ttu-id="665a2-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="665a2-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="665a2-125">Ordner</span><span class="sxs-lookup"><span data-stu-id="665a2-125">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="665a2-126">Enthält ein Array von Ordnern, die in Ordnervorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="665a2-126">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
|[<span data-ttu-id="665a2-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="665a2-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="665a2-128">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="665a2-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="665a2-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="665a2-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="665a2-130">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="665a2-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="665a2-131">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="665a2-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="665a2-132">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="665a2-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="665a2-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="665a2-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="665a2-134">Stellt Statusinformationen zur Anforderung bereit.</span><span class="sxs-lookup"><span data-stu-id="665a2-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="665a2-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="665a2-135">Parent elements</span></span>

|<span data-ttu-id="665a2-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="665a2-136">**Element**</span></span>|<span data-ttu-id="665a2-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="665a2-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="665a2-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="665a2-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="665a2-139">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="665a2-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="665a2-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="665a2-140">Remarks</span></span>

<span data-ttu-id="665a2-141">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="665a2-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="665a2-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="665a2-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="665a2-143">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="665a2-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="665a2-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="665a2-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="665a2-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="665a2-145">Schema Name</span></span>  <br/> |<span data-ttu-id="665a2-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="665a2-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="665a2-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="665a2-147">Validation File</span></span>  <br/> |<span data-ttu-id="665a2-148">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="665a2-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="665a2-149">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="665a2-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="665a2-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="665a2-150">See also</span></span>

- [<span data-ttu-id="665a2-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="665a2-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

