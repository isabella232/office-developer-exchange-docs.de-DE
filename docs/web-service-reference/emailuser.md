---
title: EmailUser
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc8133ff-c34e-4921-bb56-06e79aee0a8a
description: Das EmailUser-Element gibt einen e-Mail-Empfänger.
ms.openlocfilehash: e724b3996d37a42527ec1183cef9bb6b312b8c93
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758208"
---
# <a name="emailuser"></a><span data-ttu-id="2055d-103">EmailUser</span><span class="sxs-lookup"><span data-stu-id="2055d-103">EmailUser</span></span>

<span data-ttu-id="2055d-104">Das **EmailUser** -Element gibt einen e-Mail-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="2055d-104">The **EmailUser** element specifies an email recipient.</span></span> 
  
```XML
<EmailUser>
    <Name/>
    <UserId/>
</EmailUser>
```

 <span data-ttu-id="2055d-105">**EmailUserType**</span><span class="sxs-lookup"><span data-stu-id="2055d-105">**EmailUserType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2055d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2055d-106">Attributes and elements</span></span>

<span data-ttu-id="2055d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2055d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2055d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2055d-108">Attributes</span></span>

<span data-ttu-id="2055d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2055d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2055d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2055d-110">Child elements</span></span>

|<span data-ttu-id="2055d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2055d-111">**Element**</span></span>|<span data-ttu-id="2055d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2055d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2055d-113">Name (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="2055d-113">Name (string)</span></span>](name-string.md) <br/> |<span data-ttu-id="2055d-114">Gibt einen Suchbegriff Einschränkung und Schlüssel oder den Namen eines e-Mail-Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="2055d-114">Specifies a search refiner name or key or the name of an email user.</span></span>  <br/> |
|[<span data-ttu-id="2055d-115">Benutzer-ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="2055d-115">UserId (string)</span></span>](userid-string.md) <br/> |<span data-ttu-id="2055d-116">Gibt die Benutzer-ID eines e-Mail-Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="2055d-116">Specifies the user identifier of an email user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2055d-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2055d-117">Parent elements</span></span>

|<span data-ttu-id="2055d-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="2055d-118">**Element**</span></span>|<span data-ttu-id="2055d-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2055d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2055d-120">Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="2055d-120">Attendees</span></span>](attendees.md) <br/> |<span data-ttu-id="2055d-121">Gibt die Empfänger einer Einladung zu einer Besprechung.</span><span class="sxs-lookup"><span data-stu-id="2055d-121">Specifies the recipients of an invitation to a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2055d-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2055d-122">Remarks</span></span>

<span data-ttu-id="2055d-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2055d-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2055d-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2055d-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2055d-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2055d-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2055d-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="2055d-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2055d-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2055d-127">Schema Name</span></span>  <br/> |<span data-ttu-id="2055d-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="2055d-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="2055d-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2055d-129">Validation File</span></span>  <br/> |<span data-ttu-id="2055d-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2055d-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2055d-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2055d-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2055d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2055d-132">See also</span></span>



- [<span data-ttu-id="2055d-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2055d-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

