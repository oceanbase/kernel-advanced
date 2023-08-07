# OceanBase 数据库开发者进阶教程

欢迎访问 OceanBase 数据库开发者进阶教程，您可以在本仓库中查看开发者进阶教程的文档。本文简单为您介绍开发者进阶教程各章节包含的内容以及如何贡献文档。

* 文档介绍

* 贡献文档

## 文档介绍

开发者进阶教程共分为七个章节，从 OceanBase 数据库简介、开发环境搭建、存储、SQL 引擎、事务、内存管理、测试等几个方面介绍 OceanBase 数据库，各章节内容如下。

### 第 1 章：OceanBase 数据库系统简介

本章简单介绍 OceanBase 数据库的发展历程、整体架构及其代码的目录结构，以便大家更深入的了解 OceanBase，主要包含如下内容。

* [1.1 了解 OceanBase 数据库](zh-CN/1.introduction-to-oceanbase-database/2.understand-oceanbase-database.md)：介绍 OceanBase 数据库的几大特性，包括扩展性、高可用、多租户、高性能、低成本等。

* [1.2 OceanBase 数据库的发展历程](zh-CN/1.introduction-to-oceanbase-database/3.development-history-of-oceanbase-database.md)：介绍自 2010 年以来 OceanBase 数据库的发展历程。

* [1.3 OceanBase 数据库整体架构](zh-CN/1.introduction-to-oceanbase-database/4.overall-architecture-of-oceanbase-database.md)：介绍 OceanBase 数据库的整体架构，

* [1.4 OceanBase 数据库目录结构](zh-CN/1.introduction-to-oceanbase-database/5.directory-structure.md)：介绍 OceanBase 数据库代码的整体架构和模块构成，以及各模块的作用。

### 第 2 章：OceanBase 开发环境搭建

本章介绍如何搭建 OceanBase 数据库研发环境，帮助大家快速上手内核开发，主要包含如下内容。

* [2.1 如何编译 OceanBase 源码](zh-CN/2.construction-of-oceanbase-development-environment/2.how-to-compile-oceanbase-source-code.md)：介绍如何编译 OceanBase 数据库源码。

* [2.2 如何使用 ccls 设置 IDE](zh-CN/2.construction-of-oceanbase-development-environment/3.how-to-set-the-ide-with-ccls.md)：介绍如何使用 ccls 设置 IDE。

* [2.3 如何 debug OceanBase](zh-CN/2.construction-of-oceanbase-development-environment/5.how-to-debug-oceanbase.md)：介绍如何 debug OceanBase 数据库。

* [2.4 如何运行测试](zh-CN/2.construction-of-oceanbase-development-environment/6.how-to-run-tests.md)：介绍如何对 OceanBase 数据库运行单元测试和 MysqlTest。

* [2.5 如何为 OceanBase 贡献源代码](zh-CN/2.construction-of-oceanbase-development-environment/7.how-to-contribute-to-oceanbase.md)：介绍为 OceanBase 数据库贡献源代码的流程。

* [2.6 课后实践](zh-CN/2.construction-of-oceanbase-development-environment/8.practical-exercises.md)：根据本章内容给出相关题目供大家练习。

### 第 3 章：OceanBase 存储引擎

本章介绍 OceanBase 数据库的存储结构和 Compaction 策略，以及数据的写入和查询流程，主要包含如下内容。

* [3.1 LSM-Tree 介绍](zh-CN/3.oceanbase-storage-engine/2.lsm-tree.md)：介绍 LSM-Tree 概念，以及为什么 OceanBase 选择了 LSM-Tree。

* [3.2 Compaction 策略介绍](zh-CN/3.oceanbase-storage-engine/3.comlaction.md)：介绍几种常用的 Compaction 策略，并对这些策略的设定、优势和劣势进行比较。

* [3.3 OceanBase 的 Compaction 设计](zh-CN/3.oceanbase-storage-engine/4.compaction-in-oceanbase.md)：介绍 OceanBase 数据库中的 Compaction 设计，包括 Compaction 类型和 Compaction 算法。

* [3.4 存储格式介绍](zh-CN/3.oceanbase-storage-engine/5.introduction-to-storage-format.md)：介绍 OceanBase 数据库的存储格式，包括存储分层结构、内存数据格式和磁盘文件格式。

