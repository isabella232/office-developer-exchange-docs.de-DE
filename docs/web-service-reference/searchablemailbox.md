---
title: SearchableMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 339005cd-a3b9-47dd-bc7b-a860b699625b
description: Das SearchableMailbox -Element gibt ein Postfach aus einer Anforderung GetSearchableMailboxes zurückgegeben.
ms.openlocfilehash: f790d9a707f10f64a776b2fc35255c233ad854b6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467452"
---
# <a name="searchablemailbox"></a><span data-ttu-id="83c81-103">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="83c81-103">SearchableMailbox</span></span>

<span data-ttu-id="83c81-104">Das **SearchableMailbox** -Element gibt ein Postfach aus einer Anforderung **GetSearchableMailboxes** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83c81-104">The **SearchableMailbox** element specifies a mailbox returned from a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<SearchableMailbox>
   <Guid/>
   <PrimarySmtpAddress/>
   <IsExternalMailbox/>
   <ExternalEmailAddress/>
   <DisplayName/>
   <IsMembershipGroup/>
   <ReferenceId/>
</SearchableMailbox>
```

 <span data-ttu-id="83c81-105">**SearchableMailboxType**</span><span class="sxs-lookup"><span data-stu-id="83c81-105">**SearchableMailboxType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83c81-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="83c81-106">Attributes and elements</span></span>

<span data-ttu-id="83c81-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="83c81-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83c81-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="83c81-108">Attributes</span></span>

<span data-ttu-id="83c81-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="83c81-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83c81-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83c81-110">Child elements</span></span>

<span data-ttu-id="83c81-111">[Guid](guid-ex15websvcsotherref.md) | [PrimarySmtpAddress (Zeichenfolge)](primarysmtpaddress-string.md) | [IsExternalMailbox](isexternalmailbox.md) | [ExternalEmailAddress](externalemailaddress.md) | [DisplayName (Zeichenfolge)](displayname-string.md) | [IsMembershipGroup](ismembershipgroup.md) | [ReferenceId](referenceid.md)</span><span class="sxs-lookup"><span data-stu-id="83c81-111">[Guid](guid-ex15websvcsotherref.md) | [PrimarySmtpAddress (string)](primarysmtpaddress-string.md) | [IsExternalMailbox](isexternalmailbox.md) | [ExternalEmailAddress](externalemailaddress.md) | [DisplayName (string)](displayname-string.md) | [IsMembershipGroup](ismembershipgroup.md) | [ReferenceId](referenceid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="83c81-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83c81-112">Parent elements</span></span>

[<span data-ttu-id="83c81-113">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="83c81-113">SearchableMailboxes</span></span>](searchablemailboxes.md)
  
## <a name="remarks"></a><span data-ttu-id="83c81-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83c81-114">Remarks</span></span>

<span data-ttu-id="83c81-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="83c81-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="83c81-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="83c81-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83c81-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="83c81-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83c81-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="83c81-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="83c81-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="83c81-119">Schema name</span></span>  <br/> |<span data-ttu-id="83c81-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="83c81-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="83c81-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="83c81-121">Validation file</span></span>  <br/> |<span data-ttu-id="83c81-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="83c81-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="83c81-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="83c81-123">Can be empty</span></span>  <br/> ||
   

