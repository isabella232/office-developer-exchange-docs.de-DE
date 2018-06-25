---
title: "' MimeContent '"
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MimeContent
api_type:
- schema
ms.assetid: 4f472a08-5653-4c54-ba65-831dfe32f20f
description: Das Element ' MimeContent ' enthält den ASCII-MIME-Stream eines Objekts, das im Format base64Binary dargestellt ist und unterstützt [RFC2045].
ms.openlocfilehash: 60f2d42f09347611559137c494d93036f1192829
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830465"
---
# <a name="mimecontent"></a><span data-ttu-id="9fbc6-103">' MimeContent '</span><span class="sxs-lookup"><span data-stu-id="9fbc6-103">MimeContent</span></span>

<span data-ttu-id="9fbc6-104">Das Element **' MimeContent '** enthält den ASCII-MIME-Stream eines Objekts, das im Format base64Binary dargestellt ist und unterstützt [[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt).</span><span class="sxs-lookup"><span data-stu-id="9fbc6-104">The **MimeContent** element contains the ASCII MIME stream of an object that is represented in base64Binary format and supports [[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt).</span></span>
  
```xml
<MimeContent CharacterSet="" />
```

 <span data-ttu-id="9fbc6-105">**MimeContentType**</span><span class="sxs-lookup"><span data-stu-id="9fbc6-105">**MimeContentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9fbc6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9fbc6-106">Attributes and elements</span></span>

<span data-ttu-id="9fbc6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9fbc6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9fbc6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9fbc6-108">Attributes</span></span>

|<span data-ttu-id="9fbc6-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9fbc6-109">**Attribute**</span></span>|<span data-ttu-id="9fbc6-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9fbc6-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9fbc6-111">**UTF**</span><span class="sxs-lookup"><span data-stu-id="9fbc6-111">**CharacterSet**</span></span> <br/> |<span data-ttu-id="9fbc6-112">Wenn festgelegt, der Wert für dieses Attribut vom Server ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="9fbc6-112">If set, the value for this attribute is ignored by the server.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9fbc6-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9fbc6-113">Child elements</span></span>

<span data-ttu-id="9fbc6-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="9fbc6-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9fbc6-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9fbc6-115">Parent elements</span></span>

<span data-ttu-id="9fbc6-116">[CalendarItem](calendaritem.md) | [Kontakt](contact.md) | [DistributionList](distributionlist.md) | [Element](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md)  |  [ MeetingResponse](meetingresponse.md) | [Nachricht](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [Aufgabe](task.md)</span><span class="sxs-lookup"><span data-stu-id="9fbc6-116">[CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Item](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [Message](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="9fbc6-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="9fbc6-117">Text value</span></span>

<span data-ttu-id="9fbc6-118">Ein Textwert, der einen MIME-Stream base64Binary darstellt ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9fbc6-118">A text value that represents a base64Binary MIME stream is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9fbc6-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9fbc6-119">Remarks</span></span>

<span data-ttu-id="9fbc6-120">Der Nachrichteninhalt wird über die folgenden drei Ebenen der Codierung, bevor sie den Wert **' MimeContent '** gespeichert ist:</span><span class="sxs-lookup"><span data-stu-id="9fbc6-120">The message content goes through the following three levels of encoding before it is stored in the **MimeContent** value:</span></span> 
  
1. <span data-ttu-id="9fbc6-121">Meldungstext – Dies ist der Textkörper Codierung, z. B. Iso-2022-jp für japanischen Schriftzeichen.</span><span class="sxs-lookup"><span data-stu-id="9fbc6-121">Message text — This is the body encoding, such as iso-2022-jp for Japanese characters.</span></span>
    
2. <span data-ttu-id="9fbc6-122">MIME-Stream – Dies ist die ASCII-Codierung des Texts für das Element **' MimeContent '** Nachricht oder UTF8-Codierung von den Nachrichtentext für das [MimeContentUTF8](mimecontentutf8.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="9fbc6-122">MIME stream — This is the ASCII encoding of the message text for the **MimeContent** element, or the UTF8 encoding of the message text for the [MimeContentUTF8](mimecontentutf8.md) element.</span></span> 
    
3. <span data-ttu-id="9fbc6-123">XML-Dokument – ist dies stets die base64-codierten ASCII-Stream des MIME-Streams, in dem Zeichen wie '\<', welche zu XML, benötigt werden, werden aus XML-Parser ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="9fbc6-123">XML document — This is always the base64-encoded ASCII stream of the MIME stream, where characters such as '\<', which are meaningful to XML, are hidden from XML parsers.</span></span>
    
<span data-ttu-id="9fbc6-124">Jede Ebene ist unabhängig von der Ebene, die er vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="9fbc6-124">Each level is independent of the level that precedes it.</span></span>
  
<span data-ttu-id="9fbc6-125">Das Element **' MimeContent '** möglicherweise die gleichen Daten enthalten, die anderen Eigenschaften, die mit einem Element zurückgegeben werden enthalten.</span><span class="sxs-lookup"><span data-stu-id="9fbc6-125">The **MimeContent** element might contain the same data that other properties that are returned with an item contain.</span></span> 
  
<span data-ttu-id="9fbc6-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9fbc6-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9fbc6-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9fbc6-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fbc6-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="9fbc6-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9fbc6-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9fbc6-129">Schema Name</span></span>  <br/> |<span data-ttu-id="9fbc6-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9fbc6-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="9fbc6-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9fbc6-131">Validation File</span></span>  <br/> |<span data-ttu-id="9fbc6-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9fbc6-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9fbc6-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9fbc6-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="9fbc6-134">False</span><span class="sxs-lookup"><span data-stu-id="9fbc6-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9fbc6-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fbc6-135">See also</span></span>



- [<span data-ttu-id="9fbc6-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9fbc6-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

