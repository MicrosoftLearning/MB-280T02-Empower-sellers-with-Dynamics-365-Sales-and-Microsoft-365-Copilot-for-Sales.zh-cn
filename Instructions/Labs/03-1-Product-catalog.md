---
lab:
  title: 实验室 3.1：配置产品目录
---

# 模块 3：使用 Dynamics 365 管理订单和产品目录

## 练习实验室 3.1 - 管理产品目录

### 场景
随着 Contoso Coffee 不断发展，他们希望实现其定价结构标准化，并允许使用更准确的定价和产品详细信息更轻松地创建报价单、订单和发票。 Contoso Coffee 最近发布了其最新的智能咖啡机。 作为其 Dynamics 365 Sales 实现的功能顾问，公司要求你配置产品目录。

成功完成本实验室后，你将能够：
- 创建计价单位组
- 定义价目表
- 创建折扣表
- 定义产品和产品系列

### 练习 1 - 产品目录

#### 任务 1 - 创建计价单位组
在此任务中，将为一系列咖啡机过滤器创建计价单位组。
1. 转到 Dynamics 365 销售中心应用程序。
2. 单击“更改区域”菜单（位于屏幕左下侧）。 默认情况下，Sales 将显示在左侧菜单底部。
3. 从显示的菜单中，选择**应用设置**。
4. 从左侧菜单的“产品目录”部分选择“计价单位组”****。
5. 单击“+ 新建”  。
6. 输入“过滤器”**** 表示“名称”，输入“每个”**** 表示“基本计价单位”，然后单击“确定”****。
7. 打开“计价单位组”后，选择“相关”选项卡，然后选择“计价单位”****。
8. 你会发现，现在只有默认计价单位“每个”；你将再添加三个计价单位。 单击“+ 新建计价单位”****。
9. 输入 <bpt ctype="x-unknown" id="1" rid="1"><bpt xmlns="urn:oasis:names:tc:xliff:document:1.2" id="p1">*</bpt></bpt>Filter<ept id="2" rid="1"><ept xmlns="urn:oasis:names:tc:xliff:document:1.2" id="p1">*</ept></ept> for Name, <bpt ctype="x-unknown" id="3" rid="2"><bpt xmlns="urn:oasis:names:tc:xliff:document:1.2" id="p2">*</bpt></bpt>1<ept id="4" rid="2"><ept xmlns="urn:oasis:names:tc:xliff:document:1.2" id="p2">*</ept></ept> 表示“数量”，选择 <bpt ctype="x-unknown" id="5" rid="3"><bpt xmlns="urn:oasis:names:tc:xliff:document:1.2" id="p3">**</bpt></bpt>Each<ept id="6" rid="3"><ept xmlns="urn:oasis:names:tc:xliff:document:1.2" id="p3">**</ept></ept> 表示“基础计价单位”，然后单击“保存和新建”<bpt ctype="x-unknown" id="7" rid="4"><bpt xmlns="urn:oasis:names:tc:xliff:document:1.2" id="p4">**</bpt></bpt><ept id="8" rid="4"><ept xmlns="urn:oasis:names:tc:xliff:document:1.2" id="p4">**</ept></ept>，方法是选择 <bpt ctype="x-unknown" id="9" rid="5"><bpt xmlns="urn:oasis:names:tc:xliff:document:1.2" id="p5">**</bpt></bpt>˅<ept id="10" rid="5"><ept xmlns="urn:oasis:names:tc:xliff:document:1.2" id="p5">**</ept></ept>“保存并关闭”按钮右侧的下拉菜单图标。
10. 输入“件”** 表示“名称”，输入“2”** 表示“数量”，选择“过滤器”**** 表示“基础单位”，然后单击“保存并新建”****。
11. 输入“件值”** 表示“名称”，输入“2”** 表示“数量”，选择“件”**** 表示“基础单位”，然后单击“保存并关闭”****。
12. 现在，列表中应有四个计价单位组。

#### 任务 2 - 创建折扣表
在此任务中，将为购买 15 个或 20 个或更多过滤器的用户创建折扣表。 15 个过滤器将获得 15% 的折扣，20 到 50 个过滤器将获得 25% 的折扣。
1. 从左侧菜单的“产品目录”部分选择“折扣表”****。
2. 单击“+ 新建”  。
3. 输入“数量折扣”** 表示“名称”，选择“百分比”**** 表示“类型”，然后单击“保存”****。
4. 单击“相关”**** 并选择“折扣”****。
5. 单击“+ 新建折扣”****。
6. 确保选择“数量折扣”表示“折扣类型”，输入“15”** 表示“开始数量”，输入“19”** 表示“结束数量”，输入“15”** 表示“百分比”，然后单击“保存”****。
7. 再次单击 **+ 新建**。
8. 为折扣类型选择“数量折扣”****。 然后，输入“20”** 表示“开始数量”，输入“50”** 表示“结束数量”，输入“25”** 表示“百分比”，然后单击“保存”****。

