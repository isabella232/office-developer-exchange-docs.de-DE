---
title: AddNewImContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d5913619-0c13-429d-b9d2-057e8af220f1
description: Das AddNewImContactToGroup-Element definiert eine Anforderung zum Hinzufügen eines neuen Chat Kontakts zu einer Sofortnachrichten Gruppe.
ms.openlocfilehash: c493ba81b23832a462acd425eb60297801f8768f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463650"
---
# <a name="addnewimcontacttogroup"></a><span data-ttu-id="a8a30-103">AddNewImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="a8a30-103">AddNewImContactToGroup</span></span>

<span data-ttu-id="a8a30-104">Das **AddNewImContactToGroup** -Element definiert eine Anforderung zum Hinzufügen eines neuen Chat Kontakts zu einer Sofortnachrichten Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a8a30-104">The **AddNewImContactToGroup** element defines a request to add a new instant messaging contact to an instant messaging group.</span></span> 
  
```XML
<AddNewImContactToGroup>
   <ImAddress/>
   <DisplayName/>
   <GroupId/>
</AddNewImContactToGroup>
```

 <span data-ttu-id="a8a30-105">**AddNewImContactToGroupType**</span><span class="sxs-lookup"><span data-stu-id="a8a30-105">**AddNewImContactToGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a8a30-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a8a30-106">Attributes and elements</span></span>

<span data-ttu-id="a8a30-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a8a30-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8a30-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a8a30-108">Attributes</span></span>

<span data-ttu-id="a8a30-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a8a30-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a8a30-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8a30-110">Child elements</span></span>

<span data-ttu-id="a8a30-111">[Imaddresse (NonEmptyStringType)](imaddress-nonemptystringtype.md)  |  [DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md)  |  [Gruppen](groupid.md) -Nr</span><span class="sxs-lookup"><span data-stu-id="a8a30-111">[ImAddress (NonEmptyStringType)](imaddress-nonemptystringtype.md) | [DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupId](groupid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a8a30-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8a30-112">Parent elements</span></span>

<span data-ttu-id="a8a30-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a8a30-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8a30-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8a30-114">Remarks</span></span>

<span data-ttu-id="a8a30-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a8a30-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a8a30-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a8a30-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a8a30-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a8a30-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8a30-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8a30-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a8a30-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a8a30-119">Schema name</span></span>  <br/> |<span data-ttu-id="a8a30-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a8a30-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a8a30-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a8a30-121">Validation file</span></span>  <br/> |<span data-ttu-id="a8a30-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a8a30-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a8a30-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a8a30-123">Can be empty</span></span>  <br/> |<span data-ttu-id="a8a30-124">False</span><span class="sxs-lookup"><span data-stu-id="a8a30-124">false</span></span>  <br/> |
   

