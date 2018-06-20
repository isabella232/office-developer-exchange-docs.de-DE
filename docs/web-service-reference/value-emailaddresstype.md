---
title: Wert (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 24eaa473-0024-47e2-b7d2-051d5dd4f53c
description: Das Value-Element gibt den Wert des ein EmailAddress ein Array Marken zugeordnet.
ms.openlocfilehash: 097444d90e98e73b9e83912274ecf87249008116
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839485"
---
# <a name="value-emailaddresstype"></a><span data-ttu-id="d9ca7-103">Wert (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="d9ca7-103">Value (EmailAddressType)</span></span>

<span data-ttu-id="d9ca7-104">Das **Value** -Element gibt an, dass ein Array Marken der Wert der ein **EmailAddress** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-104">The **Value** element specifies the value of an **EmailAddress** associated with an attributions array.</span></span> 
  
```XML
<Value>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
   <OriginalDisplayName/>
</Value>
```

<span data-ttu-id="d9ca7-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="d9ca7-105">**EmailAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d9ca7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d9ca7-106">Attributes and elements</span></span>

<span data-ttu-id="d9ca7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9ca7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d9ca7-108">Attributes</span></span>

<span data-ttu-id="d9ca7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d9ca7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d9ca7-110">Child elements</span></span>

<span data-ttu-id="d9ca7-111">[Name (Zeichenfolge)](name-string.md) | [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) | [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) | [MailboxType](mailboxtype.md) | [ItemId](itemid.md) | [OriginalDisplayName](originaldisplayname.md)</span><span class="sxs-lookup"><span data-stu-id="d9ca7-111">[Name (string)](name-string.md) | [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) | [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) | [MailboxType](mailboxtype.md) | [ItemId](itemid.md) | [OriginalDisplayName](originaldisplayname.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d9ca7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d9ca7-112">Parent elements</span></span>

[<span data-ttu-id="d9ca7-113">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="d9ca7-113">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md)
  
## <a name="remarks"></a><span data-ttu-id="d9ca7-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9ca7-114">Remarks</span></span>

<span data-ttu-id="d9ca7-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d9ca7-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d9ca7-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d9ca7-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9ca7-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="d9ca7-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d9ca7-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d9ca7-119">Schema name</span></span>  <br/> |<span data-ttu-id="d9ca7-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d9ca7-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="d9ca7-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d9ca7-121">Validation file</span></span>  <br/> |<span data-ttu-id="d9ca7-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d9ca7-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d9ca7-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d9ca7-123">Can be empty</span></span>  <br/> |<span data-ttu-id="d9ca7-124">false</span><span class="sxs-lookup"><span data-stu-id="d9ca7-124">false</span></span>  <br/> |
   

