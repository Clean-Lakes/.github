<div align="center">

# Clean Lakes

**面向 SRE 的开源运维工作台**

连接资源，协同排障，让执行有迹可循。

[Lake 仓库](https://github.com/Clean-Lakes/Lake) · [下载客户端](https://github.com/Clean-Lakes/Lake/releases) · [SRE 协作](https://github.com/Clean-Lakes/Lake/blob/master/docs/sre-collaboration.md)

</div>

<br>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Clean-Lakes/Lake/master/docs/images/lake-workbench-dark.jpg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Clean-Lakes/Lake/master/docs/images/lake-workbench-light.jpg">
  <img alt="Lake 工作台：在同一对话中查看调查员、执行员、验证员与协调者的协作结果" src="https://raw.githubusercontent.com/Clean-Lakes/Lake/master/docs/images/lake-workbench-light.jpg" width="1440">
</picture>

<br>

## 一座能查清来龙去脉的湖

名字不是装饰。Lake 的每一层都对应系统里真实存在的东西——从界面到协作，再到记录。

<table>
<tr>
<td width="130" valign="top"><b>表层 · 交互</b></td>
<td><b>工作台</b><br>
资源、会话与终端同屏。按项目组织主机、数据库、Redis 和 Docker，把资源、对话和终端放在一起。</td>
</tr>
<tr>
<td width="130" valign="top"><b>中层 · 协作</b></td>
<td><b>四位专员</b><br>
协调者建立与修订 Plan；调查员只读取证；执行员提交具体操作及影响；验证员重新采样验收目标。角色只在实际接手后发言。</td>
</tr>
<tr>
<td width="130" valign="top"><b>深层 · 记录</b></td>
<td><b>湖志</b><br>
命令只记哈希，证据原文以私有权限保存。从工具调用到操作确认，再到执行记录与证据，随时查看，也能人工接管。</td>
</tr>
</table>

<br>

## 仓库

| 仓库 | 说明 | 语言 |
|---|---|---|
| [**Lake**](https://github.com/Clean-Lakes/Lake) | 面向 SRE 的 AI 运维工作台 | Go · Apache-2.0 |
| [**magpie-agent-lake**](https://github.com/Clean-Lakes/magpie-agent-lake) | 在 Magpie 的 Agent 页面为 Lake 选择模型，通过 Magpie 网关使用所选模型 | JavaScript · Apache-2.0 |

<br>

## 设计取向

**过程优先于结论。** 工具成功不等于业务恢复。没有探针或证据不完整时，Lake 保持“无法确认”，而不是给出乐观判断。

**执行留下痕迹。** Shell 等不透明操作在派发前写入持久记录；结果不确定的已派发写操作不会自动重放。

**隔离是默认值。** 开发与正式版的数据和凭据互不相通；子专员继承父会话当前授权，父会话收紧权限后同步收紧。

<br>

<div align="center">
<sub>macOS Apple Silicon · Windows x86_64 · Apache-2.0</sub>
</div>
