---
title: OutOfOffice
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OutOfOffice
api_type:
- schema
ms.assetid: fe1256ab-5c0f-467d-abb3-b38a2dc312ae
description: Das OutOfOffice-Element stellt die Antwortnachricht und eine Dauer für das Senden der Antwortnachricht dar.
ms.openlocfilehash: 082a81b62e2b783b302b3e749e0066131a46d73e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456899"
---
# <a name="outofoffice"></a><span data-ttu-id="83285-103">OutOfOffice</span><span class="sxs-lookup"><span data-stu-id="83285-103">OutOfOffice</span></span>

<span data-ttu-id="83285-104">Das **OutOfOffice** -Element stellt die Antwortnachricht und eine Dauer für das Senden der Antwortnachricht dar.</span><span class="sxs-lookup"><span data-stu-id="83285-104">The **OutOfOffice** element represents the response message and a duration time for sending the response message.</span></span> 
  
```XML
<OutOfOffice>
   <ReplyBody/>
   <Duration/>
</OutOfOffice>
```

```XML
<OutOfOffice>
   <ReplyBody/>
</OutOfOffice>
```

<span data-ttu-id="83285-105">**OutOfOfficeMailTip**</span><span class="sxs-lookup"><span data-stu-id="83285-105">**OutOfOfficeMailTip**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="83285-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="83285-106">Attributes and elements</span></span>

<span data-ttu-id="83285-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="83285-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83285-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="83285-108">Attributes</span></span>

<span data-ttu-id="83285-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="83285-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83285-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83285-110">Child elements</span></span>

|<span data-ttu-id="83285-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="83285-111">**Element**</span></span>|<span data-ttu-id="83285-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83285-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83285-113">ReplyBody</span><span class="sxs-lookup"><span data-stu-id="83285-113">ReplyBody</span></span>](replybody.md) <br/> |<span data-ttu-id="83285-114">Enthält eine Abwesenheit (Out of Office, OOF) Meldung und die für die Nachricht verwendete Sprache.</span><span class="sxs-lookup"><span data-stu-id="83285-114">Contains an Out of Office (OOF) message and the language used for the message.</span></span>  <br/> |
|[<span data-ttu-id="83285-115">Dauer (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="83285-115">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> |<span data-ttu-id="83285-116">Enthält die Dauer, für die der Abwesenheitsstatus aktiviert ist, wenn das [OofState](oofstate.md) -Element auf Scheduled festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="83285-116">Contains the duration that the OOF status is enabled if the [OofState](oofstate.md) element is set to Scheduled.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="83285-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83285-117">Parent elements</span></span>

|<span data-ttu-id="83285-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="83285-118">**Element**</span></span>|<span data-ttu-id="83285-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83285-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83285-120">E-Mail-Info</span><span class="sxs-lookup"><span data-stu-id="83285-120">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="83285-121">Stellt Werte für verschiedene Arten von e-Mail-Tipps dar.</span><span class="sxs-lookup"><span data-stu-id="83285-121">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="83285-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="83285-122">Text value</span></span>

<span data-ttu-id="83285-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="83285-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="83285-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83285-124">Remarks</span></span>

<span data-ttu-id="83285-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="83285-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83285-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="83285-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83285-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="83285-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="83285-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="83285-128">Schema Name</span></span>  <br/> |<span data-ttu-id="83285-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="83285-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="83285-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="83285-130">Validation File</span></span>  <br/> |<span data-ttu-id="83285-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="83285-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="83285-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="83285-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="83285-133">False</span><span class="sxs-lookup"><span data-stu-id="83285-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83285-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83285-134">See also</span></span>

- [<span data-ttu-id="83285-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="83285-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

