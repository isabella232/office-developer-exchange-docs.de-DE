---
title: MailboxSearchScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ef4a4203-61e5-46b8-9fa4-d1a10e785aa2
description: Das MailboxSearchScope-Element gibt ein Postfach und einen Suchbereich für eine Ermittlungs Suche an.
ms.openlocfilehash: 20f528ddfb4812de8468af33bcb0b47d7d851f1d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457186"
---
# <a name="mailboxsearchscope"></a><span data-ttu-id="3ed4e-103">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="3ed4e-103">MailboxSearchScope</span></span>

<span data-ttu-id="3ed4e-104">Das **MailboxSearchScope** -Element gibt ein Postfach und einen Suchbereich für eine Ermittlungs Suche an.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-104">The **MailboxSearchScope** element specifies a mailbox and a search scope for a discovery search.</span></span> 
  
```XML
<MailboxSearchScope>
   <Mailbox/>
   <SearchScope/>
<MailboxSearchScope>
```

<span data-ttu-id="3ed4e-105">**MailboxSearchScopeType**</span><span class="sxs-lookup"><span data-stu-id="3ed4e-105">**MailboxSearchScopeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3ed4e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3ed4e-106">Attributes and elements</span></span>

<span data-ttu-id="3ed4e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3ed4e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3ed4e-108">Attributes</span></span>

<span data-ttu-id="3ed4e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3ed4e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3ed4e-110">Child elements</span></span>

<span data-ttu-id="3ed4e-111">[Postfach (Zeichenfolge)](mailbox-string.md)  |  [SearchScope](searchscope.md)</span><span class="sxs-lookup"><span data-stu-id="3ed4e-111">[Mailbox (string)](mailbox-string.md) | [SearchScope](searchscope.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3ed4e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3ed4e-112">Parent elements</span></span>

[<span data-ttu-id="3ed4e-113">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="3ed4e-113">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
  
## <a name="remarks"></a><span data-ttu-id="3ed4e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ed4e-114">Remarks</span></span>

<span data-ttu-id="3ed4e-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3ed4e-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ed4e-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3ed4e-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ed4e-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ed4e-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3ed4e-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3ed4e-119">Schema name</span></span>  <br/> |<span data-ttu-id="3ed4e-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3ed4e-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="3ed4e-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3ed4e-121">Validation file</span></span>  <br/> |<span data-ttu-id="3ed4e-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3ed4e-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3ed4e-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="3ed4e-123">Can be empty</span></span>  <br/> ||
   

