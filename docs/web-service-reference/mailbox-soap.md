---
title: Postfach (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 4ad59e5b-4047-4c34-a318-ca06c31d3de8
description: Das Mailbox-Element enthält die e-Mail-Adresse des Benutzers, der ermittelt werden soll.
ms.openlocfilehash: e050cd9d3ca4a2d2450f315f1eedd3862328d096
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467284"
---
# <a name="mailbox-soap"></a><span data-ttu-id="5b827-103">Postfach (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5b827-103">Mailbox (SOAP)</span></span>

<span data-ttu-id="5b827-104">Das **Mailbox** -Element enthält die e-Mail-Adresse des Benutzers, der ermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b827-104">The **Mailbox** element contains the e-mail address of the user to be discovered.</span></span> 
  
```XML
<Mailbox/>
```

<span data-ttu-id="5b827-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5b827-105">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5b827-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5b827-106">Attributes and elements</span></span>

<span data-ttu-id="5b827-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5b827-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5b827-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5b827-108">Attributes</span></span>

<span data-ttu-id="5b827-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5b827-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5b827-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5b827-110">Child elements</span></span>

<span data-ttu-id="5b827-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5b827-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5b827-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5b827-112">Parent elements</span></span>

|<span data-ttu-id="5b827-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b827-113">**Element**</span></span>|<span data-ttu-id="5b827-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b827-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5b827-115">Benutzer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5b827-115">User (SOAP)</span></span>](user-soap.md) <br/> |<span data-ttu-id="5b827-116">Stellt die Identität eines einzelnen Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="5b827-116">Represents the identity of a single user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5b827-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="5b827-117">Text value</span></span>

<span data-ttu-id="5b827-118">Der Textwert des **Mailbox** -Elements ist die e-Mail-Adresse des Benutzers, der ermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b827-118">The text value of the **Mailbox** element is the e-mail address of the user to be discovered.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="5b827-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5b827-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b827-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b827-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="5b827-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5b827-121">Schema Name</span></span>  <br/> |<span data-ttu-id="5b827-122">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="5b827-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="5b827-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5b827-123">Validation File</span></span>  <br/> |<span data-ttu-id="5b827-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="5b827-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5b827-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5b827-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="5b827-126">True</span><span class="sxs-lookup"><span data-stu-id="5b827-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b827-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b827-127">See also</span></span>

- [<span data-ttu-id="5b827-128">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5b827-128">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

