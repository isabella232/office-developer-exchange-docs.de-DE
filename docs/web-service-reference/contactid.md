---
title: ContactId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 86f66275-1e39-48ed-bd89-ac3bffc465a7
description: Das Contacts-Element identifiziert einen Kontakt eindeutig.
ms.openlocfilehash: 17e8012283078d5d6e2cd1d2e88eef37b008be42
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463181"
---
# <a name="contactid"></a><span data-ttu-id="22008-103">ContactId</span><span class="sxs-lookup"><span data-stu-id="22008-103">ContactId</span></span>

<span data-ttu-id="22008-104">Das **ContactId** Contacts-Element identifiziert einen Kontakt eindeutig.</span><span class="sxs-lookup"><span data-stu-id="22008-104">The **ContactId** element uniquely identifies a contact.</span></span> 
  
```XML
<ContactId Id="" ChangeKey=""/>
```

 <span data-ttu-id="22008-105">**Itemidtype**</span><span class="sxs-lookup"><span data-stu-id="22008-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="22008-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="22008-106">Attributes and elements</span></span>

<span data-ttu-id="22008-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="22008-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22008-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="22008-108">Attributes</span></span>

|<span data-ttu-id="22008-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="22008-109">**Attribute**</span></span>|<span data-ttu-id="22008-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="22008-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="22008-111">Id</span><span class="sxs-lookup"><span data-stu-id="22008-111">Id</span></span>  <br/> |<span data-ttu-id="22008-112">Der Textwert des **ID-** Attributs ist die ID des Kontaktelements.</span><span class="sxs-lookup"><span data-stu-id="22008-112">The text value of the **Id** attribute is the identifier of the contact item.</span></span>  <br/> |
|<span data-ttu-id="22008-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="22008-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="22008-114">Der Textwert des **ChangeKey** -Attributs ist der Änderungsschlüssel des Kontaktelements.</span><span class="sxs-lookup"><span data-stu-id="22008-114">The text value of the **ChangeKey** attribute is the change key of the contact item.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="22008-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="22008-115">Child elements</span></span>

<span data-ttu-id="22008-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="22008-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="22008-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="22008-117">Parent elements</span></span>

<span data-ttu-id="22008-118">[AddImContactToGroup](addimcontacttogroup.md)  |  [RemoveContactFromImList](removecontactfromimlist.md)  |  [RemoveImContactFromGroup](removeimcontactfromgroup.md)</span><span class="sxs-lookup"><span data-stu-id="22008-118">[AddImContactToGroup](addimcontacttogroup.md) | [RemoveContactFromImList](removecontactfromimlist.md) | [RemoveImContactFromGroup](removeimcontactfromgroup.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="22008-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22008-119">Remarks</span></span>

<span data-ttu-id="22008-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="22008-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="22008-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="22008-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22008-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="22008-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22008-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="22008-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="22008-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="22008-124">Schema name</span></span>  <br/> |<span data-ttu-id="22008-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="22008-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="22008-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="22008-126">Validation file</span></span>  <br/> |<span data-ttu-id="22008-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="22008-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="22008-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="22008-128">Can be empty</span></span>  <br/> |<span data-ttu-id="22008-129">False</span><span class="sxs-lookup"><span data-stu-id="22008-129">false</span></span>  <br/> |
   

