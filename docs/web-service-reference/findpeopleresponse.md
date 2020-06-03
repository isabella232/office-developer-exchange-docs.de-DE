---
title: FindPeopleResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 95f016a9-002f-4be3-abd6-f5e3528afd44
description: Das FindPeopleResponse-Element gibt die Antwort auf eine FindPeople-Anforderung an.
ms.openlocfilehash: b969ac3f7bc2bbd3fc77bf753a15696c3b6d8216
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466402"
---
# <a name="findpeopleresponse"></a><span data-ttu-id="945b2-103">FindPeopleResponse</span><span class="sxs-lookup"><span data-stu-id="945b2-103">FindPeopleResponse</span></span>

<span data-ttu-id="945b2-104">Das **FindPeopleResponse** -Element gibt die Antwort auf eine **FindPeople** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="945b2-104">The **FindPeopleResponse** element specifies the response to a **FindPeople** request.</span></span> 
  
```XML
<FindPeopleResponse ResponseClass=" Success | Warning | Error ">
    <People/>
    <TotalNumberOfPeopleInView/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</FindPeopleResponse>
```

 <span data-ttu-id="945b2-105">**FindPeopleResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="945b2-105">**FindPeopleResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="945b2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="945b2-106">Attributes and elements</span></span>

<span data-ttu-id="945b2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="945b2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="945b2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="945b2-108">Attributes</span></span>

|<span data-ttu-id="945b2-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="945b2-109">**Attribute**</span></span>|<span data-ttu-id="945b2-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="945b2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="945b2-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="945b2-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="945b2-112">Gibt die Antwort Klasse an.</span><span class="sxs-lookup"><span data-stu-id="945b2-112">Specifies the response class.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="945b2-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="945b2-113">ResponseClass</span></span>

|<span data-ttu-id="945b2-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="945b2-114">**Value**</span></span>|<span data-ttu-id="945b2-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="945b2-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="945b2-116">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="945b2-116">Success</span></span>  <br/> |<span data-ttu-id="945b2-117">Gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="945b2-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="945b2-118">Warnung</span><span class="sxs-lookup"><span data-stu-id="945b2-118">Warning</span></span>  <br/> |<span data-ttu-id="945b2-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="945b2-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="945b2-120">Fehler (ungefährer Wortlaut)</span><span class="sxs-lookup"><span data-stu-id="945b2-120">Error</span></span>  <br/> |<span data-ttu-id="945b2-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="945b2-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="945b2-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="945b2-122">Child elements</span></span>

|<span data-ttu-id="945b2-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="945b2-123">**Element**</span></span>|<span data-ttu-id="945b2-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="945b2-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="945b2-125">Personen</span><span class="sxs-lookup"><span data-stu-id="945b2-125">People</span></span>](people.md) <br/> |<span data-ttu-id="945b2-126">Gibt ein Array von Persona-Daten an, die als Ergebnis einer **FindPeople** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="945b2-126">Specifies an array of persona data returned as the result of a **FindPeople** request.</span></span>  <br/> |
|[<span data-ttu-id="945b2-127">TotalNumberOfPeopleInView</span><span class="sxs-lookup"><span data-stu-id="945b2-127">TotalNumberOfPeopleInView</span></span>](totalnumberofpeopleinview.md) <br/> |<span data-ttu-id="945b2-128">Gibt die Gesamtzahl der auf einem Server gespeicherten Personen an, die von einer **FindPeople** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="945b2-128">Specifies the total number of personas stored on a server that are returned by a **FindPeople** request.</span></span>  <br/> |
|[<span data-ttu-id="945b2-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="945b2-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="945b2-130">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="945b2-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="945b2-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="945b2-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="945b2-132">Stellt Statusinformationen zur Anforderung bereit.</span><span class="sxs-lookup"><span data-stu-id="945b2-132">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="945b2-133">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="945b2-133">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="945b2-134">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="945b2-134">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="945b2-135">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="945b2-135">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="945b2-136">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="945b2-136">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="945b2-137">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="945b2-137">Parent elements</span></span>

|<span data-ttu-id="945b2-138">**Element**</span><span class="sxs-lookup"><span data-stu-id="945b2-138">**Element**</span></span>|<span data-ttu-id="945b2-139">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="945b2-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="945b2-140">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="945b2-140">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="945b2-141">Gibt ein Array von Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="945b2-141">Specifies an array of response messages.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="945b2-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="945b2-142">Remarks</span></span>

<span data-ttu-id="945b2-143">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="945b2-143">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="945b2-144">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="945b2-144">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="945b2-145">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="945b2-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="945b2-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="945b2-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="945b2-147">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="945b2-147">Schema Name</span></span>  <br/> |<span data-ttu-id="945b2-148">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="945b2-148">Message schema</span></span>  <br/> |
|<span data-ttu-id="945b2-149">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="945b2-149">Validation File</span></span>  <br/> |<span data-ttu-id="945b2-150">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="945b2-150">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="945b2-151">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="945b2-151">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="945b2-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="945b2-152">See also</span></span>



- [<span data-ttu-id="945b2-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="945b2-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

