---
title: RemoveImContactFromGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a62b0640-9800-45a6-a297-2105ff36881e
description: Das RemoveImContactFromGroup-Element definiert eine Anforderung zum Entfernen eines Chat Kontakts aus einer Sofortnachrichten Gruppe.
ms.openlocfilehash: 379994ad5832b05e9f7da61d752f7660a6eec5ad
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466962"
---
# <a name="removeimcontactfromgroup"></a><span data-ttu-id="a07db-103">RemoveImContactFromGroup</span><span class="sxs-lookup"><span data-stu-id="a07db-103">RemoveImContactFromGroup</span></span>

<span data-ttu-id="a07db-104">Das **RemoveImContactFromGroup** -Element definiert eine Anforderung zum Entfernen eines Chat Kontakts aus einer Sofortnachrichten Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a07db-104">The **RemoveImContactFromGroup** element defines a request to remove an instant messaging contact from an instant messaging group.</span></span> 
  
```XML
<RemoveImContactFromGroup>
   <ContactId/>
   <GroupId/>
</RemoveImContactFromGroup>
```

 <span data-ttu-id="a07db-105">**RemoveImContactFromGroupType**</span><span class="sxs-lookup"><span data-stu-id="a07db-105">**RemoveImContactFromGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a07db-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a07db-106">Attributes and elements</span></span>

<span data-ttu-id="a07db-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a07db-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a07db-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a07db-108">Attributes</span></span>

<span data-ttu-id="a07db-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a07db-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a07db-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a07db-110">Child elements</span></span>

<span data-ttu-id="a07db-111">"-" [ContactId](contactid.md)  |  [Gruppen](groupid.md) -Nr</span><span class="sxs-lookup"><span data-stu-id="a07db-111">[ContactId](contactid.md) | [GroupId](groupid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a07db-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a07db-112">Parent elements</span></span>

<span data-ttu-id="a07db-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a07db-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a07db-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a07db-114">Remarks</span></span>

<span data-ttu-id="a07db-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a07db-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a07db-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a07db-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a07db-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a07db-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a07db-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="a07db-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a07db-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a07db-119">Schema name</span></span>  <br/> |<span data-ttu-id="a07db-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a07db-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a07db-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a07db-121">Validation file</span></span>  <br/> |<span data-ttu-id="a07db-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a07db-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a07db-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a07db-123">Can be empty</span></span>  <br/> ||
   

