---
title: Teilnehmer
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 837bb372-39eb-48ae-9c09-0d2552511f93
description: Das attenders-Element gibt die Empfänger einer Einladung zu einer Besprechung an.
ms.openlocfilehash: 3a63bdf7e49309697ac503be5f4c95eb805b9635
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460330"
---
# <a name="attendees"></a><span data-ttu-id="974bd-103">Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="974bd-103">Attendees</span></span>

<span data-ttu-id="974bd-104">Das **attenders** -Element gibt die Empfänger einer Einladung zu einer Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="974bd-104">The **Attendees** element specifies the recipients of an invitation to a meeting.</span></span> 
  
```XML
<Attendees>
    <EmailUser></EmailUser>
</Attendees>
```

 <span data-ttu-id="974bd-105">**ArrayOfEmailUsersType**</span><span class="sxs-lookup"><span data-stu-id="974bd-105">**ArrayOfEmailUsersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="974bd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="974bd-106">Attributes and elements</span></span>

<span data-ttu-id="974bd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="974bd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="974bd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="974bd-108">Attributes</span></span>

<span data-ttu-id="974bd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="974bd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="974bd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="974bd-110">Child elements</span></span>

|<span data-ttu-id="974bd-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="974bd-111">**Element**</span></span>|<span data-ttu-id="974bd-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="974bd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="974bd-113">EmailUser</span><span class="sxs-lookup"><span data-stu-id="974bd-113">EmailUser</span></span>](emailuser.md) <br/> |<span data-ttu-id="974bd-114">Gibt einen e-Mail-Empfänger oder Active Directory Kontakt an.</span><span class="sxs-lookup"><span data-stu-id="974bd-114">Specifies an email recipient or Active Directory contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="974bd-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="974bd-115">Parent elements</span></span>

|<span data-ttu-id="974bd-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="974bd-116">**Element**</span></span>|<span data-ttu-id="974bd-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="974bd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="974bd-118">MeetingSuggestion</span><span class="sxs-lookup"><span data-stu-id="974bd-118">MeetingSuggestion</span></span>](meetingsuggestion.md) <br/> |<span data-ttu-id="974bd-119">Gibt eine vorgeschlagene Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="974bd-119">Specifies a proposed meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="974bd-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="974bd-120">Remarks</span></span>

<span data-ttu-id="974bd-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="974bd-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="974bd-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="974bd-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="974bd-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="974bd-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="974bd-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="974bd-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="974bd-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="974bd-125">Schema Name</span></span>  <br/> |<span data-ttu-id="974bd-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="974bd-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="974bd-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="974bd-127">Validation File</span></span>  <br/> |<span data-ttu-id="974bd-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="974bd-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="974bd-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="974bd-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="974bd-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="974bd-130">See also</span></span>

- [<span data-ttu-id="974bd-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="974bd-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

