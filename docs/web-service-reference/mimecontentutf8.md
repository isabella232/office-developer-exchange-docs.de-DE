---
title: MimeContentUTF8
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 31544c95-5231-4b57-958c-2a689464d29b
description: Das MimeContentUTF8-Element enthält den UTF-8-MIME-Stream eines Objekts, das im Format base64Binary dargestellt wird, und unterstützt die e-Mail-Adresse Internationalisierung und [RFC6530].
ms.openlocfilehash: 47599b6634738fd488e5b020f69e36d5fcf550a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830466"
---
# <a name="mimecontentutf8"></a><span data-ttu-id="09c0d-103">MimeContentUTF8</span><span class="sxs-lookup"><span data-stu-id="09c0d-103">MimeContentUTF8</span></span>

<span data-ttu-id="09c0d-104">Das **MimeContentUTF8** -Element enthält den UTF-8-MIME-Stream, der ein Objekt, wird im Format base64Binary dargestellt und unterstützt e-Mail-Adresse Internationalisierung und [[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt).</span><span class="sxs-lookup"><span data-stu-id="09c0d-104">The **MimeContentUTF8** element contains the UTF-8 MIME stream of an object that is represented in base64Binary format and supports email address internationalization and [[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt).</span></span>
  
```XML
<MimeContentUTF8 CharacterSet="" />
```

 <span data-ttu-id="09c0d-105">**MimeContentType**</span><span class="sxs-lookup"><span data-stu-id="09c0d-105">**MimeContentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="09c0d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="09c0d-106">Attributes and elements</span></span>

<span data-ttu-id="09c0d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="09c0d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="09c0d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="09c0d-108">Attributes</span></span>

|<span data-ttu-id="09c0d-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="09c0d-109">**Attribute**</span></span>|<span data-ttu-id="09c0d-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="09c0d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="09c0d-111">**UTF**</span><span class="sxs-lookup"><span data-stu-id="09c0d-111">**CharacterSet**</span></span> <br/> |<span data-ttu-id="09c0d-112">Wenn festgelegt, der Wert für dieses Attribut vom Server ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="09c0d-112">If set, the value for this attribute is ignored by the server.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="09c0d-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="09c0d-113">Child elements</span></span>

<span data-ttu-id="09c0d-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="09c0d-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="09c0d-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="09c0d-115">Parent elements</span></span>

<span data-ttu-id="09c0d-116">[CalendarItem](calendaritem.md) | [Kontakt](contact.md) | [DistributionList](distributionlist.md) | [Element](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md)  |  [ MeetingResponse](meetingresponse.md) | [Nachricht](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [Aufgabe](task.md)</span><span class="sxs-lookup"><span data-stu-id="09c0d-116">[CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Item](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [Message](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="09c0d-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="09c0d-117">Text value</span></span>

<span data-ttu-id="09c0d-118">Ein Textwert, der einen MIME-Stream base64binary darstellt ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="09c0d-118">A text value that represents a base64binary MIME stream is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="09c0d-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="09c0d-119">Remarks</span></span>

<span data-ttu-id="09c0d-120">Der Nachrichteninhalt wird über die folgenden drei Ebenen der Codierung, bevor sie den Wert des **MimeContentUTF8** gespeichert ist:</span><span class="sxs-lookup"><span data-stu-id="09c0d-120">The message content goes through the following three levels of encoding before it is stored in the **MimeContentUTF8** value:</span></span> 
  
1. <span data-ttu-id="09c0d-121">Meldungstext – Dies ist der Textkörper Codierung, z. B. Iso-2022-jp für japanischen Schriftzeichen.</span><span class="sxs-lookup"><span data-stu-id="09c0d-121">Message text — This is the body encoding, such as iso-2022-jp for Japanese characters.</span></span>
    
2. <span data-ttu-id="09c0d-122">MIME-Stream – Dies ist die UTF8-Codierung des Nachrichtentext für das **MimeContentUTF8** -Element oder die ASCII-Codierung von den Nachrichtentext für das Element [' MimeContent '](mimecontent.md) .</span><span class="sxs-lookup"><span data-stu-id="09c0d-122">MIME stream — This is the UTF8 encoding of the message text for the **MimeContentUTF8** element, or the ASCII encoding of the message text for the [MimeContent](mimecontent.md) element.</span></span> 
    
3. <span data-ttu-id="09c0d-123">XML-Dokument – ist dies stets die base64-codierten ASCII-Stream des MIME-Streams, in dem Zeichen wie '\<', welche zu XML, benötigt werden, werden aus XML-Parser ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="09c0d-123">XML document — This is always the base64-encoded ASCII stream of the MIME stream, where characters such as '\<', which are meaningful to XML, are hidden from XML parsers.</span></span>
    
<span data-ttu-id="09c0d-124">Jede Ebene ist unabhängig von der Ebene, die er vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="09c0d-124">Each level is independent of the level that precedes it.</span></span>
  
<span data-ttu-id="09c0d-125">Das **MimeContentUTF8** -Element kann die gleichen Daten enthalten, die anderen Eigenschaften, die mit einem Element zurückgegeben werden enthalten.</span><span class="sxs-lookup"><span data-stu-id="09c0d-125">The **MimeContentUTF8** element might contain the same data that other properties that are returned with an item contain.</span></span> 
  
<span data-ttu-id="09c0d-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="09c0d-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="09c0d-127">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="09c0d-127">Version differences</span></span>

<span data-ttu-id="09c0d-128">Dieses Element ist in Versionen von Exchange, beginnend mit Build 15.00.0986.00 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="09c0d-128">This element is available in versions of Exchange starting with build 15.00.0986.00.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="09c0d-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="09c0d-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09c0d-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="09c0d-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="09c0d-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="09c0d-131">Schema Name</span></span>  <br/> |<span data-ttu-id="09c0d-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="09c0d-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="09c0d-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="09c0d-133">Validation File</span></span>  <br/> |<span data-ttu-id="09c0d-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="09c0d-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="09c0d-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="09c0d-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="09c0d-136">False</span><span class="sxs-lookup"><span data-stu-id="09c0d-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09c0d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09c0d-137">See also</span></span>



- [<span data-ttu-id="09c0d-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="09c0d-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

