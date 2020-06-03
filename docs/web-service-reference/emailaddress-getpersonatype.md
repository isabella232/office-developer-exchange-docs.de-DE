---
title: E-mailemail (getpersonatype)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 052055b5-4630-40ed-9b24-9e7f4bf7ba1d
description: Das Address-Element (getpersonatype) gibt die e-Mail-Adresse an, die der Rolle zugeordnet ist.
ms.openlocfilehash: b58f61202cd94ff282b21138b47b40887b38752a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463454"
---
# <a name="emailaddress-getpersonatype"></a><span data-ttu-id="3e8c1-103">E-mailemail (getpersonatype)</span><span class="sxs-lookup"><span data-stu-id="3e8c1-103">EmailAddress (GetPersonaType)</span></span>

<span data-ttu-id="3e8c1-104">Das Address-Element **(getpersonatype)** gibt die e-Mail-Adresse an, die der Rolle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3e8c1-104">The **EmailAddress (GetPersonaType)** element specifies the email address associated with the persona.</span></span> 
  
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

 <span data-ttu-id="3e8c1-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="3e8c1-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3e8c1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3e8c1-106">Attributes and elements</span></span>

<span data-ttu-id="3e8c1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3e8c1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3e8c1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3e8c1-108">Attributes</span></span>

<span data-ttu-id="3e8c1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3e8c1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3e8c1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e8c1-110">Child elements</span></span>

<span data-ttu-id="3e8c1-111">[Name (Zeichenfolge)](name-string.md)  |  [E-mailemail (NonEmptyStringType)](emailaddress-nonemptystringtype.md)  |  [Routingtype (e-mailemailtype)](routingtype-emailaddresstype.md)  |  [Mailboxtype](mailboxtype.md)  |  [ItemID](itemid.md)  |  [OriginalDisplayName](originaldisplayname.md)</span><span class="sxs-lookup"><span data-stu-id="3e8c1-111">[Name (string)](name-string.md) | [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) | [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) | [MailboxType](mailboxtype.md) | [ItemId](itemid.md) | [OriginalDisplayName](originaldisplayname.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3e8c1-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e8c1-112">Parent elements</span></span>

[<span data-ttu-id="3e8c1-113">GetPersona</span><span class="sxs-lookup"><span data-stu-id="3e8c1-113">GetPersona</span></span>](getpersona.md)
  
## <a name="remarks"></a><span data-ttu-id="3e8c1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e8c1-114">Remarks</span></span>

<span data-ttu-id="3e8c1-115">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3e8c1-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="3e8c1-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3e8c1-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3e8c1-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3e8c1-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e8c1-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e8c1-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3e8c1-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3e8c1-119">Schema Name</span></span>  <br/> |<span data-ttu-id="3e8c1-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="3e8c1-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3e8c1-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3e8c1-121">Validation File</span></span>  <br/> |<span data-ttu-id="3e8c1-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3e8c1-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3e8c1-123">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3e8c1-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="3e8c1-124">True</span><span class="sxs-lookup"><span data-stu-id="3e8c1-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3e8c1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e8c1-125">See also</span></span>

- [<span data-ttu-id="3e8c1-126">GetPersona</span><span class="sxs-lookup"><span data-stu-id="3e8c1-126">GetPersona</span></span>](getpersona.md)
- [<span data-ttu-id="3e8c1-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3e8c1-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

