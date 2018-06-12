---
title: EmailAddress (GetPersonaType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 052055b5-4630-40ed-9b24-9e7f4bf7ba1d
description: Das EmailAddress (GetPersonaType)-Element gibt die e-Mail-Adresse, die die Rolle zugeordnet.
ms.openlocfilehash: a28a4a61a9719875fe99e1c950bcd3ec3af9ab13
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758159"
---
# <a name="emailaddress-getpersonatype"></a><span data-ttu-id="fcd86-103">EmailAddress (GetPersonaType)</span><span class="sxs-lookup"><span data-stu-id="fcd86-103">EmailAddress (GetPersonaType)</span></span>

<span data-ttu-id="fcd86-104">Das **EmailAddress (GetPersonaType)** -Element gibt die e-Mail-Adresse, die die Rolle zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="fcd86-104">The **EmailAddress (GetPersonaType)** element specifies the email address associated with the persona.</span></span> 
  
```XML
<EmailAddress>
    <Name></Name>
    <EmailAddress></EmailAddress>
    <RoutingType></RoutingType>
    <MailboxType></MailboxType>
    <ItemId></ItemId>
    <OriginalDisplayName></OriginalDisplayName>
</EmailAddress>>
```

 <span data-ttu-id="fcd86-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="fcd86-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fcd86-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fcd86-106">Attributes and elements</span></span>

<span data-ttu-id="fcd86-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fcd86-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fcd86-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fcd86-108">Attributes</span></span>

<span data-ttu-id="fcd86-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fcd86-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fcd86-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fcd86-110">Child elements</span></span>

<span data-ttu-id="fcd86-111">[Name (Zeichenfolge)](name-string.md) | [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) | [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) | [MailboxType](mailboxtype.md) | [ItemId](itemid.md) | [OriginalDisplayName](originaldisplayname.md)</span><span class="sxs-lookup"><span data-stu-id="fcd86-111">[Name (string)](name-string.md) | [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) | [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) | [MailboxType](mailboxtype.md) | [ItemId](itemid.md) | [OriginalDisplayName](originaldisplayname.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fcd86-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fcd86-112">Parent elements</span></span>

[<span data-ttu-id="fcd86-113">GetPersona</span><span class="sxs-lookup"><span data-stu-id="fcd86-113">GetPersona</span></span>](getpersona.md)
  
## <a name="remarks"></a><span data-ttu-id="fcd86-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fcd86-114">Remarks</span></span>

<span data-ttu-id="fcd86-115">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="fcd86-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="fcd86-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fcd86-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fcd86-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fcd86-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fcd86-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="fcd86-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fcd86-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fcd86-119">Schema Name</span></span>  <br/> |<span data-ttu-id="fcd86-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fcd86-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fcd86-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fcd86-121">Validation File</span></span>  <br/> |<span data-ttu-id="fcd86-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fcd86-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fcd86-123">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fcd86-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="fcd86-124">True</span><span class="sxs-lookup"><span data-stu-id="fcd86-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fcd86-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fcd86-125">See also</span></span>

- [<span data-ttu-id="fcd86-126">GetPersona</span><span class="sxs-lookup"><span data-stu-id="fcd86-126">GetPersona</span></span>](getpersona.md)
- [<span data-ttu-id="fcd86-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fcd86-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