#### 任务 3 - 创建价目表
在此任务中，将为过滤器创建价目表。
1. 从左侧菜单的“产品目录”部分选择“价目表”****。
2. 单击“+ 新建”  。
3. 输入“直通过滤器”** 表示“名称”，选择“美元”**** 表示“货币“，然后单击“保存并关闭”****。

#### 任务 4 - 创建产品
在此任务中，你将创建产品。
1. 单击“应用设置”**** 更改区域。
2. 选择“Sales”****。
3. 从左侧菜单的“附件”部分选择“产品”****。
4. 单击“添加产品”****。
5. 输入“Airpot XL 6 Month 过滤器”** 表示“名称”，输入“AXL6MF-1234”** 表示“产品 ID”，选择“多个过滤器”**** 表示“计价单位组”，选择“过滤器”**** 表示“默认计价单位”，输入“2”** 表示“支持的小数位”，然后单击“保存”****。 （可能需要选择支持小数旁边的蓝色复选标记才能接受建议。）
6. 选择“其他详细信息”**** 选项卡。
7. 单击“价目表项”部分右上角的“垂直省略号”****。 单击“+ 新建价目表”**** 项。
8. 选择“直通过滤器”**** 表示“价目表”，选择“数量折扣”**** 表示“折扣表”，然后选择“整数”**** 表示“销售数量控制”。
9. 选择“定价信息”**** 选项卡，输入“25”** 表示“金额”，然后选择“保存并关闭”****。
10. 如果启用“自动发布”，请跳过此步骤。 （“发布”不会显示在命令栏上。）否则，请选择“发布”**** 并选择“确认”**** 发布产品。
11. 在左侧菜单的“附件”组中选择“产品”****。
12. 单击“添加产品”****。
13. 输入“Airpot XL 储液池扩建”** 表示“名称”，输入“AXLRE-4321”** 表示“产品 ID”，选择“默认计价单位”**** 表示“计价单位组”，选择“基本计价单位”**** 表示“默认计价单位”，选择 2 旁边的蓝色复选标记表示“支持的小数位”，然后单击“保存”****。
14. 选择“其他详细信息”**** 选项卡。
15. 单击“价目表项”部分右上角的“垂直省略号”****。 单击“+ 新建价目表项”****。
16. 选择“直通过滤器”**** 表示“价目表”。 选择“整数”**** 表示“销售数量控制”。
17. 选择“定价信息”**** 选项卡，输入“299 美元”** 表示“金额”，然后选择“保存并关闭”****。
18. 如果启用“自动发布”，请跳过此步骤。 否则，请选择“发布”**** 和“确认”**** 以发布产品。
19. 在左侧菜单中选择“产品”****。
20. 单击“添加产品”****。
21. 输入“Airpot XL 花盆扩展器”** 表示“名称”，输入“AXPLE-7894”** 表示“产品 ID”，选择“默认计价单位”**** 表示“计价单位组”，选择“基本计价单位”**** 表示“默认计价单位”，选择 2 旁边的蓝色复选标记表示“支持的小数位”，然后单击“保存”****。
22. 选择“其他详细信息”**** 选项卡。
23. 单击“价目表项”部分右上角的“垂直省略号”****。 单击“+ 新建价目表项”****。
24. 选择“直通过滤器”**** 表示“价目表”。 选择“整数”**** 表示“销售数量控制”。
25. 选择“定价信息”**** 选项卡，输入“199”** 表示“金额”，然后选择“保存并关闭”****。
26. 如果启用“自动发布”，请跳过此步骤。 否则，请选择“发布”**** 和“确认”**** 以发布产品。
27. 从左侧菜单中选择“产品”****。
28. 创建的产品应显示在“所有产品”、“系列”和“捆绑”视图上。 可以通过选择默认视图标题旁边的 <bpt ctype="x-unknown" id="1" rid="1"><bpt xmlns="urn:oasis:names:tc:xliff:document:1.2" id="p1">**</bpt></bpt>˅<ept id="2" rid="1"><ept xmlns="urn:oasis:names:tc:xliff:document:1.2" id="p1">**</ept></ept> 下拉图标切换到此视图。 
