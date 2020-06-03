---
title: SetHoldOnMailboxesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61de0f3-24e0-434a-946a-c53d393b7d04
description: Das SetHoldOnMailboxesResponseMessage-Element gibt die Antwortnachricht für eine SetHoldOnMailboxes-Anforderung an.
ms.openlocfilehash: a6af4181218391bc9d3c177467295d771cce4c89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456409"
---
# <a name="setholdonmailboxesresponsemessage"></a><span data-ttu-id="4fa31-103">SetHoldOnMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4fa31-103">SetHoldOnMailboxesResponseMessage</span></span>

<span data-ttu-id="4fa31-104">Das **SetHoldOnMailboxesResponseMessage** -Element gibt die Antwortnachricht für eine **SetHoldOnMailboxes** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="4fa31-104">The **SetHoldOnMailboxesResponseMessage** element specifies the response message for a **SetHoldOnMailboxes** request.</span></span> 
  
```XML
<SetHoldOnMailboxesResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MailboxHoldResult/>
</SetHoldOnMailboxesResponseMessage>
```

 <span data-ttu-id="4fa31-105">**SetHoldOnMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="4fa31-105">**SetHoldOnMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4fa31-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4fa31-106">Attributes and elements</span></span>

<span data-ttu-id="4fa31-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4fa31-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4fa31-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4fa31-108">Attributes</span></span>

<span data-ttu-id="4fa31-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4fa31-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4fa31-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4fa31-110">Child elements</span></span>

<span data-ttu-id="4fa31-111">[MessageText](messagetext.md)  |  [Response Code](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [Messagexml verwendet](messagexml.md)  |  [MailboxHoldResult](mailboxholdresult.md)</span><span class="sxs-lookup"><span data-stu-id="4fa31-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [MailboxHoldResult](mailboxholdresult.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4fa31-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4fa31-112">Parent elements</span></span>

[<span data-ttu-id="4fa31-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4fa31-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="4fa31-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fa31-114">Remarks</span></span>

<span data-ttu-id="4fa31-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4fa31-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4fa31-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4fa31-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4fa31-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4fa31-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4fa31-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="4fa31-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4fa31-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4fa31-119">Schema name</span></span>  <br/> |<span data-ttu-id="4fa31-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4fa31-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4fa31-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4fa31-121">Validation file</span></span>  <br/> |<span data-ttu-id="4fa31-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4fa31-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4fa31-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="4fa31-123">Can be empty</span></span>  <br/> ||
   

