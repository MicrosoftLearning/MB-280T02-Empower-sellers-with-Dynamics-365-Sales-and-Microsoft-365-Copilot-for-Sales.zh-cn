---
lab:
  title: 实验室 5.1：自定义业务流程流
---

# 模块 5：使用 Dynamics 365 Sales Insights 和销售加速器 

## 实践实验室 5.1：自定义业务流程流

## 场景

Contoso Coffee 希望在其久经考验的销售业务流程中增加几个额外步骤。 尽管销售人员过去在遵循这一框架方面取得了成功，但他们表示，一些新建议将有助于培育潜在顾客和签订高价值合同。

销售人员希望将以下步骤添加到其业务流程中：

-   对于预算超过 \$1,000,000 的高价值潜在客户，在授予资格之前，亲自联系潜在销售顾客以确认兴趣。
-   在开发阶段，确保销售人员跟踪现有的客户痛点，以帮助确定以前可能错过的附加产品销售的潜在领域。

在此实验室中，我们将自定义业务流程流以满足销售人员的要求。

## 练习 1 - 自定义业务流程流

### 任务 1 - 创建业务流程流

在此任务中，你将从商机销售流程创建新的业务流程流，然后测试新的 BPF。

1.  导航到 [https://make.powerapps.com](https://make.powerapps.com/)。
2.  确保你位于“**销售试用**”环境中。
3.  选择**解决方案**。
4.  在顶部命令栏中选择“**+ 新解决方案**”按钮。
5.  在“**显示名称**”字段中输入 **Contoso**。
6.  选择“**+ 新建发布服务器**”。
7.  配置新发布服务器如下。
    1.  **显示名称：** Contoso
    2.  **名称：** Contoso
    3.  **前缀：** Contoso
    4.  **选择值前缀：** 10000
8.  选择“保存”。
9.  在“发布服务器”下，选择刚刚创建的新 **Contoso** 发布服务器。
10. 选择**创建**。
11. 在**命令栏**中选择“**添加**”现有内容。
12. 从显示的菜单中选择“**自动化**\>**过程**”。
13. 现在，我们将在流程列表中找到“**销售流程**”。 （现在可以使用右上角的搜索框进行搜索。）找到后，请选择它。
14. 选择“添加”按钮。
15. 选择“**销售流程**”以将其打开。
16. 新选项卡将打开 BPF 编辑器。 （将旧选项卡与解决方案列表保持打开状态。）现在，让我们添加销售人员请求的步骤。
17. 首先，我们将添加一个条件来检查客户的预算，并确定预算超过 \$1,000,000 的潜在高价值客户。 从“**组件**”选项卡中拖动“**条件**”，并将其放置在“**授予资格**”和“**开发**”阶段之间。
18. 选择“**条件**”，转到“**属性**”选项卡，然后为“**显示名称**”输入 **Check Budget**。
19. 在“**规则**”下，为“**字段**”选择“**预算金额**”。
20. 为“**运算符**”选择“**大于或等于**”。
21. 为“**类型**”选择“**值**”。
22. 在“**值**”中输入 **1,000,000** 并单击“**应用**”。
23. 现在，我们需要添加新阶段才能完成条件。 在“组件”窗格中，向“条件”右侧添加新阶段。
24. 选择“属性”选项卡。
25. 为“**显示名称**”输入“**确认兴趣**”。 选择“应用”。
26. 单击“**确认兴趣**”阶段的“**详细信息**”按钮。
27. 选择“**确认兴趣**”阶段内的“**数据步骤 \#1 新步骤**”。
28. 在“**属性**”选项卡中，打开“**数据字段**”下拉列表。 选择“**确认兴趣**”。 步骤名称将自动更新。
29. 选中“**必需**”复选框，然后单击“**应用**”。
30. 接下来，我们将根据销售人员的要求，在“开发”阶段增加一个新步骤，询问客户的痛点。 选择“**开发**”阶段并展开“**详细信息**”
31. 在“组件”窗格中，将“**数据步骤**”拖到“数据步骤 \#4”下方。
32. 在“数据字段”下拉列表中，选择“**客户痛点**”。 现在，在“开发”阶段，它将成为确定客户痛点的建议步骤。 我们不会将此字段标记为必需。
33. 选择“应用”。
34. 单击“**验证**”以确保所做的更改有效，BPF 将按预期工作。
35. 如果没有任何问题，请单击“**更新**”。
36. 使用业务流程流编辑器关闭选项卡。
37. 返回上一个选项卡，在默认解决方案区域中的弹出窗口中单击“**完成**”。 在顶部菜单中，选择“**发布所有自定义项**”。 （可能需要删除右上角文本框中的“商机”搜索才能看到此按钮。）
38. 等待自定义项**发布**。

### 任务 2 - 测试业务流程流

1.  退回“销售中心”应用。
2.  导航到“**商机**”部分，然后单击“**+新建**”以创建新商机。 输入一个主题，例如“**对新机器感兴趣**”。
3.  为联系人字段选择现有联系人。
4.  打开销售流程业务流程流的“**授予资格**”阶段。 输入 *\$800,000*，表示“估计预算”。
5.  业务流程流应分为 4 个阶段：**授予资格**、**开发**、**建议**和**关闭**。 如果预算金额小于 \$1,000,000，则“确认兴趣”阶段将不作为流程的一部分。
6.  将“**预算金额**”更改为 *\$1,200,000*。
7.  现在，业务流程应分为 5 个阶段：**授予资格**、**确认兴趣**、**开发**、**建议**和**关闭**。 从“授予资格”阶段进入下一阶段。
8.  **保存**“商机”。
9.  选择“**授予资格**”阶段，然后选择“**下一阶段**”按钮以进入“**确认兴趣**”阶段。
10. 通过选择“**否**”确认兴趣，然后选择“**是**”。
11. 选择“**下一阶段**”按钮，进入“**开发**”阶段。
12. 确认“客户痛点”字段显示在“开发”阶段底部。
13. 在“客户痛点”字段中输入“*当前机器无法处理客户量*”。
14. 选择**下一个阶段**。
15. **保存**记录。
