---
title: AddNewImContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d5913619-0c13-429d-b9d2-057e8af220f1
description: Das AddNewImContactToGroup-Element definiert eine Anforderung an einen neuen instant messaging-Kontakt zu einer instant messaging-Gruppe hinzufügen.
ms.openlocfilehash: 2736bac6880a11101e9bffee12033c838705700e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757232"
---
# <a name="addnewimcontacttogroup"></a><span data-ttu-id="b7eb1-103">AddNewImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="b7eb1-103">AddNewImContactToGroup</span></span>

<span data-ttu-id="b7eb1-104">Das **AddNewImContactToGroup** -Element definiert eine Anforderung an einen neuen instant messaging-Kontakt zu einer instant messaging-Gruppe hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7eb1-104">The **AddNewImContactToGroup** element defines a request to add a new instant messaging contact to an instant messaging group.</span></span> 
  
```XML
<AddNewImContactToGroup>
   <ImAddress/>
   <DisplayName/>
   <GroupId/>
</AddNewImContactToGroup>
```

 <span data-ttu-id="b7eb1-105">**AddNewImContactToGroupType**</span><span class="sxs-lookup"><span data-stu-id="b7eb1-105">**AddNewImContactToGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b7eb1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b7eb1-106">Attributes and elements</span></span>

<span data-ttu-id="b7eb1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b7eb1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7eb1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b7eb1-108">Attributes</span></span>

<span data-ttu-id="b7eb1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b7eb1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b7eb1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b7eb1-110">Child elements</span></span>

<span data-ttu-id="b7eb1-111">[ImAddress (NonEmptyStringType)](imaddress-nonemptystringtype.md) | [DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupId](groupid.md)</span><span class="sxs-lookup"><span data-stu-id="b7eb1-111">[ImAddress (NonEmptyStringType)](imaddress-nonemptystringtype.md) | [DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupId](groupid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b7eb1-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b7eb1-112">Parent elements</span></span>

<span data-ttu-id="b7eb1-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b7eb1-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b7eb1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b7eb1-114">Remarks</span></span>

<span data-ttu-id="b7eb1-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7eb1-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b7eb1-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b7eb1-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7eb1-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b7eb1-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7eb1-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7eb1-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b7eb1-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b7eb1-119">Schema name</span></span>  <br/> |<span data-ttu-id="b7eb1-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b7eb1-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b7eb1-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b7eb1-121">Validation file</span></span>  <br/> |<span data-ttu-id="b7eb1-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b7eb1-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b7eb1-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b7eb1-123">Can be empty</span></span>  <br/> |<span data-ttu-id="b7eb1-124">false</span><span class="sxs-lookup"><span data-stu-id="b7eb1-124">false</span></span>  <br/> |
   

