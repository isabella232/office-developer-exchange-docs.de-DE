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
ms.openlocfilehash: 0d0981d050fa388e83eaa8408b60d305296c1f36
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831284"
---
# <a name="searchablemailbox"></a><span data-ttu-id="1426b-103">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="1426b-103">SearchableMailbox</span></span>

<span data-ttu-id="1426b-104">Das **SearchableMailbox** -Element gibt ein Postfach aus einer Anforderung **GetSearchableMailboxes** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1426b-104">The **SearchableMailbox** element specifies a mailbox returned from a **GetSearchableMailboxes** request.</span></span> 
  
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

 <span data-ttu-id="1426b-105">**SearchableMailboxType**</span><span class="sxs-lookup"><span data-stu-id="1426b-105">**SearchableMailboxType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1426b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1426b-106">Attributes and elements</span></span>

<span data-ttu-id="1426b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1426b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1426b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1426b-108">Attributes</span></span>

<span data-ttu-id="1426b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1426b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1426b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1426b-110">Child elements</span></span>

<span data-ttu-id="1426b-111">[Guid](guid-ex15websvcsotherref.md) | [PrimarySmtpAddress (Zeichenfolge)](primarysmtpaddress-string.md) | [IsExternalMailbox](isexternalmailbox.md) | [ExternalEmailAddress](externalemailaddress.md) | [DisplayName (Zeichenfolge)](displayname-string.md) | [IsMembershipGroup](ismembershipgroup.md) | [ReferenceId](referenceid.md)</span><span class="sxs-lookup"><span data-stu-id="1426b-111">[Guid](guid-ex15websvcsotherref.md) | [PrimarySmtpAddress (string)](primarysmtpaddress-string.md) | [IsExternalMailbox](isexternalmailbox.md) | [ExternalEmailAddress](externalemailaddress.md) | [DisplayName (string)](displayname-string.md) | [IsMembershipGroup](ismembershipgroup.md) | [ReferenceId](referenceid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1426b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1426b-112">Parent elements</span></span>

[<span data-ttu-id="1426b-113">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="1426b-113">SearchableMailboxes</span></span>](searchablemailboxes.md)
  
## <a name="remarks"></a><span data-ttu-id="1426b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1426b-114">Remarks</span></span>

<span data-ttu-id="1426b-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1426b-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1426b-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1426b-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1426b-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1426b-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1426b-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="1426b-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1426b-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1426b-119">Schema name</span></span>  <br/> |<span data-ttu-id="1426b-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1426b-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="1426b-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1426b-121">Validation file</span></span>  <br/> |<span data-ttu-id="1426b-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1426b-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1426b-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1426b-123">Can be empty</span></span>  <br/> ||
   

