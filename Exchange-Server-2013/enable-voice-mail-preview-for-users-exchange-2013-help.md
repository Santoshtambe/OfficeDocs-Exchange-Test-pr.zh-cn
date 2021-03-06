﻿---
title: '为用户启用语音邮件预览: Exchange Online Help'
TOCTitle: 为用户启用语音邮件预览
ms:assetid: 206a5d2b-27c9-4e9b-a29a-6ddffaa07109
ms:mtpsurl: https://technet.microsoft.com/zh-cn/library/JJ673514(v=EXCHG.150)
ms:contentKeyID: 51408204
ms.date: 05/23/2018
mtps_version: v=EXCHG.150
ms.translationtype: MT
---

# 为用户启用语音邮件预览

 

_**适用于：**Exchange Online, Exchange Server 2013, Exchange Server 2016_

_**上一次修改主题：**2013-02-21_

您可以启用统一邮件 (UM) 邮箱策略与相关联，如果禁用了用户的语音邮件预览功能。如果启用此设置，用户可以接收语音邮件，在邮件正文中的电子邮件或文本消息的文本。默认设置为启用。

有关与 UM 邮箱策略相关的其他管理任务，请参阅 [UM 邮箱策略过程](um-mailbox-policy-procedures-exchange-2013-help.md)。

## 在开始之前，您需要知道什么？

  - 估计完成时间：少于 1 分钟。

  - 您必须先获得权限，然后才能执行此过程或多个过程。若要查看所需的权限，请参阅 [统一消息权限](unified-messaging-permissions-exchange-2013-help.md)主题中的\&quot;UM 邮箱策略\&quot;条目。

  - 在执行这些步骤之前，先确认已创建 UM 拨号计划。有关详细步骤，请参阅[创建 UM 拨号计划](create-a-um-dial-plan-exchange-2013-help.md)。

  - 在执行这些步骤之前，先确认已创建 UM 邮箱策略。有关详细步骤，请参阅[创建 UM 邮箱策略](create-a-um-mailbox-policy-exchange-2013-help.md)。

  - 若要了解可能适用于此主题中过程的键盘快捷键，请参阅 [Exchange 管理中心内的键盘快捷键](keyboard-shortcuts-in-the-exchange-admin-center-exchange-online-protection-help.md)。

<table>
<thead>
<tr class="header">
<th><img src="images/Bb124558.tip(EXCHG.150).gif" title="提示" alt="提示" />提示：</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>遇到问题了吗？请在 Exchange 论坛中寻求帮助。 请访问以下论坛：<a href="https://go.microsoft.com/fwlink/p/?linkid=60612">Exchange Server</a>、 <a href="https://go.microsoft.com/fwlink/p/?linkid=267542">Exchange Online</a> 或 <a href="https://go.microsoft.com/fwlink/p/?linkid=285351">Exchange Online Protection</a>。.</td>
</tr>
</tbody>
</table>


## 您想执行什么操作？

## 使用 EAC 启用语音邮件预览

1.  在 EAC 中，导航至\&quot;统一消息\&quot;\>\&quot;UM 拨号计划\&quot;，选择要更改的 UM 拨号计划，然后单击\&quot;编辑\&quot;![编辑图标](images/Bb124582.6f53ccb2-1f13-4c02-bea0-30690e6ea71d(EXCHG.150).gif "编辑图标")。

2.  在\&quot;UM 拨号计划\&quot;页面的\&quot;UM 邮箱策略\&quot;下，选择要管理的 UM 邮箱策略，然后单击\&quot;编辑\&quot;![编辑图标](images/Bb124582.6f53ccb2-1f13-4c02-bea0-30690e6ea71d(EXCHG.150).gif "编辑图标")。

3.  在\&quot;UM 邮箱策略\&quot;页面的\&quot;常规\&quot;\>中，选择\&quot;允许语音邮件预览\&quot;旁边的复选框。

4.  单击\&quot;保存\&quot;。

## 使用命令行管理程序启用语音邮件预览

此示例允许与 UM 邮箱策略 `MyUMMailboxPolicy` 关联的用户使用\&quot;语音邮件预览\&quot;功能。

    Set-UMMailboxPolicy -identity MyUMMailboxPolicy - AllowVoiceMailPreview $true