* [3.5 查询过程介绍](zh-CN/3.oceanbase-storage-engine/6.introduction-to-query-process.md)：介绍 OceanBase 数据库查询过程，包括主表查询和索引回表查询。

* [3.6 课后实践](zh-CN/3.oceanbase-storage-engine/7.practical-exercises.md)：根据本章内容给出相关题目供大家练习。

### 第 4 章：OceanBase SQL 引擎

本章介绍 SQL 引擎优化器的作用、OceanBase 数据库中查询改写和查询优化框架及细节、OceanBase 数据库中 SQL 执行引擎的相关设计，主要包含如下内容。

* [4.1 查询优化器简介](zh-CN/4.oceanbase-sql-engine/2.introduction-to-query-optimizer.md)：介绍业界最常用的两个优化器框架：System-R 框架和 Cascade 框架。

* [4.2 查询改写](zh-CN/4.oceanbase-sql-engine/3.query-rewrite.md)：介绍查询改写相关概念，包括为什么要改写、查询改写的挑战以及查询改写时的有效性判断。

* [4.3 查询优化](zh-CN/4.oceanbase-sql-engine/4.query-optimization.md)：优化过程简单来讲就是枚举所有等价的执行计划，对于每一个执行计划，优化器利用统计信息和代价模型计算执行计划的代价，之后从中选择代价最小的计划。本文详细介绍如何进行计划枚举。

* [4.4 基表访问路径选择策略](zh-CN/4.oceanbase-sql-engine/5.base-table-access-path.md)：介绍基表访问路径选择策略，并详细介绍 skyline 剪枝这一优化策略。

* [4.5 执行引擎简介](zh-CN/4.oceanbase-sql-engine/7.introduction-to-execution-engine.md)：介绍 OceanBase 数据库执行引擎的作用以及发展历程。

* [4.6 向量化执行](zh-CN/4.oceanbase-sql-engine/8.vectorization-execution.md)：介绍在第三代执行引擎中引入向量化执行后的优点，以及 OceanBase 数据库中向量化执行的实现。

* [4.7 并行执行](zh-CN/4.oceanbase-sql-engine/9.parallel-execution.md)：介绍并行执行的实现和调度，以及数据重分布的类别。

* [4.8 执行模式](zh-CN/4.oceanbase-sql-engine/10.execution-mode.md)：介绍 OceanBase 数据库的执行模式，包括本地执行、远程执行以及 DAS（Data Access Service）执行。

* [4.9 课后实践](zh-CN/4.oceanbase-sql-engine/11.homework.md)：根据本章内容给出相关题目供大家练习。

### 第 5 章：OceanBase 事务引擎

本章介绍 OceanBase 数据库有关事务执行和事务提交的相关内容，主要包含如下内容。

* [5.1 事务执行](zh-CN/5.transaction-engine/2.transaction-execution.md)：介绍 OceanBase 数据库中事务执行的相关概念和 Query 执行流程。

* [5.2 并发控制](zh-CN/5.transaction-engine/3.concurrency-control.md)：介绍 OceanBase 数据库并发控制的相关信息，包括快照管理、索引结构、读写并发、写读并发以及写写并发。

* [5.3 事务提交](zh-CN/5.transaction-engine/4.transaction-commit.md)：介绍 OceanBase 数据库的事务提交流程。

* [5.4 事务优化](zh-CN/5.transaction-engine/5.transaction-optimization.md)：介绍 OceanBase 数据库各个时期的事务优化思路。

* [5.5 课后实践](zh-CN/5.transaction-engine/6.homework.md)：根据本章内容给出相关题目供大家练习。

### 第 6 章：OceanBase 内存管理框架与线程模型

本章介绍 OceanBase 数据库的内存管理框架以及线程模型，主要包含如下内容。

