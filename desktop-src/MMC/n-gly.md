---
title: N
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
Robots: noindex, nofollow
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 5aca4dc7-4424-4ab3-8667-4848a5f1433a
ms.prod: windows-server-dev
ms.technology: microsoft-management-console
ms.tgt_platform: multiple
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# N

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J K [L](l-gly.md) [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) X Y Z

<dl> <dt>

<span id="mmc_namespace_gly"></span><span id="MMC_NAMESPACE_GLY"></span>**namespace**
</dt> <dd>

Collective term used to describe both the [*scope pane*](https://www.bing.com/search?q=*scope pane*) and the [*result pane*](https://www.bing.com/search?q=*result pane*) of a console in which one or more snap-ins are loaded. A snap-in can add scope items and result items to its namespace— that is, it can add scope items in the scope pane and result items in the result pane of the console in which it is loaded.

A [*namespace extension*](#mmc-namespace-extension-gly) snap-in can add scope items to the namespace of a primary snap-in— that is, it can add scope items as children of scope items inserted by the primary snap-in.

</dd> <dt>

<span id="mmc_namespace_extension_gly"></span><span id="MMC_NAMESPACE_EXTENSION_GLY"></span>**namespace extension**
</dt> <dd>

[*Extension snap-in*](https://www.bing.com/search?q=*Extension snap-in*) that extends the functionality of a [*primary snap-in*](https://www.bing.com/search?q=*primary snap-in*) by adding its own scope items as child items of a particular [*node type*](#mmc-node-type-gly) that are inserted by the primary snap-in.

</dd> <dt>

<span id="mmc_node_gly"></span><span id="MMC_NODE_GLY"></span>**node**
</dt> <dd>

Object in the [*console tree*](https://www.bing.com/search?q=*console tree*). There are two main types of nodes: [*static nodes*](https://www.bing.com/search?q=*static nodes*) and [*enumerated nodes*](https://www.bing.com/search?q=*enumerated nodes*). These nodes are also referred to collectively as [*scope items*](https://www.bing.com/search?q=*scope items*).

A third type of node, called a built-in node, is implemented by MMC and does not interact with snap-ins. An example of a built-in node is the Console Root.

</dd> <dt>

<span id="mmc_node_manager_gly"></span><span id="MMC_NODE_MANAGER_GLY"></span>**Node Manager**
</dt> <dd>

Used interchangeably with the term "MMC" in the MMC SDK documentation. The Node Manager implements a number of MMC COM interfaces and exposes them to snap-ins for their use.

</dd> <dt>

<span id="mmc_node_type_gly"></span><span id="MMC_NODE_TYPE_GLY"></span>**node type**
</dt> <dd>

A scope or result item's most important property, represented by a node type GUID. An item's node type describes its overall type; for example, whether it is a user, a machine, or a domain entry in a Domain Name System (DNS) database. A node type is defined by the individual snap-in rather than by MMC. MMC uses an item's node type to determine whether it can be extended by [*extension snap-ins*](https://www.bing.com/search?q=*extension snap-ins*).

</dd> <dt>

<span id="mmc_node_type_guid_gly"></span><span id="MMC_NODE_TYPE_GUID_GLY"></span>**node type GUID**
</dt> <dd>

GUID associated with a particular node type. Snap-ins must register the node type GUIDs of their extendible node types. GUIDs in this context have no COM significance, although they can be generated using Guidgen.exe.

</dd> <dt>

<span id="mmc_notification_or_notification_message__gly"></span><span id="MMC_NOTIFICATION_OR_NOTIFICATION_MESSAGE__GLY"></span>**notification (or notification message)**
</dt> <dd>

How MMC informs a snap-in that it must perform an action, usually in response to a user action, such as selecting a scope item or a context menu item. MMC sends notification messages to the snap-in's [**IComponentData::Notify**](/windows/desktop/api/Mmc/nf-mmc-icomponentdata-notify), [**IComponent::Notify**](/windows/desktop/api/Mmc/nf-mmc-icomponent-notify), or [**IExtendControlbar::ControlbarNotify**](/windows/desktop/api/Mmc/nf-mmc-iextendcontrolbar-controlbarnotify) methods, depending on the notification.

</dd> </dl>

 

 



