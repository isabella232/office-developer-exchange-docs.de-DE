---
title: FindPeopleResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 95f016a9-002f-4be3-abd6-f5e3528afd44
description: Das FindPeopleResponse-Element gibt die Antwort auf eine FindPeople an.
ms.openlocfilehash: 4f2c2f6069a515d5153ea488b35182d8b35f029f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758475"
---
# <a name="findpeopleresponse"></a><span data-ttu-id="0eb7a-103">FindPeopleResponse</span><span class="sxs-lookup"><span data-stu-id="0eb7a-103">FindPeopleResponse</span></span>

<span data-ttu-id="0eb7a-104">Das **FindPeopleResponse** -Element gibt die Antwort auf eine **FindPeople** an.</span><span class="sxs-lookup"><span data-stu-id="0eb7a-104">The **FindPeopleResponse** element specifies the response to a **FindPeople** request.</span></span> 
  
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

 <span data-ttu-id="0eb7a-105">**FindPeopleResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0eb7a-105">**FindPeopleResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0eb7a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0eb7a-106">Attributes and elements</span></span>

<span data-ttu-id="0eb7a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0eb7a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0eb7a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0eb7a-108">Attributes</span></span>

|<span data-ttu-id="0eb7a-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0eb7a-109">**Attribute**</span></span>|<span data-ttu-id="0eb7a-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0eb7a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0eb7a-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="0eb7a-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="0eb7a-112">Gibt die Antwort-Klasse.</span><span class="sxs-lookup"><span data-stu-id="0eb7a-112">Specifies the response class.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="0eb7a-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="0eb7a-113">ResponseClass</span></span>

|<span data-ttu-id="0eb7a-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0eb7a-114">**Value**</span></span>|<span data-ttu-id="0eb7a-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0eb7a-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0eb7a-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="0eb7a-116">Success</span></span>  <br/> |<span data-ttu-id="0eb7a-117">Gibt Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="0eb7a-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="0eb7a-118">Warning</span><span class="sxs-lookup"><span data-stu-id="0eb7a-118">Warning</span></span>  <br/> |<span data-ttu-id="0eb7a-119">Gibt eine Warnung an.</span><span class="sxs-lookup"><span data-stu-id="0eb7a-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="0eb7a-120">Fehler</span><span class="sxs-lookup"><span data-stu-id="0eb7a-120">Error</span></span>  <br/> |<span data-ttu-id="0eb7a-121">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="0eb7a-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0eb7a-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0eb7a-122">Child elements</span></span>

|<span data-ttu-id="0eb7a-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="0eb7a-123">**Element**</span></span>|<span data-ttu-id="0eb7a-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0eb7a-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0eb7a-125">Personen</span><span class="sxs-lookup"><span data-stu-id="0eb7a-125">People</span></span>](people.md) <br/> |<span data-ttu-id="0eb7a-126">Gibt ein Array von Persona Daten als Ergebnis einer Anforderung **FindPeople** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0eb7a-126">Specifies an array of persona data returned as the result of a **FindPeople** request.</span></span>  <br/> |
|[<span data-ttu-id="0eb7a-127">TotalNumberOfPeopleInView</span><span class="sxs-lookup"><span data-stu-id="0eb7a-127">TotalNumberOfPeopleInView</span></span>](totalnumberofpeopleinview.md) <br/> |<span data-ttu-id="0eb7a-128">Gibt die Gesamtzahl der Rollen auf einem Server gespeichert, die durch eine **FindPeople** Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0eb7a-128">Specifies the total number of personas stored on a server that are returned by a **FindPeople** request.</span></span>  <br/> |
|[<span data-ttu-id="0eb7a-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="0eb7a-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0eb7a-130">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="0eb7a-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0eb7a-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0eb7a-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0eb7a-132">Enthält Statusinformationen über die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="0eb7a-132">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="0eb7a-133">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0eb7a-133">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0eb7a-134">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="0eb7a-134">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="0eb7a-135">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0eb7a-135">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0eb7a-136">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="0eb7a-136">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0eb7a-137">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0eb7a-137">Parent elements</span></span>

|<span data-ttu-id="0eb7a-138">**Element**</span><span class="sxs-lookup"><span data-stu-id="0eb7a-138">**Element**</span></span>|<span data-ttu-id="0eb7a-139">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0eb7a-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0eb7a-140">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0eb7a-140">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="0eb7a-141">Gibt ein Array von Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="0eb7a-141">Specifies an array of response messages.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0eb7a-142">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0eb7a-142">Remarks</span></span>

<span data-ttu-id="0eb7a-143">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0eb7a-143">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0eb7a-144">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0eb7a-144">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0eb7a-145">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0eb7a-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0eb7a-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="0eb7a-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0eb7a-147">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0eb7a-147">Schema Name</span></span>  <br/> |<span data-ttu-id="0eb7a-148">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="0eb7a-148">Message schema</span></span>  <br/> |
|<span data-ttu-id="0eb7a-149">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0eb7a-149">Validation File</span></span>  <br/> |<span data-ttu-id="0eb7a-150">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0eb7a-150">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0eb7a-151">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="0eb7a-151">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0eb7a-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0eb7a-152">See also</span></span>



- [<span data-ttu-id="0eb7a-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0eb7a-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

