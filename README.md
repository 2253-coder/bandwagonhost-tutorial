# 搬瓦工 VPS：套餐选择与首次使用

这份搬瓦工 VPS 教程按选套餐、购买、首次 SSH 连接和日常管理的顺序整理。不同方案的资源与价格并不相同；下单前请在对应页面核对当前配置和计费信息。

## 套餐怎么比较

以下配置和价格为参考资料列出的信息，实际销售状态及页面报价可能变化。表中“通用入口”表示参考资料没有提供该产品的专属套餐参数，因此不另行推定。

| 套餐 | 参考配置与计费信息 | 购买入口 |
| --- | --- | --- |
| Basic VPS（KVM） | 1 核、1 GB 内存、20 GB SSD；1 TB 流量；$49.99/年 | [查看 Basic VPS（KVM）](https://bwh81.net/aff.php?aff=59244&pid=57) |
| Basic VPS（KVM，大流量） | 1 核、1 GB 内存、20 GB SSD；2 TB 流量；$52.99/半年或 $99.99/年 | [查看 Basic VPS（KVM，大流量）](https://bwh81.net/aff.php?aff=59244&pid=58) |
| E-Commerce VPS（CN2 GIA-E，小流量） | 2 核、1 GB 内存、20 GB SSD；1 TB 流量；$49.99/季或 $169.99/年 | [查看小流量方案](https://bwh81.net/aff.php?aff=59244&pid=87) |
| E-Commerce VPS（CN2 GIA-E，大流量） | 2 核、2 GB 内存、40 GB SSD；2 TB 流量；$89.99/季或 $299.99/年 | [查看大流量方案](https://bwh81.net/aff.php?aff=59244&pid=88) |
| SLA VPS | 参考资料列出 $27.99/月起；其他配置以页面为准 | [查看 SLA VPS](https://bwh81.net/aff.php?aff=59244) |
| 香港 CN2 GIA（Ultra） | 2 核、1 GB 内存、20 GB SSD；500 GB 流量；$89.99/月或 $899.99/年 | [查看香港 CN2 GIA（Ultra）](https://bwh81.net/aff.php?aff=59244&pid=100) |
| 香港 CN2 GIA 大流量（Ultra） | 2 核、2 GB 内存、40 GB SSD；1 TB 流量；$155.99/月或 $1559.99/年 | [查看香港 CN2 GIA 大流量（Ultra）](https://bwh81.net/aff.php?aff=59244&pid=101) |
| 日本大阪 CN2 GIA | 参考资料列出 2 核、1 GB 内存、20 GB SSD、500 GB 流量；价格以页面为准 | [查看日本大阪 CN2 GIA](https://bwh81.net/aff.php?aff=59244) |
| 日本东京 CN2 GIA | 参考资料列出 2 核、1 GB 内存、20 GB SSD、500 GB 流量；价格以页面为准 | [查看日本东京 CN2 GIA](https://bwh81.net/aff.php?aff=59244) |

Basic VPS 与 E-Commerce VPS 的配置及价格如表所示，可按所需资源和流量核对。SLA、香港和日本方案则应重点确认产品页面列出的具体条件；不要只凭系列名称推断配置或网络表现。

## 购买后首次连接

1. 从上表对应入口选择产品，核对配置、账期和订单信息并完成购买。
2. 登录账户，在 **Services → My Services** 找到 VPS，选择 **KiwiVM Control Panel** 进入管理面板。
3. 在 KiwiVM 主页面查找实例的 IP 地址和 **SSH Port**。端口可能不是默认的 22，应以面板显示为准。
4. 在终端或 SSH 客户端中连接：

   ```sh
   ssh root@你的IP地址 -p 你的SSH端口
   ```

   将示例中的地址与端口替换为该实例实际显示的信息。

如果本地 SSH 暂时无法使用，可在 KiwiVM 中查找 **Root shell - interactive** 作为浏览器内的管理入口。

## KiwiVM 中的常见管理操作

KiwiVM 提供若干 VPS 管理入口，具体选项以账户中当前页面为准：

- **重装系统**：重装会清除 VPS 上的数据。开始前先保存需要的数据，并确认所选系统。
- **快照**：可在面板查找快照相关功能；创建快照前后均应确认数据备份是否符合自己的需要。
- **查看流量**：在面板中查看实例流量信息，并结合套餐规则判断使用情况。
- **机房迁移**：在 **Migrate to different datacenter** 中查看可选机房及迁移说明，再决定是否操作。迁移资格和影响以面板提示为准；重要数据应预先备份。

## 常见问题

### SSH 为什么连不上默认的 22 端口？

每台 VPS 的 SSH 端口可能是随机分配的。请在 KiwiVM 主页面查找 **SSH Port**，并在连接命令中使用该端口。

### SSH 不通时还有其他管理入口吗？

可以登录 KiwiVM，查找 **Root shell - interactive**。同时检查实例 IP、SSH 端口和连接信息是否填写正确。

### 重装系统后数据还在吗？

不在。重装会清除数据；请先备份需要保留的内容，再确认是否继续。

## 更多套餐入口

- [查看搬瓦工当前在售套餐总览](https://bwh81.net/aff.php?aff=59244)
- [查看 CN2 GIA-E 套餐](https://bwh81.net/aff.php?aff=59244)
- [访问搬瓦工购买入口](https://bwh81.net/aff.php?aff=59244)