* [6.1 内存管理框架](zh-CN//6.memory-frame/2.ob-memry-frame.md)：通过性能、利用率和诊断性三个方面来介绍 OceanBase 数据库内存管理框架。

* [6.2 内存安全问题在 OceanBase 的解决方案](zh-CN//6.memory-frame/3.ob-memory-solution.md)：介绍 OceanBase 自研的快速发现漏洞并精准定位的框架——Sanity 框架，以及 Sanity 框架是怎么实现的。

* [6.3 SQL 执行过程](zh-CN//6.memory-frame/4.sql-execution-process.md)：介绍 OceanBase 数据库中一条 SQL 请求执行的完整过程。

* [6.4 课后实践](zh-CN//6.memory-frame/5.homework.md)：根据本章内容给出相关题目供大家练习。

### 第 7 章：OceanBase 开源质量体系

本章介绍 OceanBase 数据库开源版本的质量体系，主要包含如下内容。

* [7.1 OceanBase 研发测试流程](zh-CN/7.quality-system/2.test-process.md)：介绍 OceanBase 数据库的研发测试流程。

* [7.2 OceanBase 质量体系和测试工具](zh-CN/7.quality-system/3.quality-system.md)：介绍 OceanBase 数据库的质量体系以及常用的测试工具，包括 SQL 测试的工具 MysqlTest 和 RQG、正确性测试、性能测试、稳定性测试以及兼容性测试。

* [7.3 如何参与 OceanBase 测试](zh-CN/7.quality-system/4.participate-test.md)：介绍参与 OceanBase 数据库测试的几个途径。

## 贡献文档

### 开始之前

感谢您对 OceanBase 数据库文档的贡献兴趣。为厘清就个人或实体贡献内容而授予的知识产权许可，我们必须对每位贡献者签署的贡献者许可协议（Contributor Licence Agreement，简称 CLA）进行归档，以证明就 CLA 达成的一致。点击 [OceaBase CLA](https://cla-assistant.io/oceanbase/oceanbase?pullRequest=108)，点击 **Sign in with GitHub to agree** 按钮签署协议。

### 贡献指南

您可以按照以下步骤提交 Pull Request（简称 PR）：

#### 步骤 1：Fork 项目仓库

1. 访问 OceanBase 数据库开发者进阶教程文档的 [GitHub 地址](https://github.com/oceanbase/kernel-advanced)。

2. 点击 Fork 按钮创建远程分支。

#### 步骤 2：克隆分支到本地

1. 定义工作目录。

   ```shell
   # 定义工作目录
   working_dir=$HOME/Workspace
   ```

2. 配置 GitHub 用户名。

   ```shell
   user={GitHub账户名}
   ```

3. 克隆代码。

   ```shell
   # 克隆代码
   mkdir -p $working_dir
   cd $working_dir
   git clone git@github.com:$user/kernel-advanced.git
   # 或: git clone https://github.com/$user/kernel-advanced.git

   # 添加上游分支
   cd $working_dir/kernel-advanced
   git remote add upstream git@github.com:oceanbase/kernel-advanced.git
   # 或: git remote add upstream https://github.com/oceanbase/kernel-advanced.git

   # 为上游分支设置 no_push
   git remote set-url --push upstream no_push

   # 确认远程分支有效
   git remote -v
   ```

#### 步骤 3：创建新分支

1. 更新本地分支。

   ```shell
   cd $working_dir/kernel-advanced
   git fetch upstream
   git checkout $branch
   git rebase upstream/$branch
   ```

2. 基于本地 $branch 分支创建新分支。

   ```shell
   git checkout -b new-branch-name
   ```

#### 步骤 4：修改/添加/删除文档

在 `new-branch-name` 上修改文档并保存更改。

#### 步骤 5：提交更改

```shell
# 检查本地文件状态
git status

# 添加您希望提交的文件
# 如果您希望提交所有更改，直接使用 `git add .`
git add <file> ...
git commit -m "commit-message: update the xx"
```

#### 步骤 6：保持开发分支与上游分支同步

```shell
# 在开发分支执行以下操作
git fetch upstream
git rebase upstream/branch
```

#### 步骤 7：推送更改至远程分支

```shell
# 在开发分支执行以下操作
git push -u origin new-branch-name
```

#### 步骤 8：创建 PR

1. 访问您 Fork 的仓库。

2. 单击 `new-branch-name` 分支旁的 `Compare & pull request` 按钮。

以上就是参与 OceanBase 数据库文档共建的步骤，如果在此过程中遇到任何问题，可以加入我们唯一官网钉钉群：41203246，与社区热心的技术大神、热情的贡献者、经验丰富的技术专家一起交流、探讨问题。
